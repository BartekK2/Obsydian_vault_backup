### 1.

#### 1. $y'=x(1+2y^2)$

$$\begin{gathered}
\frac{dy}{dx}=x(1+2y^2)\\
\frac{dy}{1+2y^2}=xdx\ \ /\int\\
\int{\frac{dy}{1+2y^2}}=\begin{vmatrix}
y=\frac{u}{\sqrt{2}}\\
dy=\frac{du}{\sqrt{2}}
\end{vmatrix}=\int{\frac{du}{\sqrt{2}(1+u^2)}}=\\
=\frac{\arctan{u}}{\sqrt{2}}=\frac{\arctan{2\sqrt{y}}}{\sqrt{2}}\\\\\
\text{ostatecznie:}\\
\frac{\arctan{2\sqrt{y}}}{\sqrt{2}}=x^2+(C)
\end{gathered}$$
#### 2. $xy'=\sin^2{y}$

$$\begin{gathered}
x \frac{dy}{dx}=\sin^2{y}\\
\frac{dy}{\sin^2{y}}=\frac{dx}{x}\\
\int{\frac{dy}{\sin^2{y}}}=-\cot{y}\\\\
-\cot{y}=\ln{x}+(C)
\end{gathered}$$

#### 3. $y'=\frac{xe^{x^2}}{\log{y}}$

$$\begin{gathered}
\log{y}\ dy=xe^{x^2}dx\\
\int{\log{y}dy}=\begin{vmatrix}
t=\log{x}&v=x\\
dt=\frac{1}{x}&dv=1
\end{vmatrix}=y \log{y}-\int{1}=y \log{y}-1\\\\

\int{xe^{x^2}dx}=\frac{e^{x^2}}{2}\\\\
\frac{e^{x^2}}{2}=y \log{y}-1+(C)
\end{gathered}$$

#### 4. $y'=(\frac{y}{x})^2$

$$\begin{gathered}
\frac{dy}{dx}=(\frac{y}{x})^2\\\\
u(x)=\frac{y}{x}\\
xu=y\\
u(x)+x \frac{du}{dx}=\frac{dy}{dx}\\
u(x)+x \frac{du}{dx}=u^2(x)\\
\frac{du}{u^2-u}=\frac{dx}{x}\\
\int{\frac{du}{u^2-u}}:\\
\frac{1}{u^2-u}=\frac{A}{u-1}+\frac{B}{u}\\
1=Au+B(u-1)\implies B=-1 \land A =1\\\\
\dots=\int{\frac{du}{u-1}}-\int{\frac{du}{u}}=\ln{\frac{u-1}{u}}=\ln{\frac{\frac{y}{x}-1}{\frac{y}{x}}}=\ln{1-\frac{x}{y}}\\\\\
\ln{1-\frac{x}{y}}=\ln{x}+C_1\\
\ln{1-\frac{x}{y}}=\ln{C_2x}\\
1-\frac{x}{y}=C_2x\\
1-C_2x=\frac{x}{y}\\
y=\frac{x}{1-C_2x}
\end{gathered}$$

Można to było zrobić szybciej metodą zmiennych rozdzielonych po prostu...

#### 5. $y'+\frac{x}{y}=0$

$$\begin{gathered}
\frac{dy}{dx}=-\frac{x}{y}\\
ydy=-xdx\\
\frac{y^2}{2}=-\frac{x^2}{2}+C\\
y^2+x^2=C
\end{gathered}$$

#### 6. $y'=(y-x+1)^2$

$$\begin{gathered}
u=y-x+1\\
\frac{du}{dx}=\frac{dy}{dx}-1\\
\frac{du}{dx}+1=u^2\\
\frac{du}{u^2-1}=dx\\
\text{z czego:}\\\\
\frac{1}{u^2-1}=\frac{A}{u-1}+\frac{B}{u+1}\\
1=A(u+1)+B(u-1)\\
A+B=0\implies A=-B\\
A-B=1\implies -2B=1\implies B=-\frac{1}{2}\implies A=\frac{1}{2}\\\\
\int{\frac{1}{u^2-1}du}=\int{\frac{du}{2(u-1)}}-\int{\frac{du}{2(u+1)}}=\\
=\frac{\ln{|u-1|}}{2}-\frac{\ln{|u+1|}}{2}+C\\\\
\ln{\frac{u-1}{u+1}}=2x+C_1\\
\frac{u-1}{u+1}=e^{2x+C_1}=C_2e^{2x}
\end{gathered}$$

