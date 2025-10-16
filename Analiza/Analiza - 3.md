### Granica funkcji
#### 2024-10-14
##### Poprzednia: [[Analiza - 2]]
##### Następna: [[Analiza - 4]]
##### Zadania: [[Analiza zadania - indukcja, złożenie, granice ciągu i funkcji, ciągłość]]

#granica_funkcji  #analiza  

--- 
### Granica funkcji:

#### Otoczenie i sąsiedztwo punktu:

*Otoczeniem* punktu $x_0 \in \mathbb{R}$ o promieniu $r\gt 0$ nazywamy przedział $(x_0-r, x_0+r)$ i oznaczamy przez $U(x_0,r)$.
*Sąsiedztwem* punktu $x_0 \in \mathbb{R}$ o promieniu $r \gt 0$ nazywamy $(x_0-r, x_0) \cup (x_0, x_0+r)$ i oznaczamy przez $S(x_0, r)$.

Czyli otoczenie od sąsiedztwa różni sie wyłącznie tym czy włączamy $x_0$, w otoczeniu tak, w sąsiedztwie nie.

Sąsiedztwo możemy podzielić na dwie kategorie:
- *Prawostronne* $S^+ (x_0, r) = (x_0, x_0+r)$
- *Lewostronne* $S^- (x_0, r) = (x_0-r,x_0)$

Zbiór wszystkich otoczeń punktu $x_0$ oznaczamy przez $ot(x_0)$.

---
#### Definicja granicy funkcji Heinego:

Jeżeli mamy funkcję której dziedzina zawiera się w $\mathbb{R}$ a jej wartości także leżą w zbiorze liczb rzeczywistych.

A także pewien punkt $x_0 \in \mathbb{R} \cup \{-\infty, \infty\}$ i $f$ jest określona w pewnym sąsiedztwie tego punktu.

To $\lim_{x \to x_0}{f(x)} = g \Leftrightarrow \forall (x_n)_{n \in \mathbb{N}}$ spełniającego:
1. $\forall n \in \mathbb{N} \ x_n \in D_f$
2. $\forall n \in \mathbb{N} \ x_n \neq x_0$
3. $\lim_{n \to \infty} x_n = x_0$
zachodzi $\lim_{n\to \infty}{f(x_n)} = g$

Innymi słowy jeżeli ciąg $x_n$ dąży do $x_0$ (ma granicę $x_0$) i granica $\lim_{n\to \infty}{f(x_n)}$ jest równa $g$ to granica $\lim_{x \to x_0}{f(x)} = g$.

###### Przykład oblicz $\lim_{x\to 1}{\frac{x^2-1}{x-1}}$:

$$\begin{gathered}
\lim_{x \to 1}{\frac{x^2-1}{x-1}}\\\\
\frac{x^2-1}{x-1}=\frac{(x-1)(x+1)}{(x-1)}=x+1\\
\lim_{x\to 1}{x+1} = 2
\end{gathered}$$
---
#### Definicja granic jednostronnych:
Funkcja $f$ ma granicę w punkcie $x_0$ lewostronną wtedy kiedy jest określona w pewnym lewostronnym sąsiedztwie punktu $x_0$. ^402f1e

$\lim_{x \to x_0^-}{f(x)} = g \Leftrightarrow \forall (x_n)_{n \in \mathbb{N}}$ spełniającego:
1. $\forall n \in \mathbb{N} \ x_n \in D_f$
2. $\forall n \in \mathbb{N} \ x_n \lt x_0$
3. $\lim_{n \to \infty} x_n = x_0$
zachodzi $\lim_{n\to \infty}{f(x_n)} = g$

Czyli po prostu $x_n$ dąży do $x_0$ ale nigdy go nie osiągnie + zawsze będzie mniejsze (więc dążymy od strony lewej).

Analogicznie definiujemy granicę prawostronną funkcji $\lim_{x\to x_0^+}{f(x)}$.

---
#### Twierdzenie o warunku koniecznym wystarczającym na istnienie granicy:

^5106ce

Mówimy że $f$ ma granicę w punkcie $x_0$ wtedy kiedy granica lewostronna i prawostronna w punkcie $x_0$ jest taka sama.

$\lim_{x\to x_0}{f(x)} = g \Leftrightarrow \lim_{x\to x_0^-}{f(x)}=\lim_{x\to x_0^+}{f(x)}=g$

