# zadania frydzia

## Szeregi

### 1) Pokaż,że szereg jest zbieżny i oblicz jego sumę:

#### 1) $\sum^{\infty}_{n=1}{\frac{3^n+4^n}{5^n}}$

$$\begin{gathered}
a_n=\frac{3^n+4^n}{5^n}\\\\
\text{Na podstawie kryterium Cauchye'go:}\\\\
g=\lim_{n\to \infty}{\sqrt[n]{\frac{3^n+4^n}{5^n}}}=\frac{4}{5}\lt 1 \implies \text{zbieżny}\\\\
\frac{\frac{3}{5}}{1-\frac{3}{5}}+
\frac{\frac{4}{5}}{1-\frac{4}{5}}=\frac{11}{2}
\end{gathered}$$

#### 2) $\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}$

$$\begin{gathered}
a_n=\frac{1}{(3n-2)(3n+1)}\\
\text{Z kryterium porównawczego granic ilorazowych:}\\
\sum^{\infty}_{n=1}{\frac{1}{n^2}}- \text{Zbieżne na podstawie tw. o szeregach harmonicznych}\\
\lim_{n\to \infty}{\frac{\frac{1}{n^2}}{\frac{1}{9n^2-3n-2}}}=9\in (0, +\infty)\\
\text{Także zbieżny bo i tamten zbieżny}\\\\\
\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}=\frac{1}{(3-2)(3+1)}+\frac{1}{(6-2)(6+1)}+\frac{1}{(9-2)(9+1)}\dots\\\\

3n+1=3(n+1)-2\implies \text{Zauważamy że coś się znosi}\\\\
\frac{1}{4}, \ \frac{1}{4}+\frac{1}{4
\cdot 7}=\frac{2}{7}\\\\
\text{Załóżmy zatem że szereg przyjmuje postać:}\\
\sum^{\infty}_{n=1}{\frac{1}{(3n-2)(3n+1)}}=\frac{n}{3n+1}\\
\text{I udowodnijmy to indukcyjnie:}\\
a_1\checkmark\\
a_{n}=\frac{n-1}{3n-2}+\frac{1}{(3n-2)(3n+1)}=\frac{(3n+1)(n-1)+1}{(3n-2)(3n+1)}=\frac{3n^2-2n}{(3n-2)(3n+1)}=\\=\frac{n}{3n+1}\checkmark\\

\end{gathered}$$
---

### 2) Sprawdź, czy następujące szeregi są zbieżne:

#### a) $\sum^{\infty}_{n=1}{\ln(1+\frac{1}{n})}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\ln(1+\frac{1}{n})}=\\=\lim_{n\to \infty}\sum^{\infty}_{n=1}{\ln(\frac{n+1}{n})}=\ln(2)-\ln(1)+\ln(3)-\ln(2)+\dots+
\ln(n+1)=\\
=\lim_{n\to \infty}\ln(n+1)-\ln(1)=\lim_{n\to \infty}\ln(n+1)=\infty
\end{gathered}$$
#### b) $\sum^{\infty}_{n=1}{\frac{(2n)!2^n}{n^{2n}}}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(2n)!2^n}{n^{2n}}}\\\\
a_n=\frac{(2n)!2^n}{n^{2n}}\\\\
\lim_{n\to \infty}{\frac{a_{n+1}}{a_n}}=\lim_{n\to \infty}\frac{(2n)!(2n+1)(2n+2)\cdot 2\cdot 2^n}{(n+1)^{2n}\cdot (n+1)^2}\cdot \frac{n^{2n}}{(2n)!2^n}=\\\\
=\lim_{n\to \infty}{\frac{4(2n+1)n^{2n}}{(n+1)^{2n}
\cdot (n+1)}}=\lim_{n\to \infty}{\frac{8n+4}{n+1}}\cdot \lim_{n\to \infty}{\left(\frac{n}{n+1}\right)^{2n}}=8e^{-2}\approx1.083\gt 1\\\\
\text{Więc rozbieżny}
\end{gathered}$$

#### c) $\sum^{\infty}_{n=1}{\frac{n^3(\sqrt{2}+(-1)^n)^n}{3^n}}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{n^3(\sqrt{2}+(-1)^n)^n}{3^n}}\lt \sum^{\infty}_{n=1}{\frac{n^3(2\sqrt{2})^n}{3^n}}\\\\

\sum^{\infty}_{n=1}{\frac{n^3(2\sqrt{2})^n}{3^n}}\\\\
\text{Z kryterium Cauchy'ego:}\\\\
\lim_{n\to \infty}{\sqrt[n]{\frac{n^3(2\sqrt{2})^n}{3^n}}}=\frac{2\sqrt{2}}{3}\lt 1 \implies \text{Zbieżny}
\end{gathered}$$

#### d) $\sum^{\infty}_{n=1}{\frac{\cos^2{\frac{n\pi}{3}}}{2^n}}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{\cos^2{\frac{n\pi}{3}}}{2^n}}\lt \sum^{\infty}_{n=1}{\frac{1}{2^n}}\\\\
\sum^{\infty}_{n=1}{\frac{1}{2^n}} - \text{Zbieżny na podstawie czegokolwiek może być alambert}\\\\
\text{Więc zbieżny na podstawie kryterium porównawczego}

\end{gathered}$$
#### d) $\sum^{\infty}_{n=1}{\frac{\cos{\frac{n\pi}{3}}}{2^n}}$


$$\begin{gathered}
\text{Albo przekształcamy na 6 odrębnych szeregów (z okresu cosinusa)}\\
\text{Albo robimy tak:}\\\\
\sum^{\infty}_{n=1}{\left|\frac{\cos{\frac{n\pi}{3}}}{2^n}\right|}\leq \sum^{\infty}_{n=1}{\frac{1}{2^n}}\\\\
\text{Więc z kryterium porównawczego tak samo jak wyżej a jeżeli wartość}\\
\text{bezwzględna szeregu jest zbieżna to i szereg właściwy jest zbieżny}

\end{gathered}$$
#### f) $\sum^{\infty}_{n=1}{\frac{(-1)^n\cdot \ln{n}}{n}}$

$$\begin{gathered}
\text{No z szeregu naprzemiennego tylko trzeba sprawdzić założenia:}\\\\
1) \forall n\geq 1  \ \ a_n\gt 0\\
2) \lim_{n\to \infty}{a_n}=0\\
3) (a_n)^\infty_{n=1} \text{ jest malejący}\\
\end{gathered}$$
---
### 3. Zbadaj zbieżność punktową i jednostajną ciągu funkcyjnego

**Def zbieżności punktowej:**

Mówimy, że ciąg funkcyjny $(f_n(x))_{n\in \mathbb{N}}$ jest **zbieżny punktowo** na $X \Leftrightarrow$ istnieje taka funkcja $f: X\to Y$, że $\forall x \in X \ \ \lim_{n\to \infty}{f_n(x)}=f(x)$

Funkcję $f$ nazywamy **funkcją graniczną** ciągu funkcyjnego $(f_n(x))_{n\in \mathbb{N}}$
Ozn. $f_n\overset{X}{\to}Y$, że $\forall x \in X \ \lim_{n\to \infty}{f_n(x)}=f(x)$

Czyli: $\forall x \in X \ \forall \epsilon > 0 \ \ \exists n_0 \in \mathbb{N} \ \ \forall n \geq n_0 \ |f_n(x)-f(x)| \lt \epsilon$

**Def zbieżności jednostajnej**:
Mówimy że ciag funkcyjny $(f_n(x))_{n\in \mathbb{N}}$ jest **zbieżny jednostajnie** na $X$:

Wtedy i tylko wtedy gdy: $\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N}\ \  \forall n\geq n_0 \ \forall x\in X \ \ |f_n(x)-f(x)|\lt \epsilon$
Czyli tutaj - tak jak nazwa mówi ten ciąg funkcyjny się stale przybliża fo funkcji granicznej, jeżeli dany $n$-ty element będzie poniżej epsilona, to kolejne też.

Ozn. $f_n\overset{X}{⇒}f$ - ciąg $(f_n(x))_{n\in \mathbb{N}}$ jest jednostajnie zbieżny na $X$.
#### a) $f_n(x)=\frac{nx}{n^2+x^2} \ na \ \mathbb{R}$

$$\begin{gathered}
\lim_{n\to \infty}{\frac{nx}{n^2+x^2}}=0=f(x)\text{ - Więc zbieżny punktowo}
\\\\
\text{Można wykazać że ma stałe maksimum nie zależnie od n co przeczy zbieżności }\\
\text{jednostajnej lub poleciec czysto z definicji:}\\\\
\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N}\ \  \forall n\geq n_0 \ \forall x\in X \ \ |f_n(x)-f(x)|\lt \epsilon\\\\
\text{Czyli możemy tutaj zrobić tak: przyjąć że mamy }\epsilon \text{ ustalony i sprawdzić czy }\\
\text{faktycznie istnieje takie }n_0\\\\

|f_n(x)-f(x)|\lt \epsilon\\
|\frac{nx}{n^2+x^2}|\lt \epsilon\\
|nx|\lt \epsilon(n^2+x^2)\\
- \epsilon(n^2+x^2)\lt nx\lt \epsilon(n^2+x^2)\\\\
\epsilon(n^2+x^2)-nx \gt 0\\
\epsilon n^2+\epsilon x^2-nx\gt 0\\\\
\Delta\lt 0\\
n^2-4\epsilon ^2 n^2\lt 0\\
n^2(1-4\epsilon^2)\lt 0\\\\
\text{Wychodzi nam że }\epsilon \text{ nie może być dowolnie mały}\\
\text{więc nie jest jednostajnie zbieżny}

\end{gathered}$$

#### b) $f_n(x)=\frac{1}{1+nx}\ na \ [0,1]$

$$\begin{gathered}
\lim_{n\to \infty}{\frac{1}{1+nx}}=0, \text{gdy }x\gt 0\\
\lim_{n\to \infty}{\frac{1}{1+nx}}=1, \text{gdy }x= 0\\\\
f(x)=\left\{
\begin{matrix}
0, x \in (0,1]\\
1, x=0
\end{matrix}
\right.\\\\
\text{więc zbieżna punktowo}\\\\
\left|\frac{1}{1+nx}\right|\lt \epsilon\\
1\lt \epsilon(1+nx)\\
1\lt \epsilon+\epsilon nx\\
\frac{1-\epsilon}{\epsilon x}\lt n\\\\
\text{ n zależne od x więc nie zbiega jednostajnie}
\end{gathered}$$

---
### 4)  Zbadaj zbieżność punktową i jednostajną szeregu:

#### a) $\sum^{\infty}_{n=1}{\frac{\sin{nx}}{\sqrt[3]{n^4+x^2}}}\ na \ \mathbb{R}$

$$\begin{gathered}
\text{Z tw. Weierstrassa}:\\\\

\sum^{\infty}_{n=1}{\frac{\sin{nx}}{\sqrt[3]{n^4+x^2}}}\lt \sum^{\infty}_{n=1}{\frac{1}{\sqrt[3]{n^4}}} - \text{Zbieżny bo harmoniczny o rzędzie większym od 1}\\
\text{Więc zbieżny jednostajnie a co za tym idzie też punktowo}
\end{gathered}$$
#### b) $\sum^{\infty}_{n=1}{\frac{nx}{1+n^5x^2}} \ na \ [1,+\infty)$

$$\begin{gathered}
\text{Z tw. Weierstrassa}:\\\\
\sum^{\infty}_{n=1}{\frac{nx}{1+n^5x^2}}\lt 
\sum^{\infty}_{n=1}{\frac{nx}{n^5x^2}}\lt 
\sum^{\infty}_{n=1}{\frac{1}{n^4x}}\lt 
\sum^{\infty}_{n=1}{\frac{1}{n^4}} - \text{Zbieżny } \\\\
\text{Więc zbieżny jednostajnie a co za tym idzie punktowo}
\end{gathered}$$

#### c) $\sum^{\infty}_{n=1}{x^n(1-x)}\ na \ [0,1]$

$$\begin{gathered}
I: x=1\\\\
S(1)=0\\\\
II: x\neq 1\\\\
S(x)=x\implies \text{Zbieżny punktowo}\\\\

\text{w takim razie funkcja graniczna ciągła nie jest więc nie może zbiegać jednostajnie}
\end{gathered}$$

### 5) Zbadaj obszar zbieżności i wyznacz sumę szeregu potęgowego:

#### a) $\sum^{\infty}_{n=1}{\frac{3^{n-1}x^{2n}}{(n+1)4^n}}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{3^{n-1}x^{2n}}{(n+1)4^n}}=
\sum^{\infty}_{n=1}{\frac{3^{n-1}u^{n}}{(n+1)4^n}}, u=x^2\\\\
\lambda =\lim_{n\to \infty}{\frac{a_{n+1}}{a_n}}=\lim_{n\to \infty}{\frac{3\cdot 3^{n-1}}{(n+2)\cdot 4\cdot 4^n}\cdot \frac{4^n\cdot (n+1)}{3^{n-1}}}=\frac{3}{4}\\\\
u\in (-\frac{4}{3}, \frac{4}{3})\cap [0,+\infty)\implies u\in [0,\frac{4}{3})\\
x\in (-\frac{2}{\sqrt{3}}, \frac{2}{\sqrt{3}})\\\\
\lim_{x\to -\frac{2}{\sqrt{3}}^+ }=\lim_{x\to \frac{2}{\sqrt{3}}^- }=\sum^{\infty}_{n=1}{\frac{3^{n-1}\cdot 4^n}{(n+1)4^{n}\cdot 3^n}}=\sum^{\infty}_{n=1}{\frac{1}{3n+3}}\\\\
\text{A to napewno zbieżne nie będzie co można udowodnić kryterium porównawczym}\\
\text{granic ilorazowych z }\frac{1}{n}
\end{gathered}$$
#### b) $\sum^{\infty}_{n=1}{\frac{(n+1)(x+2)^n}{2^n}}$

$$\begin{gathered}
\lambda=\lim_{n\to \infty}{|\frac{n+2}{2\cdot 2^n}\cdot \frac{2^n}{n+1}|}=\frac{1}{2}\\\\

x\in (-4,0)\\\\
\lim_{x\to 0^-}{S(x)}=\sum^{\infty}_{n=1}{(n+1)}=\infty\\
\lim_{x\to -4^+}{S(x)}=\sum^{\infty}_{n=1}{(-1)^n\cdot (n+1)}=-2+3-4+5=1+1+1\dots=\infty
\end{gathered}$$


---
### 6) Oblicz sumę szeregu liczbowego $\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}}$

#### Sposób 1
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}}=\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}\cdot x^{n-1}}=\sum^{\infty}_{n=0}{\frac{(-1)^{n+2}(n+1)}{3^{n+1}}\cdot x^{n}}, x=1\\\\
\lambda=\lim_{n\to \infty}{|\frac{(-1)^{n+3}(n+2)}{9\cdot 3^n}\cdot \frac{3\cdot 3^n}{(-1)^{n+2}(n+1)}|}=\frac{1}{3}\\\\
x\in (-3,3)-\text{szereg zbieżny}\\\\
\int{S(x)\ dx}=\int{\sum^{\infty}_{n=0}{\frac{(-1)^{n+2}(n+1)}{3^{n+1}}\cdot x^{n}}\ dx}=\sum^{\infty}_{n=0}{\frac{(-1)^{n+2}}{3^{n+1}}\cdot x^{n+1}}=\\
=\frac{x}{3}\sum^{\infty}_{n=0}{\frac{(-1)^{n}}{3^{n}}\cdot x^{n}}=\frac{x}{3}\cdot \frac{1}{1-(-\frac{x}{3})}=\frac{x}{3+x}=1-\frac{3}{3+x}\\\\
S(x)=\left(\int{S(x)\ dx}\right)'=\frac{3}{9+6x+x^2}\\\\
S(1)=\frac{3}{16}
\end{gathered}$$
#### Sposób 2 (zabieramy wszystko co ma potęge n i zamieniamy to na $x^n$)

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^{n+1}n}{3^n}}=-x\sum^{\infty}_{n=1}{nx^{n-1}}=-x\sum^{\infty}_{n=0}{(n+1)x^{n}}=-x\cdot S(x),x=-\frac{1}{3}\\\\
x\in (-1,1)-\text{zbieżny}\\\\
\int{S(x)\ dx}=\sum^{\infty}_{n=0}x^{n+1}=\frac{x}{1-x}\\\\
S(x)=\left(\int{S(x)\ dx}\right)'=\frac{1}{1-2x+x^2}\\\\
f(x)=-x\cdot S(x)=\frac{-x}{1-2x+x^2}=\frac{\frac{1}{3}}{1+\frac{2}{3}+\frac{1}{9}}=\frac{1}{3+2+\frac{1}{3}}=\frac{3}{16}
\end{gathered}$$

