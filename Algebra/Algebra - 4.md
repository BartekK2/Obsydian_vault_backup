### Relacje
#### 2024-10-15
##### Poprzednia: [[Algebra - 3]]
##### Następna: [[Algebra - 5]]
##### Zadania: [[Algebra - relacje]]

#relacje #algebra  

---
### Relacje

*Def.*
Uporządkowaną trójkę $R = (X, grR, Y)$ gdzie $X, Y$ są zbiorami, a $grR \subset X \times Y$, nazywamy *relacją* (dwuargumentową) określoną między elementami zbiorów $X$ i $Y$ (lub  w zbiorze $X$, gdy $Y=X$):
- $X$ nazywamy *naddziedziną*
- $Y$ nazywamy *zapasem*
- $grR$ nazywamy *wykresem* relacji
Elementy $x \in X, \ y \in Y$ *są ze sobą w relacji* $R: \leftrightarrow (x,y) \in grR$ - co zapisujemy $xRy$.

*Dziedziną* relacji $R$ nazywamy zbiór:
$D_R := \{x \in X: \exists y\in Y: xRy\}$
*Przeciwdziedziną* relacji $R$ nazywamy zbiór:
$D^{-1}_R := \{y \in Y: \exists x \in X : xRy\}$

*Prz.*
$X=[1,3], \ Y=[1,3], \ grR=\{(x,y) \in X \times Y : x\leq y\}$
![[diagram-20241015 (4).png]]
*Prz. 2*
$S=(\mathbb{R}, grS, \mathbb{R}), \ grS = \{(x,y) \in \mathbb{R}^2: y\geq x^2\}$
![[diagram-20241015 (3).png]]
Tutaj dziedziną będzie $D_S=\mathbb{R}$, a przeciwdziedziną $D^{-1}_S = [0,+\infty]$.

*Def.*
*Relacją odwrotną* do relacji $R=(X, grR, Y)$ nazywamy relację $R^{-1}=(Y, grR^{-1}, X)$, gdzie: $grR^{-1} := \{(x,y) \in Y \times X: (y,x) \in grR\}$. 

*Prz.*
$S^{-1} = (\mathbb{R}, grS^{-1}, \mathbb{R})$ 
$grS^{-1} = \{(x,y) \in \mathbb{R}^2: (y, x) \in grS\}=\{(x,y)\in \mathbb{R}^2: x\geq y^2\}$ (x nam się zamienił z y - wcześniej warunek był $y\geq x^2$ a teraz $x \geq y^2$). 
![[diagram-20241015 (5).png]]
Jest to ten sam wykres co przy $S$ ale odbity względem prostej $y=x$. 

Innymi słowy:
Jeżeli mamy jakąś relacje $T$ gdzie $grT$ mówi nam o tym że $x$ jest dzieckiem $y$ to: relacja $T^{-1}$ czyli relacja odwrotna ma takie $grT^{-1}$ że $y$ jest dzieckiem $x$  ($x$ jest rodzicem $y$).

---
### Złożenie relacji:

*Def.*
*Złożeniem relacji* $R = (X, grR, Y)$ z relacją $S=(Y, grS, Z)$ nazywamy relację:
$$ S \circ R := (X, gr(S\circ R), Z)$$
gdzie:
$$ gr(S \circ R):= \{(x,z) \in X \times Z: \exists y \in Y: xRy \land ySz\}$$ *Prz.*
$R=(\mathbb{N}, grR, \mathbb{N})$
$grR = \{(2,1), (3,1), (4,2), (4,5), (5,3)\}$

$S=(\mathbb{N}, grS, \mathbb{N})$
$grS=\{(1,3), (4,1), (3,6), (6,8), (6,7)\}$

$S\circ R=(\mathbb{N}, gr(S \circ R), \mathbb{N})$
$gr(S \circ R) = \{(2,3), (3,3), (5,6)\}$

---
### Relacja równoważności:
*Ozn.*
Przez $(X, R)$ oznaczamy zbiór $X$ z relacją $R$, gdzie $R=(X, grR, X)$. 
*Def.*
Relację $R = (X, grR, X)$ nazywamy relacją równoważności, gdy:
1. $R$ jest *zwrotna*: $\leftrightarrow \forall x \in X: xRx$ (wszystkie elementy z $X$ występują w parze) ^53547f
2. $R$ jest *symetryczna*: $\leftrightarrow \forall x,y \in X: xRy \implies yRx$ ^b88635
3. $R$ jest *przechodnia*: $\leftrightarrow \forall x,y,z \in X: xRy \land yRz \implies xRz$  ^59d1e6

