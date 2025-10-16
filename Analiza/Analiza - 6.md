---
share_link: https://share.note.sx/rvvj4p4w#gBMINz1GBY0b+/RnP3X+WwxJInYxV+2IlHYb9V5qY5g
share_updated: 2024-11-27T10:25:34+01:00
---
### Funkcje wypukłe/wklęsłe, Asymptoty, Badanie przebiegu zmienności funkcji 
#### 2024-11-24
##### Poprzednia: [[Analiza - 5]]
##### Następna: [[Analiza - 7]]
##### Zadania: [[]]

#asymptoty #badanie_przebiegu_zmiennosci #wklesle #wypukle #analiza  

--- 
### Funkcje wypukłe i wklęsłe 

*Definicja:*
$I$ - przedział $\subset \mathbb{R}, I \subset D_f$
Funkcję $f$ nazywamy wypukłą w $I \Leftrightarrow$ gdy nadwykres funkcji $f$ czyli zbiór $\{(x,y): x \in I, y \geq f(x)\}$ jest zbiorem wypukłym.

![[diagram-20241124 (6).png]]
Funkcję $f$ nazywamy wklęsła w $I \Leftrightarrow$ gdy nadwykres funkcji $-f$ czyli zbiór $\{(x,y): x \in I, y \leq f(x)\}$ jest zbiorem wypukłym. Czyli $\{(x,y): x \in I, y \geq f(x) \}$ zbiór wklęsły.

![[diagram-20241124 (7).png]]

---
*Definicja:*

Jeśli $f$ jest różniczkowalna w $I=(a,b)$

$f$ jest ściśle wypukła w $I \Leftrightarrow \forall x_0 \in I \ \forall x \in I, x \neq x_0 \ \ f(x)\gt f(x_0)+f'(x_0)(x-x_0)$

$f$ jest ściśle wklęsła w $I \Leftrightarrow \forall x_0 \in I \ \forall x \in I, x \neq x_0 \ \ f(x)\lt f(x_0)+f'(x_0)(x-x_0)$

Czyli wykres funkcji leży ponad/pod wykresem *stycznej* dla każdego punktu $x_0$ z przedziału $(a,b)$.

---
#### Warunek wystarczający wypukłości i wklęsłości funkcji.

*Założenia:* $f \in C^2(I)$ (funkcja jest przynajmniej 2 krotnie różniczkowalna a jej pochodne przynajmniej do 2 stopnia są ciągłe).

*Teza:*
1. Jeśli $\forall x \in I  \ \ f''(x)\gt 0$, to $f$ jest wypukła w $I$.
2. Jeśli $\forall x \in I \ \ f''(x) \lt 0$, to $f$ jest wklęsła w $I$.

**Przykład:**
Sprawdź czy funkcja $f(x)=5x^4-3x+2$ jest wklęsła w $x_0=4$
$f'(x)=20x^3-3$
$f''(x)=60x^2$
$f''(4)=960$ zatem funkcja jest wypukła w punkcie $x_0=4$

**Ważne:**
Jeśli funkcja nie ma pochodnej drugiego stopnia w jakimś punkcie np w mianowniku będzie 0 to trzeba liczyć granice i sprawdzić czy się zmieni znak, to tylko warunek wystarczający.

---
### Punkt przegięcia

**Definicja:**
Założenia:
$f$ jest określona w pewnym otoczeniu $U$ punktu $x_0$
$f$ jest ciągła w $x_0$

Mówimy, że punkt $(x_0, f(x_0))$ jest punktem przegięcia funkcji $f \Leftrightarrow$ w jednym sąsiedztwie jednostronnym punktu $x_0$ funkcja $f$ jest wypukła, a w drugim wklęsła.

