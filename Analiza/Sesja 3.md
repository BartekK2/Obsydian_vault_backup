###### 1. Dla każdego z trzech ciągów o wyrazach ogólnych $a_n=\frac{n^2}{2^n}$, $b_n=\cos{n\pi}$, $c_n=\sqrt[n]{3^n-2^n}$

$$\begin{gathered}
\lim_{n\to \infty}{a_n}=\lim_{n\to \infty}{\frac{n^2}{2^n}}=[H]=\lim_{n\to \infty}{\frac{2n}{2^n\cdot \ln(2)}}=\lim_{n\to \infty}{\frac{2}{2^n\cdot \ln(2)^2}}=0\\\\
b_n\text{Nie ma granicy bo mozna wyszczegolnic podciagi z rozna granica}\\
\lim_{n\to \infty}{c_n}=3\\\\
\lim_{n\to \infty}{c_n}=\lim_{n\to \infty}{e^{\frac{\ln{(3^n-2^n)}}{n}}}=e^{\lim_{n\to \infty}{\frac{\ln{((1-\frac{2^n}{3^n})3^n)}}{n}}}=
e^{\lim_{n\to \infty}{\frac{\ln{(1-\frac{2^n}{3^n})}+n\ln{3}}{n}}}=e^{\ln{3}}=3
\end{gathered}$$
---
###### 5. Oblicz całke $\int{\frac{x^4+1}{x^3-x^2+x-1}\ dx}$

$$\begin{gathered}
\int{\frac{x^4+1}{x^3-x^2+x-1}\ dx}=\int{x+1+\frac{-1}{(x^2+1)(x-1)}\ dx}\\\\
ostatnia \ calke \ z A/x, B/x, Cx+d/x^2+1\dots
\end{gathered}$$

---
###### oraz całke $\int^{2}_{1}{\frac{dx}{x\sqrt{x^2-1}}}$

$$\begin{gathered}
\int^{2}_{1}{\frac{dx}{x\sqrt{x^2-1}}}=\begin{vmatrix}
u=x^2-1\\
du=2x\ dx\\
dx=\frac{du}{2x}
\end{vmatrix}=\int^{3}_{0}{\frac{1}{2(u+1)\cdot \sqrt{u}}\ du}=\begin{vmatrix}
k=\sqrt{u}\\
dk=\frac{1}{2\sqrt{u}}=
\frac{1}{2k}\ du
\end{vmatrix}=
\\=\int^{\sqrt{3}}_{0}{\frac{2k}{2(k^2+1)\cdot k}\ dk}=\int^{\sqrt{3}}_{0}{\frac{1}{k^2+1}}=\arctan{\sqrt{3}}-\arctan{0}=\frac{\pi}{3}
\end{gathered}$$

---
###### $\int{\frac{x^2}{\sqrt{x^2+2x+2}}\ dx}$


$$\begin{gathered}
\int{\frac{x^2}{\sqrt{x^2+2x+2}}\ dx}=\begin{vmatrix}
\sqrt{x^2+2x+2}=t-x\sqrt{1}\\
x^2+2x+2=t^2-2tx+x^2\\
2x+2=t^2-2tx\\
2x+2tx=t^2-2\\
x(2+2t)=t^2-2\\
x=\frac{t^2-2}{2+2t}\\
dx=\dots 
\end{vmatrix}
\end{gathered}
$$

---
###### 1. Korzystając z definicji całki Riemenna oblicz granicę ciągu $a_n=\sqrt[n]{\frac{n!}{n^n}}$
$$\begin{gathered}
a_n=\sqrt[n]{\frac{n!}{n^n}}=e^{\ln{(\frac{\sqrt[n]{n!}}{n})}}=e^{\frac{1}{n}\ln{(n!)-\ln{n}}}:\\
b_n=\frac{1}{n}\ln{(n!)-\ln{n}}=\frac{1}{n}\sum^{n}_{i=1}{\ln{i}}-\ln{n}=\frac{1}{n}\sum^{n}_{i=1}{\ln{\frac{i}{n}}}\\\\
\lim_{n\to \infty}{b_n}=\int^{1}_{0}{\ln{x} \ dx}\\\\
\int{\ln{x}}=\begin{vmatrix}
u'=1&v=\ln{x}\\
u=x&v'=\frac{1}{x}
\end{vmatrix}=x\ln{x}-\int{1}=x\ln{x}-x\\\\
\lim_{n\to \infty}{b_n}=-1\\\\\
\lim_{n\to \infty}{a_n}=e^{\lim_{n\to infty}{b_n}}=e^{-1}=\frac{1}{e}
\end{gathered}$$
---
###### 3. b) Oszacuj dokładność wzoru przybliżonego $\sqrt[3]{1+x}\approxeq 1+\frac{x}{3}$ dla $0\lt x\lt \frac{1}{10}$


