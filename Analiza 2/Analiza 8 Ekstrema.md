### Ekstremum
#### 2025-05-25
##### Poprzednia: [[Analiza 7 Rachunek różniczkowy funkcji wielu zmiennych]]
##### Następna: [[Analiza 9 Ekstrema warunkowe]]
##### Zadania: [[Zadania rachunek różniczkowy]]

#rachunek_różniczkowy #ekstrema #funkcje_wielu_zmiennych #analiza2  

---
### Definicja ekstremum lokalnego funkcji wielu zmiennych

$f: D\to \mathbb{R}, \ \ \ D\subset \mathbb{R}^, \ \ \ D-obszar$
Mówimy że $f$ ma maksimum (minimum) lokalne w punkcie $x_0\in D\Leftrightarrow$ istnieje takie otoczenie $U\subset D$ punktu $x_0,$ że: $\forall \overset{x\neq x_0}{x} \in U f(x)\overset{\lt}{\gt} f(x_0)$


**Przykład:**
$f(x,y)=x^2+y^2$
$f$ ma w $(0,0)$ minimum lokalne o wartości $0$
![[newplot (5)-Photoroom.png]]

---
### WK istnienia ekstremum lokalnego

Zał: $f: D\to \mathbb{R}, \ \ \ D\subset \mathbb{R}^n$
$f$ jest różniczkowalna w $x_0\in D$ ($D$ - obszar)
$f$ ma ekstremum lokalne w $x_0$
Teza: $df(x_0)=0 (\Leftrightarrow \forall h \in \mathbb{R}^n \ \ df(x_0)(h)=0)$

**a to oznacza że każda pochodna cząstkowa dla tego punktu ma być równa 0**

$$\begin{gathered}
f(x,y)=x^3-2y^3-3x+6y\\
\frac{\partial f}{\partial x}=3x^2-3=0\\
\frac{\partial f}{\partial y}=-6y^2+6y=0\\\\
\left\{
\begin{matrix}
3x^2=3\\
6y^2=6y
\end{matrix}
\right.\\\\
\left\{
\begin{matrix}
x=1\vee x=-1\\
y=1\vee y=-1
\end{matrix}
\right.
\end{gathered}
$$
![[obraz_2025-05-25_172310099-Photoroom.png]]

---
### Forma kwadratowa

**Formą kwadratową** nazwamy funkcję
$$\begin{gathered}
\varphi(x_1,x_2,\dots,x_n)=a_{11}x_1^2+a_{12}x_1x_2+a_{13}x_1x_3+\dots\\+a_{1n}x_1x_n+a_{21}x_2x_1+a_{22}x_2^2+\dots+a_{2n}x_2x_n+\dots\\+a_{n1}x_nx_1+a{n2}x_nx_2+\dots+a_{nn}x_n^2=[x_1,\dots,x_n]\begin{bmatrix}
a_{11}&a_{12}&\dots&a_{1n}\\
a_{21}&a_{22}&\dots&a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{n1}&a_{n2} & \dots &a_{nn}
\end{bmatrix}
\begin{bmatrix}
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}=\\=X^T \cdot A\cdot X
\end{gathered}$$

gdzie macierz $A$ jest macierzą symetryczą i nazywamy ją macierzą formy kwadratowej.

**Definicja:**

Mówimy, że forma kwadratowa $\varphi$ jest ($h\neq 0$)

- **dodatnio** określona $\Leftrightarrow \forall h \in \mathbb{R}^n \ \ \varphi(h)\gt 0$
- **ujemnie** określona $\Leftrightarrow \forall h \in \mathbb{R}^n \ \ \varphi(h)\lt 0$
- **nieujemnie** określona $\Leftrightarrow \forall h \in \mathbb{R}^n \ \ \varphi(h)\geq 0$
- **niedodatnie** określona $\Leftrightarrow \forall h \in \mathbb{R}^n \ \ \varphi(h)\leq 0$
- **nieokreślona** $\Leftrightarrow \exists h_1\in \mathbb{R}^n \ \ \varphi(h_1)\lt 0 \land \exists h_2\in \mathbb{R}^n \ \ \ \varphi(h_2)\gt 0$

---
### Twierdzenie Sylvestra

Zał: $A=[a_{ij}]^{i=1,\dots,n}_{j=1,\dots,n}$ - **macierz formy kwadratowej $\varphi$**
$$\begin{gathered}
d_k=\det \begin{bmatrix}
a_{11}&\dots &a_{1k}\\
\vdots &\ddots& \vdots\\
a_{k1}&\dots &a_{kk}
\end{bmatrix}, \ \ \ \ k=1,\dots,n
\end{gathered}$$

Teza:
1) $\forall k=1,\dots,n \ \ d_k\gt 0 \implies \varphi$ jest dodatnio określona
2) $\forall k=1,\dots,n \ \ (-1)^kd_k\gt 0 \implies \varphi$ jest ujemnie określona
3) $\forall k=1,\dots,n \ \ d_k\geq 0 \implies \varphi$ jest nieujemnie określona
4) $\forall k=1,\dots,n \ \ (-1)^kd_k\geq 0 \implies \varphi$ jest niedodatnio określona
5) jeśli nie zachodzi ani 3 ani 4 to $\varphi$ jest nieokreślona

