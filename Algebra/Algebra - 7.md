### Przestrzeń wektorowa ciąg dalszy - bazy, reper bazowy, sumy podprzestrzeni
#### 2024-11-10
##### Poprzednia: [[Algebra - 6]]
##### Następna: [[Algebra - 8]]
##### Zadania: [[]]

#baza_przestrzeni_wektorowej #algebra  

--- 
### Baza przestrzeni wektorowej:

#### Liniowa powłoka
*Def.* Niech $V$ będzie przestrzenią wektorową nad ciałem $K$. 
*Liniową powłoką* zbioru $A \subset V, A\neq \emptyset$, nazywamy zbiór:

$Lin \ A := \{v=\alpha_1v_1+\alpha_2v_2+...+\alpha_kv_k: \alpha_1, \alpha_2,...\alpha_k \in K, \ v_1,v_2,...,v_k \in A\}$

(Czyli zbiór wszystkich kombinacji liniowych wektorów ze zbioru $A$).

*Uw.*
$Lin \ A$ jest podprzestrzenią wektorową przestrzeni $V$ i nazywamy ją *(pod)przestrzenią generowaną przez zbiór $A$*.

---
#### Baza
*Def.*
Zbiór $B \subset V$ nazywamy *bazą przestrzeni wektorowej $V$*, jeżeli:
1. $Lin \ B = V$ (zbiór $B$ generuje całą przestrzeń $V$, czyli każdy wektor z $V$ daje się przedstawić jako kombinacja liniowa wektorów z $B$). $$\begin{gathered}
Wiemy \ ze: \ B \subset V \implies Lin \ B \subset V\\
I \ dodatkowo \ mowimy \ ze: \  V \subset Lin \ B\\
Wiec \ Lin \ B = V
\end{gathered}$$
2.  $\forall v_1, v_2, ..., v_k \in B: \{v_1, v_2, ..., v_k\}$ jest zbiorem wektorów *liniowo niezależnych*. (Jeżeli $B$ jest zbiorem skończonym, to ten warunek jest równoważny warunkowi: $B$ jest zbiorem wektorów liniowo niezależnych)
3. No i żeby nie pominąć założeń definicji przy zadaniach *B ZAWIERA SIĘ W V*

Ja to rozumiem tak że baza to minimalna ilość wektorów która generuje nam całą przestrzeń $V$.
*Wniosek:*
Zbiór $B\subset V$ jest bazą przestrzeni $V \Leftrightarrow$ każdy wektor $v \in V$ można w sposób jednoznaczny przedstawić w postaci kombinacji liniowej wektorów z $B$.

*Twierdzenie*
Niech $V$ będzie przestrzenią wektorową, $B \subset V$.
Następujące zdania są równoważne:
1. $B$ jest *bazą* przestrzeni $V$
2. $B$ jest *maksymalnym* (w sensie inkluzji - nie istnieje żaden zbiór różny od $B$ który zawierałby $B$ i byłby niezależny liniowo) No bo dodanie cokolwiek sprawi że to nie będzie liniowo niezależne, bo $B$ już generuje przecież całe $V$.
3. $B$ jest *minimalnym* (w sensie inkluzji) zbiorem wektorów *rozpinających* $V$: ($Lin B = V$) (Nie możemy pozbyć się żadnego wektoru bo wtedy nie będziemy gernerować całej przestrzeni $V$)

*Uw.*
Dla dowolnego zbioru *M liniowo niezależnego* w przestrzeni $V$, istnieje w $V$ *baza $B$* taka że $M \subset B$, oraz dla dowolnego zbioru *N rozpinającego* $V$, istnieje *baza* $B'$ przestrzeni $V$ taka, że $B' \subset N$. 

W sensie jak już mamy jakiś liniowo niezależny zbiór wektorów to możemy tam coś dorzucić i otrzymać baze. A jeśli mamy taki zbiór którego kombinacja generuje całą przestrzeń, ale jest liniowo zależny, to można usunąć jakiś wektor z niego i otrzymać baze.

*Def.* Niech $B$ będzie bazą przestrzeni wektorowej $V$.
1. Jeżeli $B$ jest zbiorem *skończonym* $(|B| \lt +\infty)$, to mówimy, że przestrzeń jest skończenie wymiarowa, a liczbę wektorów w bazie nazywamy *wymiarem* przestrzeni i oznaczamy *dimV* (np. dla $(\mathbb{R}^n, \mathbb{R},+,\cdot), \dim \mathbb{R}^n=n)$
2. Jeżeli baza $B$ składa się z *nieskończonej* liczby wektorów, to $V$ jest przestrzenią nieskończenie wymiarową i piszemy $\dim V = +\infty$ np. $(f(\mathbb{R}, \mathbb{R}),\mathbb{R},+,\cdot)$
3. Jeżeli $V=\{\overline{0}\}$, przyjmujemy $\dim V=0$

