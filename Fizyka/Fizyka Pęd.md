### Pęd
#### 2025-05-12
##### Poprzednia: [[Fizyka 1 Kinematyka, Wstęp]]
##### Następna: [[]]
##### Zadania: [[]]

#pęd

---

### Środek masy 


Położenie środka masy układu (dwóch ciał) definiujemy jako:

$$\begin{gathered}
x_{śr}=\frac{m_1x_1+m_2x_2}{m_1+m_2}
\end{gathered}$$

Przypadek ogólny definiujemy jako:

$$\begin{gathered}
x_{śr}=\frac{\sum^{n}_{i=1}{m_ix_i}}{\sum^{n}_{i=1}{m_i}}
\end{gathered}$$
Oczywiście, to jest przypadek dla osi $x$, tak samo definiujemy oś $y$ oraz $z$.

Zatem **środek masy układu punktów materialnych** zależy **tylko** od **mas** tych puntków i od **wzajemnego ich rozmieszczenia**, a nie zależy od wyboru układu odniesienia.

**Ćwiczenie**:

Znajdź środek masy układu trzech cząstek o masach $m_1 = 1\ kg,\ m_2 = 2\ kg, \ m_3 = 3 \ kg$, umieszczonych w wierzchołkach równobocznego trójkąta o boku $a = 1 m$. 

Wynik nie zależy od wyboru układu odniesienia zatem, możemy przyjąć że lewy dolny wierzchołek znajduję sie w $(0,0)$, prawy dolny $(a,0)$ a górny $(\frac{a}{2},\frac{a\sqrt{3}}{2})$

Współrzędne środka masy obliczamy zgodne z równaniem:

$x_{śr}=\frac{m_1x_1+m_2x_2+m_3x_3}{m_1+m_2+m_3}=\frac{7}{12}m$
$y_{śr}=\frac{m_1y_1+m_2y_2+m_3y_3}{m_1+m_2+m_3}=\frac{\sqrt{3}}{4}m$

---
### Ruch środka masy

Możemy zapisać dla danej współrzędnej $r$, oraz dla sumy wszystkich mas $M$:
$$\begin{gathered}
Mr_{śr}=\sum^{n}_{i=1}{m_ir_i}
\end{gathered}$$

Różniczkując względem czasu otrzymujemy:

$$\begin{gathered}
M \frac{dr_{śr}}{dt}=\sum^{n}_{i=1}{m_i \frac{dr_i}{dt}}\\
M v_{śr}=\sum^{n}_{i=1}{m_iv_i}
\end{gathered}$$
A po ponownym zróżniczkowaniu:

$$\begin{gathered}
M \frac{d v_{śr}}{dt}=\sum^{n}_{i=1}{m_i \frac{d v_i}{dt}}\\
M a_{śr}=\sum^{n}_{i=1}{m_i a_i}
\end{gathered}$$
A to ostatnie równanie możemy zapisać w postaci:
$$\begin{gathered}
M a_{śr}=\sum^{n}_{i=1}{F_i}
\end{gathered}
$$

A suma wszystkich sił działających na poszczególne punkty materialne układu jest równna wypadkowej sile zewnętrznej więc:
$$\begin{gathered}
M a_{śr}=F_{zew}
\end{gathered}$$
Z tego wynika że:

**Środek masy układu punktów materialnych porusza się w taki sposób, jakby cała masa układu była skupiona w środku masy i jakby wszystkie siły zewnętrzne nań działały**

Z twierdzenia o ruchu środka masy wynika, że nawet ciała materialne będące układami złożonymi z dużej liczby punktów materialnych możemy w pewnych sytuacjach traktować jako pojedynczy punkt materialny.

### Pęd układu punktów materialnych

Korzystając z powyższego możemy powiedzieć że pęd układu możemy zdefiniować jako:

$$\begin{gathered}
P=M v_{śr}
\end{gathered}$$