---
### Macierz Hessego (macierz formy kwadratowej związana z drugą pochodną)

$f: D\to \mathbb{R} \ \ \ D\subset \mathbb{R}^n$
$f$ jest dwukrotnie różniczkowalna w $x_0$

Macierzą formy kwadratowej związaną z drugą pochodną funkcji $f$ w punkcie $x_0$ nazywamy:

$$\begin{gathered}
M(x_0)=\begin{bmatrix}
\frac{\partial ^ 2 f}{\partial x_1^2}(x_0)&\frac{\partial ^ 2 f}{\partial x_1x_2}(x_0)&\dots & \frac{\partial ^ 2 f}{\partial x_1x_n}(x_0)\\

\frac{\partial ^ 2 f}{\partial x_2 x_1}(x_0)&\frac{\partial ^ 2 f}{\partial x_2^ 2}(x_0)&\dots & \frac{\partial ^ 2 f}{\partial x_2x_n}(x_0)\\

\vdots&\vdots&\ddots & \vdots\\

\frac{\partial ^ 2 f}{\partial x_nx_1}(x_0)&\frac{\partial ^ 2 f}{\partial x_nx_2}(x_0)&\dots & \frac{\partial ^ 2 f}{\partial x_n ^ 2}(x_0)\\
\end{bmatrix}
\end{gathered}$$

**macierzą Hessego.**

---
### WW na istnienie ekstremum lokalnego funkcji wielu zmiennych

Zał: $f: D\to \mathbb{R} \ \ \ D\subset \mathbb{R}^n$, $D$ - obszar,   $x_0\in U \subset D$
$f$ jest $C^2(U)$ (tzn. że wszystkie pochodne cząstkowe 2-go rzędu są ciągłe w $U$)
$f$ spełnia WK na istnienie ekstremum lokalnego w $x_0$ tzn. $\forall i=1,\dots,n \ \ \frac{\partial f}{\partial x_i}(x_0)=0$
Teza: $d_k$ odnosi sie do macierzy formy kwadratowe związanej z drugą pochodną funkcji $f$ czyli $M(x_0)$

1) $\forall k=1,\dots,n \ \ \ d_k\gt 0 \implies f$ ma minimum lokalne w punkcie $x_0$
2) $\forall k=1,\dots,n \ \ \ (-1)^k d_k\gt 0 \implies f$ ma maksimum lokalne w punkcie $x_0$
3) jeśli forma kwadratowa jest nieokreślona w punkcie $x_0$, to $f$ nie ma ekstremum lokalnego w tym punkcie $x_0$
**Uwaga** - z tego nic nie wynika co jeśli $d_k=0$ np w przykładzie 2 poniżej mamy:
$$\begin{gathered}
d_1=-2, d_2=0 \implies (-1)^kd_k\geq 0\implies \text{ niedodatnio określona}\\
\text{Zatem nie wiemy czy ma maksimum czy minimum}
\end{gathered}$$


