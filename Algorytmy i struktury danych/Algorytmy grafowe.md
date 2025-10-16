
## Podstawowe algorytmy + reprezentacje
### Definicje

**Przeszukiwanie grafu** - systematyczne przechodzenie wzdłuż jego krawędzi w celu odwiedzenia wszystkich wierzchołków.


### Reprezentacja grafów
![[diagram-20250429 (1).png]]
**Reprezentacja listowa/tablicowa** - po prostu który wierzchołek z którymi się łączy

$$\begin{gathered}
1\to [2,5]\\
2\to [1,5,3,4]\\
3\to [2,4]\\
4\to [2,5,3]\\
5\to [4,1,2]
\end{gathered}$$

**Reprezentacja macierzowa** - macierz połączeń 0/1

$$\begin{gathered}
\begin{vmatrix}
\begin{array}{c|cccc}
&1&2&3&4&5\\
1&0&1&0&0&1\\
2&1&0&1&1&1\\
3&0&1&0&1&0\\
4&0&1&1&0&1\\
5&1&1&0&1&0
\end{array}
\end{vmatrix}
\end{gathered}$$

**Które wybrać**?

Reprezentacja macierzowa wykrzacza się przy grafach z dużą ilością wierzchołków, w szczególności przy grafach rzadkich (mających dużo wierzchołków a mało krawędzi).
Jednakże gdy istnieje potrzeba *szybkiego* sprawdzenia czy istnieje krawędź bezpośrednio łącząca dane dwa wierzchołki być może lepiej użyć macierzowej. (bo w listowej należy wykonać operacje *in* dla tablicowej lub przejść przez liste dla listowej)

Zatem wszystko sprowadza się do pamięci i czasu działania algorytmu. Można wszystko uprościć do tego że macierzowa = więcej pamięci lecz szybszy (w teorii) algorytm a listowa mniej pamięci a wolniejszy algorytm. Najlepiej po prostu sprawdzić oba rozwiązania co szybciej hula dla danego zadania.

Dla list sąsiedztwa (reprezentacja tablicowa) złożoność pamięciowa jest liniowa a dla macierzowej kwadratowa.

Grafy skierowane:
- listy sąsiedztwa - $O(E)=E$
- macierzowa - $O(V)=V^2$

Grafy nieskierowane:
- listy sąsiedztwa - $O(E)=2\cdot E$
- macierzowa - $O(V)=V^2$

W szczególnych przypadkach np. w *grafach pełnych* to sie sobie równa, ale tak jak już było wspomniane - przy dużej ilości krawędzi lepiej macierzowa.

---
### Przeszukiwanie wszerz i wgłąb (BFS/DFS)
![[diagram-20250429 (2).png]]
**BFS:**

```python 
graf = {
1: [2,3,4],
2:[5],
3: [6],
4: [7],
5: [8],
6: [9],
7: [10]
} # używam słownika ale równie dobrze można zrobić tablice kwadratowe albo faktycznie listy

def bfs(root, graf): # root - początkowy wierzchołek
	visited = []
	queue = [root]
	while queue:
		current = queue.pop(0) # to kosztowna operacja w pythonie może lepiej po prostu pomijać usuwanie i sprawdzanie czy nie w kolejce
		visited.append(current)
		if current in graph:
			queue.extend(filter(lambda x: x not in visited and x not in queue, graph[current]))
		print(current)
	print("Zakończono przeszukiwanie")

```

Wynik dla powyższego grafu 1,2,3,4,5,6,7,8,9,10

**DFS:**

```python 
graf = {
1: [2,3,4],
2:[5],
3: [6],
4: [7],
5: [8],
6: [9],
7: [10]
}

def dfs(root, graph):
	visited = []
	stack = [root]
	while stack:
		current = stack.pop() # domyślnie to od końca
		visited.append(current)
		if current in graph:
			stack.extend(filter(lambda x: x not in visited and x not in stack, graph[current]))
		print(current)
	print("Zakończono przeszukiwanie")
```

Wynik dla powyższego grafu: 1,4,7,10,3,6,8,2,5,8

Można te algorytmy użyć do liczenia najkrótszych ścieżek dla każdego dziecka. Tylko tam już by trzeba było zastosować inne podejście z forami a nie z tym extend filter itd.

---
## Algorytmy znajdowania najkrótszych tras/odległości

### Algorytm Dijkstra

**Algorytm Dijkstry służy do znajdowania odległości najkrótszych ścieżek z danego węzła do wszystkich innych węzłów w grafie**

**Algorytm ten można odpowiednio przerobić żeby przerywał się w momencie kiedy znajdzie odpowiedni węzeł na którym nam zależy - dostaniemy algorytm który znajduje długość najkrótszej ścieżki pomiędzy dwoma wybranymi węzłami**

**Możemy również sprawić żeby nie tylko zwracał długości najkrótszych ścieżek ale również trasy - zrobimy to poprzez zbudowanie tablicy "parentów" dla każdego węzła - dzięki temu będziemy w stanie odtworzyć trasy**

##### Kolejka priorytetowa

