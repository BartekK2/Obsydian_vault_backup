
## Równanie różniczkowe Bernoulliego 

### Równanie Bernoulliego

Równanie różniczkowe pierwszego rzędu
$$\begin{gathered}
\frac{dy}{dx}=p(x)y+q(x)y^r&(1)
\end{gathered}$$
nazywamy równaniem różniczkowym Bernoulliego.
gdy $r=0$ powyższe równanie jest równaniem liniowym niejednorodnym, gdy $r=1$ równaniem liniowym jednorodnym. Zakładamy więc że $r \neq 0$ i $r \neq 1$ . Równanie to można sprowadzić do równania liniowego, podstawiając
$$\begin{gathered}
z=y^{1-r}&(2)
\end{gathered}$$
Różniczkując $z$ otrzymujemy
$$\begin{gathered}
\frac{dz}{dx}=(1-r)y^{-r}\frac{dy}{dx}&(3)
\end{gathered}$$
Mnożąc obustronnie równanie $(1)$ przez $(1-r)y^{-r}$ otrzymujemy
$$\begin{gathered}
(1-r)y^{-r}\frac{dy}{dx}=(1-r)p(x)y^{1-r}+(1-r)q(x)
\end{gathered}$$

stąd zgodnie z $(2)$ i $(3)$ 
$$\begin{gathered}
\frac{dz}{dx}=(1-r)p(x)z+(1-r)q(x)
\end{gathered}$$

Jest to równanie różniczkowe liniowe.

###### Przykład 1

Znaleźć całke ogólną równania
$$\begin{gathered}
\frac{dy}{dx}=-\frac{y}{x}+\frac{\ln{x}}{x}y^2\\\\
z=y^{1-2}=y^{-1}\\
\frac{dz}{dx}=-y^{-2}\frac{dy}{dx}\\\\
\frac{dz}{dx}=\frac{1}{xy}-\frac{\ln{x}}{x}\\
\frac{dz}{dx}=\frac{1}{x}z-\frac{\ln{x}}{x}\\
\frac{dz}{dx}-\frac{1}{x}z=-\frac{\ln{x}}{x}\\
\end{gathered}$$

Mamy równanie rózniczkowe liniowe:
$$\begin{gathered}
\frac{dz}{dx}=\frac{1}{x}z\\
\frac{dz}{z}=\frac{dx}{x}\\
\ln{z}=\ln{x}+C\\
z=C(x)x\\
\frac{dz}{dx}=C'(x)x+C(x)\\
C'(x)x+C(x)-C(x)=-\frac{\ln{x}}{x}\\
C'(x)=-\frac{\ln{x}}{x^2}\\
\end{gathered}$$
Policzmy całke:
$$\begin{gathered}
-\int{\frac{\ln{x}}{x^2}dx}=\begin{vmatrix}
t=\ln{x}&v'=\frac{1}{x^2}\\
t'=\frac{1}{x}&v=-\frac{1}{x}
\end{vmatrix}=\\
=\frac{\ln{x}}{x}+\int{-\frac{1}{x^2}}=\frac{\ln{x}}{x}+\frac{1}{x}+C_1
\end{gathered}$$
$$\begin{gathered}
C(x)=\frac{\ln{x}}{x}+\frac{1}{x}+C_1\\
z=\ln{x}+1+C_1x\\
-\frac{1}{y}=\ln{x}+1+C_1x\\
y=-\frac{1}{\ln{x}+1+C_1x}
\end{gathered}$$
---
### Równanie Riccatiego

Można wykazać, że jeżeli $y_1(x)$ jest całką szczególnią równania Riccatiego:
$$\begin{gathered}
\frac{dy}{dx}=a(x)y^2+b(x)y+c(x)
\end{gathered}$$
to można je sprowadzić do równania Bernoulliego podstawiając $z(x)=y(x)-y_1(x)$

**Obczaj potem o co chodzi**

---
## Równanie różniczkowe zupełne 

Równanie różniczkowe rzędu pierwszego
$$\begin{gathered}
\frac{dy}{dx}=-\frac{P(x,y)}{Q(x,y)}&(7)
\end{gathered}$$
można zapisać w równoważnej postaci
$$\begin{gathered}
P(x,y)dx+Q(x,y)dy=0&(8)
\end{gathered}$$
Mówimy że powyższe równanie jest **różniczkowym zupełnym** gdy istnieje funkcja $u(x,y)$ której różniczka zupełna równa się lewej stronie tego równania, a więc gdy:
$$\begin{gathered}
\frac{\partial u}{\partial x}=P(x, y)&i& \frac{\partial u}{\partial y}=Q(x,y)&(9)
\end{gathered}$$
Na przykład równanie $2xdx+3y^2dy=0$ jest zupełne, ponieważ lewa strona tego równania jest różniczką zupełną funkcji $u=x^2+y^3$. 

