### Geometria analityczna
#### 2024-12-17
##### Poprzednia: [[Algebra - 10]]
##### Następna: [[Algebra - 12]]
##### Zadania: [[]]

#geometria_analityczna #algebra 

--- 
### Przestrzenie euklidesowe

W przestrzeni $\mathbb{R}^3$ przyjmujemy *prawokrętny (zgodny z regułą prawej ręki)* układ współrzednych, którego osie rozpięte są przez *wersory* (wektory długości 1):
$$\begin{gathered}
\vec{i}=(1,0,0),\ \vec{j}=(0,1,0),\ \vec{k}=(0,0,1)
\end{gathered}$$

Dowolny element $P=(x,y,z)$ przestrzeni $\mathbb{R}^3$ *interpretować* będziemy *geometrycznie* na trzy sposoby, jako:
- punkt
- wektor zaczepiony w środku układu współrzędnych ($\vec{OP}$)
- wektor swobodny o współrzędnych x,y,z

Przestrzeń $\mathbb{R}^n$ (składającą się z punktów i wektorów), gdzie w przestrzeni wektorów swobodnych określony jest iloczyn skalarny $\circ$ nazywamy *przestrzenia euklidesową* i oznaczamy $E_n$.

---

**Oznaczenie:**
$P=(x,y,z)$ - punkt  $v=[x,y,z]$ - wektor

