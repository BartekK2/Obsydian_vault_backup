### 1. Niech X bedzie zmienna losowa równa bezwzglednej wartosci róznicy liczby oczek w rzucie dwoma kostkami symetrycznymi. Wyznacz rozkład X.

$$\begin{gathered}
\Omega=\{(1,1),(1,2),(2,1),\dots,(6,6)\}\\
\Omega=\{(d_1,d_2): d_1,d_2 \in [1,6] \cap \mathbb{N}\}\\\\
X: \Omega \to \chi\\
X(d_1,d_2)=|d_1-d_2|\\
\chi=\{1,2,3,4,5\}\\\\\\

P(X=x)=\left\{
\begin{matrix}
\frac{6}{36},x=0\\
\frac{10}{36},x=1\\
\frac{8}{36},x=2\\
\frac{6}{36},x=3\\
\frac{4}{36},x=4\\
\frac{10}{36},x=5\\
0, \text{w przeciwnym razie}
\end{matrix}
\right.
\end{gathered}$$

---
### 2. Policz wartość oczekiwaną i wariancje rozkładu z poprzedniego zadania 

$$\begin{gathered}
\mu=0\cdot \frac{6}{36}+\frac{10}{36}\cdot 1 + \dots + \frac{10}{36}\cdot 5=\frac{70}{36}\\\\
\mu^2=(0-\mu)^2\cdot \frac{6}{36}+(1-\mu)^2\cdot \frac{10}{36}+\dots + (\frac{10}{36}-\mu)^2\cdot 5=\\
=1^2\cdot \frac{10}{36}+2^2\cdot \frac{8}{36}+\dots+5^2\cdot \frac{10}{36}-\mu^2=\dots=\frac{170}{36}-\left(\frac{70}{36}\right)^2
\end{gathered}$$

---
### 3. Jakie warunki muszą spełniać liczby rzeczywiste $a,b,c,d$ żeby funkcja określona wzorem:
$$\begin{gathered}
F(x)=\left\{
\begin{matrix}
0,x\lt 0\\
ax+b, 0\leq x\leq 1\\
c+\frac{d}{x}, x\gt 1
\end{matrix}
\right.
\end{gathered}$$
#### Własności dystrybuanty 
1. Jeśli $a\lt b,$ to $F_X(b)-F_X(a)=P(a \leq X \leq b)$
2. $F_X$ jest niemalejąca
3. $\lim_{x\to - \infty}F_X(x)=0$ i $\lim_{x \to +\infty}F_X(x)=1$
4. $F_X$ jest prawostronnie ciągła
5. $F_X$ jest ciągła w $x_0 \in \mathbb{R}$ wtedy i tylko wtedy gdy
   $$\begin{gathered}
P(X=x_0)=0
\end{gathered}$$

#### a) była dystrybuantą


(1) z racji tego że ma być niemalejąca to:
$a\geq 0$ oraz $d\leq 0$ 

(2) dystrybuanta ma być prawostronnie ciągła a tutaj mamy przeskok definicyjny zatem funkcja jest zdefiniowana inaczej dla $x=1$ a inaczej dla kolejnego najmniejszego $x$ co sugeruje że te dwie funkcje w tym punkcie muszą być równe

(3) to że $\lim_{x \to \infty}c+\frac{d}{x}=1$ oznacza że $c=1$


$$\begin{gathered}
a+b=1+d\\\\
a\geq 0\  oraz \ d\leq 0
\end{gathered}$$

#### b) dystrybuantą pewnego rozkładu ciągłego 

to co powyżej plus że jest różniczkowalna a to oznacza że nie ma żadnych skoków (no rozkład ciągły przecież) zatem 
$$\begin{gathered}
b=0
\end{gathered}$$

---
### 4. Dla jakiej wartości parametru $c \in \mathbb{R}$ funkcja:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{c}{x^4}, dla \ |x| \geq 1\\
0, \ dla \ |x| \lt 1
\end{matrix}
\right.
\end{gathered}$$

jest gęstością rozkładu pewnej zmiennej losowej $X$. Oblicz $P(X \gt 2)$

$$\begin{gathered}
(1)\int^{+\infty}_{-\infty}f(x)=1\\\\
(2)\ f(x) \gt 0\\\\
c\gt 0 \text{ z drugiego warunku}\\\\
\int^{+\infty}_{-\infty}f(x)dx=\int^{-1}_{\infty}\frac{c}{x^4}dx+\int^{1}_{-1}0dx+\int^{\infty}_{1}\frac{c}{x^4}dx=\\
=\frac{2c}{3}\\\\\
\frac{2c}{3}=1\\
c=\frac{3}{2}
\end{gathered}$$


$$\begin{gathered}
P(X \gt 2)=\int^{\infty}_{2}\frac{c}{x^4}=(\frac{c}{-3x^3})|^\infty_{2}=0-(-\frac{\frac{3}{2}}{24})=\frac{1}{16}
\end{gathered}$$

---
### 5. Znajdź wartość stałej rzeczywistej $a$ dla której funkcja 

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
a(1-x), \ \ dla \ 0 \leq x \leq 1\\
a(x-1), \ \  dla \ 1 \leq x \leq 2\\
0, \text{w pozostałych przypadkach}
\end{matrix}
\right.
\end{gathered}$$

jest gestością rozkładu pewnej zmiennej losowej rzeczywistej $X$. Dla tej zmiennej wyznacz dystrybuantę, wartość oczekiwaną, medianę, wariancję, kwantyle rzędu $\frac{1}{4}$ i $\frac{3}{4}$ czyli dolny i górny kwartyl oraz współczynnik asymetrii.

$$\begin{gathered}

\int^{+\infty}_{-\infty}f(x) dx=1\\\\
\int^{1}_{0}a(1-x)dx+\int^{2}_{1}a(x-1)=\\
=\frac{a}{2}+a(\frac{4}{2}-2-\frac{1}{2}+1)=a=1\\\\
\text{Spełna poniższe warunki dla odpowiednich zakresów }x\\
0\leq a(1-x)\leq 1 \land 0\leq a(x-1)\leq 1\\
\text{ta funkcja jest ciągła dla każdego a}\\\\
\text{Zatem }a=1 \text{ nam pasuje}
\end{gathered}$$

#### dystrybuanta:

$$\begin{gathered}
F(x)=\int^{x}_{-\infty}f(x) dx=\left\{
\begin{matrix}
0, x\lt 0\\
\int^{x}_{0}1-x dx, 0\leq x\leq 1\\
\int^{1}_{0}1-x dx+\int^{x}_{1}x-1 dx, 1\leq x\leq 2\\
\int^{1}_{0}1-x dx+\int^{2}_{1}x-1 dx,x\gt 2\\
\end{matrix}
\right.=\\\\
=\left\{
\begin{matrix}
0, x\lt 0\\
x-\frac{x^2}{2}, 0\leq x\leq 1\\
\frac{x^2}{2}-x+1, 1\leq x\leq 2\\
1,x\gt 2\\
\end{matrix}
\right.=\\
\end{gathered}$$

ta dystrybuanta jest ciągła i spełnia granice w nieskończoności więc chyba spełnia wszystkie warunki
#### wartość oczekiwana 

$$\begin{gathered}
\mu=\int^{\infty}_{-\infty}xf(x) dx=\int^{1}_{0}x-x^2dx+\int^{2}_{1}x^2-xdx=\\
=\frac{1}{2}-\frac{1}{3}+\frac{8}{3}-\frac{4}{2}-\frac{1}{3}+\frac{1}{2}=1
\end{gathered}$$

#### mediana 

$$\begin{gathered}
F(x)=\frac{1}{2}\\
x=1
\end{gathered}$$

#### wariancja 

$$\begin{gathered}
\sigma^2=\int^{+\infty}_{-\infty}x^2f(x)-\mu^2\\
\sigma^2=\int^{1}_{0}x^2-x^3dx+\int^{2}_{1}x^3-x^2dx-\mu^2=\\=\frac{1}{3}-\frac{1}{4}+\frac{16}{4}-\frac{8}{3}-1=\frac{5}{3}
\end{gathered}$$

#### kwantyle 

$$\begin{gathered}
F(x)=\frac{1}{4}\\
x-\frac{x^2}{2}=\frac{1}{4}\\
4x-2x^2-1=0\\
\Delta=16-8=8\\
x_1=\frac{-4+2\sqrt{2}}{-4}\\
x_2\lt 0 \text{ nie spełnia }
\end{gathered}$$

#### współczynnik asymetrii 

$$\begin{gathered}
\mu_3=\int^{+\infty}_{-\infty}(x-1)^3f(x) dx=
\end{gathered}$$

gdzie moim $f(x)$ było:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
1-x, \ \ dla \ 0 \leq x \leq 1\\
x-1, \ \  dla \ 1 \leq x \leq 2\\
0, \text{w pozostałych przypadkach}
\end{matrix}
\right.
\end{gathered}$$

zatem:
$$\begin{gathered}
\dots=\int^{1}_{0}(x-1)^3(1-x)dx+\int^{2}_{1}(x-1)^4=\begin{vmatrix}
u=x-1\\
du=dx
\end{vmatrix}=\\
=-\frac{(x-1)^5}{5}|^1_0+\frac{(x-1)^5}{5}|^2_1
=\frac{2}{5}\end{gathered}$$

Więc moim współczynnikiem asymetrii będzie:

$$\begin{gathered}
A=\frac{\frac{2}{5}}{(\frac{5}{3})^{\frac{3}{2}}}
\end{gathered}$$

---
### Wyznacz wartość stałej $c \in \mathbb{R}$ taką że funkcja:

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
c(x+2), \ dla \ x \in [-2,0)\\
c(2-x), \ dla \ x \in [0,2)\\
c(x-3), \ dla \ x \in [3,5)\\
c(7-x), \ dla \ x \in [5,7)\\
0 \text{ w pozostałych przypadkach}
\end{matrix}
\right.
\end{gathered}$$

jest gestością rozkładu prawdopodobieństwa pewnej zmiennej losowej.

$$\begin{gathered}
\int^{+\infty}_{-\infty}f(x)dx=1\\
c \left(\int^{0}_{-2}x+2+\int^{2}_{0}2-x+\int^{5}_{3}x-3+\int^{7}_{5}7-x\right)=\\
=8c\implies c=\frac{1}{8}\\\\
\text{dla tych wartości zawsze }1\geq f(x)\geq 0
\end{gathered}$$

$$\begin{gathered}
F(X)=\left\{
\begin{matrix}
0,x\lt -2\\
\frac{1}{8}\left(\frac{x^2}{2}+2x+2\right), \ \ -2 \leq x\lt 0\\
\frac{1}{8}\left(2+2x-\frac{x^2}{2}\right), \ \ 0 \leq x \lt 3\\
\frac{1}{8}\left(4+x^2-3x\right),\ \ 3 \leq x \lt 5\\
\frac{1}{8}\left(24+7x-x^2\right), 5\leq x \lt 7\\
1, 7\leq x
\end{matrix}
\right.
\end{gathered}$$

$$\begin{gathered}
F(x)=\frac{1}{2}\\
x=?\\

\end{gathered}$$

**DOKOŃCZ POTEM tutaj coś sie dystrybuanta zjebała**

---
### 7. Jakie warunki muszą spełniać stałe $a,b \in \mathbb{R}$ żeby funkcja:

$$\begin{gathered}
f(x)=ae^{b|x|}
\end{gathered}$$

była gęstością rozkładu prawdopodobienstwa pewnej zmiennej losowej? Dla wybranej pary $(a,b)$ spełniającej te warunki wyznacz dystrybuante, wartość średnią, wariancję, medianę, dolny i górny kwartyl rozkładu tej zmiennej. Oblicz $P(|X|\lt 1)$ oraz $P(X \lt 3)$


$$\begin{gathered}
0\leq f(x)\leq 1\\
\text{w praktyce wystarczy że:}\\
a\gt 0\\
\text{ponieważ: }\\
e^{b|x|}\text{ - zawsze}\\\\\
\text{oraz}\\
\int^{\infty}_{-\infty}f(x) dx=1\\
\int^{\infty}_{-\infty}ae^{b|x|} dx=2a \int^{\infty}_{0}e^{bx}dx=\begin{vmatrix}
u=bx\\
du=b dx\\
\frac{du}{b}=dx
\end{vmatrix}=\\\\
=\frac{2a}{b} \int^{\infty}_{0}e^u=\frac{2a}{b}\int^{\infty}_{0}e^{bx}=1\\\
e^{bx}|^\infty_0=\frac{b}{2a}\\
b\lt 0\\
-1=\frac{b}{2a}\\
2a=-b\\
\text{Jeśli całka po całym zakresie funkcji}\\
\text{daje wartość 1 a ta funkcja zawsze dodatnia}\\
\text{to spełnia również }f(x)\leq 1
\end{gathered}$$

Możemy przyjąć:
$$\begin{gathered}
a=1, \ b=-2\\\\
f(x)=e^{-2|x|}\\\\
F(x)=\left\{
\begin{matrix}
\frac{1}{2}e^{2x},x\lt 0\\\
1-\frac{1}{2}e^{-2x}, x\gt 0
\end{matrix}
\right.
\end{gathered}$$
Wartość oczekiwana będzie równa 0 ponieważ funkcja prawdopodobieństwa jest symetryczna.



**DOKOŃCZ WSZYSTKO NIE ZOSTAŁO DUŻO**
