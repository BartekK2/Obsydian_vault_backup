### Zasada włączeń i wyłączeń

^2ceee3

#### 2024-11-21
##### Poprzednia: [[Dyskretna - 2]]
##### Następna: [[Dyskretna - 4]]
##### Zadania: [[Dyskretna - zadania 3 zasada włączeń i wyłączeń]]

#matematyka_dyskretna  #zasada_wlaczen_i_wylaczen

--- 
### Informacje
*Def.*
Liczba elementów zbioru X posiadających co najmniej jedną z własnoći $P_1,P_2,\dots,P_t$ wynosi:

$$\begin{gathered}
|A_1\cup A_2 \cup \dots \cup A_t| = \sum^{}_{1\leq i \leq t} |A_i| -\sum_{1\leq i \leq j \leq t}|A_i \cap A_j| +\\+\sum^{}_{1\leq i \leq j \leq k \leq t}|A_i \cap A_j \cap A_k|-\dots + (-1)^{t+1}|A_1\cap A_2 \cap \dots \cap A_t|
\end{gathered}$$

*Przykład:*
$|A_1 \cup A_2 \cup A_3|=|A_1|+|A_2|+|A_3|-|A_1 \cap A_2|-|A_2\cap A_3| - |A_1\cap A_3|+|A_1\cap A_2\cap A_3|$

![[diagram-20241121.png]]
*Przykład zastosowania:*
Ile jest liczb z zakresu $\ [1,1000]$ które są niepodzielne ani przez 4 ani przez 5 ani przez 6
$$\begin{gathered}
250 - \ podzielnych \ przez \ 4 - A_1\\
200 - \ podzielnych \ przez \ 5- A_2\\
166 - \ podzielnych \ przez \ 6- A_3  \ \ \ \ (bo \lfloor \frac{1000}{6} \rfloor)\\
50 - p. 20 - A_1\cap A_2\\
33 - p.30 - A_2\cap A_3\\ 
83 - p.12 - A_1\cap A_3\\
NWW(4,5,6)=60, \ \ \ 16-p.60 - A_1\cap A_2 \cap A_3\\
1000-(250+200+166-50-33-83+16)\\\\
Mowimy \ o \ NWW \ wtedy \ juz \ wiemy \ ze \ liczba \ jest \ podzielna \ przez \ obie\\
nie \ musimy \ np \ szukac \ wielokrotnosci \ 4\cdot 6=24 \ w \ 1000\ wystarcza \ wielokrotnosci \ 12\\ \ bo \ to \ najmniejsza \ liczba \ podzielna \ i \ przez \ 4 \ i \ 6. 
\end{gathered}$$

**Natomiast w drugą stronę, to znaczy gdy szukamy liczby elementów nie posiadających żadnych z tych własności, to po prostu od wszystkich możliwych odejmujemy te które mają co najmniej jedną z tych własności**

Liczba elementów zbioru $X$ nieposiadających żadnej z własności $P_1,P_2,P_3\dots P_t$ wynosi:
$$\begin{gathered}
|\overline{A_1}\cap \overline{A_2}\dots \cap \overline{A_t}| = |X|-|A_1\cup A_2\dots \cup A_t| = |X| - \sum_{1\leq i \leq t}{|A_i|}+\sum_{1\leq i \lt j\leq t}{|A_i\cap A_j|}\\-\sum_{1\leq i \leq j \leq k \leq t}|A_i \cap A_j \cap A_k|-\dots + (-1)^{t}|A_1\cap A_2 \cap \dots \cap A_t|
\end{gathered}$$

---
