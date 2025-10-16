### Liczby zespolone
#### 2024-10-02
##### Zadania: [[Algebra - liczby zespolone]]
##### Następna: [[Algebra - 2]]

#Liczby_zespolone #algebra #informacje

---
###### Elżbieta Bratuszewska bratusze@agh.edu.pl 502-511-256 b7 p.17 konsultacje
--- 
- zapoznać się z sylabusem (co ma być wypracowane)
- wejdź na organizacje roku 
---
#### 2025-02-01 - sesja
##### Warunki zaliczenia :
- 2 kolokwia / semestr 40pkt
- aktywność 4pkt (2plusy = 1 punkt)
- obecność 4 pkt 
##### 50% zaliczenie, 2 nb max
do tygodnia zaległe kolokwium uzupełnić 
###### Skoczylas !, Jurkiewicz
---
*W zbiorze liczb zespolonych nie są wprowadzone nierówności.
Część Re z=x i Im z=y - to liczby rzeczywiste. Mnożenie i dodawanie liczb zespolonych jest przemienne i łączne, lecz mnożenie jest rozdzielne względem dodawania.*

*Wniosek: wszystkie własności i twierdzenia wynikające z powyższych własności dodawania i mnożenia w $\mathbb{R}$, są również prawdziwe w $\mathbb{C}$.*

---
#postać_trygonometryczna
#### Jednostka urojona
$$
\sqrt{-1}=i \\
$$
- - -
#### Postacie liczby zespolonej

$$
\begin{gathered}
(x, y)=(x, 0) \oplus\left[\left(y_1 0\right) \oplus(0,1)\right] \\
(x, y)=x+i y \\
z=|z|(\cos \varphi+i \sin \varphi) \\
\left\{\begin{array}{l}
\cos \varphi=\frac{x}{|z|} \\
\sin \varphi=\frac{y}{|z|}
\end{array}\right.
\end{gathered}
$$
Oraz: [[Algebra - 2]] postać wykładnicza.
- - -
#### Działania na liczbach zespolonych

$$
\begin{gathered}
\left(x_1, y_1\right) + \left(x_2, y_2\right)=\left(x_1+x_2, y_1 + y_2\right)\\ 
\left(x_1, y_1\right) - \left(x_2, y_2\right)=\left(x_1-x_2, y_1 -y_2\right)\\ 
\left(x_1, y_1\right) \cdot\left(x_2, y_2\right)=\left(x_1 x_2-y_1 y_2, x_1 y_2+x_2 y_1\right) \\
\frac{(x_1, y_1)}{(x_2, y_2)}=\left(\frac{x_1 x_2+y_1 y_2}{x_2^2+y_2^2}, \frac{-x_1 y_2+x_2 y_1}{x_2^2+y_2^2}\right) \\

z_1 \cdot z_2=\left|z_1\right| \cdot\left|z_2\right|\left(\cos \left(\varphi_1+\varphi_2\right)+\right.
\left.i \sin \left(\varphi_1+\rho_2\right)\right) \\


 \frac{z_1}{z_2}=\frac{\left|z_1\right|}{\left|z_2\right|}\left(\cos \left(\varphi_1-\rho_2\right)+\right. i \sin \left(\varphi_1-\varphi_2\right))
\end{gathered}
$$
-- -
#### Twierdzenia
$$ \begin{gathered} \overline{z_1 z_2}=\overline{z_1} \cdot \overline{z_2} \\
\left|z_1 z_2\right|=\left|z_1\right|\left|z_2\right|\\
z \cdot \overline{z}=|z|^2\\
\overline{\left(\frac{z_1}{z_2}\right)}=\frac{\overline{z_1}}{\overline{z_2}}\\
\left|z_1+z_2\right|
\leqslant\left|z_1\right|+\left|z_2\right| \\\left|\left|z_1\right|-\left|z_2\right|\right| \leqslant\left|z_1-z_2\right| 
\end{gathered}$$
- - -
#### Wzór de Moivre'a - (potęgowanie w postaci tryg.)
#wzor_de_Moivrea
$$\begin{gathered}
z^n=|z|^n(cos(n\varphi)+i\cdot sin(n\varphi)), \; \geq 1 \\ \\
Przykład \ potęgowania: \\ 
z=-2\sqrt{3}-2i \\
|z|=\sqrt{12+4}=4 \\
z^{16}=4^{16}(16*\frac{7\pi}{6}+i sin(16*\frac{7\pi}{6})) \\
z^{16} = 4^{16}(cos(\frac{2\pi}{3})+i\cdot sin(\frac{2\pi}{3})) \\
z^{16}=2^{32}(-\frac{1}{2}+i\cdot \frac{\sqrt{3}}{2}) \\
\end{gathered}$$
---
*Przydatne własności:*

- $arg(-z)=arg(z)+\pi, 0 \leq arg(z) \lt \pi$
- $arg(-z)=arg(z)-\pi, \ \ \pi \leq arg(z) \lt 2\pi$ 
Wynika z tego że zmieniamy zarówno część rzeczywistą i  urojoną, ale jeżeli mamy pod osią ox to odejmujemy pi żeby wrócić na górną część a jeżeli nad ox to dodajemy pi by zejść na dolną część.

- $arg(\frac{1}{z})=2\pi-arg(z)$ 
Wynika to z własności dzielenia w postaci trygonometrycznej (odejmujemy argumenty)

- $arg(\overline{z})=2\pi-arg(z)$
Wynika to z symetrii względem osi Ox którą dostajemy przy zamianie znaku części urojonej