**Najlepiej rozpatrywać najkrótsze aktualnie krawędzie co pozwoli nam szybciej sprawdzić wszystkie ścieżki** (Sprawdzanie krawędzi dłuższych niż najkrótsza z tych jakie mamy do dyspozycji jest bez sensu i jest nie optymalne)

**Potrzebujemy zatem przechowywać najmniejszą krawędź tak żeby zawsze była dostępna w odpowiednim miejscu a pozostałe w miare możliwości rosnąco** (Ciśnie się zatem kopiec min)

**Dla przypomnienia:**

```python title:priority_queue.py
class PriorityQueue:
    def parent(self,n):
        return (n-1)//2
    def left(self,n):
        return n*2+1
    def right(self,n):
        return n*2+2
    def __init__(self,key=lambda x: x,min_max="min"):
        self.heap=[]
        self.heap_size=0
        self.min_max=min_max
        self.key=key
    def heapify_max(self,start,end=None):
        largest=start
        if end is None:
            if self.left(start)<self.heap_size and self.key(self.heap[self.left(start)])>self.key(self.heap[largest]):
                largest=self.left(start)
            if self.right(start)<self.heap_size and self.key(self.heap[self.right(start)])>self.key(self.heap[largest]):
                largest=self.right(start)
        else:
            if self.left(start)<end and self.key(self.heap[self.left(start)])>self.key(self.heap[largest]):
                largest=self.left(start)
            if self.right(start)<end and self.key(self.heap[self.right(start)])>self.key(self.heap[largest]):
                largest=self.right(start)
        if start!=largest:
            self.heap[largest],self.heap[start]=self.heap[start],self.heap[largest]
            self.heapify_max(largest,end)
    def heapify_min(self,start,end=None):
        smallest=start
        if end is None:
            if self.left(start)<self.heap_size and self.key(self.heap[self.left(start)])<self.key(self.heap[smallest]):
                smallest=self.left(start)
            if self.right(start)<self.heap_size and self.key(self.heap[self.right(start)])<self.key(self.heap[smallest]):
                smallest=self.right(start)
        else:
            if self.left(start)<end and self.key(self.heap[self.left(start)])<self.key(self.heap[smallest]):
                smallest=self.left(start)
            if self.right(start)<end and self.key(self.heap[self.right(start)])<self.key(self.heap[smallest]):
                smallest=self.right(start)
        if start!=smallest:
            self.heap[smallest],self.heap[start]=self.heap[start],self.heap[smallest]
            self.heapify_min(smallest,end)
    def append(self,key):
        self.heap.append(key)
        self.heap_size+=1
        n=self.heap_size-1
        if self.min_max=="min":
            while self.parent(n)>=0 and self.heap[self.parent(n)]> self.heap[n]:
                self.heap[self.parent(n)],self.heap[n]=self.heap[n],self.heap[self.parent(n)]
                n=self.parent(n)
        else:
            while self.parent(n)>=0 and self.heap[self.parent(n)]<self.heap[n]:
                self.heap[self.parent(n)],self.heap[n]=self.heap[n],self.heap[self.parent(n)]
                n=self.parent(n)

    def remove(self):
        c=self.heap[0]
        self.heap[0],self.heap[self.heap_size-1]=self.heap[self.heap_size-1],self.heap[0]
        if self.min_max=="max":
            self.heapify_max(0,self.heap_size-1)
        else:
            self.heapify_min(0,self.heap_size-1)
        self.heap.pop()
        self.heap_size-=1
        return c
    def __bool__(self):
        return self.heap_size>0
```

##### Różne wersje:

###### Najbardziej basic ale też troche wolniejsza (choć nadal złożoność $O(n\cdot \log{n})$)

```python title:dijkstra_wolniejsza.py
# zakładając że korzystamy z jakiejś formy adjacency list czyli 1:[2,3,4] itd
def dijkstra(arr,start=0):
    n=len(G)
    inf=float('inf')
    weights=[inf]*n
    pq=PriorityQueue(lambda x: x[0], "min")
    pq.append((0,start))
    weights[start]=0
    while pq:
        _,u=pq.remove()
        for v,weight in G[u]:
            if  weights[u]+weight < weights[v]:
                weights[v]=weights[u]+weight
                pq.append((weights[v],v))
    return weights
```

Czyli algorytm działa w sposób następujący:
1. Tworzymy tablice odległości od wybranego węzła (startu) do wszystkich innych węzłów i jako wartość domyślną nadajemy nieskończoność.
2. Tworzymy kolejke priorytetową która za priorytet uznaje jak najmniejszą odległość.
3. Do kolejki dodajemy (0,start)
4. Póki coś jest w kolejce zdejmujemy z niej kolejne elementy.
5. Dla każdego sąsiada danego węzła patrzymy czy nowa możliwa odległość jest mniejsza niż wpisana w tablice.
	1. Jeśli tak to podmieniamy odległość w tablicy odległości
	2. I dodajemy nowo przetworzony węzeł do kolejki.
6. Gdy pętla skończy działać zwracamy tablice wag.

###### Lepsza wersja:

