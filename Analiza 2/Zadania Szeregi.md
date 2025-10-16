

##### 1. Pokaż że szereg jest zbieżny i oblicz jego sumę

###### a)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{3^n+4^n}{5^n}}:\\\
a_n=\frac{3^n+4^n}{5^n}\\
\lim_{n\to \infty}{\sqrt[n]{a_n}}=\frac{4}{5}\lt 1 \text{ z Cauchy'ego zbieżny}\\\\
\sum^{\infty}_{n=1}{\frac{3^n+4^n}{5^n}}=
\sum^{\infty}_{n=1}{(\frac{3}{5})^n}+
\sum^{\infty}_{n=1}{(\frac{4}{5})^n}=\frac{\frac{3}{5}}{1-\frac{3}{5}}+\frac{\frac{4}{5}}{1-\frac{4}{5}}=\frac{11}{2}
\end{gathered}$$

###### b)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}:\\\\
\text{znowu Cauchym albo alambertem udawadniamy zbieżność}\\\\
\frac{A}{3n-2}+\frac{B}{3n+1}=\frac{1}{(3n-2)(3n+1)}\\
A(3n+1)+B(3n-2)=1\\
A-2B=1\\
3(A+B)=0\\
A=-B\\
-3B=1\\
B=-\frac{1}{3}\\
A=\frac{1}{3}\\
\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}=\frac{1}{3}\sum^{\infty}_{n=1}{\frac{1}{3n-2}-\frac{1}{3n+1}}=\frac{1}{3}(\frac{1}{1}-\frac{1}{4}+\frac{1}{4}-\frac{1}{7}+\frac{1}{7}-\frac{1}{10})=\\
=\lim_{n \to \infty }\frac{1}{3}(1-\frac{1}{3n+1})=\frac{1}{3}
\end{gathered}$$

---
##### 2. Sprawdź czy następujące szeregi są zbieżne:


###### a) 
$$\begin{gathered}
\sum^{\infty}_{n=1}{\ln{(1+\frac{1}{n})}}=\ln(2)+\ln(\frac{3}{2})+\ln(\frac{4}{3})+\dots =\ln{n}=\infty\\
\end{gathered}$$

###### b)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(2n)!2^n}{2^{2n}}}\\\\
a_n=\frac{(2n)!2^n}{2^{2n}}\\\\
g=\lim_{n \to \infty}{|\frac{a_{n+1}}{a_n}|}=
\\=\lim_{n \to \infty}{|\frac{2n!\cdot (2n+1)(2n+2)2^n\cdot 2}{2^{2n}\cdot 2^2}\cdot \frac{2^{2n}}{(2n)!2^n}|}=\lim_{n\to \infty}{\frac{(2n+1)(2n+2)}{2}}=\infty\gt 1
\end{gathered}$$

###### c)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{n^3(\sqrt{2}+(-1)^n)^n}{3^n}}:\\
\sqrt{2}+1=\sqrt{2}(1+\frac{1}{\sqrt{2}})\lt \sqrt{2}\cdot 2\\\\
\sum^{\infty}_{n=1}{\frac{n^3(2\sqrt{2})^n}{3^n}}=\sum^{\infty}_{n=1}{b_n}\\
g=\lim_{n\to \infty}{|\frac{b_{n+1}}{b_n}|}=\lim_{n\to \infty}{\frac{(n+1)^3}{n^3}\cdot \frac{2\sqrt{2}}{3}}=\frac{2\sqrt{2}}{3}\lt 1
\end{gathered}$$

###### d)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{\cos^2{\frac{n\pi}{3}}}{2^n}}\lt 
\sum^{\infty}_{n=1}{\frac{1}{2^n}} =\frac{\frac{1}{2}}{1-\frac{1}{2}}=1- zbieżny
\end{gathered}$$

###### e)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{\cos{\frac{n\pi}{3}}}{2^n}}\lt 
\sum^{\infty}_{n=1}{\frac{1}{2^n}}\\\\
g=\lim_{n\to \infty}{|\frac{a_{n+1}}{a_n}|}=\lim_{n\to \infty}{|\frac{1}{2}\cdot \frac{1}{2}^n\cdot 2^n|}=\frac{1}{2}\lt 1 - zbieżny\\\\
\text{z kryterium porównawczego jak podobne wyżej}
\end{gathered}$$


