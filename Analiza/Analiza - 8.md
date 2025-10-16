## Całka Riemenna
#### 2025-01-31
##### Poprzednia: [[Analiza - 7]]
##### Następna: [[Analiza - 9]]
##### Zadania: [[]]

#rachunek_całkowy #całka_riemenna #analiza 

---
### Całka Riemenna

$f:[a,b]\to \mathbb{R}$, ograniczona 
Tworzymy ciąg podziałów $(P_n)_{n\in \mathbb{N}}$ przedziału $[a,b]$
$P_n:a=x_0\lt x_1\lt x_2\lt\dots\lt x_i \lt \dots \lt x_n=b$
$x_0,\dots,x_n$ - punkty podziału
$\Delta x_i=x_i-x_{i-1}, i=1,\dots,n$
$\delta_n=max\{x_i-x_{i-1}:i=1,\dots,n\}$ - średnica podziału $P_n$ 
Ciąg podziałów $(P_n)_{n\in \mathbb{N}}$ nazywamy *normalnym* $\Leftrightarrow \lim_{n\to \infty}{\delta_n=0}$
Niech $P_n$ będzie podziałem przedziału $[a,b]$
W każdym z przedziałów $[x_{i-1},x_{i}]$ wybieramy punkt pośredni $c_1: \forall i=1,\dots,n \ c_i\in [x_{i-1}, x_i]$.
Niech $S_n=\sum^{n}_{i=1}{f(c_i)\Delta x_i}$ - suma całkowa dla podziału $P_n$ przy ustalonym wyborze punktów pośrednich.

**Def.**
Jeśli dla każdego normalnego ciągu podziałów przedziału $[a,b]$ i dowolnego wyboru punktów pośrednich $c_i$ istnieje $\lim_{n\to \infty}{S_n}$ która nie zależy ani od wyboru ciągu podziałów, ani od wyboru punktów pośrednich, to granicę tę nazywamy całką Riemenna funkcji $f$ na przedziale $[a,b]$

$$\begin{gathered}
\int^{b}_{a}{f(x)\ dx}=\underset{\delta_n\to 0}{\lim_{n\to \infty}}{\sum^{n}_{i=1}f(c_i)\Delta x_i}
\end{gathered}$$
gdzie przyjmujemy że:
$$\begin{gathered}
\int^{a}_{a}{f(x) \ dx}=0
\end{gathered}$$
---
**Przykład**:
Oblicz całke Riemenna funkcji stałej $f(x)=K$ na $[a,b]$
$$\begin{gathered}
\int^{b}_{a}K\ dx=\sum^{n}_{i=1}{K\cdot \Delta x_i}=K(b-a)
\end{gathered}$$

---
**Twierdzenie**:
Funkcja ciągła na przedziale domkniętym i ograniczonym $[a,b]$ jest całkowalna w sensie Riemenna

---
**Twierdzenie**:
interpretacja geometryczna całki Riemenna:
Zał: $f:[a,b]\to \mathbb{R}$, ciągła
$\forall x\in [a,b] f(x)\geq 0$

Teza: pole obszaru pod powierzchnią funkcji równe $\int^{b}_{a}{f(x)\ dx}$

---
**Dodawanie przedziałów całek:**
$$\begin{gathered}
\int^{c}_{a}{f(x)\ dx}=\int^{b}_{a}{f(x)\ dx}+\int^{c}_{b}{f(x) \ dx}
\end{gathered}$$

---
**Def.**
Funkcję górnej granicy całkowania nazywamy taką funkcje że:
$$\begin{gathered}
\phi(x)=\int^{x}_{a}f(x) \ dx
\end{gathered}$$
**Twierdzenie**:
Pochodna tej funkcji wynosi:
$$\begin{gathered}
\phi'(x_0)=f(x_0)
\end{gathered}$$
---
**Twierdzenie Newtona Leibniza:**
$$\begin{gathered}
\int^{b}_{a}{f(x) \ dx}=F(b)-F(a)
\end{gathered}$$

---
**Przykład:** Oblicz $\lim_{n\to \infty}{\frac{1}{n+1}+\frac{1}{n+2}+\frac{1}{n+3}+\dots + \frac{1}{n+n}}$
$$\begin{gathered}
S_n=\sum^{n}_{k=1}{\frac{1}{n+k}}=\frac{1}{n}\sum^{n}_{k=1}{\frac{1}{1+\frac{k}{n}}}=\int^{1}_0{\frac{1}{1+x}\ dx}=\ln{|2|}
\end{gathered}$$
---
### Całki niewłaściwe 

1) $f$ jest ciągła w $[a,b)$ ale nie w $b$, lub nie określona w $B
$$\begin{gathered}
\int^{b}_{a}{f(x)\ dx}=\lim_{\beta \to b^-}{\int^{\beta}_{a}{f(x) \ dx}}
\end{gathered}$$
Jeśli istnieje ta granica, to tę granicę nazywamy całką niewłaściwą na $[a,b]$ i mówimy że ta całka jest zbieżna (w przeciwnym wypadku rozbieżna)

2) $f$ jest ciągła w $[a,b)$ ale nie w $b$, lub nie określona w $B
$$\begin{gathered}
\int^{b}_{a}{f(x)\ dx}=\lim_{\alpha \to a^+}{\int^{b}_{\alpha}{f(x) \ dx}}
\end{gathered}$$
3) $f$ jest ciągła w $(a,b)$ ale nie w $a,b$ oraz $x_0\in (a,b)
$$\begin{gathered}
\int^{b}_{a}{f(x) \ dx}=\lim_{\alpha \to a^+}{\int^{x_0}_{\alpha}}{f(x) \ dx}+\lim_{\beta \to b^-}{\int^{\beta}_{x_0}}{f(x) \ dx}
\end{gathered}$$

Analogicznie z $\int^{\infty}_{\infty}$ itd.

---
**Twierdzenie o zbieżności całek:**
Jeżeli mamy funkcje większą od tej której zbieżność chcemy sprawdzić a całka z tamtej większej funkcji jest zbieżna to i nasza jest zbieżna.