**Przykład:** $f(x)=x^3$
$$\begin{gathered}
f(x)=x^3\\
f'(x)=3x^2\\
f''(x)=6x\\
x=0, (0,0)\ punkt \ przegiecia \ bo:\\
f''(x) \gt 0 \ \Leftrightarrow x\gt 0\\
f''(x) \lt 0 \ \Leftrightarrow x\lt 0\\
\end{gathered}$$
---
#### Warunek konieczny istnienia punktu przegięcia jeśli pochodna 2 st. ciągła:

*Założenia:*
1. $U$ - otoczenie punktu $x_0$
2. $f \in C^2(U)$
3. punkt $(x_0, f(x_0))$ jest punktem przegięcia funkcji $f$

*Teza:* $f''(x_0)=0$

Czyli jeśli funkcja jest różniczkowalna do minimum drugiego stopnia oraz jej pochodna 2 stopnia jest ciągła to w tym punkcie musi być równa 0.

---
#### Warunek wystarczający istnienia punktu przegięcia.

*Założenia:*
1. $f$ jest określona w pewnym otoczeniu $U$ punktu $x_0$.
2. $f$ jest klasy $C^2$ na pewnym sąsiedztwiie $S$ punktu $x_0$
3. $f$ jest ciągła w $x_0$
4. $\exists S^- (x_0, \delta) \forall x \in S^- (x_0,\delta) f''(x) \stackrel{\lt}{\gt} 0$ oraz $\exists S^+ (x_0, \delta) \forall x \in S^+ (x_0,\delta) f''(x) \stackbin{\gt}{\lt}0$ (Czyli odległość punktów ($\delta$) taka sama musi być żeby sprawdzić)

*Teza:* $f$ ma w punkcie $x_0$ punkt przegięcia

**Przykład:** 
$$\begin{gathered}
f(x)=e^{-x^2}\\
f'(x)=\frac{1}{e^{x^2}}\cdot -2x=-\frac{2x}{e^{x^2}}\\
f''(x)=-\frac{2\cdot e^{x^2}-2x\cdot e^{x^2}\cdot 2x}{(e^{x^2})^2}=-\frac{-4x^2+2}{e^{x^2}}=\frac{4x^2-2}{e^{x^2}}\\\\

4x^2-2\lt 0\\
4x^2\lt 2\\
x^2\lt \frac{1}{2}\\
x\lt \frac{\sqrt{2}}{2} \ \vee \ x\gt -\frac{\sqrt{2}}{2}\\\\
e^{x^2} \gt 0 \Leftrightarrow x^2\in \mathbb{R}\\\\
Wiec \ f''(x) \gt 0 \Leftrightarrow x \in (-\frac{\sqrt{2}}{2},\frac{\sqrt{2}}{2})\\\\
Zatem \ funkcja \ ma \ dwa \ punkty \ przegiecia \ dla \ x=\pm \frac{\sqrt{2}}{2} 
\end{gathered}$$

**Zatem to że pochodna drugiego stopnia się zeruje to nie wystarcza, musimy jeszcze sprawdzić czy faktycznie zmienia znak w tym punkcie!!!**

---
### Asymptoty 

##### Pionowa:

*Definicja:* 
Mówimy, że prosta $x=x_0$ jest *asymptotą pionową lewostronną* funkcji $f$ wtedy i tylko wtedy gdy:
1. $f$ jest określona w pewnym lewostronnym sąsiedztwie punktu $x_0$
2. $\lim_{x \to x_0^-}{f(x)}=\pm \infty$
Analogicznie *prawostronną*.

Jeśli prosta $x=x_0$ jest asymptotą pionową lewostronną i prawostronną to nazywamy ją asymptotą pionową *obustronną*.

**Przykład:** 
Wyznacz asymptoty pionowe funkcji $f(x)=e^{\frac{1}{x}}$
$\lim_{x \to 0}{e^{\frac{1}{x}}}=e^{\lim_{x \to 0}\frac{1}{x}}=e^\infty = \infty$