---
### 7) Rozwiń w szereg Taylora funkcję $f(x)$ w otoczeniu punktu $x_0$

#### a) $f(x)=\ln{x}, x_0=1$

$$\begin{gathered}
f'(x)=\frac{1}{x}=\frac{1}{1-(1-x)}=\sum^{\infty}_{n=0}{(1-x)^n}, 
|1-x|\lt 1\implies x\in (0,2)\\\\
\int{f'(x)\ dx}=\int{\left(\sum^{\infty}_{n=0}{(1-x)^n}\right) dx}=\begin{vmatrix}
u=1-x\\
du=-dx
\end{vmatrix}=\int{\left(\sum^{\infty}_{n=0}{-u^n}\right) du}=\sum^{\infty}_{n=0}{-\frac{u^{n+1}}{n+1}}=\\=
\sum^{\infty}_{n=0}{-\frac{(1-x)^{n+1}}{n+1}}=
\sum^{\infty}_{n=0}{-(-1)^{n+1}\frac{(x-1)^{n+1}}{n+1}}=
\sum^{\infty}_{n=1}{(-1)^{n+1}\frac{(x-1)^{n}}{n}}(+C)\\\\
C=0 \text{ bo po podstawieniu 1 w obu przypadkach dostajemy 0}
\end{gathered}$$

#### b) $f(x)=\ln{(x^2+3x+2)}, x_0=0$

$$\begin{gathered}
x^2+3x+2\gt 0\\ 
\Delta=9-8=1\\
x_1=\frac{-3+1}{2}=-1\\
x_2=\frac{-3-1}{2}=-2\\
x\in (-\infty, -2)\cup (-1, \infty)\\
\\
f'(x)=\frac{2x+3}{x^2+3x+2}=\frac{2x+3}{(x+2)(x+1)}\\\\
\frac{A}{x+2}+\frac{B}{x+1}=\frac{2x+3}{(x+2)(x+1)}\\
A(x+1)+B(x+2)=2x+3\\\\
\left\{
\begin{matrix}
A+B=2\\
A+2B=3
\end{matrix}
\right.\
\left\{
\begin{matrix}
A=1\\
B=1
\end{matrix}
\right.\\\\
f'(x)=\frac{1}{x+1}+\frac{1}{x+2}=\frac{1}{1-(-x)}+\frac{1}{2}\cdot \frac{1}{1-(-\frac{x}{2})}=\sum^{\infty}_{n=0}{(-x)^n+\frac{1}{2}\cdot \sum^{\infty}_{n=0}(-\frac{x}{2})^n}\\\\
|-x|\lt 1 \ \land |-\frac{x}{2}|\lt 1\implies x\in (-1,1)\cap (-2,2)\implies x\in (-1,1)\\\\
f(x)=\int{f'(x) \ dx}=\int{\sum^{\infty}_{n=0}{(-x)^n+\frac{1}{2}\cdot \sum^{\infty}_{n=0}(-\frac{x}{2})^n}}=\\=
\int{\sum^{\infty}_{n=0}{(-x)^n}+\frac{1}{2}\cdot \int{\sum^{\infty}_{n=0}(-\frac{x}{2})^n}}=(1)+(2):\\\\
(1):\\\\
\int{\sum^{\infty}_{n=0}{(-x)^n}\ dx}=\begin{vmatrix}
u=-x\\
du=-dx
\end{vmatrix}=-\sum^{\infty}_{n=0}{\frac{(-x)^{n+1}}{n+1}}=\sum^{\infty}_{n=0}{\frac{(-1)^{n+2}(x)^{n+1}}{n+1}}(+C)\\\\
(2):\\\\
\frac{1}{2}\cdot \int{\sum^{\infty}_{n=0}(-\frac{x}{2})^n\ dx}=\begin{vmatrix}
u=-\frac{x}{2}\\
du=-\frac{1}{2}dx\\
dx=-2du
\end{vmatrix}=-\int{\sum^{\infty}_{n=0}(u)^n\ du}=-\sum^{\infty}_{n=0}{\frac{u^{n+1}}{n+1}}=\\=
-\sum^{\infty}_{n=0}{\frac{(-\frac{x}{2})^{n+1}}{n+1}}=

-\sum^{\infty}_{n=0}{(-\frac{1}{2})^{n+1}\frac{x^{n+1}}{n+1}}=

\sum^{\infty}_{n=0}{(-1)^{n+2}(\frac{1}{2})^{n+1}\frac{x^{n+1}}{n+1}}\\\\
\dots (1)+(2)=\sum^{\infty}_{n=0}{(-1)^{n+2}(\frac{1}{2})^{n+1}\frac{x^{n+1}}{n+1}}+\sum^{\infty}_{n=0}{\frac{(-1)^{n+2}(x)^{n+1}}{n+1}}=\\
=\sum^{\infty}_{n=0}{\frac{(-1)^{n}(x)^{n+1}}{n+1}\cdot (\frac{1}{2}^{n+1}+1)}\\\\
\text{po uwzględnieniu dziedziny funkcji i przedziału zbieżności tam gdzie ułamki były }\\
\text{otrzymujey że }x\in (-1,1)
\end{gathered}$$

#### c) $f(x)=\frac{1}{(x+2)^2}, x_0=0$

$$\begin{gathered}
f(x)=\frac{1}{(x+2)^2}, \ \ x\neq -2\\
\int{f(x)\ dx}=\begin{vmatrix}
u=x+2\\
du=dx
\end{vmatrix}=\int{\frac{1}{u^2}\ du}=-\frac{1}{u}=-\frac{1}{x+2}=-\frac{1}{2}\cdot \frac{1}{1-(-\frac{x}{2})}=\\
=-\frac{1}{2}\sum^{\infty}_{n=0}{(-\frac{x}{2})^n}+C, \ \ \ |-\frac{x}{2}|\lt 1\implies x\in (-2,2)\\\\
f(x)=\left(\int{f(x)\ dx}\right)'=-\frac{1}{2}\sum^{\infty}_{n=1}(-\frac{1}{2})^n\cdot n\cdot x^{n-1}\\\\
\text{Ważna uwaga - przy różniczce gdybyśmy pozostali przy indeksie zaczynając}\\
\text{od zera jednym z wyrazów byłoby }x^{-1} \text{ co nie może się pojawić przy szeregu}\\
\text{Taylora, warto zauważyć że wyraz dla zerowego indeksu n można pominąć bo to}\\
\text{stała więć różniczka tego wyrazu to i tak 0 a wtedy mamy cały szereg taylora i lux}
\end{gathered}$$

#### d) $f(x)=e^{-x^2}, x_0=0$


$$\begin{gathered}
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}}\\\\
e^{-x^2}=\sum^{\infty}_{n=0}{\frac{(-x^2)^n}{n!}}=\sum^{\infty}_{n=0}{(-1)^{n}\frac{x^{2n}}{n!}}
\end{gathered}$$

#### e) $f(x)=e^{x}, x_0=2$

$$\begin{gathered}
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}}\\\\
e^x=e^2\cdot e^{x-2}=\sum^{\infty}_{n=0}{\frac{e^2\cdot(x-2)^n}{ n!}}
\end{gathered}$$

#### f) $f(x)=\sin^2{x}, x_0=0$

$$\begin{gathered}
f'(x)=2\sin{x}\cos{x}=\sin{2x}=\sum^{\infty}_{n=0}{\frac{(-1)^n(2x)^{2n+1}}{(2n+1)!}}=\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}x^{2n+1}}{(2n+1)!}}\\\\
f(x)=\int{\left(f'(x) \right) \ dx}+C=\sum^{\infty}_{n=0}{\frac{(-1)^n2^{2n+1}x^{2n+2}}{(2n+2)!}}+C, C=0
\end{gathered}$$

---
### 8) Rozwiń w szereg Fouriera funkcję $$f(x)=\left\{\begin{matrix}0, -\pi\lt x\lt 0\\x, 0\leq x\lt \pi \end{matrix}\right.$$ Narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ oraz korzystając z otrzymanego rozwinięcia oblicz sumę szeregu liczbowego $1+\frac{1}{3^2}+\frac{1}{5^2}+\dots$

**Sprawdźmy najpierw warunki Dirichleta:**

1) $f: [a,b] \to \mathbb{R}, f - ograniczona$ :LiCheck: 
2) monotoniczna przedzialami :LiCheck:
3) ciągła poza skończoną liczbą punktów w których wartość jest równa średniej arytmetycznej granic jednostronnych :LiCheck: 
4) $f(a)=f(b)=\frac{\lim_{x\to a^+}f(x)+\lim_{x\to b^-}f(x)}{2}$ :LiCross: 


$$\begin{gathered}
\text{Najpierw warunki dirichleta}:
f(-\pi)=f(\pi)=\frac{\pi}{2}\\\\
a_0=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x) \ dx}\\
a_0=\frac{1}{\pi}\left(\int^{\pi}_{0}{x\ dx}+\int^{0}_{-\pi}{0 \ dx}\right)=\frac{\pi^2}{2\pi}=\frac{\pi}{2}\\\\

a_n=\frac{1}{\pi}\left(\int^{\pi}_{0}{x\cos{nx}\ dx}\right)=\begin{vmatrix}
u=x&v'=\cos{nx}\\
u'=1&v=\frac{\sin{nx}}{n}
\end{vmatrix}=\\
=\frac{1}{\pi}\left(\frac{x \sin{nx}}{n}-\int{\frac{\sin{nx}}{n}}\right)|^{\pi}_0=\frac{1}{\pi}\left(\frac{x \sin{nx}}{n}+\frac{ \cos{nx}}{n^2}\right)|^{\pi}_0=\\
=\frac{1}{\pi}\left(\frac{(-1)^n-1}{n^2}\right)\\\\
b_n=\frac{1}{\pi}\left(\int^{\pi}_{0}{x\sin{nx}\ dx}\right)=\begin{vmatrix}
u=x&v'=\sin{nx}\\
u'=1&v=\frac{-\cos{nx}}{n}
\end{vmatrix}=\frac{1}{\pi}\left(\frac{-x \cos{nx}}{n}+\frac{\sin{nx}}{n^2}\right)|^{\pi}_0=\\
=\frac{1}{\pi}\left(\frac{-\pi (-1)^n}{n}\right)=\frac{(-1)^{n+1}}{n}\\\\

f(x)=\frac{\pi}{4}+\sum^{\infty}_{n=1}{\cos{nx}\cdot \frac{1}{\pi}\left(\frac{(-1)^n-1}{n^2}\right)+\sin{nx}\cdot \frac{(-1)^{n+1}}{n}}\\\\
1+\frac{1}{3^2}+\frac{1}{5^2}+\dots=-\frac{1}{2}\sum^{\infty}_{n=1}{\frac{(-1)^n-1}{n^2}}=(f(0)-\frac{\pi}{4})\cdot \pi\cdot -\frac{1}{2}=\frac{\pi^2}{8}
\end{gathered}$$


### 9) Rozwiń w szereg Fouriera funkcję $f(x)=x^2$ w $[-\pi,\pi]$, narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ i korzystając z otrzymanego rozwinięcia oblicz sumę szeregu $1+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}+\dots$ oraz sumę szeregu $1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}+\dots$

$$\begin{gathered}
a_0=\frac{2}{\pi}\int^{\pi}_{0}{f(x) \ dx}=\frac{2}{\pi}\cdot \frac{\pi^3}{3}=\frac{2\pi^2}{3}\\\\
a_n=\frac{2}{\pi}\int^{\pi}_{0}{x^2\cos{nx} \ dx}=\dots\\\\

