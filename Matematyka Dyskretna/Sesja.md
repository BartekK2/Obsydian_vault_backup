###### 1. Zakładamy $1\leq m\leq k\lt n$. Podaj W.

$$\begin{gathered}
\binom{n}{k}=\binom{W}{n-k}, W=n\\
\binom{n}{k}=\binom{n-1}{k}+\binom{n-1}{W},W=k-1\\
\binom{n}{k}\binom{k}{m}=\binom{n}{m}\binom{n-m}{n-k}\\
k\binom{n}{k}=n\binom{n-1}{W}, W=k-1
\end{gathered}$$

###### 2. Uzupełnij

$$\begin{gathered}
0\lt k\lt n, S(n,k)=S(n-1,k-1)+k\cdot S(n-1,k)\\
n\geq 1, S(n,n)=1\\
n\geq 2, S(n,2)=\frac{2^n-2}{2!}=2^{n-1}-1\\
n\geq 3, S(n,n-2)=\binom{n}{3}+\frac{1}{2}\binom{n}{2}\binom{n-2}{2}
\end{gathered}$$
---
###### 3. Rozważmy ciągi o elementach ze zbioru $X=\{1,2,3,4,5,6,7,8,9\}$

- Liczba ciągów długości 7, w których sumy każdej sąsiedniej pary elementów są nieparzyste

Skoro sumy sąsiednich par są nieparzyste to znaczy że ma być albo:

Np,P,Np,P$\dots$ 
albo
P,Np,P,Np,$\dots$

$$\begin{gathered}
5^44^3+5^34^3
\end{gathered}$$
- Liczba ciągów niemalejących długości 6

$$\begin{gathered}
\binom{9+6-1}{6-1}=\binom{14}{5}
\end{gathered}$$

- Liczba ciągów różnowartościowych długości 5
$$\begin{gathered}
\binom{9}{5}\cdot 5!
\end{gathered}$$
- Liczba permutacji takich, że dla każdego parzystego $n,f(n)\neq n$

$$\begin{gathered}
9!-\binom{4}{1}\cdot 8!+\binom{4}{2}\cdot 7!-\binom{4}{3}\cdot 6!+\binom{4}{4}\cdot 5!
\end{gathered}$$

---
###### 4. $a_n$ - liczba ciągów długości n złożonych z $\{2,3,4,5,6\}$ gdzie 3 i 5 mają występować parzystą liczbe razy a 4 i 6 nieparzystą. L jest zbiorem wszystkich takich ciągów

Ile jest w L liczb z parami różnymi cyframi?

$$\begin{gathered}
a_0=0\\
a_1=1\\
a_2=2\\
a_3=3!=6\\
a_4=44\\
\end{gathered}$$
Czyli dla $n\geq 4$ nie mogą być wszystkie różne, więc wystarczy dodać $a_2,a_3$ i otrzymujemy $2!+3!$ 

Funkcja tworząca $a_n$ to:

$$\begin{gathered}
f(x)=(1+\frac{x}{1!}+\frac{x^2}{1!}+\dots )(1+\frac{x^2}{2!}+\frac{x^4}{4!}+\dots)^2(x+\frac{x^3}{3!}+\dots)^2
\end{gathered}$$

Bo:
- składnik $(1+\frac{x}{1!}+\frac{x^2}{1!}+\dots )$ odpowiada za 2, które pojawia się dowolną ilość razy
- składnik $(1+\frac{x^2}{2!}+\frac{x^4}{4!}+\dots)^2$ odpowiada za parzyste (parzyste potęgi i silnie) wystąpienie liczb $3,5$ których jest $2$ więc do potęgi $2$
- składnik $(x+\frac{x^3}{3!}+\dots)^2$ odpowiada za nieparzyste (nieparzyste potęgi i silnie) wystąpienie liczb $4,6$ których jest $2$ więc do potęgi $2$

należy pamiętać że:
$$\begin{gathered}
f_1(x)=1+\frac{x}{1!}+\frac{x^2}{2!}+\frac{x^3}{3!}+\dots = e^x\\\\
\text{Co można zauważyć po prostu z wzoru taylora:}
\end{gathered}$$
Więc można zapisać funkcje tworzącą jako:

$$\begin{gathered}
(1+\frac{x}{1!}+\frac{x^2}{1!}+\dots )=e^x\\
(1+\frac{-x}{1!}+\frac{x^2}{1!}+\frac{-(x^3)}{3!}+\frac{x^4}{4!}+\frac{-(x^5)}{5!})=e^{-x}\\
(1+\frac{x^2}{2!}+\frac{x^4}{4!}+\dots)=\frac{e^x+e^{-x}}{2}\\\\
f(x)=(1+\frac{x}{1!}+\frac{x^2}{1!}+\dots )(1+\frac{x^2}{2!}+\frac{x^4}{4!}+\dots)^2(x+\frac{x^3}{3!}+\dots)^2=\\
=e^x(\frac{e^x+e^{-x}}{2})^2(\frac{e^x-e^{-x}}{2})^2=e^x(\frac{(e^x+e^{-x})^2(e^x-e^{-x})^2}{16})=\\=e^x\frac{(e^{2x}-e^{-2x})^2}{16}=\frac{e^{5x}-2e^x+e^{-3x}}{16}
\end{gathered}$$

Nierekurenycjny wzór na $a_n$:

$$\begin{gathered}
\frac{1}{16}(5^n-2\cdot 1^n+(-3)^n)
\end{gathered}$$

---
###### 5. S=$\{1,2,3,4,5,6\}$ Generujemy wszystkie permutacje $S$ w porządku leksykograficznym. Numerujemy je $1,2,\dots,6!$

W porządku leksykograficznym oznacza że porządkujemy je "rosnąco" elementami tzn:
$$\begin{gathered}
a_1=123456\\
a_2=123465\\
a_3=123546\\
a_4=123564
\end{gathered}$$

Dla każdej permutacji $\alpha$ typu $1^i2^j$ gdzie $i+2j=6$, liczba permutacji odwrotnych wynosi?

Typ permutacji $A^iB^jC^g$ to oznacza że mamy $i$ cykli $A$ elementowych, $j$ cykli $B$ elementowych $\dots$ 

Czyli np jak $i=1, j=3$:

$$\begin{gathered}
(A)(BCD)(EFG)
\end{gathered}$$
Pytają nas o to ile jest takich cyklów odwrotnych to znaczy jeśli $B\to C$ to musi w odwrotnej $C\to B$:

$$\begin{gathered}
A\to A\\
C\to B\\
B\to D\\
D\to C\\
F\to E\\
E\to G\\
G\to F\\
(A)(CBD)(FEG) - 1
\end{gathered}$$

Tutaj można zauważyć że po prostu odpowiedzią zawsze jest jeden bo mamy konkretny cykl, konkretną permutacje i odwracamy jej kolejność, to nie ma chuja że może być wiele sposóbów na które to odwrócimy.

---
Liczba permutacji, w których $1,3,4$ występują na kolejnych pozycjach:

$$\begin{gathered}
(1,2,3,4,5,6)\\
(1,3,4)(2,5,6), \text{Permutujemy }(2,5,6)=3!\\
A \ (1,3,4)\text{ Wstawiamy w dowolne miejsce tzn:}\\
\text{mamy 4 miejsca na to jesli potraktujemy to jako jeden element}\\
\text{I musimy spermutować }(1,3,4)=3!\\\\
3!\cdot 3!\cdot 4=3!\cdot 4!
\end{gathered}$$

---
Na której pozycji jest $<4,3,2,1,6,5>$?

To jest uporządkowane rosnąco więc przed tą permutacją stoją permutacje z 1,2,3 na pierwszym miejscu, permutacje z 4 na pierwszym miejscu a na drugim 1,2, permutacje z 4 na pierwszym, 3 na drugim, 1 na trzecim, permutacje 4321 z 56 na końcu i ostatecznie nasza permutacja:

$$\begin{gathered}
3\cdot 5!+2\cdot 4!+3!+1+1
\end{gathered}$$

---
Następnik $<1,2,5,6,4,3>$ to: $<1,2,6,3,4,5>$

---
###### 6. Niech $G$ będzie grafm rzędu 9 powstałym przez zwinięcie jednej z krawędzi w grafie Petersena:

![[diagram-20250211 (1).png]]
To jest graf Peteresena, jest to graf zaproponowany przez niego jako typ grafu którego krawędzi nie da się pokolorować trzema kolorami, nie ma mostów (krawędzi których usunięcie rozspójnia graf), ma stopień 3. ma ścieżke Hamiltona, nie jest grafem planarnym.

$$\begin{gathered}
rząd - 10\\
rozmiar - 15\\
średnica - 2\\
stopień - 3\\
liczba \ chromatyczna - 3\\
indeks \ chromatyczny - 4\\
promień - 2\\
\end{gathered}$$

Zwinięcie krawędzi oznacza połączenie wierzchołków tej krawędzi w jeden wierzchołek.

Minimalna liczba krawędzi aby graf był trasowalny (posiadający ścieżke Hamiltona czyli ścieżke która odwiedza każdy wierzchołek tylko raz) - 0

Możemy zwinąć krawędź albo w otoczce: (dowolnie bo jeżeli obrócimy graf to wyjdzie na to samo)