###### f)
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^n\ln{n}}{n}}=
\sum^{\infty}_{n=1}{(-1)^n\cdot a_n}:\\\\
1. \frac{\ln{n}}{n}\gt 0\\
2. \lim_{n\to \infty}\frac{\ln{n}}{n}=0\\
3. malejący\\\\\
z \ tw. \ o \ szeregu \ naprzemiennym
\end{gathered}$$

###### g)

$$\begin{gathered}
S=\sum^{\infty}_{n=2}{\frac{1}{n\ln^2n}}\\
\int{\frac{1}{n\ln^2{n}}dn}=\begin{vmatrix}
u=\ln{n}\\
du=\frac{1}{n}\ dn
\end{vmatrix}=\int{\frac{1}{u^2}\ du}=\int{u^{-2} \ du}=-\frac{1}{\ln{n}}+C\\\\
\text{Chcemy żeby f była nierosnąca bo takie jest założenie kryterium całkowego}\\\\
(\frac{1}{n\ln^2{n}})'\dots\\
n\uparrow \forall n \in \mathbb{R}, \ln{n}\uparrow \forall n\in (e,+\infty)\\
n_0=e\\
\int^{+\infty}_{e}{\frac{1}{x\ln^2{x}}}=-\frac{1}{\ln{x}}|^{+\infty}_e=\lim_{x\to +\infty}{-\frac{1}{\ln{x}}}-(-\frac{1}{\ln{e}})=1\ zbiezne
\end{gathered}$$


###### h)
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{n+3}{n^3+3n-2}}=\sum^{\infty}_{n=1}{a_n}\\\\
b_n=\frac{1}{n^2}\\\\
\lim_{n\to \infty}\frac{a_n}{b_n}=\lim_{n\to \infty}{\frac{n^3+3n^2}{n^3+3n-2}}=1\in (0,+\infty)\\\\
\sum^{\infty}_{n=1}{b_n} - zbieżny \ na \ podstawie \ kryterium \ o \ szeregu\ harmonicznym \ rzad \gt 1\\
wiec \ na \ podstawie \ kryterium \ porownawczego \ granic \ ilorazowych\\\\
\sum^{\infty}_{n=1}{\frac{n+3}{n^3+3n-2}} - zbiezny
\end{gathered}$$


---
##### 3. Zbadaj zbieżność punktową i jednostajną ciągu funkcyjnego:

###### a)

$$\begin{gathered}
f_n(x)=\frac{nx}{n^2+x^2} \ na \ \mathbb{R}\\\\
Jednostajna:\\
\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N}: \forall n \gt n_0 \ \ \forall x \in X: \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
f(x)=0\\\\
|\frac{nx}{n^2+x^2}|\lt \epsilon\\
nx\lt \epsilon(n^2+x^2)\\
nx\lt \epsilon n^2+\epsilon x^2\\
\epsilon x^2+\epsilon n^2-nx\gt 0\\
\Delta \lt 0\\
n^2-4\epsilon^2n^2\lt 0\\
n^2(1-4\epsilon^2)\lt 0\\
\frac{1}{2}\lt \epsilon\\
\end{gathered}$$

Zatem nie jest zbieżny jednostajnie.


$$\begin{gathered}
f_n(x)=\frac{nx}{n^2+x^2} \ na \ \mathbb{R}\\\\
Punktowa:\\
\forall \epsilon \gt 0 \ \ \forall x \in X \ \exists n_0 \in \mathbb{N}: \forall n \gt n_0 \: \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
f(x)=0\\\\
|\frac{nx}{n^2+x^2}|\lt \epsilon\\
nx\lt \epsilon(n^2+x^2)\\
nx\lt \epsilon n^2+\epsilon x^2\\
\epsilon x^2+\epsilon n^2-nx\gt 0\\
\Delta \lt 0\\
x^2-4\epsilon^2x^2\lt 0\\
x^2(1-4\epsilon^2)\lt 0\\
\epsilon \gt \frac{1}{2}
\end{gathered}$$

