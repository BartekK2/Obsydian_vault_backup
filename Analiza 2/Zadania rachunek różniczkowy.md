
##### 1. Pokaż, że funkcja $d((x_1,y_1), (x_2,y_2))=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}$ jest metryką w $\mathbb{R}^2$

Warunki metryki to:
1. nieujemność $d(A,B)\geq 0$
2. zerowa odległość dla identycznych $d(A,B)=0\Leftrightarrow A=B$
3. symetria $d(A,B)=d(B,A)$
4. nierówność trójkąta

$$\begin{gathered}
1) \sqrt{(x_2-x_1)^2+(y_2-y_1)^2}\geq 0\\\\
2) d(A,B)=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}=0\Leftrightarrow x_2=x_1 \land y_2=y_1 \Leftrightarrow A=B\\\\
3) \sqrt{(x_2-x_1)^2+(y_2-y_1)^2}=\sqrt{(x_1-x_2)^2+(y_1-y_2)^2}\\\\
4) \sqrt{(x_2-x_1)^2+(y_2-y_1)^2}\leq \sqrt{(x_3-x_1)^2+(y_3-y_1)^2}+\sqrt{(x_2-x_3)^2+(y_2-y_3)^2}
\end{gathered}$$
---
##### 2. Oblicz granicę ciągu $x_n=\left(\frac{n^2\cos{(n!)}}{n^3+2n},(1+\frac{1}{n})^{2n-3}, \sqrt{4n^2+3n-2}-2n\right)$

Granica ciągu $\mathbb{R}^k$ jest równa granicy współczynników w sensie:

$\lim_{n\to \infty}x_n=(g_1,g_2,\dots,g_k)\Leftrightarrow \forall i =1,2,\dots,k \ \ \lim_{n\to \infty}x_n^i=g_i$

$$\begin{gathered}
\lim_{n\to \infty}{\frac{n^2\cos{(n!)}}{n^3+2n}}=0 \text{ (cosinus ograniczony a pozostale zbiezne do 0)}\\
\lim_{n\to \infty}(1+\frac{1}{n})^{2n-3}=\lim_{n\to \infty}\frac{(1+\frac{1}{n})^{2n}}{(1+\frac{1}{n})^{3}}=e^2\\
\lim_{n\to \infty}\sqrt{4n^2+3n-2}-2n=\lim_{n\to \infty}\frac{4n^2+3n-2-4n^2}{\sqrt{4n^2+3n-2}+2n}=\lim_{n\to \infty}{\frac{3n-2}{2n\sqrt{1+\frac{3}{4n}-\frac{1}{2n^2}}+2n}}=\frac{3}{4}\\\\
\lim_{n\to \infty}{x_n}=(0,e^2,\frac{3}{4})
\end{gathered}$$

---

##### 3. Oblicz granicę $\lim_{(x,y)\to (0,0)}\frac{x^2}{x^2+y^2}$

Na podstawie definicji granicy Heinego potrzebujemy ciągów dążących do 0:

$$\begin{gathered}
\lim_{(x,y)\to (0,0)}\frac{x^2}{x^2+y^2}:\\
x=\frac{1}{n}\\
x\to 0 \Leftrightarrow n\to \infty\\
y=0\\
\lim_{n\to \infty}\frac{\frac{1}{n^2}}{\frac{1}{n^2}+0}=1
\\\\
x=\frac{1}{n}\\
y=\frac{1}{n}\\
x\to 0 \land y\to 0\Leftrightarrow n\to \infty\\
\lim_{n\to \infty}\frac{\frac{1}{n^2}}{\frac{1}{n^2}+\frac{1}{n^2}}=\frac{1}{2}
\end{gathered}$$

Różne granice więc niezbieżne.

---
##### 4. Zbadaj ciągłość w całej dziedzinie funkcji:

###### a)

