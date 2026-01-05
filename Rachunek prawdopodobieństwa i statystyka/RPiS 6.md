
### Rozkład jednostajny 

Mówimy, że zmienna losowa $X$ ma rozklad jednostajny na przedziale $[a,b]$ tzn $X \sim \mathbb{U}(a,b)$ jeśli jej gęstość wyraża się wzorem:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{1}{b-a}, \ dla \ x \in [a,b]\\
0 \ dla \ x \notin [a,b]
\end{matrix}
\right.
\end{gathered}$$

Dystrybuanta takiej zmiennej ma postać:
$$\begin{gathered}
F(x)=\left\{
\begin{matrix}
0, \ \ dla \ x \lt a\\
\frac{1}{b-a}(x-a), \ dla \ a \leq x \leq b\\
1, \ \ dla \ x \gt b
\end{matrix}
\right.
\end{gathered}$$
wartość oczekiwana to oczywiście:
$$\begin{gathered}
\mu=\frac{a+b}{2}
\end{gathered}
$$

---
### Rozkład wykładniczy 

Niech $T$ będzie zmienną modelującą czas oczekiwania na pierwsze zdarzenie w ciągu zdarzeń takim, że ich liczba w przedziale $[0,t]$ opisana jest przez zmienną $X$ o rozkładzie Poissona z parametrem $\lambda t$. Wtedy:
$$\begin{gathered}
P(T \gt t)=P(X=0)=e^{-\lambda t}\\
P(T \gt 0)=1
\end{gathered}$$
Zatem dystrybuanta $T$ ma postać:
$$\begin{gathered}
F(t)=1-P(T \gt t)=\left\{
\begin{matrix}
0, \ \  dla \ \ t \leq 0\\
1-e^{-\lambda t}, \ \  dla \ \  t \gt 0
\end{matrix}
\right.
\end{gathered}$$
Mówimy wtedy że $T$ ma **rozkład wykładniczy z parametrem** $\lambda$, tzn $T \sim Exp(\lambda)$. Gęstość rozkładu wykladniczego ma postać:
$$\begin{gathered}
f(t)=\left\{
\begin{matrix}
0, \ \  dla \ \  t\leq 0\\
\lambda e^{-\lambda t}, \ \  dla \ \ t\gt 0
\end{matrix}
\right.
\end{gathered}$$
Wielkości:
$$\begin{gathered}
\mu=\frac{1}{\lambda}\\
\sigma^2=\frac{1}{\lambda^2}
\end{gathered}$$
**chcesz wiedzieć, ile czasu minie do pierwszego zdarzenia → bierzemy wykładniczy**

---
### Rozkład gamma 

Mówimy że zmienna losowa $X$ ma **rozkład gamma z parametrami** $s \gt 0$ i $r \gt 0$ tzn. $X \sim Gamma(s,r)$ jeśli jej gęstość wyraża się wzorem:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
0, \ \  x\leq 0\\
\frac{r^2}{\Gamma (s)}x^{s-1}e^{-rx}, \ \ x\gt 0
\end{matrix}
\right.\\\\
gdzie: \Gamma: (0, +\infty)\to (0, + \infty) \ jest \ tzw. funkcja \ Eulera\\\\
\Gamma(s)=\int^{+\infty}_{0}x^{s-1}e^{-x}dx
\end{gathered}$$

**Jak długo muszę czekać, aż zdarzą się k zdarzenia?**

W szczególności:
$$\begin{gathered}
Gamma(1,\lambda)=Exp(\lambda)
\end{gathered}$$

$\lambda$ - ile zdarzeń średnio zachodzi w jednostce czasu
$s$ - ile zdarzeń chcemy "odczekać"

Wielkości opisujące podobne do Poissona:
$$\begin{gathered}
\mu=\frac{s}{\lambda}\\
\sigma^2=\frac{s}{\lambda^2}
\end{gathered}$$
Dobrym przykładem opisującym to jest taki że s to  ilość mikrouszkodzeń samochodu potrzebna by samochód sie zepsuł (tj poluzowana śrubka, korozja etc). Jeszcze działa ale jest w gorszym stanie. A $\lambda$ ile takich mikrouszkodzeń dzieję się w danej jednostce czasu. Pozwala to nam modelować prawdopodobieństwo na to że w danym okresie czasu zdarzy się $k$ wydarzeń

---
