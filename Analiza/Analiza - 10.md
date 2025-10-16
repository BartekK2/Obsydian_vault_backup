
### ## Przestrzenie metryczne 
#### 2025-02-15
##### Poprzednia: [[Analiza - 9]]
##### Zadania: [[]]

#analiza #przestrzen_metryczna

---
### Wstęp

**Def.** zbiór $X\neq \emptyset$

**Metryką** w zbiorze $X$ nazywamy dowolną funkcję $d: X\times X\to \mathbb{R}$ taką, że:

1. $\forall x,y \in X$   $d(x,y)\geq 0$
2. $\forall x,y \in X$  $d(x,y)=d(y,x)$ (symetria)
3. $\forall x,y,z \in X$   $d(x,z)\leq d(x,y)+d(y,z)$ (warunek trójkąta)
4. $\forall x,y \in X$   $d(x,y)=0 \Leftrightarrow x=y$

Parę $(X, d)$ nazywamy **przestrzenią metryczną**.

##### Przykłady:

$X=\mathbb{R}, \ x,y \in \mathbb{R}$
$d(x,y)=|y-x|$

$X=\mathbb{R}^2$
$d_e((x_1,y_1),(x_2,y_2))=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}$ - **metryka euklidesowa**

$d_t((x_1,y_1),(x_2,y_2))=|x_2-x_1|+|y_2-y_1|$ - **metryka taksówkowa**
$d_m((x_1,y_1),(x_2,y_2))=\max\{|x_2-x_1|, |y_2-y_1|\}$ - **metryka maksimum**

$X=\mathbb{R}^n, x=(x_1,\dots,x_n), \ y=(y_1,\dots,y_n)$ 
$d_e(x,y)=\sqrt{\sum^{n}_{i=1}{(y_i-x_i)^2}}$
$d_t(x,y)=\sum^{n}_{i}{|y_i-x_i|}$
$d_m(x,y)=\max\{|y_i-x_i|: i=1,\dots,n\}$

