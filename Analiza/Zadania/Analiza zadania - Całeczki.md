### Całki
#### 2025-01-11

#całki 

---
##### 1. Oblicz całki nieoznaczone:
###### a)
$$\begin{gathered}
\int{\frac{(1-x)^2}{\sqrt{x}} \ dx}=\int{\frac{x^2-2x+1}{\sqrt{x}} \ dx}=\\
=\int{\frac{x^2}{\sqrt{x}}}-2\int{\sqrt{x}}+\int{\frac{1}{\sqrt{x}}}=
\frac{x^{\frac{5}{2}}}{\frac{5}{2}}-2\frac{x^{\frac{3}{2}}}{\frac{3}{2}}+\frac{\sqrt{x}}{\frac{1}{2}}=\\
=\frac{5}{2}\sqrt{x^5}-3\sqrt{x^3}+\frac{1}{2}\sqrt{x}+C
\end{gathered}$$
---
###### b)
$$\begin{gathered}
\int{\frac{1}{x^2(1+x^2)}}:\\\\
\frac{1}{x^2(1+x^2)}=\frac{A}{x^2}+\frac{Bx+C}{1+x^2}+\frac{D}{x}\\
1=A(1+x^2)+Bx^3+Cx^2+D(x^3+x)\\
1=A+x^2(A+C)+(B+D)x^3+Dx\\
\left\{
\begin{matrix}
A=1\\
A+C=0
B+D=0\\
D=0
\end{matrix}
\right.
\
\left\{
\begin{matrix}
A=1\\
B=0\\
C=-1\\
D=0
\end{matrix}
\right.
\\
\int{\frac{1}{x^2(1+x^2)}\  dx}=\int{\frac{1}{x^2}-\frac{1}{1+x^2}  \ dx}=\\
=\int{\frac{1}{x^2}\ dx}-\int{\frac{1}{x^2+1}\ dx}=-\frac{1}{x}-\arctan(x)+C
\end{gathered}$$
---
###### c)
$$\begin{gathered}
\int{x^2\cos{x} \ dx}=\int{uv' \ dx}:\\
u=x^2, \ v=\sin{x}\\
\int{x^2\cos{x} \ dx}=x^2\cdot \sin{x}-\int{2x\cdot \sin{x}}=
x^2\cdot \sin{x}-(-2x\cdot \cos{x} - \int{2\cdot \cos{x}})=\\
=x^2\cdot \sin{x}+2x\cdot \cos{x+2\sin{x}}
\end{gathered}$$
---
###### d)
$$\begin{gathered}
\int{(\ln{x})^2 \ dx}:\\
\text{Podstawienie:}\\
u=\ln{x}\\
du=\frac{1}{x}dx\\
\int{(\ln{x})^2 \ dx}=\begin{vmatrix}
u=\ln{x}&du=\frac{1}{x}dx
\end{vmatrix}=\int{u^2x \ du}=\int{u^2e^u \ du}=\\
=u^2e^u-\int{2u \cdot e^u}=u^2e^u-(2u\cdot e^u-2e^u)=\\
=u^2e^u-2ue^u+2e^u=e^u(u^2-2u-2)=e^{\ln{x}}(\ln^2{x}-2\ln{x}-2)=\\
=x(\ln^2{x}-2\ln{x}-2)+C
\end{gathered}$$
---
###### e)
$$\begin{gathered}
\int{\cos{(\ln{x})} \ dx}=\begin{vmatrix}
t=\ln{x}, dt=\frac{1}{x}dx
\end{vmatrix}=\int{cos{(t)}\cdot e^t \ dt}=e^t\cdot \sin{x}-\int{e^t\cdot \sin{x}}=\\
=e^t\cdot \sin{t}-(-e^t\cdot \cos{t}-\int{e^t\cdot (-\cos{t})})=\\
=e^t\cdot \sin{t}+e^t\cdot \cos{t}-\int{e^t\cdot \cos{t}}\\\\
\int{e^t\cdot \cos{t} \ dt}=e^t\cdot \sin{t}+e^t\cdot \cos{t}-\int{e^t\cdot \cos{t}}\\
\int{e^t\cdot \cos{t} \ dt}=\frac{e^t\cdot \sin{t}+e^t\cdot \cos{t}}{2}\\
\int{e^{\ln{x}}\cdot \cos{\ln{x}} \ \frac{1}{x}\ dx}=\frac{e^{\ln{x}}\cdot \sin{\ln{x}}+e^{\ln{x}}\cdot \cos{\ln{x}}}{2}\\
\int{\cos{\ln{x}} \ dx}=\frac{e^{\ln{x}}\cdot \sin{\ln{x}}+e^{\ln{x}}\cdot \cos{\ln{x}}}{2}\\
\end{gathered}$$
---
###### f)
$$\begin{gathered}
\int{\frac{\sin{2x}}{\cos{x}} \ dx}=\int{\frac{2\sin{x}\cdot \cos{x}}{\cos{x}} \ dx}=\int{2\sin{x} \ dx}= 2\int{\sin{x} \ dx}=-2\cos{x}+C
\end{gathered}$$
---
###### g)
$$\begin{gathered}
\int{\frac{dx}{\sqrt[3]{4x+5}}\ dx}=\begin{vmatrix}
t=4x+5, dt=4 \ dx
\end{vmatrix}=\int{\frac{1}{t^{\frac{1}{3}}} \cdot \frac{1}{4}dt}=\frac{1}{4}\int{t^{-\frac{1}{3}}}=\frac{1}{4}\frac{t^{\frac{2}{3}}}{\frac{2}{3}}=\\
=\frac{3}{8}\cdot \sqrt[3]{t^2}=\frac{3}{8}\cdot \sqrt[3]{(4x+5)^2}
\end{gathered}$$
---
###### h)
$$\begin{gathered}
\int{\frac{3x^2+2}{x^3+2x+4} \ dx}:\\\\
\int{\frac{f'(x)}{f(x)}\ dx}=\ln{|f(x)|} + C\\\\
\text{No a przecież licznik czyli: }3x^2+4 \text{ jest pochodną mianownika czyli: }x^3+2x+4.\\
\int{\frac{3x^2+2}{x^3+2x+4} \ dx}=\ln{|x^3+2x+4|}+C
\end{gathered}$$
---
###### i)
$$\begin{gathered}
\int{\frac{dx}{3+4x^2}\ dx}=\frac{1}{3}\int{\frac{dx}{1+\frac{4}{3}x^2}}=\begin{vmatrix}
u=\frac{2}{\sqrt{3}}x \ dx\\
du=\frac{2}{\sqrt{3}}
\end{vmatrix}=
\frac{1}{3}\int{\frac{1}{1+u^2}\cdot \frac{\sqrt{3}}{2} du}=\\
=\frac{1}{2\sqrt{3}}\cdot \arctan{u}=\frac{1}{2\sqrt{3}}\cdot\arctan{\frac{2}{\sqrt{3}}x}+C

\end{gathered}$$
---
###### j)
$$\begin{gathered}
\int{\frac{x^2+6x+5}{x^2-6x+5} \ dx}=\int{1+\frac{12x}{x^2-6x+5} \ dx}=
x+\int{\frac{12x}{x^2-6x+5}\ dx}:\\\\
x^2-6x+5:\\
\Delta=16, x_1=\frac{6+4}{2}=5, x_2=1\\
x^2-6x+5=(x-1)(x-5)\\\\
\frac{12x}{x^2-6x+5}=\frac{A}{x-5}+\frac{B}{x-1}\\
12x=A(x-1)+B(x-5)\\
12x=x(A+B)-A-5B\\\\\
\left\{
\begin{matrix}
A+B=12\\
-5B=A
\end{matrix}
\right.
\left\{
\begin{matrix}
-4B=12\\
-5B=A
\end{matrix}
\right.
\left\{
\begin{matrix}
B=-3\\
15=A
\end{matrix}
\right.\\\\
\dots=x+\int{\frac{15}{x-5}-\frac{3}{x-1} \ dx}=x+15\int{\frac{1}{x-5}\ dx}-3\int{\frac{1}{x-1}\ dx}=\\
=x+15\ln{|x-5|-3\ln{|x-1|}}+C
\end{gathered}$$
---
###### k)
$$\begin{gathered}
\int{\frac{1}{x^3+6x^2+12x+8} \ dx}=\int{\frac{1}{(x+2)^3}\ dx}=\begin{vmatrix}
t=x+2, dt=dx
\end{vmatrix}=\\
=\int{\frac{1}{t^3}\ dt}=-\frac{1}{2t^2}=-\frac{1}{2(x+2)^2}+C
\end{gathered}$$

---
###### l)
$$\begin{gathered}
\int{\frac{1}{x^3-4x^2+5x-2} \ dx}=\int{\frac{1}{(x-1)(x^2-3x+2)}}:\\\\
\Delta=9-8=1, \ \ x_1=\frac{3+1}{2}=2, \ \ \ x_2=\frac{3-1}{2}=1\\\\
\dots =\int{\frac{1}{(x-1)(x-1)(x-2)}}=\int{\frac{1}{(x-1)^2(x-2)}\ dx}:\\\\


\frac{1}{(x-1)^2(x-2)}=\frac{A_1}{x-1}+\frac{A_2}{(x-1)^2}+\frac{B}{x-2}\\
1=A_1(x-1)(x-2)+A_2(x-2)+B(x-1)^2\\
1=A_1(x^2-3x+2)+A_2(x-2)+B(x^2-2x+1)\\
1=x^2(A_1+B)+x(-3A_1+A_2-2B)+2A_1-2A_2+B\\\\
\left\{
\begin{matrix}
A_1+B=0\\
-3A_1+A_2-2B=0\\
2A_1-2A_2+B=1
\end{matrix}
\right.
\left\{
\begin{matrix}
A_1+B=0\\
2A_2+2B=0\\
-2A_2-B=1
\end{matrix}
\right.
\left\{
\begin{matrix}
A_1+B=0\\
2A_2+2B=0\\
B=1
\end{matrix}
\right.
\left\{
\begin{matrix}
A_1=-1\\
A_2=-1\\
B=1
\end{matrix}
\right.\\\\
\dots=\int{\frac{-1}{x-1}+\frac{-1}{(x-1)^2}+\frac{1}{x-2} \ dx}=-\int{\frac{1}{x-1} \ dx } - \int{\frac{1}{(x-1)^2} \ dx} + \int{\frac{1}{x-2}}=\\
=-\ln{(|x-1|)}-\int{\frac{1}{(x-1)^2}}+\ln{(|x-2|)}=\\=-\ln{(|x-1|)}-\frac{(x-1)^{-1}}{-1}+\ln{(|x-2|)}=-\ln{(|x-1|)}+\frac{1}{x-1}+\ln{(|x-2|)}
\end{gathered}$$

---
###### m)
$$\begin{gathered}
\int{\frac{1}{5+4\cos{x}}\ dx}=\begin{vmatrix}
t=\tan{\frac{x}{2}}\\
\frac{x}{2}=\arctan{t}\\
dx=\frac{2}{1+t^2}\ dt
\end{vmatrix}=\int{\frac{1}{5+4\frac{1-t^2}{1+t^2}}\ \frac{2}{1+t^2}\ dt}=\\\\
=\int{\frac{2}{5+5t^2+4-4t^2} dt}=2\int{\frac{1}{9+t^2}\ dt}=\begin{vmatrix}
u=\frac{t}{3}\\
du=\frac{1}{3} \ dx
\end{vmatrix}=2\int{\frac{1}{9+9u^2}\cdot 3 \ dx}=\\
=\frac{2}{3}\int{\frac{1}{1+u^2} \ du}=\frac{2}{3}\cdot \arctan{\frac{\tan{\frac{x}{2}}}{3}}

\end{gathered}$$
**Podstawienie Weierstrassa** $t=\tan{\frac{x}{2}}$ z którego możemy sobie wyznaczyć $\cos$ lub $\sin$ na podstawie rozpisania wzorów $\sin{2x}$ oraz $\cos{2x}$:
$$\begin{gathered}
\cos{x}=\frac{\cos^2{\frac{x}{2}}-\sin^2{\frac{x}{2}}}{\cos^2{\frac{x}{2}}+\sin^2{\frac{x}{2}}}=\frac{1-\tan{\frac{x}{2}}}{1+\tan{\frac{x}{2}}}=\frac{1-t}{1+t}\\\\
\sin{x}=\frac{2\sin{\frac{x}{2}}\cos{\frac{x}{2}}}{\sin^2{\frac{x}{2}}+\cos^2{\frac{x}{2}}}=\frac{2\tan{\frac{x}{2}}}{\tan{\frac{x}{2}}+1}=\frac{2t}{t+1}
\end{gathered}$$


###### n)
$$\begin{gathered}
\int{\frac{cos^3{x}}{\sin^2{x}}\ dx}=\begin{vmatrix}
t=\tan{\frac{x}{2}}\\
x=2\arctan{t}\\
dx=\frac{2}{1+t^2} \ dt
\end{vmatrix}=\int{\frac{(1-t)^3}{(1+t)^3}\cdot \frac{(1+t)^2}{4t^2}\cdot \frac{2}{1+t^2}\ dt}=\\=\frac{1}{2}\int{\frac{1-3t+3t^2-t^3}{t^2+t^3+t^4+t^5} dt}=\frac{1}{2}\int{\frac{1-3t+3t^2-t^3}{t^2(1+t)(1+t^2)}\ dt}:\\\\\\

\frac{1-3t+3t^2-t^3}{t^2(1+t)(1+t^2)}=\frac{A_1}{t}+\frac{A_2}{t^2}+\frac{B}{1+t}+\frac{Cx+D}{1+t^2}\\
1-3t+3t^2-t^3=\frac{A_1}{t}+\frac{A_2}{t^2}+\frac{B}{1+t}+\frac{Cx+D}{1+t^2}\\\\
\dots
\end{gathered}$$
---
###### o)

$$\begin{gathered}
\int{\frac{\cos^3{x}}{\sin^2{x}}\ dx}=\begin{vmatrix}
t=\sin{x}\\
dt=\cos{x}\ dx\\
\end{vmatrix}=\int{\frac{1-t^2}{t^2}\ dt}=\int{\frac{1}{t^2}-1\ dt}=\int{t^{-2}\ dt}-\int{1\ dt}=\\
=-\frac{1}{t}-t=-\frac{1}{\sin{x}}-\sin{x}
\end{gathered}$$
###### p)
$$\begin{gathered}
\int{\sin^4{x}\cos^2{x}\ dx}=\begin{vmatrix}
\sin^2{x}=\frac{1-\cos{2x}}{2}\\
\cos^2{x}=\frac{1+cos(2x)}{2}
\end{vmatrix}=\int{\left(\frac{1-\cos{2x}}{2}\right)^2 \cdot \frac{1+\cos{2x}}{2} \ dx}=\\\\
=\int{(\frac{1-2\cos{2x}+\cos^2{2x}}{4})\cdot \frac{1+\cos{2x}}{2} \ dx}=\\\\
=\int{\frac{1-2\cos{2x}+cos^2{2x}+cos{2x}-2cos^2{2x}+\cos^3{2x}}{8}}=\\\\
=\int{\frac{1-\cos{2x}-\cos^2{2x}+\cos^3{2x}}{8}\ dx}=\begin{vmatrix}
t=\cos{2x}\\
dt=-2\sin{2x}\ dx
\end{vmatrix}

\end{gathered}$$

---




### INNE:
$$
\begin{gathered}
\int{\frac{1}{5+4\cos{x}}\ dx}=\begin{vmatrix}
t=\tan{\frac{x}{2}}\\
\cos{x}=\frac{1-t^2}{1+t^2}\\
\frac{x}{2}=\arctan{t}\\
x=2\arctan{t}\\
dx=2\frac{1}{t^2+1} \ dt
\end{vmatrix}=\int{\frac{1}{5+4\frac{1-t^2}{1+t^2}}\ \frac{2}{t^2+1}\ dt}=\\\\\
=2\int{\frac{1}{t^2+9}}=\frac{2}{9}\int{\frac{1}{(\frac{1}{3}t)^2+1}}=\\
=\begin{vmatrix}
u=\frac{1}{3}t\\
3du= dx
\end{vmatrix}=\frac{2}{3}\int{\frac{1}{u^2+1}\ du}=\frac{2}{3}\arctan{\frac{\tan{\frac{x}{2}}}{3}}
\end{gathered}
$$

---
$$\begin{gathered}
\int{x\sqrt{2x-10}\ dx}=\begin{vmatrix}
t^2=2x-10\\
t \ dt= dx
\end{vmatrix}=\int{\frac{t^2+10}{2}t^2 \ dt}=\\\\
=\frac{1}{2}\int{t^4+10t^2}=\frac{1}{2}\left(\int{t^4 \ dt} + 10\int{t^2\ dt}\right)
\end{gathered}$$


$$\begin{gathered}
\int{\frac{2x+1}{\sqrt{4x+1}}\ dx}=\begin{vmatrix}
t^2=4x+1\\
2t\ dt =4\ dx\\
dx=2t-4\ dt
\end{vmatrix}=\int{\frac{(t^3-2t^2+t+2)}{t^2}\ \ dt}
\end{gathered}$$


$$\begin{gathered}
\int{\sqrt{e^x-1}\ dx}=\begin{vmatrix}
e^x=t\\
x=\ln{t}\\
dx=\frac{1}{t}\ dt
\end{vmatrix}=
\int{\frac{\sqrt{t-1}}{t}\ dt}=\begin{vmatrix}
u^2=t-1\\
2u \ du=dt\\
\end{vmatrix}=\\\\\
=\int{\frac{u}{u^2+1}\cdot 2u\ du}=2\int{\frac{u^2}{u^2+1}\ du}=2\int{\frac{u^2+1}{u^2+1}\ du}-2\int{\frac{1}{u^2+1}\ du}=\\
=2\int{1}-2\arctan{u}=2u-2\arctan{u}=2\sqrt{e^x-1}-2\arctan{\sqrt{e^x-1}}
\end{gathered}$$


$$\begin{gathered}
\int{\frac{(8x+3)\ dx}{\sqrt{4x^2+3x+1}}}=\begin{vmatrix}
t=4x^2+3x+1\\
dt=8x+3 \ dx
\end{vmatrix}=\int{\frac{1}{\sqrt{t}}\ dt}=\int{t^{-\frac{1}{2}}\ dt}=\\\\
=\frac{t^{\frac{1}{2}}}{\frac{1}{2}}=2\sqrt{t}=2\sqrt{4x^2+3x+1}+C
\end{gathered}$$
$$\begin{gathered}
\int{x\sqrt{2+3x}\ dx}=\begin{vmatrix}
u^2=2+3x\\
\frac{2}{3}u \ du = dx
\end{vmatrix}=\int{\frac{(u^2-2)}{3}\cdot u \cdot \frac{2}{3}u \ du}=\\\\
=\frac{2}{9}\int{(u^2-2)\cdot u^2\ du}=\frac{2}{9}\int{u^4-2u^2\ du}=\\\\
=\frac{2}{9}(\frac{u^5}{5}-2\frac{u^3}{3})=\frac{2(2+3x)^2}{45}
\end{gathered}$$


$$\begin{gathered}
\int{\frac{dx}{\sqrt{2x-x^2}}}=\int{\frac{dx}{\sqrt{1-(x-1)^2}}}=\begin{vmatrix}
t=x-1\\
dt=dx
\end{vmatrix}=\int{\frac{1}{\sqrt{1-t^2}}\ dt}=\arcsin{t}=\\\\
=\arcsin{(x-1)}
\end{gathered}$$
