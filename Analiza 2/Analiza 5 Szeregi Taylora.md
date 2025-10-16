### Szeregi Taylora
#### 2025-04-01
##### Poprzednia: [[Analiza 4 Szeregi potęgowe]]
##### Następna: [[Analiza 6 Szeregi Fouriera]]
##### Zadania: [[Zadania Szeregi]]

#szeregi_taylora #analiza2  

---
**Twierdzenie** o wzorze Taylora:

zał: $U$ - otoczenie punktu $x_0$
$f\in C^n(U)$
$x\in U$
teza: $\exists c \in (x_0,x): f(x)=\sum^{n-1}_{k=0}{\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k}+R_n(x_0,x)$, gdzie $R_n(x_0,x)=\frac{f^{(n)}(c)}{n!}(x-x_0)^n$

**Twierdzenie** o rozwijaniu funkcji w szereg Taylora:

zał: $U$ - otoczenie punktu $x_0$
$f\in C^\infty(U)$
$x\in U$
$\forall x \in U$ $\lim_{n\to \infty}{R_n(x_0,x)}=0$
teza: $f(x)=\sum^{\infty}_{n=0}{\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n}$

**Przykład:**
$$\begin{gathered}
e^x=\sum^{\infty}_{n=0}{\frac{x^n}{n!}},x \in \mathbb{R}\\
\sin{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n+1}}{(2n+1)!}}, x \in \mathbb{R}\\
\cos{x}=\sum^{\infty}_{n=0}{\frac{(-1)^nx^{2n}}{(2n)!}}, x \in \mathbb{R}\\

\end{gathered}$$

**Przykłady:**
Rozwinąć w szereg Maclaurina $f(x)=\frac{1}{1-x}$
$$\begin{gathered}
(\frac{1}{1-x})'=-\frac{1}{(1-x)^2}\cdot (1-x)'=\frac{1}{(1-x)^2}\\
(\frac{1}{(1-x)^2})'=\frac{-2}{(1-x)^3}\cdot -1 = \frac{2}{(1-x)^3}\\\\
\dots\\
f^{(n)}=\frac{n!}{(1-x)^{n+1}}\\
f^{(n)}(0)=n!\\\\
\frac{1}{1-x}\eqsim 1+x+x^2+x^3\dots\\\\
\frac{1}{1-x}=\sum^{\infty}_{n=0}{x^n}
\end{gathered}$$

Rozwiń $f(x)=\frac{2x}{3-4x}$
$$\begin{gathered}
f(x)=\frac{2x}{3-4x}=2x\cdot \frac{1}{3}\cdot \frac{1}{1-\frac{4}{3}x}=\frac{2x}{3}\cdot \sum^{\infty}_{n=0}{\frac{4x}{3}^n}=\\
=\sum^{\infty}_{n=0}{\frac{2\cdot4^n}{3^{n+1}}x^{n+1}}, \text{dla: }|\frac{4x}{3}|\lt 1
\end{gathered}$$