*Spostrzeżenie:* Jeśli $f$ ciągła w $x_0$ to oczywiście $x=x_0$ nie jest asymptotą.

---
##### Ukośne

*Definicja:*
Prostą $y=ax+b$ nazywamy *asymptotą ukośną* funkcji $f$ w $+\infty$
1. $f$ jest określona w otoczeniu $+\infty$
2. $\lim_{x \to \infty }{f(x)-(ax+b)}=0$
$a=\lim_{x\to \infty}{\frac{f(x)}{x}}$ i $b=\lim_{x\to \infty}{f(x)-ax}$
Analogicznie asymptota ukośna w $-\infty$. 
Jeśli $a=0$ to asymptotę nazywamy *Poziomą*

##### Pozioma (wynika z ukośnej)

$\lim_{x\to \infty}{f(x)-(0x+b)}=0$
$\lim_{x\to \infty}{f(x)-b}=0$
$\lim_{x\to \infty}{f(x)}=b$

**Przykład:**

$$\begin{gathered}
f(x)=\frac{\sin{x}}{x}\\
\lim_{x\to \infty}{\frac{\sin{x}}{x^2}}=0\\
\lim_{x\to \infty}{f(x)}=0\\
y=0
\end{gathered}$$

**Przykład 2:**
Wyznacz wszystkie asymptoty funkcji $f(x)=x\ln{(1+\frac{1}{x})}$


$$\begin{gathered}
\mathbb{D}:\\
1+\frac{1}{x}\gt 0\\
\frac{1}{x}\gt -1\\
x\gt -x^2\\
x^2-x\gt 0\\
x(x-1)\gt 0\\
x \in (-\infty, 0) \cup (1, +\infty)
\\\\

f(x)=x\ln{(1+\frac{1}{x})}=\frac{\ln{(1+\frac{1}{x})}}{\frac{1}{x}}\\

\lim_{x\to 0}{\frac{(\frac{1}{1+\frac{1}{x}})\cdot -\frac{1}{x^2}}{-\frac{1}{x^2}}=\lim_{x\to 0}\frac{1}{1+\frac{1}{x}}=0}\\
1+\frac{1}{x}=0 \Leftrightarrow x=-1\\
\lim_{x\to -1}{\frac{1}{1+\frac{1}{x}}}=+\infty
\end{gathered}$$


Pionowej w 0 nie będzie ale będzie dla $ln(x)$ gdzie x dąży do 0 czyli dla $x=-1$


$$\begin{gathered}
f(x)=x\ln{(1+\frac{1}{x})}\\

\lim_{x\to \infty}{\frac{f(x)}{x}}=\lim_{x\to \infty }{\ln{(1+\frac{1}{x})}}=0\\
a=0\\
\lim_{x\to \infty}{f(x)-ax}=\lim_{x\to \infty}{f(x)-0x}=\lim_{x\to \infty}{f(x)}=\lim_{x\to \infty}\frac{1}{1+\frac{1}{x}}=1\\
y=1
\end{gathered}$$
Zatem mamy poziomą.

---
### Funkcje parzyste, nieparzyste, okresowe (trywialne, warto tylko sprawdzić warunek dziedziny)

*Definicja:* 
$f: D\to \mathbb{R}, D \subseteq \mathbb{R}$
Funkcję $f$ nazywamy *parzystą* $\Leftrightarrow$
1. $\forall x \in D -x \in D$ ($D$ - zbiór symetryczny względem 0)
2. $\forall x \in D \ \ f(-x)=f(x)$

*Definicja:* 
$f: D\to \mathbb{R}, D \subseteq \mathbb{R}$
Funkcję $f$ nazywamy *nieparzystą* $\Leftrightarrow$
3. $\forall x \in D -x \in D$ ($D$ - zbiór symetryczny względem 0)
4. $\forall x \in D \ \ f(-x)=-f(x)$

