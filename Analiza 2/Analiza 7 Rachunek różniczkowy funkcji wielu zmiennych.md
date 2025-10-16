### Wstęp, granice, pochodne
#### 2025-05-12
##### Poprzednia: [[Analiza 6 Szeregi Fouriera]]
##### Następna: [[Analiza 8 Ekstrema]]
##### Zadania: [[Zadania rachunek różniczkowy]]

#rachunek_różniczkowy #pochodne #funkcje_wielu_zmiennych  #analiza2  

---
### Twierdzenie o granicy ciągu wielu zmiennych

Zał: ciąg $(x_n) \subseteq \mathbb{R}^k$
$\forall n \in \mathbb{N} \ x_n=(x_n^1, x_n^2, \dots, x_n^k) \in \mathbb{R}^k$
Teza: $\lim_{n\to \infty}{x_n}=(g_1,g_2,\dots,g_k) \Leftrightarrow \forall i =1,2\dots,k \ \lim_{n\to \infty}{x_n^i}=g_i$

Czyli przyjmując ciąg na przykład:
$$\begin{gathered}
(1,2,3),(0.9,1.9,2.9),(0.8,1.8,2.8),\dots\\
\text{I zbiega on do }(0,0,0) \text{ wtedy i tylko wtedy gdy każda składowa zbiega do 0}\\
(x\to 0, y\to 0, z\to 0)
\end{gathered}$$
---
### Definicja funkcji wielu zmiennych

$D\subset \mathbb{R}^n$
$f: D\to \mathbb{R}^m$
$x\in \mathbb{R}^n \Leftrightarrow x=(x_1,x_2,\dots,x_n)\in \mathbb{R}^n$
$f(x_1,x_2,\dots,x_n)=(f_1(x_1,x_2,\dots,x_n),f_2(x_1,x_2,\dots,x_n),\dots f_m(x_1,x_2,\dots,x_n))\in \mathbb{R}^m$
$f_i: D\to \mathbb{R} - \text{funkcja składowa, }i=1,2,\dots,m$
$f$ jest funkcją wielu n zmiennych 

---
### Definicja granicy funkcji w punkcie

$D\subset \mathbb{R}^m, \ \ \ S(x_0,r)\subset D$

**Mówimy, że granicą funkcji $f$ w punkcie $x_0$ jest $g$ wtedy i tylko wtedy gdy dla każdego ciągu $(x_n)_n\in \mathbb{N}$ spełniającego warunki:

1. $\forall n \in \mathbb{N} \ \ x_n\in \mathbb{D}$
2. $\forall n \in \mathbb{N} \ \ x_n\neq x_0$
3. $\lim_{n\to \infty}{x_n}=x_0$

zachodzi $\lim_{n\to \infty}{f(x_n)}=g$

**Przykład:**

$f(x,y)=\frac{xy}{x^2+y^2}$
$f: D\to \mathbb{R}, D=\mathbb{R}^2 \setminus \{(0,0)\}$
$x_0=(0,0)$
$\lim_{(x,y)\to (0,0)}f(x,y)=\lim_{(x,y)\to (0,0)}{\frac{xy}{x^2+y^2}}$

$x_n=(\frac{1}{n}, 0)$
$\lim_{n\to \infty}{f(x_n)}=\lim_{n\to \infty}{f(\frac{1}{n},0)}=\frac{\frac{1}{n}\cdot 0}{\frac{1}{n^2}+0}=0$

$x_n'=(\frac{1}{n},\frac{1}{n})$
$\lim_{n\to \infty}{f(x_n)}=\lim_{n\to \infty}{f(\frac{1}{n},\frac{1}{n})}=\frac{\frac{1}{n}\cdot \frac{1}{n}}{\frac{1}{n^2}+\frac{1}{n^2}}=\frac{1}{2}$
$\implies \lim_{(x,y)\to (0,0)}{\frac{xy}{x^2+y^2}}$ - **nie istnieje** 

---
**Przykład 2:**

$$\begin{gathered}
\lim_{(x,y)\to (0,0)}{\frac{x^2y}{x^2+y^2}}=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
(x,y)\to (0,0)\Leftrightarrow r\to 0\\
\varphi - \ dowolne
\end{vmatrix}=\lim_{r\to 0}{\frac{r^2\cos^2{\varphi}\cdot r\sin{\varphi}}{r^2}}=\\=\lim_{r\to 0}{r\cdot \cos^2{\varphi}\cdot \sin{\varphi}}=0
\end{gathered}$$

