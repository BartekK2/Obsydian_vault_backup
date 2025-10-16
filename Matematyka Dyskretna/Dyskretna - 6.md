### Funkcja tworząca
#### 2024-12-05
##### Poprzednia: [[Dyskretna - 5]]
##### Nastepna: [[Dyskretna - 7]]
##### Zadania: 

#matematyka_dyskretna  #ciągi_rekurencyjne #funkcje_tworzące #postać_jawna

--- 
*Definicja:*
Nieskończonemu ciągowi $a_0, a_1, a_2,\dots$ może zostać przypisany szereg formalny:
$$\begin{gathered}
A(x)=\sum^{\infty}_{i=0}{a_ix^i}
\end{gathered}$$
Wówczas $A(x)$ oznacza *funkcje tworzącą (zwyczajną)* dla tego ciągu.

Jeśli $a_k=0$ dla każdego $k\gt n$, to wtedy szereg utożsamiamy z wielomianem $a_nx^n+a_{n-1}x^{n-1}+\dots+a_0$.

*Lemat:*
Każdy ciąg $a_0, a_1,a_2,\dots$ wyznacza jednoznacznie funkcje tworzącą $A(x)$. Każda funkcja $A(x)$ określa jednoznacznie $a_0, a_1, a_2,\dots$

*Definicja:* 
Funkcją tworzącą eksponencjalną nieskończonego ciągu $a_0, a_1, a_2, \dots$ jest szereg formalny.
$$\begin{gathered}
B(x)=\sum^{\infty}_{i=0}{a_i \frac{x^i}{i!}}
\end{gathered}$$
*Lemat:*
Każdy ciąg $a_0, a_1, a_2,\dots$ wyznacza jednoznacznie funkcje tworzącą eksponencjalną $B(x)$. Każda funkcja $B(x)$ określa jednoznacznie ciąg $a_0, a_1, a_2, \dots$

Niech $h_0, h_1,\dots, h_n, \dots$ będzie nieskończonym ciągiem liczb spełniającym homogeniczne równanie rekurencyjne liniowe stopnia $k$ o stałych współczynnikach.

$h_n-a_1h_{n-1}-a_2h_{n-2}-\dots-a_kh_{n-k}=0, (a_k\neq 0, n \geq k)$

Wówczas funkcja tworząca dla tego równania ma postać $H(x)=\frac{P(x)}{Q(x)}$, gdzie $Q(x)$ jest wielomianem stopnia $k$ o niezerowym współczynniku stałym, natomiast $P(x)$ jest wielomianem stopnia mniejszego niż $k$.

Temat dosyć mało zrozumiały z samych definicji także przykłady w praktyce:

---
$$\begin{gathered}
a_n=7a_{n-1}, a_0=1\\\\
f(x)=\sum^{\infty}_{n=0}{a_nx^n}=a_0x^0+\sum^{\infty}_{n=1}{a_nx^n}=1+\sum^{\infty}_{n=1}{7a_{n-1}x^n}=1+7\cdot \sum^{\infty}_{n=1}{a_{n-1}x^{n-1}}\cdot x=\\
=1+7\cdot \sum^{\infty}_{n=0}{a_{n}x^{n}}\cdot x=1+7x\cdot f(x)\\\\
f(x)=1+7x\cdot f(x)\\
f(x)(1-7x)=1\\
f(x)=\frac{1}{1-7x}\\\\
Gdzie \ z \ sumy \ ciagu \ geometrycznego: S=\frac{1}{1-|q|}\\
f(x)=\sum^{\infty}_{n=0}{(7x)^n}
\\
Co \ implikuje \ ze \ a_n=7^n

\end{gathered}$$

