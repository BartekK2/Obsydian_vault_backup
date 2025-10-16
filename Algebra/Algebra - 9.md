### Wyznacznik macierzy, rząd macierzy, macierz odwrotna
#### 2024-12-14
##### Poprzednia: [[Algebra - 8]]
##### Następna: [[Algebra - 10]]
##### Zadania: [[]]

#macierze #algebra #wyznacznik_macierzy #rząd_macierzy #macierz_odwrotna

--- 
## Wyznacznik macierzy

### Oznaczenie

Wyznacznik macierzy oznacza się $\det A$ lub:
$$\begin{gathered}
\begin{vmatrix}
     a_{11} & a_{12} & a_{13}\\ 
     a_{21} & a_{22} & a_{23}\\
     a_{31} & a_{32} & a_{33} 
\end{vmatrix}
\end{gathered}$$
Czyli pionowe kreski zamiast nawiasów kwadratowych.

---
### Metoda Sarrusa
Wyznacznik macierzy $A=[a_{ij}]_{2\times 2}=a_{11}a_{22}-a_{12}a_{21}$
Dla macierzy $3\times 3$.
$$\begin{gathered}
\begin{vmatrix}
	a_{11} & a_{12} & a_{13}\\ 
	a_{21} & a_{22} & a_{23}\\
	a_{31} & a_{32} & a_{33} 
\end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{12}a_{21}a_{33}-a_{11}a_{23}a_{32}
\end{gathered}$$
Czyli przekątne z lewej do prawej minus przekątne z prawej do lewej z doklejeniem macierzy jeśli przekątna wyjdzie poza macierz tzn.

$$\begin{gathered}
\begin{vmatrix}
	a_{11} & a_{12} & a_{13}\\ 
	a_{21} & a_{22} & a_{23}\\
	a_{31} & a_{32} & a_{33} 
\end{vmatrix}

\begin{vmatrix}
	a_{11} & a_{12} & a_{13}\\ 
	a_{21} & a_{22} & a_{23}\\
	a_{31} & a_{32} & a_{33} 
\end{vmatrix}

\begin{vmatrix}
	a_{11} & a_{12} & a_{13}\\ 
	a_{21} & a_{22} & a_{23}\\
	a_{31} & a_{32} & a_{33} 
\end{vmatrix}
\end{gathered}$$
---
**Permutacje**

Dwa elementy permutacji $\sigma(i), \sigma(j)$ tworzą *inwersję* jeżeli $i \lt j, \land \ \sigma(i)\gt \sigma(j)$ 

Liczbę inwersji w permutacji $\sigma$ oznaczamy przez $[\sigma]$, a *znak permutacji* jako $\epsilon(\sigma)=(-1)^{[\sigma]}$.
Permutację nazywamy *parzystą* jeśli $\epsilon(\sigma)=1$ i *nieparzystą* jeśli $\epsilon(\sigma)=-1$.

$$\begin{gathered}

\det A = \sum_{\sigma \in S_n}{\epsilon(\sigma)\cdot a_{1\sigma(1)}\cdot a_{2\sigma(2)}\dots a_{n\sigma(n)}}
\end{gathered}
$$
---
### Własności wyznaczników
1. $\det A^T=A$
2. $\det I=1$
3. Jeżeli któraś z kolumn/wierszy jest wypełniona samymi zerami to $\det A=0$
4. $\det[k_1,\dots,k_i'+k_i'',\dots,k_n]=\det[k_1,\dots,k_i',\dots,k_n]+\det[k_1,\dots,k_i'',\dots,k_n]$
Przykład:
   $$\begin{gathered}
	A=
	\begin{bmatrix}
	1&(2+3)\\
	4&(5+6)
	\end{bmatrix}
	\end{gathered}$$
