### Podstawy
#### 2024-11-01

##### Następna: [[Analiza - 2]]

#biekcja #iniekcja #suriekcja #analiza 
#złożenie #odwrotna

--- 
#### Iniekcja:
Funkcja różnowartościowa, Y może mieć tylko jeden X.
$\forall_{x1,x2 \in D_f} [x_1 \neq x_2 \implies f(x_1) \neq f(x_2)]$
![[diagram-20241101 (1).png]]

---
#### Suriekcja:
Każdy Y z przeciwdziedziny ma swój X. (Żaden nie został sam)
$\forall_{y \in Y} \ \exists_{x \in X} \ f(x)=y$
![[diagram-20241101 (2).png]]

---
#### Biekcja
Zarówno iniekcja jak i suriekcja.
$f: X \rightarrow_{na}^{1:1} Y$
![[diagram-20241101 (3).png]]

---

#### Złożenie funkcji:

$f: X\rightarrow Y, \ \ g: Y\rightarrow Z$

Złożeniem funkcji $g$ i $f$ nazywamy funkcję $g\circ f: X\rightarrow Z$ taką że:
$\forall_{x\in X} \ \ (g\circ f)(x) = g(f(x))$
$f$  - funkcja wewnętrzna
$g$ - funkcja zewnętrzna

*Oczywiście składanie funkcji nie jest przemienne!*

---
#### Funkcja odwrotna:

$f: X\rightarrow Y$ - bijekcja (skoro musimy zamienić Y z X to nasze nowe argumenty muszą przyjmować tylko jedną wartość)

Funkcją odwrotną do funkcji $f$ nazywamy funkcję $f^{-1}: Y \rightarrow X$ taką, że:
$\forall_{y \in Y} \ f^{-1}(y)=x \Leftrightarrow y=f(x)$

Czyli po prostu zamieniamy dziedzinę z przeciwdziedziną.
*Wykresy funkcji i funkcji do niej odwrotnej są symetryczne względem osi y=x*
###### Przykłady:
Wyznacz funkcję odwrotną do $f(x)=x^3$.
$f^{-1}(y)=x$ więc $f^{-1}(x)=\sqrt[3]{x}$

---
