### Całki podwójne potrójne itd
#### 2025-06-15
##### Poprzednia: [[Analiza 10 Funkcje uwikłane]]
##### Następna: [[]]
##### Zadania: ]]

#całki #rachunek_całkowy 

---
## Całka podwójna po prostokącie

$P$ - prostokąt $\subset \ \mathbb{R}^2$
$f: P \to \mathbb{R}$

Tworzymy podział $\pi_n$ prostokąta $P$ na $n$ małych prostokątów $P_1, P_2, \dots, P_n$
$\delta n$ - średnica podziału - długość najdłuższej przekątnej prostokątów $P_1,P_2,\dots,P_n$.
Tworzymy ciąg podziałów:

$\pi_1: P_1$
$\pi_2: P_1,P_2$
$\vdots$
$\pi_n: P_1,P_2,\dots,P_n$

Mówimy, że ciąg podziałów $(\pi_n)_{n\in \mathbb{N}}$ jest normalny $\Leftrightarrow \ \lim_{n\to \infty}{\delta_n}=0$
$\forall i=1,\dots,n$ wybierzemy punkt pośredni $(c_i,d_i)\in P_i$
Tworzymy sumę całkowitą $S_n=\sum^{n}_{i=1}{f(c_i,d_i)\cdot |P_i|}$ (gdzie $|P_i|$ to pole prostokąta $P_i$)

**Def.**
Jeśli dla dowolnego normalnego ciągu podziałów prostokąta $P$ istnieje granica właściwa ciągu sum całkowych $S_n$ i granica ta nie zależy ani od wyboru ciągu podziałów, ani od wyboru punktów pośrednich, to granicę tę nazywamy **całką podwójną funkcji $f$ po prostokącie P** i oznaczamy symbolem:
$$\begin{gathered}
\underset{P}{\int \int}{f(x,y)dxdy}(=\lim_{n\to \infty}S_n)
\end{gathered}$$

Mówimy wtedy, że $f$ jest całkowalna po prostokącie $P$.


**Jest to analogia do definicji zwykłej całki:**
###### def.

$f:[a,b]\to \mathbb{R}$, ograniczona 
Tworzymy ciąg podziałów $(P_n)_{n\in \mathbb{N}}$ przedziału $[a,b]$
$P_n:a=x_0\lt x_1\lt x_2\lt\dots\lt x_i \lt \dots \lt x_n=b$
$x_0,\dots,x_n$ - punkty podziału
$\Delta x_i=x_i-x_{i-1}, i=1,\dots,n$
$\delta_n=max\{x_i-x_{i-1}:i=1,\dots,n\}$ - średnica podziału $P_n$ 
Ciąg podziałów $(P_n)_{n\in \mathbb{N}}$ nazywamy *normalnym* $\Leftrightarrow \lim_{n\to \infty}{\delta_n=0}$
Niech $P_n$ będzie podziałem przedziału $[a,b]$
W każdym z przedziałów $[x_{i-1},x_{i}]$ wybieramy punkt pośredni $c_1: \forall i=1,\dots,n \ c_i\in [x_{i-1}, x_i]$.
Niech $S_n=\sum^{n}_{i=1}{f(c_i)\Delta x_i}$ - suma całkowa dla podziału $P_n$ przy ustalonym wyborze punktów pośrednich.

**Def.**
Jeśli dla każdego normalnego ciągu podziałów przedziału $[a,b]$ i dowolnego wyboru punktów pośrednich $c_i$ istnieje $\lim_{n\to \infty}{S_n}$ która nie zależy ani od wyboru ciągu podziałów, ani od wyboru punktów pośrednich, to granicę tę nazywamy całką Riemenna funkcji $f$ na przedziale $[a,b]$

$$\begin{gathered}
\int^{b}_{a}{f(x)\ dx}=\underset{\delta_n\to 0}{\lim_{n\to \infty}}{\sum^{n}_{i=1}f(c_i)\Delta x_i}
\end{gathered}$$

---

### WW na całkowalność funkcji po prostokącie

Jeżeli $f$ jest ciągła na prostokącie $P$, to $f$ jest całkowalna po prostokącie $P$

**ciągła na P $\implies$ całkowalna po P**

---
### Fubiniego

zał: $P=[a_1,b_1]\times [a_2,b_2]$
$f: P\to \mathbb{R}$ całkowalna po prostokącie $P$