\int{x^2\cdot \cos{nx} \ dx}=\begin{vmatrix}
u=x^2&v'=\cos{nx}\\
u'=2x&v=\frac{\sin{nx}}{n}
\end{vmatrix}=\frac{x^2\cdot \sin{nx}}{n}-\int{\frac{2x \sin{nx}}{n}\ dx}=\\
=\frac{x^2\cdot \sin{nx}}{n}-\left(\frac{-2x\cdot \cos{nx}}{n^2}-\int{\frac{-2\cdot \cos{nx}}{n^2}}\right)=\\=
\frac{x^2\cdot \sin{nx}}{n}+\frac{2x\cdot \cos{nx}}{n^2}-\frac{2 \sin{nx}}{n^3}\\\\
\dots=\frac{4\cdot(-1)^n}{n^2}\\\\
f(x)=\frac{\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4\cdot(-1)^n}{n^2}\cdot \cos{nx}}\\\\
1+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}+\dots=\sum^{\infty}_{n=1}{\frac{1}{n^2}}=(f(\pi)-\frac{\pi^2}{3})\cdot \frac{1}{4}=\\=\frac{2\pi^2}{12}\\\\
1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}+\dots=(f(0)-\frac{\pi^2}{3})\cdot -\frac{1}{4}=\frac{\pi^2}{12}
\end{gathered}$$

### 10) Rozwiń w szereg sinusów funkcję $f(x)=\frac{\pi}{4}$ w $(0,\pi)$, narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ oraz korzystując z otrzymanego rozwinięcia oblicz sumę szeregu liczbowego $1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots$

$$\begin{gathered}
f_2(x)=\left\{
\begin{matrix}
\frac{\pi}{4}, x\in (0,\pi)\\
0, x\in \{-\pi,0,\pi\}\\
-\frac{\pi}{4}, x\in (-\pi,0)\\
\end{matrix}
\right.\\\\
b_n=\frac{2}{\pi}\int^{\pi}_{0}{\frac{\pi}{4}\sin{nx}\ dx}=-\frac{1}{2}\frac{(-1)^n-1}{n}=\frac{1-(-1)^n}{2n}\\\\
f(x)=\sum^{\infty}_{n=1}{\frac{1-(-1)^n}{2n}\cdot \sin{nx}}\\\\
1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots=f(\frac{\pi}{2})=\frac{\pi}{4}
\end{gathered}$$


---

# 2018/2019

## Termin $I$

### 1) Wyznacz obszar zbieżności szeregu funkcyjnego $\sum^{\infty}_{n=1}{\frac{nx}{e^{nx}}}$

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=1}{\frac{nx}{e^{nx}}}=x\sum^{\infty}_{n=1}{\frac{n}{e^{nx}}}-\text{Dla }x\neq 0 \text{ zbieżny jedynie gdy szereg zbieżny}\\\\
\sum^{\infty}_{n=1}{\frac{n}{e^{nx}}}=\sum^{\infty}_{n=1}{n\cdot u^n}, u=\frac{1}{e^x}\\\\
\lambda=1\\
u\in (-1,1)\\
-1\lt \frac{1}{e^x}\lt 1\\
e^x\gt 1\implies x\gt 0\\\\
\lim_{u\to 1^-}\sum^{\infty}_{n=1}{n\cdot u^n}=\lim_{x\to 0^-}\sum^{\infty}_{n=1}{n\cdot 1^n}-\text{nie zbieżne}\\\\
x\in (0,\infty)\\\\
\text{Ale }S(0)=0\implies \text{Dodatkowo mamy zbieżność w punkcie }x=0
\end{gathered}$$

---
### 2) Rozwiń w szereg sinusów funkcję $f(x)=x(\pi-x)$ w $(0,\pi)$. Narysuj wykres sumy otrzymanego szeregu dla wszystkich $x \in \mathbb{R}$ i korzystając z otrzymanego rozwinięcia oblicz sumę szeregu $1-\frac{1}{3^3}+\frac{1}{5^3}-\frac{1}{7^3}+\dots$

$$\begin{gathered}
b_n=\frac{2}{\pi}\int^{\pi}_{0}{(x \pi - x^2)\sin{nx}}=\dots\\\\
\int{\pi x \sin{nx}}=\begin{vmatrix}
u=x&dv=\sin{nx}\\
du=1&v=-\frac{\cos{nx}}{n}
\end{vmatrix}=\pi \left(-\frac{x \cos{nx}}{n}-\int{\frac{-\cos{nx}}{n}}\right)=\\\\
=\pi \left(-\frac{x \cos{nx}}{n}+\frac{\sin{nx}}{n}\right)\\\\
\int{x^2 \sin{nx}}=\begin{vmatrix}
u=x^2&dv=\sin{nx}\\
du=2x&v=-\frac{\cos{nx}}{n}
\end{vmatrix}=-\frac{x^2 \cos{nx}}{n}+\int{\frac{2x \cos{nx}}{n}}=\\\\
=-\frac{x^2 \cos{nx}}{n}+\frac{2x \sin{nx}}{n^2}-\int{\frac{2 \sin{nx}}{n^2}}=
-\frac{x^2 \cos{nx}}{n}+\frac{2x \sin{nx}}{n^2}+\frac{2 \cos{nx}}{n^3}\\\\

\dots=\frac{2}{\pi}\pi \left(-\frac{x \cos{nx}}{n}+\frac{\sin{nx}}{n}\right)^\pi_0-\frac{2}{\pi}\left(-\frac{x^2 \cos{nx}}{n}+\frac{2x \sin{nx}}{n^2}+\frac{2 \cos{nx}}{n^3}\right)^\pi_0=\\\\
=-2\frac{\pi(-1)^n}{n}-\frac{2}{\pi}\cdot \left(-\frac{\pi^2 (-1)^n}{n}+\frac{2 (-1)^n}{n^3}-\frac{2}{n^3}\right)=-\frac{2}{\pi}\left(\frac{2 (-1)^n}{n^3}-\frac{2}{n^3}\right)\\\\
f(x)=\sum^{\infty}_{n=1}{-\frac{2}{\pi}\left(\frac{2 (-1)^n}{n^3}-\frac{2}{n^3}\right) \sin{nx}}\\\\
1-\frac{1}{3^3}+\frac{1}{5^3}-\frac{1}{7^3}+\dots=\frac{f(\frac{\pi}{2})}{-\frac{2}{\pi}}\cdot -\frac{1}{4}=\frac{\pi^3}{32}\\\\

\end{gathered}$$


# 2019/2020

### 1 a) Zbadaj zbieżność i zbieżność bezwzględną szeregu $\sum^{\infty}_{n=1}{\frac{(-1)^n}{n-\ln{n}}}$

$$\begin{gathered}
\text{Szereg naprzemienny}:\\
a_n=\frac{1}{n-\ln{n}}\\\\
a_n - \text{Malejący bo:}\\
f(n)=\frac{1}{n-\ln{n}}, f'(n)=-\frac{1-\frac{1}{n}}{(n-\ln{n})^2}\gt 0 \Leftrightarrow 1\gt \frac{1}{n} \forall n \gt 1\\\\
a_n -\text{dodatni skoro }f(1)=1 \text{ i malejący}\\\\
\lim_{n\to \infty}{a_n}=\frac{1}{\lim_{n\to \infty}{n-\ln{n}}}=0\\\\
\text{Spełnia warunki zbieżności szeregu naprzemiennego więc zbieżny}\\\\
\sum^{\infty}_{n=1}{\left|\frac{(-1)^n}{n-\ln{n}}\right|}=
\sum^{\infty}_{n=1}{\frac{1}{n-\ln{n}}}\geq \sum^{\infty}_{n=1}{\frac{1}{n}}\\\\
\text{Czyli udowodniliśmy że bezwzględnie zbieżny nie jest na podstawie }\\
\text{kryterium porównawczego porównując z szeregiem harmonicznym o rzedzie 1}\\
\text{który zbieżny nie jest}
\end{gathered}$$

### 1 b)  Zbadaj zbieżność punktową i jednostajną ciągu funkcyjnego $f_n(x)=\frac{n}{n+x}$ na przedziale $[0,+\infty]$

$$\begin{gathered}
\lim_{n\to \infty}f_n(x)=\lim_{n\to \infty}\frac{n}{n+x}=1\\\\
\forall x \in X \exists n_0 : \forall n\gt n_0 \forall \epsilon\gt 0: |f_n(x)-f(x)|\lt \epsilon\\\\
|\frac{n}{n+x}-1|\lt \epsilon\\
|\frac{-x}{n+x}|\lt \epsilon\\
x\lt \epsilon n+\epsilon x\\
\frac{x-\epsilon x}{\epsilon}\lt n\\\\
\text{Zbieżny punktowo}\\\\\
 \forall \epsilon\gt 0\exists n_0 : \forall n\gt n_0 \forall x \in X : |f_n(x)-f(x)|\lt \epsilon\\\\
\frac{x}{n+x}\lt \epsilon\\
x\lt \epsilon n+\epsilon x\\
x(1-\epsilon) \lt \epsilon n\\
x\lt \frac{\epsilon n}{(1-\epsilon)}
\end{gathered}$$

---
### 2) Rozwiń w szereg Fouriera funkcję $f(x)=\pi^2-x^2$ w $[-\pi,\pi]$, narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ i korzystając z otrzymanego rozwinięcia oblicz sumę szeregu $1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}+\dots$ Czy otrzymany szereg Fouriera jest jednostajnie zbieżny do funkcji $f$? Odpowiedź uzasadnij.

$$\begin{gathered}
a_0=\frac{2}{\pi}\int^{\pi}_{0}{\pi^2-x^2\ dx}=\frac{2}{\pi} \left(\pi^3-\frac{\pi^3}{3}\right)=\frac{4 \pi^2}{3}\\\\
a_n=\frac{2}{\pi}\int^{\pi}_{0}{(\pi^2-x^2)\cos{nx}\ dx}=
\dots\\\\
\int{x^2 \cos{nx}}=\begin{vmatrix}
u=x^2&dv=\cos{nx}\\
du=2x&v=\frac{\sin{nx}}{n}
\end{vmatrix}=\\=\frac{x^2\sin{nx}}{n}-\int{\frac{2x\sin{nx}}{n}}=\begin{vmatrix}
u=2x&dv=\frac{\sin{nx}}{n}\\
du=2&v=-\frac{\cos{nx}}{n^2}
\end{vmatrix}=\\
=\frac{x^2\sin{nx}}{n}-\left(-\frac{2x\cos{nx}}{n^2}-\int-2\frac{\cos{nx}}{n^2}\right)=\\
\frac{x^2\sin{nx}}{n}+\frac{2x\cos{nx}}{n^2}-2\frac{\sin{nx}}{n^3}\\\\
\dots=\frac{2}{\pi}\left(-\frac{2\pi (-1)^n}{n^2}\right)=\frac{4(-1)^{n+1}}{n^2}\\\\\
f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}{a_n \cos{nx}}, x\in [-\pi, \pi]\\\\
f(x)=\frac{2\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4(-1)^{n+1}}{n^2} \cdot \cos{nx}}\\\\\
1-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}+\dots=\frac{f(0)-\frac{2\pi^2}{3}}{4}=\\
=\frac{\pi^2-\frac{2 \pi^2}{3}}{4}=\frac{\pi^2}{12}\\\\
\text{Czy otrzymany szereg Fouriera jest zbieżny jednostajnie do }\\
\text{f(x)?}\\\\
\text{Jedyne co może psuć w rozwinięciu f(x) zbieżność jednostajną }\\
\text{to jest szereg nie stała zatem wystarczy sprawdzić czy }\\
\text{szereg: }\sum^{\infty}_{n=1}{\frac{4(-1)^{n+1}}{n^2} \cdot \cos{nx}}\\
\text{jest zbieżny jednostajnie a na podstawie Weierstrassa}:\\
\sum^{\infty}_{n=1}{\frac{4(-1)^{n+1}}{n^2} \cdot \cos{nx}}=-
\sum^{\infty}_{n=1}{\frac{4(-1)^{n+1}}{n^2} \cdot \cos{nx}}\lt -\sum^{\infty}_{n=1}{\frac{4}{n^2}}\\\\
\text{gdzie } \sum^{\infty}_{n=1}{\frac{-4}{n^2}} \text{ jest zbiezny jako szereg harmoniczny rzedu większego od 1}\\
\text{Zatem tak, ten szereg Fouriera jest zbiezny jednostajnie do }f(x)
\end{gathered}$$

---
### 3) Wyznacz metodą Lagrange'a ekstrema warunkowe funkcji $f(x,y,z)=xyz$ przy warunku $x+y+z=3$, gdzie $x\neq 0$

