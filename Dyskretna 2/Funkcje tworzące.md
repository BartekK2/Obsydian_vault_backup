
### Zadania fortunki


###### a)
$$\begin{gathered}
f(x)=\frac{x}{1-x}\\\\
f(x)=x\sum^{\infty}_{n=0}{x^n}=0+\sum^{\infty}_{n=1}{x^n}\\\\
\text{Zatem ciąg to:}\\
(0,1,1,1,\dots)
\end{gathered}$$

###### b)
$$\begin{gathered}
f(x)=\frac{1}{x^2-4x+4}=\\
=\frac{1}{(x-2)^2}=\frac{1}{(2-x)^2}=\frac{1}{4}\cdot \frac{1}{(1-\frac{x}{2})^2}=\dots\\\\\
\int\frac{1}{(1-u)^2}du=\begin{vmatrix}
t=1-u\\
dt=-du
\end{vmatrix}=-\int t^{-2}dt=\\
=-\frac{t^{-1}}{-1}=t^{-1}=\frac{1}{1-u}=\sum^{\infty}_{n=0}u^n\Leftrightarrow \frac{1}{(1-u^2)}=\sum^{\infty}_{n=1}{nu^{n-1}}\\\\
\dots=\frac{1}{4}\cdot \sum^{\infty}_{n=1}{\frac{n}{2^{n-1}}x^{n-1}}=
\frac{1}{4}\cdot \sum^{\infty}_{n=0}{\frac{(n+1)}{2^{n}}x^{n}}\\\\
x_n=\frac{1}{4}(n+1)\cdot \frac{1}{2^n}

\end{gathered}$$


###### c)

$$\begin{gathered}
f(x)=\frac{1}{x^2-4x+13}\\\\
\Delta=16-52=-36\\
x_1=2-3i,x_2=2+3i\\\\
\frac{1}{x^2-4x+13}=\frac{A}{x-(2-3i)}+\frac{B}{x-(2+3i)}\\
1=A[x-(2+3i)]+B[x-(2-3i)]\\
A+B=0\implies A=-B \ \ \ \ (x)\\
-A(2+3i)+A(2-3i)=1\\
A=-\frac{1}{6i}\\
B=\frac{1}{6i}\\\\
x_n=\frac{1}{12i+18}\sum^{\infty}_{n=0}\frac{1}{(2-3i)}^nx^n-\dots
\end{gathered}$$


Jeżeli funkcja tworzącą ciągu spełniającego równania $a_n=4a_{n-1}+2a_{n-2},a_0=2,a_1=2$

jest funkcja $f(x)=\frac{Ax+B}{Cx^2+Dx+1}$
to:

$$\begin{gathered}
a^2-4a+2=0\\
\Delta=16-8=8\\
a_1=\frac{4-2\sqrt{2}}{2}=2-\sqrt{2},
a_2=\frac{4+2\sqrt{2}}{2}=2+\sqrt{2}\\
a_n=A(2-\sqrt{2})^n+B(2+\sqrt{2})^n\\
a_0=2=A+B\implies B=2-A\\
a_1=2=2A+2B+\sqrt{2}(B-A)\\\\
a_1=2=4+\sqrt{2}(2-2A)\\\\
1+\sqrt{2}=A\\
B=1-\sqrt{2}\\\\\
a_n=(1+\sqrt{2})(2-\sqrt{2})^n+(1-\sqrt{2})(2+\sqrt{2})^n\\\\
f(x)=\sum^{\infty}_{n=0}(1+\sqrt{2})(2-\sqrt{2})^nx^n+\sum^{\infty}_{n=0}(1-\sqrt{2})(2+\sqrt{2})^nx^n=\\\\\
=\frac{1+\sqrt{2}}{1-x(2-\sqrt{2})}+\frac{1-\sqrt{2}}{1-x(2+\sqrt{2})}=\dots\\\\\
\frac{1+\sqrt{2}}{1-x(2-\sqrt{2})}+\frac{1-\sqrt{2}}{1-x(2+\sqrt{2})} = \mathbf{\frac{2 - 8x}{1 - 4x + 2x^2}}
\end{gathered}$$

$$$$