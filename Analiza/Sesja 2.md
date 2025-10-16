
## 2011/2012 

### $I$ termin 

###### 1. Znaleźć asymptoty, ekstrema i przedziały monotoniczności funkcji $f(x)=x^{\frac{1}{x}}$. Naszkicować jej wykres bez obliczenia drugiej pochodnej.

$$\begin{gathered}
f(x)=x^{\frac{1}{x}}=e^{\ln{(x)}\cdot \frac{1}{x}}\\\\
D: (0, \infty)\\
\lim_{x\to \infty}{f(x)}=e^{\lim_{x\to \infty}{\frac{\ln{(x)}}{x}}}=e^{\lim_{x\to \infty }{\frac{1}{x}}}=1\\\\
\lim_{x\to 0^+}{f(x)}=\lim_{x\to 0^+}{e^{\frac{\ln{(x)}}{x}}}=0\\\\
f'(x)=e^{\frac{\ln{(x)}}{x}}=e^{\frac{\ln{(x)}}{x}}\cdot \frac{1-\ln{(x)}}{x^2}\\\\
f'(x)=0\Leftrightarrow 1=\ln{(x)}\implies x=e\\\\
f'(x)\gt 0\\
1-\ln{(x)}\gt 0\\
1\gt \ln{(x)}\\
x\lt e\\\\
f'(x)\lt 0\\
1-\ln{(x)}\lt 0\\
1\lt \ln{(x)}\\
x\gt e
\end{gathered}$$

---
###### 2. Udowodnić, że $\frac{x}{x+1}\leq \ln{(x+1)}\leq x$ dla $x\in (-1,+\infty)$

$$\begin{gathered}
1) \ln(x+1)\leq x\\\\
\ln{(x+1)}=x-x^2+R_3(0,x)\implies \ln{(x+1)}\leq x\\\\
1) \frac{x}{x+1}\leq \ln{(x+1)}\\\\
f(x)=\ln{(x+1)}-\frac{x}{x+1}\\
f'(x)=\frac{x+1}{(x+1)^2}-\frac{1}{(x+1)^2}=\frac{x}{(x+1)^2}\\\\
f'(x)\lt 0 \Leftrightarrow x\lt 0\\
f'(x)\gt 0 \Leftrightarrow x\gt 0\\
f'(x)=0 \Leftrightarrow x=0\\
f(x)=0 \checkmark\\\\
\text{Zatem wiemy że funkcja maleje do }x=0\\
\text{A w punkcie x=0 funkcja dalej spełnia równanie}\\
\text{Co dowodzi nam nierówności }
\end{gathered}$$

---
###### 3. Oblicz:

