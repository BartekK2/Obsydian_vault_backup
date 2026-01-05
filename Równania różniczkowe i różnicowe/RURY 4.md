## Równania różniczkowe Lagrange'a i Clairauta


### 1. Wstęp

Weźmy pod uwagę równania różniczkowe postaci:
$$\begin{gathered}
y=g(x,y')&(1)
\end{gathered}$$
oraz:
$$\begin{gathered}
x=h(y,y')&(2)
\end{gathered}$$

**będziemy zapisywać $y'$ jako $p$**

### 1.1 Równanie 1

Równanie pierwsze przepiszemy jako
$$\begin{gathered}
y=g(x,p)&(3)
\end{gathered}$$

różniczkując obustronnie względem x otrzymamy:
$$\begin{gathered}
\frac{dy}{dx}=\frac{\partial g}{\partial x}+\frac{\partial g}{\partial p}\frac{dp}{dx}
\end{gathered}$$
czyli:
$$\begin{gathered}
p=\frac{\partial g}{\partial x}+\frac{\partial g}{\partial p}\frac{dp}{dx}&(4)
\end{gathered}$$
Jest to równanie różniczkowe rzędu pierwszego ze względu na funkcję $p(x)$.

##### Wytłumaczenie:

Z racji tego że równanie $(4)$ przedstawia skomplikowany mix różniczek najlepiej pokazać to na prostym przykładzie:

Równanie:
$$\begin{gathered}
y=x+(y')^2
\end{gathered}$$
Spełnia naszą postać:
$$\begin{gathered}
y=g(x,y')
\end{gathered}$$

Jeżeli zastosujemy podstawienie $p=y'$ oraz zróżniczkujemy po $x$ otrzymujemy:
$$\begin{gathered}
y=x+p^2\\
\frac{dy}{dx}=1+2p \frac{dp}{dx}\\
p=1+2p \frac{dp}{dx}\\
\frac{dp}{dx}=\frac{p-1}{2p}
\end{gathered}$$
gdzie równanie różniczkowe rzędu pierwszego oznacza:
$$\begin{gathered}
\frac{dp}{dx}=f(x,p)
\end{gathered}$$
a różne formy tego już potrafimy rozwiązać :)

---
Niech 
$$\begin{gathered}
p=\varphi(x,C)&(5)
\end{gathered}$$
gdzie $C$ jest dowolną stałą będzie całką ogólną równania $(4)$. Korzystamy z $(3)$ i $(5)$

otrzymamy:
$$\begin{gathered}
y=g(x,\varphi(x,C))&(6)
\end{gathered}$$
który przedstawia całkę ogólną równania $(3)$.

##### Wytłumaczenie 2

Załóżmy że po przekształceniach otrzymaliśmy:
$$\begin{gathered}
\frac{dp}{dx}=2x\\
dp=2xdx\\
p=x^2+C\\
p=\varphi(x,C)
\end{gathered}$$

---
Jednakże nie w każdym przypadku dostaniemy tak prosty wynik $p=\varphi(x,C)$ na przykład dla przykładu z wytłumaczenia 1 otrzymalibyśmy $2p+2\ln{|p-1|}=x+C$

co utrudnia lub uniemożliwia wyznaczenie $p$ i wrócenie do równania pierwotnego.

Wtedy należy postąpić w sposób analogiczny parametryzując $x$:

Jeśli założymy, że funkcja $p=p(x)$ ma funkcję odwrotną $x=x(p)$ to równanie $(4)$ możemy zastąpić równoważnym równaniem:
$$\begin{gathered}
\frac{dx}{dp}\left(p-\frac{\partial g}{\partial x}\right)=\frac{\partial g}{\partial p}&(7)
\end{gathered}$$
niech
$$\begin{gathered}
x=\psi(p,C)&(8)
\end{gathered}$$

będzie całką ogólną równania $(7)$. Wobec $(3)$ 
$$\begin{gathered}
y=g(\psi(p,C),p)&(9)
\end{gathered}$$
Mówimy że wzory $(8)$ i $(9)$ opisują parametrycznie całkę ogólną równania $(3)$ przy czym $p$ odgrywa rolę parametru, jeżeli wyrygujemy $p$ ze wzorów $(8)$ i $(9)$ otrzymamy całkę ogólną w postaci $(6)$.


---
##### Przykład 1

Znaleźć całkę ogólną równania:
$$\begin{gathered}
y=2y'x+(y')^2+\frac{x^2}{2}\\
y=2p(x)x+p(x)^2+\frac{x^2}{2}\\
\frac{dy}{dx}=2x\frac{dp}{dx}+2p(x)+2p(x)\frac{dp}{dx}+x\\
p(x)=2x\frac{dp}{dx}+2p(x)+2p(x)\frac{dp}{dx}+x\\
\end{gathered}$$

spróbujemy wydobyć $p(x)$ 

$$\begin{gathered}
\frac{dp}{dx}(2x+2p(x))=-x-p(x)\\
dp=-\frac{1}{2}dx\\
p=-\frac{x}{2}+C\\
y'=-\frac{x}{2}+C\\

\end{gathered}$$
otrzymaliśmy postać $p=\varphi(x,C)$

$$\begin{gathered}
y=2(-\frac{x}{2}+C)x+(-\frac{x}{2}+C)^2+\frac{x^2}{2}\\
y=-x+2xC+\frac{x^2}{4}-Cx+C^2+\frac{x^2}{2}\\
y=\frac{3x^2}{4}-x+Cx+C^2
\end{gathered}$$

ogólnie tutaj dzielilśmy przez $x+p(x)$ czyli założyliśmy że to nie jest $0$ a taki osobliwy przypadek też wypadałoby sprawdzić
$$\begin{gathered}
p(x)=x\\
y=2x^2+\frac{3x^2}{2}\\
\end{gathered}$$

### Równanie $(2)$

Równanie 2 rozwiązuje się podobnie jak równanie $(1)$. Jeżeli $y'=p$ to $\frac{dx}{y}=\frac{1}{p}$, przy czym $p=p(y)$ zgodnie z $(2)$
$$\begin{gathered}
x=h(y',p)&(14)
\end{gathered}$$
Różniczkując powyższe obustronnie względem $y$ otrzymamy:
$$\begin{gathered}
\frac{1}{p}=\frac{\partial h}{\partial y}+\frac{\partial h}{\partial p}\frac{dp}{dy}&(15)
\end{gathered}$$

Jest to równanie różniczkowe rzędu pierwszego ze wzgledu na funkcje $p(y)$ 
Niech:
$$\begin{gathered}
p=\phi(y,C)&(16)
\end{gathered}$$
gdzie $C$ jest dowolną stłą, będzie całką ogólną równania $(15)$. Korzystając z $(14)$ i $(16)$ otrzymamy wzór:

$$\begin{gathered}
x=h(y,\phi(y,C))
\end{gathered}$$
który przedstawia całke ogólną równania $(14)$.

###### Przykład

$$\begin{gathered}
x=(y')^2-(y')+10\\\\
x=p^2-p+10\\
\frac{1}{p}=2p \frac{dp}{dy}-\frac{dp}{dy}\\
dy=(2p^2-p)dp\\
y=\frac{2}{3}p^3-\frac{1}{2}p^2+C
\end{gathered}$$

### Równanie różniczkowe Lagrange'a

Równanie 
$$\begin{gathered}
y=\varphi(y')x+\psi(y')&(22)
\end{gathered}
$$
nazywamy **równaniem różniczkowym Lagrange'a**. Równanie to jest postaci $(1)$
$$\begin{gathered}
y=\varphi(p)x+\psi(p)
\end{gathered}$$
Różniczkując powyższe obustronnie względem $x$ otrzymujemy:
$$\begin{gathered}
p=\varphi(p)+\varphi'(p)x\frac{dp}{dx}+\psi'(p)\frac{dp}{dx}
\end{gathered}$$
Można teraz to przekształcić w:
$$\begin{gathered}
p-\varphi(p)=\varphi'(p)x\frac{dp}{dx}+\psi'(p)\frac{dp}{dx}\\\\
\frac{dx}{dp}=\frac{\varphi'(p)x+\psi'(p)}{p-\varphi(p)}\\\\
\frac{dx}{dp}-\frac{\varphi'(p)}{p-\varphi(p)}x=\frac{\psi'(p)}{p-\varphi(p)}\\\\
\end{gathered}$$

z funkcją niewiadomą $x(p)$ które potrafimy zcałkować bo to to samo co:
$$\begin{gathered}
\frac{dy}{dx}+f(x)y=g(x)
\end{gathered}$$

Niech $x=\omega(p,C)$
będzie całką ogólną tego równania. Zgodnie z $(23)$
$$\begin{gathered}
y=\varphi(p)\omega(p,C)+\psi(p)
\end{gathered}$$

I mamy opis parametryczny.

---
###### Przykład

$$\begin{gathered}
y=(y')^2x+\frac{1}{y'}\\
y=p^2x+\frac{1}{p}\\
p=2px \frac{dp}{dx}+p^2-\frac{1}{p^2}\frac{dp}{dx}\\\\
p-p^2=(2px-\frac{1}{p^2})\frac{dp}{dx}\\
\frac{dx}{dp}=\frac{2px-\frac{1}{p^2}}{p-p^2}\\\\
\frac{dx}{dp}-\frac{2p}{p-p^2}x=-\frac{1}{p^3-p^4}
\end{gathered}$$

Rozwiązujemy jak te co znamy:

$$\begin{gathered}
\frac{dx}{dp}=\frac{2p}{p-p^2}x\\\\
\frac{dx}{x}=\frac{2p}{p-p^2}dp\\\\
\ln{|x|}=\int{\frac{2p}{p-p^2}dp}=\int{\frac{2}{1-p}dp}=-2\ln{|1-p|}+C\\\\
x=\frac{C(p)}{(1-p)^2}\\\\
\frac{dx}{dp}=2C(p)\frac{1}{(1-p)^3}+C'(p)\frac{1}{(1-p)^2}
\end{gathered}$$

Znajdujemy $C(p)$:

$$\begin{gathered}
2C(p)\frac{1}{(1-p)^3}+C'(p)\frac{1}{(1-p)^2}-\frac{2C(p)}{(1-p)^3}=-\frac{1}{p^3-p^4}\\\\
C'(p)=-\frac{1}{p^3(1-p)}\cdot (1-p)^2=-\frac{1-p}{p^3}\\\\
C(p)=\frac{1}{2p^2}-\frac{1}{p}+C_1\\\\
x=\frac{\frac{1}{2p^2}-\frac{1}{p}+C_1}{(1-p)^2}\\\\
\downarrow\\\\
y=p^2x+\frac{1}{p}\\\\
y(p)=\frac{\frac{1}{2}-p+C_1p^2}{(1-p)^2}+\frac{1}{p}
\end{gathered}
$$

---
### Równanie różniczkowe Clairauta

Równanie:

$$\begin{gathered}
y=y'x+\psi(y')
\end{gathered}$$

nazywamy równaniem różniczkowym clairauta. Równanie to jest szczególnym przypadkiem równania Lagrange'a.
$$\begin{gathered}
y=px+\psi(p)\\
p=p+x \frac{dp}{dx}+\psi'(p) \frac{dp}{dx}
\end{gathered}
$$

czyli:
$$\begin{gathered}
\frac{dp}{dx}[x+\psi'(p)]=0
\end{gathered}
$$
skąd:
$$\begin{gathered}
\frac{dp}{dx}=0
\end{gathered}
$$
co daje $p=C$
zatem:
$$\begin{gathered}
y=Cx+\psi(C)
\end{gathered}$$
lub
$$\begin{gathered}
x=-\psi'(p)\\\\
\downarrow\\\\
y=px+\psi(p)\\\\
y=-\psi'(p)p+\psi(p)
\end{gathered}
$$

###### Przykład:

$$\begin{gathered}
y=xy'+\frac{1}{2y'}\\
y=xp+\frac{1}{2p}\\
p=p+x\frac{dp}{dx}-\frac{1}{2p^2}\frac{dp}{dx}\\
\frac{dp}{dx} \left(x-\frac{1}{2p^2}\right)=0
\end{gathered}
$$

albo $p=C$
$$\begin{gathered}
y=Cx+\frac{C}{2}
\end{gathered}$$
albo:
$$\begin{gathered}
x=\frac{1}{2p^2}\\\\
\downarrow\\
y=xy'+\frac{1}{2y'}\\\\
y=\frac{1}{2p}+\frac{1}{2p}=\frac{1}{p}
\end{gathered}$$


## Zadania:

### Na zajęcia:

#### 1. $y=3xy'+e^{-\sqrt{y'}}$

$$\begin{gathered}
y=3xy'+e^{-\sqrt{y'}}\\
y=3xp+e^{-\sqrt{p}}\\
p=3p+3x \frac{dp}{dx}-\frac{e^{-\sqrt{p}}}{2 \sqrt{p}}\frac{dp}{dx}\\\\
-2p=3x \frac{dp}{dx}-\frac{e^{-\sqrt{p}}}{2 \sqrt{p}}\frac{dp}{dx}\\\\
\frac{dx}{dp}=-\frac{3}{2p}x-\frac{e^{-\sqrt{p}}}{4p^{\frac{3}{2}}}
\end{gathered}$$

