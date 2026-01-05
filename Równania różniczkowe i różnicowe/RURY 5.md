## Równania różniczkowe liniowe rzędu drugiego o stałych współczynnikach

### 1. Wstęp

Rozpatrzmy:
$$\begin{gathered}
y''+p(x)y'+q(x)y=0&(1)
\end{gathered}$$
oraz funkcję zespoloną zmiennej rzeczywistej
$$\begin{gathered}
w(x)=u(x)+iv(x)&(2)
\end{gathered}$$
gdzie $u(x)=\mathbb{R}w(x), v(x)=\Im w(x)$ a $i$ jednostka urojona.

#### Twierdzenie 1. Jeżeli funkcja $(2)$ jest całką równania $(1)$ z rzeczywistymi współczynnikami $p(x)$ i $q(x)$, to jej część rzeczywista $u(x)$ i część urojona $v(x)$ są także całkami tego równania.

### 2. Równanie różniczkowe liniowe jednorodne rzędu drugiego o stałych współczynnikach:

Wyznaczanie układu podstawowego całek dla równania:
$$\begin{gathered}
y''+py'+qy=0&(3)
\end{gathered}$$
gdzie $p$ i $q$ są to dane liczby rzeczywiste.

Rozwiązanie równania $(3)$ poszukujemy w postaci funkcji wykładniczej: 
$$\begin{gathered}
y=e^{rx}&(4)
\end{gathered}$$
w którym dobieramy $r$ tak by funkcja $(4)$ spełniała równanie $(3)$. Ponieważ $y'=re^{rx}$ i $y''=r^2e^{rx}$ więc funkcja $(4)$ spełnia równanie $(3)$ wtedy i tylko wtedy gdy liczba $r$ jest pierwiastkiem równania kwadratowego:
$$\begin{gathered}
r^2+pr+q=0&(5)
\end{gathered}$$
Równanie $(5)$ nazywamy **równaniem charakterystycznym** równania $(3)$. Rozpatrzmy trzy przypadki równania charakterystycznego w zależności od wyróżnika $\Delta=p^2-4q$:


1) $\Delta \gt 0$
równanie $(5)$ ma wówczas dwa różne pierwiastki rzeczywiste $r_1$ i $r_2$. Funkcje:
$$\begin{gathered}
y_1(x)=e^{r_1x}&y_2(x)=e^{r_2x}
\end{gathered}$$
są więc rozwiązaniami równania $(3)$. Funkcje te stanowią układ podstawowy całek tego równania ponieważ wrońskian:
$$\begin{gathered}
W(x)=\begin{vmatrix}
e^{r_1x}&e^{r_2x}\\
r_1e^{r_1x}&r_2e^{r_2x}
\end{vmatrix}=(r_2-r_1)e^{(r_1+r_2)x}\neq 0
\end{gathered}$$
Wzór:
$$\begin{gathered}
y=C_1e^{r_1x}+C_2e^{r_2x}&(6)
\end{gathered}$$
przedstawia zatem rozwiązanie równania $(3)$ dla $\Delta \gt 0$