Tak, mamy rozwiązanie że przy ustalonym x i epsilonie znajdziemy n.

###### b)

$$\begin{gathered}
f_n(x)=\frac{1}{1+nx}\ na \ [0,1]\\\\
f=\left\{
\begin{matrix}
1, x=0\\
0, x \in (0,1]
\end{matrix}
\right.\\
d_c(f_n,f)=\sup|f_n(x)-f|=1
\end{gathered}$$
---
##### 5. Zbadaj obszar zbieżności i wyznacz sumę szeregu potęgowego:

###### a)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{3^{n-1}x^{2n}}{(n+1)4^n}}\overset{x^2=t}{=}
\sum^{\infty}_{n=1}{\frac{3^{n-1}t^{n}}{(n+1)4^n}}=
\sum^{\infty}_{n=1}{a_nt^{n}}\\\\

\lambda = \lim_{n\to \infty}{|\frac{a_{n+1}}{a_n}|}=\lim_{n\to \infty}{\frac{3^n}{(n+2)4^{n+1}}\cdot \frac{(n+1)4^{n}}{3^{n-1}}}=\lim_{n\to \infty}{\frac{3}{4}\frac{n+1}{n+2}}=\frac{3}{4}\\\
R=\frac{1}{\lambda}=\frac{4}{3}\\\\
\text{Zbieżny w }(-\frac{4}{3},\frac{4}{3}) \text{ no ale przeciez to kwadrat wiec: }[0,\frac{4}{3})\\
\lim_{t\to \frac{4}{3}}{\sum^{\infty}_{n=1}}{\frac{3^{n-1}}{(n+1)4^n}\cdot (\frac{4}{3})^n}=\frac{1}{3}\lim_{t\to \frac{4}{3}}{\sum^{\infty}_{n=1}{\frac{1}{(n+1)}}}=\frac{1}{3}\lim_{t\to \frac{4}{3}}{\sum^{\infty}_{n=0}{\frac{1}{n}}}\\
\text{nichuja nie zbiezny w tym bo to szereg harmoniczny q=1}\\\\
x\in (0,\frac{2\sqrt{3}}{3})\\\\
suma:\\\\

\end{gathered}$$
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{3^{n-1}t^{n}}{(n+1)4^n}}=\frac{1}{t}\sum^{\infty}_{n=1}{\frac{3^{n-1}t^{n+1}}{(n+1)4^n}}=S\cdot \frac{1}{t}\\\\
S'=\sum^{\infty}_{n=1}{\frac{3^{n-1}}{4^n}t^n}=\frac{1}{3}\sum^{\infty}_{n=1}{(\frac{3}{4}t)^n}=\frac{1}{3}\frac{1}{1-\frac{3}{4}t}\\
|\frac{3}{4}t|\lt 1, \ tak \ bo \ \frac{3}{4}\cdot \frac{2\sqrt{3}}{3}=\frac{2\sqrt{3}}{4}\lt 1\\
\int{S}'=\frac{1}{3}\int{\frac{1}{1-\frac{3}{4}t}}=\begin{vmatrix}
u=1-\frac{3}{4}t\\
du = -\frac{3}{4}dx\\
dx=\frac{4}{3}du
\end{vmatrix}=\frac{4}{9}\int{\frac{1}{u}}=\frac{4}{9}\ln{(1-\frac{3}{4}t)}=S\\\\
\sum^{\infty}_{n=1}{\frac{3^{n-1}t^{n}}{(n+1)4^n}}=\frac{1}{t}(\frac{4}{9})\ln{1-\frac{3}{4}t}
\end{gathered}
$$