---
$$\begin{gathered}
a_n=a_{n-1}+3^{n-1}, a_0=1\\
f(x)=\sum^{\infty}_{n=0}{a_nx^n}=1+\sum^{\infty}_{n=1}{a_nx^n}=1+\sum^{\infty}_{n=1}{(a_{n-1}+3^{n-1})x^n}=1+\sum^{\infty}_{n=1}{a_{n-1}x^n}+\sum^{\infty}_{n=1}{3^{n-1}x^n}\\=1+x\sum^{\infty}_{n=1}{a_{n-1}x^{n-1}}+x\sum^{\infty}_{n=1}{3^{n-1}x^{n-1}}=
1+x\sum^{\infty}_{n=0}{a_nx^n}+x\sum^{\infty}_{n=0}{(3x)^n}=\\
=1+xf(x)+\frac{x}{1-3x}\\\\
f(x)=1+xf(x)+\frac{x}{1-3x}\\
f(x)(1-x)=1+\frac{x}{1-3x}\\
f(x)=\frac{1-2x}{(1-3x)(1-x)}\\\\
\frac{A}{1-3x}+\frac{B}{1-x}=\frac{1-2x}{(1-3x)(1-x)}\\
A(1-x)+B(1-3x)=1-2x\\
A+B-Ax-3Bx=1-2x\\\\
\left\{
\begin{matrix}
A+B=1\\
-A-3B=-2
\end{matrix}
\right.
\left\{
\begin{matrix}
B=1-A\\
-A-3(1-A)=2A-3=-2
\end{matrix}
\right.\implies A=\frac{1}{2}=B\\\\
f(x)=\frac{\frac{1}{2}}{1-3x}+\frac{\frac{1}{2}}{1-x}\\
a_n=\frac{1}{2}\cdot 3^n + \frac{1}{2}\cdot 1^n

\end{gathered}$$---
$$\begin{gathered}
a_n=a_{n-1}+6a_{n-2}, a_0=3, a_1=6\\
f(x)=\sum^{\infty}_{n=0}{a_nx^n}=3+6x+\sum^{\infty}_{n=2}{a_nx^n}=3+6x+\sum^{\infty}_{n=2}{(a_{n-1}+6a_{n-2})x^n}=\\
=3+6x+\sum^{\infty}_{n=2}{a_{n-1}x^n}+\sum^{\infty}_{n=2}{6a_{n-2}x^n}=3+6x+x\sum^{\infty}_{n=2}{a_{n-1}x^{n-1}}+x^2\cdot 6\cdot \sum^{\infty}_{n=2}{a_{n-2}x^{n-2}}=\\
=3+6x+x\sum^{\infty}_{n=1}{a_nx^n}+6x^2\sum^{\infty}_{n=0}{a_nx^n}=
3+6x+x(f(x)-a_0x^0)+6x^2\cdot f(x)=\\
=3+6x+x(f(x)-3)+6x^2\cdot f(x)\\\\
f(x)=3+6x+x\cdot f(x)-3x+6x^2\cdot f(x)\\
f(x)(1-6x^2-x)=3+3x\\
f(x)=\frac{3+3x}{-6x^2-x+1}\\
\Delta=1+24=25\\
x_1=\frac{1+5}{-12}=-\frac{1}{2}\\
x_1=\frac{1-5}{-12}=\frac{1}{3}\\\\
f(x)=\frac{3+3x}{(x+\frac{1}{2})(x-\frac{1}{3})}\\
\frac{A}{x-\frac{1}{3}}+\frac{B}{x+\frac{1}{2}}=\frac{3+3x}{(x+\frac{1}{2})(x-\frac{1}{3})}\\
A(x+\frac{1}{2})+B(x-\frac{1}{3})=3+3x\\
(A+B)x+\frac{A}{2}-\frac{B}{3}=3+3x\\
\left\{
\begin{matrix}
A+B=3\\
3A-2B=18
\end{matrix}
\right.
\left\{
\begin{matrix}
B=3-A\\
5A-6=18
\end{matrix}
\right. \
A=\frac{24}{5}, \ B=-\frac{17}{5}
\end{gathered}$$
itd.. nie wiem błąd w obliczeniach gdzieś

---
