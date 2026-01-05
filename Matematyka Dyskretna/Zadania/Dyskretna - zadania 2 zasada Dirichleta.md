### Zasada pudełkowania Dirichleta
#### 2024-11-16
##### Lekcja: [[Dyskretna - 2]]

#matematyka_dyskretna  #zasada_pudelkowa 

---
###### 1. Każdy punkt płaszczyzny pomalowano na jeden z kolorów: czerwony lub zielony. Wykaż, że istnieją dwa punkty tego samego koloru odległe od siebie o 1.

Jeżeli rozważymy trójkąt równoboczny (kwadrat też by w sumie zadziałał) to mamy 3 wierzchołki a tylko 2 kolory do wyboru więc któryś z wierzchołków musi mieć ten sam kolor co inny. W tym przypadku naszymi pudełkami będą kolory a wierzchołki obiektami, któreś z 2 pudełek (kolorów) musi mieć 2 obiekty (wierzchołki).
![[diagram-20241116 1.png]]

---
###### 2. Udowodnij, że w dowolnej grupie $n + 2$ różnych liczb całkowitych są dwie, których różnica lub suma dzieli się przez $2n$.

Reszty z dzielenia przez $2n$: $\{0,1,2,3...,2n-2,2n-1\}$ jeżeli podzielimy go na zbiór par:
$\{1,2n-1\}, \{2,2n-2\},...,\{n-1,n+1\},\{n\},\{0\}$ to zauważamy że ma $n+1$ takich par. Jeśli wrzucimy $n+2$ liczb do owych pudełek to w którymś pudełku muszą być 2 takie liczby a wtedy ich różnica/suma będzie podzielna przez $2n$.

---
###### 3. Udowodnij, że wśród $k$ punktów dowolnie wybranych z koła o promieniu $1$ są dwa, których odległość nie przekracza $1$ jeżeli:
- k=7
  Możemy to sobie zwizualizować wpisując sześciokąt foremny w okrąg, przekątne sześciokąta foremnego tworzą nam 6 trójkątów o każdym z boków równych 1. Zatem w jednym z tych trójkątów muszą być 2 punkty. A maksymalna odległość 2 punktów w trójkącie równobocznym (i ogólnie $\frac{1}{6}$ okręgu o promieniu=1) wynosi 1.
  ![[diagram-20241116 (1).png]]
- k=6
  Tutaj musimy zastosować pewien trik. Najpierw rozmieszczamy sobie punkty, potem dzielimy okrąg na sześciokąt foremny tak żeby jedna z przekątnych przechodziła przez dany punkt. Zostało nam wtedy 5 punktów do rozmieszczenia. Jeżeli rozmieścimy je w którymkolwiek trójkącie w którego boku znajduje sie pierwszy rozmieszczony punkt wtedy ich odległość jest $\leq 1$, a jeżeli będziemy je próbować rozmieszczać w pozostałych 4 częściach okręgu to w którejś będą musialy się znajdować 2 punkty.
  ![[diagram-20241116 (2).png]]
---
###### 4. W pewnym kraju jest 66 miast. Każde dwa połączone są jednym z czterech środków komunikacji (kolej, autobus, statek, samolot). Wykaż, że istnieją trzy miasta, takie, że można odbyć podróż pomiędzy nimi ”po trójkącie” używając tylko jednego środka komunikacji.

Zasada dirichleta mówi nam że jeśli mamy $m$ rzeczy i $n$ pudełek a każde pudełko musi mieć minimum jedną rzecz, to w jednym z pudełek musi być minimum $\lceil \frac{m}{n}\rceil$ rzeczy.
Więc:
$\lceil \frac{66}{4} \rceil=17$ - Czyli minimum 17 miast ma jeden ze środków transportu np. samolot
$\lceil \frac{17}{3} \rceil=6$ - Czyli minimum 6 z tych 17 miast ma również połączenie np. samolot
$\lceil \frac{6}{2} \rceil=3$ - Czyli minimum 3 z tych 6 miast ma również połączenie np. samolot

---
###### 5. Wykaż, że w dowolnym ciągu $n$ liczb naturalnych można wskazać pewną liczbę kolejnych wyrazów, których suma jest podzielna przez $n$.

