### Zasada włączeń i wyłączeń 
#### 2024-10-24
##### Poprzednia: [[Dyskretna - 2]]
##### Nastepna: [[]]
##### Zadania: [[]]

#temat #matematyka_dyskretna  

--- 
1. - 
2. Ile jest trzycyfyfrowych liczb które nie są podzielne ani przez 3 ani przez 7
3. Ile jest liczb z zakresu $<1,2,...,1000>$ które są niepodzielne ani przez 4 ani przez 5 ani przez 6
4. Ile jest liczb z zakresu $<1,2,...,10 000>$ które nie są ani $a^2$ ani $a^3$ gdzie $a \in \mathbb{N}$ 
5. Mamy ciąg liter {M,A,T,H,I,S,F,U,N} ile jest jego permutacji które nie tworzą słów "MATH", "IS", "FUN"
6. mamy równanie $x_1+x_2+x_3+x_4=12$ gdzie $x_n$ jest całkowite nieujemne. Ile jest rozwiązań gdzie $x_i \leq 5$
7. mamy zbiór $\{0,1,2,...,9\}$ ile jest permutacji tego zbioru gdzie pierwsza liczba jest $\lt 8$ a ostatni element $\gt 0$ żadna nieparzysta nie jest punktem stałym. ( w sensie że nie zostanie na swoim miejscu)

2 
$$\begin{gathered}
250 - \ podzielnych \ przez \ 4\\
200 - \ podzielnych \ przez \ 5\\
166 - \ podzielnych \ przez \ 6  \ \ \ \ (bo \lfloor \frac{1000}{6} \rfloor)\\
50 - p. 20 \\
33 - p.30\\ 
83 - p.12\\
NWW(4,5,6)=60, \ \ \ 16-p.60\\
1000-(250+200+166-50-33-83+16)
\end{gathered}$$
5
$$\begin{gathered}
Wszystkie - 9!\\
Takie \ gdzie \ math \ - 6\cdot5!=6!\\
Takie \ gdzie \ is \ - 8 \cdot 7!=8!\\
Takie \ gdzie \ fun \ - 7\cdot6!=7!\\
\\
fun \ + \ math - 4! \ (tak \ jakbysmy \ skleili \ math \ oraz \ fun \ jako \ jeden \ element)\\ 
fun \ + \ is - 6!\\
math \ + \ is - 5!\\
math \ + \ is \ + \ fun - 3! \ (bo \ mamy \ 3 \ elementy \ - \ kazde \ slowo)\\
wynik = 9!-6!-8!-7!+5!+4!+6!-3!
\end{gathered}$$
---
6
$$\begin{gathered}
{{12+4-1} \choose {12}}-{4 \choose 1}\cdot {{6+4-1} \choose 6}+{4 \choose 2} \cdot 1\\
\\
{{12+4-1} \choose {12}} - tak \ rozwiazywalismy \ te \ zadania \ typu \ x_1+x_2+x_3+x_4=12 \\
{4\choose 1}\cdot {{6+4-1} \choose 6} - wybieramy \ jedna \ sposrod \ zmiennych \ i \ rozkladamy \ kolejne \\ kulki \ w \ pudelkach \ 
\end{gathered}$$