$$\begin{gathered}
L(x,y,z,\lambda)=xyz+\lambda(x+y+z-3)\\\\
\frac{\partial L}{\partial x}=yz+\lambda\\
\frac{\partial L}{\partial y}=xz+\lambda\\
\frac{\partial L}{\partial z}=xy+\lambda\\
\frac{\partial L}{\partial \lambda}=x+y+z-3\\\\
\left\{
\begin{matrix}
yz+\lambda=0\\
\left.
\begin{matrix}
xz+\lambda=0\\
xy+\lambda=0\\
\end{matrix}
\right\}\implies y=z\\
x+y+z=3
\end{matrix}
\right.\ \
\left\{
\begin{matrix}
y^2=-\lambda\\
xy=y^2\implies y(x-y)=0\\
y=0\vee x=y
\end{matrix}
\right.\\\\
I:\\
x=3\land y=z=0\\\\
H=\begin{bmatrix}
0&1&1&1\\
1&0&z&y\\
1&z&0&x\\
1&y&x&0\
\end{bmatrix}=\begin{bmatrix}
0&1&1&1\\
1&0&0&0\\
1&0&0&3\\
1&0&3&0
\end{bmatrix}\\
H_2=\begin{vmatrix}
0&1&1\\
1&0&0\\
1&0&0
\end{vmatrix}=0\\
H_3=\begin{vmatrix}
0&1&1&1\\
1&0&0&0\\
1&0&0&3\\
1&0&3&0
\end{vmatrix}=
-\begin{vmatrix}
1&0&1&1\\
0&1&0&-3\\
0&0&-3&3\\
0&0&0&3
\end{vmatrix}=9\\\\
\text{nie ma tu ani maksimum ani minimum}
II:\\
\begin{bmatrix}
0&1&1&1\\
1&0&z&y\\
1&z&0&x\\
1&y&x&0\
\end{bmatrix}=\begin{bmatrix}
0&1&1&1\\
1&0&1&1\\
1&1&0&1\\
1&1&1&0\
\end{bmatrix}\\\\
H_2=\begin{vmatrix}
0&1&1\\
1&0&1\\
1&1&0\\
\end{vmatrix}=1+1=2\\
H_3=-\begin{vmatrix}
1&0&1&1\\
0&1&1&1\\
0&0&-3&-1\\
0&0&0&-1\
\end{vmatrix}=-3\\
\text{to jest w takim razie maksimum}\\
f(1,1,1)=1
\end{gathered}$$

---
### 4) Oblicz moment bezwładności jednorodnej bryły $\sqrt{x^2+y^2}\leq z \leq \sqrt{R^2-x^2-y^2}$ o masie $M$ względem osi $OZ$.

$$\begin{gathered}
\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
\varphi\in [0,2\pi]\\
|J|=r
\end{vmatrix}\\\\
\sqrt{x^2+y^2}=\sqrt{R^2-x^2-y^2}\\
r=\sqrt{R^2-r^2}\\
r^2=R^2-r^2\\
r^2=\frac{R^2}{2}\implies r=\frac{R}{\sqrt{2}}\\\\
V=\int^{2\pi}_{0}d \varphi \int^{\frac{R}{\sqrt{2}}}_{0}{r\sqrt{R^2-r^2}-r^2dr}=\dots\\\\
\int{r \sqrt{R^2-r^2}dr}=\begin{vmatrix}
u=R^2-r^2\\
du=-2r\ dr
\end{vmatrix}=-\frac{1}{2}\int{\sqrt{u}}=-\frac{1}{2}\frac{2u^{\frac{3}{2}}}{3}=-\frac{u^{\frac{3}{2}}}{3}=\\=-\frac{(R^2-r^2)^{\frac{3}{2}}}{3}\\\\
\dots=\int^{2\pi}_{0}d \varphi \left[-\frac{(R^2-r^2)^{\frac{3}{2}}}{3}-\frac{r^3}{3}\right]=
\int^{2\pi}_{0}d \varphi \left[-\frac{\frac{R^3}{2\sqrt{2}}}{3}-\frac{\frac{R^3}{2\sqrt{2}}}{3}+\frac{R^3}{3}\right]=\\\\
=\int^{2\pi}_{0}\left(\frac{R^3}{3}-\frac{R^3}{3\sqrt{2}}\right) d \varphi=\frac{2\pi R^3}{3}\left(1-\frac{1}{\sqrt{2}}\right)\\\\
p=\frac{M}{V}=\frac{M}{\frac{2\pi R^3(\sqrt{2}-1)}{3\sqrt{2}}}\\\\
I=p\int^{2\pi}_{0}d \varphi \int^{\frac{R}{\sqrt{2}}}_{0}r^3\sqrt{R^2-r^2}-r^4dr
\end{gathered}$$

---
## Termin $II$

### 1) Wyznacz obszar zbieżności punktowej i jednostajnej szeregu $\sum^{\infty}_{n=1}{x^2e^{-nx}}$

$$\begin{gathered}
\frac{1}{e^x}\lt 1\\
1\lt e^x\implies x\gt 0\\\\
\text{zbieżny punktowo dla }x\geq 0\\\\

\left|\frac{x^2}{e^x}\cdot \frac{1-\frac{1}{e}^{xn}}{1-\frac{1}{e}^x}-\frac{x^2}{e^x}\cdot \frac{1}{1-\frac{1}{e}^x}\right|\lt \epsilon\\\\

\left|\frac{-x^2\frac{1}{e}^{xn}}{e^x-1}\right|\lt \epsilon\\\\
\end{gathered}$$

### 2) Wyznacz obszar zbieżności i sumę szeregu $x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\dots$

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=0}{(-1)^n \frac{x^{2n+1}}{2n+1}}\\\\
\lambda=\lim_{n\to \infty}{\left|\frac{(-1)^{n+1}}{2n+2}\cdot \frac{2n+1}{(-1)^n}\right|}=1\\\\
x\in (-1,1)\\\\
\text{dla }x=1\\
S(1)=\sum^{\infty}_{n=0}{(-1)^n \frac{1}{2n+1}}\\
\text{dla }x=-1\\
S(1)=-\sum^{\infty}_{n=0}{(-1)^n \frac{1}{2n+1}}\\

\text{co jest szeregiem naprzemiennym spełniającym założenia}\\
\text{maleje, nieujemne, i zbieżne do 0}\\
\text{Zatem równiż zbieżny}\\
x\in [-1,1]\\
S'(x)=\sum^{\infty}_{n=0}{(-1)^n x^{2n}}=\sum^{\infty}_{n=0}{(-x^2)^n}=\frac{1}{1+x^2}\\\\
\int{\frac{1}{1+x^2}\ dx}=\arctan{x}+C\\
S(0)=0\\
\arctan{0}=0\implies C=0\\\\
\text{Zatem suma tego szeregu to }\arctan{x}, \text{ dla }x\in [-1,1]
\end{gathered}$$

---
### 3. Wyznacz wartość największą i najmniejszą osiąganą przez funkcję $f(x,y,z)=x+y+z$ na zbiorze $V=\{(x,y,z):x^2+y^2\leq z\leq 1\}$

$$\begin{gathered}
\text{Rozpatrując przedziały otwarte:}\\
\frac{\partial f}{\partial x}=1\implies \text{Nie może być ekstremów }\neq 0\\\\
V=(1)\cup (2)\cup (3)\\\\
(1):\\
x^2+y^2\lt z=1\\\\
L(x,y,z,\lambda)=x+y+z+\lambda(z-1)\\
\frac{\partial L}{\partial x}=1\implies \text{Nie może być ekstremów }\neq 0\\\\
(2):\\
x^2+y^2=z\lt 1\\\
L(x,y,z,\lambda)=x+y+z+\lambda(x^2+y^2-z)\\
\frac{\partial f}{\partial x}=1+2\lambda x\\
\frac{\partial f}{\partial y}=1+2\lambda y\\
\frac{\partial f}{\partial z}=1-\lambda\\
\left\{
\begin{matrix}
1+2\lambda x=0\\
1+2\lambda y=0\\
1=\lambda
\end{matrix}
\right. \ \
\left\{
\begin{matrix}
x=-\frac{1}{2}\\
y=-\frac{1}{2}\\
z=\frac{1}{2}
\end{matrix}
\right.\\\\
f(-\frac{1}{2},-\frac{1}{2},\frac{1}{2})=-\frac{1}{2}\\\\
(3):\\
x^2+y^2=z=1\\
L(x,y,\lambda)=x+y+1+\lambda(x^2+y^2-1)\\
\frac{\partial f}{\partial x}=1+2\lambda x=0\\
\frac{\partial f}{\partial y}=1+2\lambda y=0\\
x^2+y^2=1\\
\downarrow\\
x=y=\frac{1}{\sqrt{2}}\vee x=y=-\frac{1}{\sqrt{2}}\\\\
f(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}},1)=\frac{2}{\sqrt{2}}+1=1+\sqrt{2}\\
f(-\frac{1}{\sqrt{2}},-\frac{1}{\sqrt{2}},1)=-\frac{2}{\sqrt{2}}+1=1-\sqrt{2}\\

\end{gathered}$$

---
### 4) Wyznacz środek ciężkości jednorodnej bryły $x^2+y^2+z^2\leq R^2, x\geq 0, y\geq 0, z\geq 0$

$$\begin{gathered}
\begin{vmatrix}
x=r\cos{\theta}\cos{\varphi}\\
y=r\cos{\theta}\sin{\varphi}\\
z=r \sin{\theta}\\
|J|=r^2 \cos{\theta}
\end{vmatrix}\\\\
r^2\leq R^2, \varphi\in [0,\frac{\pi}{2}], \theta\in [0,\frac{\pi}{2}]\\\\
M=p\cdot V=p\cdot \frac{\pi r^3}{6}\\\\
x_0=\frac{M_{OYZ}}{M}\\\\
M_{OYZ}=p\int^{\frac{\pi}{2}}_{0}d \theta \int^{\frac{\pi}{2}}_{0}d \varphi \int^{R}_{0}r^3\cos^2{\theta}\cos{\varphi} dr=
p\int^{\frac{\pi}{2}}_{0}d \theta \int^{\frac{\pi}{2}}_{0}\frac{R^4}{4}\cos^2{\theta}\cos{\varphi}d \varphi =\\=p
\int^{\frac{\pi}{2}}_{0}d \theta \frac{R^4}{4}\cos^2{\theta}=\dots\\\\
\int{\cos^2{x} \ dx}=
\int{\frac{2 \cos^2{x}-1}{2}+\frac{1}{2}\ dx}=\frac{x}{2}+\int{\frac{\cos{2x}}{2}\ dx}=\frac{x}{2}+\frac{\sin{2x}}{4}\\\\
\dots=p\frac{R^4}{4}\cdot \frac{\pi}{4}=p\frac{R^4 \pi}{16}\\\\
x_0=\frac{p\frac{R^4 \pi}{16}}{p\cdot \frac{\pi R^3}{6}}=\frac{3R}{8}\\\\
\text{A z symetrii widać że }x_0=y_0=z_0\\\\
\text{Zatem }Śr=(\frac{3R}{8},\frac{3R}{8},\frac{3R}{8})
\end{gathered}$$


# 2020/2021

## Termin $I$ 

### 1) Wyznacz obszar zbieżności punktowej $D_p$ i sumę szeregu $\sum^{\infty}_{n=1}{\frac{x^2}{(1+x^2)^n}}$. Sprawdź czy ten szereg jest również zbieżny jednostajnie w $D_p$