Wiadomo że istnieja funkcja dla której są spełnione równości $(9)$ wtedy i tylko wtedy gdy spełniony jest warunek:

$$\begin{gathered}
\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}&(10)
\end{gathered}$$
Wtedy jedną z funkcji, dla ktorych zachodzą równości $(9)$ jest funkcja $u(x,y)$ wyrażona za pomocą wzoru:

$$\begin{gathered}
u(x,y)=\int^{x}_{x_0}P(t,y)dt+\int^{y}_{y_0}Q(x_0,t)dt
\end{gathered}$$
Przypuśćmy że funkcja $y(x)$ spełnia równanie $(8)$ czyli:
$$\begin{gathered}
P(x,y(x))+Q(x,y(x))y'=0
\end{gathered}$$

Stąd, zgodnie z $(9)$ otrzymujemy:
$$\begin{gathered}
\frac{\partial u(x,y(x))}{\partial x}+\frac{\partial u(x,y(x))}{\partial y}y'=0
\end{gathered}$$
czyli:
$$\begin{gathered}
\frac{d}{dx}u(x,y(x))=0
\end{gathered}$$
i wobec tego:
$$\begin{gathered}
u(x,y(x))=C&(12)
\end{gathered}$$

gdzie $C$ jest dowolną stałą.


**Dopisz twierdzenie**


###### Przykład 1

Znajdź całke ogólną równania:

$$\begin{gathered}
(x^3+xy^2+1)dx+(x^2y+y^3)dy=0\\
\end{gathered}$$
Sprawdzamy warunek tego czy to jest równanie różniczkowe zupełne:

$$\begin{gathered}
P(x,y)=x^3+xy^2+1\\
Q(x,y)=x^2y+y^3\\\\
\frac{\partial P}{\partial y}=2xy\\
\frac{\partial Q}{\partial x}=2xy\\
\\
\frac{\partial P}{\partial y}=
\frac{\partial Q}{\partial x}\\
\end{gathered}$$

warunek jest spełniony a co za tym idzie możemy skorzystać ze wzoru na $u(x,y)$

$$\begin{gathered}
u(x,y)=\int^{x}_{x_0}P(t,y)dt+\int^{y}_{y_0}Q(x_0,t)dt
\end{gathered}$$
Policzmy:
$$\begin{gathered}
u(x,y)=\frac{x^4}{4}+\frac{x^2y^2}{2}+x+\frac{x^2y^2}{2}+\frac{y^4}{4}+C_1
\end{gathered}$$

Zatem ostatecznym równaniem które to spełnia to:

$$\begin{gathered}
\frac{x^4}{4}+\frac{x^2y^2}{2}+x+\frac{x^2y^2}{2}+\frac{y^4}{4}=C
\end{gathered}$$

---
### Czynnik całkujący

Przypuśćmy, że równanie $(8)$ nie jest równaniem różniczkowym zupełnym. Weźmy pod uwagę funkcję $\mu(x,y)$ Rozważmy równanie:

$$\begin{gathered}
\mu(x,y)P(x,y)dx+\mu(x,y)Q(x,y)dy=0&(15)
\end{gathered}$$
będące wynikiem obustronnego pomnożenia równania $(8)$ przez $\mu(x,y)$. Mówimy że funkcja $\mu(x,y)$ jest **czynnikiem całkującym** równania $(8)$, gdy równanie $(15)$ jest równaniem różniczkowym zupełnym, czyli:
$$\begin{gathered}
\frac{\partial (\mu P)}{\partial y}=\frac{\partial (\mu Q)}{\partial x}
\end{gathered}$$
lub inaczej:
$$\begin{gathered}
P \frac{\partial \mu}{\partial y}-Q \frac{\partial \mu}{\partial x}=\mu \frac{\partial Q}{\partial y}-\mu \frac{\partial P}{\partial x}&(16)
\end{gathered}$$

###### Przykład 1

Równanie:
$$\begin{gathered}
(3x+2y+y^2)dx+(x+4xy+5y^2)dy=0&(17)
\end{gathered}
$$
nie jest równaniem różniczkowym zupełnym ponieważ:
$$\begin{gathered}
\frac{\partial P}{dy}=2+2y&i&\frac{\partial Q}{dx}=1+4y
\end{gathered}$$
Mnożąc równanie $(17)$ obustronnie przez funkcje $\mu=x+y^2$ otrzymamy:
$$\begin{gathered}
(x+y^2)(3x+2y+y^2)dx+(x+y^2)(x+4xy+5y^2)dy=0&(18)
\end{gathered}
$$