*Prz.*
$X=\mathbb{R}^2: (x_1,y_1)R(x_2,y_2): \leftrightarrow x_1^2+y_1^2=x_2^2+y_2^2$
(W tym przykładzie naszą naddziedziną a zarazem zapasem jest płaszczyzna $\mathbb{R}^2$, zatem relacje mamy pomiędzy punktami a nie np: x,y)
![[diagram-20241016 (2).png]]
Ten przykład jest idealnym przykładem relacji równoważności, mówi nam o tym że tworzymy relacje między punktami których odległość od środka układu współrzędnych jest taka sama. Czyli na tym przykładowym kole każdy punkt jest z każdym innym w relacji zatem:
1. $R$ jest zwrotna bo punkt jest sam ze sobą w relacji.
2. $R$ jest symetryczna bo jeżeli $(x_1,y_1)$ jest w relacji z $(x_2,y_2)$ to $(x_2,y_2)$ jest w relacji z $(x_1,y_1)$.
3. $R$ jest przechodnia, bo jeżeli $(x_1,y_1)$ jest w relacji z $(x_2,y_2)$ a $(x_2,y_2)$ jest w relacji z $(x_3,y_3)$ to punkt $(x_1,y_1)$ musi być w relacji także z punktem $(x_3,y_3)$. (tworzy się nam taki "łańcuszek relacyjny")

##### Klasa równoważności
*Def.*
Jeżeli $(X,R)$ jest zbiorem z relacją równoważności i $x \in X$, to *klasą równoważności / abstrakcji* elementu x nazywamy zbiór:
$$[x]:=\{y \in X: xRy\}$$
Zbiór wszystkich y w których x jest w relacji.
Każdy element $y \in [x]$ nazywamy *reprezentantem* tej klasy.
(Czyli dla powyższego przykładu klasą równoważności punktu np $(x_1,y_1)$ jest cały tamten okrąg)

##### Zbiór ilorazowy
*Def.* 
Zbiór klas równoważności relacji $R$ nazywamy *zbiorem ilorazowym* i oznaczamy $X/_R$. Zatem $X/_R:=\{[x]: x \in X\}$