$$\begin{gathered}
q=\frac{1}{1+x^2}\\\\
\frac{1}{1+x^2}\lt 1\\\\
x^2\gt 0\\\\
x\in \mathbb{R}\\\\
S(x)=\frac{x^2}{1+x^2}\cdot \frac{1}{1-\frac{1}{1+x^2}}=\frac{x^2}{1+x^2}\cdot \frac{1}{\frac{x^2}{1+x^2}}=1, x \neq 0\\
S(0)=0\\\\
S(x)=\left\{
\begin{matrix}
1, x\neq 0\\
0, x=0
\end{matrix}
\right.\\\\
\text{Zatem szereg zbieżny punkowo dla }x\in \mathbb{R}\\
\text{Nie jest zbieżny jednostajnie na podstawie twierdzenia mówiącego}\\
\text{Że zbieżność jednostajna implikuje że funkcja graniczna jest ciągła}

\end{gathered}$$

---
### 2) Korzystając z odpowiedniego szeregu potęgowego oblicz sumę szeregu liczbowego $1-\frac{3}{2^2}+\frac{4}{2^3}-\frac{5}{2^4}+\dots$


$$\begin{gathered}
1-\frac{3}{2^2}+\frac{4}{2^3}-\frac{5}{2^4}+\dots=-\sum^{\infty}_{n=1}{\frac{1+n}{2^n}\cdot (-1)^n}=-\sum^{\infty}_{n=1}{(n+1)\cdot x^n}, x=-\frac{1}{2}\\\\
\lambda=\lim_{n\to \infty}{\frac{n+2}{n+1}}=1\\
x\in (-1,1)\\
\text{zbieżny, różniczkowalny, całkowalny dla }x\in (-1,1)\\
S(x)=-\sum^{\infty}_{n=1}{(n+1)\cdot x^n}\\
\int{S(x)\ dx}=-\sum^{\infty}_{n=1}{x^{n+1}}+C=-\frac{x^2}{1-x}+C\\
S(x)=\left(\int{S(x)\ dx}\right)'=\left(-\frac{x^2}{1-x}+C\right)'=-\frac{2x(1-x)-x^2(-1)}{(1-x)^2}=\frac{x^2-2x}{1-2x+x^2}\\\\
1-\frac{3}{2^2}+\frac{4}{2^3}-\frac{5}{2^4}+\dots=S(-\frac{1}{2})=\frac{\frac{1}{4}+1}{1+1+\frac{1}{4}}=\frac{\frac{5}{4}}{\frac{9}{4}}=\frac{5}{9}
\end{gathered}$$


---
### 3) Wyznacz ekstrema lokalne funkcji uwikłanej $y=y(x)$ danej równaniem: $y^3-(y-\ln{x})^2=y$

$$\begin{gathered}
F(x,y)=y^3-y^2+2y \ln{x}-\ln^2{x}-y=0, x\gt 0\\
\frac{\partial F}{\partial y}=3y^2-2y+2\ln{x}-1\neq 0\\
y'(x)=-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial y}}=0\\
-\frac{\partial F}{\partial x}=0\\
-\frac{2y}{x}+\frac{2\ln{x}}{x}=0, x\neq 0\\

y=\ln{x}\\
F(x,\ln{x})=\ln^3{x}-\ln^2{x}+2\ln^2{x}-\ln^2{x}-\ln{x}=0\\
\ln^3{x}-\ln{x}=0\\
\ln{x}(\ln^2{x}-1)=0\\
\ln{x}=0\vee \ln^2{x}=1\\
x=1, y=0 \vee \ x=e, y=1\vee x=\frac{1}{e}, y=-1\\
F(1,0)=0\\
F(e,1)=2-1-1=0\\
F(\frac{1}{e},-1)=-1-1+2-1+1=0\\
\frac{\partial F}{\partial y}(1,0)=-1\neq 0\\
\frac{\partial F}{\partial y}(e,1)=2\neq 0\\
\frac{\partial F}{\partial y}(\frac{1}{e},-1)=2\neq 0\\
y''(x)=-\frac{\frac{\partial^2 F}{\partial^2 x}}{\frac{\partial F}{\partial y}}(x,y(x))=\frac{\frac{2\ln{x}}{x^2}+2\frac{1-\ln{x}}{x^2}}{3\ln^2{x}-1}\\\\
y''(1)=\frac{2}{-1}=-2\lt 0\\
y''(e)=\frac{\frac{2}{e^2}}{2}\gt 0\\
y''(\frac{1}{e})=\frac{-2e^2+4e^2}{3-1}\gt 0
\end{gathered}$$


---
### 4) Oblicz objętość bryły wyciętej walcem $x^2+y^2=Ry$ z kuli $x^2+y^2+z^2\leq R^2$

$$\begin{gathered}
x^2+(y-\frac{R}{2})^2\leq \frac{1}{4}R^2\\\\
\begin{vmatrix}
x=r \cos{\varphi}\\
y=r \sin{\varphi}\\
\varphi\in [0,\pi]\\
|J|=r
\end{vmatrix}\\\\
r^2=Rr\sin{\varphi}\\
r=R\sin{\varphi}\\\\
z^2\leq R^2-r^2\\
-\sqrt{R^2-r^2}\leq z\leq \sqrt{R^2-r^2}\\\\\
\int^{\pi}_{0}d \varphi \int^{R \sin{\varphi}}_{0}2r\sqrt{R^2-r^2}d r=\dots\\\\
\int{2r \sqrt{R^2-r^2}\ dr}=\begin{vmatrix}
u=R^2-r^2\\
du=-2r
\end{vmatrix}=-\int{\sqrt{u}\ du}=-\frac{u^{\frac{3}{2}}}{\frac{3}{2}}=-\frac{2}{3}(R^2-r^2)^{\frac{3}{2}}\\\\
\dots=-\frac{2}{3}\int^{\pi}_{0}\left[(R^2-R^2\sin^2{\varphi})^{\frac{3}{2}}-R^3\right]=-\frac{2}{3}\int^{\pi}_{0}R^3 \cos^3{\varphi}-R^3 d \varphi=\dots\\\\
\int{\cos^3{\varphi} d \varphi}=
\int{(1-\sin^2{\varphi})\cos{\varphi} d \varphi}=
\begin{vmatrix}
u=\sin{\varphi}\\
du=\cos{\varphi} d \varphi
\end{vmatrix}=\int{1-u^2}=\sin{\varphi}-\frac{\sin^3{\varphi}}{3}\\\\
\dots=-\frac{2}{3}\left(R^3\left[\sin{\varphi}-\frac{\sin^3{\varphi}}{3}\right]^\pi_0-R^3\pi \right)=R^3 \frac{2\pi}{3}
\end{gathered}$$

---
## Termin $II$

### 1) Rozwiń w szereg Maclaurina funkcję $f(x)=\frac{12-5x}{6-5x-x^2}$. Dla jakich $x$ suma otrzymanego szeregu jest równa $f(x)$?

$$\begin{gathered}
f(x)=\frac{12-5x}{6-5x-x^2}=\frac{5x-12}{(x-1)(x+6)}\\
\frac{A}{x-1}+\frac{B}{x+6}=\frac{5x-12}{(x-1)(x+6)}\\
A(x+6)+B(x-1)=5x-12\\\\
\left\{
\begin{matrix}
A+B=5\\
6A-B=-12\\
\end{matrix}
\right. \ \
\left\{
\begin{matrix}
A=-1\\
B=6
\end{matrix}
\right.\\\\
f(x)=\frac{6}{x+6}-\frac{1}{x-1}=\frac{1}{1-(-\frac{x}{6})}+\frac{1}{1-x}=\\
=\sum^{\infty}_{n=0}{(-\frac{x}{6})^n+x^n}=\sum^{\infty}_{n=0}{\left(\left(-\frac{1}{6}\right)^n+1\right)x^n}\\\\

|-\frac{x}{6}|\lt 1 \land |x|\lt 1\implies x\in (-1,1)\\\\
\end{gathered}$$

---
### 2) Rozwiń w szereg sinusów funkcję $f(x)=\pi-x$ w $(0,\pi)$ i narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$


$$\begin{gathered}
f(-x)=-(\pi-x)=x-\pi=-(-x)-\pi\\
\downarrow\\\\
f(x)=\left\{
\begin{matrix}
\pi-x, x\in [0,\pi]\\
-x-\pi, x\in [-\pi,0]
\end{matrix}
\right.\\\\
\text{Warunki Dirichleta:}\\
1) \text{monotoniczna przedziałami }\checkmark \\
2) \text{skończone punkty nieciągłości w których zachodzi }\\ f(x_0)=\frac{\lim_{x\to x_0^-}f(x)+\lim_{x\to x_0^+}f(x)}{2}\checkmark \\
3) f(a)=f(b)=\frac{\lim_{x\to b^-}f(x)+\lim_{x\to a^+}f(x)}{2}\checkmark \\
4) \text{ograniczona }\checkmark \\\\\
b_n=\frac{2}{\pi} \int^{\pi}_{0}{\sin{nx}\left(x-\pi\right)\ dx}=\dots\\\\
\int{\sin{nx}\cdot x\ dx}=\begin{vmatrix}
u=x&dv=\sin{nx}\\
du=1&v=\frac{\cos{nx}}{n}
\end{vmatrix}=\frac{x\cos{nx}}{n}-\int{\frac{\cos{nx}}{n}\ dx}=\\
=\frac{x\cos{nx}}{n}+\frac{\sin{nx}}{n^2}\\\\
\dots=\frac{2}{\pi}\left[\frac{x\cos{nx}}{n}+\frac{\sin{nx}}{n^2}-\pi \frac{\cos{nx}}{n}\right]^\pi_0=\frac{2}{\pi}\left(\frac{\pi (-1)^n}{n}-\frac{\pi(-1)^n}{n}+\frac{\pi}{n}\right)=\frac{2}{n}\\\\\\
f(x)=\sum^{\infty}_{n=1}{\frac{2}{n}\cdot \sin{nx}}, x \in [-\pi,\pi]
\end{gathered}$$

---
### 3) Korzystając z metody Lagrange'a daną liczbę dodatnią $a$ rozłóż na $n$ składników tak, aby suma ich kwadratów była najmniejsza z możliwych.


$$\begin{gathered}
f(x_1,x_2,\dots,x_n,\lambda)=x_1^2+x_2^2+\dots+x_n^2+\lambda(x_1+x_2+\dots+x_n-a)\\\\
\left\{
\begin{matrix}
\frac{\partial f}{\partial x_i}=2x_i+\lambda =0\\
\frac{\partial f}{\partial \lambda}=x_1+x_2+\dots + x_n=a\\

\end{matrix}
\right.\\\\
\left\{
\begin{matrix}
\lambda=-\frac{x_i}{2}\\
x_i=-\frac{\lambda}{2}\\
-\frac{n \lambda}{2}=a\implies \lambda=-\frac{2a}{n}\implies x_i=\frac{a}{n}
\end{matrix}
\right.\\\\
H=\begin{bmatrix}
0&\frac{\partial g}{\partial x_1}&\frac{\partial g}{\partial x_1}&\dots &\frac{\partial g}{\partial x_n}\\

\frac{\partial g}{\partial x_1}&\frac{\partial^2 f}{\partial^2 x_1}&\frac{\partial^2 f}{\partial x_2 x_1} & \dots &\frac{\partial^2 f}{\partial x_n x_1}\\
\frac{\partial g}{\partial x_2}&\frac{\partial^2 f}{\partial x_2x_1}&\frac{\partial^2 f}{\partial^2 x_2} & \dots &\frac{\partial^2 f}{\partial^2 x_n}\\
\vdots&\vdots&\vdots&\ddots&\vdots\\
\frac{\partial g}{\partial x_n}&\frac{\partial^2 f}{\partial x_nx_1}&\frac{\partial^2 f}{\partial x_n x_2} & \dots &\frac{\partial^2 f}{\partial^2 x_n}
\end{bmatrix}=
\begin{bmatrix}
0&1&1&\dots & 1\\
1&2&0&\dots & 0\\
1&0&2&\dots & 0\\
\vdots&\dots&\dots&\ddots&\vdots\\
1&0&0&\dots&2
\end{bmatrix}\\\\
H_2=\begin{vmatrix}
0&1&1\\
1&2&0\\
1&0&2\\
\end{vmatrix}=\begin{vmatrix}
-1&1&1\\
0&2&0\\
0&0&2\\
\end{vmatrix}=-4\\\\
H_k=2^k\cdot -\frac{1}{2}\cdot k\implies H_k\lt 0\\\\
\text{Więc jest to nasze minimum}\\\\
f_{min}(x_1,x_2,\dots,x_n)=n\cdot \frac{a^2}{n^2}=\frac{a^2}{n}
\end{gathered}$$


---
### 4) Oblicz masę nieskończonej bryły $x^2+y^2+z^2\geq 1$ o gęstości $p(x,y,z)=e^{-\sqrt{x^2+y^2+z^2}}$

- Masa bryły $V: M=\underset{V}{\int \int \int}\rho(x,y,z) dx dy dz$
$$\begin{gathered}
\begin{vmatrix}
x=r\cos{\theta}\cos{\varphi}\\
y=r \cos{\theta}\sin{\varphi}\\
z=r \sin{\theta}\\
|J|=r^2\cos{\theta}\\
\varphi \in [0,2\pi]\\
\theta \in [-\frac{\pi}{2}, \frac{\pi}{2}]
\end{vmatrix}\\\\\\
r^2\geq 1\\
p(x,y,z)=e^{-\sqrt{r^2}}=\frac{1}{e^r}\\\\
\int^{2\pi}_{0} d \varphi \int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}d \theta \int^{\infty}_{1}{r^2\cos{\theta}\cdot \frac{1}{e^r} dr}=\dots\\\\
\int{\frac{r^2}{e^r} dr }=\begin{vmatrix}
t=\frac{1}{e^r}\\
dt=-\frac{1}{e^r} dr\\
r=-\ln{t}
\end{vmatrix}=-\int{\ln^2{t}\  dt}=\begin{vmatrix}
u=\ln^2{t}&dv=1\\
du=\frac{2\ln{t}}{t}&v=t
\end{vmatrix}=\\
=-\left(\ln^2{t}\cdot t-\int{2 \ln{t} dt}\right)=-\left(\ln^2{t}\cdot t-2(\ln{t}\cdot t-t)\right)=\\
=-(e^{-r}-2(-e^{-r}-e^{-r}))=-5e^{-r}\\\\
\dots=\int^{2\pi}_{0} d \varphi \int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}\frac{5}{e}\cos{\theta}d \theta =\int^{2\pi}_{0}\frac{10}{e}d \varphi=\frac{20 \pi}{e}
\end{gathered}$$

---
## Termin $III$

### 1) Sprawdź, czy szereg $\sum^{\infty}_{n=1}{x^n(1-x)}$ jest jednostajnie zbiezny na przedziale:

#### a) $[0,1]$

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=1}{x^n(1-x)}=\frac{x-x^2}{1-x}=x, x\in [0,1)\\\\
S(1)=0\\\\
\text{funkcja graniczna nie jest ciągła a co za tym idzie szereg }\\
\text{nie może być zbieżny jednostajnie}
\end{gathered}$$

#### b) $[0,\frac{1}{2}]$

$$\begin{gathered}
\sum^{\infty}_{n=1}{x^n(1-x)}\lt \sum^{\infty}_{n=1}{\frac{1}{2^{n+1}}}-\text{Zbieżny punktowo}\\\\
\text{na podstawie tw. Weirestrassa szereg jest zbieżny jednostajnie}
\end{gathered}$$

#### c) $[0,1)$

$$\begin{gathered}
\forall \epsilon \gt0 \exists n_0 : \forall n\gt n_0 \forall x \in X: |S_n(x)-S(x)|\lt \epsilon\\\\
|S_n(x)-S(x)|=\left|x\frac{1-x^n}{1-x}-x^2 \frac{1-x^n}{1-x}-x \right|=|x-x^{n+1}-x|=\\
=|x^{n+1}|\\\\
\text{nie istnieje takie }n_0 \text{, zawsze znajdzie sie x bliższy 1}\\
\text{przez co nigdy n nie będzie odpowiednio duże żeby pokryć już wszystkie}\\
\text{możliwe wartości x dla jakiegoś epsilona}
\end{gathered}$$

---
### 2) Wyznacz obszar zbieżności i sumę szeregu $\sum^{\infty}_{n=1}{\frac{(-1)^n(x-1)^{2n}}{n\cdot 4^n}}$

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=1}{\frac{(-1)^n(x-1)^{2n}}{n\cdot 4^n}}\overset{(x-1)^2=u}{=}
\sum^{\infty}_{n=1}{\frac{(-1)^nu^n}{n\cdot 4^n}}\overset{h=-u}{=}=
\sum^{\infty}_{n=1}{\frac{h^n}{n\cdot 4^n}}\\\\
\lambda=\lim_{n\to \infty}{\left|n\cdot 4^n \over (n+1)\cdot 4\cdot 4^n\right|}
=\frac{1}{4}\\\\
h\in (-4,4)\\
-u \in (-4,4)\\
-(x-1)^2\in (-4,4)\\
(x-1)^2\lt 4\\
x-1\lt 2\land x-1\gt -2\\
x\lt 3\land x\gt -1\implies x\in (-1,3)\\\\
\lim_{x\to 3^-}{S(x)}=\sum^{\infty}_{n=1}{\frac{(-1)^n}{n\cdot 4^n}}\\\\
\text{zbiezny bo szereg naprzemienny spełniający założenia}:\\
a_n-\text{malejące}\\
a_n\to 0\\
a_n\gt 0\\\\
\lim_{x\to -1^+}{S(x)}=\sum^{\infty}_{n=1}{\frac{1}{n\cdot 4^n}}\lt\sum^{\infty}_{n=1}{\frac{1}{4^n}}\\\\
\text{zbiezny na podstawie kryterium porównawczego z szeregiem geometrycznym}\\
\text{o ilorazie mniejszym od 1 i większym od -1}\\\\
\text{Zatem }S(x) \text{zbieżny w }[-1,3]\\\\

\end{gathered}$$

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=1}{\frac{(-1)^n(x-1)^{2n}}{n\cdot 4^n}}\\\\
S'(x)=\sum^{\infty}_{n=1}{\frac{2(-1)^n(x-1)^{2n-1}}{4^n}}=2\sum^{\infty}_{n=1}{\frac{(-1)^n(x-1)^{2n-1}}{4^n}}=\\=-\frac{1}{2}(x-1)\cdot \frac{1}{1-(-\frac{1}{4}(x-1)^2)}=\frac{1-x}{2+\frac{1}{2}(x-1)^2}=\frac{2-2x}{4+(x-1)^2}\\\\
S(x)=\int{\frac{2-2x}{4+(x-1)^2} dx}=\begin{vmatrix}
u=x-1\\
du=dx
\end{vmatrix}=\int{\frac{-2u}{4+u^2}}=\begin{vmatrix}
t=4+u^2\\
dt=2u \ du
\end{vmatrix}=\\
=-\int{t^{-1}}=-\ln{t}+C=-\ln{(4+(x-1)^2)}+C\\\\
S(1)=0\implies C=\ln{4}\\\\
S(x)=\ln{\left(\frac{4}{4+(x-1)^2}\right)}

