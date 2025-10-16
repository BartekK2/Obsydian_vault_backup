
---
### Definicja granicy ciągu Couchy'ego:

Funkcja ma granice dla x dążącego do nieskończoności jeżeli dla każdego epsilona większego od zera istnieje takie $N_0$ że dla każdego $n\in \mathbb{N}$ większego od tego $N_0$ wartość bezwzględna różnicy wyrazów ciągu $a_n-g$ jest mniejsza od tego epsilona.

$$ \lim_{a_n \to \infty} a_n=g \leftrightarrow \forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N} \ \  \forall n \geq n_0 \ |a_n-g| \lt \epsilon  $$

---
### Kryterium zbieżności Couchy'ego / Alamberta

1. Jeżeli granica ciągu gdzie n dąży do nieskończoności z pierwiastka n-tego stopnia z ciągu $a_n$ jest mniejsza od jeden, to implikuje że granica ciągu $a_n$ gdzie n dąży do nieskończoności jest równa 0.
2. Jeżeli granica gdzie n dąży do nieskończoności wartości bezwzględnej ilorazu kolejnych dwóch wyrazów $a_{n+1},a_n$ jest mniejsza od 1 to oznacza że granica tego ciągu $a_n$ jest równa 0


3. $\lim_{n \to \infty}{\sqrt[n]{|a_n|}}\lt 1 \implies lim_{n \to \infty}{a_n}=0 \ \ \ Couchy$
4. $\lim_{n \to \infty}{|\frac{a_{n+1}}{a_n}|} \lt 1 \implies \lim_{n \to \infty} a_n=0 \ \ \ Alambert$

---
### Twierdzenie o ciągu ograniczonym i zbieżnym do 0

Jeżeli mamy dwa ciągi z czego granica jednego z nich równa 0 a drugi z nich jest ograniczony to implikuje że granica iloczynu tych ciągów równa 0.

---
### Twierdzenie o granicy podciągu

Jeżeli granica ciągu jest równa $g$ to granica każdego z tych podciągów tego ciągu także jest równa $g$.

---
### Twierdzenie o różnych granicach podciągu

Kiedy z ciągu da się wyróżnić dwa podciągi o różnej granicy oznacza to że granica tego ciągu nie istnieje (ciąg nie jest zbieżny).

---
### Twierdzenie Bolzano-Weierstrassa

Jeśli ciąg jest ograniczony to ma podciąg zbieżny do granicy właściwej (czyli do liczby różnej od nieskończoności)

---
### Zasada Indukcji matematycznej

1. Sprawdzamy czy twierdzenie działa dla pewnego $n$
2. Zakładamy że działa 
3. Udowadniamy że działa dla $n+1$

---
### Definicja granicy funkcji Heinego w punkcie

Jeżeli chcemy policzyć granice funkcji w punkcie $x$ to:

Możemy wyszczególnić sobie pewien ciąg $x_n$ dążący do tego punktu $x$i następnie policzyć granice ciągu gdzie n dąży do nieskończoności  z $f(x_n)$.

---
### Twierdzenie o warunku koniecznym wystarczającym na istnienie granicy funkcji w punkcie

Jeżeli granica lewostronna i prawostronna punktu jest sobie równa to ciąg ma granicę w tym punkcie.

---
### Twierdzenie o trzech funkcjach 

Analogicznie jak w przypadku twierdzenia o trzech ciągach. Jeżeli mamy funkcję która jest zawsze większa, i funkcje która jest zawsze mniejsza od funkcji której granicę liczymy. A obie te funkcje większe i mniejsze mają tą samą granicę to ta funkcja której granicę liczymy musi mieć granicę równą granic tamtych funkcji.

---
### Granice specjalne funkcji

$$\begin{gathered}
\lim_{x\to 0}{\frac{\sin{x}}{x}}=1\\
\lim_{x\to \infty}{(1+\frac{1}{x})^x}=e\\
\lim_{x\to 0}{\frac{a^x-1}{x}}=\ln{x}, a>0
\end{gathered}$$
---
### Ciągłość funkcji

Funkcja jest ciągła w punkcie jeżeli granica gdzie x dąży do tego punktu jest równa wartości funkcji w tym punkcie.

---
### Własność Darboux

Jeżeli funkcja jest ciągła w przedziale $[a,b]$ oraz wartość tej funkcji na krańcach tych przedziałów jest różna. To dla dowolnej liczby z zakresu $[f(a),f(b)]$ którą możemy sobie oznaczyć jako $c$ istnieje takie $x_0$ że $f(x_0)=c$ 

