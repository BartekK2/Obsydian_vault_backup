### Pierwiastki liczb zespolonych
#### 2024-10-10

##### Zadania: [[Algebra - liczby zespolone]]
##### Poprzednia: [[Algebra - 2]]
##### Następna: [[Algebra - 4]]

#Liczby_zespolone #wzory_viete #algebra #pierwiastki_zespolone  #wielomiany_zespolone 

--- 
##### Jak obliczyć $\cos{\frac{\pi}{5}}$?
$$\begin{gathered}
\cos{\frac{\pi}{5}}=? \\ \\
\left\{
\begin{align*}
&\cos{\frac{4\pi}{5}}=-\cos{\frac{\pi}{5}} \\
&\cos{\frac{2\pi}{5}}=2\cos^2{\frac{\pi}{5}-1} \\
&-\cos{\frac{\pi}{5}}=\cos{\frac{4\pi}{5}}=2\cos^2{\frac{2\pi}{5}-1}
\end{align*}
\right.
\\
\\

\left\{
\begin{aligned}
&A=\cos{\frac{\pi}{5}} \\
&B=\cos{\frac{2\pi}{5}} \\
\end{aligned}
\right.
&
\left\{
\begin{aligned}
&B=2A^2-1 \\
&-A=2B^2-1 \\
\end{aligned}
\right.
\\ \\
B-(-A)=2A^2-1-2B^2+1=2A^2-2B^2 \\
A+B=2(A-B)(A+B) \\
B=A-\frac{1}{2} \\
2A^2-1=A-\frac{1}{2} \\
2A^2-A-\frac{1}{2}=0 \\
\Delta4+16=20 = 2^2\cdot5 \\
A1=\frac{2+2\sqrt(5)}{8}=\frac{1+\sqrt{5}}{4} \\
A2=\frac{2-2\sqrt(5)}{8}=\frac{1-\sqrt{5}}{4}, \ sprzeczne
\end{gathered}$$

---
#### Pierwiastek stopnia n liczby zespolonej:
###### a) gdy liczba ma dostępną postać trygonometryczną
[[Algebra - 2#Pierwiastkowanie liczb zespolonych|Sposób]]
###### b) gdy nie ma to rozwiązujemy z definicji:
$$
\begin{gathered}
\sqrt{3-4i}=x+i\cdot y \leftrightarrow  (x+i\cdot y)^2=3-4i \\ 
\left\{
\begin{matrix}
x^2-y^2=3,\ rzeczywiste\\
2xy=-4, \ imaginaries\\
x^2+y^2=5, \ wynika \ z \ |z| \\

\end{matrix}
\right. \\ \\

x^2+x^2+y^2-y^2=5+3 \\
2x^2=8 \\
y=\frac{-2}{x}, x \neq 0 \\
\left\{
\begin{matrix}
x=2 \\
y=-1 \\
\end{matrix}
\right. \ \ \
\left\{
\begin{matrix}
x=-2 \\
y=1 \\
\end{matrix}
\right.
\end{gathered}
$$
---
#### Uogólnione wzory Viete'a
$$\begin{gathered}
Dla \ wielomianu:\\\\
W(z)=a_nz^n+a_{n-1}z^{n-1}+...+a_1z+a_0, \ \ a_n \neq 0\\ \\
1. \ \ z_1+z_2+z_3+...+z_n=\frac{-a_{n-1}}{a_n} \\ 
Czyli \ analogicznie \ do \ wzorow \ Viete'a \ z \ funkcji \ kwadratowej:\\
x_1+x_2=\frac{-b}{a}\\ \\
2. \ \ (z_1z_2)+(z_1z_3)+...+(z_1z_n)+...+(z_{n-1}z{n})=\frac{a_{n-2}}{a_n} \\
Czyli \ analogicznie \ do \ wzorow \ Viete'a \ z \ funkcji \ kwadratowej: \\
x_1x_2 = \frac{c}{a} \\\\

3. \ \ z_1\cdot z_2 \cdot z_3 \cdot ... \cdot z_n = (-1)^n \frac{a_0}{a_n}
\end{gathered}$$
---
#### Rozpisany wzór na $\cos{n\varphi}$ 
$$\begin{gathered}
Kroki \ na \ dowod: \\
1. \ \left\{
\begin{matrix}
(\cos{\varphi}+i\cdot \sin{\varphi})^n=\cos{n\varphi}+i\cdot \sin{n\varphi} \\
(x+y)^n = \sum_{i=0}^{n} {n \choose i}x^n y^i 
\end{matrix}
\right. \\ \\
(\cos{\varphi}+i\cdot \sin{\varphi})^n = {n \choose 0} cos^n{\varphi}sin^0{\varphi}+...+\\\\
\downarrow bo \ sie \ redukuje \ przez \ i \\\\
\cos{n\varphi} = \sum_{i=0}^{\lfloor{n/2}\rfloor} {n \choose 2i } (-1)^i \cdot \cos^{n-2i}{\varphi}\sin^{2i} {\varphi} \\ 

\end{gathered}$$
---
#### :LiHome: Zadania
##### Podaj ile to $\cos{5\varphi}$
---
###### Liczone ze wzoru:
$$\begin{gathered} \\
cos{5\varphi}=?\\\\
cos{5\varphi} =  1cos^5-10cos^3(1-cos^2) +5cos^1(1-cos^2)^2=\\
=1cos^5-10cos^3+10cos^5+5cos^1(1-2cos^2+cos^4)=\\
=5cos-10cos^3+5cos^5+10cos^5+1cos^5-10cos^3=16cos^5-20cos^3+5cos^1 \\ 
\end{gathered}$$
###### Z trójkąta Pascala:
![[Screenshot_20241012_013146_Obsidian.jpg]]
#### Wielomiany:

*Tw. Bezout'a*:
Liczba $z_0 \in \mathbb{C}$ jest pierwiastkiem wielomianu W wtedy i tylko wtedy, gdy istnieje wielomian P (stopnia o 1 mniejszego od W) taki, że:
$W(z)=(z-z_0)P(z)$

*Tw. (o pierwiastkach wymiernych wielomianu)*:
Niech:
$W(x)=a_nx^n+a_{n-1}x^{n-1}+...+a_1x+a_0$
będzie wielomianem stopnia n o współczynnikach **CAŁKOWITYCH**, oraz niech licza wymierna $\frac{p}{q}$, gdzie p, q są względnie pierwszymi (w sensie sie nie skracają) liczbami całkowitymi, będzie pierwiastkiem wielomianu W. Wówczas p jest dzielnikiem współczynnika $a_0$ a q jest dzielnikiem współczynnika $a_n$.

*Tw. (zasadnicze twierdzenie algebry)*:
Każdy wielomian zespolony stopnia $n \geq 1$ ma co najmniej jeden pierwiastek zespolony.

*Tw. (o przedstawieniu wielomianu w postaci iloczynu dwumianów)*:
Każdy wielomian zespolony:
$W(z)=a_nz^n+a_{n-1}z^{n-1}+...+a_1z+a_0$
stopnia $n \in \mathbb{N}$ ma DOKŁADNIE  n pierwiastków zespolonych (uwzględniając krotności). Zatem każdy wielomian zespolony można przedstawić w postaci iloczynu dwumianów i nierozkładalnych trójmianów:
$W(z)=a_n(z-z_1)^{k_1}(z-z_2)^{k_2)}...(z-z_m)^{k_m}$ 

*Tw. (o pierwiastkach zespolonych wielomainu rzeczywistego)*:
Jeżeli $z_0$ jest k krotnym pierwiastkiem wielomianu $W(z)$ to $\overline{z}$ również jest k krotnym pierwiastkiem tego wielomianu.

