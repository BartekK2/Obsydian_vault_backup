### Wstęp & kinematyka
#### 2025-03-04
##### Następna: [[Fizyka 2 Dynamika]]
##### Zadania: [[]]

#wektory #przyspieszenie

---
## Absolutne podstawy (przypomnienie):

### Dodawanie wektorów:

Dodawanie wektorów (np. prędkości) w fizyce odbywa się w identyczny sposób jak w algebrze 
![[diagram-20250318 (2).png]]
$$\begin{gathered}
\vec{a}+\vec{b}=\{a_x+b_x,a_y+b_y,a_z+b_z\}
\end{gathered}$$
### Iloczyn skalarny:

Jest to iloczyn wektorów opisany za pomocą liczby. Przykład wielkości którą da się opisać w ten sposób jest praca. (Iloczyn skalarny siły i przemieszczenia)

$$\begin{gathered}
a\cdot b = |a|\cdot |b| \cdot \cos{\alpha}\\
W=\vec{F}\cdot \vec{s} \cdot \cos{\alpha}
\end{gathered}$$

### Iloczyn wektorowy:

Jest to iloczyn wektorów opisany za pomocą wektoru. Jego długość jest wyrażona poniższym wzorem: 
$$\begin{gathered}
c=ab\sin{\alpha}
\end{gathered}$$
Wektor powstały z iloczynu wektorowego jest prostopadły do obu tych wektorów.


## Kinematyka:

Kinematyką nazywamy dział fizyki zajmujący się opisem ruchu ciał.

**Def. Ruchu**
Pod pojęciem ruchu rozumiemy zmiany wzajemnego położenia jednych ciał względem drugich wraz z upływem czasu.

Ważnym jest tutaj zwrócenie uwagi w definicji na "wzajemne położenie". Ruch określamy względem pewnych układów odniesienia. Nie ma ruchu bezwzględnego. Da się tylko poruszać **względem** czegoś.

**Ruch jest pojęciem względnym.**

**Def. Punktu materialnego**
Punkty materialne to obiekty obdarzone masą, których rozmiary (objętość) możemy zaniedbać.

**Def. Prędkości**
Prędkość definiujemy jako zmianę położenia ciała w jednostce czasu.

$$\begin{gathered}
v=\frac{x-x_0}{t-t_0}
\end{gathered}$$

Z pitagorasa prędkość ciała, którego znamy prędkości składowe wyraża się wzorem:
$$\begin{gathered}
v=\sqrt{v_x^2+v_y^2}
\end{gathered}$$

**Def. Prędkości chwilowej**

Prędkość chwilową definiujemy jako prędkość analizując nieskończenie małą ilość czasu. Zatem:
$$\begin{gathered}
v=\lim_{\Delta t \to 0}{\frac{\Delta x}{\Delta t}}
\end{gathered}$$
Co jest przecież definicją pochodnej:
$$\begin{gathered}
v=\frac{d\ x}{d\ t}
\end{gathered}$$
Co więcej zgodnie z naszą wiedzą na temat stycznych do wykresu możemy również zdefiniować jako styczną do wykresu prędkości ciała.


![[diagram-20250319 (3).png]]
**Def. Prędkości średniej**

Gdy określenie zależności $x(t)$ nie jest możliwe lub nie potrzebna jest nam precyzja możemy posłużyć się pojęciem prędkości średniej. Która jest definiowana przez przebytą odległość podzieloną przez czas.

$$\begin{gathered}
\overline{v}=\frac{x-x_0}{t}
\end{gathered}$$

$(x-x_0)$ to odległość przebyta w czasie $t$ 


**Przykładowe zadanie:**
Oblicz drogę hamowania samochodu który hamuje jednostajnie (w sensie ciągle tyle samo się zmniejsza prędkość), a jechał wcześniej z prędkością $20\frac{m}{s}$, i hamował $5s$. 
$$\begin{gathered}
V_{śr}=\frac{20\frac{m}{s}+0\frac{m}{s}}{2}=10\frac{m}{s}\\\\
d=V_{śr}\cdot 5s=50m
\end{gathered}$$


---
### Przyspieszenie:

**Def. Przyspieszenia jednostajnego**
Jeżeli ciało przyspiesza lub hamuje i jego prędkość zmienia się jednostajnie z czasem to przyspieszenie $a$ tego ciała jest stałe.
$$\begin{gathered}
a=\frac{v-v_0}{t}
\end{gathered}$$
Gdy prędkość rośnie ($a\gt 0$) to ruch nazywamy **jednostajnie przyspieszonym**, a gdy
prędkość maleje ($a\lt 0$) to ruch określamy jako **jednostajnie opóźniony**.

**Def. Przyspieszenia chwilowego**
Jeżeli przyspieszenie nie jest stałe, zmienia się z czasem należy ograniczyć się do zmiany prędkości w krótkim czasie $\Delta t$ (tak samo jak dla prędkości chwilowej). Wówczas **przyspieszenie chwilowe** definiujemy jako pierwszą pochodną $v$ względem $t$.

$$\begin{gathered}
a=\frac{dv}{dt}
\end{gathered}$$
---
### Ruch jednostajnie zmienny:

Ruch jednostajnie zmienny to taki ruch z niezerowym stałym przyspieszeniem.

Prędkość ciała poruszającego się ze stałym przyspieszeniem możemy otrzymać ze wzoru:
$$\begin{gathered}
v=v_0+at
\end{gathered}$$
Do policzenia położenia:
$$\begin{gathered}
r=r_0+\overline{v}t
\end{gathered}$$
Łącząc powyższe trzy równania otrzymujemy:
$$\begin{gathered}
r=r_0+\overline{v}t\\
\overline{v}=\frac{v_0+v}{2}\\
v=at\\
r=r_0+v_0t+\frac{at^2}{2}
\end{gathered}$$

Ale lepiej to zapamiętać / zrozumieć poprzez zrozumienie $\frac{at^2}{2}$ z całki Riemenna. A dwa pierwsze czyli $r_0 + v_0t$ to wiadomo.

---
