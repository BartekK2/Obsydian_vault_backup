
#### 1. Spośród liter $a,a,k,s,s,t,t,t,y,y$ losujemy bez zwracania po jednej i układamy je w kolejności losowania. Jakie jest prawdopodobieństwo otrzymania słów $tata,statystyk,statystyka$

$$\begin{gathered}
tata: & \frac{3}{10}\cdot \frac{2}{9}\cdot \frac{2}{8}\cdot \frac{1}{7}\\
statystyk: & \frac{2!3!2!}{10!}\\
\dots
\end{gathered}$$

---

#### 2. Odcinek  o długości $10$ podzielono losowo na $3$ części, przy czym długość każdej części jest liczbą całkowitą. Oblicz prawdopodobieństwo tego że z powstałych części można ułożyć trójkąt.

$$\begin{gathered}
\text{Zał:}\\
a \geq 1 \ \ b\geq 1\ \ c\geq 1\\\\
\text{Wszystkie możliwe kombinacje:}\\
(a+1)+(b+1)+(c+1)=10\\
a'+b'+c'=7\\

\binom{7+3-1}{3-1}=\binom{9}{7}=36\\\\
\text{Kombinacje poprawne:}\\
\text{Albo mamy tylko jedną czwórke (reszta (3,3))}\\
\binom{3}{1}\\
\text{Albo dwie czwórki reszta (2)}\\
\binom{3}{2}=3\\\\
\text{Zatem wynik to:}\\
\frac{6}{36}=\frac{1}{6}
\end{gathered}$$

---
#### 3) Sześcian wykonany z jasnego drewna pomalowano na czarno, a następnie pocięto 9 płaszczyznami równoległymi do ścian na 64 mniejsze sześciany. Z powstałego zbioru sześcianów losujemy jeden. Jakie jest prawdopodobieństwo tego, że:

- ma on wszystkie ściany jasne
  
$$\begin{gathered}
\Omega=\{1,\dots,64\}\\
A_1=\{1,\dots,8\}\\\text{ bo bierzemy ten mniejszy sześcian który po lewej i prawej ma czarne}\\
\text{Licząc od środka jako jeden itd}\\\\
P(A_1)=\frac{|A_1|}{|\Omega|}=\frac{8}{64}=\frac{1}{8}
\end{gathered}$$

- ma on dwie ściany czarne
  $$\begin{gathered}
|A_2|=16\\
P(A_2)=\frac{16}{64}=\frac{1}{4}
\end{gathered}$$
- ma on jedną ściane czarną
  $$\begin{gathered}
A_3- \text{trzy ściany czarne}\\
|A_3|=8\\
A_4- \text{Jedna ściana czarna}\\
P(A_4)=1-\frac{8}{64}-\frac{1}{4}-\frac{1}{8}=\\
=1-\frac{2}{16}-\frac{4}{16}-\frac{2}{16}=\frac{1}{2}
\end{gathered}$$

---
#### 4. Jak dużo osób musiałoby zebrać się w jednym pomieszczeniu, żeby prawdopodobieństwo tego, że przynajmniej dwie z nich obchodzą urodziny tego samego dnia, było nie mniejsze niż $\frac{1}{2}$?

$$\begin{gathered}
\text{Skoro mamy w zadaniu powiedziane że "przynajmniej 2"}\\
\text{Najlepiej byłoby rozwiązać przypadek przeciwny tj.}\\
\text{Żadna para osób nie ma urodzin w tym samym dniu}\ (A)\\
\text{Sortując osoby po wzroście i pytając ich o dzień urodzin}\\
\text{mamy kombinacji:}\\
|A|=\bigcap^n_{i=0}{365-i}=\frac{365!}{(365-n)!}\\\\
\text{A wszystkich kombinacji jest:}\\
|\Omega|=365^n\\\\
P(A)=\frac{365!}{(365-n)!\cdot 365^n}\\
B-\text{Co najmniej dwójka osób ma urodziny w tym samym dniu}\\\\
P(B)=1-P(A)\\
1-\frac{365!}{(365-n)!\cdot 365^n}\gt \frac{1}{2}\\\\
n=23
\end{gathered}$$

