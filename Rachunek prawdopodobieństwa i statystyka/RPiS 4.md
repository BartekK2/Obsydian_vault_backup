
### Rozkład ciągły zmiennej losowej 

Mówimy, że zmienna losowa rzeczywista $X$ ma **rozkład ciągły** jesli istnieje funkcja 

$$\begin{gathered}
f: \mathbb{R} \to [0,+\infty]
\end{gathered}$$
taka, że dla dowolnych $a,b \in \mathbb{R} \cup \{-\infty, \infty\}$ takich że $a \lt b$ zachodzi równość 

$$\begin{gathered}
P(a \lt X \lt b)=\int^{b}_{a}f(x) dx
\end{gathered}$$
Taką funkcje nazywamy **gęstością zmiennej losowej** $X$ lub **gęstością rozkładu** albo po prostu **gęstością**

Zmienną losową o rozkładzie ciągłym nazywa się też zmienną losową typu ciągłego albo nawet **zmienna losową ciągłą**. 

#### Własności rozkładów ciągłych $I$

Niech $X$ będzie zmienną o rozkładzie ciągłym
1. $\int^{+\infty}_{-\infty}f(x)dx=1$
2. $P_X(A)=\int_{A}f(x)dx$
3. $F(x)=\int^{x}_{-\infty}f(s)ds$
4. Dystrybuanta $X$ jest funkcją ciągła.
5. Dla każdego $x \in \mathbb{R}$ zachodzi $P(X=x)=0$
6. Jeśli gęstość jest ciągła w pewnym punkcie $x_0 \in \mathbb{R}$, to dystrybuanta jest w tym punkcie różniczkowalna i
   $$\begin{gathered}
f(x_0)=F'(x_0)
\end{gathered}$$
---
### Całka Lebesgue'a

Całka Lebesgue'a między innymi pozwala całkować zmienne losowe rzeczywiste i wektory losowe względem miar probabilistycznych co zapisujemy na jeden z poniższych sposobów
$$\begin{gathered}
\int_\Omega XdP=\int_\Omega X(\omega)dP(\Omega)
\end{gathered}$$

Niech $(\Omega,\Sigma,P)$ będzie przestrzenią probabilistyczną, a $X: \Omega \to \mathbb{R}$ zmienną losową rzeczywistą.

**Twierdzenie o całce względem rozkładu dyskretnego**
Jeśli $X$ jest zmienną o rozkładzie dyskretnym z funkcją prawdopodobieństwa $p$, to
$$\begin{gathered}
\int_\Omega XdP=\sum_{k: x_k \in S}x_kp(x_k)
\end{gathered}$$

**Twierdzenie o całce względem rozkładu ciągłego**
Jeśli $X$ jest zmienną o rozkładzie ciągłym z gęstościa $f$ to
$$\begin{gathered}
\int_\Omega XdP=\int^{+\infty}_{-\infty}xf(x)dx\end{gathered}$$

---
### Wartość oczekiwana 

**Wartością oczekiwaną** (również wartością średnią, wartością przecietną albo nadzieja matematyczną) zmiennej losowej rzeczywistej $X$ nazywamy liczbę określoną wzorem 

$$\begin{gathered}
\mu = \mu x = E(X)=EX \overset{def}{=} \int_\Omega X dP
\end{gathered}$$

**Uwaga**
Z uwagi na to, że całka w definicji nie zawsze istnieje niektóre zmienne losowe nie mają dobrze określonej wartości oczekiwanej.

#### Wartość oczekiwana w znanych typach rozkładów

Jeśli $X$ jest zmienna o rozkładzie dyskretnym z funkcją prawdopodobieństwa $p$, to
$$\begin{gathered}
\mu = \sum_{k: x_k \in S}x_k p(x_k)
\end{gathered}$$

Jeśli $X$ jest zmienną o rozkładzie ciągłym z gęstościa $f$ to

$$\begin{gathered}
\mu=\int^{+\infty}_{-\infty}xf(x) dx
\end{gathered}$$
**Przykłady:**
**1)**
Niech $X=\max\{d_1,d_2\}$ będzie zmienną określającą te dwie rzucone kostki. Wtedy $S=\{1,2,3,4,5,6\}$
$$\begin{gathered}
p(k)=\frac{2k-1}{36}
\end{gathered}$$
Wartość oczekiwana $X$ wynosi:
$$\begin{gathered}
\mu=1\cdot \frac{1}{36}+2\cdot \frac{3}{36}+3\cdot \frac{5}{36}+\dots+6\cdot \frac{11}{36}\approx4,47
\end{gathered}$$

**2)**
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
1-|x|, \ \  dla \ \ -1 \leq x \leq 1\\
0, \ \  \text{w przeciwnym przypadku}
\end{matrix}
\right.
\end{gathered}$$

