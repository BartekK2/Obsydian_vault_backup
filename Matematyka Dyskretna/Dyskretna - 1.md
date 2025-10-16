### Cykle i podstawowe wzory kombinatoryczne
#### 2024-10-10
##### Następna: [[Dyskretna - 2]]
##### Zadania: [[Dyskretna - zadania 1 kombinacje]]

#cykle #złożenie #kombinatoryka #matematyka_dyskretna

---

Liczba funkcji różnowartościowych: 
($|x|=|y|=n$)
Jest równa: $n!$ (Jak w permutacji)

---
###### Złożenie funkcji 
Złożenie funkcji f i goznaczany $(g \circ f)(x)=g(f(x))$

---
###### Permutacja identycznościowa
Permutację $e=<1,2,3,...,n>$ nazywamy identycznościową 
Dla dowolnej permutacji $f \in S_n: f \circ e = e \circ f =f$

---
### Wzory kombinatoryczne:

$$\begin{gathered}
\binom{n}{k}=\binom{n-1}{k}+\binom{n-1}{k-1}\\
\binom{n}{k}=\binom{n}{n-k}\\
k\cdot \binom{n}{k}=n\cdot \binom{n-1}{k-1}\\
\binom{n}{k}\binom{k}{m}=\binom{n}{m}\binom{n-m}{n-k}\\
\binom{m+n}{k}=\sum^{k}_{i=0}\binom{m}{i}\cdot \binom{n}{k-i}\\
\sum^{k}_{i=0}\binom{k}{i}^2\cdot \binom{n+2k-i}{2k}=\binom{n+k}{k}^2
\end{gathered}$$
---
### Tłumaczenia wzorów rozrysowane w zbiorach graficznych i przełożone na język naturalny
---
###### 1.
$$\begin{gathered}
\binom{n}{k}=\frac{n!}{k!\cdot (n-k)!}=\binom{n}{n-k}=\frac{n!}{(n-k)!\cdot (n-(n-k)!)}
\end{gathered}
$$
Jeżeli chcemy wybrać np. 3 żołnierzy z 7 osobowego oddziału, którzy pójdą na pole bitwy, to nieważne czy wybierzemy kto pójdzie czy kto nie pójdzie bo to daje nam ten sam wybór.

---
###### 2.
$$
\begin{gathered}
\binom{n}{k}=\binom{n-1}{k}+\binom{n-1}{k-1}
\end{gathered}
$$
![[Pasted image 20241008014648.png]]

---
###### 3.
$$
\begin{gathered}
\binom{n}{k}\binom{k}{m}=\binom{n}{m}\binom{n-m}{n-k}
\end{gathered}
$$

![[Pasted image 20241008014254.png]]


---

###### 4.

$$\begin{gathered}
k\binom{n}{k}=n\binom{n-1}{k-1}\\
Dlaczego?\\
k\binom{n}{k}=\frac{n!\cdot k}{k!\cdot (n-k)!}=\frac{n!}{(k-1)!\cdot (n-k)!}=n\cdot \frac{(n-1)!}{(k-1)!\cdot (n-k)!}=n\binom{n-1}{k-1}
\end{gathered}$$

---
###### 5.

$$\begin{gathered}
\binom{m+n}{k}=\sum^{k}_{i=0}\binom{m}{i}\cdot \binom{n}{k-i}
\end{gathered}$$

Ten wzór opisuje liczbę kombinacji, kiedy wybieramy $k$ elementów z sumy dwóch zbiorów, które mają $m$ i $n$ elementów.

- Lewa strona, $\binom{m+n}{k}$, to liczba sposobów wybrania $k$ elementów z $m+n$ elementów.
- Prawa strona to suma wszystkich możliwych przypadków, w których wybieramy $i$ elementów z pierwszego zbioru (o $m$ elementach) i $k-i$ elementów z drugiego zbioru (o $n$ elementach), gdzie $i$ zmienia się od $0$ do $k$.
---
$$\begin{gathered}
\sum^{k}_{i=0}\binom{k}{i}^2\cdot \binom{n+2k-i}{2k}=\binom{n+k}{k}^2
\end{gathered}$$
---
![[diagram-20241115 2.png]]
##### Przykłady:
###### Kombinacje bez powtórzeń:
Na ile sposobów można wybrać 10 osób z 30 osób? - $\binom{30}{10}$

