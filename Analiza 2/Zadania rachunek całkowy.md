u
##### 1. Oblicz całki:

###### a) $\underset{D}{\int \int}{\frac{x^2}{y^2}}dxdy$, gdzie $D$ jest ograniczony krzywymi: $y=\frac{1}{x}, \ y=x$ oraz $x=2$

$$\begin{gathered}
D=\{(x,y): x\in[1,2], \frac{1}{x}\leq y\leq x\}\\\\
\int^{2}_{1}\left(\int^{x}_{\frac{1}{x}}\frac{x^2}{y^2}dy\right)dx=\int^{2}_{1}x^2[-\frac{1}{y}]^x_{\frac{1}{x}}=\int^{2}_{1}{x^2(-\frac{1}{x}+\frac{1}{\frac{1}{x}})}=\\=
\int^{2}_{1}{-x+x^3}=[\frac{x^4}{4}-\frac{x^2}{2}]^2_1=4-2-\frac{1}{4}+\frac{1}{2}=\frac{9}{4}
\end{gathered}$$

###### b) $\int^{R}_{0}dx \int^{\sqrt{R^2-x^2}}_{0}{\ln{1+x^2+y^2}dx dy}$

Przejdźmy sobie na współrzędne biegunowe (tym razem rozpiszemy wszystko)

$$\begin{gathered}\\
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\\\
\Phi(r,\varphi)=(r\cos{\varphi}, r\sin{\varphi})\\
\Phi'(r,\varphi)=\begin{bmatrix}
\cos{\varphi}&-r \sin{\varphi}\\
\sin{\varphi}&r \cos{\varphi}
\end{bmatrix}\\\\
J=r \cos^2{\varphi}-(-r \sin^2{\varphi})=r\\\\

\underset{D}{\int \int}f(x,y) dxdy=\underset{D}{\int \int}f(x(u,v),y(u,v))\cdot |J(u,v)| dudv
\\\\

\int^{R}_{0}dx \int^{\sqrt{R^2-x^2}}_{0}{\ln{(1+x^2+y^2)}dx dy}=\\=
\int^{\frac{\pi}{2}}_{0}d \varphi \int^{R}_{0}{\ln{(1+r^2)}\cdot r \ dr}=(1):\\\\\\

\int{\ln{(1+r^2)r \ dr}}=\begin{vmatrix}
u=1+r^2\\
du=2r \ dr
\end{vmatrix}=\frac{1}{2}\int{\ln{u}}=\\=\begin{vmatrix}
x=\ln{u}&dx=\frac{1}{u}\\
dy=1&y=u
\end{vmatrix}=\frac{1}{2}(\ln{u}\cdot u-u)=\\=\frac{1}{2}(1+r^2)(\ln{(1+r^2)-1)}\\\\
(1)=\int^{\frac{\pi}{2}}_{0}{(\frac{1}{2}(1+R^2)(\ln{(1+R^2)-1)} +\frac{1}{2})d \varphi}=\\=\frac{\pi}{2}
(\frac{1}{2}(1+R^2)(\ln{(1+R^2)-1)} +\frac{1}{2})
\end{gathered}$$

###### c) $\underset{D}{\int\int}\sqrt{a^2-x^2-y^2}dxdy$, gdzie $D$ jest ograniczony krzywą $(x^2+y^2)^2=a^2(x^2-y^2)$

