### Macierze
#### 2024-11-19
##### Poprzednia: [[Algebra - 7]]
##### Następna: [[Algebra - 9]]
##### Zadania: [[]]

#macierze #algebra 

--- 
### Macierz

```ad-Definicja
title: Macierze

*Macierzą* o elementach ze zbioru $K$ nazywamy dowolne odwzorowanie:
$\{1,2,...,m\} \times \{1,2,...,n\} \ni (i,j) \to a_{ij} \in K$
gdzie zbiór wartości zapisujemy w formie
$$\begin{gathered}m \ wierszy
\begin{bmatrix}  
a_{11} & a_{12} &\dots& a_{1n}\\  
a_{21} & a_{22} &\dots& a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1} & a_{m2} &\dots& a_{mn}
\end{bmatrix}\\
n \ kolumn
\end{gathered}
$$
Ten zbiór (tę tablicę) utozsamiamy z macierzą.
Macierz o $m$ wierszach i $n$ kolumnach nazywamy macierzą *o wymiarach* $m\times m$.
*Ozn.* $A=[a_{ij}]=[a_{ij}]_{m \times n}=A_{m\times n}$
```

---

```ad-Definicja
title: Macierz transponowana

*Macierzą transponowaną* do macierzy $A=[a_{ij}]_{m \times n}$ nazywamy macierz $A^T = [b_{ij}]_{n \times m}$ gdzie $b_{ij} = a_{ij}$ dla $i \in \{1,...,n\},j \in \{1,...,m\}$.
```

```ad-Przyklad
$$\begin{gathered}
A=\begin{bmatrix}  
1 & 2\\  
0 & 1\\
-3 & 2\\
0 & 4
\end{bmatrix}_{4\times 2} &
A^T=\begin{bmatrix}  
1 & 0 & -3 & 0\\  
2 & 1 & 2 & 4
\end{bmatrix}_{2\times 4}\\
\end{gathered}$$

Czyli po prostu odwracamy tą macierz. Kolumny stają się wierszami, wiersze kolumnami.
```

---
```ad-Definicja
title: Macierz zerowa

Macierz nazywamy *macierzą zerową* jeżeli wszystkie jej elementy równe są zero.
*Ozn.* $\boldsymbol{0},\boldsymbol{0}_{m\times n}$ 
```

```ad-Przyklad
$$\begin{gathered}\boldsymbol{0}_{2\times 3}=
\begin{bmatrix}  
0 & 0 & 0\\
0 & 0 & 0
\end{bmatrix}\\
\end{gathered}$$
```

---
```ad-Definicja
title: Macierz kwadratowa
Jeżeli liczba wierszy macierzy równa jest liczbie jej kolumn $(m=n)$, to macierz taką nazywamy *macierze kwadratową*.
```

```ad-Przyklad
$$\begin{gathered}
A_{n\times n}=
\begin{bmatrix} 
1 & 0 & \pi\\
e & 7 & -\pi\\
9 & 3 & 0\\
\end{bmatrix}\\
\end{gathered}$$
```

---
```ad-Definicja
title: Przekątna główna
O elementach $a_{ij}, i=1,2,...,n$, mówimy, że tworzy *przekątną główną* macierzy A.
$$
\begin{bmatrix} 
a_{11} & & & &\\
& a_{22} & & &\\
& & a_{33} & &\\
& & & \ddots &\\
& & & & a_{nn}\\
\end{bmatrix}\\
$$
```
---
```ad-Definicja
title: Macierz diagonalna
Macierz $A$ nazywamy *macierzą diagonalną*, jeżeli wszystkie jej elementy poza przekątną główną są równe 0.
$$
\begin{bmatrix} 
7 & 0 & 0 & 0\\
0 & -1 & 0 & 0\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 2\\
\end{bmatrix}\\
$$
Co prawda jedna z wartości w przekątnej głównej to 0, ale to nas nie obchodzi. Najważniejsze że reszta jest równa 0.
```
---
```ad-Definicja
title: Macierz jednostkowa
*Macierz jednostkowa* to *macierz diagonalna*, w której wszystkie elementy na głównej przekątnej są równe 1. A reszta elementów równa 0. *Ozn.* $I, I_n$
```

