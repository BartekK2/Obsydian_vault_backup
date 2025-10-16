
---
### Binary search

```python 
def binary_search(arr,search_for,n):
	guess=n//2
	l=0
	r=n
	if n==0:
		return None
	while arr[guess]!=search_for and l!=r:
		if arr[guess]>search_for:
			r=guess
		elif arr[guess]<search_for:
			l=guess
		guess=l+(r-l)//2
	if arr[guess]=search_for:
		return guess
	else:
		return None
```

---
### Merge Sort

**Złożoność:** $O(n\cdot \log{n})$
```python
def merge(tab, lewo,srodek, prawo):
    n1=srodek-lewo+1
    n2=prawo-srodek

    L=[0]*n1
    R=[0]*n2
    for i in range(n1):
        L[i]=tab[lewo+i]
    for j in range(n2):
        R[j]=tab[srodek+1+j]
    
    i=0
    j=0
    k=lewo

    while i<n1 and j<n2:
        if L[i] <= R[j]:
            tab[k]=L[i]
            i+=1
        else:
            tab[k]=R[j]
            j+=1
        k+=1

    while i<n1:
        tab[k]=L[i]
        i+=1
        k+=1
    while j<n2:
        tab[k]=R[j]
        j+=1
        k+=1
    
def mergeSort(tab,lewo,prawo):
    if lewo<prawo:
        srodek=(lewo+prawo)//2
        mergeSort(tab,lewo,srodek)
        mergeSort(tab,srodek+1,prawo)
        merge(tab,lewo,srodek,prawo)

if __name__=="__main__":
    arr=[38,27,43,10,90]
    mergeSort(arr,0,len(arr)-1)
    print(arr)
	
```


---
### CountingSort

**To działa gdy mamy małą liczbe unikalnych elementów do posortowania i możemy po prostu policzyć ile jest każdego rodzaju i wypisać po kolei**

```python title:counting_sort.py
from random import randint


arr = [randint(0,9) for _ in range(10**6)]
def counting_sort(arr):
	n=len(arr)
	counts=[0]*10
	for i in range(n):
		counts[arr[i]]+=1
	res_array=[0]*n
	p=0
	for i in range(n):
		while counts[p]==0:
			p+=1
		counts[p]-=1
		res_array[i]=p
	return res_array

print(counting_sort(arr)==sorted(arr)) # True
```

Ten algorytm można oczywiście dostrajać do własnych potrzeb i inteligentnie wykorzystywać gdy zauważymy pewne tendencje np:


---
### QuickSort

1. **wybierz pivot**
2. **mniejsze na lewo, większe na prawo od pivota**
3. **można zauważyć że pivot jest już na swojej pozycji!**
4. **rekursywnie lewa i prawa strona**

```python title:okropny_quick_sort.py
def quick_sort(arr):
    if len(arr) < 2: return arr
    less=[i for i in arr[1:] if i<arr[0]]
    more=[i for i in arr[1:] if i>=arr[0]]

    return quick_sort(less)+[arr[0]]+quick_sort(more)
print(quick_sort([randint(0,100) for _ in range(10**4)]))
```

To najgorszy quicksort jaki można sobie wyobrazić - ale przyda się żeby pokazać clue całego algorytmu. Po jednej stronie mamy mniejsze, po drugiej większe a pivot powinien znaleźć się już na swoim miejscu w posortowanej tablicy.

Minusów tego algorytmu jest sporo ale najłatwiej wskazać na to ile miejsca w pamięci zajmą dodatkowe tablice (less,more) zamiast robić wszystko w miejscu, rekurencja, pivot z tego samego miejsca.

Poniższe wady jedna po drugiej rozwalimy poniżej:

```python title:prymitywny_quick_sort.py
def partition(arr,low,high):
    pivot=arr[high]
    i=low-1
    for j in range(low,high):
        if arr[j]<=pivot:
            i=i+1
            (arr[i],arr[j])=(arr[j],arr[i])
    (arr[i+1],arr[high])=(arr[high],arr[i+1])
    return i+1
    
def quick_sort2(arr,low,high):
    if low < high:
	    i=partition(arr,low,high)
	    quick_sort2(arr,low,i-1)
	    quick_sort2(arr,i+1,high)

```