###### Kombinacje z powtórzeniami:
Na ile sposobów można rozdać 10 cukierków 30 osobom? - $\binom{10+30-1}{30-1}=\binom{10+30-1}{10}$
Rozdanie 10 jabłek 3 osobom to: $\binom{10+3-1}{3-1}$ czyli naszym n=10 (liczba przedmiotów), k=3 (liczba grup) 

Wynika to z tego że wyobrażamy sobie rozstawione 10 jabłek i 2 "przerwy" które rozdzielą nam jabłka na 3 grupy. Więc z wszystkich miejsc (jabłek i przerw) wybieramy przerwy.
###### Wariacje bez powtórzeń:
Na ile sposobów mozna wybrać 10 osób z 30 osób, i ustawić je w kolejce (np: wybieramy 10 osób z 30 osobowej klasy do tablicy, i ustalamy im kolejność w jakiej pójdą)? - $\binom{30}{10}\cdot 10!$

###### Permutacje bez powtórzeń:
Na ile sposobów mozna ustawić w kolejce 10 osób? - $10!$

###### Wariacje z powtórzeniami:
Na ile sposobów można dać zieloną/niebieską/czerwoną koszulke każdej z 10 osób? - $3^{10}$

###### Permutacja z powtórzeniami:
Ile różnych wyrazów można ułożyć przestawiając litery w wyrazie "MATEMATYKA"? - $\frac{10!}{2!\cdot 3!\cdot 2!}$
Ponieważ najpierw permutujemy wszystkie litery a potem pozbywamy się tych samych wyrazów 
($M_1ATEM_2ATYKA$) to to samo co ($M_2ATEM_1ATYKA$) 

---
### Twierdzenie dwumienne

Niech $x,y \in \mathbb{R}, n \in \mathbb{N}$ Wówczas
$$\begin{gathered}
(x+y)^n = \sum^{n}_{i=0}\binom{n}{i}x^i\cdot y^{n-i}
\end{gathered}$$
W szczególności $x=y=1$

$$\begin{gathered}
2^n=(1+1)^n=\sum_{i=0}^n{\binom{n}{i}}
\end{gathered}$$

---
### Twierdzenie wielomienne

Niech $x_1,x_2,...,x_t \in \mathbb{R}, n \in \mathbb{N}$. Wówczas

$$\begin{gathered}
(x_1+x_2+...+x_t)^n=\sum{\frac{n!}{n_1!n_2!...n_t!}x_1^{n_1}x_2^{n_2}...x_t^{n_t}}\\
Gdzie \ sumowanie \ przeprowadzone \ jest \ po \\ wszystkich \ nieujemnych \ calkowitoliczbowych \ rozwiazan \ rownania:\\
n_1+n_2+...+n_t=n
\end{gathered}$$
---
### Lematy:

1) Jeśli $|X|=n$ oraz $|Y|=m$, to liczba wszystkich funkcji $f: X \to Y$ wynosi $m^n$ 
   Tłumaczenie: każdemu argumentowi przypisujemy jedną wartość (mogą być takie same jak w innych), np: dla dziedziny 3 elementowej i zw 2 elementowej mamy $2^3$
2) Jeśli $|X|=n$ oraz $|Y|=m, m\geq n$, to liczba wszystkich funkcji różnowartościowych $f: X \to Y$ wynosi $\frac{m!}{(m-n)!}$
   Tłumaczenie: $\frac{m!}{(m-n)!}$ to nic innego jak $m\cdot (m-1)\cdot (m-2)\cdot (m-3)...\cdot (m-n+1)$ czyli każdemu argumentowi przypisujemy jedną różną wartość z tych które nam pozostały jeszcze nie wybrane
3) Jeśli $|X|=n$ oraz $|Y|=m, m\geq n$, to liczba wszystkich funkcji rosnących $f: X \to Y$ wynosi $\binom{m}{n}$
   Tłumaczenie: Po prostu wybieramy ileś wartości ze zbioru wartości a można je poukładać rosnąco tylko na jeden sposób