można wróćić z podstawieniem i przekształcić by mieć $y=\dots$

#### 7. $\sin^2{(x+y)}(y'+1)=1$

$$\begin{gathered}
\sin^2{(x+y)}(\frac{dy}{dx}+1)=1\\
\sin^2{(x+y)}\frac{dy}{dx}+\sin^2{(x+y)}=1\\
\frac{dy}{dx}=\frac{1-\sin^2{(x+y)}}{\sin^2{(x+y)}}=\frac{1}{\sin^2{(x+y)}}-1\\\\
u=x+y\\
\frac{du}{dx}=1+\frac{dy}{dx}\\\\
\frac{du}{dx}=\frac{1}{\sin^2{u}}\\

\end{gathered}$$

#### 8. $y'=\frac{x+y}{x-y+2}$

$$\begin{gathered}
W=\begin{vmatrix}
1&1\\
1&-1
\end{vmatrix}=-1-1=-2 \neq 0\\\\
\beta=x-h, \Psi=y-k\\\\
h+k=0\\
h-k+2=0\\
h=-k\\
k=1, h=-1\\
\frac{d \Psi}{d \beta}=\frac{\beta+\Psi}{\beta-\Psi}=\frac{1+\frac{\Psi}{\beta}}{1-\frac{\Psi}{\beta}}\\\\
u=\frac{\Psi}{\beta}\\
\beta u=\Psi\\
u+\beta u'=\frac{d \Psi}{d \beta}\\\\
u+\beta u'=\frac{1+u}{1-u}\\
\beta \frac{du}{d \beta}=\frac{1+u^2}{1-u}\\
\frac{1-u}{u^2+1}du=\frac{d \beta}{\beta}
\end{gathered}$$

policzmy:
$$\begin{gathered}
\arctan{u}-\int{\frac{udu}{u^2+1}}=\begin{vmatrix}
t=u^2+1\\
dt=2u du\\
\frac{dt}{2}=udu
\end{vmatrix}=\\=\arctan{u}-\frac{\ln{u^2+1}}{2}+C_1\\\\\
\arctan{u}-\frac{\ln{u^2+1}}{2}=\ln{\beta}+C_2
\end{gathered}$$

wystarczy z powrotem popodstawiać wszelakie $\Psi, \beta, u$ i mamy rozwiązanie w pewnej skomplikowanej ale poprawnej formie.


#### 9. $y'(x+y)=x+y-1$

$$\begin{gathered}
\frac{dy}{dx}=\frac{x+y-1}{x+y}\\\\
W=\begin{vmatrix}
1&1\\
1&1
\end{vmatrix}=0\\\\
u=x+y\\
\frac{du}{dx}=1+\frac{dy}{dx}\\
\frac{du}{dx}-1=\frac{x+y-1}{x+y}\\
\frac{du}{dx}=\frac{2u-1}{u}\\
\frac{u}{2u-1}du=dx\\\\
\int{\frac{u \ du}{2u-1}}=\begin{vmatrix}
t=2u\\
\frac{t}{2}=u\\
\frac{dt}{2}=du
\end{vmatrix}=\frac{1}{4}\int{\frac{t}{t-1}}=\begin{vmatrix}
k=t-1\\
dk=dt
\end{vmatrix}=\\
=\frac{1}{4}\int{\frac{k+1}{k}dk}=\frac{k+\ln{k}}{4}=\\
=\frac{k+\ln{k}}{4}=\frac{2u+\ln{2u-1}}{4}+C_1
\end{gathered}$$


Kontynuując:

$$\begin{gathered}
\frac{2x+2y+\ln{(2x+2y-1)}}{4}=x+C_2\\
\end{gathered}$$
Można to zapisać ładniej ale napewno nie w formie $y=\dots$  więc pozostawie to już tak...

#### 10. $y'+\frac{x+y-4}{x-y-4}=0$

$$\begin{gathered}
\frac{dy}{dx}=\frac{-x-y-4}{-x+y+4}\\\\
W=\begin{vmatrix}
-1&-1\\
-1&1
\end{vmatrix}=-2\\\\
\gamma=y-k\\
\xi=x-h\\
-h-k-4=0\\
-h+k+4=0\\
h=0, k=-4\\\\\
\frac{d \gamma}{d \xi}=\frac{dy}{dx}\\\\
\frac{d \gamma}{d \xi}=\frac{-\xi-\gamma}{-\xi+\gamma}=\frac{-1-\frac{\gamma}{\xi}}{-1+\frac{\gamma}{\xi}}
\end{gathered}$$

