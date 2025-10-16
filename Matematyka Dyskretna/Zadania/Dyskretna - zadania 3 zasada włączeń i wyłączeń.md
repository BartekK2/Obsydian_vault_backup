### Zasada włączeń i wyłączeń
#### 2024-11-25
##### Lekcja: [[Dyskretna - 3]]

#matematyka_dyskretna  #zasada_wlaczen_i_wylaczen

---
###### 1. Ile jest różnych dzielników liczby $10!$ podzielnych przez $20,24$ lub $32$?

Z zadania z kombinatoryki:
$10! = 1\cdot2\cdot3..\cdot10$, rozkład na liczby pierwsze: $\{2,3,2,2,5,2,3,7,2,2,2,3,3,5,2\}=\{2_8, 3_4, 5_2,7\}$
zatem każdy dzielnik musi być iloczynem pewnej wybranej liczby tych czynników pierwszych:
wzór na liczbę dzielników $(k_1+1)\cdot(k_2+1)\cdot(k_3+1)...\cdot(k_n+1)$ bo każdy dzielnik to: 
$p_1^{k_1}\cdot p_2^{k_2} \cdot p_3^{k_3} ... \cdot p_n^{k_n}$ więc dochodząc do konkluzji naszym wynikiem jest $9\cdot5\cdot3\cdot2=270$

Ile zatem jest takich dzielników które są podzielne przez 20?
$d_{20}=5\cdot 2^2 \cdot k$ gdzie $k$ możemy wybrać na (nie uwzględniając już wybranych dzielników do 20) $(k_2+1)\cdot (k_3+1)\cdot (k_5+1)\cdot (k_7+1)$
czyli $7\cdot 5 \cdot 2 \cdot 2=140$ sposobów.

Ile jest takich dzielników które są podzielne przez 24?
$d_{24}=3\cdot 2^3 \cdot k$ gdzie $k$ możemy wybrać na (nie uwzględniając już wybranych dzielników do 24) $(k_2+1)\cdot (k_3+1)\cdot (k_5+1)\cdot (k_7+1)$
czyli $6\cdot 4 \cdot 3 \cdot 2=144$ sposobów.

Ile jest takich dzielników które są podzielne przez 32?
$d_{32}=2^5 \cdot k$ gdzie $k$ możemy wybrać na (nie uwzględniając już wybranych dzielników do 32) $(k_2+1)\cdot (k_3+1)\cdot (k_5+1)\cdot (k_7+1)$
czyli $4\cdot 5 \cdot 3 \cdot 2=120$ sposobów.

Ile jest takich dzielników które są podzielne przez 20 oraz 24?
$NWW(20,24)=120$
$$\begin{gathered}
120|2\\
60|2\\
30|3\\
10|2\\
5|5\\
120=2^3\cdot 5\cdot 3\\
d_{120}=2^3\cdot 5\cdot 3 \cdot k
\end{gathered}$$
gdzie $k$ można wybrać na $6\cdot 2 \cdot 4 \cdot 2=96$

Ile jest takich dzielników które są podzielne przez 20 oraz 32?
$NWW(20,32)=160$
$$\begin{gathered}
160|2\\
80|2\\
40|2\\
20|2\\
10|2\\
5|5\\

160=2^5\cdot 5\\
d_{160}=2^5\cdot k
\end{gathered}$$
gdzie $k$ można wybrać na $4\cdot 5 \cdot 2 \cdot 2=80$

Ile jest takich dzielników które są podzielne przez 24 oraz 32?
$NWW(24,32)=96$
$$\begin{gathered}
96|2\\
48|2\\
24|2\\
12|2\\
6|2\\
3|3\\

96=2^5\cdot 3\\
d_{96}=2^5\cdot 3\cdot k
\end{gathered}$$
gdzie $k$ można wybrać na $4\cdot 4 \cdot 3 \cdot 2=96$

Ile jest takich dzielników które są podzielne przez 20, 24 oraz 32?
$NWW(20,24,32)=480$
$$\begin{gathered}
480|2\\
240|2\\
120|2\\
60|2\\
30|2\\
15|3\\
5|5\\


480=2^5\cdot 3\cdot 5\\
d_{480}=2^5\cdot 3\cdot 5\cdot k
\end{gathered}$$
gdzie $k$ można wybrać na $4\cdot 4 \cdot 2 \cdot 2=64$


