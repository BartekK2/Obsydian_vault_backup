
### Macierz odwzorowania liniowego
#### 2025-01-30
##### Poprzednia: [[Algebra - 12]]
##### Następna: [[]]
##### Zadania: [[]]

#macierze #macierz_odwzorowania #algebra 

---
### Definicja 

Niech $B_v=(e_1,e_2,\dots,e_n), B_W=(I_1,I_2,\dots,I_m)$ będą (ustalonymi) bazami (reperami bazowymi) przestrzeni wektorowych, $V$ i $W$ nad tym samym ciałem $K$ (więc $\dim V=n, \dim W=m$). Niech $f: V\to W$ będzie odwzorowaniem liniowym, gdzie:
$$\begin{gathered}
f(e_1)=a_{11}I_1+a_{21}I_2+\dots+a_{m1}I_m\\
f(e_2)=a_{12}I_1+a_{22}I_2+\dots+a_{m2}I_m\\
\dots 
\end{gathered}$$

**Macierzą odwzorowania liniowego** $f$ w bazach $B_V,B_W$ nazywamy macierz:
$$\begin{gathered}
M_f(B_V,B_W):=[a_{ij}]_{m\times n}=\begin{bmatrix}
a_{11}&a_{12}&\dots &a_{1n}\\
a_{21}&a_{22}&\dots& a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}&a_{m2}&\dots & a_{mm}
\end{bmatrix}
\end{gathered}$$
---
**Def.** Niech $f: V \to W$ będzie odwzorowaniem liniowym, a $B_V=(e_1,e_2,\dots, e_n), B_W=(I_1,I_2,\dots,I_m)$ pewnymi (ustalonymi) bazami przestrzeni, odp. $V$ i $W$:

Niech $y=f(x)$, gdzie $x\in V, y\in W$ oraz:
$$\begin{gathered}
x=[x_1,x_2,\dots,x_n]_{B_{V}}, y=[y_1,y_2,\dots,y_m]_{B_{W}}
\end{gathered}$$
Równanie macierzowe:
$$\begin{gathered}
\begin{bmatrix}
y_1\\
y_2\\
\vdots\\
y_m
\end{bmatrix}=
\begin{bmatrix}
a_{11}&a_{12}&\dots &a_{1n}\\
a_{21}&a_{22}&\dots& a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}&a_{m2}&\dots & a_{mm}
\end{bmatrix}
\begin{bmatrix}
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}
\end{gathered}$$
gdzie A jest macierzą odwzorowania $f$ w bazach $B_V,B_W$ nazywamy **macierzową postacią odwzorowania liniowego**.

Przyjmując oznaczenia: 
$$\begin{gathered}
X=\begin{bmatrix}
y_1\\
y_2\\
\vdots\\
y_m
\end{bmatrix}, \ Y=\begin{bmatrix}
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}
\end{gathered}$$
gdzie $X$, $Y$ są kolumnowymi macierzami (wektorami) współrzędych wektorów $x,y$ w odpowiednich bazach, możemy równanie zapisać w postaci:
$$\begin{gathered}
Y=AX
\end{gathered}$$

**Uwaga:**
Przy ustalonych bazach w przestrzeniach $V$ i $W$, danemu **odwzorowaniu liniowemu** odpowiada **dokładnie jedna macierz** spełniająca powyższe równanie dla wszystkich $x,y$ 

**Przykład:**

$$\begin{gathered}
f: \mathbb{R}^3 \to \mathbb{R}^2: \ f(x_1,x_2,x_3)=(x_1-x_2+2x_3, -x_1+3x_3)\\
B_1'=((1,1,1),(1,1,0),(1,0,0)), \ B_2'=((1,2),(2,1))
\end{gathered}$$

Wyznacz macierz odwzorowania $f$ w bazach $B_1', B_2'$

$$\begin{gathered}
f(e_1)=f((1,1,1))=(2,2)\ \ \\\\
 a_{11}(1,2)+a_{21}(2,1)=\\\\
\left\{
\begin{matrix}
b=\frac{2}{3}\\
a=\frac{1}{3}
\end{matrix}
\right.
\end{gathered}$$
Korzystając z macierzy $M_f$ wyznacz wartość odwzorowania $f$ dla $x=(1,2,1)$

$$\begin{gathered}
\begin{bmatrix}
y_1\\
y_2\\

\end{bmatrix}=AX
\end{gathered}$$

---
**Def.**
**Macierzą endomorfizmu** $f: V\to V$ w bazie B (przestrzeni V) nazywamy macierz $M_f(B)=M_f(B,B)$


**Twierdzenie**:
Niech $f: V\to W$ będzie odwzorowaniem liniowym $B_V, B_W$ dowolnymi ustalonymi bazami przestrzeni $V,W$ i niech $A=M_f(B_V,B_W)$ Wówczas:
$$\begin{gathered}
r(f)=r(A), r(f)=\dim Imf
\end{gathered}$$
**Wniosek:**
Rzędy macierzy tego samego odwzorowania ale w różnych bazach są takie same.
$$\begin{gathered}
M_{f+g}=M_f+M_g\\
M_{\alpha f}=\alpha M_f
\end{gathered}$$
---
### Macierz przejścia

**Def.**
**Macierzą przejścia** $P_{B\to B'}$ od (starej) bazy $B=(e_1,e_2,\dots, e_n)$ do nowej bazy $B'=(e_1',e_2',\dots, e_n')$ przestrzeni wektorowej $V$ nazywamy macierz odwzorowania identycznościowego przestrzeni $V$ w bazach $B',B$ tj:
$$\begin{gathered}
P_{B\to B'}=M_{Idv}(B',B)
\end{gathered}$$
(j-tą kolumnę macierzy przejścia od bazy $B$, do bazy $B'$ stanowią współrzędne j-tego wektora nowej bazy względem starej bazy)

Odwrotnością tej macierzy jest macierz przejścia z bazy $B'$ do bazy $B$.

---
**Wniosek:**
Jeżeli $X$, $X'$ są kolumnowymi macierzami **współrzędnych** wektora $x\in V$ względem baz, odpowiednio $B$, $B'$ wówczas:
$$\begin{gathered}
X=P_{B\to B'}\cdot X' \land X'=(P_{B\to B'})^{-1}X
\end{gathered}$$
---
**Twierdzenie:** O zmianie macierzy odwzorowania przy zmianie baz

Niech $f: V\to W$ będzie odwzorowaniem liniowym, $B_V, B_V'$ bazami przestrzeni $V$, a $B_W,B_W'$ bazami przestrzeni $W$ Wówczas jeżeli:
$$\begin{gathered}
A=M_f(B_V,B_W),\ \  B=M_f(B_V', B_W')\\
P=P_{B_V\to B_V'},\ \ Q=P_{B_W\to B_W'}
\end{gathered}$$
to:
$$\begin{gathered}
B=Q^{-1}\cdot A\cdot P
\end{gathered}$$
---