---
**Przykład:**
$$\begin{gathered}
\lim_{(x,y)\to (0,0)}\frac{x^2y}{x^2+y^4}\\\\
\text{z biegunowych nic nie wykminimy}\\\\
x_n=(\frac{1}{n},0)\\\\
\lim_{n\to \infty}{\frac{\frac{1}{n^2}\cdot 0}{\frac{1}{n^2}+0^2}}=\lim_{n\to \infty}0=0\\\\
x_n'=(\frac{1}{n}, \frac{1}{n})\\\\
\lim_{n\to \infty}{\frac{\frac{1}{n^3}}{\frac{2}{n^2}}}=\lim_{n\to \infty}{\frac{n}{n^2+1}}=0\\\\
\text{Lecz z tego że dla dwóch ciągów wychodzi to samo jeszcze nic nie wynika}\\
\text{Musimy bezpośrednio udowodnić że faktycznie to jest zbiezne do 0}\\\\
0\leq |\frac{x^2y}{x^2+y^4}|\leq |\frac{x^2}{x^2+y^4}||y|\leq 1 \cdot |y|\to 0\\
\text{I tu mamy faktyczny dowód na podstawie tw. o 3 funkcjach}
\end{gathered}$$

---
### Granice iterowane

$$\begin{gathered}
\lim_{(x,y)\to (x_0,y_0)}f(x,y) \ \ \ f: D\to \mathbb{R}, \ \ \ D\subset \mathbb{R}^2\\
\lim_{y\to y_0}(\lim_{x\to x_0}f(x,y)), \ \lim_{x\to x_0}(\lim_{y\to y_0}f(x,y))
\end{gathered}$$

**Przykład:**
$\lim_{(x,y)\to (0,0)}{\frac{x^2y^2}{x^2y^2+(x-y)^2}}$

![[diagram-20250513 (1).png]]
$\lim_{x\to 0}{\frac{x^4}{x^4+0^2}}=\lim_{x\to 0}1=1$
![[diagram-20250513 (2).png]]
$\lim_{x\to 0}{\frac{x^2\cdot 0}{x^2\cdot 0 + x^2}}=\lim_{x\to 0}{\frac{0}{x^2}}=0$

Dostajemy różne granice co implikuje że granica podwójna nie istnieje natomast w iterowanych:

$$\begin{gathered}
\text{Iterowane:}\\\\\
\lim_{x\to 0}(\lim_{y\to 0}{\frac{x^2y^2}{x^2y^2+(x-y)^2}})=0\\

\lim_{y\to 0}(\lim_{x\to 0}{\frac{x^2y^2}{x^2y^2+(x-y)^2}})=0\\
\end{gathered}$$

Zatem widzimy że z istnienia (i/lub równości) granic iterowanych **NIE** wynika, że istnieje granica podwójna. Z tego, że granice iterowane nie istnieją (lub sa różne) **NIE** wynika, że granica podwójna równiez nie istnieje.


**Granice iterowane są useless**

---
### Definicja ciągłości funkcji w punkcie:

$f: D\to \mathbb{R}^k, D \subset \mathbb{R}^n$
$x_0 \in U, \ \ \ U \text{ - otoczenie punktu }x_0, \ \ \ U\subset D$
$f$ jest ciągła w punkcie $x_0 \Leftrightarrow \ \lim_{x\to x_0}{f(x)=f(x_0)}$

---
### Twierdzenie o ciągłości funkcji wielowymiarowej

Zał: $f: D \to \mathbb{R}^m, \ \ \ D\subset \mathbb{R}^n$
$f(x_1,\dots, x_n)=(f_1(x_1,\dots,x_n), f_2(x_1,\dots, x_n), \dots, f_m(x_1,\dots, x_n))$
$x_0=(x_0^1, x_0^2, \dots, x_0^n) \in U \subset D$
$f_i: D\to \mathbb{R}, i=1,\dots, m$
Teza: $f$ jest ciągła w $x_0 \Leftrightarrow \forall i = 1, \dots, k \ \ f_i$ jest ciągła w $x_0$

**Przykład**:

Zbadaj ciągłość funkcji 
$$\begin{gathered}
f(x,y)=\left\{
\begin{matrix}
\frac{x^2-y^2}{x^2+y^2}, \ \ \ (x,y)\neq (0,0)\\
0, \ \ \ (x,y)=(0,0) 
\end{matrix}
\right., \ \ \ D=\mathbb{R}^2
\end{gathered}$$
w punkcie $(0,0)$.

$$\begin{gathered}
\lim_{(x,y)\to (0,0)}{f(x,y)}=\lim_{(x,y)\to (0,0)}{\frac{x^2-y^2}{x^2+y^2}}=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
r\to 0\\
\varphi - dowolne
\end{vmatrix}=\lim_{r\to 0 }{\frac{r^2\cos^2{\varphi}-r^2\sin^2{\varphi}}{r^2(\cos^2{\varphi}+\sin^2{\varphi})}}=\\\\
=\lim_{r\to 0}{(\cos^2{\varphi}-\sin^2{\varphi})}\implies f \text{ nie jest ciągła w punkcie }(0,0)
\end{gathered}$$
---
### Twierdzenie o ciągłości złożenia funkcji ciągłych

Zał: $f: X\to Y, \ \ g: Y\to Z$, gdzie $X,Y,Z$ są przestrzeniami topologicznymi
$f$ jest ciągła w $x_0$
$g$ jest ciągła w $y_0=f(x_0)$
Teza: złożenie funkcji $g\circ f$ jest ciągłe w punkcie $x_0$

---
### Twierdzenie o ciągłości funkcji będących sumą, różnicą$\dots$ funkcji ciągłych

Zał: $f,g : D\to \mathbb{R}, \ \ \ D\subset \mathbb{R}^n$
$f$ i $g$ są ciągłe w $x_0\in U \subset D$
Teza: $f+g, f-g, f\cdot g, \frac{f}{g}$ są ciągłe w punkcie $x_0$ (oczywiście przy tym ilorazie trzeba uważać żeby $g(x)\neq 0$ w tym otoczeniu)

**Przykład**
Sprawdź ciągłość w dziedzinie funkcji $f(x,y)=\frac{x^2-y^2}{x^2+y^2}$
$D=\mathbb{R}^2 \setminus \{(0,0)\}$
$x^2-y^2, x^2+y^2$ - wielomiany dwóch zmiennych są ciągłe
$\implies \frac{x^2-y^2}{x^2+y^2}$ jest ciągła (jako iloraz funkcji ciągłych), o ile $x^2+y^2\neq 0$

**Przykład 2:**
Sprawdź ciągłość w dziedzinnie funkcji
$$\begin{gathered}
f(x,y)=\left\{
\begin{matrix}
\frac{\sin(x^2+y^2)}{x^2+y^2}, \ \ (x,y)\neq (0,0)\\
1, \ \ \ (x,y)=(0,0)
\end{matrix}
\right.
\end{gathered}$$
$D=\mathbb{R}^2$
$\sin(x^2+y^2)$ jest ciągły jako złożenie funkcji ciągłych
i analogicznie jak w poprzednim przykładzie funkcja $f$ jest ciągła w $D=\mathbb{R}^2 \setminus \{(0,0)\}$
$$\begin{gathered}
\lim_{(x,y)\to (0,0)}{\frac{\sin(x^2+y^2)}{x^2+y^2}}=\begin{vmatrix}
t=x^2+y^2
\end{vmatrix}=\lim_{t\to 0 }{\frac{\sin{t}}{t}}=1\implies f \text{ jest ciągła w }(0,0)
\end{gathered}$$
$\implies f$ jest ciągła w całym $\mathbb{R}^2$

---
### Pochodna wzdłuż wektora
$f: D\to \mathbb{R}^m,  \ \ \ D\subset \mathbb{R}^n$
$x_0 \in U \subset D$
$h\in \mathbb{R}^n, \ \ \ h \text{ - wektor}$
Pochodną funkcji w punkcie $x_0$ wzdłuż wektora $h$ nazywamy
$D_hf(x_0)=\lim_{t\to 0}{\frac{f(x_0+th)-f(x_0)}{t}}$
Inne oznaczenie: $\frac{\partial f}{\partial h}(x_0)$

**Przykład:**
$f(x,y)=x^2+y^2, \ \  \ (x_0,y_0)=(1,0), \ \ \ h=(2,1)$
$D_{(2,1)}f(1,0)=\lim_{t\to 0}{\frac{f((1,0)+t(2,1))-f(1,0)}{t}}=\lim_{t\to 0}{\frac{f(1+2t,t)-f(1,0)}{t}}=\lim_{t\to 0}{\frac{(1+2t)^2+t^2-1}{t}}$
$=\lim_{t\to 0}{\frac{5t^2+4t}{t}}=\lim_{t\to 0}{(5t+4)}=4$

---
### Pochodna w kierunku wektora

**Praktycznie to samo tylko że teraz przjmując dany wektor bierzemy wersor tego wektora, a nie ten wektor**

$f: D\to \mathbb{R}^m, \ \ \ D\subset \mathbb{R}^n$
$x_0\in U \subset D$
$h\in \mathbb{R}^n$

Pochodną kierunkową funkcji $f$ w punkcie $x_0$ w kierunku wektora $h$ nazywamy pochodną funkcji $f$ w punkcie $x_0$ wzdluż wersora wektora $h$ tzn. wzdłuż $\frac{h}{|h|}$

**Przykład:**
Oblicz pochodną kierunkową funkcji $f(x,y)=(xy,x+y)$ w punkcie $(1,-1)$ w kierunku wektora $h=(2,2)$
$$\begin{gathered}
\frac{h}{|h|}=\frac{(2,2)}{\sqrt{2^2+2^2}}=\frac{(2,2)}{2\sqrt{2}}=(\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2})\\\\\
D_{(\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2})}f(1,-1)=\lim_{t\to 0}{\frac{f(x_0+th)-f(x_0)}{t}}=
\lim_{t\to 0}{\frac{f((1,-1)+t(\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2}))-f(1,-1)}{t}}\\
=\lim_{t\to 0}{\frac{f(1+t\frac{\sqrt{2}}{2}, t\frac{\sqrt{2}}{2}-1)-f(1,-1)}{t}}=\\
=\lim_{t\to 0}{\frac{\left((1+t\frac{\sqrt{2}}{2})(t\frac{\sqrt{2}}{2}+1), 1+t\frac{\sqrt{2}}{2}-1+t\frac{\sqrt{2}}{2}\right)}{t}}=\lim_{t\to 0}{\frac{(\frac{1}{2}t^2-1, t\sqrt{2})-(-1,0)}{t}}=\\
=\lim_{t\to 0}{\frac{(\frac{1}{2}t^2, t\sqrt{2})}{t}}=\lim_{t\to 0}(\frac{1}{2}t, \sqrt{2}) = (0,\sqrt{2})
\end{gathered}$$

