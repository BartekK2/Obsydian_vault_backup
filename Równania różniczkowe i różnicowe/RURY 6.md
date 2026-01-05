
## Przestrzenie funkcyjne

### Zacznijmy od słownika symboli matematycznych:

#### $C^k(\Omega)$

Przestrzeń funkcji "gładkich" na zbiorze $\Omega$ czyli zbiór który zawiera wszystkie funkcje które można różniczkować i dalej mieć funkcje ciągłą.

W szczególności:
$C^0$ - funkcja ciągła,
$C^1$ - funkcja ciągła i jej pochodna ciągła
$\vdots$
$C^\infty$ - funkcja idealnie gładka. można ją różniczkować w nieskończoność

#### $L^k(\Omega)$

To przestrzeń funkcji "całkowalnych z potęgą $k$".

Funkcja należy do $L^k$ jeśli $\int_\Omega{|f(x)|^k dx} \lt \infty$

**Intuicja:**

$L^1 \implies$ funkcja ma skończone pole pod wykresem

#### $L^1_{LOC}(\Omega)$

Funkcja lokalnie całkowalna czyli $\forall K \subset \Omega \ \ \ K - zwarty$ 
zachodzi $\int^{}_{K}{|f(x)|dx} \lt \infty$ 

ważnym jest że $K$ jest domknięte i ograniczone a także leży wewnątrz $\Omega$
#### $<f,g>$ 

To po prostu iloczyn skalarny, w tym kontekście to wynik całki $\int{f(x)g(x) dx}$ 

#### support $(supp \varphi)$

Obszar na którym funkcja ma inne wartości niż zero

#### Zbiór zwarty

Taki bez dziur i zawierający swoją granice no

#### Zbiór zupełny

Jeśli liczymy granice ciągu którego elementy należą do tego zbioru to i ostateczny wynik musi też należeć do tego zbioru.

#### $D(\Omega)=C^\infty_c(\Omega)$ 

ta mała literka $c$ oznacza że funkcja staje sie zerem zanim dotrze brzegu $\Omega$ od angielskiego compact - zwarty nośnik

### Przejdźmy do skryptu

#### Wstęp

$\Omega$ - zbiór otwarty (w skrypcie są dodatkowe warunki żeby to był w miare normalny ładny zbiór a nie jakiś pojebany)

Powiedziane też jest że:
$C^0(\Omega) \supset C^1(\Omega) \supset C^2(\Omega) \supset \dots \supset C^\infty(\Omega)$ 

Zdefiniowali też co oznacza $C^k(\overline{\Omega})$:
$\overline{\Omega}$ - domknięty zbiór np $(0,1) \to [0,1]$

Z powodu jakichś matematycznych problemów z definicją nie da sie sprawdzać ciągłości na zamkniętych więc rozpatrujemy czy istnieje zbiór otwarty zawierający $\overline{\Omega}$ w którym zachodzi warunek $C^k$

#### Problem 

Oznajmiają nam że przestrzenie $C^k$ nie są zupełne i pokazany jest dowód:

dla dowolnego naturalnego $n$
$$\begin{gathered}
C^1((-1,1)) \ni \sqrt{\frac{1}{n}+x^2}
\end{gathered}$$
gdy dążymy $n \to \infty$ otrzymujemy $|x|$ które $\notin C^1((-1,1))$

implikacją jest że nie ma przestrzeni Banacha - oznacza to tyle że nasza przestrzeń ma "dziury" czyli ciąg ładnych funkcji ucieka w brzydkie. (przez co niektóre obliczenia mogą być niemożliwe)

#### Rozwiązanie

Skoro $C^k$ okazało się nieodpowiednie musimy zmienić reguły gry. $C^k$ sprawdza nam ciągłość/różniczkowalność w każdym punkcie przedziału. Zamiast tego sprawdzamy całki. (Dlatego że całka w punkcie jest równa zero czyli nic nie mówi, nic nie znaczy pojedynczy dziwny punkt).

Na przykład rozpatrzmy tutaj $L^2$ i zróbmy ponownie poprzedni przykład:

$$\begin{gathered}
\lim_{n \to \infty}{\int_{(0,1)}{\left(\sqrt{\frac{1}{n}+x^2}\right)^2}dx} \lt \infty \implies \in L^2
\end{gathered}$$

Wprowadzone zostało twierdzenie o reprezentacji Riesza, mówi ono że dowolną funkcje $f: f \in L^2(\Omega)$ można jednoznacznie reprezentować za pomocą $\langle f, \varphi \rangle$

To znaczy rozpatrujemy wszystkie funkcje $\varphi$ i to jak $f$ oddziałuje z nimi i to nam mówi co to jest za funkcja $f$. (Nawet jeśli dwie funkcje dają ten sam wynik z każdym $\varphi$ to oznacza to że różnią sie one jedynie w pojedynczych punktach i traktujemy je jako te same funkcje).

Możemy rozpatrywać $\varphi$ które należą do $C^\infty_0(\Omega)$ - czyli funkcje klasy $C^\infty(\Omega)$ które jednak na pewnym przedziale "zasypiają" - mają wartość $0$.

Przechodzimy do $L^1_{LOC}$ - lokalnej całkowalności, korzystając z tego zbioru uogólniamy twierdzenie Riesza.

Dostajemy wniosek że dla $\varphi \in C^\infty_0(\Omega)$ oraz $f \in L^1_{LOC}(\Omega)$ mamy:

$$\begin{gathered}
\text{dla supportu (przedziału dla którego }\varphi \text{ różne od 0):}\\
supp\ \varphi=K \subset \Omega\\\\
|\langle f, \varphi \rangle| \leq \int_\Omega{|f||\varphi|}=\int_K{|f||\varphi|}\leq M \int_K{|f|}
\end{gathered}$$
czyli w skrócie kiedy sprawdzamy oddziaływanie $f,\varphi$ możemy rozpatrywać tylko przestrzeń supportu $\varphi$, i skoro $\varphi$ jest skończone (mniejsze od nieskończoności z racji tego że ciągłe) w każdym punkcie możemy dobrać stałą taką że ta stała przemnożona przez całke po $f$ jest większa od tego oddziaływania.

Czyli dostajemy iniekcje (f. różnowartościowa) z $L^1_{LOC}(\Omega) \to (C^\infty_c(\Omega))$. 

W tej iniekcji argumentem jest funkcja $f$ a wartością jest przypisywana jej dystrybucja - czyli "maszyna" która przyjmuje funkcje testową a zwraca liczbe:

$$\begin{gathered}
T_f: \varphi \to \int{f(x)\varphi(x) dx}
\end{gathered}$$

---

## Z filmiku 

### Dystrybucje

$f \in C(\overline{\Omega})$

$T_f : \varphi \to \int_\Omega{f \varphi dx}$

$T_f : D(\Omega) \to \mathbb{R}$ gdzie $D(\Omega)=C^\infty_c(\Omega)$ czyli funkcje nieskończenie gładkie, nie posiadające nigdzie nieskończoności i przed końcami przedziału uderzające w 0

![[Pasted image 20260103172120.png]]

$T_f(\alpha \varphi + B \psi)=\alpha T_f(\varphi)+\beta T_f(\psi)$ - liniowość

$D'(\Omega)$ - przestrzeń funkcjonałów liniowyuch na $D(\Omega)$
zatem $T_f \in D'(\Omega)$

dystrybucja = element $D'(\Omega)$
a dystrybucja regularna to $T_f$ w sensie po prostu $T_f$ to konkretny rodzaj dystrybucji a jest ich więcej jak np Delta diraca

Delta diraca oznaczana jako $\delta$ lub $\delta_0$ to dystrybucja nieregularna. Jej działanie na funkcję testową $\varphi \in D(\Omega)$ jest:

$$\begin{gathered}
\langle \delta, \varphi \rangle = \varphi(0)
\end{gathered}$$

### Dystrybucje - różniczkowanie