**Powyższe to prymitywny algorytm pokazujący jedynie jak to ma działać**

- możemy zauważyć że w rekurencyjnym odwołaniu już nie uwzględniamy indeksu na którym poprzednio skończyliśmy, z tej racji iż jest on już na swoim miejscu!
- jednakże jest to algorytm prosty mający swoje wady - np. pivot brany ciągle z tego samego miejsca zepsuje złożoność w przypadku kiedy tablica jest posortowana (albo prawie posortowana) - wtedy złożoność wyniesie nawet $O(n^2)$

**Co z pivotem?**
Nasze opcje to:
- branie pivota ciągle ze środka - nie zmieni to dużo w szczególnych przypadkach (choć napewno posortowane tablice nam już krzywdy nie zrobią)
- branie pivota z mediany trzech/dziewięciu median
- losowy - chyba odpada na egzaminach + nie gwarantuje złożoności $O(n\cdot \log{n})$
- mediana median - chyba najlepsza ze wszystkich opcji :)

```python title:lepszy_quick_sort.py

def median_of_three(array, low, high):
    mid = (low + high) // 2
    a, b, c = array[low], array[mid], array[high]

    # porównania: znajdź medianę
    if (a <= b <= c) or (c <= b <= a):
        return mid
    elif (b <= a <= c) or (c <= a <= b):
        return low
    else:
        return high

def partition2(arr,low,high):
    p=median_of_three(arr,low,high) # albo median_of_nine czyli potrójne uruchomienie median_of_three na podzielonej tablicy
    pivot=arr[p]
    arr[high],arr[p]=arr[p],arr[high]
    i=low-1
    for j in range(low,high):
        if arr[j]<=pivot:
            i=i+1
            (arr[i],arr[j])=(arr[j],arr[i])
    (arr[i+1],arr[high])=(arr[high],arr[i+1])
    return i+1


def quick_sort3(arr,low,high):
    if low < high:
	    i=partition2(arr,low,high)
	    quick_sort3(arr,low,i-1)
	    quick_sort3(arr,i+1,high)

```