---
### Pochodna cząstkowa funkcji w punkcie względem zmiennej 

$f: D\to \mathbb{R}^m, D\subset \mathbb{R}^n$
$x_0\in U \subset D$
$x_0=(x_0^1, x_0^2, \dots x_0^n)$

Pochodną cząstkową funkcji $f$ w punkcie $x_0$ względem zmiennej $x_i$ (i-tej zmiennej) nazywamy:
$$\begin{gathered}
\frac{\partial f}{\partial x_i}(x_0)=\lim_{\Delta x_i \to 0}{\frac{f(x_0^1,x_0^2,\dots, x_0^i+\Delta x_i, \dots, x_0^n)-f(x_0^1,\dots,x_0^n)}{\Delta x_i}}
\end{gathered}$$

**Przykład**:
$f(x,y)=x^2+y^2, \ \ \ x_0=(1,-1)$
$$\begin{gathered}
\frac{\partial f}{\partial x}(1,-1)=\lim_{\Delta x\to 0}{\frac{f(1+\Delta x, -1)-f(1,-1)}{\Delta x}}=\\\\=\lim_{\Delta x \to 0}{\frac{(1+\Delta x)^2+(-1)^2-(1)^2-(-1)^2}{\Delta x}}=\lim_{\Delta x\to 0}{\frac{(\Delta x)^2+2\Delta x}{\Delta x}}=\lim_{\Delta x \to 0}{(\Delta x + 2)}=2
\end{gathered}
$$

**Przykład 2:**
$f(x,y)=e^x\cos{y}, \ \ \ D=\mathbb{R}^2, \ \ \ (x_0,y_0)\in \mathbb{R}^2$
$$\begin{gathered}
\frac{\partial f}{\partial x}(x_0,y_0)=(e^x\cos{y_0})'_x |_{x=x_0}=\cos{y_0}e^x|_{x=x_0}=e^{x_0}\cos{y_0}
\end{gathered}$$
---
### Definicja różniczkowalności funkcji

$f: D\to \mathbb{R}^m, \ \ \ D\subset \mathbb{R}^n$
$x_0\in U \subset D$
Mówimy, że $f$ jest różniczkowalna w $x_0 \Leftrightarrow$ gdy istnieje takie odzorowanie liniowe:
$L_{x_0}: \mathbb{R}^n \to \mathbb{R}^m$, że:
$$\begin{gathered}
\forall h \in \mathbb{R}^n \ \ \ f(x_0+h)-f(x_0)=L_{x_0}(h)+r_{x_0}(h)
\end{gathered}$$
gdzie $\lim_{h\to 0}{\frac{r_{x_0}(h)}{||h||}}=0$, $r_{x_0}(h)$ - reszta
oznaczenie: $L_{x_0}=df(x_0)$ - różniczka funkcji $f$ w punkcie $x_0$
$L_{x_0}(h) = df(x_0)(h)$