$$\begin{gathered}
f(x,y)=\left\{\begin{matrix}
\frac{x^2y^2}{x^2+y^2}, & (x,y)\neq (0,0)\\
0, & (x,y)=(0,0)
\end{matrix}
\right.\\\\
\lim_{(x,y)\to (0,0)}{f(x,y)}\overset{x=\frac{1}{n}, y=\frac{2}{n}}{=}\lim_{n\to \infty}{\frac{\frac{4}{n^2}}{\frac{5}{n^2}}}=\frac{4}{5}
\\\\
\text{Granica różna od wartości w punkcie więc nie ciągła.}

\end{gathered}$$


###### b) 
$$\begin{gathered}
f(x,y)=\left\{
\begin{matrix}
\frac{x^4-y^4}{x^2+y^2}=x^2-y^2&(x,y)\neq (0,0)\\
0&(x,y)=(0,0)
\end{matrix}
\right.\\\\
\lim_{(x,y)\to (0,0)}{x^2-y^2}=0\\\\
\text{Granice jednostronne są sobie równe i są równe wartości w punkcie więc ciągłe}
\end{gathered}$$
---
##### 5. Oblicz granicę $\lim_{(x,y)\to (0,0)}{(x+y)\sin{\frac{1}{x}}\sin{\frac{1}{y}}}$ oraz granicę iterowaną $\lim_{y\to 0}(\lim_{x\to 0}{(x+y)\sin{\frac{1}{x}}\sin{\frac{1}{y}}})$

$$\begin{gathered}
iterowana:\\
\lim_{y\to 0}(\lim_{x\to 0}{(x+y)})=\lim_{y\to 0}{(0+y)}=0\\\\
-(x+y)\lt (x+y)\sin{\frac{1}{x}}\sin{\frac{1}{y}}\lt x+y\\\\
\lim_{(x,y)\to (0,0)}{x+y}=
\lim_{(x,y)\to (0,0)}{-(x+y)}=0
\end{gathered}$$
---
##### 6. Pokaż że funkcja f ma w punkcie $(0,0)$ pochodne kierunkowe w dowolnym kierunku ale nie jest różniczkowalna w tym punkcie.

$$\begin{gathered}
f(x,y)=\left\{
\begin{matrix}
\frac{xy^2}{x^2+y^2}, \ \ \ (x,y)\neq (0,0)\\
0, \ \ \ (x,y)=(0,0)
\end{matrix}
\right.\\\\
\text{Przyjmując dowolny wektor }t\\
\text{jego wersor:}\\
h=\frac{t}{||t||}=\frac{t}{\sqrt{x_t^2+y_t^2}}=(h_x,h_y)\\\\
D_hf(0,0)=\lim_{j\to 0}{\frac{f(jh)-0}{j}}=\lim_{j\to 0}{\frac{\frac{j^3(h_xh_y^2)}{j^2h_x^2+j^2h_y^2}}{j}}=
\lim_{j\to 0}{\frac{h_xh_y^2}{h_x^2+h_y^2}}=\frac{h_xh_y^2}{h_x^2+h_y^2}\\
\text{Czyli pochodna kierunkowa w punkcie }(0,0)\text{ istnieje dla dowolnnego kierunku }h
\end{gathered}$$

Czy funkcja jest różniczkowalna w (0,0)?

$$\begin{gathered}
f((0,0)+(h_x,h_y))-f(0,0)=L_{(0,0)}(h_x,h_y)+r_{(0,0)}{(h_x,h_y)}\\
\lim_{h\to 0}{\frac{r_{(0,0)}{(h)}}{||h||}}=0\\\\\\
f(h_x,h_y)=L_{(0,0)}(h_x,h_y)+r_{(0,0)}{(h_x,h_y)}\\\\
f(h_x,h_y)=\frac{\partial f}{\partial x}(0,0)h_x+\frac{\partial f}{\partial y}(0,0)h_y+r_{(0,0)}{(h_x,h_y)}\\\\
\frac{\partial f}{\partial x}(0,0)=\lim_{h\to 0}{\frac{f(h,0)}{h}}=
\lim_{h\to 0}{\frac{\frac{h\cdot 0}{h^2+0}}{h}}=0\\
\frac{\partial f}{\partial y}(0,0)=\lim_{h\to 0}{\frac{f(0,h)}{h}}=
\lim_{h\to 0}{\frac{\frac{0\cdot h^2}{0+h^2}}{h}}=0\\\\\
f(h_x,h_y)=r_{(0,0)}{(h_x,h_y)}\\
\frac{h_xh_y^2}{h_x^2+h_y^2}=r_{(0,0)}{(h_x,h_y)}\\
\lim_{h\to 0}{\frac{r_{(0,0)}{(h)}}{||h||}}=\lim_{h\to 0}{\frac{\frac{h_xh_y^2}{h_x^2+h_y^2}}{\sqrt{h_x^2+h_y^2}}}=\lim_{(h_x,h_y)\to (0,0)}{\frac{\frac{h_xh_y^2}{h_x^2+h_y^2}}{\sqrt{h_x^2+h_y^2}}}=\begin{vmatrix}
h_x=r\cos{\varphi}\\
h_y=r\sin{\varphi}\\
r \to 0\\
\varphi - dowolne
\end{vmatrix}=\\
=\lim_{r\to 0}{\frac{\frac{r^3\cos{\varPhi}\sin^2{\varphi}}{r^2}}{\sqrt{r^2}}}=
\lim_{r\to 0}{\frac{r^3\cos{\varphi}\sin^2{\varphi}}{r^3}}=\lim_{r\to 0}\cos{\varphi}\sin^2{\varphi}\\\\
\text{Granica nie istnieje (zalezy od }\varphi )\\
\text{Więc funkcja nie jest różniczkowalna}
\end{gathered}$$

---
##### 7. Pokaż, że funkcja $f(x,y)=\left\{\begin{matrix}0,xy\neq 0\\ 1, xy=0\end{matrix}\right.$ ma obie pochodne cząstkowe w punkcie (0,0) a nie jest nawet ciągła w tym punkcie. 

$$\begin{gathered}
\text{Pochodne cząstkowe:}\\\\
\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}\frac{f(0+\Delta x, 0)-f(0,0)}{\Delta x}=
\lim_{\Delta x\to 0}\frac{f(\Delta x, 0)-f(0,0)}{\Delta x}=\lim_{\Delta x\to 0}\frac{0}{\Delta x}=0\\
\frac{\partial f}{\partial y}(0,0)=\lim_{\Delta y\to 0}\frac{f(0, 0+\Delta y)-f(0,0)}{\Delta y}=
\lim_{\Delta y\to 0}\frac{f(0, \Delta y)-f(0,0)}{\Delta y}=\lim_{\Delta y\to 0}\frac{0}{\Delta y}=0\\\\
\text{Ciągłość:}\\\\
\lim_{(x,y)\to (0,0)}{f(x,y)}=\begin{vmatrix}
x=\frac{1}{n}\\
y=0
\end{vmatrix}=\lim_{n\to \infty}{0}=0\\
\lim_{(x,y)\to (0,0)}{f(x,y)}=\begin{vmatrix}
x=\frac{1}{n}\\
y=\frac{1}{n}
\end{vmatrix}=\lim_{n\to \infty}{1}=1\\\\
\text{Dla różnych ciągów otrzymujemy różne wartości, zatem granica podwójna nie istnieje.}
\end{gathered}$$

---
##### 8. Zbadaj różniczkowalność w całej dziedzinie funkcji:


###### a) $f(x,y)=\sqrt{x^2+y^2}$
$$\begin{gathered}
\text{Dla }(x,y)\in \mathbb{R}^2\setminus \{(0,0)\} \text{ funkcja jest różniczkowalna jako złożenie funkcji }g(u)=\sqrt{u}\\
\text{która jest różniczkowalna dla }u\gt0, \text{oraz funkcji }h(x,y)=x^2+y^2,\\ \text{która jest różniczkowalna w całym }\mathbb{R}^2\\\\
f((0,0)+h)-f(0,0)=f(h_x,h_y)=\sqrt{h_x^2+h_y^2}\\
\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}{\frac{f(\Delta x, 0)-f(0,0)}{\Delta x}}=\lim_{\Delta x\to 0}{\frac{\sqrt{(\Delta x)^2}}{\Delta x}}=\lim_{\Delta x\to 0}{\frac{|x|}{x}} - \text{nie istnieje}:\\
\lim_{\Delta x\to 0^-}{\frac{|x|}{x}} =-1\\
\lim_{\Delta x\to 0^+}{\frac{|x|}{x}} =1\\
\text{Zatem pochodna cząstkowa nie istnieje w punkcie } (0,0) \text{ co jest warunkiem koniecznym }\\
\text{różniczkowalności funkcji w tym punkcie }.\\
\text{Zatem ta funkcja nie jest różniczkowalna w całej dziedzinie, jest różniczkowalna w }\\\mathbb{R}^2 \setminus \{(0,0)\}
\text{ a nie jest w }\{(0,0)\}.
\end{gathered}$$
---
###### b) $f(x,y)=\sqrt{x^4+y^4}$

$$\begin{gathered}
\text{Dla }(x,y)\in \mathbb{R}^2\setminus \{(0,0)\} \text{ funkcja jest różniczkowalna jako złożenie funkcji }g(u)=\sqrt{u}\\
\text{która jest różniczkowalna dla }u\gt0, \text{oraz funkcji }h(x,y)=x^4+y^4,\\ \text{która jest różniczkowalna w całym }\mathbb{R}^2\\\\
\text{Dla }(x,y)=(0,0)\\\\
\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}{\frac{f(\Delta x, 0)-f(0,0)}{\Delta x}}=\lim_{\Delta x\to 0}{\frac{\sqrt{(\Delta x)^4}}{\Delta x}}=\lim_{\Delta x\to 0}{\frac{|(\Delta x)^2|}{\Delta x}}=0\\\\\

