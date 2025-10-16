
### Kwadraty łacińskie

**Def.**
Kwadratem łacińskim rzędu $n$ (o boku $n$) nazywamy tablicę rozmiaru $n\times n$, w której każda komórka zawiera element ze zbioru $S$ rzędu $n$ w taki sposób, że każdy symbol z $S$ występuje dokładnie raz w każdym wierszu i dokładnie raz w każdej kolumnie:

$$\begin{gathered}
\begin{bmatrix}
1&2&3\\
2&3&1\\
3&1&2
\end{bmatrix}, &
\begin{bmatrix}
a&b&d&c\\
b&c&a&d\\
c&d&b&a\\
d&a&c&b
\end{bmatrix}
\end{gathered}$$
---
### Ortagonalność kwadratów łacińskich

**Def.**
Dwa kwadraty łacińskie. $L$ i $L'$, rzędu $n$ są ortagonalne, jeśli wszystkie spośród $n^2$ par $(L(i,j),L'(i,j))$ są parami różne

$$\begin{gathered}
\begin{bmatrix}
1&2&3\\
2&3&1\\
3&1&2
\end{bmatrix}, &
\begin{bmatrix}
3&1&2\\
2&3&1\\
1&2&3
\end{bmatrix}\\\\
\end{gathered}$$

te dwa na przykład są ortagonalne.

**Twierdzenie:**
Dla każdego $n\geq 1, n\neq 2,6$ istnieje para ortogonalnych kwadratów łacińskich rzędu $n$.

---
#### Zbiór $MOLS(n)$, czyli zbiór kwadratów łacińskich wzajemnie ortogonalnych

**Def.**
Mówimy, że w zbiorze $L_1,L_2,\dots,L_m$ kwadraty łacińskie rzędu $n$ są wzajemnie ortogonalne (ozn. $MOLS(n)$), jeśli dla każdych $1\leq i \lt j\leq m$, $L_i$ oraz $L_j$ są ortogonalne. Niech $N(n)$ oznacza maksymalną liczbę kwadratów w zbiorze $MOLS(n)$.

Czyli $MOLS(n)$ to zbiór wszystkich wzajemnie ortogonalnych kwadratów łacińskich, $N(n)$ to liczba ich.

---
**Lemat:**
Dla każdego $n$ zachodzi $1\leq N(n)\leq n-1$

---
**Twierdzenie:**
Jeśli $q=p^k$ jest potęgą liczby pierwszej, wówczas $N(q)=q-1$.

---
### Częściowy kwadrat łaciński:

Częściowym kwadratem łacińskim rzędu $n$ nazywamy tablicę rozmiaru $n\times n$, w której każda komórka jest albo pusta albo zawiera element ze zbioru $S$ w taki sposób że każdy symbol z $S$ występuje co najwyżej raz w każdym wierszu i co najwyżej raz w każdej kolumnie.

$$\begin{gathered}
\begin{bmatrix}
a&b&d&c\\
&c&a&\\
c&&b&a\\
d&a&c&b
\end{bmatrix}
\end{gathered}$$
Częściowy kwadrat łaciński rzędu $n$, w którym co najwyżej $n-1$ komórek jest niepustych może zostać uzupełniony do kwadratu łacińskiego rzedu $n$.

Co implikuje że każdy kwadrat $n\times n$ może być kwadratem łacińskim.

---
**Def.**
Niech $a,b$ i $n$ będą liczbami naturalnymi spełniającymi zależność $a\times b=n$. Wówczas tablica rozmiaru $n\times n$ może zostać podzielona na rozłączne bloki, każdy z nich będący podtablicą rozmiaru $a\times b$. $(a-b)$ - *kwadratem sudoku* nazywamy kwadrat łaciński nad zbiorem symboli $\{1,2,\dots,n\}$, w którym każdy blok zawiera wszystkie symbole z $S$.

$$\begin{gathered}
\begin{bmatrix}
    \begin{array}{cc|cc}
      A & B&C&D\\
      C & D&B&A\\
      \hline
	  B & A&C&D\\
      D & C&A&B
    \end{array}
\end{bmatrix}
\end{gathered}
$$

---
**Def.**
$(a,b)$ - **zbiorem krytycznym Sudoku** nazywamy częściowy kwadrat łaciński $P$, który może zostać uzupełniony w sposób jednoznaczny do $(a,b)$ - kwadratu Sudoku, a ponadto usunięcie jakiejkolwiek niepustej komórki z $P$ zaburza jednoznaczność tego uzupełnienia.

Chodzi o to że już musimy mieć wpisane tyle że nie da się zbudować kwadratu łacińskiego na wiele sposobów, mamy już praktycznie zdefiniowany cały kwadrat łaciński w zbiorze krytycznym Sudoku, jedynie pozostaje dopisać brakujące elementy.

Innymi słowy:

**Zbiór krytyczny Sudoku to najmniejszy możliwy zbiór podanych cyfr, który jednoznacznie wyznacza rozwiązanie.**

---
**Lemat:**
Dla każdego $k, \ 17\leq k\leq 35$, istnieje $(3,3)$ - zbiór krytyczny Sudoku posiadający $k$ niepustych komórek.

Sudoku klasyczne to kwadrat $9\times 9$, podzielony na $9$ bloków $3\times 3$.

$k$ to liczba niepustych komórek, czyli liczba cyfr podanych w planszy Sudoku na starcie.

Twierdzenie mówi, że dla każdej wartości $k$ z zakresu $17\leq k\leq 35$ istnieje taki **zbiór krytyczny**, który zawiera dokładnie $k$ wpisanych cyfr i nadal prowadzi do unikalnego rozwiązania.

---

##### Zadania:

###### 1. Niech $L$ będzie kwadratem łacińskim rzedu $5$ o elmenetach ze zbioru $S=\{1,2,3,4,5\}$. Niech $L'$ oznacza częściowy kwadrat łaciński rzędu $5$, uzyskany z $L$ poprzez usunięcie elmentów z komórek w pierwszej i ostatniej kolumnie (w wyniku usunięcia komórki te stały się puste)

P/**F** Kwadrat rzędu $4$, utworzony z $L$ poprzez usunięcie ostatniej kolumny i usunięcie ostatniego wiersza, jest kwadratem łacińskim.

$$\begin{gathered}
\begin{bmatrix}
a&b&d&c&e\\
b&c&a&e&d\\
c&d&e&b&a\\
d&e&c&a&b\\
e&a&b&d&c\\
\end{bmatrix}\to 

\begin{bmatrix}
a&b&d&c\\
b&c&a&e\\
c&d&e&b\\
d&e&c&a\\
\end{bmatrix}
\end{gathered}$$
nie.

**P**/F Istnieją 4 inne kwadraty łacińskie rzędu $5$, tworzące wraz z $L$ zbiór $MOLS(5)$

Prawda, mamy twierdzenie które mówi że jeśli $q=p^k$, gdzie $q$ to rząd kwadratu, a p liczba pierwsza to mamy dokładnie $q-1$ kwadratów ortagonalnych. Czyli 4.

P/**F** $L'$ może zostać uzupełniony do kwadratu łacińskiego rzedu 5 w sposób jednoznaczny.

Chyba nie, wystarczy przecież zamienić kolumny.

$$\begin{gathered}
\begin{bmatrix}
a&b&d&c&e\\
b&c&a&e&d\\
c&d&e&b&a\\
d&e&c&a&b\\
e&a&b&d&c\\
\end{bmatrix}\to 

\begin{bmatrix}
&b&d&c&\\
&c&a&e&\\
&d&e&b&\\
&e&c&a&\\
&a&b&d&\\
\end{bmatrix}\\\\
\downarrow\\\\
\begin{bmatrix}
a&b&d&c&e\\
b&c&a&e&d\\
c&d&e&b&a\\
d&e&c&a&b\\
e&a&b&d&c\\
\end{bmatrix}\ \ \ \ \vee \ \ \ \ 
\begin{bmatrix}
e&b&d&c&a\\
d&c&a&e&b\\
a&d&e&b&c\\
b&e&c&a&d\\
c&a&b&d&e\\
\end{bmatrix}
\end{gathered}$$
---

P/**F** Każdy częściowy kwadrat łaciński o $n$ niepustych komórkach posiada uzupełnienie do kwadratu łacińskiego.

Powołując się na twierdzenie:
Częściowy kwadrat łaciński rzędu $n$, w którym co najwyżej $n-1$ komórek jest niepustych może zostać uzupełniony do kwadratu łacińskiego rzedu $n$.

---
###### 2. Niech $L'$ będzie częściowym kwadratem łacińskim rzędu $4$, w którym pierwszy wiersz ma postać $1,2,3,4$ a pozostałe komórki są puste. Niech $L''$ będzie częściowym kwadratem łacińskim rzędu 4 zawierającym $L'$, w którym wszystkie komórki w drugim wierszu są wypełnione, a pozostałe komórki są puste. Niech $L$ będzie kwadratem łacińskim rzedu 4 zawierajacym $L''$

P/**F** Liczba parami różnych częściowych kwadratów $L''$ wynosi $6\cdot 2!-4\cdot 1!=8$

$$\begin{gathered}
\begin{bmatrix}
1&2&3&4\\
&&II \ wiersz
\end{bmatrix}\\\\
II \ wiersz \ da \ sie \ obliczyc \ nieporzadkiem:\\
9
\\\\
\end{gathered}$$
Zatem muszą być przynajmniej 9 takich.

P/**F** $L''$ może zostać uzupełniony do $L$ w sposób jednoznaczny.

Nie, 

$$\begin{gathered}
\begin{bmatrix}
    \begin{array}{cc|cc}
      1 & 2&3&4\\
      4 & 1&2&3\\
      \hline
	  2 & 3&4&1\\
      3 & 4&1&2
    \end{array}
\end{bmatrix}
\begin{bmatrix}
    \begin{array}{cc|cc}
      1 & 2&3&4\\
      4 & 1&2&3\\
      \hline
	  3 & 4&1&2\\
      2 & 3&4&1
    \end{array}
\end{bmatrix}
\end{gathered}$$


Wystaczy zamienić kolejność ostatnich wierszy rozwiązanego kwadratu.


---
**P**/F Istnieją dwa wzajemnie ortagonalne kwadraty łacińskie rzędu 4 zawierające $L''$ 

$$\begin{gathered}
\begin{bmatrix}
    \begin{array}{cc|cc}
      1 & 2&3&4\\
      4 & 1&2&3\\
      \hline
	  2 & 3&4&1\\
      3 & 4&1&2
    \end{array}
\end{bmatrix}
\begin{bmatrix}
    \begin{array}{cc|cc}
      1 & 2&3&4\\
      4 & 1&2&3\\
      \hline
	  3 & 4&1&2\\
      2 & 3&4&1
    \end{array}
\end{bmatrix}
\end{gathered}$$

Wystarczy chyba sprawdzić czy te 2 są ortogonalne. 

(2,3),(3,4),(4,1),(1,2),(3,2),(4,3),(1,4),(2,1)

Wygląda na to że są.

---
P/**F** Nie istnieją trzy inne kwadraty łacińskie rzedu 4, tworzące wraz z $L$ zbiór $MOLS(4)$
$q=2^2=4, N(4)=3$

---