$$\begin{gathered}
\left\{
\begin{matrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}
\end{matrix}
\right.\\\\
r^4=a^2(r^2\cos^2{\varphi}-r^2\sin^2{\varphi})\\
r^2=a^2(\cos^2{\varphi}-\sin^2{\varphi})\\
r=a \sqrt{\cos{2\varphi}}\\\\

\end{gathered}$$![[diagram-20250616.png]]
$$\begin{gathered}
D=\{(r,\varphi):\varphi\in[0,2\pi], 0\leq r\leq a\sqrt{\cos{2\varphi}}\}\\\\
\underset{D}{\int\int}\sqrt{a^2-x^2-y^2}dxdy=
4\cdot \int^{\frac{\pi}{2}}_{0}d\varphi\int^{a\sqrt{\cos{2\varphi}}}_{0}\sqrt{a^2-r^2}dr =\\
=4\cdot \int^{\frac{\pi}{2}}_{0}d\varphi \left[-\frac{\sqrt{(a^2-r^2)^3}}{3}\right]^{a \sqrt{2\cos \varphi}}_0=\\=
4\cdot \int^{\frac{\pi}{2}}_{0}d\varphi \left(-\frac{a(\sqrt{1-\cos{2\varphi}}-1)}{3}\right)=
\\
=4\cdot \int^{\frac{\pi}{2}}_{0}d\varphi \left(-\frac{a(\sqrt{1-\cos{2\varphi}}-1)}{3}\right)=
\\=-\frac{4a}{3}\int^{\frac{\pi}{2}}_{0}\sqrt{1-\cos{2\varphi}}-1
=\\
=-\frac{4a}{3}\int^{\frac{\pi}{2}}_{0}{2\sin^2\varphi-1=\\
}\dots
\end{gathered}
$$

---
###### d) $\underset{V}{\int \int \int}(x^2+y^2)dv$, gdzie $a^2\leq x^2+y^2+z^2\leq b^2, \ z\geq 0$
$$\begin{gathered}
z\geq 0 \land z^2\leq b^2-x^2-y^2\\\\
\underset{V}{\int \int \int}(x^2+y^2)dv=\\=4\cdot \int^{b}_{0}dx\int^{\sqrt{b^2-x^2}}_{0}dy\int^{\sqrt{b^2-x^2-y^2}}_{0}(x^2+y^2)dz-4\cdot \\\int^{a}_{0}dx\int^{\sqrt{a^2-x^2}}_{0}dy\int^{\sqrt{a^2-x^2-y^2}}_{0}(x^2+y^2)dz=\\
=4\cdot \int^{b}_{a}dx \int^{\sqrt{b^2-x^2}}_{0}dy \sqrt{b^2-x^2-y^2}(x^2+y^2)=*\\\\\
*=\int{ \sqrt{b^2-x^2-y^2}(x^2+y^2)dy}=\begin{vmatrix}
u=x^2+y^2\\
du=2y dy\\
dy=\frac{du}{2y}=\frac{du}{\sqrt{u-x^2}}
\end{vmatrix}=\\
=
\end{gathered}$$


$$\begin{gathered}
x=r\cos{\beta}\cos{\alpha}\\
y=r\cos{\beta}\sin{\alpha}\\
z=r\sin{\beta}\\
|J|=r^2\cos{\beta}\\\\
a^2\leq x^2+y^2+z^2\leq b^2\\\\\
\underset{V}{\int \int \int}(x^2+y^2)dv=\\=\int^{2\pi}_{0}d\alpha \int^{\frac{\pi}{2}}_{0}\int^{b}_{a}(r^2\cos^2{\beta}\cos^2{\alpha}+r^2\cos^2\beta\sin^2\alpha)r^2\cos{\beta}dr=\\
=\int^{2\pi}_{0}\int^{\frac{\pi}{2}}_{0}\int^{b}_{a}r^4\cos^3{\beta}\ dr=
\int^{2\pi}_{0}\int^{\frac{\pi}{2}}_{0}\cos^3{\beta}(\frac{b^5}{5}-\frac{a^5}{5})\ d \beta=\\=
\int^{2\pi}_{0}\int^{\frac{\pi}{2}}_{0}\cos^3{\beta}(\frac{b^5}{5}-\frac{a^5}{5})\ d \beta=*\\\\
*=\int{\cos^3{\beta} d\beta}=\int{\cos{\beta}(1-\sin^2{\beta})}=\begin{vmatrix}
u=sin{\beta}\\
du=\cos{\beta} d \beta
\end{vmatrix}=\\
=\int{1-u^2\ du}=\sin-\frac{\sin^3}{3}\\\\\
\dots=\int^{2\pi}_{0}(\sin(\frac{\pi}{2})-\frac{\sin \frac{\pi}{2}}{3})\cdot (\frac{b^5}{5}-\frac{a^5}{5})
\end{gathered}$$
---
##### 2. Znajdź środek ciężkości jednorodnej figury ograniczonej krzywymi $y=\ln{x}, y=0, x=e$

![[diagram-20250617.png]]
$$\begin{gathered}
D=\{(x,y): x\in [1,e] \land 0\leq y\leq \ln x\}\\\\

\end{gathered}$$$D$ - obszar regularny
- $\rho: D\to \mathbb{R}_+$ gęstość powierzchniowa masy, ładunku elektrycznego$\dots$
- Masa obszaru $D: M=\underset{D}{\int \int}\rho(x,y) dx dy$
- Moment statyczny względem osi $OX$ obszaru $D$
  $M_{OX}=\underset{D}{\int \int}y\rho(x,y) dx dy$
  względem osi $OY$
  $M_{OY}=\underset{D}{\int \int}x\rho(x,y) dx dy$
- Środek ciężkści obszaru $D$
  $\left\{\begin{matrix}x_0=\frac{M_{OY}}{M} \\ y_0=\frac{M_{OX}}{M}\end{matrix}\right.$

$$\begin{gathered}
M=\underset{D}{\int \int}p \ dx dy=\int^{e}_{1}dx \int^{\ln x}_{0}p \ dy=p\int^{e}_1\ln{x}=p\left[x\ln{x}+x\right]^e_
1=p(2e-1)\\\\

M_{OX}=\underset{D}{\int \int}yp(x,y) dx dy=\int^{e}_{1}dx\int^{\ln{x}}_{0}py \ dy=p\int^{e}_{1}\left[\frac{\ln^2 x}{2}\right]

\end{gathered}
$$



$$\begin{gathered}
z=x^2+y^2&x^2+y^2-y=0&z=0\\\\\
\v
\end{gathered}$$