$$\begin{gathered}
\theta (x)=\int^{x}_{-\infty}{f(t) \ dt}, \text{Jeśli }
f(x)=\left\{
\begin{matrix}
x^3e^{-x^2}, x \leq 0\\
\frac{\sin{2x}}{\sqrt{\cos^2{x}+2\cos{x}+2}}, x \gt 0
\end{matrix}
\right.
\end{gathered}$$
Oblicz $\theta'(x)$ tam gdzie istnieje:

---
###### 4. Oblicz pole figury ograniczonej krzywymi $r=\frac{1}{\theta}, r=\frac{1}{\sin{\theta}}$ dla $\theta \in (0,\frac{\pi}{2})$

$$\begin{gathered}
P=\frac{1}{2}\int^{\frac{\pi}{2}}_{0}{\frac{1}{\sin^2{x}}-\frac{1}{x} dx }=\frac{1}{2}\int^{\frac{\pi}{2}}_{0}{\frac{1}{\sin^2{x}}\ dx}-\int^{\frac{\pi}{2}}_{0}{\frac{1}{x}}=\frac{1}{2}(-\cot{\frac{\pi}{2}-\cot{0}})\\\\
\dots \text{Nieskonoczone pole}
\end{gathered}$$

---
###### 2a) Podaj treść twierdzenia Rolle'a
Jeżeli funkcja w przedziale $[a,b]$ osiąga te same wartości na krańcach to ma gdzieś w tym przedziale punkt gdzie pochodna równa 0. Albo dlatego że jest stała albo dlatego że gdzieś musi "zawrócić", osiągnąć wartość maksymalną lub minimalną.

###### b) Udowodnić, że dla $n\geq 1$ równanie $f'(x)=0$ ma dokładnie $n-1$ pierwiastków, gdzie:
$$\begin{gathered}
f(x)=(x-1)(x-2)(x-3)\dots(x-n)
\end{gathered}$$
Z twierdzenia rolle'a wynika że pomiędzy każdą parą punktów $a,b$ należących do dziedziny, jeśli funkcja osiąga na krańcach przedziału $[a,b]$ tą samą wartość to w tym zakresie ma punkt $c$ taki dla którego pochodna równa zero.

Zatem utwórzmy sobie przedziały $[1,2],[2,3],[4,5]\dots,[n-1,n]$ jest ich łącznie $n-1$ i dla każdego z nich istnieje w nim punkt że pochodna się zeruje, co oznacza że ma $n-1$ pierwiastków w tych przedziałach. Dla $(0,1), (n,+\infty)$ nie ma żadnego punktu dla którego pochodna się zeruje bo albo musiałaby zawrócić, do czego musielibyśmy ją pomnożyć razy kolejny wyraz $(x-i)$ albo musiałaby być stała.

###### 3. Podaj definicje funkcji górnej granicy całkowania i wypowiedź twierdzenia o różniczkowalności tej funkcji:

Funkcję górnej granicy całkowania definiujemy jako:
Niech $f: [a,b]\to \mathbb{R}$ 
$$\begin{gathered}
\int^{x}_{a}{f(t)\ dt}, x\in [a,b]
\end{gathered}$$

Funkcja ta jest różniczkowalna w pewnym punkcie $x_0\in [a,b]$ wtedy i tylko wtedy kiedy funkcja jest ciągła w tym punkcie a wartość pochodnej dla tego punktu wynosi po prostu $f(x_0)$

---
### 2 Termin 

###### 1. Oblicz granicę: 
$$\begin{gathered}
\lim_{x\to 0^+}{x^{\sin{x}}}=
\lim_{x\to 0^+}{x^{x}}=
\lim_{x\to 0^+}{e^{\frac{\ln{(x)}}{\frac{1}{x}}}}=
e^{\lim_{x\to 0^+}\frac{\ln{(x)}}{\frac{1}{x}}}=1
\end{gathered}$$
###### 2. Wyznacz wartość największą i najmniejszą funkcji: $f(x)=|\frac{\sin{x}}{2+\cos{x}}|$

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{\sin{x}}{2+\cos{x}}, 
\frac{\sin{x}}{2+\cos{x}}\gt 0\\
-\frac{\sin{x}}{2+\cos{x}}, \frac{\sin{x}}{2+\cos{x}}\lt 0
\end{matrix}
\right.\\\\
\frac{\sin{x}}{2+\cos{x}}\gt 0\\
\sin{x}\gt 0\\
x\in (2k\pi, 2k\pi+\pi )\\\\\
f(x)=\left\{
\begin{matrix}
\frac{\sin{x}}{2+\cos{x}}, x\in [0,\pi ]\\
-\frac{\sin{x}}{2+\cos{x}}, x\in (\pi, 2\pi ]\\
\end{matrix}
\right.\\\\
g(x)=\frac{\sin{x}}{2+\cos{x}}\\
g'(x)=\frac{2\cos{x}+1}{(2+\cos{x})^2}\\\\
g'(x)=0\Leftrightarrow\frac{2\cos{x}+1}{(2+\cos{x})^2}=0\\
\cos{x}=-\frac{1}{2}\\
\\
g'(x)\lt0 \Leftrightarrow x\gt  \frac{2\pi}{3}\\
g'(x)\gt 0 \Leftarrow x\lt  \frac{2\pi}{3}\\
max=f(\frac{2\pi}{3})\\
min=0
\end{gathered}$$

---
###### 3. Obliczyć całke $\int{\frac{\arcsin{(e^x)}}{e^x}\ dx}$

$$\begin{gathered}
\int{\frac{\arcsin{(e^x)}}{e^x}\ dx}=\begin{vmatrix}
t=e^x\\
dt=e^x\ dx\\
\frac{dt}{e^x}=dx
\end{vmatrix}=\int{\frac{\arcsin{t}}{t^2}\ dt}=\\\\
=\int{\arcsin{t} \cdot t^{-2}\ dt}=\begin{vmatrix}
u=\arcsin{t}&u'=\frac{1}{\sqrt{1-t^2}}\\
v'=t^{-2}&v=-t^{-1}
\end{vmatrix}=\\=
\arcsin{t}\cdot -t^{-1}+\int{\frac{1}{t\sqrt{1-t^2}}\ dt}\\\\
\int{\frac{1}{t\sqrt{1-t^2}}\ dt}=\begin{vmatrix}
u=1-t^2\\
du=-2t\ dt\\
\frac{1}{-2t}\ du = dt
\end{vmatrix}=\int{\frac{1}{(2u-2)\sqrt{u}}\ du}=
\begin{vmatrix}
k=\sqrt{u}\\
k^2=u
\end{vmatrix}=\\\\
=\frac{1}{2}\int{\frac{1}{k(k-1)(k+1)}}=\frac{1}{2}\int{\frac{-1}{k}+\frac{\frac{1}{2}}{k-1}+\frac{\frac{1}{2}}{k+1}}=-\frac{1}{2}
\end{gathered}$$

itd

---
###### 4. Obliczyć:

a) pole ograniczone parabolą $x^2$, styczną do wykresu w punkcie $A(2,4)$ oraz osią odciętych (y=0)
![[Pasted image 20250207214239.png]]

Zatem należy policzyć pole ograniczone styczną i od niego odjąć pole ograniczone parabolą.

$$\begin{gathered}
\int^{1}_{0}{4x-4-x^2\ dx}=2x^2-4x-\frac{x^3}{3}|^1_0=2-4-\frac{1}{3}=-\frac{7}{3}\\\\
|P|=|-\frac{7}{3}|=\frac{7}{3}
\end{gathered}$$

oraz długość $x^2$ od $x=0$ do $2$

$$\begin{gathered}
|L|=\int^{2}_{0}{\sqrt{1+4x^2}}=\begin{vmatrix}
\sqrt{1+4x^2}=t-x\sqrt{4}\\
1+4x^2=t-2tx\sqrt{4}+4x^2\\
1=t-2tx\sqrt{4}\\
4tx=t-1\\
x=\frac{t-1}{4t}\\
\sqrt{1+4x^2}=t-\frac{t-1}{2t}=\frac{2t^2-t+1}{2t}\\
dx=\frac{1}{4t^2}\ dt
\end{vmatrix}=\\\\\\\
=\int^{\sqrt{17}+4}_{1}{\frac{2t^2-t+1}{8t^3}\ dt}=\frac{\ln{t}}{4}+\frac{1}{8t}-\frac{1}{16t^2}|^{\sqrt{17}+4}_1=\dots
\end{gathered}$$

---

###### 1. Podaj twierdzenie o trzech ciągach:

Gdy mamy ciągi: $a_n,b_n,c_n: \exists n_0: \forall n \gt n_0\  a_n\leq b_n\leq c_n$ oraz $\lim_{n\to \infty}{a_n}=\lim_{n\to \infty}{c_n}=g$ to $\lim_{n\to \infty}{b_n}=g$

###### b) obliczyć $\lim_{n\to \infty}{a_n}$ gdzie: $a_n=\frac{1}{n^2+1}+\frac{2}{n^2+2}+\dots+\frac{n}{n^2+n}$

$$\begin{gathered}
a_n=\frac{1}{n^2+1}+\frac{2}{n^2+2}+\dots+\frac{n}{n^2+n}=\sum^{n}_{k=1}{\frac{k}{n^2+k}}\geq \frac{k}{n^2+n}\\\\
b_n=\frac{1}{n^2+n}+\frac{2}{n^2+n}+\dots+\frac{n}{n^2+n}\\\\
b_n=\frac{1}{n^2+n}\cdot \frac{(1+n)\cdot n}{2}\text{ suma ciagu arytm}=\frac{1}{2}\\\\
c_n=\frac{1}{n^2+1}+\frac{2}{n^2+1}+\dots+\frac{n}{n^2+1}\\\\
c_n=\sum^{n}_{i=1}{\frac{i}{n^2+1}}=\frac{1}{n^2+1}\cdot \frac{(1+n)n}{2}\\\\
\lim_{n\to \infty }{\frac{n^2+n}{n^2+1}}\cdot \frac{1}{2}=\frac{1}{2}\\\\
b_n\leq a_n\leq c_n \land b_n=c_n=\frac{1}{2}\implies a_n=\frac{1}{2}
\end{gathered}$$

---
###### 2) Podaj twierdzenie o wzorze Taylora:

Zał:
U - otoczenie punktu $x_0$, $x_0\in U$ 
$f: f\in C^n(U)$

istnieje takie $c\in (x_0,x)$
$f(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+\dots+R_n(x_0,x)$
gdzie $R_n=\frac{f^n(c)}{n!}(x-x_0)^n$ 

###### stosując wzór Taylora do funkcji $f(x)=\ln{(x+1)}$ obliczyć $\ln{(0.9)}$ z dokładnością do 0.01

$$\begin{gathered}
ln(x+1)=x-\frac{x^2}{2!}+\frac{x^3}{3!}-\frac{x^4}{4!}\dots \\\\
ln(0.9)\implies x=-0.1, n\gt 2\\
ln(0.9)=-0.1-\frac{0.01}{2}+\frac{0.001}{3}=-0.1-0.01+0.000333=-0.104
\end{gathered}$$
---
###### 3. Podaj definicję funkcji górnej granicy całkowania, podaj twierdzenie o różniczkowalności funkcji granicy górnej całkowania i udowodnij je

Funkcję górnej granicy całkowania definiujemy jako: 

$$\begin{gathered}
f: całkowalna \ na \ [a, b]\\\\
F(x)=\int^{x}_{a}{f(t)\ dt}, gdzie \ x\ \in [a,b]
\end{gathered}$$

Funkcja górnej granicy całkowania jest różniczkowalna w punkcie $x$ jeżeli funkcja całkowalna jest w tym punkcie ciągła i wynosi wartości funkcji całkowalnej w punkcie x. To znaczy:

$$\begin{gathered}
F'(x)=f(x) \Leftrightarrow f\in C^1(U), x\in U
\end{gathered}$$
Dowód:

$$\begin{gathered}
F'(x)=\lim_{h\to 0}{\frac{F(x+h)-F(x)}{h}}\\\\
\frac{F(x+h)-F(x)}{h}=\frac{\int^{ x+h}_{x}f(t)\ dt+\int^{x}_{-\infty}f(t)dt-\int^{x}_{-\infty}f(t) dt}{h}=\frac{\int^{x+h}_{x}{f(t)\ dt}}{h}=\\=\frac{f(x+h)-f(x)}{h}=f'(x)
\end{gathered}$$

---
### 3 Termin 

###### 1. Podaj definicję ciągłości i różniczkowalności w punkcie 

Funkcja jest ciągła w punkcie $x_0$ jeżeli:
1) $x_0\in D$
2) istnieje $\lim_{x\to x_0}f(x)$
3) $\lim_{x\to x_0}{f(x)}=f(x_0)$