$X=\emptyset, \ x,y \in X$
$$\begin{gathered}
d(x,y)=\left\{
\begin{matrix}
0, x=y\\
1, x\neq y
\end{matrix}
\right. - \ metryka \ dyskretna
\end{gathered}$$
---
### Przestrzeń metryczna
 
**Def.**
$(X,d) - \text{przestrzeń metryczna}$
$x_0\in X, r\gt 0$ 
**Kulą** o środku $x_0$ i promieniu $r$ nazywamy $K(x_0,r)=\{x\in X: d(x_0,x)\lt r\}$

**Def.**
$(X,d) - \text{przestrzeń metryczna}$
Zbiór $A\subset X$ nazywamy **ograniczonym** $\Leftrightarrow \exists x_0\in X \ \exists r \gt 0 \ \ \ A\subset K(x_0,r)$

**Def.**

$I$ - dowolny zbiór indeksów
$\forall i \in I$ $A_i$ - zbiór (rodzina zbiorów)
$\bigcup_{i\in I}{A_i}=\{x: \exists i\in I \ \ \ x\in A_i\}$ - suma zbiorów 
$\bigcap_{i\in I}{A_i}=\{x: \forall i\in I \ \ \ x\in A_i\}$ - wspólna część zbiorów 

**Def.** topologii w zbiorze
$X\neq \emptyset$
Topologią $\tau$ w zbiorze $X$ nazywamy dowolną rodzinę zbiorów $A\subset X$ spełniającą warunki:
1. $\emptyset \in \tau, X\in \tau$
2. $\forall i \in I \ A_i \in \tau \implies \bigcup_{i\in I} \ A_i \in \tau$
3. $\forall i =1,\dots,n \ A_i\in \tau \implies \bigcap^n_{i=1}\ A_i \in \tau$

Zbiory należące do $\tau$ nazywamy **zbiorami otwartymi**.

**Def.**
$(X,d) - \text{przestrzeń metryczna}$
Zbiór $U \in X$ nazywamy otwartym w $(X,d)\Leftrightarrow U=\emptyset$ lub $\forall x \in X \ \exists r\gt 0 \ K(x,r)\subset U$

**Tw.** 
$(X,d) - \text{przestrzeń metryczna}$
$\tau_d = \{U \in X: U - otwarty \ w \ (X,d)\}$ jest topologią na zbiorze $X$ (nazywaną **topologią indukowaną przez metrykę** $d$)

**Dowód:**

Żeby udowodnić że $\tau_d=\{U\in X: U - otwarty \ w \ (X,d)\}$ jest topologią należy udowodnić warunki topologi to znaczy:

Zbiór pusty należy do $\tau_d$ - to wiemy na podstawie definicji zbioru otwartego, to znaczy zbiór otwarty jest albo pusty albo taki że da się wyznaczyć kule która się zawiera w tym wzorze.
Więc wiemy że $\tau_d$ będące sumą zbiorów otwartch musi zawierać też zbiór pusty.

Suma zbiorów otwartych także jest zbiorem otwartym zatem należy do $\tau_d$:

Tu wystarczy uzasadnić że skoro istnieje takie $x$ oraz $r$ dla $A_i$ takie że $K(x,r)\subset A_i$ (bo $A_i$ jest zbiorem otwartym) to także i dodanie nowych elementów, tworzące sume wszystkich zbiorów jest zbiorem otwartym bo przecież $K(x,r) \subset A_i\subset \bigcup_{i\in I}$ 

Oraz warunek że część wspólna tych zbiorów jest zbiorem otwartym.
Tutaj działamy analogicznie jak przy sumie, z tym że musimy wybrać minimalną kule tak by była ona podzbiorem jednego ze zbiorów, wtedy będzie też podzbiorem części wspólnej.

$$\begin{gathered}
1) \emptyset \in T_d \ \text{(z definicji zbioru otwartego w p. metrycznej)}\\
X\in T_d, \text{bo każda kula }K(x,r)=\{x\in X: \dots\}\subset X\\
\\
2) \forall i\in I \ A_i\in \tau_d\implies \bigcup_{i\in I}A_i\in \tau_d?\\\
\Leftrightarrow \forall x \in \bigcup_{i\in I}A_i \ \ \exists r\gt 0 \ \ \ K(x,r) \subset \bigcup_{i\in I}A_i\\\\
\text{Weźmy dowolny }x\in \bigcup_{i\in I} \ A_i\Leftrightarrow \exists i_0 \in I \ x\in A_{i_0}\text{ - zbiór otwarty}\implies \\
\implies \exists r_0\gt 0 \ K(x,r_0)\subset A_{i_0}\subset \bigcup_{i\in I}A_i\\\\
1) \forall i=1,\dots,n \ A_i\in \tau_d \implies \bigcap^n_{i=1}\ A_i\in \tau_d\\
\text{Mamy pokazać, że }\forall x\in \bigcap^n_{i=1}\ A_i\ \exists r\gt 0 \ K(x,r)\subset \bigcap^n_{i=1}\ A_i\\
\text{Niech }x\in \bigcap^n_{i=1}\ A_i\Leftrightarrow \forall i=1,\dots,n x\in A_i \Leftrightarrow \forall i=1,\dots,n \ \exists r_i\gt 0 \ K(x,r_i)\subset A_i\\
\text{Niech }r=\min\{r_1,\dots,r_n\}. \text{Wtedy }K(x,r)\subset \bigcap^n_{i=1}\ A_i
\end{gathered}$$

**Def.**
$(X,d) - \text{przestrzeń metryczna}$, $\tau$ - topologia na $X$, $A\subset X$

Wtedy $\tau_A=\{A\cap U: U \in \tau\}$ jest topologią na zbiorze $A$ (zwaną **topologią indukowaną przez $\tau$ na zbiorze $A$**)

**Def.**
$(X,\tau) - \text{przestrzeń metryczna}$, $A\subset X$

**Wnętrzem zbioru** $A$ nazywamy największy (ze względu na zawieranie, $\subset$) zbiór otwarty zawarty w $A$

Ozn. $int \ A$ - interior

**Def.**
$x_0\in X$
**Otoczeniem** punktu $x_0 \in X$ nazywamy dowolny zbiór otwarty zawierający punkt $x_0$.
Ozn. $ot(x_0)$ - zbiór wszystkich otoczeń punktu $x_0$

**Def.**
$B\subset X$
Zbiór $B$ nazywamy **domkniętym** $\Leftrightarrow X\setminus B$ jest zbiorem otwartym.

