### Szeregi funkcyjne
#### 2025-05-01
##### Poprzednia: [[Analiza 2 Ciągi funkcyjne]]
##### Następna: [[Analiza 4 Szeregi potęgowe]]
##### Zadania: [[Zadania Szeregi]]

#szeregi_funkcyjne #analiza2  

---
**Definicja** Szeregiem funkcyjnym nazywamy parę ciągów $((f_n(x), (S_n(x))), x\in X$
Ozn. $\sum^{\infty}_{n=1}{f_n(x)}$

**Przykład:**
$f_n(x)=x^n, \ x\in [0,1)$

**Definicja** Szereg funkcyjny $((f_n(x))), (S_n(x)))$ jest **punktowo zbieżny** na $X$ 
istnieje taka funkcja $S: X\to Y$, że $S_n\overset{X}{\to}S$

**Definicja** Szereg funkcyjny $((f_n(x))), (S_n(x)))$ jest **jednostajnie zbieżny** na $X$ 
istnieje taka funkcja $S: X\to Y$, że $S_n\overset{\to}{\to}S$


Czyli lepiej wg definicji, to samo co z ciągami zbieżnymi:

$S: X\to Y \Leftrightarrow \forall \epsilon \gt 0 \forall x \in X \ \ \exists n_0 \in \mathbb{N} \ \ \forall n \gt n_0 \ \ |S_n(x)-S(x)|\lt \epsilon$
$S: X\overset{\to}{\to} Y \Leftrightarrow \forall \epsilon \gt 0\ \ \exists n_0 \in \mathbb{N} \ \ \forall n \gt n_0 \ \ \forall x \in X \ \ |S_n(x)-S(x)|\lt \epsilon$

No i oczywiście jeżeli jest jednostajnie zbieżny to też jest punktowo zbieżny.

**WK punktowej zbieżności szeregu funkcyjnego**
zał: $\sum^{\infty}_{n=1}{f_n(x)}$ jest punktowo zbieżny na $X$

teza: $\forall x\in X \ \ \lim_{n\to \infty}{f_n(x)=0}$ czyli $f_n\to 0$

**WK jednostajnej zbieżności szeregu funkcyjnego**
zał: $\sum^{\infty}_{n=1}{f_n(x)}$ jest jednostajnie zbieżny na $X$

teza: $f_n\overset{\to}{\to} 0$

---
**Przykład:**
Czy $\sum^{\infty}_{n=1}{x^n}$ jest jednostajnie zbieży na $[0,1)$

$$\begin{gathered}
\forall \epsilon \gt 0 \exists n_0 \in \mathbb{N} \ \forall n \gt n_0 \forall x \in X: \ \ |S_n(x)-S(x)|\lt \epsilon\\\\
S(x)=\lim_{n\to \infty}{x^n}=\frac{x}{1-x}\\
|S(x)-S_n(x)|\lt \epsilon\\
|\frac{x}{1-x}-\sum^{n}_{k=1}{x^k}|\lt \epsilon\\
|\frac{x^{n+1}}{1-x}|\lt \epsilon\\
\text{epsilon jest nie tylko zależny od n  ale także od x więc nie dla każdego epsilona}\\
\text{większego od zera istnieje n od którego każdy x spełnia}
\end{gathered}$$

---
**Twierdzenie Weierstrassa**

zał: $f_n: X\to \mathbb{R}, X\subset \mathbb{R}$
$\forall n \in \mathbb{N} \ \ \forall x \in X \ \ |f_n(x)|\leq a_n$
$\sum^{}_{}{a_n}$ - zbieżny
teza: $\sum^{}_{}{f_n(x)}$ jest jednostajnie zbieżny na zbiorze $X$ 

---
**Czemu to nie działa z poprzednim przykładem?**

Bo dla $x=1^-$ można powiedzieć że $a_n=1$

---
Czy ten szereg jest jednostajnie zbieżny na $[0,1]$?

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{x^n(1-x)}{n}}
\end{gathered}$$