Funkcja jest różniczkowalna w punkcie $x_0$ jeżeli:
1) funkcja ciągła w punkcie $x_0$
2) istnieje granica: $\lim_{h\to 0}{\frac{f(x_0+h)-f(x_0)}{h}}$

---
###### Podaj i udowodnij twierdzenie o ciągłości funkcji różniczkowalnej.

Jeżeli funkcja jest różniczkowalna w jakimś punkcie/przedziale to jest też w nim ciągła.

Dowód:

Funkcja jest różniczkowalna kiedy istnieje taka granica:
$$\begin{gathered}
\lim_{x\to x_0}{\frac{f(x)-f(x_0)}{x-x_0}}=g
\end{gathered}$$
Możemy ją przekształcić w:
$$\begin{gathered}

\frac{\lim_{x\to x_0}{f(x)-f(x_0)}}{\lim_{x\to x_0}{x-x_0}}=g\\
\lim_{x\to x_0}{f(x)-f(x_0)}=g\cdot \lim_{x\to x_0}(x-x_0)\\
\lim_{x\to x_0}{f(x)-f(x_0)}=0\\
\text{Czyli z lewej i prawej strony funkcja zbiega do }x_0
\end{gathered}$$
---
###### 3) Oblicz funkcję górnej granicy całkowania dla $f(x)=|\cos{(x)}|$

$$\begin{gathered}
f(x)=\int^{x}_{b}{f(t)\ dt}, gdzie: \ f(x)=\left\{
\begin{matrix}
\cos{x},x\in [-\frac{\pi}{2}+2k\pi, \frac{\pi}{2}+2k\pi]\\
-\cos{x}, x \notin \dots
\end{matrix}
\right.\\\\
k=|x-b|\cdot \frac{1}{\pi}\\\\
\int^{x}_{k\pi-\frac{\pi}{2}}{\cos{x}}
\end{gathered}$$
itd, czyli liczymy ile mamy pełnych, dodajemy je i musimy sobie wytypować jeszcze jak dodać dolny i górny zakres 

---
## 2012/2013

### $I$ termin

###### 1) Pokaż, że dla każdego $x\gt 0$ zachodzi nierówność $\ln{(1+x)}\lt x$
$$\begin{gathered}
\ln{(1+x)}=0+x-x^2+R_3(0,x)\\
gdzie \ R_3(0,x)\ jest \ mniej \ znaczace \ od \ -x^2\\\\
tzn. \ \ |R_3(0,x)|\lt |-x^2|
\end{gathered}
$$
$$\begin{gathered}
\frac{a_{n+1}}{a_n}=(1+\frac{1}{3^{n+1}})\gt 1 \implies a_n \ rosnacy\\\\
a_n=(1+\frac{1}{3})\cdot (1+\frac{1}{9})\cdot (1+\frac{1}{27})\dots (1+\frac{1}{3^n})=e^{\ln{[(1+\frac{1}{3})\cdot (1+\frac{1}{9})\dots (1+\frac{1}{3^n})]}}\\\\
=e^{\ln{(1+\frac{1}{3})+\ln{(1+\frac{1}{9})}\dots ln(1+\frac{1}{3^n})}}\lt e^{\frac{1}{3}+\frac{1}{9}+\frac{1}{27}+\frac{1}{3^n}}=e^{\frac{\frac{1}{3}}{1-\frac{1}{3}}}=e^{\frac{\frac{1}{3}}{\frac{2}{3}}}=e^{\frac{1}{2}}\\\\
\text{Ciąg który jest zawsze większy od ciagu an jest ograniczony ponadto}\\
\text{Ciąg an jest rosnący co implikuje że jest zbieżny}
\end{gathered}$$

---
###### 2. Wyznacz ekstrema lokalne oraz przedziały monotoniczności, wypukłości, wklęsłości funkcji $f(x)=x^x$

$$\begin{gathered}
f(x)=x^x=e^{\ln(x)\cdot x}\\
x\gt 0\\
f'(x)=e^{\ln{(x)}\cdot x}\cdot (1+\ln{x})\\
f'(x)\gt 0 \Leftrightarrow (1+\ln(x))\gt 0\\
\ln(x)\gt -1\\
x \gt \frac{1}{e}\\
f'(x)\lt 0 \\
x\lt \frac{1}{e}\\\\
f''(x)=e^{ln(x)\cdot x}(1+\ln(x))^2+e^{ln(x)\cdot x}\frac{1}{x}\\\\
f''(x)\gt 0 \Leftrightarrow (1+ln(x))^2+\frac{1}{x}\gt 0\\\\
(1+ln(x))^2\gt 0 \land \frac{1}{x}\gt 0 \forall x \gt 0
\end{gathered}$$
Zatem funkcja jest wypukła w całej dziedzinie :LiSmile:

---
###### 3) Wyznacz funkcję $\theta=\int^{x}_{-\infty}{f(t)\ dt}$, jeśli:

$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{4}{x^2+2x+4}, x\leq 0\\
e^{-\sqrt{x}}, x\gt 0
\end{matrix}
\right.
\end{gathered}$$
I oblicz $\theta'(x)$ tam gdzie istnieje.

$$\begin{gathered}
\theta=\int^{x}_{-\infty}{f(t)\ dt}\\
\text{Jeżeli }x\gt 0:\\
\theta=\int^{x}_{0}{e^{-\sqrt{x}}}+\int^{0}_{-\infty}{\frac{4}{x^2+2x+4}}\\
\text{Jeżeli }x\lt 0\\
\theta=\int^{x}_{-\infty}{\frac{4}{x^2+2x+4}}\\\\
1)\\\\
\theta=\int^{x}_{0}{e^{-\sqrt{x}}}+\int^{0}_{-\infty}{\frac{4}{x^2+2x+4}}\\\\
\int{e^{-\sqrt{x}}\ dx}=\begin{vmatrix}
t=-\sqrt{x}\\
dt=\frac{1}{2t}\ dx
\end{vmatrix}=\int{e^t\cdot 2t\ dt}=\begin{vmatrix}
u'=e^t&u=e^t\\
v=2t&v'=2
\end{vmatrix}=\\=e^{-\sqrt{x}}\cdot (-2\sqrt{x}-2)\\\\
4\int{\frac{1}{(x+1)^2+3}}=\begin{vmatrix}
t=x+1\\
dt=dx
\end{vmatrix}=4\int{\frac{1}{t^2+3}}=\begin{vmatrix}
u=\frac{t}{\sqrt{3}}\\
du=\frac{1}{\sqrt{3}}\ dt
\end{vmatrix}=\\\\
=\frac{4}{3}\int{\frac{1}{u^2+1}}=\frac{4}{3}\arctan{\frac{x+1}{\sqrt{3}}}
\end{gathered}$$

