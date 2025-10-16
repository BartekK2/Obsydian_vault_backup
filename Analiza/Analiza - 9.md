## Zastosowania geometryczne całek
#### 2025-01-31
##### Poprzednia: [[Analiza - 8]]
##### Następna: [[Analiza - 9]]
##### Zadania: [[]]

#rachunek_całkowy #zastosowania_geometryczne_calek #analiza 

---
### Pole obszaru

**Twierdzenie:**
Zał: $\forall x \in [a,b] \phi(x)\leq \omega(x)$
$D=\{(x,y): x\in[a,b], \phi(x)\leq y\leq \omega(x)\}$
gdzie $\phi, \omega$ - to funkcje ciągłe w $[a,b]$ takie że $\phi$ zawsze mniejsze od $\omega$

Teza: $|D|=\int^{b}_{a}{(\omega(x) - \phi(x))\ dx}$

Dowód wyglądałby tak że jak mamy jakiś kształt, jakiś obszar na wykresie. To możemy podzielić go na "paski" których wysokość to właśnie $\omega(x)-\phi(x)$, więc sumujemy nieskończenie wiele takich pasków i cyk pyk mamy cały obszar, kształt.

#### Współrzędne biegunowe

$r$-promień wodzący
$\phi$ - kąt (biegunowy) skierowany
$\frac{x}{r}=\cos{\phi}$
$\frac{y}{r}=\sin{\phi}$
$\left\{\begin{matrix}x=r\cos{\phi}\\y=r\sin{\phi}\end{matrix}\right.$
$(r,\phi)$ - współrzędne biegunowe punktu

**Przykład:**
$$\begin{gathered}
(x^2+y^2)^2=a^2(x^2-y^2)\\
r^4=a^2(r^2\cos^2{\phi}-r^2\sin^2{\phi})\\
r^2=a^2(\cos^2{\phi}-\sin^2{\phi})
\end{gathered}$$

**Twierdzenie:**
Zał: $r(\phi)$ ciągła w $[\alpha,\beta]$, $r(\phi)\geq 0$
Teza:
$$\begin{gathered}
|D|=\frac{1}{2}\int^{\beta}_{\alpha}{r^2(\phi) \ d\phi}
\end{gathered}$$
Tutaj nie operujemy w układzie kartezjańskim lecz biegunowym, intuicyjnie można sobie wyobrazić ten wzór jako podzielenie kąta $2\pi$ na nieskończenie wiele małych kawałków, małych kątów. Pole trójkąta utworzonego z takiego małego wycinka przybliżyć można w ten sposób:
$$\begin{gathered}
\text{jaka to część okręgu? - }\frac{d\phi}{2\pi}\\\\
\frac{d\phi}{2\pi}\cdot \pi r^2=\frac{1}{2}r^2 d\phi 
\end{gathered}$$
I dodajemy sobie bo to całka riemanna zwiększając kąt tych wycinków.

---
**Przykład:**
Oblicz pole ograniczone lemniskatą Bernoulliego $(x^2+y^2)^2=a^2(x^2-y^2)$
$$\begin{gathered}
(x^2+y^2)^2=a^2(x^2-y^2)\\
r^4=a^2(r^2\cos^2{\phi}-r^2\sin^2{\phi})\\
r^2=a^2(\cos^2{\phi}-\sin^2{\phi})\\
r^2=a^2(\cos{2\phi})\\
r=a\sqrt{\cos{2\phi}}\implies k\pi -\frac{\pi}{4}\lt \phi \lt \frac{\pi}{4}+k\pi
\\\\
\frac{1}{4}|P|=\int^{\frac{\pi}{4}}_{0}{\frac{1}{2}a^2 \cos{2\phi} \ d\phi}=\frac{1}{4}a^2\int^{\frac{\pi}{2}}_{0}{\cos{\phi}}=\\
=\frac{1}{4}a^2(\sin{\frac{\pi}{2}-\sin{0}})=\frac{1}{4}a^2\\\\
P=a^2\\\\
\end{gathered}$$
---
### Krzywa zadana parametrycznie

$x=x(t),y=y(t),t\in [\alpha, \beta]$

**Przykład:**
Okrąg zadany parametrycznie:
$$\begin{gathered}
x(t)=r\cos(t)\\
y(t)=r\sin(t)
\end{gathered}$$

**Twierdzenie o polu obszaru ograniczonego krzywą zadaną parametrycznie:**

$$\begin{gathered}
Zał: L:\left\{
\begin{matrix}
x=\phi(t)\\
y=\omega(t)
\end{matrix}
\right., \ \ t\in [\alpha, \beta]\\\\
\forall t\in [\alpha,\beta]\ \ \omega(t)\geq 0\\
\forall t\in [\alpha, \beta] \ \ \phi'(t)\gt 0\\\\
\phi \in C^1([\alpha,\beta])\\
\omega \in C([\alpha,\beta])\\\\
D:\{(x,y)\in \mathbb{R}^2: \phi(\alpha)\leq x\leq \phi(\beta), 0\leq y\leq \omega(t), t\in [\alpha, \beta]\}\\\\
\text{Teza: }|D|=\int^{\beta}_{\alpha}{\omega(t)\cdot q'(t) \ dt}
\end{gathered}$$

---
**Przykład:**
Obliczyć pole obszaru ograniczonego elipsą $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$

$$\begin{gathered}
x(t)=a \cos{t}\\
y(t)=b \sin{t}\\
x'(t)=-a\sin{t}\\\\
\text{Wykres elipsy jest taki sam gdy zamienimy znak }a\\
\text{Zatem przy nowym }a \text{ równym }-a:\\
P_a=P_{-a}\\
x'(t)=-(-a)=a\sin{t}\\
x'(t)\gt 0 \Leftrightarrow t\in [0,\pi], y(t)\gt 0 \Leftrightarrow t\in [0,\pi]\\\\
|P|=2ab\cdot \int^{\pi}_{0}{\sin^2{t}\ dt}=
2ab\cdot \int^{\pi}_{0}{\frac{1-\cos{2t}}{2}\ dt}=\\
=ab(\int^{\pi}_{0}{1\ dt}-\int^{\pi}_{0}{cos{2t}\ dt})
=ab(\pi -\frac{1}{2}\int^{2\pi}_{0}{\cos{x}})=ab\pi

\end{gathered}$$


---
**Przykład 2:**
Obliczyć pole obszaru ograniczonego cykloidą:

$$\begin{gathered}
x=a(t-\sin{t})\\
(at-a\sin{t})'=1-\cos{t}\\
\\
y=a(1-\cos{t})\\
1-\cos{t}\gt 0 \ 
t\in [0,2\pi]\\\\
|P|=\int^{2\pi}_{0}{a(1-\cos{t})\cdot a(1-\cos{t})\ dt}=
a^2\int^{2\pi}_{0}{1-2\cos{t}+\cos^2{t}\ dt}=\\
=a^2(\int^{2\pi}_{0}{1 \ dt}+\int^{2\pi}_{0}{-2\cos{t} \ dt}+\int^{2\pi}_{0}{\cos^2{t} \ dt}=a^22\pi +\int^{2\pi}_{0}{\cos^2{\pi}}=\\\\=a^22\pi + a^2\int^{2\pi}_{0}{\frac{1+2\cos{2t}}{2}\ dt}=a^22\pi +a^2{\int^{2\pi}_{0}}{\frac{1}{2}}=3\pi \cdot a^2
\end{gathered}$$
---
###### 10. Oblicz pole figury ograniczonej krzywą $r=a\cos{3\phi}$
$$\begin{gathered}
\cos{3\phi}\gt 0\\
3\phi \in [2k\pi - \frac{\pi}{2}, 2k\pi +\frac{\pi}{2}]\\
3\phi \in [2k\pi - \frac{\pi}{2}, 2k\pi +\frac{\pi}{2}]\\
\phi \in [\frac{4k-1}{6}\pi , \frac{4k+1}{6}\pi]\\
(0,\frac{1}{6}\pi)\cup (\frac{3}{6}\pi , \frac{5}{6}\pi)\cup (\frac{7}{6}\pi , \frac{9}{6}\pi), (\frac{11}{6}\pi ,0)\\
\downarrow\\
(-\frac{1}{6}\pi,\frac{1}{6}\pi)\cup (\frac{3}{6}\pi , \frac{5}{6}\pi)\cup (\frac{7}{6}\pi , \frac{9}{6}\pi)\\
\downarrow\\
3 \text{ identyczne fragmenty}
\\\\
|P|=3\cdot \int^{\frac{\pi}{6}}_{-\frac{\pi}{6}}{\frac{1}{2}r^2(\phi)\ d\phi}=\frac{3}{2}a^2\cdot \int^{\frac{\pi}{6}}_{-\frac{\pi}{6}}{\cos^2{3\phi}\ d\phi}=\begin{vmatrix}
t=3\phi\\
dt = 3 d\phi
\end{vmatrix}=\\
=\frac{3}{6}a^2\cdot \int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}{\cos^2{t}\ dt}=
\frac{1}{2}a^2\cdot \int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}{\frac{1+\cos{2t}}{2}\ dt}=\\
=\frac{1}{4}a^2\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}{1+\cos{2t}\ dt}=\\=
\begin{vmatrix}
x=2t\\
dx=2 dt
\end{vmatrix}=

\frac{1}{4}a^2(\frac{\pi}{2}-(-\frac{\pi}{2})+
\frac{1}{2}
\int^{\pi}_{-\pi}{\cos{x}\ dt})=\frac{a^2}{4}(\pi +\frac{1}{2}(\sin{\pi}-\sin{-\pi}))\\=\frac{a^2}{r}\pi
\end{gathered}$$

---
###### 11) Narysuj krzywą $(x^2+y^2)^3=4x^2y^2$ i oblicz pole obszaru ograniczonego tą krzywą.

$$\begin{gathered}
x=r\cos{\phi}\\
y=r\sin{\phi}\\\\

(x^2+y^2)^3=4x^2y^2\\
r^6=4r^2\cos^2{\phi}r^2\sin^2{\phi}\\
r^2=4\sin^2{\phi}\cos^2{\phi}=\sin^2{2\phi}\\\\
|P|=\frac{1}{2}\int^{2\pi}_{0}{r^2}=
\frac{1}{2}\int^{2\pi}_{0}{\sin^2{2\phi}\ d\phi}=
\begin{vmatrix}
t=2\phi\\
dt = 2 d\phi
\end{vmatrix}=\frac{1}{4}\int^{4\pi}_{0}{\sin^2{t}\ dt}=\\\\
=\frac{1}{4}\int^{4\pi}_{0}{\frac{1-\cos{2t}}{2}\ dt}=
\frac{1}{8}\int^{4\pi}_{0}{1-\cos{2t}\ dt}=
\frac{1}{8}\int^{4\pi}_{0}{1\ dt}-\int^{4\pi}_{0}{\cos{2t}\ dt}=\\
=\frac{1}{8}({4\pi }-\frac{1}{2}\int^{8\pi}_{0}{\cos{u}\ du})=
\frac{\pi}{2}
\end{gathered}$$

---
### Długość krzywej

$L:\left\{\begin{matrix}x=x(t)\\ y=y(t)\end{matrix}\right., t\in [\alpha,\beta]$

Tworzymy ciąg podziałów przedziału $[\alpha,\beta]$
$\alpha=t_0\lt t_1\lt \dots \lt t_{n-1}\lt t_n=\beta$
$\delta_n=max\{|t_i-t_{i-1}|, i=1,\dots,n\}$
$P_{i-1}=(x(t_{i=1}),y(t_{i-1}))$
$P_i=(x(t_i),y(t_i))$
$|P_{i-1}P_i|=\sqrt{(x(t_i)-x(t_{i-1}))^2+(y(t_i)-y(t_{i-1}))^2}$
$d_n=\sum^{n}_{i=1}{|P_{i-1}P_i|}$

**Def.**
Jeśli istnieje $\underset{\delta_n\to 0}{\lim_{n\to \infty}{d_n}}$, to krzywą nazywamy **prostowalną** i tę granicę nazywamy **długością** krzywej.

**Def.**
Krzywą $L$ nazywamy **łukiem gładkim** $\Leftrightarrow$
1) $x(t),y(t) \in C^1([\alpha,\beta])$
2) $\forall t\in [\alpha,\beta]\ ((x'(t))^2+(y'(t))^2\gt 0\ \Leftrightarrow$ w każdym punkcie krzywej istnieje styczna

**Twierdzenie:**
Każdy łuk gładki jest krzywą prostowalną i jego długość wynosi:
$$\begin{gathered}
|L|=\int^{\beta}_{\alpha}{\sqrt{(x'(t))^2+(y'(t))^2}\ dt}
\end{gathered}$$
**Jeśli krzywa zadana jest w sposób jawny:**
$L: y=f(x), x\in [a,b]$
$f\in C^1([a,b])$
Wtedy:
$$\begin{gathered}
|L|=\int^{b}_{a}{\sqrt{1+(f'(x))^2}\ dx}
\end{gathered}$$

**Jeśli w biegunowy:**
$L: r=r(\phi), \phi\in [\alpha,\beta]$
$r(\phi)\in C^1([\alpha,\beta])$
Wtedy:
$$\begin{gathered}
|L|=\int^{\beta}_{\alpha}{\sqrt{(r(\phi))^2+(r'(\phi))^2}\ d\phi}
\end{gathered}$$

---
**Przykłady:**
Oblicz długość cykloidy:
$$\begin{gathered}
x=a(t-\sin{t})\\
y=a(1-\cos{t})\\
t\in [0,2\pi]\\\\
x'=a-a\cos{t}\\
y'=a\sin{t}
\\\\
|L|=\int^{2\pi}_{0}{\sqrt{(x'(t))^2+(y'(t))^2}\ dt}=
\int^{2\pi}_{0}{\sqrt{(a-a\cos{t})^2+(a\sin{t})^2}\ dt}=\\\\
=\int^{2\pi}_{0}{\sqrt{a^2-2a^2\cos{t}+a^2\cos^2{t}+a^2\sin^2t}\ dt}=\\\\
=\sqrt{2}a\int^{2\pi}_{0}{\sqrt{1-\cos{t}}\ dt}=
2a\int^{2\pi}_{0}{\sqrt{\sin^2{\frac{t}{2}}}\ dt}=
2a\int^{2\pi}_{0}{\sin{\frac{t}{2}}}=\begin{vmatrix}
u=\frac{t}{2}\\
2du= dt
\end{vmatrix}=\\\\
=4a\int^{\pi}_{0}{\sin{u}\ du}=|4a\cdot (-\cos{\pi}+\cos{0})|=4a \cdot (-(-1)+1)=8a
\end{gathered}$$
---
**Przykład 2:**
Oblicz długość asteroidy

$$\begin{gathered}
x=a\cos^3{t}\\
y=a\sin^3{t}\\
t\in [0,2\pi]\\\\
x'=-3a\cos^2{t}\cdot\sin{t}\\
y'=3a\sin^2{t}\cdot \cos{t}\\\\
|L|=\int^{2\pi}_{0}{\sqrt{(x'(t))^2+(y'(t))^2}\ dt}=
\int^{2\pi}_{0}{\sqrt{9a^2\cos^4{t}\sin^2{t}+9a^2\sin^4{t}\cos^2{t}}\ dt}=\\\\
=3a\int^{2\pi}_{0}{\sqrt{\cos^4{t}\sin^2{t}+\sin^4{t}\cos^2{t}}\ dt}=\\=
3a\int^{2\pi}_{0}{\sqrt{\sin^2{t}\cos^2{t}(cos^2{t}+\sin^2{t})}\ dt}=\\
=\frac{3}{2}a\int^{2\pi}_{0}{\sqrt{\sin^2{2t}}}=\frac{3a}{2}\int^{2\pi}_{0}{|\sin{2t}|}=\begin{vmatrix}
u=2t\\
du=2\ dt
\end{vmatrix}=\\\\
=\frac{3a}{4}\int^{4\pi}_{0}{|\sin{u}|}=
\frac{3a}{4}\cdot 8\int^{\frac{\pi}{2}}_{0}{\sin{u}}=6a
\end{gathered}$$
---
### Objętość, i pole powierzchni bryły obrotowej

$y=f(x), x \in [a,b]$
$f\in C([a,b])$
$V$ - bryła powstała przez obrót krzywej $y=f(x)$ wokół osi $OX$
Wtedy: 
$$\begin{gathered}
\text{Objętość bryły powstałej poprzez obrót krzywej f(x) wokół osi OX:}\\\\
|V|=\pi \int^{b}_{a}f^2(x)\ dx
\end{gathered}$$

Jeśli krzywa jest zadana parametrycznie:
$x=x(t)$
$y=y(t)$
$y(t)\in C([\alpha,\beta])$
$x(t)\in C^1([\alpha,\beta])$
$\forall t\in [\alpha,\beta]\  x'(t)\gt 0$
Wtedy:
$$\begin{gathered}
|V|=\pi \int^{\beta}_{\alpha}{y^2(t)\cdot x'(t) \ dt}
\end{gathered}$$
---
**Przykład:**
Oblicz objętość bryły powstałej poprzez obrót elipsy $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$
$$\begin{gathered}
x(t)=a\cdot \cos{t}\\
y(t)=b\cdot \sin{t}\\\\
\frac{1}{2}|P|=\pi \int^{2\pi}_{\pi}{ab^2\cdot \sin^3{t}\ dt}=
\pi ab^2 \int^{2\pi}_{\pi}{(1-\cos^2{})\cdot \sin{t}\ dt}=\\
=\begin{vmatrix}
x=\cos{t}\\
dx = \sin{t}
\end{vmatrix}=\pi ab^2\int^{1}_{0}{x^2-1\ dx}=|\pi ab^2(\frac{1}{3}-(1-0))|=\frac{2}{3}\pi ab^2\\\\
P=\frac{4\pi}{3}ab^2
\end{gathered}$$
Oblicz objętość torusa $x^2+(y-R)^2=r^2$:

$$\begin{gathered}
x(t)=r\cos{t}+R\\
y(t)=r\sin(t)\\\\
\frac{1}{2}|P|=\int^{2\pi}_{\pi}{r^2\sin^2{(t)}\cdot -r\sin{t}\ dt}=
-r^3\int^{2\pi}_{\pi}{\sin^3{t}\ dt}=\\
=-r^3\int^{2\pi}_{\pi}{(1-\cos^2{t})\sin{t}}=\begin{vmatrix}
x=\cos{t}\\
dx = -\sin{t}
\end{vmatrix}=-r^3\int^{1}_{0}{x^2-1\ dx}=\\
=-r^3(\frac{1}{3}-1)=\frac{2}{3}r^3\\\\
|P|=\frac{4}{3}r^3
\end{gathered}$$
---
### Pole powierzchni bocznej bryły obrotowej

Zał:
$y=f(x), x \in [a,b]$
$f\in C^1([a,b])$
$\forall x \in [a,b] \ f(x)\geq 0$
Teza: pole powierzchni bocznej bryły powstałej przez obrót krzywej wokół osi OX:
$$\begin{gathered}
|S|=2\pi \int^{b}_{a}{f(x)\sqrt{1+(f'(x))^2}\ dx}
\end{gathered}$$

Jeśli krzywa jest łukiem gładkim:
$x=x(t)$
$y=y(t), t\in [\alpha,\beta]$
$x(t),y(t)\in C^1([\alpha,\beta])$
$\forall t \in [\alpha, \beta] y(t)\geq 0$
Teza: pole powierzchni bocznej bryły powstałej przez obrót krzywej wokół osi $OX$ 
$$\begin{gathered}
|S|=2\pi \int^{\beta}_{\alpha}{y(t)\sqrt{(x'(t))^2+(y'(t))^2}\ dt}
\end{gathered}$$

---
