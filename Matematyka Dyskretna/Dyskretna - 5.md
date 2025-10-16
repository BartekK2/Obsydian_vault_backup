### Ciągi rekurencyjne, funkcje tworzące, postać jawna
#### 2024-11-27
##### Poprzednia: [[Dyskretna - 4]]
##### Nastepna: [[Dyskretna - 6]]
##### Zadania: 

#matematyka_dyskretna  #ciągi_rekurencyjne #funkcje_tworzące #postać_jawna

--- 
### Ciąg rekurencyjny

*Definicja:*
Niech $h_0,h_1,\dots,h_n,\dots$ będzie nieskończonym ciągiem liczb. Mówimy, że spełnia on *liniowe równanie rekurencyjne* stopnia $k$ jeśli istnieją współczynniki $a_1,a_2,\dots,a_k,b \ \ (a_k\neq 0)$
$$\begin{gathered}
h_n=a_1h_{n-1}+a_2h_{n-2}+\dots+a_kh_{n-k}+b, \ \ (n\geq k)
\end{gathered}$$
gdzie każdy ze współczynników $a_1,a_2,\dots,a_k,b$ może zależeć od $n$.

Ciąg liczb $h_0,h_1,\dots,h_n,\dots$ spełniających powyższe równanie jest jednoznacznie wyznaczony przez liczby $h_0,h_1,\dots,h_{k-1}$ nazywane *wartościami początkowymi*.

*Przykłady:*
$h_n=2n\cdot h_{n-1} + (\frac{3}{n+1}+1)\cdot h_{n-2} + 2n$
$h_n=2\cdot h_{n-1} + 3\cdot h_{n-2} + 4$
$h_n=2\cdot h_{n-1} + 3\cdot h_{n-2} +5\cdot h_{n-1} + 7\cdot h_{n-2}+ 2^n$

Liniowe równanie rekurencyjne jest *homogeniczne*, jeśli $b=0$.

*Przykład:*
$h_n=h_{n-1} + h_{n-2}$ - fibbonacci

Liniowe równanie rekurencyjne ma stałe współczynniki, jeśli każdy ze współczynników $a_1,a_2,\dots,a_k$  jest stałą.

*Twierdzenie:*
Niech $q$ będzie niezerową stałą.
Wówczas $h_n=q^n$ jest rozwiązaniem *homogenicznego* równania rekurencyjnego liniowego o *stałych współczynnikach*.
$$\begin{gathered}
h_n-a_1h_{n-1}-a_2h_{n-2}-\dots-a_kh_{n-k}=0, \ \  (a_k\neq 0, n \geq k)
\end{gathered}$$
wtedy i tylko wtedy gdy q jest pierwiastkiem wielomianu:
$$\begin{gathered}
x^k-a_1x^{k-1}-a_2x^{k-2}\dots a_k=0
\end{gathered}$$

Wielomian ten nazywany jest *wielomianem charakterystycznym*, a wszystkie jego pierwiastki *pierwiastkami charakterystycznymi*.

Jeśli wielomian charakterystyczny ma $k$ różnych pierwiastków $q_1,q_2,\dots, q_k$ wtedy:
$$\begin{gathered}
h_n=c_1q_1^n+c_2q_2^n+\dots+c_kq^n
\end{gathered}$$
Dla każdego wyboru wartości początkowych $h_0,h_1,\dots,h_{k-1}$ istnieją jednoznacznie określone stałe $c_1,c_2,\dots,c_k$.

Jeśli $q_i$ jest pierwiastkiem $s_i$-krotnym wielomianu charakterystycznego, to wówczas każda z wartości $h_n=q_i^n, h_n=nq_i^n, h_n=n^2q_i^n,\dots,h_n=n^{s_i-1}q_i^n$ jest rozwiązaniem równania, a stąd:
$$\begin{gathered}
h_n^{(i)}=c_1q_i^n+c_2nq_i^n+\dots+c_{s_i}n^{s_i-1}q_i^n
\end{gathered}$$
jest rozwiązaniem dla pierwiastka $q_i$, przy każdym wyborze współczynników $c_1,c_2,\dots,c_{s_i}$.

Niech $q_1,q_2,\dots,q_t$ będą różnymi pieriwastkami, o krotnościach odpowiednio $s_1,s_2,\dots s_t$. 
Ogólna postać rozwiązania homogenicznego równania rekurencyjnego liniowego o stałych współczynnikach:
$$\begin{gathered}
h_n=h_n^{(i)}+h_n^{(2)}+\dots+h_n^{(t)}
\end{gathered}$$
W celu rozwiązania niehomogenicznego równania rekurencyjnego liniowego o stalych współczynnikach wykonujemy następujące kroki:
1. znajdujemy rozwiązanie ogólne odpowiedniego równania homogenicznego
2. znajdujemy rozwiązanie szczególne równania niehomogenicznego
3. łączymy oba rozwiązania z wykorzystaniem wartości początkowych

Wykonanie kroku (2) wymaga próby wykorzystania różnych form rozwiązania szczególnego $h_n$ w zależności od postaci czynnika niehomogenicznego $b$. W szczególności:
 - gdy $b$ jest wielomianem stopnia $k$ to za testowane rozwiązanie szczególne $h_n$ przyjmujemy również wielomain stopnia $k$
 - gdy $b=sp^n$ to próbujemy wykorzystać $h_n=tp^n$

Powodzenie w wykonaniu kroku (2) zależy od postaci wielomianu charakterystycznego.