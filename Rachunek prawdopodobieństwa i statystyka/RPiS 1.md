
### Interpretacje prawdopodobieństwa


**Obiektywistyczna** - prawdopodobieństwo jest liczbą określającą pewien obiektyczny lub fizyczny stan rzeczy, np. interpretacja częstościowa albo skłonnościowa

**Subiektywistyczna** - prawdopodobieństwo określa *subiektywny* poziom ufności

---
### Doświadczenie losowe

**Def.**

Doświadczenie nazywamy **losowym** jeśli:

- może być powtarzane w (zasadniczo) tych samych warunkach
- jego wynik nie może być przewidziany w sposób pewny 
- zbiór wszystkich możliwych wynikach jest znany i może być opisany przed przeprowadzeniem doświadczenia 

---

### Przestrzeń zdarzeń elementarnych 

**Def.**

Niepusty zbiór $\Omega$ wszystkich możliwych wyników doświadczenia losowego nazywamy **przestrzenią zdarzeń elementarnych** albo **przestrzenią próbkowania**

Elementy $\Omega$ nazywamy **zdarzeniami elementarnymi**.

**Przykładowo:**

Dla jednokrotnego rzutu monetą symetryczną:
$$\begin{gathered}
\Omega=\{O,R\}
\end{gathered}$$
Dla dwukrotnego rzutu monetą symetryczną
$$\begin{gathered}
\Omega=\{OO,OR,RO,RR\}
\end{gathered}$$
Dla rzutu kostką sześcienną
$$\begin{gathered}
\Omega=\{1,2,3,4,5,6\}
\end{gathered}$$
Dla $n-$krotnego rzutu kostką
$$\begin{gathered}
\Omega=\{(d_1,\dots,d_n): d_i\in \{1,\dots,6\}\}
\end{gathered}
$$
Dla eksperymentu polegającego na tym, że dotąd rzucamy monetą, aż wypadnie orzeł
$$\begin{gathered}
\Omega=\{O,RO,RRO,RRRO,\dots\}
\end{gathered}$$
Dla eksperymentu polegającego na obserwacji momentu pierwszej awarii laptopa
$$\begin{gathered}
\Omega=[0,+\infty)
\end{gathered}$$

---
### $\sigma$-algebra zdarzeń

W rodzinie wszystkich podzbiorów $\Omega$ wyróżniamy podrodzine $\Sigma$ o następujących własnościach:

1. $\Omega \in \Sigma$
2. Jeśli $A\in \Sigma$, to $A'=\Omega \setminus A \in \Sigma$
3. Dla dowolnego ciągu zbiorów $A_1,A_2,\dots$ takiego że $A_i \in \Sigma$ dla dowolnego $i\in \mathbb{N}$, zachodzi:
   $$\begin{gathered}
\bigcup^{\infty}_{i=1}{A_i\in \Sigma}
\end{gathered}$$

**Definicja:**

Rodzinę $\Sigma$ o takich własnościach nazywamy $\sigma$-**algebrą zdarzeń**, a jej elementy **zdarzeniami losowymi**.

#### Wyjaśnienie 

**Można to także interpretować w taki sposób że tworzymy sobie zbiór pewnych właściwości które nas interesują dla przykładu rozpatrzmy liczby $1-10$ jako zdarzenia elementarne - dla własności $1$ $\Sigma=\{\emptyset,\Omega\}$ nie interesuje nas właściwie nic zatem to taki fundament, a jeśli interesuje nas czy dana liczba jest parzysta (własność $2$ ) $A-parzyste$ to automatycznie interesuje nas czy jest również to zdarzenie nieparzyste, prawda? Tak samo jak przy tym czy wygramy na loterii interesuje nas czy nie wygramy bo to też nam mówi o tym że nie wydarzyło sie to co nas interesuje. Następnie $3$ własność mówi jedynie tyle że jeżeli interesuje nas czy liczba $1-10$ jest parzysta i podzielna przez $3$ to z 2 pierwszych własności dostajemy tak: $\{\emptyset, \Omega, \{3,6,9\}, \{2,4,6,8\},\{1,2,4,5,7,8\}, \{1,3,5,7,9\}\}$ ale nie dowiadujemy sie z tego wszystkiego! Co jeśli chcemy wiedzieć czy liczba jest parzysta lub podzielna przez 3? Dodajemy zbiór $\{3,6,9\}\cup \{2,4,6,8\}$ (i jego przeciwieństwo) $\{1,5,7\}$ - ani parzysta ani podzielna przez 3. Tak samo postąpimy dla nie parzysta lub nie podzielna przez 3, a przeciwieństwo takiego zbioru to i parzysta i nie podzielna przez 3! $\{6\}$. W każdym razie zawsze będziemy mieli każdy zbiór jaki nas interesuje**


---
### Własności zdarzeń

Jeśli $\Sigma$ jest $\sigma$-algebrą zdarzeń, to:

1. $\emptyset \in \Sigma$
2. Jeśli $A_1\in \Sigma, A_2\in \Sigma,\dots, A_n \in \Sigma, to A_1\cup A_2 \cup \dots \cup A_n \in \Sigma$
3. Dla dowolnego ciągu $A_1,A_2,\dots$ takiego, że $A_i \in \Sigma$ dla $i\in \mathbb{N}$ zachodzi:
   $$\begin{gathered}
\bigcap^\infty_{i=1}A_i \in \Sigma
\end{gathered}$$
4. Jeśli $A,B \in \Sigma$, to $A\setminus B \in \Sigma$
   
---
### Terminologia

- $\emptyset$ nazywamy **zdarzeniem niemożliwym**
- $\Omega$ nazywamy **zdarzeniem pewnym**
- $A'=\Omega \setminus A$ nazywamy **dopełnieniem zdarzenia** $A$
- Jeśli $A\cap B=\emptyset$, to mówimy, że zdarzenia $A$ i $B$ **wzajemnie sie wykluczają**

---
**Przykłady:**

1. Dla dowolnego $\Omega$ możemy wziąć
   $\begin{gathered}\Sigma=2^\Omega=\{A: A \subset \Omega\}\end{gathered}$
   Jest to wybór typowy dla skończonych i przeliczalnych przestrzeni zdarzeń elementarnych.
2. Dla dowolnego $\Omega$ można wziąć $\Sigma=\{\emptyset, \Omega\}$ - tzw. $\sigma$-algebrę trywialną.
3. Dla $\Omega=\{1,2,3\}$ można wziąć
   $\Sigma=\{\emptyset,\Omega,\{1\},\{2,3\}\}$

---
### Zbiory Borelowskie

Jeśli $\Omega=\mathbb{R}^N$, to typowo przyjmuje się:
$$\begin{gathered}
\Sigma=\mathbb{B}(\mathbb{R}^N)
\end{gathered}$$
gdzie $\mathbb{B}(\mathbb{R}^N)$ jest najmniejszą $\sigma$-algebrą zawierającą zbiory otwarte. Nazywa się ją $\sigma$-algebrą **zbiorów borelowskich**.

#### Własności zbiorów Borelowskich

1. $\mathbb{B}(\mathbb{R}^N)$ jest najmniejszą $\sigma$-algebrą zawierającą kostki otwarte, czyli zbiory postaci:
   $$\begin{gathered}
(a_1,b_1)\times (a_2,b_2)\times \dots \times (a_N,b_N)
\end{gathered}$$
2. Jeśli $A$ jest dowolną kostką (iloczynem kartezjańskim dowolnych przedziałów), to $A\in \mathbb{B}(\mathbb{R}^N)$
3. Jeśli $A$ jest zbiorem otwartym, to $A \in \mathbb{B}(\mathbb{R}^N)$
4. Jeśli $A$ jest zbiorem domkniętym, to $A \in \mathbb{B}(\mathbb{R}^N)$

---
- Ponieważ zdarzenia elementarne są elementami przestrzeni $\Omega$, a zdarzenia jej podzbiorami, więc **zdarzenia elementarne nie są zdarzeniami** w sensie formalnym.
- Natomiat dla $\sigma$-algebry z przykładu $1$ i dla $\sigma$-algebry zbiorów borelowskich prawdą jest, że
  $$\begin{gathered}
\forall \omega \in \Omega: \{\omega\} \in \Sigma
\end{gathered}$$
Jeśli więc przyjmiemy naturalne utożsamienie $\omega$ z $\{\omega\}$, możemy uznać zdarzenia elementartne za zdarzenia w sensie tego utożsamienia.

---
### Miara probabilistyczna 

**Miarą probabilistyczną** (albo **rozkładem prawdopodobieństwa**) w przestrzeni $\Omega$ z $\sigma$-algebrą zdarzeń $\Sigma$ nazywamy dowolne odwzorowanie
$$\begin{gathered}
P: \Sigma \rightarrow [0,1]
\end{gathered}$$
spełniające następujące warunki:
1. $P(\Omega)=1$
2. dla dowolnego ciągu zdarzeń $A_1,A_2,\dots \ (A_i \in \Sigma)$ takiego, że
   $$\begin{gathered}
A_i \cap A_j = \emptyset &dla & i\neq j
\end{gathered}$$
zachodzi równość
$$\begin{gathered}
P\left(\bigcup_{i=1}^\infty A_i \right)=\sum^{\infty}_{i=1}P(A_i)
\end{gathered}$$
---
### Przestrzeń probabilistyczna i prawdopodobieństwo

**Definicja**
**Przestrzenią probabilistyczną** nazywamy trójke $(\Omega, \Sigma, P)$, gdzie $\Omega$ jest niepustym zbiorem, $\Sigma$-$\sigma$ algebrą w $\Omega$, a $P$ - miarą probabilistyczną.

**Prawdopodobieństwem** zdarzenia $A$ nazywamy liczbę $P(A)$

