## Rachunek całkowy funkcji jednej zmiennej
#### 2025-01-07
##### Poprzednia: [[Analiza - 6]]
##### Następna: [[Analiza - 8]]
##### Zadania: [[]]

#rachunek_całkowy #całki #analiza 

--- 
### Definicja całki nieoznaczonej

**Definicja:**
$f : I \to \mathbb{R}$   $I \subseteq \mathbb{R}$ 

Funkcję $F: I \to \mathbb{R}$ nazywamy funkcją pierwotną funkcji $f$ na przedziale $I \leftrightarrow$ gdy $\forall x \in I \ \ \ F'(x)=f(x)$

Czyli mianem funkcji pierwotnej funkcji $f$ w danym przedziale określamy funkcję której pochodna jest równa $f$ w danym przedziale.

---

**Definicja:**

Zatem jeśli funkcja $f$ ma funkcję pierwotną na $I$, to $f$ nazywamy *całkowalną* w sensie Newtona na $I$.

Czyli mówimy że funkcja jest całkowalna jeśli istnieje taka funkcja której pochodna zawsze w tym przedziale jest równa tej funkcji.

---
**Przykład: Wyznacz funkcje pierwotne funkcji $f(x)=2x$ oraz funkcji $g(x)=\frac{1}{x}$.
$$\begin{gathered}
f(x)=2x\\
F'(x)=2x\\
F(x)=x^2+c\\\\
g(x)=\frac{1}{x}\\
G'(x)=\frac{1}{x}\\
G(x)=\log{x}+c
\end{gathered}$$

---
**Twierdzenie:**
Zał:
$F$ jest funkcją pierwotną funkcji $f$ na $I$. 

Teza: $G$ jest funkcją pierwotną funkcji $f$ na $I \leftrightarrow \exists C \in \mathbb{R} \ \forall x \in I \ G(x)=F(x)+C$