---
##### 6. Oblicz sumę szeregu liczbowego:

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}}=
-1\sum^{\infty}_{n=1}{\frac{(-1)^{n}n}{3^n}}\overset{x=1}{=}
-1\sum^{\infty}_{n=1}{\frac{(-1)^{n}n}{3^n}x^{n-1}}=\\
=-1\sum^{\infty}_{n=1}{\frac{(-1)^{n}n}{3^n}x^{n-1}}=S(x)\\\\
\int{S(x) \ dx}=-\int{\sum^{\infty}_{n=1}{\frac{(-1)^{n}n}{3^n}x^{n-1}}\ dx}=
-\sum^{\infty}_{n=1}{\frac{(-1)^{n}}{3^n}x^{n}}=
-\sum^{\infty}_{n=1}{(\frac{-x}{3})^n}(+C)\\\\
\text{na podstawie:}
\sum^{\infty}_{n=1}{aq^{n-1}}=\frac{a}{1-q}, |q|\lt 1\\\\
\int{S(x)}=-\sum^{\infty}_{n=1}{(\frac{-x}{3})^n}=\frac{x}{3}\sum^{\infty}_{n=1}{(\frac{-x}{3})^{n-1}}=\frac{\frac{x}{3}}{1-\frac{-x}{3}}=\frac{x}{3+x}\\\\
\left(\int{S(x)}\right)'=(\frac{x}{3+x})'=\frac{3}{(3+x)^2}\overset{x=1}{=}\frac{3}{16}
\end{gathered}$$

---
##### 7. Rozwiń w szereg Taylora funkcję f(x) w otoczeniu punktu $x_0$

###### a)

$$\begin{gathered}
f(x)=\ln{x}, x_0=1\\
f'(x)=\frac{1}{x}=\frac{1}{1-(1-x)}=\sum^{\infty}_{n=1}{(1-x)^{n-1}}\\\\

f(x)=\int{f'(x)}=\int{\sum^{\infty}_{n=1}{(1-x)^{n-1}}}=\begin{vmatrix}
u=1-x\\
du=-dx\\
\end{vmatrix}=\\\\
=\int{-\sum^{\infty}_{n=1}{u^{n-1}}}=-\sum^{\infty}_{n=1}{\frac{u^n}{n}}=-\sum^{\infty}_{n=1}{\frac{(1-x)^n}{n}}
\end{gathered}$$

###### b)
$$\begin{gathered}
f(x)=\ln{(x^2+3x+2)}, x_0=0\\
x^2+3x+2\gt 0\\
\Delta=9-8=1\\
x_1=\frac{-3+1}{2}=-1, x_2=\frac{-4}{2}=-2\\
x\gt -1\\\\
f'(x)=\frac{2x+3}{x^2+3x+2}\\\\
\frac{A}{x+1}+\frac{B}{x+2}=\frac{2x+3}{x^2+3x+2}\\
A(x+2)+B(x+1)=2x+3\\
\left\{
\begin{matrix}
A+B=2\\
2A+B=3
\end{matrix}
\right.
\left\{
\begin{matrix}
B=2-A\\
2A+2-A=3\implies A=1, B=1
\end{matrix}
\right.\\
f'(x)=\frac{1}{x+1}+\frac{1}{x+2}=\frac{1}{1-(-x)}+\frac{1}{2}\frac{1}{1-(-\frac{x}{2})}=\sum^{\infty}_{n=0}{(-x)^n}+\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{x}{2})^n}\\
\int{f'(x)\ dx}=f(x)=-\sum^{\infty}_{n=0}{\frac{(-x)^{n+1}}{n+1}}-\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{x}{2})}^n

\end{gathered}$$

---
###### c) 

$$\begin{gathered}
f(x)=\frac{1}{(x+2)^2}, x_0=0\\\\
\int{f(x)}=\begin{vmatrix}
u=x+2\\
du=dx
\end{vmatrix}=\int{\frac{1}{u^2}\ du}=-\frac{1}{u}=-\frac{1}{x+2}=-\frac{1}{2}\cdot \frac{1}{1-(-\frac{x}{2})}\\
|-\frac{x}{2}|\lt 1 \implies x \in (-2,2)\\\\
\int{f(x)}=-\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{x}{2})^n}\\
f(x)=\left(-\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{x}{2})^n}\right)'=-\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{1}{2})^n\cdot n\cdot x^{n-1}}=\\
=-\frac{1}{2}\sum^{\infty}_{n=1}{(-\frac{1}{2})^n\cdot n\cdot x^{n-1}}=
-\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{1}{2})^{n+1}\cdot (n+1)\cdot x^{n}}=


