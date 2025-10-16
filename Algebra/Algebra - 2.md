### Liczby zespolone
#### 2024-10-08
##### Zadania: [[Algebra - liczby zespolone]]
##### Następna: [[Algebra - 3]]
##### Poprzednie: [[Algebra - 1]]
#Liczby_zespolone  #algebra   #postać_trygonometryczna 


---
### Odwrotność liczby zespolonej
$$ |z|(cos(\varphi)+i\cdot sin(\varphi)) \cdot \frac{1}{|z|}(cos(-\varphi)+i\cdot sin(-\varphi))=1, \ z\neq0$$

---
### Pierwiastkowanie liczb zespolonych

$$\begin{gathered}\sqrt[n]{z} = w: \, \Leftrightarrow w^n=z\\
w^n=z, |w|^n(cos(n\varphi)+i\cdot sin(n\varphi))=|z|(cos(\varphi)+i \cdot sin(\varphi)) \\ 

|w|^n=|z| \wedge \exists k\in \mathbb{Z}: k= n\varphi = 2k\pi
|w| = \sqrt[n]{|z|}, \ \alpha = \frac{\varphi + 2k\pi}{n} \\ \\
\sqrt[n]{z}=\sqrt[n]{|z|}(cos(\frac{\varphi+2k \pi}{n})+i \cdot \sin(\frac{\varphi+2k \pi}{n}))

\end{gathered}$$

#### Formalnie $\sqrt[n]{z}$ definiuje sie jako zbiór wszystkich tych $w_k$:

$$ \sqrt[n]{z}:= \{w_0,w_1,...,w_{n-1}\}$$

#### Przykład:
$$\begin{gathered}
\sqrt[3]{1}, \ z=1=1(cos(0)+i\cdot sin(0)), \\
w_0=\sqrt[3]{1}(cos(\frac{0+2\cdot0\cdot \pi}{3})+i \cdot sin(\frac{0+2\cdot0\cdot \pi}{3}))
 \\
w_1=\sqrt[3]{1}(cos(\frac{0+2\cdot1\cdot \pi}{3})+i \cdot sin(\frac{0+2\cdot1\cdot \pi}{3}))\\
w_2=\sqrt[3]{1}(cos(\frac{0+2\cdot2\cdot \pi}{3})+i \cdot sin(\frac{0+2\cdot2\cdot \pi}{3}))

\end{gathered}$$

##### Pierwiastków $\sqrt[n]{z}, \ z \neq 0$ jest n i leżą one na okręgu o środku w (0,0) i promieniu $\sqrt[n]{|z|}$, dzieląc ten okrąg na n równych części.
(Rysunek)


#### Postać wykładnicza liczb zespolonych:
Postać wykładnicza jest jedną z [[Algebra - 1#Postacie liczby zespolonej|postaci liczb zespolonych]]

$$\begin{gathered}
Dla \ dowolnej \ liczby \ \varphi \in \mathbb{R}, \ oznaczamy:\\
e^{i\varphi} = \cos{\varphi} + i\cdot \sin{\varphi}\\\\
Z \ wzorow / tozsamosci \ z \ postaci \ trygonometrycznej \ wynikaja \ ponizsze.\\
e^{i(\varphi_1+\varphi_2)}=e^{i\varphi_1}\cdot e^{i\varphi_2}\\
e^{i(\varphi_1-\varphi_2)}=\frac{e^{i\varphi_1}}{e^{i\varphi_2}}\\
(e^{i\varphi})^k=e^{ik\varphi}\\
e^{i\varphi_1}=e^{i\varphi_2} \leftrightarrow \varphi_1\equiv \varphi_2 \ (mod \ 2 \pi) \\
Zatem: \  z=re^{i\varphi}, \ gdzie \ r=|z| \geq 0\\
To \ wlasnie \ re^{i\varphi} \ - \ nazywamy \ postacia \ wykladnicza. \\\\
\overline{z} = re^{-i\varphi} \\
-z=re^{i(\varphi+\pi)}\\
\frac{1}{z}=\frac{1}{r}e^{-i\varphi}\\
z^k = r^ke^{ik\varphi}\\
z_1z_2 = r_1r_2 e^{i(\varphi_1+\varphi_2)}\\
\frac{z_1}{z_2}=\frac{r_1}{r_2}e^{i(\varphi_1-\varphi_2)}\\
\end{gathered}$$