teza:

1) $[a_1,b_1]\ni x\to \varpi(x)=\int^{b_2}_{a_2}{f(x,y) dy}$
   
   Funkcja $\varphi(x)$ jest całkowalną w sensie Riemenna na przedziale $[a_1,b_1]$
2) 
   
   $$\begin{gathered}
\underset{P}{\int \int}{f(x,y)dxdy}=\int^{b_1}_{a_1}\left[\int^{b_2}_{a_2}{f(x,y) dy}\right]dx\\ \left(=\int^{b_1}_{a_1}{\varphi(x)dx=\int^{b_1}_{a_1}dx}
\int^{b_2}_{a_2}{f(x,y)dy}
\right)
\end{gathered}$$

---
## Całka podwójna po obszarze ograniczonym

$D\subset \mathbb{R}^2 \ \ \exists P$ - prostokąt  $D\subset P$, $D$ - ograniczony

**Def. Funkcją charakterystyczną** zbioru $D$ nazywamy funkcę

$$\begin{gathered}
\chi_D(x,y)=\left\{
\begin{matrix}
1, \ \ (x,y)\in D\\
0, \ \ (x,y)\notin D
\end{matrix}
\right.
\end{gathered}$$
**Uwaga.** $f:P\to \mathbb{R}$

$$\begin{gathered}
(f\cdot \chi_D)(x,y)=\left\{
\begin{matrix}
f(x,y), \ \ \ (x,y)\in D\\
0, \ \ \ (x,y) \notin D
\end{matrix}
\right.
\end{gathered}$$

**Def. Całką podwójną funkcji $f$ po zbiorze ograniczonym $D$ nazywamy:**

$$\begin{gathered}
\underset{P}{\int \int}{f(x,y)dxdy}=
\underset{P}{\int \int}{(f\chi_D)(x,y)dxdy}
\end{gathered}$$


**Def. Obszarem normalnym względem osi OX nazywany obszar $D=\{(x,y)\in \mathbb{R}^2: x\in[a,b], \varphi(x)\leq y \leq \Psi(x)\}$, gdzie $\varphi, \Psi: [a,b]\to \mathbb{R}$ są ciągłe**

No i analogicznie względem osi $OY$

---
### Twierdzenie o zamianie całki podwójnej na całke iterowaną dla obszaru normalnego względem osi $OX$

Zał: $D=\{(x,y)\in \mathbb{R}^2: x\in [a,b], \varphi(x)\leq y \leq \Psi(x)\}, \varphi, \psi:[a,b]\to \mathbb{R}$ ciągłe
$f:D\to\mathbb{R}$ ciągła

Teza:
$$\begin{gathered}
\underset{D}{{\int \int}}f(x,y)dxdy=\int^{b}_{a}\left(\int^{\Psi(x)}_{\varphi(x)}f(x,y)dy\right)dx
\end{gathered}
$$


**Pyrzykład:**

$$\begin{gathered}
\underset{D}{\int \int}{e^{\frac{x}{y}}dx\ dy}, \ \ D=\left\{\begin{matrix}
y=\sqrt{x}\\
x=0\\
y=1
\end{matrix}
\right.\\\\

D=\{(x,y): y\in[0,1] \ \underset{\varphi(y)}{0}\leq x\leq \underset{\Psi(y)}{y^2}\}\\\\
\underset{D}{\int \int}{e^{\frac{x}{y}}dx\ dy}=\int^{1}_{0}dy\int^{y^2}_{0}e^{\frac{x}{y}}dx=\int^{1}_{0}dy\left[ye^{\frac{x}{y}}\right]^{y^2}_0=\\=\int^{1}_{0}{dy(ye^y-y)}=\dots\\\\
\end{gathered}$$


---
### Twierdzenie o całce z sumy

zał: $f,g: D\to \mathbb{R}$ całkowalne
$D$ - obszar normalny względem jednej z osi 

teza: $\forall \alpha, \beta \in \mathbb{R} \ \ \ \underset{D}{\int \int}{(\alpha \cdot f+\beta \cdot g)(x,y) dxdy}=\alpha \underset{D}{\int \int}f(x,y)dxdy+\beta \underset{D}{\int \int}g(x,y)dxdy$

---
### Twierdzenie analogiczne do $\int^{c}_{a}{f(x)dx}=\int^{b}_{a}{f(x)dx}+\int^{c}_{b}{f(x) dx}$

zał: $D_1, D_2$ - obszary normalne względem jednej z osi 
$int \ D_1 \cap int\  D_2=\emptyset$
$f: D_1 \cup D_2 \to \mathbb{R}$ całkowalna

teza:
$$\begin{gathered}
\underset{D_1\cup D_2}{\int \int}{f(x,y) dxdy}=
\underset{D_1}{\int \int}{f(x,y) dxdy}+
\underset{D_2}{\int \int}{f(x,y) dxdy}
\end{gathered}
$$

---
**Def.** Obszar $D$ nazywamy **obszarem regularnym** $\Leftrightarrow$

1) $D=D_1\cup D_2 \cup \dots \cup D_n$
2) $\forall i =1, \dots, n \ \ D_i$ - obszar normalny względem jednej z osi 
3) $\forall i,j \in \{1,\dots,n\}\ \ \ i\neq j \implies int D_i \cap D_j =\emptyset$