rozwiązujemy:
$$\begin{gathered}
\frac{dx}{x}=-\frac{3dp}{2p}\\
\ln{x}=-\frac{3}{2}\ln{|p|}+C\\
x=C(p)\frac{1}{p^{\frac{3}{2}}}\\
\frac{dx}{dp}=C'(p)\frac{1}{p^{\frac{3}{2}}}-\frac{3}{2}p^{-\frac{5}{2}}C(p)
\end{gathered}$$

podstawiamy:
$$\begin{gathered}
C'(p)\frac{1}{p^{\frac{3}{2}}}=-\frac{e^{-\sqrt{p}}}{4p^{\frac{3}{2}}}\\
C'(p))=-e^{-\sqrt{p}}=\dots\\\\
\int{e^{-\sqrt{p}}dp}=\begin{vmatrix}
t=-\sqrt{p}\\
dt=-\frac{1}{2\sqrt{p}}dp\\
2tdt=dp
\end{vmatrix}=2t\int{te^{t}dt}=e^tt-e^t=-\sqrt{p}e^{-\sqrt{p}}-e^{-\sqrt{p}}+C\\\\
C(p)=-\sqrt{p}e^{-\sqrt{p}}-e^{-\sqrt{p}}+C\\\\
x=(-\sqrt{p}e^{-\sqrt{p}}-e^{-\sqrt{p}}+C)\frac{1}{p^{\frac{3}{2}}}
\end{gathered}$$