\end{gathered}$$

---
### 3) Zbadaj różniczkowalność w całej dziedzinie funkcji $f(x,y)=\left\{\begin{matrix}\frac{y^4-x^3}{x^2+y^2}, (x,y)\neq (0,0)\\ 0, (x,y)=(0,0)\end{matrix}\right.$

$$\begin{gathered}
\text{Ciągłość:}\\\\
\lim_{(x,y)\to (0,0)}f(x,y)=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
\varphi-dowolny\\
r\to 0
\end{vmatrix}=\lim_{r\to 0}{\frac{r^3(r\sin{\varphi}-\cos{\varphi})}{r^2}}=0\\\\\

\frac{\partial f}{\partial x}(0,0)=\lim_{\Delta x\to 0}{\frac{f(\Delta x,0)-f(0,0)}{\Delta x}}=\lim_{\Delta x\to 0}{\frac{-(\Delta x)^3}{(\Delta x)^3}}=-1\\
\frac{\partial f}{\partial y}(0,0)=\lim_{\Delta y\to 0}{\frac{f(0,\Delta y)-f(0,0)}{\Delta y}}=\lim_{\Delta y\to 0}{\frac{(\Delta x)^4}{(\Delta x)^3}}=0\\\\
f((0,0)+h)-f(0,0)=\frac{\partial f}{\partial x}(0,0)h_x+\frac{\partial f}{\partial x}(0,0)h_y+r_{(0,0)}(h)\\\\
\frac{h_y^4-2h_x^3-h_xh_y^2}{h_x^2+h_y^2}=r_{(0,0)}(h)\\\\
\lim_{h\to 0}{\frac{h_y^4-2h_x^3-h_xh_y^2}{(h_x^2+h_y^2)^{\frac{3}{2}}}}=\begin{vmatrix}
h_x=r\cos{\varphi}\\
h_y=r\sin{\varphi}\\
\varphi-dowolny\\
r\to 0
\end{vmatrix}=\lim_{r\to 0}{\frac{r^3(r \sin{\varphi}-2\cos{\varphi}-\sin^2{\varphi}\cos{\varphi})}{r^3}}=\\\\
=-2\cos{\varphi}-\sin^2{\varphi}\cos{\varphi}\\\\
\text{Zależne od kąta - można przyjąć }y=0, x=\frac{1}{n}\text{ oraz }x=y=\frac{1}{n}\\
\text{i wykazać że wychodzą rózne wartości co oznacza że różniczkowalna nie jest w tym}\\
\text{punkcie, ale poza }(0,0) \text{ jest różniczkowalna jako iloraz funkcji }\\
\text{różniczkowalnych (wielomianów)}

\end{gathered}$$

---
### 4) Oblicz objętość bryły ograniczonej powierzchniami $x^2+y^2+z^2=4$ i $x^2+y^2=3z$ do której należy punkt $A(0,0,1)$

$$\begin{gathered}
\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
\varphi\in [0,2\pi]\\
|J|=r
\end{vmatrix}\\\\\
z^2=4-r^2\\
3z=r^2\\\
x^2+y^2+z^2=4
\text{ kula},x^2+y^2=3z \text{ coś ala stożek}\\\\
\text{Jeśli należy tam punkt }(0,0,1) \text{ oznacza to że kula ogranicza z góry}\\
\text{a stożek z dołu}\\\\
z^2=\frac{r^4}{9}=4-r^2\implies r^4+9r^2-36=0\\
\Delta=81+144=225=15^2\\
r^2=\frac{-9-15}{2}\vee r^2=\frac{-9+15}{2}=3\implies r=\sqrt{3}
\int^{2\pi}_{0}d \varphi \int^{\sqrt{3}}_{0} dr \int^{\sqrt{4-r^2}}_{\frac{r^2}{3}}r dz=\\
=\int^{2\pi}_{0}d \varphi \int^{\sqrt{3}}_{0}r \sqrt{4-r^2}-\frac{r^3}{3} dr =\dots\\
\int{r \sqrt{4-r^2}}=\begin{vmatrix}
u=4-r^2\\
du=-2r dr
\end{vmatrix}=-\frac{1}{2}\int{\sqrt{u} du}=-\frac{1}{2}\frac{2u^{\frac{3}{2}}}{3}=-\frac{(4-r^2)^{\frac{3}{2}}}{3}\\\\
\dots=\int^{2\pi}_{0}\left[-\frac{(4-r^2)^{\frac{3}{2}}}{3}-\frac{r^4}{12}\right]^\sqrt{3}_0d \varphi =\int^{2\pi}_{0}{-\frac{1}{3}-\frac{9}{12}+\frac{8}{3}d\varphi}=\\
=2\pi\cdot \frac{19}{12}=\frac{19\pi}{6}
\end{gathered}$$
---



---

# 2021/2022

## Termin $I$

### 1) Wyznacz obszar zbieżności punktowej $D_p$ i sumę szeregu $\sum^{\infty}_{n=1}{(-1)^ne^{-xn}}$. Sprawdź,czy szereg ten jest również zbieżny jednostajnie w $D_p$

$$\begin{gathered}
\sum^{\infty}_{n=1}{(-1)^ne^{-xn}}=\sum^{\infty}_{n=1}{(-1)^n \frac{1}{e^{xn}}}\\\\
\text{traktując x jako stałą mamy:}\\
a_n=\frac{1}{e^{xn}}\\
\text{dla: }x\gt 0\\\\
1. \text{dąży do 0}\\
2. \text{wyrazy maleją}\\
\text{więc szereg zbiega}\\\\
\text{dla: }x= 0\\\\
\sum^{\infty}_{n=1}{(-1)^n\cdot 1}-\text{nie zbiega do niczego (oscylują kolejne wyrazy -1 +1)}\\\\
\text{gdy: }x\lt 0\\\\
a_n\to \infty - \text{nie zbiega a wręcz z każdym kolejnym wyrazem rośnie}\\\\
D_p=(0,+\infty)\\\\
Suma:\\\\
\sum^{\infty}_{n=1}{(-1)^ne^{-xn}}=\sum^{\infty}_{n=1}{{(-e^{-x}})^n}=\frac{-e^{-x}}{1-(-e^{-x})}=\frac{-e^{-x}}{1+e^{-x}}, x\in (0,+\infty)
\end{gathered}$$


### 2) Rozwiń w szereg Taylora o środku $x_0=-1$ funkcję $f(x)=\ln(x^2+2x+2)$. Dla jakich $x$ funkcja $f(x)$ jest równa sumie otrzymanego rozwinięcia?

$$\begin{gathered}
f(x)=\ln(x^2+2x+2)\\\\
\Delta=4-8
\lt 0 \ \land \ a\gt 0 \implies \forall x \in \mathbb{R} \ \ x^2+2x+2\gt 0 \\\\
f'(x)=\frac{1}{x^2+2x+2}\cdot (2x+2)=\frac{2x+2}{x^2+2x+2}=\frac{2x+2}{1-(-x^2-2x-1)}=\\
=\frac{2x+2}{1-(-(x+1)^2)}\\\\
f'(x)=\sum^{\infty}_{n=0}{(2x+2)\cdot (-(x+1)^2)^n}=\dots, \ \ |-(x+1)^2|\lt 1
\\
-1\lt x+1\lt 1 \\
-2\lt x\lt 0\\
x\in (-2,0)
\\
\dots=\sum^{\infty}_{n=0}(2x+2) \cdot (-1)^n \cdot(x+1)^{2n}\\\\
f(x)=\int{f'(x)\ dx}=\int{
\sum^{\infty}_{n=0}2\cdot  (-1)^n \cdot(x+1)^{2n+1}dx}=\\=
\sum^{\infty}_{n=0}{2\cdot (-1)^n\cdot \frac{(x+1)^{2n+2}}{2n+2}}+C\\\\\
f(-1)=\ln(1-2+2)=0\implies C=0\\\\
f(x)=\sum^{\infty}_{n=0}{2\cdot (-1)^n\cdot \frac{(x+1)^{2n+2}}{2n+2}}, x\in (-2,0)
\end{gathered}$$


---
### 3) Dana jest funkcja $\left\{\begin{matrix}\frac{y^3}{x^2+y^2}, (x,y)\neq (0,0) \\ 0, (x,y)=(0,0)\end{matrix}\right.$

#### a) Sprawdź czy dana pochodna cząstkowa $\frac{\partial f}{\partial y}$ istnieje i jest ciągła w punkcie $(0,0)$


$$\begin{gathered}
\lim_{\Delta y\to 0}{\frac{f((0,0+\Delta y))-f(0,0)}{\Delta y}}=\lim_{\Delta y\to 0}{\frac{\frac{\Delta y^3}{\Delta y^2}}{\Delta y}}=1\\\\
\text{tak, istnieje }\\\\
\frac{\partial f}{\partial y}=\frac{3y^2(x^2+y^2)-2y^4}{(x^2+y^2)^2}\\\\
\lim_{(x,y)\to (0,0)}\frac{\partial f}{\partial y}=\lim_{(x,y)\to (0,0)}\frac{3y^2(x^2+y^2)-2y^4}{(x^2+y^2)^2}=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
r\to 0\\
\varphi - dowolne
\end{vmatrix}=\\=\lim_{r\to 0}{\frac{3r^4\sin^2{\varphi}-2r^4{\cos^4{\varphi}}}{r^4}}=3\sin^2{\varphi}-2\cos^4{\varphi}- \text{Zależne od }\varphi\\\\
\text{Należałoby jeszcze udowodnić że to faktycznie zależne od }\varphi\\
\text{ponieważ może się tak tylko wydawac na pierwszy rzut oka a w rzeczywistosci}\\
\text{się zerować:}\\\\
\text{dla: }\varphi=0\implies -2\\
\text{dla: }\varphi=\frac{\pi}{2}\implies 3\\

\end{gathered}$$
#### b) Sprawdź różniczkowalność funkcji $f$ w punkcie $(0, 0)$

$f: D\to \mathbb{R}^m, \ \ \ D\subset \mathbb{R}^n$
$x_0\in U \subset D$
Mówimy, że $f$ jest różniczkowalna w $x_0 \Leftrightarrow$ gdy istnieje takie odzorowanie liniowe:
$L_{x_0}: \mathbb{R}^n \to \mathbb{R}^m$, że:
$$\begin{gathered}
\forall h \in \mathbb{R}^n \ \ \ f(x_0+h)-f(x_0)=L_{x_0}(h)+r_{x_0}(h)
\end{gathered}$$
gdzie $\lim_{h\to 0}{\frac{r_{x_0}(h)}{||h||}}=0$, $r_{x_0}(h)$ - reszta
oznaczenie: $L_{x_0}=df(x_0)$ - różniczka funkcji $f$ w punkcie $x_0$
$L_{x_0}(h) = df(x_0)(h)$


$$\begin{gathered}
\forall h\in \mathbb{R}^2\ \ \ f((0,0)+h)-f(0,0)=(\frac{\partial f}{\partial x}(0,0)+\frac{\partial f}{\partial y}(0,0))(h)+r_{(0,0)}(h)\\\\
\frac{h_y^3}{h_x^2+h_y^2}=h_y+r_{(0,0)}(h)\\\\
\frac{-h_yh_x^2}{h_x^2+h_y^2}=r_{(0,0)}(h)\\\\
\lim_{h\to 0}{\frac{-h_yh_x^2}{(h_x^2+h_y^2)^{\frac{3}{2}}}}=\begin{vmatrix}
x=r\cos{\varphi}\\
y=r\sin{\varphi}\\
r\to 0\\
\varphi - dowolny
\end{vmatrix}=\lim_{r\to 0}{\frac{-r^3 \sin{\varphi}\cos^2{\varphi}}{r^3}}=-\sin{\varphi}\cos^2{\varphi}\neq 0
\end{gathered}$$

---
### 4) Oblicz objętość części wspólnej walców $x^2+y^2=R^2$ i $x^2+z^2=R^2$

$$\begin{gathered}
x\in [-R,R]\\
y=\sqrt{R^2-x^2}\vee y=-\sqrt{R^2-x^2}\\\\
z=\sqrt{R^2-x^2}\vee z=-\sqrt{R^2-x^2}\\\\
\int^{R}_{-R}{dx}\int^{\sqrt{R^2-x^2}}_{-\sqrt{R^2-x^2}}{dy}\int^{\sqrt{R^2-x^2}}_{-\sqrt{R^2-x^2}}{dz}=
\int^{R}_{-R}{dx}\int^{\sqrt{R^2-x^2}}_{-\sqrt{R^2-x^2}}{dy}2\sqrt{R^2-x^2}=\\
=\int^{R}_{-R}{4R^2-4x^2\ dx}=\frac{16R^3}{3}

\end{gathered}$$

---
## Termin $II$

### 1) Zbadaj zbieżność szeregu liczbowego $\sum^{\infty}_{n=1}{\frac{\sqrt{n}}{e^{\sqrt{n}}}}$
**Twierdzenie o kryterium całkowym**:
zał: $\sum{a_n}$
$\forall n \geq n_0 \ \ a_n\geq 0$
$f: [n_0, +\infty] \to \mathbb{R}_+$
$\forall n \geq n_0 \ \ a_n=f(n)$
$f$ jest nierosnąca na przedziale $[n_0,+\infty]$