**Mamy już lepiej wybranego pivota! (jeśli chcemy być bardziej dokładni można zrobić mediane median i wtedy będzie gwarancja $O(n\cdot \log{n})$**

**Teraz pozostaje jedynie kwestia rekurencji - należałoby ją zamienić na coś co wyeliminuje możliwość błędu limitu rekursji (np. własny stos albo iteracyjnie ale nie chce mi sie)**

##### Zalety quicksorta:

Znajdowanie k-tego największego elementu (podobnie jak w heapsort ale ciutke szybciej)

```python title:quick_select.py

def quick_select(arr,k):
    low = 0
    high=len(arr)-1
    i=partition3(arr,low,high)
    while i!=k:
        if i>k:
            high=i-1
        else:
            low=i+1
        i = partition3(arr,low,high)
    
    return arr[i]
```

---
### HeapSort

```python title:funkcje_pomocnicze.py
# indeksując korzeń od zera
def left(index):
	return index*2+1
def right(index):
	return index*2+2
def parent(index):
	return (index-1)//2

```

- **heapify ma za zadanie przywrócić własność kopca min/max wtedy gdy
rodzic nie jest większy od swoich dzieci w przypadku kopca max
lub adekwatnie w przypadku kopca min**

- **MUSIMY uruchomić potem rekurencyjnie to dla każdego zamienionego dziecka bo nie mamy już gwarancji że spełnia on własności kopca max/min**

```python title:heapify.py
def heapify(arr,index,n):
	largest=index
	if left(index)<n and arr[left(index)] > arr[largest]:
		largest=left(index)
	if right(index)<n and arr[right(index)] > arr[largest]:
		largest=right(index)
	if index!=largest:
		arr[largest], arr[index]=arr[index],arr[largest]
		heapify(arr,largest,n)
```

**mając już funkcje heapify możemy przejść do budowy kopca w sposób następujący**

```python title:build_heap.py
def build_max_heap(arr,n):
 # n//2 ponieważ ostatnie elementy nie mają swoich dzieci, idziemy od końca kończywszy na korzeniu włącznie
	for i in range(n//2,-1,-1):
		heapify(arr,i,n)
```

**Gdy już zbudowaliśmy kopiec maksymalny lub w zależności od potrzeb kopiec minimalny możemy przejść do sortowania heapsort:**

Zauważając że:
1. zawsze zachowujemy element maksymalny/minimalny w korzeniu 
2. musimy pomijać ten element ponieważ jest on już na swoim miejscu
3. po "wycięciu" go musimy przywrócić własność kopca max/min

Zatem właściwą strategią jest zamiana korzenia z ostatnim elementem, zmniejszenie liczby elementów do której algorytm może dojść (tak by już pominąć posortowany element) a następnie przywrócenie struktury kopca max/min.

```python title:heapsort.py

def heapsort(arr,n):
	build_max_heap(arr,n)
	# zatem zaczynamy od kopca maks/min
	for i in range(n-1,-1,-1):
		arr[0],arr[i]=arr[i],arr[0] # zamieniamy z ostatnim
		heapify(arr,0,i) # przywrócamy strukture kopca 
	return arr
```


##### Złożoność:
- heapify $O(\log{n})$
- build_heap $O(n)$
- heapsort $O(n\cdot \log{n})$

##### Zastosowanie HeapSort:

 - Można go zastosować do znajdowania k-największych elementów w złożoności $O(n\cdot log{k})$
 - Można również połaczyć wiele posortowanych list w złożoności $O(n\cdot \log{k})$ gdzie $n$ to liczba wszystkich elementów a $k$ liczba wszystkich list
 - Wykrywanie mediany "w locie" czyli razem z dodawanymi kolejnymi elementami
 - Sortowanie "in-place" gdy ma sie ograniczoną pamięć

Zastosowania te po kolei przedstawie poniżej, lecz najpierw dorzuce kilka potrzebnych i przydatnych algorytmów.

Wyciąganie największego/najmniejszego

```python title:heap_pop.py
def heap_remove_max(arr,n):
	arr[0],arr[n-1]=arr[n-1],arr[0]
	heapify(arr,0,n-1)
	arr.pop()
	return arr
```

Dodawanie nowego elementu

```python title:heap_append.py
def heap_insert(arr, el):
    arr.append(el)          # dodajemy na końcu
    n = len(arr) - 1         # indeks nowego elementu
    while n > 0:             # dopóki nie jesteśmy w korzeniu
        p = parent(n)        # indeks rodzica
        if arr[n] > arr[p]:  # dla kopca max — dziecko > rodzic
            arr[n], arr[p] = arr[p], arr[n]  # zamień
            n = p            # idź w górę
        else:
            break            # własność kopca jest zachowana
    return arr
```

**Wyciąganie k-największych**

```python title:k_max.py

def k_max(arr,k, heap=False):
	k_el = [0 for _ in range(k)]
	n=len(arr)
	if k>0:
		if not heap:
			build_max_heap(arr,n) # jeśli nie zbudowany kopiec
		for i in range(k):
			k_el[i]=arr[0]
			arr[0],arr[n-i-1]=arr[n-i-1],arr[0]
			heapify(arr,0,n-i-1)
	return k_el
```


#### Łączenie k-posortowanych tablic

```python title:merge_k_sorted.py

sorted_arr=[sorted(randint(0,100) for _ in range(randint(0,20))) for _ in range(randint(0,10))]

def merge_k_sorted(sorted_arrays):
    k = len(sorted_arrays)
    get_value = lambda el: el[0]
    sum_all_el = sum(len(arr) for arr in sorted_arrays)
    merged=[None]*sum_all_el # Alokacja gdyby dużo było tych elementów
    heap = []
    for i in range(k):
        if len(sorted_arrays[i])>0:
            heap.append((sorted_arrays[i][0],i,0)) # structure: (value, row eg. array, column)
    build_min_heap(heap,len(heap),key=get_value)

    for i in range(sum_all_el):
        deleted = heap_remove_min(heap,len(heap),key=get_value)
        (value, current_array,current_col)=deleted
        merged[i]=value
        if current_col+1<len(sorted_arrays[current_array]):
            next_el=(sorted_arrays[current_array][current_col+1], current_array, current_col+1) # structure: (value, row eg. array, column)
            heap_insert_min(heap,next_el,key=get_value)
    return merged

```