$f \in C^1(\overline{\Omega})$ - zakładamy 
$\langle T_{f'}, \varphi \rangle = \int_{\Omega}f' \varphi dx=f \varphi|^b_a - \int_\Omega{f \varphi' dx}$

Zakładając że $\varphi \in C^1(\overline{\Omega})$ oraz że funkcja zeruje sie na brzegach wtedy dostaniemy implikacje że $f \varphi|^b_a=0$
a co za tym idzie:
$\langle T_{f'},\varphi \rangle=-\langle T_f, \varphi' \rangle$

Możemy użyć tą relacje żeby uogólnić znaczenie różniczkowania.

ten zapis z $T_f$ miał nam jedynie oznajmić że dla każdej funkcji której możemy przypisać dystrybucje, dla każdej która ma dystrybucje regularną zachodzi:
$$\begin{gathered}
\langle f', \varphi \rangle = - \langle f, \varphi' \rangle
\end{gathered}$$
zachodzi nawet ogólniejszy przypadek:
$$\begin{gathered}
\langle F^n, \varphi \rangle = (-1)^n \langle F, \varphi^n \rangle
\end{gathered}$$
ale tutaj już założeniem będzie oczywiście że sie zeruje pochodna n-tego stopnia na brzegu itd

a dla wymiarowej funkcji:
$$\begin{gathered}
\langle \frac{\partial f}{\partial x_k}, \varphi \rangle = - \langle F, \frac{\partial \varphi}{\partial x_k} \rangle
\end{gathered}$$

i dla dowolnej kolejności pochodnych cząstkowych też.

---
### Zadania:

Oblicz pochodną dystrybucyjną funkcji $f(x)=|x|$ na $\Omega=(-1,1)$.

$$\begin{gathered}
\langle f', \varphi \rangle = - \langle f, \varphi' \rangle=\dots\\\\\\
\dots=-\int^{1}_1{|x|\varphi'dx}=-\int^{1}_0{x\varphi'dx}-\int^{0}_{-1}{-x \varphi' dx}=\\
=- \left(x \varphi|^1_0 -x \varphi|^0_{-1} -\int^{1}_{0}{\varphi}dx+\int^{0}_{-1}{\varphi dx
}\right)=\\
=\int^{1}_{0}{\varphi}dx-\int^{0}_{-1}{\varphi dx
}=\int^{1}_{-1}{g(x)\varphi(x) dx}\\\\
\text{gdzie:}\\\\
g(x)=\left\{
\begin{matrix}
-1, dla \ \ x \lt 0\\
1, dla \ \ x \gt 0
\end{matrix}
\right.
\end{gathered}$$

wniosek:
pochodną (słabą) - czyli dystrybucyjną funkcji $|x|$ jest $sgn(x)$

##### 3. zadanie

Oblicz pochodną dystrybucyjną funkcji skoku, która zaczyna się w innym punkcie niż zero:$$f(x) = \begin{cases} 0 & \text{dla } x < 3 \\ 1 & \text{dla } x \geq 3 \end{cases}$$
$$\begin{gathered}
\text{Załóżmy }\Omega=\mathbb{R}\\\\
\langle f', \varphi \rangle = - \langle f, \varphi' \rangle\\\\\
\langle f', \varphi \rangle=-\int^{+\infty}_{-\infty}{f(x)\varphi' dx}=
- \int^{\infty}_{3}{\varphi' dx}=-\varphi|^{\infty}_3=\\\\
\text{funkcja testowa zeruje sie przy brzegach}\\\\
=\varphi(3)=\delta_3
\end{gathered}
$$

###### Zadanie 4: Druga pochodna (Wyższy poziom)Skoro $H' = \delta$ (pochodna skoku to Delta Diraca), to czym jest $H''$? Innymi słowy, oblicz pochodną dystrybucji $\delta$.Wzór: $\langle \delta', \varphi \rangle = - \langle \delta, \varphi' \rangle$.

$$\begin{gathered}
\langle \delta', \varphi \rangle = - \langle \delta, \varphi' \rangle\\\\\
\langle \delta', \varphi \rangle =-\varphi'(0)
\end{gathered}$$


##### 2. Niech $f(x)$ będzie dana na $\Omega=(-1,1)$ przez:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
x^2\sin{\frac{1}{x}}\ \ \ dla \ \  x \neq 0\\
0 \ \ \ dla \ \  x = 0
\end{matrix}
\right.
\end{gathered}$$

a) Czy $f$ posiada pochodną w każdym punkcie dziedziny?

Dla $x \neq 0$
$$\begin{gathered}
f'(x)=2x \sin{\frac{1}{x}}+x^2 \cos{\frac{1}{x}}\cdot -\frac{1}{x^2}=2x \sin{\frac{1}{x}}-\cos{\frac{1}{x}}
\end{gathered}$$
A dla $x=0$
$$\begin{gathered}
f'(0)=\lim_{h \to 0}\frac{f(0+h)-f(0)}{h}=\frac{h^2 \sin{\frac{1}{h}}}{h}=h \sin{\frac{1}{h}}\lt h \cdot 1 = 0
\end{gathered}$$

posiada

b) Jeśli tak, czy jest ona ograniczona?

no jest bo składa sie z funkcji trygonometrycznych które są ograniczone, a postawienie x przed jedną z nich dla tej dziedziny nic nie zmienia

c) Czy $f \in C^1(\Omega)$?

funkcja jest ciągła, to widać
ma pochodną wszędzie która dodatkowo jest ograniczona

jedyne pytanie to czy ta pochodna jest ciągła

$$\begin{gathered}
\lim_{x \to 0}2x \sin{\frac{1}{x}}-\cos{\frac{1}{x}}- nie \ istnieje
\end{gathered}$$

pochodna nie zbiega do swojej wartości w punkcie 0 

zatem nie należy do $C^1(\Omega)$

---
##### 4. Niech $f(x)=|x|^{-p}$, $p \in \mathbb{R}$. Dla jakich wartości $p$ zachodzi $f \in L^1_{LOC}(\Omega)$, jeśli dziedzina to:

a) $\Omega=(-1,1) \subset \mathbb{R}$

$$\begin{gathered}
dla \ \ a\gt 0 \ \ oraz \ \ b\lt 1\\\\
\int^b_a{|x|^{-p}}=\int^b_a{x^{-p}}=\frac{1}{x^{p-1}(-p+1)}|^b_a \text{ - dla }a=0 \text{ nie ograniczone}\\
\end{gathered}$$

nie należy do całkowalnych lokalnie dla $p \neq 1$ 


##### 5. Niech $f(x)=||x|-1|$ na dziedzinie $\Omega=(-2,2)$

a) Policz dwie pierwsze pochodne dystrybucyjne $f$