Jest to równanie różniczkowe zupełne, wię funkcja $\mu=x+y^2$ jest czynnikiem całkującym równania $(17)$

Rozwiązanie:

$$\begin{gathered}
\frac{\partial u}{\partial x}=P(x,y)=3x^2+2xy+4xy^2+2y^3+y^4
\end{gathered}$$

po scałkowaniu otrzymamy:
$$\begin{gathered}
u(x,y)=x^3+x^2y+2x^2y^2+2xy^3+xy^4+C_1(y)
\end{gathered}$$
$$\begin{gathered}
\frac{\partial u}{\partial y}=Q(x,y)=x^2+4x^2y+6xy^2+4xy^3+C'(y)=\\
=x^2+4x^2y+6xy^2+4xy^3+5y^4
\end{gathered}$$

czyli $C'(y)=5y^4$ stąd $C(y)=y^5+C_2$

Ostatecznie całką ogólną równania $(17)$ jest:
$$\begin{gathered}
x^3+x^2y+2x^2y^2+2xy^3+xy^4+y^5=C
\end{gathered}$$

Poszukiwanie funkcji $\mu(x,y)$ na ogół nie jest łatwe. Zadanie to upraszcza się, gdy funkcja $\mu(x,y)$ jest funkcją tylko jednej zmiennej, czyli gdy $\mu=\mu(x)$ lub $\mu=\mu(y)$

Równanie $(16)$ można zapisać w postaci już idąc na skróty:

$$\begin{gathered}
\mu(x)=e^{\int{\frac{1}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)dx}}
\end{gathered}$$
lub alternatywnie

$$\begin{gathered}
\mu(y)=e^{\int{\frac{1}{P}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dy}}
\end{gathered}$$
jednakże to co siedzi pod całkami musi być zależne jedynie od swoich zmiennych x/y.

###### Przykład 2 (samodzielnie)
$$\begin{gathered}
(x^2y-y \ln{y})dx+(\frac{2}{3}x^3-2x \ln{y}-x)dy=0
\end{gathered}$$
$$\begin{gathered}
\frac{\partial P}{\partial y}=x^2-\ln{y}-1\\
\frac{\partial Q}{\partial x}=2x^2-2\ln{y}-1\\
\end{gathered}$$

Różne więc trzeba wprowadzic czynnik całkujący:
$$\begin{gathered}
\frac{x^2-\ln{y}}{x^2y-y \ln{y}}=\frac{1}{y}\implies \mu(y)=e^{\int{\frac{1}{y}dy}}=y
\end{gathered}$$
Zatem otrzymujemy:
$$\begin{gathered}
(x^2y^2-y^2 \ln{y})dx+(\frac{2}{3}x^3y-2xy \ln{y}-xy)dy=0
\end{gathered}$$
I liczymy:
$$\begin{gathered}
\frac{\partial u}{\partial x}=P(x,y)=x^2y^2-y^2 \ln{y}\\
u(x,y)=\frac{x^3y^2}{3}-xy^2 \ln{y}+C(y)\\\\
\frac{\partial u}{\partial y}=\frac{2}{3}x^3y-2xy \ln{y}-xy+C'(y)\\
\text{brak wyrazów zależnych tylko od y}\\
\text{więc }C(y)=C\\
\text{ostatecznie:}\\
\frac{x^3y^2}{3}-xy^2 \ln{y}=C
\end{gathered}$$




---
## zadania

### do kolokwium przykłady

#### 1. $y'=\frac{y}{x}+\frac{y^2}{\ln{x}}$

$$\begin{gathered}
z=y^{1-2}=y^{-1}\\
\frac{dz}{dy}=-y^{-2}\\
\frac{dz}{dx}=-y^{-2}\frac{dy}{dx}\\
\end{gathered}$$

podstawiamy:
$$\begin{gathered}
y'=\frac{y}{x}+\frac{y^2}{\ln{x}}\\
\downarrow\\
-y^{-2}\frac{dy}{dx}=-y^{-2}(\frac{y}{x}+\frac{y^2}{\ln{x}})\\
\downarrow\\
\frac{dz}{dx}=-\frac{1}{xy}-\frac{1}{\ln{x}}\\
\frac{dz}{dx}=-\frac{1}{x}z-\frac{1}{\ln{x}}\\
\frac{dz}{dx}+\frac{1}{x}z=-\frac{1}{\ln{x}}\\\\
\frac{dz}{dx}+p(x)z=f(x)
\end{gathered}$$

