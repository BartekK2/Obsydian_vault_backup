
$$\begin{gathered}
x_1+x_2+x_3+x_4+x_5+x_6 = 42\\
0 \leq x_1 \leq 9\\
0 \leq x_2 \leq 9\\
2 \leq x_3 \leq 11\\
4 \leq x_4 \leq 13\\
3 \leq x_5 \leq 12\\
3 \leq x_6 \leq 12\\
\\
y_1=x_1, \ y_2=x_2, \ y_3=x_3-2, \ y_4=x_4-4, \ y_5=x_5-3, \ y_6=x_6-3\\
x_1+x_2+x_3+x_4+x_5+x_6 = 42\\
y_1+ y_2+(y_3+2)+(y_4+4)+(y_5+3)+(y_6+3)=42\\
y_1+ y_2+y_3+y_4+y_5+y_6=30\\
1.Liczba \ rozwiazan \ bez \ ograniczenia \ gornego:\\
\binom{30+6-1}{6-1}=\binom{35}{5}\\
2.Liczba \ rozwiazan \ z \ jednym \gt 9:\\
z_1=y_1-10\\
(z_1+10)+y_2+y_3+y_4+y_5+y_6=30\\
z_1+y_2+y_3+y_4+y_5+y_6=20\\
6 \cdot \binom{20+6-1}{6-1}=6\cdot\binom{25}{5}\\
3.Liczba \ rozwiazan \ z \ dwoma \gt 9:\\
z_1=y_1-10\\
(z_1+10)+(z_2+10)+y_3+y_4+y_5+y_6=30\\
z_1+z_2+y_3+y_4+y_5+y_6=10\\
\frac{6 \cdot 5}{2} \cdot \binom{10+6-1}{6-1}=15\cdot \binom{15}{5}\\
4.Liczba \ rozwiazan \ z \ trzema \gt 9:\\
z_1=y_1-10\\
(z_1+10)+(z_2+10)+(z_3+10)+y_4+y_5+y_6=30\\
z_1+z_2+z_3+y_4+y_5+y_6=0\\
\frac{6\cdot 5 \cdot 4}{3!}=20 \cdot 1, \ (1 \ rozwiazanie \ bo \ rowne \ 0 \ i \ wieksze \ od 0)\\\\

Liczba \ rozwiazan:\\
1.+2.-3.+4.=

\end{gathered}$$




$$\begin{gathered}
f(x)=\frac{24}{-2x^2-x+1}\\
a_n=A\cdot \alpha^n + B\cdot \beta^n\\
\alpha \lt \beta\\\\
-2x^2-x+1:\\
\Delta=1+8=9\\
x_1=\frac{1+3}{-4}=-1\\
x_2=\frac{1-3}{-4}=\frac{1}{2}\\
f(x)=\frac{12}{-(x+1)(x-\frac{1}{2})}\\
\frac{-12}{(x+1)(x-\frac{1}{2})}=\frac{A}{x+1}+\frac{B}{x-\frac{1}{2}}\\
-12=A(x-\frac{1}{2})+B(x+1)\\
-12=(A+B)x-\frac{1}{2}A+B\\
\left\{
\begin{matrix}
A+B=0\\
-\frac{1}{2}A+B=-12
\end{matrix}
\right.\\\\
\left\{
\begin{matrix}
B=-A\\
-\frac{1}{2}A+B=-12
\end{matrix}
\right.\\
-\frac{1}{2}A-A=-12\\
-\frac{3}{2}A=-12\\
A=\frac{24}{3}=8\\
B=-8\\
f(x)=\frac{8}{x+1}+\frac{-8}{x-\frac{1}{2}}\\
f(x)=\frac{8}{1-(-x)}+\frac{16}{1-2x}\\
\end{gathered}$$

$$\begin{gathered}
\sum^{\infty}_{n=0}{(8)\cdot (-x)^n}+\sum^{\infty}_{n=0}{(16)\cdot (2x)^n}=
\sum^{\infty}_{n=0}{(8)\cdot (-1)^n}x^n+\sum^{\infty}_{n=0}{(16)\cdot (2)^nx^n}=\\\sum^{\infty}_{n=0}{[8\cdot (-1)^n+16\cdot 2^n]}x^n

\end{gathered}$$

---

$$\begin{gathered}
f(x)=\frac{12}{-2x^2-x+1}\\
a_n=A\cdot \alpha^n + B\cdot \beta^n\\
\alpha \lt \beta\\\\
-2x^2-x+1:\\
\Delta=1+8=9\\
x_1=\frac{1+3}{-4}=-1\\
x_2=\frac{1-3}{-4}=\frac{1}{2}\\
f(x)=\frac{-6}{(x+1)(x-\frac{1}{2})}=\frac{A}{x+1}+\frac{B}{x-\frac{1}{2}}\\
-6=A(x-\frac{1}{2})+B(x+1)\\
-6=(A+B)x-\frac{1}{2}A+B\\
\left\{
\begin{matrix}
A+B=0\\
-\frac{1}{2}A+B=-6
\end{matrix}
\right.\\
B=-A\\
-\frac{1}{2}A-A=-6\\
\frac{3}{2}A=6\\
A=4, \ \ B=-4\\
f(x)=\frac{4}{x+1}+\frac{-4}{x-\frac{1}{2}}\\
f(x)=\frac{4}{1-(-x)}+\frac{8}{1-2x}\\
\sum^{\infty}_{n=0}{(4)\cdot (-x)^n}+\sum^{\infty}_{n=0}{(8)\cdot (2x)^n}=
\sum^{\infty}_{n=0}{(4)\cdot (-1)^n}x^n+\sum^{\infty}_{n=0}{(8)\cdot (2)^nx^n}=\\\sum^{\infty}_{n=0}{[4\cdot (-1)^n+8\cdot 2^n]}x^n=a_n
\end{gathered}$$---
$$\begin{gathered}
x_n-9x_{n-1}+8x_{n-2}=-14n-33, \ \ x_0=2, \ x_1=18\\
\\ Jednorodne\\
x^2-9x+8=0\\
\Delta=81-32=49\\
x_1=\frac{9+7}{2}=8, \ \ x_2=1\\\\
Niejednorodne:\\
x_n^{(p)}=An^2+Bn+C\\
An^2+Bn+C-9(A(n-1)^2+B(n-1)+C)+8(A(n-2)^2+B(n-2)+C)=-14n-33\\
n^2(A-9A+8A)+n(B+18A-9B-32A+8B)+C-9A+9B-9C+32A-16B+8C=-14n-33\\
n(-14A)+23A-7B=-14n-33\\
-7B=-56\\
B=8\\
x_n=c_18^n+c_2+n^2+8n\\
x_0=c_1+c_2=2\\
c_2=2-c_1\\
x_1=c_1\cdot 8-c_1=7\\
c_1=1\\
c_2=2-c_1=1
\end{gathered}
$$