
## Fortuna

### 13.12.2019  zestaw A

---
###### 1. Na ile różnych sposobów można rozdać 22 pary kajdanek sześciu milicjantom jeśli każdy musi dostać przynajmniej jedną parę, a żaden nie może dostać więcej niż cztery pary?

$$\begin{gathered}
x_1+x_2+x_3+x_4+x_5+x_6=22\\
Gdzie: \ 1\leq x_i \leq 4\\
(x_1+1)+(x_2+1)+(x_3+1)+(x_4+1)+(x_5+1)+(x_6+1)=22\\
y_1+y_2+y_3+y_4+y_5+y_6=16\\
Gdzie: 0\leq y_i\leq 3, y_i=x_i+1\\
Wszystkie \ mozliwosci:\\
\binom{16+6-1}{6-1}=\binom{21}{5}\\
Jedna \ powyzej \ 4:\\
6\cdot \binom{12+6-1}{6-1}\\
Dwie \ powyzej \ 4:\\
\binom{6}{2}\cdot \binom{8+6-1}{6-1}\\
Trzy \ powyzej \ 4:\\
\binom{6}{3}\cdot \binom{4+6-1}{6-1}\\
Cztery \ powyzej \ 4:\\
\binom{6}{4}\cdot \binom{0+6-1}{6-1}=\binom{6}{4}\\
Z \ zasady \ wlaczen \ i \ wylaczen:\\
\binom{21}{5}-6\cdot \binom{12+6-1}{6-1}+\binom{6}{2}\cdot \binom{8+6-1}{6-1}-
\binom{6}{3}\cdot \binom{4+6-1}{6-1}+\binom{6}{4}\cdot \binom{0+6-1}{6-1}=\binom{6}{4}
\end{gathered}$$

---
###### 2. Na ile różnych sposobów można rozmieścić w dwóch różnych celach o nieograniczonej pojemności S internowanych i B agentów, jeśli w każdej celi musi być agent i internowany, ale w żadnej nie może być więcej niż S − 4 internowanych?

$$\begin{gathered}
x_1+x_2=S\\
1\leq x_i\leq S-4\\
(x_1+1)+(x_2+1)=S\\
y_1+y_2=S-2\\
\binom{S-2+2-1}{2-1}=\frac{(S-1)!}{1!\cdot (S-2)!}=S-1\\
Złe:\\
W \ jednej \ celi \ przynajmniej \ S-3 \ internowanych:\\
z_1+z_2+S-3=S-2\\
2\cdot \binom{5+2-1}{2-1}=12\\
\\
x_1+x_2=B\\
1\leq x_i\\
y_1+y_2=B-2\\
\binom{B-2+2-1}{2-1}=B-1
\\\\
(S-13)\cdot (B-1)
\end{gathered}$$
---
###### 3. Na ile różnych sposobów może gęsiego maszerować konwój złożony z M milicjantów i A aresztowanych opozycjonistów, jeżeli każda dwójka aresztowanych opozycjonistów musi być rozdzielona przynajmniej dwójką milicjantów, a na początku i na końcu idzie milicjant?


$$\begin{gathered}
M.AMM.AMM.A.M\\
\binom{m-2(a-1)-2+a+1-1}{a+1-1}\cdot m!\cdot a!
\end{gathered}$$

