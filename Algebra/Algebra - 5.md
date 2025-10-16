### Struktury algebraiczne
#### 2024-10-24
##### Poprzednia: [[Algebra - 4]]
##### Następna: [[Algebra - 6]]
##### Zadania: [[]] 

#struktury_algebraiczne  #algebra 

---
### Działania

##### Wewnętrzne:

^a72f3a

*Def.* $A$ - zbiór, $A \neq \emptyset$
(Dwuelementowym) *działaniem wewnętrznym*, lub po prostu *działaniem*, określonym w zbiorze $A$ nazywamy każde odwzorowanie:

$$\begin{gathered}
h: A \times A \rightarrow A\\
\end{gathered}$$
Wartość tego odwzorowania, $h(a, b)$, nazywamy wynikiem działania.
(Czyli po prostu dajmy na to dodajemy 3+2 i otrzymujemy 5) - $\mathbb{N} \times \mathbb{N} \rightarrow \mathbb{N}$

*Oznaczenia:* $(A,h) \ lub \ (A, \circ)$ - zbiór z określonym działaniem;
w drugim przypadku piszemy $a \circ b$ zamiast $h(a,b)$.
*Prz.*
$h: \mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{Z}$  $h(n,k) = n+k$

*Lub:*
$(Z_+, h) \ \ \  h(n,k) = \frac{n}{k}$ 

$h$ tutaj *nie określa* działania (wewnętrznego) (w tym zbiorze) bo $\frac{n}{k}$ nie koniecznie jest w $\mathbb{Z}_+$
O działaniu *wewnętrznym* możemy mówić tylko wtedy kiedy wynik także należy do danego zbioru.
##### Zewnętrzne:

^eb0a26

*Def.*  $F, X$ - zbiory,  $F,X \neq \emptyset$
*Działaniem zewnętrznym* w zbiorze $X$ nazywamy każde odwzorowanie
$$\begin{gathered}
g: F \times X \rightarrow X
\end{gathered}$$
*Ozn.* $g(\alpha, x) = \alpha * x$ - wynik  działania, gdzie $\alpha \in F, \ \ x \in X$.
*Prz.* $X$ - zbiór wektorów na płaszczyźnie
F = $\mathbb{R}$
$*$ - mnożenie wektora przez liczbę (wynik - wektor)

---
### Własności działania wewnętrznego
*Def.* $(A, \circ)$ - zbiór z działaniem wewnętrznym

1) Działanie $\circ$ jest *łączne*, jeżeli: $$\forall x,y,z \in A: \ (x \circ y) \circ z = x\circ (y\circ z)$$
2) Działanie $\circ$ jest *przemienne*, jeżeli $$\forall x,y \in A: x\circ y = y\circ x$$
3)  $e \in A$ jest *elementem neutralnym* działania, jeżeli: $$ \forall x \in A: x \circ e = e \circ x = x$$
*Tw.* Jeżeli w zbiorze $A$ z działaniem wewnętrznym $\circ$ istnieje element neutralny, to jest on jedyny.
$$\begin{gathered}
D: e_1, e_2 \in A: e_1, e_2 \ - \ el. \ neutralne \circ \ w \ zb. A\\
e_1 \ - \ el. \ neutralny \implies e_2 \circ e_1 = e_2 \\
e_2 \ - \ el. \ neutralny \implies e_1 \circ e_2 = e_1\\
z \ def. \ el. \ neutralnego \ x \circ e = e \circ x = x \ wynika \ ze \ e_1=e_2
\end{gathered}$$