$$\begin{gathered}
\sqrt[3]{1+x}\approxeq 1+\frac{\frac{1}{3}(1+x)^{-\frac{2}{3}}}{1!}+R_2(0,x)\\
R(c)=-\frac{1}{9}\cdot (1+c)^{-\frac{5}{3}} \cdot x^2, c\in (0,\frac{1}{10})\\
R_{max}\ dla \ c \ =0\\
R(x)=-\frac{1}{9}\cdot x^2, maks \ dla \ x =\frac{1}{10}\\
R_{max}=\frac{1}{900}
\end{gathered}$$

Inny lepszy zapis:

$$\begin{gathered}
\sqrt[3]{1+x}\approxeq 1+\frac{x}{3}-\frac{x^2}{9}+\frac{5x^3}{81}\\\\
\text{Dominujacy skladnik to }-\frac{x^2}{9}\\\\
R(x)=\frac{x^2}{9}, R_{max}=\frac{1}{900}
\end{gathered}$$
---
###### 4. Oblicz całke (o ile istnieje) $\int^{\infty}_{-\infty}{\frac{1}{(x^2+x+1)^2}\ dx}$

$$\begin{gathered}
x^2+x+1=0\\
\Delta=1-4\neq 0\\\\
\int^{\infty}_{-\infty}{\frac{1}{(x^2+x+1)^2}\ dx}=
\int^{\infty}_{-\infty}{\frac{1}{((x+\frac{1}{2})^2+\frac{3}{4})^2}\ dx}=\begin{vmatrix}
u=x+\frac{1}{2}
\end{vmatrix}=\\\\
=\int^{\infty}_{-\infty}{\frac{1}{(u^2+\frac{3}{4})^2}}
=\int^{\infty}_{-\infty}{\frac{1}{(\frac{3}{4}(\frac{2u}{\sqrt{3}})^2+1))^2}}=\begin{vmatrix}
t=\frac{2u}{\sqrt{3}}\\
dt=\frac{2}{\sqrt{3}}du
\end{vmatrix}=
\\=\frac{16\sqrt{3}}{18}\int^{\infty}_{-\infty}{\frac{1}{(t^2+1)^2}\ dt}=\frac{16\sqrt{3}}{18}{\int^{\infty}_{-\infty}{\frac{t^2+1}{(t^2+1)^2}-\frac{t^2}{(t^2+1)^2}}\ dt}=
\\=\frac{8\sqrt{3}}{9}\int^{\infty}_{-\infty}{\frac{1}{t^2+1}\ dt}-\frac{8\sqrt{3}}{9}\int^{\infty}_{-\infty}{\frac{t}{2}\frac{2t}{(t^2+1)^2}\ dt}=\\
=\frac{8\pi \sqrt{3}}{9}-\frac{8\sqrt{3}}{9}\int^{\infty}_{-\infty}{\frac{t}{2}\frac{2t}{(t^2+1)^2}\ dt}=\begin{vmatrix}
u=\frac{t}{2}&v'=\frac{2t}{(t^2+1)^2}\\
u'=\frac{1}{2}&v=-\frac{1}{t^2+1}
\end{vmatrix}=\\\\\
=\frac{8\pi \sqrt{3}}{9}-\frac{4\pi \sqrt{3}}{9}=\frac{4\pi }{3\sqrt{3}}
\end{gathered}$$

---
###### Narysuj krzywą i  $r(\varphi)=a\cos^3{(\frac{\varphi}{3})}$ i oblicz jej długość:

$$\begin{gathered}
|L|=\int^{}_{}{\sqrt{r(\varphi)^2+(r'(\varphi))^2}}
\end{gathered}$$
$$\begin{gathered}
b=6\pi, a=0\\\\
r'(\phi)=-\cos^{2}\left(\frac{x}{3}\right)\,\sin\left(\frac{x}{3}\right)\\\\
|L|=a\int^{6\pi}_{0}{\sqrt{\cos^6(\frac{x}{3})+\cos^4(\frac{x}{3})(1-\cos^2(\frac{x}{3}))}}=a\int^{6\pi}_{0}{\cos^2(\frac{x}{3})}=\begin{vmatrix}
u=\frac{x}{3}\\
du=\frac{1}{3}\ dx
\end{vmatrix}=
\\=3a\int^{2\pi}_{0}{\cos^2{u} \ du}=\frac{3}{2}a\int^{2\pi}_{0}{1+cos{2x}\ dx}=\frac{3}{2}a(x+\frac{\sin{2x}}{2})|^{6\pi}_{0}=\frac{3}{2}a(2\pi)=3a\pi  
\end{gathered}$$
---
### Ważne, optymalizacja stereo

###### 1. Jaką największą objętość może mieć ostrosłup prawidłowy trójkątny wpisany w sferę o promieniu $R$?

prawidłowy oznacza że podstawa ma wszystkie boki równe

![[Pasted image 20250210000241.png]]

Najpierw wyznaczam współrzędne jednego z wierzchołków podstawy, przy założeniu że leży na osi OX
$$\begin{gathered}
y=0, z=H, x\\
x^2+H^2=R^2\\
x^2=R^2-H^2\\
x=\sqrt{R^2-H^2}
\end{gathered}$$
Teraz wiem że współrzędne pozostałych wierzchołków da się wyliczyć na podstawie:
$$\begin{gathered}
h=x_B-x_A=\frac{\sqrt{3}}{2}u\\
x_b=\frac{\sqrt{3}}{2}u+x_A\\
y_b=\frac{u}{2}, \text{gdzie }u=\text{bok podstawy}\\
\text{Podstawiamy pod wzór ponieważ wierzchołek musi leżeć}\\
\text{na sferze.}\\
x_b^2+y_b^2+H^2=R^2\\
(\frac{\sqrt{3}}{2}u+x_A)^2+(\frac{u}{2})^2+H^2=R^2\\
(\frac{\sqrt{3}}{2}u+\sqrt{R^2-H^2})^2+(\frac{u}{2})^2+H^2=R^2\\
u^2+\sqrt{3}u\sqrt{R^2-H^2}+H^2=R^2\\
\text{Obliczamy u jak ze zwyklej funkcji kwadratowej}\\
u=\pm \frac{2 \sqrt{3}+\sqrt{12-4 H^2}}{2}=\sqrt{3}+\sqrt{3-H^2}\\\\
\text{Wyznaczamy pole podstawy}\\
P_p=u^2\cdot \frac{\sqrt{3}}{4}\\
\text{Wyznaczamy objętość}:\\
V=\frac{1}{3}P_p\cdot H
\end{gathered}$$

I lecimy z optymalizacją.

---
Wyznacz objętość największego stożka wpisanego w kule o promieniu R.


$$\begin{gathered}
V=\frac{1}{3}P_p\cdot H=\frac{1}{3}\pi r^2H\\
P_{\Delta}=\frac{1}{2}2r\cdot H=\frac{2r\cdot b^2}{4R}\\
2HR=b^2=r^2+H^2\\
2HR-H^2=r^2\\

\end{gathered}$$

Ewentualnie na podstawie twierdzenia sinusow

$$\begin{gathered}
l=\cos{\alpha}2R\\
h=\sin{\alpha}l=2R\cos^2{\alpha}\\
r=2R\sin{\alpha}\cos{\alpha}\\
V=\frac{1}{3}\pi 8R^3\sin^2\cos^4=\frac{1}{3}\pi8R^3t(1-t)^2\implies t=1\implies \sin{\alpha}=1\Leftrightarrow \alpha=45\degree\\\\
r=2R
\end{gathered}$$
---
###### 1. Narysuj krzywą i oblicz jej pole
![[Pasted image 20250210174414.png]]

$$\begin{gathered}
x^4+y^4=x^2+y^2\\
\left\{
\begin{matrix}
x=r\cos{\phi}\\
y=r\sin{\phi}\\
\end{matrix}
\right.\\\\
r^4\cos^4{\phi}+r^4\sin^4{\phi}=r^2\cos^2{\phi}+r^2\sin^2{\phi}\\
r^2=\frac{1}{\cos^4{\phi}+\sin^4{\phi}}\\\\
\cos^4{\phi}+\sin^4{\phi}=(\sin^2{\phi}+\cos^2{\phi})^2-2sin^2{\phi}\cos^2{\phi}=\\=1-\frac{1}{2}\cdot 4sin^2{\phi}\cos^2{\phi}=1-\frac{1}{2}\sin^2{2\phi}\\
r^2=\frac{1}{1-\frac{1}{2}sin^2{2\phi}}\\
r^2=\frac{2}{2-sin^2{2\phi}}\\
r^2=\frac{2}{2-sin^2{2\phi}}\\
\end{gathered}$$

$$\begin{gathered}
\int^{\frac{\pi}{2}}_{0}{r^2}=
2\int^{\frac{\pi}{2}}_{0}{\frac{1}{2-sin^2{2\phi}}}=\begin{vmatrix}
t=\tan{2\phi}\\
dt=(t^2+1)\cdot 2d\phi\\
d\phi=\frac{dt}{2(t^2+1)}\\
\sin^2{2\phi}=\frac{\sin^2{2\phi}}{\sin^2{2\phi}+\cos^2{2\phi}}=\frac{t^2}{t^2+1}
\end{vmatrix}=\\\\\\
=2\int^{\infty}_{0}{\frac{1}{2-\frac{t^2}{t^2+1}}\cdot \frac{1}{2(t^2+1)} dt}=2\int^{\infty}_{0}{\frac{1}{\frac{2t^2+2}{t^2+1}-\frac{t^2}{t^2+1}}\cdot \frac{1}{2(t^2+1)} \ dt}=\\\\
=2\int^{\infty}_{0}{\frac{1}{\frac{t^2+2}{t^2+1}\cdot 2(t^2+1)}\ dt}=\\\\
=\int^{\infty}_{0}{\frac{1}{t^2+2}\ dt}
=\frac{1}{2}\int^{\infty}_{0}{\frac{1}{((\frac{t}{\sqrt{2}})^2+1)}\ dt}=\begin{vmatrix}
u=\frac{t}{\sqrt{2}}\\
du=\frac{1}{\sqrt{2}}\ dt
\end{vmatrix}=\\\\
=\frac{\sqrt{2}}{2}\int^{\infty}_{0}{\frac{1}{u^2+1}\ du}=\frac{\sqrt{2}}{2}\frac{\pi}{2}=\frac{\pi\sqrt{2}}{4}

\end{gathered}$$


$$\begin{gathered}
2\int{\frac{1}{2-\sin^2{2\phi}}\ d\phi}=\begin{vmatrix}
t=\tan{2\phi}\\
\sin^2{2\phi}=\frac{\sin^2{2\phi}}{\sin^2{2\phi}+\cos^2{2\phi}}=\frac{t^2}{t^2+1}\\
dt=(t^2+1)\cdot 2=2t^2+2\ d\phi\\
d\phi=\frac{dt}{2t^2+2}
\end{vmatrix}=\\\\\
=\int{\frac{1}{2-\frac{t^2}{t^2+1}}\cdot \frac{1}{t^2+1}\ dt}=\int{\frac{1}{{t^2+2}}\ dt}=\int{\frac{1}{2((\frac{t}{\sqrt{2}})^2+1)}\ dt}=\begin{vmatrix}x=\frac{t}{\sqrt{2}}\\
dx=\frac{1}{\sqrt{2}}\ dt\\
\sqrt{2}dx= dt
\end{vmatrix}=\\\\\
=\frac{1}{2}\int{\frac{1}{x^2+1}\ dt}=
\frac{1}{2}\arctan{(\frac{tan{2\phi }}{\sqrt{2}})}|^{\frac{\pi}{4}}_0=\frac{1}{2}\cdot \frac{\pi}{2}=\frac{\pi}{4}
\end{gathered}$$



---
![[diagram-20250210.png]]

$$\begin{gathered}
P_b=\pi \cdot R\cdot \sqrt{H^2+R^2}\\
R^2=\frac{3V}{\pi H}\\
R=\sqrt{\frac{3V}{\pi H}}\\\\
P_b=\pi \sqrt{\frac{3V}{\pi H}}\cdot \sqrt{H^2+\frac{3V}{\pi H}}\\\\
P_b'=\dfrac{\sqrt{3}\,\sqrt{v}\,\left(\pi\,{h}^{3}-6\,v\right)}{2\,{h}^{2}\,\sqrt{\pi\,{h}^{3}+3\,v}}=0\\
\sqrt{3v}\pi \cdot h^3-6v\sqrt{v}\sqrt{3}=0\\
h^3=\frac{6v}{\pi}\\
h=\sqrt[3]{\frac{6v}{\pi }}
\end{gathered}$$
---