**Tw.**
Własności zbiorów domkniętych
1. $\emptyset, X$ - zbiory domknięte
2. $\forall i \in I \ B_i - domknięty \implies \bigcap_{i\in I} B_i - domknięty$
3. $\forall i \in 1,\dots,n$ $B_i - domknięty \implies \bigcup^n_{i=1} B_i - domknięty$

**Def.**
**Domknięciem** zbioru $A\subset X$ nazywamy najmniejszy zbiór domknięty zawierający zbiór $A$.
Ozn. $\overline{A}$

**Def.**
Punkt $x_0 \in X$ nazywamy punktem **brzegowym** zbioru $A\subset X \Leftrightarrow \forall r\gt 0 \ \ \ K(x_0,r)\cap A\neq \emptyset \land K(x_0,r)\cap (X\setminus A)\neq \emptyset$
**Brzegiem** zbioru $A$ nazywamy zbiór wszystkich punktów brzegowych zbioru $A$.
Ozn. $\partial A$.

**Def.**
Punkt $x_0\in X$ nazywamy **punktem skupienia** zbioru $A\subset X \Leftrightarrow \forall r\gt 0\ \ (K(x_0,r)\setminus \{x_0\})\cap A\neq \emptyset$

**Tw.** 
$A$ jest zbiorem domkniętym $\Leftrightarrow$ gdy $A$ zawiera wszystkie swoje punkty skupienia.

**Def.** (granicy ciągu)
$(X,d) - \text{przestrzeń metryczna}$
$(a_n)_{n\in \mathbb{N}}\subset X, g\in X$
$\lim_{n\to \infty}{a_n}=g\Leftrightarrow \lim_{n\to \infty}d(a_n,g)=0$
($\Leftrightarrow \forall \epsilon \gt 0 \ \exists n_0 \in \mathbb{N} \ \forall n \geq n_0 \ \ d(a_n,g)\lt \epsilon)$

**Def.** (o równoważności metryk)
$(X,d_1), (X,d_2)$ - przestrzenie metryczne

Metryki $d_1$ i $d_2$ nazywamy **równoważnymi** na $X \Leftrightarrow$ $\forall (x_n)_{n\in \mathbb{N}} \subset X \ \ (x_n)_{n\in \mathbb{N}}$ zbieżny w $(X,d_1)\Leftrightarrow (x_n)_{n\in \mathbb{N}}$ zbieżny w $(X,d_2)$

**Def.** (jednostajnej równoważności metryk)

Metryki $d_1$ i $d_2$ nazywamy **jednostajnie równoważnymi na $X$** $\Leftrightarrow  \exists m\gt 0 \ \exists M\gt 0 \ \forall x,y \in X \ d_1(x,y)\leq Md_2(x,y)$ i $d_2(x,y)\leq md_1(x,y)$

**Tw.** Jeśli $d_1$ i $d_2$ są jednostajnie równoważne na $X$, to $d_1$ i $d_2$ są równoważne na $X$.

**Tw.** Metryki: euklideoswa, taksówkowa i maksimum są jednostajnie równoważne (i równoważne na $\mathbb{R}^n$)

**Def.** (punktu skupienia)
$A\subset X$
Punkt $x_0 \in X$ nazywamy punktem skupienia zbioru na $A \Leftrightarrow \exists (x_n)_{n\in \mathbb{N}} \subset A\setminus \{x_0\}\ \ \ \lim_{n \to \infty}{x_n}=x_0$

**Def.** (ciągu Cauchy'ego)

Ciąg $(a_n)_{n\in \mathbb{N}}$ jest ciągiem Cauchy'ego w $(X,d) \Leftrightarrow \forall \epsilon \gt 0 \ \exists n_0 \in \mathbb{N} \ \forall n,m \geq n_0 \ \  \ d(a_n,a_m)\lt \epsilon$

**Tw.**
Każdy ciąg zbieżny w $(X,d)$ jest ciągiem Cauchy'ego w $(X,d)$ 

Dowód: $0\leq d(a_n,a_m)\leq d(a_n,g)+d(a_m,g)\lt \frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon$

**Def.** Przestrzeń metryczną $(X,d)$ nazywamy **zupełną** $\Leftrightarrow$ każdy ciąg Cauchy'ego elementów w tej przestrzeni jest zbieżny (do granicy należącej do tej przestrzeni)

**Def.** (zbioru zwartego)
$(X,d) - \text{przestrzeń metryczna}$

Zbiór $A\subset X$ nazywamy **zwartym** $\Leftrightarrow \forall (a_n)_{n\in \mathbb{N}}\subset A \ \exists (a_{n_k})_{k\in \mathbb{N}}\ \lim_{k\to \infty}{a_{n_k}=g\in A})$
**Istnieje podciąg zbieżny do $g$**