$$\begin{gathered}
1)\theta=-2e^{-\sqrt{x}}(\sqrt{x}+1)+2-\frac{2\pi}{3}\\
2) \frac{4}{3}\arctan{\frac{x+1}{\sqrt{3}}}-\frac{2\pi}{3}\\\\
Ciągłe \ więc \ różniczkowalne\\\\
Ale \ dla \ x=0:\\
1)\lim_{x\to 0^-}{\theta}=-2+2-\frac{2\pi}{3}=\frac{2\pi}{3}\\
2)\lim_{x\to 0^+}{\theta}=\frac{2\pi}{9}-\frac{6\pi}{9}\\
\text{Są różne granice więc nie ciągła, więc nie różniczkowalna w tym punkcie }

\end{gathered}$$

---
###### 4. Oblicz pole powierzchni bryły powstałej z obrotu dookoła osi OX krzywej $y=\frac{x^2}{2}$, $x\in [0,1]$

$$\begin{gathered}
|P|=2\pi \int^{1}_{0}{\frac{x^2}{2}\sqrt{1+x^2}\ dx}=\\\\\\
\frac{1}{2}\int{x^2\sqrt{1+x^2}\ dx}=\begin{vmatrix}
x=\tan{u}\\
dx=\frac{1}{\cos^2{u}}\ du=x^2+1\\
\frac{1}{\cos{u}}=\sqrt{x^2+1}
\end{vmatrix}=\frac{1}{2}\int{\frac{sin^2{u}}{\cos^5{u}}\ du}=\\=\frac{1}{2}\int{\frac{\sin^2{u}\cos{u}}{(1-\sin^2)^3}}=\begin{vmatrix}
t=\sin{u}\\
dt=\cos{u} \ dt
\end{vmatrix}=\frac{1}{2}\int{\frac{t^2}{(1-t^2)^3}\ dt}
\end{gathered}$$

**DOKOŃCZ TO**

---
###### 1) Dany jest ciąg rekurencyjny $a_1=2, a_{n+1}=\frac{a_n}{1+a_n}$. Wyznacz wzór jawny na $a_n$ i pokaż jego słuszność korzystając z zasady indukcji matematycznej.

$$\begin{gathered}
\frac{2}{1},\frac{2}{3},\frac{2}{5}, \frac{2}{7}, \frac{2}{9}\\\\

1) a_1=\frac{2}{1+2(1-1)}=\frac{2}{1}=2\checkmark\\\\
2) a_n=\frac{2}{1+2(n-1)}\\\\
3) a_{n+1}=\frac{a_n}{1+a_n}=\frac{\frac{2}{1+2(n-1)}}{\frac{1+2n}{1+2(n-1)}}=\frac{2}{1+2n}=\frac{2}{1+2((n+1)-1)}\checkmark 
\end{gathered}$$

---
###### 4a) Podaj definicję wartości średniej funkcji na przedziale $[a,b]$ i wypowiedź drugiego twierdzenia całkowego o wartości średniej.

Wartością średnią funkcji na przedziale $[a,b]$ nazywamy: $\frac{\int^{a}_{b}{f(x)\ dx}}{a-b}$
Drugie twierdzenie o wartości średniej mówi że:
Zakładając że funkcja jest ciągła w $[a,b]$
to istnieje takie c należące do tego przedziału że $f(c)=f_{śr}$

$f\in C([a,b])$
$\exists c\in [a,b]: f(c)=f_{śr}=\frac{\int^{b}_{a}{f(x) \ dx}}{b-a}$


Notabene pierwsze twierdzenie o wartości średniej mówi że:

$$\begin{gathered}
\exists m,M \ \ \forall x \in [a,b]: m\leq f(x)\leq M\\
Teza: m(b-a)\leq \int^{b}_{a}{f(x) \ dx}\leq M(b-a)
\end{gathered}$$

Oblicz wartość średnią funkcji $f(x)=arctan{x}$ na przedziale $[0,\sqrt{3}]$