\end{gathered}
$$

---
###### d) 

$$\begin{gathered}
f(x)=e^{-x^2}, x_0=0\\\\
\text{Korzystając z :}\ \ \ \ 
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}},x \in \mathbb{R}\\

e^{-x^2}=\sum^{\infty}_{n=0}{\frac{(-x^2)^n}{n!}}=
\sum^{\infty}_{n=0}{\frac{(-1)^n}{n!}x^{2n}}
\end{gathered}$$

---
###### e)

$$\begin{gathered}
f(x)=e^x, x_0=2\\\\

\text{Korzystając z :}\ \ \ \ 
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}},x \in \mathbb{R}\\
\text{oraz : }f(x)=\sum^{\infty}_{n=0}{\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n}\\\\
e^x=\sum^{\infty}_{n=0}{\frac{e^2}{n!}(x-2)^n}
\end{gathered}$$
---

**Co gdyby zrobić podpunkt c względem $x_0=1$?**

$$\begin{gathered}
f(x)=\frac{1}{(x+2)^2}, x_0=1\\\\
\text{Należy tak zrobić żeby z domysłu, dostać }(x-1)^n\text{ w szeregu, zatem zapisać}\\
\text{to co dostaniemy w odpowiedni sposób:}\\\\
\int{f(x)}=\begin{vmatrix}
u=x+2\\
du=dx
\end{vmatrix}=\int{\frac{1}{u^2}\ du}=-\frac{1}{u}=-\frac{1}{x+2}=-\frac{1}{2}\frac{1}{1-(-\frac{x}{2})}\\\\
\text{i tutaj zwracamy uwage że normalnie dostalibyśmy }x^n \text{ z jakimś tam czynnikiem}\\
\text{a chcemy przecież }x-1 \text{ więc możemy po prostu odpowiednio zamienić:}\\\\
\dots=-\frac{1}{2}\frac{1}{\frac{3}{2}-(-\frac{x-1}{2})}=-\frac{1}{3-(-(x-1))}=-\frac{1}{3}\frac{1}{1-(-\frac{x-1}{3})}=\\=-\frac{1}{3}\sum^{\infty}_{n=0}{\left(\frac{-x+1}{3}\right)^n}=-\frac{1}{3}\sum^{\infty}_{n=0}{\left(\frac{-1}{3}\right)^n(x-1)^n}\\\\
\left(\int{f(x)}\right)'=\left(-\frac{1}{3}\sum^{\infty}_{n=0}{\left(\frac{-1}{3}\right)^n(x-1)^n}\right)'=-\frac{1}{3}\sum^{\infty}_{n=0}{\left(\frac{-1}{3}\right)^n\cdot n\cdot (x-1)^n}\\\\
\text{to można tam ładniej zapisać bo dla n=0 nic nie daje itd}\dots
\end{gathered}$$

---
###### f)

$$\begin{gathered}
f(x)=\sin^2{(x)}, x_0=0\\\\
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n+1}}{(2n+1)!}}, x \in \mathbb{R}\\
\text{do zapamiętania z tipem na nieparzystość i parzystość}\\\\
f'(x)=2\sin{x}\cos{x}=\sin{2x}\\\\
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^n(2x)^{2n+1}}{(2n+1)!}}=\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}x^{2n+1}}{(2n+1)!}}\\\\
\int{f'(x)}=\int\left(\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}x^{2n+1}}{(2n+1)!}}\right)=\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}x^{2n+2}}{(2n+2)!}}
\end{gathered}$$

**jest jeszcze drugi sposób z $\sin^2{x}=\frac{1-\cos{2x}}{2}$ i to jest sposób łatwiejszy bo wystarczy podstawić pod gotowy wzór a nie sie męczyć z pochodnymi i całkowaniem**


$$\begin{gathered}
f(x)=\sin^2{(x)}, x_0=0\\\\
\sin^2{x}=\frac{1-\cos{2x}}{2}\\\\
\frac{1-\cos{2x}}{2}=\frac{1}{2}-\frac{\cos{2x}}{2}=\frac{1}{2}-\frac{1}{2}\sum^{\infty}_{n=0}{\frac{(-1)^n(2x)^{2n}}{(2n)!}}=
\frac{1}{2}-\frac{1}{2}\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n}(x)^{2n}}{(2n)!}}=\\\\
=\frac{1}{2}+\sum^{\infty}_{n=0}{\frac{(-1)^{n+1}2^{2n}(x)^{2n}}{2\cdot (2n)!}}
\end{gathered}$$