Czyli w skrócie - pochodna z $f_1(x)=x^2+4$  ($f'_1(x)=2x$) jest równa pochodnej z funkcji $f_2(x)=x^2+100$ zatem całka z $f(x)=2x$ to będzie $\int f(x)=x^2+C$.

---
**Definicja:** 
$f$ jest całkowalna w sensie Newtona
$F$ - funkcja pierwotna funkcji $f$ 
Całką nieoznaczoną funkcji $f$ nazywamy zbiór wszytkich funkcji pierwotnych funkcji $f$, czyli:
$$\begin{gathered}
\{F(x)+C: C\in \mathbb{R}\}
\end{gathered}$$
Zapis: $\int f(x)dx = F(x)+C, C\in \mathbb{R}$ 
$\int$ - symbol całki
$x$ - zmienna calkowania
$f(x)$ - funkcja podcałkowa
$C$ - stała całkowania

---
### Definicja całki oznaczonej

**Definicja:**
$f$ - całkowalna w sensie Newtona
$F$ - funkcja pierwotna funkcji $f$ na $[a,b]$ 
Całkę oznaczoną (Newtona) nazywamy:
$$\begin{gathered}
\int^{b}_{a}{f(x)\ dx}\overset{df}{=}F(b)-F(a)\ \ \text{- liczba}
\end{gathered}$$
$a$ - dolna granica całkowania
$b$ - górna granica całkowania
Inny zapis: $F(b)-F(a)=[F(x)]\overset{b}{a}=F(x)|\overset{b}{a}$

**Spostrzeżenie:**
Wartość całki oznaczonej nie zależy od wyboru funkcji pierwotnej tzn. jeśli $F$ i $G$ są funkcjami pierwotnymi funkcji $f$ na $[a,b]$, to:
$$\begin{gathered}
\int^{b}_{a}{f(x) \ dx} = F(b)-F(a)=G(b)-G(a)
\end{gathered}$$
Czyli np:

$$\begin{gathered}
\int{2x \ dx} = x^2+ C\\
F(x) = x^2+4\\
G(x)=x^2-2
\\
\int^{4}_{2}{2x \ dx} = F(4)-F(2)=G(4)-G(2)=12
\end{gathered}$$

---
**Twierdzenie:**

*Warunek wystarczający istnienia funkcji pierwotnej*
Jeśli funkcja $f$ jest ciągła na $I$, to $f$ ma pierwotną na $I$.

*Lecz uwaga:* Funkcja pierwotna funkcji elementarnej niie musi być funkcją elementarną!
np. $\int{e^{-x^2} \ dx}$ 

---
### Całki funkcji elementarnych:
$$\begin{gathered}
\int{0 \ dx} = 0+C\\
\int{a \ dx} = ax+C\\
\int{x^r \ dx} = \frac{x^{r+1}}{r+1}+C, \ \ r \neq -1\\
\int{\frac{1}{x} \ dx}=\ln{|x|}+C\\
\int{a^x \ dx}=\frac{a^x}{\ln{a}}+C\\
\int{e^x \ dx} = e^x+C\\
\int{\sin{(x)} \ dx} = -\cos{x}+C\\
\int{\cos{(x)} \ dx} = \sin{x}+C\\
\int{\frac{1}{\cos^2{x}} \ dx} = \tan{x}+C\\
\int{\frac{1}{\sin^2{x}} \ dx} = -\cot{x}+C\\
\int{\frac{1}{1+x^2} \ dx} = \arctan{x}+C\\
\int{\frac{1}{\sqrt{1-x^2}} \ dx} = \arcsin{x}+C\\
\end{gathered}$$
---
### Twierdzenia o całce z sumy funkcji, całce funkcji pomnożonej przez liczbe

**Podobnie jak było w przypadku pochodnych**:
1. $\int{[f(x)+g(x)] dx}=\int{f(x) \ dx} + \int{g(x) \ dx}$
2. $\int{[af(x)] \ dx}=a \int{f(x) \ dx}$

**Przykład:**
$\int{(2x^3-4x^2+2x+1) \ dx}=2\cdot\frac{x^4}{4}-4\cdot \frac{x^3}{3}+2\frac{x^2}{2}+x+C$

$\int{\frac{x^2}{1+x^2} \ dx}=\int{1-\frac{1}{1+x^2}}=x-\arctan{x}+C$

---
### Całkowanie przez części

**Twierdzenie: (wzór na całkowanie przez części)**
Jeżeli: $u,v \in C^{1}(I)$ - (czyli $u,v$ ciągłe na $I$ i różniczkowalne na $I$)

Wtedy:
$$
\begin{gathered}
\int{u(x)v'(x) \ dx} = u(x)\cdot v(x) - \int{u'(x)v(x) \ dx}
\end{gathered}
$$
**INTUICYJNY DOWÓD:**
Całkowanie przez części wynika z wzoru na pochodną iloczynu:
$$\begin{gathered}
(u(x)\cdot v(x))' = u'(x)v(x)+u(x)v'(x)\\
\int{(u(x)\cdot v(x))' \ dx} = \int{u'(x)v(x)+u(x)v'(x) \ dx} = \int{u'(x)v(x) \ dx} + \int{u(x)v'(x) \ dx}\\
u(x)\cdot v(x) = \int{u'(x)v(x)\ dx } + \int{u(x)v'(x)\ dx}\\
\int{u(x)v'(x) \ dx} = u(x)\cdot v(x) -\int{u'(x)v(x) \ dx}
\end{gathered}$$
---
**Przykłady:**
$I$ 
$$\begin{gathered}
\int{x^2\sin{x} \ dx}=\int{u(x)v'(x)}\\
u(x)=x^2, \ v(x)=-\cos{x}\\\\
\int{x^2\sin{x} \ dx}=x^2\cdot -\cos{x}-\int{2x\cdot -\cos{x}}:\\
u_2(x)=2x, \ \ v_2(x)=-\sin\\\\
=x^2\cdot - \cos{x}-(2x\cdot -\sin{x}-\int{-2\sin{x}})=\\
=x^2\cdot -\cos{x}+2x\sin{x}+2\cdot \cos{x}+C
\end{gathered}$$
**Tutaj kilkukrotnie zastosowaliśmy całkowanie przez części.**
$$\begin{gathered}
\int{x^2\cdot \ln{x} \ dx}=\int{\ln{x}\cdot x^2 \ dx}:\\
u(x)=\ln{x}, \ \ \ v(x)=\frac{x^3}{3}\\\\
\dots = \ln{x}\cdot \frac{x^3}{3}-\int{\frac{1}{x}\cdot \frac{x^3}{3}}=\ln{x}\cdot \frac{x^3}{3}-\frac{1}{3}\int{x^2}=\ln{x}\cdot \frac{x^3}{3}-\frac{x^3}{9}
\end{gathered}$$

$II$ 
$$\begin{gathered}
\int{e^x\cdot \sin{x} \ dx}=\int{\sin{x}\cdot e^x} = \sin{x}\cdot e^x-\int{\cos{x}\cdot e^x}=\\
=\sin{x}\cdot e^x-(\cos{x}\cdot e^x-\int{-\sin{x}\cdot e^x})=\\
=\sin{x}\cdot e^x -\cos{x}\cdot e^x +\int{-\sin{x}\cdot e^x}\\\\
\int{\sin{x}\cdot e^x} =\sin{x}\cdot e^x -\cos{x}\cdot e^x +\int{-\sin{x}\cdot e^x}\\
\int{\sin{x}\cdot e^x} =\sin{x}\cdot e^x -\cos{x}\cdot e^x -\int{\sin{x}\cdot e^x}\\
2\cdot \int{\sin{x}\cdot e^x} =\sin{x}\cdot e^x -\cos{x}\cdot e^x\\
\int{\sin{x}\cdot e^x} =\frac{\sin{x}\cdot e^x -\cos{x}\cdot e^x}{2}+C\\
\end{gathered}$$
**Tutaj idąc krok po kroku metodą całkowania przez części dotarliśmy do tej samej całki od której zaczynaliśmy. Można ją wtedy przerzucić na lewą strone i dokończyć równanie.**

---
### Twierdzenie o całkowaniu przez podstawienie

**Założenia:**
1. $f: J \to \mathbb{R}, \ \ \ f \  \text{całkowalna na} \ J$
2. $\varphi: \ I \to J, \ \ \varphi \in C^1(I)$

Czyli mamy funkcje całkowalną oraz drugą funkcje której zbiór wartości jest równy z dziedziną tej pierwszej funkcji. (W końcu mowa o funkcjach złożonych więc musi tak być!)

**Teza:**
$$\begin{gathered}
\int{f(\varphi(x))\cdot \varphi'(x) \ dx}=F(\varphi(x))+C
\end{gathered}$$

**Przykłady:**
$$\begin{gathered}
\int{2\cos{2x} \ dx}=\sin{2x}+C
\end{gathered}$$
---
$$\begin{gathered}
\int{(3x-5)^{10} \ dx}:\\
f(x)=x^{10}\\
\varphi=3x-5\\\\
\int{(3x-5)^{10}\ dx}=\frac{1}{3}\int{(3x-5)^{10}\cdot 3 \  dx}=\frac{1}{3}\frac{(3x-5)^{11}}{11}=\frac{(3x-5)^{11}}{33}+C
\end{gathered}$$
---
$$\begin{gathered}
\int{\frac{x}{\sqrt{1-x^2}} \ dx}=\int{\sin{(\arcsin{x})}\cdot (\arcsin{x})' \ dx}=-\cos{\arcsin{x}}=-\sqrt{1-x^2}
\end{gathered}$$
---
**Spostrzeżenie:**
$$\int{\frac{f'(x)}{f(x)}}=
\begin{vmatrix}
t=f(x)\\
dt=f'(x) \ dx
\end{vmatrix}=\int{\frac{1}{t}\ dt} = \ln{|t|}+C=\ln{|f(x)|}+C
$$

$$\begin{gathered}
\text{Wynika to z tego że tutaj przyjmujemy że:}\\
g(x)=\frac{1}{x} \text{ nastepnie podstawiamy pod  funkcje } f(x)\\
\text{A z wzoru: } \int{g(f(x))\cdot f'(x)} \ \text{wychodzi nam} \int{\frac{f'(x)}{f(x)}}
\end{gathered}$$
**Przykłady:**
$\int{\tan{x} \ dx}=\int{\frac{\sin{x}}{\cos{x}}}=\int{\frac{1}{\cos{x}}\cdot -(\cos{x})'\ dx}=-\ln{|\cos{x}|}+C$

$$\begin{gathered}
\int{\arctan{x} dx}=\begin{vmatrix}
u=\arctan{x}&v=x\\
u'=\frac{1}{1+x^2}&v'=1
\end{vmatrix}=\arctan{x}\cdot x - \int{\frac{x}{1+x^2}}=\\
=\arctan{x}\cdot x-\frac{1}{2}\int{\frac{2x}{1+x^2}}=\arctan{x}\cdot x-\frac{\ln{|x^2+1|}}{2} +C
\end{gathered}$$
---
### Całkowanie funkcji wymiernych
$f(x)=\frac{P(x)}{Q(x)}$
$P(x), Q(x)$ - wielomiany

**Definicja:**
Funkcję wymierna nazywamy *właściwą* jeśli stopień wielomianu w liczniku jest mniejszy od stopnia wielomianu w mianowniku.

**Spostrzezenie:**
Każdą funkcję wymierną da się przedstawić w postaci sumy wielomianu i funkcji wymiernej właściwej.

**Twierdzenie:**
Każdy wielomian $Q(x)$ da się rozłożyć na iloczyn wielomianów stopnia pierwotnego i wielomianów nierozkładalnych stopnia drugiego.
$$\begin{gathered}
Q(x)=a_n(x-x_1)^{k_1}\cdot (x-x_2)^{k_2} \cdot \dotsc \cdot (x^2+p_1x+q_1)^{l_1}\cdot (x^2+p_2x+q_2)^{l_2}\cdot \dotsc, \\ 
\text{gdzie } \Delta=p_i^2-4q_i\lt 0 \text{ dla każdego i.}
\end{gathered}$$
**Przykład:**
$x^4+1=(x^2-1)(x^2+1)=(x-1)(x+1)(x^2+1)$
$x^4+1=(x^2-\sqrt{2}x+1)(x^2+\sqrt{2}x+1)$

**Twierdzenie:**
Każdą funkcję wymierną właściwą da się w jednoznaczny sposób zapisać w postaci:
$$\begin{gathered}
\frac{R(x)}{Q(x)}=\frac{A_1}{x-x_1}+\frac{A_2}{(x-x_1)^2}+\dotsc+\frac{A_k}{(x-x_1)^k}+\dotsc \text{ - ułamki proste I rodzaju}\\
+\frac{B_1x+C_1}{(x^2+p_1x+q_1)}+\frac{B_2x+C_2}{(x^2+p_1x+q_1)^2}+\dotsc+\frac{B_lx+C_l}{(x^2+p_1x+q_1)^l}+\dotsc \text{ - ułamki proste II rodzaju}
\end{gathered}$$

**Przykład:**
Rozłóż na sumę ułamków prostych funkcje:
$$\begin{gathered}
\frac{4}{x^4-1}=\frac{4}{(x-1)\cdot (x+1)\cdot (x^2+1)}=\frac{A}{x-1}+\frac{B}{x+1}+\frac{Cx+D}{x^2+1}\\\\
\frac{4}{(x-1)\cdot (x+1)\cdot (x^2+1)}=\frac{A}{x-1}+\frac{B}{x+1}+\frac{Cx+D}{x^2+1} \ /\cdot M\\\\
4=A(x^3+x^2+x+1)+B(x^3+x-x^2-1)+Cx^3-Cx+Dx^2-D\\
4=x^3(A+B+C)+x^2(A-B+D)+x(A+B-C)+A-B-D
\\\\
\left\{
\begin{matrix}
A+B+C=0\\
A-B+D=0\\
A+B-C=0\\
A-B-D=4
\end{matrix}
\right. \ \ \ 
\left\{
\begin{matrix}
A+B+C=0\\
A-B+D=0\\
A=-B\\
A-B-D=4
\end{matrix}
\right. \ \ \ 
\left\{
\begin{matrix}
C=0\\
A-B+D=0\\
A=-B\\
A-B-D=4
\end{matrix}
\right. \ 
\left\{
\begin{matrix}
C=0\\
-2B+D=0\\
A=-B\\
-2B-D=4
\end{matrix}
\right. \ 
\left\{
\begin{matrix}
C=0\\
D=-2\\
A=1\\
B=-1
\end{matrix}
\right. \ 
\\\\
\text{Zatem:}\\
\frac{4}{x^4-1}=\frac{1}{x-1}-\frac{1}{x+1}-\frac{2}{x^2+1}
\end{gathered}$$

Następnie jak już mamy taką funkcje wymierną rozłożoną, łatwiej ja zcałkować.

---
#### Całkowanie ułamków prostych $I$-go rodzaju:

$$\begin{gathered}
1. \ \int{\frac{1}{x-x_0}\ dx}=\ln{|x-x_0|+C}\\
2. \int{\frac{1}{(x-x_0)^n}\ dx}=\begin{vmatrix}
t=x-x_0\\
dt=dx
\end{vmatrix}=\int{t^{-n} \ dt} = \frac{t^{-n+1}}{-n+1}+C=\frac{1}{1-n}\cdot \frac{1}{(x-x_0)^{n-1}}+C
\end{gathered}$$

---
#### Całkowanie ułamków prostych $II$-go rodzaju:

**Twierdzenie (od Frydrycha):**
$$\begin{gathered}
I_n=\int{\frac{1}{(1+x^2)^n} \ dx}\\
I_1=\int{\frac{1}{1+x^2} \ dx}=\arctan{x}+C\\
I_n=\frac{x}{2(n-1)(1+x^2)^{n-1}} + \frac{2n-3}{2(n-1)}I_{n-1}
\end{gathered}$$

**Lepiej napisany wytłumaczony wzór od Ćmiela:**

$$\begin{gathered}
\int{\frac{Bx+C}{(x^2+px+q)^n}}=\frac{B}{2}\int{\frac{2x+p}{(x^2+px+q)^n}\ dx}+(C-\frac{Bp}{2})\int{\frac{dx}{(x^2+px+q)^n}}=\\
=\frac{B}{2}I_1+(C-\frac{B}{2})I_2\\\\
I_1=\int{\frac{2x+p}{(x^2+px+q)^n}}=\begin{vmatrix}
t=x^2+px+q\\
dt=(2x+p)dx
\end{vmatrix}=\int{\frac{dt}{t^n}}=
\left\{
\begin{matrix}
\ln{(x^2+px+q)+c}, \ \text{dla n}=1\\
\frac{1}{1-n}(x^2+px+q)^{1-n}+c, \text{dla n}\gt 1
\end{matrix}
\right.\\\\
I_2=\int{\frac{dx}{(x^2+px+q)^n}\ dx}=\int{\frac{dx}{\left((x+\frac{p}{2})^2+(q-\frac{p^2}{4})\right)^n}}=\\=\begin{vmatrix}
t=\frac{x+\frac{p}{2}}{\sqrt{q-\frac{p^2}{4}}}\\
dx=\sqrt{q-\frac{p^2}{4}}dt
\end{vmatrix}=\left(\frac{1}{\sqrt{q-\frac{p^2}{4}}}\right)^n\int{\frac{dt}{(t^2+1)^n}}\\\\
\text{gdzie ostatnią całke liczymy rekurencyjnie:}\\
\int{\frac{dt}{(t^2+1)^n}}=\int{\frac{t^2+1-t^2}{(t^2+1)^n}\ dt}=\int{\frac{1}{(t^2+1)^{n-1}}-\frac{t}{2}\frac{2t}{(t^2+1)^n}\ dt}=\\
=\int{\frac{1}{(t^2+1)^{n-1}}}-\int{\frac{t}{2}\frac{2t}{(t^2+1)^n}\ dt}=\begin{vmatrix}
u=\frac{t}{2}&v'=\frac{2t}{(t^2+1)^n}\\
u'=\frac{1}{2}&v=\frac{1}{1-n}(1+t^2)^{-n+1}
\end{vmatrix}=\\
=\int{\frac{1}{(t^2+1)^{n-1}}}+\frac{t}{2}\frac{1}{n-1}\frac{1}{(1+t^2)^{n-1}}+\frac{1}{2-2n}\int{\frac{1}{(1+t^2)^{n-1}}}
\end{gathered}$$


---
**Przykłady:**
$$\begin{gathered}
\int{\frac{2x+3}{x^2+2x+3} \ dx} = \int{\frac{2x+2}{x^2+2x+3} \ dx}+\int{\frac{1}{x^2+2x+3} \ dx}=\\
=\ln{|x^2+2x+3|} + C+\int{\frac{1}{(x+1)^2+2}\ dx}=\\=\ln{|x^2+2x+3|} + C+\int{\frac{1}{v^2+2} \ dv}=\\
=\begin{vmatrix}
t=\frac{v}{\sqrt{2}}\\
v=\sqrt{2}t\\
dv=\sqrt{2}\ dt
\end{vmatrix}=\ln{|x^2+2x+3|} + C+\int{\frac{1}{2t+2}\cdot \sqrt{2}\ dt}=\\
=\ln{|x^2+2x+3|} + C+\frac{1}{\sqrt{2}}\int{\frac{1}{t+1}\ dt}=\\
=\ln{|x^2+2x+3|} + C+\frac{1}{\sqrt{2}}\arctan{\frac{x+1}{\sqrt{2}}}
\end{gathered}$$
$$\begin{gathered}
\int{\frac{x+2}{(x^2+2x+2)^2} \ dx}=\begin{vmatrix}
t=x+2\\
dt=dx
\end{vmatrix}=\int{\frac{x+2}{((x+1)^2+1)^2}\ dx}=\begin{vmatrix}
u=x+1\\
dx=du
\end{vmatrix}=\\
=\int{\frac{u+1}{(u^2+1)^2} \ du}=\int{\frac{\frac{1}{2}(2u)+1}{(u^2+1)^2}}=
\frac{1}{2}\int{\frac{2u}{(u^2+1)^2} \ du} + \int{\frac{1}{(u^2+1)^2} \ du}=\\
=\begin{vmatrix}
v=u^2+1\\
dv=2u\ du
\end{vmatrix}=\frac{1}{2}\int{\frac{1}{v^2}}+\int{}
\end{gathered}$$
---
### Całkowanie funkcji niewymiernych

#### Podstawienie Eulera:

$$\begin{gathered}
\sqrt{ax^2+bx+c}=t-x\sqrt{a}\ \ \ /^2\\
ax^2+bx+c=t^2-2xt\sqrt{a}+ax^2\ \ \ /-ax^2+2xt\sqrt{a}-c\\
bx+2xt\sqrt{a}=t^2-c\\
x(b+2t\sqrt{a})=t^2-c\\
x=\frac{t^2-c}{b+2t\sqrt{a}}\\
dx=\left(\frac{t^2-c}{b+2t\sqrt{a}}\right)' \ dt\\
\sqrt{ax^2+bx+c}=t-\left(\frac{\sqrt{a}(t^2-c)}{b+2t\sqrt{a}}\right)
\end{gathered}$$

**Przykład: Pokaż że $\int{\frac{dx}{\sqrt{x^2+A}}}=\ln{(|x+\sqrt{x^2+A}|)}+C$

$$
\begin{gathered}
\int{\frac{1}{\sqrt{x^2+A}}\ dx}=\begin{vmatrix}
t-x=\sqrt{x^2+A}\\
t^2-2tx+x^2=x^2+A\\
t^2-2tx=A\\
t^2-A=2tx\\
x=\frac{t^2-A}{2t}\\
dx=\frac{t^2+A}{2t^2} \ dt
\end{vmatrix}=\int{\frac{2t}{t^2+A}\cdot \frac{t^2+A}{2t^2} \ dt}=\\\\=\int{\frac{1}{t}\ dt}=\ln{(x+\sqrt{x^2+A})}+C\\
\end{gathered}
$$

#### Metoda współczynników nieoznaczonych (Lagrange’a)

$$\begin{gathered}
\int{\frac{x^2}{\sqrt{4-x^2}} \ dx}=(Ax+B)\cdot \sqrt{4-x^2}+C\int{\frac{dx}{\sqrt{4-x^2}}}\\\\
\text{Różniczkujemy stronami:}\\\\
\frac{x^2}{\sqrt{4-x^2}}=A\cdot\sqrt{4-x^2}+(Ax+B)\cdot \frac{-x}{\sqrt{4-x^2}}+\frac{C}{\sqrt{4-x^2}}\\\\
\text{Mnożymy stronami razy:} \ \sqrt{4-x^2}\\\\
x^2=A(4-x^2)-(Ax+B)\cdot x+C\\
x^2=4A-Ax^2-Ax^2-Bx+C\\
x^2=x^2(-2A)+x(-B)+4A+C\\\\
\left\{
\begin{matrix}
A=-\frac{1}{2}\\
B=0\\
C=2
\end{matrix}
\right.\\\\
\int{\frac{x^2}{\sqrt{4-x^2}}\ dx}=-\frac{1}{2}x\cdot \sqrt{4-x^2}+2\int{\frac{dx}{\sqrt{4-x^2}}}
\end{gathered}$$

**Dokończ**

---
### Całkowanie funkcji trygonometrycznych

#### 1.  $\int{\sin^n{x}\cos^m{x}\ dx}$, $m,n \in \mathbb{Z}$

- Kiedy przynajmniej jedna z potęg jest nieparzysta: np. $m=2k+1$
  $$\begin{gathered}
\int{\sin^n{x}\cos^m{x}\ dx}=\int{\sin^n{x}(\cos^2{x})^k\cdot \cos{x} \ dx}=\\
=\begin{vmatrix}
t=\sin{x}\\
dt=\cos{x}\ dx\\
\cos^2{x}=1-t^2
\end{vmatrix}=\int{t^n(1-t^2)^k \ dt}=\dots
\end{gathered}$$
- Obie są parzyste:
  $$\begin{gathered}
\int{\sin^n{x}\cos^m{x} \ dx}=\begin{vmatrix}
\cos^2{x}=\frac{1+\cos{2x}}{2}\\
\sin^2{x}=\frac{1-\cos{2x}}{2}
\end{vmatrix}=
\end{gathered}$$
#### 2. $\sin{ax}\cos{bx}, \sin{ax}\sin{bx}, \cos{ax}\cos{bx}$

$$\begin{gathered}
\int{\sin{(\alpha x)}\cos{(\beta x)}\ dx}=\frac{1}{2}\int{\sin{(\alpha+\beta)}x+\sin{(\alpha-\beta)}x \ dx}\\
\int{\sin{(\alpha x)}\sin{(\beta x)}}=\frac{1}{2}\int{\cos{(\beta-\alpha)}x-\cos{(\alpha+\beta)}x \ dx}\\
\int{\cos{(\alpha x)}\cos{(\beta x)}] dx}=\frac{1}{2}\int{\cos{(\beta-\alpha)}+\cos{(\alpha+\beta)}\ dx}
\end{gathered}$$
#### 3. podstawienie $\tan{x}$ dla $\sin^2{x}, \cos^2{x}, \sin{x}\cos{x}$ 
$$\begin{gathered}
\int{\frac{dx}{\sin^2{x}\cos^4{x}}\ dx}=\begin{vmatrix}
t=\tan{x}\\
\sin^2{x}=\frac{\sin^2{x}}{\sin^2{x}+\cos^2{x}}=\frac{t^2}{t^2+1}\\
\cos^2{x}=\frac{\cos^2{x}}{\sin^2{x}+\cos^2{x}}=\frac{1}{t^2+1}\\
dt=\frac{1}{\cos^2{x}}=t^2+1\ dx
\end{vmatrix}=\int{\frac{1}{\frac{t^2}{t^2+1}\cdot \frac{1}{(t^2+1)^2}}\cdot \frac{1}{t^2+1}\ dt}=\\\\
=\int{\frac{(t^2+1)^2}{t^2}\ dt}=\int{\frac{t^4+2t^2+1}{t^2}\ dt}=\int{t^2+2+\frac{1}{t^2}\ dt}=\frac{t^3}{3}+2t-\frac{1}{t}=\\=
\frac{(\tan{x})^3}{3}+2\tan{x}-\frac{1}{\tan{x}}+C
\end{gathered}$$

#### 4. reszta - podstawienie $\tan{\frac{x}{2}}$, właściwie można tego użyć zawsze xd

$$\begin{gathered}
\int{\frac{\sin^n}{\cos^m}}=\begin{vmatrix}
\sin=\frac{2\sin{\frac{x}{2}}\cos{\frac{x}{2}}}{\sin{\frac{x}{2}^2}+\cos{\frac{x}{2}}^2}=\frac{2\frac{\sin}{\cos}}{\frac{\sin^2}{\cos^2}+1}=\frac{2t}{t^2+1}\\
t=\tan{\frac{x}{2}}\\
\cos=\frac{\cos^2{\frac{x}{2}}-\sin^2{\frac{x}{2}}}{\sin^2+\cos^2}=\frac{1-t^2}{t^2+1}
\end{vmatrix}
\end{gathered}$$

---
