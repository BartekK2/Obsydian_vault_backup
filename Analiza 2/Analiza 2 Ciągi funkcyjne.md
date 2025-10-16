### Ciągi funkcyjne
#### 2025-03-25
##### Poprzednia: [[Analiza 1 Szeregi liczbowe]]
##### Następna: [[]]
##### Zadania: [[]]

#ciągi_funkcyjne #analiza2  

---
$Y=\mathbb{R}, \ \ X\subset \mathbb{R}$

**Def.** Ciągiem funkcyjnym nazywamy $(f_n(x))_{n\in \mathbb{N}}$, gdzie $\forall n \in \mathbb{N} \ f_n: X\to Y$.
**Przykład**:
$$\begin{gathered}
x^1,x^2,x^3,x^4\dots 
\end{gathered}$$

**Def zbieżności punktowej:**

Mówimy, że ciąg funkcyjny $(f_n(x))_{n\in \mathbb{N}}$ jest **zbieżny punktowo** na $X \Leftrightarrow$ istnieje taka funkcja $f: X\to Y$, że $\forall x \in X \ \ \lim_{n\to \infty}{f_n(x)}=f(x)$

Funkcję $f$ nazywamy **funkcją graniczną** ciągu funkcyjnego $(f_n(x))_{n\in \mathbb{N}}$
Ozn. $f_n\overset{X}{\to}Y$, że $\forall x \in X \ \lim_{n\to \infty}{f_n(x)}=f(x)$

Czyli: $\forall x \in X \ \forall \epsilon > 0 \ \ \exists n_0 \in \mathbb{N} \ \ \forall n \geq n_0 \ |f_n(x)-f(x)| \lt \epsilon$

**Przykład**:
![[diagram-20250325.png]]
$(x^n)_{n\in \mathbb{N}}, \ \ x\in [0,1]$

Zatem naszą funkcją graniczną będzie funkcja:
$$\begin{gathered}
f:\left\{
\begin{matrix}
0,x\in [0,1)\\
1, x=1
\end{matrix}
\right.\\\\
\text{A dla każdego }x\lt 0 \ \ \lim_{n\to \infty}{x^n}=0
\end{gathered}$$

**Def zbieżności jednostajnej**:
Mówimy że ciag funkcyjny $(f_n(x))_{n\in \mathbb{N}}$ jest **zbieżny jednostajnie** na $X$:

Wtedy i tylko wtedy gdy: $\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N}\ \  \forall n\geq n_0 \ \forall x\in X \ \ |f_n(x)-f(x)|\lt \epsilon$
Czyli tutaj - tak jak nazwa mówi ten ciąg funkcyjny się stale przybliża fo funkcji granicznej, jeżeli dany $n$-ty element będzie poniżej epsilona, to kolejne też.

Ozn. $f_n\overset{X}{⇒}f$ - ciąg $(f_n(x))_{n\in \mathbb{N}}$ jest jednostajnie zbieżny na $X$.

**Twierdzenie - zbieżny jednostajnie $\implies$ zbieżny punktowo**

$f_n\overset{X}{⇒}f \implies f_n\overset{X}{\to}f$

---
**Przykład**:
$f_n(x)=\frac{\sin{nx}}{n}$

$$\begin{gathered}
f_n(x)=\frac{\sin{nx}}{n}\\\\
\lim_{n\to \infty}{\frac{\sin{nx}}{n}}=0\\
f=0\\
\text{Mamy pytanie czy:}\\
\forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N}\ \  \forall n\geq n_0 \ \forall x\in X \ \ |f_n(x)-f(x)|\lt \epsilon\\\
|f_n(x)-0|=|f_n(x)|\lt \epsilon\\
|\frac{\sin{nx}}{n}|\lt \frac{1}{n}\lt \epsilon, \ \text{Tak, dla }e=\frac{1}{n-1}\\\\
\text{Zatem jest zbieżny jednostajnie, a co za tym idzie na podstawie tw.}\\
\text{o tym że ciąg jest zbieżny punktowo wtedy gdy jest zbieżny jednostajnie, jest też }\\
\text{jednostajnie zbieżny.}
\end{gathered}$$

**Twierdzenie mówiące o tym że jeżeli funkcja ciągu funkcyjnego jest jednostajnie zbieżna, to funkcja graniczna jest ciągła.**

zał: $\forall n \in \mathbb{N}, \ \ f_n: X \to Y$ ciągłe, $f_n\overset{X}{⇒}f$
teza: $f$ jest ciągła na $X$

**Przykład:**
$f_n(x)=x^n, X=[0,1]$

wiemy że $x^n$ dla każdego $n$ jest ciągłe, (i dla każdego x)
wiemy że $f$ tego ciagu funkcyjnego to:
$$\begin{gathered}
f:\left\{
\begin{matrix}
0,x\in [0,1)\\
1, x=1
\end{matrix}
\right.
\end{gathered}$$
Czyli nie jest to ciągłe, a co za tym idzie to ten ciąg funkcyjny napewno nie jest zbieżny jednostajnie.

---
**Definicja Metryki Czebyszewa**:

Def. zbioru funkcji ograniczonych $B(X,Y)$
$f\in B(X,Y) \Leftrightarrow f: X \to Y \ \land \ f[X]$ jest ograniczony.

Zał: $f,g \in B(X,Y)$
$d_c(f,g) = \sup_{x\in X}{|f(x)-g(x)|}$


Dzięki tej metryce Czebyszewa możemy sprawdzic czy funkcja jest jednostajnie zbieżna (jeżeli jest ograniczona).

Jeżeli $f_n(x))_{n\in \mathbb{N}}$ jest ciągiem funkcyjnym ograniczonym, to jest jednostajnie zbieżny wtedy i tylko wtedy gdy: $\lim_{n\to \infty}{d_c(f_n,f)}=0$

**Przykład:**
$f_n(x)=x^n, \ \ x\in [0,1)$
$f=0$
$\lim_{n\to \infty}{\sup|x^n-0|}=1$, nie to nie jest ciąg jednostajnie zbieżny.


$$\begin{gathered}
\frac{x^3}{x^2-25}:\frac{6x^2}{2x+10}=\frac{x^3}{x^2-25}:6x^2:(2x+10)\\\\
\text{A nawet lepiej:}\\
x^3:(x^2-25):6x^2:(2x+10)\\\\
\text{Teraz widać jak byk że dzielimy przez:}\\
1) \ \ \ x^2-25\\
2) \ \ \ 6x^2\\
3) \ \ \ 2x+10\\\\
\text{A nie dzielimy przez 0 i z tego sie nam właśnie wzięły wszystkie założenia}
\end{gathered}$$







