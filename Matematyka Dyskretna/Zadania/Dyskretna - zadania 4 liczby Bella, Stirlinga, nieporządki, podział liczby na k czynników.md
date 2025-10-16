### Liczby Bella, Stirlinga, nieporządki, podział liczby na k czynników
#### 2024-11-26
##### Lekcja: [[Dyskretna - 4]]

#matematyka_dyskretna  #liczba_bella #liczba_stirlinga #podzial_liczby_n_na_k #nieporzadki 

---
###### 1. Na ile różnych sposobów można ulokować n osób w dokładnie k spośród m ponumerowanych pokoi?
$$\begin{gathered}
\binom{m}{k}\cdot S(n,k)\cdot k!
\end{gathered}$$

Wybieramy pokoje z dostępnych $\to$ Dzielimy osoby na grupy $\to$ przydzielamy ich do wybranych pokoi

---
###### 2. Ile jest różnych liczb co najwyżej 20-cyfrowych, które zawierają wszystkie 10 cyfr?

$$\begin{gathered}
\sum^{20}_{k=10}{(S(20-k,10) \cdot 9\cdot 9!)}
\end{gathered}$$

- Np przy 12 cyfrowej liczbie chcemy wiedziec ile mamy mozliwosci przydziału cyfr. To znaczy np. 3 cyfry 1 reszta cyfr po 1 cyfrze. $(S(k,10))$
- $\cdot 9$ bo 9 możliwych cyfr na pierwszym miejscu, nie może być 0
- $9!$ bo załóżmy że każda cyfra jest zupełnie inna, to znaczy $1_1$ to nie to samo co $1_2$ więc mamy 11 pozycji na cyfre do rozłożenia i zostało 11 cyfr z czego niektóre będą się powtarzać
  $11!$ dzielimy przez wybór jednej z 11 cyfr, a następnie przez wybór jednej z 10 cyfr (założyliśmy że rozróżnialne na potrzeby wyjaśnienia) i wychodzi 9!

Chyba to wyjaśnienie ma sens, nie wiem nie rozumiem w 100% tego $9\cdot 9!$

---
###### 3. Na ile różnych sposobów Arek można składać w listopadzie codzienne wizyty u jednej z 12 koleżanek, tak by ostatecznie odwiedzić wszystkie z nich?

$$\begin{gathered}
S(30,12)\cdot 12!
\end{gathered}$$

---
###### 4. Na ile różnych sposobów można przydzielić 12 z 20 rycerzy do obrony dokładnie 3 z 4 baszt zamku?

$$\begin{gathered}
\binom{20}{12}\cdot \binom{4}{3}\cdot S(12,3)
\end{gathered}$$
---
###### 5. Na ile różnych sposobów kapitan piratów może ukryć skarb złożony z tysiąca złotych dukatów w 13 identycznych dostatecznie dużych skrzyniach?

$$\begin{gathered}
\sum^{13}_{i=0}{P(1000,i)}\\\\
Alternatywny \ sposob:\\
x_1+x_2+\dots+x_{13}=1000\\
\binom{1000+13-1}{13-1}=\binom{1012}{12}
\end{gathered}$$

---
###### 6. Na ile różnych sposobów można rozmieścić w n skrytkach zapasowe klucze do nich tak, aby w każdej był jeden klucz i tak by istniało k takich skrytek, do których włamanie się pozwoli otworzyć wszystkie pozostałe?

$$\begin{gathered}
\sum^{k}_{i=1}{c(n,i)}=\sum^{k}_{i=1}{s(n,i)}\\\\ (to \ te \ sama \ liczba \ alternatywne \ oznaczenie)
\end{gathered}$$

Sumujemy każdy możliwy rozkład permutacji $n$ elementowej na $k$ cykli ponieważ albo pierwsza skrytka pozwoli nam na otwarcie wszystkich itd itd albo będziemy musieli się włamać aż do k skrytek (k cykli) które otworzy nam reszte.

---
###### 7. Ile jest takich permutacji zbioru $\{1, 2,\dots , n\}$ mających $k$ cykli, takich, że jedynka jest w cyklu L-elementowym?

$$\begin{gathered}
\binom{n-1}{l-1}\cdot (l-1)! \cdot c(n-l,k-1)\\
\end{gathered}$$

---
###### 8. Ile jest takich permutacji zbioru A, w których liczby parzyste są na przemian z nieparzystymi i nie ma punktów stałych, gdy:

a) $A = \{1, 2,\dots , 9\}$?
$$\begin{gathered}
D_5\cdot D_4=!5\cdot !4 \ \ \ (Inne \ oznaczenie)
\end{gathered}$$

b) $A = \{1, 2, \dots , 10\}$?
$$\begin{gathered}
(D_5)^2 \cdot 2
\end{gathered}$$
---
###### 9. Na ile sposobów można podać obiad $2n$ osobom, z których każda zamówiła inną zupę i inne drugie danie, tak aby połowa z nich dostała swoją zupę, ale nie swoje drugie danie, a druga połowa odwrotnie?

$$\begin{gathered}
\binom{2n}{n}\cdot !n \cdot !n
\end{gathered}$$
---