---
#### 5. Obliczyć prawdopodobieństwo tego, że losowo wybrany punkt kwadratu $\max\{|x|,|y|\}\lt 4$ leży na zewnątrz okręgu $x^2+y^2=1$

$$\begin{gathered}
|\Omega|=8^2=64\\
|A|=\pi\\
A\subset \Omega \implies P(A)=\frac{|A|}{|\Omega|}\frac{\pi}{64}\\
1-P(A)=\frac{64-\pi}{64}
\end{gathered}$$

---
#### 6. Kawałek drutu o długości $20cm$ zgięto pod kątem prostym w przypadkowo wybranym punkcie. Następnie zgięto drut jeszcze w $2$ punktach, tak by utworzyła sie ramka prostokątna o obwodzie $20cm$. Jakie jest prawdopodobieństwo tego, że pole utworzonego prostokąta nie przekracza $21cm^2$?

$$\begin{gathered}
10cm-\text{Połowa obwodu}\\
a,b - \text{boki prostokąta}\\
\text{Zał:}\\
a\gt 0, b\gt 0\\\\\
a+b=10cm\implies b=10-a\\\\
Pole: ab=a(10-a)\\
a(10-a)\leq 21\\
10a-a^2-21\leq 0\\
\Delta=100-84=16\\
a_1=\frac{-10+4}{-2}=3\\
a_2=\frac{-10-4}{-2}=7\\
a\in (0,3]\cup [7,10)\\
\downarrow\\
|A|=3+3=6\\
|\Omega|=10\\\\
P(A)=0.6
\end{gathered}$$

---
#### 7. Na płaszczyźnie poprowadzono proste równoległe odległe o $2a$. Na płaszczyzne tę rzucamy w sposób przypadkowy monetę o promieniu $r\lt a$. Jakie jest prawdopodobieństwo tego, że moneta nie przetnie żadnej prostej?

$$\begin{gathered}
|A|=a-r\\\\
|\Omega|=2a\\\\
P(A)=\frac{a-r}{2a}
\end{gathered}$$![[obraz_2025-10-30_153637025-Photoroom.png]]
Rozpatrując tylko "górną" część prostej możemy zmieścić środek odcinka między $a$ a $r$ stąd $|A|=a-r$ a $|\Omega|=a$, możemy rozpatrywać tylko pojedynczą prostą i tylko część nad nią ponieważ analogicznie jest z częścią pod, oraz z innymi prostymi. Założenie że proste są prostopadłe do osi $OY$ ułatwia liczenie a nie zmienia nam zadania.

---
#### 8. Płaszczyznę podzielono prostymi równoległymi odległymi o $2a$. Na płaszczyznę tę rzucamy w sposób przypadkowy odcinek o długości $2l\lt 2a$. Jakie jest prawdopodobieństwo tego, że odcinek przetnie jedną z prostych?


$$\begin{gathered}
\text{Podobnie, rozpatrujemy tylko "góre" prostej prostopadłej do osi OY}\\
\text{to znaczy rozpatrujemy ten obszar jako miejsce gdzie może znaleźć się }\\
\text{środek tej prostej}\\\\
\text{pozycja x środka nas nie interesuje zatem przyjmiemy oznaczenie}\\
y_s \text{ co jest odległością środka od najbliższej mu prostej.}\\\\
\Omega=\{(y_s,\alpha):y_s\in (0,a), \alpha \in (0,\pi)\}\\\\
|\Omega|=a\cdot \pi\\\\
\text{Rozpatrzmy punkt na lewo od środka który będzie miał pozycje:}\\
L=(x_s,y_s)-(\cos{\alpha},\sin{\alpha})\cdot l\\\\
\text{Interesuje nas policzenie obszaru gdzie }A_y\lt 0\\\\
L_y\lt 0 \Leftrightarrow y_s-\sin{\alpha}\cdot l\lt 0\\\\
A:\{(y_s,\alpha):  y_s-\sin{\alpha}\cdot l\lt 0, \alpha\in (0,\pi)\}\\\\\
|A|=\int^{\pi}_{0}\ d\alpha\int^{\sin{\alpha}l}_0 d y_s=\\\\
=\int^{\pi}_{0}{\sin{\alpha}l}=2l\\\\\
P(A)=\frac{|A|}{|\Omega|}=\frac{2l}{\alpha \pi}
\end{gathered}$$