Można by tu jeszcze te $\frac{1}{2}$ upchnąć do środka szeregu cofając wszędzie n chyba.

---
##### 8) Rozwiń w szereg Fouriera funkcję $$f(x)=\left\{\begin{matrix}0, -\pi\lt x\lt 0\\x, 0\leq x\lt \pi
\end{matrix}\right.$$ Narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ oraz korzystając z otrzymanego rozwinięcia oblicz sumę szeregu liczbowego $1+\frac{1}{3^2}+\frac{1}{5^2}+\dots$


**Sprawdźmy najpierw warunki Dirichleta:**

1) $f: [a,b] \to \mathbb{R}, f - ograniczona$ :LiCheck: 
2) monotoniczna przedzialami :LiCheck:
3) ciągła poza skończoną liczbą punktów w których wartość jest równa średniej arytmetycznej granic jednostronnych :LiCheck: 
4) $f(a)=f(b)=\frac{\lim_{x\to a^+}f(x)+\lim_{x\to b^-}f(x)}{2}$ :LiCross: 

**4 warunek nie prawidłowy więc zamieniamy funkcje na taką która spełnia ten warunek zatem od teraz dla $x=-\pi \ \ \ f(-\pi)=\frac{\pi}{2}=f(\pi)$ 

teraz możemy powiedzieć że: $\forall x\in [-\pi, \pi] \ \ f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}(a_n\cos{nx}+b_n\sin{nx})$

gdzie:
$$\begin{gathered}
a_0=\frac{1}{\pi}{\int^{\pi}_{-\pi}{f(x) }\ dx}\\
a_n=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x)\cos{nx}\ dx}\\
b_n=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x)\sin{nx}\ dx}
\end{gathered}$$

zatem:

$$\begin{gathered}
a_0=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x)}=\frac{1}{\pi}\int^{\pi}_{0}{x\ dx}=\frac{1}{\pi}\frac{x^2}{2}|^{\pi}_0=\frac{1}{\pi}(\frac{\pi^2}{2}-0)=\frac{\pi}{2}
\end{gathered}$$

**tamte punkty na krańcach przedziałów nic nie zmieniają bo to... punkty czyli mają zerową szerokość (zerową miare) i nie zmieniają wartości całki**

$$\begin{gathered}
a_n=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x)\cos{nx}}=\frac{1}{\pi}\int^{\pi}_{0}{x\cos{nx}}=\begin{vmatrix}
u=x&v'=\cos{nx}\\
u'=1&v=\frac{1}{n}\sin{nx}
\end{vmatrix}=\\
=\frac{1}{\pi}(\frac{x\sin{nx}}{n}-\int{\frac{\sin{nx}}{n}})^=(\frac{x\sin{nx}}{n\pi}+\frac{\cos{nx}}{n^2\pi})|^{\pi}_0=\frac{\cos{n\pi}-1}{n^2\pi}
\end{gathered}$$

$$\begin{gathered}
b_n=\frac{1}{\pi}\int^{\pi}_{0}{f(x)\sin{nx}\ dx}=\frac{1}{\pi}\int^{\pi}_{0}{x\sin{nx}\ dx}=\begin{vmatrix}
u=x&dv=\sin{nx}\\
du=1&v=-\frac{1}{n}\cos{nx}
\end{vmatrix}=\\
=\frac{1}{\pi}(-\frac{x\cos{nx}}{n}-\int{-\frac{1}{n}\cos{nx}})
=\frac{1}{\pi}(-\frac{x\cos{nx}}{n}+\frac{\sin{nx}}{n^2})|^{\pi}_0=\frac{- \cos{n\pi}}{n}
\end{gathered}$$