$$\begin{gathered}

d|A_{20}\cup A_{24} \cup A_{32}|=|A_{20}|+\\ |A_{24}| + |A_{32}| - |A_{20}\cap A_{24}| - |A_{20}\cap A_{32}| -\\ |A_{32}\cap A_{24}|+A_{24} \cap A_{32} \cap A_{20}|=140+120+144-96-80-96+64=196
\end{gathered}
$$

###### 2. Na ile sposobów można rozsadzić cztery małżeństwa przy okrągłym stole, tak aby by nikt nie siedział obok swojego małżonka?

$$\begin{gathered}
X=7! \ (wszystkie \ mozliwe \ rozstawienia)\\
|A_i| \ i \in \{1,2,3,4\}\\
|A_i| = 4\cdot 2 \cdot 6!\\
|A_i \cap A_j | \ i,j \in \{1,2,3,4\}\\
|A_i \cap A_j | = \binom{4}{2}\cdot 2^2 \cdot 5!\\
|A_i \cap A_j \cap A_k| = \binom{4}{3}\cdot 2^3 \cdot 4!\\
|A_i \cap A_j \cap A_k \cap A_l| = \binom{4}{4}\cdot 2^4 \cdot 3!\\

\end{gathered}$$

*Wyjaśnienie:*
$|A_i| = 4\cdot 2 \cdot 6!$
4  - wybór małżeństwa
2  - rozstawienie MŻ, ŻM
6! - permutacja osób przy stole gdzie jedno małżeństwo traktujemy jako jedną jednostke także mamy $\frac{7!}{7}$
itd.

---
###### 3. Na ile sposobów można rozsadzić cztery kobiety i czterech mężczyzn przy okrągłym stole, tak aby żadne dwie kobiety nie siedziały naprzeciw siebie?

$$\begin{gathered}
X - 7! \ (wszystkie \ mozliwe \ rozstawienia \ ludzi)\\
|A_i| = \binom{4}{2} \cdot 6! \ (2 \ kobiety \ naprzeciwko \ siebie)\\
|A_i \cap A_j| = \binom{4}{4}\cdot 5!\ (4 \ kobiety \ naprzeciwko \ siebie)\\

\end{gathered}$$
**SPRAWDŹ PÓŹNIEJ OD KOGOŚ**

---
###### 4. Ile jest ciągów długości n złożonych z cyfr {0, 1, . . . , 9}, w których każda z cyfr 1, 3, 6 występuje co najmniej raz? 

$$\begin{gathered}
10^{n} - \ (wszystkie \ ciagi)\\
9^{n} - \ (np \ 1 \ nie \ wystapi)\\
8^{n} - \ (np \ 1 \ i \ 3 \ nie \ wystapi)
7^{n} - \ (1, \ 3 \ i \ 6 \ nie \ wystapi)\\
\\
10^n-9^n\cdot 3 + \binom{3}{2}\cdot 8^n + 7^n
\end{gathered}$$
---
###### 5. Na ile sposobów można utworzyć zestawów składających się z 11 owoców, jeżeli mamy do dyspozycji 13 bananów, 10 jabłek i 4 pomarańcze, a każdy zestaw musi zawierać przynajmniej dwa banany i nie może zawierać więcej niż trzy jabłka?

**Ten przypadek że mamy przynajmniej 2 banany (gdy chcemy zrobić odwrotność czyli mniej niż 2 banany) traktujemy w ten sposób że wszystkie możliwe - te gdzie banany $\geq 2$ i nam wychodzi wtedy przypadek gdzie banany $\lt 2$.