4) Jeśli $|X|=n$ oraz $|Y|=m, m\geq n$, to liczba wszystkich funkcji niemalejących $f: X \to Y$ wynosi $\binom{n+m-1}{m-1}$
   Tłumaczenie: To po prostu kombinacja z powtórzeniami, wybieramy tyle wartości ile nam potrzeba (mogą sie powtarzać) a następnie je układamy na jeden możliwy sposób
5) **Wniosek** Jeśli $|X|=|Y|=n, \ m\geq n$, to każda funkcja różnowartościowa $f: X \to Y$ jest wzajemnie jednoznaczna (bijektywa). Wówczas liczba takich funkcji jest równa $n!$.
6) [[Dyskretna - 4#^b14b20|Liczba odwzorowań suriektywnych]]

*Def.*
Odwzorowanie bijektywne $f: X\to Y$ nazywamy permutacją zbioru $X$.

### Permutacje

Permutację $f: X \to X$ zapisujemy:
$$\begin{gathered}
f=\dbinom{x_1,x_2,...,x_n}{f(x_1),f(x_2),...f(x_n)}\\\\
A \ zakladajac \ ze \ X=\{1,2,3...,n\}\\\\
Wowczas:\\
f=<f(1),f(2),...,f(n)>
\end{gathered}
$$

Złożeniem permutacji $f,g \in S_n$ gdzie $S_n$ oznaczamy zbiór wszystkich permutacji zbioru $n$-elementowego, nazywamy permutację $g \circ f$ zdefiniowaną następujaco:
$$\begin{gathered}
\forall i  \in X: \ (g\circ f)(i)=g(f(i))
\end{gathered}$$

*Def.*
Permutację $e=<1,2,...,n>$ nazywamy identycznościową.

Każda permutacja $f \in S_n$ wyznacza jednoznacznie taką permutację $f^{-1}\in S_n$ że $f\circ f^{-1}=f^{-1}\circ f=e$, $f^{-1}$ nazywamy permutacją odwrotną do $f$.


Przykład permutacji: $<3,2,4,1>$ 

Normalnie permutacja ma oczywiście $n!$ tyle możliwych kombinacji jednakże dla *multizbiorów* (zbiorów z powtarzającymi sie elementami) ma $\frac{n!}{n_1!n_2!...n_t!}$ kombinacji gdzie $n_1,n_2,...,n_t$ oznacza liczbę powtórzeń każdego z powtarzających sie elementów.
Przykładowo permutacja zbioru $\{1,1,1,2,3,3,4,4,4,5,6\}$ wynosi $\frac{11!}{3!2!3!}$

### Cykle

*Def.*
Cyklem długości $k$ nazywamy permutację $f_k=(x_1^kx_2^k...x_k^k)$, w której $f_k(x_1^k)=x_2^k, f_k(x_2^k)=x_3^k, f_k(x_3^k)=x_4^k, ... f_k(x_{k-1}^k)=x_k^k, f_k(x_k^k)=x_1^k$ oraz $f_k(x)=x$ dla każdego $x \in X \setminus \{x_1^k, x_2^k, ..., x_k^k\}$.
Przykład cyklu dla permutacji $<3,2,4,1,> \ (1,3,4)(2)$

*Lemat*
Każdą permutację można przedstawić jednoznacznie w postaci złożenia (niezależnych) cykli. Przedstawienie takie nazywamy *rozkładem na cykle*.


*Def*
Mówimy, że permutacja $f$ jest typu $(\lambda_1, \lambda_2,...,\lambda_n)$ jeśli w rozkładzie na cykle zawiera dokładnie $\lambda_i$ cykli długości $i$, dla $i=1,2,...,n$.
Do zapisu typu stosujemy zwykle notację $1^{\lambda_1}2^{\lambda_2}...n^{\lambda_n}$ (pomijając $i^{\lambda_i}$ jeśli $\lambda_i=0$)
Przykład typu permutacji dla permutacji $f=<1,2,3>=(1\ 2)(3)$ mamy 1 cykl długości 1 i 1 cykl długości 2 więc typ tej permutacji to $1^12^1$ 


