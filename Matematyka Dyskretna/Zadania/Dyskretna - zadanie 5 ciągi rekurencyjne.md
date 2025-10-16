### Jednorodne, niejednorodne, ustalanie wzoru.
#### 2024-11-27
##### Lekcja: [[Dyskretna - 5]]

#matematyka_dyskretna  #ciągi_rekurencyjne 

---
###### 1. Na ile obszarów dzieli płaszczyznę n prostych, z których żadne dwie nie są równoległe, ani żadne trzy nie przecinają się w jednym punkcie? Znajdź zależność rekurencyjną.
$$\begin{gathered}
a_0=1, a_1=2\\
a_n=a_{n-1}+n
\end{gathered}$$
###### 2. Ile jest różnych ciągów binarnych długości n, w których nie ma dwóch kolejnych zer? Znajdź zależność rekurencyjną.

$$\begin{gathered}
a_1=2
,\ a_2=3
, \ a_3=5\\
b_n - zakonczone \ 1\\
c_n - zakonczone \ 0\\
a_n=2\cdot b_{n-1} + c_{n-1}\\
b_{n}=a_{n-1}\cdot 1\\
c_{n}=b_{n-1}\cdot 1=a_{n-2}\\
a_n=2\cdot a_{n-2}+a_{n-3}=a_{n-2}+(a_{n-2}+a_{n-3}) \ ciag \ fibbonacciego

\end{gathered}$$
###### 4. Znajdź i uzadadnij zależność rekurencyjną na:
Liczba tych permutacji zbioru $n$-elementowego które w rozkładzie na cykle posiadają $k$ cykli.
$$\begin{gathered}
a) \ Liczba \ Strirlinga \ I \ rodzaju:\\
s(n,k)=s(n-1,k-1)+(n-1)\cdot s(n-1,k), \ \ dla \ \ 0\lt k \lt n\\
s(n,n)=1, \ \ dla \ \ n\geq 0\\
s(n,0)=0, \ \ dla \ \ n\gt 0\\
\end{gathered}$$

- Pierwszy składnik - bierzemy wszystkie rozkłady na $k-1$ cykli $n-1$ elementowej permutacji i tworzymy nowy cykl dla $n$-tego elementu
- Drugi składnik - bierzemy wszystkie rozkłady na $k$ cykli $n-1$ elementowej permutacji i po każdym z $n-1$ elementów możemy dopisać $n$-ty element co nam dalej da cykl.

---
Podział n elementowego zbioriu na k bloków 
$$\begin{gathered}
b) \ Liczba \ Stirlinga \ II \ rodzaju:\\
S(n,k) = S(n-1, k-1) + k\cdot S(n-1,k), \ dla \ \ 0 \lt k \lt n\\
S(n,n)=1, \ dla \ n \geq 0\\
S(n,0)=0, \ dla \ n \gt 0
\end{gathered}$$
- Pierwszy składnik - dzielimy n-1 obiektów na k-1 bloków a ostatni $n$-ty element będzie w osobnym bloku
- Drugi składnik - dzielimy n-1 obiektów na k-1 bloków  a ostatni $n$-ty dorzucamy do któregokolwiek z bloków
---
$$\begin{gathered}
c) \ Liczba \ nieporzadkow:\\
D_n=\sum^{n}_{i=0}{(-1)^i\binom{n}{i}(n-i)!}
\end{gathered}$$
Wzór wynika z zasady włączeń i wyłączeń. Najpierw dodajemy wszystkie permutacje, a potem odejmujemy tą w której jedna pozycja pozostała na swoim miejscu, dodajemy tam gdzie dwie pozostały, odejmujemy gdzie 3 itd.

###### 5. Rozwiąż równania rekurencyjne:

$$\begin{gathered}
a) \ x_n=2x_{n-1}+x_{n-2}-2x_{n-3}, \ \ x_0=0,x_1=2,x_2=0\\
x^3-2x^2-x+2=0\\
(x-2)(x^2-1)=0\\\\
x_1=2, \ x_2=1, \ x_3=-1\\\\
h_n=c_12^n+c_21^n+c_3(-1)^n\\
h_0=c_12^0+c_21^0+c_3(-1)^0=0\\
h_1=c_12^1+c_21^1+c_3(-1)^1=2\\
h_2=c_12^2+c_21^2+c_3(-1)^2=0\\\\
\left\{
\begin{matrix}
c_1+c_2+c_3=0\\
2c_1+c_2-c_3=2\\
4c_1+c_2+c_3=0\\
\end{matrix}
\right.\implies c_1=0
\left\{
\begin{matrix}
c_2-c_3=2\\
c_2+c_3=0\\
\end{matrix}
\right.\implies c_2=1, \ c_3=-1\\\\
h_n=1^n-1\cdot (-1)^n
\end{gathered}$$

$$\begin{gathered}
b) \ x_n=x_{n-1}+x_{n-2}, \ x_0=0, \ x_1=1\\
r^2-r-1=0\\
\Delta=1+4=5\\
r_1=\frac{1-\sqrt{5}}{2}, \ r_2=\frac{1+i\sqrt{5}}{2}\\
x_n=c_1(\frac{1-\sqrt{5}}{2})^n+c_2(\frac{1+\sqrt{5}}{2})^n\\
x_0=c_1+c_2=0\\
c_1=-c_2\\
x_1=c_1(\frac{1-\sqrt{5}}{2})+c_2(\frac{1+\sqrt{5}}{2})=1\\
x_1=c_1(\frac{1-\sqrt{5}}{2})-c_1(\frac{1+\sqrt{5}}{2})=1\\
c_1\cdot -\sqrt{5}=1 \implies c_1=-\frac{1}{\sqrt{5}}\\
x_n=-\frac{1}{\sqrt{5}}(\frac{1-\sqrt{5}}{2})^n+\frac{1}{\sqrt{5}}(\frac{1+\sqrt{5}}{2})^n\\

\end{gathered}$$

$$\begin{gathered}
c) \ x_{n+2} - 5x_{n+1} + 6x_n = 2^n, \ x_0=0, \ x_1=1\\
Jednorodne:\\
x_{n+2} - 5x_{n+1} + 6x_n = 0\\
r^2-5r+6=0\\
\Delta=25-24=1\\
r_1=\frac{5+1}{2}=3, \ \ r_2=\frac{5-1}{2}=2\\
h_n=c_12^n+c_23^n\\