```python title:lepsza_dijkstra.py

def dijkstra(G, s):
    n = len(G)
    inf = float('inf')
    weights = [inf] * n
    
    to_relax = n
    pq = PriorityQueue()
    pq.put((0, s))

    while not pq.empty() and to_relax:
        min_w, u= pq.get()
        # Znajdziemy minimalną odległość jedynie raz więc poniższy kod uruchomi się jedynie raz.
        if min_w < weights[u]:
            weights[u] = min_w
            to_relax -= 1
            for v, weight in G[u]:
                if weights[v] == inf:
                    pq.put((weights[u] + weight, v))
                
    return weights
```

**Tutaj zauważamy że indukcyjnie następuje pewna własność:**

1. Zaczynając od startu i rozpatrując w kolejce najkrótszą odległość mamy pewność że wybrany sąsiad startu ma już dobrze zapisaną swoją odległość i nie należy go ponownie rozpatrywać.
2. Indukcyjnie lecimy także dla jego sąsiadów itd.

**Pozwoli nam to skrócić czas działania algorytmu choć dalej złożoność pozostanie taka sama**

**Zatem jak teraz powinien przebiegać algorytm?**

Różnice:
1. Mamy zmienną przechowującą liczbe wierzchołków do sprawdzenia (pozwoli to również przerwać program gdy sprawdzimy wszystkie wierzchołki)
2. Do kolejki dodajemy wierzchołki jedynie wtedy kiedy ich jeszcze nie sprawdziliśmy.

Jak działa algorytm?
1. Tworzymy tablice odległości, wypełniamy nieskończonościami.
2. Tworzymy zmienną wierzchołków do rozpatrzenia.
3. Tworzymy kolejke priorytetową i dodajemy (0,start)
4. Dopóki istnieje coś w kolejce i nie sprawdziliśmy wszystkich wierzchołków:
	1. Zdejmujemy z kolejki najmniejszą wartość.
	2. Zmiejszamy licznik wierzchołków do sprawdzenia.
	3. Dla każdego **nieodwiedzonego** sąsiada aktualnie sprawdzanego wierzchołka dodajemy go do kolejki. (to znaczy jedynie wtedy gdy odległość do niego nie wynosi infinity)
5. zwracamy odległości

**OD TERAZ NASTĘPNE WERSJE (Z DODATKAMI) BĘDĄ TWORZONE NA PODSTAWIE POWYŻSZEGO ALGORYTMU**
###### Dijkstra która pozwala na odtworzenie najkrótszej trasy:

**Przechowujemy również tablice rodziców - pozwala to następnie drugą funkcją przyjąć tą tablice i idąc od końca iść ciągle odpowiednią trasą by dojść do początku czyli naszego startu**

```python title:trasa_dijkstra.py

def dijkstra(G, s):
    n = len(G)
    inf = float('inf')
    weights = [inf] * n
    parents = [None]*n
    to_relax = n
    pq = PriorityQueue()
    pq.put((0, s, None)) # odległość, wierzchołek, jego rodzic

    while not pq.empty() and to_relax:
        min_w, u, parent= pq.get()
        # Znajdziemy minimalną odległość jedynie raz więc poniższy kod uruchomi się jedynie raz.
        if min_w < weights[u]:
            weights[u] = min_w
            parents[u] = parent
            to_relax -= 1
            for v, weight in G[u]:
                if weights[v] == inf:
                    pq.put((weights[u] + weight, v, u))
                
    return parents, weights
```

Zatem powyższa dijkstra nie tylko zwraca tablice najkrótszych odległości start-wierzchołek x, ale także tablice rodziców co pozwoli odtworzyć najkrótszą scieżke start-wierzchołek x dla każdego wierzchołka x:


```python title:route_from_parents.py
def route_from_parents(parents, start, end):
	node=end
	route=[end]
	while node!=start:
		route.append(parents[node])
		node=parents[node]
	route.append(start)
	return route[::-1]
```

###### Znalezienie jedynie najkrótszej ścieżki do wierzchołka na którym nam zależy (nie do wszystkich):


**sprawa ma sie prosto - przerywamy algorytm gdy znaleźliśmy to co chcieliśmy (korzystając z zauważonego wcześniej indukcyjnego patentu)**

```python title:dijkstra_only_to.py
def dijkstra(G, s, look_for):
    n = len(G)
    inf = float('inf')
    weights = [inf] * n
    parents = [None]*n
    to_relax = n
    pq = PriorityQueue()
    pq.put((0, s, None)) # odległość, wierzchołek, jego rodzic

    while not pq.empty() and to_relax:
        min_w, u, parent= pq.get()
        # Znajdziemy minimalną odległość jedynie raz więc poniższy kod uruchomi się jedynie raz.
        if min_w < weights[u]:
            weights[u] = min_w
            parents[u] = parent
            to_relax -= 1
            for v, weight in G[u]:
				if v==look_for:
					return weights[u]+weight
                if weights[v] == inf:
                    pq.put((weights[u] + weight, v, u))
                
    return None # w przypadku nie istnienia danej ścieżki
```

---
### Algorytm Bellmana-Forda

