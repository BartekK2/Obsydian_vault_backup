
## Równania różniczkowe liniowe rzędu pierwszego

### 1. Wiadomości wstępne

Równanie:
$$\begin{gathered}
\frac{dy}{dx}+p(x)y=f(x)&(1)
\end{gathered}$$
gdzie $p(x)$ i $f(x)$ są to funkcje dane, ciągłe w pewnym przedziale $(a,b)$ nazywamy **równaniem różniczkowym liniowym rzędu pierwszego**.

Równanie $(1)$ nazywamy **jednorodnym** $(RJ)$ jeżeli $f(x)$ jest tożsamościowo równa zeru w rozważanym przedziale, **niejednorodnym** zaś $(RN)$ w przypadku przeciwnym.

**Metoda rozwiązywania $RN$ wiedzie poprzez rozwiązanie $RJ$ które otrzymujemy zastępując funkcje $f(x)$ funkcją równą zeru.**

$$\begin{gathered}
\frac{dy}{dx}+p(x)y=0&(2)
\end{gathered}$$
Równanie $(2)$ jest **równaniem o zmiennych rozdzieloncyh**. Zakładając, że $y(x)\neq 0$ mamy:
$$\begin{gathered}
\frac{dy}{y}=-p(x)dx&(3)
\end{gathered}
$$
i całkujemy
$$\begin{gathered}
\ln{|y|}=-\int{p(x)dx}+\ln{C}&(4)
\end{gathered}
$$

stąd 
$$\begin{gathered}
y=Ce^{-\int{p(x)dx}}&(5)
\end{gathered}$$
Jeżeli mamy rozwiązanie $RJ$, to rozwiązanie ogólne $RN$ uzyskujemy za pomocą jednej z dwóch metod:
- **metody uzmienniania stałej**
- **metody przewidywań**

---
#### 1.1 Metoda uzmienniania stałej

Metoda ta polega na tym, że zastępujemy we wzorze $(5)$ stałą $C$ nieznaną funkcją $C(x)$ a następnie staramy się dobrać $C(x)$, aby wzór:
$$\begin{gathered}
y(x)=C(x)e^{-\int{p(x)dx}}&(6)
\end{gathered}$$
przedstawiał rozwiązanie ogólne $RN$.

z $(6)$ mamy 
$$\begin{gathered}
\frac{dy}{dx}=C'(x)e^{-\int{p(x)dx}}-C(x)p(x)e^{-\int{p(x)dx}}&(7)
\end{gathered}$$

Po podstawieniu $(6)$ oraz $(7)$ do $RN$ odpowiednio w miejsce $y$ i $\frac{dy}{dx}$ i redukcji otrzymamy:
$$\begin{gathered}
C'(x)=f(x)e^{\int{p(x)dx}}&(8)
\end{gathered}$$
całkując dostajemy:
$$\begin{gathered}
C(x)=\int{f(x)e^{\int{p(x)dx}}dx}+C_1&(9)
\end{gathered}$$
wobec $(6)$ mamy zatem:
$$\begin{gathered}
y(x)=C_1e^{-\int{p(x)dx}}+e^{-\int{p(x)dx}}\int{f(x)e^{\int{p(x)dx}}dx}&(10)
\end{gathered}$$

Oznaczając drugi składnk po prawej stronie wzoru $(10)$ symbolem $y_1(x)$ oraz zakładając $P'(x)=p(x)$ mamy:
$$\begin{gathered}
y(x)=C_1e^{-P(x)}dx+y_1(x)&(11)
\end{gathered}$$
Wzór $(11)$ przedstawia całkę ogólną $RN$ równania $(1)$.

###### 1.2 Przykład 1

