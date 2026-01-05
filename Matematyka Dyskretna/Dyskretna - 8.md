### Grafy
#### 2025-01-22
##### Poprzednia: [[Dyskretna - 7]
##### Nastepna: [[]]
##### Zadania: [[]

#matematyka_dyskretna  #grafy

---
### Definicja grafu i wielkości/własności opisujące graf

**Grafem** nazywamy parę $G=(V,E)$, w której $V$ oznacza skończony zbiór **wierzchołków**, natomiast $E \subseteq \{\{u,v\}: u,v \in V\}$ jest zbiorem **krawędzi**. 
![[diagram-20250122.png]]
**Rząd grafu** - ilość wierzchołków $|V|$
**Wielkość/Rozmiar grafu** - ilość krawędzi $|E|$ 

**Stopień wierzchołka** - Ilość krawędzi wychodząca z wierzchołka
**Stopień maksymalny w grafie** - maksymalny *stopień wierzchołka* w grafie oznaczamy $\Delta(G)$
**Stopień minimalny w grafie** - minimalny *stopień wierzchołka* w grafie oznaczamy $\delta(G)$
![[diagram-20250122 (2).png]]
**Spacer w grafie** - ciąg wierzchołków $<v_0,v_1,v_2,\dots, v_n>$ o takiej własności, że dla każdego $1\leq i\leq n$ $\{v_{i-1},v_{i}\} \in E$
- zamknięty spacer (cykl) jest wtedy gdy $\{v_n,v_0\} \in E$![[diagram-20250122 (4).png]]
- otwarty spacer gdy nie jest zamknięty![[diagram-20250122 (3).png]]
**Ścieżka w grafie** - *spacer* który nie zawiera powtarzających się wierzchołków
**Droga w grafie** - *spacer* który nie zawiera powtarzających się krawędzi
**Cykl w grafie** - *zamknięta ścieżka*
**Długość spaceru** - liczba krawędzi w *spacerze*
**Odległością dwóch wierzchołków** - nazywamy *ścieżke* o najkrótszej *długości* pomiędzy wybranymi dwoma wierzchołkami![[diagram-20250122 (5).png]]
**Średnica grafu** - najdłuższa *odległość dwóch wierzchołków* oznaczamy $diam(G)$
![[diagram-20250122 (6).png]]
**Podgraf grafu** - graf zawierający część wierzchołków i część krawędzi z innego grafu oznaczamy $G'=(V',E')$ dla grafu $G=(V,E)$
- Jeśli $G'$ zawiera każdą krawędź grafu $G$, której oba wierzchołki końcowe są w $V'$, to $G'$ jest podgrafem **indukowanym** przez $V$
- Jeśli $V'=V$ to $G'$ jest podgrafem spinającym
**Spójne składowe** - podgrafy indukowane przez $V_1,V_2,\dots,V_n$ gdzie $V_1\cup V_2 \cdots \cup \cdots V_n=V$, Każde z tych $V_i$ są rozłączne z innym $V_j$ 

**Izomorficzne grafy** - grafy $G=(V,E)$ oraz $G'=(V',E')$ są izomorficzne gdy istnieje taka bijekcja $\varphi: V\to V'$, że: $\{x,e\} \in E\Leftrightarrow \{\varphi(x), \varphi(y)\}\in E'$ 

**Dopełnieniem grafu** - to graf który zawiera wszystkie brakujące krawędzie grafu by stał się grafem pełnym

**Droga Eulera (zamknięta)/ Cykl Eulera** - droga zamknięta zawierająca każdą krawędź ze zbioru $E$ 
**Droga Eulera (otwarta)** - droga otwarta zawierająca każdą krawędź ze zbioru $E$ 
**Cykl Hamiltona** - cykl zawierający każdy wierzchołek grafu $G=(V,E)$ 
**Ścieżka Hamiltona** - ścieżka zawierająca każdy wierzchołek grafu $G=(V,E)$