---
#### 9. W przypadkowych chwilach z przedziału czasowego $[0,T]$ do odbiornika mogą nadejść dwa sygnały. Odbiornik zostaje uszkodzony jesli różnica w czasie między sygnałami jest mniejsza niż $\theta$ $(\theta\lt T)$. Oblicz prawdopodobieństwo uszkodzenia odbiornika w przedziale $[0,T]$

$$\begin{gathered}
\text{Zakładając że }x\in [0,T]\\
\text{to któryś z sygnałów a }y\in [0,T]\\
\text{to drugi sygnał to:}\\
|x-y|\lt \theta\\
\text{Definiuje nam obszar gdzie odbiornik się zepsuje.}\\\\\

\end{gathered}$$![[obraz_2025-10-30_165304653-Photoroom.png|400]]
$$\begin{gathered}
\text{Wystarczy policzyć obszar niebieskiego pola jako:}\\
2\cdot \frac{(T-\theta)^2}{2}=(T-\theta)^2\\\\
\text{i odjąć od mocy przestrzeni elementarnej}\\\\\
P(A)=1-\frac{(T-\theta)^2}{T^2}
\end{gathered}$$

---
#### 10. Przez odcinek jednotorowy o końcach $A$ i $B$ mają przejechać dwa pociągi nadjeżdżające z przeciwnych kierunków (pierwszy od strony $A$, drugi od strony $B$) niezależnie od siebie. Pierwszy przybywa do $A$ w chwili $t_1$, drugi do $B$ w chwili $t_2$, przy czym obie chwile sa wybrane losowo z przedziału $[T_s,T_e]$, gdzie $T_e-T_s=15min$. Zakładamy, że prawdopodobieństwo wybrania danej chwili jest rozłożone równomiernie na całym przedziale. Oblicz prawdopodobieństwo tego, że jeden z pociągów będzie musiał czekać na przejazd drugiego, jeżeli czas przejazdu od $A$ do $B$ wynosi $3min$, a czas przejazdu od $B$ do $A \  2min$.


$$\begin{gathered}
\Omega=\{(t_1,t_2):t_1\in [T_s,T_e] \land t_2\in [T_s,T_e]\}\\\\
|A|=\{(t_1,t_2):(t_2\lt t_1<t_2+2)\vee( t_1\lt t_2\lt t_1+3)\}\\\\
P(A)=1-\frac{(15-3)^2}{2}\cdot \frac{1}{15^2}-\frac{(15-2)^2}{2}\cdot \frac{1}{15^2}
\end{gathered}$$
![[obraz_2025-10-30_174321055-Photoroom.png|400]]


---
#### Dwaj rowerzyści codziennie pokonują ten sam odcinek między punktami $A$ i $B$ w przeciwne strony (pierwszy od $A$ do $B$, drugi od $B$ do $A$). Droga od $A$ do $B$ biegnie stale pod górę. Pierwszy przybywa do $A$ w chwili $t_1$, drugi do $B$ w chwili $t_2$. Przy czym obie chwile są wybrane losowo z przedziału $[T_s,T_e]$ gdzie $T_s=8:15$, $T_e=8:45$. Zakładamy, że prawdopodobieństwo wybrania danej chwili jest rozłożone równomiernie na całym przedziale. Czas przejazdu wspólnego odcinka pod górę jest dla obu rowerzystów taki sam i wynosi $10$ minut, czas przejazdu w dół jest również taki sam i wynosi $5$ minut. Oblicz prawdopodobieństwo spotkania rowerzystów.


$$\begin{gathered}
\Omega=\{(t_1,t_2): t_1,t_2\in [8.25,8.75]\}\\
\text{Skonwerterowałem czas na liczby rzeczywiste}\\\
A - \text{Spotkają się}\\
A=\{(t_1,t_2):t_1\lt t_2+\frac{5}{60} \land t_2\lt t_1+\frac{10}{60}\}\cap \Omega\\\\

t_2-\frac{10}{60}\lt t_1\lt t_2+\frac{5}{60}\\\\