**Spostrzeżenie** Wykres funkcji parzystej jest symetryczny względem osi $OY$, a wykres funkcji nieparzystej jest symetryczny względem punktu $(0, 0)$.

*Definicja:* 
$f: D\to \mathbb{R}, D \subseteq \mathbb{R}$
Funkcję $f$ nazywamy *okresową* $\Leftrightarrow$ gdy istnieje takie $T \gt 0$ że:
5. $\forall x \in D x+T \in D$ ($D$ - zbiór symetryczny względem 0)
6. $\forall x \in D \ \ f(x+T)=f(x)$
Liczbę $T$ nazywa się wówczas *okresem* funkcji $f$.

### Badanie przebiegu zmienności funkcji
---
**$I$ ANALIZA WZORU FUNKCJI**
7. Dziedzina
8. Punkty przecięcia z osiami ukł. wsp.
9. Własności szczególne (parzystość, nieparzystość, okresowość, ciągłość)
10. Granice na krańcach dziedziny
11. Asymptoty
**$II$ ANALIZA PIERWSZEJ POCHODNEJ FUNKCJI**
12. Obliczamy $f'$, rozwiązujemy równanie $f'(x)=0$ oraz nierówność mniejsze większe od 0.
13. Przedziały monotoniczności
14. Ekstrema lokalne
**$III$ ANALIZA PIERWSZEJ POCHODNEJ FUNKCJI**
15. Obliczamy $f''$, rozwiązujemy równanie $f''(x)=0$ oraz nierówność mniejsze większe od 0.
16. Przedziały wypukłości i wklęsłości.
17. Punkty przegięcia.
**$IV$ ANALIZA +/- FUNKCJA + POCHONE**
Tabelka
**$V$ ANALIZA PIERWSZEJ POCHODNEJ FUNKCJI**
Szkic wykresu funkcji.

---
**Przykład:**
Zbadaj przebieg zmienności funkcji $f(x)=\frac{x}{\ln{x}}$
18. Dzedzina $\mathbb{D} = (0,+\infty) \setminus \{1\}$
19. Nima
20. Parzystość/nieparzystość/okresowość - nie. Ciągłość:
   $$\begin{gathered}
\lim_{x\to 1^-}{\frac{x}{\ln{x}}}=-\infty\\
\lim_{x\to 1^+}{\frac{x}{\ln{x}}}=+\infty\\
Nie \ ciagla.
\end{gathered}$$
21. $\lim_{x\to 0}{f(x)}=0 \ \ \lim_{x\to \infty}{f(x)}=\infty$
22. Asymptoty:
   $$\begin{gathered}
\lim_{x\to 1}{f(x)}=\pm \infty\\
x=1\\
\lim_{x\to \infty}{\frac{f(x)}{x}}=\lim_{x\to \infty}\frac{1}{\ln{x}}=0\\
\lim_{x\to \infty}{f(x)-ax}=\lim_{x\to \infty}{\frac{x}{\ln{x}}}=\lim_{x\to \infty}{\frac{1}{\frac{1}{x}}}=+\infty\\
Brak \ poziomej
\end{gathered}$$
23. 
   $$\begin{gathered}
f'(x)=\frac{\ln{x}-1}{(\ln{x})^2}=0 \Leftrightarrow x=e\\
f'(x) \lt 0 \Leftrightarrow x\lt e\\
f'(x) \gt 0 \Leftrightarrow x\gt e
\end{gathered}$$
24. $f \ rosnie  \ (0, e) \ maleje <e, +\infty)$ 
25. $f'(x)=0 \Leftrightarrow x=e \vee x=1, sprzeczne$
26. $f''(x)=\frac{\frac{1}{x} \cdot (\ln{x})^2 - (\ln{x}-1)\cdot \frac{2\ln{x}}{x}}{(\ln{x})^4}=\frac{-(\ln{x})^2 + 2\ln{x}}{x\cdot( \ln{x})^4}$
27. 