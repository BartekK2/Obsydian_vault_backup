##### Lekcja: [[Algebra - 4]]
#algebra  #relacje  
###### 2024-10-16

#### Z ćwiczeń:

---
###### 1)
$$\begin{gathered}
Tw. R=(A,grR,A)\\\\
Z: R \ - \ zwrotna, \forall a \in A: aRa\\
T:R=R\circ R \leftrightarrow R \ - \ przechodnia, \forall a,b,c \in A: (aRb \land bRc \implies aRc) \\
D: (\implies) \ zakl. \ ze \ R \ - \ zwrotna \ i \ zakl. \ ze \ R\circ R = R \\
[\forall (a,b) \in A \times A: ((a,b) \in R\circ R \leftrightarrow (a,b)  \in R )]\\\\
Mam \ pokazac \ ze \ wtedy \ R \ - \ przechodnia \ czyli: \forall a,b,c \in A: (aRb \land bRc \implies aRc)\\
Niech  \ \ a,b,c \in A \ beda \ dowolnie \ ustalone \ i \ zakladam, \ ze \ aRb \land bRc \leftrightarrow (a,c) \in R  
\end{gathered}$$

Dowód równoważności:
$(p\leftrightarrow q) \leftrightarrow (p\implies q \land q \implies p)$

---
###### 2. Wykaż że dla zbioru $X$ z relacją $R$: $R$ jest relacją równoważności $\leftrightarrow R^{-1}$ jest relacją równoważności.

$$\begin{gathered}
Z: R - \ relacja \ rownowaznosci\\\\
zatem:\\
1. \ \forall x \in A: xRx \\
2. \ \forall x,y \in A: xRy \implies  \ yRx\\
3. \ \forall x,y,z \in A: xRy \ \land \ yRz \implies xRz \\\\

\forall (x,y): (x,y) \in R \ \implies  (y,x) \in R^{-1}\\
Zatem\\
\forall x: xRx \land  xR^{-1}x\\
\\
\forall (x,y) \in R \implies (y,x) \in R \ \land (y,x) \in R^{-1}\\
\forall (y,x) \in R \implies (x,y) \in R \ \land (x,y) \in R^{-1}\\
wiec\\
\forall (x,y) \in R^{-1} \implies (y,x) \in R^{-1}\\
\\
yR^{-1}x  \ \land zR^{-1}y \implies zR^{-1}x \\

Dowod \ w \ przeciwna \ strone \ gdzie \ na \ poczatku \ zakladamy \\
ze \ to \ R^{-1} \ jest \ rownowazne \ i \ udowadniamy \ ze \ wtedy \ R \ tez \ jest \ przebiega \ analogicznie 
\end{gathered}$$

---
###### 3. Wykaż że jeżeli relacja $R$ określona w zbiorze $X$ jest zwrotna i przechodnia to $R \cap R^{-1}$ określa relację równoważności.

$$\begin{gathered}
S=R \cap R^{-1} \\
S=\{\forall (x,y): (x,y) \in R \ \land (x,y) \in R^{-1}\}\\
gdzie \\
(x,y) \in R^{-1} \implies (y,x) \in R\\
wiec\\
S=\{\forall (x,y): (x,y) \in R \ \land (y,x) \in R\} \ - \ symetryczna 
\\\\
Mamy \ z \ zal. \ ze \ zwrotna \ i \ przechodna \ a \ teraz \ udowodnilismy \ symetrycznosc.\\
Wiec \ \ S=R \cap R^{-1} - rownowazna 