**Przykład:**
Czy funkcja $f(x,y)=\left\{\begin{matrix}\frac{xy^2}{x^2+y^2}, \ \ (x,y)\neq (0,0)\\ 0, (x,y)=(0,0)\end{matrix}\right.$  jest różniczkowalna w punkcie $(0,0)$?

$$\begin{gathered}
f(x_0+h)-f(x_0)=L_{x_0}(h)+r_{x_0}(h)\\
f((0,0)+(h_1,h_2))=\frac{\partial f}{\partial x}(0,0)h_1+\frac{\partial f}{\partial y}(0,0)h_2+r_{x_0}(h)\\
\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}{\frac{f(0+\Delta x,0)-f(0,0)}{\Delta x}}=\lim_{\Delta x \to 0}{\frac{0-0}{\Delta x}}=0\\
\frac{\partial f}{\partial y}(0,0)=0\\
f(h_1,h_2)-0=0\cdot h_1+0\cdot h_2+r_{(0,0)}(h_1,h_2)\\
r_{(0,0)}(h_1,h_2)=\frac{h_1\cdot h_2^2}{h_1^2+h_2^2}\\
\lim_{(h_1,h_2)\to (0,0)}{\frac{r_{(0,0)}(h_1,h_2)}{||(h_1,h_2)||}}=\lim_{(h_1,h_2)\to (0,0)}{\frac{\frac{h_1h_2^2}{h_1^2+h_2^2}}{\sqrt{h_1^2+h_2^2}}}=\lim_{(h_1,h_2)\to (0,0)}{\frac{h_1h_2^2}{(h_1^2+h_2^2)^{\frac{3}{2}}}}=\\
=\lim_{r\to 0, \varphi - dowolne}{\frac{r^3\cos{\varphi}\sin^2{\varphi}}{r^3}}=
\lim_{r\to 0, \varphi - dowolne}{\cos{\varphi}\sin^2{\varphi}} - nie \ istnieje\\
\implies f \ nie \ jest \ rozniczkowalna \ w \ (0,0)
\end{gathered}$$

---
### Twierdzenie - postać macierzowa różniczki funkcji

Zał: $f:D\to \mathbb{R}^m, D\subset \mathbb{R}^n, x_0=(x_0^1,x_0^2,\dots, x_0^n)$
$f$ jest różniczkowalna w punkcie $x_0\in U\subset D$
$f(x_1,\dots,x_n)=(f_1(x_1,\dots,x_n), f_2(x_1,\dots,x_n),\dots, f_m(x_1,\dots,x_n))$
**Teza: różniczka funkcji w punkcie $x_0$ ma postać**
$$\begin{gathered}
df(x_0)(h)=\begin{bmatrix}
\frac{\partial f_1}{\partial x_1}(x_0)&
\frac{\partial f_1}{\partial x_2}(x_0)&
\dots &
\frac{\partial f_1}{\partial x_n}(x_0)
\\
\frac{\partial f_2}{\partial x_1}(x_0)&
\frac{\partial f_2}{\partial x_2}(x_0)&
\dots &
\frac{\partial f_2}{\partial x_n}(x_0)
\\
\vdots&
\vdots&
\ddots &
\vdots
\\
\frac{\partial f_m}{\partial x_1}(x_0)&
\frac{\partial f_m}{\partial x_2}(x_0)&
\dots &
\frac{\partial f_m}{\partial x_n}(x_0)
\\
\end{bmatrix}
\begin{bmatrix}
h_1\\
h_2\\
\vdots\\
h_n
\end{bmatrix}
\end{gathered}$$
**Def.** Macierz $f'(x_0)=\begin{bmatrix}\frac{\partial f_i}{\partial x_j}(x_0)\end{bmatrix}^{i=1,\dots,m}_{j=1,\dots,n}$ nazywamy **macierzą Jacobiego funkcji $f$ w punkcie $x_0$**
Jeśli $n=m$, to $J(x_0)=\det \begin{bmatrix}\frac{\partial f_i}{\partial x_j}(x_0)\end{bmatrix}^{i=1,\dots,m}_{j=1,\dots,n}$ nazywamy **jakobianem** funkcji $f$ w punkcie $x_0$.

---
### Twierdzenie o związku różniczki z pochodnymi wzdłuż wektora. WK różniczkowalności.

Zał: $f: D\to \mathbb{R}^m,  \ \ \ D\subset \mathbb{R}^n$
$x_0\in D \subset D$
$f$ jest różniczkowalna w punkcie $x_0$ (i niech $df(x_0)$ oznacza różniczkę funkcji $f$ w punkcie $x_0$)
Teza: istnieje pochodna funkcji $f$ w punkcie $x_0$ wzdłuż dowolnego wektora $h\in \mathbb{R}^n$ i zachodzi $D_hf(x_0)=df(x_0)(h)$

**funkcja różniczkowalna $\implies$ pochodna wzdłuż wektora jest równy różniczce iloczyn skalarny ten wektor**

**Przykład**:
Oblicz pochodną wzdłuż wektora $h=(3,-1)$ funkcji $f(x,y)=x^4+y^4+2x^2y+1$ w punkcie $x_0=(1,2)$


$$\begin{gathered}
\text{Korzystam z twierdzenia o związku różniczki }\\
\text{z pochodnymi wzdłuż wektora.}\\\\
\frac{\partial f}{\partial x}(1,2)=4x^3+4xy (1,2)=4+8=12\\
\frac{\partial f}{\partial y}(1,2)=4y^3+2x^2(1,2)=34\\\\
D_hf(x,y)=df(x,y)(h)\\\\
D_{(3,-1)}f(1,2)=df(1,2)(3,-1)=36-34=2
\end{gathered}$$

---
### Warunek konieczny różniczkowalności związany z pochodnymi cząstkowymi