$$\begin{gathered}
\frac{dy}{dx}-y \cot{x}=\sin^3{x}\\\\
\text{Zaczynamy od jednorodnego:}\\
\frac{dy}{dx}=y \cot{x}\\
\frac{dy}{y}=\cot{x}dx\\
\ln{|y|}=\int{\frac{\cos}{\sin}dx}=\ln{|\sin{x}|}+C_1\\\\
y=C\sin{x}\\\\
\text{zastępujemy stałą C funkcją C(x)}\\\\
y=C(x)\sin{x}
\end{gathered}$$
$$\begin{gathered}
\frac{dy}{dx}=C'(x)\sin{x}+C(x)\cos{x}\\\\
\text{Mamy }y, \frac{dy}{dx} \text{ - zatem podstawmy do początkowego równania}\\\\
\frac{dy}{dx}-y \cot{x}=\sin^3{x}\\\\
\downarrow\\\\
C'(x)\sin{x}+C(x)\cos{x}-C(x)\sin{x} \cot{x}=\sin^3{x}\\\\
\text{tutaj te rzeczy z }C(x)\text{ się znoszą}\\\\
C'(x)\sin{x}=\sin^3{x}\\
C'(x)=\sin^2{x}\\
C(x)=\int{\sin^2{x}dx}=(1)\\\\\
(1):\\\\
\int{\sin^2{x}dx}=\int{\frac{1-\cos(2x)}{2}dx}=\frac{x}{2}-\frac{1}{2}\int{cos{2x}dx}=\begin{vmatrix}
t=2x\\
dt=2 dx
\end{vmatrix}=\\
=\frac{x}{2}-\frac{1}{4}\sin{2x}+C_1
\end{gathered}$$

Zatem naszym $C(x)$
$$\begin{gathered}
C(x)=\frac{x}{2}-\frac{1}{4}\sin{2x}+C_1\\\\
\text{ostatecznie podstawiamy pod y}:\\\\
y=C(x)\sin{x}\\
y=\sin{x}\left(\frac{x}{2}-\frac{1}{4}\sin{2x}+C_1\right)\\
\text{Musimy uwzględnić warunek początkowy:   } (y(-\frac{\pi}{2})=1)\\\\
1=-1\left(-\frac{\pi}{4}+C_1\right)\implies C_1=\frac{\pi}{4}-1\\\\
y=\sin{x}\left(\frac{x}{2}-\frac{1}{4}\sin{2x}+\frac{\pi}{4}-1\right)\\
\end{gathered}
$$
###### 1.3 Przykład 2

Znajdź rozwiązanie równania:
$$\begin{gathered}
\frac{dy}{dx}=\frac{1}{x \cos{y}+\sin{2y}}
\end{gathered}$$
Tutaj należy skorzystać z **twierdzenia o pochodnej funkcji odwrotnej**, z racji tego że tutaj nie mamy tego co w tym rozdziale dla $y(x)$ a dla $x(y)$.
$$\begin{gathered}
(f^{-1})'=\frac{1}{f'}
\end{gathered}$$

$$\begin{gathered}
\frac{dx}{dy}=x \cos{y}+\sin{2y}\\
\frac{dx}{dy}-x \cos{y}=\sin{2y}\\
\end{gathered}$$

Ponownie zaczynamy od jednorodnego:
$$\begin{gathered}
\frac{dx}{dy}=x \cos{y}\\
\frac{dx}{x}=\cos{y}dy\\
\ln{|x|}=\sin{y}+C\\
x=C_1e^{\sin{y}}
\end{gathered}$$
I podstawiamy $C(y)$
$$\begin{gathered}
x=C(y)e^{\sin{y}}\\
\frac{dx}{dy}=C'(y)e^{\sin{y}}+C(y)e^{\sin{y}}\cos{y}\\\\
\end{gathered}$$
Mamy zarówno $x(y)$ jak i $\frac{dx}{dy}$ zatem podstawmy do równania początkowego:
$$\begin{gathered}
C'(y)e^{\sin{y}}+C(y)e^{\sin{y}}\cos{y}-C(y)e^{\sin{y}} \cos{y}=\sin{2y}\\\\
C'(y)e^{\sin{y}}=\sin{2y}\\
C'(y)=\frac{\sin{2y}}{e^{\sin{y}}}\\\\
C(y)=\int{R dy}=\begin{vmatrix}
t=\sin{y}\\
dt=\cos{y}dy
\end{vmatrix}=\int{\frac{2t}{e^t}dt}=\begin{vmatrix}
v=2t&v'=2\\
u'=e^{-t}&u=-e^{-t}
\end{vmatrix}=\\
=-2te^{-t}+2\int{e^{-t}}=-2te^{-t}-2e^{-t}=
\frac{-2(1+\sin{y})}{e^{\sin{t}}}+(C_1)
\end{gathered}$$
Skoro mamy już funkcje podstawiamy :)
$$\begin{gathered}
x=\left(\frac{-2(1+\sin{y})}{e^{\sin{t}}}+(C_1)\right)e^{\sin{t}}=
\\=-2(1+\sin{y})+C_1e^{\sin{t}}
\end{gathered}$$

---
## zadania

