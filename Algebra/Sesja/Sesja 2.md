
###### 7) Znajdź rzut prostokątny punktu $P=(6,4,0)$ na prostą oraz punkt symetryczny do $P$ względem tej prostej
$$\begin{gathered}
\left\{
\begin{matrix}
x=6+6t\\
y=4+3t\\
z=-6t
\end{matrix}
\right.\\\\
v=[6,3,-6]\\
PQ(t)=(6t,3t,-6t)\ \\\text{ wzór na wektor od punktu na prostej wyznaczonego przez t do punktu P}\\\\
PQ(t)\circ v=36t+9t+36t=81t=0\implies t=0\\
Q(t)=(6+6t,4+3t,-6t)\\
Q(0)=(6,4,0)\\\\
\text{P leży na prostej więc P' też.}
\end{gathered}$$
---
###### 9) Znajdź odległość prostej $l:\frac{x-2}{1}=\frac{y+3}{2}=\frac{z-2}{-1}$ od płaszczyzny:

$$\begin{gathered}
\pi: \left\{
\begin{matrix}
x=1-s+t\\
y=2-2s-2t\\
z=-1+s-t
\end{matrix}
\right.
\end{gathered}$$

$$\begin{gathered}
l:\frac{x-2}{1}=\frac{y+3}{2}=\frac{z-2}{-1}\\
\left\{
\begin{matrix}
x=2+t_l\\
y=-3+2t_l\\
z=2-t_l
\end{matrix}
\right.\\\\
P_l=(2,-3,2)\\
P_\pi=(1,2,-1)\\\\
d(l,\pi)=\frac{|n\circ (P_\pi-P_l)|}{|n|}\\\\
n=\begin{vmatrix}
i&j&k\\
-1&-2&1\\
1&-2&-1
\end{vmatrix}=[4,0,4]\\\\
d(l,\pi)=\frac{|[4,0,4]\circ (-1,5,-3)|}{\sqrt{32}}=\frac{16}{4\sqrt{2}}=2\sqrt{2}
\end{gathered}$$

---
###### 10) Dana jest prosta $l$ oraz płaszczyzna $\pi_1$. Znajdź równanie ogólne płaszczyzny $\pi$ zawierającej prostą $l$ i prostopadłej do płaszczyzny $\pi_1$. Zbadaj wzajemne położenie prostej $l$ i krawędzi $k$ przecięcia się płaszczyzn $\pi$ i $\pi_1$

$$\begin{gathered}
l:\left\{
\begin{matrix}
3x-2y+z=3\\
x-2z=0
\end{matrix}
\right., \ \ \ 
\pi_1:x+y+z+8=0\\\\
n_{\pi_1}=[1,1,1]\\
n_{{l}_1}=[3,-2,1]\\
n_{{l}_2}=[1,0,-2]\\\\
\left\{
\begin{matrix}
3x-2y+z=3\\
x-2z=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\frac{7z-3}{2}=y\\
x=2z
\end{matrix}
\right.\implies P_1=(2,1,2)\\\\
v_l=P_2-P_1=(4,2,\frac{11}{2})-(2,1,2)=(2,1,\frac{7}{2})\\\\
n_\pi = n_{\pi_1}\times v_l=\begin{vmatrix}
i&j&k\\
1&1&1\\
2&1&\frac{7}{2}
\end{vmatrix}=(\frac{5}{2},-\frac{3}{2},-1)\\\\
\pi:[x-2,y-1,z-2]\circ n_\pi=0\\
\pi:\frac{5}{2}x-5-\frac{3}{2}y+\frac{3}{2}-z+2=0\\\\
\pi:5x-10-3y+3-2z+4=0\\\\
\pi: 5x-3y-2z-3=0\\\\
\end{gathered}$$

$$\begin{gathered}
k:\left\{
\begin{matrix}
5x-3y-2z-3=0\\
x+y+z+8=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\frac{-7z-43}{8}=y\\
x=\frac{-z-21}{8}\\
z=z
\end{matrix}
\right.\\

\end{gathered}$$

---
###### 11) Znajdź punkt symetryczny do punktu $P=(2,3,-1)$ względem prostej:

$$\begin{gathered}
P\notin l\\\\\

l:\left\{
\begin{matrix}
x+y=0\\
y+z=0
\end{matrix}
\right.
\left\{
\begin{matrix}
x=-y\\
z=-y\\
y=y
\end{matrix}
\right.
\implies v_l=[-1,1,-1]\\\\
Q(t)\text{ - punkt na prostej zależnie od t}\\\\
Q(t)=t(-1,1,-1)\\\\
PQ(t)\text{ - wektor od punktu P do punktu Q(t)}\\\\
PQ(t)=[-t-2,t-3,-t+1]\\\\
\text{Sprawdzamy kiedy wektor }PQ(t) \text{ jest prostopadły do prostej }l\\\\
PQ(t)\circ v_l=0\\
[-t-2,t-3,-t+1]\circ [-1,1,-1]=0\\
t+2+t-3+t-1=0\\
3t-2=0\\
t=\frac{2}{3}\\\\
Q'=P+2[-\frac{2}{3}-2,\frac{2}{3}-3,-\frac{2}{3}+1]=(2,3,-1)+2[-\frac{8}{3},-\frac{7}{3},\frac{1}{3}]=\\\\
=(2,3,-1)+[-\frac{16}{3},-\frac{14}{3},\frac{2}{3}]=[-\frac{10}{3},-\frac{5}{3},-\frac{1}{3}]
\end{gathered}$$
---
###### 12) Zbadaj wzajemne położenie prostej $l$ prostopadłej do płaszczyzny $\pi: y=2+z$ i przechodzącej przez punkt $A=(1,2,0)$ oraz prostej $k$ przechodzącej przez punkt $B=(0,3,-1)$ i równoległej do prostej, wyznacz odległość prostych $l$ i $k$. Wyznacz objętość równoległościanu rozpiętego przez wersory prostych $l$ i $k$ oraz wektor $\overrightarrow{AB}$.
$$\begin{gathered}
k':\left\{
\begin{matrix}
x+y-z=-1\\
x-2y-z=2
\end{matrix}
\right.
\\\\
l=(1,2,0)+t(v_l)\\
v_l=(0,-1,0)\\
l=(1,2,0)+t(0,-1,0)\\\\
k=(0,3,-1)+t_k(v_k)\\
v_k=v_{k'}:\\
\left\{
\begin{matrix}
x+y-z=-1\\
x-2y-z=2

\end{matrix}
\right.
\left\{
\begin{matrix}
y=-1\\
x=z
\end{matrix}
\right.\implies v_{k'}=[1,0,1]\\\\
k=(0,3,-1)+t_k[1,0,1]\\
\not \exists a:a\cdot t_k=t\implies l\not \parallel k\\\\
\left\{
\begin{matrix}
t_k=1\\
-1=t\\
0=-1+t_k
\end{matrix}
\right.\checkmark \implies P=(0,3,-1)+[1,0,1]=[1,3,0]\\\\
\text{Skoro proste mają punkt przecięcia,ich odlełość jest równa 0}\\\\
\text{wersor prostej}l: a\cdot |v_l|=1 \implies a\cdot 1 = 1\implies a=1\\
w_l=1\cdot v_l=[0,-1,0]\\\\
\text{wersor prostej }k:a\cdot |v_k|=1\\
a\cdot \sqrt{2}=1\\
a=\frac{\sqrt{2}}{2}\\
\implies \\
w_k=\frac{\sqrt{2}}{2}[1,0,1]=[\frac{\sqrt{2}}{2},0,\frac{\sqrt{2}}{2}]\\\\
\end{gathered}$$

$$\begin{gathered}
V_{r}=|(w_l\times w_k)\circ \overrightarrow{AB}|=\begin{vmatrix}
i&j&k\\
0&-1&0\\
\frac{\sqrt{2}}{2}&0&\frac{\sqrt{2}}{2}
\end{vmatrix}\circ [-1,1,-1]=\\\\
=|[\frac{\sqrt{2}}{2},0,\frac{\sqrt{2}}{2}]|=\sqrt{1}=1
\end{gathered}$$

---
###### 1) Sprawdź, które z podanych odwzorowań są liniowe:

a) L: $\mathbb{R}[x] \to \mathbb{R}[x]$, $(Lp)(x)=xp'(x)+p(1)$
$$\begin{gathered}
(Lp)(x_1+x_2)=(x_1+x_2)p'(x_1+x_2)+p(1)\\\\
(Lp)(x_1)+(Lp)(x_2)=x_1p'(x_1)+x_2'p'(x_2)+p(1)+p(1)\\\\
\text{Różne np dla:}\\
f(x)=x\\
(Lp)(x_1+x_2)=x_1+x_2+1\\
(Lp)(x_1)+(Lp)(x_2)=x_1+x_2+1+1
\end{gathered}$$

---

b) $L: \mathbb{R}[x]\to \mathbb{R}[x], (Lp)(x)=p(x)p'(x)$
