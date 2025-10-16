

pokaż że zbieżny i oblicz sume

$$\begin{gathered}
\text{Na podstawie kryterium Cauchy'ego}\\
g=\lim_{n\to \infty}\sqrt{\frac{3^n+4^n}{5^n}}=\frac{4}{5}\lt 1 - zbieżny
\end{gathered}
$$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{3^n+4^n}{5^n}}=
\sum^{\infty}_{n=1}{(\frac{3}{5})^n}+\sum^{\infty}_{n=1}{(\frac{4}{5})^n}=
\frac{\frac{3}{4}}{1-\frac{3}{4}}+\frac{\frac{4}{5}}{1-\frac{4}{5}}=3+4=7
\end{gathered}$$

---
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}\\
\text{Na podstawie kryterium porównawczego granic ilorazowych:}\\
\sum^{\infty}_{n=1}{a_n}=\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}\\
\sum^{\infty}_{n=1}{b_n}=\sum^{\infty}_{n=1}{\frac{1}{n^2}}\\\\
\lim_{n\to \infty}{\frac{\frac{1}{9n^2-3n-2}}{\frac{1}{n^2}}}=\frac{1}{9} \in (0, +\infty)\\\\\
Gdzie \sum^{\infty}_{n=1}{\frac{1}{n^2}} \ zbiezny \ na \ podstawie \ tw \ o \ zbieznosci \ szeregow \ harmonicznych\\\\

\end{gathered}$$


$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}\\\\
\frac{A}{3n-2}+\frac{B}{3n+1}=\frac{1}{(3n-2)(3n+1)}\\
A(3n+1)+B(3n-2)=1\\
A=-B\\
-3B=1\\
B=-\frac{1}{3}\\
A=\frac{1}{3}\\
\frac{1}{3}\sum^{\infty}_{n=1}{\frac{1}{(3n-2)}-\frac{1}{(3n+1)}}=\frac{1}{3}(1-\frac{1}{4}+\frac{1}{4}-\frac{1}{7}+\frac{1}{7}\dots)=\frac{1}{3}
\end{gathered}$$


---
$$\begin{gathered}
f_n(x)=\frac{\sin{nx}}{n}\\\\
f=0\\\\\
\forall \epsilon \gt 0\ \ \exists n_0\in \mathbb{N} \ \ \forall n\geq n_0 \ \ \forall x\in X \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
\frac{\sin{nx}}{n}\lt \epsilon\\
\sin{nx}\lt \epsilon n\\
\text{Napewno spełnione dla }n_0=\frac{1}{\epsilon}\text{ i dla większych.}
\end{gathered}$$

---
$$\begin{gathered}
f_n(x)=\frac{nx}{n^2+x^2}, x\in \mathbb{R}\\\\
\frac{nx}{n^2+x^2}\lt \epsilon , \forall \epsilon \gt 0, \ \ \forall x \in X\\\\
nx\lt \epsilon (n^2+x^2)\\
\epsilon x^2-nx+\epsilon n^2\gt 0\\
q=\frac{-\Delta}{4a}\gt 0\\
-\Delta\gt 0\\
\Delta\lt 0\\
n^2-4\epsilon^2n^2\lt 0\\
n^2(1-4\epsilon^2)\lt 0\\
\frac{1}{4}\lt \epsilon^2\\
\epsilon\gt \frac{1}{2}\\\\
\text{Czyli dla }\epsilon \leq \frac{1}{2} \text{ sie nie da więc nie jest zbieżny jednostajnie.}
\end{gathered}$$

$$\begin{gathered}
f_n(x)=\frac{nx}{n^2+x^2}\\\\
\forall x \in X \ \ \forall \epsilon \gt 0 \ \ \exists n_0 : \forall n \gt n_0 \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
|\frac{nx}{n^2+x^2}|\lt \epsilon \\\\\text{ możemy rozpatrzyć tylko dodatnie x bo dla ujemnych działamy tak samo}\\\\
\frac{nx}{n^2+x^2}\lt \epsilon\\\\
nx\lt \epsilon(n^2+x^2)\\
nx\lt \epsilon n^2+\epsilon x^2\\
\epsilon x^2+\epsilon n^2-nx\gt 0\\
\Delta\lt 0\\
x^2-4\epsilon^2x^2\lt 0\\
x^2(1-4\epsilon^2)\lt 0\\
\frac{1}{4}\lt \epsilon^2\\
\frac{1}{2}\lt \epsilon
\end{gathered}$$