```ad-Przyklad
$$
I_3=\begin{bmatrix} 
\textcolor{lightgreen}{1}&0&0\\
0&\textcolor{lightgreen}{1}&0\\
0&0&\textcolor{lightgreen}{1}\\
\end{bmatrix}\\
$$
Wszystkie elementy oprócz przekątnej głównej są równe 0, a wszystkie elementy w przekątnej głównej są równe 1.
```

---
```ad-Definicja
title: Macierz trójkątna górna/dolna
Macierz $A$ nazywamy *trójkątną górną/dolną*, jeżeli wszystkie jej elementy poniżej/powyżej głównej przekątnej są równe 0.
```

```ad-Przyklad
$$\begin{gathered}
Ponizej:\
\begin{bmatrix} 
\textcolor{lightgreen}{1}&2\\
\textcolor{Orange}{0}&\textcolor{lightgreen}{-1}\\
\end{bmatrix}
&
Powyzej:\
\begin{bmatrix} 
\textcolor{lightgreen}{1}&\textcolor{Orange}{0}&\textcolor{Orange}{0}\\
2&\textcolor{lightgreen}{0}&\textcolor{Orange}{0}\\
-1&3&\textcolor{lightgreen}{-7}
\end{bmatrix}
\end{gathered}$$
W drugim przykładzie ponownie, mamy w przekątnej głównej 0 ale to nas nie obchodzi. Najważniejsze że powyżej przekątnej są 0.
```

---
```ad-Definicja
title: Macierz symetryczna
Macierz $A$ nazywamy *symetryczną*, jeżeli $A=A^T$.
```

```ad-Przyklad
$$\begin{gathered}
A=\begin{bmatrix} 
1&3&-1\\
3&5&2\\
-1&2&0
\end{bmatrix}=A^T
\end{gathered}$$
```

---
### Działania na macierzach

```ad-Definicja
title: Równość dwóch macierzy
*Równość dwóch macierzy* zachodzi wtedy i tylko wtedy gdy macierze mają takie same wymiary i odpowiednie ich elementy są sobie równe

Tak symbolicznie to:
$$\begin{gathered}
\ [a_{ij}]_{m\times n}=[b_{ij}]_{l\times p}: \Leftrightarrow (m=l \land n=p\\ \land \forall i \in \{1,...,m\} \forall j \in \{1,...,n\}: a_{ij}=b_{ij})
\end{gathered}$$
```

---

```ad-Definicja
title: Suma dwóch macierzy
*Suma dwóch macierzy* zdefiniowana jest jedynie dla macierzy o tych samych wymiarach jako:
$\ [a_{ij}]_{m\times n}+[b_{ij}]_{m\times n}:=[c_{ij}]_{m \times n}$, gdzie $c_{ij}=a_{ij}+b_{ij}$ dla $i\in \{1,...,m\}, j \in \{1,...,n\}$.

Czyli dodajemy do siebie każde elementy na tych samych pozycjach po prostu.
```

```ad-Przyklad
$$\begin{gathered}
\begin{bmatrix}
\textcolor{lightgreen}{-1}&\textcolor{Orange}{2}\\
\textcolor{Goldenrod}{3}&\textcolor{Fuchsia}{7}
\end{bmatrix}
+
\begin{bmatrix}
\textcolor{lightgreen}{5}&\textcolor{Orange}{-3}\\
\textcolor{Goldenrod}{4}&\textcolor{Fuchsia}{-7}
\end{bmatrix}
=
\begin{bmatrix}
\textcolor{lightgreen}{4}&\textcolor{Orange}{-1}\\
\textcolor{Goldenrod}{7}&\textcolor{Fuchsia}{0}
\end{bmatrix}
\end{gathered}
$$
```

---

```ad-Definicja
title: Mnożenie macierzy przez liczbę (skalar)
*Mnożenie macierzy przez liczbę (skalar)* - mnożąc macierz przez liczbę (skalar), mnożymy każdy element macierzy przez tę liczbę (skalar).

$A=[a_{ij}], \ \ \  \alpha A:=[\alpha a_{ij}]$
```