teza: $\sum{a_n}$ jest zbieżny $\Leftrightarrow \int^{+\infty}_{n_0}{f(x) \ dx}$ jest zbieżna

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{\sqrt{n}}{e^{\sqrt{n}}}}\\\\
a_n=\frac{\sqrt{n}}{e^{\sqrt{n}}}\geq 0 \ \ \ \forall n\geq 1\\\\
f(n)=\frac{\sqrt{n}}{e^{\sqrt{n}}}- \text{nierosnąca co widać ale może trzeba udowodnić}\\\\
f'(n)=\frac{e^\sqrt{n}-\sqrt{n}e^\sqrt{n}}{e^{2\sqrt{n}}}\cdot \frac{1}{2\sqrt{n}}\lt 0 \Leftrightarrow e^{\sqrt{n}}-\sqrt{n}e^{\sqrt{n}}\lt 0\\
\text{a tak jest zawsze dla n które rozpatrujemy czyli większych od 1}\\\\
\text{Zatem spełnione są założenia kryterium całkowego:}\\\\
\int^{+\infty}_{1}{\frac{\sqrt{n}}{e^{\sqrt{n}}}\ dn}=\begin{vmatrix}
u=\sqrt{n}\\
du=\frac{1}{2\sqrt{n}}dn\\
du\cdot 2\sqrt{n}=dn
\end{vmatrix}=\int^{+\infty}_{1}{\frac{2u^2}{e^u}\ du}=\begin{vmatrix}
a=u^2&b'=e^{-u}\\
da=2u&b=-e^{-u}
\end{vmatrix}=\\
=2\left(-\frac{u^2}{e^{u}}-\int{-\frac{2u}{e^u}}\right)|^{+\infty}_1=
2\left(-\frac{u^2}{e^{u}}+2\int{\frac{u}{e^u}}\right)|^{+\infty}_1=
\begin{vmatrix}
c=u&df=\frac{1}{e^u}\\
dc=1&f=-\frac{1}{e^u}
\end{vmatrix}=\\
=2\left(-\frac{u^2}{e^{u}}+2\left(-\frac{u}{e^u}-\int{-\frac{1}{e^u}}\right)\right)|^{+\infty}_1=
2\left(-\frac{u^2}{e^{u}}+2\left(-\frac{u}{e^u}-\frac{1}{e^u}\right)\right)|^{+\infty}_1=\\
=2\left(-\frac{n}{e^{\sqrt{n}}}+2\left(-\frac{\sqrt{n}}{e^\sqrt{n}}-\frac{1}{e^\sqrt{n}}\right)\right)|^{+\infty}_1=2\lim_{n\to \infty}{\dots}-2\left(-\frac{1}{e}+2(-\frac{1}{e}-\frac{1}{e}\right)=\\
=-2\cdot -\frac{5}{e}=\frac{10}{e}-\text{cała zbieżna to i szereg też}
\end{gathered}$$

---
### 2) Korzystając z odpowiedniego szeregu potęgowego oblicz sumę szeregu $1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}\dots$

$$\begin{gathered}
\text{ZAPAMIĘTAJ:}\\
\arctan{x}=\int{\frac{1}{1+x^2}}=\int{\frac{1}{1-(-x^2)}}=\int{\sum^{\infty}_{n=0}{(-1)^n\cdot x^{2n}}}=\sum^{\infty}_{n=0}{\frac{(-1)^n}{2n+1}\cdot x^{2n}}\\\\
\arctan{1}=\frac{\pi}{4}=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots\\\\
\end{gathered}$$

**Przypomnienie jak wyprowadzić pochodne funkcji trygo**

$$\begin{gathered}
\tan'(x)=\left(\frac{\sin{x}}{\cos{x}}\right)'=\frac{\cos^2{x}-\sin{x}\cdot (-\sin{x})}{\cos^2{x}}=\frac{1}{\cos^2{x}}\\
\downarrow\\
(\arctan{(\tan{x})})'=x'\\
\arctan'{(\tan{x})}\cdot \frac{1}{\cos^2{x}}=1\\
\arctan'{(\tan{x})}=\cos^2{x}\\
\arctan'{(\frac{\sqrt{1-\cos^2{x}}}{\cos{x}})}=\cos^2{x}\\\\
u=\frac{\sqrt{1-\cos^2{x}}}{\cos{x}}\\
u^2=\frac{1-\cos^2{x}}{\cos^2{x}}\\
u^2=\frac{1}{\cos^2{x}}-1\\
\frac{1}{u^2+1}=\cos^2{x}\\\\
\arctan'{(u)}=\frac{1}{u^2+1}
\end{gathered}$$


---
### 3) Wyznacz ekstrema warunkowe funkcji $f(x,y,z)=x-2y+2z$ przy warunku $x^2+y^2+z^2=1$


$$\begin{gathered}
f(x,y,z,\lambda)=x-2y+2z+\lambda(x^2+y^2+z^2-1)\\\\
\frac{\partial f}{\partial x}=1+2\lambda x=0\\
\frac{\partial f}{\partial y}=-2+2\lambda y=0\\
\frac{\partial f}{\partial z}=2+2\lambda z=0\\
\frac{\partial f}{\partial \lambda}=x^2+y^2+z^2-1=0\\\\

\left\{
\begin{matrix}
1+2\lambda x=0\\
-2+2\lambda y=0\\
2+2\lambda z=0\\
x^2+y^2+z^2-1=0
\end{matrix}
\right. \ \ \
\left\{
\begin{matrix}
x=-\frac{1}{2\lambda}\\
y=\frac{1}{\lambda}\\
z=-\frac{1}{\lambda}\\
\frac{1}{4\lambda^2}+\frac{1}{\lambda^2}+\frac{1}{\lambda^2}-1=0\implies \lambda^2=\frac{9}{4}\\
\lambda=\frac{3}{2}\vee \lambda=-\frac{3}{2}
\end{matrix}
\right.\\\\
\lambda=\frac{3}{2}\implies x=-\frac{1}{3},y=\frac{2}{3}, z=-\frac{2}{3}\\\\
H=\begin{bmatrix}
0&2x&2y&2z\\
2x&2\lambda&0&0\\
2y&0&2\lambda&0\\
2z&0&0&2\lambda
\end{bmatrix}=\begin{bmatrix}
0&-\frac{2}{3}&\frac{4}{3}&-\frac{4}{3}\\
-\frac{2}{3}&3&0&0\\
\frac{4}{3}&0&3&0\\
-\frac{4}{3}&0&0&3
\end{bmatrix}\\\\
H_2=\begin{vmatrix}
0&-\frac{2}{3}&\frac{4}{3}\\
-\frac{2}{3}&3&0\\
\frac{4}{3}&0&3\\
\end{vmatrix}=-\frac{20}{3}\\\\
H_3=\begin{vmatrix}
0&-\frac{2}{3}&\frac{4}{3}&-\frac{4}{3}\\
-\frac{2}{3}&3&0&0\\
\frac{4}{3}&0&3&0\\
-\frac{4}{3}&0&0&3
\end{vmatrix}=
\begin{vmatrix}
-\frac{20}{27}&-\frac{10}{3}&\frac{4}{3}&-\frac{4}{3}\\
0&3&0&0\\
0&0&3&3\\
0&0&0&3
\end{vmatrix}=-20\\\\
\text{minimum lokalne równe: }-\frac{1}{3}-\frac{4}{3}-\frac{4}{3}=-3
\end{gathered}$$

Teza:
1) $\forall k=2,\dots,n \ \ H_k\lt 0 \implies f$ ma minimum lokalne warunkowe w punkcie $x_0$
2) $\forall k=2,\dots,n \ \ (-1)^{k+1}H_k\lt 0 \implies f$ ma maksimum lokalne warunkowe w punkcie $x_0$
3) Jeśli nie zachodzi ani $(\forall k=2,\dots,n \ \ H_k\leq 0)$, ani $(\forall k=2,\dots,n) \ \ (-1)^{k+1}H_k\leq 0)$ to $f$ nie ma ekstremum lokalnego warunkowego w punkcie $x_0$
---
### 4) Oblicz moment bezwładności jednorodnej bryły $V=\{(x,y,z):x^2+y^2+z^2\leq 2, z\geq 1\}$ o gęstości $p$.

$$\begin{gathered}
M_b=\underset{V}{\int \int \int}(x^2+y^2)\rho(x,y,z)dV\\\\

\end{gathered}$$
---
## Termin $III$

### 1) Wyznacz sumę szeregu funkcyjnego $\sum^{\infty}_{n=1}{\frac{x^2}{(1+x^2)^n}}$ na $\mathbb{R}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{x^2}{(1+x^2)^n}}=x^2 \sum^{\infty}_{n=1}{\left(\frac{1}{1+x^2}\right)^n}=x^2\cdot \frac{\frac{1}{1+x^2}}{1-\frac{1}{1+x^2}},\ \ \ |\frac{1}{1+x^2}|\lt 1\implies x^2 \gt 0\\\\
\dots=\frac{\frac{1}{1+x^2}}{\frac{x^2}{1+x^2}}\cdot x^2=1\\\\
x=0:\\\\
\dots=0\\\\
S(x)=\left\{
\begin{matrix}
1, x\neq 0\\
0, x=0
\end{matrix}
\right.
\end{gathered}$$

**I sprawdź czy ten szereg jest jednostajnie zbieżny na $\mathbb{R}$**

$$\begin{gathered}
\text{funkcja graniczna szeregu nie jest ciągła zatem ciąg nie może być jednostajnie zbieżny}
\end{gathered}$$

---
### 2) Rozwiń w szereg Maclaurina funkcję $f(x)=\arctan{x^2}$. Dla jakich $x$ otrzymany szereg jest zbieżny? Dla jakich $x$ wartość $f(x)$ jest równa sumie otrzymanego szeregu.

$$\begin{gathered}
(\arctan{x^2})'=\frac{2x}{1+x^4}=\frac{2x}{1-(-x^4)}=\sum^{\infty}_{n=0}{2x\cdot (-1)^n\cdot x^{4n}}, |-x^4|\lt1\\\\
\int{(\arctan{x^2})' \ dx}=\sum^{\infty}_{n=0}{2\cdot (-1)^n\cdot \frac{x^{4n+2}}{4n+2}}+C, C=0 \text{ bo arctan(0)=0}\\\\

\end{gathered}$$

---
### 3) Zbadaj różniczkowalność funkcji $f(x,y)=\sqrt{x^2+y^2}$ w całej dziedzinie. Podaj wypowiedzi dwóch twierdzeń, z których skorzystałeś (jedno gdy $(x,y)\neq (0,0)$ drugie gdy $(x,y)=(0,0)$).


$$\begin{gathered}
\text{Złożenie funkcji różniczkowalnych jest różniczkowalne w dziedzinie }\\
\text{różniczkowalności ograniczonej przez te funkcje}\\
\text{więc }\sqrt{u}\text{ jest różniczkowalne }\forall u \gt 0\\
x^2+y^2 \text{ jest różniczkowalne w całej dziedzinie.}\\\\
\text{Zatem }f(x,u)=\sqrt{x^2+y^2} \text{ jest różniczkowalne }\\
\text{dla każdego }(x,y): x^2+y^2\gt 0 \implies (x,y)\neq (0,0)\\\\
\text{A dla }(x,y)=(0,0)\\\\
\text{z WK różniczkowalności w punkcie, pochodne}\\
\text{cząstkowe istnieją w tym punkcie}\\\\
\lim_{\Delta x\to 0}{\frac{\sqrt{(\Delta x)^2}}{\Delta x}}=|\Delta x| - \text{ nie istnieje (-1 lub 1)}\\\\
\text{A co za tym idzie nie można mówić o różniczkowalności w tym punkcie.}
\end{gathered}
$$

---
### 4) Wyznacz esktrema lokalne funkcji uwikłanej $y=y(x)$ danej równaniem:


Zał: $F: D\to \mathbb{R} \ \ \ D\subseteq \mathbb{R}^2$
$F(x,y)=0$
$F(x_0,y_0)=0$
$U$ - otoczenie punktu $(x_0,y_0)$
$F\in C^1(U)$
$\frac{\partial F}{\partial y}(x_0,y_0)\neq 0$

Teza: 
1) istnieje takie otoczenie $V$ punktu $x_0$ i takie otoczenie $W$ punktu $y_0$ oraz istnieje taka funkcja $y=V\to W$, że $\forall x \in V \ \ F(x,y(x))=0$
(czyli istnieje funkcja uwikłana $y=y(x)$ dana równaniem $F(x,y)=0$ w otoczeniu punktu $(x_0,y_0)$)

2) Ponadto 
   $y'(x_0)=-\frac{\frac{\partial F}{\partial x}(x_0,y_0)}{\frac{\partial F}{\partial y}(x_0,y_0)}$

3) A jeżeli $F\in C^2(U)$ oraz $y'(x_0)=0$
   to: $y''(x_0)=-\frac{\frac{\partial^2 F}{\partial x^2}(x_0,y_0)}{\frac{\partial F}{\partial y}(x_0,y_0)}$

$$\begin{gathered}
x^4-2x^2y-x^2+y^2+y=0\\
(x^2-y)^2-(x^2-y)=0\\
(x^2-y-1)(x^2-y)=0\\\\
y_1=x^2\vee y_2=x^2-1\\\\
(y_1(x))'=2x=0 \Leftrightarrow x=0\ \ \ y_1(0)=0\\\\
(y_2(x))'=2x=0\Leftrightarrow x=0 \ \ \ y_2(0)=-1\\\\
\end{gathered}$$
---
### 5) Oblicz objętość części wspólnej kuli $x^2+y^2+z^2\leq R^2$ i walca $x^2+y^2-Rx\leq 0$

$$\begin{gathered}
x^2+y^2-Rx\leq 0\\
(x^2-\frac{1}{2}R)^2+y^2\leq \frac{1}{4}R^2\\\\
x\in \left[\frac{1}{4}R, \frac{3}{4}R\right],\ \  y\in \left[-\sqrt{x^2-Rx}, \sqrt{x^2-Rx}\right]\\\\
z\in \left[-\sqrt{R^2-x^2-y^2}, \sqrt{R^2-x^2-y^2}\right]\\\\
\text{Gdzie wyrazimy x i y za pomocą współrzędnych biegunowych:}\\\\
\begin{vmatrix}
x=r \cos{\varphi}\\
y=r \sin{\varphi}\\
|J|=r
\end{vmatrix}\\\\\
\varphi\in [-\frac{\pi}{2}, \frac{\pi}{2}], \ \ \
r\in \left[0, R \cos{\varphi}\right]\\
z\in [-\sqrt{R^2-r^2}, \sqrt{R^2-r^2}]\\\\\\\
\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}d \varphi \int^{R \cos{\varphi}}_{0} dr \int^{\sqrt{R^2-r^2}}_{-\sqrt{R^2-r^2}} r dz=
\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}d \varphi \int^{R \cos{\varphi}}_{0} 2r\sqrt{R^2-r^2}dr=\\\\
=\begin{vmatrix}
u=R^2-r^2\\
du=-2r\ dr
\end{vmatrix}=
\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}d \varphi \int^{R^2-R^2 \cos^2{\varphi}}_{R^2} -\sqrt{u}dr=\\
=-\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}} \left[\frac{2u^\frac{3}{2}}{3}\right]^{R^2-R^2 \cos^2{\varphi}}_{R^2}=-\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}\left[\frac{2R^3(\sin{\varphi}^3-1)}{3}\right]=\\
=\frac{2R^3}{3}\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}(1-\sin^3{\varphi}) d \varphi=(\sin^3\text{nieparzysta})=\\
=\frac{2R^3}{3}\int^{\frac{\pi}{2}}_{-\frac{\pi}{2}}1 \varphi=\frac{2R^3}{3}
\end{gathered}$$