---
$$\begin{gathered}
f_n(x)=\frac{x}{1+n^2x^2}\\\\
\text{Zbadaj zbieżność jednostajną}\\\\
\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N} : \forall n\gt n_0  \ \ \forall x \in X  \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
f(x)=0\\\\
|\frac{x}{1+n^2x^2}|\lt \epsilon\\\\
\frac{x}{1+n^2x^2}\lt \epsilon\\
x\lt \epsilon+n^2\epsilon x^2\\
n^2\epsilon x^2-x+\epsilon\gt 0\\
\Delta \lt 0\\
1-4(ne)^2\lt 0\\
\frac{1}{4}\lt (ne)^2\\
\frac{1}{2}\lt ne\\
\frac{1}{2e}\lt n\\\\
\text{Tak, począwszy od pierwszej liczby naturalnej większej od }\frac{1}{2e}
\end{gathered}$$


---
$$\begin{gathered}
f_n(x)=\frac{nx}{1+n^2x^2}\\\\
f(x)=0\\\\
\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N}: \forall n \gt n_0  \ \ \forall x\in X \ \ |f_n(x)-f(x)| \lt \epsilon\\\\
\frac{nx}{1+n^2x^2}\lt \epsilon\\
nx\lt \epsilon+\epsilon n^2 x^2\\
\epsilon n^2x^2-nx+\epsilon\gt 0\\
\Delta \lt 0\\
n^2-4\epsilon^2n^2\lt 0\\
n^2(1-4\epsilon^2)\lt 0\\
\frac{1}{4}\lt \epsilon^2\\
\epsilon\gt \frac{1}{2}\\\\
\end{gathered}$$

---
$$\begin{gathered}
f_n(x)=\frac{1}{1+n^2x^2}\\\\
\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N} \ \ \forall n \gt n_0 \ \ \forall x \in X \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
f(x)=0\\\\
\frac{1}{1+n^2x^2}\lt \epsilon\\
1\lt \epsilon+n^2\epsilon x^2\\
\epsilon n^2x^2+\epsilon-1\gt 0\\
\Delta \lt 0\\
-4(\epsilon-1)\epsilon n^2\lt 0\\
(\epsilon -1)\epsilon n^2 \gt 0\\
\epsilon-1\gt 0\\
\epsilon \gt 1
\end{gathered}$$


---
### Gorzkowska

###### 1. Oblicz sumę podanego szeregu:

a)
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{2^n+3^n}{6^n}}=
\sum^{\infty}_{n=1}{(\frac{2}{6})^n}+\sum^{\infty}_{n=1}{(\frac{3}{6})^n}=\frac{\frac{2}{6}}{1-\frac{2}{6}}+\frac{\frac{3}{6}}{1-\frac{3}{6}}=\frac{2}{6}\cdot \frac{6}{4}+\frac{3}{6}\cdot \frac{6}{3}=\frac{3}{2}
\end{gathered}$$


b)
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{1}{n(n+2)}}=(1):\\\\
(1):
\frac{1}{n(n+2)}=\frac{A}{n}+\frac{B}{n+2}\\
1=A(n+2)+Bn\\
\left\{
\begin{matrix}
A+B=0\\
2A=1
\end{matrix}
\right.\
\left\{
\begin{matrix}
-\frac{1}{2}=B\\
A=\frac{1}{2}
\end{matrix}
\right.\\\\\
(1)=\frac{1}{2}\sum^{\infty}_{n=1}{\frac{1}{n}-\frac{1}{n+2}}=\frac{1}{2}(1-\frac{1}{3}+\frac{1}{2}-\frac{1}{4}+\frac{1}{3}-\frac{1}{5}+\frac{1}{4}-\frac{1}{6}+\frac{1}{5}-\frac{1}{7}\dots)=\\=\frac{1}{2}(\frac{3}{2})=\frac{3}{4}
\end{gathered}$$
c)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{2n+1}{n^2(n+1)^2}}\\\\
\frac{2n+1}{n^2(n+1)^2}=\frac{A}{n}+\frac{B}{n^2}+\frac{C}{n+1}+\frac{D}{(n+1)^2}\\
2n+1=An(n+1)^2+B(n+1)^2+Cn(n+1)+Dn^2\\
2n+1=A(n^3+2n^2+n)+B(n^2+2n+1)+C(n^2+n)+Dn^2\\