\end{gathered}$$
---
#### Zbiór zadań:
###### 1. 
$$\begin{gathered}
grR = \{(1,1), (1,2), (3,2), (3,4), (3,7), (2,9), (5,3)\}\\
grS = \{(1,2),(1,7),(2,5),(2,4),(7,9),(4,10)\}\\\\
D_R = \{1,3,2,5\}\\
D^{-1}_R = \{1,2,3,4,7,9\}\\\\
D_S=\{1,2,7,4\}\\
D^{-1}_S = \{2,7,5,4,9,10\}
\\\\
grR^{-1}=\{(1,1),(2,1),(2,3),(4,3),(7,3),(9,2),(3,5)\}\\
grS^{-1}=\{(2,1),(7,1),(5,2),(4,2),(9,7),(10,4)\}\\
\\\\
gr(S^{-1} \circ R^{-1})=\{(9,1),(3,2)\}\\
gr(R \circ S)=\{(1,9),(2,3)\}\\
gr(R \circ S)^{-1}=gr(S \circ R)=\{(9,1),(3,2)\}\\
\end{gathered}$$

$$\begin{gathered}
Sprawdz \ ze:\\
S^{-1} \circ R^{-1} = (R \circ S)^{-1}\\\\
S^{-1} \circ R^{-1} = \{(9,1),(3,2)\}\\
(R \circ S)^{-1} = \{(1,9),(2,3)\}^{-1} = \{(9,1),(3,2)\}
\end{gathered}$$ ---
###### 2. 

Dana jest relacja: $R=(A, grR, B)$ 
Z: $grR^{-1} \subset grR$
T: $grR^{-1} = grR$
D: mam pokazać, że $grR^{-1} \subset grR \land grR \subset grR^{-1}$, gdzie $grR^{-1} \subset grR$ wiemy z założenia. Zatem musimy udowodnić tylko drugą część.
Mam pokazać że, $\forall (a,b) \in A\times B: ((a,b) \in grR \implies (a,b)\in grR^{-1})$
Gdzie założenie innymi słowami mówi że: $\forall (b,a) \in B\times A: ((b,a) \in grR^{-1} \implies (b,a) \in grR)$

Niech $(a,b) \in A \times B$ będzie dowolnie ustalone i zakładam, że $(a,b) \in grR \leftrightarrow (b,a) \in grR^{-1} \implies \ (z \ zal.) \ (b,a)\in grR \leftrightarrow \ (z \ def \ R^{-1}) (a,b) \in grR^{-1}$ 

Dana jest relacja $R=(A, grR, A)$ mówimy, że $R$:
1. $R$ - jest zwrotna $\leftrightarrow \forall a \in A: aRa$
2. $R$ - jest symetryczna $\leftrightarrow \forall a,b \in A: (aRb \implies bRa)$
3. $R$ - jest przechodniościowa $\leftrightarrow \forall a,b,c \in A: (aRb \land bRc \implies aRc)$

