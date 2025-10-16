### Subtytuł 
#### 2024-11-07
##### Poprzednia: [[]]
##### Następna: [[]]
##### Zadania: [[]]

#temat #przedmiot 

--- 
Ile jest dzielników liczby $10!$ podzielnych przez 20,24 lub 32?
$$\begin{gathered}
10!=2^8\cdot 3^4\cdot 5^2 \cdot 7^1\\
20: | 2^2\cdot 5^1 | 2^6 \ 3^4 \ 5^1 \ 7^1 | 7\cdot 5 \cdot 2 \cdot 2\\
24: | 2^3\cdot 3^1 | 2^5 \ 3^3 \ 5^2 \ 7^1 | 6\cdot 4 \cdot 3 \cdot 2\\
32: | 2^5 | 2^3 \ 3^4 \ 5^2 \ 7^1 | 4\cdot 5 \cdot 3 \cdot 2\\
(+)\\
20 \ i \ 24: | 2^3\cdot 3^1\cdot 5^ | 2^5 \ 3^3 \ 5^1 \ 7^1 | 6\cdot 4 \cdot 2 \cdot 2\\
20 \ i \ 32: | 2^5\cdot 5^1 | 2^3 \ 3^4 \ 5^1 \ 7^1 | 4\cdot 5 \cdot 2 \cdot 2\\
(-)\\

20 \ i \ 24 \ i \ 32: | 2^5\cdot 3^1\cdot 5^1 | 2^3 \ 3^3 \ 5^1 \ 7^1 | 4\cdot 4 \cdot 2 \cdot 2\\
(+)
\end{gathered}$$

---
Ciąg $h_n$ opisuje liczbę przecięć $n$ okręgów.

$$\begin{gathered}
h_1=2\\
h_2=4\\
h_3=8\\
h_4=14\\
\end{gathered}$$
Dodanie $(n+1)$ okręgu dodaje $2n$ punktów bo okrąg ten przecina się z każdym w 2 punktach. Punkty te wyznaczają na nowym okręgu elementarne łuki - liczba tych łuków wynosi $2n$ . Każdy taki łuk dzieli wcześniejszy obszar na dwie części. Zatem liczbę elementanrych ... po dodaniu $(n+1)$ okręgu wzrasta o $2n$.

$$\begin{gathered}
\left\{\begin{align*}
h_{n+1}=h_n+2n, \ \ n\geq 1\\
h_1=2
\end{align*}
\right.
\end{gathered}$$

$$\begin{gathered}h_{n+1}=h_n+2n=h_{n-1}+2(n-2)+2n=h_{n-2}+2(n-3)+2(n-2)+2n+...+2=\\
=2+2(1+2+3+...+n)=2+2(\frac{1+n}{2}n) =2+n^2+n\\
h_{n+1}=n^2+n+2
\end{gathered}$$
---
#### Przykład
Rozpoczynamy hodowlę królików z jedną parą królików nowo naroczonych. Każda para królików po osiągnięciu więku dwóch miesięcy wydaje na świat jedną parę w każdym miesiącu. Niech $f_n$ oznaccza liczbę par królików w hodowli po $n$ miesiącach.
Wyznacz ciąg $f_n$:

n:|w0|w1|w2| suma
0 |1   |0   | 0  |1
1 |  0   |  1    |   0 |1
2|    1  |  0   |    1|2
3 | 1    |   1  |   1|3
4|  2    | 1   |  2|5
5...

$f_n=f_{n-1}+f_{n-2}, \ n \geq 2$
$f_0=1$
$f_1=1$

##### Definicja
Niech $h_0, h_1, ..., h_n, ...$ będzie nieskończonym ciągiem liczb. Mówimy, że spełnia on *liniowe* równanie rekurencyjne stopnia $k$ jeśli istnieją współczynniki $a_1, a_2, ..., a_k,b \ (a_k \neq 0)$:

$h_n=a_1h_{n-1} + a_2 h_{n-2} + ... + a_kh_{n-k}+b, \ (n \geq k)$
Gdzie każdy ze współczynników $a_1, a_2, ..., a_k, b$ może zależeć od n.

Ciąg liczb $h_0, h_1, ..., h_n, ....$ spełniających powyższe równanie jest 
jednoznacznie wyznaczony przez liczby $h_0, h_1, ..., h_{k-1}$ nazywane wartościami początkowymi.

Liniowe równanie rekurencyjne jest homogeniczne, jeśli $b=0$.

Liniowe równanie rekurencyjne ma stałe współczynniki, jeśli każdy ze współczynników $a_1, a_2, ..., a_k$ jest stała.

###### Twierdzenie
Niech $q$ będzie niezerową stałą.
Wówczas $h_n=q^n$ jest rozwiązaniem homogenicznego równania rekurencyjnego *liniowego* o stałych współczynnikach:

$h_n - a_1h_{n-1} - a_2 h_{n-2} - ... - a_k h_{n-k}=0, \ (a_k \neq 0, n \geq k)$

wtedy i tylko wtedy, gdy $q$ jest pierwiastkiem wielomianu:

$x^k-a_1 x^{k-1} - a_2 x^{k-2} ... - a_k=0$



*Przykład z wykładu*

$u_n = u_{n-1} + u_{n-2}-u_{n-3}$
$u_0=1, \ u_1=3, \ u_2=7$

Rozpisz  domu

powinno wyjsc c1=1/2, c2=3/ c3=1/2

un=1/2+3n+1/2(-1)^n


W kostnicy grabarz zabawia się przepinając etykiety przypięte do zwłok, każda z imieniem/nazwiskiem, dziesięciu osób. 

Ile jest takich przepięć przy których żaden zmarły nie trafi ostatecznie do swojego grobu. :LiSkull:

Własnosć $P_i$ - $i$-ty zmarły ma właściwą etykiete.

$\overline{A_1} \cap \overline{A_2} \cap \ ...\ \cap \overline{A_{10}}$ 
$|X|=10!$
$\forall i \ |A_i| = 9!$
$\forall i,j\ \ i\leq j  \ \ |A_i \cap A_j|  8!$

Liczba nieporządków zbioru n-elementowego $X$:
$D_n = \sum_{i=0}^n \ (-1)^i {n \choose i} (n-i)!$


Dorzuć tu zdj. z tel na rozpisanie liczbe Stirlinga