$$\begin{gathered}
\int{\arctan{x}}=x\arctan{x}-\int{\frac{x}{x^2+1}}=\begin{vmatrix}
t=x^2+1\\
dt=2x\ dx
\end{vmatrix}=\\
=x\arctan{x}-\frac{1}{2}\int{\frac{1}{t}\ dt}=x\arctan{x}-\frac{1}{2}\ln{(x^2+1)}\\\\
\frac{\frac{\pi}{3}\sqrt{3}-\frac{1}{2}ln(4)}{\sqrt{3}}=\frac{\pi}{3}-\frac{\ln{(4)}}{2\sqrt{3}}
\end{gathered}$$
---

### $II$ Termin 

###### 1. Wyznacz wszystkie asymptoty funkcji $f(x)=\frac{x}{x+2\sqrt{x^2-3}}$

$$\begin{gathered}
x+2\sqrt{x^2-3}=0\\
2\sqrt{x^2-3}=-x\\
4x^2-12=x^2\\
x^2=4\\
x=-2\\
\lim_{x\to -2^-}{\frac{x}{x+2\sqrt{x^2-3}}}=\frac{-2}{0^+}=-\infty\\
\lim_{x\to -2^+}{\frac{x}{x+2\sqrt{x^2-3}}}=\frac{-2}{0^-}=\infty\\
\lim_{x\to \infty}{\frac{x}{x+2\sqrt{x^2-3}}}=
\lim_{x\to \infty}{\frac{1}{1+2\sqrt{1-\frac{3}{x^2}}}}=\frac{1}{3}\\
\lim_{x\to \infty}{\frac{1}{1+2\sqrt{1-\frac{3}{x^2}}}}=\frac{1}{3}\\
\lim_{x\to -\infty}{\frac{1}{1+2\sqrt{1-\frac{3}{x^2}}}}=\frac{1}{3}\\
x=-2\\
y=\frac{1}{3}
\end{gathered}$$

---
###### 2. Znajdź wymiary największego prostokąta wpisanego w elipse $\frac{x^2}{16}+\frac{y^2}{9}=1$

$$\begin{gathered}
y^2=9-\frac{9}{16}x^2\\
y=\sqrt{9-\frac{9}{16}x^2}\\\\
a=2x,b=2y\\
P=ab=4xy\\
P_{cw}=x\cdot \sqrt{9-\frac{9}{16}x^2}\\
P'_{cw}=\sqrt{9-\frac{9}{16}x^2}+\frac{-9x^2}{16\sqrt{9-\frac{9}{16}x^2}}\\\

\sqrt{9-\frac{9}{16}x^2}+\frac{-9x^2}{16\sqrt{9-\frac{9}{16}x^2}}=0\\
\frac{144-9x^2}{16\sqrt{9-\frac{9}{16}x^2}}+\frac{-9x^2}{16\sqrt{9-\frac{9}{16}x^2}}=0\\
144-18x^2=0\\
x^2=\frac{144}{18}=8\\
x=2\sqrt{2}\\\\
Wymiary:\\
a=2\cdot x=4\sqrt{2}\\
b=2\cdot \sqrt{9-\frac{9}{2}}=\sqrt{18}=3\sqrt{2}
\end{gathered}$$

---
###### 3. Oblicz całke:

$$\begin{gathered}
\int^{\infty}_{3}{\frac{1}{(x-1)^3\sqrt{x^2-2x-1}}\ dx}=\begin{vmatrix}
u=x-1\\
du=dx
\end{vmatrix}=\int^{\infty}_{2}{\frac{1}{u^3\sqrt{u^2-2}}}=\begin{vmatrix}
t=u^2-2\\
dt=2u\ du
\end{vmatrix}=\\\\
=\int^{\infty}_{2}{\frac{1}{2(t+2)^2\sqrt{t}}\ dt}=\frac{1}{2}\int^{\infty}_{2}{\frac{1}{(t^2+4t+4)\sqrt{t}}\ dt}=\begin{vmatrix}
k=\sqrt{t}\\
dk=\frac{1}{2k}\ dt\\
dt=2k\ dk
\end{vmatrix}=
\\=\int^{\infty}_{\sqrt{2}}{\frac{1}{k^6+4k^4+4k^2}\ dk}=\int^{\infty}_{\sqrt{2}}{\frac{1}{k^2(k^2+2)^2}\ dk}=\begin{vmatrix}
v=\frac{1}{k}\\
dv=-\frac{1}{k^2}\ dk
\end{vmatrix}
\end{gathered}$$
**DOKOŃCZ**

###### 4. Oblicz pole powierzchni bryły powstałej z obrotu jednego łuku cykloidy dookoła osi OX

