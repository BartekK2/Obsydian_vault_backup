### Szeregi potęgowe
#### 2025-03-25
##### Poprzednia: [[Analiza 3 Szeregi funkcyjne]]
##### Następna: [[Analiza 5 Szeregi Taylora]]
##### Zadania: [[Zadania Szeregi]]

#szeregi_potegowe #analiza2  

---

**Def.** Szeregiem potęgowym o środku w punkcie $x_0$ nazywamy szereg funkcyjny postaci:

$\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$, gdzie:
$\forall n \in \mathbb{N} \ \ \ a_n\in \mathbb{R}, \ \ x\in \mathbb{R}, \ \ x_0\in \mathbb{R}$

**Spostrzeżenie**: Szereg $\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$ jest zbieżny w $x_0$

**Twierdzenie**:
zał: $\sum^{\infty}_{n=0}{a_n(x-x_0)^n}\ (*)$
teza:
1) jeśli szereg $(*)$ jest zbieżny dla pewnego $x_1$ to, jest zbieżny dla wszystkich $x_1$ takich, że:
   $|x_2-x_0|\lt |x_1-x_0|$
2) Jeśli szereg $(*)$ nie jest zbieżny dla $x_1$, to nie jest również zbieżny dla wszystkich $x_2$ takich że:
   $|x_2-x_0|\gt |x_1-x_0|$

**Def.**
$R=\sup\{|x-x_0|: \text{szereg }\sum^{\infty}_{n=0}{a_n(x-x_0)^n} \text{ jest zbieżny}\}$$R=0\implies \text{szereg } (*) \text{ jest zbieżny tylko w }x_0$
$R=+\infty \implies \text{szereg } (*) \text{ jest zbieżny }\forall x \in \mathbb{R}$
$0\lt R\lt +\infty$
Przedział $(x_0-R, x_0+R)$ nazywamy **przedziałem zbieżności**.
Zbiór $\{x\in \mathbb{C}: |x-x_0| \lt R\}$ nazywamy kołem zbieżności.

**Spostrzeżenie**:
Szereg $(*)$ jest zbieżny w $(x_0-R, x_0+R)$ i nie jest zbieżny w $(-\infty, x_0-R) \cup (x_0+R, +\infty)$.
Szereg $(*)$ w punktach $x_0-R$ i $x_0+R$ może być zbieżny lub niezbieżny.

**Twierdzenie**: Cauchy'ego-Hadamarda
zał: $\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$
$\lambda=\lim_{n\to \infty}{|\frac{a_{n+1}}{a_n}}|$   lub $\lambda=\lim_{n\to \infty}{\sqrt[n]{a_n}}$
teza:
$$\begin{gathered}
R=\left\{\begin{matrix}
+\infty, \lambda=0 \\ \frac{1}{\lambda}, 0\lt\lambda\lt +\infty\\ 0, \lambda=+\infty 
\end{matrix}\right.
\end{gathered}
$$

**Twierdzenie** o własnościach sumy szeregu potęgowego:

zał: $\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$ jest zbieżny w $(x_0-R, x_0+R)$ 
teza:
1) Suma szeregu $S(x)=\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$ jest funkcją ciągła w $(x_0-R,x_0+R)$
2) Suma szeregu $S(x)=\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$ jest różniczkowalna $\forall x \in (x_0-R, x_0+R)$ i zachodzi wzór:
   $S'(x)=\left(\sum^{\infty}_{n=0}{a_n(x-x_0)^n}\right)'=\sum^{\infty}_{n=0}{[a_n(x-x_0)^n]'}$
3) Suma szeregu $S(x)$ jest całkowalna w $(x_0-R, x_0+R)$ i zachodzi wzór:
   $\forall x_1,x_2\in (x_0-R,x_0+R)$
   $\int^{x_2}_{x_1}{S(x) \ dx}=\int^{x_2}_{x_1}{S(x) \ dx}=\int^{x_2}_{x_1}{\sum^{\infty}_{n=0}{a_n(x-x_0)^n}}\ dx=\sum^{\infty}_{n=0}{\int^{x_2}_{x_1}a_n(x-x_0)^n}\ dx$

**Przykład:** Wyznacz obszar zbieżności i sumę szeregu potęgowego $\sum^{\infty}_{n=1}{\frac{x^n}{n}}$ 

$$\begin{gathered}
S(x)=\sum^{\infty}_{n=1}{\frac{x^n}{n}}\\
S'(x)=\sum^{\infty}_{n=1}{(\frac{x^n}
{n})'}=\sum^{\infty}_{n=1}{x^{n-1}}\\
\text{Dla x}: |x|\lt 1\\
S'(x)=\frac{x}{1-x}\\\\
\int{S'(x)}=\int{-1+\frac{1}{1-x}\ dx}=-x-\ln{|1-x|}
\end{gathered}$$

---
**Twierdzenie**: Abela

zał: szereg potęgowy $\sum^{\infty}_{n=0}{a_n(x-x_0)^n}$ jest zbieżny w $(x_0-R, x_0+R)$ i w $x_1=x_0-R$ $(x_2=x_0+R)$ 
istnieje $\lim_{x\to x_1^+}{S(x)} \ \ (\lim_{x\to x_2^-}{S(x)})$

teza: $S(x_1)=\lim_{x\to x_1^+}{S(x)} \ \ (S(x_2)=\lim_{x\to x_2^-}{S(x)})$

**Przykład:** Wyznacz obszar zbiezności i sumę szeregu potęgowego $\sum^{\infty}_{n=1}{\frac{(-1)^nnx^{2n}}{4^n}}$

$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^nnx^{2n}}{4^n}}\overset{t=x^2}{=}\sum^{\infty}_{n=1}{\frac{(-1)^nn\cdot t^{n}}{4^n}}\\\\
a_n=\frac{(-1)^n\cdot n}{4^n}\\\\
\lim_{n\to \infty}{|\frac{\frac{(-1)^{n+1}\cdot (n+1)}{4^{n+1}}}{\frac{(-1)^n\cdot n}{4^n}}}|=\lim_{n\to \infty}{|\frac{-\cancel{(-1)}^n\cdot (n+1)}{\cancel{4^n}\cdot 4}\cdot \frac{\cancel{4^n}}{\cancel{(-1)^n}\cdot n}|}=\\=\lim_{n\to \infty}{\frac{(n+1)}{4n}}=\frac{1}{4}\\\\\
R=\frac{1}{\frac{1}{4}}=4, \ \ \ t\in(-4,4)\\\\
t=x^2 \implies t\in (0,4)\implies x\in (0,2)\\\\
\lim_{x\to 2^-}=+\inf/-\inf\\\
\lim_{x\to 0^+}=0, \text{zbieżny w }x=0\\\\
\text{Suma:}\\\\
\sum^{\infty}_{n=1}{\frac{(-1)^nn\cdot t^{n}}{4^n}}=t\cdot \sum^{\infty}_{n=1}{\frac{(-1)^nn\cdot t^{n-1}}{4^n}}=t\cdot S_1(n)\\\\
\int S_1(n)=\sum{(\frac{-t}{4})^n}=\frac{-t}{4}\cdot \frac{1}{1+\frac{t}{4}}=\frac{-t}{4+t}\\\\
\end{gathered}$$

---


