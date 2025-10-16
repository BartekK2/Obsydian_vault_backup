## Monotoniczność, Ekstrema, Taylor, Maklaren
#### 2024-10-28
##### Poprzednia: [[Analiza - 4]]
##### Następna: [[Analiza - 6]]
##### Zadania: [[]]

#monotoniczność #ekstrema #analiza  #taylor #maklaren

--- 
### Twierdzenie o warunkach wystarczających monotoniczności funkcji
Niech $f$ będzie funkcją różniczkowalną na przedziale $p=(a,b)$
Jeśli $\forall x \in p$:
1. $f'(x) =0$, to $f$ jest stała w $p$
2. $f'(x)\gt 0$, to $f$ jest rosnąca na $p$
3. $f'(x) \geq 0$, to $f$ jest niemalejąca na $p$
4. $f'(x) \lt 0$, to $f$ jest malejąca na $p$
5. $f'(x) \leq 0$, to $f$ jest nierosnąca na $p$

Dowód odnosi się do [[Analiza - 4#^31ed24|twierdzenia Lagrange'a]] czyli istnieje takie c dla którego $f'(c)$ jest równe ilorazowi przyrostu wartości przez przyrost parametrów, gdzie przy założeniu że przyrost parametrów dodatni to pochodna dodatnia wtedy i tylko wtedy kiedy funkcja wzrosła (różnica wartości dodatnia).

###### Przykład: Czy $f(x)=\frac{1}{x}$ jest malejąca na całej dziedzinie?
$f(x) = \frac{1}{x}$
$f'(x) = -\frac{1}{x^2}$
$x^2 \gt 0, \forall x \in \mathbb{R} \setminus \{0\}$
Więc pochodna zawsze ujemna co implikuje że funkcja jest malejąca w całej dziedzinie.

---
### Ekstrema lokalne funkcji
*Def.*
Niech $f$ będzie określona w pewnym otoczeniu $U$ punktu $x_0$.
Mówimy, że $f$ ma w punkcie $x_0$ maksimum/minimum lokalne wtedy i tylko wtedy kiedy istnieje takie sąsiedztwo $S(x_0, \delta) \subset U$, w którym $\forall x \in \ S(x_0, \delta) \ f(x) \lt {/} \gt f(x_0)$

---
### Twierdzenie Fermata - warunek konieczny istnienia ekstremum
Jeżeli funkcja jest różniczkowalna w punkcie $x_0$ a w tym punkcie ma ekstremum lokalne to musi ta pochodna wynosić 0.

Założenia
1. $f$ przyjmuje ekstremum lokalne w $x_0$
2. $f$ jest różniczkowalna w $x_0$
Teza: $f'(x_0)=0$
Dowód analogiczny do dowodu twierdzenia że pochodna się zeruje w punkcie w którym funkcja osiąga wartość ekstremalną.

---
### Twierdzenie o pierwszym warunku wystarczającym istnienia ekstremum lokalnego

1. $f$ jest różniczkowalna w pewnym otoczeniu $U$ punktu $x_0$
2. $f'(x_0)=0$
3. istnieje takie sąsiedztwo $S(x_0, \delta)$, że:
   - jeśli $(\forall x \in S^-(x_0, \delta) \ f'(x)\gt 0 \ oraz\  \forall x \in S^+(x_0, \delta) \ f'(x)\lt 0)$ to $f$ przyjmuje w $x_0$ makismum lokalne 
   -  jeśli $(\forall x \in S^-(x_0, \delta) \ f'(x)\lt 0 \ oraz\  \forall x \in S^+(x_0, \delta) \ f'(x)\gt 0)$ to $f$ przyjmuje w $x_0$ minimum lokalne 
Dowód: [[Analiza - 4#^31ed24|na podstawie twierdzenia Lagrange'a]] 

*Przykład:*

$f(x)=\frac{\ln{x}}{x}$
$f'(x)=\frac{\frac{1}{x}\cdot x-\ln{x}}{x^2}=\frac{-\ln{x}}{x^2}$
$f'(x) \gt 0 \Leftrightarrow \ln{x} \lt 0 \implies x \lt e$
$f'(x) \gt 0 \Leftrightarrow \ln{x} \gt 0 \implies x \gt e$

Więc ekstremum (maksimum) jest w $x=e$.

---
### Ekstremum globalne

*Przykład:*
Wyznaczyć najmniejszą i największą wartość funkcji $f(x)=x^3|x+2|$ osiąganą na przedziale $[-4,1]$.

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
x^4+2x^3, \ x\lt -2\\
-x^4-2x^3, \ x\geq -2\\
\end{matrix}
\right.\\

f'(x)=\left\{
\begin{matrix}
4x^3+6x^2, \ x \lt -2\\
-4x^3-6x^2, \ x \geq 2
\end{matrix}
\right.\\\\
f'(x)=0 \Leftrightarrow
x^2(4x+6)=0 \implies x=0 \vee x=-\frac{6}{4}, \ sprzeczne \ z \ x\lt -2\\
-x^2(4x+6)=0 \implies x=0 \vee x=-\frac{6}{4}, \ sprzeczne \ z \ x\geq -2\\
f(0)=0\\
f(-\frac{6}{4})=-1,6875\\\\
Krance \ przedzialow:\\
f(-4)=-128\\
f(1)=3\\\\
Funkcja \ nie \ rozniczkowalna \ w \ x=-2\\
f(-2)=0\\\\
Najmniejsza \ wartosc -128\\
Najwieksza \ wartosc -3\\
\end{gathered}$$

---
**Drugi przykład:** Wyznacz najmniejszą i największą wartość funkcji $f(x)=x^x$ osiąganą na całej dziedzinie.

$$\begin{gathered}
f(x)=e^{\ln{x}\cdot x}\\
f'(x)=e^{\ln{x}\cdot x}\cdot (\frac{1}{x}\cdot x+\ln{x})=(1+\ln{x})\cdot e^{\ln{x}\cdot x}=x^x(1+\ln{x})\\
\mathbb{D}_{f}=(0,+\infty)\\
f'(x)=0 \Leftrightarrow \ln{x}=-1 \implies x=\frac{1}{e}\\
\lim_{x\to 0}{x^x}=e^{\lim_{x\to 0}{\ln{x}\cdot x}}=e^{\lim_{\frac{1}{t}\to 0}{\ln{\frac{1}{t}}\cdot \frac{1}{t}}}=e^{\lim_{t\to \infty}{\frac{\ln{\frac{1}{t}}}{t}}}\\
\lim_{t\to \infty}{\frac{\ln{\frac{1}{t}}}{t}}=
\lim_{t\to \infty}{-\frac{\ln{t}}{t}}=(Z \ Hospitala)=\lim_{t\to \infty}{-\frac{1}{t}}=0 \implies \lim_{x\to 0} x^x=e^0=1\\
\lim_{x\to \infty} x^x=\infty
\end{gathered}$$
---
### Twierdzenie Taylora

*Założenia:*
1. $U$ - otoczenie punktu $x_0$
2. $x\in U$
3. $f\in C^n(U)$
*Teza:* $\exists c \in (x_0, x)$:
$f(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+...+\frac{f^{n-1}(x_0)}{(n-1)!}(x-x_0)^{n-1}+R_n(x_0,x)$
Gdzie $R_n(x_0,x)=\frac{f^{(n)}(c)}{n!}(x-x_0)^n$ - *reszta Lagrange'a we wzorze Taylora*

Czyli:

$f(x)=\sum^{n-1}_{k=0}\frac{f^k(x_0)}{k!}(x-x_0)^k+R_n(x_0,x)$
Gdzie przyjmujemy, że $f^{0}(x)=f(x)$

*Inny zapis wzoru Taylora: $h=x-x_0$*

$f(x_0+h)=f(x_0)+\frac{f'(x_0)}{1!}h+\frac{f''(x_0)}{2!}h^2+...+\frac{f^{n-1}(x_0)}{(n-1)!}h^{n-1}+R_n(x_0,x)$
Gdzie $R_n(x_0,x)=\frac{f^{(n)}(c)}{n!}h^n$
*Inny zapis reszty Lagrange'a:*
$\exists \theta \in (0,1) \ R_n(x)=\frac{f^{(n)}(x_0+\theta(x-x_0))}{n!}(x-x_0)^n$


*Jeśli $x_0=0$, to wzór Taylora nazywany jest wzorem Maclaurina*
$f(x)=f(0)+\frac{f'(0)}{1!}x+...+\frac{f^{n-1}(0)}{(n-1)!}x^{n-1}+R_n(x)$

$R_n(x)=\frac{f^{(n)}(c)}{n!}x^n$,  $c\in (0,x)$

![[tumblr_n9ejwiGSbi1tzs5dao1_r2_1280 (1).gif]]
Taka jakby aproksymacja funkcji wielomianami.

*Definicja:*
Wielomian $W(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\dots+\frac{f^{(n-1)}}{(n-1)!}(x-x_0)^{n-1}$ nazywamy wielomianem Taylora dla funkcji $f$ w punkcie $x_0$.

Spostrzeżenie:  $\forall k=0,\dots,n-1 \ \ W^{(k)}(x_0)=f^{(k)}(x_0)$

*Wniosek:*
1. $f(x)=\approxeq W(x) \ \ \forall x \in U$
2. $|f(x)-W(x)|=|R_n(x)| \ \ \forall x \in U$

**Przykład:** Oblicz $\sqrt[10]{e}$ z dokładnością do $10^{-4}$.

$$\begin{gathered}
\sqrt[10]{e}=e^{\frac{1}{10}}:\\
e^x=e^0+\frac{(e^0)'}{1!}x+\dots+\frac{f^{(n-1)})(0)}{(n-1)!}x^{n-1}+R_n(x)\\
e^{x}=1+x+\frac{x^2}{2}+\frac{x^3}{6}+\dots+\frac{x^n}{n!}+R_n(x)\\
e^{\frac{1}{10}}\approx1+\frac{1}{10}+\frac{1}{200}+\frac{1}{6000}+\frac{1}{240000}\approx 1.0517
\end{gathered}$$
---
### 2 Warunek wystarczający istnienia ekstremum lokalnego.

*Założenia:*
1. $U$ - otoczenie punktu $x_0$
2. $f \in C^2(U)$
3. $f'(x_0)=0$

*Teza:*
1. Jeśli $f''(x_0)\gt 0$, to $f$ przyjmuje minimum lokalne w $x_0$
2. Jeśli $f''(x_0)\lt 0$, to $f$ przyjmuje maksimum lokalne w $x_0$

Jak w liceum było tak w skrócie.

**No i dalsze rozwinięcie w przypadku kiedy nawet $f''(x_0)=0$**

*Założenia:*
1. $U$ - otoczenie punktu $x_0$
2. $f \in C^2(U)$
3. $f'(x_0)=f''(x_0)=\dots=f^{(2n-1)}(x_0)=0$

*Teza:*
1. Jeśli $f^{(2n)}(x_0)\gt 0$, to $f$ przyjmuje minimum lokalne w $x_0$
2. Jeśli $f^{(2n)}(x_0)\lt 0$, to $f$ przyjmuje maksimum lokalne w $x_0$

**Przykład:** Pokaż, że $f(x)=x^4$ ma minimum lokalne w 0.

$$\begin{gathered}
f'(x)=4x^3\\
f''(x)=12x^2\\
f'''(x)=24x\\
f''''(x)=24, 24 \gt 0\\
Czyli \ to \ jest \ minimum \ lokalne.
\end{gathered}$$

---