Podstawiając $u=\frac{\gamma}{\xi}$

$$\begin{gathered}
u \xi=\gamma\\
u' \xi + u=\frac{d\gamma}{d\xi}\\\\
u' \xi + u=\frac{-1-u}{-1+u}\\
\frac{du}{d \xi} \xi=\frac{-1-u^2}{-1+u}\\
\frac{1-u}{u^2+1}du=\frac{d \xi}{\xi}\\
\arctan{u}-\frac{\ln{(u^2+1)}}{2}=\ln{\xi}+C
\end{gathered}$$

z powrotem podstawiamy $u=\frac{\gamma}{\xi}=\frac{y+4}{x}$ i gituwa

---
### 2.

#### 1. $y'-y \ln{x}=0$

$$\begin{gathered}
\frac{dy}{dx}=y \ln{x}\\
\frac{dy}{y}=\ln{x}dx\\
\ln{y}=x \ln{(x)}-x +C_1\\
y=e^{x \ln{(x)}-x +C_1}=C_2 \frac{x^x}{e^x}
\end{gathered}$$

#### 2. $y'+yx^2=y$

$$\begin{gathered}
\frac{dy}{dx}+y(x^2-1)=0\\
-\frac{dy}{y}=(x^2-1)dx\\
-\ln{y}=\frac{x^3}{3}-x+C_1\\
\ln{y}=-\frac{x^3}{3}+x+C_2\\
y=C_3e^{-\frac{x^3}{3}+x}
\end{gathered}$$

#### 3. $y'-y \cot{x}=x^2\sin{x}$

$$\begin{gathered}
\frac{dy}{dx}=y \cot{x}\\
\frac{dy}{y}=\cot{x}dx\\
\ln{y}=\ln{\sin{x}}+C\\
y=C(x)\sin{x}\\\\
\frac{dy}{dx}=C'(x)\sin{x}+C(x)\cos{x}\\\\
\end{gathered}$$

wróćmy do równania pierwotnego i podstawmy:
$$\begin{gathered}
C'(x)\sin{x}+C(x)\cos{x}-C(x)\sin{x} \cot{x}=x^2\sin{x}\\
C'(x)=x^2\\
C(x)=\frac{x^3}{3}+C\\
y=\frac{x^3}{3}\sin{x}+C\sin
{x}
\end{gathered}$$

#### 4. $xy'+2xy=x^2-x$

$$\begin{gathered}
y'+2y=x-1\\
\frac{dy}{dx}=-2y\\
-\frac{dy}{2y}=dx\\
-\frac{1}{2}\ln{y}=x+C_1\\
\ln{y}=-2x+C_2\\
y=C(x)e^{-2x}\\
\frac{dy}{dx}=-2C(x)e^{-2x}+C'(x)e^{-2x}\\\\
C'(x)e^{-2x}=x-1\\
C'(x)=e^{2x}x-e^{2x}\\
C(x)=\left(\frac{x}{2}-\frac{3}{4}\right)\,{e}^{2\,x}+C\\\\
y=\left(\frac{x}{2}-\frac{3}{4}\right)+\frac{C}{e^{2x}}
\end{gathered}$$

#### 6. $y'-\frac{4y}{x}=x^5-x^4$

$$\begin{gathered}
\frac{dy}{dx}=\frac{4y}{x}\\
\ln{y}=4\ln{x}+C\\
y=C(x)x^4\\\\
\frac{dy}{dx}=C'(x)x^4+4C(x)x^3\\\\
C'(x)x^4+4C(x)x^3-\frac{4C(x)x^4}{x}=x^5-x^4\\
C'(x)=x-1\\
C(x)=\frac{x^2}{2}-x+C\\\\
y=(\frac{x^2}{2}-x+C)x^4=\frac{x^6}{2}-x^5+Cx^4
\end{gathered}$$

#### 7. $y'+2y=xe^x$


