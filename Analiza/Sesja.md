
###### 2. Udowodnij, że dla każdego $x\gt 0$ zachodzi nierówność $e^{\sqrt{x}}\gt 1+\sqrt{x}$

$$\begin{gathered}
e^{\sqrt{x}}-1-\sqrt{x}\gt 0\\
\text{Dla }x=0 \text{ obie strony nierówności są sobie równe:}\\
e^{\sqrt{0}}-1-\sqrt{0}=0\\\\
f(x)=e^{\sqrt{x}}-1-\sqrt{x}\\
f'(x)=e^{\sqrt{x}}\cdot \frac{1}{2\sqrt{x}}-\frac{1}{2\sqrt{x}}=\frac{e^{\sqrt{x}}-1}{2\sqrt{x}}\\\\
\frac{e^{\sqrt{x}}-1}{2\sqrt{x}}\gt 0\\
e^{\sqrt{x}}\gt 1\\
x\in \mathbb{R}_+\\\\
\text{Pochodna zawsze większa od 0, dla }x\gt 0 \text{ oraz obie strony nierówności są sobie równe}\\
\text{dla }x=0 \text{ co implikuje że nierówność jest prawdziwa.}
\end{gathered}$$

---
###### 3. Sprawdź zbieżność całki $\int^{1}_{0}{\frac{1}{e^{\sqrt{x}}-1}}$.
$$\begin{gathered}
\int{\frac{1}{e^{x}-1}}=\begin{vmatrix}
t=e^x\\
dt = e^x \ dx\\
dx=\frac{1}{t}\ dt
\end{vmatrix}=\int{\frac{1}{t^2-t}\ dt}=\int{\frac{1}{t-1}\ dt}-\int{\frac{1}{t}\ dt}=\ln{|e^x-1|}-x\\\\
\int^{1}_{0}{\frac{1}{e^x-1}\ dx}=\ln{|e-1|}-1-(\lim_{x\to 0}{\ln{|e^x-1|-x}})=\inf\\\\
\text{Gdzie}: \ \frac{1}{e^x-1}\lt \frac{1}{e^{\sqrt{x}}-1} \ \forall x\in \mathbb{D}\\\\
\text{Zatem rozbieżna}
\end{gathered}$$

---

###### 1.b) Dany jest ciąg rekurencyjny $a_1=1,  \ a_{n+1}=a_n+\frac{1}{n(n+1)}$. Wyznacz wzór jawny na $a_n$ i udowodnij metodą indukcji matematycznej jego poprawność:
$$\begin{gathered}
1,\frac{3}{2},\frac{10}{6},\frac{21}{12},\frac{18}{10}\\\\
1,0.5,0.33,0.25,0.2\\\\
\text{Zakładam że }a_n=2-\frac{1}{n}\\\\
1)a_1=2-\frac{1}{1}=1, \checkmark\\
2)\text{Zakładam że }a_n=2-\frac{1}{n}\\
3)a_{n+1}=2-\frac{1}{n+1}=\frac{2n+1}{n+1}=\frac{n(2n+1)}{n(n+1)}=\frac{(2n-1)(n+1)}{n(n+1)}+\frac{1}{n(n+1)}, \ \checkmark
\end{gathered}$$

---

###### 3. Oblicz całke $\int{\frac{dx}{(1-e^x)^4}}$

