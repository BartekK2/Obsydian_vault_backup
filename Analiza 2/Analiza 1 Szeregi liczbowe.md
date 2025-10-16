### Szeregi liczbowe
#### 2025-03-25
##### Następna: [[Analiza 2 Ciągi funkcyjne]]
##### Zadania: [[]]

#szeregi #analiza2  

---
### Definicja, wstęp:

Jeżeli mamy dany ciąg $(a_n)_{n\in \mathbb{N}}$, i obliczymy lub wyrazimy jego $n$-tą sumę częściową to szeregiem nazwiemy parę:
$$\begin{gathered}
((a_n)_{n\in \mathbb{N}}, (S_n)_{n\in \mathbb{N}})\\
Ozn: \sum^{\infty}_{n=1}{a_n}
\end{gathered}$$

**Przykład**:
$$\begin{gathered}
\frac{1}{1\cdot 2}+\frac{1}{2\cdot 3}+\frac{1}{3\cdot 4}+\dots = \sum^{\infty}_{n=1}{\frac{1}{n(n+1)}}\\
a_n=\frac{1}{n(n+1)}\\
S_1=a_1=\frac{1}{2}\\
S_2=a_1+a_2=\frac{1}{2}+\frac{1}{6}=\frac{4}{6}=\frac{2}{3}\\
\dots\\
S_n=\frac{n}{n+1}\ \ \text{Dowód indukcyjny}\\
\sum^{\infty}_{n=1}{\frac{1}{n(n+1)}}\leftrightarrow \left(\left(\frac{1}{n(n+1)}\right)_{n\in \mathbb{N}}, \left(\frac{n}{n+1}\right)_{n\in \mathbb{N}}\right)
\end{gathered}$$

### Zbieżność szeregu:

**Def. zbieżności szeregu**:

Szereg $\sum^{\infty}_{n=1}{a_n}$ nazywamy zbieżnym $\Leftrightarrow$ istnieje takie $S(\in \mathbb{R}, \mathbb{C})$, że $\lim_{n\to \infty}{S_n=S}$

**Spostrzeżenie:**

zał $k\in \mathbb{N}$ 
teza: $\sum^{\infty}_{n=1}{a_n}\text{ zbieżny }\Leftrightarrow \sum^{\infty}_{n=k}{a_n}\text{ zbieżny}$

**Twierdzenie o WK zbieżności szeregu**:

zał: $\sum^{\infty}_{n=1}{a_n}$ jest zbieżny
teza: $\lim_{n\to \infty}{a_n}=0$

**Twierdzenie o zbieżności szeregów harmonicznych**:

zał $\sum^{\infty}_{n=1}{\frac{1}{n^{\alpha}}}, \ \alpha \in \mathbb{R}$ (szereg harmoniczny rzędu $\alpha$)
teza:
$a\gt 1\implies \sum^{\infty}_{n=1}{\frac{1}{n^{\alpha}}}$ jest zbieżny
$a\leq 1\implies \sum^{\infty}_{n=1}{\frac{1}{n^{\alpha}}}$ nie jest zbieżny

Zatem szereg harmoniczny rzedu $\alpha=1$ nie jest zbieżny.

**Szereg bezwzględnie zbieżny**:

Szereg $\sum^{\infty}_{n=1}{a_n}$ nazywamy **bezwzględnie zbieżnym** $\Leftrightarrow$ gdy $\sum^{\infty}_{n=1}{|a_n|}$ jest zbieżny.

Jeśli $\sum^{\infty}_{n=1}{a_n}$ jest zbieżny, ale nie jest bezwzględnie zbieżny, to mówimy że jest **warunkowo zbieżny**.

**Twierdzenie o zbieżności szeregu bezwzględnie zbieżnego**:

zał: $\sum^{\infty}_{n=1}{a_n}$ jest bezwzględnie zbiezny
teza: $\sum^{\infty}_{n=1}{a_n}$ jest zbieżny

(to oczywiste bo przecież $\sum^{\infty}_{n=1}{|a_n|}\geq \sum^{\infty}_{n=1}{a_n})$ 

**Przykład**:
$$\begin{gathered}
\sum^{\infty}_{n=1}{\frac{(-1)^n}{n^2}}\\
\sum^{\infty}_{n=1}{\left|\frac{(-1)^n}{n^2}\right|}=\sum^{\infty}_{n=1}{\frac{1}{n^2}}\\
\text{Gdzie }\sum^{\infty}_{n=1}{\frac{1}{n^2}}\text{ zbieżny na podstawie tw o zbieżności szeregów harmonicznych}\\\\
\text{A na podstawie twierdzenia o zbieżności szeregu bezwzglednie zbieżnego:}\\
\sum^{\infty}_{n=1}{\frac{(-1)^n}{n^2}}\text{ również zbieżny.}
\end{gathered}$$

**Twierdzenie o kryterium d' Alamberta**:
zał: $\sum^{\infty}_{n=1}{a_n}$
$\forall n \in \mathbb{N} \ a_n \neq 0$
$g=\lim_{n \to \infty}{|\frac{a_{n+1}}{a_n}|}$
teza:
$g\lt 1 \implies \sum^{\infty}_{n=1}{a_n}$ zbieżny
$g\gt 1 \implies \sum^{\infty}_{n=1}{a_n}$ nie jest zbieżny

**UWAGA**: kryterium d'Alamberta nic nie mówi dla przypadku gdzie $g=1$