###### Przykład funkcji która nie ma granicy w punkcie $x_0=0$.
$$\begin{gathered}
f(x)=sgn(x)=\left\{
\begin{align*}
-1, x\lt 0\\
0, x=0\\
1, x\gt 0
\end{align*}\right.\\\\
\lim_{x\to 0}{f(x)} \ nie \ istnieje \ bo:\\
\lim_{x\to 0^-}{f(x)}=-1\\
\lim_{x\to 0^+}{f(x)}=1\\\\
Wiec \ granica \ lewostronna \ i \ prawostronna \ jest \ rozna \\ co \ implikuje \ ze \ funkcja \ nie \ ma \ granicy.
\end{gathered}$$
---
#### Twierdzenie o arytmetyce granic funkcji

Praktycznie to samo co w [[Analiza - 2#^6a1c39| ciągach]].
Czyli suma granic to granica sumy, to samo z iloczynem/ilorazem.

---
#### Twierdzenie o trzech funkcjach:

To samo co w [[Analiza - 2#^89a611| ciągach]].
Jak znajdziemy dwie funkcje, jedną większą od naszej i drugą mniejszą, i te 2 funkcje mają tą samą granice to "nasza" (środkowa) również ma tą samą granice.

###### Przykład $\lim_{x\to \infty}{\frac{\sin{x}}{x}}$:

$-1\leq \sin{x} \leq 1$
$\frac{-1}{x} \leq \frac{\sin{x}}{x} \leq \frac{1}{x}$

Gdzie $\lim_{x\to \infty}{\frac{-1}{x}}=\lim_{x\to \infty}{\frac{1}{x}}=0$
Więc $\lim_{n \to \infty}{\frac{\sin{x}}{x}} = 0$

---
#### Twierdzenie analogiczne do tego z ciągów że granica $f(x) \cdot g(x)$ = 0 wtedy kiedy granica np. $g(x)=0$

---
#### Granice specjalne (warte do zapamiętania):

$$\begin{gathered}
\lim_{x\to 0}{\frac{\sin{x}}{x}} = 1\\
\lim_{x\to \infty}{(1+\frac{1}{x})^x} = e\\
\lim_{x\to 0}{\frac{a^x-1}{x}} = \ln{x}, \ a \gt 0 \\
\end{gathered}$$

###### Przykład $\lim_{x\to 0}{\frac{\arcsin{x}}{x}}$
To chyba trzeba zrobić tak że dla $x\to 0$ $\lim{\sin{x}}=\lim{\arcsin{x}}$ więc jest równe $\lim{\frac{\sin{x}}{x}}=1$?

---
#### Twierdzenie o granicy funkcji złożonej $g(f(x))$:
Założenia: 
$\lim_{x\to x_0}{f(x)} = y_0$
$\forall x \in S(x_0,r) f(x) \neq y_0$
$\lim_{y \to y_0}{g(y)} = z_0$

Teza:
$\lim_{x\to x_0}{g(f(x))} = z_0$

---
### Ciągłość funkcji:

*Def.* 
Z: $f$ jest określona w otoczeniu punktu $x_0 \in Df$

$f$ jest ciągła w $x_0 \Leftrightarrow \lim_{x\to x_0}{f(x)}=f(x_0)$

###### Przykład czy $f(x) = sng(x)$ jest ciągła w 0?
Nie bo granica $x\to x_0$ nie istnieje więc nie jest równa $f(0)$.

###### Przykład 2: Dla jakiej wartości parametru $a$ funkcja $f(x)$  jest ciągła w 0?
$$\begin{gathered}
f(x) = \left\{\begin{align*}\frac{
\sin{5x}}{x}, x \neq 0\\
a, x=0\end{align*}\right.\\\\
\sin{5x} = \sin{x}, x=0\\
\lim_{x\to 0}{\frac{\sin{5x}}{x} = 1}\\
Z \ def. \ ciaglosci \ funkcji: \ \lim_{x \to 0}{f(x)}=f(0)=a=1
\end{gathered}$$

---
#### Twierdzenie o działaniach na funkcjach ciągłych:
1. Oczywiście suma, różnica iloczyn funkcji w punkcie $x_0$ jest funkcją ciągłą w $x_0$.
2. Iloraz jest ciągły kiedy w pewnym otoczeniu mianownika jest różny od 0.
3. Jeśli 2 funkcje są ciągłe to ich złożenie też będzie ciągłe (w $x_0$)
---
*Funkcja jest ciągła na zbiorze $A \subset Df$ wtedy kiedy jest ciągła w każdym z punktów $A$* 
*Ozn.* 
$C(A)$ - zbiór wszystkich funkcji ciągłych na zbiorze $A$ 
$f \in C(A) \Leftrightarrow f$ jest ciągłe na zbiorze $A$ 

*Wszystkie funkcje elementarne są ciągłe na swoich dziedzinach.*

---
### Własności funkcji ciągłych:

#### Własność Darboux:
$$\begin{gathered}
f \in C([a,b]) \ \land \ f(a) \neq f(b)\\
c \ - \ dowolna \ liczba \ pomiedzy \ f(a) \ i \ f(b)\\
Teza: \ istnieje \ takie \ x_0 \in (a,b) \ ze \ f(x_0) = c
\end{gathered}$$

Skoro funkcja jest ciągła w pewnym zbiorze to musi kiedyś zahaczyć o jakąś liczbę.

---
#### Twierdzenie Weierstrassa o osiąganiu kresów:

^643abd

Jeżeli funkcja $f$ jest ciągła na przedziale domkniętym $[a,b]$, to istnieje
1. $x_1 \in [a,b], f(x_1) = inf\{f(x): x\in [a,b]\}$ - wartość najmniejsza funkcji $f$ na $[a,b]$
2.  $x_1 \in [a,b], f(x_1) = sup\{f(x): x\in [a,b]\}$ - wartość największa funkcji $f$ na $[a,b]$

Innymi słowy kiedy funkcja jest ciągła w domkniętym zbiorze to ma wartość największą i najmniejszą w tym zbiorze.

Nie wiem co to za twierdzenie z dupy XD. 

---
