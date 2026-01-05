
---
## Równania różniczkowe o zmiennych rozdzielonych

### 1. Wiadomości wstępne

Szukamy funkcji $y(x)$ spełniającej w każdym punkcie przedziału $(a,b)$ równanie:
$$\begin{gathered}
\frac{dy}{dx}=f(x)&(1)
\end{gathered}$$

Jeżeli $F(x)$ jest jakąkolwiek funkcją pierwotną $f(x)$ to zbiór wszystkich funkcji 
$$\begin{gathered}
y(x)=F(x)+C&(2)
\end{gathered}$$
gdzie $C$ jest dowolną stałą zawiera wszystkie funkcje spełniające równanie $(1)$ i tylko takie funkcje. Zbiór funkcji $(2)$ jest **całką ogólną** równania $(1)$.

Jeżeli zażądamy dodatkowo, by funkcja $f(x)$ spełniała warunek:
$$\begin{gathered}
y(x_0)=y_0&(3)
\end{gathered}$$
to z $(2)$ otrzymamy $y_0=F(x_0)+C$ a stąd $C=y_0-F(x_0)$. Istnieje zatem dokładnie jedna funkcja spełniająca równanie $(1)$ i warunek początkowy $(3)$:
$$\begin{gathered}
y(x)=F(x)+y_0-F(x_0)
\end{gathered}$$

###### 1.1 Przykład

Znaleźć rozwiązanie równania $y'=-2x$, spełniające warunek początkowy $y(0)=1$. 
$$\begin{gathered}
y(x)=-x^2+C\\
y(0)=1\implies C=1\\
y=1-x^2
\end{gathered}$$
---
### 2. Równania różniczkowe o zmiennych rozdzielonych 

Równanie 
$$\begin{gathered}
\frac{dy}{dx}=\frac{f(x)}{h(y)}&(6)
\end{gathered}$$
o funkcji niewiadomej $y(x)$ nazywamy **równaniem różniczkowym o zmiennych rodzielonych**. Równanie te możemy zapisać:
$$\begin{gathered}
h(y)dy=f(x)dx&(7)
\end{gathered}$$
Niech
$$\begin{gathered}
\int{h(y)dy}=H(y)+C_H, \int{f(x) dx}=F(x)+C_F&(8)
\end{gathered}$$
Czyli 
$$\begin{gathered}
H(y)+C_H=F(x)+C_F\\
H(y)-F(x)=C, \ \ \ \ C=C_F-C_H
\end{gathered}$$
###### 2.1 Przykład

Znaleźć calkę równania $y'=-2x/y$, spełniające warunek początkowy $y(1)=1$

$$\begin{gathered}
\frac{dy}{dx}=\frac{-2x}{y}\\
ydy=-2x dx\\
\frac{y^2}{2}+C_y=-x^2+C_x\\
\frac{y^2}{2}+x^2=C\\
y(1)=1\implies C=\frac{3}{2}\\
\frac{y^2}{2}+x^2=\frac{3}{2}
\end{gathered}$$

---
### 3. Równania jednorodne 

Równanie:
$$\begin{gathered}
\frac{dy}{dx}=f(\frac{y}{x})
\end{gathered}$$

o funkcji niewiadomej $y(x)$ nazywamy **równaniem różniczkowym jednorodnym**. Równanie to za pomocą podstawienia:
$$\begin{gathered}
u(x)=\frac{y}{x}
\end{gathered}$$

można sprowadzić do równania różniczkowego o zmiennych rozdzielonych. 
$$\begin{gathered}
\frac{dy}{dx}=u(x)+x \frac{du}{dx}\\
u+xu'=f(u)\\
\frac{du}{f(u)-u}=\frac{dx}{x}
\end{gathered}$$

Czyli równanie różniczkowe o zmiennych rozdzielonych.

###### 3.1 Przykład

Znaleźć całke ogólną równania $y'=\frac{(x+y)}{x}$
$$\begin{gathered}
\frac{dy}{dx}=\frac{(x+y)}{x}=1+\frac{y}{x}\\\\
u=\frac{y}{x}\\
ux=y\\
\frac{du}{dx}x+u=\frac{dy}{dx}\\
\frac{du}{dx}x+u=1+u\\
\frac{du}{dx}x=1\\
du=\frac{dx}{x}\\
u=\ln{|x|+C}\\\\
y=\ln{|x|x+Cx}
\end{gathered}$$

