

$$\begin{gathered}
zał:\sum^{\infty}_{n=0}{c_n\varphi_n}\text{- szereg ortagoalny zbieżny jednostajnie do funkcji }f\in L^2\\\\\
teza: \forall n \in \mathbb{N}\ \ \ c_n=\frac{f\circ \varphi_n}{||\varphi_n||}-\text{współczynniki Eulera-Fouriera}\\\\
\end{gathered}$$

**Dowód tożsamości Persevala**

$$\begin{gathered}
f\sim  \sum^{\infty}_{n=0}{c_n\varphi_n}\text{ czyli ten szereg jest szeregiem Fouriera funkcji f względem }\varphi_n\\\\
teza:\\
\sum^{\infty}_{n=0}{c_n\varphi_n} \text{ - zbiezny przeciętnie z kwadratem do }f\Leftrightarrow||f||^2=\sum^{\infty}_{n=0}{c_n^2||\varphi_n||^2}\\\\
f\circ g=\int_{[a,b]}f(x)g(x)\ dx\\\\
\frac{f\circ \varphi_n}{||\varphi_n||^2}=\frac{\int{\sum^{\infty}_{k=1}}c_k\varphi_k(x)\cdot \varphi_n(x) \ dx}{||\varphi_n||^2}=
\frac{\sum^{\infty}_{k=1}c_k\int \varphi_k(x)\cdot \varphi_n(x) \ dx}{||\varphi_n||^2}=\dots\\
gdzie:\\
\int{q_k(x)q_n(x)\ dx}=\left\{
\begin{matrix}
0, k\neq n\\
||\varphi_n||^2, k=n
\end{matrix}
\right.\\
więc:\\\\
\dots=c_n\\\\
||f||^2=f\circ f=\int{|f(x)|^2 \ dx}=||\sum^{\infty}_{n=0}{c_n\varphi_n(x)}||^2=\sum^{\infty}_{n=0}{|c_n|^2|\varphi_n|^2}
\end{gathered}$$


(coś tego typu idk najpierw wytłumaczyła skąd sie bierze wzór na $c_n$ potem przeszła do dowodu nie czaje)

**Info od bratusze**

Żeby dało się coś zamienić na szereg trygonometryczny Fouriera musi spełniać warunki Dirichleta, jeśli nie spełnia trzeba zamienić tą funkcje na taką co spełnia i nie zmieni nam to rozwiązania. Tzn. np jeśli mamy $f(x)=x$ w przedziale $(-\pi,\pi)$ to zamieniamy to na:

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
x, x\in (-\pi, \pi ]\\
\pi , x=-\pi 
\end{matrix}
\right.
\end{gathered}$$
tak samo w przedziałach nieciągłości.

**zadania**

Zad 1.

$$\begin{gathered}
f(x)=x^2, x \in [-\pi, \pi]\\\\
\text{jest to funkcja parzysta i spełniająca warunki dirichleta}\\\\
\text{skoro parzysta to możemy uprościć wzór i korzystać z tego na parzyste}\\\\
a_0=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x) \ dx}=\frac{1}{\pi}\int^{\pi}_{-\pi}{x^2 \ dx}=\frac{1}{\pi}\frac{x^3}{3}|^{\pi}_{-\pi}=\frac{1}{\pi}(\frac{\pi^3}{3}-\frac{-\pi^3}{3})=\frac{1}{\pi}\cdot \frac{2\pi^3}{3}=\frac{2\pi^2}{3}\\=(\frac{2}{\pi}\int^{\pi}_{0}{f(x) \ dx})\\\\
a_n=\frac{2}{\pi}\int^{\pi}_{0}{f(x) \ cos{nx} \ dx}=\frac{2}{\pi}\int^{\pi}_{0}{x^2\cos{nx}}:\\\\
\int{x^2\cos{nx} \ dx}=\begin{vmatrix}
u=x^2&dv=\cos{nx}\\
du=2x&v=\frac{1}{n}\sin{nx}
\end{vmatrix}=\frac{x^2\sin{nx}}{n}-\frac{1}{n}\int{2x\sin{nx}}=\\\\
=\begin{vmatrix}
u=2x&v'=\sin{nx}\\
du=2&v=-\frac{1}{n}{\cos{nx}}
\end{vmatrix}=\frac{x^2\sin{nx}}{n}-\frac{1}{n}(\frac{-2x\cos{nx}}{n}-\int{-\frac{2}{n}\cos{nx}})=\\\\
=\frac{x^2\sin{nx}}{n}+\frac{2x\cos{nx}}{n^2}-\frac{2\sin{nx}}{n^3}\\\\
n\neq 0\\\\
a_n=\frac{2}{\pi}\frac{x^2\sin{nx}}{n}+\frac{2x\cos{nx}}{n^2}-\frac{2\sin{nx}}{n^3}|^{\pi}_0=\frac{4}{n^2}\cdot (-1)^n\\\\
f(x)=\frac{\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4}{n^2}(-1)^n\cos{nx}}
\end{gathered}$$

ciąg dalszy zadania (kolejny podpunkt)
$$\begin{gathered}
\text{na podstawie powyższego policz }S=1+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}\dots\\
\text{jeżeli przyjmiemy }x=\pi\text{ to cosinus równy }(-1)^n\\\\
f(\pi)=\pi^2=\frac{\pi^2}{3}+\sum^{\infty}_{n=1}{\frac{4}{n^2}}=\frac{\pi^2}{3}+4\sum^{\infty}_{n=1}{\frac{1}{n^2}}\\\\
S=\sum^{\infty}_{n=1}{\frac{1}{n^2}}=\frac{\pi^2-\frac{\pi^2}{3}}{4}=\frac{\pi^2}{6}
\end{gathered}$$

Zad 2. Rozwiń w szereg sinusów $f(x)=\frac{\pi}{4}, \ x\in (0,\pi)$

Nie spełnia warunków dirichleta więc zamieniamy: (rozszerzając jednocześnie na przedział $[-\pi, \pi]$)

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
0, x\in \{-\pi,0,\pi\}\\
-\frac{\pi}{4}, x\in (-\pi,0)\\
\frac{\pi}{4}, x \in (0,\pi)
\end{matrix}
\right.\\\\
\text{i tak samo }b_0, b_n \ itd \ (nie \ dokonczylismy)
\end{gathered}$$


**Dała do zrobienia zadania na następną**
Rozwiń w fouriera trygo:
$$\begin{gathered}
1.f(x)=|x|, x\in [-\pi, \pi]\\
2.f(x)=\frac{\pi-x}{2}, x\in [0,2\pi]\\
3.f(x)=10-x, x\in [5,15]
\end{gathered}$$
