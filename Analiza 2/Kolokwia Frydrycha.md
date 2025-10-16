
###### 1. Wyznacz obszar zbieżności i sumę szeregu:
$$\begin{gathered}
\sum^{\infty}_{n=0}{\frac{3^n(x+1)^{2n}}{4^n(n+1)}}\\\\
\text{Widze dwa sposoby, pierwszy:}\\\\
\sum^{\infty}_{n=0}{\frac{3^n(x+1)^{2n}}{4^n(n+1)}}=
\sum^{\infty}_{n=0}{\frac{3^n(x^2+2x+1)^{n}}{4^n(n+1)}}=\\=
\sum^{\infty}_{n=0}{\frac{3^n(x^2)^{n}}{4^n(n+1)}}+
\sum^{\infty}_{n=0}{\frac{3^n(2x)^{n}}{4^n(n+1)}}+
\sum^{\infty}_{n=0}{\frac{3^n(1)^{n}}{4^n(n+1)}}:\\\\
\text{Badamy zbieżność każdego z szeregów składowych, i bierzemy część wspólną}\\
\text{Ich wszystkich.}\\\\
\sum^{\infty}_{n=0}{\frac{3^n(x^2)^{n}}{4^n(n+1)}}\overset{u=x^2}{=}\sum^{\infty}_{n=0}{\frac{3^n(u)^{n}}{4^n(n+1)}}\\
\lambda=\lim_{n\to \infty}{\frac{3^n\cdot 3}{4^n\cdot 4(n+2)}\cdot \frac{4^n(n+1)}{3^n}}=\lim_{n\to \infty}{\frac{3(n+1)}{4(n+2)}}=\frac{3}{4}\\
R=\frac{1}{\lambda}=\frac{4}{3}\\\\
\lim_{u\to \frac{4}{3}}{S(x)}=\lim_{n\to \infty}{\sum^{\infty}_{n=0}{\frac{1}{n+1}}}=\infty\\
\lim_{u\to -\frac{4}{3}}{S(x)}=\lim_{n\to \infty}{\sum^{\infty}_{n=0}{\frac{-1}{n+1}}}=-\infty\\
x^2\in (-\frac{4}{3},\frac{4}{3})\\
x\in (0,\frac{2}{\sqrt{3}})
\end{gathered}$$

$$\begin{gathered}
\sum^{\infty}_{n=0}{\frac{3^n\cdot (2x)^n}{4^n(n+1)}}=
\sum^{\infty}_{n=0}{\frac{6^n\cdot x^n}{4^n(n+1)}}=S(x)\\\\
\lambda = \lim_{n\to \infty}{\frac{6\cdot 6^n}{4^n\cdot 4(n+2)}\cdot \frac{4^n(n+1)}{6^n}}=\frac{6}{4}\\\\
R=\frac{4}{6}\\\\
\lim_{x\to \frac{4}{6}^-}{S(x)}=\sum^{\infty}_{n=0}{\frac{1}{n+1}}=\infty\\
\lim_{x\to -\frac{4}{6}^+}{S(x)}=\sum^{\infty}_{n=0}{\frac{-1}{n+1}}=-\infty\\
x\in (-\frac{4}{6},\frac{4}{6})\\\\
\sum^{\infty}_{n=0}{\frac{3^n}{4^n(n+1)}}\\\\
\text{Na podstawie kryterium porównawczego zbieżny.}\\
x\in \mathbb{R}\\\\
\text{Więc dochodząc do konkluzji:}\\
x\in (0,\frac{2}{3})
\end{gathered}
$$

**I suma:**

$$\begin{gathered}
\sum^{\infty}_{n=0}{\frac{3^n(x+1)^{2n}}{4^n(n+1)}}\overset{u=(x+1)^2}{=}
\sum^{\infty}_{n=0}{\frac{3^n(u)^{n}}{4^n(n+1)}}=\frac{1}{u}\sum^{\infty}_{n=0}{\frac{3^n(u)^{n+1}}{4^n(n+1)}}=\frac{1}{u}\cdot S(u)\\\\
S'(u)=\sum^{\infty}_{n=0}{\frac{3^n(u)^{n}}{4^n}}=\frac{1}{1-\frac{3u}{4}}=\frac{4}{4-3u}\\\\
\int{S'(u)\ du}=\int{\frac{4}{4-3u}\ du}=\begin{vmatrix}
p=4-3u\\
dp=-3 \ du\\
\frac{dp}{-3}=du
\end{vmatrix}=-\frac{4}{3}\int{\frac{1}{p}\ dp}=-\frac{4}{3}\ln{|p|}=\\=-\frac{4}{3}\ln{4-3(x+1)^2}=-\frac{4}{3}\ln{1-3x^2-6x}
\end{gathered}$$

###### 2. Zbadaj punktową, bezwzględną i jednostajną zbieżność szeregu na $[0,1]$

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=1}{\frac{x^n(1-x)}{n}}\\\\
Punktowa:\\\\
\lim_{n\to \infty}{|\frac{x^n(x-x^2)}{n+1}\cdot \frac{n}{x^n(1-x)}|}=\lim_{n\to \infty}{|\frac{x-x^2}{1-x}|}=|x|\\\\
dla \ x\gt 1\ \text{Rozbieżny}\\
dla \ x=1 \ mamy \ S(0)=0 - zbieżny\\
dla \ x \lt 1 \ \text{Zbieżny}
\end{gathered}$$

###### 3. Rozwiń w szereg Taylora w otoczeniu $x_0=-1$ funkcję $f(x)=\ln{(3+2x+x^2)}$. Dla jakich $x$ funkcja $f(x)$ jest równa sumie otrzymanego rozwinięcia.

$$\begin{gathered}
f(x)=\ln{(3+2x+x^2)}\\
f'(x)=\frac{2x+2}{3+2x+x^2}=\frac{2x+2}{2+(x+1)^2}=\frac{x+1}{1-(-\frac{(x+1)^2}{2})}=\sum^{\infty}_{n=0}{\frac{(x+1)^{2n+1}}{2^{n}}}\\\\
\int{f'(x)\ dx}=\sum^{\infty}_{n=0}{\frac{(x+1)^{2n+2}}{2^n\cdot (2n+1)}}
\end{gathered}$$