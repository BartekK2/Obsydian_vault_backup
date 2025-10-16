#### Git: https://github.com/BartekK2/zadania_wdi
##### Lekcja: [[Wstęp do Informatyki - 1]]
#WDI  #bisekcja #algorytmy #nwd #rozklad_na_czynniki #kody_huffmana  
###### 2024-10-07
![[Messenger_creation_92CF654E-DB88-424A-B944-907113AE09B4.jpeg]]###### 

###### ◦ Ile informacji zawiera 10 znakowe słowo, którego każdy znak  z jednakowym prawdopodobieństwem jest jedną z liter a, b, c ?
$$
X= \{ a, b,c\} 
$$


◦ Jak stworzyć kody Huffmana dla zbiorów 5,6,7,... elementowych? 
◦ Jak przyspieszyć działanie algorytmu Euklidesa?
Zamienić a, b= a - b, b-a na a,b=b, a % b
◦ Ile czasu potrzebuje w najgorszym przypadku drugi algorytm  aby rozłożyć na czynniki 50 cyfrową liczbę?
◦ Jak przyspieszyć działania programu rozkładu na czynniki pierwsze?
Nie szukamy dzielników aż do n tylko do $\sqrt{n}$
◦ Proszę znaleźć najmniejszą liczbę pierwszą, której suma cyfr wynosi 101,  a cyfry są w porządku nierosnącym.
1. Najpierw sprawdźmy jak długa musi być liczba by suma cyfr =101 (12 cyfr)
2. Zacznijmy od 10^13 -1 i szukajmy liczb które spełniają warunek z sumą cyfr
3. Sprawdzamy czy pierwsza
◦ Dla jakich liczb algorytm Euklidesa wykonuje najwięcej iteracji? 
Dla dwóch sąsiednich liczb Fibonacciego bo z definicji nie mają one dzielników: 


```Python title:Fib
 def fib(x):
	 a,b=1,1
	 while a<x:
		 a,b = b,a + b
		 print(b)
```

```Python title:sqrt
eps= 1e(-10)
a=0
s=float(input())
an=1
while abs(a-an)>eps:
	a=an
	an = (s/a + a)/2.0
```

```Python title:do_while.py
while True:
	if warunek:
		break
```
Bisekcja - aproksymacja przez dzielenie 2 skrajnych odpowiedzi
```Python title: bisekcja.py
# X ^ X =2024,x=?
a =O
b=10
eps= 1e(-10)
while True:
	