![[diagram-20250211 (2).png]]
Albo w środku:
![[diagram-20250211 (3).png]]
![[diagram-20250211 (5).png]]
###### 8. Niech $G$ będzie grafem rzedu $2n+1$ dla $n\geq 2$ utworzonym poprzez rozdzielenie jednej z krawędzi $K_{n,n}$.

Dla $n\geq 3$, liczba ścieżek hamiltonowskich w $\overline{G}$ to:

$$\begin{gathered}
(n-1)!^2(n-1)^2+2(n-2)(n-1)!^2+4n(n-1)!^2=\\
=(n-1)!^2(n^2+4n-3)
\end{gathered}$$
---
###### 1. Niech $X=\{1,2,3,4\}$, $Y=\{1,2,3,4,5,6\}$, $f: X\to Y$ oraz $g: Y\to X$

Liczba tych odwzorowań $f$ które są malejące wynosi: $\binom{6}{4}=\binom{6}{2} \ \checkmark$
Liczba tych odwzorowań $g$ które są nierosnące wynosi: $\binom{6+4-1}{4-1}=\binom{9}{3}=\binom{9}{6}\ \checkmark$
Liczba tych odwzorowań $f$ które są iniekcjami $\binom{6}{4}\cdot 4!=\frac{6!}{2}$
Liczba tych odwzorowań $g$ które są suriekcjami: (czyli każdy element z $X$ musi być): 
z zasady włączeń i wyłączeń $4^6-4\cdot 3^6+\binom{4}{2}2^6-\binom{4}{3}\cdot 1^6$

---
###### 2. Niech $S=\{1,2,3,4,5,6\}$ oraz $A$ będzie algorytmem generowania listy wszystkich permutacji zbioru w porządku leksykograficznym; każda permutacja ma przypisaną pozycję na liście $i=1,2,\dots, 6!$

P/**F** Następnikiem permutacji $<1,2,6,5,4,3>$ jest permutacja $<1,3,6,5,4,2>$
*ponieważ następną permutacją jest: $<1,3,2,4,5,6>$*

**P**/F Permutacja $<4,3,1,2,6,5>$ występuje na pozycji 410

$$\begin{gathered}
|<1,\dots>|=5!\\
\vdots \\(1,2,3)\\
|<4,1,\dots>|=4!\\
\vdots \\
(1,2)\\
|<4,3,1,2,5,6>|\\
|<4,3,1,2,6,5>|\\ 
\end{gathered}$$

$5!\cdot 3+4!\cdot 2+2=360+48+2=410\ \checkmark$

P/**F** Elementy 1,2,5 występują na trzech kolejnych pozycjach łącznie w 24 permutacjach.

$$\begin{gathered}
<(1,2,5),\dots >\\
<(2,1,5),\dots >\\
<(5,1,2),\dots >\\
\vdots \\
<x,(1,2,5),\dots >\\
<x,(2,1,5),\dots >\\
<x,(5,1,2),\dots >\\
\vdots \\
<x,y,(1,2,5),\dots >\\
<x,y(2,1,5),\dots >\\
<x,y(5,1,2),\dots >\\
\end{gathered}$$

$$\begin{gathered}
4\cdot 3!\cdot 3!=144
\end{gathered}$$
---
**P**/F Każda permutacja $\alpha$ typu $1^i2^j,i+2j=6$ posiada permutacje odwrotną $\alpha^{-1}:\alpha^{-1}=\alpha$

Tak, każda permutacja ma odwrotną. (dokładnie jedną)

---
###### 3. Niech $a_n$ oznacza liczbę ciągów ternarnych (składających się z cyfr $0,1,2$) o długości $n$, w których krotność wystąpienia cyfry $1$ jest parzysta, a krotność wystąpienia cyfry $2$ nieparzysta.

P/**F** Funkcja tworząca dla ciągu $\{a_n\}$ ma postać $A(n)=(1+x+x^2\dots)(1+x^2+x^4+\dots)(x+x^3+x^5+\dots)$


Nie, funkcja tworząca tego ciągu ma postać:
$$\begin{gathered}
f(x)=(1+\frac{x^2}{2!}+\frac{x^4}{4!}\dots)(x+\frac{x^3}{3!}+\frac{x^5}{5!}\dots )(1+\frac{x}{1!}+\frac{x^2}{2!}+\frac{x^3}{3!})
\end{gathered}$$

**P**/F $A(n)=\frac{e^{3x}+e^{-x}}{4}$

$$\begin{gathered}
f(x)=\frac{e^x+e^{-x}}{2}\cdot \frac{e^x-e^{-x}}{2}\cdot e^x=\frac{e^{3x}-e^{-x}}{4}\\
\end{gathered}$$