**Skojarzenie w grafie** - nazywamy podzbiór krawędzi wierzchołkowo rozłącznych
- **pełne** gdy *liczność* $|M|=\frac{n}{2}$
- **prawie pełne** gdy *liczność* $|M|=\frac{n-1}{2}$
**Liczność skojarzenia** - ilość krawędzi w *skojarzeniu* oznaczamy $|M|$
**Liczba skojarzeniowa grafu** - najliczniejsze skojarzenie oznaczamy $\mu(G)$

**Liść** - wierzchołek stopnia 1 w drzewie/lesie

**Rozdzielenie krawędzi** - dodanie nowego wierzchołka $w$ który zamieni krawędź $\{u,v\}$ na dwie krawędzie $\{u,w\}, \{w,v\}$ 
**Rozdzielenie grafu** - graf powstały poprzez rozdzielenie kolejnych krawędzi w grafie

**Płaska reprezentacja** - takie rozmieszczenie wierzchołków na płaszczyźnie (sferze) że krawędzie sie nie przecinają (oprócz oczywiście w wierzchołkach).
**Ściany** - *reprezentacja płaska* rozdziela sfere na regiony zwane ścianami

**Zwinięcie krawędzi** - usunięcie pętli i równoległych krawędzi
**Minor grafu** - graf powstały poprzez wykonanie operacji usuwania wierzchołków/krawędzi lub zwinięcia krawędzi.
**Zbiór niezależny** - podzbiór wierzchołków takich że żadne dwa wierzchołki nie są sąsiednie.
oznaczamy $\alpha(G)$
**Klika** - podzbiór wierzchołków takich że każde dwa są sąsiednie (łączą się krawędzią) oznaczamy $\omega(G)$ 
**Liczba chromatyczna** - minimalna liczba kolorów na które da się pomalować wierzchołki tak żeby żadne sąsiednie (połączone krawędzią) nie miały tych samych kolorów
**Indeks chromatyczny** - minimalna liczba kolorów na które da się pomalować krawędzie tak żeby z żadnego wierzchołka nie wychodziły krawędzie o takim samym kolorze.

---
### Różne rodzaje grafów:

**Graf pełny:**
Każdy wierzchołek jest połączony z każdym innym wierzchołkiem.

**Graf acykliczny:**
Nie zawierający cykli

**Graf skierowany (digraf):**
To taki graf w którym krawędź *(łuk)* $(u,v)$ zachowuje kolejność, nie jest zbiorem więc ma także kierunek.

**Multigraf:**
Może mieć więcej niż jedną taką samą krawędź.

**Hipergraf:**
Jego krawędź należy rozumieć raczej jako zbiór, krawędź z wierzchołka A łączy z grupą wierzchołków BCD.

**Graf spójny:**
Istnieje wtedy gdy dla każdych wierzchołków istnieje ścieżka.

**Graf niespójny:**
Gdy istnieją dwa wierzchołki które nie da się połączyć ścieżką.

**Samodopełniający się graf:**
graf *izomorficzny* ze swoim *dopełenieniem*

**Graf dwudzielny:**
Jeżeli da się podzielić wierzchołki grafu na dwie grupy, tak by jedyne krawędzie prowadziły z jednej do drugiej.

**Drzewo:**
Graf spójny, acykliczny.

**Las:**
Zbiór drzew, *graf acykliczny*.

**Graf Hamiltonowski:**
Graf posiadający *cykl Hamiltona*.

**Graf Eulerowski:**
Graf posiadający *cykl Eulera* czyli *zamkniętą drogę Eulera*.

**Trasowalny:**
Graf posiadający *ścieżke Hamiltona*.

**Graf planarny:**
Posiadający *płaską reprezentacje*.


---
### Lematy i twierdzenia

#### O sumie stopni wszystkich wierzchołków (parzysta suma):

Suma stopni wszystkich wierzchołków w grafie jest liczbą parzystą. (Bo dodanie nowej krawędzi zwiększa sumę stopni o 2)