Druga kolumna to suma $k_i' \ i \ k_i''$, gdzie:
$$\begin{gathered}
k_i'=\begin{bmatrix}
2\\
5
\end{bmatrix},\ \ \
k_i''=\begin{bmatrix}
3\\
6
\end{bmatrix},\ \ \
\end{gathered}$$
Wzór mówi, że:
$$\begin{gathered}
\det
\begin{bmatrix}
1&(2+3)\\
4&(5+6)
\end{bmatrix}=
\det
\begin{bmatrix}
1&2\\
4&5
\end{bmatrix}+
\det
\begin{bmatrix}
1&3\\
4&6
\end{bmatrix}
\end{gathered}$$
5. Analogicznie w przypadku wierszy
6. Jeżeli *pomnożymy* wiersz/kolumne przez skalar $\alpha$, wówczas wyznacznik tej nowej macierzy to $\alpha \cdot \det A$
7. Wniosek z poprzedniego: $\det(\alpha A)=\alpha^n\det A$
8. Przestawienie dwóch wierszy/kolumn macierzy zmienia znak wyznacznika na przeciwny.
9. Wniosek z poprzedniej własności - jeśli macierz ma dwa takie same wiersze/kolumny to $\det A=0$
10. Wartość wyznacznika nie zmieni się, jeżeli do wiersza/kolumny dodamy kombinacje liniową pozostałych wierszy/kolumn.

---
### Twierdzenie Cauchy'ego
Dla dowolnych macierzy $A,B \in M_{n\times n}(K)$ zachodzi:
$$\begin{gathered}
\det(A\cdot B)=det A \cdot det B
\end{gathered}$$
---
### Minory

Minorem stopnia k macierzy $A_{m\times n}$ nazywamy *wyznacznik* dowolnej *(pod)macierzy kwadratowej wymiaru* $k\times k, k\leq min\{m,n\}$ powstałej z macierzy A poprzez wykreślenie z niej $n-k$ kolumn i $m-k$ wierszy.

Przykład:
$$\begin{gathered}
A=\begin{bmatrix}
0&2&-3&5\\
1&-2&4&-5\\
-1&3&-4&6
\end{bmatrix}\\\\
A'=\begin{bmatrix}
0&2\\
1&-2\\
\end{bmatrix}\\\\
Minor \ to \ \det A'
\end{gathered}$$
Jeżeli $A=[a_{ij}]_{n\times n}$ jest macierzą kwadratową, to wyznacznik macierzy powstałej poprzez wykreślenie z $A$ i-tego wiersza i j-tej kolumny nazywamy *minorem macierzy A odpowiadającym elementowi* $a_{ij}$ i oznaczamy przez $M_{ij}$ są to minory stopnia $(n-1)$ macierzy $A$.
$$\begin{gathered}
A=\begin{bmatrix}
2&2&-3&4\\
2&1&-6&9\\
2&1&\textcolor{lightgreen}{-5}&2\\
8&4&-3&7\\
\end{bmatrix}\\\\
A'=\begin{bmatrix}
2&2&4\\
2&1&9\\
8&4&7\\
\end{bmatrix}\\\\
\det A'
\end{gathered}$$
---
### Twierdzenie Laplace'a


#### Dopełnienie algebraiczne

Dopełnieniem algebraicznym elementu $a_{ij}$ macierzy kwadratowej $A=[a_{ij}]_{n\times n}$ nazywamy liczbę (skalar).
$$\begin{gathered}
A_{ij}=(-1)^{i+j}M_{ij}
\end{gathered}$$
Czyli $\pm$ minora macierzy $A$ odpowiadającemu elementami $a_{ij}$.

**Twierdzenie:**
Założenia: $A=[a_{ij}] \in M_{n\times n}(K)$ 
$A$ to macierz kwadratowa.

Twierdzenie:
$\forall j \in \{1,\dots,n\}: \det A=a_{1j}A_{1j}+a_{2j}A_{2j}+\dots+a_{nj}A_{nj}$$\forall i \in \{1,\dots,n\}: \det A=a_{i1}A_{i1}+a_{i2}A_{i2}+\dots+a_{in}A_{in}$

