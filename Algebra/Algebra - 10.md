### Układy równań
#### 2024-12-15
##### Poprzednia: [[Algebra - 9]]
##### Następna: [[Algebra - 11]]
##### Zadania: [[]]

#uklady_rownan #algebra 

--- 
### Układ równań liniowych

**Definicja**:

Układ m równań liniowych z n niewiadomymi ma postać:
$$\begin{gathered}
(*)
\left\{
\begin{matrix}
\textcolor{lightgreen}{a_{11}}x_1+\textcolor{lightgreen}{a_{12}}x_2+\dots+\textcolor{lightgreen}{a_{1n}}x_n=\textcolor{orange}{b_1}\\
\textcolor{lightgreen}{a_{21}}x_1+\textcolor{lightgreen}{a_{22}}x_2+\dots+\textcolor{lightgreen}{a_{2n}}x_n=\textcolor{orange}{b_2}\\
\textcolor{lightgreen}{a_{31}}x_1+\textcolor{lightgreen}{a_{32}}x_2+\dots+\textcolor{lightgreen}{a_{3n}}x_n=\textcolor{orange}{b_3}\\
\dots\\
\textcolor{lightgreen}{a_{m1}}x_1+\textcolor{lightgreen}{a_{m2}}x_2+\dots+\textcolor{lightgreen}{a_{mn}}x_n=\textcolor{orange}{b_m}\\
\end{matrix}
\right.,\ \ \ gdzie:\\
\\
a_{ij}- wspolczynniki \ (dane - ustalone)\\
b_{i}- wyrazy \ wolne \ (dane - ustalone)\\
x_j - niewiadome/zmienne \ (szukane)\\
rozwiazanie - \ kazda \ n-ka \ (elementow \ z \ ciala \ \ \mathbb{K}) \ x_1,x_2,\dots,x_n\\
spelniajacych \ wszystkie \ rownania \ ukladu \ (*)
\end{gathered}$$

---

Macierz 
$$
\begin{gathered}A=
\begin{bmatrix}
\textcolor{lightgreen}{a_{11}}
&\textcolor{lightgreen}{a_{12}}&\dots & \textcolor{lightgreen}{a_{1n}}\\
\textcolor{lightgreen}{a_{21}}&\textcolor{lightgreen}{a_{22}}& \dots & \textcolor{lightgreen}{a_{2n}}\\
\vdots & \vdots & \ddots&\vdots\\
\textcolor{lightgreen}{a_{m1}}&\textcolor{lightgreen}{a_{m2}}& \dots & \textcolor{lightgreen}{a_{mn}}\\
\end{bmatrix}
\end{gathered}$$
nazywamy *macierzą współczynników (macierzą główną)* układu (\*),

Macierz
$$\begin{gathered}
B=
\begin{bmatrix}
\textcolor{orange}{b_1}\\
\textcolor{orange}{b_2}\\
\vdots\\
\textcolor{orange}{b_m}
\end{bmatrix}
\end{gathered}$$

nazywamy *macierzą (kolumną) wyrazów wolnych*, a macierz:

$$\begin{gathered}\
[A|B]=
\begin{bmatrix}
\begin{array}{cccc|c}
\textcolor{lightgreen}{a_{11}}
&\textcolor{lightgreen}{a_{12}}&\dots&\textcolor{lightgreen}{a_{1n}}&\textcolor{orange}{b_1}\\
\textcolor{lightgreen}{a_{21}}&\textcolor{lightgreen}{a_{22}}&\dots&\textcolor{lightgreen}{a_{2n}}&\textcolor{orange}{b_2}\\
\vdots & \vdots & \ddots & \vdots & \vdots\\
\textcolor{lightgreen}{a_{m1}}
&\textcolor{lightgreen}{a_{m2}}&\dots & \textcolor{lightgreen}{a_{mn}}&\textcolor{orange}{b_m}
\end{array}
\end{bmatrix}
\end{gathered}$$
nazywamy *macierzą uzupełnioną układu* (\*).

---
### Zapis macierzowy układu

*Układ* (\*) zapisujemy *macierzowo* jako:
$$\begin{gathered}
A \cdot X = B
\end{gathered}$$
gdzie:
$$\begin{gathered}
X=\begin{bmatrix}
x_1\\x_2\\\vdots \\x_n
\end{bmatrix}
\end{gathered}$$
jest *macierzą (kolumną) niewiadomych*.
$$\begin{gathered}
A \cdot X = B \Leftrightarrow\\\\
\begin{bmatrix}
\textcolor{lightgreen}{a_{11}}
&\textcolor{lightgreen}{a_{12}}&\dots & \textcolor{lightgreen}{a_{1n}}\\
\textcolor{lightgreen}{a_{21}}&\textcolor{lightgreen}{a_{22}}& \dots & \textcolor{lightgreen}{a_{2n}}\\
\vdots & \vdots & \ddots&\vdots\\
\textcolor{lightgreen}{a_{m1}}&\textcolor{lightgreen}{a_{m2}}& \dots & \textcolor{lightgreen}{a_{mn}}\\
\end{bmatrix}\cdot \begin{bmatrix}
x_1\\x_2\\\vdots \\x_n
\end{bmatrix}=
\begin{bmatrix}
\textcolor{orange}{b_1}\\
\textcolor{orange}{b_2}\\
\vdots\\
\textcolor{orange}{b_m}
\end{bmatrix}
\end{gathered}$$
---

**Definicja**:
Jeżeli wszystkie wyrazy wolne układu (\*) są zerami, tj:
$$\begin{gathered}
b_1=b_2=\dots =b_m=0  \ (B=\overline{0})
\end{gathered}$$

to taki układ nazywamy *jednorodnym*. W przeciwnym wypadku, tj. gdy choć jeden wyraz wolny jest różny od zera, to taki układ nazywamy *niejednorodnym*.

---

**Definicja**:
Układ (\*) nazywamy:
1. *oznaczonym*, jeżeli ma dokładnie jedno rozwiązanie
2. *nieoznaczonym*, jeżeli ma więcej niż 1 rozwiązanie
3. *sprzecznym*, jeżeli nie ma rozwiązań

---
### Układy kwadratowej

**Definicja**:
Jeżeli w układzie (\*) liczba niewiadomych jest równa liczbie równań ($m=n \Leftrightarrow A$ jest macierzą kwadratową), to nazywamy go *układem kwadratowym*.

---
**Definicja**:
Układ (\*) nazywamy *układem Cramera*, jeżeli jest *układem kwadratowym* i $\det A \neq 0$.

---
### Twierdzenie Cramera

Jeśli układ (\*) jest *układem Cramera*, to:
1. ma *dokładnie jedno* rozwiązanie
2. jedyne jego rozwiązanie wyraża się następującymi *wzorami Cramera*
   
   $x_j=D_{xj}\cdot \frac{1}{\det A}, \ \ j=1,2,\dots,n$
   gdzie $D_{xj}$ jest *wyznacznikiem* macierzy powstałej z $A$ poprzez *zastąpienie j-tej kolumny* przez *kolumne wyrazów wolnych*.

**Przykład**:
$$\begin{gathered}
\left\{
\begin{bmatrix}
x-3y+z=0\\
x-4y+z=-3\\
-2x+6y-z=-7\\
\end{bmatrix}
\right.\\\\\\
A=\begin{bmatrix}
1&-3&1\\
1&-4&1\\
-2&6&-1
\end{bmatrix}\ \ \ 
B=\begin{bmatrix}
0\\
-3\\
-7
\end{bmatrix}\\\\
\det A = \begin{vmatrix}
1&-3&1\\
1&-4&1\\
-2&6&-1
\end{vmatrix}=
4+6+6-8-3-6=-1\neq 0\\\\
D_x=\begin{bmatrix}
0&-3&1\\
-3&-4&1\\
-7&6&-1
\end{bmatrix}=
21-18-28+9=-16\\\\
D_y=\begin{bmatrix}
1&0&1\\
1&-3&1\\
-2&-7&-1
\end{bmatrix}=
3-7-6+7=-3\\\\
D_z=\begin{bmatrix}
1&-3&0\\
1&-4&-3\\
-2&6&-7
\end{bmatrix}=
28-18-21=7\\\\
x=\frac{-16}{-1}=16, \ \ y=\frac{-3}{-1}=3, \ \ z=\frac{7}{-1}=-7\\
\left\{
\begin{matrix}
x=16\\
y=3\\
z=-7
\end{matrix}
\right.
\end{gathered}$$
---
### Twierdzenie Kroneckera-Capellego

Układ
$$\begin{gathered}
(*) \ AX=B
\end{gathered}$$
ma *co najmniej 1 rozwiązanie* wtedy i tylko wtedy, gdy $r(A)=r([A|B])$.

---
**Wniosek**:
Układ (\*) jest sprzeczny $\Leftrightarrow r(A)\neq r([A|B])$

---
**Twierdzenie**:
- Układ (\*) ma *dokładnie 1 rozwiązanie* $\Leftrightarrow$, gdy $r(A)=r([A|B])=n$, gdzie n jest liczbą niewiadomych
- Jeżeli $r(A)=r([A|B])=r$, gdzie $r\lt n$ to układ (\*) jest *nieoznaczony* i ma rozwiązania zależne od *n-r parametrów*.
---
**Uwaga**: 
Układ jednorodny ma zawsze przynajmniej jedno rozwiązanie, $X=\overline{0}, \ \ (x_1=x_2=\dots=x_n=0)$, zatem jest oznaczony lub nieoznaczony.

---
**Intuicja**:
$$\begin{gathered}
\left\{
\begin{matrix}
a_{11}x_1+a_{12}x_2+\dots +a_{1n}x_n=0\\
a_{21}x_1+a_{22}x_2+\dots +a_{2n}x_n=0\\
\dots\\
a_{m1}x_1+a_{m2}x_2+\dots +a_{mn}x_n=0\\
\end{matrix}
\right.\\\\
Jedno \ z \ mozliwych \ rozwiazan \ bedzie \ zawsze \ \ x_1=x_2=\dots=x_n=0
\end{gathered}$$
---
**Uwaga**:
Jeżeli mamy dany układ *kwadratowy* (\*) rozmiaru $n\times n$, dla którego:
1. $\det A =0$ oraz dla pewnego $j\in \{1,\dots,n\}, \ \ D_{xj}\neq 0$ to jest on *sprzeczny*
2. $\det A=0=D_{x1}=\dots=D_{xn}$ to jest on *nieoznaczony* albo *sprzeczny*
---
### Rozwiązywanie układów równań metodą Gaussa

**Uwaga**:
Układy równań można rozwiązywać używając *metody Gaussa*, polegającej na stosowaniu do (wierszy) macierzy $\ [A|B]$ *operacji elementarnych* w celu sprowadzenia jej do *postaci schodkowej*.


**Przykład**:
$$\begin{gathered}
\left\{
\begin{matrix}
x+y+z=0\\
2x-y-z=-3\\
4x-5y-3z=-7
\end{matrix}
\right.\\\\
\begin{bmatrix}
\begin{array}{ccc|c}
1&1&1&0\\
2&-1&-1&-3\\
4&-5&-3&-7
\end{array}
\end{bmatrix}\to 
\begin{bmatrix}
\begin{array}{ccc|c}
1&1&1&0\\
0&-3&-3&-3\\
0&-9&-7&-7
\end{array}
\end{bmatrix}\to 
\begin{bmatrix}
\begin{array}{ccc|c}
1&1&1&0\\
0&-3&-3&-3\\
0&0&2&2
\end{array}
\end{bmatrix}\\\\ r(A)=3=r([A|B])=n \ \ \ \ Uklad \ jest \ oznaczony\\\\
\left\{
\begin{matrix}
x+y+z=0\\
-2y-3z=-3\\
2z=2\\
\end{matrix}
\right. \ \ \ 
\left\{
\begin{matrix}
x=-1\\
y=0\\
z=1\\
\end{matrix}
\right.
\end{gathered}$$
---
### Metoda macierzy odwrotnej:

Metodę macierzy odwrotnej stosujemy jako jeden z sposobów na rozwiązanie układu równań. Polega ona na tym że po pewnym przekształceniu równania układu otrzymamy wzór na macierz niewiadomych.

$$\begin{gathered}
\text{Mając układ równań zapisany macierzowo:}\\\\

A\cdot X=B\\\\
\text{Mnożymy go od lewej strony przez }A^{-1}\\
A^{-1}AX=A^{-1}B\\
IX=A^{-1}B\\
X=A^{-1}B\\
\end{gathered}$$

**Przykład:**

$$\begin{gathered}
\left\{
\begin{matrix}
x+y=3\\
2x+3y=7
\end{matrix}
\right.\\\\
A=\begin{bmatrix}
1&1\\
2&3
\end{bmatrix}, \ X=
\begin{bmatrix}
x\\
y
\end{bmatrix}, \ B=
\begin{bmatrix}
3\\
7
\end{bmatrix}\\\\
\det(A)=3-2=1\neq 0 \text{ zatem istnieje macierz odwrotna}\\\\
\begin{bmatrix}
\begin{array}{cc|cc}
1&1&1&0\\
2&3&0&1
\end{array}
\end{bmatrix}\to
\begin{bmatrix}
\begin{array}{cc|cc}
1&1&3&-1\\
0&1&-2&1
\end{array}
\end{bmatrix}, \ \ \ A^{-1}=\begin{bmatrix}
3&-1\\
-2&1
\end{bmatrix}\\\\
X=A^{-1}B=\begin{bmatrix}
3&-1\\
-2&1
\end{bmatrix}
\begin{bmatrix}
3\\
7
\end{bmatrix}=\begin{bmatrix}
2\\
1
\end{bmatrix}
\end{gathered}
$$

---