$$\begin{gathered}
\frac{dy}{dx}=-2y\\
-\frac{dy}{2y}=dx\\
\ln{\frac{1}{2y}}=x+C_1\\
\frac{1}{2y}=C_2e^x\\
y=C(x)\frac{1}{2e^x}\\
\frac{dy}{dx}=-\frac{C(x)}{2e^x}+C'(x)\cdot \frac{1}{2e^x}\\\\
C'(x)=2xe^{2x}\\
C(x)=\begin{vmatrix}
t=2x\\
dt=2dx
\end{vmatrix}=\frac{1}{2}\int{te^tdt}=\frac{te^t-e^t}{2}=\frac{2xe^{2x}-e^{2x}}{2}+C\\\\
y=\frac{2x-1}{4}+\frac{C}{2e^{2x}}
\end{gathered}$$

błąd gdzieś tam


---
### 3.

#### 2. $xy'+\frac{2xy}{1-x^2}=x \sqrt{y}$

$$\begin{gathered}
y'+\frac{2y}{1-x^2}=\sqrt{y}\\
y'=\sqrt{y}-\frac{2y}{1-x^2}\\
z=y^{1-\frac{1}{2}}\\
\frac{dz}{dx}=(1-\frac{1}{2})y^{-\frac{1}{2}}\frac{dy}{dx}=\frac{1}{2\sqrt{y}}\frac{dy}{dx}\\\\
\frac{dz}{dx}=\frac{1}{2}-\frac{\sqrt{y}}{1-x^2}=\frac{1}{2}-\frac{z}{1-x^2}\\
\frac{dz}{dx}+\frac{z}{1-x^2}=\frac{1}{2}\\
\text{trzeba to teraz rozwiązać z tego równania typu:}\\
y'+g(x)y=f(x)
\end{gathered}$$

#### 3. $y \tan{x}+e^xy^3+2y'=0$

$$\begin{gathered}
2y'=-y \tan{x}-e^xy^3\\\\
z=y^{1-3}\\
\frac{dz}{dx}=(1-3)y^{-3}\frac{dy}{dx}=-2y^{-3}\frac{dy}{dx}\\\\
-2y^{-3}\frac{dy}{dx}=\tan{x}y^{-2}+e^x\\\\
\frac{dz}{dx}=\tan{x}z+e^x\\\\
\text{wystarczy rozwiązać}\\\\
\frac{dz}{z}=\tan{x}dx\\
\ln{z}=-\ln{\cos{x}}+C\\

z=\frac{C(x)}{\cos{x}}\\\\
\frac{dz}{dx}=\frac{C'(x)}{\cos{x}}+\frac{C(x)\sin{x}}{\cos^2{x}}
\end{gathered}$$

podstawiając otrzymujemy:

$$\begin{gathered}
C'(x)=e^x \cos{x}\\
\int{e^x \cos{x} dx}=\begin{vmatrix}
t=e^x&v'=\cos{x}\\
t'=e^x&v=\sin{x}
\end{vmatrix}=\\
=e^x \sin{x}-\int{e^x \sin{x}dx}=\begin{vmatrix}
t=e^x&v'=\sin{x}\\
t'=e^x&v=-\cos{x}
\end{vmatrix}=\\
=e^x \sin{x}+e^x \cos{x}+\int{-e^x \cos{x}}\\
\text{co prowadzi do:}\\
2\int{e^x \cos{x} dx}=e^x \sin{x}+e^x \cos{x}\\
\int{e^x \cos{x} dx}=\frac{e^x \sin{x}+e^x \cos{x}}{2}\\\\\\
C(x)=\frac{e^x(\cos{x}+\sin{x})}{2}+C\\
z=\frac{e^x(\cos{x}+\sin{x})+2C}{2\cos{x}}\\\\
y=\sqrt{\frac{2\cos{x}}{e^x(\cos{x}+\sin{x})+2C}}
\end{gathered}$$
#### 4. $(\sin{y}+\frac{1}{2}y^2)dx+x(\cos{y}+y)dy=0$

$$\begin{gathered}
\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}\\
\frac{\partial u}{\partial x}=\sin{y}+\frac{1}{2}y^2\\
u=x \sin{y}+\frac{xy^2}{2}+C(y)\\
\frac{\partial u}{\partial y}=x \cos{y}+xy+C'(y)=Q(x,y)\implies C'(y)=0\\
C(y)=C\\
x \sin{y}+\frac{xy^2}{2}=C
\end{gathered}$$