*Przykład:*
$$\begin{gathered}
j=3\\
\begin{vmatrix}
1&1&\textcolor{lightgreen}{0}&0\\
0&1&\textcolor{lightgreen}{1}&0\\
0&0&\textcolor{lightgreen}{1}&1\\
1&0&\textcolor{lightgreen}{0}&1\\
\end{vmatrix}
=0\cdot (-1)^{1+3}\cdot \begin{vmatrix}
0&1&0\\
0&0&1\\
1&0&1\\
\end{vmatrix}+1\cdot (-1)^{2+3}\cdot
\begin{vmatrix}
1&1&0\\
0&0&1\\
1&0&1\\
\end{vmatrix}
+\dots+0\cdot (-1)^{4+3}\cdot
\begin{vmatrix}
1&1&0\\
0&1&0\\
0&0&1\\
\end{vmatrix}
\end{gathered}$$

**Ważny wniosek:**
Wyznacznik macierzy trójkątnej górnej (dolnej) jest równy iloczynowi elementów na przekątnej głównej.

---
## Rząd macierzy

**Twierdzenie:**

*Maksymalna liczba liniowo niezależnych kolumn* dowolnej macierzy $A\in M_{m\times n}(\mathbb{K})$ jest równa *maksymalnej liczbie liniowo niezależnych wierszy* tej macierzy.

*Rzędem macierzy* $A=[a_{ij}]_{m\times n}$ nazywamy *maksymalną liczbę jej liniowo niezależnych kolumn* (lub *wierszy*).

Wniosek: 
Jeżeli $A\in M_{m\times n}$ to
1. $r(A)\leq min\{m,n\}$, no bo maksymalnie niezależne mogą być tyle ile ich jest kolumn/wierszy minimum
2. $r(A^T)=r(A)$, bo na to samo wychodzi jak sie macierz odwróci bo sie zamienia wiersze na kolumny
---
### Postać schodkowa macierzy

*Definicja:* Mówimy, że macierz $A$ ma *postać schodkową*, jeżeli wszystkie jej niezerowe wiersze występują kolejno (jeden pod drugim), począwszy od pierwszego, a pierwsze niezerowe elementy (tzw. *schodki*) w kolejnych niezerowych wierszach tej macierzy znajdują się w kolumnach o rosnących numerach (lub $A$ jest macierzą zerową).

**Przykład:**
$$\begin{gathered}
\begin{bmatrix}
0&|\underline{-1}&3&-1&1&0\\
0&0&|\underline{1}&\underline{1}&0&-1\\
0&0&0&0&|\underline{2}&\underline{1}\\
0&0&0&0&0&0\\
\end{bmatrix}
\end{gathered}$$

*Uwaga:* *Rząd* macierzy w postaci schodkowej *równy* jest *liczbie* jej *schodków*.
W tym przypadku $r(A)=3$.

---
### Operacje elementarne

*Definicja*: Następujące przekształcenia nazywamy *operacjami elementarnymi* na macierzach:
1. *zamiana* miejscami *wierszy* (*kolumn*) macierzy
2. *dodanie* do wiersza (kolumny) kombinacji liniowej *pozostałych wierszy* (odpowiednio: kolumn)
3. *pomnożenie* wiersza (kolumny) przez *skalar* $\alpha \neq 0$

Rząd macierzy *nie zmienia się* pod wpływem operacji elementarnych wykonanych na wierszach bądź kolumnach. 
No bo czemu miałby się zmienić skoro mowa o liniowo niezależnych wierszach/kolumnach.

---
### Algorytm Gaussa

*Uwaga*: Każdą macierz $A$ można doprowadzić do postaci schodkowej $B$ za pomocą operacji elementarnych stosując *algorytm Gaussa* na wierszach (wówczas $r(A)=r(B)$).

