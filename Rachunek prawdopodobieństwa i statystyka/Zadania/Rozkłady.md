
### 1) Urządzenie składa się z $500$ elementów. Każdy z tych elementów może ulec w ciągu roku awarii z prawdopodobieństwem $0.02$. Zakładamy że prawdopodobieństwo awarii pojedynczego elementu nie zależy od stanu pozostałych. Oblicz prawdopodobieństwo uszkodzenia co najmniej 3 elementów w ciągu roku.

- bespośrednio 

**Jest to rozkład dwumianowy**

$$\begin{gathered}
P(X=1)=\binom{500}{1}0.2\cdot (0.98)^{499}\\
P(X=2)=\binom{500}{2}0.2^2\cdot (0.98)^{498}\\\\
P(X\geq 3)=P(X\gt 2)=1-P(X=1)-P(X=2)
\end{gathered}$$

**Możemy również użyć aproksymacji Poissona**
$$\begin{gathered}
\lambda=500\cdot 0.02=10\\\\
P(X=1)=\frac{e^{-10}10^1}{1!}\\
P(X=2)=\frac{e^{-10}10^2}{2!}\\
P(X\geq 3)=P(X\gt 2)=1-P(X=1)-P(X=2)
\end{gathered}$$

---
### Liczba bramek strzelonych w każdym meczu przez pewną drużynę piłkarską ma rozkład $Pois(2)$. Jakie jest prawdopodobieństwo zdobycia przez tę drużyne co najmniej $5$ bramek w meczu?

$$\begin{gathered}
Pois(2) \text{ oznacza że }\lambda=2\\\\
P(X=1)=\frac{e^{-2}2^1}{1!}\\
P(X=2)=\frac{e^{-2}2^2}{2!}\\
P(X=3)=\frac{e^{-2}2^3}{3!}\\
P(X=4)=\frac{e^{-2}2^4}{4!}\\
P(X\geq 5)=1-P(X=1)-P(X=2)-P(X=3)-P(X=4)
\end{gathered}$$

---
### 3. Czas całkowitego zużycia pewnego typu czołgu (mierzony w latach) jest opisany zmienną losową $T$ o rozkładzie gamma takim że, oblicz $P(T \gt 23)$:
$$\begin{gathered}
E(T)=20, Var(T)=5\\\\
\text{Dla rozkładu Gamma:}\\
\mu=\frac{s}{\lambda}\\
\sigma^2=\frac{s}{\lambda^2}\\\\
20=\frac{s}{\lambda}\\
5=\frac{s}{\lambda^2}\\
\lambda=4,s=80
\end{gathered}$$