Najpierw znajdźmy odpowiednie postaci:
$$\begin{gathered}
|x|-1\gt 0\\
|x| \gt 1\\
x\gt 1\vee x\lt -1\\\\
f(x)=\left\{
\begin{matrix}
x-1, x \in (1,2)\\
-x-1, x \in (-2,-1)\\
x+1, x \in (-1,0)\\
-x+1, x \in (0,1)
\end{matrix}
\right.
\end{gathered}$$

pierwsza pochodna jest po prostu:
$$\begin{gathered}
f'(x)=\left\{
\begin{matrix}
1, x \in (1,2)\\
-1, x \in (-2,-1)\\
1, x \in (-1,0)\\
-1, x \in (0,1)
\end{matrix}
\right.
\end{gathered}$$
co w zapisie dystrybucyjnym da to samo, to jest pochodna dystrybucyjna regularna


druga pochodna:

$$\begin{gathered}
\langle f'', \varphi \rangle =- \langle f', \varphi' \rangle\\\\
\langle f', \varphi' \rangle = \int^{2}_{1}\varphi'+\int^{1}_{0}-\varphi'+\int^{0}_{-1}\varphi'+\int^{-1}_{-2}-\varphi'=\\
=\varphi|^2_1-\varphi|^1_0+\varphi|^0_{-1}-\varphi|^{-1}_{-2}=\\=-\varphi(1)-\varphi(1)+\varphi(0)+\varphi(0)-\varphi(-1)-\varphi(-1)=\\=
-2\delta_{1}+2\delta_0-2\delta_{-1}
\end{gathered}$$

to nie jest pochodna dystrybucyjna regularna bo składa się z delt diraca ( a przynajmniej ich przesunięć )

---