---
### 4. Równania sprowadzalne do równań jednorodnych

#### 4.1 Równanie $\frac{dy}{dx}=f(ax+by+c)$

Równanie 
$$\begin{gathered}
\frac{dy}{dx}=f(ax+by+c)
\end{gathered}
$$
gdzie $a,b,c\neq 0$ są to dane liczby, sprowadzamy do równania różniczkowego o zmiennych rozdzielonych za pomocą podstawienia
$$\begin{gathered}
u(x)=ax+by+c
\end{gathered}
$$
Z powyższego mamy 
$$\begin{gathered}
u'=a+by'
\end{gathered}$$
więc
$$\begin{gathered}
\frac{du}{dx}=a+b \frac{dy}{dx}\\\\
\downarrow\\\\
\frac{dy}{dx}=\frac{1}{b}\left(\frac{du}{dx}-a\right), \ \ \ \ \frac{du}{dx}=a+bf(u)
\end{gathered}$$
czyli
$$\begin{gathered}
\frac{du}{a+bf(u)}=dx
\end{gathered}$$

###### 4.2 Przykład

Znaleźć całkę ogólną równania $y'=x+y+7$

$$\begin{gathered}
u(x)=x+y+7\\
\frac{dy}{dx}=u(x)\\
\frac{du}{dx}=1+\frac{dy}{dx}\\
\frac{du}{dx}=1+u\\
\frac{du}{1+u}=dx\\
\ln{|u+1|}=x+C\\
u+1=Ae^x\\
x+y+8=Ae^x\\
y=Ae^x-x-8
\end{gathered}
$$

---
### 4.3  Równanie $\frac{dy}{dx}=f \left(\frac{a_1x+b_1y+c_1}{a_2x+b_2y+c_2}\right)$
Równanie
$$\begin{gathered}
\frac{dy}{dx}=f \left(\frac{a_1x+b_1y+c_1}{a_2x+b_2y+c_2}\right)
\end{gathered}$$
sprowadzamy do równania jednorodnego lub równania różniczkowego o zmiennych rozdzielonych.

Jeżeli
$$\begin{gathered}
W=\begin{vmatrix}
a_1&b_1\\
a_2&b_2
\end{vmatrix} \neq 0
\end{gathered}$$
wprowadzamy zmienne
$$\begin{gathered}
\xi=x-h, \gamma=y-k
\end{gathered}$$
gdzie
$$\begin{gathered}
a_1h+b_1k+c_1=0\\
a_2h+b_2k+c_2=0\\
\end{gathered}$$
Ponieważ
$$\begin{gathered}
\frac{d \gamma}{d \xi}=\frac{dy}{dx}
\end{gathered}$$
mozna zapisac pierwotne równanie jako 
$$\begin{gathered}
\frac{d \gamma}{d \xi}=f \left(\frac{a_1 \xi+b_1 \gamma}{a_2 \xi+b_2 \gamma}\right)
\end{gathered}$$
Powyższe równanie jest równaniem jednorodnym.
Jeżeli:
$$\begin{gathered}
W=\begin{vmatrix}
a_1&b_1\\
a_2&b_2
\end{vmatrix}=0
\end{gathered}$$

to istnieje liczba $\lambda=\frac{a_1}{a_2}=\frac{b_1}{b_2}$ wówczas:
$$\begin{gathered}
\frac{dy}{dx}=f \left(\frac{\lambda (a_2x+b_2y)+c_1}{a_2x+b_2y+c_2}\right)
\end{gathered}$$
Podstawiamy $u=a_2x+b_2y$ wówczas $u'=a_2+b_2y'$ i otrzymujemy równanie o zmiennych rozdzielonych
$$\begin{gathered}
\frac{du}{dx}=a_2+b_2f \left(\frac{\lambda u+c_1}{u+c_2}\right)
\end{gathered}$$
###### 4.4 Przykład 1