**Ten algorytm również służy do znajdowania najkrótszych ścieżek pomiędzy początkiem i wszystkimi innymi wierzchołkami - jednakże działa on również w przypadku krawędzi ujemnych**

**Ma złożoność gorszą od dijkstry wynoszącą $O(V\cdot E)$**

**Potrafi sprawdzić czy istnieje cykl ujemny w grafie**


```python title:bellman_ford.py
def bellman_ford(G: 'graph represented by adjacency lists', s: 'source'):
    n = len(G)
    inf = float('inf')
    weights = [inf] * n
    weights[s] = 0
    
    # Calculate shortest paths distances
    for _ in range(n):
        for u in range(n):
            for v, weight in G[u]:
                if weights[u] + weight < weights[v]:
                    weights[v] = weights[u] + weight
                
    # Look for negative cycles and replace distances
    # with a -infinity if a vertex is affected by
    # a negative cycle
    for _ in range(n):
        for u in range(n):
            for v, weight in G[u]:
                # If we still can relax a u vertex, there
                # must be a negative cycle
                if weights[u] + weight < weights[v]:
                    weights[v] = -inf
        
    return weights
```

**Przebieg działania:**
1. Inicjalizacja (stworzenie tablic odległości, przypisanie początkowi 0)
2. Wejście w pętle:
	1. Jest to pętla potrójna, najwyższa odpowiada za relaksacje tylekroć ile jest wierzchołków.
	2. Pętla niższa iteruje po tychże wierzchołkach.
	3. A najniższa po krawędziach aktualnego wierzchołka.
**Można zauważyć że skoro na początku każdy wierzchołek ma odległość nieskończoną a jedynie start ma zerową to pierwsza pętla uruchomi jedynie krawędzie wychodzące ze startu**
3. Jeżeli zachodzi warunek - badając krawędź że tą krawędzią da sie dotrzeć z wierzchołka A do wierzchołka B szybciej niż dotychczas to zapisujemy nową najkrótszą odległość.
4. uruchamiamy podobnną potrójną pętlą jednakże tym razem sprawdzając czy da sie zmniejszyć odległość jeszcze bardziej co sugeruje istnienie cyklu ujemnego - wtedy wierzchołkom które mogą skorzystać z tego cheata przypisujemy odległość ujemnie nieskończoną.

##### Wyznaczanie ścieżki:

**Podobnie jak w przypadku algorytmu dijkstry, jednakże tym razem jeżeli już wiemy że wierzchołek ma odległość ujemnie nieskończoną nie możemy wyznaczyć jednoznacznej ścieżki i zwracamy $None$**

```python title:bellman_ford_path.py
def bellman_ford(G: 'graph represented by adjacency lists', s: 'source'):
    n = len(G)
    inf = float('inf')
    weights = [inf] * n
    parents = [None] * n
    weights[s] = 0
    
    # Calculate shortest paths distances
    for _ in range(n):
        for u in range(n):
            for v, weight in G[u]:
                if weights[u] + weight < weights[v]:
                    weights[v] = weights[u] + weight
                    parents[v] = u
                
    # Look for negative cycles and replace distances
    # with a -infinity if a vertex is affected by
    # a negative cycle
    for _ in range(n):
        for u in range(n):
            for v, weight in G[u]:
                # If we still can relax a u vertex, there
                # must be a negative cycle
                if weights[u] + weight < weights[v]:
                    weights[v] = -inf
        
    return weights, parents
    
    
def get_shortest_path(G, s, t):
    weights, parents = bellman_ford(G, s)
    if weights[t] == float('-inf'):
        # When there is a negative cycle, there is no shortest path (this is endless)
        return None
    
    path = []
    while t != s:
        path.append(t)
        t = parents[t]
    path.append(s)
    
    return path[::-1]
```

**Ciekawostka - generowanie ścieżek nawet z ujemnym cyklem**

```python title:bellman_ford_negative_cycle.py

"""
Ulepszona wersja funkcji, która pozwala na odtworzenie ścieżek, na których występuje
ujemny cykl. Wówczas waga takiej ścieżki zawsze wynosi -inf, więc bierzemy dowolną
o tej wadze.
"""
def get_shortest_path_with_cycle(G, parents, s, t):
    # If no path exists
    if parents[t] is None: return []
    it = 0
    n = len(parents)
    iters = [-1] * n
    seq = []
    
    last_u = None
    
    while t is not None:
        # Check if we visited the same vertex again
        # (If we have a negative cycle)
        if iters[t] >= 0:
            cycle = tuple(seq[i] for i in range(len(seq) - 1, iters[t] - 1, -1))
            last_u = cycle[0]
            for i in range(len(seq) - iters[t]): seq.pop()
            seq.append(cycle)
            break
        seq.append(t)
        iters[t] = it
        t = parents[t]
        it += 1
        
    # If there was a cycle
    if last_u is not None:
        new_parents = [None] * n

        def dfs(u):
            if u == last_u: return
            for v, _ in G[u]:
                if new_parents[v] is None:
                    new_parents[v] = u
                    dfs(v)

        new_parents[s] = s
        dfs(s)
        new_parents[s] = None
        
        u = new_parents[last_u]
        while u is not None:
            seq.append(u)
            u = new_parents[u]
    
    seq.reverse()
    return seq
```