P/**F** $a_i=\frac{3^n-(-1)^n}{4i!}$

$$\begin{gathered}
a_i=\frac{3^n-(-1)^n}{4}
\end{gathered}$$
**P**/F $a_5=61$

$$\begin{gathered}
a_5=\frac{3^5-(-1)^5}{4}=\frac{244}{4}=61
\end{gathered}$$

---
###### 4. Które z poniższych własności są prawdziwe dla liczb Strirlinga

**P**/F $S(n,1)=1$ dla każdego $n\geq 1$(bo możemy rozdzielić do 1 wora n cukierków na 1 sp.)
**P**/F $S(n,n-1)=\binom{n}{2}$ dla każdego $n\geq 1$ (bo wybieramy 2 które będa razem, reszta po 1)
P/**F** $S(n,2)=2^{n+1}+1$ dla każdego $n\geq 2$ 
Podpiszmy worki na cukierki, a potem usuniemy podpisy:
$$\begin{gathered}
\frac{2^n-2}{2}=2^{n-1}-1
\end{gathered}$$
P/**F** $S(n,k)=S(n,k-1)+k\cdot S(n-1,k-1)$ dla $0\lt k\lt n$ 

Nie, $S(n,k)=S(n-1,k)+k\cdot S(n-1,k)$ ponieważ albo cukierek jest w swoim własnym worku, sam albo rozdzielamy reszte do **dokładnie** $k$ worków i ostatni cukierek do jednego z nich.

---
###### 5. Niech $G$ będzie grafem rzędu $n=2^3$, w którym wierzchołki są wyznaczone przez parami różne ciągi binarne długości 3. Dwa wierzchołki są połączone krawędzią wtedy i tylko wtedy, gdy różnica symetryczna odpowiadających im ciągów ma nieparzystą liczbe jedynek.

Różnica symetryczna zbiorów to jest suma zbioru minus część wspólna, zatem zakładam że różnica symetryczna ciągów to jest operacja $\Delta$ taka że: $1010\ \Delta\ 1100 = 0110$


![[diagram-20250211 (6).png]]

**P**/F Minimalna liczba krawędzi, jakie należy usunąć z G, aby otrzymany graf był niespójny wynosi 4.

Tak bo wystarczy usunąć wszystkie krawędzie od wierzchołka najmniejszego stopnia w tym przypadku.

P/**F** Maksymalna liczba krawędzi, jakie można usunąć z $G$, aby otrzymany graf nadal był spójny wynosi 8

Można sobie znaleźć ścieżke łączącą wszystkie wierzchołki o długości 7, a wszystkich krawędzi jest 14 zatem nie.

P/**F** **G** nie posiada dekompozycji na cykle długości 4.

Są takie cykle np 110->111>000>001>110 oraz 101>010>011>100>101

P/**F** $G$ nie posiada zamkniętej drogi Eulera

Musi posiadać bo stopień każdego wierzchołka jest parzysty (wynosi 4)

---
###### 6. Niech $G$ będzie grafem rzędu $2n+2, n\geq 2$ utworzonym z grafu pełnego dwudzielnego $K_{n,n}$ poprzez rozdzielenie dwóch incydentnych krawędzi. Wyznacz liczbę chromatyczną oraz indeks chromatyczny grafu $G$

Krawędzie incydentne to takie które mają wspólny wierzchołek.

**P**/F Graf $G$ jest dwudzielny 

tak, rozdzielenie krawędzi nic nie zmienia w grafie dwudzielnym 