---
# 2022/2023

## Termin $I$

### 1) Korzystając z odpowiedniego szeregu potęgowego oblicz sumę szeregu liczbowego

$$\begin{gathered}
1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}=\sum^{\infty}_{n=0}{\frac{(-1)^n}{2n+1}}\\\\
(\arctan{x})'=\frac{1}{1+x^2}=\frac{1}{1-(-x^2)}=\sum^{\infty}_{n=0}{(-x^2)^n}=
\sum^{\infty}_{n=0}{(-1)^nx^{2n}}\\\\
\arctan{x}=\int \left(\sum^{\infty}_{n=0}{(-1)^nx^{2n}}\right) dx=\sum^{\infty}_{n=0}{\frac{(-1)^n}{2n+1}x^{2n+1}}\\\\
\arctan{1}=\sum^{\infty}_{n=0}{\frac{(-1)^n}{2n+1}}=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}\dots=\frac{\pi}{4}
\end{gathered}$$

---
### 2) Korzystając z metody Lagrange'a wyznacz wymiary prostopadłościanu o największej objętości, jeśli suma pól powierzchni wszystkich ścian jest równa 6.

$$\begin{gathered}
f(x,y,z)=xyz\\\\
2xy+2xz+2yz=6\\\\
F(x,y,z,\lambda)=xyz+\lambda(2xy+2xz+2yz-6)\\\\
\left\{
\begin{matrix}
\frac{\partial f}{\partial x}=yz+2\lambda y+2\lambda z=0\\
\frac{\partial f}{\partial y}=xz+2\lambda x+2\lambda z=0\\
\frac{\partial f}{\partial z}=xy+2\lambda x+2\lambda y=0\\
2xy+2xz+2yz-6=0
\end{matrix}
\right.\\\\
x=y=z=1\\\\

\end{gathered}$$
$$\begin{gathered}
H=\begin{bmatrix}
0&4&4&4\\
4&0&1&1\\
4&1&0&1\\
4&1&1&0
\end{bmatrix}\\\\
H_2=16+16=32\\\\
H_3=-48\\\\
(-1)^{k+1}H_k\lt 0\checkmark \implies \text{maksimum}
\end{gathered}$$
---
### 3) Oblicz objętość nieograniczonego obszaru zawartego między płaszczyzną $z=0$ i powierzchnią $z=(x^2+y^2)e^{-(x^2+y^2)}$

$$\begin{gathered}
\begin{vmatrix}
x=r \cos{\varphi}\\
y=r \sin{\varphi}\\
|J|=r
\end{vmatrix}\\\\
z=\frac{r^2}{e^{r^2}}\\\\
\int^{2\pi }_{0}\int^{+\infty}_{0}{r^3e^{-r^2}\ dr}=\begin{vmatrix}
u=r^2\\
du=2r\ dr
\end{vmatrix}=
\int^{2\pi }_{0}\int^{+\infty}_{0}{\frac{u}{2}e^{-u}\ dr}=\\\\
=\int^{2\pi }_{0}\frac{1}{2}(-e^{-u}\cdot u-e^{-u})^{\infty}_0=\int^{2\pi }_{0}\frac{1}{2}=\pi
\end{gathered}$$
---
## Termin $II$ i $III$

### 1) Pokaż, że szereg funkcyjny $\sum^{\infty}_{n=1}(x^{2n}-x^{2n+2})$ jest zbieżny punktowo na $[0,1]$

$$\begin{gathered}
\sum^{\infty}_{n=1}(x^{2n}-x^{2n+2})=\sum^{\infty}_{n=1}x^{2n}(1-x^2)=\frac{x^{2}(1-x^{2})}{1-x^{2}}=x^2, |x^2|\lt 1\\
S(x)=x^2, x\in (-1,1)\\\\
S(1)=1(1-1)=0\\\\
\text{ta, zbieżny punktowo}\\\\
\text{funkcja graniczna nieciągła zatem nie może być jednostajnie zbieżny}
\end{gathered}$$
---
### 2) Rozwiń w szereg Maclaurina funkcję $f(x)=\ln{(4+x^2)}$. Dla jakich $x$ suma otrzymanego szeregu jest równa wartości funkcji $f(x)$?

$$\begin{gathered}
f'(x)=\frac{2x}{4+x^2}=\frac{1}{4}\cdot \frac{2x}{1+(\frac{1}{2}x)^2}=
\frac{1}{4}\cdot \frac{2x}{1-(-\frac{1}{4}x^2)}=
\\\\=\sum^{\infty}_{n=0}{(\frac{1}{4})^{n+1}\cdot (-1)^n\cdot x^{2n+1}\cdot 2}, |\frac{x}{2}|\lt 1\implies x\in (-2,2)\\\\
f(x)=\int{\dots}=
\sum^{\infty}_{n=0}{(\frac{1}{4})^{n+1}\cdot (-1)^n\cdot \frac{x^{2n+2}}{2n+2}\cdot 2}+C\\\\
f(0)=\ln{4}\implies C=\ln{4}
\end{gathered}$$

---
### 3) Sprawdź różniczkowalność funkcji w punkcie $(0,0,0)$:

$$\begin{gathered}
f(x,y,z)=\left\{
\begin{matrix}
\frac{y^3}{x^2+y^2+z^2}, \ \ \ (x,y,z)\neq (0,0,0)\\
0, \ \ \ (x,y,z)=(0,0,0)
\end{matrix}
\right.\\\\\\

\lim_{(x,y,z)\to (0,0,0)}f(x,y,z)=\begin{vmatrix}
x=r \sin{\theta}\cos{\varphi}\\
y=r \sin{\theta}\sin{\varphi}\\
z=r \cos{\theta}\\
\theta -dowolne\\
\varphi - dowolne\\
r\to 0
\end{vmatrix}=\\
=\lim_{r\to 0}{\frac{r^3 \dots }{r^2(\dots)}}=0- \text{Ciągła}\\\\

\frac{\partial f}{\partial y}(0,0,0)=\lim_{\Delta y\to 0}{\frac{\frac{\Delta y^3}{\Delta y^2}}{\Delta y}}=1\\

\frac{\partial f}{\partial x}(0,0,0)=0\\

\frac{\partial f}{\partial z}(0,0,0)=0\\\\
\frac{h_y^3}{h_x^2+h_y^2+h_z^2}=h_y+r_{(0,0,0)}(h)\\
r_{(0,0,0)}=\frac{-h_x^2h_y-h_z^2h_y}{h_x^2+h_y^2+h_z^2}\\\\
\lim_{h\to 0}{\frac{\frac{-h_x^2h_y-h_z^2h_y}{h_x^2+h_y^2+h_z^2}}{\sqrt{h_x^2+h_y^2+h_z^2}}}=
\lim_{h\to 0}{\frac{-h_x^2h_y-h_z^2h_y}{(h_x^2+h_y^2+h_z^2)^\frac{3}{2}}}=\\
=\begin{vmatrix}
x=r \sin{\theta}\cos{\varphi}\\
y=r \sin{\theta}\sin{\varphi}\\
z=r \cos{\theta}\\
\theta -dowolne\\
\varphi - dowolne\\
r\to 0
\end{vmatrix}=\lim_{r\to 0}{\frac{-r^3(\sin^3{\theta}\cos^2{\varphi}\sin{\varphi}-\cos^2{\theta \sin{\theta} \sin{\varphi}})}{r^3(\dots)}} \text{ nie istnieje}\\\\
\text{tutaj przez to ile jest tych funkcji trygonometrycznych można }\\
\text{nie dowieść w pełni tego że to faktycznie jest zależne od kątów}\\
\text{plus łatwiej jest po prostu sprawdzić różne tory:}\\\\
\lim_{(h_x,h_y,h_z)\to (0,0,0)}{\frac{-h_x^2h_y-h_z^2h_y}{(h_x^2+h_y^2+h_z^2)^\frac{3}{2}}}\\\\
\text{dla toru gdzie }h_y=0, \text{granica równa zero}\\
\text{a dla toru gdzie }h_z=0, h_x=h_y=\frac{1}{n} \text{granica równa 2}
\end{gathered}$$


---

# 2023/2024

## Termin $I$ i $II$

### 1) Rozwiń w szereg sinusów funkcję $f(x)=x(\pi-x)$ w $(0,\pi)$, narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ i korzystając z otrzymanego rozwinięcia oblicz sumę szeregu $1-\frac{1}{3^3}+\frac{1}{5^3}-\frac{1}{7^3}+\dots$ Czy otrzymany szereg jest jednostajnie zbieżny do $f$ na $(0,\pi)$? Odpowiedź uzasadnij.

$$\begin{gathered}
\text{Warunki Dirichleta:}\\\\
\text{1. przedziałami monotoniczna}\\
\text{2. ograniczona}\\
\text{3. ciągła poza skończoną liczbą punktów nieciągłości}\\
\text{4.}f(a)=f(b)=\frac{\lim_{x\to a^+}f(x)+\lim_{x\to b^-}f(x)}{2}\\\\\

f(-x)=-f(x)\\
f(-x)=-x(\pi-x)\\
f(x)=x(\pi+x)\\\\
f(x)=\left\{
\begin{matrix}
x(\pi-x), x\in (0,\pi]\\
x(\pi+x), x\in [-\pi,0]\\
\end{matrix}
\right.\\\\
b_n=\frac{2}{\pi}\int^{\pi}_{0}{f(x)\sin{nx}\ dx}=
\frac{2}{\pi}\int^{\pi}_{0}{x(\pi-x)\sin{nx} dx}\\=
\frac{2}{\pi}\left(\int^{\pi}_{0}\pi x \sin{nx}-\int^{\pi}_{0}x^2 \sin{nx}\right)=\frac{2}{\pi}\left((1)-(2)\right)\\\\
(1):\\
\int{\pi x\sin{nx} dx}=\begin{vmatrix}
u=x & v'=\sin{nx}\\
u'=1& v=-\frac{\cos{nx}}{n}
\end{vmatrix}=\\
=\pi \left(-\frac{x\cdot \cos{nx}}{n}+\int{\frac{\cos{nx}}{n}}\right)
=\pi \left(-\frac{x\cdot \cos{nx}}{n}+\frac{\sin{nx}}{n^2}
\right)\\
\pi \left(-\frac{x\cdot \cos{nx}}{n}+\frac{\sin{nx}}{n^2}
\right)^{\pi}_0=\frac{\pi^2 (-1)^{n+1}}{n}
\\
(2):\\\\
\int{x^2 \sin{nx} dx}=\begin{vmatrix}
u=x^2&dv=\sin{nx}\\
du=2x&v=-\frac{\cos{nx}}{n}
\end{vmatrix}=\\=
-\frac{x^2 \cos{nx}}{n}+\int{\frac{2x\cos{nx}}{n}}=
-\frac{x^2 \cos{nx}}{n}+\frac{2x \sin{nx}}{n^2}-\int{\frac{2\sin{nx}}{n^2}}=\\
=-\frac{x^2 \cos{nx}}{n}+\frac{2x \sin{nx}}{n^2}+\frac{2\cos{nx}}{n^3}
\\\\
\left(-\frac{x^2 \cos{nx}}{n}+\frac{2x \sin{nx}}{n^2}+\frac{2\cos{nx}}{n^3}\right)^{\pi}_0=\frac{\pi^2 (-1)^{n+1}}{n}+\frac{2(-1)^n}{n^3}-\frac{2}{n^3}\\
f(x)=\sum^{\infty}_{n=1}{\frac{2}{\pi}\left(\frac{2}{n^3}-\frac{2(-1)^n}{n^3}\right)\sin{nx}}, x\in [-\pi,\pi]\\\\
1-\frac{1}{3^3}+\frac{1}{5^3}-\frac{1}{7^3}+\dots=\frac{\pi}{4}\cdot f(\frac{\pi}{2})=\frac{\pi^3}{32}
\end{gathered}$$

---
### 2) Wyznacz esktrema warunkowe funkcji $f(x_1,x_2,\dots,x_n)=x_1^2+x_2^2+\dots+x_n^2$ przy warunku $x_1+x_2+\dots+x_n=n$

$$\begin{gathered}
f(x_1,x_2,\dots,x_n, \lambda)=x_1^2+x_2^2+\dots+x_n^2+\lambda(x_1+x_2+\dots+x_n-n)\\\\
\frac{\partial L}{\partial x_i}=2x_i+\lambda =0\\
x_1+x_2+\dots+x_n=n\\
x_i=-\frac{\lambda}{2}\\
\sum^{\infty}_{n=1}{x_i}=-\frac{n \lambda}{2}=n\implies \lambda=-2\\
x_i=-\frac{-2}{2}=1\\
f(1,1,1,\dots)=n
\end{gathered}$$
---
### 3) Oblicz moment bezwładności jednorodnej bryły $x^2+y^2+z^2\leq 2Ry$ o masie $M$ względem osi $OZ$

---
# 2024/2025

### 3) Oblicz moment bezwładności jednorodonego walca o masie $M$, promieniu podstawy $R$ i wysokości $H$ względem prostej stycznej do powierzchni bocznej tego walca (równoległej do osi symetrii przechodzacej przez środki podstaw).



$$\begin{gathered}
x^2+(y-R)^2=R^2\\\\
\begin{vmatrix}
x=r \cos{\varphi}\\
y=r \sin{\varphi}\\
|J|=r\\
\varphi \in [0,2\pi]
\end{vmatrix}\\\\
r^2-2R r \sin{\varphi}+R^2=R^2\\\\
r=2R \sin{\varphi}\\\\
pH\int^{\pi}_{0} \int^{2R \sin{\varphi}}_{0}r^3 dr=pH\int^{\pi}_{0}\frac{16R^4 \sin^4{\varphi}}{4}=pH 4R^4 \int^{\pi}_{0}\sin^4{\varphi}=\\\\
4pHR^4 \int^{\pi}_{0}{(\frac{1-\cos{2x}}{2})^2}=pHR^4 (\pi-2\\\\
i
\end{gathered}$$