

rozwinięcie $e^x$ ale w $x_0=2$

$$\begin{gathered}
f(x)=e^x=e^{x-2+2}=e^2\cdot \sum^{\infty}_{n=0}{\frac{(x-2)^n}{n!}}=\\=\sum^{\infty}_{n=0}{\frac{e^2}{n!}\cdot (x-2)^n}
\end{gathered}$$


8.B

$$\begin{gathered}
f(x)=\ln{(x^2+3x+2)}\\
x^2+3x+2\gt 0\\
\Delta=1\\
x_1=-1, x_2=-2\\
x\in (-\infty,-2)\cup (-1,\infty)\\\\
f'(x)=\frac{2x+3}{x^2+3x+2}\\
\frac{A}{x+1}+\frac{B}{x+2}=\frac{2x+3}{x^2+3x+2}\\
A=1, B=1\\
f'(x)=\frac{1}{x+1}+\frac{1}{x+2}=\frac{1}{1-(-x)}+\frac{1}{2}\cdot \frac{1}{1-(-\frac{x}{2})}=\\
=\sum^{\infty}_{n=0}{(-x)^n}+\sum^{\infty}_{n=0}{(-\frac{x}{2})^n}=\sum^{\infty}_{n=0}{(-1)^nx^n}+\sum^{\infty}_{n=0}{\frac{1}{2}(-\frac{1}{2})^nx^n}\\\\
q_1=-x, |-x|\gt 1, x \in (-1,1)\\
q_2=-\frac{x}{2}, |-\frac{x}{2}|\gt 1, x\in (-2,2)\\\\\
f'(x)=\sum^{\infty}_{n=0}{((-1)^n+\frac{1}{2}\cdot (-\frac{1}{2})^n)x^n}\\\\
g(x)=\int{f'(x)}=\sum^{\infty}_{n=0}{\frac{x^{n+1}}{n+1}((-1)^n+\frac{1}{2}\cdot (-\frac{1}{2})^n)+C}=\\=\sum^{\infty}_{n=1}{\frac{x^{n}}{n}((-1)^{n-1}+\frac{1}{2}\cdot (-\frac{1}{2})^{n-1})+C}\\\\
f(0)=\ln(2)\\
g(0)=\sum^{\infty}_{n=1}{\frac{0^{n}}{n}((-1)^{n-1}+\frac{1}{2}\cdot (-\frac{1}{2})^{n-1})+C}=C=\ln{2}\\\\
\ln{x^2+3x+2}=\sum^{\infty}_{n=1}{\frac{0^{n}}{n}((-1)^{n-1}+\frac{1}{2}\cdot (-\frac{1}{2})^{n-1})+\ln{2}}
\end{gathered}$$


dla $x=1$
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{1^{n}}{n}((-1)^{n-1}+\frac{1}{2}\cdot (-\frac{1}{2})^{n-1})}\\\\
\text{Czy to zbieżne?}\\\\
\text{Z szeregu naprzemiennego:}\\
\sum^{\infty}_{n=1}{\frac{((-1)^{n-1}+\frac{1}{2}\cdot (-\frac{1}{2})^{n-1})}{n}}=\sum^{\infty}_{n=1}{\frac{(-1)^{n-1}(1+(\frac{1}{2})^{n})}{n}}=\\=-
\sum^{\infty}_{n=1}{\frac{(-1)^{n}(1+(\frac{1}{2})^{n})}{n}}\\\\
a_n=\frac{(1+(\frac{1}{2})^{n})}{n}\\\\
\forall n\geq 1 \ \ a_n\gt 0\\\\
\lim_{n\to \infty}{a_n}=0\\\\
a_n\downarrow
\end{gathered}$$

Skoro wiemy że jest zbieżny można z tw. Abela sprawdzić czy ma tam granice, a ma bo jest ciągła więc też w $x=1$ wzór jest poprawny. Dla $x=-1$ nie ma co sprawdzać bo wtedy logarytm nie istnieje.


---
7.c

$$\begin{gathered}
f(x)=\frac{1}{(x+2)^2}\\\\
\int{f(x)}=\int{\frac{1}{(x+2)^2}\ dx}=\begin{vmatrix}
u=x+2\\
du=dx
\end{vmatrix}=\int{\frac{1}{u^2}\ du}=-\frac{1}{u}=-\frac{1}{x+2}+C=\\=-\frac{1}{2}\cdot \frac{1}{1-(-\frac{x}{2})}+C\\\\
|-\frac{x}{2}|\gt 1\\
x\in (-2,2)
\\\\
\sum^{\infty}_{n=0}{-\frac{1}{2}\cdot (-\frac{x}{2})^n}=
\sum^{\infty}_{n=0}{(-\frac{1}{2})^{n+1}x^n}=
f(x)=\left[\sum^{\infty}_{n=0}{(-\frac{1}{2})^{n+1}x^n}\right]'=\sum^{\infty}_{n=0}{(-\frac{1}{2})^{n+1}nx^{n-1}}=\\
=\sum^{\infty}_{n=1}{(-\frac{1}{2})^{n+1}nx^{n-1}}=\sum^{\infty}_{n=0}{(-\frac{1}{2})^{n+2}(n-1)x^{n}}, x\in (-2,2)\\\\
\text{Zamienilismy tak by nie miec }x^{-1} \text{ w sumie.}\\\\
\text{Z tw Abela:}\\\\
\dots\end{gathered}$$

8f
$$\begin{gathered}
f(x)=\sin^2{x}\\
f'(x)=2\sin{x}\cos{x}=\sin{2x}\\
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n+1}}{(2n+1)!}}\\\\
\sin{2x}=\sum^{\infty}_{n=0}{\frac{(-1)^n(2x)^{2n+1}}{(2n+1)!}}=\sum^{\infty}_{n=0}{\frac{(-1)^n\cdot 4^n\cdot 2\cdot x^{2n+1}}{(2n+1)!}}\\\\
f(x)=\int{f'(x)\ dx}=\sum^{\infty}_{n=0}{\frac{(-1)^n\cdot 4^n\cdot 2\cdot x^{2n+2}}{(2n+2)!}}+C\\\\
f(0)=0=C
\end{gathered}$$