P/**F**
Dla każdego $n\geq 2$ $\chi(G)=3$ 

Fałsz, skoro jest dwudzielny to musi mieć liczbe chromatyczną równą 2.

P/**F** Liczba chromatyczna grafu G wynosi 3 ponieważ dwa wierzchołki stopnia $n$ są sąsiadami jednego wierzchołka stopnia 2

Nie ma to żadnego sensu + jest dwudzielny więc liczba $=2$ 


P/F Indeks chromatyczny grafu $G$ wynosi $n+1$ ponieważ liczba krawędzi w $G$ wynosi $n^2+2$ 
chyba tak ale nie wiem jakie jest tu powiązanie z liczbą krawędzi 

![[Pasted image 20250211222650.png]]
na czerwono zaznaczony graf $K_5$ a graf z czarnymi krawędziami złożony z 7 wierzchołków w którym każdy stopień wierzchołka jest parzysty jest cyklem eulera więc jest cyklem $C_n$ który można usunąć by otrzymać graf $K_5$ który nichuja planarny nie jest

![[Pasted image 20250211224552.png]]

$H_6$ chyba jest planarny

---
###### 1. Niech $s_n$ oznacza liczbę ciągów ternarnych (składających się z cyfr 0,1 i 2) o długości $n$, w których nie występują podciągi $00$ oraz $01$. Wyznacz rekurencyjną zależność dla $s_n, n\geq 1$, a następnie znajdź wzór na $s_n$ w postaci nierekurencyjnej.

$$\begin{gathered}
a_1=3\\
a_2=7\\
S_n=a_n+b_n+c_n\\
a_n- takie \ S_n \ ze \ \ konczy \ sie \ 0\\
b_n- takie \ S_n \ ze \ \ konczy \ sie \ 1\\
c_n- takie \ S_n\ ze \ \ konczy \ sie \ 2\\\\
a_n=b_{n-1}+c_{n-1}\\
b_n=b_{n-1}+c_{n-1}\\
c_{n}=S_{n-1}=a_{n-1}+b_{n-1}+c_{n-1}\\\\
S_n=b_{n-1}+c_{n-1}+b_{n-1}+c_{n-1}+a_{n-1}+b_{n-1}+c_{n-1}=\\
=a_{n-1}+3b_{n-1}+3c_{n-1}=2S_{n-1}-a_{n-1}+b_{n-1}+c_{n-1}=\\
=2S_{n-1}-b_{n-2}-c_{n-2}+b_{n-2}+c_{n-2}+S_{n-2}=2S_{n-1}+S_{n-2}
\end{gathered}$$

**ciekawa sztuczka jeżeli 2 podciągi są od siebie uzależnione**

---
###### 4. W koszyku znajduje się 10 bananów, 8 jabłek, 6 pomarańczy oraz 4 gruszki. Niech $a_i$ oznacza liczbę parami różnych zestawów składających się z i owoców; każdy taki zestaw zawiera co najmniej jednego banana, co najwyżej dwa jabłka, liczba pomarańczy jest parzysta, a liczba gruszek nieparzysta. Skonstruuj funkcję tworzącą dla ciągu. $\{a_i\}^\infty_{i=1}$ Znajdź $a_5$.

$$\begin{gathered}
f(x)=(x+x^2+x^3+\dots+x^{10})(1+x+x^2)(1+x^2+x^4+x^6)(x+x^3)\\\\
f(x)=B\cdot J\cdot P\cdot G
\end{gathered}$$

Jeżeli to jest dobrze to:
$$\begin{gathered}
a_5:\\
f(x)'=(x+x^2+x^3+x^4+x^5)(1+x+x^2)(1+x^2+x^4)(x+x^2)=\\\\
(3x^5+3x^4+3x^3+2x^2+x)(1+x^2+x^4):\\\\
(7x^5+5x^4+4x^3+2x^2+x)(x+x^2):\\\\
(5x^5+4x^4+2x^3+x^2|4x^5\\\
a_5=9
\end{gathered}$$

---
###### 3. Niech $s_n$ będzie liczbą dodatnich, całkowitych rozwiązań równania $x_1+x_2+x_3=n$, w których $x_1$ jest parzyste, $x_2$ nieparzyste, $x_3\in \{2,3\}$

Funkcja tworząca dla ciągu $\{s_n\}$:
$$\begin{gathered}
(x^2+x^3)(x^2+x^4+\dots)(x+x^3+x^5+\dots)
\end{gathered}$$

$$\begin{gathered}
I) \ n \ parzyste\\
x_1+x_2+3=n\\
x_1+x_2=n-3\\
2a+2b-1=n-3\\
2a+2(b+1)=n-2\\
a+(b'+1)=\frac{n-2}{2}\\
a+b'=\frac{n-4}{2}\\
\binom{\frac{n-4}{2}+2-1}{2-1}=\frac{n-2}{2}=\frac{n}{2}-1
\end{gathered}$$

$$\begin{gathered}
II)\  n \ nieparzyste\\
x_1+x_2+x_3=n\\
x_1+x_2+2=n\\
x_1+x_2=n-2\\
2a+2b-1=n-2\\
2a+2b=n-1\\
a+(b'+1)=\frac{n-3}{2}\\
a+b'=\frac{n-3}{2}\\
\binom{\frac{n-4}{2}+2-1}{2-1}=\frac{n-1}{2}-1
\end{gathered}$$

Czyli dokładnie to samo, jednakże musi nam wyjść przecież liczba całkowita zatem można założyć że to będzie podłoga z tego ułamka.

Nierekurenycjny wzór na $s_n,n\geq 1$ ma postać:

$$\begin{gathered}
\left\{
\begin{matrix}
a_n=\lfloor \frac{n-1}{2}\rfloor -1, n\geq 3\\
a_0=a_1=a_2=0!!!!
\end{matrix}
\right.
\end{gathered}$$

$s_5=1$
$s_{24}=10$

---
###### 3b) Niech $s_n$ będzie liczbą dodatnich, całkowitych rozwiązań równania $x_1+x_2+x_3=n$, w których $x_1$ jest parzyste, $x_2$ nieparzyste, $x_3=\{1,2\}$

$$\begin{gathered}
x_1+x_2+x_3=n,\ \ \  n \ parzyste\\
x_1+x_2+1=n\\
x_1+x_2=n-1\\
2a+2b-1=n-1\\
2a+2b=n\\
a+b=\frac{n}{2}\\
a+(b'+1)=\frac{n}{2}\\
a+b'=\frac{n}{2}-1\\
\binom{\frac{n}{2}-1+2-1}{2-1}=\frac{n}{2}
\end{gathered}$$


$$\begin{gathered}
x_1+x_2+x_3=n,\ \ \  n \ nieparzyste\\
x_1+x_2+2=n\\
x_1+x_2=n-2\\
2a+2b-1=n-2\\
2a+2b=n-1\\
a+b=\frac{n-1}{2}\\
a+(b'+1)=\frac{n-1}{2}\\
a+b=\frac{n-1}{2}-1\\
\binom{\frac{n-1}{2}2-1-1}{2-1}=\frac{n-1}{2}
\end{gathered}$$

$$\begin{gathered}
\frac{n-1}{2}, n=2k+1\\
\frac{n}{2}, n=2k\\
jest \ rownowazne \ z \\
\lfloor \frac{n}{2}\rfloor 
\end{gathered}$$
Nierekurencyjny wzór:

$S_n=\lfloor \frac{n+2}{2}\rfloor$
$S_2=1$ bo 0+1+1=2
$S_3=1$ bo 0+1+2=3
$S_{22}=11$
$S_{24}=12$

---
###### 9. Niech $G$ będzie grafem rzędu $8$, utworzonym z grafu pełnego dwudzielnego $K_{3,3}$ poprzez rozdzielenie dwóch incydentnych krawędzi. Znajdź liczbę parami nierównoważnych pokolorowań wierzchołków grafu $G$ za pomocą 2 kolorów.

**P**/F Grupa automorfizmów grafu $G$ ma rząd $2$