\left\{
\begin{matrix}
A=0\\
B+C+D=0\\
2B+C=2\\
B=1
\end{matrix}
\right.
\left\{
\begin{matrix}
A=0\\
D=-1\\
C=0\\
B=1
\end{matrix}
\right.\\\\
\sum^{\infty}_{n=1}{\frac{2n+1}{n^2(n+1)^2}}=\sum^{\infty}_{n=1}{\frac{1}{n^2}-\frac{1}{(n+1)^2}}=\lim_{n\to \infty }1-\frac{1}{(n+1)^2}=1
\end{gathered}
$$


---
###### 2. Zbadaj zbieżność szeregów liczbowych:

a)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\left(\frac{3n+1}{n+2}\right)^n}=
\sum^{\infty}_{n=1}{\left(\frac{3n+6-5}{n+2}\right)^n}=
\sum^{\infty}_{n=1}{\left(3-\frac{5}{n+2}\right)^n}=\sum^{\infty}_{n=1}{a_n}
\\\\
\lim_{n\to \infty}{(3-\frac{5}{n+2})^n}=\infty \gt 0\\\\
\text{Nie spełnia warunku koniecznego:}\\\\
\sum^{\infty}_{n=1}{a_n} - \text{zbieżny }\implies  \lim_{n\to \infty}{a_n=0}

\end{gathered}$$


b)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(3n)!}{n^{3n}}}=\sum^{\infty}_{n=1}{a_n}:\\\\
\lim_{n\to \infty}{|\frac{a_{n+1}}{a_n}|}=\lim_{n\to \infty}{\frac{(3n+3)!}{(n+1)^{3(n+1)}}}\cdot \frac{n^{3n}}{(3n)!}=\\=\lim_{n\to \infty}{\frac{(3n+1)(3n+2)(3n+3)}{(n+1)^3}\cdot (\frac{n}{(n+1)})^{3n}}=27\cdot (e^{-1})^3\gt 1\\\\
\text{Na podstawie kryterium de Alamberta nie spełnia warunku zbieżności}
\end{gathered}$$

c)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{n+3}{n^3+3}}=\sum^{\infty}_{n=1}{a_n}\\\\
\sum^{\infty}_{n=1}{\frac{1}{n^2}}=\sum^{\infty}_{n=1}{b_n} \\\text{Zbieżny na podstawie twierdzenia o zbieżności szeregów harmonicznych o rzędzie }\gt 2\\\\
\lim_{n\to \infty}{\frac{a_n}{b_n}}=\lim_{n\to \infty }{\frac{n^3+3n^2}{n^3+3}}=1\in (0,+\infty )\\\\
\text{Więc na podstawie kryterium porównawczego granic ilorazowych zbieżny.}
\end{gathered}$$

d)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{n^3(\sqrt{2}+(-1)^n)^n}{3^n}}\lt \sum^{\infty}_{n=1}{\frac{n^3(2\sqrt{2})^n}{3^n}}\\\\
\lim_{n\to \infty}{\sqrt[n]{(\frac{n^32\sqrt{2}}{3})^n}}=\frac{2\sqrt{2}}{3}\lt 1\\\\
\text{Więc szereg większy jest zbieżny na podstawie kryterium Cachy'ego a jeżeli}\\
\text{szereg większy od badanego jest zbieżny (i zawsze dodatnie) to na podstawie kryterium}\\
\text{porównawczego nasz badany szereg też jest zbieżny.}
\end{gathered}$$

e)