$$\begin{gathered}
\int{\frac{dx}{(1-e^x)^4}}=\begin{vmatrix}
t=1-e^x\\
dt=-e^x\ dx
\end{vmatrix}=
\int{\frac{1}{t^4}\cdot \frac{1}{t-1}}=\\\\\\
\frac{1}{t^4(t-1)}=\frac{A}{t}+\frac{B}{t^2}+\frac{C}{t^3}+\frac{D}{t^4}+\frac{Ex+F}{t-1}\\\\\
1=A(t^4-t^3)+B(t^3-t^2)+C(t^2-t)+D(t-1)+(Et+F)t^4\\
1=At^4-At^3+Bt^3-Bt^2+Ct^2-Ct+Dt-D+Et^5+Ft^4\\
1=t^5(E)+t^4(A+F)+t^3(B-A)+t^2(-B+C)+t(D-C)-D\\\\
\left\{
\begin{matrix}
D=-1\\
E=0\\
F=1\\
A=-1\\
B=-1\\
C=-1
\end{matrix}
\right.
\end{gathered}$$
---
###### Wyznacz max i min $f(x)=x^{\frac{1}{x}}$

$$\begin{gathered}
f(x)=x^{\frac{1}{x}}=\sqrt[x]{x}\\
\lim_{x\to \inf}=1\\

f'(x)=(e^{\frac{\ln{x}}{x}})'=e^{\frac{ln{x}}{x}}\cdot \frac{1-\ln{x}}{x^2}\\\\
f'(x)=0\\
e^{\frac{ln{x}}{x}}\cdot \frac{1-\ln{x}}{x^2}=0\\
e^{\frac{ln{x}}{x}}\cdot (1-\ln{x})=0\\
1=\ln{x}\\
x=e\\
f'(x)\gt 0\\
\ln{x}\lt 1\\
x\lt e\\
f'(x)\gt 0\\
x\gt e
\end{gathered}$$

---
###### 2b) Sprawdź zbieżność całki $\int^{1}_{0}{\frac{1}{e^{\sqrt{x}}-1}\ dx}$

$$\begin{gathered}
\int{\frac{1}{e^{\sqrt{x}}-1}\ dx}\\\\
f(x)=f(0)+\frac{f'(0)}{1!}x+...+\frac{f^{n-1}(0)}{(n-1)!}x^{n-1}+R_n(x)\\\\\
e^y=1+y+\frac{y^2}{2}\dots \\
e^{\sqrt{x}}=1+\sqrt{x}+\frac{x}{2}+R_3(x)\\
e^{\sqrt{x}}-1\gt \sqrt{x}\\\\
\int{\frac{1}{\sqrt{x}}}\gt \int{\frac{1}{e^{\sqrt{x}}-1}}\\\\
\int{\frac{1}{\sqrt{x}}\ dx}= 2\sqrt{x}\\
\int^{1}_{0}{\frac{1}{\sqrt{x}}\ dx}= 2\sqrt{1}-2\sqrt{0}=2\\\\
\text{Zatem zbiezna bo wieksza funkcja zbiezna}
\end{gathered}$$

---
###### 3) Oblicz całke $\int{\tan{x}\sqrt{1+\frac{1}{\cos^4{x}}}\ dx}$

$$\begin{gathered}
\int{\tan{x}\sqrt{1+\frac{1}{\cos^4{x}}}\ dx}=\begin{vmatrix}
t=\tan{\frac{x}{2}}\\
x=2\arctan{t}\\
dx=\frac{2}{x^2+1}\ dt\\
\cos{x}=\frac{\cos^2-\sin^2}{\cos^2+\sin^2}=\frac{1-t^2}{1+t^2}\\
\sin{x}=\frac{2sincos}{sin^2+cos^2}=\frac{2t}{t^2+1}
\end{vmatrix}:\\\\\
tan(2x)=\frac{\sin{2x}}{\cos{2x}}=\frac{2\sin{x}\cos{x}}{\cos^2{x}-\sin^2{x}}\\\\\\
=\int{\frac{2sincos}{cos^2-sin^2}\sqrt{\frac{\cos^4+1}{\cos^4}}\ dx}=\\\\
=2\int{\frac{2t}{1-t^2}}\cdot \sqrt{(\frac{1-t^2}{1+t^2}+1)^4\cdot (\frac{1+t^2}{1-t^2})^4}=\\\\
=2\int{\frac{2t}{1-t^2}}\cdot \sqrt{(\frac{2}{1+t^2})^4\cdot (\frac{1+t^2}{1-t^2})^4}=\\\\
=2\int{\frac{2t}{1-t^2}\cdot \sqrt{(\frac{2}{1-t^2})^4}}=2\int{\frac{2t}{1-t^2}\cdot \frac{4}{(1-t^2)^2}}=16\int{\frac{t}{(1-t^2)^3}}=\\\\
\end{gathered}$$
$$\begin{gathered}
16\int{\frac{t}{(1-t^2)^3} \ dt}=-8\int{\frac{-2t}{(1-t^2)^3}\ dt}=\begin{vmatrix}
u=1-t^2\\
du=-2t
\end{vmatrix}=-8\int{\frac{du}{u^3}}=-8\int{u^{-3}}=\\=-8\cdot \frac{u^{-2}}{-2}
=\frac{4}{u^2}=\frac{4}{(1-t^2)^2}=\frac{4}{(1-\tan{(\frac{x}{2})^2})^2}
\end{gathered}$$

---
$$\begin{gathered}
\int{\tan^2{x}\ dx}=\begin{vmatrix}
t=\tan{x}\\
dt=\frac{1}{\cos^2{x}}\\
dt=\frac{sin^2+cos^2}{\cos^2{x}}\ dx \\
\frac{\cos^2{x}}{sin^2+cos^2}dt=\ dx \\
\frac{1}{t^2+1}dt=\ dx \\
\end{vmatrix}=\int{\frac{t^2}{t^2+1}\ dt}=\int{1-\frac{1}{t^2+1}\ dt}=\\\\\
=t-\arctan{t}=\tan{x}-x
\end{gathered}$$---
###### 3) Narysuj krzywą zadaną we współrzędnych biegunowych wzorem: $r(\phi)=a(1+\cos{\phi})$ oraz oblicz pole obszaru ograniczonego tą krzywą

$$
\begin{gathered}
\frac{1}{2}\int^{2\pi}_{0}{r^2(\phi) \ d\phi }=\frac{1}{2}\int^{2\pi}_{0}{a^2(1+2\cos{\phi}+\cos^2{\phi})}=
\\=\frac{1}{2}a^2(2\pi +\int^{2\pi}_{0}{\cos^2{\phi}})=a^2\frac{3\pi}{2}
\end{gathered}
$$

---
###### 5) Pokaż, że ciąg o wyrazie $b_n=(1+\frac{1}{1^2})\cdot (1+\frac{1}{2^2})\cdot (1+\frac{1}{3^2})\dots (1+\frac{1}{n^2})$ jest zbieżny.

$$
\begin{gathered}
b_n=(1+\frac{1}{1^2})\cdot (1+\frac{1}{2^2})\cdot (1+\frac{1}{3^2})\dots (1+\frac{1}{n^2})\\\\
b_n\uparrow\\\\
b_n=e^{\ln{(1+\frac{1}{1^2})\cdot (1+\frac{1}{2^2})\cdot (1+\frac{1}{3^2})\dots (1+\frac{1}{n^2})
}}=e^{\ln{(1+\frac{1}{1})}+\ln{(1+\frac{1}{4}})+\dots}\leq\\
\leq e^{2-1}\cdot e^{1-\frac{1}{4}}\cdot e^{\frac{1}{4}-\frac{1}{8}}\dots e^{\frac{1}{(n-1)^2}-\frac{1}{n^2}}=e^{2-\frac{1}{n^2}} \approx e^2\\\\
e^{\ln{(1+\frac{1}{x^2})}}\lt e^{\frac{1}{x^2}}
\end{gathered}
$$

###### Oszacuj dokładność wzoru przybliżonego:

$$\begin{gathered}
\sqrt[3]{1+x}\approxeq 1+\frac{x}{3}\\%
(\sqrt[3]{1+x})'=\frac{1}{3}(1+x)^{-\frac{2}{3}}=\frac{1}{3}\frac{1}{\sqrt[3]{(1+x)^2}}\\\\
\sqrt[3]{1+x}\approxeq f(0)+\frac{f'(0)}{1!}x+R_2{(x)\\
}\\\\
R_2(x)=-\frac{2}{9}x^2\cdot \frac{1}{2!}\\\\
\end{gathered}$$

---
###### 2) Udowodnij że dla każdego $x\gt 0$ zachodzi nierówność $e^{\sqrt{x}}\gt 1+\sqrt{x}$

$$\begin{gathered}
e^{\sqrt{x}}:\\
y=\sqrt{x}\\
e^{y}\approxeq 1+y+y^2+\dots\\
\text{Po ponownym podstawieniu}\\
e^{\sqrt{x}}\approxeq 1+\sqrt{x}+x+\dots, \text{gdzie }x\gt 0\implies e^{\sqrt{x}}\gt 1+\sqrt{x}
\end{gathered}$$

---
###### 3) Sprawdź zbieżność całki $\int^{1}_{0}{\frac{1}{e^{\sqrt{x}}-1}}$

$$\begin{gathered}
\text{Bazując na dowodzie z powyższego zadania że:}\\
e^{\sqrt{x}}\gt 1+\sqrt{x}:\\\\
f(x)=\frac{1}{e^{\sqrt{x}}-1}\lt g(x)=\frac{1}{\sqrt{x}}\\\\
\int^{1}_{0}{g(x)\ dx}=\int^{1}_{0}{\frac{1}{1+\sqrt{x}-1}\ dx}=
\int^{1}_{0}{x^{-\frac{1}{2}}\ dx}=2\sqrt{1}-2\sqrt{0}=2\\\\
\text{Całka funkcji większej od tej której zbieżność mieliśmy zbadać}\\
\text{Jest zbieżna co implikuje że nasza badana całka jest zbieżna.}
\end{gathered}$$

---
###### 3) Oblicz pole powierzchni (bocznej) bryły powstałej poprzez obrót dookoła osi $OX$ krzywej $y=\tan{x}, x\in [0,\frac{\pi}{4}]$

$$\begin{gathered}
\tan{x}\gt 0 \Leftrightarrow x\in [0,\frac{\pi}{2})\implies \forall x\in [0,\frac{\pi}{4}]y=f(x)\gt 0\\\\
f'(x)=\frac{1}{\cos^2{x}}=\frac{\sin^2{x}+\cos^2{x}}{\cos^2{x}}=1+\tan^2{x}\\
\\
|S|=2\pi \int^{\frac{\pi}{4}}_{0}{f(x)\cdot \sqrt{1+(f'(x))^2}\ dx}=\\\\
=2\pi \int^{\frac{\pi}{4}}_{0}{\tan{x}\cdot \sqrt{1+(1+2\tan^2+\tan^4{x})}\ dx}=\\=
\begin{vmatrix}
t=\tan{x}\\
dt=\frac{1}{cos^2{x}}=1+tan^2{x}\ dx=1+t^2
\end{vmatrix}=2\pi \int^{1}_{0}{\frac{t}{1+t^2}\sqrt{1+(1+2t^2+t^4)}\ dt}=\\\\=
\pi \int^{1}_{0}{\frac{2t}{1+t^2}\sqrt{1+(1+t^2)^2}\ dt}=\begin{vmatrix}
x=(1+t^2)\\
dx=2t\ dt
\end{vmatrix}=\\\\
=\pi \int^{2}_{1}{\frac{\sqrt{1+x^2}}{x} \ dx}
=\begin{vmatrix}
u=\sqrt{1+x^2}\\
du=\frac{x}{\sqrt{1+x^2}}\ dx\\
dx=\frac{\sqrt{1+x^2}}{x}\ du=\frac{u}{x}\ du
\end{vmatrix}=\pi \int^{\sqrt{5}}_{\sqrt{2}}{1 \ du}=\pi( \sqrt{5}-\sqrt{2})
\end{gathered}$$
---
###### 2) Wykonaj uprosczone (tzn. bez analizy drugiej pochodnej badanie przebiegu zmienności zmienności funkcji $f(x)=x^{\frac{1}{x}}$)

$$\begin{gathered}
D:(0,+\infty)\\
\text{Punkt przecięcia z osią OX}:\\
x^{\frac{1}{x}}=\sqrt[x]{x}=0 \Leftrightarrow x=0 \notin D\\
f(x)=x^{\frac{1}{x}}\neq f(-x)=(-x)^{x}\\
f(x)=x^{\frac{1}{x}}\neq -(-x)^{\frac{1}{-x}}\\\\
\lim_{x\to 0}{x^\frac{1}{x}}=\lim_{x\to 0}{e^{\ln{x}\cdot \frac{1}{x}}}=\\
=e^{\lim_{x \to 0}{\frac{\ln{x}}{x}}}=e^{\lim_{x \to 0}{\frac{\ln{x}}{x}}}=0\\\\
\lim_{x\to \infty}{\sqrt[x]{x}}=0\text{\ bo:}\\
\lim_{x\to \infty}{x^\frac{1}{x}}=\lim_{x\to \infty}{e^{\ln{x}\cdot \frac{1}{x}}}=\\
=e^{\lim_{x \to \infty}{\frac{\ln{x}}{x}}}=e^{\lim_{x \to \infty}{\frac{1}{x}}}=e^0=1\\\\
x=1\\\\\
f'(x)=(e^{\ln{x}\frac{1}{x}})'=e^{\ln{x}\frac{1}{x}}\cdot 
(\frac{1}{x}\cdot \frac{1}{x}+\ln{x}\cdot -\frac{1}{x^2})=\\
e^{\frac{\ln{x}}{x}}\cdot \frac{1-\ln{x}}{x^2}\\\\
f'(x)=0 \Leftrightarrow e^{\frac{\ln{x}}{x}}\cdot \frac{1-\ln{x}}{x^2}=0\\
1=\ln{x}\implies x=e\\
f'(x)\gt 0 \implies x\gt e\\
f'(x)\lt 0\implies x\lt e\\\\
f(e)=e^{\frac{1}{e}}\implies Ekstremum
\end{gathered}$$---
### 3) Zbadaj zbieżność całki $\int^{1}_{-1}{\frac{x}{1-x^4}\ dx}$

$$\begin{gathered}
\int^{1}_{-1}{\frac{x}{1-x^4}\ dx}=\begin{vmatrix}
t=x^2\\
dt = 2x\ dx
\end{vmatrix}=\frac{1}{2}\int^{1}_{1}{\frac{1}{1-x^2}\ dt}=0\\\\
\text{Inaczej:}\\
f(x)=\frac{x}{1-x^4}=-f(-x)\\
\text{Zatem funkcja jest nieparzysta co implikuje że}\\
\text{Pole powierzchni }\\\\\\
\int^{1}_{-1}{\frac{x}{1-x^4}\ dx}=\int^{0}_{-1}{\frac{x}{1-x^4}\ dx}+\int^{1}_{0}{\frac{x}{1-x^4}\ dx}=-\int^{1}_{0}{\frac{x}{1-x^4}\ dx}+\int^{1}_{0}{\frac{x}{1-x^4}\ dx}
\end{gathered}$$

---
# 2016/2017

## Termin 1

###### 1) Pokaż, że dla każego $x\gt 0$ zachodzi nierówność $\ln{(1+x)}\lt x$

$$\begin{gathered}
f(x)=\ln{(1+x)}-x\\
\lim_{x\to 0^+}{f(x)}=0-0=0\\\\
f'(x)=\frac{1}{1+x}-1\\\\
f'(x)\lt 0\ \ \forall x\gt 0\\
\frac{1}{1+x}-1\lt 0\\
1-1-x\lt 0\\
-x\lt 0\\
x\gt 0 \ \ \checkmark\\
\end{gathered}$$
Lub taylor:
$$\begin{gathered}
f(x)=\ln{(1+x)}=f(0)+\frac{f'(0)}{1!}\cdot x+\frac{f''(0)}{2!}x^2+R_3(x)\\\\
\ln{(1+x)}=x-\frac{1}{2}x^2+R_3(x)\implies \ln{(1+x)}\lt x
\end{gathered}$$
---
###### 1b) Pokaż że ciąg o wyrazie $a_n=(1+\frac{1}{3})(1+\frac{1}{9})\dots(1+\frac{1}{3^n})$ jest zbieżny

$$\begin{gathered}
\frac{a_{n+1}}{a_n}=(1+\frac{1}{3^{n+1}})\gt 1\\\\

\\
a_n=e^{\ln((1+\frac{1}{3})(1+\frac{1}{9})\dots (1+\frac{1}{3^n}))}=
e^{\ln(1+\frac{1}{3})+\ln(1+\frac{1}{9})\dots (1+\frac{1}{3^n})}=\\
=e^{\ln(1+\frac{1}{3})}\cdot e^{\ln(1+\frac{1}{9})}\dots e^{\ln(1+\frac{1}{3^n})}=\\
\lt e^{\frac{1}{3}}\cdot e^\frac{1}{9}\dots e^{\frac{1}{3^n}}=e^{\frac{\frac{1}{3}}{1-\frac{1}{3}}}=e^{\frac{1}{3}\cdot \frac{3}{2}}=\sqrt{e}\\\\
\text{Ciąg }a_n \text{ jest rosnący, a ciąg większy od niego ma granicę.}
\end{gathered}$$

---
###### 2) Zbadaj przebieg zmienności funkcji $f(x)=x^x$

$$\begin{gathered}\\
f(x)=x^x=e^{\ln{x}\cdot x}\\\\
D:(0,+\infty)\\
\text{Nie jest parzysta, nie jest nieparzysta, ani nie jest okresowa. Jest ciągła.}\\\\
\text{Nie przecina się z osią OX bo 0 nie należy do dziedziny.}\\
e^{\ln{x}\cdot x}=0\\
\ln{x}\cdot x=-\infty \ \text{Sprzeczne}\\
\text{Nie przecina się z osią OY}\\\\
f'(x)=e^{\ln{x}\cdot x}\cdot (1+\ln{x})\\\\
f'(x)=0\\
f'(x)=1+\ln{x}=0\\
\ln{x}=-1\implies x=\frac{1}{e}\\

\lim_{x\to \infty}=\infty\\
\lim_{x\to 0^+}f(x)=\lim_{x\to 0^+}e^{\ln{x}\cdot x}=
e^{\lim_{x\to 0^+}{\ln{x}\cdot x}}=
e^{\lim_{x\to 0^+}{\frac{\frac{1}{x}}{-\frac{1}{x^2}}}}=e^{\lim_{x\to 0^+}{-x}}=1\\\\
Asymptoty:\\\\
a=\lim_{x\to \infty}{\frac{e^{\ln{x}\cdot x}}{x}}=
\lim_{x\to \infty}{\frac{e^{\ln{x}\cdot x}}{e^{\ln{x}}}}=
\lim_{x\to \infty}{e^{\ln{x}(x-1)}}=\infty \\
\text{Zatem nie ma żadnych asymptot}\\
f''(x)=(e^{\ln{x}\cdot x}\cdot (1+\ln{x}))'=e^{\ln{x}\cdot x}[(1+\ln{x})^2+\frac{1}{x}]\gt 0\\
\text{Zatem brak punktów przegięcia}
\end{gathered}$$
---
###### 3. Oblicz wartość $\sin{10\degree}$ z dokładnością do $0.00001$ i sprawdź czy $\sin{10\degree}\lt \frac{\sqrt{3}}{10}$ Podaj dokładną wypowiedź twierdzenia z którego skorzystałeś.

Twierdzenie taylora mówi że jeżeli mamy otoczenie $U$ do którego należy $x_0$ a funkcja należy do $C^n(x_0)$ to istnieje takie c że:

$$\begin{gathered}
f(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+\dots +R_n(x,x_0)\\\\
gdzie \ R_n(x,x_0)=\frac{f^n(c)}{n!}(x-x_0)^n\\\\
\end{gathered}$$

$$\begin{gathered}
10\degree=\frac{\pi}{18}\approx 0.17452\\
x_0=0\\
\sin{x}=\frac{\cos{0}}{1!}x+\frac{-\sin{0}}{2!}x^2+\frac{-\cos{0}}{3!}x^3+\dots R_n(x_0,x)=\\
=x-\frac{x^3}{3!}+\frac{x^5}{5!}\dots +R_n(0,x)\\
\\
\sin{x}=0.1745329-\frac{0.1745329^3}{6}+\frac{0.1745329^5}{120}\\
\end{gathered}$$
---
###### 4. Oblicz pole części figury ograniczonej krzywą $(x^2+y^2)^2=2xy$ zawartej wewnątrz okręgu $x^2+y^2=\sqrt{2}y$

$$\begin{gathered}
x^2+y^2=\sqrt{2}y\\
x^2+y^2-\sqrt{2}y+\frac{1}{2}=\frac{1}{2}\\
x^2+(y-\frac{\sqrt{2}}{2})^2=\frac{1}{2}\\\\
\left\{
\begin{matrix}
r^2=\sin{2\phi}\\
r^2\lt \sqrt{2}\sin{\phi}
\end{matrix}
\right.\\\\
\sqrt{2}\sin{\phi}\cos{\phi}\lt \sin{\phi}\\
\sin{\phi}(\sqrt{2}\cos{\phi}-1)\lt 0\\
(\sin{\phi}\gt 0\land \cos{\phi}\lt \frac{\sqrt{2}}{2})\\
\phi \gt \frac{\pi}{4}\\\\

\frac{1}{2}\int^{\frac{\pi}{2}}_{\frac{\pi}{4}}{r_1^2(\phi)-r_2^2(\phi)\ d\phi}=\dots 
\end{gathered}$$

---
###### 5. Oblicz objętość bryły powstałej z obrotu dookoła osi $OX$ krzywej $y=e^{-x}|\sin{x}|$, dla $x\geq 0$

$$\begin{gathered}
|V|=\pi \int^{2\pi }_{0}f^2(x)\ dx=
\pi \int^{2\pi}_{0}{\sin^2{x}\cdot e^{-2x}\ dx}\\


\int{\sin^2{x}\cdot e^{-2x}\ dx}=\frac{1}{2}\int{(1-\cos{2x})\cdot e^{-2x}\ dx}=\\
=\frac{1}{2}\int{(1-\cos{(-2x)})\cdot e^{-2x}\ dx}=\begin{vmatrix}
t=-2x\\
dt=-2 \ dx
\end{vmatrix}=\\
=-\frac{1}{4}{\int{(1-\cos{t})\cdot e^t}\ dt}=
-\frac{1}{4}((1-cos{t})\cdot e^t-\int{\sin{t}e^t\ dt})=\\=
-\frac{1}{4}((1-cos{t})\cdot e^t-(\sin{t}e^t-\int{\cos{t}e^t\ dt}))=\\\\

-\frac{1}{4}\int{(1-\cos{t})\cdot e^t \ dt}=-\frac{1}{4}((1-\cos{t})\cdot e^t-(sin{t}e^t-\int{\cos{t}e^t}))\\
\int{(1-\cos{t})\cdot e^t \ dt}=((1-\cos{t})\cdot e^t-sin{t}e^t-\int{\cos{t}e^t}))

\end{gathered}$$

$$\begin{gathered}
|V|=\pi \int^{2\pi}_{0}{f^2(x)\ dx}=
\pi \int^{2\pi}_{0}{\sin^2{x}\cdot e^{-2x}\ dx}=
\pi \int^{2\pi}_{0}{\frac{1-cos{2x}}{2}\cdot e^{-2x}\ dx}=\\
=\frac{\pi}{2}\int^{2\pi}_{0}{(1-\cos{(-2x)}\cdot e^{-2x})}=\begin{vmatrix}
t=-2x\\
dt = -2 \ dx
\end{vmatrix}=-\frac{\pi}{4}\int^{-4\pi }_{0}{e^t-\cos{t}e^t\ dt}=\\
=-\frac{\pi}{4}(\int^{-4\pi}_{0}{e^t}-\int^{-4\pi}_{0}{\cos{t}e^t \ dt})=
-\frac{\pi}{4}(e^{-4\pi}-(\frac{e^{-4\pi}}{2}-\frac{1}{2}))=\\
=\frac{\pi}{8}(-\frac{1}{2}-\frac{e^{-4\pi}}{2})
\end{gathered}$$

---
## Termin II

###### 1. Wyznacz wszystkie asymptoty funkcji $f(x)=\frac{1}{x+2\sqrt{x^2+1}}$

$$\begin{gathered}
f(x)=\frac{1}{x+2\sqrt{x^2+1}}\\\\
\text{Pionowe:}\\\\
x+2\sqrt{x^2+1}=0\\
2\sqrt{x^2+1}=-x\\
4x^2+4=x^2\\
3x^2=-4\\
x\notin \mathbb{R}\\
\text{Nie ma asymptot pionowych.}
\\
\lim_{x\to \infty}{\frac{f(x)}{x}}=
\lim_{x\to \infty}\frac{\frac{1}{x+2\sqrt{x^2+1}}}{x}=0\\
\lim_{x\to \infty}f(x)=0\\
\lim_{x\to -\infty}f(x)=\lim_{x\to -\infty}{\frac{1}{x+2\sqrt{x^2+1}}}=\begin{vmatrix}
t=-x\\
-\infty \to \infty 
\end{vmatrix}=\lim_{t\to \infty }{\frac{1}{2\sqrt{t^2+1}-t}}=\\
\lim_{t\to \infty }{\frac{2\sqrt{t^2+1}+t}{(2\sqrt{t^2+1}-t)\cdot (2\sqrt{t^2+1}+t)}}=\lim_{t\to \infty }{\frac{2\sqrt{t^2+1}+t}{4t^2+4-t^2}}=0\\\\\
\text{Asymptota pozioma lewostronna i prawostronna jest określona równaniem }y=0
\end{gathered}$$

---
###### 2. Wyznacz wymiary stożka opisanego na kuli o promieniu $R$, który ma najmniejszą objętość.

![[diagram-20250202 (1).png]]
$$\begin{gathered}
V=\frac{1}{3}\pi r^2H\\
x=\frac{HR}{r}\\
\frac{H}{\frac{HR}{r}+r}=\frac{\frac{HR}{r}}{H-R}\\
H^2-HR=\frac{(HR)^2}{r^2}+HR\\
r^2(H^2-HR)=(HR)^2+r^2(HR)\\
r^2(H^2-2HR)=(HR)^2\\
r^2=\frac{HR^2}{H-2R}\\\\

V(H)=\frac{1}{3}r^2H=\frac{1}{3}\frac{(HR)^2}{H-2R}\\
V'(H)=\frac{1}{3}\cdot \frac{2HR^2(H-2R)-(HR)^2}{H^2-4HR+4R^2}=
\frac{(HR)^2-4HR^3}{3(H^2-4HR+4R^2)}\\\\


\frac{R^2(H^2-4HR)}{(H-2R)^2}=0\\\\
H^2-4HR=0\\
H(H-4R)=0\\
H=4R\\
r^2=\frac{4R^3}{2R}=2R^2\\
r=\sqrt{2}R
\end{gathered}$$
---
###### 3. a) Podaj definicję wypukłości w przedziale $(a,b)$ funkcji różniczkowalnej. 

$$\begin{gathered}
\text{funkcja różniczkowalna jest wypukła w przedziale (a,b) jeżeli:}\\
\{(x,y): x\in (a,b) \land y\gt f(x)\}\text{ jest zbiorem wypukłym}\\\\
\text{funkcja jest różniczkowalna w zbiorze }(a,b) \Leftrightarrow\\
\forall x_0 \in I \ \forall x \in I, x \neq x_0 \ \ f(x)\gt f(x_0)+f'(x_0)(x-x_0)
\end{gathered}$$
###### 3. b) Podaj wypowiedź twierdzenia będącego warunkiem wystarczającym na wypukłość funkcji w przedziale $(a,b)$ i udowodnij to twierdzenie:

$$\begin{gathered}
Z: f\in C^2(x)\forall x\in (a,b)\\
\text{Funkcja jest wypukła jeżeli: }f''(x)\gt 0\\\\
D:\\
\text{Przybliżając sobie funkcję taylorem otrzymujemy:}\\\\
f(x)=f(x_0)+\frac{f'(x_0)}{1}(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+R_3(x_0,x)\\
\text{Zatem jeżeli }f(x) \text{ ma być większe od }f(x_0)+f'(x_0)(x-x_0)\\
\text{to: }\frac{f''(x_0)}{2!}(x-x_0)^2 \text{ musi być większe od 0}\\\\
\frac{f''(x_0)}{2!}(x-x_0)^2\gt 0\\
f''(x_0)\gt 0 \ c.k.d
\end{gathered}$$
Wyznacz przedziały wypukłości i wklęsłości funkcji $f(x)=(\ln{x})^2-2\ln{x}$

$$\begin{gathered}
f'(x)=2\ln{x}\cdot \frac{1}{x}-2\frac{1}{x}=\frac{2\ln{x}-2}{x}\\\\
f''(x)=\frac{2-(2\ln{x}-2)}{x^2}=\frac{4-2\ln{x}}{x^2}\\\\
f''(x)\gt 0\\
\Leftrightarrow\\
\frac{4-2\ln{x}}{x^2}\gt 0\\
4\gt 2\ln{x}\\
2\gt \ln{x} \implies x\lt e^2\\
\\\\
f''(x)\lt 0\\
\Leftrightarrow\\
\frac{4-2\ln{x}}{x^2}\lt 0\\
4\lt 2\ln{x}\\
2\lt \ln{x} \implies x\gt e^2\\
\end{gathered}$$
---
###### 4. Oblicz długość krzywej $y=\arcsin{(e^{-x})}, 0\leq x\leq 1$

$$\begin{gathered}
\arcsin{x}'=\frac{1}{\sqrt{1-x^2}}\\
y'=\frac{1}{\sqrt{1-e^{-2x}}}\cdot e^{-x}\cdot -1

\\
|S|=\int^{1}_{0}{\sqrt{1+f'(x)^2}}=\int^{1}_{0}{\sqrt{1+\frac{e^{-2x}}{1-e^{-2x}}}\ dx}=\\\\
=\int^{1}_{0}{\sqrt{\frac{1-e^{-2x}}{1-e^{-2x}}+\frac{e^{-2x}}{1-e^{-2x}}}\ dx}=\int^{1}_{0}{\sqrt{\frac{1}{1-e^{-2x}}}\ dx}=\begin{vmatrix}
t=1-e^{-2x}\\
dt=2e^{-2x}\ dx\\
dx=\frac{dt}{2e^{-2x}}
\end{vmatrix}=\\\\
=-\frac{1}{2}\int^{1-e^{-2}}_{0}{\frac{1}{\sqrt{t}}\cdot \frac{1}{t-1}\ dt}=
\begin{vmatrix}
u=\sqrt{t}\\
2u du=dt
\end{vmatrix}=-\int^{\sqrt{1-e^{-2}}}_{0}{\frac{1}{u^2-1}\ du}=\\\\
=-\int^{\sqrt{1-e^{-2}}}_{0}{\frac{1}{u-1}+\frac{1}{u+1}\ du}=
-\frac{1}{2}\int^{\sqrt{1-e^{-2}}}_{0}{\frac{1}{u-1}}+\frac{1}{2}\int^{\sqrt{1-e^{-2}}}_{0}{\frac{1}{u+1}\ du}=\\\\
=\frac{1}{2}(\ln{|\sqrt{1-e^{-2}}+1|}-\frac{1}{2}(\ln{|\sqrt{1-e^{-2}}-1})=
\frac{1}{2}{\ln{\frac{1-e^{-2}+2\sqrt{1-e^{-2}}+1}{-e^{-2}}}}
\end{gathered}$$

---
###### 5. Oblicz całke $\int{\frac{x^3-6}{x^4+6x^2+8}\ dx}$

$$\begin{gathered}
\int{\frac{x^3-6}{x^4+6x^2+8}\ dx}=\\\\\

\frac{x^3-6}{x^4+6x^2+8}=\frac{x^3-6}{(x^2+2)(x^2+4)}=\frac{Ax+B}{x^2+2}+\frac{Cx+D}{x^2+4}\\\\
x^3-6=(Ax+B)(x^2+4)+(Cx+D)(x^2+2)\\
x^3-6=Ax^3+4Ax+Bx^2+4B+Cx^3+2Cx+Dx^2+2D\\
x^3-6=x^3(A+C)+x^2(B+D)+x(4A+2C)+4B+2D\\
\left\{
\begin{matrix}
A=-1\\
B=-3\\
2=C\\
D=3
\end{matrix}
\right.\\\\
\int{\frac{x^3-6}{x^4+6x^2+8}\ dx}=\int{\frac{-x-3}{x^2+2}\ dx}+\int{\frac{2x+3}{x^2+4}\ dx}=\\\\
=-\frac{1}{2}\int{\frac{2x+6}{x^2+2}}+\int{\frac{2x}{x^2+4}}+\int{\frac{3}{x^2+4}}=\\\\
=-\frac{1}{2}\int{\frac{2x}{x^2+2}\ dx}-\frac{1}{2}\int{\frac{6}{x^2+2}\ dx}+\ln{|x^2+4|}+\int{\frac{3}{x^2+4}\ dx}=
\end{gathered}$$$$\begin{gathered}
=-\frac{1}{2}\ln{|x^2+2|}-3\int{\frac{1}{x^2+2}\ dx}+\ln{|x^2+4|}+3\int{\frac{1}{x^2+4}\ dx}=\\\\
=-\frac{1}{2}\ln{|x^2+2|}-\frac{3}{2}\int{\frac{1}{(\frac{x}{\sqrt{2}})^2+1}}+\ln{|x^2+4|}+\frac{3}{4}\int{\frac{1}{(\frac{x}{2})^2+1}\ dx}=\\\\
\int{\frac{1}{(\frac{x}{\sqrt{2}})^2+1}}=\begin{vmatrix}
t=\frac{x}{\sqrt{2}}\ dx\\
dt=\frac{1}{\sqrt{2}}\ dx\\
\sqrt{2}\ dt=dx
\end{vmatrix}=\sqrt{2}\arctan{\frac{x}{\sqrt{2}}}
\end{gathered}$$

---
## Termin 3

###### 1. Sprawdź dla jakich $x$ zachodzi równość $\arcsin{x}=\arctan{\frac{x}{\sqrt{1-x^2}}}$.

$$\begin{gathered}
\arcsin{x}=\arctan{\frac{x}{\sqrt{1-x^2}}}\\
|x|\lt 1\\
\arcsin{\sin{x}}=\arctan{\frac{\sin{x}}{\sqrt{1-\sin^2{x}}}}\\
\arcsin{\sin{x}}=\arctan{\frac{\sin{x}}{\cos{x}}}\\
\arcsin{\sin{x}}=\arctan{\tan{x}}\\
x=x\\\\
\forall x \in [-1,1]
\end{gathered}$$
---
###### 1.b) Wyznacz dziedzinę i asymptoty ukośne funkcji $f(x)=\frac{x}{x+2\sqrt{x^2-1}}$

$$\begin{gathered}
1) \sqrt{x^2-1}:\\
x^2-1\geq 0\implies x^2\geq 1\implies x\in (-\infty, -1] \cup [1,\infty ]\\\\
2)\ \ x+2\sqrt{x^2-1}=0\\
2\sqrt{x^2-1}=-x\\
4(x^2-1)=x^2\\
3x^2-4=0\\
3x^2=4\\
x=\frac{2\sqrt{3}}{3}\vee x=-\frac{2\sqrt{3}}{3}\\\
x\in (-\infty,-\frac{2\sqrt{3}}{3})\cup (-\frac{2\sqrt{3}}{3},-1]\cup [1,\frac{2\sqrt{3}}{3})\cup (\frac{2\sqrt{3}}{3},\infty)\\\\

a=\lim_{x\to \infty}{\frac{f(x)}{x}}=\frac{1}{x+2\sqrt{x^2-1}}=0\\\\
b=\lim_{x\to \infty}{f(x)-ax}=\frac{1}{3}\\
a=\lim_{x\to -\infty}{\frac{f(x)}{x}}=\frac{1}{x+2|x|\sqrt{1-\frac{1}{x^2}}}=0\\\\
\end{gathered}$$---
# 2017/2018

### Termin 1

###### 1. Pokaż, że ciąg rekurencyjny $a_1=1, a_{n+1}=\frac{a_n^2+a_n+1}{a_n+3}$ jest zbieżny i oblicz jego granicę.

$$\begin{gathered}
\text{Ograniczenie dolne:}\\
1) a_1\gt \frac{1}{2}\\
2) a_n\gt \frac{1}{2}\\
3) a_{n+1}=\frac{a_n^2+a_n+1}{a_n+3}\gt \frac{\frac{7}{4}}{\frac{7}{2}}=\frac{1}{2}\\\\
\text{Ograniczenie górne:}\\
1) a_1\leq 1\\
2) a_n\leq 1\\
3) a_{n+1}=\frac{a_n^2+a_n+1}{a_n+3}\gt \frac{1+1+1}{1+3}=\frac{3}{4}\leq 1\\\\
a_n\in [\frac{1}{2},1]
\end{gathered}$$

$$\begin{gathered}
a_{n+1}-a_n\lt 0\\
\frac{a_n^2+a_n+1}{a_n+3}-a_n\lt0\\
\frac{a_n^2+a_n+1}{a_n+3}-\frac{a_n^2+3a_n}{a_n+3}\lt 0\\
\frac{-2a_n+1}{a_n+3}\lt 0\\
-2a_n+1\lt 0\\
a_n\gt \frac{1}{2}\\\\
a_n \text{ jest ciągiem monotonicznym, malejącym}
\end{gathered}$$

$$\begin{gathered}
a_n=\frac{a_n^2+a_n+1}{a_n+3}\\
a_n=\frac{1}{2}
\end{gathered}$$
---
###### 2. Wyznacz wszystkie asymptoty, przedziały monotoniczności i ekstrema lokalne funkcji $f(x)=|x|^{\frac{1}{x}}$

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
x^{\frac{1}{x}}=e^{\ln{x}\cdot \frac{1}{x}}, x\gt 0\\
-x^{\frac{1}{x}}=e^{\ln{-x}\cdot \frac{1}{x}}, x\lt 0
\end{matrix}
\right.\\\\
\text{Asymptoty:}\\
\lim_{x\to 0^-}{f(x)}=e^g:\\
g={\lim_{x\to 0^-}{\frac{\ln{(-x)}}{x}}}=\infty \\
\dots =\infty \\
x=0\\\\\\\
\lim_{x\to 0^+}{f(x)}=e^g:\\
g={\lim_{x\to 0^+}{\frac{\ln{(x)}}{x}}}=-\infty \\
\dots =0 \\
x=0\\\\
\lim_{x\to \infty}e^g:\\
g=\lim_{x\to \infty}{\frac{\ln{x}}{x}}=\lim_{x\to \infty}{\frac{\frac{1}{x}}{1}}=0\\\\
\lim_{x\to -\infty}e^g:\\
g=\lim_{x\to- \infty}{\frac{\ln{-x}}{x}}=\lim_{x\to -\infty}{\frac{\frac{-1}{-x}}{1}}=0\\
\end{gathered}$$

$$\begin{gathered}
f'(x)=\left\{
\begin{matrix}
e^{\ln{x}\cdot \frac{1}{x}}\cdot \frac{1-\ln{x}}{x^2}, x\gt 0\\
e^{\ln{-x}\cdot \frac{1}{x}}\cdot (\frac{1-\ln{-x}}{x^2},x \lt 0\\
\end{matrix}
\right.\\\\
e^{\ln{x}\cdot \frac{1}{x}}\cdot \frac{1-\ln{x}}{x^2}=0\\
1=\ln{x}\implies x=e\\
e^{\ln{-x}\cdot \frac{1}{x}}\cdot (\frac{1-\ln{-x}}{x^2}=0\\
1=\ln{-x}\implies x=-e
\end{gathered}$$
---
###### 3a) Podaj definicję całki Riemanna funkcji na przedziale domkniętym (wraz ze wszystkimi pojęciami potrzebnymi do wypowiedzi tej definicji)

$$\begin{gathered}
f: [a,b]\to \mathbb{R}, ograniczona\\
P_n:a= x_0,x_2,\dots,x_n= b,\ ciąg \ podzialu\\
a=x_0,x_2,\dots,x_n= b,\ punkty \ podzialu\\
\Delta x_i=x_i-x_{i=1} \forall i \in [1,n]\\
\delta_n=max\{\Delta x_i: i=1,2,\dots,n\}\\
\text{Ciag podzialu jest normalny jezeli}
\lim_{n\to \infty}\delta_n=0\\\\
Niech \ P_f \ będzie \ ciągiem \ podzialu \ [a,b]\text{ w każdym z podziałów } [x_i, x_{i-1}]\\ \text{ wybieramy punkt pośredni }c_i: c_i\in [x_i,x_{i-1}]\\
\text{Jeżeli wartość }
\end{gathered}$$
Jeśli dla każdego normalnego ciągu podziałów przedziału $[a,b]$ i dowolnego wyboru punktów pośrednich $c_i$ istnieje $\lim_{n\to \infty}{S_n}$ która nie zależy ani od wyboru ciągu podziałów, ani od wyboru punktów pośrecnih, to granicę tę nazywamy całką Riemenna funkcji $f$ na przedziale $[a,b]$

$$\begin{gathered}
\underset{\lim_{\delta_n\to 0}}{
\lim_{n\to \infty}}{\sum^{n}_{1}{f(c_i)\Delta_i}}
\end{gathered}$$

###### 3b) Oblicz granicę ciągu $a_n=\frac{1}{n+1}+\frac{1}{n+2}+\dots+\frac{1}{n+n}$

$$\begin{gathered}
\lim_{n\to \infty}{\sum^{n}_{i=1}{\frac{1}{n+i}}}=
\lim_{n\to \infty}{\sum^{n}_{i=1}{\frac{1}{1+\frac{i}{n}}\cdot \frac{1}{n}}}=\int^{1}_{0}{\frac{1}{1+x}\ dx}=\ln{2}-\ln{1}=\ln{2}

\end{gathered}$$

###### 4) Oblicz długość krzywej $y=\ln{(\cos{x})}$. $0\leq x\leq \frac{\pi}{3}$
$$\begin{gathered}
y=\ln{\cos{x}}\\
y'=\frac{1}{\cos{x}}\cdot -\sin{x}=-\tan{x}\\\\
\int^{\frac{\pi}{3}}_{0}{\sqrt{1+\tan^2{x}}\ dx}=
\int^{\frac{\pi}{3}}_{0}{\frac{1}{\cos{x}}\ dx}=
\begin{vmatrix}
t=\sin{x}\\
dt=\cos{x}\ dx
\end{vmatrix}=\int^{\frac{\sqrt{3}}{2}}_{0}{\frac{1}{1-t^2}dt}=\\\\
=\int^{\frac{\sqrt{3}}{2}}_{0}{\frac{\frac{1}{2}}{1-t}+\frac{\frac{1}{2}}{t+1}\ dt}=\frac{1}{2}\ln{|1+\frac{\sqrt{3}}{2}|}-\frac{1}{2}(\ln{|1-\frac{\sqrt{3}}{2}|})
\end{gathered}$$

---
###### 5. Oblicz pole powierzchni elipsoidy powstałej z obrotu dookoła osi $OX$ elipsy $x=\cos{t}, y=2\sin{t}$

$$\begin{gathered}
x=\cos{t}\\
y=2\sin{t}\\
y(t)=2\sin{t}\gt 0\\
\sin{t}\gt 0\\
t\in [0,\pi ]

\\\\

|S|=2\pi \int^{\pi}_{0}{2\sin{t}\sqrt{1+3\cos^2}\ dt}=
2\pi \int^{\pi}_{0}{2\sin{t}\sqrt{1+3\cos^2}\ dt}=
\begin{vmatrix}
x=\cos{t}\\
dx=-\sin{t}\ dt
\end{vmatrix}=\\\\
=-4\pi \int^{0}_{1}{\sqrt{1+3x^2}\ dx}=\begin{vmatrix}
\sqrt{1+3x^2}=t-x\sqrt{3}\\
1=t^2-2xt\sqrt{3}\\
2xt\sqrt{3}=t^2-1\\
x=\frac{t^2-1}{2\sqrt{3}t}\\
dx=\frac{t^2+1}{2\sqrt{3}t^2}\ dt
\end{vmatrix}=\\\\
=-\frac{1}{\sqrt{3}}\pi \int^{1}_{2+\sqrt{3}}{\frac{(t^4+t^2+1)}{t^3}\ dt}=-\frac{1}{\sqrt{3}}\int^{1}_{2+\sqrt{3}}{t+\frac{1}{t}+\frac{1}{t^3}\ dt}=\\\\
=-\frac{1}{\sqrt{3}}(-1-\sqrt{3}+\ln{1-\ln{2+\sqrt{3}}}+\frac{1}{-2}-\frac{1}{-14+4\sqrt{3})})\\\\
\end{gathered}$$

---
###### 2a) Oblicz granicę $\lim_{x\to 0^+}{\sin{x}^{tan{x}}}$

$$\begin{gathered}
\lim_{x\to 0^+}{\sin{x}^{tan{x}}}=lim_{x\to 0^+}{(x\cdot \frac{\sin{x}}{x})^{\frac{x\cdot \frac{\sin{x}}{x}}{\cos{x}}}}=\lim_{x\to 0^+}{x^\frac{x}{\cos{x}}}=\lim_{x\to 0^+}{e^{\ln{x}\cdot \frac{x}{\cos{x}}}}:\\\\
\lim_{x\to 0^+}{\frac{\ln{x}}{\frac{1}{x}\cos{x}}}=
\lim_{x\to 0^+}{\frac{\frac{1}{x}}{\frac{-\sin{x}x-\cos{x}}{x^2}}}=
\lim_{x\to 0^+}{\frac{x}{-\sin{x}\cdot x-\cos{x}}}=0\\
e^g=e^0=1

\end{gathered}$$
---
###### 3b) Oblicz granicę ciągu $a_n=\frac{n}{(n+1)^2}+\frac{n}{(n+2)^2}+\dots+\frac{n}{(n+n)^2}$

$$\begin{gathered}
\sum^{n}_{i=1}{\frac{n}{(n+i)^2}}=
\sum^{n}_{i=1}{\frac{1}{(1+\frac{1}{n})^2}\cdot \frac{1}{n}}=\int^{2}_{1}\frac{1}{(1+x)^2}=\begin{vmatrix}
u=1+x\\
du=\ dx
\end{vmatrix}=\int^{2}_{1}{\frac{1}{u^2}}=\\=\frac{1}{2}
\end{gathered}$$
---
###### 4) Oblicz objętość bryły ograniczonej powierzchnią powstałą poprzez obrót dookoła osi $OX$ krzywej $y=\arcsin{x}, 0\leq x\leq \frac{1}{2}$

$$\begin{gathered}
\pi \int{\arcsin^2{x}\ dx}=
\begin{vmatrix}
u=\arcsin^2{x}&v'=1\\
du=\frac{2\arcsin{x}}{\sqrt{1-x^2}}\ dx&v=x
\end{vmatrix}=x\arcsin^2{x}-\int{\frac{2x\arcsin{x}}{\sqrt{1-x^2}}}=\\\\
=\begin{vmatrix}
u=\arcsin{x}&v'=\frac{2x}{\sqrt{1-x^2}}\\
du=\frac{1}{\sqrt{1-x^2}}&v=-2\sqrt{1-x^2}
\end{vmatrix}=x\arcsin^2{x}+2\arcsin{x}\sqrt{1-x^2}-2x\\\\\
\frac{\pi^2}{72}+\frac{\pi}{3}\frac{\sqrt{3}}{2}-1
\end{gathered}$$
---
###### 5) Narysuj krzywą $f(\varphi)=a\cos^3{\frac{\varphi}{3}}$ i oblicz jej długość:

$$\begin{gathered}
f(\varphi)=a\cos^3{(\frac{\varphi}{3})}\\
f'(\varphi)=a\cos^2{(\frac{\varphi}{3})}\cdot -\sin{(\frac{\varphi}{3})}\\
\\
|L|=\int^{6\pi}_{0}{\sqrt{1+a^2\cos^4{(\frac{\varphi}{3})}\sin^2{(\frac{\varphi}{3})}}\ d\varphi}=\begin{vmatrix}
u=\frac{\varphi}{3}\\
du=\frac{1}{3}\ d \varphi
\end{vmatrix}=\\=3\int^{2\pi}_{0}{\sqrt{1+a^2\cos^4{u}\sin^2{u}}\ du}=\begin{vmatrix}
x=\tan{u}\\
\sin^2{u}=\frac{\sin^2{u}}{\sin^2+\cos^2{u}}=\frac{t^2}{t^2+1}\\
\cos^2{u}=\frac{\cos^2{u}}{\sin^2+\cos^2{u}}=\frac{1}{t^2+1}\\
dx=\frac{1}{\cos^2{u}}=t^2+1 \ dt
\end{vmatrix}=\\\\\
=3\int^{0}_{0}{}
\end{gathered}$$


$$\begin{gathered}
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1\\
P=4\cdot (a-x)\cdot \sqrt{b^2-\frac{b^2x^2}{a^2}}\\\\
\dfrac{4\,\left|b\right|\,\left(2\,{x}^{2}-a\,x-{a}^{2}\right)}{\left|a\right|\,\sqrt{{a}^{2}-{x}^{2}}}=0\\
(2x^2-ax-a^2)=0\\
p=-\frac{-a}{2}=\frac{a}{2}
\end{gathered}$$