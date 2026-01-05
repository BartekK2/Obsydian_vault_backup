### Współczynnik asymetrii 

**Definicja**

**Współczynnikiem asymetrii** lub **skośności** rozkładu zmiennej $X$ nazywa się liczbę:
$$\begin{gathered}
A=\gamma_1 =\frac{\mu_3}{\sigma^3}
\end{gathered}$$
Rozkład, dla którego:
- $A=0$ nazywa się **symetrycznym**
- $A \gt 0$ nazywa się **prawostronnie (dodatnio) skośnym**
- $A \lt 0$ nazywa się **lewostronnie (ujemnie) skośnym**

($\mu_x$ to był ten moment centralny a $\sigma^3$ to nic innego jak odchylenie standardowe do potęgi trzeciej)

**Dla przypomnienia $\mu_x$ liczymy jako $\mu_k=E((X-\mu)^k)$**

$$\begin{gathered}
\mu=\sum^{n}_{i=0}{x_i\cdot p(x_i)}\\
\mu=\int^{+\infty}_{-\infty}xf(x) dx\\\\
\mu_k=\sum_{i: x_i \in S}(x_i-\mu)^k p(x_i)\\
\mu_k=\int^{+\infty}_{-\infty}(x-\mu)^k f(x) dx\\\\\\
Var(x)=\sigma^2_X=\sigma^2\overset{def}{=}\mu_2=E((X-\mu)^2)
\end{gathered}$$

---
### Kurtoza 

**Definicja**

**Kurtozą** nazywa się liczbe:
$$\begin{gathered}
Kurt(X)=K=\frac{\mu_4}{\sigma^4}
\end{gathered}$$
natomiast **kurtozą nadwyżkową** nazywa się liczbe 
$$\begin{gathered}
\gamma_2=Kurt(X)-3
\end{gathered}$$
(bo dla rozkładu normalnego wychodzi zawsze 3)

- Jeśli $\gamma_2=0$ to rozkład nazywamy **mezokurtycznym**
- Jeśli $\gamma_2 \gt 0$ to rozkład nazywamy **leptokurtycznym**
- Jeśli $\gamma_2 \lt 0$ to rozkład nazywamy **platykurtycznym**

---
### Kwantyle i mediana 

**Definicja**
**Kwantylem rzędu** $p \in (0,1)$ zmiennej losowej $X$ o dystrybuancie $F$ nazywamy dowolna liczbę $q_p \in \mathbb{R}$ taką, że
$$\begin{gathered}
F(q_p-)\leq p \leq F(q_p)
\end{gathered}$$
Kwantyl $q_{0.5}$ rzędu $\frac{1}{2}$ nazywamy **medianą**, kwantyl rzędu $\frac{1}{4}$ nazywamy **dolnym kwartylem**, a kwantyl rzędu $\frac{3}{4}$ nazywamy **górnym kwartylem**

**Uwaga**
Jeśli $X$ ma rozkład ciągły, to kwantylem $q_p$ rzędu $p$ jest dowolne rozwiązanie równania

$$\begin{gathered}
F(q_p)=p
\end{gathered}$$
---
### Moda 

**Definicja**

**Modą** zmiennej losowej o rozkładzie dyskretnym nazywa się dowolne maksimum funkcji prawdopodobieństwa tego rozkładu.

**Dla rozkładów ciągłych** - maksimum lokalne gęstości.

**DOWOLNE** ZATEM MOŻEMY ROZPATRYWAĆ MAKSIMA LOKALNE A NIE GLOBALNE

---
### Rozkład jednopunktowy 

Jeśli $S=\{x_0\}$ i $p(x_0)=1$, to mówimy że zmienna losowa ma **rozkład jednopunktowy**. Wtedy:
$$\begin{gathered}
\mu=x_0\\
Var(X)=0\\
A=0\\
K=0\\
\gamma_2=-3
\end{gathered}$$

---
### Rozkład dwupunktowy 

Jeśli 
$$\begin{gathered}
S=\{x_1,x_2\}
\end{gathered}$$
oraz:
$$\begin{gathered}
p(x_1)=\theta, \ \ p(x_2)=1-\theta
\end{gathered}$$

dla pewnego $\theta \in (0,1)$ to mówimy że zmienna losowa ma **rozkład dwupunktowy z parametrem** $\theta$.

$$\begin{gathered}
\mu=\theta x_1+(1-\theta)x_2\\
\vdots
\end{gathered}$$

---
### Rozkład Bernoulliego 

to rozkład dwupunktowy gdzie $x_2=0$ (inaczej rozkład **zero-jedynkowy**).

Notacja:
$$\begin{gathered}
X \sim Bern(\theta)
\end{gathered}$$