4) Jeśli istnieje element neutralny $e \in A$ działania $\circ$, to *elementem symetrycznym (przeciwnym/odwrotnym)* do $x \in A$ nazywamy taki element: $x' \in A$, że $x \circ x' = e = x' \circ x$ **Ważnym jest żeby pamiętać o drugiej stronie warunku**
*Tw.* Jeśli działanie $\circ$ jest *łączne* w zbiorze $A$ i istnieje element neutralny $e \in A$ tego działania, wówczas jeśli jakiś element $x \in A$ ma element symetryczny, to jest on jedyny oraz: $(x')' = x$.

*Prz.* $(\mathbb{Z}, +)$
Działanie + jest łączne bo: $\forall x,y,z \in \mathbb{Z}: (x+y)+z = x+(y+z)$
Działanie + jest przemienne bo: $\forall x,y \in \mathbb{Z}: x+y=y+x$
Elementem neutralnym działania + jest 0: $x+0=0+x=0$
Elementem symetrycznym do każdego $x \in \mathbb{Z}$ jest $-x$.

---
### Grupa 
*Def.* $(A, \circ), \ \ A \neq \emptyset$, $\circ$ - działanie wewnętrzne w zb. $A$:
Strukturę $(A, \circ)$ nazywamy *grupą*, jeżeli spełnione są warunki:
1. $\forall x,y,z \in A: (x \circ y) \circ z = x \circ (y \circ z)$ - *Łączność* ^e5a53c
2. $\exists e \in A \ \forall x \in A: x \circ e = x = e \circ x$ - *El. neutralny*
3. $\forall x \in A \ \exists x' \in A: x \circ x'  =e = x' \circ x$ - *El. symetryczny dla każdego x*
Jeżeli dodatkowo:
4. $\forall x,y \in A: x\circ y = y\circ x$ - *Przemienność*
to grupę nazywamy *grupą przemienną / abelową*. ^ae68d6

---
### Pierścień
*Def.* $P \neq \emptyset$,  $\circ, *$ - działania wewnętrzne w zbiorze $P$
Strukturę $(P, \circ, *)$ nazywamy *pierścieniem*, jeżeli spełnionne są warunki:
1) Struktura $(P, \circ)$ jest [[#^ae68d6| grupą abelową]]
2) $\forall x,y,z \in P: \ (x*y)*z = x*(y*z)$ - [[#^e5a53c| Łączność *]]
3) $\forall x,y,z \in P: (x \circ y) * z = (x*z) \circ (y * z) \ \land \ x*(y \circ z) = (x *y )\circ (x*z)$ - *prawo i lewo stronna rozdzielność $\ast$ względem $\circ$*
Jeżeli dodatkowo:
4) $\forall x,y \in P: x*y = y*x$ - *Przemienność $\ast$* 
To pierścień nazywamy *pierścieniem przemiennym*.

*Prz.* $(\mathbb{Z}, +, \cdot)$ - pierścień przemienny

*Uw.* $(P, \circ, *)$ - pierścień
Pierwsze działanie $\circ$ nazywamy *działaniem addytywnym* i oznaczamy (zazwyczaj) *+* Element neutralny tego działania nazywamy *zerem* i oznaczamy *0* (a element symetryczny do $x \in P$ względem tego działania nazywamy *przeciwnym* i oznaczamy *-x*). Drugie działanie nazywamy *działaniem multiplikatywnym*, oznaczamy je zazwyczaj $\cdot$  )

*Def.* $(P, +, \cdot)$ - pierścień
-  Jeżeli dodatkowo istnieje w $P$ element neutralny ze względu na działanie multiplikatywne, to element ten nazywamy *jedynką*, oznaczamy *1*, a pierścień nazywamy *pierścieniem z jednością*. 
- $x,y \in P$ nazywamy *dzielnikami 0*, jeżeli $x,y \neq 0$ i $x \cdot y=0$
- Pierścień przemienny z jednością i bez dzielników zera nazywamy *pierścieniem całkowitym*.
---
### Ciało 
*Def.* Pierścień z jednością $(K, +, \cdot)$ nazywamy *ciałem*, jeżeli:
$\forall x \in K \ \setminus \ \{0\} \ \exists x^{-1} \in K: x \cdot x^{-1}=1=x^{-1} \cdot x$ 
Czyli istnieje element symetryczny działania multiplikatywnego dla każdego x różnego od elementu neutralnego działania addytywnego.

Jeżeli ponadto:
$\forall x,y \in K: x \cdot y = y\cdot x$
to ciało nazywamy *ciałem przemiennym*. ^dd2f3e

*Uwagi.* Równoważnie, struktura $(K, +, \cdot)$ jest ciałem (przemiennym), jeżeli:
1) struktura $(K, +)$ jest [[#^ae68d6| grupą abelową]].
2) struktura $(K \ \setminus \{0\}, \cdot)$ jest grupą (odpowiednio przemienną).
3) $\forall x,y,z \in K : (x+y) \cdot z = (x\cdot z) + (y\cdot z) \ \land \ x \cdot (y+z) = (x\cdot y) + (x\cdot z)$

*Obs.* W ciele nie ma dzielników zera. 

---
### Homomorfizmy struktur
*Def.* Odwzorowanie $h: A_1 \rightarrow A_2$ nazywamy *homomorfizmem* grupy $(A_1, +)$ w grupę $(A_2, \oplus)$ jeżeli $\forall x,y \in A_1: h(x+y) = h(x) \oplus h(y)$.

*Prz.* $(\mathbb{R}, +), (\mathbb{R}_+, \cdot)$
$h: \mathbb{R} \rightarrow \mathbb{R}_+, \ h(x) = e^x$ - homomorfizm 

*Tw.* Z: $h: A_1 \rightarrow A_2$ - homomorfizm grupy $(A_1, +)$ w grupę $(A_2, \oplus)$ 
T: (a) $e_1$ - el. neutralny w $A_1 \implies h(e_1)$ - el. neutralny w $A_2$
b) $\forall x \in A_1: h(x') = (h(x))'$

*Def.* Dwie struktury nazywamy *izomorficznymi*, jeżeli istnieje *izomorfizm*, tj. *homomorfizm bijektywny*, jednej struktury na drugą.

---