---
#### O liczbie wierzchołków stopnia nieparzystego (parzysta liczba):

Liczba wszystkich wierzchołków stopnia nieparzystego w grafie zawsze jest liczbą parzystą.

(No bo skoro suma wszystkich stopni jest parzysta, a suma stopni wszystkich wierzchołków stopnia parzystego jest nieparzysta to suma stopni wszystkich wierzchołków stopnia nieparzystego także musi być parzysta - co implikuje że jest ich parzysta ilość)

$$\begin{gathered}
S - \text{suma wszystkich stopni wierzchołków}\\
P - \text{suma wszystkich stopni wierzchołków o stopniu parzystym}\\
N - \text{suma wszystkich stopni wierzchołków o stopniu nieparzystym}\\\\
S=P+N\\
S-P=N\\
S-P\mod{2}=0\implies N\mod{2}=0\\
N \text{ parzyste}\\
\text{A skoro każdy wierzchołek ma nieparzysty stopień a suma ich stopni jest parzysta}\\
\text{To musi być ich parzysta ilość}
\end{gathered}$$

---
#### Graf jest spójny jeżeli $\delta(G) \geq \lfloor \frac{n}{2}\rfloor$

(Jest to jedynie warunek wystarczający, a nie konieczny. Może być graf którego najmniejszy stopień jest mniejszy od tego a i tak jest to graf spójny)


---

#### Multigraf (graf) spójny $G=(V,E)$ posiada otwartą drogę Eulera $\Leftrightarrow$ gdy dokładnie dwa wierzchołki w G mają stopnie nieparzyste.

Z zamkniętej drogi Eulera robimy otwartą, dodając jedną krawędź.

---
#### Graf posiada zamkniętą drogę Eulera $\Leftrightarrow$ gdy stopień każdego wierzchołka jest parzysty.

To wynika z faktu, że cykl eulerowski musi "wchodzić" i "wychodzić" z każdego wierzchołka

---
#### Graf $G$ jest dwudzielny gdy $\Leftrightarrow$ gdy każdy cykl w $G$ ma parzystą długość.

No bo idąc takim cyklem przez każdą krawędź podpisujemy naprzemiennie A, B.
![[diagram-20250122 (7).png]]

---
#### Rozmiar drzewa rzędu $n$ wynosi $n-1$ 

No to widać intuicyjnie, idąc od korzenia prowadzimy krawędź do jego dziecka. A następnie dla każdego innego wierzchołka istnieje krawędź która łączy go z rodzicem.

---
#### Liczba liści w drzewie rzędu $n$ spełnia $0\leq l \leq n$. Liczba liści $l$ w drzewie rzedu $n\geq 3$ spełnia $2 \leq l \leq n-1$.

---
#### W drzewie każda para wierzchołków połączona jest dokładnie jedną ścieżką.

Wynika właściwie z definicji, tego czym jest drzewo. Drzewo musi być spójne i acykliczne.

---
#### Niech $n\geq 3$. Jeśli $\delta(G)\geq \frac{n}{2}$ to G jest Hamiltonowski. (TWIERDZENIE DIRACA)

Hamiltonowski czyli posiadający cykl Hamiltona czyli cykl który przechodzi przez każdy wierzchołek, gdzie cykl musi zawierać każdy wierzchołek tylko raz.

---
#### Niech $G$ będzie grafem, w którym, dla każdej pary niesąsiednich wierzchołków $u$ i $v$, zachodzi warunek $d(u)+d(v)\geq n$. Wtedy $G$ jest Hamiltonowski.

---
#### Twierdzenie o liczbie krawędzi: Jeśli graf prosty o $n$ wierzchołkach ma co najmniej $\frac{(n-1)(n-2)}{2}+2$ krawędzi to jest Hamiltonowski

---
#### W każdym grafie planarnym $G=(V,E)$ rzedu $n\geq 3$ zachodzi zależność $m\leq 3n-6$

---
#### Każdy graf planarny posiada wierzchołki MAKSYMALNIE 5 stopnia.

