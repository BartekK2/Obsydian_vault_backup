### Ekstrema warunkowe
#### 2025-05-25
##### Poprzednia: [[Analiza 8 Ekstrema]]
##### Następna: [[Analiza 10 Funkcje uwikłane]]
##### Zadania: [[Zadania rachunek różniczkowy]]

#rachunek_różniczkowy #ekstrema #analiza2  #funkcje_wielu_zmiennych #ekstrema_warunkowe

---
**Przykład**
$$\begin{gathered}
f(x,y)=x+y\\
\text{Dodatkowy warunek (tam gdzie szukać ekstremów coś a'la dziedzina)}\ \ \ x^2+y^2=1\\\\
\text{Zbiór D nie jest zbiorem otwartym w }\mathbb{R}^2 \text{ więc nie da się tutaj zastosować podanych }
\\
\text{wcześniej definicji i twierdzeń dotyczących ekstremów lokalnych}
\end{gathered}$$
---

**Definicja**
$f: D\to \mathbb{R} \ \ \ D\subset \mathbb{R}^n$
warunek: $g: D'\to \mathbb{R} \ \ \ D'\subset \mathbb{R}^n$
Zakładamy, że $f$ jest klasy $C^2$ na $D$ 
oraz $g$ jest klasy $C^1$ na $D'$
$S=\{x\in \mathbb{R}^n : g(x)=0\}_{warunek}\subset D\subset D'$
Znaleźć ekstrema lokalne funkcji $f: S\to \mathbb{R}$ $\text{ zwane ekstrema warunkowymi.}$

---
**Definicja**

Mówimy, że funkcja $f$ osiąga **maksimum lokalne warunkowe** w punkcie $x_0\in S\Leftrightarrow$ 
$\exists U \subset D: \forall x\in U \cap S \ \ \ f(x)\overset{\lt}{\gt}f(x_0)$

---
### Metoda Lagrange'a

Tworzymy funkcję Lagrange'a
$L(x,\lambda)=f(x)+\lambda g(x), \ \ \ x\in D\subset \mathbb{R}^n \ \ \ \ \lambda \in \mathbb{R}$

---
### WK istnienia ekstremum warunkowego

Zał: $f,g$ są klasy $C^1$ na odpowiednich zbiorów $D, D'$
$f$ ekstremum warunkowe w punkcie $x_0\in S$

teza: $\left\{\begin{matrix}\exists \lambda_0 \in \mathbb{R}: \forall i=1,\dots,n \frac{\partial L}{\partial x_i}(x_0,\lambda_0)=0\\ g(x_0)=0\end{matrix}\right.$

---
### Hesjan obrzeżony

$$\begin{gathered}
H=\begin{bmatrix}
0&\frac{\partial g}{\partial x_1}(x_0)&\frac{\partial g}{\partial x_2}(x_0)&\dots& \frac{\partial g}{\partial x_n}(x_0)\\

\frac{\partial g}{\partial x_1}(x_0)&\frac{\partial^2 L}{\partial x_1^2}(x_0,\lambda_0)&\frac{\partial^2 L}{\partial x_1\partial x_2}(x_0,\lambda_0)&\dots& \frac{\partial^2 L}{\partial x_1\partial x_n}(x_0, \lambda_0)\\
\frac{\partial g}{\partial x_2}(x_0)&\frac{\partial^2 L}{\partial x_2x_1}(x_0,\lambda_0)&\frac{\partial^2 L}{\partial x_2^2}(x_0,\lambda_0)&\dots& \frac{\partial^2 L }{\partial x_2x_n}(x_0,\lambda_0)\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
\frac{\partial g}{\partial x_n}(x_0)& \frac{\partial^2L}{\partial x_n \partial x_1}(x_0,\lambda_0)&\frac{\lambda^2 L}{\partial x_n \partial x_2}(x_0,\lambda_0)
&\dots & \frac{\partial^2 L}{\partial x_n^2}(x_0,\lambda_0)
\end{bmatrix}\\\\\\\\
H_2=\det \begin{bmatrix}
0& \frac{\partial g}{\partial x_1}& \frac{\partial g}{\partial x_2}\\
\frac{\partial g}{\partial x_1}&\frac{\partial^2 L}{\partial x_1^2 }&\frac{\partial^2 L }{\partial x_1 \partial x_2}\\
\frac{\partial g}{\partial x_2}& \frac{\partial^2 L }{\partial x_2 \partial x_1}& \frac{\partial^2 L }{\partial x_2^2}
\end{bmatrix}\\
\vdots\\
H_k=\dots\\
\vdots\\
H_n=\dots
\end{gathered}$$
---
### WW na istnienie ekstremum warunkowego

Zał: $f\in C^2(D)$ oraz $g\in C^2(D')$
spełniony jest WK istnienia ekstremum warunkowego w punkcie $(x_0,y_0), x_0\in S$.

Teza:
1) $\forall k=2,\dots,n \ \ H_k\lt 0 \implies f$ ma minimum lokalne warunkowe w punkcie $x_0$
2) $\forall k=2,\dots,n \ \ (-1)^{k+1}H_k\lt 0 \implies f$ ma maksimum lokalne warunkowe w punkcie $x_0$
3) Jeśli nie zachodzi ani $(\forall k=2,\dots,n \ \ H_k\leq 0)$, ani $(\forall k=2,\dots,n) \ \ (-1)^{k+1}H_k\leq 0)$ to $f$ nie ma ekstremum lokalnego warunkowego w punkcie $x_0$