**Tw.** $(\mathbb{R}^n,d), d\in \{d_e,d_t,d_m\}$
Zbiór $A\subset \mathbb{R}^n$ jest zwarty $\Leftrightarrow A$ jest zbiorem domkniętym i ograniczonym.

---

### Odwzorowania ciągłe

**Def.** $f: X\to Y$ 
$A\subset X$
**Obrazem zbioru $A$** poprzez odwzorowanie $f$ nazywamy zbiór $f[A]=\{f(x)\in Y: x\in A\}$

**Def.** $B\subset Y$
**Przeciwobrazem zbioru $B$** poprzez odwzorowanie $f$ nazywamy zbiór $f^{-1}[B]=\{x\in X: f(x)\in B\}$

**Def.** (granicy funkcji)
$f: X\to Y$
$x_0\in X, g\in Y$

Def topologiczna (Cauchy'ego)
$\lim_{x\to x_0}{f(x)}=g\Leftrightarrow \forall V \in ot(g)\ \exists U \in ot(x_0)\ f[U \setminus \{x_0\}]\subset V$

Def. Cauchy'ego w przestrzeniach metrycznych
$(X,d), (Y,p)$ - przestrzenie metryczne
$\lim_{x\to x_0}{f(x)}=g \Leftrightarrow \forall \epsilon \gt 0 \ \exists \delta \gt 0 \ \forall x\in X \ 0 \lt d(x,x_0)\lt \delta \implies p(f(x),g)\lt \epsilon$

Def. Heinego (w przestrzeniach metrycznych)
$\lim_{x\to x_0}{f(x)}=g \Leftrightarrow \forall (x_n)_{n\in \mathbb{N}} \subset X \setminus \{x_0\} \ \lim_{n\to \infty}{d(x_n,x_0)}=0 \implies \lim_{n\to \infty}{p(f(x_n),g)}=0$
($\lim_{n\to \infty}x_n)=x_0\implies \lim_{n\to \infty}{f(x_n)}=g$)

**Def.** (funkcji ciągłej)

$f: X_{\tau_x}\to Y_{\tau_y}$

$f$ jest ciągła w zbiorze $X\Leftrightarrow \forall V\in \tau_y\ \  f^{-1}[V]\in \tau_x$

$f$ jest ciągła w $x_0\in X \Leftrightarrow \lim_{x\to x_0}{f(x)=f(x_0)}$

$f$ jest ciągła w zbiorze $A\subset X \Leftrightarrow f$ jest ciągła w każdym punkcie $x_0\in A$

**Def.** 
$f: X\to Y, \ (X,d), \ (Y,p)$ - przestrzenie metryczne

Odwzorowanie $f$ nazywamy **ograniczonym** $\Leftrightarrow f[X]$ jest zbiorem ograniczonym (w przestrzeni $(Y,p)$)

**Tw.** o zwartości obrazu funkcji ciągłej na zbiorze zwartym
Zał: $f: X\to Y, (X,d),(Y,p)$ - przestrzenie metryczne
$f$ ciągła na $X$ 
$X$ - zbiór zwarty
Teza: $f[X]$ jest zbiorem zwartym

**Dowód:**

Mamy pokazać że $\forall x_n \subset f[x] \ \exists(y_{n_k})\lim_{k\to \infty}{y_{n_k}=y_0}$ gdzie $y_0\in f[X]$

Niech $(y_n)\subset f[X]$ będzie dowolnym ciągiem.
$\forall n \in \mathbb{N} \ \exists x_n\in X \ f(x_n)=y_n$
$(x_n)\subset X, X$ - zwarty $\implies \exists(x_{n_k})\ \lim_{x\to \infty}{x_{n_k}=x_0, x_0\in X}$
$y_{n_k}=f(x_{n_k})$
$\lim_{k\to \infty}{x_{n_k}}=\lim_{k\to \infty}{f(y_{n_k})}=f(x_0)=y_0\in f[X]$