---
###### 3)
$$\begin{gathered}
R=(\mathbb{N}^2, grR, \mathbb{N}^2): (a,b)R(c,d) \Leftrightarrow a+d=b+c\\
Tw.: R-rownowaznosc\\
1.R-zwrotna\\
\forall a,b: a+b=a+b:=(a,b)R(a,b)\\
2. R-symetryczna:
\forall (a,b),(c,d): a+d=b+c\  \land  \ c+b=d+a \\:= (a,b)R(c,d) \implies (c,d)R(a,b)\\
3. R-przechodnia:
\forall (a,b), (c,d), (x,y) \in \mathbb{N}^2: ((a,b)R(c,d) \ \land \ (c,d)R(x,y) \\ \implies (a,b)R(x,y)\\
(a+d=b+c \ \land \ c+y = d+x) \implies a+y=b+x\\
(a-b=c-d \ \land \ c-d=x-y) \implies a-b=c-d 
\end{gathered}$$


---
###### 4. Niech $k \in \mathbb{N}_{+}$. W zbiorze $\mathbb{Z}$ wprowadzamy relację $m \equiv n(mod k) \leftrightarrow k|(m-n)$. Wykaż że relacja ta jest równoważnością. Zbiór ilorazowy tej relacji będziemy ozaczać przez $\mathbb{Z}/k$. Przyjmującc $k=7$ podaj:

$$\begin{gathered}
(zapis \ \ m\equiv n(mod \ k ) \ oznacza \ ze \ m \ i \ n \ daja \ ta \ sama \ reszte \ z \ dzielenia \ przez \ k)\\\\
R=(\mathbb{Z}, grR), \  grR=\{\forall m,n \in \mathbb{Z}: m\equiv n(mod \ k)\}\\
m \equiv n(mod \ k) \Leftrightarrow \exists \ q \in \mathbb{Z}: m-n=k \cdot q\\\\
Dowod \ rownowaznosci:\\
1. \forall m \in \mathbb{Z}: mRm \ bo \ m-m=k\cdot 0\\
Zwrotnosc \ spelniona \ \forall m \in \mathbb{Z}: mRm\\\\
2. \forall m,n: m-n=k\cdot q \implies n-m =k\cdot (-q)\\
innymi \ slowy \ jesli \ m \ i \ n \ daje \ ta \ sama \ reszte \ to \ n \ i \ m \ oczywiscie \ tez \\
Symetrycznosc \ spelniona \ \forall m,n \in \mathbb{Z}: mRn \implies nRm\\\\

3. \forall n,p, m: nRp \land pRm \Leftrightarrow n-p=k\cdot q\ \land \ p-m=k\cdot q', \ \  q,q' \in \mathbb{Z} \implies \\
\implies n-m=(n-p)+(p-m)=k\cdot(q+q'), \ \ q+q' \in \mathbb{Z} \Leftrightarrow nRm\\
Przechodnosc \ spelniona \ \forall n,p,m \in \mathbb{Z}: nRp \land pRm \implies nRm 

\end{gathered}$$

Wykazaliśmy że jest równoważnością.

---
###### $[2], [5], [-5]$ (klasy równoważności przyjmując $k=7$), $\mathbb{Z}/7$ 
$$\begin{gathered}
\ [2] = \{7k+2: k \in \mathbb{Z}\}\\
\ [5] = \{7k+5: k \in \mathbb{Z}\}\\
\ [-5] = [5] = \{7k+2: k \in \mathbb{Z}\}\\\\
\mathbb{Z}/7 =\{[0],[1],[2],...,[6]\}
\end{gathered}$$

---
###### 5. Dane jest odwzorowanie $f: \mathbb{R} \rightarrow \mathbb{R}$ takie że $f(x)=x^3-3x +2$. Niech $S=(\mathbb{R}, grS, \mathbb{R})$ będzie relacją taką, że $grS = \{(x,y): f(x)=f(y)\}$.

###### a) Wykaż, że $S$ jest relacją równoważności:

$$\begin{gathered}
1. \forall x \in \mathbb{R}: f(x)=f(x) \implies \forall x \in \mathbb{R} \ \ xRx\\
2. \forall x,y \in \mathbb{R}: (f(x)=f(y) \Leftrightarrow f(y)=f(x)) \Leftrightarrow (xRy \Leftrightarrow yRx)\\
3. \forall x,y,z \in \mathbb{R}: \ \  [f(x)=f(y) \land f(y)=f(z) \implies f(x)=f(z) ] \Leftrightarrow [xRy \land yRz \implies xRz] 
\end{gathered}$$

###### b) Niech $a \in \mathbb{R}$. Określ w zależności od $a$ liczność klasy równoważności $[a]$. 

$$\begin{gathered}
f(x) =x^3-3x+2\\
f(x) = (x-1)(x^2+x-2)=(x-1)(x-1)(x+2)=(x-1)^2(x+2)\\
x_1=1 \ \ (dwukrotny ), \ \ x_2=-2 
\end{gathered}$$
![[diagram-20241026 (1).png]]
$$\begin{gathered}
\ [a]=1, \ \ a\lt -2 \ \ (bo \ z \ samym \ soba)\\
\ [a]=2, \ \ a\in \{-2,1 \}\\\\

f'(x) = 3x^2-3=0\\
x^2=1, \ \ x=1 \ \vee \ x=-1\\
[a]=2, \ a\in \{-1,1\}\\
[a]=3, \ a\in (-2,1) \setminus \{-1\}\\
[a]=1, \ a\in (1, +\infty)
\end{gathered}$$
---

###### Niech $R=(\mathbb{R}^2, grR, \mathbb{R}^2)$, gdzie: $(x,y)R(x',y') \leftrightarrow x\leq x' \ \land \ y \leq y'$. 
###### a) Wykaż, że $R$ jest relacją porządku. Czy ten porządek jest liniowy?
$$\begin{gathered}
1. \forall (x,y) \in \mathbb{R}^2 \ \ x \leq x \ \land \ y\leq y \implies \forall (x,y) \in \mathbb{R}^2 (x,y)R(x,y) \\\\
2. \forall (x,y),(x',y') \in \mathbb{R}^2: \ \ (x\leq x' \land x'\leq x) \ \land \ (y \leq y' \ \land \ y' \leq y) \implies (x=x' \ \land \ y=y') \Leftrightarrow\\ \Leftrightarrow (x,y)= (x',y')\\
\forall (x,y), (x',y') \in \mathbb{R}^2: (x,y)R(x',y') \land (x',y')R(x,y) \implies (x,y)=(x',y')\\\\
3. \forall (x,y), (x',y'), (x'',y'') \in \mathbb{R}^2: (x\leq x' \land y\leq y') \ \land \ (x'\leq x'' \ \land \ y'\leq y'') \implies \\
\implies x\leq x'' \land y\leq y'' \\
\forall (x,y), (x',y'), (x'',y'') \in \mathbb{R}^2: (x,y)R(x',y') \land (x',y')R(x'',y'') \implies (x,y)R(x'',y'')\\\\
Nie \ jest \ spojny \ bo \ moze \ byc \ tak \ ze \ np. \ tylko \ x \ mniejszy \ a \ y \ wieksze:\\
(3,4), (4,2) \ \ \neg \ (3,4)R(4,2) \ \land \ \neg \ (4,2)R(3,4) \ \land \ \neg \ (4,2)=(3,4)
\end{gathered}$$

###### b) Znajdź zbiory minorant i majorant oraz kresy zbiorów $A=\{(1,2), (3,1)\}$, $B=\{(x,y): x^2+y^2 \leq 9 \}$.

*Dla przypomnienia:*
W relacji $(M, \leq)$ 

- Majoranty to takie elementy $M \in X: \ \forall x \in A: x\leq M$. Czyli taki element, który jest "większy" od każdego z elementów w $A$  (to znaczy w relacji $xRy$ jest tym $y$ dla każdego $x$ w $A$)
- Minoranty to takie elementy $m \in X: \forall x \in A: m \leq x$. Czyli taki element, który jest "mniejszy" od każdego  z elementów w $A$ (to znaczy w relacji $xRy$ jes tym $x$ dla każdego $y$ w $A$)
- Supremum (Kres górny) to "najmniejsza" z majorant zbioru $A$ (oznaczamy $Sup. A$)
- Infimum (Kres dólny) to "największa" z minorant zbioru $A$ (Oznaczamy $Inf. A$)

###### $A=\{(1,2), (3,1)\}$
![[diagram-20241026 (3).png]]


###### $B=\{(x,y): x^2+y^2 \leq 9 \}$
![[diagram-20241026 (2).png]]

---
###### 7. Niech $S=(\mathbb{R}^2, grS, \mathbb{R}^2)$, gdzie: $(x_1,y_1)S(x_2,y_2) \Leftrightarrow ln(1+x_1^2+y_1^2)=ln(1+x_2^2+y_2^2)$ Czy tak określona relacja S jest porządkiem w $\mathbb{R}^2$?

$$\begin{gathered}
\forall (x_1,y_1), (x_2,y_2) \in \mathbb{R}^2\ \ ln(1+x_1^2+y_1^2)=ln(1+x_2^2+y_2^2) \Leftrightarrow x_1^2+x_2^2=x_2^2+y_2^2\\\\
Zatem \ grS \ mozemy \ przedstawic \ jako:\\
grS=\{((x_1,y_1),(x_2,y_2)) \in \mathbb{R}^2: x_1^2+x_2^2=x_2^2+y_2^2\}\\\\
1. Zwrotnosc:\\\forall (x,y) \in \mathbb{R}^2 \ \ x^2+y^2=x^2+y^2 \Leftrightarrow (x,y)R(x,y) \\\\
2. Antysymetria:\\x^2+y^2={x'}^2+{y'}^2 \land  {x'}^2+{y'}^2=x^2+y^2 \ nie \ implikuje \ ze:  \ x=x' \ i \ y=y' \ np: \\
(x,y)=(3,1), \ \ (x',y') = (1,3) \\
3^2+1^2=1^2+3^2, \ \ pomimo \ tego \ ze \ x \neq x' \ \ y \neq y' \\
\\
Zatem \ to \ nie \ jest \ porzadek. 
\end{gathered}$$

---
###### 8. Dany jest uporządkowany zbiór $(\mathbb{Q}, \leq)$ oraz podzbiór $A=\{x: x=\frac{1}{n}+\frac{1}{m}, \ n,m \in \mathbb{N_+}\}$. Znajdź kresy zbioru $A$ oraz elementy największy i najmniejszy (o ile istnieją). Czy zbiór $A$ stanowi łańcuch?

*Dla przypomnienia:*

- Element najmniejszy - to taki element który jest "mniejszy" od każdego innego elmentu w $X$ (coś jak minoranta ale nie podzbioru tylko całej naddziedziny) ozn. $\overline{m}$ 
- Element największy - to taki element który jest "większy" od każdego innego elmentu w $X$ (coś jak majoranta ale nie podzbioru tylko całej dziedziny) ozn. $\overline{M}$ 
- Łańcuch - taki podzbiór który jest liniowo uporządkowany

Element największy i najmniejszy nie istnieją.
Kresy zbioru $A$: 
- $inf. A$ = 0
- $sup. A$ = 2

Łańcuch: 
zwrotność jest oczywista x=x
antysymetryczność też $x \leq y \ \land \ y\leq x \implies x=y$ 
przechodność też $x\leq y \ \land \ y\leq z \implies x\leq z$
spójność też bo $x \leq y \ \vee \ x\geq y$

Więc $A$ to łańcuch bo: $A \in \mathbb{Q} \ \land \ (A,R_{|A \times A})$ liniowo uporządkowane.

---
###### 9. W zbiorze liczb zespolonych $\mathbb{C}$ określona jest następująca relacja $S: zSz' \Leftrightarrow z-z' \in \mathbb{R}_+$ Sprawdź, że relacja $S$ porządkuje zbiór $\mathbb{C}$ . Dla zbioru $A=\{1+2i, 2+2i, 3+2i, 2+i\} \subset \mathbb{C}$ znajdź elementy wyróżnione oraz najliczniejszy łańcuch złożony z elementów zbioru $A$.

$$\begin{gathered}
zakladajac \ ze \ 0 \ nie \ nalezy \ do \ \mathbb{R}_+\\\\
1. \forall z \in \mathbb{C} \ \ z-z =0 \notin \mathbb{R}_+ \\
wiec \ nie \ porzadkuje\\
Nie \ ma \ zadnego \ elmentu \ wyroznionego.
\end{gathered}$$
---
###### 3. Wykaż, że dla relacji zwrotnej $R$, równość $R\circ R=R$ jest równoważna "przechodności" relacji $R$ 