\frac{\partial f}{\partial y}(0,0)=\lim_{\Delta y\to 0}{\frac{f(0, \Delta y)-f(0,0)}{\Delta y}}=\lim_{\Delta y\to 0}{\frac{\sqrt{(\Delta y)^4}}{\Delta y}}=\lim_{\Delta y\to 0}{\frac{|(\Delta y)^2|}{\Delta y}}=0\\\\
f(h_x,h_y)=r_{(0,0)}h\\
r_{(0,0)}h=\sqrt{h_x^4+h_y^4}\\\\
\lim_{(h_x,h_y)\to (0,0)}{\frac{\sqrt{h_x^4+h_y^4}}{\sqrt{h_x^2+h_y^2}}}=\begin{vmatrix}
h_x=r\cos{\varphi}\\
h_y=r\sin{\varphi}\\
r\to 0\\
\varphi - dowolne
\end{vmatrix}=\lim_{r\to 0}{\frac{\sqrt{r^4(\cos^4{\varphi}+\sin^4{\varphi})}}{|r|}}=\\=lim_{r\to 0}{\ r\sqrt{\cos^4{\varphi}+\sin^4{\varphi}}}=0\checkmark\\\\
\end{gathered}$$
---
###### c) $f(x,y)=\left\{\begin{matrix}\frac{x^3+y^3}{x^2+y^2}, \ \ (x,y)\neq (0,0)\\ 0, \ \ \ (x,y)=(0,0)\end{matrix}\right.$