i to ostatnie podłożyć pod y i git

---
#### 2. $y=\left(y'+\frac{1}{\cos{y'}}\right)x+\sin^3{y'}$

$$\begin{gathered}
y=(p+\frac{1}{\cos{p}})x+\sin^3{p}\\
p=p+\frac{1}{\cos{p}}+(1+\frac{\sin{p}}{\cos^2{p}})x \frac{dp}{dx}+3\sin^2{p}\cos{p} \frac{dp}{dx}\\
-\frac{1}{\cos{p}}=\frac{dp}{dx} \left((1+\frac{\sin{p}}{\cos^2{p}})x +3\sin^2{p}\cos{p} \right)\\
\frac{dx}{dp}=-\cos{p}\left((1+\frac{\sin{p}}{\cos^2{p}})x +3\sin^2{p}\cos{p} \right)\\

\frac{dx}{dp}=(-\cos{p}-\frac{\sin{p}}{\cos{p}})x -3\sin^2{p}\cos^2{p} \\
\end{gathered}$$

Rozwiązujemy jak zwykłe te liniowe:
$$\begin{gathered}
\ln{x}=-\sin{p}+\ln{\cos{p}}+C\\\\
x=e^{-\sin{p}+\ln{\cos{p}}+C}=(e^{-\sin{p}}\cdot \cos{p})\cdot C(p)\\
\frac{dx}{dp}=C(p)\cdot (-e^{-\sin{p}}\cos^2{p}-e^{-\sin{p}}\cdot  \sin{p})+C'(p)e^{-\sin{p}}\cdot \cos{p}\\\\\
\frac{dx}{dp}+(\cos{p}+\frac{\sin{p}}{\cos{p}})x =-3\sin^2{p}\cos^2{p} \\
C(p)\cdot (-e^{-\sin{p}}\cos^2{p}-e^{-\sin{p}}\cdot  \sin{p})+C'(p)e^{-\sin{p}}\cdot \cos{p}+\\+(\cos{p}+\frac{\sin{p}}{\cos{p}})(e^{-\sin{p}}\cdot \cos{p})\cdot C(p) =-3\sin^2{p}\cos^2{p} \\\\
C'(p)e^{-\sin{p}}\cos{p}=-3\sin^2\cos^2{p}\\
C'(p)=\frac{-3\sin^2\cos{p}}{e^{-\sin{p}}}=\dots\\\\
\int{\frac{-3\sin^2\cos{p}}{e^{-\sin{p}}} dp}=\begin{vmatrix}
t=-\sin{p}\\
dt=-\cos{p}dp
\end{vmatrix}=\int{\frac{3t^2}{e^t} dt}=\dots\\\\
C(p)=-\dfrac{3\,\left({-\sin{p}}^{2}+2\,-\sin{p}+2\right)}{{e}^{-\sin{p}}}+C
\end{gathered}$$


nie chce mi sie dalej, wracamy z tym do x potem x podstawiamy pod y i mamy sparametryzowane ładnie


---