#### Przykład - prawdopodobieństwo klasyczne

Niech
$$\begin{gathered}
\Omega=\{\omega_1,\dots,\omega_N\}, \Sigma=2^\Omega
\end{gathered}$$
Dla $A \subset \Omega$ określamy
$$\begin{gathered}
P(A)=\frac{|A|}{|\Omega|}
\end{gathered}$$
Tak określone odwzorowanie $P$ jest miarą probabilistyczną. Prawdopodobieństwo wyznaczane przez tę miarę nazywa się **prawdopodobieństwem klasycznym**.

---
### Własności prawdopodobieństwa

1. $P(\emptyset)=0$
2. Jeśli skończony ciąg zdarzeń $A_1,A_2,\dots,A_n$ spełnia warunki:
   $$\begin{gathered}
A_i \cap A_j = \emptyset & dla & i\neq j
\end{gathered}$$
to
$$\begin{gathered}
P(A_1 \cup A_2 \cup \dots \cup A_n)=P(A_1)+P(A_2)+\dots +P(A_n)
\end{gathered}$$
3. Dla dowolnego zdarzenia $A$ zachodzi równość
   $$\begin{gathered}
P(A')=1-P(A)
\end{gathered}$$
4. Dla dowolnych zdarzeń $A$ i $B$ zachodzi równość
   $$\begin{gathered}
P(A\cup B)=P(A)+P(B)-P(A\cap B)
\end{gathered}$$
5. Jeśli $A \subset B$, to $P(A)\leq P(b)$
6. Jeśli zdarzenia $A_1,A_2,\dots$ tworzą **ciąg wstępujący**, tzn.
   $$\begin{gathered}
A_1\subset A_2 \subset A_3 \subset \dots \subset,
\end{gathered}$$
to
$$\begin{gathered}
P\left(\bigcup^\infty_{i=1}A_i\right)=\lim_{i\to \infty}P(A_i)
\end{gathered}$$
7. Jeśli zdarzenia $A_1,A_2,\dots$ tworzą **ciąg zstępujący** tzn.
   $$\begin{gathered}
A_1 \supset A_2 \supset A_3 \supset \dots
\end{gathered}$$
to
$$\begin{gathered}
P \left(\bigcap^\infty_{i=1}A_i\right)=\lim_{i\to \infty}P(A_i)
\end{gathered}$$
---
### Dowód własności 4 

($P(A\cup B)=P(A)+P(B)-P(A\cap B)$)

Zauważamy że
$$\begin{gathered}
A\cup B=A\cup (B\setminus A)
\end{gathered}$$
przy czym $A$ oraz $B\setminus A$ się wzajemnie wykluczają zatem można zastosować własność (2) czyli sume prawdopodobieństw niezależnych zatem:
$$\begin{gathered}
P(A\cup B)=P(A)+P(B\setminus A)
\end{gathered}$$
podobnie robimy dla B:
$$\begin{gathered}
B=(B\cap A)+(B\setminus A)
\end{gathered}$$
zatem:
$$\begin{gathered}
P(B)=P(B\cap A)+P(B\setminus A)\\
P(B\setminus A)=P(B)-P(A\cap B)
\end{gathered}$$
podstawiając otrzymujemy:
$$\begin{gathered}
P(A \cap B)=P(A)+P(B)-P(A\cap B)
\end{gathered}$$

---
### Zbiory przeliczalne

**Zbiorem przeliczalnym** nazywamy zbiór:
- **skończony** lub
- **nieskończony** ale taki, że istnieje odwzorowanie wzajemnie jednoznaczne tego zbioru na zbiór liczb naturalnych

#### Przeliczalna przestrzeń zdarzeń elementarnych $I$ 

Niech $\Omega$ będzie zbiorem przeliczalnym. Weźmy ciąg liczb rzeczywistych nieujemnych $p_i$ takich, że:
- jeśli $\Omega=\{\omega_1,\omega_2,\dots\}$ jest zbiorem nieskończonym to
  $$\begin{gathered}
\sum^{\infty}_{i=1}p_i=1
\end{gathered}$$
- jeśli $\Omega=\{\omega_1,\omega_2,\dots,\omega_N\}$ jest zbiorem nieskończonym to
  $$\begin{gathered}
\sum^{N}_{i=1}p_i=1
\end{gathered}$$

Zatem określając $\Sigma=2^\Omega$ to:
$$\begin{gathered}
P(A)=\Sigma\{p_k: \omega_k \in A\}
\end{gathered}$$
dla dowolnego $A \subset \Omega$.

---
### Konwencja oznaczeniowa

Jeśli $\{x\} \in \Sigma$, to będziemy pisać
$$\begin{gathered}
P(x)=P(\{x\})
\end{gathered}$$
W szczególności dla przeliczalnych przestrzeni probabilistycznych
$$\begin{gathered}
P(\omega_i)=P(\{\omega_i\})=p_i
\end{gathered}$$