$$\begin{gathered}
\left\{
\begin{matrix}
x=a(t-\sin{t})\\
y=a(1-\cos{t})
\end{matrix}
\right.
\end{gathered}$$

$$\begin{gathered}
|P|=2\pi a^2 \int^{2\pi}_{0}{(1-\cos{t})\cdot \sqrt{(1-\cos{t})^2+\sin^2{t}}}=
\\=2\sqrt{2}\pi a^2\int^{2\pi}_{0}{(1-\cos{t})\sqrt{1-\cos{t}}}=\begin{vmatrix}
\sin{\frac{t}{2}}=\frac{1-\cos{t}}{2}
\end{vmatrix}=\\
=8\pi a^2\int^{2\pi}_{0}{(\sin{\frac{t}{2}})^\frac{3}{2}}=

\end{gathered}$$

Chuj wie jak to dokończyć

---
###### 1. Podaj twierdzenie Rolle'a

Zał: funkcja ciągła w $[a,b]$
jeżeli funkcja przyjmuje te same wartości na a i b to ma gdzieś pochodną równą 0 (istnieje takie c należące do $[a,b]$ że $f'(c)=0$)

###### wykaż że równanie $x^3-3x+c=0$ nie może mieć dwóch różnych pierwiastków w przedziale $[0,1]$

$$\begin{gathered}
f(x)=x^3-3x+c\\
f'(x)=3x^2-3\\
f'(x)\gt 0 \Leftrightarrow x\gt 1 \vee x\lt -1\\
f'(x)\lt 0 \Leftrightarrow x\in [-1,1]\\\\
[0,1]\subset [-1,1]\\\\
\text{Funkcja jedynie maleje w tym przedziale, może mieć co najwyżej jeden pierwiastek}
\end{gathered}$$

---
###### Sprawdź dla jakich x

$$\begin{gathered}
2\arctan{x}+\arcsin{\frac{2x}{1+x^2}}=\pi \\
\sin{2\phi}=\frac{2\sin{\phi}\cos{\phi}}{\sin^2{\phi}+\cos^2{\phi}}=\frac{2\frac{\sin}{\cos}}{\frac{\sin^2}{\cos^2}+1}=\frac{2\tan{\phi}}{\tan^2{\phi}+1}\\
\text{Więc jeżeli:}\\
\phi = \arctan{x}\\
2\phi+2\phi =\pi \\
\phi = \frac{\pi}{4}\\
\frac{\pi}{4}=\arctan{x}\\
x=1
\end{gathered}$$

---
###### 3. Pokaż, że: $\frac{2}{e}\leq \int^{2}_{0}{e^{x^2-2x}\ dx}\leq 2$

Na podstawie $I$ twierdzenia o wartości średniej rachunku całkowego, mówiącego że:

$$\begin{gathered}
Z: f\ \text{Ciągła w }[a,b]\\
\exists M,m: m\leq f(x)\leq M, \forall x \in [a,b]:\\
m(b-a)\leq \int^{b}_{a}{f(x)\ dx}\leq M(b-a)
\end{gathered}$$
$$\begin{gathered}
f(x)=e^{x^2-2x}\\
f'(x)=e^{x^2-2x}\cdot (2x-2)\\
f'(x)\gt 0\Leftrightarrow x\gt 1\\
f'(x)\lt 0\Leftrightarrow x\lt 1\\
f(1)=e^{1-2}=\frac{1}{e}\\
f(0)=1\\
f(2)=1\\
m=\frac{1}{e}, \ M=1\\
m(2-0)\leq \int^{2}_{0}{e^{x^2-2x}\ dx}, M(2-0)\\
\frac{2}{e}\leq \int^{2}_{0}{e^{x^2-2x}\ dx}\leq 2\checkmark 
\end{gathered}$$

A funkcja $e^{x^2-2x}$ jest ciągła ponieważ $e^x$ oraz $x^2-2x$ są funkcjami elementarnymi, a ich złożenie jest ciągłe.

---
###### Wyznacz funkcję $\phi(x)=\int^{x}_{-\infty}{f(t)\ dt}$, jeśli:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{4}{x^2+2x+4}, x \leq 0\\
e^{-\sqrt{x}}, x \gt 0 
\end{matrix}
\right.
\end{gathered}$$
Czy funkcja $\phi(x)$ jest funkcją pierwotną funkcji f? Odpowiedź uzasadnij.

$$\begin{gathered}
dla \ x \leq 0\\
\phi(x)=4\int^{x}_{-\infty}{\frac{1}{x^2+2x+4}}=4\int^{x}_{-\infty}{\frac{1}{(x+1)^2+3}}=\begin{vmatrix}
t=x+1\\
dt = dx
\end{vmatrix}=\\
=4\int^{x+1}_{-\infty}{\frac{1}{t^2+3}}=4\int^{x+1}_{-\infty}{\frac{1}{3(\frac{t}{\sqrt{3}})^2+3}}=\frac{4}{3}\int^{x+1}_{-\infty}{\frac{1}{(\frac{t}{\sqrt{3}})^2+1}}=\begin{vmatrix}
u=\frac{t}{\sqrt{3}}\\
du=\frac{1}{\sqrt{3}}dt
\end{vmatrix}=\\
=\frac{4}{\sqrt{3}}\int^{\frac{x+1}{\sqrt{3}}}_{-\infty}{\frac{1}{u^2+1}\ du}=\frac{4}{\sqrt{3}}(\arctan{\frac{x+1}{\sqrt{3}}}+\frac{\pi}{2})\\\\
dla \ x\gt 0\\
\phi(x)=\int^{x}_{0}{e^{-\sqrt{x}}\ dx}+\int^{0}_{-\infty}=\frac{2\pi}{\sqrt{3}}+\int^{x}_{0}{e^{-\sqrt{x}}\ dx}=\\\\
\int{e^{-\sqrt{x}}\ dx}=\begin{vmatrix}
u^2=x\\
dx=2u \ du
\end{vmatrix}=\int{e^{-u}\cdot 2u\ du}=\begin{vmatrix}
v'=e^{-u}&h=2u\\
v=-e^{-u}&h'=2
\end{vmatrix}=\\=-2ue^{-u}-2e^{-u}=e^{-u}(-2u-2)=e^{-\sqrt{x}}(-2\sqrt{x}-2)\\\\
\phi(x)=e^{-\sqrt{x}}(-2\sqrt{x}-2)+2+\frac{2\pi}{\sqrt{3}}
\end{gathered}$$

Dla $x\lt 0$ i dla $x\gt 0$ pochodne tej funkcji są równe tamtej funkcji więc git. Teraz pytanie czy ta funkcja jest ciągła.

$$\begin{gathered}
\lim_{x\to 0^-}{\phi(x)}=\frac{2\pi}{\sqrt{3}}\\
\lim_{x\to 0^+}{\phi(x)}=1(-2)+2+\frac{2\pi}{\sqrt{3}}=\frac{2\pi}{\sqrt{3}}\\
\checkmark 
\end{gathered}$$

---
###### Podaj wypowiedź twierdzenia Newtona-Leibniza i dowód tego twierdzenia:

Jeśli f(x) ciągła na $[a,b]$
$$\begin{gathered}
F(x)=\int{f(x) \ dx}\\
\int^{b}_{a}{f(x)\ dx}=F(b)-F(a)
\end{gathered}$$
gdzie F(x) to **DOWOLNA** funkcja pierwotna funkcji $f$ na tym przedziale.

Dowód:
$$\begin{gathered}
\int^{b}_{a}{f(x)\ dx}=\phi(b)=\phi(b)-\int^{a}_{a}{f(x)\ dx}=\phi(b)-\phi(a)=F(b)-F(a)
\end{gathered}$$

---
### 2013/2014

###### 1. Zbadaj przebieg zmienności funkcji $f(x)=x\cdot e^{\frac{1}{x}}$

$$\begin{gathered}
f(-x)=-x\cdot e^{-x}\neq f(x), - \ nie \ jest \ symetryczna, nie \ jest \ niesymetryczna\\
\ nie \ jest \ okresowa\\

D: x\neq 0\\
f'(x)=e^{\frac{1}{x}}+e^{\frac{1}{x}}\cdot -\frac{1}{x}=e^{\frac{1}{x}}(1-\frac{1}{x})\\
f'(x)\gt 0 \Leftrightarrow 1-\frac{1}{x}\gt 0\\
1-\frac{1}{x}\gt 0\\
x^2-x\gt 0\\
x(x-1)\gt 0\\
x\gt 1\vee x\lt0\\\\
f'(x)\lt 0\\
1-\frac{1}{x}\lt 0\\
x^2-x\lt 0\\
x(x-1)\lt 0\\
x\in (0,1)\\\\
f'(x)=0 \Leftrightarrow x=1\\\\
f(1)=e\\
\lim_{x\to 0^+}{f(x)}=\lim_{x\to 0^+}{x\cdot e^{\frac{1}{x}}}=
\lim_{x\to 0^+}{\frac{e^{\frac{1}{x}}}{\frac{1}{x}}}=
\lim_{x\to 0^+}{\frac{e^{\frac{1}{x}}\cdot -\frac1{x^2}}{-\frac{1}{x^2}}}=\lim_{x\to \infty}{e^x}=\infty
\end{gathered}$$
Punkty przecięcia z osiami:
$$\begin{gathered}
f(x)=0 \Leftrightarrow x\cdot e^{\frac{1}{x}}=0\implies x=0\notin \mathbb{D}\\
f(0)=\infty 
\end{gathered}
$$
Nie ma przecięć

Asymptoty

$$\begin{gathered}
\lim_{x\to \infty}{f(x)}=\lim_{x\to \infty}{x\cdot e^{\frac{1}{x}}}=\infty \\
\lim_{x\to -\infty}{f(x)}=\lim_{x\to -\infty}{x\cdot e^{\frac{1}{x}}}=-\infty \\
a=\lim_{x\to \infty}{\frac{f(x)}{x}}=\lim_{x\to \infty}{e^{\frac{1}{x}}}=1\\
b=\lim_{x\to \infty}{f(x)-ax}=
\lim_{x\to \infty}{x\cdot e^{\frac{1}{x}}-x}=

\lim_{x\to \infty}{x\cdot (e^{\frac{1}{x}}-1)}=
\lim_{x\to \infty}{\frac{(e^{\frac{1}{x}}-1)}{\frac{1}{x}}}=1\\\\
Zatem \ asymptoty: y=x+1\\
x=0\\
\end{gathered}$$
Druga pochodna
$$\begin{gathered}
f'(x)=e^{\frac{1}{x}}(1-\frac{1}{x})\\
f''(x)=e^{\frac{1}{x}}\cdot \frac{1}{x^2}+e^{\frac{1}{x}}\cdot -\frac{1}{x^2}(1-\frac{1}{x})=e^{\frac{1}{x}}(\frac{1}{x^3})\\\\
f''(x)\gt 0 \Leftrightarrow x\gt 0\\
f''(x)\lt 0 \Leftrightarrow x\lt 0\\
f''(x)\neq 0 \forall x\in D
\end{gathered}$$
---
###### 2. Korzystając z twierdzenia Taylora oblicz $\sin{(18\degree)}$ z dokładnością do $0.001$.

$$\begin{gathered}
\sin{x}=0+\frac{1}{1!}\cdot x-\frac{1}{3!}x^3+\frac{1}{5!}x^5-\frac{1}{7!}x^7+R_8(0,x)\\
18\degree = \frac{\pi}{10}\\
\sin{\frac{\pi}{10}}=0.3141592-0.0015=0.309\\
\end{gathered}$$
---
###### 4. Narysuj spirale daną wzorem $r(\phi)=\frac{1}{\phi}$. Oblicz długość spirali $[\frac{3}{4},\frac{4}{3}]$
$$\begin{gathered}
|L|=\pi \int^{\frac{4}{3}}_{\frac{3}{4}}{\sqrt{\frac{1}{\phi^2}-\frac{1}{\phi^4}}}=\pi \int^{\frac{4}{3}}_{\frac{3}{4}}{\sqrt{\frac{\phi^2-1}{\phi^4}}}=
\pi \int^{\frac{4}{3}}_{\frac{3}{4}}{\frac{\sqrt{\phi^2-1}}{\phi^2}}=\begin{vmatrix}
u=\phi^2-1\\
du=2\phi \ d\phi
\end{vmatrix}=\\
=\int{\frac{\sqrt{u}}{u+1}}=\begin{vmatrix}
a=\sqrt{u}\\
u=a^2\\
du=2a\ da
\end{vmatrix}=\int{\frac{2a^2}{a^2+1}}=2\int{1-\frac{1}{a^2+1}}=2a-2\arctan{a}\\\\\
\end{gathered}$$
---
###### 1. Dla każdego z ciągów o wyrazach ogólnych $a_n=\frac{n}{n+1}\cos{\frac{n\pi}{2}}$ oraz $b_n=\frac{n}{1+3+5+\dots+(2n-1)}\cos{\frac{n\pi}{2}}$ oblicz jego granicę lub pokaż, że nie jest zbieżny. Gdy korzystasz z jakiegoś twierdzenia to podaj jego dokładną wypowiedź.

$$\begin{gathered}
\lim_{n\to \infty}{a_n}=
\lim_{n\to \infty}{\frac{n}{n+1}\cdot \cos{\frac{n\pi}{2}}}=\lim_{n\to \infty }{\cos{\frac{n\pi}{2}}}\\
\lim_{k\to \infty}{a_{4k}}=1\\
\lim_{k\to \infty}{a_{4k+1}}=0\\
\text{Podciągi są różne, więc ciąg nie jest zbieżny.}
\end{gathered}$$
$$\begin{gathered}
b_n=\frac{n}{1+3+5+\dots+(2n-1)}\cos{\frac{n\pi}{2}}=
\frac{n}{\frac{1+(2n-1)\cdot n}{2}=n^2}\cdot \cos{\frac{n\pi}{2}}=\frac{1}{n}\cdot \cos{\frac{n\pi}{2}}\\
\lim_{n\to \infty}{b_n}=0
\end{gathered}$$

---
###### 2. Podaj wypowiedź twierdzenia Lagrange'a 


Jeżeli funkcja różniczkowalna w (a,b) to istnieje w tym przedziale takie c które jest ilorazem przyrostu wartości funkcji od b do a, z przyrostem b do a.
Założenia:
1. $f \in C([a,b])$
2. $f \in D((a,b))$
Teza:
$\exists c \in (a,b) \ f'(c) = \frac{f(b)-f(a)}{b-a}=\frac{f\Delta_{a\to b}}{\Delta_{a\to b}}$

###### Sprawdź czy funkcja $f(x)=x+|\sin{x}|$ spełnia założenia tw. Lagrange'a na przedziale $[-\frac{\pi}{2}, \frac{\pi}{2}]$ jeśli tak to wyznacz punkt z tezy tego twierdzenia.

1) Jest ciągła bo składa się z funkcji elementarnych
2) Czy jest różniczkowalna w tym przedziale?