$$\begin{gathered}
2\leq b\leq 13, 0\leq j\leq 3, 0\leq p\leq 4\\\\
Bez \ zadnych \ warunkow:\\
b+j+p=11\\
\binom{11+3-1}{3-1}=\binom{13}{2}=78\\
A_b \ (b\lt 2)\\
(b-2)+j+p=9\\
\binom{9+3-1}{3-1}=\binom{11}{2}=55\\
78-55=23
\\\\
A_p \ (p\geq 5)\\
b+j+(p-5)=6\\
\binom{6+3-1}{3-1}=\binom{8}{2}=28\\\\
A_j \ (j\geq 4)\\
b+(j-4)+p=7\\
\binom{7+3-1}{3-1}=\binom{9}{2}=36\\\\
---\\
A_b \land A_p \ (b\lt 2 \land p\geq 5)\\
b+j+(p-5)=6\\
\binom{6+3-1}{3-1}=\binom{8}{2}=28\\
(b-2)+j+(p-5)=4\\
\binom{4+3-1}{3-1}=\binom{6}{2}=15\\
28-15=13
\\\\
A_b \land A_j \ (b\lt 2 \land j\geq 4)\\
b+(j-4)+p=7\\
\binom{7+3-1}{3-1}=\binom{9}{2}=36\\
(b-2)+(j-4)+p=5\\
\binom{5+3-1}{3-1}=\binom{7}{2}=21\\
36-21=15
\\
A_p \land A_j \ (p\geq 5 \land j\geq 4)\\
b+(j-4)+(p-5)=2\\
\binom{2+3-1}{3-1}=\binom{4}{2}=6\\
---\\
A_b \land A_p \land A_j \ (p\geq 5 \land b \lt 2 \land j\geq 4)\\
b+(j-4)+(p-5)=2\\
\binom{2+3-1}{3-1}=6\\\\

(b-2)+(j-4)+(p-5)=0\\
\binom{0+3-1}{3-1}=1\\
6-1=5\\
|\overline{A_1}\cap \overline{A_2}\dots \cap \overline{A_t}| = |X|-|A_1\cup A_2\dots \cup A_t| = |X| - \sum_{1\leq i \leq t}{|A_i|}+\sum_{1\leq i \lt j\leq t}{|A_i\cap A_j|}\\-\sum_{1\leq i \leq j \leq k \leq t}|A_i \cap A_j \cap A_k|-\dots + (-1)^{t}|A_1\cap A_2 \cap \dots \cap A_t|\\\\
78-23-28-36+13+15+6-5=20
\end{gathered}$$---
###### 6. Ile jest funkcji ze zbioru n-elementowego na k-elementowy, które nie są surjekcjami?

$$\begin{gathered}
k^n - \ (wszystkie \ funkcje)\\
1) \ n\lt k \ (nie \ ma \ suriekcji) (wiec \ k^n)\\\\
2) \ n\gt k\\
k^n-\sum^{k}_{j=0}{(-1)^j\cdot \binom{k}{j}\cdot (k-j)^n}\\
3) \ n=k\\
k^n-n!
\end{gathered}$$

Czyli korzystamy z wzoru na liczbe elementów zbioru który nie zawiera żadnej z danych własności (naszymi własnościami są to że nie używamy iluś elementów).

$$\begin{gathered}
|\overline{A_1}\cap \overline{A_2}\dots \cap \overline{A_t}| = |X|-|A_1\cup A_2\dots \cup A_t| = |X| - \sum_{1\leq i \leq t}{|A_i|}+\sum_{1\leq i \lt j\leq t}{|A_i\cap A_j|}\\-\sum_{1\leq i \leq j \leq k \leq t}|A_i \cap A_j \cap A_k|-\dots + (-1)^{t}|A_1\cap A_2 \cap \dots \cap A_t|
\end{gathered}$$

---
###### 7. Na ile sposobów można utworzyć ciągów długości $2n$ takich, że każda liczba $i \in \{1, . . . , n\}$ występuje dokładnie dwa razy, przy czym żadne dwa kolejne wyrazy nie są równe?

$$\begin{gathered}
\frac{2n!}{2^n}- n\cdot \frac{(2n-1)!}{2^{n-1}}+\binom{n}{2}\cdot\frac{(2n-2)!}{2^{n-2}}\dots \binom{n}{n}\cdot \frac{(2n-n)!}{2^{n-n}}\\\\

\sum^{n}_{i=0}{\binom{n}{i}\cdot \frac{(2n-i)!}{2^{n-i}}}
\end{gathered}$$
---
###### 8. Na ile sposobów można... informatyków, filozofów i ludożerców na pewnej wyspie, na której mieszka 300 dzikusów, z których każdy jest informatykiem, filozofem lub ludożercą, jeżeli połowa ludożerców to filozofowie, połowa filozofów to informatycy, połowa informatyków to ludożercy, a żaden z ludożerców nie zajmuje się filozofią i informatyką jednocześnie?

**DOKOŃCZ JAK BĘDZIESZ MIAŁ SIŁY NA TEN SHIT**