---
### Floyd Marshall (to co sam wymyśliłeś na kolosie)

```python title:floyd_marshall.py

def floyd_warshall(G: 'graph represented by adjacency matrix'):
    n = len(G)
    inf = float('inf')
    
    # Create a copy of a graph as we have to have lengths
    # of edges stored at the beginning of an algorithm
    W = copy.deepcopy(G)
    
    for t in range(n):
        for i in range(n):
            for j in range(n):
                if W[i][t] + W[t][j] < W[i][j]:
                    W[i][j] = W[i][t] + W[t][j]
                
    return W
    
def shortest_path(W: "array of path's weights", s: 'source', t: 'target'):
    return W[s][t]
```

**Ideaa taka jak powyżej: jeżeli z A do B oraz z B do C jest trasa krótsza niż A do C to zapisujemy nową najkrótszą odległość**

**Na początku nie istniejące krawędzie są oznaczane jako $inf$ np.**

**Można tego również użyć do wyznaczenia np czy w ogóle da sie gdzieś dotrzeć**

##### Wykrywanie ujemnych cykli - podobnie jak w Bellman Ford uruchamiamy drugi raz i g.

```python title:better_floyd_warshall.py
def floyd_warshall(G: 'graph represented by adjacency matrix'):
    n = len(G)
    inf = float('inf')
    
    # Create a copy of a graph as we have to have lengths
    # of edges stored at the beginning of an algorithm
    W = copy.deepcopy(G)
    
    for t in range(n):
        for i in range(n):
            for j in range(n):
                if W[i][t] + W[t][j] < W[i][j]:
                    W[i][j] = W[i][t] + W[t][j]
                    
    # Detect negative cycles (the same approach as in the
    # Bellman-Ford's algoritm)
    for t in range(n):
        for i in range(n):
            for j in range(n):
                if W[i][t] + W[t][j] < W[i][j]:
                    W[i][j] = -inf
                
    return W
```


**Z odtwarzaniem trasy:**

```python title:bellman_path.py

def floyd_warshall(G: 'graph represented by adjacency matrix'):
    n = len(G)
    inf = float('inf')
    
    # Create a copy of a graph as we have to have lengths
    # of edges stored at the beginning of an algorithm
    W = copy.deepcopy(G)
    
    # B[i][j] - a vetrex on the shortest path from i to j
    # for which a path has the lowest total weight (length)
    B = [[None] * n for _ in range(n)]
    
    for t in range(n):
        for i in range(n):
            for j in range(n):
                if W[i][t] + W[t][j] < W[i][j]:
                    W[i][j] = W[i][t] + W[t][j]
                    B[i][j] = t
                    
    # Detect negative cycles (the same approach as in the
    # Bellman-Ford's algoritm)
    for t in range(n):
        for i in range(n):
            for j in range(n):
                if W[i][t] + W[t][j] < W[i][j]:
                    W[i][j] = -inf
                    B[i][j] = -1
                
    return W, B


def get_shortest_path(B: 'array of vertices between two vertices on a path', s: 'source', t: 'target'):
    # Check if there is a path
    if B[s][t] is None: return None
    # Check if we have a negative cycle (there is no shortest path)
    if B[s][t] < 0: return []
    
    path = []
    
    # Recursively restore a path
    def recur(i, j):
        if B[i][j] is None:
            return path.append(i)
        recur(i, B[i][j])
        recur(B[i][j], j)
    
    recur(s, t)
    path.append(t)
    
    return path
    
```

---
## Algorytmy właściwości np. sprawdzanie eulerowości
### Sortowanie topologiczne DAG 

**Jedna z najprostszych rzeczy w grafach**

Sortowanie topologiczne DAG można sobie **wyobrazić** w ten sposób że sortujemy zadania jakie mamy do zrobienia w ten sposób żebyśmy mogli każde wykonać, zakładając że do wykonania pewnych par zadań konieczne jest wykonanie wcześniejszego zadania. To znaczy:

**Żeby sie ubrać:**

- czapke możemy ubrać w dowolnej kolejności
- żeby ubrać bluze najpierw należy ubrać koszulke
- koszulke należy ubrać przed bluzą
- spodnie przed paskiem
- pasek po spodniach
- skarpetki po spodniach (takie widzimisie żeby nie było za prosto)
- skarpetki przed butami
- buty po skarpetkach

Należy zatem sobie rozrysować ten graf i posortować topologicznie żeby dostać **jakikolwiek realny schemat** ubioru. Będzie on jeden z możliwych, niekoniecznie jedyny. Nam zależy jedynie na tym żeby zadania sie nie wykluczały.

![[diagram-20250825 (1).png]]
Teraz mając taki graf jak wyżej jasno widać co należy zrobić najpierw.

Jest to prosty przykład na którym jedynie wizualizuje po co jest to sortowanie z racji jego prostoty nie przedstawie na nim tego algorytmu. Zatem przedstawie kolejny (bardziej skomplikowany):

![[Pasted image 20250825003229.png]]