P/**F** W grupie automorfizmów grafu $G$ występuje permutacja będąca cyklem długości $4$

P/F W indeksie cyklicznym grupy automorfizmów wszystkie monomiany występują ze współczynnikiem $1$.

P/F Liczba nierównoważnych pokolorowań wynosi 120.

---
### Poprzedni egzamin ($I$ termin)

###### 1. Niech $x=\{1,2,3,4\}, Y=\{1,2,3,4,5\}, f: X\to Y, g: Y\to X$

Liczba tych odwzorowań $f$, które są słabo monotoniczne:
$\binom{8}{4}\cdot 2-5$

Liczba tych odwzorowań $g$, które są słabo monotoniczne:
$\binom{8}{4}\cdot 2-4$

Liczba tych odwzorowań $f$ które są silnie rosnące oraz $f(3)=4$

$$\begin{gathered}
2,3, 4,5\\
1,2, 4,5
\end{gathered}$$
2

Liczba tych odwzorowań $g$, które są malejące i $g(3)=2$
0

Liczba tych odwzorowań $f$ dla których $|f(X)|=3$
$$\begin{gathered}
\binom{5}{3}\cdot 3^4-\binom{5}{3}\binom{3}{2}2^4+\binom{5}{3}\binom{3}{1}1^4
\end{gathered}$$

Liczba tych odwzorowań $g$ dla których $|g(Y)|=3$ 
$$\begin{gathered}
\binom{4}{3}\cdot 3^5-\binom{4}{3}\cdot \binom{3}{2}2^5+\binom{3}{1}\binom{4}{3}1^5
\end{gathered}$$

Liczba tych odwzorowań $f$, w których $f(1)\neq f(4)$

$$\begin{gathered}
5^4-5^3
\end{gathered}$$
Liczba tych odwzorowań $g$, dla których $g(1)\neq g(3)$
$$\begin{gathered}
4^5-4^4
\end{gathered}$$
---
###### 2. Niech $s(n,k)$ oznacza liczbę Stirlinga pierwszego rodzaju, czyli liczbę tych permutacji zbioru $n$-elementowego, które w rozkładzie mają $k$ cykli

Dla każdego $n\geq 1$, wartość $s(n,1)=\frac{n!}{n}=(n-1)!$

Dla każdego $0\lt k\lt n$, zależność rekurencyjna na $s(n,k)$ ma postać:
$s(n,k)=s(n-1,k-1)+(n-1)\cdot s(n-1,k)$

Dla każdego $n\geq 2$ wartość $s(n,2)=\sum^{n-1}_{i=1}{\binom{n}{i}\cdot (n-1)! \cdot \frac{1}{2}}$

Dla każdego $n\geq 3$ wartość $s(n,n-2)=\binom{n}{2}\cdot \binom{n-2}{2}\cdot \frac{1}{2}+\binom{n}{3}\cdot 2!$

Dla każdego $n\geq 4$ wartość $s(n,n-3)=\binom{n}{4}\cdot 3!+\binom{n}{3}\cdot 2!\cdot \frac{(n-3)(n-4)}{2}+\binom{n}{2}\binom{n-2}{2}\binom{n-4}{2}\frac{1}{3!}$

Dla każdego $n\geq 2$ wartość $s(n,n-1)=\binom{n}{2}$

---
###### 3. Niech $L$ będzie listą w porządku antyleksykograficznym tych podziałów liczby 20, w których każdy składnik jest parzysty: każdy podział ma nierosnąco uporządkowane składniki oraz jednoznacznie przypisaną pozycje $i$ $i=(1,2,3\dots)$ na tej liście.

(20,0)
(18,2)
(16,2,2)
(14,6)
$\dots$
Ich łączna liczba to podział liczby 10 na x składników 

---


Podział $(8,8,2,2)$ występuje na pozycji:

Jeżeli mamy:
(20,0)
(18,2)
(16,2,2)
(14,6)

to można zauważyć że po wypisaniu początkowych wyrazów aż do 8:

20
18
16
14
12
10

Zadanie sprowadza się do policzenia podziałów $\frac{(n-i)}{2}$ tzn:

20-20=0 **ten składnik też liczymy mimo że P(0)=0**
20-18=2 $P(\frac{2}{2})=P(1)=1$
20-16=4 P(2)=1+1=2
20-14=6 P(3)=1+1+1=3
20-12=8 P(4)=1+2+1+1=5
20-10=10 P(5)=1+2+2+1+1=7

I teraz już można ręcznie policzyć albo analogicznie stosując powyższą metode, lecz przesuwając się w prawo:
8,8,4
8,8,2,2

8,8,2,2 znajduje sie na 21 pozycji

---
Powyższy podpunkt daje nam automatycznie odpowiedź na pytanie o pozycje podziału (12,6,2)

Do 12 mamy 7, potem mamy:

(12,8)
(12,6,2)

Czyli na pozycji 9.

---


Liczba tych podziałów w $L$, w których $6$ oraz $2$ występują jednocześnie:
$$P(n,k)=\sum^{k}_{i=0}{P(n-k,i)}\\\\ $$
$$\begin{gathered}
P(6)=\sum^{6}_{i=0}{P(6,i)}\\\\
P(6,0)=0\\
P(6,1)=1\\
P(6,2)=\sum^{2}_{i=0}{P(4,i)}=0+1+P(4,2)=\\
=1+\sum^{2}_{i=0}{P(2,i)}=1+1+1=3\\
P(6,3)=\sum^{3}_{i=0}{P(3,i)}=0+1+1+1=3\\
P(6,4)=\sum^{4}_{i=0}{P(2,i)}=1+1=2\\
P(6,5)=\sum^{5}_{i=0}{P(1,i)}=1\\
P(6,6)=1
\end{gathered}$$

Liczba tych podziałów w $L$, w których $4$ oraz $2$ występują jednocześnie:

analogicznie - 11

---
###### 4. Dla każdego $n\geq 0$, niech $a_n$ oznacza liczbe nieujemnych, całkowitoliczbowych rozwiązań równania $x_1+2x_2+4x_3=4n$

Suma tych składników musi być liczbą podzielna przez 4 zatem:

---

$I$ przypadek:

4$x_3$ - zawsze
$x_2$ - parzyste oraz $x_1$ postaci $4x$

$II$ przypadek:

4$x_3$ - zawsze
$x_2$ - nieparzyste oraz $x_1$ daje reszte z dzielenia przez 4 - dwa: 
$x_2=2b+1$, $x_1=4a+2$

(zapisanie tego z minusem jako np: $x_2=2b-1$, albo jakoś inaczej pozwoliłoby na to żeby rozwiązanie przyjmowało liczby ujemne do tej sumy $x_1+2x_2+4x_3$, więc taki sposób jest albo jedynym poprawnym, albo bezpiecznym i optymalnym)

---
$$\begin{gathered}
I:\\\\
x_1+2x_2+4x_3=4n\\
4a+2\cdot (2b)+4c=4n\\
a+b+c=n\\\\
\end{gathered}$$
A funkcja tworząca wtedy:
$$\begin{gathered}
f^1(x)=(1+x+x^2+x^3+\dots)\cdot (1+x+x^2+x^3+\dots)\cdot (1+x+x^2+x^3\dots)=\\
=(1+x+x^2+x^3+\dots)^3
\end{gathered}$$

$$\begin{gathered}
II:\\
x_1+2x_2+4x_3=4n\\
(4a+2)+2\cdot 2(b+1)+4c=4n\\
4a+4b+4c+4=4n\\
a+b+c+1=n\\\\
f^2(x)=x\cdot (1+x+x^2+x^3+\dots)^3
\end{gathered}$$


---
Łączymy oba przypadki w jedno rozwiązanie, jedną funkcje:

$$\begin{gathered}
f(x)=(x+1)(1+x+x^2+x^3+\dots)^3=\frac{x+1}{(1-x)^3}
\end{gathered}$$
---
$a_4=?$, można rozpisać sobie funkcje tworzącą lub rozwiązać najpierw podpunkt z rekurencyjną zależnością.

Zrobię na 2 sposoby:

$$\begin{gathered}
f(x)=(x+1)(1+x+x^2+x^3+\dots)^3\\\\
\text{Potrzebujemy jedynie te składniki które będą nam generowały współczynniki }\\
\text{przy }x^4\\\\
f'(x)=(x+1)(1+x+x^2+x^3+x^4)^3=\\=(1+x+x^2+x^3+x^4+x+x^2+x^3+x^4+x^5)
\cdot (1+x+x^2+x^3+x^4)^2\\\\
\text{Ponownie,potrzebujemy jedynie niektore skladniki wiec usuwamy od }x^5\\\\
f'(x)=(x+1)(1+x+x^2+x^3+x^4)^3=\\=(1+2x+2x^2+2x^3+2x^4)
\cdot (1+x+x^2+x^3+x^4)^2=\\
=(1+3x+2x^2+2x^3+2x^4+2x^2+2x^3+2x^4+x^2+2x^3+2x^4+x^3+2x^4+x^4)\\
\cdot (1+x+x^2+x^3+x^4)=(1+3x+5x^2+7x^3+9x^4)(1+x+x^2+x^3+x^4)=\\
=\dots x^4+3x^4+5x^4+7x^4+9x^4=25x^4
\end{gathered}$$

Zatem $a_4=25$

---
$II$ sposób z rekurencji o ile sie ją jakoś wymyśli, albo rozpisze z funkcji tworzącej....

$$\begin{gathered}
f(x)=\frac{x+1}{(1-x)^3}=\sum^{\infty}_{n=1}{a_nx^n}\\
\text{Możemy to robić na różne sposoby, spróbujmy przekształcić całką}\\\\
\int{f(x)\ dx}=\int{\frac{x+1}{(1-x)^3}\ dx}=\begin{vmatrix}
u=x-1\\
du=dx
\end{vmatrix}=-\int{\frac{u+2}{u^3}\ du}=\\
=-\int{\frac{1}{u^2}\ du}-2\int{\frac{1}{u^3}\ du}=\frac{1}{u}-2\frac{u^{-2}}{-2}=\frac{1}{u}+\frac{1}{u^2}=\frac{1}{x-1}+\frac{x-1}{(x-1)^2}=\\
=\frac{x}{(x-1)^2}\\\\
\frac{x}{(x-1)^2}=\sum^{\infty }_{n=1}{a_n\frac{x^{n+1}}{n+1}}\\\\
\frac{x+1}{(1-x)^3}-\frac{x}{(x-1)^2}=\sum^{\infty}_{n=1}{a_nx^n-a_n\frac{x^{n+1}}{n+1}}=\sum^{\infty}_{n=1}{a_n(x^n-\frac{x^{n+1}}{n+1}})\\
\frac{1-x^2}{(1-x)^3}=\sum^{\infty}_{n=1}{a_n(x^n-\frac{x^{n+1}}{n+1}})\\
\frac{1+x}{(1-x)^2}=\sum^{\infty}_{n=1}{a_n(x^n-\frac{x^{n+1}}{n+1}})\\
\end{gathered}$$

**DOKOŃCZ MOŻE SIE UDA XD**



$$\begin{gathered}
I - identycznosc\\
z_1^6\\\
II-obrot \ 90,270 \ os \ przez \ podstawy\\
2z_1^2z_4\\
III- obrot \ 180 \ os \ przez \ podstawy\\
2z_1^2z_2^2\\\\
IV - obrot \ śś\\
z_1^2z_2^2\\
V - obrot \ kk\\
2z_2^3\\\\
Indeks \ cykliczny: \frac{1}{8}(z_1^6+3z_1^2z_4+2z_1^2z_2^2+2z_2^3)
\end{gathered}$$

**ZRÓB WIERZCHOŁKI**


![[Pasted image 20250218181130.png]]

