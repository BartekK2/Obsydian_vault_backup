
### 🧲 Podsumowanie Indukcji Elektromagnetycznej

Indukcja elektromagnetyczna to fizyczny proces, w którym wytwarzamy prąd elektryczny bez użycia baterii, polegający na zamianie ruchu na elektryczność.

1. Zaczynamy od Magnesu i Kabla
- Magnes: Ma wokół siebie pole magnetyczne. Wyobrażamy je sobie jako niewidzialne linie pola (strugi wody).
- Kabel: To jest przewodnik pełen swobodnych elektronów, który ma określoną powierzchnię (koło młyńskie, przez które mogą płynąć strugi).


![[indukcja_elektromagnetyczna.mp4]]

---
### 2. Dlaczego tylko ruch ma znaczenie?
Prąd powstaje tylko wtedy, gdy magnes się porusza (lub kabel się porusza względem magnesu). (Ruch jest przecież względny)

Magnes stoi obok: Linie pola są w kablu, ale są nieruchome (stałe). Woda w rzece stoi. Żadna energia nie jest wkładana, więc nie ma prądu.

Magnes rusza się: Wkładasz energię mechaniczną (pracę). Ten ruch powoduje, że liczba linii pola przechodzących przez kabel zmienia się w czasie.

Można do porównać do koła młyńskiego - nawet jeśli koło młynskie jest zalane wodą (czyli magnes stoi obok obwodu) to koło młyńskie sie nie rusza. Dopiero kiedy woda ma swój bieg i nurt to koło młyńskie ruszać się zacznie.

---
### 3. Kluczowy Element: Zmiana Strumienia

Strumień Magnetyczny ($\Phi_B$) to miara tego, ile linii pola magnetycznego przechodzi przez powierzchnię kabla. Aby powstał prąd, ten strumień musi się zmieniać 
($\boldsymbol{d\Phi_B}$). Szybkość tej zmiany ($\boldsymbol{d\Phi_B/dt}$) jest najważniejsza. Im szybciej ruszamy magnesem, tym szybciej zmienia się strumień.

---
### 4. Co to jest SEM?

Siła Elektromotoryczna ($\epsilon$ - SEM) to nie jest siła, ale napięcie (mierzone w woltach), które jest wytwarzane przez tę zmianę strumienia. SEM to siła napędowa dla elektronów. Wytwarza ją indukowane pole elektryczne, które powstało w wyniku zmiany pola magnetycznego (ruchu magnesu).Im większa i szybsza zmiana strumienia (szybki ruch magnesu), tym większa SEM (większe napięcie) i tym silniejszy prąd.

Można to porównać ponownie do koła młyńskiego - SEM to nic innego jak to jak "poważny" jest obrót tego koła czyli to jak duże to koło jest i jak szybko się ono kręci.

**Zauważymy to patrząc na wzory:**
$$\begin{gathered}
\epsilon - SEM\\\\
\epsilon=-\frac{d \Phi_B}{dt}\\\\
\text{gdzie:}\\\\
 \Phi_B=\int^{}_{S}BdS
\end{gathered}$$
Czyli ile liń pola magnetycznego jest na tej powierzchni (całka po to bo to może nie być stałe). Coś jak to że na poszczególne łopatki koła młyńskiego działają różne nurty wody.

**Dla płaskiego obwodu w jednorodnym polu magnetycznym upraszcza się to do:**

$$\begin{gathered}
\Phi_B=BS \cos{\alpha}
\end{gathered}$$
gdzie $\alpha$ to kąt między strumieniem pola magnetycznego a powierzchnią.

Zatem zauważmy. Taki strumień pola magnetycznego to iloczyn wektora indukcji magnetycznej (jego siła i kierunek) razy powierzchnia razy kąt. Zatem jego zmiana zależy od tych 3 czynników.

Ruch magnesu tutaj jest ukryty pod $B$ bo kiedy ruszamy magnesem, zmienia się wartość i kierunek pola $B$ w punkcie, w którym znajduje się cewka.

Widzimy, że możemy zmienić strumień magnetyczny, i w konsekwencji wyindukować prąd w obwodzie, zmieniając wartość pola magnetycznego w obszarze, w którym znajduje się przewodnik. Magnes jest zbliżany do obwodu i w wyniku tego narasta pole magnetyczne (pochodzące od magnesu) przenikające przez obwód (pętlę). Gdy magnes zostaje zatrzymany, pole wewnątrz pętli przestaje zmieniać się i nie obserwujemy zjawiska indukcji.

**Rozpatrując już jedynie ten prostszy przypadek z jednorodnym polem magnetycznym oraz płaskim obwodem:**

![[an_indukcja3.gif]]

tak to wyglada jeśli chodzi o obrót tym płaskim obwodem. Coś jakbyśmy to koło młyńskie ustawiali w poprzek strumienia wody - też się obracać nie będzie.

Jeśli zdefiniujemy kąt na podstawie prędkości kątowej i czasu:
$$\begin{gathered}
\alpha=\omega t
\end{gathered}$$
to przekształcimy wzór 
$$\begin{gathered}
\Phi_B=BS \cos{\alpha}\\
\downarrow\\
\Phi_B=BS \cos{\omega t}
\end{gathered}$$

oraz wzór SEM indukcji:
$$\begin{gathered}
\epsilon=-\frac{d \Phi_B}{dt}=\frac{d(BS \cos{\omega t})}{dt}=\omega BS \sin(\omega t)
\end{gathered}$$

---
### 5. Prawo Lenza (Kierunek)

Indukowany prąd zawsze płynie w kierunku, który ma przeciwdziałać ruchowi, który go wywołał. Musisz użyć siły, aby pokonać to przeciwdziałanie.

---
### Podsumowanie Końcowe:

Indukcja Elektromagnetyczna to mechanizm, który zamienia włożoną przez nas energię ruchu (zmianę pola magnetycznego) na siłę napędową (SEM), która zmusza elektrony w kablu do uporządkowanego ruchu (prądu).

---