---
###### 4. Rozwiąż równanie rekurencyjne:
$$\begin{gathered}
\left\{
\begin{matrix}
x_n=4x_{n-1}-3x_{n-2}+n^2, n \geq 2\\
x_0=7\\
x_1=9
\end{matrix}
\right.\\\\
f(x)=\sum^{\infty}_{n=0}{a_nx^n}=7+9x+\sum^{\infty}_{n=2}{a_nx^n}=
7+9x+\sum^{\infty}_{n=2}{(4a_{n-1}-3a_{n-2}+n^2)x^n}=\\=7+9x+\sum^{\infty}_{n=2}{4a_{n-1}x^n}-\sum^{\infty}_{n=2}{3a_{n-2}}x^n+\sum^{\infty}_{n=2}{n^2}x^n=\\=7+9x+4x\sum^{\infty}_{n=1}a_nx^n-3x^2\sum^{\infty}_{n=0}{a_nx^n}+\sum^{\infty}_{n=2}{n^2x^n}=\\=
7+9x+4x\cdot (f(x)-7)-3x^2\cdot f(x)+\sum^{\infty}_{n=2}{n^2x^n}=:\\
\sum^{\infty}_{n=2}{n^2x^n}:\\
\sum^{\infty}_{n=2}x^n=\frac{1}{1-x}\ /rozniczkujemy\\
\sum^{\infty}_{n=2}nx^{n-1}=\frac{1}{(1-x)^2}\ /\cdot x\\
\sum^{\infty}_{n=2}nx^n=\frac{x}{(1-x)^2}\ / rozniczkujemy\\
\sum^{\infty}_{n=2}n^2x^{n-1}=\frac{1+x}{(1-x)^3}\ / \cdot x\\
\sum^{\infty}_{n=2}n^2x^n=\frac{x+x^2}{(1-x)^3}\\\\
f(x)=7+9x+4x\cdot (f(x)-7)-3x^2\cdot f(x)+\frac{x+x^2}{(1-x)^3}\\
f(x)-4x\cdot f(x)+3x^2\cdot f(x)=7+9x-28x+\frac{x+x^2}{(1-x)^3}\\
f(x)(1-4x+3x^2)=7+9x-28x+\frac{x+x^2}{(1-x)^3}\\
f(x)=\frac{1}{1-4x+3x^2}\cdot (7+9x-28x+\frac{x+x^2}{(1-x)^3})\\
a_n=\frac{1}{1-4n+3n^2}\cdot (7+9n-28n+\frac{n+n^2}{(1-n)^3})
\end{gathered}$$

---
### 13.12.2019 zestaw B

###### 1. Na ile różnych sposobów można zorganizować dwa wspólne patrole wojskowo-milicyjne z udziałem W żołnierzy i M milicjantów, jeśli w każdym patrolu musi być żołnierz i milicjant, lecz w żadnym nie może być mniej niż pięciu żołnierzy?

$$\begin{gathered}
(x_1+1)+(x_2+1)=M, x_1,x_2\geq 1\\
y_1+y_2=M-2\\
\binom{M-2+2-1}{2-1}=\binom{M-1}{1}=M-1\\\\

a_1+a_2=W, 5\leq a_1, 5\leq a_2\\
b_1+b_2=W-10\\
\binom{W-10+2-1}{2-1}=\binom{W-9}{1}=W-9\\\\
Wynik:\\
(W-9)\cdot (M-1)\\
Zalozenia:\\
W\geq 10\\
M\geq 2
\end{gathered}$$

---
###### 2. Na ile różnych sposobów siedmiu opozycjonistów może zabrać z tajnej drukarni 32 paczki z ulotkami, jeśli każdy zabiera przynajmniej dwie paczki i nikt nie zabiera więcej niż sześć?

$$\begin{gathered}
Wszystkie \ (przynajmniej \ 2 ):\\
x_1+x_2+x_3+x_4+x_5+x_6+x_7=32\\
y_1+y_2+y_3+y_4+y_5+y_6+y_7=20\\
\binom{20+7-1}{7-1}=\binom{26}{6}\\
Złe \ (wiecej \ niz \ 6):\\
Jedno:\\
7+y_1+y_2+y_3+y_4+y_5+y_6+y_7=13\\
7\cdot \binom{13+7-1}{7-1}=\binom{19}{6}\cdot 7\\
Dwa:\\
14+y_1+y_2+y_3+y_4+y_5+y_6+y_7=6\\
\binom{7}{2}\cdot \binom{6+7-1}{7-1}=\binom{12}{5}\cdot \binom{7}{2}\\
Z  \ zasady \ wlaczen\ i \ wylaczen:\\
Wynik:\\
\binom{26}{6}-\binom{19}{6}\cdot 7+\binom{12}{5}\cdot \binom{7}{2}
\end{gathered}$$
---
###### 3. Na ile różnych sposobów mogą odbywać się spacery dookoła spacerniaka jeśli wszyscy idą gęsiego w jedną stronę równo odlegli od osoby za i przed, bierze w nich udział A internowanych i S strażników, a każda dwójka aresztowanych musi być rozdzielona przynajmniej jednym strażnikiem?

$$\begin{gathered}
.S.S.S.S.S.\\
AAA
\\
a!\cdot s!\cdot \binom{s+1}{a}
\end{gathered}$$
---
### 2020 - Zestaw A

###### 1. Jeśli ciągiem spełniającym równania $x_n -4x_{n-1}+3x_{n-2}=-4n-6$ oraz wartości początkowe: $x_0=2, \ x_1=12$ jest ciąg $x_n=A(r_1)^n+B(r_2)^n+an^2+bn+c$ oraz $r_1\leq r_2$ i $ac=0$ to:

---
###### 2. Jak powszechnie wiadomo Świętych Mikołajów jest dwóch - jeden mieszka w Finlandii, drugi w Norwegii. Niewielu ludzi jednak wie, że mają oni wspólne stado 8 reniferów, z których każdy ma za sobą od 1 do 38 lat służby (każdy różną liczbę). Sanie każdego Świętego Mikołaja może ciągnąć różna liczba reniferów, ale nigdy jeden lub dwa. Nie wszystkie zwierzęta muszą być użyte. Zgodnie z ustaleniami w tym roku pierwszy wybierał Święty Mikołaj norweski. Udowodnij, że mógł on wybrać dwa różne podzbiory reniferów (jeden na 6 grudnia, drugi na 24 grudnia) lecz mające tę samą sumę lat służby.

Ile różnych podzbiorów istnieje?
$$\begin{gathered}
\binom{8}{3}+\binom{8}{4}+\binom{8}{5}+\binom{8}{6}+\binom{8}{7}+\binom{8}{8}=\\
=56+70+56+28+8+1=219\\\\
\end{gathered}$$
Minimalnie stado może mieć 3 renifery, każdy z różną ilością lat służby a najmniej 1. Zatem stado może mieć minimalnie 1+2+3=6 lat służby łącznie, wtedy maksymalną ilość lat służby stado mogłoby mieć 1+2+3+38+37+36+35+34=186 (bo ustalając minimalną ilość łącznie lat służby przypisujemy już trzem reniferom ile mają lat) (zatem max wynika z min)

Zatem w bardziej ogólnym przypadku: $min=S_{min}$, $max=38+37+36+35+34+S_{min}$ 

$$\begin{gathered}
najmlodsze= S_1\leq S_2\dots \leq S_{219}=najstarsze\\
najmlodsze= S_1\leq S_2\dots \leq S_{219}=180+ najmlodsze\\

\end{gathered}$$
$\lceil \frac{219}{181} \rceil =2$ czyli z dirichleta wychodzi nam że co najmniej 2 mają taką samą ilość lat służby

---
###### 3. Jeżeli każdy prezent wręcza jeden Święty Mikołaj jednemu grzecznemu dziecku, nie wszystkie grzeczne dzieci muszą dostać prezent, za to wolno dostać więcej niż jeden prezent od jednego lub wielu Świętych Mikołajów oraz nie każdy Święty Mikołaj musi wręczać cokolwiek, to na ile różnych sposobów M nierozróżnialnych Świętych Mikołajów może rozdać P rozróżnialnych prezentów D grzecznym dzieciom?

Przydzielmy prezenty mikołajom (z uwzględnieniem że nie każdy musi rozdać jakiś prezent)
$$\begin{gathered}
\binom{P+M-1}{M-1}
\end{gathered}$$
I teraz po prostu rozdajmy prezenty dzieciom:
$$\begin{gathered}
D^P
\end{gathered}$$
I to złączamy:
$$\begin{gathered}
D^P \cdot \binom{P+M-1}{M-1}
\end{gathered}$$



---
### 1 grudnia 2021 - Zestaw B1

---
###### 1. Na ile różnych sposobów można rozmieścić n osób przy n rozróżnialnych okrągłych stołach?

Nie wiadomo jak intepretować to zadanie XD chyba wynik: $n!$ po prostu.

---
###### 2. Na ile różnych sposobów można rozmieścić w jednym rzędzie n małżeństw tak by przynajmniej jedno z nich znalazło się koło siebie?

$$\begin{gathered}
\frac{2n!}{2^n\cdot n!}
\end{gathered}$$
Lub:
$$\begin{gathered}
\sum^{n}_{i=1}{(-1)^{i+1}\cdot \binom{n}{i}\cdot (2n-i)!\cdot 2^i} 
\end{gathered}$$

---
###### 3. Jeśli nie wszyscy muszą być w parze to na ile sposobów można połączyć w pary n osób? Podaj i uzasadnij zależność rekurencyjną.
$$\begin{gathered}
a_1=1, \ a_2=2, a_3=3\\
a_n=a_{n-1}+(n-1)\cdot a_{n-2}
\end{gathered}$$
Bo albo:
- osoba pozostaje samotna (pierwszy składnik) to łączymy w pary pozostałe $a_{n-1}$ osób.
- albo osoba łączy się w parę z dowolną spoza $(n-1)$ osób, a następne rozkładamy na pary

---
###### 4. Rozwiąż równanie rekurencyjne:
$$\begin{gathered}
\left\{
\begin{matrix}
x_n-9x_{n-2}=-24n+54\\
x_0=-1\\
x_1=-6\\
\end{matrix}
\right.\\
x^2-9=0\\
x^2=9\\
x_1=3, x_2=-3\\
x_n^j=a\cdot 3^n+b\cdot (-3)^n\\\\
x_n^p=An+B\\
An+B-9(A(n-2)+B)=-24n+54\\
An+B-9An+18A-9B=-24n+54\\
\left\{
\begin{matrix}
-8A=-24\\
18A-8B=54
\end{matrix}
\right.\\
\left\{
\begin{matrix}
A=3\\
B=0
\end{matrix}
\right.\\
x_n=a\cdot 3^n +  b \cdot (-3)^n + 3n\\
x_0=-1=a+b\\
x_1=-6=3a-3b+3\\
\left\{
\begin{matrix}
a+b=-1\\
3a-3b+3=-6
\end{matrix}
\right.
\left\{
\begin{matrix}
a+b=-1\\
a-b=-3
\end{matrix}
\right.
\left\{
\begin{matrix}
b=-1-a\\
a-(-1-a)=-3
\end{matrix}
\right.\\
a=-2, b =1\\
x_n=-2\cdot 3^n + (-3)^n + 3n
\end{gathered}$$

---
### 26 listopada 2021 - Zestaw A1

###### 1. Ile jest różnych podzbiorów zbioru {1, 2, . . . , 100} nie zawierających żadnych dwóch liczb sumujących się do 101?

Na każdą liczbe z zakresu 1-50 włącznie przypadają 3 możliwości. Albo bierzemy ją, albo jej "siostre" - liczbę dopełniającą ją do 101, albo nie bierzemy żadnej z tych dwóch.
$$\begin{gathered}
3^{50}
\end{gathered}$$

###### 2. Podaj i uzadnij wzór jawny na liczbę nieporządków (było wyżej to samo).

Było ale dla przećwiczenia zrobie drugi raz.
Z zasady włączeń i wyłączeń. Naszymi właściwościami są: 
1. Jedna liczba zostanie na swoim miejscu
2. Dwie liczby zostaną na swoim miejscu
3. ....

$$\begin{gathered}
\\
n!-\binom{n}{1}(n-1)!+\binom{n}{2}(n-2)!-\binom{n}{3}(n-3)!\dots\\
D_n=\sum^{n}_{i=0}(-1)^i\binom{n}{i}(n-i)!
\end{gathered}$$

---
###### 3. Na ile różnych sposobów n osób można posadzić przy nierozróżnialnych okrągłych stołach tak, żeby żaden z użytych stołów nie był pusty? Podaj i uzasadnij zależność rekurencyjną.
Stirling 1 rodzaju + coś?
$$\begin{gathered}
A(n,k)=A(n-1,k-1) + A(n-1,k-1)\cdot (k-1)
\end{gathered}$$
---
### 1 grudnia 2021 - Zestaw C2
###### 1. Na ile różnych sposobów można rozmieścić nk osób na k nierozróżnialnych n osobowych karuzelach, jeśli są one umieszczone równomiernie na też obracającym się okręgu?
![[diagram-20241208 (1).png]]
$$\begin{gathered}
\frac{(n\cdot k)!}{(n!)^ k\cdot k!} \cdot  (n-1)!^k \cdot  (k-1)!
\end{gathered}$$

Ponieważ:
1. 

$$\begin{gathered}
\frac{(n\cdot k)!}{(n!)^k\cdot k!}
\end{gathered}$$
dzielimy osoby na k osobowe grupy
Analogia do podziału 2n osób na pary: $\frac{(2n)!}{2^n\cdot n!}$

2. $$\begin{gathered}
(n-1)^k
\end{gathered}$$
Ustalamy kolejność siedzenia każdej z osoby na każdej mniejszej karuzeli (identycznie jak rozsadzenie osób na okrągłym stole)
3. $$\begin{gathered}
(k-1)!
\end{gathered}$$
Jak już mamy wybrane kto gdzie siedzi w swojej małej karuzeli to teraz rozstawiamy małe karuzele na dużej karuzeli.

###### 2. Na ile różnych sposobów można rozsadzić przy okrągłym stole n małżeństw tak by przynajmniej jedno z nich znalazło się koło siebie?
$$\begin{gathered}
\binom{n}{1}\cdot 2\cdot (2n-2)!-\binom{n}{2}\cdot 2^2 \cdot (2n-3)!\dots \pm \binom{n}{n}\cdot 2^n\cdot (2n-n-1)!\\
Czyli:\\
\sum^{\infty}_{i=1}{(-1)^{i+1} \cdot \binom{n}{i}\cdot 2^i \cdot (2n-i-1)!}
\end{gathered}$$
###### 3. Jeśli nie wszyscy muszą być w trójkach to na ile sposobów można połączyć w trójki n osób? Podaj i uzasadnij zależność rekurencyjną.
$$\begin{gathered}
a_0=0, a_1=1, a_2=1, a_3=2\\
a_n=a_{n-1}+\binom{n-1}{2}\cdot a_{n-3}
\end{gathered}$$
Albo jest bez pary (trójki) wtedy $a_{n-1}$ albo wybieramy 2 osoby do trójki i reszte na pary.

---
### 2 grudnia 2022 

###### 1. Dziekan przygotowuje prezenty dla studentów. Ma do dyspozycji k pudełek, do których chce włożyć m czapek. Na ile sposobów może to zrobić, jeśli:

pudełka są ponumerowane, a czapki różnokolorowe oraz w żadnym pudełku nie może być więcej niż połowa wszystkich czapek?
$$\begin{gathered}
k^m -k \cdot k^{\lfloor \frac{m}{2} \rfloor -1}\\
To \ to \ samo \ co \\
k^m-\sum^{m}_{i=\lfloor \frac{m}{2}+1 \rfloor }{k\cdot \binom{m}{i}\cdot (k-1)^{m-i}}\\\\
\end{gathered}$$
pudełka są ponumerowane, a czapki identyczne oraz w żadnym pudełku nie może być więcej niż połowa czapek?

$$
\begin{gathered}
\binom{m+k-1}{k-1}-\binom{k}{1}\cdot \binom{m-(\lfloor \frac{m}{2}\rfloor + 1)+k-1}{k-1}
\end{gathered}
$$
pudełka są identyczne, a czapki różnokolorowe oraz żadne pudełko nie może być puste?
$$\begin{gathered}
S(m,k)
\end{gathered}$$
---
###### 2. Jaś zawsze wrzuca do skarbonki całkowitą liczbę złotych, przy czym codziennie przynajmniej złotówkę, a tygodniowo nie więcej niż 12 złotych. Udowodnij, że na przestrzeni szesnastu tygodni istnieje podciąg kolejnych dni, podczas których Jaś wrzucił do skarbonki łącznie 31 złotych.

$$\begin{gathered}
1\leq S_1\leq S_2\leq \dots \leq S_{112}\leq 192\\
32\leq S_1+31\leq S_2+31\leq \dots \leq S_{112}+31\leq 223\\
1\leq S_1,S_2,S_3,\dots S_1+31,S_2+31\dots S_{112}+31\leq 223\\
\end{gathered}$$
Mamy 224 różnych liczb całkowitych które mieszczą się między 1 a 223 zatem przynajmniej dwa z nich muszą być takie same. 

---
###### 3. Pewien człowiek ma siedmiu przyjaciół. Na ile sposobów może zapraszać po trzech z nich na kolację przez siedem kolejnych dni tak, aby każdy z nich został zaproszony co najmniej raz?

$$\begin{gathered}
\binom{7}{3}^7-7\cdot \binom{6}{3}^7+\binom{7}{2}\cdot \binom{5}{3}^7-\binom{7}{3}\cdot \binom{4}{3}^7+\binom{7}{4}\cdot 1
\end{gathered}$$
---
###### 4. Niech $a_n$ dla $n\geq2$ oznacza liczbę n-wyrazowych ciągów o wyrazach ze zbioru $\{1, 2, 3\}$ takich, że iloczyn każdych dwóch kolejnych wyrazów jest parzysty. Podaj i rozwiąż zależność rekurencyjną dla ciągu.

$$\begin{gathered}
a_n=b_n+3\cdot c_n\\\\
Gdzie \ b_n - \ poprzednia \ nieparzysta\\
Gdzie \ c_n - \ poprzednia \ parzysta\\
b_n=a_{n-2}\cdot 2\\
c_n=a_{n-1}\\
a_n=a_{n-1}+2\cdot a_{n-2}
\\
a_0=1, a_1=3, a_2=5
\\
r^2-r-2=0\\
\Delta=1+8=9\\
r_1=\frac{1+3}{2}=2, \ r_2=\frac{1-3}{2}=-1\\
a_n=A\cdot 2^n + B\cdot (-1)^n\\
a_n=\frac{4}{3}\cdot 2^n -\frac{1}{3}\cdot (-1)^n
\end{gathered}$$
---
### 7 grudnia 2023 - $I$ 

###### 1. Na ile różnych sposobów można ustawić w kolejce k studentek oraz m studentów, jeżeli pomiędzy każdymi dwoma studentkami ma stać co najmniej trzech studentów, a ponadto na początku kolejki ma stać studentka, a na końcu student. Podaj konieczne założenia.

$$\begin{gathered}
k - studentek, \ m-studentow\\
KMMM.KMMM.KM.\\
m\geq (k-1)\cdot 3+1\\\\
m\cdot k!\cdot \binom{k+m-3k+2-1}{m-3k+2}
\end{gathered}$$

---
###### 2. W kwadracie o boku długości 1 rozmieszczonych zostało 101 punktów. Wykaż, że istnieje koło o promieniu $\frac{1}{7}$, w którym znajduje się co najmniej pięć spośród danych punktów.
![[diagram-20241209 (1).png]]
$$\begin{gathered}
Z\ dirichleta \ \lceil \frac{101}{5\cdot 5}\rceil = 5\\
Musi \ byc \ kwadrat \ ktory \ ma \ co \ najmniej \ 5 \ punktow \ a \ ten \ kwadrat \ da \ sie \ zawrzec \ w \ okregu \\
\ o \ promieniu \frac{1}{7}
\end{gathered}$$

**Analogiczne zadanie z lekko zmienionym poleceniem:**
Promień koła dalej $\frac{1}{7}$ ale rozmieszczamy 76 punktów, i ma być co najmniej 4 punkty.

Jak sie domyśleć na ile kwadratów musimy podzielić ten kwadrat? Rozwiązać równanie:
$\lceil \frac{76}{x^2}\rceil = 4$
Czyli x=5, dalej dzielimy na $5\times 5$ kwadratów jak wcześniej. W tym w którym jest najwięcej punktów musi być co najmniej 4 punkty.
Średnica okręgu większa od przekątnej kwadratu więc dalej może zawrzeć cały kwadrat.


---
###### 3. Niech $X= \{1,2,3,4,5,6,7\}, \ Y=\{1,2,3,4,5\}$. Jaka jest liczba parami różnych odwzorowań $f: X\to Y$, w których:

a) $f(1)=f(3)\neq f(5)$ i $f$ jest nierosnące:

Skoro $f(1)=f(3)$ i $f$ nierosnące to: $f(1)=f(2)=f(3)$.

Metoda wszystkie minus złe. Wszystkie - rozkład od $f(3)$ do $f(7)$. Czyli dla 5 argumentów i 5 wartości.
$$\begin{gathered}
\binom{5+5-1}{5-1}
\end{gathered}$$
Złe to takie które nie spełniają warunku $f(3)\neq f(5)$ Czyli $f(3)=f(4)=f(5)$.
$$\begin{gathered}
\binom{3+5-1}{5-1}
\end{gathered}$$

---
(b) $|f(X)| = 4$
$$\begin{gathered}
\binom{5}{4}\cdot (4^7 - \binom{4}{1}\cdot 3^7 +\binom{4}{2}2^7 - \binom{4}{3}1^7 )
\end{gathered}$$
---
###### 4. Ile różnych słów można otrzymać przez przestawienie liter w słowie MATEMATYKA w taki sposób, że żadna z liter T nie występuje bezpośrednio przed A, żadna z liter A bezpośrednio przed M, natomiast litera E występuje bezpośrednio przed T?

Zasada włączeń i wyłączeń.
Wszystkie gdzie litera E występuje bezpośrednio przed T: 
ET - razem jako jeden klocek $\frac{9!}{2!\cdot 3!}$  M,A,T,ET,M,A,Y,K,A

**Dla warunków musimy pamiętać że nasze wszystkie możliwości uwzgledniają już E przed T**

$A_1$ - chociaż jedna litera T występuje bezpośrednio przed A
TA - 
1. razem jako jeden klocek M,A,ET,M,TA,Y,K,A $\frac{8!}{2!\cdot 2!}$
2. jako doklejenie do ET ETA,M,M,A,T,Y,K,A $\frac{8!}{2!\cdot 2!}$
3. pojawia się dwukrotnie ETA,M,M,TA,Y,K,A $\frac{7!}{2!}$
Tutaj zatem pojawia się kolejna zasada włączeń i wyłączeń

Więc $|A_1|=2\cdot \frac{8!}{2!\cdot 2!} - \frac{7!}{2!}=\frac{8!}{2!}-\frac{7!}{2!}$ 

$A_2$ - chociaż jedna z liter A stoi przed M
ET,AM,A,A,M,T,Y,K co daje $\frac{8!}{2!}-\frac{7!}{2!}$ permutacji

$A_1\cap A_2$ TA oraz AM

M,A,T,ET,M,A,Y,K,A:

M,A,T,ETAM,Y,K,A - TA doklejone do ET, AM do TA w jednym bloku ETAM
M,AM,T,ETA,Y,K,A - TA doklejone do ET, AM osobny blok AM, ETA
M,AM,TA,ET,Y,K,A - TA oraz AM osobny blok

... coś w tym stylu XD

---
###### 5. Na ile różnych sposobów można rozmieścić 20 osób:
a) W pięciu czterosobowych zespołach tak, aby każdy zespół wykonał jedno z pięciu zadań i każdy zespół inne zadanie.

$$\begin{gathered}
\binom{20}{4}\cdot 
\binom{16}{4}\cdot 
\binom{12}{4}\cdot 
\binom{8}{4}\cdot 
\binom{4}{4}\cdot 5!\\\\
\frac{20!}{(4!)^5\cdot 5!}\cdot 5!
\end{gathered}$$
b) W dwóch niepustych zespołach tak, aby każdy zespół wykonał jedno z dwóch różnych zadań

$$\begin{gathered}
S(20,2) \cdot 2^2=\frac{1}{2}(2^{20}-2)\cdot 2^2 \\
\end{gathered}
$$
Albo używamy stirlinga do podziału osób na DOKŁADNIE 2 (co zapewnia nam to że są niepuste) zbiory. I dla pierwszego wybieramy jedno z dwóch zadań, i dla drugiego jedno z dwóch.

c) W trzech niepustych zespołach tak, aby każdy zespół wykonał to samo zadanie. Wyniki przedstaw w postaci liczbowej.

$$\begin{gathered}
S(20,3) = \frac{1}{3!}(3^{20}-3\cdot 2^{20}+3)
\end{gathered}$$
---

###### Wykaż że suma jest równa $n\cdot 2^{n-1}$:
$$\begin{gathered}

k\cdot \binom{n}{k}=n\cdot \binom{n-1}{k-1}\\
\end{gathered}$$


$$\begin{gathered}
S=\binom{n}{1}+2\binom{n}{2}+3\binom{n}{3}+...+n\binom{n}{n}=\sum^{n}_{i=1}i\cdot \binom{n}{i}\\\\
Korzystamy \ ze \ wzoru:\\
k\cdot \binom{n}{k}=n\cdot \binom{n-1}{k-1}\\
\downarrow\\
S=\sum^{n-1}_{i=0}n\cdot \binom{n-1}{i}\\\\
A \ z \ ponizszego \ tw.:\\
(x+y)^n = \sum^{n}_{i=0}\binom{n}{i}x^i\cdot y^{n-i}\\
Dla\ x=y=1\\
(1+1)^n = \sum^{n}_{i=0}\binom{n}{i}1^i\cdot 1^{n-i}\\
2^n=\sum^{n}_{i=0}\binom{n}{i}\\\\
Wiec:\\
S=n\cdot 2^{n-1}
\end{gathered}$$

---
### DOKOŃCZ PÓŹNIEJ: https://wiki.iiet.pl/lib/exe/fetch.php?media=studia:przedmioty:dyskretna:meszkakolos202122.pdf

###### 4. Określ liczbę tych permutacji $f: A \to A$ zbioru $A = \{1, 2,\dots , 9\}$, w których dla każdej liczby nieparzystej 𝑖 zachodzi własność $f(i)\neq i$


To jest po prostu podręcznikowa definicja nieporządku $D(9)$ która wynika z zasady włączeń i wyłączeń.

$$\begin{gathered}
9\cdot 8!-\binom{9}{1}\cdot 8!+\binom{9}{2}\cdot 7! - \binom{9}{3}\cdot 6!+\binom{9}{4}\cdot 5! -\binom{9}{5}\cdot 4!+\binom{9}{6}\cdot 3! - \binom{9}{7}\cdot 2!+\binom{9}{8}\cdot 1!=\\
=362880-362880+\frac{362880}{2}-\frac{362880}{6}+\frac{362880}{24}-\frac{362880}{120}+\frac{362880}{720}-\frac{362880}{5040}+9-1=\\
=362880-362880+181440-60480+15120-3024+504-72+9-1=133496
\end{gathered}$$



###### 5. W kole o promieniu 2 wybranych zostało 13 punktów, z których żadne 3 nie są współliniowe. Uzasadnij, że wśród trójkątów, których wierzchołkami są wybrane punkty znajduje się trójkąt o polu nie większym niż $\sqrt{3}$ 

Jeżeli podzielimy okrąg na 6 równych części to z zasady dirichleta musi być okrąg w którym są $\lceil \frac{13}{6}\rceil=3$ punkty.

![[diagram-20241210.png]]
Czyli w najgorszym przypadku 3 punkty zawarte w $\frac{1}{6}$ okręgu utworzą nam trójkąt równoboczny o polu $\sqrt{3}$, w innych przypadkach te pola będą mniejsze. 


###### 6. Uzasadnij, że dla liczb Stirlinga drugiego rodzaju spełniona jest zależność $S(n,3)=\frac{3^{n-1}-2^n+1}{2}$

Liczba stirlinga drugiego rodzaju mówi nam o tym na ile sposobów możemy podzielić obiekty na DOKŁADNIE ileś bloków. Gdzie te bloki są nierozróżnialne.

Czyli to dokładnie to samo co gdybyśmy próbowali z zasady włączeń i wyłączeń i kombinatoryki rozdzielić rozróżnialne obiekty do rozróżnialnych bloków a następnie usuńmy rozróżnialność bloków.

$$\begin{gathered}
Rozdzielenie \ rozroznialnych \ obiektow \ do \ rozroznialnych \ blokow:\\
\binom{3}{3}3^n-\binom{3}{2}2^n+\binom{3}{1}1^n=
3^n-3\cdot 2^n +3\\
Usuniemy \ rozroznialnosc \ blokow \ dzielac \ calosc \ przez \ 3! \ czyli \ przemieszanie \ blokow:\\
(3^n-3\cdot 2^n +3)\cdot \frac{1}{3!}=\frac{3^{n}-3\cdot 2^n+3}{1\cdot 2 \cdot 3}=
\frac{3^{n-1}-2^n+1}{1\cdot 2}= S(n,3)
\\
\end{gathered}$$

---
### 14.02.2019

###### 1. Na ile różnych sposobów Walenty może obdarować 5 swoich koleżanek nierozróżnialnymi różami jeśli ma 25 róż i chce wszystkie je rozdać, a każdej z koleżanek dać przynajmniej jedną, lecz żadnej nie więcej niż siedem.

$$\begin{gathered}
x_1+x_2+x_3+x_4+x_5=25, \ \ x_i\geq 1\\
(x_1-1)+(x_2-1)+(x_3-1)+(x_4-1)+(x_5-1)=20\\
y_1+y_2+y_3+y_4+y_5=20\\
\binom{20+5-1}{5-1}=\binom{24}{4}\\\\
Przypadek \ I -jedna \ osoba \ dostala \ wiecej \ niz \ 7:\\
(y_1-7)+y_2+y_3+y_4+y_5=13\\
5\cdot \binom{13+5-1}{5-1}=5\cdot \binom{17}{4}\\\\
Przypadek \ II -dwie \ osoby \ dostaly \ wiecej \ niz \ 7:\\
(y_1-7)+(y_2-7)+y_3+y_4+y_5=6\\
\binom{5}{2}\cdot \binom{6+5-1}{5-1}=\binom{5}{2}\cdot \binom{10}{4}\\\\
Z \ zasady \ wlaczen  \ i \ wylaczen:\\
\binom{24}{4}-5\cdot \binom{17}{4}+\binom{5}{2}\cdot \binom{10}{4}
\end{gathered}$$

---
###### 2. Na ile różnych sposobów Walenty może obdarować dokładnie $a$ swoich koleżanek wręczając im w sumie dokładnie $x$ róż jeżeli koleżanek ma $b$, róż $y$ a ponadto:

a) róże są nierozróżnialne

$$\begin{gathered}
\binom{b}{a}\cdot \binom{x+a-1}{a-1}
\end{gathered}$$
b) róże są rozróżnialne
$$\begin{gathered}
\binom{b}{a}\cdot S(x,a)\cdot a!
\end{gathered}$$
---
###### 3. W kolejce do Walerii ustawiło się w kolejności alfabetycznej $n$ jej kolegów, z których każdy chciał jej wręczyć jedną lub trzy róże. Jeśli któryś kolega wręczył jej trzy róże to Waleria dziękowała mu na tyle długo, że następny w kolejce zniecierpliwiony rezygnował i odchodził nie wręczając róż wcale.

a) Podaj zależność rekurencyjną na liczbę sposobów w jaki mogło przebiegać wręczenie róż Walerii
$$\begin{gathered}
b_n - pierwszy \ wrecza \ 1\\
c_n - pierwszy \ wrecza \ 3\\
a_n=a_{n-1}+a_{n-2}\\
a_0=1\\
a_1=2
\end{gathered}$$
b) znajdź funkcje tworzącą powyższego ciągu
$$\begin{gathered}
f(x)=\sum^{\infty}_{n=0}{a_nx^n}=1+2x+\sum^{\infty}_{n=2}{a_nx^n}=\\
=1+2x+\sum^{\infty}_{n=2}{(a_{n-1}+a_{n-2})x^n}=1+2x+\sum^{\infty}_{n=2}{a_{n-1}x^n}+\sum^{\infty}_{n=2}{a_{n-2}x^n}=\\
=1+2x+\sum^{\infty}_{n=1}{a_nx^{n+1}}+\sum^{\infty}_{n=0}{a_nx^{n+2}}=1+2x+x\sum^{\infty}_{n=1}{a_nx^n+x^2\sum^{\infty}_{n=0}a_nx^n}=\\
1+2x+x\cdot (f(x)-1)+x^2\cdot f(x)\\\\
f(x)=1+2x+x\cdot f(x)-x+x^2\cdot f(x)\\
f(x)-x\cdot f(x)-x^2\cdot f(x)=1+x\\
f(x)\cdot (1-x-x^2)=1+x\\
f(x)=\frac{1+x}{1-x-x^2}
\end{gathered}$$