$\vec{\mathbb{R}^n}$ - zbiór (przestrzeń wektorów   $\mathbb{R}^n$ - zbiór punktów $E_n$ - przestrzeń euklidesowa.

---
**Definicja**:
*Uporządkowana* trójka *liniowo niezależnych* wektorów:
$u=[u_1,u_2,u_3], \ v=[v_1,v_2,v_3],\ w=[w_1,w_2,w_3] \in \overrightarrow{E_3}$ tworzy układ *prawoskrętny*, jeżeli:
$$\begin{gathered}
\begin{vmatrix}
u_1&u_2&u_3\\
v_1&v_2&v_3\\
w_1&w_2&w_3\\
\end{vmatrix}
\gt 0
\end{gathered}$$
---
### Odległość punktów, długość wektora

**Definicja**:
Odległością euklidesową punktów $P=(x_1,\dots,x_n) \in \mathbb{R}^n$ i $Q=(y_1,\dots,y_n) \in \mathbb{R}^n$ nazywamy liczbę:
$$\begin{gathered}
d(P,Q)=\sqrt{\sum^{n}_{i=1}{(y_i-x_i)^2}}
\end{gathered}$$
*Przykład*:
$$\begin{gathered}
P=(1,7,-4), \ \ Q=(-3,2,10)\\
d(P,Q)=\sqrt{(1+3)^2+(7-2)^2+(-4-10)^2}
\end{gathered}$$
---
**Uwaga**:
Dla dowolnych punktów
$$\begin{gathered}
P=(x_1,\dots,x_n), \ \ \ Q=(y_1,\dots,y_n)\in \mathbb{R}^n\\
\overrightarrow{PQ}=[y_1-x_1,y_2-x_2,\dots,y_n-x_n]
\end{gathered}$$

---
**Długość wektora (norma Euklidesowa)**:
Wynika z powyższych:
$$\begin{gathered}
v=[v_1,\dots,v_n]\in \overrightarrow{\mathbb{R}^n} \\
||v||=\sqrt{\sum^{n}_{i=1}{v_i^2}}
\end{gathered}$$

*Przykład*
$$\begin{gathered}
v=[8,-3,2]\\
||v||=\sqrt{64+9+4}
\end{gathered}$$
Zatem:
$$\begin{gathered}
d(P,Q)=||\overrightarrow{PQ}||
\end{gathered}$$
---
**Własności normy**:
1. $||u|| \geq 0$, przy czym $||u||=0 \Leftrightarrow u=\overline{0}$
2. $||\alpha u||=|\alpha| \cdot ||u||$
3. $||u+v||\leq ||u||+||v||$ (analogia do nierówności trójkąta)

---
### Iloczyn skalarny

**Definicja**:
Standardowym *iliczynem skalarnym wektorów* $u=[u_1,\dots,u_n]$ i $v=[v_1,\dots,v_n]$ w przestrzeni $\overrightarrow{\mathbb{R}^n}$ nazywamy liczbę:
$$\begin{gathered}
u \circ v = \sum^{n}_{i=1}{u_iv_i}=u_1v_1+\dots+u_nv_n
\end{gathered}$$
*Przykład*:
$$\begin{gathered}
u=[9,-2,3], \ \ v=[2,-1,3]\\
u\circ v = 18+2+9
\end{gathered}$$
---
**Własności iloczynu skalarnego**:
1. $u\circ v = v\circ u$
2. $(\alpha u)\circ v=\alpha(u\circ v)$
3. $(u+v)\circ w=u\circ w+v\circ w$
4. $v\circ v \geq 0$, gdzie $v\circ v=0\Leftrightarrow v=\overline{0}$, oraz $||v||=\sqrt{v\circ v}$
---
**Nierówność Cauchy'ego, Buniakowskiego, Schwarza**
Dla dowolnych wektorów $u=[u_1,\dots,u_n], \ v=[v_1,\dots,v_n] \in \overrightarrow{E_n}$
$$\begin{gathered}
|u\circ v| \leq ||u|| \cdot ||v||
\end{gathered}$$
gdzie *równość* zachodzi wtw, gdy $u,v$ są *liniowo zależne*.

---
### Kąt
**Definicja**:
*Kątem* między *niezerowymi* wektorami $u,v \in \overrightarrow{E_n}$ nazywamy taką liczbę $\varphi \in [0,\pi]$, dla której:

$$\begin{gathered}
\cos{\varphi}=\frac{u\circ v}{||u||\cdot ||v||}
\end{gathered}$$
Oznaczamy ją zazwyczaj jako $\angle(u,v)$
(*dokładnie jedna* taka liczba zawsze istnieje, gdyż na podstawie nierówności Schwarza:
$$\begin{gathered}
-1\leq \frac{u\circ v}{||u||\cdot ||v||}\leq 1
\end{gathered}$$
---
**Definicja**:
Niezerowe wektory $u,v \in \overrightarrow{E_n}$ nazywamy *prostopadłymi*, jeżeli $\angle(u,v)=\frac{\pi}{2}$ natomiast równoległymi gdy $\angle(u,v)=0 \vee \angle(u,v)=\pi$. Piszemy wówczas, odpowiednio $u\bot v$ lub $u\parallel v$. Ponadto, przyjmujemy, że wektor *zerowy* jest zarówno *prostopadły*, jak i *równoległy* do wszystkich innych wektorów.
$$\begin{gathered}
Zatem:\\
u\bot v \Leftrightarrow u\circ v=0
\end{gathered}$$
---
### Iloczyn wektorowy

**Twierdzenie**:
Dla dowolnych wektorów $u=[u_1,u_2,u_3], \ v=[v_1,v_2,v_3] \in \overrightarrow{E_3}$:

$$\begin{gathered}
u \times v = \left[
\begin{vmatrix}
u_2&u_3\\
v_2&v_3
\end{vmatrix},
\begin{vmatrix}
u_3&u_1\\
v_3&v_1
\end{vmatrix},
\begin{vmatrix}
u_1&u_2\\
v_1&v_2
\end{vmatrix},
\right]
\end{gathered}$$
---
**Uwaga**:
W praktyce wygodnie jest liczyć iloczyn wektorowy w następujący sposób:
$$\begin{gathered}
u\times v=
\begin{vmatrix}
\vec{i}&\vec{j}&\vec{k}\\
u_1&u_2&u_3\\
v_1&v_2&v_3
\end{vmatrix}=
\begin{vmatrix}
u_2&u_3\\
v_2&v_3
\end{vmatrix}\ \vec{i}+
\begin{vmatrix}
u_3&u_1\\
v_3&v_1
\end{vmatrix}\ \vec{j}+
\begin{vmatrix}
u_1&u_2\\
v_1&v_2
\end{vmatrix}\ \vec{k}
\end{gathered}$$
---

**Własności iloczynu wektorowego**:
1. $u\times v=-(v\times u)$
2. $(\alpha u)\times v=\alpha(u\times v)$
3. $u\times (v+w)=u\times v+u\times w$
4. $(u+v)\times w=u\times w+v\times w$
5. $||u\times v|| \leq ||u||\cdot ||v||$

---
**Twierdzenie**:
Niech $u,v \in \overrightarrow{E_3}$. Wówczas $u,v$ są *liniowo zależne* (równoległe) $\Leftrightarrow u\times v=\overline{0}$

---

**Twierdzenie**: 
Dla dowolnych $u,v \in \overrightarrow{E_3}$, liczba $||u\times v||$ określa *pole równoległoboku* rozpiętego przez wektory $u$ i $v$.
![[diagram-20241217.png]]
**Wniosek**:
*Pole trójkąta* rozpiętego przez wektory $u,v \in \overrightarrow{E_3}=\frac{1}{2}||u\times v||$

---
### Iloczyn mieszany

**Definicja**:
*Iloczynem mieszanym* uporządkowanej trójki wektorów $u,v,w \in \overrightarrow{E_3}$ nazywamy liczbę:
$$\begin{gathered}
(u\times v)\circ w
\end{gathered}$$
**Uwaga**:
Dla dowolnych $u,v,w \in \overrightarrow{E_3}$ liczba $|(u\times v)\circ w|$ określa *objętość równoległościanu* rozpiętego przez wektory $u, v$ oraz $w$ 

![[diagram-20241218 (4).png]]

---
**Wniosek**:
*Objętość czworościanu* rozpiętego przez $u,v,w \in \overrightarrow{E_3}$ wyraża się wzorem $\frac{1}{6}|(u\times v)\circ w|$

---
**Twierdzenie**:
Jeżeli $u=[u_1,u_2,u_3], \ v=[v_1,v_2,v_3], w=[w_1,w_2,w_3] \in \overrightarrow{E_3}$ to:

$$\begin{gathered}
(u\times v)\circ w =
\begin{vmatrix}
u_1&u_2&u_3\\
v_1&v_2&v_3\\
w_1&w_2&w_3\\
\end{vmatrix}
\end{gathered}$$
---
### Przykłady:

###### Sprawdź, czy punkty są współliniowe, jeżeli nie wyznacz pole $\triangle ABC$:
$$\begin{gathered}
A(-1,1,1), \ B(2,-1,0), \ C(1,-1,3)\\\\
v=\overrightarrow{AB}=(3,-2,-1), \ \ u=\overrightarrow{AC}=(2,-2,2)\\
v\times u = 
\begin{vmatrix}
k&i&j\\
3&-2&-1\\
2&-2&2\\
\end{vmatrix}=
[-4-2,-2-6,-6+4]=[-6,-8,-2] \neq \overline{0}\\
P_{\triangle ABC}=\frac{1}{2}||v\times u]=\frac{1}{2}\sqrt{36+64+4}=\sqrt{26}\\\\


\end{gathered}$$
---
###### Sprawdź, czy punkty są współpłaszczyznowe, jeżeli nie wyznacz długość wysokości głównej czworościanu ABCD wychodzącej z wierzchołka D.

$$\begin{gathered}
A(-1,1,1),\ B(2,-1,0), \ C(1,-1,2), \ D(3,2,-1)\\\\

v=\overrightarrow{AB}=[3,-2,-1], \ \ u=\overrightarrow{AC}=[2,-2,1], \ \ w=\overrightarrow{AD}=[4,1,-2]\\\\
v\times u=
\begin{vmatrix}
i&j&k\\
3&-2&-1\\
2&-2&1
\end{vmatrix}=[-2-2,-2-3,-6+4]=[-4,-5,-2]
\\\\
(v\times u) \circ w = [-4,-5,-2]\circ [4,1,-2]=-16-5+4=-17\neq 0 \\\\
P_{ABCD}=\frac{1}{6}\cdot ||(v\times u)\circ w||=\frac{17}{6}\\\\
P_{p}=\frac{1}{2}||[-4,-5,-2]||=\frac{1}{2}\sqrt{16+25+4}=\frac{1}{2}\sqrt{45}\\\\
V=\frac{1}{3}p_pH=\frac{1}{3}\cdot \frac{1}{2}\sqrt{45}\cdot H=\frac{17}{6}\\\\H=\frac{17}{\sqrt{45}}
\end{gathered}$$
---
### Płaszczyzna w $E_3$:

**Definicja**:
Dla ustalonego punktu $P_0=(x_0,y_0,z_0) \in E_3$ oraz wektora $n=[A,B,C] \in \overrightarrow{E_3}, \ n \neq \overline{0}$, zbiór punktów:
$$\begin{gathered}
\pi=\{P=(x,y,z) \in E_3:\overrightarrow{P_0P}\bot n\}
\end{gathered}$$

nazywamy *płaszczyzną* (w przestrzeni $E_3$), a wektor n *wektorem normalnym płaszczyzny* (prostopadłym do płaszczyzny)

**Uwaga**:
$\overrightarrow{P_0P}\bot n \Leftrightarrow \overrightarrow{P_0P}\circ n=0$

**Czyli płaszczyzne możemy zdefiniować poprzez ustalenie punktu oraz pewnej prostej prostopadłej do tej płaszczyzny. Każdy punkt naszej płaszczyzny musi tworzyć prostą z tym punktem która jest prostopadła do tamtej prostej**

---

**Definicja**:
Współrzędne punktów $P=(x,y,z) \in E_3$ tworzących daną płaszczyznę $\pi$ określone mogą być poprzez następujące równania:

*Równanie normalne płaszczyzny* (wynikające z iloczynu skalarnego i prostopadłości prostych)
   gdzie $P_0=(x_0,y_0,z_0)\in \pi, n=[A,B,C] \bot \pi, n \neq \overline{0}$ :
   $$\begin{gathered}
\pi: [x-x_0,y-y_0,z-z_0]\circ [A,B,C]=0 \Leftrightarrow A(x-x_0)+B(y-y_0)+C(z-z_0)=0
\end{gathered}$$
*Równanie ogólne płaszczyzny* (wynikające z przekształcenia równania normalnego)
   gdzie $P_0=(x_0,y_0,z_0)\in \pi, n=[A,B,C] \bot \pi, n \neq \overline{0}$ :
   $$\begin{gathered}
\pi=Ax+By+Cz+D=0, \ D\in \mathbb{R}
\end{gathered}$$
*Równanie parametryczne płaszczyzny* (wynikające z dwóch wektorów rozpinających płaszczyzne i wskazujących na każdy punkt)
   gdzie 
$P_0=(x_0,y_0,z_0)\in \pi, u=[u_1,u_2,u_3], v=[v_1,v_2,v_3]\in \overrightarrow{E_3}$ są *liniowo niezależne* i $u\parallel \pi, v \parallel \pi$
   
   $$\begin{gathered}
\pi: \left\{
\begin{matrix}
x=x_0+su_1+tv_1\\
y=y_0+su_2+tv_2\\
z=z_0+su_3+tv_3\\

\end{matrix} \ \ s,t \in \mathbb{R}
\right.
\end{gathered}$$ 
![[diagram-20241218 (1).png]]
*Równanie odcinkowe płaszczyzny*: (można po prostu przekształcić ogólne/normalne)
   $$\begin{gathered}
\pi=\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1, \ \ a,b,c\neq 0\\\\
\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1 \Leftrightarrow \overset{Ax+}{bcx}+\overset{By+}{acy}+\overset{Cz+}{abz}\overset{D}{-abc}=0
\end{gathered}$$
![[diagram-20241218 (3).png]]

---
### Przykłady:

###### Znajdź równania normalne, ogólne, parametryczne i odcinkowe płaszczyzny $\pi$ zawierającej punkty:
$$\begin{gathered}
A=(-1,-2,2), \ \ B(0,-2,4),\ \ C=(-1,-3,5)\\\\
\overrightarrow{AB}=[1,0,2] \parallel \pi , \ \ \overrightarrow{AC}=[0,-1,3] \parallel \pi\\\\
n=\overrightarrow{AB}\times \overrightarrow{AC}=
\begin{vmatrix}
k&i&j\\
1&0&2\\
0&-1&3
\end{vmatrix}=[2,-3,-1]\neq \overline{0} \implies \overrightarrow{AB}, \overrightarrow{AC} - liniowo \ niezalezne\\\\
Rownanie \ normalne:\\
\pi:2(x+1)-3(y+2)-1(z-2)=0\\\\
Rownanie \ ogólne:\\
\pi:2x-3y-z-2=0\\\\
Rownanie \ parametryczne:\\
\pi:\left\{
\begin{matrix}
x=-1+1\cdot s+0\cdot t\\
y=-2+0\cdot s-1\cdot t\\
z=2+2\cdot s+3\cdot t\\
\end{matrix}
\right.\\\\
Rownanie \ odcinkowe:\\
\frac{x}{1}+\frac{y}{-\frac{2}{3}}+\frac{z}{-2}=1
\end{gathered}$$
---
### Prosta w $E_3$

**Definicja**:
Prostą l (w przestrzeni $E_3$) *przechodzącą przez punkt* $P_0=(x_0,y_0,z_0) \in E_3$ i *równoległą do wektora* $v=[a,b,c] \in \overrightarrow{E_3}, v\neq \overline{0}$ nazywamy zbiór punktów postaci:
$$\begin{gathered}
P=(x,y,z)=P_0+tv=(x_0,y_0,z_0)+t[a,b,c]
\end{gathered}$$
Wektor $v$ nazywamy *wektorem kierunkowym rozpinającym/tworzącym* prostej l.

**Definicja**:
Współrzędne punktów $P=(x,y,z)\in E_3$ tworzących daną prostą l określone mogą być przez następujące równania:
*Równanie parametryczne prostej* gdzie $P_0=(x_0,y_0,z_0) \in l, v=[a,b,c]\parallel l, v \neq \overline{0}$
   $$\begin{gathered}
l:\left\{
\begin{matrix}
x=x_0+at\\
y=y_0+bt\\
z=z_0+ct
\end{matrix}
\right.t \in \mathbb{R}
\end{gathered}$$
*Równanie kierunkowe prostej* $P_0=(x_0,y_0,z_0) \in l, v=[a,b,c]\parallel l, a,b,c\neq 0$:
   $$\begin{gathered}
l:\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}(=t)
\end{gathered}$$
*Równanie krawędziowe prostej* (gdzie $l \subset \pi_1, l \subset \pi_2, \pi_1: A_1x+B_1y+C_1z+D_1=0, \pi_2: A_2x+B_2y+C_2z+D_2=0, \ \pi_1,\pi_2 \ nie \ sa \ rownolegle)$
   $$\begin{gathered}
l:\left\{
\begin{matrix}
A_1x+B_1y+C_1z+D_1=0\\
A_2x+B_2y+C_2z+D_2=0\\
\end{matrix}
\right.
\end{gathered}$$
### Przykład:
###### Znając równanie krawędziowe prostej l:
$$\begin{gathered}
l:\left\{
\begin{matrix}
x+2y-3z+2=0\\
-x-y+z=0
\end{matrix}
\right.\\\\
I \ sposób:\\\\
l:\left\{
\begin{matrix}
z=t\\
y=-2+2t\\
x=2-t
\end{matrix}
\right.\\
\\
II \ sposób:\\
n_1=[1,2,-3] \bot \pi_1\\
n_2=[-1,-1,+1] \bot \pi_2\\
v=n_1\times n_2=
\begin{vmatrix}
i&j&k\\
1&2&-3\\
-1&-1&1\\
\end{vmatrix}=[-1,2,1] \parallel l\\\\
P_0: z=0\\\\
\left\{
\begin{matrix}
x+2y=-2\\
-x-y=0
\end{matrix}
\right. \left\{
\begin{matrix}
y=-2\\
x=2\\
z=0
\end{matrix}
\right.
\end{gathered}$$
---
### Odległości

#### Odległość punktu od płaszczyzny
Dane: płaszczyzna $\pi=Ax+By+Cz+D=0$ i punkt $Q=(x_1,y_1,z_1)$
$$\begin{gathered}
d(Q,\pi)=\frac{|Ax_1+By_1+Cz_1+D|}{\sqrt{A^2+B^2+C^2}}
\end{gathered}$$
---
#### Odległość płaszczyzn równoległych
Dane: płaszcyzny $\pi_1: Ax+By+Cz+D_1=0$ i $\pi_2=Ax+By+Cz+D_2=0$.
$$\begin{gathered}
d(\pi_1,\pi_2)=d(P_2,\pi_1)=\frac{|Ax_2+By_2+Cz_2+D_1|}{\sqrt{A^2+B^2+C^2}}=\frac{|D_1-D_2|}{\sqrt{A^2+B^2+C^2}}
\end{gathered}$$
---
#### Odległość punktu od prostej:
$$\begin{gathered}
d(P,l)=\frac{||\overrightarrow{P_0P}\times v||}{||v||}
\end{gathered}$$
---
### Wzajemne położenie 2 prostych w $E_3$ 

- *równoległe* (wliczamy tu przypadek, gdy się pokrywają)
- *przecinające się* (w jednym punkcie)
- *skośne* (nierównoległe i nieprzecinające się)

2. Jeżeli proste są *skośne*, to odległość między nimi, równa długości najkrótszego odcinka łączącego obie proste, można wyrazić wzorem:
   $$\begin{gathered}
d(l_1,l_2)=\frac{|(v_1\times v_2)\circ \overrightarrow{P_1P_2}|}{||v_1\times v_2||}
\end{gathered}$$

Ten wzór wynika z tego że gdy zbudujemy sobie równoległościan i zrobimy mu wysokość, to ta wysokość będzie stała, a w pewnym miejscu będzie łączyć te obie proste.
![[diagram-20241218 (5).png]]
3. Jeżeli $l_1\parallel l_2$, to $d(l_1,l_2)=d(P_1,l_2)$ - czyli po prostu odległość punktu od prostej, niezależnie od punktu będą takie same.

---
### Wzajemne położenie płaszczyzn w $E_3$ 

$$\begin{gathered}
\left\{
\begin{matrix}
A_1x+B_1y+C_1z=-D_1\\
A_2x+B_2y+C_2z=-D_2
\end{matrix}
\right.
\end{gathered}$$
Jeżeli powyższy układ stworzony z płaszczyzn o równaniach ogólnych ma:
- 0 rozwiązań to płaszczyzny są *równoległe* i nie są takie same
- $\infty$ rozwiązań zależnie od 1 parametru, to przecinają się wzdłuż prostej
- $\infty$ rozwiązań zależnie od 2 parametrów to płaszczyzny się pokrywają