Zał: $f: D\to \mathbb{R}^m, \ \ \ D\subset \mathbb{R}^n, \ \ x_0\in U \subset \mathbb{R}^n$
$f$ jest różniczkowalna w punkcie $x_0$ (i niech $df(x_0)$ oznacza różniczkę funkcji $f$ w punkcie $x_0$)

Teza:
1. $\forall i=1,\dots,n$ istnieje pochodna cząstkowa $\frac{\partial f}{\partial x_i}$ w punkcie $x_0$
2. $\forall h = (h_1,\dots,h_n)\in \mathbb{R}^n \ \ \ df(x_0)(h_1,\dots,h_n)=\sum^{n}_{i=1}{\frac{\partial f}{\partial x_i}}(x_0)\cdot h_i$

**istnieje pochodna $\implies$ istnieją pochodne cząstkowe i różniczka równa ich sumie razy $h_i$**

---
### Warunek konieczny różniczkowalności związany z ciągłością

Zał: $f:D\to \mathbb{R}^m, \ \ D\subset \mathbb{R}^n, \ \ \ x_0\in U \subset D$
$f$ jest różniczkowalna w $x_0$
Teza: $f$ jest ciągła w $x_0$

**różniczkowalna $\implies$ ciągła**

---
### Warunek wystarczający różniczkowalności
Zał: $f: D\to \mathbb{R}^m, \ \ D \subset \mathbb{R}^n, \ \ \ x_0\in U \subset D$
$\forall i = 1,\dots,n$ istnieją i są ciągłe pochodne cząstkowe $\frac{\partial f}{\partial x_i}$ w punkcie $x_0$
Teza: $f$ jest różniczkowalna w punkcie $x_0$ i zachodzi:

$\forall h = (h_1,\dots,h_n) \in \mathbb{R}^n \ \ \ df(x_0)(h_1,\dots,h_n)=\sum^{n}_{i=1}{\frac{\partial f}{\partial x_i}}(x_0)h_i$

**istnieją i ciągłe pochodne cząstkowe $\implies$ pochodna równa sumie tych pochodnych razy $h_i$

**Przykład:**
Czy funkcja $f(x,y)=x^2+\ln{y}$ jest różniczkowalna w $(x_0,y_0)=(1,1)$? Jeśli tak, to podaj różniczke tej funkcji w tym punkcie.

$$\begin{gathered}
D: x\in \mathbb{R}, \ \ \ y\gt 0\\
D=\{(x,y): x\in \mathbb{R}, \ y\gt 0 \}\\
(x_0,y_0)=(1,1)\\
\frac{\partial f}{\partial x}=2x\\
\frac{\partial f}{\partial y}=\frac{1}{y}\\\\
\frac{\partial f}{\partial x}(1,1)=2\\
\frac{\partial f}{\partial y}(1,1)=1\\
\text{istnieją}\\
\frac{\partial f}{\partial x}=2x \text{ jest ciągła w }(1,1)\text{ bo jest wielomianem}\\

\frac{\partial f}{\partial y}=\frac{1}{y}\text{ jest ciągła w }(1,1)\text{ bo jest funkcją wymierną}\\\\
\text{Z twierdzenia powyższego tj. WW różniczkowalności funkcji wynika że}\\
\text{funkcja jest różniczkowalna w }(1,1)\\\\
\text{Z tego samego twierdzenia możemy podać różniczkę tej funkcji:}\\
h\in \mathbb{R}^2 \ \ \ df(1,1)(h_x,h_y)=\frac{\partial f}{\partial x}(1,1)\cdot h_x + \frac{\partial f}{\partial y}(1,1)\cdot h_2 =2h_1+h_2\\\\
df(1,1): \mathbb{R^2}\to \mathbb{R}
df(1,1)(h_x,h_y)=2h_1+h_2\\
f'(1,1)=[2,1]
\end{gathered}$$

---
### Interpretacja geometryczna różniczkowalności, $WKW$ różniczkowalności

Zał: $f: D\to \mathbb{R}, \ \ \ D\subset \mathbb{R}^2$
Teza: $f$ jest różniczkowalna w $(x_0,y_0)\in U \subset D \Leftrightarrow$ istnieje płaszczyzna (ściśle) styczna do powierzchni $z=f(x,y)$ w punkcie $(x_0,y_0,f(x_0,y_0))$ o równaniu:


$$\begin{gathered}
z-f(x_0,y_0)=\frac{\partial f}{\partial x}(x_0,y_0)\cdot (x-x_0)+\frac{\partial f}{\partial y}(x_0,y_0)(y-y_0)\\\\
\text{Analogia do funkcji jednej zmiennej:}\\
y=f(x_0)+f'(x_0)(x-x_0)
\end{gathered}$$