---
### Twierdzenie o całce po obszarze regularnym

Jeśli $f: D\to \mathbb{R}$ ciągła i $D$ - obszar regularny, to $f$ jest całkowalna na $D$ i zachodzi wzór:

$$\begin{gathered}
\underset{D}{\int \int}f(x,y) dxdy=\sum^{n}_{i=1}{\underset{D_i}{\int \int}} f(x,y) dx dy
\end{gathered}$$
---
### Twierdzenie o zamianie zmiennych w całce podwójnej 

zał: $f: D\to \mathbb{R}$ - ciągła
$D$ - regularny
$\Phi: D'\to D$
$\Phi$ przeprowadzka $int \ D'$ na $int \ D$
$D'\ni (u,v) \to \Phi(u,v)=(x(u,v), y(u,v))\in D$
$\Phi'(u,v)$ - macierz Jacobiego funkcji $\Phi$ 
$J(u,v)=\det \Phi'(u,v)$ - jakobian
$\forall (u,v)\in int \ D' \ \ \ J(u,v)\neq 0$

teza: $\underset{D}{\int \int}f(x,y) dxdy=\underset{D}{\int \int}f(x(u,v),y(u,v))\cdot |J(u,v)| dudv$

---
### Współrzędne biegunowe

$x=x(r,\varphi)=r\cos{\varphi}$
$y=y(r,\varphi)=r\sin{\varphi}$

**Przykład:**

$$\begin{gathered}
D=\{(x,y): x\in [0,R], 0\leq y\leq \sqrt{R^2-x^2}\}\\\\
r\in [0,R], \ \ \ \varphi\in [0,\frac{\pi}{2}]\\
D'=\{(r,\varphi): r\in[0,R], \ \varphi\in [0,\frac{\pi}{2}]\}\\
\Phi: (r,\varphi)\to (r\cos{\varphi}, r\sin{\varphi})\\
J(r,\varphi)=r\\\\
bo:\\\\
\Phi'(r,\varphi)=\begin{bmatrix}
\cos{\varphi}&-r\sin{\varphi}\\
\sin{\varphi}&r\cos{\varphi}
\end{bmatrix}\\\\
J(r,\varphi)=\det \Phi'(r,\varphi)=\cos{\varphi}\cdot r\cos{\varphi}-(-r\sin\cdot \sin{\varphi})=r(\cos^2{\varphi}+\sin^2{\varphi})=r
\end{gathered}$$

Zatem **Tw. o przejściu na współrzedne biegunowe w całce podwójnej prezentuje się jako:**