**Przykład:**
$$\begin{gathered}
f(x,y)=x^2+y^2\\
\frac{\partial f}{\partial x}=2x \ \ \ \frac{\partial f}{\partial y}=2y\\
\frac{\partial^2 f}{\partial x^2}=2 \ \ \ \frac{\partial^2 f}{\partial x \partial y}=0 \ \ \ \frac{\partial^2 f}{\partial y^2}=2 \ \ \ \frac{\partial^2 f}{\partial y \partial x}=0\\\\
M(x,y)=\begin{bmatrix}
2&0\\
0&2
\end{bmatrix}\\\\
M(0,0)=\begin{bmatrix}
2&0\\
0&2
\end{bmatrix}\\\\
d_1=\det[2]=2\gt 0\\
d_2=4\gt 0
\\
\implies f \text{ ma minimum lokalne w punkcie }(0,0)
\end{gathered}$$

**Przykład 2:**
$$\begin{gathered}
f(x,y)=x^3+y^3-x^2-2xy-y^2=x^3+y^3-(x+y)^2\\\\
\frac{\partial f}{\partial x}=3x^2-2x-2y=0\\
\frac{\partial f}{\partial y}=3y^2-2x-2y=0\\
\\\\
\left\{
\begin{matrix}
3x^2-2x-2y=0\\
3y^2-2x-2y=0
\end{matrix}
\right.\\\\
\left\{
\begin{matrix}
3x^2-2x-2y=0\\
3y^2-2x-2y=0
\end{matrix}
\right.\\\\
3x^2-y^2=0\\
(x-y)(x+y)=0\\
(1)x=y\vee (2) x=-y\\\\
(1):\\
3x^2-4x=0\\
x(3x-4)=0\\
(x=0\land y=0)\vee (x=\frac{4}{3}\land y=\frac{4}{3})\\
(2):\\
3x^2=0\implies x=y=0\\\\
\frac{\partial f}{\partial x^2}=6x-2\\
\frac{\partial f}{\partial y^2}=6x-2\\
\frac{\partial f}{\partial x\partial y}=-2\\
\frac{\partial f}{\partial y\partial x}=-2\\
M(x,y)=\begin{bmatrix}
6x-2&-2\\
-2&6y-2\\
\end{bmatrix}\\\\
M(\frac{4}{3},\frac{4}{3})=\begin{bmatrix}
6&-2\\
-2&6\\
\end{bmatrix}\\\\
d_1=6\gt 0\\
d_2=36-4=32\gt 0\\
\implies f \text{ ma minimum lokalne w punkcie }(\frac{4}{3},\frac{4}{3})\\\\
M(0,0)=\begin{bmatrix}
-2&-2\\
-2&-2
\end{bmatrix}\\
d_1=-2\lt 0\\
d_2=0\geq 0\\\\
\text{Z tego nie można wnioskować ani o istnieniu, ani o nieistnieniu ekstremum lokalnego w }\\(0,0)\\
\text{Forma kwadratowa która jest stowarzyszona z macierzą  }M(0,0)\\ \text{ jest niedodatnio określona więc funkcja może mieć maksimum lokalne w punkcie }(0,0)


\end{gathered}$$

$$\begin{gathered}
\text{Jednakże z definicji maksimum: }\\
f \text{ ma maksimum lokalne w punkcie }x_0\in U \Leftrightarrow  \forall x\in U f(x)\lt f(x_0)\\\\
\text{Co by oznaczalo ze zblizajac sie do tego punktu dowolnym sposobem}\\
\text{czyli wzdłuż dowolnego wektora nie znajdziemy punktów większych od 0}\\
f(x,y)\overset{y=-x}{=}-2x^2+2x^2=0\\
\text{Zatem nie spełnione jest że każdy punkt w otoczeniu daje wartosc wiekszą lub mniejszą.}

\end{gathered}$$

![[Pasted image 20250525235358.png]]
$$\ln(1+x^2+y^2)$$

$(x^2-1)^2+(y^2-1)^2$

![[newplot (12)-Photoroom.png]]
![[newplot (9)-Photoroom.png]]

---
