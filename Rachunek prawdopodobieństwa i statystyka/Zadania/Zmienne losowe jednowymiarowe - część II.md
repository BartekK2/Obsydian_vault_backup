
### 1) Urządzenie składa się z $500$ elementów. Każdy z tych elementów może ulec w ciągu roku awarii z prawdopodobieństwem $0.02$. Zakładamy że prawdopodobieństwo awarii pojedynczego elementu nie zależy od stanu pozostałych. Oblicz prawdopodobieństwo uszkodzenia co najmniej 3 elementów w ciągu roku.

- bespośrednio 
  
$$\begin{gathered}
P(X=0)=(0.98)^{500}\\
P(X=1)=\binom{500}{1}0.02\cdot (0.98)^{498}\\
P(X=2)=\binom{500}{2}0.02^2\cdot (0.98)^{497}\\
P(X\geq 3)=1-P(X=1)-P(X=2)
\end{gathered}$$

- korzystając z aproksymacji rozkładem Poissona 
$$\begin{gathered}
\lambda=500 \cdot 0.02=10\\\\
P(X=0)=\frac{e^{-10}10^0}{0!}=e^{-10}\\
P(X=1)=\frac{e^{-10}10^1}{1!}=10\cdot e^{-10}\\
P(X=2)=\frac{e^{-10}10^2}{2!}=\frac{10\cdot e^{-10}}{2}\\
P(X\geq 3 )=1-P(X\leq 2)=1-\dots
\end{gathered}$$

---
### Liczba bramek strzelonych w każdym meczu przez pewną drużynę piłkarską ma rozkład $Pois(2)$. Jakie jest prawdopodobieństwo zdobycia przez tę drużyne co najmniej $5$ bramek w meczu?

$$\begin{gathered}
P(X\leq 4)=e^{-2}+2e^{-2}+\frac{e^{-2}4}{2}+\frac{e^{-2}8}{6}+\frac{e^{-2}16}{24}=\\
=7e^{-2}\\\\
P(X\geq 5)=1-7e^{-2}
\end{gathered}$$

---
### 3. Czas całkowitego zuzycia pewnego typu czołgu (mierzony w latach) jest opisany zmienną losową $T$ o rozkładzie $\gamma$ takim że:
$$\begin{gathered}
E(T)=20\\
Var(T)=5
\end{gathered}$$

Oblicz $P(T\gt 23)$
$$\begin{gathered}
E(T)=\frac{s}{\lambda}=20\\
Var(T)=\frac{s}{\lambda^2}=5\\\\
zatem:\\
\lambda=4\\
s=80\\\\
P(T\gt 23)=?\\\
f(x)=\left\{
\begin{matrix}
0, \ \  x\leq 0\\
\frac{16}{\Gamma(s)}x^{79}e^{-4x} \ \ x\gt 0
\end{matrix}
\right.\\\\
\Gamma(s)=\int^{+\infty}_{0}x^{79}e^{-x=\begin{vmatrix}

\end{vmatrix}}
\end{gathered}$$


**?? DOKOŃCZ KURWA**

---
### 5. Doświadczenie losowe polega na tym że rzucamy symetryczną kostką czworościenną i jeśli wypadnie $4$ powtarzamy rzut. Jeśli kolejny raz wypadnie $4$ po raz kolejny itd. Wartością zmiennej losowej $X$ jest suma wyników wszystkich rzutów. Oblicz wartość oczekiwaną $X$.

$$\begin{gathered}
x=4k+i, k \in \mathbb{N}, i \in \{1,2,3\}\\\\
P(X=x)=\frac{1}{4}^k\cdot \frac{1}{4}\\\\
\mu=\sum^{\infty}_{k=0}{\frac{1}{4^k}\cdot \frac{1}{4}(4k+1+4k+2+4k+3)}=\\
=\sum^{\infty}_{k=0}{\frac{12k+6}{4^{k+1}}}=\frac{6}{4}\sum^{\infty}_{k=0}\frac{2k+1}{4^k}\\\\
\text{reszte sie da policzyc z geo, całki itd}
\end{gathered}$$

---
### 6. Doświadczenie losowe polega na tym, że rzucamy dwoma monetami symetrycznymi i jeśli wypadną $2$ orły powtarzame rzuty. Jeśli kolejny raz wypadną $2$ orły powtarzamy rzuty po raz kolejny i tak dalej. Wartością zmiennej losowej $X$ jest liczba wszystkich wyrzuconych orłów. Oblicz wartość oczekiwaną $X$.


$$\begin{gathered}
P(X=x)\\\\\\
x=2^k+i,k \in \mathbb{N}, i \in \{0,1\}\\\\
P(X=x)=\left (\frac{1}{4}\right)^k\cdot i \left(\frac{3}{4}\right)\\\\

\mu=\sum^\infty_{k=0}\left(\frac{1}{4}\right)^k\cdot \left(\frac{3(2^k+1)}{4}+2^k \right)=\dots

\end{gathered}$$