\end{gathered}$$
![[Pasted image 20251113155509.png]]

$$\begin{gathered}
P(A)=1-\frac{\frac{1}{2}\cdot \frac{25}{60}^2+\frac{1}{2}\cdot \frac{20}{60}^2}{0.25}
\end{gathered}$$


---
#### Odcinek o długości $10$ podzielono losowo na $3$ części. Oblicz prawdopodobieństwo tego, że z powstałych części można zbudować trójkąt

$$\begin{gathered}
\Omega=\{(a,b):a,b\gt 0 \land a+b\lt10\}\\\\

A:\\
\max\{a,b,10-a-b\}\lt 5\Leftrightarrow\\
a\lt 5 \land b\lt 5 \land 5\lt a+b\\\\
A=\{(a,b): 0\lt a\lt 5, 0\lt b\lt 5, 5\lt a+b\lt 10\}\\\\

\end{gathered}$$

![[Pasted image 20251113162320.png]]

$$\begin{gathered}
|\Omega|=10^2\cdot \frac{1}{2}\\
P(A)=\frac{\frac{1}{2}\cdot 5^2}{|\Omega|}=0.25
\end{gathered}$$

---
#### Na okręgu wybrano losowo 3 punkty. Jakie jest prawdopodobieństwo tego, że wybrane punkty tworzą trójkąt ostrokątny?

Można przyjąć że rozpatrujemy okrąg:
$$\begin{gathered}
x^2+y^2=r^2
\end{gathered}$$

Po rozrzuceniu punktów $(a,b,c)$ obracam okrąg tak żeby punkt przy którym kąt jest największy miał $y\gt 0$ a odcinek łączący pozostałe punkty był równoległy do osi x. Wtedy możemy zauważyć że warunek pozwalający na to by trójkąt był ostrokątny to to żeby dwa pozostałe punkty miały $y\lt 0$. Zatem możemy przyjąć że największy kąt jest przy $b$ - żeby łatwiej zapisać $\Omega$ i zdarzenie które rozpatrujemy. Zmieniamy jedynie adnotacje punktów więc nie zmieniamy tym treści i warunków zdania.

$$\begin{gathered}
\Omega=\{(y_a,y_c): y_a,y_c\in [-r,r]\}
\end{gathered}$$
naszym warunkiem będzie:
$$\begin{gathered}
A=\{(y_a,y_c): y_a,y_c\in [-r,0]\}
\end{gathered}$$

I liczymy prawdopodobieństwo jako:
$$\begin{gathered}
P(A)=\frac{|A|}{|\Omega|}=\frac{r^2}{4r^2}=\frac{1}{4}
\end{gathered}$$

---
#### 14) Niech $(a,b)$ będzie losowo wybranym punktem prostokąta $\{(a,b)\in \mathbb{R}^2: |a|\lt 2, |b|\lt 1\}$. Obliczyć prawdopodobieństwo trego, że pierwiastki równania:

$$\begin{gathered}
x^2+2ax+b=0
\end{gathered}$$
są
- rzeczywiste

$$\begin{gathered}
\Delta=4a^2-4b\gt 0\\
a^2\gt b
\end{gathered}$$

  


$$\begin{gathered}
\Omega=\{(x,y): -2\lt x\lt 2, -1\lt y\lt 1\}\\
|\Omega|=4\cdot 2=8\\\\\
|A|=6+2\int^{1}_{0}x^2=6+\frac{2}{3}=\frac{20}{3}\\\\
P(A)=\frac{\frac{20}{3}}{\frac{24}{3}}=\frac{5}{6}
\end{gathered}$$

![[Pasted image 20251113172112.png]]


- rzeczywiste dodatnie 
$$\begin{gathered}
x_1=\frac{a-\sqrt{\Delta}}{2}\\
x_2=\frac{a+\sqrt{\Delta}}{2}\\\\
A:
\Delta\gt 0\\
x^2\gt y\\

\text{Drugi warunek z wzorów viete'a}\\\\
x_1+x_2\gt 0\\
2a\gt 0\\\\
x_1\cdot x_2\gt 0\\
b^2\gt \Delta\\\\

\end{gathered}$$

