### Geometria analityczna
#### 2024-12-18
##### Lekcja: [[Algebra - 11]]

#algebra #geometria_analityczna 

---
###### 1. Sprawdź, czy:
wektory $u=[-1,3,-5], v=[1,-1,1],w=[4-2,0]$ są współpłaszczyznowe

$$\begin{gathered}
(u\times v)\circ w=
\begin{vmatrix}
-1&3&-5\\
1&-1&1\\
4&-2&0
\end{vmatrix}=
12+10-20-2=0 \implies tak
\end{gathered}$$
punkty $P=(0,0,0), Q=(-1,2,3,), R=(2,3,-4),S=(2,-1,5)$ są współpłaszczyznowe
$$\begin{gathered}
\overrightarrow{PQ}=[-1,2,3], \ \overrightarrow{PR}=[2,3,-4], \ \overrightarrow{PS}=[2,-1,5]\\\\
(\overrightarrow{PQ}\times \overrightarrow{PR})\circ \overrightarrow{PR}=
\begin{vmatrix}
-1&2&3\\
2&3&-4\\
2&-1&5
\end{vmatrix}=
-15-16-6-18+20+4=-33\neq 0\\
nie \ sa \ wspolplaszczyznowe
\end{gathered}$$

---
###### 2. Trójkąt ABC rozpięty jest na wektorach $\overrightarrow{AB}=[1,5,-3], \overrightarrow{AC}=[-1,0,4]$. Oblicz wysokość tego trójkąta opuszczoną z wierzchołka C.

