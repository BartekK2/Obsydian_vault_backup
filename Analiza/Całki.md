
### Symbole:

$\int dx$ - całka pojedyncza nieoznaczona
- całki z podstawowych wzorów
- całki funkcji wymiernych
- całki przez podstawienie
- całki przez części

$\int \int f(x,y) dx dy$ - całka podwójna

$\int^{b}_{a} f(x)dx$ - całka pojedyncza oznaczona


$d(coś)$ oznacza nam że całkujemy po iksie, na przykład:
$\int y \  dx=yx+c$

$\int yx \ dy=x\cdot \int y \ dy=x\cdot \frac{y^2}{2}$

W tych przykładach $y$ dla $dx$ traktowaliśmy jako stałą i analogicznie na odwrót.

---
### Podstawowe wzory całek:

**Ważne - nie zapominaj o $dx$ oraz $+c$.

$\int x^n dx=\frac{x^{n+1}}{n+1}+c$ ponieważ $(\frac{1}{n+1}\cdot x^{n+1}+c)'=\frac{n+1}{n+1}x^{n+1-1}=x^n$ dla $n \neq -1$
- $\int x^5 dx = \frac{x^6}{6}+c$
- $\int \frac{1}{x^4} dx=\int x^{-4} dx=\frac{x^{-3}}{-3}+c$ ponieważ $(-\frac{1}{3}x^{-3}+c)'=x^{-4}$

**Operacje arytmetyczne w całce**:
$\int (2x^{-3}-\frac{1}{x^2}+2) dx = \int 2x^{-3} dx - \int \frac{1}{x^2} dx + \int 2 dx$:
- $\int 2x^{-3} dx=2\cdot \int x^{-3} dx= 2\cdot( \frac{x^{-2}}{-2}+c)$
- $\int \frac{1}{x^2} dx=\int x^{-2} dx=\frac{x^{-1}}{-1}+c$
- $\int 2 \ dx=2x+c$
$\dots= -x^{-2}+x^{-1}+2x+c$

**Ta wiedza pozwala nam liczyć niektóre pierwiastki, ilorazy itd...**

$\int (\sqrt{x^3}+\frac{1}{x}+3x^7-5) dx=\int (x^{\frac{3}{2}}+\frac{1}{x}+3x^7-5)\ dx=\frac{x^{\frac{5}{2}}}{\frac{5}{2}}+\ln{|x|}+3\frac{x^8}{8}-5x+c$
$\int (\frac{3}{x}-\frac{5}{\sqrt{x}}+\frac{x\cdot x^2}{\sqrt[3]{x}})dx=\int (3\cdot \frac{1}{x}-5\cdot x^{-\frac{1}{2}}+x^{3-\frac{1}{3}})dx=3\ln{|x|}-5\cdot \frac{x^{\frac{1}{2}}}{\frac{1}{2}}+\frac{x^{\frac{11}{3}}}{\frac{11}{3}}=3\ln{|x|}-10\cdot x^{\frac{1}{2}}+\frac{3}{11}x^{\frac{11}{3}}+c$
$\int (\frac{x\sqrt{x}+2x^3}{\sqrt[4]{x^5}}) dx=\int (x^{\frac{3}{2}-\frac{5}{4}}+2x^{3-\frac{5}{4}}) dx=\int (x^{\frac{1}{4}}+2x^{\frac{7}{4}}) dx=\frac{x^{\frac{5}{4}}}{\frac{5}{4}}+2\frac{x^{\frac{11}{4}}}{\frac{11}{4}}+c=\frac{4}{5}\cdot x^{\frac{5}{4}}+\frac{8}{11}\cdot x^{\frac{11}{4}}+c$
---
**Co w przypadku gdy całkujemy jakiś sinus albo cosinus albo $e^x$? **

$\int (\sin{x}+e^x+\cos{x}) \ dx=\int \sin{x} \ dx + \int e^x \ dx + \int \cos{x} \ dx=-\cos{x}+e^x+\sin{x}+c$

No po prostu, zastanawiamy się co zróżniczkowane da nam to co całkujemy :LiSmile:

Łatwo się tu pomylić przy $\sin{x}$ ponieważ $(\cos{x})'=-\sin{x}$ zatem $\int -\sin{x}\  dx=\cos{x}$
**Najlepiej sobie zróżniczkować wynik i sprawdzić.**

---
$$\begin{gathered}
\int{(\ln{x})^2 \ dx}=\begin{vmatrix}
t=\ln{x}\\
dt=\frac{1}{x}\ dx\\
dx=dt\cdot x=dt \cdot e^t
\end{vmatrix}=
\int{t^2 \cdot x \ dt}=
\int{t^2 \cdot e^t \ dt}=\begin{vmatrix}
u=t^2&v=e^t\\
u'=2t&v'=e^t
\end{vmatrix}=\\\\
=t^2e^t-\int{2t\cdot e^t\ dt}=\begin{vmatrix}
u=2t&v=e^t\\
u'=2&v'=e^t
\end{vmatrix}=
t^2e^t-(2t\cdot e^t-\int{2e^t)}=\\\\
=t^2e^t-2t\cdot e^t+2e^t+C=(\ln{x})^2x-2\ln{x}\cdot x+2x+C
\end{gathered}$$


---
$$\begin{gathered}
\int{x\cdot (\ln{x})^2\ dx}=\begin{vmatrix}
u=(\ln{x})^2&v'=x\\
u'=2\ln{x}\cdot \frac{1}{x} & v=\frac{1}{2}x^2
\end{vmatrix}=\ln{x}^2\cdot \frac{1}{2}x^2-\int{\ln{x}\cdot  x}=\\
\\
=\begin{vmatrix}
u=\ln{x}&v'=x\\
u'=\frac{1}{x}&v=\frac{1}{2}x^2
\end{vmatrix}=

\ln{x}^2\cdot \frac{1}{2}x^2-(\ln{x}\cdot \frac{1}{2}x^2-\frac{1}{2}\frac{x^2}{2})=\\\\
=\ln{x}^2\cdot \frac{1}{2}x^2-\ln{x}\cdot \frac{1}{2}x^2+\frac{x^4}{4}+C
\end{gathered}$$

---
$$\begin{gathered}
\int{\frac{e^{-2x}}{\sqrt{4+e^{-2x}}}\ dx}=\begin{vmatrix}
t=e^{-2x}\\
dt=-2e^{-2x}\ dx
\end{vmatrix}=-\frac{1}{2} \int{ \frac{1}{\sqrt{4+t}} \ dt}=
\begin{vmatrix}
t_2=\sqrt{4+t}\\
dt_2=\frac{1}{2\sqrt{4+t}}\ dx
\end{vmatrix}=\\
=-\frac{1}{2}\int{2 \ dt_2}=-t_2=-\sqrt{4+e^{-2x}}+C
\end{gathered}$$

Sposób babki z matmy:
Podstawienie t żeby zabrać jak najwięcej
$$\begin{gathered}
\int{\frac{e^{-2x}}{\sqrt{4+e^{-2x}}}\ dx}=\begin{vmatrix}
t=4+e^{-2x}\\
t'=-2e^{-2x}
\end{vmatrix}=-\int{ \frac{1}{2\sqrt{t}}}=-\sqrt{t}+C=-\sqrt{4+e^{-2x}}+C
\end{gathered}$$

---