**Ważna** *uwaga* (wynikająca z poniższego przykładu dla bazy kanonicznej przestrzeni $\mathbb{R}^n$)
Jeżeli $V$  jest przestrzenią wektorową *wymiaru n* to:
- każdy zespół *n+1* wektorów jest liniowo *zależny* w $V$
- każdy zespół *n* wektorów które *generują* przestrzeń $V$ jest liniowo *niezależny* (więc stanowi *bazę* tej przestrzeni)
- każdy zespół *n* wektorów liniowo *niezależnych* w $V$ *generuje* przestrzeń $V$ (więc stanowi bazę tej przestrzeni)
###### Przykład $(\mathbb{R}^3, \mathbb{R}, +, \cdot)$ sprawdź czy baza.
$$\begin{gathered}
B=\{u=(3,2,-1), v=(1,-2,1), w=(1,1,1)\}\\
1. B \subset \mathbb{R}^3\\\\
2. Lin \ B \subset \mathbb{R}^3\\\land\\
t=(x,y,z) \in \mathbb{R}^3 - dowolnie \ ustalone \ t\\
\exists \alpha, \beta, \gamma \in \mathbb{R}: \alpha(3,2-1)+\beta(1,-2,1)+\gamma(1,1,1)=(x,y,z)\\
\Leftrightarrow\\
(3\alpha+\beta+\gamma, 2\alpha-2\beta+\gamma, -\alpha+\beta+\gamma)=(x,y,z)\\
\Leftrightarrow\\
\left\{
\begin{array}{1}
3\alpha+\beta+\gamma = x\\
2\alpha-2\beta+\gamma = y\\
-\alpha+\beta+\gamma=z 
\end{array}
\Rightarrow
\right.
\left\{\begin{array}{2}
\alpha =\frac{1}{4}x-\frac{1}{4}z\\
\beta =\frac{1}{4}x-\frac{1}{3}y+\frac{1}{12}z\\
\gamma =\frac{1}{3}y+\frac{2}{3}z\\
\end{array}
\right.
\Rightarrow\
istnieja \ \alpha, \beta, \gamma\\
\Leftrightarrow\\
Lin B=\mathbb{R}^3\\\\
3.Liniowa \ niezaleznosc\\
\alpha(3,2-1)+\beta(1,-2,1)+\gamma(1,1,1)=(0,0,0) \Leftrightarrow \alpha=\beta=\gamma=0\\
\Leftrightarrow\\
\left\{
\begin{array}{1}
3\alpha+\beta+\gamma = 0\\
2\alpha-2\beta+\gamma = 0\\
-\alpha+\beta+\gamma=0\\
\end{array}
\Rightarrow
\right.
\left\{\begin{array}{2}
\alpha =0\\
\beta =0\\
\gamma =0\\
\end{array}
\right. \Rightarrow LinB-liniowo \ niezalezne
\end{gathered}$$
---
### Reper bazowy i współrzędne wektora
*Def*. *Reperem bazowym* (a czasem po prostu bazą) danej przestrzeni wektorowej nazywamy dowolną jej bazę, w której ustaliliśmy kolejność wektorów.

*Def* Niech $B=(e_1,e_2,...e_n)$ będzie reperem bazowym przestrzeni wektorowej $V$ nad ciałem $K$. 
Dla dowolnego wektora $v=\alpha_1e_1+\alpha_2e_2+...+\alpha_ne_n \in V$, skalary $\alpha_1, \alpha_2,...,\alpha_n \in K$ nazywamy *współrzędnymi* wektora $v$ względem bazy $B$ (w bazie $B$) i stosujemy zapis $v=[\alpha_1, \alpha_2,...\alpha_n]_B$.

##### Przykładowe zadania

###### a) Znajdź współrzędne wektora $(4,4,8)$ względem bazy $B$.

Czyli tak naprawdę w poleceniu pytają nas o wyrażenie wektora $(4,4,8)$ za pomocą bazy $B$.
(Tak jak wyrażamy współrzędne punktu na płaszczyźnie, przy bazie $(u=(1,0), v=(0,1))$
$$\begin{gathered}
B=(u=(3,2,-1),v=(1,-2,1),w=(1,1,1))\\
\alpha(3,2,-1)+\beta(1,-2,1)+\gamma(1,1,1)=(4,4,8)\\
\left\{
\begin{array}{1}
3\alpha+\beta+\gamma = 4\\
2\alpha-2\beta+\gamma = 4\\
-\alpha+\beta+\gamma=8\\
\end{array}
\Rightarrow
\right.
\left\{\begin{array}{2}
\alpha =-1\\
\gamma=\frac{20}{3}\\
\beta=\frac{1}{3}\\
\end{array}
\right.\\
(4,4,8)=(-1)\cdot(3,2,-1)+\frac{1}{3}\cdot(1,-2,1)+\frac{20}{3}\cdot(1,1,1)\\
Czyli \ naszymi \ wspolrzednymi \ sa \ (\alpha=-1, \beta=\frac{1}{3}, \gamma=\frac{20}{3})\\
\end{gathered}$$
###### b) Znajdź wektor, którego współrzędne w bazie $B$ wynosza $1,-1,2$
$$\begin{gathered}
\ [1,-1,2]_B=1(3,2,-1)-1(1,-2,1)+2(1,1,1)=(3-1+2,2+2+2,-1-1+2)=(4,6,0)
\end{gathered}
$$

---
### Typowe bazy i ich oznaczenia:

*Def.* Przestrzeń $(\mathbb{R}^n, \mathbb{R}, +, \cdot)$ oznaczamy w skrócie $\mathbb{R}^n(\mathbb{R})$ (lub $\mathbb{R}^n$, a bazę tej przestrzeni: 
$B_k := (e_1=(1,0,....,0), e_2=(0,1,0...,0),...e_n=(0,0,...,0,1)))$ nazywamy *bazą kanoniczną*.

Tak jak $B_k:=(e_1=(1,0,0),e_2=(0,1,0),e_3=(0,0,1))$ wyznacza nam każdy punkt przestrzeni trójwymiarowej $(Lin B_k = \mathbb{R}^3)$
![[diagram-20241112.png]]
*Wniosek*
$\dim \mathbb{R}^n=n$

**Ważna** *uwaga*.
Jeżeli $V$  jest przestrzenią wektorową *wymiaru n* to:
- każdy zespół *n+1* wektorów jest liniowo *zależny* w $V$
- każdy zespół *n* wektorów które *generują* przestrzeń $V$ jest liniowo *niezależny* (więc stanowi *bazę* tej przestrzeni)
- każdy zespół *n* wektorów liniowo *niezależnych* w $V$ *generuje* przestrzeń $V$ (więc stanowi bazę tej przestrzeni)
###### Przykład:
Wiedząc że $B=(e_0(x)=1,e_1(x)=x, e_2(x)=x^2)$
$(e_i, \mathbb{R} \to \mathbb{R})$ jest (standardową) bazą w $\mathbb{R}[x]_2(\mathbb{R})=(\mathbb{R}[x]_2, \mathbb{R}, +, \cdot)$ sprawdź czy:
$B'=(w_0(x)=1+x^2, w_1(x)=x, w_2(x)=x-x^2)$ też jest bazą w $\mathbb{R}[x]_2$

Tutaj wystarczy sprawdzić czy te wektory są niezależne na mocy powyższej uwagi, 
($Dim B=3=|B'|$) wyjdzie nam wtedy rozpiętość na zbiór wielomianów co najwyżej stopnia drugiego co implikuje że będzie to baza.

Czy $\alpha(1+x^2)+\beta(x)+\gamma(x-x^2)=0 \Leftrightarrow \alpha=\beta=\gamma=0$?

$$
\begin{gathered}
\left\{\begin{array}{1}
\alpha\cdot 1=0\\
(\beta+\gamma)x=0\\
(\alpha-\gamma)x^2=0
\end{array}
\right.
\Rightarrow
\left\{\begin{array}{1}
\alpha=0\\
\beta=0\\
\gamma=0
\end{array}
\right.
\end{gathered}
$$
Tak, liniowo niezależne. Rozpinają nam też całą przestrzeń wektorów (wielomianów co najwyżej stopnia drugiego) zatem jest to baza.

---
*Twierdzenie*
Niech $V$ będzie przestrzenią *skończenie wymiarową* a $U$ jej podprzestrzenią. Wówczas:
- $dim U \leq  dim V$
- $dimU = dimV \Leftrightarrow U=V$

### Sumy podprzestrzeni

*Definicja*
*Sumą podprzestrzeni* $V_1, V_2$ przestrzeni wektorowej $V$ nazywamy zbiór:

$V_1+V_2=\{v\in V \ |\  \exists v_1 \in V_1\  \exists v_2 \in V_2: v=v_1+v_2\}=\{v_1+v_2: v_1\in V_2, \ v_2 \in V_2\}$
Czyli jest to zbiór sum wektorów (każdy z każdym).

Przykład:
$$
\begin{lgathered}
\begin{array}{#}
A=\{0,3\}\\
B=\{0,2,4\}
\end{array}
\ \ A+B=\{0,2,4,3,5,7\}
\end{lgathered}
$$

*Twierdzenie*
Jeżeli $V_1,V_2$ są podprzestrzeniami przestrzeni wektorowej $V$, to:
- $V_1+V_2$ jest podprzestrzenią przestrzeni V
- $V_1 \cap V_2$ jest podprzestrzenią przestrzeni $V$