$$\begin{gathered}
\lim_{(x,y)\to (0,0)}{\frac{x^3+y^3}{x^2+y^2}}=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
r\to 0\\
\varphi - dowolne
\end{vmatrix}=\lim_{r\to 0}{\frac{r^3(\cos^3{\varphi}+\sin^3{\varphi})}{1}}=0\\\\
\text{Ciągła więc WK mamy z głowy}\\\\
\frac{x^3+y^3}{x^2+y^2} - \text{Różniczkowalne wszędzie poza }(0,0) \text{ jako iloraz funkcji wielomianowej}\\\\
f(h_x,h_y)-f(0,0)=\frac{h_x^3+h_y^3}{h_x^2+h_y^2}\\
\frac{h_x^3+h_y^3}{h_x^2+h_y^2}=\frac{\partial f}{\partial x}(0,0)h_x+\frac{\partial f}{\partial y}(0,0)h_y+r_{(0,0)}h\\
\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}{\frac{\frac{\Delta x^3+0^3}{\Delta x^2+0^2}}{\Delta x}}=1\\
\frac{\partial f}{\partial y}(0,0)=\lim_{\Delta y\to 0}{\frac{\frac{0^3+y^3}{0+\Delta y^2}}{\Delta y}}=1\\
\frac{h_x^3+h_y^3}{h_x^2+h_y^2}-h_x-h_y=r_{(0,0)}h\\
r_{(0,0)}h=\frac{h_x^3+h_y^3}{h_x^2+h_y^2}-\frac{h_x^3+h_xh_y^2}{h_x^2+h_y^2}-\frac{h_yh_x^2+h_y^3}{h_x^2+h_y^2}=-\frac{h_xh_y^2+h_yh_x^2}{h_x^2+h_y^2}\\\\
\lim_{(h_x,h_y)\to (0,0)}{-\frac{h_xh_y^2+h_yh_x^2}{h_x^2+h_y^2}\cdot \frac{1}{\sqrt{h_x^2+h_y^2}}}=
\lim_{(h_x,h_y)\to (0,0)}{-\frac{h_xh_y^2+h_yh_x^2}{(h_x^2+h_y^2)^{\frac{3}{2}}}}=\\
=\begin{vmatrix}
h_x=r\cos{\varphi}\\
h_y=r\sin{\varphi}\\
r\to 0\\
\varphi - dowolne
\end{vmatrix}=\lim_{r\to 0}{-\frac{r^3(\cos{\varphi}\sin^2{\varphi}+\sin{\varphi}\cos^2{\varphi})}{1}}=0\\\\
\text{Zatem różniczkowalne w }(0,0)
\end{gathered}$$
---
##### 9. Oblicz pochodną wzdłuż wektora $h=(3,-1)$ funkcji $f(x,y)=x^4+y^4+2x^2y+1$ w punkcie $x_0=(1,2)$