*Przykład:*
$$\begin{gathered}
\begin{bmatrix}
0&0&0&0&2&1\\
0&-1&3&-1&1&0\\
0&-2&7&-1&2&-1\\
0&1&0&4&-5&-5\\

\end{bmatrix}\overset{\implies}{w_1\Leftrightarrow w_2}
\begin{bmatrix}
0&-1&3&-1&1&0\\
0&0&0&0&2&1\\
0&-2&7&-1&2&-1\\
0&1&0&4&-5&-5\\

\end{bmatrix}\overset{\implies}{w_3- 2w_1, w_4+w_1}\\\\
\begin{bmatrix}
0&-1&3&-1&1&0\\
0&0&0&0&2&1\\
0&0&1&1&0&-1\\
0&0&3&3&-4&-5\\
\end{bmatrix}
\overset{\implies}{w_2\Leftrightarrow w_3}
\begin{bmatrix}
0&-1&3&-1&1&0\\
0&0&1&1&0&-1\\
0&0&0&0&2&1\\
0&0&3&3&-4&-5\\
\end{bmatrix}
\overset{\implies}{w_4-3w_2}
\\\\
\begin{bmatrix}
0&-1&3&-1&1&0\\
0&0&1&1&0&-1\\
0&0&0&0&2&1\\
0&0&0&0&-4&-2\\
\end{bmatrix}
\overset{\implies}{w_4+2w_3}
\begin{bmatrix}
0&-1&3&-1&1&0\\
0&0&1&1&0&-1\\
0&0&0&0&2&1\\
0&0&0&0&0&0\\
\end{bmatrix}\\\\
3=r(B)=r(A)
\end{gathered}$$

*Twierdzenie*: 

*Rząd* dowolnej macierzy $A$ jest równy *największemu ze stopni minorów niezerowych* tej macierzy.

---
## Macierz odwrotna

**Definicja**: Niech $A$ będzie macierzą kwadratową. Macierz (kwadratową) $B$ taką, że $A\cdot B=B\cdot A=I$, nazywamy *macierzą odwrotną* do macierzy $A$. Jeżeli taka macierz istnieje, to oznaczamy ją przez $A^{-1}$, a $A$ nazywamy macierzą *odwracalną*.

*Uwaga*: Macierz odwrotna do danej macierzy, o ile istnieje, jest jednoznacznie określona.

*Twierdzenie*: 
Jeżeli $A_{n\times n}$ jest macierzą odwracalną, to:
1. $\det A\neq 0 \  \ \land \ \ \det(A^{-1})=(\det A)^{-1}$
2. $A^{-1}=(\det A)^{-1} \ (A^D)^T$, 
   gdzie $A^D$ jest *macierzą dopełenień algebraicznych* macierzy $A$. 

**Przykład**:
$$\begin{gathered}
A=
\begin{bmatrix}
2&-3&-1\\
1&-1&0\\
2&0&1\\
\end{bmatrix}
\ \ \det A=-2-2+3=-1\neq 0\implies A- \ odwracalna\\\\
A^D=
\begin{bmatrix}
-1&-1&2\\
3&4&-6\\
-1&-1&1\\
\end{bmatrix}\\\\
A^{-1}=\frac{1}{\det A}\cdot (A^D)^T=-1\cdot 
\begin{bmatrix}
-1&3&-1\\
-1&4&-1\\
2&-6&1
\end{bmatrix}=
\begin{bmatrix}
1&-3&1\\
1&-4&1\\
-2&6&-1
\end{bmatrix}
\end{gathered}$$
---

**Definicja**: Macierz kwadratową $A$ nazywamy *osobliwą*, jeżeli $\det A=0$, lub *nieosobliwą*, jeżeli $\det A\neq 0$.

**Wniosek**: Macierz $A_{n\times n}$ jest *nieosobliwa* (*odwracalna*) wtedy i tylko wtedy gdy $r(A)=n$.