Na górze graf, na dole przykład poprawnej kolejności wykonywania zadań.

Algorytm sortowania topologicznego działa w ten sposób że uruchamiamy DFS i kolejno zapisujemy kolejne rzeczy do tablicy od końca. (Ewentualnie możemy również dodawać i odwrócić tablice).

```python title:DAG_sort.py
def topological_sort(G):
    n = len(G)
    visited = [False] * n
    result = [None] * n
    idx = n
    
    def dfs(u):
        visited[u] = True
        for v in G[u]:
            if not visited[v]:
                dfs(v)
        nonlocal idx
        idx -= 1
        result[idx] = u
        
    for u in range(n):
        if not visited[u]:
            dfs(u)
            
    return result
```

Zatem najpierw uruchamiamy dfs i dopiero docierając do końca możemy zapisać dany wierzchołek na tablicy. 

---
### Cykl Eulera 

**Dla przypomnienia graf ma cykl Eulera jeżeli istnieje w nim cykl przechodzący przez każdą z krawędzi dokładnie raz**

**Tw. graf ma cykl Eulera jeżeli jest spójny i każdy wierzchołek ma stopień parzysty $\Leftrightarrow$**


##### Bez sprawdzania czy graf jest Eulerowski:

**Dla macierzowej reprezentacji grafu:**

Jeżeli graf nie jest Eulerowski wynik będzie błędny, ale na razie chcemy jedynie przedstawić idee które za tym idą.

```python title:euler_cycle.py

def euler_cycle(G):
	n=len(G)
	result=[]
	def dfs(i):
		for j in range(n):
			if G[i][j]==1:
				G[i][j]=G[j][i]=-1 # zakładając że nie skierowany
				dfs(j)
		result.append(i)
	dfs(0)
	for i in range(n):
		for j in range(n):
			G[i][j]=abs(G[i][j])
	return result	
```


**Dla listowej:**

```python title:list_euler_cycle.py

def euler_cycle(G: 'graph represented using adjacency lists'):
    n = len(G)
    result = []
    visited = [[False] * n for _ in range(n)]
            
    def dfs(u):
        for v in G[u]:
            if not visited[u][v]:
                visited[u][v] = visited[v][u] = True
                dfs(v)
        result.append(u)
        
    dfs(0)
            
    return result
```


##### Ze sprawdzeniem czy napewno Eulerowski:

```python title:czy_spojny.py

def is_consistent(G: 'graph represented using adjacency matrix'):
    n = len(G)
    visited = [False] * n
    
    def dfs(i):
        visited[i] = True
        for j in range(n):
            if G[i][j] and not visited[j]:
                dfs(j)
                
    dfs(0)
    return all(visited)
```

```python title:euler_cycle.py

def euler_cycle(G: 'graph represented using adjacency matrix'):
    if not is_consistent(G): return []
    n = len(G)
    result = []
    
    def dfs(i):
        deg = 0
        for j in range(n):
            # If has an edge no matter if visited or not
            if G[i][j]:
                deg += 1
                # Is still not visited
                if G[i][j] == 1:
                    # Remove an edge (by replacing 1 with -1)
                    G[i][j] = G[j][i] = -1  # I assume the graph is not directed
                    if not dfs(j): return False
        # If a vertex has odd degree, return False as a graph isn't euleran
        if deg % 2: return False
        result.append(i)
        return True
        
    # Run dfs algorithm to search for the euler cycle
    # (if a graph isn't eulerian, return empty array)
    if not dfs(0):
        result = []
        
    # Restore original values of edges (replace -1 with 1)
    for i in range(n):
        for j in range(n):
            G[i][j] = abs(G[i][j])
            
    return result
```


##### Zatem podsumowując:

###### Czy spójny:

```python title:czy_spojny.py
def is_consistent(G: 'graph represented using adjacency matrix'):
    n = len(G)
    visited = [False] * n
    
    def dfs(i):
        visited[i] = True
        for j in range(n):
            if G[i][j] and not visited[j]:
                dfs(j)
                
    dfs(0)
    return all(visited)
```

###### Czy ma cykl Eulera:

```python title:has_euler_cycle.py
def has_euler_cycle(G: 'graph represented using adjacency matrix'):
    if not is_consistent(G): return False
    n = len(G)
    # Check for each vertex if its degree is even
    for i in range(n):
        deg = 0
        for j in range(n):
            if G[i][j]: deg += 1
        # If a degree of a vertex is odd, return False as a graph cannot have euler cycle
        if deg % 2:
            return False
    return True
```

###### Czy ma ścieżke Eulera, jeśli tak to gdzie sie ona zaczyna?

```python title:euler_path.py
def has_euler_path(G: 'graph represented using adjacency matrix'):
    if not is_consistent(G): return False, -1
    n = len(G)
    odd_count = 0
    odd_vertex = None
    # Check for each vertex if its degree is even
    for i in range(n):
        deg = 0
        for j in range(n):
            if G[i][j]: deg += 1
        # If a degree of a vertex is odd, increment a number of odd degree vertices
        # and check if we exceeded the maximum number of odd degree vertices
        if deg % 2:
            odd_vertex = i
            odd_count += 1
            if odd_count > 2:
                return False, -1
    return (True, odd_vertex) if odd_count == 2 else (False, -1)
```