$$\begin{gathered}
\sum^{\infty}_{n=2}{\frac{1}{n\ln^2{n}}}\\\\\
f(n)=\frac{1}{n\ln^2{n}}\geq 0 \ \ \forall n \in \mathbb{N}\\\\
\text{Funkcja musi być również nierosnąca na przedziale }[n_0, +\infty )\\\\
\text{Więc żeby nie liczyć weźmy duże n żeby napewno tak było }n_0=3\\\\
\int^{\infty}_{3}{\frac{1}{n\ln^2{n}}\ dn}=\begin{vmatrix}
u=\ln{n}\\
du=\frac{1}{n}dn
\end{vmatrix}=\int^{\infty}_{\ln{3}}{\frac{1}{u^2}\ du}=-\frac{1}{\ln{n}}|^{\infty}_{\ln{3}}=\\=\lim_{n\to \infty}{-\frac{1}{\ln{n}}}-(-\frac{1}{\ln{\ln{3}}})=\frac{1}{\ln{\ln{3}}} - \text{Zbieżna}\\\\
\text{Więc na podstawie kryterium całkowego szereg jest zbieżny.}
\end{gathered}$$

f)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^n\ln{n}}{n}}=\sum^{\infty}_{n=1}{(-1)^na_n}\\\\
\lim_{n\to \infty}{a_n}=
\lim_{n\to \infty}{\frac{\ln{n}}{n}}=0\\
\forall n \geq 3 \ \ a_n\gt 0\\
(a_n)^\infty_3 - \text{malejący }\\\\
\text{Więc na podstawie kryterium szeregów naprzemiennych zbieżny}
\end{gathered}$$

g)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{2^n+3^n}{3^n+4^n}}\\\\
\lim_{n\to \infty}{\sqrt[n]{\frac{2^n+3^n}{3^n+4^n}}}=\frac{3}{4}
\end{gathered}$$
h)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{\sqrt{n+1}-\sqrt{n}}{n}}=
\sum^{\infty}_{n=1}{\frac{1}{n\sqrt{n+1}+n\sqrt{n}}}=\sum^{\infty}_{n=1}{\frac{1}{n\sqrt{n+1}+n\sqrt{n}}}=\sum^{\infty}_{n=1}{a_n}\\\\\\
\sum^{\infty}_{n=1}{\frac{1}{n^{\frac{3}{2}}}}=\sum^{\infty}_{n=1}{b_n} - \text{zbieżny (twierdzenie o zbieżności szeregów harmonicznych)}\\\\\\
\lim_{n\to \infty}{\frac{a_n}{b_n}}=\frac{1}{2}\in (0,+\infty)\\
\text{Na podstawie twierdzenia o kryterium porównawczego granic ilorazowych}\\
\text{Szereg który badamy jest zbieżny}
\end{gathered}$$

i)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{\ln{n}}{n^2}}\\\\
n_0 = 3\\\\
\text{Bo od 3 jest malejące i zawsze dodatnie}\\\\
f(n)=\frac{\ln{n}}{n^2}\\\\
\int{f(n) \ dn}=\begin{vmatrix}
u=\ln{n}\\
du=\frac{1}{n}
\end{vmatrix}=\int{\frac{u}{e^u}\ du}=\begin{vmatrix}
k=u&dv=\frac{1}{e^u}=e^{-u}\\
dk=1&v=-e^{-u}
\end{vmatrix}=u\cdot -e^{-u}-\int{-e^{-u}}\\\\
=-ue^{-u}-e^{-u}=-\ln{e^{-\ln{n}}}-e^{-\ln{n}}=-\ln{n}\cdot \frac{1}{n}-\frac{1}{n}|^{\infty}_{3}=-\ln{3}\cdot \frac{1}{3}-\frac{1}{3} - \text{Zbieżna}\\\\
\text{Na podstawie kryterium całkowego badany szereg jest zbieżny}
\end{gathered}$$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{4^n\cdot x^{3n}}{n+1}}=(t=x^3)
\sum^{\infty}_{n=1}{\frac{4^n\cdot t^{n}}{n+1}}=\frac{1}{t}\sum^{\infty}_{n=1}{\frac{4^n\cdot t^{n+1}}{n+1}}=\frac{1}{t}\cdot S\\\\
S'=\sum^{\infty}_{n=1}{(4t)^n}=\frac{4t}{1-4t}=\\\\
\frac{1}{t}\cdot \int {\frac{4t}{1-4t}\ dt}=\frac{1}{t}\int{\frac{-(1-4t)+1}{1-4t}}=\frac{1}{t}(\int{-1}+\int{\frac{1}{1-4t}})=\\
=\frac{1}{t}\cdot (-t-4\int{\frac{1}{u}})=\frac{1}{t}(-t-4\ln{t})=-1-\frac{\ln{1-4x^3}}{4x^3}\\\
\end{gathered}$$
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{n+2}{4^n}}=
\sum^{\infty}_{n=1}{\frac{n+2}{4^n}x^{n+1}}(x=1)\\\\
\int{\sum^{\infty}_{n=1} \frac{n+2}{4^n}x^{n+1}\ dx}=\sum^{\infty}_{n=1} \frac{x^{n+2}}{4^n}=\frac{\frac{x^3}{4}}{1-\frac{x}{4}}=\frac{x^3}{4-x}(+C)\\\\
\left(\frac{x^3}{4-x}\right)'=-\frac{2(x^3-6x^2)}{x^2-8x+16}\\\\
\text{Z powrotem podstawiajac x=1}\\\\
Wynik: -\frac{2(1-6)}{1-8+16}=-\frac{2\cdot -5}{9}=\frac{10}{9}


