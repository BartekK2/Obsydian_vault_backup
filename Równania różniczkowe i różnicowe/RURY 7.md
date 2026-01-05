
### $L^p, \ L^1_{LOC}, L^\infty$
$L^p(\Omega)=\{f: \int_\Omega{|f(x)|^p} \lt \infty\}$

Czy $f(x)=\frac{1}{x}$ należy do $L^1$ na $\Omega=(0,1)$?

$$\begin{gathered}
\int^1_0{\left|\frac{1}{x}\right|dx}=
\int^1_0{\frac{1}{x}dx}=\ln{x}|^1_0=-\lim_{x \to 0}{\ln{x}}=\infty\\\\
\implies f \notin L^1(\Omega)
\end{gathered}$$

Za to powyższa funkcja należy do $L^1_{LOC}$ z racji tego że na dowolnym przedziale zamkniętym ma wartość skończoną.

A czy funkcja należy do $L^\infty(\Omega)$? Nie bo jej supremum to nieskończoność!
(Testem czy $f(x)$ należy do $L^\infty(\Omega)$ może być jej norma Supremum)


#### Dlaczego funkcja może nie należeć do $L^p(\Omega)$?

- Osobliwość w jakimś punkcie 
  (dla skończonej przestrzeni zachodzi $f \notin L^p, q \lt p \leftrightarrow f \notin L^q$)
- zbyt wolne zmierzanie do zera gdy $x \to \infty$


#### Norma i implikacje porównawcze funkcji z niej wynikające

Definicja normy w $L^P$:

Dla $1 \leq p \lt \infty$:

$$\begin{gathered}
||f||_{L^p(\Omega)}=\left(\int_\Omega{|f(x)|^p}\right)^{\frac{1}{p}}
\end{gathered}$$
ogólnie można zauważyć że skoro norma jest zdefiniowana całką, to możemy traktować funkcje różniące sie skończoną ilością punktów jako te same funkcje.

a dla $p=\infty$ mamy supremum które też olewa punkty także no.


### $W^{k,p}$ - przestrzenie Soboleva

$f \in W^{n,p}(\Omega)=\{f \in L^p(\Omega): D^\alpha f \in L^p\ \ \ \forall |\alpha| \leq n\}$

gdzie $D^{\alpha}$ oznaczają pochodne dystrybucyjne regularne takie że różniczkujemy po $|\alpha|$ wymiarach to znaczy kiedy różniczkujemy po $x$ dwukrotnie i raz po $y$ to mamy $\alpha=(2,1)$ czyli $|\alpha|=3$


### $H^n(\Omega)=W^{n,2}(\Omega)$ - przestrzeń Hilberta


### Przykładowe sprawdzanie czy $f$ należy do którejś z tych przestrzeni

$$\begin{gathered}
f(x)=\sqrt{x} \ \ \ \Omega=(0,1)\\\\
\text{Czy należy do }L^1?\\\\
\int^{1}_{0}{\sqrt{x}dx}=\frac{2x^{\frac{3}{2}}}{3}|^1_0=\frac{2}{3}\lt \infty\\
\text{tak.}\\\\
\text{Czy należy do }L^2?\\\\
\int^{1}_{0}{\sqrt{x}^2dx}=\frac{1}{2}\lt \infty\\
\text{tak.}
\end{gathered}$$

Przestrzeń $W^{1,1}$

$$\begin{gathered}
\text{wiemy że }f \in L^1\\
\text{ale czy }D^1(f) \text{ też?}\\
\text{dla tego przykładu }D^1(f) \text{ oznacza po prostu:}\\
g=f'(x)=\frac{1}{2\sqrt{x}}\\
\text{też w }L^1 \text{ bo całka z tego równa 1}\\\\
\end{gathered}$$

Przestrzeń $W^{1,2}$ czyli $H^1$

$$\begin{gathered}
\text{wystarczy sprawdzić czy pochodna też należy do }L^2\\\\
\int^1_0{\frac{1}{2\sqrt{x}}^2dx}=\frac{1}{4}\ln{x}|^1_0=\infty
\end{gathered}$$

nie należy


