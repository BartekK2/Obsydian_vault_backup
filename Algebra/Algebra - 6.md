### Przestrzeń wektorowa - definicja, kombinacja liniowa, własności i twierdzenia
#### 2024-11-10
##### Poprzednia: [[Algebra - 5]]
##### Następna: [[Algebra - 7]]
##### Zadania: [[]]

#przestrzen_wektorowa #algebra  #kombinacja_liniowa #zaleznosc_i_niezaleznosc #podprzestrzen

--- 
### Definicja przestrzeni wektorowej:

*Def.* $V \neq \emptyset$ - *zbiór*, $(K, \oplus, \odot)$ - [[Algebra - 5#^dd2f3e|ciało przemienne]]
Ciało nie jest trywialne, $|K| \geq 2$ !!!

*+*: $V \times V \rightarrow V$ (*[[Algebra - 5#^a72f3a|Działanie wewnętrzne]]* w zb. V)
**$\cdot$** : $K \times V \rightarrow V$ (*[[Algebra - 5#^eb0a26|Działanie zewnętrzne]]* w zb. V)

Strukturę $(V, K, +, \cdot)$ nazywamy *przestrzenią wektorową (liniową) nad ciałem* K, jeżeli:
1. struktura $(V, +)$ jest grupą abelową
2. $\forall u,v \in V \ \forall \alpha \in K: \ \alpha \cdot (u+v) = (\alpha \cdot u) + (\alpha \cdot v)$
3. $\forall v \in V \ \forall \alpha, \beta \in K: \ (\alpha \odot \beta) \cdot v=\alpha \cdot (\beta \cdot v) \land (\alpha \oplus \beta) \cdot v = (\alpha \cdot v) + (\beta \cdot v)$
4. $\forall v \in V: 1\cdot v=v$ (gdzie 1 rozumiemy jako el. neutralny $\odot$)
Tutaj $V$ może być np. wektorami $R^3$ a $K$ liczbami, skalarami, to wyjaśnia różnice między działaniami "w kółku" i bez kółka.

Elementy zbioru $V$ nazywamy *wektorami*.
Elementy ciała $K$ nazywamy *skalarami*.

Element neutralny dodawania wektorów nazywamy *wekorem zerowym* i oznaczamy zazwyczaj $\overline{0}$.

*Uw.* Często zamiast przestrzeń wektorowa $(V, K, +, \cdot)$ piszemy w skrócie przestrzeń $V$ lub oznaczamy $V(K)$.

##### Klasyczny przykład przestrzeni wektorowej:
$(\mathbb{R}^3, \mathbb{R}, +, \cdot)$, gdzie 

$(x_1,y_1,z_2)+(x_2,y_2,z_2):=(x_1+x_2, y_1+y_2, z_1+z_2)$
$\alpha (x,y,z) := (\alpha x, \alpha y, \alpha z)$

($\mathbb{R}^3$ - wektory, $\mathbb{R}$ - skalary, $\oplus, \odot$ - zwykłe działania dodawania i mnożenia w $\mathbb{R}$, a $\overline{0}=(0,0,0)$)

##### Inne przykłady (oznaczenia):
$\mathbb{R}[x]_n$ - będzie oznaczało w przykładach z wielomianami wielomian stopnia *co najwyżej* n.
$\mathbb{R}[x]$ - oznacza zbiór wszystkich wielomianów rzeczywistych
Mogą być też przykłady z odwzorowaniami (funkcjami):
$(F(X, \mathbb{R}), \mathbb{R}, +, \cdot)$ - gdzie $F(X, \mathbb{R})$ będzie oznaczało odwzorowanie prowadzące z $X$ do $\mathbb{R}$

---
### Własności działań w przestrzeni wektorowej

*Uw.* Przez "$u-v$" rozumiemy "$u + (-v)$"
*Tw.*
Z: $(V, K, +, \cdot)$ - prz. wekt.
T: 
(1) $\forall v \in V: 0\cdot v=\overline{0}$ , gdzie $0$ rozumiem jako element neutralny d. add. w ciele (skalarów).
(2) $\forall \alpha \in K: \alpha \cdot \overline{0}=\overline{0}$
(3) $\forall \alpha \in K \ \forall v \in V: (-\alpha) \cdot v = -(\alpha \cdot v)$
(4) $\forall \alpha \in K \ \forall v \in V: \alpha \cdot (-v) = -(\alpha \cdot v)$
(5) $\forall \alpha \in K \ \forall v \in V: \alpha \cdot v = \overline{0} \Leftrightarrow (\alpha = 0 \vee v=\overline{0})$
(6) $\forall \alpha \in K \setminus \{0\} \ \forall u,v \in V: \alpha \cdot u = \alpha \cdot v \Rightarrow u=v$
(7) $\forall \alpha, \beta \in K \ \forall v \in V \setminus \{\overline{0}\}: \alpha  \cdot v = \beta \cdot v \Rightarrow \alpha = \beta$

---
### Podprzestrzenie wektorowe
*Def.* $(V,K, +, \cdot)$ - przestrzeń wektorowa
Zbiór $U \subset V, U \neq \emptyset$, nazywamy *podprzestrzenią wektorową (liniową)* przestrzeni $V$, jeżeli:
(1) $\forall u,v \in U: (u+v) \in U$, suma wektorów podprzestrzeni zostaje w tej podprzestrzeni
(2) $\forall \alpha \in K \ \forall u \in U: (\alpha \cdot u) \in U$, iloczyn wektora ze skalarem podprzestrzeni zostaje w tej podprzestrzeni

*Uw.* Każda podprzestrzeń danej przestrzeni wektorowej jest też przestrzenią wektorową.

*Prz.* $(\mathbb{R}^3, \mathbb{R}, +, \cdot)$ - przestrzeń wektorowej
$U:= \{(x,y,z) \in \mathbb{R}^3: x+y+z=0\}$

*Uw.* Wektor zerowy przestrzeni liniowej jest elementem każdej jej podprzestrzeni.
![[diagram-20241110 (2).png]]
#### Równoważna charakterystyka podprzestrzeni:

Z: $(V,K, +, \cdot)$ - przestrzeń wektorowa, $U \subset V, U \neq \emptyset$
T: $U$ jest podprzestrzenią liniową przestrzeni $V$
$\Leftrightarrow \forall \alpha, \beta \in K \ \forall u,v, \in U: \alpha \cdot u + \beta \cdot v \in U$

Bo przecież dla dowolnego $\alpha, \beta \in K$, i dowolnego $u,v \in U$:
$\alpha \cdot u \in U$, $\beta \cdot v \in U$ a suma dowolnych wektorów należących do $U$ też musi należeć do $U$ zatem:
$\alpha \cdot u + \beta \cdot v \in U$

---
### Liniowa niezależność wektorów, kombinacja liniowa

*Def.* Niech $V$ będzie przestrzenią wektorową nad ciałem $K$, $v_1,v_2,...,v_n \in V, \alpha_1, \alpha_2,..., \alpha_n \in K$
Wektor postaci $a_1 v_1+a_2 v_2+...+a_n v_n$ nazywamy *liniową kombinacją* wektorów $v_1, v_2, ..., v_n$ a skalary $\alpha_1, \alpha_2, ..., \alpha_n$ nazywamy jej *współczynnikami*.

*Def.* Niech $V$ bedzie przestrzenią wektorową nad ciałem $K$, 
$v_1, v_2, ..., v_n \in V$.

 1. Wektory $v_1,v_2,...,v_n$ nazywamy *liniowo niezależnymi*, jeżeli $\forall \alpha_1, \alpha_2,...,\alpha_n \in K$:
$\alpha_1v_1+\alpha_2v_2+...+\alpha_nv_n=\overline{0} \Rightarrow \alpha_1, \alpha_2,...,\alpha_n=0$
2. Wektory $v_1, v_2,..., v_n$ nazywamy *liniowo zależnymi*, jeżeli nie są liniowo niezależne, tzn., gdy $\exists \alpha_1, \alpha_2, ..., \alpha_n \in K$:  $\alpha_1v_1+\alpha_2v_2+...+\alpha_nv_n = \overline{0} \land (\alpha_1 \neq 0 \vee \alpha_2 \neq 0 \ \vee ... \vee \ \alpha_n \neq 0)$ Gdzie $0$ oznacza element neutralny działania addytywnego w ciele.
##### Przykład: $(\mathbb{R}^3, \mathbb{R}, +, \cdot)$ 
###### a)
$u=(0,1,1), \ v=(1,0,0), \ w=(1,1,1)$ 

Czy $\alpha \cdot u + \beta \cdot v + \delta \cdot w = \overline{0}$ wtedy i tylko wtedy kiedy $\alpha=\beta=\delta=0$ ? 

0 - el. neutralny działania + w $\mathbb{R}$ czyli po prostu 0
$\overline{0}$ - wektor zerowy z $\mathbb{R}^3$ czyli $(0,0,0)$ 

$$
\begin{gathered}
Zapis\\
\alpha \cdot u + \beta \cdot v + \delta \cdot w =\overline{0}\\
\Leftrightarrow\\
\alpha \cdot (0,1,1) + \beta\cdot(1,0,0) + \delta \cdot (1,1,1)=\overline{0}\\\\
Czyli:\\
(0,\alpha, \alpha) + (\beta,0,0) + (\delta, \delta, \delta) = (0,0,0)\\
(\beta+\delta, \alpha + \delta, \alpha + \delta) = (0,0,0)\\\\
\left\{
\begin{aligned}
\beta + \delta = 0\\
\alpha + \delta = 0\\
\alpha + \delta = 0\\
\end{aligned}
\right.
\Leftrightarrow
\left\{
\begin{aligned}
\beta = -\delta\\
\alpha  = - \delta\\
\delta \in \mathbb{R}
\end{aligned}
\right.
\Leftrightarrow
\left\{
\begin{aligned}
\beta = -t\\
\alpha  = -t\\
\delta =t
\end{aligned}
\right.
\\\\
Dla \ t = 3, \alpha =-3, \beta = -3, \delta = 3\\
oraz\\
\alpha \cdot u + \beta \cdot v + \delta \cdot w = \overline{0}\\\\
Liniowo \ zalezne \ (3 \neq el. \ neutralny).
\end{gathered}
$$

---
###### b)
$u=(3,2,-1), \ v=(1,-2,1), \ w=(1,1,1)$ 

Czy $\alpha \cdot u + \beta \cdot v + \delta \cdot w = \overline{0}$ wtedy i tylko wtedy kiedy $\alpha=\beta=\delta=0$ ? 

0 - el. neutralny działania + w $\mathbb{R}$ czyli po prostu 0
$\overline{0}$ - wektor zerowy z $\mathbb{R}^3$ czyli $(0,0,0)$ 
$$
\begin{gathered}
Zapis\\
\alpha \cdot u + \beta \cdot v + \delta \cdot w =\overline{0}\\
\Leftrightarrow\\
\alpha \cdot (3,2,-1) + \beta\cdot(1,-2,1) + \delta \cdot (1,1,1)=\overline{0}\\\\
Czyli:\\
(3\alpha,2\alpha, -\alpha) + (\beta,-2\beta,\beta) + (\delta, \delta, \delta) = (0,0,0)\\
(3\alpha+\beta+\delta, 2\alpha-2\beta+\delta,-\alpha+\beta+\delta) = (0,0,0)\\\\
\left\{
\begin{aligned}
3\alpha+\beta+\delta= 0\\
2\alpha-2\beta+\delta = 0\\
-\alpha+\beta+\delta = 0\\
\end{aligned}
\right.
\Leftrightarrow
\left\{
\begin{aligned}
4\alpha = 0\\
\beta+\delta=0\\
2\beta+\delta=0\\
\end{aligned}
\Rightarrow
-3\beta = 0\\
\right.
\Leftrightarrow
\left\{
\begin{aligned}
\alpha = 0\\
\beta  = 0\\
\delta =0
\end{aligned}
\right.
\\\\
\alpha \cdot u + \beta \cdot v + \delta \cdot w = \overline{0} \Leftrightarrow (\alpha=\beta=\delta=0)\\\\
Liniowo \ niezalezne \ (0 = el. \ neutralny).
\end{gathered}
$$


---
##### Twierdzenie 
Niech $V$ będzie przestrzenią wektorową nad ciałem $K$, $v_1,v_2,...,v_n \in V$. Wówczas wektory $v_1,v_2,...,v_n$ są *liniowo zależne* wtedy i tylko wtedy, gdy przynajmniej *jeden* z nich jest *kombinacją liniową pozostałych* (lub $\{v_1,....v_n\} = \{\overline{0}\}$).

###### Dowód:
Dla $n \geq 2$
$(\Rightarrow) v_1,...,v_n$ - liniowo zależne $\ \stackrel{b.s.o}{\Rightarrow} \exists \beta_1,...,\beta_n \in K: \beta_1v_1+...\beta_nv_n=\overline{0} \land \beta_1 \neq 0$
$\beta_1v_1 = -(\beta_2v_2+...+\beta_nv_n)$
$v_1=-(\beta_1^{-1}\beta_2v_2 +....+\beta_1^{-1}\beta_nv_n) \rightarrow v_1$ jest kombinacją liniową pozostałych wektorów

$(\Leftarrow) \exists \alpha_2,...,\alpha_n \in K: v_1=\alpha_2 v_2 + ... + \alpha_n v_n$
$\Rightarrow \stackrel{1\neq 0}{1}\cdot v_1 + (-\alpha_2)v_2 + ... + (-\alpha_n)v_n = \overline{0} \rightarrow v_1,...v_n$ - liniowo zależne ($1\neq 0$ a z definicji żeby wektory były liniowo niezależne to mają dać wektor zerowy wtedy i tylko wtedy kiedy skalary są równe 0)
Jedynke traktujemy jako jedynke działania multiplikatywnego (el. neutralny) zatem nie wiemy czy jest równy czy różny skalarowi równemu elementowi neutralnemu działania addytywnego)
Jeżeli jest różny to jak wyżej a jeżeli równy to:
$1=0 \ v \in K$
$v=1\cdot v = (1+0)\cdot v=(1+1)\cdot v=1\cdot v + 1\cdot v = v+v /+(-v)$
$0=v \implies |K| = 1$ - sprzeczne z założeniami przestrzeni wektorowej

##### Uwagi i wnioski :
*Uwagi:*
1. Zbiór $\{v\}$ jest liniowo niezależny wtedy i tylko wtedy, gdy $v\neq \overline{0}$
2. Podzbiór zbioru wektorów liniowo niezależnych jest liniowo niezależny

*Wnioski.*
1. Jeżeli wektory są liniowo niezależne, to żaden z nich nie jest kombinacją liniową pozostałych.
2. Zespół wektorów: $v_1,v_2,...,\overline{0}, ..., v_n$ jest liniowo zależny
3. Dla dwóch wektorów, $u,v \ u\neq \overline{0}$:  $u,v$ są liniowo zależne $\Leftrightarrow \exists \alpha \in K: v=\alpha u$

##### Twierdzenie
Niech $v_1,v_2,...,v_n$ będą *liniowo niezależnymi* wektorami z przestrzeni wektorowej V. Wówczas, jeżeli wektor $v \in V$ jest *kombinacją liniową* wektorów $v_1,v_2,...,v_n$ to współczynniki tej kombinacji sa wyznaczone *jednoznacznie* (z dokładnością do kolejności).
tzn jeżeli:
$$\begin{gathered}
v=\alpha_1v_1+\alpha_2v_2+...+\alpha_n v_n\\
v=\beta_1v_1+\beta_2v_2+...+\beta_n v_n\\
to\\
\alpha_1=\beta_1 \land ... \land \alpha_n = \beta_n
\end{gathered}
$$

---
Ciąg dalszy w [[Algebra - 7]]