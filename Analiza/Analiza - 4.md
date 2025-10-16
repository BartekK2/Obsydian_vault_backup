### Rachunek różniczkowy funkcji jednej zmiennej
#### 2024-10-16
##### Poprzednia: [[Analiza - 3]]
##### Następna: [[Analiza - 5]]
##### Zadania: [[]]

#rachunek_różniczkowy #pochodne #analiza  

---
### Rachunek różniczkowy funkcji jednej zmiennej

Jeśli istnieje granica właściwa $\lim_{x \to x_0}{\frac{f(x)-f(x_0)}{x-x_0}}$, to mówimy że funkcja $f$ jest różniczkowalna w punkcie $x_0$. Wartość tej granicy oznaczamy przez $f'(x_0)$ i nazywamy *pochodną* funkcji $f$ w punkcie $x_0$.

$$\begin{gathered}
f'(x_0) = \lim_{x \to x_0}{\frac{f(x)-f(x_0)}{x-x_0}}
\end{gathered}$$

Można to także zapisać z $h=x-x_0$ czyli jakby zmianą $x\to x_0$.
$$\begin{gathered}
f'(x_0) = \lim_{h \to 0}{\frac{f(x_0+h)-f(x_0)}{h}}
\end{gathered}$$
Jeszcze inny zapis:
$$\begin{gathered}
f'(x_0) = \frac{df}{dx}(x_0)
\end{gathered}$$
Czyli bezpośrednio zmiana wartości przez przyrost $x$ (dla $x_0$).
*Możemy też zdefiniować pochodne lewostronne i prawostronne (wynika to z [[Analiza - 3#^402f1e|granic lewostronnych i prawostronnych funkcji]].*

*Funkcja $f$ ma pochodną w punkcie $x_0$ wtedy i tylko wtedy kiedy pochodne jednostronne w punkcie $x_0$ istnieją i są sobie równe. Wynika to z [[Analiza - 3#^5106ce|warunku koniecznego na istnienie granicy funkcji]].*

*Funkcja musi być także ciągła w $f(x_0)$ aby  mieć pochodną w $x_0$*

###### Przykład: Czy funkcja $sgn$ ma pochodną w $x=0$?
Nie bo nie jest ciągła w x=0!
###### Przykład oblicz pochodną $\sqrt{x}$:
$$\begin{gathered}
\frac{\sqrt{x}-\sqrt{x_0}}{x-x_0}=\frac{\sqrt{x}-\sqrt{x_0}}{(\sqrt{x}-\sqrt{x_0})(\sqrt{x}+\sqrt{x_0})}=\frac{1}{\sqrt{x}+\sqrt{x_0}}\\\\
lim_{x\to x_0}{\frac{1}{\sqrt{x}+\sqrt{x_0}}}=\frac{1}{2\sqrt{x}}
\end{gathered}$$
---
### Interpretacja geometryczna pochodnej:
Funkcja $f$ jest różniczkowalna w $x_0 \Leftrightarrow$ istnieje styczna do wykresu funkcji $f$ w punkcie $(x_0, f(x_0))$.
Ponadto:
1. $\tan{\alpha} = f'(x_0)$, gdzie $\alpha$ jest kątem pomiędzy osią OX, a prostą styczną.
2. $y= f'(x_0)(x-x_0)+ f(x_0)$ jest równaniem stycznej do wykresu funkcji $f$ w punkcie $(x_0, f(x_0))$
###### Przykład: Wyznacz równanie stycznej do wykresu funkcji $f(x) = \sqrt{x}$ w punkcie $x_0=1$
$y=\frac{1}{2}(x-1)+1=\frac{1}{2}x+\frac{1}{2}$

---
### Wzory NAJWAŻNIEJSZYCH pochodnych funkcji elementarnych:
$$\begin{gathered}
(c)'=0\\
(\frac{1}{x})'=-\frac{1}{x^2}\\
(x^r)' = rx^{r-1}, \ r\in \mathbb{R}\\
W \ szczegolnosci:\\
(\sqrt{x})'=\frac{1}{2\sqrt{x}}\\
(\sin{x})'=\cos{x}\\
(\cos{x})'=-\sin{x}\\
(\tan{x})' = \frac{1}{\cos^2{x}}=1+\tan^2{x}\\
(\cot{x})'=-\frac{1}{\sin^2{x}}=-1-\cot^2{x}\\
(e^x)'=e^x\\
(a^x)'=a^x\cdot \ln{a}\\\\\
Odwrotne:\\
(arcsin \ x)'=\frac{1}{\sqrt{1-x^2}}, \ x\in(-1,1)\\
(arccos \ x)'=-\frac{1}{\sqrt{1-x^2}}, \ x\in(-1,1)\\
(arctg \ x)'=\frac{1}{1+x^2}\\
(arcctg \ x)'=-\frac{1}{1+x^2}\\
(ln \ x)' = \frac{1}{x}\\
(\log_a{x})' = \frac{1}{x\ln{a}}
\end{gathered}$$

---
### Twierdzenie o działaniach arytmetycznych na pochodnych:

$$\begin{gathered}
Zal. \ f \ i \ g \ rozniczkowalne \ w \ x:\\\\
1. (c\cdot f(x))' = c\cdot f'(x),  \ c \ - \ stala \in \mathbb{R}\\
Przyklad:
(3\cdot x)'=3\cdot 1=3\\\\
2. (f(x) \pm g(x))' = f'(x) \pm g'(x)\\\\
3. (f(x)\cdot g(x))' = f'(x)\cdot g(x) + f(x)\cdot g'(x)\\\\
4. (\frac{f(x)}{g(x)})' = \frac{f'(x)\cdot g(x) - f(x)\cdot g'(x)}{[g(x)]^2}

\end{gathered}$$
---
### Twierdzenie o pochodnej funkcji złożonej:
Założenia:
$f$ - różniczkowalna w $x_0$
$g$ - różniczkowalna w $f(x_0)$

Teza:
$g \circ f$ jest różniczkowalna w $x_0$ i $(g \circ f)'(x_0)=g'(f(x_0)) \cdot f'(x_0)$

##### Przykłady:

###### 1.
$$\begin{gathered}
h(x)=\sqrt{x^2+1}\\
g(x)=\sqrt{x}, \ \ f(x)=x^2+1\\
h'(x)=g'(f(x))\cdot f'(x)=\frac{1}{2\sqrt{x^2+1}} \cdot 2x\\\\
h(x)=cos^5(3x)\\
k(x)=x^5 \ f(x)=cos(x), \ g(x)=3x\\
(k\circ f)'=5(\cos{x})^4 \cdot -\sin{x}\\
(k \circ f) \circ g = 5(\cos{3x})^4\cdot -\sin{x} \cdot 3=-15\cos^4{3x}\cdot \sin{3x}\\\\
h(x)=x^x=e^{x \ln{x}}\\
h(x)=e^{x}, \ gdzie \ g(x)=x\ln{x}\\
h'(x)=e^{x\ln{x}}\cdot (x\ln{x})'=e^{x\ln{x}}\cdot(x'\cdot \ln{x}+\ln{x}'\cdot x)=e^{x\ln{x}}\cdot (\ln{x}+1)=x^x(\ln{x}+1)\\\\
\end{gathered}$$
###### 2.
$$\begin{gathered}
\cos^5{3x}\\
f(x)=cos^5{x}, \  \ g(x) = 3x\\
gdzie \ cos^5{x}:\\
h(x)=x^5, \ \ j(x)=cos{x}\\
czyli:\\
cos^5{x}=(h \circ j)\circ g:\\
(h\circ j)'=5\cos^4{x} \cdot -\sin{x}\\
[(h \circ j)\circ g]' = (5\cos^4{3x} \cdot - \sin{3x})\cdot 3=-15\cos^4{3x}\cdot \sin{3x}
\end{gathered}$$
###### 3.
$$\begin{gathered}
x^x=e^{\ln{x}\cdot x}\\
g(x)=e^{x}, \ \ h(x)=\ln{x} \cdot x\\
(x^x)'=g'(h(x))\cdot h(x)=e^{\ln{x}\cdot x}\cdot (\ln{x}\cdot x)'=\\
=x^x\cdot(\frac{1}{x}\cdot x + \ln{x}\cdot 1)=x^x(1+\ln{x})
\end{gathered}$$
###### 4.
$$\begin{gathered}
\cos{x^{\sin{x}}}:\\
g(x)=\cos{x}, \ \ h(x)=x^{\sin{x}}=e^{\ln{x}\cdot \sin{x}}\\
\cos{x^{\sin{x}}}=g(x)\circ h(x)\\
(\cos{x^{\sin{x}}})'=-\sin{e^{\ln{x}\cdot \sin{x}}}\cdot (e^{\ln{x}\cdot \sin{x}})'=\\
(f(x)=e^x, \ \ j(x)=\ln{x}\cdot \sin{x})\\
cd...\\
=-\sin{e^{\ln{x}\cdot \sin{x}}}\cdot e^{\ln{x}\cdot \sin{x}}\cdot (\frac{\sin{x}}{x}+(\cos{x}\cdot \ln{x}))=\\
=-\sin{x^{\sin{x}}}\cdot x^{\sin{x}} \cdot (\frac{\sin{x}}{x}+(\cos{x}\cdot \ln{x}))
\end{gathered}$$
###### 5.
$$\begin{gathered}
x^{x^x}=e^{\ln{x}\cdot x^x}:\\
g(x)=e^{x}, \ \ h(x)=\ln{x}\cdot x^x=\ln{x}\cdot e^{\ln{x}\cdot x}\\
(x^{x^x})' = e^{ln{x}\cdot e^{\ln{x}\cdot x}}\cdot (\ln{x}\cdot e^{\ln{x}\cdot x})'=x^{x^{x}}\cdot (\frac{1}{x}\cdot x^x+\ln{x}\cdot x^x)=\\
=(x^{x^x})\cdot (x^x)\cdot (\ln{x}+\frac{1}{x})
\end{gathered}$$



---
### Twierdzenie o pochodnej funkcji odwrotnej:
Założenia:
1. $f: U \to V$ jest bijekcją, gdzie $U$ jest otoczeniem punktu $x_0$ oraz $V$ jest otoczeniem punktu $y_0=f(x_0)$
2. $f$ jest różniczkowalna w $x_0$ 
3. $f'(x_0) \neq 0$

Teza: $f^{-1}$ jest różniczkowalna w $y_0=f(x_0)$ oraz $(f^{-1})'(y_0)=\frac{1}{f'(y_0)}$

![[diagram-20241103.png]]
##### Przykłady:

###### 1. $arccot(x)$
$$\begin{gathered}
(arccot(\cot{x}))' = x'\\
(arccot(\cot{x}))'\cdot \cot'{x}=1\\
(arccot(\cot{x}))'\cdot (-1-\cot^2{x})=1\\
(arccot(\cot{x}))' =-\frac{1}{(1+\cot^2{x})}\\
(arccot(x))'=-\frac{1}{1+x^2}\\\\
Czyli \ naszym \ f(x) \ musi \ byc \ konkretnie \ ta \ funkcja \ ktora \ odwracamy.
\end{gathered}$$
###### 2. $\ln{x}$
$$\begin{gathered}
(\ln{x})':\\
(\ln(e^x))'=x'\\
(\ln{e^x})' \cdot e^x=1\\
Czyli \ dla \ innego \ argumentu \ niz \ e^x, dla \ x:\\
(\ln{x})'=\frac{1}{x}
\end{gathered}$$
###### 3. $(\arcsin{x})'$
$$\begin{gathered}
(\arcsin{x})':\\
(\arcsin{sin{x}})'=x'\\
(\arcsin{sin{x}})'\cdot (\sin{x})'=1\\
(\arcsin{sin{x}})'\cdot \cos{x}=1\\
(\arcsin{sin{x}})'\cdot =\frac{1}{\cos{x}}\\\\
Z \ jedynki \ trygonometrycznej:\\
(\arcsin{sin{x}})'\cdot =\frac{1}{\sqrt{1-\sin^2{x}}}\\
(\arcsin{x})'\cdot =\frac{1}{\sqrt{1-x^2}}\\
\end{gathered}$$

#### Ważne spostrzeżenie (wprowadzenie do szeregu Taylora):
$f(x) \approx f(x_0)+f'(x_0)(x-x_0), \ dla \ x \ bliskich \ x_0.$

Wynika to z tego że $f'(x_0)$ przecież reprezentuje to jak rośnie funkcja, im mniejsze $x_0$ od $x$ tym bardziej dokładnie, ale z pewnym przybliżeniem można również dla większych $x_0$ liczyć takie wartości.

![[diagram-20241103 (3).png]]
###### Przykład: Oblicz przybliżoną wartość $\arctan{1.05}$
$$\begin{gathered}
Dla \ x_0 = 1\\\\
f(1.05)\approx f(1)+\frac{1}{1+1^2}(1.05-1)=\frac{\pi}{4}+0.025...
\end{gathered}$$

---
### Pochodne n-te funkcji:

*Def.*
Druga pochodna funkcji.
$f: U \to \mathbb{R}$, $f$ różniczkowalna w otoczeniu $U$ punktu $x_0$
$f': U \ni x \to f'(x) \in \mathbb{R}$ 

Drugą pochodną (pochodną 2-go rzędu) funkcji $f$ w punkcie $x_0$ nazywamy
$f''(x_0) = \lim_{x\to x_0}{\frac{f'(x)-f'(x_0)}{x-x_0}}$ o ile istnieje.
Prościej:
$f''(x)=(f'(x))'$

Ogólnie jeśli istnieje pochodna rzędu $(n-1)$-go funkcji $f$ w otoczeniu punktu $x$, to pochodna rzędu $n$-tego jest równa $f^{(n)}(x)=(f^{n-1}(x))'$

*Oznaczenia:*
$D^{n}(A)$ - zbiór funkcji $n$-krotnie różniczkowalnych na $A$ 
$C^{n}(A)$ - zbiór funkcji $n$-krotnie różniczkowalnych na $A$ i takich, że $f^{(N)}$ jest ciągła na $A$.
$C^{n}(A) \subset D^{n}(A)$

###### Przykład:
Wyznacz wzór na $n$-tą pochodną funkcji $f(x) = \ln{x}$.
$$\begin{gathered}
f'(x)=\frac{1}{x}=x^{-1}\\
f''(x)=-\frac{1}{x^2}=-x^{-2}\\
f^{(n)} = (-1)^n\cdot \frac{1}{x^n}
\end{gathered}$$
---
### Twierdzenia ekstremów
#### Twierdzenie o tym że pochodna dla $\max(f(x))$ i $\min(f(x))$ jest równa 0:

Dowód dla $x_0$ max:
$f(x_0) \gt f(x)$ bo max
jeżeli $x\lt x_0$ to pochodna (lewostronna) większa  bądź równa od 0 (bo mianownik: $x-x_0$ mniejszy od 0 a licznik $f(x)-f(x_0)$ też mniejszy od 0)

analogicznie dla prawostronnej wtedy prawostronna mniejsza bądź równa 0
i jeżeli lewostronna większa bądź równa 0 a prawostronna mniejsza bądź równa 0 to granica w tym punkcie równa 0. (Bo zakładamy że istnieje a jeśli istnieje to prawostronna równa lewej)

---
### Twierdzenia o wartości średniej rachunku różniczkowego
#### Twierdzenie Rolle'a
Jeżeli funkcja w przedziale $[a,b]$ osiąga te same wartości na krańcach to ma gdzieś w tym przedziale punkt gdzie pochodna równa 0. Albo dlatego że stała albo dlatego że $\min$ lub $\max$

Założenia:
1. $f \in C([a,b])$
2. $f \in D((a,b))$
3. $\exists{c} \in (a,b) \ \ f'(c)=0$
Dowód:
1. Jeśli $f$ stała to oczywiście $f'(c)=0$
2. Jeśli $f$ nie stała z [[Analiza - 3#^643abd| Twierdzenia Weierstrassa]] $\rightarrow \ \exists c \in (a,b) f(c)=\max_{x \in [a,b]}{f(x)} \vee  f(c)=\min_{x \in [a,b]}{f(x)}$ a z poprzedniego twierdzenia wiemy że wtedy $f'(c)=0$
#### Twierdzenie Lagrange'a

^31ed24

Jeżeli funkcja różniczkowalna w (a,b) to istnieje w tym przedziale takie c które jest ilorazem przyrostu wartości funkcji od b do a, z przyrostem b do a.
Założenia:
1. $f \in C([a,b])$
2. $f \in D((a,b))$
Teza:
$\exists c \in (a,b) \ f'(c) = \frac{f(b)-f(a)}{b-a}=\frac{f\Delta_{a\to b}}{\Delta_{a\to b}}$
#### Twierdzenie Cauchy'ego
Jeżeli funkcje f,g różniczkowalne w przedziale (a,b) to dla każdego x z tego przedziału takiego że pochodna $g'(x)$ różna od 0 to wtedy istnieje taki punkt w którym iloraz pochodnych tych dwóch funkcji jest równy ilorazie różnicy ich wartości.

Założenia:
1. $f,g \in C([a,b])$
2. $f,g \in D((a,b))$
3. $\forall x \in (a,b) \ g'(x) \neq 0$
Wtedy:
$\exists c \in (a,b) \frac{f'(c)}{g'(c)} = \frac{f(b)-f(a)}{g(b)-g(a)}$

*Twierdzenia Rolle'a, Lagrange'a i Cauchy'ego nazywamy twierdzeniami o wartości średniej rachunki różniczkowego.*

---
### Reguła de L'Hospitala!!!

^a2a2d9

Jeżeli granica ilorazu jest [[Analiza - 2#^669a6f|symbolem nieoznaczonym]] tzn. $\frac{\infty}{\infty}$ $\frac{0}{0}$ to jest ona równa granicy ilorazu pochodnych.
Założenia:
1. $f$ i $g$ są różniczkowalne w pewnym sąsiedztwie $S$ punktu $x_0$
2. $\forall x \in S \ g(x) \neq 0 \land g'(x) \neq 0$
3. $\left(\lim_{x \to x_0}{f(x)}=0 \land \lim_{x \to x_0}{g(x)}=0)\right.$ lub $\left(\lim_{x \to x_0}{f(x)}=\pm \infty \land \lim_{x \to x_0}{g(x)}=\pm \infty)\right.$
4. istnieje $\lim_{x\to x_0}{\frac{f'(x_0)}{g'(x_0)}}$
Teza: istnieje $\lim_{x\to x_0}{\frac{f(x)}{g(x)}}=\lim_{x\to x_0}{\frac{f'(x)}{g'(x)}}$

###### Przykłady - Oblicz granice:
$$\begin{gathered}
\lim_{x \to 0 }{\frac{x - \sin{x}}{x^3}}\\\\
\lim_{x \to 0 }{\frac{x - \sin{x}}{x^3}}=\lim_{x \to 0 }{\frac{(x - \sin{x})'}{(x^3)'}}=\lim_{x \to 0 }{\frac{1-\cos{x}}{3x^2}}=\\
=\lim_{x \to 0 }{\frac{(1-\cos{x})'}{(3x^2)'}}=\lim_{x \to 0 }{\frac{\sin{x}}{6x}}=\lim_{x \to 0 }{\frac{(\sin{x})'}{(6x)'}}=\lim_{x \to 0 }{\frac{\cos{x}}{6}}=\frac{1}{6}
\end{gathered}$$
$$\begin{gathered}
\lim_{x \to 0 }{x\ln{x}}\\\\
\lim_{x \to 0 }{x\ln{x}}=\lim_{x \to 0 }{\frac{(\ln{x})'}{(\frac{1}{x})'}}=
\lim_{x \to 0 }{\frac{\frac{1}{x}}{-\frac{1}{x^2}}}=\lim_{x \to 0 }{\frac{1}{x}\cdot x^2}=\lim_{x \to 0 }{-x}=0
\end{gathered}$$
$$\begin{gathered}
\lim_{x\to 0+}{x^x}=\lim_{x\to 0+}{e^{x\cdot \ln{x}}}=\lim_{x\to 0+}{e^{0}}=1
\end{gathered}$$