```ad-Przyklad
$$\begin{gathered}
3\cdot \begin{bmatrix} 
1\\
0\\
-2
\end{bmatrix}=
\begin{bmatrix} 
3\\
0\\
-6
\end{bmatrix}
\end{gathered}
```

---
```ad-Definicja
title: Mnożenie dwóch macierzy
*Mnożenie dwóch macierzy* $A \cdot B$, jest wykonalne tylko wtedy, gdy *liczba kolumn* macierzy *A* równa jest *liczbie wierszy* macierzy *B*, czyli dla:

$A=[a_{ij}]_{m\times p}, B=[b_{ij}]_{p \times n}$ i jest definiowane jako:
$A\cdot B:=[c_{ij}]_{m\times n}$, gdzie $c_{ij}=\sum^{p}_{k=1}{a_{ik}b_{kj}}=a_{i1}b_{1i}+a_{i2}b_{2j}+...+a_{ip}b_{pj}$
```

```ad-Przyklad
$$\begin{gathered}
\begin{bmatrix}
\textcolor{lightgreen}{1}&\textcolor{lightgreen}{2}&\textcolor{lightgreen}{0}&\textcolor{lightgreen}{-3}\\
2&0&1&-1\\
\textcolor{Goldenrod}2&\textcolor{Goldenrod}{3}&\textcolor{Goldenrod}{-2}&\textcolor{Goldenrod}{0}
\end{bmatrix}_{3\times 4}

\cdot

\begin{bmatrix}
\textcolor{lightgreen}{1}&\textcolor{Goldenrod}{-1}\\
\textcolor{lightgreen}{2}&\textcolor{Goldenrod}{0}\\
\textcolor{lightgreen}{3}&\textcolor{Goldenrod}{-1}\\
\textcolor{lightgreen}{2}&\textcolor{Goldenrod}{-2}
\end{bmatrix}_{4\times 2}=

\begin{bmatrix}
\textcolor{lightgreen}{-1}&5\\
3&-1\\
2&\textcolor{Goldenrod}{0}
\end{bmatrix}
\end{gathered}
$$

Bo np dla lewego górnego rogu w wyniku tego mnożenia (-1):
$1\cdot 1+2\cdot 2+0\cdot 3+(-3)\cdot2=-1$

A np dla pierwszego wiersza, drugiej kolumnie (5):
$1\cdot (-1)+2\cdot 2+0\cdot 3+(-3)\cdot 2=5$

Czyli jeżeli chcemy w wyniku obliczyć wartość $i$ wiersza $j$ kolumny to musimy pomnożyć każdy składnik $i$ wiersza z $A$ z każdym elementem z $j$ kolumny z $B$.
```

```ad-Uwaga
Mnożenie macierzy *nie* jest przemienne, $B\cdot A$ może być niewykonalne, albo wyjdzie po prostu inny wynik.
```

---
### Własności działań na macierzach

```ad-note
title: Oznaczenie

$M_{m \times n}(K)$ - zbiór macierzy o wymiarach $m\times n$, o elementach z ciała przemiennego $K$, $|K|\geq 2$
```

1. Dla ustalonych m, n, K
   $(M_{m\times n}(K), K, +, \cdot)$ - *przestrzeń wektorowa*
   z tego wynikają różne własności które również wynikają z przestrzeni wektorowej np:
   - $\alpha \cdot (A+B) = \alpha \cdot A + \alpha \cdot B$
   - $(\alpha+\beta)\cdot A=\alpha \cdot A+\beta \cdot A$
2. $\exists l' - mac. \forall A \in M_{m\times n}(K): l'\cdot A =A$ - istnieje jedynka mnożenia macierzy $(I'=I_m)$
   $\exists l' - mac. \forall A \in M_{m\times n}(K):  A\cdot I'' =A \ \ \ (I''=I_n)$
3. Ponadto, o ile dane działania są wykonalne, to:
   $(A\cdot B)\cdot C=A\cdot (B\cdot C)$
4. $A\cdot (B+C)=A\cdot B+A\cdot C$
   $(A+B)\cdot C=A\cdot C+B\cdot C$
5. $(A+B)^T=A^T+B^T$
   $(\alpha A)^T = \alpha A^T$
   $(AB)^T=B^TA^T$

---