---

###### 1. Aby się nie pomylić Święty Mikołaj wszystkie prezenty oznaczył kodami kreskowymi w postaci naprzemiennych czarnych i białych pasków szerokości 1 lub 2, zaczynających się i kończących się paskiem czarnym. Podaj wzór rekurencyjny opisujący ile mógł stworzyć różnych kodów kreskowych o sumarycznej szerokości n:

$$\begin{gathered}
a_n=a_{n-2}+2\cdot a_{n-3}+a_{n-4}
\end{gathered}$$
bo ma się zaczynać i kończyć czarnym zatem albo kończy się ⬛|🔲⬛ ($a_{n-2}$) albo ⬛|🔲🔲⬛ albo ⬛|🔲⬛⬛ ($2\cdot a_{n-3}$) albo kończy się ⬛|🔲🔲⬛⬛($a_{n-4}$)

###### 2. Na ile różnych sposobów Święty Mikołaj mógł zapakować $k$ spośród $l$ prezentów do dokładnie $m$ spośród $n$ pudełek (czyli tak aby $m$ było niepustych a $n-m$ pustych), jeżeli:

a) prezenty były nierozróżnialne, a pudełka rozróżnialne
$$\begin{gathered}
\binom{n}{m}\cdot \binom{(k-m)+m-1}{m-1}
\end{gathered}$$
b) prezenty były rozróżnialne, a pudełka rozróżnialne
$$\begin{gathered}
\binom{l}{k}\cdot \binom{n}{m}\cdot S(k,m)\cdot m!
\end{gathered}$$
c) prezenty były rozróżnialne a pudełka nierozróżnialne
$$\begin{gathered}
\binom{l}{k}\cdot S(k,m)
\end{gathered}$$
d) prezenty były nierozróżnialne, a pudełka nierozróżnialne:
$$\begin{gathered}
P(k,m)
\end{gathered}$$
### Ciekawe kolokwium https://wiki.iiet.pl/lib/exe/fetch.php?media=studia:przedmioty:dyskretna:kolokwia_2017_2018.pdf