\end{gathered}$$


$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}}{n\cdot 3^n}}\overset{x=1}{=}
-\sum^{\infty}_{n=1}{\frac{(-1)^{n}}{n\cdot 3^n}x^n}=S(x)\\\\
S'(x)=-\sum^{\infty}_{n=1}{(\frac{-1}{3})^n\cdot x^{n-1}}=-\frac{1}{x}\sum^{\infty}_{n=1}{(\frac{-x}{3})^n}=-\frac{1}{x}\cdot \frac{\frac{-x}{3}}{1+\frac{x}{3}}=\frac{1}{3+x}\\\\
g(x)=\int{S'(x)\ dx}=\ln{|3+x|}+C\\\\
S(0)=0\\\
g(0)=\ln{3}\implies C=-\ln{3}\\\\
\text{Więc wynik to:}\ln{4}-\ln{3}=\ln{\frac{4}{3}}
\end{gathered}$$


$$\begin{gathered}
f(x)=\ln{x}, x_0=1\\\\
f'(x)=\frac{1}{x}=\frac{1}{1-(1-x)}=\sum^{\infty}_{n=0}{(1-x)^n}\\\
\int{f'(x)\ dx}=\int{\sum^{\infty}_{n=0}{(1-x)^n}}=\begin{vmatrix}
u=1-x\\
du=-1
\end{vmatrix}=\int{\sum^{\infty}_{n=0}{-u^n}}=-\sum^{\infty}_{n=0}{(1-x)^{n+1}\cdot \frac{1}{n+1}}\\
=-\sum^{\infty}_{n=0}{(-1)^{n+1}(x-1)^{n+1}\cdot \frac{1}{n+1}}=
\sum^{\infty}_{n=0}{(-1)^{n+2}(x-1)^{n+1}\cdot \frac{1}{n+1}}=\\=
\sum^{\infty}_{n=1}{(-1)^{n+1}(x-1)^{n}\cdot \frac{1}{n}}=
\end{gathered}$$

$$\begin{gathered}
f(x)=e^{2x+1}, x_0=0\\
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}}\\\\
e^{2x+1}=e\sum^{\infty}_{n=0}{\frac{2^nx^n}{n!}}
\end{gathered}$$


$$\begin{gathered}
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n+1}}{(2n+1)!}}\\
\cos{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n}}{(2n)!}}\\
\sin{x}=\cos{(x-\frac{\pi}{2})}\\
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^n(x-\frac{\pi}{2})^{2n}}{(2n)!}}
\end{gathered}$$