**Przykład 1**:
$$\begin{gathered}
f(x,y)=x^2+\ln{y}\\
z=f(1,1)+\frac{\partial f}{\partial x}(1,1)(x-1)+\frac{\partial f}{\partial y}(1,1)(y-1)\\\\
z=1+2(x-1)+(y-1)
\end{gathered}$$

![[newplot (4)-Photoroom.png]]
**Przykład 2:**
$$\begin{gathered}
f(x,y)=\sqrt{4-x^2-y^2}, \ \ \ (x_0,y_0)=(1,1)\\
z=f(1,1)+\frac{\partial f}{\partial x}(1,1)(x-1)+\frac{\partial f}{\partial y}(1,1)(y-1)\\
\frac{\partial f}{\partial x}=-\frac{x}{\sqrt{4-x^2-y^2}}\\
\frac{\partial f}{\partial y}=-\frac{y}{\sqrt{4-x^2-y^2}}\\

z=\sqrt{2}-\frac{1}{\sqrt{2}}(x-1)-\frac{1}{\sqrt{2}}(y-1)
\end{gathered}$$

---
### Uwaga dot. aproksymacji funkcji wielu zmiennych

Zał: $f: D \to \mathbb{R}, \ \ \ D\subset \mathbb{R}^2$
$f$ jest różniczkowalna w $x_0\in U \subset D$
$x_0+h\in U$

Teza: $f(x_0+h)\approxeq f(x_0)+df(x_0)(h)$

**Przykład:**
Oblicz przybliżoną wartość $\frac{(1,03)^2}{\sqrt[3]{0,98\sqrt[4]{1,05}}}$
$$\begin{gathered}
f(x,y,z)=\frac{x^2}{\sqrt[3]{y \sqrt[4]{z}}}\\
f(1.03,0.98,1.05)\approxeq f(1,1,1)+D_{(0.3,-0.2,0.5)}(1,1,1)\\\\
f(1,1,1)=1\\
D_{(0.03,-0.02,0.05)}(1,1,1):\\
\frac{\partial f}{\partial x}=\frac{2x}{\sqrt[3]{y \sqrt[4]{z}}}\\
\frac{\partial f}{\partial y}=-\frac{x^2}{3(y^{\frac{4}{3}}) \sqrt[12]{z}}\\
\frac{\partial f}{\partial z}=-\frac{x^2}{12\sqrt[3]{y}}\cdot z^{-\frac{13}{12}}\\\\
\frac{\partial f}{\partial x}(1,1,1)=2\\
\frac{\partial f}{\partial y}(1,1,1)=-\frac{1}{3}\\
\frac{\partial f}{\partial z}(1,1,1)=-\frac{1}{12}\\\\
\frac{(1,03)^2}{\sqrt[3]{0,98\sqrt[4]{1,05}}}=1+2\cdot 0.03+\frac{2}{300}-\frac{1}{240}=1.0625
\end{gathered}$$
**Przykład 2:**
Oblicz przybliżoną wartość $\sqrt{(0.98)^3+(2.05)^3}$
$$\begin{gathered}
f(x,y)=\sqrt{x^3+y^3}\\
f(1,2)=\sqrt{1^3+2^3}=\sqrt{9}=3\\
f(0.98,2.05)\approxeq f(1,2)+df(1,2)(-0.02,0.05)\\
df(1,2)(h_x,h_y)=\frac{\partial f}{\partial x}(1,2)h_x+\frac{\partial f}{\partial y}(1,2)h_y=\\=\frac{3x^2}{2\sqrt{x^3+y^3}}(1,2)h_x+\frac{3y^2}{2\sqrt{x^3+y^3}}(1,2)h_y
=\frac{1}{2}h_x+2h_y\\\\
f(0.98,2.05)\approxeq 3-0.01+0.1=3.09\\
\end{gathered}$$

---
### Pochodna cząstkowa $II$ rzędu

$f: D\to \mathbb{R}^k, \  \ \ D\subset \mathbb{R}^n$
niech $\frac{\partial f}{\partial x_i}$ będzie określona w pewnym otoczeniu $U\subset D$ punktu $x_0$
**Pochodną cząstkową drugiego rzędu nazywamy**:

$$\begin{gathered}
\frac{\partial f^2}{\partial x_j \partial x_i}(x_0)=\lim_{\Delta x_j\to 0}{\frac{\frac{\partial f}{\partial x_i}(x_1,\dots,x_{j-1},x_j+\Delta x_j,\dots,x_n)-\frac{\partial f}{\partial x_i}(x_1,\dots,x_j,\dots,x_n)}{\Delta x_j}}\\\\
\text{Lub innymi słowami:}\\
\frac{\partial^2 f}{\partial x_j \partial x_i}=\frac{\partial }{\partial x_j}\left(\frac{\partial f}{\partial x_i}\right)
\end{gathered}$$