---
### Twierdzenie Weierstrassa

Jeżeli funkcja jest ciągła w pewnym przedziale to musi istnieć maksymalna i minimalna wartość w tym przedziale.

---
### Twierdzenie Rolle'a

Jeżeli funkcja w przedziale $[a,b]$ osiąga te same wartości na krańcach to ma gdzieś w tym przedziale punkt gdzie pochodna równa 0. Albo dlatego że jest stała albo dlatego że gdzieś musi "zawrócić", osiągnąć wartość maksymalną lub minimalną.

---
### Definicja pochodnej

Pochodna jest granicą gdzie $x$ dąży do $x_0$ z ilorazu przyrostu funkcji przez przyrost argumentów.

$$
\begin{gathered}
f'(x_0) = \lim_{x \to x_0}{\frac{f(x)-f(x_0)}{x-x_0}}
\\
\begin{gathered}
f'(x_0) = \lim_{h \to 0}{\frac{f(x_0+h)-f(x_0)}{h}}
\end{gathered}
\end{gathered}
$$
---
### Wzory poszczególnych pochodnych



$$
\begin{gathered}
(c)'=0\\
(\frac{1}{x})'=-\frac{1}{x^2}\\
(x^r)' = rx^{r-1}, \ r\in \mathbb{R}\\
W \ szczegolnosci:\\
(\sqrt{x})'=\frac{1}{2\sqrt{x}}\\
(\sin{x})'=\cos{x}\\
(\cos{x})'=-\sin{x}\\
(\tan{x})' = \frac{1}{\cos^2{x}}=1+\tan^2{x}\\
(\cot{x})'=-\frac{1}{\sin^2{x}}=-1-\cot^2{x}\\
(e^x)'=e^x\\
(a^x)'=a^x\cdot \ln{a}\\\\\
Odwrotne:\\
(arcsin \ x)'=\frac{1}{\sqrt{1-x^2}}, \ x\in(-1,1)\\
(arccos \ x)'=-\frac{1}{\sqrt{1-x^2}}, \ x\in(-1,1)\\
(arctg \ x)'=\frac{1}{1+x^2}\\
(arcctg \ x)'=-\frac{1}{1+x^2}\\
(ln \ x)' = \frac{1}{x}\\
(\log_a{x})' = \frac{1}{x\ln{a}}
\end{gathered}
$$
---
### Reguła de L Hospitala

Jeżeli granica ilorazu jest **symbolem nieoznaczonym** tzn. $\frac{\infty}{\infty}$ lub $\frac{0}{0}$ to jest ona równa granicy ilorazu pochodnych.

---
### Twierdzenie Taylora

Taylor twierdził że funkcje można opisać za pomocą kolejnych przybliżeń stycznych.