Znajdź całke ogólną równania $\frac{dy}{dx}=-\frac{x+y-2}{x-y-4}$
$$\begin{gathered}
W=\begin{vmatrix}
1&1\\
1&-1
\end{vmatrix}=-2 \neq 0\\
\xi=x-h, \gamma=y-k\\
\left\{
\begin{matrix}
h+k-2=0\\
h-k-4=0
\end{matrix}\right. \implies h=3,k=-1\\\\
\xi=x-3,\gamma=y+1\\\\
\frac{d \gamma}{d \xi}=\frac{dy}{dx}\\
\downarrow\\
\frac{d \gamma}{d \xi}=-\frac{\xi+\gamma}{\xi-\gamma}\\
u(\xi)=\frac{\gamma}{\xi}\\\\
-\frac{\xi+\gamma}{\xi-\gamma}=-\frac{\frac{\xi}{\xi}+\frac{\gamma}{\xi}}{\frac{\xi}{\xi}-\frac{\gamma}{\xi}}=-\frac{1+u}{1-u}\\\\
u+\xi u'=\frac{d \gamma}{d \xi}
\end{gathered}$$

 Zatem przechodzimy do rozwiązania równania jednorodnego:
$$\begin{gathered}
u+\xi u'=\frac{u+1}{u-1} /-u\\
\xi \frac{du }{d \xi}=\frac{u+1-u^2+u}{u-1}=\frac{-u^2+2u+1}{u-1}\\
\frac{u-1}{-u^2+2u-1}du=\frac{1}{\xi}d \xi / \int\\
\int{\frac{u-1}{-u^2+2u-1}du}=\begin{vmatrix}
t=-u^2+2u-1\\
dt=-2u+2\\
u-1=-\frac{1}{2}dt
\end{vmatrix}=\\
=-\frac{1}{2}\int{\frac{1}{t}dt}=-\frac{1}{2}\ln{|-u^2+2u-1}\\
-\frac{1}{2}\ln{|-u^2+2u-1|}=\ln{|\xi|+C_1}\\
\ln{|-u^2+2u-1|}=-2\ln{|\xi|+C_1}\\
\ln{|-u^2+2u-1|}=\ln{|\frac{1}{\xi^2}|+C_1}\\
\xi^2(-u^2+2u+1)=C_2\\
\text{Podstawiamy z powrotem nasze }u,\xi\\
x^2+2xy-y^2-4x-8y=C
\end{gathered}$$

###### 4.5 Przykład 2

Znajdź całke ogólną równania:
$$\begin{gathered}
\frac{dy}{dx}=-\frac{x+2y+1}{x+2y-1}\\
W=\begin{vmatrix}
1&2\\
1&2
\end{vmatrix}=0\\
\lambda=1\\
\frac{dy}{dx}=f \left(\frac{\lambda (a_2x+b_2y)+c_1}{a_2x+b_2y+c_2}\right)\\\\
u=a_2x+b_2y\implies u'=a_2+b_2y'\\
\downarrow\\
u'=a_2+b_2 f(\frac{\lambda u+c_1}{u+c_2})\\\\

u=x+2y\\
u'=1+2\frac{dy}{dx}\\
u'=1-2\frac{u+1}{u-1}\\
u'=\frac{u-1-2(u+1)}{u-1}=\frac{-u-3}{u-1}\\
-\frac{u-1}{u+3}du=dx\\
-\frac{u+3-4}{u+3}du=dx\\
-1-4\frac{1}{u+3}du=dx\\
-u-4\ln{|u+3|}=x\\
-x-2y-4\ln{|x+2y+3|}=x\\
x+y-2\ln{|x+2y+3|}=C
\end{gathered}$$
---

### zadania

###### 1. $y'=\frac{1}{1+x^2},y(0)=1$

$$\begin{gathered}
\frac{dy}{dx}=\frac{1}{1+x^2}\\
y=\int{\frac{1}{1+x^2}dx}=\arctan{x}+C\\
y(0)=0\implies C=1\\
y=\arctan{x}+1
\end{gathered}$$

###### 2. $y'=\frac{\cos{x}}{y}, y(\frac{\pi}{2})=\sqrt{2}$

$$\begin{gathered}
ydy=\cos{x}dx\\
\frac{y^2}{2}=\sin{x}+C_1\\
y^2=2\sin{x}+C_2\\
2=2\sin{\frac{\pi}{2}}+C_2=2+C_2\implies C_2=0\\
y^2=2\sin{x}
\end{gathered}$$

###### 3. $y'=-\frac{1}{1-\frac{y}{x}}+\frac{x}{y-\frac{y^2}{x}}$

$$\begin{gathered}
u=\frac{y}{x}\\
u'x+u=\frac{dy}{dx}=y'\\
u'x+u=-\frac{1}{1-u}+\frac{1}{u-u^2}=\frac{1-u}{u-u^2}=\frac{1}{u}\\\\
u'x=\frac{1-u^2}{u}\\
\frac{u}{1-u^2}du=\frac{dx}{x}\\
\int{Ldu}=\begin{vmatrix}
t=1-u^2\\
dt=-2u\\
u=-\frac{dt}{2}
\end{vmatrix}=-\frac{1}{2}\int{\frac{1}{t}dt}=-\frac{1}{2}\ln{|1-u^2|}\\\\
-\frac{1}{2}\ln{|1-\frac{y^2}{x^2}|}=\ln{|x|}+C_1\\
\ln{|1-\frac{y^2}{x^2}|}=\ln{|\frac{1}{x^2}|}+C_2\\
\ln{|1-\frac{y^2}{x^2}|}+\ln{A}=\ln{|\frac{1}{x^2}|}+C_2\\

\ln{|A(1-\frac{y^2}{x^2})|}=\ln{|\frac{1}{x^2}|}\\
A(1-\frac{y^2}{x^2})=\frac{1}{x^2}\\
x^2-y^2=C_3
\end{gathered}$$
###### 5. $y'=\frac{x^2+y^2}{xy},y(1)=0$

$$\begin{gathered}
y'=\frac{x^2+y^2}{xy}=\frac{1+\frac{y^2}{x^2}}{\frac{y}{x}}\\
u=\frac{y}{x}\\
u+u'x=\frac{dy}{dx}=y'\\
u+u'x=\frac{1+u^2}{u}\\
u'x=\frac{1}{u}\\
u du=\frac{dx}{x}\\
\frac{u^2}{2}=\ln{x}\\
\frac{\frac{y^2}{x^2}}{2}=\ln{x}\\
y^2=2x^2\ln{|x|}\\
y=\sqrt{2x \ln{|x|}}\\
y(1)=0\implies C=0
\end{gathered}$$

###### 5. $y'=-\frac{x}{y}, y(1)=0$
$$\begin{gathered}
ydy=-xdx\\
\frac{y^2}{2}=-\frac{x^2}{2}+C_1\\
y^2+x^2=C_2\\
1+0=C_2\implies C_2=1\\
y^2+x^2=1
\end{gathered}$$
###### 6. $y'=\frac{y-x}{y+x},y(1)=1$

$$\begin{gathered}
y'=\frac{y-x}{y+x}=\frac{\frac{y}{x}-1}{\frac{y}{x}+1}\\
u(x)=\frac{y}{x}\\
u(x)+xu'=\frac{dy}{dx}\\
u+xu'=\frac{u-1}{u+1}\\
xu'=\frac{u-1-u^2-u}{u+1}=\frac{-u^2-1}{u+1}\\
\frac{u+1}{-u^2-1}du=\frac{dx}{x}\\
\int{Ldu}=\begin{vmatrix}
t=-u^2-1\\
dt=-2u\\
u=-\frac{1}{2}dt
\end{vmatrix}=-\frac{1}{2}\int{\frac{dt}{t}}+\int{\frac{1}{-u^2-1}}=\\
=-\frac{1}{2}\ln{|-u^2-1|-\arctan{u^2}}\\     
=-\frac{1}{2}\ln{|-\frac{y}{x}^2-1|-\arctan{\frac{y}{x}^2}}\\\\
-\frac{1}{2}\ln{|-\frac{y}{x}^2-1|-\arctan{\frac{y}{x}^2}}=\ln{x}+C_1\\
C_1=\dots
\end{gathered}$$

###### 7. $y'=x+y-1,y(0)=2$

$$\begin{gathered}
u(x)=x+y-1\\
u'=1+y'\\
u'-1=y'\\
u'-1=u\\
\frac{du}{1+u}=dx\\
\ln{|1+u|}=x+C_1\\
|1+u|=e^{x+C_1}=e^{C_1}\cdot e^x=C_2\cdot e^x\\
x+y=C_2\cdot e^x\\
2=C_2\\
y=2\cdot e^x-x
\end{gathered}$$

###### 8. $y'=e^{x+y}, y(0)=0$

$$\begin{gathered}
u(x)=x+y\\
u'-1=\frac{dy}{dx}\\\\
u'-1=e^u\\
\frac{du}{e^u+1}=dx\\
\int{\frac{1}{e^u+1}du}=
\int{\frac{e^u+1-e^u}{e^u+1}du}=u-\int{\frac{e^u}{e^u+1}du}=\\
=\begin{vmatrix}
t=e^u+1\\
dt=e^u du
\end{vmatrix}=u-\int{\frac{dt}{t}}=u-\ln{|e^u+1|}\\\\
u-\ln{|e^i+1|}=x+C\\
x+y-\ln{|e^{x+y}+1|}=x+C\\
y-\ln{|e^{x+y}+1|}=C\\
0-\ln{|1+1|}=C\implies C=-\ln{2}\\\\
y-\ln{|e^{x+y}+1|}=-\ln{2}

\end{gathered}$$




### Dodatkowe zadania do ostatniej części

###### 1. $y'=\frac{x+y+1}{2x+2y-1}$

$$\begin{gathered}
y'=\frac{x+y+1}{2x+2y-1}\\\\
W=\begin{vmatrix}
1&1\\
2&2
\end{vmatrix}=2-2=0\\\\
u=x+y\\
u'-1=y'\\
y'=\frac{u+1}{2u-1}\\
\downarrow\\\\\
u'-1=\frac{u+1}{2u-1}\\\\
\frac{du}{dx}=\frac{3u}{2u-1}\\
\frac{2u-1}{3u}du=dx\\
\frac{2}{3}u-\frac{1}{3}\ln{|u|}=x+C\\
\frac{2}{3}\left(x+y\right)-\frac{1}{3}\ln{|\left(x+y\right)|}=x+C_1\\
2x+2y-\ln{|x+y|}=3x+C_2\\
\end{gathered}$$

###### 2. $y'=\frac{x+y-4}{x-y-2}, y(2)=4$

$$\begin{gathered}
W=\begin{vmatrix}
1&1\\
1&-1
\end{vmatrix}=-1-1=-2\neq 0\\\\
\xi=x-k, \ \ \ \gamma=y-h\\
\\\left\{
\begin{matrix}
k+h-4=0\\
k-h-2=0
\end{matrix}
\right.\implies k=3, h=1\\\\\
\frac{d \gamma}{d \xi}=\frac{dy}{dx}\\\\
\frac{d \gamma}{d \xi}=\frac{\xi+\gamma}{\xi-\gamma}=\frac{\frac{\xi}{\xi}+\frac{\gamma}{\xi}}{\frac{\xi}{\xi}-\frac{\gamma}{\xi}}=\frac{1+u}{1-u}\\\\
\text{gdzie:  }u=\frac{\gamma}{\xi}\\\\
u+u' \xi = \frac{d \gamma}{d \xi}=\frac{dy}{dx}\\\\
u+u' \xi=\frac{1+u}{1-u}
\end{gathered}$$
Wystarczy dokończyć równanie o zmiennych rozdzielonych.

$$\begin{gathered}
u' \xi=\frac{1+u^2}{1-u}\\
\frac{1-u}{1+u^2}du=\frac{d \xi}{\xi}\\\\
\arctan{u}-(1)=\ln{|\xi|}+C\\\\
(1)=\dots\\\\
\int{\frac{u}{1+u^2}du}=\begin{vmatrix}
t=1+u^2\\
dt=2u \ du\\
\frac{dt}{2}=u\ du
\end{vmatrix}=\frac{1}{2}\int{\frac{dt}{t}}=\frac{1}{2}\ln{|1+u^2|}\\\\
\arctan{u}-\frac{1}{2}\ln{|1+u^2|}=\ln{|x-3|}+C\\\\
\arctan{\frac{y-1}{x-3}}-\frac{1}{2}\ln{|1+\frac{y-1}{x-3}^2|}=\ln{|x-3|}+C\\\\
\text{Pozostało wyliczenie stałej:}\\\\
C=\dots
\end{gathered}$$