Sum prefiksowych jest łącznie $S_1, S_2, ..., S_n$ - czyli $n$.
Możliwe reszty z dzielenia tych sum przez $n$ - $\{0,1,2,...,n-1\}$
Jeżeli którakolwiek z reszt = 0 to mamy spełnioną tezę.
Jeśli żadna nie jest to mamy n sum i n-1 reszt więc przynajmniej dwie sumy muszą mieć taką samą reszte a ich różnica będzie podzielna przez n.

---
###### 6. Udowodnij, że dla dowolnej dodatniej liczby całkowitej istnieje taka jej niezerowa wielokrotność, którą można zapisać w systemie dziesiętnym używając wyłącznie cyfr 0 i 1.

Tutaj trzeba pójść troche "na około" tzn nie skupijamy się na tym żeby liczba była postaci np:
$$\begin{gathered}
101010001
\end{gathered}$$
Ale postaci:
$$\begin{gathered}
111110000
\end{gathered}$$
Co osiągniemy przez odjęcie od siebie dwóch liczb stworzonych *tylko za pomocą jedynek.*
Powiedzmy że naszą liczbą jest liczba $n$. Zatem stwórzmy sobie $n+1$ takich liczb:
$$\begin{gathered}
n+1\left\{
\begin{array}{1}
1\\
11\\
111\\
...
\end{array}
\right.\\
\end{gathered}$$
Ich różnica jest stworzona z cyfr 0 i 1.
Wśród tych $n+1$ liczb stworzonych z jedynek muszą być dwie liczby które przy dzieleniu przez $n$ dają taką samą reszte z dzielenia:
$$\begin{gathered}
Dla \ n=3\\
4\left\{
\begin{array}{1}
1, \mod{3}=1\\
11, \mod{3}=2\\
111, \mod{3}=0\\
1111, \mod{3}=1\\
\end{array}
\right.\\\\
Np: \ 1 \ oraz \ 1111 \ maja \ ta \ sama \ reszte:\\
1111-111=3a+1-3b-1=3(a-b), \ a,b \in \mathbb{Z}
\end{gathered}$$

---

###### 7. Uzasadnij, że istnieje niezerowa liczba całkowita k, dla której część ułamkowa (mantysa $x$ czyli $x-\lfloor x\rfloor$) liczby $k \sqrt{2}$ jest mniejsza od 0,01.

Przyjmijmy np: 100 pierwszych k:
Wtedy wrzucamy każde $k\sqrt{2}$ do pudełka $n$ jeśli mantysa jest większa od $0,0n$ ale mniejsza od $0,0(n+1)$.
Wtedy wiemy że w którymś z pudełek muszą być przynajmniej dwie takie same mantysy (lub któraś mantysa mniejsza od 0,01).
Jeżeli żadna z mantys nie jest mniejsza od 0,01 wtedy mamy 2 różne $a,b$ których mantysa różnicy jest mniejsza od 0,01.

---
###### 8. Wykaż, że z dowolnego zbioru $n$ liczb całkowitych $(n \geq 3)$ da się wybrać trzy parami różne elementy $a,b,c$ w taki sposób, że liczba $a(b-c)$ jest podzielna przez n.

Przykład dla lepszego zobrazowania:
Przyjmijmy n=10, 10 liczb całkowitych - $\{17,23,4,93,9,8,7,5,11,18\}$ 
Albo któraś z tych liczb jest podzielna przez n i wtedy jest to nasze $a$.
Albo żadna z tych liczb nie jest podzielna przez n wtedy nasz zbiór reszt z dzielenia przez n:
$\{1,2,3,4,5,6,7,8,9\}$ - 9 takich reszt i mamy 10 liczb więc przynajmniej dwie mają tą samą reszte z dzielenia wtedy te 2 nasze liczby są $b$ oraz $c$. A ich różnica jest podzielna przez n.

Ogólny przypadek:
$a(b-c)=n\cdot k, a,b,c,n,k \in \mathbb{Z} \implies a=n\cdot m, \ m\in \mathbb{Z} \vee (b-c)=n\cdot i, \ i\in \mathbb{Z}$
Jeżeli mamy $n$ liczb, a zbiór reszt z dzielenia przez $n$ jest $n$ elementowy to wtedy:
- któraś z liczb może być podzielna przez $n$ (dawać reszte 0) - wtedy jest to $a$
  Albo:
- żadna z liczb nie jest podzielna przez $n \implies$ zbiór reszt z dzielenia tych liczb przez $n$ ma maksymalnie $n-1$ elementów a z zasady pudełkowej wiemy że wtedy przynajmniej 2 liczby mają tą samą reszte z dzielenia $\implies$ ich różnica jest podzielna przez $n$ (wtedy jest to nasze $b$ oraz $c$)

#### Olimpiada Matematyczna

---
###### 1. Wykaż, że wśród dowolnie wybranych 11 liczb naturalnych znajdują sie dwie, których cyfry jedności są równe.

Zbiór pudełek odpowiadających za cyfry jedności - $\{0,1,2,3,4,5,6,7,8,9\}$
Zbiór liczb - 11 liczb naturalnych.
$\lceil \frac{11}{10} \rceil=2$ - przynajmniej dwie liczby mają tą samą cyfre jedności.

---
###### 4. Danych jest 1001 liczb naturalnych. Udowodnij, że istnieje wśród nich 501 liczb parzystych lub 501 nieparzystych.
Trywialne $\lceil \frac{1001}{2} \rceil=501$, więc przynajmniej dwie liczby w tych samych pudełkach (albo parzystych albo nieparzystych)

---
###### 5. Danych jest 111 dodatnich liczb całkowitych. Wykaż, że spośród nich można wybrać 11 takich liczb, których suma jest podzielna przez 11.
Trywialne $\lceil \frac{111}{11} \rceil=11$. Więc przynajmniej 11 liczb mają tą samą reszte z dzielenia przez 11=r, zatem ich suma to:
$$\begin{gathered}
11\cdot (a_1+a_2+a_3+...+a_{11})+11\cdot r = 11\cdot (a_1+a_2+a_3+...+a_{11}+r)
\end{gathered}$$

Czyli jest podzielna przez 11.

---
###### 7. Na okręgu umieszczonych jest 101 dodatnich liczb całkowitych o sumie równej 300. Udowodnij, że istnieje taki łuk okręgu, że suma umieszczonych na nim liczb jest równa 200.
![[diagram-20241119 (3).png]]
Rozważmy następujące sumy:
$$\begin{gathered}
100\left\{
\begin{array}{1}
a_1\\
a_1+a_2\\
a_1+a_2+a_3\\
...\\
a_1+a_2+a_3+...+a_{100}\\
\end{array}\right.
\end{gathered}$$
Załóżmy że żadna z tych sum nie jest równa 200 (lub 100 - co również by spełniło warunki zadania). Zatem mamy 100 sum różnych od 200 i od 100 ale mniejszych od 300.
Podzielmy każdą z sum przez 100:
$$
\begin{gathered}
Reszty:\\
\\
100\left\{
\begin{array}{1}
1\\
2\\
3\\
...\\
99\\
\cancel{100}, \ zalozylismy \ ze \ nie \ ma \ 100 \ i \ 200
\end{array}\right.
\end{gathered}
$$
Także mamy 100 różnych sum z czego każda ma 99 możliwości na resztę. Także przynajmniej dwie sumy:
$$\begin{gathered}
a_1+a_2+a_3+...+a_k\\
oraz\\
a_1+a_2+a_3+...+a_l\\
maja \ te \ same \ reszty
\end{gathered}$$
Więc ich różnica (coś jakby wycinek okręgu?) dzieli się przez 100. Zatem jest wielokrotnością 100 ale mniejszą od 300. Także jest albo 100 albo 200.

---
###### 9. Danych jest 12 różnych dwucyfrowych liczb naturalnych. Udowodnij, że można tak wybrać pewne dwie z nich, aby ich różnica była liczbą postaci $\overline{aa}$ (gdzie a jest cyfrą).

Liczba $\overline{aa}$ jest równa $11\cdot a, a\leq 9$. A różnica dwóch różnych dwucyfrowych liczb o tej samej reszcie dzielenia przez 11 wynosi $a\cdot 11 + r - (b\cdot 11+r)=(a-b)\cdot 11$ gdzie $(a-b) \lt 10$ ponieważ mówimy tylko o dwucyfrowych liczbach ($a\cdot 11+r$ -  2 cyfrowa, $a,b - 1$ cyfrowa).

Reszt z dzielenia przez 11 jest 11 a mamy 12 różnych liczb więc przynajmniej 2 liczby mają tą samą reszte z dzielenia.

---