###### Wypisz cykl Eulera:

```python title:euler_cycle.py

def euler_cycle(G: 'graph represented using adjacency matrix'):
    # Check if a graph has an euler cycle
    if not has_euler_cycle(G): return []
    
    n = len(G)
    result = []
    
    def dfs(i):
        for j in range(n):
            # Is still not visited
            if G[i][j] == 1:
                # Remove an edge (by replacing 1 with -1)
                G[i][j] = G[j][i] = -1  # I assume the graph is not directed
                dfs(j)
        result.append(i)
        
    # Run dfs algorithm to search for the euler cycle
    dfs(0)
        
    # Restore original values of edges (replace -1 with 1)
    for i in range(n):
        for j in range(n):
            G[i][j] = abs(G[i][j])
            
    return result

```

###### Wypisz ścieżke Eulera:

```python title:euler_path.py
# Algorytm identyczny do tego, który znajduje cykl
def euler_path(G: 'graph represented using adjacency matrix'):
    has_path, begin_i = has_euler_path(G)
    if not has_path: return []
    
    n = len(G)
    result = []
    
    def dfs(i):
        for j in range(n):
            # Is still not visited
            if G[i][j] == 1:
                # Remove an edge (by replacing 1 with -1)
                G[i][j] = G[j][i] = -1  # I assume the graph is not directed
                dfs(j)
        result.append(i)
        
    # Run dfs algorithm to search for the euler path
    # (We must start from a vertex of odd degree)
    dfs(begin_i)
        
    # Restore original values of edges (replace -1 with 1)
    for i in range(n):
        for j in range(n):
            G[i][j] = abs(G[i][j])
            
    return result
```


---
### Minimalne drzewa spinające

#### Kruskal

```python title:kruskal.py

class Node:
    def __init__(self, id_):
        self.id = id_
        self.parent = self
        self.rank = 0  # The upper tree's height limit
        

def find(x: 'Node object') -> 'set representative id':
    # If we have to compress a path as we are not a root of a tree
    if x != x.parent:
        # Point all sobsequent nodes on a path to the root node
        x.parent = find(x.parent)
    # Return the current (updated) parent of the node
    return x.parent


def union(x: 'Node object', y: 'Node object'):
    # Find parents of both x and y
    x = find(x)
    y = find(y)
    # Return if x and y are in the same set as there is nothing to do
    if x == y: return
    # Otherwise, link the smaller tree to the larger one
    if x.rank < y.rank:
        x.parent = y
    else:
        y.parent = x
        # If both x and y have the same rank and y was linked to x,
        # we have to increase the rank of x
        if x.rank == y.rank: x.rank += 1
            
            
def make_set(x: 'id'):
    return Node(x)


def connected(x: 'id', y: 'id'):
    return find(x) == find(y)


def kruskal(G: '(V, E)'):
    V, E = G
    n=len(V)
    # Sort all edges by their weights
    E.sort(key=lambda e: e[2])
    # Makeset for each of the vertices
    vert = [make_set(v) for v in V]
    # In a loop pick an edge of the smallest weight
    # and check if we can add this edge to the minimum
    # spanning tree
    counter=0
    result = []
    for edge in E:
	    if counter>=n-1:
		    break
        u, v, weight = edge
        if not connected(vert[u], vert[v]):
            union(vert[u], vert[v])
            counter+=1
            result.append(edge)
    # Return the resulting array of MST edges
    return result
    
```


1. Sortujemy krawędzie po wagach
2. result=$\emptyset$
3. Przeglądamy krawędzie w kolejności posortowanej od najmniejszej wagi.
4. Jeśli krawędź $e$ nie zawiera cyklu to $A=A\cup \{e\}$
5. zwracamy $A$

W kroku 3 korzystamy z struktury find/union pozwalającej na "kolorowanie" grupy wierzchołków a gdy 2 grupy sie połączą łączymy je jednym kolorem. Zachowujemy wtedy podział na niepołączone grupy.

Złożoność $O(E\cdot \log{E})$

**Możemy sortować swoimi własnymi sposobami np CountingSort/radix sort albo heapsort itd**

**Algorytm nie sprawdza czy graf jest spójny, zakładamy że dostajemy graf który jest spójny i jest grafem ważonym i nieskierowanym**

**Musimy korzystać z tablicy krawędzi**

---
#### Prima