**Twierdzenie**: Własności macierzy odwrotnej
Niech $A,B, \in M_{n\times n}(\mathbb{K})$ będą macierzami *nieosobliwymi*, $\alpha \in \mathbb{K}$, $\alpha \neq 0$. Wówczas $A^{-1}, A^T, \alpha A, AB, A^n$ dla $n=1,2,\dots,$ też są nieosobliwe, oraz:

1. $\det (A^{-1})=(\det A)^{-1}$ 
2. $(A^{-1})^{-1}=A$ 
3. $(A^T)^{-1}=(A^{-1})^T$ 
4. $(\alpha A)^{-1} = \alpha^{-1}A^{-1}$
5. $(AB)^{-1}=B^{-1}A^{-1}$
6. $(A^n)^{-1}=(A^{-1})^n$

**Uwaga**: Do znalezienia macierzy odwrotnej do danej można wykorzystać *algorytm Gaussa* opierający się na operacjach elementarnych wykonywanych na wierszach.

*Przykład*: Znajdź macierz odwotną do:
$$\begin{gathered}
A=\begin{bmatrix}
2&-3&-1\\
1&-1&0\\
2&0&1
\end{bmatrix}
\end{gathered}$$

$$\begin{gathered}
\begin{bmatrix}
\begin{array}{ccc|ccc}
2&-3&1&1&0&0\\
1&-1&0&0&1&0\\
2&0&1&0&0&1\\
\end{array}
\end{bmatrix}
\overset{\implies}{w_2-\frac{1}{2}w_1, w_3-w_1}
\begin{bmatrix}
\begin{array}{ccc|ccc}
2&-3&-1&1&0&0\\
0&\frac{1}{2}&\frac{1}{2}&-\frac{1}{2}&1&0\\
0&3&2&-1&0&1\\
\end{array}
\end{bmatrix}
\overset{\implies}{\frac{1}{2}w_1, 2\cdot w_2}\\\\
\begin{bmatrix}
\begin{array}{ccc|ccc}
1&\frac{-3}{2}&-\frac{1}{2}&\frac{1}{2}&0&0\\
0&1&1&-1&2&0\\
0&3&2&-1&0&1\\
\end{array}
\end{bmatrix}
\overset{\implies}{w_3-3w_2}
\begin{bmatrix}
\begin{array}{ccc|ccc}
1&\frac{-3}{2}&-\frac{1}{2}&\frac{1}{2}&0&0\\
0&1&1&-1&2&0\\
0&0&-1&2&-6&1\\
\end{array}
\end{bmatrix}
\overset{\implies}{w_1-\frac{1}{2}w_3, w_2+w_3}\\\\
\begin{bmatrix}
\begin{array}{ccc|ccc}
1&\frac{-3}{2}&0&\frac{1}{2}&3&-\frac{1}{2}\\
0&1&0&1&-4&1\\
0&0&-1&2&-6&1\\
\end{array}
\end{bmatrix}
\overset{\implies}{w_1+\frac{3}{2}w_2,(-1)\cdot w_3}\\\\
\begin{bmatrix}
\begin{array}{ccc|ccc}
1&0&0&1&-3&1\\
0&1&0&1&-4&1\\
0&0&1&-2&6&-1\\
\end{array}
\end{bmatrix}\\\\
A^{-1}=\begin{bmatrix}
1&-3&1\\
1&-4&1\\
-2&6&-1\\
\end{bmatrix}
\end{gathered}$$

---

Można też poprzez rozwiązanie układu równań z macierzy tzn:
$$\begin{gathered}
\left\{
\begin{matrix}
x-31y+10z=3\\
4x+6y+4z=9\\
78x+2y+4z=-2\\
\end{matrix}
\right.\implies 
\left\{
\begin{matrix}
x=\dots\\
y=\dots\\
z=\dots
\end{matrix}
\right.
\end{gathered}$$
---
