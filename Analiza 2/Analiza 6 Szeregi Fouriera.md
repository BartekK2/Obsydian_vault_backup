### Szeregi Fouriera
#### 2025-04-08
##### Poprzednia: [[Analiza 5 Szeregi Taylora]]
##### Następna: [[Analiza 7 Rachunek różniczkowy funkcji wielu zmiennych]]
##### Zadania: [[Zadania Szeregi]]

#szeregi_fouriera #analiza2  

---
### Szeregi trygonometryczne Fouriera 

**Uwaga:** Funkcje rózniące sie pojedynczymi punktami (dowolna, skończona ilość) będziemy utożsamiać.

Jeżeli funkcja jest całkowalna z kwadratem i spełnia **warunki Dirichleta** tzn:

1. $f: [a,b]\to \mathbb{R}, f -$ ograniczona
2. $f$ jest przedziałami monotoniczna w $[a,b]$ 
3. $f$ jest ciągła w $[a,b]$ poza skończoną ilością punktów nieciągłości $x_0$ w których zachodzi 
   $f(x_0)=\frac{\lim_{x\to x_0^-}f(x)+\lim_{x\to x_0^+}}{2}$
4. $f(a)=f(b))\frac{\lim_{x\to b^-}f(x)+\lim_{x\to a^+}}{2}$

to da sie ją rozwinąć w szereg Fouriera i jest do tego szeregu zbieżna punktowo na $[a,b]$.

### Przypadek ogólny $[-\pi,\pi]$

**W szczególnym przypadku kiedy $[a,b]=[-\pi,\pi]$ zachodzi:**

$$\begin{gathered}
a_0=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x) \ dx}\\\\
a_n=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x) \cos{nx}\ dx}\\\\
b_n=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x) \sin{nx}\ dx}\\\\
f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}{a_n \cos{nx} + b_n \sin{nx}}
\end{gathered}$$
##### Rozwiń w szereg Fouriera funkcję $$f(x)=\left\{\begin{matrix}0, -\pi\lt x\lt 0\\x, 0\leq x\lt \pi \end{matrix}\right.$$

**Sprawdźmy najpierw warunki Dirichleta:**

1) $f: [a,b] \to \mathbb{R}, f - ograniczona$ :LiCheck: 
2) monotoniczna przedzialami :LiCheck:
3) ciągła poza skończoną liczbą punktów w których wartość jest równa średniej arytmetycznej granic jednostronnych :LiCheck: 
4) $f(a)=f(b)=\frac{\lim_{x\to a^+}f(x)+\lim_{x\to b^-}f(x)}{2}$ :LiCross: 


$$\begin{gathered}
\text{Najpierw warunki dirichleta}:
f(-\pi)=f(\pi)=\frac{\pi}{2}\\\\
a_0=\frac{1}{\pi}\int^{\pi}_{-\pi}{f(x) \ dx}\\
a_0=\frac{1}{\pi}\left(\int^{\pi}_{0}{x\ dx}+\int^{0}_{-\pi}{0 \ dx}\right)=\frac{\pi^2}{2\pi}=\frac{\pi}{2}\\\\

a_n=\frac{1}{\pi}\left(\int^{\pi}_{0}{x\cos{nx}\ dx}\right)=\begin{vmatrix}
u=x&v'=\cos{nx}\\
u'=1&v=\frac{\sin{nx}}{n}
\end{vmatrix}=\\
=\frac{1}{\pi}\left(\frac{x \sin{nx}}{n}-\int{\frac{\sin{nx}}{n}}\right)|^{\pi}_0=\frac{1}{\pi}\left(\frac{x \sin{nx}}{n}+\frac{ \cos{nx}}{n^2}\right)|^{\pi}_0=\\
=\frac{1}{\pi}\left(\frac{(-1)^n-1}{n^2}\right)\\\\
b_n=\frac{1}{\pi}\left(\int^{\pi}_{0}{x\sin{nx}\ dx}\right)=\begin{vmatrix}
u=x&v'=\sin{nx}\\
u'=1&v=\frac{-\cos{nx}}{n}
\end{vmatrix}=\frac{1}{\pi}\left(\frac{-x \cos{nx}}{n}+\frac{\sin{nx}}{n^2}\right)|^{\pi}_0=\\
=\frac{1}{\pi}\left(\frac{-\pi (-1)^n}{n}\right)=\frac{(-1)^{n+1}}{n}\\\\

f(x)=\frac{\pi}{4}+\sum^{\infty}_{n=1}{\cos{nx}\cdot \frac{1}{\pi}\left(\frac{(-1)^n-1}{n^2}\right)+\sin{nx}\cdot \frac{(-1)^{n+1}}{n}}\\\\