$$\begin{gathered}
\forall x_0\in D:\\
f(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+\dots + R_n(x_0)
\end{gathered}$$

Możemy wyszczególnić $x_0=0$ i wtedy wzór przyjmuje postać:

$$\begin{gathered}
f(x)=f(0)+\frac{f'(0)}{1!}x+\frac{f''(0)}{2!}x^2+\dots +R_n(0)
\end{gathered}$$

I ten wzór (przybliżenie) nazywamy wzorem Maclaurina.

---
### Funkcje wypukłe i wklęsłe

Funkcja jest wypukła jeżeli jej druga pochodna jest większa od 0, a wklęsła kiedy jej druga pochodna jest mniejsza od 0.

---
### Punkt przegięcia

Punktem przegięcia nazywamy taki punkt w którym druga pochodna zmienia swój znak.

---
### Asymptoty  

$$\begin{gathered}
\lim_{x\to \infty}{\frac{f(x)}{x}}=a\\
\lim_{x\to \infty}{f(x)-ax}=b
\end{gathered}$$
---
### Badanie przebiegu zmienności funkcji
---
**$I$ ANALIZA WZORU FUNKCJI**
1. Dziedzina
2. Punkty przecięcia z osiami ukł. wsp.
3. Własności szczególne (parzystość, nieparzystość, okresowość, ciągłość)
4. Granice na krańcach dziedziny
5. Asymptoty
**$II$ ANALIZA PIERWSZEJ POCHODNEJ FUNKCJI**
6. Obliczamy $f'$, rozwiązujemy równanie $f'(x)=0$ oraz nierówność mniejsze większe od 0.
7. Przedziały monotoniczności
8. Ekstrema lokalne
**$III$ ANALIZA PIERWSZEJ POCHODNEJ FUNKCJI**
9. Obliczamy $f''$, rozwiązujemy równanie $f''(x)=0$ oraz nierówność mniejsze większe od 0.
10. Przedziały wypukłości i wklęsłości.
11. Punkty przegięcia.
**$IV$ ANALIZA +/- FUNKCJA + POCHONE**
Tabelka
**$V$ ANALIZA PIERWSZEJ POCHODNEJ FUNKCJI**
Szkic wykresu funkcji.

---
## Całki

Funkcja jest całkowalna w sensie Newtona jeżeli istnieje taka funkcja której pochodna jest równa tej funkcji.

$$
\begin{gathered}
\int{0 \ dx} = 0+C\\
\int{a \ dx} = ax+C\\
\int{x^r \ dx} = \frac{x^{r+1}}{r+1}+C, \ \ r \neq -1\\
\int{\frac{1}{x} \ dx}=\ln{|x|}+C\\
\int{a^x \ dx}=\frac{a^x}{\ln{a}}+C\\
\int{e^x \ dx} = e^x+C\\
\int{\sin{(x)} \ dx} = -\cos{x}+C\\
\int{\cos{(x)} \ dx} = \sin{x}+C\\
\int{\frac{1}{\cos^2{x}} \ dx} = \tan{x}+C\\
\int{\frac{1}{\sin^2{x}} \ dx} = -\cot{x}+C\\
\int{\frac{1}{1+x^2} \ dx} = \arctan{x}+C\\
\int{\frac{1}{\sqrt{1-x^2}} \ dx} = \arcsin{x}+C\\
\end{gathered}
$$
---
### Całkowanie przez części

$$\begin{gathered}
\int{u\cdot v'}=u\cdot v-\int{u'\cdot v}
\end{gathered}$$

Wynika z wzoru na pochodną iloczynu.

---
### Pole obszaru

Pole pewnego obszaru ograniczonego funkcją.
$$\begin{gathered}
\phi(x)\leq y\leq \omega(x)\\\\
|D|=\int^{b}_{a}{(\omega(x) - \phi(x))\ dx}
\end{gathered}$$

Jeżeli zapiszemy sobie to w współrzędnych biegunowych za pomocą funkcji $r(\phi)$:
$$\begin{gathered}
\forall \phi:
r(\phi)\gt 0\\\\
|D|=\int^{b}_{a}{\frac{1}{2}r^2(\phi)\ d\phi}
\end{gathered}$$
Jeżeli mamy $x,y$ uzależnione od kąta i promienia to:

$$\begin{gathered}
x=\phi(t)\\
y=\omega(t)\\
w(t)\geq 0\\
\phi'(t)\gt 0\\\\
|D|=\int^{b}_{a}{w(t)\cdot \phi'(t)\ dt}
\end{gathered}$$
---
### Długość krzywej:


$$\begin{gathered}
\forall t\in [\alpha,\beta]\ ((x'(t))^2+(y'(t))^2\gt 0\ \\\\
|L|=\int^{b}_{a}{\sqrt{((x'(t))^2+(y'(t))^2}\ dt}
\end{gathered}$$
---
$$\begin{gathered}
y=f(x)\\\\
|L|=\int^{b}_{a}{\sqrt{1+(f'(x))^2}\ dx}
\end{gathered}$$

---
$$\begin{gathered}
|L|=\int^{\beta}_{\alpha}{\sqrt{(r(\phi))^2+(r'(\phi))^2}\ d\phi}
\end{gathered}$$
---
### Objętość bryły obrotowej

$$\begin{gathered}
y=f(x)\\
|V|=\pi \int^{b}_{a}f^2(x)\ dx
\end{gathered}$$
---

$$\begin{gathered}
\forall t\in [\alpha,\beta]\  x'(t)\gt0\\\\
|V|=\pi \int^{\beta}_{\alpha}{y^2(t)\cdot x'(t) \ dt}
\end{gathered}$$

---
### Pole powierzchni bryły obrotowej
$$\begin{gathered}
|S|=2\pi \int^{b}_{a}{f(x)\sqrt{1+(f'(x))^2}\ dx}\\\\
|S|=2\pi \int^{\beta}_{\alpha}{y(t)\sqrt{(x'(t))^2+(y'(t))^2}\ dt}
\end{gathered}$$