$$\begin{gathered}
\text{Korzystam z twierdzenia o związku różniczki }\\
\text{z pochodnymi wzdłuż wektora.}\\\\
\frac{\partial f}{\partial x}(1,2)=4x^3+4xy (1,2)=4+8=12\\
\frac{\partial f}{\partial y}(1,2)=4y^3+2x^2(1,2)=34\\\\
D_hf(x,y)=df(x,y)(h)\\\\
D_{(3,-1)}f(1,2)=df(1,2)(3,-1)=36-34=2
\end{gathered}$$

---
##### 10. Oblicz pochodną kierunkową w kierunku wektora $h=(1,2,2)$ funkcji $f(x,y,z)=\ln{(x^2+y^2+z^2)}$ w punkcie $x_0=(-2,1,2)$.

$$\begin{gathered}
\frac{\partial f}{\partial x}=\frac{2x}{x^2+y^2+z^2}\\

\frac{\partial f}{\partial y}=\frac{2y}{x^2+y^2+z^2}\\

\frac{\partial f}{\partial z}=\frac{2z}{x^2+y^2+z^2}\\

\frac{\partial f}{\partial x}(-2,1,2)=-\frac{4}{9}\\

\frac{\partial f}{\partial y}(-2,1,2)=\frac{1}{9}\\
\frac{\partial f}{\partial z}(-2,1,2)=\frac{4}{9}\\
D_{(1,2,2)}f(-2,1,2)=-\frac{4}{9}+\frac{2}{9}+\frac{8}{9}=\frac{2}{3}
\end{gathered}$$