teraz mamy to równanie jakieś tam z rur 2

$$\begin{gathered}
\frac{dz}{dx}=-\frac{1}{x}z\\
\frac{dz}{z}=-\frac{dx}{x}\\
\ln{|z|}=-\ln{|x|}+C\\
z=C(x)\frac{1}{x}\\
\frac{dz}{dx}=\frac{C'(x)}{x}-\frac{C(x)}{x^2}\\
\downarrow\\
\frac{C'(x)}{x}-\frac{C(x)}{x^2}+\frac{C(x)}{x^2}=-\frac{1}{\ln{x}}\\\\
C'(x)=-\frac{x}{\ln{x}}
\end{gathered}$$
$C(x)$ sie nie da policzyć xd

#### 3. $y'=e^xy+\frac{e^{e^x}e^x}{y}$

$$\begin{gathered}
r=-1\\
z=y^{1-(-1)}=y^2\\
\frac{dz}{dx}=2y \frac{dy}{dx}\\
\frac{dz}{dx}=2e^xz+2e^{e^x}e^x
\end{gathered}$$

to jest to równanie z drugich rur 

$$\begin{gathered}
\frac{dz}{dx}=2e^xz\\
\ln{z}=2e^x+C_1\\
z=e^{2e^x+C_1}=e^{2e^x}\cdot C_2=C(x)e^{2e^x}\\
\frac{dz}{dx}=C'(x)e^{2e^x}+C(x)e^{2e^x}\cdot 2e^x\\
\downarrow\\
\frac{dz}{dx}=2e^xz+2e^{e^x}e^x\\
C'(x)e^{2e^x}+C(x)e^{2e^x}\cdot 2e^x=2e^xC(x)e^{2e^x}+2e^{e^x}e^x\\
C'(x)=\frac{2e^{e^x}e^x}{e^{2e^x}}=\frac{2e^x}{e^{e^x}}
\end{gathered}$$
liczymy całeczke
$$\begin{gathered}
\int{\frac{e^x}{e^{e^x}}dx}=\begin{vmatrix}
t=e^x\\
dt=e^xdx
\end{vmatrix}=\int{\frac{dt}{e^t}}=\begin{vmatrix}
u=-t\\
du=-dt
\end{vmatrix}=-\int{e^udu}=-\frac{1}{e^{e^x}}+C
\end{gathered}$$
zatem:
$$\begin{gathered}
C(x)=-\frac{2}{e^{e^x}}+C\\\\
z=(-\frac{2}{e^{e^x}}+C)e^{2e^x}\\
y^2=-2e^{e^x}+Ce^{2e^x}\\
y=\dots
\end{gathered}$$

---
#### 9. $\frac{x dx}{\sqrt{x^2+y^2}}+\frac{y dy}{\sqrt{x^2+y^2}}=0$

Zrobimy czynnik całkujacy $\sqrt{x^2+y^2}$ bo widać że zadziała, nawet jeśli nie wiem czy teraz działa.

$$\begin{gathered}
xdx+ydy=0\\
\frac{\partial P}{\partial y}=0=\frac{\partial Q}{\partial y}\\\\
u=\frac{x^2}{2}+C(y)\\
\frac{\partial u}{\partial y}=y=C'(y)\\
C(y)=\frac{y^2}{2}+C\\
\frac{x^2+y^2}{2}=C
\end{gathered}$$

---
#### 12. $(3xy^2+2y^3)dx+(2x^2y+3xy^2)dy=0$

$$\begin{gathered}
\frac{\partial P}{\partial y}=6xy+6y^2\\
\frac{\partial Q}{\partial x}=4xy+3y^2
\end{gathered}$$
różne więc wrzucimy czynnik całkujący, spróbujemy najpierw podstawowe $u(x),u(y)$
$$\begin{gathered}
u(x)=\frac{2xy+3y^2}{2x^2y+3xy^2}=\frac{1}{x}\implies u(x)=e^{\int{\frac{1}{x}dx}}=x
\end{gathered}$$
nowe równanie:
$$\begin{gathered}
(3x^2y^2+2xy^3)dx+(2x^3y+3x^2y^2)dy=0\\\\
\frac{\partial u}{\partial x}=3x^2y^2+2xy^3\\\\
u=x^3y^2+x^2y^3+C(y)\\\\
\frac{\partial u}{\partial y}=2x^3y+3x^2y^2+C'(y)\\\\
C(y)=C\\\
x^3y^2+x^2y^3=C
\end{gathered}$$

---