**Tw.** (Weierstrassa o osiąganiu kresów)
Zał: $(X,d)$ - przestrzeń metryczna ($\mathbb{R}, |\cdot|)$
$X$ - zwarty
$f: X\to \mathbb{R}$ ciągła
Teza:
$\exists x_1 \in X \ f(x_1)=sup f[X]$
$\exists x_2 \in X \ f(x_2)=inf f[X]$

**Dowód:** Twierdzenie jest wnioskiem z tw. poprzedniego.

$f[X]\subset \mathbb{R}$ - jest zwarty (a z odpowiedniego tw. oznacza to, że $f[X]$ jest zbiorem ograniczonym i domkniętym)

**Def.** $(X,d)$ - przestrzeń metryczna

$X$ - nazywamy **niespójną** $\Leftrightarrow \exists A_1,A_2\ (otwarte) \in \tau_d$ takie że:

$A_1\cup A_2=X$
$A_1\cap A_2=\emptyset$
$A_1\neq \emptyset, A_2\neq \emptyset$

**Def.** $X$ jest **spójna** $\Leftrightarrow X$ nie jest niespójna.

**Tw.** (o przyjmowaniu wartości pośrednich)
Zał $(X,d)$ - przestrzeń metryczna spójna 
$f: X\to \mathbb{R}$ ciągła
$x_1,x_2 \in X \ f(x_1)\lt f(x_2)$

Teza: $\forall c\in (f(x_1),f(x_2)) \ \exists x_0 \in X \ f(x_0)=c$


**Tw.** (o własności Darboux)
Zał: $f: A \to \mathbb{R}$ ciągła
$A$ - odcinek (przedział) $\subset \mathbb{R}$
$x_1,x_2\in A \ f(x_1)\lt f(x_2)$

Teza: $\forall c \in (f(x_1),f(x_2))\ \exists x_0 \in (x_1,x_2) \ f(x_0)=c$

**Tw.** (o spójności obrazu zbioru spójnego)
Zał $f: X\to Y, (X,d), (Y,p)$ - przestrzenie metryczne 
$X$ - spójna 
$f: X \to Y$ - ciągła

Teza: $f[X]$ jest spójny.

---
### Przestrzenie unormowane

$(X,K,+,\cdot)$ - przestrzeń wektorowa, $K=\mathbb{R} \vee K=\mathbb{C}$

**Def.** Funkcję $|| \cdot ||: X\to \mathbb{R}$ nazywamy **normą** w $X\Leftrightarrow$

$\forall x\in X \ ||x|| \geq 0$
$\forall \alpha \in K \ \forall x\in X \ ||\alpha \cdot x|| = |\alpha| \ ||x||$ - jednorodność normy 
$\forall x,y \in X \ ||x+y|| \leq ||x||+||y||$ - warunek trójkąta
$\forall x\in X \ ||x||=0 \Leftrightarrow x=\overline{0}$

**Tw.** Każda przestrzeń unormowana jest metryczna
Zał: $(X, || \cdot ||)$ - przestrzeń unormowana
$x,y \in X \ d(x,y)=||x-y||$ - metryka indukowana przez normę
Teza: $(X,d)$ - przestrzeń metryczna

**Def.** Przestrzeń unormowaną i zupełną nazywamy **przestrzenią Banacha**.

---
### Przestrzenie unitarne

**Def.** $(X,K,+,\cdot)$ - przestrzeń wektorowa $K=\mathbb{R} \vee K=\mathbb{C}$

Funkcję $\circ: X\times X \to K$ nazywamy **iloczynem skalarnym**

$\forall x \in X \ x\circ x \geq 0$
$\forall x,y \in X \ x\circ y=\overline{y\circ x}$
$\forall x,y,z \in X \ (x+y)\circ z=x\circ z+y\circ z$
$\forall x,y \in X \ \forall \alpha \in K \ (\alpha x)\circ y = \alpha(x\circ y)$
$\forall x\in X \ x\circ x =  0 \Leftrightarrow x=\vec{0}$

$(X, \circ)$ - przestrzeń unitarna


**Tw.** Każda przestrzeń unitarna jest przestrzenią unormowaną (z $||x||=\sqrt{x\circ x}$)

**Def.** Przestrzeń unitarną zupełną nazywamy **przestrzenią Hilberta**