*Twierdzenie.*
Z: $(X, R)$ - zbiór. z relacją równoważności
1. $\forall x \in X: [x] \neq \emptyset$ (wynika z [[Algebra - 4#^53547f|zwrotności]] tzn. $[x]$ musi zawierać przynajmniej samego siebie)
2. $\forall x,y,z \in X: y \in [x] \land z \in [x] \implies yRz$ - wynika z [[Algebra - 4#^59d1e6|przechodniości]] 
3. $\forall x,y \in X: [x] \neq [y] \leftrightarrow [x] \cap [y] = \emptyset$ - wynika z [[Algebra - 4#^b88635|symetryczności]]
4.  $X - \bigcup_{x\in X} [x]$  - oczywiście po dodaniu każdej klasy abstrakcji dostaniemy całą naddziedzinę bo dla każdego $x$ klasa abstrakcji to co najmniej $\{x\}$

*Czyli klasy abstrakcji dzielą nam zbiór $X$ na podzbiory niepuste, rozłączne, dające w sumie cały zbiór $X$.*

---
### Zbiory uporządkowane
*Def.* Dla danego zbioru z relacją $(X, R)$, mówimy że:

4. $R$ jest *antysymetryczna*: $\leftrightarrow \forall x,y \in X: xRy \land yRx \implies x=y$ ^be0cb2
5. $R$ jest *asymetryczna* $\leftrightarrow \forall x,y \in X: xRy \implies \sim  yRx$
6. $R$ jest *spójna*: $\leftrightarrow \forall x,y \in X: xRy \vee yRx \vee x=y$  ^6310b2

*Def.* Relacja $R$ określona w zbiorze $X$ nazywana jest *porządkiem* lub relacją *słabego porządku (częściowego)*, jeżeli jest [[#^53547f|zwrotna]], [[#^be0cb2|antysymetryczna]] i [[#^59d1e6|przechodnia]]. Wówczas $X$ nazywamy zbiorem (częściowo) uporządkowanym (przez $R$). Jeżeli $R$ jest dodatkowo [[#^6310b2|spójna]], to nazywamy ją relacją porządku *totalnego* albo *liniowego*, a zbiór $X$ nazywamy uporządkowanym totalnie (liniowo).

Dodatkowo jeżeli $(X, \leq)$ - zbiór uporządkowany:
$\forall x,y \in X: x \leq y: \leftrightarrow (x \leq y \land x \neq y)$ Czyli elementy nie mogą być w relacji z samymi sobą - Relacja ta jest nazywana *silnym porządkiem* w $X$ (jest asymetryczna i przechodnia).

Elementy $x,y \in X$ nazywamy *porównywalnymi*, jeżeli: $xRy \vee yRx$. 

*Uw.* Jeżeli relacja $R$ porządkuje $X$ i $A \subset X$ to zbiór A jest również uporządkowany przez $R$. ($R|_{A\times A}$)

*Przykład* takiego porządku to po prostu taka relacja $(R, \leq)$ która przyporządkowuje każdemu elementowi mniejsze bądź równe elementy. 
"Bądź równe" - zatem jest zwrotność.
Antysymetryczność również tu działa $a\leq b \land b\leq a \Leftrightarrow a=b$. 
Przechodnia oczywiście też bo jeśli $a \leq b \land b\leq c \implies a\leq c$ 
No i spójność bo w ten sposób można porównać każdą liczbę.
Zatem jest to relacja liniowego porządku.

Inny popularny przykład to $(2^{R^2}, \subset)$ gdzie $2^{R^2}$ oznacza zbiór podzbiorów płaszczyzny. *Ale nie będzie to wtedy porządek liniowy* bo możemy mieć takie podzbiory które się w sobie nie zawierają (ani pierwszy w drugim ani drugi w pierwszym, zatem nie ma relacji pomiędzy każdym elementem).

Rysunek dla zwizualizowania:
![[diagram-20241023.png]]

---
### Elementy wyróżnione zbioru uporządkowanego

#### Elementy max/min, najw/najm

*Def.* $(X, \leq)$ - zbiór uporządkowany (nieoficjalny zapis tylko po to żeby go teraz użyć)

1. Element $\overline{M} \in X$ nazywamy *elementem największym* zbioru $X$: $\leftrightarrow \forall x \in X: x \leq \overline{M}$.
2. Element $\overline{m} \in X$ nazywamy *elementem najmniejszym* zbioru X: $\leftrightarrow \forall x \in X: \overline{m} \leq x$.
3. Element $M_{max} \in X$ nazywamy *elementem maksymalnym* zb. $X$: $\leftrightarrow \forall x \in X: (M_{max} \leq x) \implies (M_{max} = x)$.
4. Element $m_{min} \in X$ nazywamy *elementem minimalnym* zb. $X$: $\leftrightarrow \forall x \in X: (x \leq m_{min}) \implies (m_{min} = x)$.

Innymi słowy element największy/najmniejszy to taki który jest w relacji z *każdym* elementem bądź *każdy* element jest w relacji z nim.
A element maksymalny/minimalny to taki dla którego nie jest w relacji z *żadnym* innym elementem poza sobą lub *żaden* nie jest z nim poza sobą.

---
#### Łańcuch 

Podzbiór $C \subset X$ nazywamy *łańcuchem*, jeżeli $(C, R|_{C \times C})$ jest zbiorem liniowo uporządkowanym.

(np. $C=\{1,2,4,8 \}) \subset B, \ gdzie \ B=\{1,2,3,4,5,6,7,8\}, \ grB: \forall x,y \in B: x\leq y$)

Czyli po prostu dowolny poukładany podzbiór zbioru, poukładany według tej samej techniki (wykresu $grB$).

---
#### Majoranty i minoranty

1. Element $M \in X$ nazywamy *majorantą* zbioru $A$: $\leftrightarrow \forall x \in A: x \leq M$.
2. Element $m \in X$ nazywamy *minorantą* zbioru $A$: $\leftrightarrow \forall x \in A: m \leq x$.

gdzie: $(X, \leq)$ - zbiór uporządkowany $A \subset X$

*WAŻNE* - zauważ że majoranta/minoranta należy do $X$ ale jest sprawdzana ($\leq$) tylko dla tego podzbioru ($A$). Zatem tych majorant/minorant może być nieskończenie wiele. Tak dla zobrazowania to jest coś w stylu jak ograniczenie ciągu, nad/pod granicą można również ustawić "granice".

*Def.* Jeżeli zbiór $A$ posiada co najmniej jedną majorantę (minorantę), to mówimy, że jest on ograniczony od góry (lub od dołu). Jeżeli ma i minorante i majorantę, mówimy że jest ograniczony. 

---
### Kres górny i dolny

1. *Kresem górnym* zbioru $A$ (w zbiorze $X$) nazywamy, o ile istnieje - element najmniejszy zbioru majorant i oznaczamy to: $sup A$. 
2. *Kresem dolnym* zbioru $A$ (w zbiorze $X$) nazywamy, o ile istnieje - element największy zbioru minorant i oznaczamy jako: $inf A$.

*Prz.* $(\mathbb{R}, \leq), \ A=[-1,5)$
![[diagram-20241023 (1).png]]

---
### Funkcja jako przykład relacji:

*Funkcja* przekształcająca zbiór. $X$ w zbiór. $Y$ definiowana jest jako relacja $(X, grR, Y)$, która jest prawostronnie jednoznaczna, to znaczy:

$\forall x \in X \ \  \forall y, z \in Y: \ (xRy \land xRz) \implies y=z$

Innymi słowy jednemu argumentowi (x) możemy przypisać tylko jedną wartość (y). Ale nie na odwrót to znaczy z powyższego nie wynika że (y) może mieć tylko jednego (x). 

Wówczas możemy sobie normalnie napisać $f(x)=y$, zamiast $xRy$. 