$$\begin{gathered}
\overrightarrow{AB}\times \overrightarrow{AC}=
\begin{vmatrix}
i&j&k\\
1&5&-3\\
-1&0&4
\end{vmatrix}=
[20,-1,5]\\
P_{\triangle ABC}=\frac{1}{2}|[20,-1,5]|=\frac{1}{2}\cdot \sqrt{400+1+25}=\frac{1}{2}\sqrt{426}\\\\
P_{\triangle ABC}=\frac{1}{2}\cdot H\cdot |AB|=\frac{1}{2}H\cdot \sqrt{35}\\
H=\sqrt{\frac{426}{35}}
\end{gathered}$$
---
###### 3. Proste $l_1$ i $l_2$ dane są równaniami parametrycznymi:
$$\begin{gathered}
l_1:\left\{
\begin{matrix}
x=1-4t\\
y=-2t\\
z=2+4t
\end{matrix}
\right.\ \ \ \ \ 
l_2:\left\{
\begin{matrix}
x=6+6t\\
y=4+3t\\
z=-6t
\end{matrix}
\right.
\end{gathered}$$

Wykaż że $l_1$ i $l_2$ są równoległe. Oblicz odległość między nimi. Znajdź równanie ogólne ich wspólnej płaszczyzny.

$$\begin{gathered}
P_1=(1,0,2), \ \ \ P_2=(6,4,0)\\
v_1=[-4,-2,4], \ \ \ v_2=[6,3,-6]\\\\
v_1\times v_2=
[0,0,0]=\overline{0}\\
d(P_1,l_2)=\frac{||\overrightarrow{P_0P}\times v_2||}{||v_2||}=\frac{||[5,4,-2]\times [6,3,-6]||}{\sqrt{36+9+36}}=\frac{|[-18,18,-9]|}{9}=\frac{\sqrt{729}}{9}=3
\end{gathered}$$


---
###### 4. Zbadaj wzajemne położenie prostych
$$\begin{gathered}
l_1:\left\{
\begin{matrix}
x=2-t\\
y=3+2t\\
z=-3t
\end{matrix}
\right.\ \ \
l_2:\left\{
\begin{matrix}
x=-3+2t\\
y=1+2t\\
z=-3
\end{matrix}
\right.\\\\
P_1=(2,3,0), \ \ \ P_2=(-3,1,-3)\\
v_1=[-1,2,-3], \ \ \ v_2=[2,2,0]\\\\
v_1\times v_2=[-6, -6,-6]\neq \overline{0}\\
\left\{
\begin{matrix}
2-t=-3+2t\\
3+2t=1+2t\\
-3t=-3
\end{matrix}
\right. \ \ \ 3+2t=1+2t \implies 3=1, \ sprzeczne\\\\
Proste \ sa \ skosne \ wiec \ nie \ generuja \ plaszczyzny
\end{gathered}$$
Znajdź równanie normalne ich wspólnej płaszczyzny (jeżeli istnieje).

---
###### 5. Zbadaj wzajemne położenie prostych
$$\begin{gathered}
l_1:\left\{
\begin{matrix}
x=1+2t\\
y=t\\
z=2
\end{matrix}
\right.\ \ \
l_2:\left\{
\begin{matrix}
x=3\\
y=t\\
z=-t
\end{matrix}
\right.\\\\
P_1=(1,0,2),  \ \ \ P_2(3,0,0)\\
v_1=[2,1,0], \ \ \ v_2=[0,1,-1]\\\\

v_1\times v_2=
\begin{bmatrix}
i&j&k\\
2&1&0\\
0&1&-1
\end{bmatrix}
[-1,-2,2]\neq \overline{0}\\
\left\{
\begin{matrix}
1+2t=3\\
t=t\\
2=-t
\end{matrix}
\right.
\left\{
\begin{matrix}
1+2t=3\\
t=t\\
-2=t
\end{matrix}
\right.
\left\{
\begin{matrix}
1-4=3\\
t=t\\
-2=t
\end{matrix}
\right., \ sprzeczne
\\
Proste \ sa \ skosne \ nie \ generuja \ plaszczyzny.\\\\
d(l_1,l_2)=\frac{||(v_1\times v_2)\circ \overrightarrow{P_1P_2}||}{|v_1\times v_2|}=\frac{|[-1,-2,2]\circ [2,0,-2]|}{\sqrt{9}}=\frac{|-2-4|}{3}=2
\end{gathered}$$
---
###### 6. Napisz równanie ogólne płaszczyzny $\pi$ przechodzącej przez punkty $A=(-1,2,4), \ B=(2,1,3)$ i $C=(3,-1,5)$. Wyznacz odległość punktu $Q=(5,0,8)$ od płaszyzny $\pi$ oraz znajdź punkt symetryczny do punktu $Q$ względem tej płaszczyzny.
$$\begin{gathered}
\overrightarrow{AB}=[3,-1,-1], \ \ \overrightarrow{AC}=[4,-3,1]\\
\overrightarrow{AB}\times \overrightarrow{AC}=
\begin{bmatrix}
i&j&k\\
3&-1&-1\\
4&-3&1
\end{bmatrix}=[-4,-7,-5]\\\\
-4(x-3)-7(y+1)-5(z-5)=0\\
-4x+12-7y-7-5z+25=0\\
-4x-7y-5z+30=0\\\\
d(Q,\pi)=\frac{|Ax_1+By_1+Cz_1+D|}{\sqrt{A^2+B^2+C^2}}\\\\
d(Q,\pi)=\frac{|-4\cdot 5-7\cdot0 -5\cdot 8+30|}{\sqrt{16+49+25}}=\frac{|-30|}{\sqrt{90}}=\frac{10}{\sqrt{10}}=\sqrt{10}\\\\
Q'=(x',y',z')\\
\left\{
\begin{matrix}
x'=5-4t\\
y'=0-7t\\
z'=8-5t
\end{matrix}
\right.
\sqrt{(-4t)^2+(-7)^2+(-5t)^2}=2\sqrt{10}
\sqrt{90t^2}=2\sqrt{10}\\
3\sqrt{10}|t|=2\sqrt{10}
t=\frac{2}{3}\\
x'=5-\frac{8}{3}\\
\dots
\end{gathered}$$
---