$$\begin{gathered}
\mu=\int^{+\infty}_{-\infty}xf(x) dx=\int^{1}_{-1}x(1-|x|)dx=0
\end{gathered}$$
**3)**
Niech $X$ będzie zmienną o rozkładzie ciągłym z gęstością
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{1}{x^2}, \ \  dla \ x \geq 1\\
0, \ \ dla \ x \lt 1
\end{matrix}
\right.
\end{gathered}$$

Wtedy
$$\begin{gathered}
\mu=\int^{+\infty}_{-\infty}xf(x)dx=\int^{+\infty}_{1}x \frac{1}{x^2} dx=\int^{+\infty}_{1}\frac{1}{x}dx=+\infty
\end{gathered}$$

czyli **wartość oczekiwana $X$ nie istnieje**

---
### Momenty i momenty centralne

**Definicja**
**Momentem (zwykłym) rzędu k** zmiennej losowej $X$ dla $k \in \mathbb{N} \setminus \{0\}$ nazywamy liczbę:
$$\begin{gathered}
\mu'_k=E(X^k)
\end{gathered}$$

**Momentem centralnym rzędu k** zmiennej losowej $X$ nazywamy liczbę:
$$\begin{gathered}
\mu_k=E((X-\mu)^k)
\end{gathered}$$
**Dla rozkładów dyskretnych**
$$\begin{gathered}
\mu_k'=\sum_{i: x_i \in S}x_i^k p(x_i)\\
\mu_k=\sum_{i: x_i \in S}(x_i-\mu)^k p(x_i)
\end{gathered}$$

**Dla rozkładów ciągłych**
$$\begin{gathered}
\mu_k'=\int^{+\infty}_{-\infty}x^kf(x) dx\\
\mu_k=\int^{+\infty}_{-\infty}(x-\mu)^k f(x) dx
\end{gathered}$$
**Uwagi**
1. $\mu'_1=\mu$ - po prostu po podstawieniu pod wzory to ten sam wzór
2. $\mu_1=0$ bo przesuwamy według tej średniej 
3. Momet rzędu $k$ danej zmiennej losowej może nie istniec, ale zachodzi następujące twierdzenie
   **Jeśli istnieje moment zmiennej losowej $X$ rzędu $k$, to istnieją też wszystkie momenty rzędów $l \lt k$



---
### Wariancja 

**Wariancją** zmiennej losowej $X$ nazywamy jej drugi moment centralny tzn.
$$\begin{gathered}
Var(x)=\sigma^2_X=\sigma^2\overset{def}{=}\mu_2=E((X-\mu)^2)
\end{gathered}$$

---
### Odchylenie standardowe 

**Odchyleniem standardowym** zmiennej losowej $X$ nazywamy pierwiastek jej wariancji, tzn:
$$\begin{gathered}
\sigma=\sigma_X=\sqrt{Var(X)}
\end{gathered}$$
---
### Odchylenie przeciętne 

**Odchyleniem przeciętnym** zmiennej losowej $X$ nazywamy liczbę zdefiniowana następująco
$$\begin{gathered}
d_1=E|X-\mu|
\end{gathered}$$

---
### Własności wariancji 

1. $Var(X)=E(X^2)-(EX)^2$
2. $Var(X)=0$ zachodzi wtedy i tylko wtedy gdy $X$ jest stała z prawdopodobieństwem $1$ 

---
### Zmienne standaryzowane 

Zmienną o wartości średniej $0$ i wariancji $1$ nazywa się **zmienną standaryzowaną**.

Jeśli $X$ jest dowolną zmienną o niezerowej wariancji, to
$$\begin{gathered}
Z=\frac{X-\mu}{\sigma}
\end{gathered}$$

jest zmienną standaryzowaną, ponieważ
$$\begin{gathered}
EZ=\frac{1}{\sigma}(EX-\mu)=0\\
Var(Z)=\frac{1}{\sigma^2}Var(X)=1
\end{gathered}$$
---
### Nierówność Czebyszewa 

**Twierdzenie**

Jeśli zmienna losowa $X$ ma skończoną wartość średnia $\mu$ i skończoną wariancje $\sigma^2$, to dla dowolnego $\epsilon \gt 0$
$$\begin{gathered}
P(|X-\mu|\geq \epsilon)\leq \frac{\sigma^2}{\epsilon^2}
\end{gathered}$$
Wnioski - jeśli w miejsce $\epsilon$ podstawimy $\epsilon \sigma$ to otrzymamy następującą nierówność
$$\begin{gathered}
P(|X-\mu| \geq \epsilon \sigma)\leq \frac{1}{\epsilon^2}
\end{gathered}$$
Albo jeśli $Z=\frac{X-\mu}{\sigma}$ jest zmienną standaryzowaną, to 
$$\begin{gathered}
P(|Z| \geq \epsilon)\le \frac{1}{\epsilon^2}
\end{gathered}$$

---