$$\begin{gathered}
f(x)=\ln{(x^2-3x+2)}, x_0=0\\
\Delta=9-8=1\\
x_1=\frac{3+1}{2}=2, x_2=\frac{3-1}{2}=1\\
x\in (-\infty, 1)\cup (2,+\infty)\\\\
f'(x)=\frac{2x-3}{x^2-3x+2}=\frac{1}{x-1}+\frac{1}{x-2}\\\\
f'(x)=-\sum^{\infty}_{n=0}{x^n}-\frac{1}{2}\sum^{\infty}_{n=0}{(\frac{x}{2})^n}\\\\
\int{f'(x)\ dx}=\sum^{\infty}_{n=0}{\frac{-x^{n+1}}{n+1}-\frac{1}{2}\cdot 2^n\cdot \frac{x^{n+1}}{n+1}}=\sum^{\infty}_{n=0}{\frac{x^{n+1}\cdot (-1-\frac{1}{2^{n+2}})}{n+1}}+\ln{2}
\end{gathered}$$



---
$$\begin{gathered}
f(x)=\frac{1}{(x+2)^2}, \ x_0=0\\\\
\int{f(x) \ dx}=\begin{vmatrix}
u=x+2\\
du = dx
\end{vmatrix}=\int{\frac{1}{u^2}\ du}=\int{u^{-2}\ du}=-\frac{1}{u}=-\frac{1}{x+2}=-\frac{1}{2}\cdot \frac{1}{1-(-\frac{x}{2})}\\
=-\frac{1}{2}\sum^{\infty}_{n=0}{\frac{(-1)^nx^n}{2^n}}=
\sum^{\infty}_{n=0}{(\frac{-1}{2})^{n+1}x^n}\\\\
\left(\sum^{\infty}_{n=0}{(\frac{-1}{2})^{n+1}x^n}\right)'=\sum^{\infty}_{n=0}{n(\frac{-1}{2})^{n+1}x^{n-1}}=\sum^{\infty}_{n=0}{(n+1)(\frac{-1}{2})^{n+2}x^{n}}\\\\
|-\frac{x}{2}|\lt 1\\
|x|\lt 2\\
x\in (-2,2)

\end{gathered}$$

$$\begin{gathered}
f(x)=e^{-x^2}, x_0=0\\\\
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}}\\
e^{-x^2}=\sum^{\infty}_{n=0}{\frac{(-x^2)^n}{n!}}=\sum^{\infty}_{n=0}{\frac{(-1)^n(x^2)^n}{n!}}
\end{gathered}$$

$$\begin{gathered}
f(x)=e^{x}, x_0=2\\\\
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}}\\
e^{x-2}=\sum^{\infty}_{n=0}{\frac{(x-2)^n}{n!}}\\
e^x=e^{x-2}\cdot e^2=\sum^{\infty}_{n=0}{e^2\frac{(x-2)^n}{n!}}
\end{gathered}$$

$$\begin{gathered}
f(x)=\sin^2{x}\\
f'(x)=2\cos{x}\sin{x}=\sin{2x}\\
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n+1}}{(2n+1)!}}\\
\sin{2x}=\sum^{\infty}_{n=0}{\frac{(-1)^n(2x)^{2n+1}}{(2n+1)!}}=\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}(x)^{2n+1}}{(2n+1)!}}=\\
f(x)=\int{\sin{2x}\ dx}=\int{\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}(x)^{2n+1}}{(2n+1)!}}}=\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+2}(x)^{2n+1}}{(2n+2)!}}
\end{gathered}$$


###### Oblicz sumę szeregu liczbowego:

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}}\overset{x=1}{=}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}x^n}=\frac{1}{x}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}}x^{n-1}=\frac{1}{x}S(x)\\\\
\lim_{n\to \infty}{|\frac{(-1)^{n+2}\cdot (n+1)}{3^{n}\cdot 3}\cdot \frac{3^n}{(-1)^{n+1}\cdot n}|}=\frac{1}{3}\\
R=3\\\\
\int{S(x)\ dx}=
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}x^n}{3^n}}=-\sum^{\infty}_{n=1}{(-\frac{x}{3})^n}=-\frac{1}{1+\frac{x}{3}}=-\frac{3}{3+x}\\\\
S(x)=\left(\int{S(x)}\right)'=(-\frac{3}{3+x})'=\frac{3}{9+6x+x^2}=\frac{3}{16}
\end{gathered}$$