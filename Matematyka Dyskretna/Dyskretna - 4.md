### Nieporządki, liczby Stirlinga I i II rodzaju, liczba Bella, podział liczby na składniki 
#### 2024-11-25
##### Poprzednia: [[Dyskretna - 3]]
##### Nastepna: [[Dyskretna - 5]]
##### Zadania: [[Dyskretna - zadania 4 liczby Bella, Stirlinga, nieporządki, podział liczby na k czynników]]

#matematyka_dyskretna  #liczba_bella #liczba_stirlinga #podzial_liczby_n_na_k #nieporzadki 

--- 
### Nieporządek

*Definicja:* 
Permutację $f$ nazywamy *nieporządkiem* jeśli, dla każdego $1\leq i \leq n, f(i)\neq i$

Czyli w skrócie, żadna z liczb nie jest na swoim miejscu.

*Oznaczenie i wzór liczby nieporządków:*
$D_n$ oznacza liczbę nieporządków zbioru n-elementowego $X$. 

$$\begin{gathered}
D_n=\sum^{n}_{i=0}{(-1)^i\binom{n}{i}(n-i)!}
\end{gathered}$$
*Inne oznaczenie:*
$!n$ 
###### intuicyjne wytłumaczenie wzoru:
Wynika to z [[Dyskretna - 3#^2ceee3|zasady włączeń i wyłączeń]] a konkretniej z tego wzoru:
$$\begin{gathered}
|\overline{A_1}\cap \overline{A_2}\dots \cap \overline{A_t}| = |X|-|A_1\cup A_2\dots \cup A_t| = |X| - \sum_{1\leq i \leq t}{|A_i|}+\sum_{1\leq i \lt j\leq t}{|A_i\cap A_j|}\\-\sum_{1\leq i \leq j \leq k \leq t}|A_i \cap A_j \cap A_k|-\dots + (-1)^{t}|A_1\cap A_2 \cap \dots \cap A_t|
\end{gathered}$$
Możemy wyprowadzic sobie gdzie założymy że własnościami $A_i$ są że i-ty element jest na swoim miejscu.
$$\begin{gathered}
n!-\binom{n}{1}\cdot (n-1)! \dots \pm \binom{n}{n}\cdot (n-n)!
\end{gathered}$$
Czyli bierzemy wszystkie możliwe permutacje i usuwamy te które nam nie spełniają warunków, korzystając z zasady włączeń i wyłączeń (liczba elementów zbioru który nie ma żadnej z podanych własności) gdzie $\binom{n}{i}\cdot (n-i)!$ to liczba możlliwości wyboru tych elementów które nie zmienią miejsca razy permutacja reszty.

Jednakże w wzorze na nieporządki zaczynamy od $i=0$ co po podstawieniu daje oczywiście nam $n!$także jest to po prostu skrócona forma tego wzoru.

###### Lemat:
Możemy zauważyć że:
$$\begin{gathered}
\lim_{n\to \infty}{\frac{D_n}{n!}}=e^{-1}\approx 0.368
\end{gathered}$$

###### Liczba odwzorowań suriektywnych:

^b14b20

Właściwie wzór na to wygląda niemal identycznie co do nieporządków
$$\begin{gathered}
|X|=n,\ \ \ |Y|=m\\
m^n - \binom{m}{1}\cdot (m-1)! + \binom{m}{2}\cdot (m-2)! - \binom{m}{3}\cdot (m-3)!\dots + (-1)^{m-1}\binom{m}{m-1}1^n
\end{gathered}$$
---
### Podział n elementowego zbioru na k bloków (Liczba Stirlinga II rodzaju)

*Definicja:*
Przez podział n-elementowego zbioru $X$ na $k$ bloków rozumiemy taką rodzinę $B=\{B_1,B_2,\dots B_k\}$ podzbiorów zbioru $X$ , że $B_i\neq \emptyset, B_i \cap B_j \neq \emptyset \ oraz \ B_1\cup B_2\cup B_3 \dots \cup B_k=X$ dla każdych $i,j \in \{1,2,3\dots,k\}$

Czyli w skrócie dzielimy ten zbiór na takie bloki żeby suma tych bloków pokrywała każdy element zbioru $X$ oraz każdy blok miał inne elementy (żaden element nie może być naraz w dwóch różnych blokach) oraz żaden blok nie jest pusty.

Liczbę podziałów zbioru $n$-elementowego na $k$-bloków nazywamy *liczbą Strirlinga drugiego rodzaju* i oznaczamy $S(n,k)$

*Wzór:* (rekurencyjny)

$$\begin{gathered}
S(n,k) = S(n-1, k-1) + k\cdot S(n-1,k), \ dla \ \ 0 \lt k \lt n\\
S(n,n)=1, \ dla \ n \geq 0\\
S(n,0)=0, \ dla \ n \gt 0
\end{gathered}$$

###### Intuicyjne wytłumaczenie:
- Jeżeli chcemy podzielić zbiór n elementowy na k bloków to *możemy podzielić n-1 elementów na k bloków i n-ty element dorzucić do jednego z k bloków*. Albo *podzielić n-1 elementów na k-1 bloków a n-ty element wrzucić do nowego k-tego bloku*.
- Oczywiście możemy podzielić n elementów na n bloków tylko na jeden sposób.
- A podzielić n elementów na 0 bloków nie da się wcale. Zawsze będzie minimum jeden blok.

**Nie jest ważna tutaj kolejność elementów w bloku, nie robimy permutacji po prostu je "dzielimy do worków"**

---
### Liczba Bella

*Definicja:*
Liczbę podziałów zbioru $n$-elementowego nazywamy *liczbą Bella* i oznaczamy symbolem *B(n)*.
$$\begin{gathered}
B(n)=\sum^{n}_{k=0}S(n,k)
\end{gathered}$$
Czyli po prostu wszystkie możliwe podziały $n$-elementowego zbioru na dowolną ilość bloków.

*Lemat:*
$$\begin{gathered}
B(n+1)=\sum^{n}_{i=0}{\binom{n}{i}B(i)}
\end{gathered}$$

###### Wytłumaczenie intuicyjne lematu:

Najlepiej to pokazać zaczynając od końca czyli od $i=n$. Wtedy wyobrażamy sobie że dzielimy $n$ elementów na bloki ale dodatkowo $n+1$ element ma swój blok. Jednakże jeśli $i$ będzie mniejsze od $n$ np. $i=n-1$ to dzielimy $n-1$ elementów na bloki a 2 elementy muszą znaleźć miejsce w którymś spośród tych bloków. Itd itd...

---
### Podział liczby $n$ na $k$ składników

*Definicja:*
Podziałem liczby $n$ na $k$ składników nazywamy taki ciąg liczb naturalnych $<b_1,b_2,\dots,b_k>$, że $b_1\geq b_2\geq \dots \geq b_k \gt 0$ oraz $b_1+b_2+\dots+b_k=n$.

$$\begin{gathered}
P(n)=\sum^{n}_{k=0}{P(n,k)}\\\\
P(0,0)=P(0)=1
\end{gathered}$$
*Lemat:*
Liczba podziałów liczby $n$ na $k$ składników jest równa liczbie tych podziałów liczby $n$ , w których największy składnik ma wartość $k$.

*Lemat 2:*
Dla $n\geq k \geq 0$ zachodzi zależność:
$$\begin{gathered}
P(n,k)=\sum^{k}_{i=0}{P(n-k,i)}\\\\
P(n,k)=0,\ \  \ dla \ n\lt k\\
P(n,0)=0,\ \  \ dla \ n\gt 0\\
P(n,n)=1,\ \  \ dla \ n\geq 0\\
\end{gathered}$$
###### Intuicyjne wytłumaczenie wzoru:
Skoro zakładamy że lemat który przedstawiłem powyżej jest prawdziwy czyli że największy składnik musi być co najmniej równy $k$. Na przykład dla $P(4,2)$ najmniejszy składnik to $2$ ponieważ mamy albo $2+2$ albo $1+3$. To to jest analogiczne do tego że mamy:

$k+b_2+b_3+\dots +b_{k-1}=n$ 

Co następnie przekształcamy do:
$b_2+b_3+\dots +b_{k-1}=n-k$

A tu pozostaje pytanie na ile sposobów możemy to przedstawić? A no na tyle sposobów ile jest możliwych $P(n-k,i)$ gdzie $0\leq i \leq k$. (Dodajemy je).
Albo inaczej:
Dla $P(4,2)$ mamy $2+1+1=3+1+2+2=4$ czyli albo jeden z elementów jakby nam wjedzie do pierwszego albo nie będzie jakby rozdzielności.

No i pozostają nam jedynie krańcowe przypadki wtedy czyli:
$P(n,k)=0,\ \  \ dla \ n\lt k$  - nie ma takich podziałów liczby $n$ na $k$ liczb naturalnych gdzie $k$ większe od $n$, to znaczy np podzielmy liczbe 3 na 10 bloków.
$P(n,0)=0,\ \  \ dla \ n\gt 0$ - nie damy rady podzielić żadnej liczby na 0 liczb naturalnych które ją tworzą
$P(n,n)=1$ - no to mamy tylko jeden przypadek gdy dzielimy jakąś liczbe na tyle samo bloków ile wynosi np dla liczby $4$ mamy $1+1+1+1=4$ 

###### Przykład:

Przykład dla zwizualizowania jak to działa:
$b_1+b_2=4$ z czym $b_1\leq b_2$
$$\begin{gathered}
P(n,k)=\sum^{k}_{i=0}{P(n-k,i)}\\
P(4,2)=P(2,0)+P(2,1)+P(2,2)\\
P(4,2)=0+P(2,1)+1\\
P(4,2)=1+P(2,1)=1+P(1,0)+P(1,1)=2\\
2+2=4, \ 1+3=4
\end{gathered}$$
**Nie jest ważna tutaj żadna permutacja, kolejność tych liczb, mamy ja ustaloną wiedząc która jest największa itd**


---
### Ważne 
![[diagram-20241126.png]]

---
### Liczba Stirlinga pierwszego rodzaju

*Definicja:*
Liczbę Stirlinga pierwszego rodzaju oznaczamy symbolem $s(n,k)$ i definiujemy jako liczbę tych permutacji zbioru $n$-elementowego które w rozkładzie na cykle posiadają $k$ cykli.

*Wzór:*
$$\begin{gathered}
s(n,k)=s(n-1,k-1)+(n-1)\cdot s(n-1,k), \ \ dla \ \ 0\lt k \lt n\\
s(n,n)=1, \ \ dla \ \ n\geq 0\\
s(n,0)=0, \ \ dla \ \ n\gt 0\\
\end{gathered}$$
*Alternatywne oznaczenie:*
$c(n,k)$

###### intuicyjne wytłumaczenie wzoru:

- Pierwszy składnik - bierzemy wszystkie rozkłady na $k-1$ cykli $n-1$ elementowej permutacji i tworzymy nowy cykl dla $n$-tego elementu
- Drugi składnik - bierzemy wszystkie rozkłady na $k$ cykli $n-1$ elementowej permutacji i po każdym z $n-1$ elementów możemy dopisać $n$-ty element co nam dalej da cykl.

---
 $$\begin{gathered}
 
\end{gathered}$$