$$\begin{gathered}
f(x)=x+|\sin{x}|, 
\ \ \ \ \ \ f(x)=\left\{
\begin{matrix}
x+\sin{x}, x\in (0,\frac{\pi}{2}]\\
x-\sin{x}, x\in (-\frac{\pi}{2}, 0]
\end{matrix}
\right.\\\\
f'(x)=\left\{
\begin{matrix}
1+\cos{x}, x \in (0,\frac{\pi}{2}]\\
1-\cos{x}, x \in (-\frac{\pi}{2}, 0]
\end{matrix}
\right.\\\\
\lim_{x\to 0^-}{f'(x)}=0\\
\lim_{x\to 0^+}{f'(x)}=2\\
\end{gathered}$$

Pochodna nie istnieje w punkcie x=0 zatem nie jest różniczkowalna w całym przedziale, więc nie spełnia założen tw. lagrange.

---
$$\begin{gathered}
\int{\frac{\arctan{x}}{x^4}}=\begin{vmatrix}
u=\arctan{x}&u'=\frac{1}{x^2+1}\\
v'=\frac{1}{x^4}&v=-\frac{1}{3x^3}
\end{vmatrix}=arctan{x}\cdot -\frac{1}{3x^3}+\frac{1}{3}\int{\frac{1}{x^3(x^2+1)}}\\\\\\
\frac{1}{x^3(x^2+1)}=\frac{A}{x}+\frac{B}{x^2}+\frac{C}{x^3}+\frac{Dx+E}{x^2+1}\\
1=A(x^4+x^2)+B(x^3+x)+C(x^2+1)+D(x^4)+Ex^3\\
1=Ax^4+Ax^2+Bx^3+Bx+Cx^2+C+Dx^4+Ex^3\\
1=x^4(A+D)+x^3(B+E)+x^2(A+C)+x(B)+C\\
\left\{
\begin{matrix}
C=1\\
A=-1\\
D=1\\
B=0\\
E=0
\end{matrix}
\right.\\\\
=-\frac{\arctan{x}}{3x^3}+\frac{1}{3}\int{\frac{-1}{x}+\frac{1}{x^3}+\frac{x}{x^2+1}}
\end{gathered}$$
---
###### Podaj definicję minimum lokalnego funkcji w punkcie oraz twierdzenie wykorzystujące drugą pochodną będące warunkiem wystarczającym na istnienie minimum lokalnego w punkcie.

Def. minimum lokalnego.
Niech $f: D\to \mathbb{R}$, mówimy że $f$ ma minimum lokalne w $x_0\in D$ wtedy kiedy $\forall x \in U(x_0)$ $f(x)\geq f(x_0)$.

Warunek wystarczający
jeżeli $f''(x_0)\gt 0 \land f'(x_0)=0$ to jest to minimum lokalne. Jeżeli $f''(x_0)=0$ konieczne są dalsze pochodne do testu.

Dowód:
$$\begin{gathered}
f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{1}{2}f''(x_0)(x-x_0)^2\dots \\\\
f'(x_0)=0\\\\
f(x)=f(x_0)+\frac{1}{2}f''(x_0)(x-x_0)^2\\
f(x)\gt f(x_0)\Leftrightarrow f''(x_0)\gt 0
\end{gathered}$$
---
###### 3. Wyznaczyć funkcję $\phi(x)=\int^{x}_{-1}{f(t)\ dt}$ jeśli:
$$\begin{gathered}
f(x)=\left\{
\begin{matrix}
\frac{4x+5}{\sqrt{1-2x-x^2}}, -1\leq x\leq 0\\
\frac{\sin^3{x}}{\sqrt{\cos^2{x}+2\cos{x}+5}}, x\gt 0
\end{matrix}
\right.\\\\
\int{\frac{\sin^3{x}}{\sqrt{\cos^2{x}+2\cos{x}+5}}\ dx}=\begin{vmatrix}
u=\cos{x}\\
du=-\sin{x}\ dx
\end{vmatrix}=\int{\frac{-1+u^2}{\sqrt{u^2+2u+5}}\ du}=\\=
\int{\frac{(u-1)(u+1)}{\sqrt{(u+1)^2+4}}\ du}=
\int{\frac{(u-1)(u+1)}{2\sqrt{(\frac{u+1}{2})^2+1}}\ du}=
\begin{vmatrix}
k=\frac{u+1}{2}\\
dk=\frac{1}{2}\ du
\end{vmatrix}=\\\\
=\int{\frac{4k^2-4k}{\sqrt{k^2+1}}\ dk}=\begin{vmatrix}
\sqrt{k^2+1}=t-k\sqrt{1}\\
k^2+1=t^2-2tk+k^2\\
1=t^2-2tk\\
2tk=t^2-1\\
k=\frac{t^2-1}{2t}\\
dk=\frac{t^2+1}{2t^2}
\end{vmatrix}=
\end{gathered}$$

$$\begin{gathered}
\int{\frac{\frac{t^4-2t^2+1}{t^2}-2\frac{t^2-1}{t}}{t-\frac{t^2-1}{2t}}
\frac{t^2+1}{2t^2}\ dk}=\int{\frac{\frac{t^4-2t^2+1-2t^3+2t}{t^2}}{\frac{t^2+1}{2t}}\frac{t^2+1}{2t^2}\ dt}=\\=
\int{(t^4-2t^3-2t^2+2t+1)\cdot \frac{2t}{t^2+1}\cdot \frac{t^2+1}{2t^2}\ dt}=\\\\
=\int{(t^3-2t^2-2t+2+\frac{1}{t})}=\frac{t^4}{4}-2\frac{t^3}{3}-t^2+2t+\ln{t}=\\=
\frac{(\sqrt{(\frac{u+1}{2})^2+1}+(\frac{u+1}{2}))^4}{4}-2\frac{(\sqrt{(\frac{u+1}{2})^2+1}+(\frac{u+1}{2}))^3}{3}-\\-(\sqrt{(\frac{u+1}{2})^2+1}+(\frac{u+1}{2}))^2+2t+\ln{(\sqrt{(\frac{u+1}{2})^2+1}+(\frac{u+1}{2}))}=\\\\
=\frac{(\sqrt{(\frac{\cos{x}+1}{2})^2+1}+(\frac{\cos{x}+1}{2}))^4}{4}-2\frac{(\sqrt{(\frac{\cos{x}+1}{2})^2+1}+(\frac{\cos{x}+1}{2}))^3}{3}-\\-(\sqrt{(\frac{\cos{x}+1}{2})^2+1}+(\frac{\cos{x}+1}{2}))^2+2t+\ln{(\sqrt{(\frac{u+1}{2})^2+1}+(\frac{\cos{x}+1}{2}))}=
\end{gathered}$$

---