---
### Dyskretny rozkład jednostajny 

Jeśli $S=\{x_1,\dots,x_n\}$ i $p(x_i)=\frac{1}{n}$ dla każdego $i$ to mówimy że zmienna losowa ma **dyskretny rozkład jednostajny** na $n$ punktach.

Wówczas:
$$\begin{gathered}
\mu=\overline{x}=\frac{1}{n}\sum^{n}_{i=1}x_i\\
\sigma^2=\frac{1}{n}\sum^{n}_{i=1}(x_i-\mu)^2\\
\vdots
\end{gathered}$$
---
### Próba Bernoulliego

Rozważmy doświadczenie losowe o dwu możliwych wynikach 

- sukces osiągamy z $p=\theta$
- porażke z $p=1-\theta$

Doświadczenie takie jest **próbą Bernoulliego**. Modelowane przez zmienną o rozkładzie dwupunktowym.

---
### Schemat dwumianowy 

Schematem doświadczenia określony jako $n$-krotne powtórzenie próby Bernoulliego w ten sposób że próby są **niezalenże** nazywa się **schematem dwumianowym** albo **schematem Bernoulliego**.

Liczba powtórzeń $(n)$ nazywa się **długością schematu**

Długość schematu może być również **nieskończona**.


#### Rozkład dwumianowy 

Niech $X$ będzie zmienną losową, której wartością jest **liczba sukcesów w schemacie dwumianowym o długości $n$ z $p=\theta$**

Wówczas $X$ ma rozkład dyskretny w którym:
$$\begin{gathered}
S=\{0,\dots,n\}
\end{gathered}$$

oraz $p(X=k)=\binom{n}{k}\theta^k (1-\theta)^{n-k}$

Notacja to:
$$\begin{gathered}
X \sim Binom(n,\theta)
\end{gathered}$$
$$\begin{gathered}
\mu=n \theta\\
\sigma^2=n \theta(1-\theta)\\
\vdots
\end{gathered}$$

---
### Rozkład geometryczny

Mówimy, że zmienna losowa $T$ ma **rozkład geometryczny** z parametrem $\theta$ tzn:
$$\begin{gathered}
T \sim Geom(\theta)
\end{gathered}$$

jeśli:
$$\begin{gathered}
S=\mathbb{N} \setminus \{0\}
\end{gathered}$$
a funkcja prawdopodobieństwa ma postać:
$$\begin{gathered}
p(k)=(1-\theta)^{k-1}\theta
\end{gathered}$$

Zmienna $T$ opisuje czas oczekiwania na pierwszy sukces w schemacie dwumianowym (o nieskończonej długości).

$$\begin{gathered}
p(k)=\sum^{\infty}_{k=1}{(1-\theta)^{k-1}\theta}\\\\
\text{Policzmy}\\
\mu=\sum k(1-\theta)^{k-1}\theta\\\\
\mu=\theta\sum k(1-\theta)^{k-1}\\\\
\int\sum k(1-\theta)^{k-1}d \theta=\begin{vmatrix}
w=1-\theta\\
dw=-d \theta
\end{vmatrix}=-\int \sum kw^{k-1}\\
=-\sum w^k=-\frac{1}{1-(1-\theta)}=-\frac{1}{\theta}\\
(-\frac{1}{\theta})'=\frac{1}{\theta^2}\\\\
\mu=\frac{1}{\theta}
\end{gathered}$$

reszte jakoś podobnie należy liczyć :/

---
### Rozkład Poissona

Jeśli zmienna $N$ o wartościach w $\mathbb{N}$ opisuje liczbę wystąpień pewnego powtarzalnego zdarzenia w przedziale czasowym $[0,t]$ przy czym spełnia następujące założenia:

- powtórzenie zdarzenia wystąpują niezależnie od siebie 
- intensywność wystąpień $r \gt 0$ czyli średnia liczba wystąpień w jednostce czasu jest stała
- w danej chwili (bardzo mały przedział) może zajść co najwyżej jedno powtórzenie 

to zmienna ma **rozkład Poissona** z **parametrem** $\lambda=rt$ tzn:

$$\begin{gathered}
N \sim Pois(\lambda)=Pois(rt)
\end{gathered}$$

Rozkład Poissona jest rozkładem dyskretnym w którym:
$$\begin{gathered}
S=\mathbb{N}\\
p(k)=\frac{e^{-\lambda}\lambda^k}{k!},k=0,1,\dots
\end{gathered}$$

$$\begin{gathered}
\mu=\lambda\\
\sigma^2=\lambda\\
A=\frac{1}{\sqrt{\lambda}}\\
\gamma_2=\frac{1}{\lambda}
\end{gathered}$$
---