zał: $\left\{\begin{matrix}x=r\cos{\varphi}\\y=r\sin{\varphi}\end{matrix}\right.$

$D'=\{(r,\varphi), r\in \dots, \varphi\in \dots\}$
$D=\{(x,y),\dots\}$
$\Phi: D'\ni (r,\varphi)\to (x,y)\in D$
$f: D\to \mathbb{R}$ ciągła

teza: $\underset{D}{\int \int}f(x,y) dx dy = \underset{D}{\int \int}f(r\cos{\varphi}, r\sin{\varphi})\cdot r \ dr \ d \varphi$

**Przykład:**
$$\begin{gathered}
\underset{D}{\int \int}y\ dx dy, \ \ \ \text{gdzie }D \text{ - ćwiartka koła o promieniu }R\text{ w I ćw. układu współrzędnych}\\\\
D'=\{(r,\varphi): r\in [0,R], \varphi\in [0,\frac{\pi}{2}]\}\\\\
\underset{D}{\int \int}y \ dx \ dy=
\underset{D'}{\int \int}r\sin{\varphi}\cdot r \ dr \ d \varpi=\int^{R}_{0}dr \int^{\frac{\pi}{2}}_{0}r^2\sin{\varphi}\ d \varphi=\int^{R}_{0}r^2 dr[-\cos{\varphi}]^{\frac{\pi}{2}}_0=\\
=\int^{R}_{0}r^2 dr \left(-\cos{\frac{\pi}{2}}-(-\cos0)\right)=\int^{R}_{0}r^2 dr (0+1)=\left[\frac{r^3}{3}\right]^R_0=\frac{R^3}{3}
\end{gathered}$$

---
### Twierdzenie o interpretacji geometrycznej całki podwójnej

zał: $D$ - regularny 
$f: D\to \mathbb{R}_+$ ciągła

teza: objętość bryły $V=\{(x,y,z)\in \mathbb{R}^3: (x,y)\in D, 0\leq z\leq f(x,y)\}$ jest równa $|V|=\underset{D}{\int \int}f(x,y) dx dy$

---
### Wzór na objętość obszaru

zał: $V=\{(x,y,z)\in \mathbb{R}^3: (x,y) \in D, \varphi(x,y) \leq z \leq \Psi(x,y)\}$
gdzie $D$ - obszar regularny 
$\varphi, \Psi: D\to \mathbb{R}$ ciągłe

teza: $|V|=\underset{D}{\int \int}[\Psi(x,y)-\varphi(x,y)]dx dy$

**Przykład:**
Oblicz objętość bryły ograniczonej powierzchniami $z=\sqrt{x^2+y^2}$ oraz $z=2-x^2-y^2$

Powierzchnie tworzą nam coś jak wycinek kuli i to właśnie to mamy policzyć:
![[newplot (14)-Photoroom.png]]
Skoro to jest ograniczone dwoma powierzchniami interesuje nas tylko taki obszar który zawiera się między ich przecięciem:
$$\begin{gathered}
z=2-x^2-y^2=2-(x^2+y^2)\\
\Psi(x,y)=2-(x^2+y^2)\\
\varphi(x,y)=\sqrt{x^2+y^2}\\\\
\left\{
\begin{matrix}
z=\sqrt{x^2+y^2}\\
z=2-(x^2+y^2)
\end{matrix}
\right.\\
\downarrow\\
z=2-z^2\\
z^2+z-2=0\\
\Delta = 1+8=9\\
z_1=-2 \ \ \ z_2=1\\
1=\sqrt{x^2+y^2}\\
1=x^2+y^2\\
\downarrow\\
D=K((0,0),1) - \text{okrąg o promieniu 1 o środku } (0,0)
\end{gathered}$$

Co możemy zobaczyć z góry:
![[newplot (16)-Photoroom.png]]
Zatem wiedząc gdzie sie przecinają możemy wyprowadzić sobie obszar (czyli ten okrąg jak zauważyliśmy wcześniej) ale od razu przejdźmy na biegunowe:

$$\begin{gathered}
D=\{(x,y): x\in[-1,1], -\sqrt{1-x^2}\leq y\leq \sqrt{1-x^2}\}\\
\downarrow\\
D'=\{(r,\varphi): r\in[0,1], \varphi\in[0,2\pi]\}\\\\
|V|=\underset{D}{\int\int}\left[(2-x^2-y^2)-\sqrt{x^2+y^2}\right]dxdy=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
|J|=r\\
r\in[0,1]\\
\varphi\in[0,2\pi]
\end{vmatrix}=\\\\
=\int^{1}_{0}dr \int^{2\pi}_{0}\left[(2-r^2)-r\right]\cdot rd\varphi=2\pi \int^{1}_{0}{2r-r^3-r^2 \ dr}=2\pi\left(r^2-\frac{r^4}{4}-\frac{r^3}{3}\right)^1_0=\\\\=2\pi (1-\frac{1}{4}-\frac{1}{3})=\frac{5\pi}{6}
\end{gathered}$$
---
### Zastosowanie całki podwójnej w fizyce

$D$ - obszar regularny
- Pole powierzchni obszaru $D: \ \ |D|=\underset{D}{\int \int}dx dy$
  $\rho: D\to \mathbb{R}_+$ gęstość powierzchniowa masy, ładunku elektrycznego$\dots$
- Masa obszaru $D: M=\underset{D}{\int \int}\rho(x,y) dx dy$
- Moment statyczny względem osi $OX$ obszaru $D$
  $M_{OX}=\underset{D}{\int \int}y\rho(x,y) dx dy$
  względem osi $OY$
  $M_{OY}=\underset{D}{\int \int}x\rho(x,y) dx dy$
- Środek ciężkści obszaru $D$
  $\left\{\begin{matrix}x_0=\frac{M_{OY}}{M} \\ y_0=\frac{M_{OX}}{M}\end{matrix}\right.$
- Moment bezwładności względem punktu $(0,0)$ obszaru $D$
  $M_B=\underset{D}{\int \int}(x^2+y^2)\rho(x,y) dx dy$

---
## Całka potrójna 

### Całka potrójna po prostopadłościanie 

$P=[a_1,b_1]\times [a_2,b_2]\times [a_3,b_3]$

- Tworzymy ciąg podziałów prostopadłościanu $P$
  Podział prostopadłościanu $P$: dzielimy prostopadłościan $P$ na $n$ mniejszych prostopadłościanów $P_1,P_2,\dots,P_n$
- $\forall i=1,\dots,n \ (c_i,d_i,e_i)\in P_i$
- Ciąg podziałów nazywamy normalnym, jeśli $\lim_{n\to \infty}\delta_n=0$ gdzie $\delta_n$ - najdłuższa przekątna tych prostopadłościanów 
- $f: P\to \mathbb{R}$ (funkcja trzech zmiennych)
- Tworzymy sumy całkowe $S_n=\sum^{n}_{i=1}{f(c_i,d_i,e_i)\cdot |V_i|}$ gdzie $V_i$ to objętość prostopadłościanu $P_i$


$$\begin{gathered}
\underset{P}{\int \int \int}f(x,y,z)dxdydz=\lim_{n\to \infty}S_n
\end{gathered}$$
o ile ta granica nie zależy ani od wyboru ciągu podziałów normalnych, ani wyboru punktów pośrednich

**Def. Całką potrójną funkcji $f$ po zbiorze ograniczonym $V\subset \mathbb{R}^3$ nazywamy:**

$$\begin{gathered}
\underset{V}{\int\int \int}{f(x,y,z)\underset{dV}{dxdydz}}=
\underset{P}{\int\int \int}{(f\chi_D)(x,y,z)dxdydz}
\end{gathered}$$

**Def. Obszarem normalnym względem osi OXY nazywany obszar $V=\{(x,y,z)\in \mathbb{R}^2: (x,y)\in D, \Phi(x)\leq z \leq \Psi(x)\}$, gdzie D jest obszarem regularnym $\subset \mathbb{R}^2$**

---
### Twierdzenie - całka iterowana dla obszaru normalnego względem płaszczyzny $OXY$

zał: $V$ - obszar normalny względem płaszczyzny $OXY$
$f: V\to \mathbb{R}$ - ciągła

teza:
$$\begin{gathered}
\underset{V}{\int \int \int}f(x,y,z) dx dy dz=\underset{D}{\int \int}dx dy \int^{\Psi(x,y)}_{\Phi(x,y)}f(x,y,z) dz
\end{gathered}$$
Jeśli ponadto obszar $D$ jest normalny względem osi $OX$, to:

$$\begin{gathered}
\underset{V}{\int \int \int}f(x,y,z) dx dy dz=\int^{b}_{a}dx\int^{\psi(x,y)}_{\varphi(x,y)}dy \int^{\Psi}_{\Phi}f(x,y,z) dz
\end{gathered}$$
**Przykład:**
$\underset{V}{\int \int \int}xDV$, gdzie $V$ jest ograniczony płaszczyznami $x=0, y=0, z=0, x+y+z=1$

1. Rzutujemy obszar $V$ na płaszczyzne $OXY$
2. $z=0 \ \ \ \Phi(x,y)=0$
   $\Psi(x,y)=1-x-y$
   $\underset{V}{\int \int \int}x dv = \underset{D}{\int \int}dx dy \int^{1-x-y}_{0}xdz=*$
3. $y=\psi(x)=1-x$
   $y=\varphi(x)=0$
   $*=\int^{1}_{0}dx \int^{1-x}_{0}dy \int^{1-x-y}_{0}xdz=\int^{1}_{0}x dx \int^{1-x}_{0}dy[z]^{1-x-y}_0=$
   $=\int^{1}_{0}dx \int^{1-x}_0(1-x-y-0)dy=\int^{1}_{0}x dx [y=xy-\frac{1}{2}y^2]^{1-x}_0=$
   $=\int^{1}_{0}dx[1-x-x(1-x)-\frac{1}{2}(1-x)^2]=\int^{1}_{0}xdx[1-2x+x^2-\frac{1}{2}+x-\frac{1}{2}x^2]=\dots$

**Def. Obzarem regularnym** (w $\mathbb{R}^3)$ nazywamy sumę skończonej liczby obszarów normalnych względem pewnej płaszczyzny $(OXY, OXZ, OYZ)$
$V=V_1\cup V_2\cup \cup \dots \cup V_n \ \ \ int V_i \cap int V_j = \emptyset \ \ \forall_{i, j}$

---
### Współrzędne sferyczne

Wybieramy jeden ze sposobów:

$$\begin{gathered}
\begin{matrix}
\left\{
\begin{matrix}
x=r\sin\theta \cos{\varphi}\\
y=r\sin{\theta}\sin \varphi\\
z=r\cos{\theta}
\end{matrix}
\right.\\
r\geq 0\\
\varphi \in [0,2\pi]\\
\theta \in [0,\pi]\\
|J|=r^2\sin{\theta}
\end{matrix}&
\begin{matrix}
\left\{
\begin{matrix}
x=r\cos{\theta}\cos{\varphi}\\
y=r\cos{\theta}\sin{\varphi}\\
z=r\sin{\theta}
\end{matrix}
\right.\\
r\geq 0\\
\varphi \in [0,2\pi]\\
\theta\in [-\frac{\pi}{2}, \frac{\pi}{2}]\\
|J| = r^2\cos{\theta}
\end{matrix}
\end{gathered}$$


**Wizualizacja by nie musieć wzorów pamiętać**
![[diagram-20250703 (2).png]]

**Analogicznie dla pierwszego sposobu z tym że kąt $\theta$ idzie od osi $OZ$ do $XOY$. (Czyli wzory takie same po podstawieniu $\frac{\pi}{2}-\theta$ w miejsce $\theta$ tak praktycznie nie zmienia to nic oprócz zamiany $\cos{\theta}$ na $\sin{\theta}$ i na odwrót**
![[diagram-20250705.png]]

**Jak pamiętać Jakobiany?**
Wystarczy zapamiętać że $|J|=r\cdot a$, dla pierwszego rysunku mamy wtedy $r^2 \cos{\theta}$. A dla drugiego $r\cdot r\cos{(\frac{\pi}{2}-\theta)}=r^2 \sin{\theta}$


**Zastosowanie całki potrójnej**

- Objętość bryły $V: |V|=\underset{V}{\int \int \int}dV$
  $\rho: V\to \mathbb{R}_+$ gęstość masy, ładunku elektrycznego$\dots$
- Masa bryły $V: M=\underset{V}{\int \int \int}\rho(x,y,z) dx dy dz$
- Momenty statyczne bryły $V$ względem płaszczyzn:
  $M_{OXY}=\underset{V}{\int \int \int}z\cdot \rho(x,y,z)dV$
  $M_{OYZ}=\underset{V}{\int \int \int}x\cdot \rho(x,y,z)dV$
  $M_{OXZ}=\underset{V}{\int \int \int}y\cdot \rho(x,y,z)dV$
- Środek ciężkości bryły $V$
  $x_0=\frac{M_{OYZ}}{M}\ \ y_0=\frac{M_{OXZ}}{M} \ \ z_0=\frac{M_{OXY}}{M}$
- Moment bezwładnosci bryły $V$ względem osi $OZ$
  $M_b=\underset{V}{\int \int \int}(x^2+y^2)\rho(x,y,z)dV$
---