#### 1. $y'+y \tan{x}=e^{2x}$
$$\begin{gathered}
\frac{dy}{dx}=-\tan{x}y\\
\frac{dy}{y}=-\tan{x}dx\\
\ln{|y|}=\ln{|\cos{x}|}+C \\
y=C(x)\cos{x}\\\\\
\frac{dy}{dx}=C'(x)\cos{x}-C(x)\sin{x}\\
\frac{dy}{dx}+y \tan{x}=e^{2x}\\\\\
C'(x)\cos{x}-C(x)\sin{x}+C(x)\cos{x} \tan{x}=e^{2x}\\
C'(x)\cos{x}=e^{2x}\\
 C'(x)=\frac{e^{2x}}{\cos{x}}
\end{gathered}$$
---
#### 2. $y'-\frac{y}{x}=\frac{1}{\ln{x}}$

$$\begin{gathered}
\frac{dy}{dx}=\frac{y}{x}\\
\frac{dy}{y}=\frac{dx}{x}\\
\ln{y}=\ln{x}+C\\
y=C(x)x\\\\\
\frac{dy}{dx}=C'(x)x+C(x)\\
C'(x)x+C(x)-C(x)=\frac{1}{\ln{x}}\\
C'(x)=\frac{1}{x\ln{x}}\\\\
\int{\frac{1}{x \ln{x}}dx}=\begin{vmatrix}
t=\ln{x}\\
dt=\frac{1}{x}dx
\end{vmatrix}=\int{\frac{1}{t}dt}=\ln{\ln{x}}\\\\
C(x)=\ln{|\ln{x}|}\\\\
y=\ln{|\ln{x|x}}
\end{gathered}$$

---
#### 3. $\left(x+\frac{y}{\ln{y}}\right)y'=y$

$$\begin{gathered}
y'+p(x)y=q(x)\\\\
\left(x+\frac{y}{\ln{y}}\right)y'=y\\
y'=\frac{y}{x+\frac{y}{\ln{y}}}
\end{gathered}$$

z twierdzenia o pochodnej funkcji odwrotnej

$$\begin{gathered}
\frac{dx}{dy}=\frac{x+\frac{y}{\ln{y}}}{y}\\
\frac{dx}{dy}=\frac{x}{y}+\frac{1}{\ln{y}}\\
\frac{dx}{dy}-\frac{x}{y}=\frac{1}{\ln{y}}\\
\end{gathered}$$

i rozwiązujemy jak normalnie
$$\begin{gathered}
\frac{dx}{dy}=\frac{x}{y}\\
\frac{dx}{x}=\frac{dy}{y}\\
\ln{x}=\ln{y}+C\\
x=C(y)y\\
\frac{dx}{dy}=C'(y)y+C(y)
\end{gathered}$$

podstawiamy
$$\begin{gathered}
\frac{dx}{dy}-\frac{x}{y}=\frac{1}{\ln{y}}\\
C'(y)y+C(y)-C(y)=\frac{1}{\ln{y}}\\
C'(y)=\frac{1}{y \ln{y}}\\
C(y)=\ln{\ln{y}}\\
x=\ln{\ln{y}}y
\end{gathered}
$$

---
#### 5. $y'+\frac{y}{2(x+1)}=x$

$$\begin{gathered}
\frac{dy}{dx}=-\frac{y}{2(x+1)}\\
\frac{dy}{y}=-\frac{dx}{2x+2}\\
\ln{y}=-\frac{1}{2}\ln{x+1}+C\\
y=C(x)(x+1)^{-\frac{1}{2}}=C(x)\frac{1}{\sqrt{x+1}}\\
\frac{dy}{dx}=C'(x)\frac{1}{\sqrt{x+1}}-C(x)\frac{\sqrt{x+1}}{2}\\\\
C'(x)\frac{1}{\sqrt{x+1}}-C(x)\frac{\sqrt{x+1}}{2}+C(x)\frac{\sqrt{x+1}}{2}=x\\\\\
C'(x)\frac{1}{\sqrt{x+1}}=x\\\\\
C'(x)=x \sqrt{x+1}\\
C(x)=2\sqrt{x+1}\,\left(\dfrac{{x}^{2}}{5}+\dfrac{x}{15}-\dfrac{2}{15}\right)+C\\\\
y=2\left(\dfrac{{x}^{2}}{5}+\dfrac{x}{15}-\dfrac{2}{15}\right)+\frac{C}{\sqrt{x+1}}
\end{gathered}$$