**Twierdzenie o kryterium Cauchy'ego**:
zał: $\sum^{\infty}_{n=1}{a_n}$
$\forall n \in \mathbb{N} \ a_n \neq 0$
$g=\lim_{n \to \infty}{\sqrt[n]{|a_n|}}$
teza:
$g\lt 1 \implies \sum^{\infty}_{n=1}{a_n}$ zbieżny
$g\gt 1 \implies \sum^{\infty}_{n=1}{a_n}$ nie jest zbieżny

**Przykład**:
$\sum^{\infty}_{n=1}{\frac{1}{n}}$, tutaj Alambert ani Cauchy nie pomogą bo $g=1$ 

$\sum^{\infty}_{n=1}{\frac{3^n\cdot n!}{n^n}}$
$a_n=\frac{3^n\cdot n!}{n^n}$
$\lim_{n\to \infty}{\left|\frac{a_{n+1}}{a_n}\right|}=\lim_{n\to \infty}{\frac{3\cdot 3^n\cdot (n+1)\cdot n!}{(n+1)^{n+1}}\cdot \frac{n^n}{3^n\cdot n!}}=\frac{3n^n}{(n+1)^n}=\frac{3}{e}\gt 1 \implies \text{nie zbieżny}$

**Twierdzenie o kryterium porównawczym granic ilorazowych**:
zał $\sum^{\infty}_{n=1}{a_n}, \sum^{\infty}_{n=1}{b_n}$
$\forall n \geq n_0 \ \ a_n\geq 0, \ \ b_n\gt 0$
$\lim_{n\to \infty}{\frac{a_n}{b_n}}=g \in (0,+\infty)$

teza: $\sum^{\infty}_{n=1}{a_n}$ jest zbieżny $\Leftrightarrow \ \sum^{\infty}_{n=1}{b_n}$ jest zbieżny.

:LiHome: **Dokończ przykłady**
$\sum^{\infty}_{n=1}{\frac{n^2-2n+3}{n^4+2n^3-2}}$

$\sum^{\infty}_{n=1}{\frac{2+(-1)^n}{n}}$

**Twierdzenie o kryterium porównawczym**:
zał: $\sum^{\infty}_{n=1}{a_n}, \sum^{\infty}_{n=1}{b_n}$
$\forall n \geq n_0 \ \ a_n\geq 0, \ \ b_n\geq 0$
$\forall n \geq n_1 \ \ a_n\leq b_n$
teza:
1) kryterium na zbieżność
   Jeśli $\sum{b_n}$ jest zbieżny $\implies \sum{a_n}$ jest zbieżny
2) kryterium na rozbieżność:
   Jeśli $\sum{a_n}$ jest rozbieżny $\implies \sum{b_n}$ jest rozbieżny

(to oczywiste, jeżeli ciąg który od pewnego momentu jest zawsze większy od naszego sprawdzanego ciągu jes zbieżny to i nasz ciąg musi być zbieżny, a jeżeli mniejszy od sprawdzanego rozbieżny to i nasz musi być rozbieżny)

**Przykład:**
$\sum^{\infty}_{n=1}{\frac{2+(-1)^n}{n}}=\sum^{\infty}_{n=1}{b_n}$
$a_n=\frac{1}{n}$
$a_{n} \leq b_n, \forall n \in \mathbb{N}$
$\sum{\frac{1}{n}}$ rozbieżny $\implies \sum{\frac{2+(-1)^n}{n}}$ również rozbieżny

**Twierdzenie o kryterium całkowym**:
zał: $\sum{a_n}$
$\forall n \geq n_0 \ \ a_n\geq 0$
$f: [n_0, +\infty] \to \mathbb{R}_+$
$\forall n \geq n_0 \ \ a_n=f(n)$
$f$ jest nierosnąca na przedziale $[n_0,+\infty]$

teza: $\sum{a_n}$ jest zbieżny $\Leftrightarrow \int^{+\infty}_{n_0}{f(x) \ dx}$ jest zbieżna

**Przykłady**:
$\sum{\frac{1}{n}}$
$n_0=1, \frac{1}{n}\geq 0 \land f\downarrow$ 
$f(x)=\frac{1}{x}$
$\int^{\infty}_{1}{\frac{1}{x}\ dx}=\ln{x}|^{\infty}_{1}=\infty$

Zatem całka rozbieżna co implikuje że i szereg jest rozbieżny ( w tym twierdzeniu jest równoważność nie implikacja ).

$\sum{\frac{1}{n\cdot \ln{n}}}$
$\frac{1}{n\cdot \ln{n}}\geq 0 \land \downarrow$
$\int{\frac{1}{x\cdot \ln{x}}}=\begin{vmatrix}t=\ln{x}\\ dt=\frac{1}{x}\ dx\end{vmatrix}=\int{\frac{1}{t}\ dt}=\ln{t}=\ln{\ln{x}}$
znów rozbieżna

**Def. Szeregu naprzemiennego**:

Szeregiem naprzemiennym nazywamy szereg postaci:
$\sum{(-1)^na_n}$ gdzie:
1) $\forall n\geq 1  \ \ a_n\gt 0$
2) $\lim_{n\to \infty}{a_n}=0$
3) $(a_n)^\infty_{n=1}$ jest malejący

**Twierdzenie o kryterium Leibniza**:

Szereg naprzemienny jest zbieżny.
Ponadto:
$\forall n \in \mathbb{M} \ \ |S_n-S| \lt {a_{n+1}}$

**Przykład**:
$\sum{\frac{(-1)^n}{n}}$
$a_n=\frac{1}{n}$
$a_n$ zbieżny i malejący od $n=1$ do nieskończoności
zatem jest to szereg zbieżny bo jest to szereg naprzemienny (na podstawie kryterium Leibniza)

---



