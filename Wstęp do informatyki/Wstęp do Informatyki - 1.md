### Wstęp i informacje
#### 2024-10-07
##### Ćwiczenia: [[Wstęp do Informatyki-1 - zadania]]
##### Następna [[Wstęp do Informatyki - 2]]

#algorytmy   #WDI #informacje

--- 
###### Informacje 
Marek Gajęcki 3 kolokwia 2 zadania po 5 pkt razem 30 pkt , ocena = max(round(SR), 3.0)
Jeżeli pozytywną ocenę z ćwiczeń i egzaminu uzyskano w pierwszym terminie oraz ocena końcowa < niż 5.0 to ocena jest podnoszona o 0.5
- - -
###### Zakres przedmiotu:
- Pojęcia podstawowe
- Mechanizmy języka strukturalniego
- Skalarne typy danych
- Strukturalne typy danych
- Procedury i funkcje
- Rekurencja
- Struktury odsyłaczowe
- Przykłady Struktur danych
- Złożoność obliczeniowa
- Przykłady algorytmów
- Reprezentacja liczb w komputerze 
- Pojęcie architektury Komputera, paradygmatów programowania
- - -
###### Literatura
- D. Harel "Rzecz o istocie informatyki - algorytmika"
- I.G. Brookshear "Informatyka w ogólnym zakresie "
- I. Mieścichi "Wstęp do Informatyki nie tylko dla informatyków"
- N. Wirth "Algorytmy + struktury danych"
- - -
###### Teoria Informacji
> Wielkość Informacji zawarta w danym zbiorze jest miarą stopnia trudności rozpoznania elementów tego zbioru.

Ilością informacji zawartej w zbiorze
$$
X=\{ x_1, x_2 , ..., x_n \}
$$
nazywamy liczbę:
$$
H( X ) =-\sum_{i=1}^N {p_i} \cdot log_2(p_i)
$$
gdzie: 
$$
p_i (p_i>0, \sum{p_i=1})
$$
jest prawdopodobieństwem wystąpienia elementu $x_i$
** Przykłady **
{0.1} - 1 bit
{0..9} - 3.32 bita
zbiór liter języka ang. - 4.7 bita

---

###### Podstawowe pojęcia
** Zadanie algorytmiczne -** polega na określeniu:
- wszystkich poprawnych danych wejściowych 
- oczekiwanych wyników jako funkcji danych wejściowych

** Algorytm - ** specyfikacja ciągu elementarnych operacji, które przekształcają dane wejściowe na wyniki.
- opis słowny
- schemat blokowy
- kod
---
###### Algorytm Euklidesa - NWD
###### Najprostszy: (nie używać)
```Python title:nwd_euklidesa.py
while a!=b:
	if a>b: 
		a=a-b
	else:
		b=b-a
return a
```

###### Najlepszy:
```Python title:nwd_lepsze.py
def nwd2(a, b):
	while b!=0:
		a,b= b, a%b
	return a
```
---
###### Wzór Newtona na obliczenie pierwiastków

$$
a_{n+1} = \frac{(\frac{S}{a_n}+a_n)}{2}, \ \ S- liczba \ do  \ spierwiastkowania
$$

```Py title:pierwiastek.py
def sqrt(S):
	eps = 1e(-10)
	a=S
	while True:
		an=(S/an+an)/2
		if abs(a-an)<eps:
			break
		a=an
```
---




Ebnf/bnf