###### 1. Ile jest naturalnych liczb czterocyfrowych, których suma cyfr jest nie większa niż 31?
$$\begin{gathered}
a+b+c+d\leq 31\\
Powyzsza \ nierownosc \ jest \ rownowazna \ z:\\
a+b+c+d+e=31\\
bo:\\
a+b+c+d=31-e\ gdzie \ 0 \lt e \leq 31\\\\
musimy \ uwzglednic \ to \ ze \ a\geq 1 \ bo \ pierwsza \ cyfra \ nie \ moze \ byc \ 0\\\\
(a-1)+b+c+d+e=30\\
a'+b+c+d+e=30\\
\binom{30+5-1}{5-1}
\end{gathered}$$
---
###### 2. Ile jest palindromicznych liczb (2n+1)-cyfrowych parzystych takich, że zawierają przynajmniej jedna jedynkę lub nie zawierają dwójek? Liczby palindromiczne to takie, które są czytane od przodu tak samo, jak od tyłu, np. 123454321.

$$\begin{gathered}
Wszystkie \ parzyste \ palindromy:\\
Zawierajace\ jedynke:\\
4\cdot (\frac{2n+1-2-1}{2}+1)\cdot 10^{\frac{2n+1-2-1}{2}}=4\cdot n\cdot 10^{n-1}\\
skrajne \ parzyste \cdot wybor \ miejsca \ gdzie \ napewno \ 1\cdot reszta\\
Nie \ zawieraja \ dwójek\\
3\cdot 9^{\frac{2n+1-1-2}{2}+1}=3\cdot 9^{n}\\
Zawierajace \ jedynke\ i \ nie \ zawierajace \ dwójek:\\
3\cdot n\cdot 9^{n-1}\\\\
Z \ zasady \ wlaczen \ i \ wylaczen:\\
4\cdot n \cdot 10^{n-1}+3\cdot 9^n -3\cdot n \cdot 9^{n-1}
\end{gathered}$$
---
###### 3. W ilu macierzach zero-jedynkowych o wymiarach $n\times n$ przynajmniej jeden wiersz jest wypełniony zerami?
$$\begin{gathered}
Co\ najmniej \ jeden \ wiersz:\\
n\cdot 2^{n^2-n}\\
Co\ najmniej \ dwa \ wiersze:\\
\binom{n}{2}\cdot 2^{n^2-2n}\\
\dots\\
Kazdy \ wiersz \ ma \ same \ zera:\\
1\\\\
Z \ zasady \ wlaczen \ i \ wylaczen:\\
n\cdot 2^{n^2-n}-\binom{n}{2}\cdot 2^{n^2-2n}+\binom{n}{3}\cdot 2^{n^2-3n}\dots \pm 1=\\=\sum^{n}_{i=1}{(-1)^{i-1}\cdot \binom{n}{i}\cdot 2^{n^2-i\cdot n}}\\\\

\end{gathered}$$
---