**Przykład:**
$$\begin{gathered}
f(x,y)=x+y\\
x^2+y^2=1\\
g(x,y)=x^2+y^2-1\\
L(x,y,\lambda)=f(x,y)+\lambda g(x,y)=x+y+\lambda (x^2+y^2-1)\\
\frac{\partial L}{\partial x}=1+2\lambda x\\
\frac{\partial L}{\partial y}=1+2\lambda y\\
\left\{
\begin{matrix}
1+2\lambda x=0\\
1+2\lambda y=0
\end{matrix}
\right.
\left\{
\begin{matrix}
-\frac{1}{2\lambda}=x\\
-\frac{1}{2\lambda}=y\\
x^2+y^2-1=0
\end{matrix}
\right.\\\\
\frac{1}{4\lambda^2}+\frac{1}{4\lambda^2}-1=0\\
\frac{1}{2\lambda^2}=1\\
\frac{1}{2}=\lambda^2\\
1) \ \lambda=\frac{\sqrt{2}}{2}\ \  \vee \ 2) \ \lambda=-\frac{\sqrt{2}}{2}\\
\\
1)\ \ 
x=-\frac{1}{2}\cdot \frac{2}{\sqrt{2}}=-\frac{1}{\sqrt{2}}\ \ \ y=-\frac{1}{\sqrt{2}}\\
2)\ \ 
x=\frac{1}{2}\cdot \frac{2}{\sqrt{2}}=-\frac{1}{\sqrt{2}}\ \ \ y=\frac{1}{\sqrt{2}}\\
\\
\frac{\partial L}{\partial x^2}=2\lambda\\

\frac{\partial^2 L}{\partial y^2}=2\lambda\\
\frac{\partial g}{\partial x}=2x\\
\frac{\partial^2 L}{\partial y \partial x}=0\\
\frac{\partial^2 L}{\partial x \partial y}=0\\
\frac{\partial g}{\partial y}=2y\\
\\\\
H=\begin{bmatrix}
0&2x&2y\\
2x&2\lambda&0\\
2y&0&2\lambda
\end{bmatrix}=\begin{bmatrix}
0&\sqrt{2}&\sqrt{2}\\
\sqrt{2}&-\sqrt{2}&0\\
\sqrt{2}&0&-\sqrt{2}
\end{bmatrix}\\\\
H_2=\det H=2\sqrt{2}+2\sqrt{2}=4\sqrt{2}\gt 0\implies\\ \implies f \text{ ma maksimum lokalne warunkowe w }(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}})
\end{gathered}$$
**Przykład 2:**
Wyznaczyć wartość największą i najmniejszą osiąganą przez funkcje $f(x,y,z)=x^2+2y^2+3z^2$ na zbiorze $V=\{(x,y,z) \in \mathbb{R}^2: x^2+y^2+z^2\leq 100\}$

$I$ badamy wnętrze zbioru $V$
$$\begin{gathered}
\begin{matrix}
\frac{\partial f}{\partial x}=2x\\
\frac{\partial f}{\partial y}=4y\\
\frac{\partial f}{\partial z}=6z\\
\end{matrix}\ \
\left\{
\begin{matrix}
2x=0\\
4y=0\\
6z=0
\end{matrix}\ \
\right.
\left\{
\begin{matrix}
2x=0\\
4y=0\\
6z=0
\end{matrix}
\right.\\\\
f(0,0,0)=0

\end{gathered}$$
$II \ \ x^2+y^2+z^2=100$
$$\begin{gathered}
L(x,y,z,\lambda)=x^2+2y^2+3z^2+\lambda(x^2+y^2+z^2-100)\\\\
\begin{matrix}
\frac{\partial L}{\partial x}=2x+2\lambda x\\
\frac{\partial L}{\partial y}=4y+2\lambda y\\
\frac{\partial L}{\partial z}=6z+2\lambda z\\
\end{matrix}\ \ \ 
\begin{matrix}
\left\{
\begin{matrix}
2x+2\lambda x=0\\
4y+2\lambda y=0\\
6z+2\lambda z=0
\end{matrix}\right.\\\\
\left\{
\begin{matrix}
x(2+2\lambda )=0\\
y(4+2\lambda)=0\\
z(6+2\lambda)=0\\
x^2+y^2+z^2=100
\end{matrix}\right.
\end{matrix}\\\\
1. x=0\\\\
\ \  1.1 \ \ y=0\\
0^2+0^2+z^2=100\\
z=10 \ \vee \ z=-10\\
\lambda=-3\\
f(0,0,10)=300\\
f(0,0,-10)=300\\\\
1.2 \ \ 2+\lambda=0 \Leftrightarrow \ \ \lambda=-2\\
z(3-2)=0\\
z=0\\
0^2+y^2+0^2=100\\
y=10 \ \vee \ y=-10\\
f(0,10,0)=200\\
f(0,-10,0)=-200\\\\\
2. \ \ 1+\lambda=0 \Leftrightarrow \lambda = -1\\
y(2-1)=0\implies y=0\\
z(3-1)=0\implies z=0\\
x^2+0^2+0^2=100\\
x=10\  \ \vee \ \ x=-10\\
f(10,0,0)=100\\
f(0,10,))=200\\
f(-10,0,0)=100\\
f(0,-10,0)=200\\
\text{Odp. Największa wartość to 300 a najmniejsza to 0.}
\end{gathered}$$

---