---
##### 11. Oblicz przybliżoną wartość $\frac{(1,03)^2}{\sqrt[3]{0,98\sqrt[4]{1,05}}}$
$$\begin{gathered}
f(x,y,z)=\frac{x^2}{\sqrt[3]{y \sqrt[4]{z}}}\\
f(1.03,0.98,1.05)\approxeq f(1,1,1)+D_{(0.3,-0.2,0.5)}(1,1,1)\\\\
f(1,1,1)=1\\
D_{(0.03,-0.02,0.05)}(1,1,1):\\
\frac{\partial f}{\partial x}=\frac{2x}{\sqrt[3]{y \sqrt[4]{z}}}\\
\frac{\partial f}{\partial y}=-\frac{x^2}{3(y^{\frac{4}{3}}) \sqrt[12]{z}}\\
\frac{\partial f}{\partial z}=-\frac{x^2}{12\sqrt[3]{y}}\cdot z^{-\frac{13}{12}}\\\\
\frac{\partial f}{\partial x}(1,1,1)=2\\
\frac{\partial f}{\partial y}(1,1,1)=-\frac{1}{3}\\
\frac{\partial f}{\partial z}(1,1,1)=-\frac{1}{12}\\\\
\frac{(1,03)^2}{\sqrt[3]{0,98\sqrt[4]{1,05}}}=1+2\cdot 0.03+\frac{2}{300}-\frac{1}{240}=1.0625
\end{gathered}$$
---
##### 12. Wyznacz równanie płaszczyzny stycznej do wykresu funkcji $f(x,y)=arctg(\frac{y}{x})$ w punkcie $(1,1)$

$$\begin{gathered}
z=f(1,1)+\frac{\partial f}{\partial x}(1,1)(x-1)+\frac{\partial f}{\partial y}(1,1)(y-1)\\
z=arctg(1)-\frac{y}{(1+\frac{y^2}{x^2})\cdot x^2}(1,1)(x-1)+\frac{x}{x^2+y^2}(1,1)(y-1)=\\
=\frac{\pi}{4}-\frac{1}{2}(x-1)+\frac{1}{2}(y-1)=
\frac{\pi}{4}-\frac{1}{2}x+\frac{1}{2}y

\end{gathered}$$

---
##### 13. Wyznacz macierz Jacobiego i jakobian odwzorowania $(r,\varphi, \psi)\to (x(r,\varphi, \psi), y(r,\varphi, \psi), z(r,\varphi, \psi))$ gdzie $x=r\sin{\psi}\cos{\varphi}, y=r \sin{\psi}\sin{\varphi}, z=r \cos{\psi}$

$$\begin{gathered}
df(x_0)(h)=df(r,\varphi,\psi)=\begin{bmatrix}
\frac{\partial x}{\partial r}(x_0)&
\frac{\partial x}{\partial \varphi}(x_0)&
\frac{\partial x}{\partial \psi}(x_0)\\

\frac{\partial y}{\partial r}(x_0)&
\frac{\partial y}{\partial \varphi}(x_0)&
\frac{\partial y}{\partial \psi}(x_0)\\

\frac{\partial z}{\partial r}(x_0)&
\frac{\partial z}{\partial \varphi}(x_0)&
\frac{\partial z}{\partial \psi}(x_0)

\end{bmatrix}=\\\\=\begin{bmatrix}
\sin{\psi}\cos{\varphi}(x_0)&
-r\sin{\psi}\sin{\varphi}(x_0)&
r \cos{\psi}\cos{\varphi}(x_0)\\

\sin{\psi}\sin{\varphi}(x_0)&
r \sin{\psi}\cos{\varphi}(x_0)&
r \cos{\psi}\sin{\varphi}(x_0)\\

\cos{\psi}(x_0)&
0(x_0)&
-r \sin{\psi}(x_0)
\end{bmatrix}=\\\\
=
\begin{bmatrix}
\sin{\psi}\cos{\varphi}&
-r\sin{\psi}\sin{\varphi}&
r \cos{\psi}\cos{\varphi}\\

\sin{\psi}\sin{\varphi}&
r \sin{\psi}\cos{\varphi}&
r \cos{\psi}\sin{\varphi}\\

\cos{\psi}&
0&
-r \sin{\psi}
\end{bmatrix}
\end{gathered}$$

$$\begin{gathered}
\det df(x_0)(h)=-\sin{\psi}^3\cos{\varphi}^2\cdot r^2-r^2\sin{\varphi}^2\sin{\psi}\cos{\psi}-r^2\cos{\psi}^2\cos{\varphi}^2\sin{\psi}\dots
\end{gathered}$$

---
##### 14. Oblicz pochodną $z'(t)$ funkcji złożonej $z=e^{x-2y}$, gdzie $x=\sin{t},y=t^3$