**Przykład 1:**
$$\begin{gathered}
f(x,y)=x^2-\sin{y}\\
\frac{\partial f}{\partial x}=2x\\
\frac{\partial f}{\partial y}=-\cos{y}\\
\frac{\partial^2 f}{\partial x \partial x}=\frac{\partial }{\partial x}\left(\frac{\partial f}{\partial x}\right)=\frac{\partial}{\partial x}\left(2x\right)=2\\

\frac{\partial^2 f}{\partial y \partial x}=\frac{\partial }{\partial y}\left(\frac{\partial f}{\partial x}\right)=\frac{\partial}{\partial y}\left(2x\right)=0\\

\frac{\partial^2 f}{\partial x \partial y}=\frac{\partial }{\partial x}\left(\frac{\partial f}{\partial y}\right)=\frac{\partial}{\partial x}\left(-\cos{y}\right)=0\\

\frac{\partial^2 f}{\partial y \partial y}=\frac{\partial }{\partial y}\left(\frac{\partial f}{\partial y}\right)=\frac{\partial}{\partial y}\left(-\cos{y}\right)=\sin{y}\\
\end{gathered}$$
**Przykład 2:**
Rozwiąż równanie różniczkowe cząstkowe $yz'_x-xz'_y=0$, gdzie $z=z(x,y)$, przyjmując nowe zmienne $u=x, v=x^2+y^2$.

$$\begin{gathered}
\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}\frac{\partial u}{\partial x}+\frac{\partial z}{\partial v}\frac{\partial v}{\partial x}\\\\
\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}+2x \frac{\partial z}{\partial v}\\\\

\frac{\partial z}{\partial y}=\frac{\partial z}{\partial u}\frac{\partial u}{\partial y}+\frac{\partial z}{\partial v}\frac{\partial v}{\partial y}\\\\
\frac{\partial z}{\partial y}=2y \frac{\partial z}{\partial v}\\\\

y\frac{\partial z}{u}+2xy \frac{\partial z}{\partial v}-2xy \frac{\partial z}{\partial v}=0\\
y \frac{\partial z}{\partial u}=0\\\\
\text{Zatem }y=0 \text{ lub funkcja zalezy jedynie od }v \text{ i przyjmuje postac: }z=\varphi(x^2+y^2)
\end{gathered}$$

**Czyli innymi slowami - badajac przyrost (zależność) funkcji od danej zmiennej $(x)$ gdy zechcemy wprowadzic nową zmienną $(u)$ zależną od zmiennej $x$ to zależność funkcji równa sie iloczynowi zależności funkcji od $u$ oraz zależności zmiennej / funkcji $u$ od $x$.**

---
### Definicja 2-krotnie różniczkowalności 

Zakładająć że w pewnym otoczeniu $U$ funkcja $f$ jest różniczkowalna tzn. $\forall x \in U \ \ \ \exists df(x)$ czyli istnieje funkcja:
$U \ni x \to df(x)$

Funkcję $f$ nazywamy 2-krotnie różniczkowalną w punkcie $x_0 \in U \Leftrightarrow$ gdy funkcja $U \ni x \to df(x)$ jest różniczkowalna w $x_0$.

$d^2f(x_0)=d(df)|_{x=x_0}$

**Przykład:**
$f: D\to \mathbb{R}, \ \ D\subset \mathbb{R}^2$
$df(h_1,h_2)=\frac{\partial f}{\partial x}h_1+\frac{\partial f}{\partial y}h_2$
$d^2f(h_1,h_2)=d(\frac{\partial f}{\partial x}h_1+\frac{\partial f}{\partial y}h_2)=\frac{\partial f}{\partial x}(\frac{\partial f}{\partial x}h_1+\frac{\partial f}{\partial y}h_2)h_1+\frac{\partial f}{\partial y}(\frac{\partial f}{\partial x}h_1+\frac{\partial f}{\partial y}h_2)h_2=$
$=\frac{\partial^2 f}{\partial x^2}h_1^2+\frac{\partial ^2 f}{\partial x \partial y}h_2h_1+\frac{\partial ^2 f}{\partial y \partial x}h_1h_2+\frac{\partial ^2 f}{\partial y^2}h_2^2$
$\uparrow$
różniczka zupełna rzędu 2-go funkcji $f$ w punkcie $x_0$

---
### WW na 2-krotną różniczkowalność 

Zał: istnieją i są ciągłe wszystkie pochodne cząstkowe 2-go rzędu funkcji $f$ w punkcie $x_0\in U \subset D_f$
Teza: $f$ jest 2-krotnie różniczkowala w $x_0$

---
### Twierdzenie Schhwarza o równości pochodnych mieszanych

Zał: $f$ jest 2-krotnie różniczkowalna w $x_0$ 
teza: $\frac{\partial ^2 f}{\partial x \partial y}(x_0)=\frac{\partial ^2 f}{\partial y \partial x}(x_0)$

---