$$\begin{gathered}
f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}{a_n\cos{nx}+b_n\sin{nx}}=
\frac{\pi}{4}+\sum^{\infty}_{n=1}{\frac{\cos{nx}(\cos{n\pi}-1)}{n^2\pi}-\frac{\cos{n\pi\sin{nx}}}{n}}=\\
=\frac{\pi}{4}+\sum^{\infty}_{n=1}{\frac{\cos{nx}((-1)^n-1)}{n^2\pi}-\frac{(-1)^n\sin{nx}}{n}}
\end{gathered}$$



teraz chcemy obliczyć: $1+\frac{1}{3^2}+\frac{1}{5^2}+\dots$

zatem musimy dobrać odpowiednie $x$:

$$\begin{gathered}
1+\frac{1}{3^2}+\frac{1}{5^2}+\dots=\frac{1}{2}\sum^{\infty}_{n=1}{\frac{1}{n^2}((-1)^{n-1}+1)}
\end{gathered}$$

A mając:

$$\begin{gathered}
f(x)=\frac{\pi}{4}+\sum^{\infty}_{n=1}{\frac{\cos{nx}((-1)^n-1)}{n^2\pi}-\frac{(-1)^n\sin{nx}}{n}}=0/x, x\in [-\pi, \pi] (okresowo)\\\\
\pi \cdot f(0)=\frac{\pi^2}{4}+\sum^{\infty}_{n=0}{\frac{(-1)^n-1}{n^2}}=\frac{\pi^2}{4}+(-1)(1+\frac{1}{3^2}+\frac{1}{5^2}\dots)\\
0=\frac{\pi^2}{4}-S\\\\
S=\frac{\pi^2}{4}
\end{gathered}$$

---
##### 9) Rozwiń w szereg Fouriera funkcję $f(x)=x^2$ w $[-\pi,\pi]$, narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ i korzystając z otrzymanego rozwinięcia oblicz sumę szeregu $1+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}\dots$ oraz sumę szeregu $1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}\dots$


**Na oko - spełnia wszystkie warunki dirichleta a w dodatku jest parzysta więc można uprościć liczenie rozwinięcia trygo Furiera**

$$\begin{gathered}
a_0=\frac{2}{\pi}\int^{\pi}_{0}{f(x) \ dx}=\frac{2}{\pi}\int^{\pi}_{0}{x^2\ dx}=\frac{2}{\pi}\frac{x^3}{3}|^{\pi}_0=\frac{2}{\pi}(\frac{\pi^3}{3}-0)=\frac{2\pi^2}{3}
\end{gathered}$$

$$\begin{gathered}
a_n=\frac{2}{\pi}\int^{\pi}_{0}{f(x) \cos{nx} \ dx}=\frac{2}{\pi}\int^{\pi}_{0}{x^2\cos{nx}}=\begin{vmatrix}
u=x^2&v'=\cos{nx}\\
u'=2x&v=\frac{1}{n}\sin{nx}
\end{vmatrix}=\\\\
=\frac{2}{\pi}(\frac{x^2\sin{nx}}{n}-\int{\frac{2x}{n}\sin{nx} \ dx})=\begin{vmatrix}
u=2x&dv=\sin{nx}\\
du=2&v=-\frac{1}{n}\cos{nx}
\end{vmatrix}=\\=
\frac{2}{\pi}(\frac{x^2\sin{nx}}{n}+\frac{2x\cos{nx}}{n^2}+\int{-\frac{2\cos{nx}}{n^2}})=\\=
\frac{2}{\pi}(\frac{x^2\sin{nx}}{n}+\frac{2x\cos{nx}}{n^2}-\frac{2\sin{nx}}{n^3})|^{\pi}_0=\frac{2}{\pi}\cdot \frac{2\pi\cos{n\pi}}{n^2}=\frac{4\cdot (-1)^n}{n^2}
\end{gathered}$$