\end{gathered}$$
**Narysuj wykres sumy otrzymanego szeregu dla wszystkich $x\in \mathbb{R}$ oraz korzystając z otrzymanego rozwinięcia oblicz sumę szeregu liczbowego $1+\frac{1}{3^2}+\frac{1}{5^2}+\dots$**

$$\begin{gathered}
1+\frac{1}{3^2}+\frac{1}{5^2}+\dots=-\frac{1}{2}\sum^{\infty}_{n=1}{\frac{(-1)^n-1}{n^2}}=(f(0)-\frac{\pi}{4})\cdot \pi\cdot -\frac{1}{2}=\frac{\pi^2}{8}
\end{gathered}$$

**Jak rysować wykres?** 

Tak samo jak przy rysowaniu zwykłego wykresu $f(x)$ ale **najpierw należy uwzględnić warunki Dirichleta jeżeli coś zmieniliśmy** (tak jak powyżej zmieniliśmy wartości na krańcach przedziału). A następnie **zapętlić** funkcje czyli sprawić żeby była okresowa co przedział czyli w tym przypadku rozważając przedział $[-\pi,\pi]$ rysujemy tak samo dla $[\pi,2\pi]$ co rysowaliśmy dla $[-\pi,\pi]$ itd.

Dla powyższego przykładu tj. $$f(x)=\left\{\begin{matrix}0, -\pi\lt x\lt 0\\x, 0\leq x\lt \pi \end{matrix}\right.$$
1. uwzględnienie zmian jeśli jest taka potrzeba żeby spełnić warunki Dirichleta
   $f(0)=f(\pi)=\frac{\pi}{2}$
2. rysujemy
3. zapętlamy

![[diagram-20250707.png]]

---

### Przypadek kiedy funkcja nieparzysta $[-\pi,\pi]$ (szereg sinusów)

$$\begin{gathered}
a_0- \text{znika (przecież nieparzysta)}\\\\
b_n=\frac{2}{\pi}\int^{\pi}_{0}{f(x) \sin{nx}}\\
\text{ (sinus zamienia na funkcje parzystą więc można przemnożyć razy 2 i robić }[0,\pi])\\\\
f(x)=\sum^{\infty}_{n=1}{b_n \sin{nx}}, x\in [-\pi,\pi]
\end{gathered}$$

**Co jeżeli każą nam przedstawić za pomocą szeregu sinusów funkcję która nie jest nieparzysta?**

- zamieniamy ją na taką żeby nieparzysta była tj:
  $f(x)=x^2\implies f(x)=x^2, x\in [0,\pi] \land f(x)=-x^2, x\in [-\pi,0]$

**Analogicznie poniżej**

---

### Przypadek kiedy funkcja parzysta $[-\pi,\pi]$ (szereg cosinusów)

$$\begin{gathered}
a_0=\frac{2}{\pi}\int^{\pi}_{0}f(x)\\\\
a_n=\frac{2}{\pi}\int^{\pi}_{0}{f(x) \cos{nx}}\\
f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}{f(x) \cos{nx}}, x\in [-\pi,\pi]
\end{gathered}$$

---

### Przypadek na dowolnym przedziale:

$$\begin{gathered}
przedział: [a,b]\\\\
x_0=l=\frac{a+b}{2}\ \  \text{środek przedziału}, \text{połowa długości przedziału}\\\\
f(x)=\frac{a_0}{2}+\sum^{\infty}_{n=1}{a_n \cos{\frac{n \pi x}{l}}+b_n \sin{\frac{n \pi x}{l}}}\\\\
\text{Skąd się pojawiło }\frac{\pi}{l}\ \  \text{w sin/cos?}\\
\text{- funkcja musi być okresowa co przedział }\\
\cos{\frac{n \pi x}{l}}=\cos{\frac{n \pi (x+2l)}{l}}\\\\
a_0=\frac{1}{l}\int^{b}_{a}f(x)\\
a_n=\frac{1}{l}\int^{b}_{a}f(x) \cos{\frac{nx \pi }{l}}\\
b_n=\frac{1}{l}\int^{b}_{a}f(x)\sin{\frac{nx \pi }{l}}\\
\end{gathered}$$

**Oczywiście można zauważyć że te wszystkie wzory to jest jedno i to samo po prostu w niektórych coś sie może redukować ze względu na właściwość (np. parzystość) funkcji, lub jej przedział będący wielokrotnością $\pi$ itd.**

---