\\\\
Niejednorodne:\\
x_n^{(p)}=C\cdot n\cdot 2^n\\
C\cdot (n+2)\cdot 2^{n+2}-5\cdot C\cdot (n+1)\cdot 2^{n+1}+6C\cdot n\cdot 2^n=2^n\\
C\cdot (n+2)\cdot4\cdot  2^n-5\cdot C\cdot (n+1)\cdot 2\cdot  2^n+6C\cdot n\cdot 2^n=2^n\\
C\cdot 2^n ((n+2)\cdot4-5\cdot (n+1)\cdot 2+6 n)=2^n\\
C\cdot 2^n \cdot -2=2^n\\
C \cdot -2=1\\
C=-\frac{1}{2}\\
x_n^{(p)}=-\frac{1}{2}\cdot n\cdot 2^n\\
x_n=x_n^{(h)}+x_n^{(p)}\\
x_n=c_12^n+c_23^n-\frac{1}{2}\cdot n\cdot 2^n\\\\\\
h_0=c_12^0+c_23^0=c_1+c_2=0\\
h_1=c_12^1+c_23^1-1=1\\
\left\{
\begin{matrix}
c_1+c_2=0\\
2c_1+3c_2=2
\end{matrix}
\right.\implies c_2=-c_1 \implies 2c_1-3c_1=-c_1=2 \implies c_1=-2 \land c_2 = 2\\
x_n=-2\cdot 2^n+2\cdot 3^n-\frac{1}{2}\cdot n\cdot 2^n\\

\end{gathered}$$
---
$$\begin{gathered}
d) \ x_{n+2}-5x_{n+1}+6x_n=5^n+n,\ \ x_0=0, \ x_1=1\\
Jednorodne:\\
x^2-5x+6=0\\
\Delta=25-24=1\\
x_1=\frac{5+1}{2}=3, \ \ x_2=\frac{5-1}{2}=2\\
x_n=A\cdot 3^n+B\cdot 2^n\\\\
Niejednorodne:\\
x_n^{(p)}=5^n+n\\\\
x_n^{(p_1)}=a\cdot 5^n\\
a\cdot 5^{n+2}-a\cdot 5\cdot 5^{n+1}+a\cdot 6\cdot 5^n=5^n\\
25A-25A+6A=1\\
a=\frac{1}{6}\\\\
x_n^{(p_2)}=b\cdot n+c\\
b\cdot (n+2)+c-5\cdot (b\cdot (n+1)+c)+6\cdot (b\cdot n+c)=n+0\\
n(b-5b+6b)+2b+c-5b-5c+6c=n+0\\
6b+b-5b=7b-5b=2b=1\\
b=\frac{1}{2}\\
-3b+2c=0\\
2c-\frac{3}{2}=0\\
c=\frac{3}{4}\\
x_n=A\cdot 3^n+B\cdot 2^n+\frac{1}{6}\cdot 5^n+\frac{1}{2}n+\frac{3}{4}\\
x_0=A+B+\frac{1}{6}+\frac{3}{4}=0\\
x_1=A\cdot 3+B\cdot 2+\frac{1}{6}\cdot 5+\frac{1}{2}+\frac{3}{4}=3A+2B+\frac{8}{6}+\frac{3}{4}=1\\
\left\{
\begin{matrix}
A+B+\frac{22}{24}=0\\
3A+2B+\frac{50}{24}=1
\end{matrix}
\right.
\left\{
\begin{matrix}
B=-A-\frac{22}{24}\\
3A+-2A-\frac{44}{24}+\frac{50}{24}=1
\end{matrix}
\right.
\left\{
\begin{matrix}
B=-A-\frac{22}{24}\\
A+\frac{6}{24}=1
\end{matrix}
\right.
\left\{
\begin{matrix}
B=-\frac{40}{24}=-\frac{20}{12}\\
A=\frac{18}{24}=\frac{9}{12}
\end{matrix}
\right.\\\\
x_n=\frac{9}{12}\cdot 3^n-\frac{20}{12}\cdot 2^n+\frac{1}{6}5^n+\frac{1}{2}n+\frac{3}{4}\\\\
\end{gathered}$$---
$$\begin{gathered}
x_{n+1} = x_n + n^3, \ \  x_0 = 1\\
x_{n+1}-x_n=n^3\\
x-1=0\\
x=1\\
x_n^{(nj)}=c_1\cdot 1^n\\
x_n^{(p)}=A\cdot n^3+B\cdot n^2+Dn+E\\

A\cdot (n+1)^3+B\cdot (n+1)^2+D(n+1)+E-A\cdot n^3+B\cdot n^2+Dn+En=n^3\\
n^3(A-A)=0\neq 1\cdot n^3\\\\
x_n^{(p)}=A\cdot n^4+B\cdot n^3+Cn^2+Dn+E\\
A\cdot (n+1)^4+B\cdot (n+1)^3+C(n+1)^2+D(n+1)+E-(A\cdot n^4+B\cdot n^3+Cn^2+Dn+E)=n^3\\
A\cdot (n^4+4n^3+6n^2+4n+1)+B(n^3+3n^2+3n+1)+C(n^2+2n+1)+\\+Dn+D+E-An^4-Bn^3-Cn^2-Dn-E=n^3\\
n^4(A-A)+n^3(4A+B-B)+n^2(6A+3B+C-C)+\\+n(4A+3B+2C+D-D)+A+B+C+D+E-E=n^3\\
n^3(4A)+n^2(6A+3B)+n(4A+3B+2C)+A+B+C+D=n^3\\
\left\{
\begin{matrix}
4A=1\\
6A+3B=0\\
4A+3B+2C=0\\
A+B+C+D=0\\
\end{matrix}
\right.
\left\{
\begin{matrix}
A=\frac{1}{4}\\
B=-\frac{2}{4}\\
C=\frac{1}{4}\\
D=0\\
\end{matrix}
\right.\\
x_n=c_1\cdot 1^n+\frac{1}{4}\cdot n^4-\frac{2}{4}n^3+\frac{1}{4}n^2+0\\
x_0=c_1\cdot 1=1\\
c_1=1\\
x_n=1\cdot 1^n+\frac{1}{4}\cdot n^4-\frac{2}{4}n^3+\frac{1}{4}n^2\\

\end{gathered}$$