```python title:prim.py
from queue import PriorityQueue


def is_consistent(G: 'graph represented using adjacency lists'):
    n = len(G)
    visited = [False] * n
    
    def dfs(u):
        visited[u] = True
        for v, _ in G[u]:
            if visited[v]:
                dfs(v)
                
    dfs(0)
    return all(visited)


def prims(G: 'graph represented by adjacency lists'):
    if not is_consistent(G): return [], []
    n = len(G)
    inf = float('inf')
    parents   = [-1] * n
    weights   = [inf] * n
    processed = [False] * n
    pq = PriorityQueue()
    pq.put((0, 0)) 
    
    while not pq.empty():
        u_weight, u = pq.get()
        # Skip a vertex if it was processed before
        if processed[u]: continue
        # If we remove the vertex from a priority queue this must be a vertex
        # with the lowest weight in a queue so we will mark this vertex as
        # processed because all the future occurrences of this vertex
        # in a priority queue must be skipped
        processed[u] = True
        # Loop over all the u vertex's neighbours and update parents of such
        # vertices which are not processed and their current weight is greater
        # than the u_weight
        for v, e_weight in G[u]:
            if not processed[v] and e_weight < weights[v]:
                parents[v] = u
                weights[v] = e_weight
                pq.put((e_weight, v))

    return parents, weights


def get_MST(G: 'graph represented by adjacency lists') -> 'minimum spanning tree graph':
    parents, weights = prims(G)
    n = len(parents)
    G = [[] for _ in range(n)]
    for u in range(n):
        if parents[u] >= 0:
            G[parents[u]].append((u, weights[u]))
            G[u].append((parents[u], weights[u]))
    return G
```

**Działa praktycznie tak samo jak dijkstra**


---
### Silnie spójne składowe 

```python title:silnie_spojne.py

def directed_graph_list(E: 'array of edges', n: 'number of vertices'):
    G = [[] for _ in range(n)]
    for edge in E:
        G[edge[0]].append(edge[1])
    return G


def get_process_times(G: 'graph represented using adjacency lists'):
    n = len(G)
    times = [0] * n
    visited = [False] * n
    time = 0
    
    def dfs(u):
        visited[u] = True
        for v in G[u]:
            if not visited[v]:
                dfs(v)
        nonlocal time
        time += 1
        times[u] = time
        
    for u in range(n):
        if not visited[u]:
            dfs(u)
            
    return times


def get_transposed_graph(G: 'graph represented using adjacency lists'):
    n = len(G)
    G2 = [[] for _ in range(n)]
    
    for u in range(n):
        for v in G[u]:
            G2[v].append(u)
            
    return G2


def get_vertices_order(times):
    n = len(times)
    order = [-1] * n
    for i in range(n):
        order[n - times[i]] = i
    return order


def find_coherent_components(G: 'graph represented using adjacency lists'):
    n = len(G)
    # Get processing time of each vertex
    times = get_process_times(G)
    # Create a transposed graph
    G = get_transposed_graph(G)
    # Get order of vertices in which DFS will be started from such vertices
    order = get_vertices_order(times)    
    # Create an array in which a result will be stored (each number will refer
    # to the other coherent component of a graph)
    result = [-1] * n  # This array will also be used to check if a vertex was visited
    token = 0
    
    def dfs(u):
        result[u] = token
        for v in G[u]:
            if result[v] < 0:
                dfs(v)
        
    # Start dfs from vertices of the highest processing time
    for i in range(n):
        u = order[i]
        if result[u] < 0:
            dfs(u)
            token += 1
            
    return result
```


---
### Maksymalny przepływ w grafie

```python title:max_flow.py
def ford_fulkerson(G: 'graph represented by adjacency matrix', s: 'source vertex', t: 'target vertex'):
    n = len(G)
    inf = float('inf')
    flow     = [[0] * n for _ in range(n)]
    visited  = [0] * n
    token    = 1  # Number of iteration to check which vertices have been visited
    max_flow = 0
    
    def dfs(u, bottleneck):
        visited[u] = token
        
        if u == t: return bottleneck
        
        for v in range(n):
            remaining = G[u][v] - flow[u][v]
            if visited[v] != token and remaining > 0:
                new_bottleneck = dfs(v, min(remaining, bottleneck))
                if new_bottleneck:
                    flow[u][v] += new_bottleneck
                    flow[v][u] -= new_bottleneck
                    return new_bottleneck
        return 0
    
    while True:
        increase = dfs(s, inf)
        if not increase: break
        max_flow += increase
        token += 1
        
    return max_flow
```

---
### Znajdowanie mostów 

```python title:find_bridges.py
def find_bridges(G: 'graph represented by adjacency lists'):
    n = len(G)
    low = [0] * n
    times = [0] * n
    bridges = []
    time = 0
    
    def dfs(u, parent):
        nonlocal time
        time += 1
        low[u] = times[u] = time

        for v in G[u]:
            # when there is no visit time, a vertex hasn't been yet visited
            if not times[v]:
                dfs(v, u)
                # If we have a cycle, we must update the low value of the parent vertex
                if low[v] < low[u]: low[u] = low[v]
            # v cannot be a parent of u as it's obvious it will always be visited before
            # and connected to the vertex u which doesn't imply that we have a back edge
            elif v != parent:  
                # We have a back edge (we try to enter a vertex which was entered before)
                if times[v] < low[u]: low[u] = times[v]
                    
        # We will start from parent -1 as the first vertex has no parent
        if times[u] == low[u] and parent >= 0:
            bridges.append((parent, u))
    # Check all possible starting vertices as a graph doesn't have to be consistent
    for i in range(n):
        if not times[i]:
            dfs(i, -1)

    return bridges
```