$$\begin{gathered}
f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}{a_n\cos{nx}}=\frac{\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4(-1)^n}{n^2}\cos{nx}}
\end{gathered}$$

wracając do zadania: oblicz sumę szeregu $1+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}\dots$ 

jeżeli przyjmiemy $x=\pi$ 

$$\begin{gathered}
f(\pi)=\pi^2=\frac{\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4(-1)^n}{n^2}\cdot (-1)^n}=\frac{\pi^2}{3}+4\sum^{\infty}_{n=1}\frac{1}{n^2}\\
S=1+\frac{1}{2^2}+\frac{1}{3^2}\dots = \sum^{\infty}_{n=1}{\frac{1}{n^2}}\\\
\pi^2=\frac{\pi^2}{3}+4S\\
\frac{2\pi^2}{3}=4S\\
\frac{\pi^2}{6}=S
\end{gathered}$$oraz sumę szeregu $1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}\dots$

teraz możemy przyjąć $x=0$

$$\begin{gathered}
f(0)=\frac{\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4(-1)^n}{n^2}\cdot 1}=\frac{\pi^2}{3}-4\sum^{\infty}_{n=1}\frac{(-1)^{n-1}}{n^2}\\\\
\text{gdzie przeciez:}\\
S=1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}\dots=\sum^{\infty}_{n=1}{\frac{(-1)^{n-1}}{n^2}}\\\\
f(0)=0^2=\frac{\pi^2}{3}-4S\\\\
S=\frac{\pi^2}{12}
\end{gathered}$$


---
##### 10) Rozwiń w szereg sinusów funkcję $f(x)=\frac{\pi}{4}$ w $(0,\pi)$, narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ oraz korzystując z otrzymanego rozwinięcia oblicz sumę szeregu liczbowego $1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots$

Skoro w szereg sinusów to należy zamienić to na funkcję nieparzystą i spełniającą warunki dirichleta zatem nasza nowa funkcja to:

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{\pi}{4}, x\in (0,\pi)\\
-\frac{\pi}{4}, x\in (-\pi,0)\\
0,x\in \{-\pi,0,\pi\}
\end{matrix}
\right.\\\\
b_n=\frac{2}{\pi}\int^{\pi}_{0}{\frac{\pi}{4}\sin{nx}\ dx}=\frac{1}{2}\int^{\pi}_{0}{\sin{nx}\ dx}=\begin{vmatrix}
u=nx\\
du=n\ dx\\
du\frac{1}{n}=dx
\end{vmatrix}=\frac{1}{2n}\cdot (-\cos{nx})|^{\pi}_0
=\\
=\frac{1}{2n}(-\cos{n\pi-(-\cos{0})})=\frac{1}{2n}(-\cos{n\pi+1})=\frac{1}{2n}(-(-1)^n+1)\\\\
f(x)=\sum^{\infty}_{n=1}{\frac{1}{2n}(-(-1)^n+1)\sin{nx}}\\\\
S=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots=\sum^{\infty}_{n=1}{\frac{1}{n}\sin{\frac{n\pi}{2}}}\\\\
f(\frac{\pi}{2})=\sum^{\infty}_{n=1}{\frac{1}{2n}(-(-1)^n+1)\sin{\frac{n\pi}{2}}}\\\\
\sin{\frac{n\pi}{2}}: 1,0,-1,0,1,0,-1\dots\\
-(-1)^n+1: 2,0,2,0,2,0,2\dots\\\\
\text{przemnożone daje}\\
2,0,-2,0,2,0,-2\\
\text{a dzieli sie przez 2 i daje}\\
1,0,-1,0,1,0,-1\\
\text{podzielone przez n}\\
\frac{1}{1},0,-\frac{1}{3},\frac{1}{5},-\frac{1}{7}\\\\
\text{wiec to po prostu wychodzi }f(\frac{\pi}{2})=\frac{\pi}{4}
\end{gathered}$$

---