$$\begin{gathered}
z'(t)=e^{x-2y}\cdot (x-2y)'=e^{\sin{t}-2t^3}\cdot (\cos{t}-6t^2)\\\\
\text{lub traktując jako funkcje wielu zmiennych}\\\\
\frac{\partial z}{\partial x}=e^{x-2y}\\
\frac{\partial z}{\partial y}=e^{x-2y}\cdot (-2)\\
\frac{dx}{dt}=\cos{t}\\
\frac{dy}{dt}=3t^2\\
\frac{dz}{dt}=e^{x-2y}\cdot \cos{t}+e^{x-2y}\cdot (-2)\cdot 3t^2
\end{gathered}$$
---
##### 15. Oblicz pochodne cząstkowe $z'_u$ oraz $z_v'$ funkcji złożonej $z=x^2y-xy^2$, gdzie $x=u+v, y=u-v$

$$\begin{gathered}
\frac{\partial z}{\partial u}=\frac{\partial z}{\partial x}\cdot \frac{\partial x}{\partial u}+\frac{\partial z}{\partial y}\cdot \frac{\partial y}{\partial u}=\frac{\partial z}{\partial x}+\frac{\partial z}{\partial y}=
2xy-y^2+x^2-2xy=x^2-y^2
\\\\

\frac{\partial z}{\partial v}=\frac{\partial z}{\partial x}\cdot \frac{\partial x}{\partial v}+\frac{\partial z}{\partial y}\cdot \frac{\partial y}{\partial v}=\frac{\partial z}{\partial x}-\frac{\partial z}{\partial y}=2xy-y^2-(x^2-2xy)=4xy-y^2-x^2
\end{gathered}$$

---
##### 16. Rozwiąż równanie różniczkowe cząstkowe $yz'_x-xz'_y=0$, gdzie $z=z(x,y)$, przyjmując nowe zmienne $u=x, v=x^2+y^2$.

$$\begin{gathered}
\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}\frac{\partial u}{\partial x}+\frac{\partial z}{\partial v}\frac{\partial v}{\partial x}\\\\
\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}+2x \frac{\partial z}{\partial v}\\\\

\frac{\partial z}{\partial y}=\frac{\partial z}{\partial u}\frac{\partial u}{\partial y}+\frac{\partial z}{\partial v}\frac{\partial v}{\partial y}\\\\
\frac{\partial z}{\partial y}=2y \frac{\partial z}{\partial v}\\\\

y\frac{\partial z}{u}+2xy \frac{\partial z}{\partial v}-2xy \frac{\partial z}{\partial v}=0\\
y \frac{\partial z}{\partial u}=0\\\\
\text{Zatem }y=0 \text{ lub funkcja zalezy jedynie od }v \text{ i przyjmuje postac: }z=\varphi(x^2+y^2)
\end{gathered}$$
Czyli innymi slowami - badajac przyrost (zależność) funkcji od danej zmiennej $(x)$ gdy zechcemy wprowadzic nową zmienną $(u)$ zależną od zmiennej $x$ to zależność funkcji równa sie iloczynowi zależności funkcji od $u$ oraz zależności zmiennej / funkcji $u$ od $x$.

---
##### 17. Sprawdź, czy funkcja $f(x,y)=e^{x+y}$ jest dwukrotnie różniczkowalna w $\mathbb{R}^2$. Jeśli tak, to oblicz różniczkę zupełną 2-go rzędu $d^2f$

$$\begin{gathered}
f(x,y)=e^{x+y}\\
\frac{\partial^2 f}{\partial x^2}=e^{x+y}\\
\frac{\partial^2 f}{\partial y^2}=e^{x+y}\\
\frac{\partial^2 f}{\partial x\partial y}=e^{x+y}\\
\frac{\partial^2 f}{\partial y\partial x}=e^{x+y}\\\\
\text{Istnieją pochodne cząstkowe i są ciągłe więc 2-krotnie }\\
\text{różniczkowalna}\\\\
d^2f=\frac{\partial^2 f}{\partial x^2}(dx)^2+2\frac{\partial^2 f}{\partial x \partial y}dx dy+\frac{\partial^2 f}{\partial y^2}(d_y)^2\\
d^2f=e^{x+y}(dx)^2+2e^{x+y}dx dy+e^{x+y}(d_y)^2\\