2. $\Delta=0$
Równanie $(5)$ ma wówczas jeden pierwiastek rzeczywisty podwójny $r_0=-\frac{p}{2}$. Mamy więc tylko jedną całke szczególną $y_1(x)=e^{r_0x}$ równania $(3)$. Zauważmy, że $y=Cy_1$ jest też całką tego równania dla dowolnej stałej $C$. Zatem szukamy rozwiązania w postaci:
$$\begin{gathered}
y=C(x)e^{r_0x}&(7)
\end{gathered}$$
Stąd
$$\begin{gathered}
\left\{
\begin{matrix}
y'=C'(x)e^{r_0x}+r_0C(x)e^{r_0x}\\
y''=e^{r_0x} \left(C''(x)+2r_0C'(x)+r_0^2C(x)\right)
\end{matrix}
\right.&(8)
\end{gathered}$$

Podstawiając $(7)$ i $(8)$ do $(3)$ otrzymujemy warunek:
$$\begin{gathered}
C''(x)+(2r_0+p)C'(x)+(r_0^2+pr_0+q)C(x)=0
\end{gathered}$$

Ponieważ $r_0$ jest podwójnym pierwiastkiem równania charakterystycznego $(5)$, więc $2r_0+p=0$ i $r_0^2+pr_0+q=0$. Stąd $C''(x)=0$ czyli $C(x)=C_1x+C_2$. Funkcja:

$$\begin{gathered}
y=(C_1x+C_2)e^{r_0x}&(9)
\end{gathered}$$
spełnia $(3)$ dla wszystkich wartości stałych $C_1,C_2$ w szczególności dla $C_1=1$ i $C_2=0$, więc funkcja:
$$\begin{gathered}
y=xe^{r_0x}
\end{gathered}$$
jest całką tego równania. Całki:
$$\begin{gathered}
y=e^{r_0x}&i&y=xe^{r_0x}
\end{gathered}$$
stanowią układ podstawowy całek tego równania, ponieważ wrońskian:
$$\begin{gathered}
W(x)=\begin{vmatrix}
e^{r_0x}&xe^{r_0x}\\
r_0e^{r_0x}&(1+r_0x)e^{r_0x}
\end{vmatrix}=e^{2r_0x} \neq 0
\end{gathered}$$

Wzór $(9)$ przedstawia zatem rozwiązanie równania $(3)$ dla $\Delta=0$.

3. $\Delta \lt 0$: równanie $(5)$ ma wówczas dwa różne pierwiastki zespolone sprzężone $r_1=\alpha+i \omega$  i $r_2=\alpha-i \omega$. Funkcje zespolone zmiennej rzeczywistej postaci:
$$\begin{gathered}
y_1(x)=e^{(\alpha+i \omega)x}&i&y_2(x)=e^{(\alpha-i \omega)x}
\end{gathered}$$

są więc całkami równania $(3)$, Na podstawie wzoru Eulera $(e^{i \varphi}=\cos{\varphi}+i \sin{\varphi})$ mamy:
$$\begin{gathered}
y_1(x)=e^{\alpha x}\cos{\omega x}+i e^{\alpha x}\sin{\omega x}
\end{gathered}$$
zatem na mocy twierdzenia $1$, funkcje:
$$\begin{gathered}
y_1(x)=e^{\alpha x}\sin{\omega x}&i&y_2(x)=e^{\alpha x}\cos{\omega x}
\end{gathered}$$
są także całkami równania $(3)$. Całki te stanowią układ podstawowy całek tego równania, ponieważ wrońskian:
$$\begin{gathered}
W(x)=\omega e^{2\alpha x}\neq 0&(10)
\end{gathered}$$
Funkcja:
$$\begin{gathered}
y_1(x)=e^{\alpha x} \left(C_2\cos{\omega x}+C_1 \sin{\omega x}\right)
\end{gathered}$$
przedstawia rozwiązanie równania $(3)$ dla $\Delta \lt 0$.

##### Przykład 1

$$\begin{gathered}
y''+4y=0\\
r^2+4=0\\
r=2i \vee r=-2i\\\\
więc:\\
\alpha=0, \omega=2
\end{gathered}$$
Czyli rozwiązanie to:
$$\begin{gathered}
y=C_1 \sin{2x}+C_2 \cos{2x}
\end{gathered}$$
##### Przykład 2
$$\begin{gathered}
y''+4y'+5y=0\\
r^2+4r+5=0\\
\Delta=16-20=-4\\
r_1=\frac{-4+2i}{2}=-2+i\\
r_2=\frac{-4-2i}{2}=-2-i\\
więc:\\
\alpha=-2, \omega=1
\end{gathered}$$

Zatem rozwiązaniem jest:
$$\begin{gathered}
y=e^{-2x}(C_1 \sin{x}+C_2 \cos{x})
\end{gathered}$$

---
### 3. Równanie różniczkowe liniowe niejednorodne rzędu drugiego o stałych wspołczynnikach

Równanie
$$\begin{gathered}
y''+py'+qy=f(x)&(13)
\end{gathered}$$
gdzie $p$ i $q$ są to dane liczby rzeczywiste, nazywamy **równaniem różniczkowym liniowym niejednorodnym rzędu drugiego o stałych współczynnikach**

Korzystając z 3 poprzednich gotowych wzorów zależnych od $\Delta$ na CORJ możemy wyznaczyć CORN $(13)$ stosując metodę uzmienniania stałych lub metodę przewidywań.

#### Twierdzenie 2

Suma całek szczególnych jest całką szczególną:
$$\begin{gathered}
y''+p(x)y'+q(x)y=f_1(x)\\
y''+p(x)y'+q(x)y=f_2(x)\\\\
y''+p(x)y'+q(x)y=f_1(x)+f_2(x)
\end{gathered}$$

##### Przykład:

Znajdź rozwiązanie ogólne równania $y''+y=e^{2x}+4x \cos{x}$

Mamy $r^2+1=0$, $r_1=i, r_2=-i$ - więc $\alpha=0, \omega=1$ czyli szukaną CORJ jest:
$$\begin{gathered}
y_0=C_1 \sin{x}+C_2 \cos{x}
\end{gathered}$$

Z twierdzenia 2 sumą CSRN
$$\begin{gathered}
y''+y=e^{2x}
\end{gathered}$$
oraz
$$\begin{gathered}
y''+y=4x \cos{x}
\end{gathered}$$
jest CSRN $(14)$.

CSRN $(15)$ przewidujemy w postaci $y_1=a e^{2x}$, stąd $y'_1=2ae^{2x}$ oraz $y''=4ae^{2x}$, czyli $4ae^{2x}+ae^{2x}=e^{2x}$. Wynika stąd że $a=\frac{1}{5}$ i ostatecznie:
$$\begin{gathered}
y=\frac{1}{5}e^{2x}
\end{gathered}$$

CSRN $(16)$ przewidujemy w postaci najpierw:
$$\begin{gathered}
y_2^*=(a_1x+b) \sin{x}+(a_2x+b)\cos{x}
\end{gathered}$$
ale następnie zauważamy rezonans z CORJ więc należy całość przemnożyć przez $x$ żeby wyliczyć współczynniki:
$$\begin{gathered}
y_2=(a_1x+b) x\sin{x}+(a_2x+b)x\cos{x}
\end{gathered}$$

stąd:
$$\begin{gathered}
y_2'=(2a_1x+b_1)\sin{x}+(a_1x+b+1)x \cos{x}+\\+(2a_2x+b_2)\cos{x}-(a_2x+b_2)x \sin{x}\\\\
y_2''=2a_1\sin{}+2(2a_1x+b_1)\cos{x}-(a_1x+b+1)xsin
{x}\\
+2a_2\cos{x}-2(2a_2x+b_2)\sin{x}-(a_2x+b_2)x \cos{x}
\end{gathered}$$
Wynika stąd, że:
$$\begin{gathered}
2a_1\sin{x}+2(2a_1x+b_1)\cos{x}+2a_2\cos{x}-2(2a_2x+b_2)\sin{x}=4xcos{x}\\
a_1=1,a_2=0,b_1=0,b_2=1
\end{gathered}$$
czyli:
$$\begin{gathered}
y_2=x^2\sin{x}+x \cos{x}
\end{gathered}$$
CORN $(14)$ ma więc postać:
$$\begin{gathered}
y=y_0+y_1+y_2=C_1 \sin{x}+C_2 \cos{x}+\frac{1}{5}e^{2x}+x^2 \sin{x}+x \cos{x}
\end{gathered}$$

---
### 4. Równanie różniczkowe Eulera rzędu drugiego:

Równanie:
$$\begin{gathered}
x^2y''+pxy'+qy=0&(17)
\end{gathered}$$
gdzie $p$ i $q$ są to dane liczby rzeczywiste, nazywamy **równaniem różniczkowym Eulera rzędu drugiego**.


Rozwiązanie równania $(17)$ sprowadzamy do rozwiązywania równania różniczkowego liniowego o stałych współczynnikach. Stosujemy podstawienie:
$$\begin{gathered}
x=e^u&(18)
\end{gathered}$$

więc funkcja niewiadoma $y(x)$ jest funkcją złożoną:
$$\begin{gathered}
y=y[x(u)]&(19)
\end{gathered}$$
zmiennej niezależnej $u$. Obliczamy:

$$\begin{gathered}
\frac{dy}{du}=\frac{dy}{dx}\frac{dx}{du}=e^u \frac{dy}{dx}\\\\
\frac{dy}{dx}=e^{-u} \frac{dy}{du}&(20)
\end{gathered}$$

a następnie:
$$\begin{gathered}
\frac{d^2y}{du^2}=\frac{d^2y}{dx^2}e^{2u}+\frac{dy}{dx}e^u=\frac{d^2y}{dx^2}e^{2u}+\frac{dy}{du}\\\\
\frac{d^2y}{dx^2}=e^{-2u} \left(\frac{d^2y}{du^2}-\frac{dy}{du}\right)&(21)
\end{gathered}$$
Wstawiając poszczególne różniczki do wzoru $(17)$ otrzymujemy równanie:
$$\begin{gathered}
y''+(p-1)y+qy=0
\end{gathered}$$
które jest równaniem liniowym o stałych współczynnikach. W całce ogólnej $(22)$ wystarczy uwzględnić $(18)$ by otrzymać całke ogólną równania $(17)$.


#### Przykład

$$\begin{gathered}
x^2y''-2xy'+6y=0
\end{gathered}$$
$p=-2, q=6$ więc otrzymujemy:
$$\begin{gathered}
y''-3y'+6y=0
\end{gathered}$$
Pierwiastkami są:
$$\begin{gathered}
r^2-3r+6=0\\
r_1=\frac{3+i\sqrt{15}}{2}, \ \ \ \ 
r_1=\frac{3-i\sqrt{15}}{2}
\end{gathered}$$

czyli całka ogólna przyjmuje postać:
$$\begin{gathered}
y=e^{\frac{3}{2}u} \left(C_1 \sin{\frac{\sqrt{15}}{2}u}+C_2 \cos{\frac{\sqrt{15}}{2}u}\right)
\end{gathered}$$

stąd uwzględniając $x=e^u$ otrzymujemy:
$$\begin{gathered}
y=x^{\frac{3}{2}} \left(C_1 \sin{\frac{\sqrt{15}}{2}\ln{x}}+C_2 \cos{\frac{\sqrt{15}}{2}\ln{x}}\right)
\end{gathered}$$


---
## zadania

### 1. Równania liniowe 

#### 1. $y''-3y'-4y=4x^2-e^x$

$$\begin{gathered}
y''-3y'-4y=0\\\\
r^2-3r-4=0\\
\Delta=9+16=25\\
r_1=\frac{3+5}{2}=4, \ \ \ \ r_2=\frac{3-5}{2}=-1
\end{gathered}$$
Zatem mamy:
$$\begin{gathered}
y=C_1 e^{4x}+C_2 e^{-x}
\end{gathered}$$
Do szczególnej przewidujemy kolejno:
Wielomian stopnia drugiego:

$$\begin{gathered}
y=Ax^2+Bx+C\\
y'=2Ax+B\\
y''=2A\\
2A-6Ax-3B-4Ax^2-4Bx-4C=4x^2\\
-4A=4\implies A=-1\\
-6A-4B=0 \implies6-4B=0 \implies B=\frac{3}{2}\\
2A-3B-4C=0 \implies  C=-\frac{13}{8}\\\\
y_2=-x^2+\frac{3}{2}x-\frac{13}{8}
\end{gathered}$$

Do drugiego podstawiamy $Ae^{x}$
$$\begin{gathered}
y=Ae^x\\
y'=Ae^x\\
y''=Ae^x\\\\
-6Ae^x=-e^x\\
A=\frac{1}{6}\\\\
y_2=\frac{1}{6}e^x
\end{gathered}$$

ostatecznie mamy wynik:
$$\begin{gathered}
y=C_1 e^{4x}+C_2 e^{-x}+-x^2+\frac{2}{3}x-1+\frac{1}{6}e^x
\end{gathered}$$
---
#### 2. $y''+y=\sin{x}-\cos{x}+x$

$$\begin{gathered}
r^2+1=0\\
r_1=i, \ \ \ r_2=-i\\\\
y=C_1 \cos{x}+C_2 \sin{x}
\end{gathered}$$

teraz mamy taki problem że $sin{x}, \cos{x}$ interferuje z naszym CORJ rozwiązaniem zatem spróbujemy podstawić przemnożone przez x przewidywanie, ponadto postać przewidywana jest taka sama dla $\sin{x}$ oraz $\cos{x}$ zatem można podstawić za całe $\sin{x}-\cos{x}$:
$$\begin{gathered}
y=Ax \sin{x}+Bx \cos{x}\\\\
y'=A \sin{x}+Ax \cos{x}+B \cos{x}-Bx \sin{x}\\\\
y''=2A \cos{x}-Ax\sin{x}-2B\sin{x}-Bx\cos{x}\\\\
y''+y=2A \cos{x}-Ax\sin{x}-2B\sin{x}-Bx\cos{x}+Ax \sin{x}+Bx \cos{x}=\\
=2A \cos{x}-2B\sin{x}=\sin{x}-\cos{x}\\\\
2A=-1 \implies A=-\frac{1}{2}\\\\
-2B=1 \implies B=-\frac{1}{2}\\\\
y_2=-\frac{1}{2}x \sin{x}-\frac{1}{2}x \cos{x}
\end{gathered}$$


I jeszcze wielomian stopnia pierwszego:

$$\begin{gathered}
y=Ax+B\\
y'=A\\
y''=0\\
A=1, B=0\\\\
y_3=x
\end{gathered}$$

ostateczne rozwiązanie:

$$\begin{gathered}
y=C_1 \cos{x}+C_2 \sin{x}-\frac{1}{2}x \sin{x}-\frac{1}{2}x \cos{x}+x
\end{gathered}$$


### Równania eulera

#### 1. $x^2y''+3xy'+5y=0$

$$\begin{gathered}
y''+2y'+5y=0\\\\
r^2+2r+5=0\\
\Delta=4-20=-16\\\\
r_1=\frac{-2+4i}{2}=-1+2i\\
r_2=\frac{-2-4i}{2}=-1-2i\\
\end{gathered}$$

robimy tak jak zawsze potem uwzględniamy $x=e^u$

$$\begin{gathered}
y=\frac{1}{x} \left(\sin{2 \ln{x}}+\cos{2 \ln{x}}\right)
\end{gathered}$$
