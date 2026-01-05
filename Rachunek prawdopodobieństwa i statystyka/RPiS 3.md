
### Zmienna losowa o dowolnych wartościach 

Niech $(\Omega, \Sigma, P)$ będzie przestrzenią probabilistyczną, $\chi$ dowolnym niepustym zbiorem, a $\Sigma_{\chi}$ $\sigma$-algebrą podzbiorów $\chi$.

**Definicja**

**Zmienną losową** nazywamy odwzorowanie 
$$\begin{gathered}
X: \Omega \to \chi
\end{gathered}$$
takie, że dla każdego $A \in \Sigma_{\chi}$ zachodzi warunek 
$$\begin{gathered}
X^{-1}(A)\in \Sigma
\end{gathered}$$
**Wytłumaczenie na przykładzie:**
Rzuty kostką:
$$\begin{gathered}
\Omega=\{1,2,3,4,5,6\}\\
\Sigma=2^\Omega\\\\
\chi=\{0,1\}\\
\text{gdzie:}\\
0 - \text{parzyste}\\
1 - \text{nieparzyste}\\
\end{gathered}$$

Zatem nasza zmienna losowa to:
$$\begin{gathered}
X(\omega)=\left\{
\begin{matrix}
1 \ \text{jeśli }\omega \in \{2,4,6\}\\
0 \ \text{jeśli }\omega \in \{1,3,5\}\\
\end{matrix}
\right.
\end{gathered}$$
Jeżeli tylko powyższe odwzorowanie spełnia **warunek mierzalności**
$$\begin{gathered}
\Sigma_{\chi}=\{\emptyset,\{0\},\{1\},\{0,1\}\}
\end{gathered}$$

Zatem dla każdego $A$ w $\Sigma_\chi$ sprawdzamy:
$$\begin{gathered}
X^{-1}(\emptyset)=\emptyset \in \Sigma\\
X^{-1}(\{0\})=\{2,4,6\}\in \Sigma\\
X^{-1}(\{1\})=\{1,2,3\} \in \Sigma\\
X^{-1}(\{0,1\})=\Omega \in \Sigma\\
\end{gathered}$$
To, czy funkcja $X: \Omega \to \chi$ jest zmienną losową, **zależy nie tylko od samego $X$ ale również od $\sigma$-algebry $\Sigma$ na $\Omega$**

Na przykład przyjmując tutaj $\Sigma=\{\emptyset,\Omega,\{1,2,3\},\{4,5,6\}\}$ nie spełnimy warunku mierzalności.


#### Zmienne losowe rzeczywiste i $n$-wymiarowe

Jeśli $\chi=\mathbb{R}$ i $\Sigma_{\chi}=\mathbb{B}(\mathbb{R})$, to $X$ nazywamy **zmienną losową rzeczywistą** albo **zmienną losową jednowymiarową**.

Jeśli $\chi=\mathbb{R}^n$ i $\Sigma_\chi=\mathbb{B}(\mathbb{R}^n)$ dla $n \geq 2$, to $X$ nazywamy **zmienną losową n-wymiarową** albo **wektorem losowym**

#### Uwaga o zbiorach przeliczalnych

Jeśli $\Sigma=2^\Omega$, to każde odwzorowanie 
$$\begin{gathered}
X: \Omega \to \chi
\end{gathered}$$
jest zmienną losową 

(bo zawsze to co będzie w sigma algebrze zmiennej losowej będzie też w sigmie algebrze zbiorów elementarnych)

---
### Rozkład prawdopodobieństwa zmiennej losowej 

Niech $(\Omega, \Sigma, P)$ będzie przestrzenią probabilistyczną, $\chi$ niepustym zbiorem, $\Sigma_\chi$ $\sigma$-algebrą w $\chi$, a $X: \Omega \to \chi$ zmienną losową.

**Definicja**
Funkcję:
$$\begin{gathered}
P_X: \Sigma_\chi \to [0,1]
\end{gathered}$$
określoną następująco
$$\begin{gathered}
P_X(A)=P(X^{-1}(A))
\end{gathered}$$
nazywamy **rozkładem prawdopodobieństwa zmiennej losowej** $X$.

**Oznaczenie**
$$\begin{gathered}
P(X \in A)\overset{ozn}{=} P(\{\omega \in \Omega: X(\omega) \in  A\})=P{(X^{-1}(A))}
\end{gathered}$$
Tutaj oznaczamy tak naprawde to co siedzi w $P$ a nie całe $P(\dots)$, chodzi o aspekt $X \in A$ który definiujemy coś a'la obraz odwzorowania czy coś. **preobraz?**

zatem:
$$\begin{gathered}
P_X(A)=P(X \in A)
\end{gathered}
$$

Podobnie stosujemy oznaczenia:
$$\begin{gathered}
P(X=x)=P(\{\omega \in \Omega: X(\omega)=x\})
\end{gathered}$$
oraz 
$$\begin{gathered}
P(X \lt a)=P(\{\omega \in \Omega: X(\omega)\lt a\})
\end{gathered}$$
w skrócie chodzi o to żebyśmy mogli działać na mierze probabilistycznej z przestrzeni probabilistycznej a nie z rozkładu zmiennej losowej. Ponadto pozwoli nam to liczyć rzeczy w tym rozkładzie ciągłym.

---
### Rozkład zmiennej jako miara probabilistyczna 

**Twierdzenie**
Rozkład prawdopodobieństwa $P_X$ zmiennej losowej $X: \Omega \to \chi$ jest miarą probabilistyczną na $\chi$

Oznacza to tyle że spełnia warunki bycia miara probabilistyczną tj:
1. $P_X(\Omega)=1$
2. dla dowolnego ciągu zdarzeń $A_1,A_2,\dots \ (A_i \in \Sigma_\chi)$ takiego, że
   $$\begin{gathered}
A_i \cap A_j = \emptyset &dla & i\neq j
\end{gathered}$$
zachodzi równość
$$\begin{gathered}
P_X\left(\bigcup_{i=1}^\infty A_i \right)=\sum^{\infty}_{i=1}P(A_i)
\end{gathered}$$
**Dowód to skorzystanie z definicji rozkładu czyli tego jak się ma element zmiennej losowej do zdarzeń elementarnych podstawienie i skorzystanie z miary probabilistycznej przestrzeni probabilistycznej**

---
### Dystrybuanta zmiennej losowej 

Niech $X: \Omega \to \mathbb{R}$ będzie zmienną losową rzeczywistą.

**Definicja**

**Dystrybuantą zmiennej losowej rzeczywistej** $X$ nazywamy funkcję:

$$\begin{gathered}
F_X: \mathbb{R} \to [0,1]
\end{gathered}$$
określoną wzorem 

$$\begin{gathered}
F_X(x
)\overset{def}{=}P(X \leq x)=P_X((-\infty,x])
\end{gathered}$$

#### Własności dystrybuanty 
1. Jeśli $a\lt b,$ to $F_X(b)-F_X(a)=P(a \leq X \leq b)$
2. $F_X$ jest niemalejąca
3. $\lim_{x\to - \infty}F_X(x)=0$ i $\lim_{x \to +\infty}F_X(x)=1$
4. $F_X$ jest prawostronnie ciągła
5. $F_X$ jest ciągła w $x_0 \in \mathbb{R}$ wtedy i tylko wtedy gdy
   $$\begin{gathered}
P(X=x_0)=0
\end{gathered}$$



---
### Rozkład dyskretny zmiennej losowej 

Mówimy że zmienna losowa rzeczywista $X$ ma **rozkład dyskretny** jeśli istnieje **przeliczalny** zbiór $S \subset \mathbb{R}$ taki że
$$\begin{gathered}
P_X(S)=1
\end{gathered}$$

Taką zmienną nazywamy również zmienną losową dyskretną albo zmienną losową typu skokowego.

W tej sytuacji zbiór $S$ ma postać 
$$\begin{gathered}
S=\{x_1,\dots,x_N\}\\
lub\\
S=\{x_1,x_2,\dots\}
\end{gathered}$$

---