\end{gathered}$$

---
##### 18. Dana jest funkcja $f(x,y)=\left\{\begin{matrix}\frac{x^3y-xy^3}{x^2+y^2}, \ \ \ (x,y)\neq (0,0)\\ 0, \ \ \ (x,y)=(0,0)\end{matrix}\right.$  Sprawdź czy pochodne mieszane tej funkcji w punkcie $(0,0)$ są sobie równe.

$$\begin{gathered}
\frac{\partial f}{\partial y}(0,0)=\lim_{\Delta y\to 0}\frac{f(0,\Delta y)-f(0,0)}{\Delta y}=\\=\lim_{\Delta \to 0}{\frac{\frac{0^3\Delta y-0\Delta y ^3}{0^2+(\Delta y )^2}}{\Delta y}}=0\\\\

\frac{\partial^2 f}{\partial x \partial y}(0,0)=\lim_{\Delta x\to 0}\frac{\frac{\partial f}{\partial y}(\Delta x, 0)-\frac{\partial f}{\partial y}(0,0)}{\Delta x}=\\
=\lim_{\Delta x\to 0}{\frac{\frac{\partial f}{\partial y}(\Delta x, 0)-0}{\Delta x}}\dots\\\\
\frac{\partial f}{\partial y}(\Delta x, 0)=\lim_{\Delta y \to 0}\frac{f(\Delta x, \Delta y)-f(\Delta x, 0)}{\Delta y}=\lim_{\Delta y\to 0}\frac{\frac{(\Delta x)^3 \Delta y - \Delta x (\Delta y)^3}{(\Delta x)^2 +(\Delta y)^2}-\frac{(\Delta x)^3 0-\Delta x\cdot 0}{(\Delta x)^2+0^2}}{\Delta y}=\\
=\lim_{\Delta y \to 0}\frac{(\Delta x)^3-\Delta x (\Delta y)^2}{(\Delta x)^2+(\Delta y)^2}=\Delta x\\\\
\dots = \lim_{\Delta x \to 0}{\frac{\Delta x}{\Delta x}}=1\\\\
\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}\frac{f(\Delta x, 0)-f(0,0)}{\Delta x}=\lim_{\Delta x\to 0}{\frac{\frac{(\Delta x)^3\cdot 0-\Delta x\cdot 0^3}{(\Delta x)^2+(\Delta y)^2}}{\Delta x}}=0\\\\
\frac{\partial ^2 f}{\partial y \partial x}(0,0)=\lim_{\Delta y\to 0}{\frac{\frac{\partial f}{\partial x}(0, \Delta y)-\frac{\partial f}{\partial x}(0,0)}{\Delta y}}=\dots\\\\
\frac{\partial f}{\partial x}(0, \Delta y)=\lim_{\Delta x\to 0}{\frac{f(\Delta x, \Delta y)-f(\Delta x, 0)}{\Delta x\to 0}}=\lim_{\Delta x\to 0}{\frac{\frac{(\Delta x)^3\Delta y-\Delta x (\Delta y)^3}{(\Delta x)^2+(\Delta y)^2}-\frac{0^3\Delta y-0\cdot (\Delta y)^3}{0^2+(\Delta y)^2 }}{\Delta x}}=\\
=\lim_{\Delta x\to 0}\frac{(\Delta x)^2\Delta y-(\Delta y)^3}{(\Delta x)^2+(\Delta y)^2}=-\Delta y\\\\
\dots = \lim_{\Delta y\to 0}{\frac{-\Delta y}{\Delta y}}=-1\\\\
\text{ Różne pochodne cząstkowe}
\end{gathered}$$

---
##### 27. Oblicz wszystkie pochodne cząstkowe pierwszego i drugiego rzędu funkcji uwikłanej $z = z(x, y)$ danej równaniem $x^2 + 2y^2 + 3z^2 + xy − z − 9 = 0$ w punkcie $(1, −2), (z = 1).$


