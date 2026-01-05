
## Metoda różnic skończonych

### Aproksymacja pochodnych pierwszego rzędu

Dla przypomnienia:

$$\begin{gathered}
f'(x)=\lim_{h \to 0}{\frac{f(x+h)-f(x)}{h}} \overset{ozn}{=}f'_p(x)
\end{gathered}$$
nazywamy to **różnicą prawostronną**

**lewostronna wygląda analogicznie tak jak brzmi:**

$$\begin{gathered}
f'(x)=\lim_{h \to 0}{\frac{f(x)-f(x-h)}{h}}
\overset{ozn}{=}f'_l(x)
\end{gathered}$$

można założyć przyjęcie małego $h$ żeby pozbyć się granic a wprowadzić aproksymacje, przejdźmy do **różnicy centralnej**:

$$\begin{gathered}
f'(x)\approx\frac{f'_p(x)+f'_l(x)}{2h}=\frac{f(x+h)-f(x-h)}{2h}\overset{ozn}{=}f'_c(x)
\end{gathered}$$

**Różnica centralna szybicej zmniejsza nam wartość błędu** - dla jednostronnych mamy $O(h)$ czyli dla zmniejszenia wartości $h$ np. dwukrotnie zmniejszamy również błąd dwukrotnie, w przypadku centralnej mamy już $O(h^2)$

### Aproksymacja pochodnych rzędu drugiego:

Korzystając z najdokładniejszej aproksymacji z poprzednich czyli z różnicy centralnej możemy zaproksymować pochodną drugiego rzędu (również w sposób **centralny**):

Przyjmując to samo przybliżenie $h$ dla pierwszego i drugiego rzędu (tutaj oznaczone jako $m$) mamy:

$$\begin{gathered}
f''(x)\approx\frac{f'(x+m)-f'(x-m)}{2m}\approx\\
\approx \frac{\frac{f(x+m+m)-f(x+m-m)}{2m}-\frac{f(x-m+m)-f(x-m-m)}{2m}}{2m}=\\\\
=\frac{f(x+2m)-f(x-2m)-2f(x)}{4m^2}=\begin{vmatrix}
2m=h
\end{vmatrix}=\\=\frac{f(x+h)-2f(x)+f(x-h)}{h^2}
\end{gathered}$$

### Równanie konwekcji-dyfuzjii?

$$\begin{gathered}
cu'(x)-u''(x)=f(x)&(1)&\Omega=[0,1]&u(0)=0&u(1)=0\\\\
\end{gathered}$$
Wprowadzamy nową funkcje $w$ taką że $w(0)=0$ oraz $w(1)=0$ 
Przyjmijmy teraz że $u=w+\overline{u}$ gdzie możemy np. przyjąć:  $\overline{u}(x)=x$ 

Zatem pochodne:
$$\begin{gathered}
\overline{u}'(x)=1\\
\downarrow\\
u'=w'+1\\\\
\overline{u}''(x)=0\\
\downarrow\\
u''=w''\\\\
\end{gathered}$$
Podstawiając adekwatne do równania $(1)$:
$$\begin{gathered}
c(w'+1)-w''=f&\Omega=[0,1]&w(0)=0&w(1)=0
\end{gathered}$$

korzystając z naszych aproksymacji pochodnych:
$$\begin{gathered}
c \frac{w(x+h)-w(x-h)}{2h}+c-\frac{w(x+h)-2w(x)+w(x-h)}{h^2}=f(x)
\end{gathered}$$

Przerzućmy c na prawo:
$$\begin{gathered}
c \frac{w(x+h)-w(x-h)}{2h}-\frac{w(x+h)-2w(x)+w(x-h)}{h^2}=f(x)-c
\end{gathered}$$
I pogrupujmy człony w naszym równaniu:
$$\begin{gathered}
w(x-h) \left[-\frac{c}{2h}-\frac{1}{h^2}\right]+w(x) \left[\frac{2}{h^2}\right]+w(x+h)\left[\frac{c}{2h}-\frac{1}{h^2}\right]=f(x)-c\ (2)
\end{gathered}$$

Mając przedział $[0,1]$ można go podzielić na równe $n$ kawałków, to znaczy:
$$\begin{gathered}
\ [0,1]=\bigcup_{i=0}^{n-1} \left[\frac{i}{n}, \frac{i+1}{n}\right]=
\bigcup_{i=0}^{n-1} \left[x_i, x_{i+1}\right]
\end{gathered}$$
oraz zakładając że nasza aproksymacja $h=\frac{1}{n}$ oznacza to że:
$$\begin{gathered}
x_{i-1}+h=x_i\\
x_i+h=x_{i+1}
\end{gathered}$$

podstawiając teraz kolejno $x_0,x_1,\dots,x_n$:

możemy założyć że prawdziwym jest:
$$\begin{gathered}
cw'(x_i)+c+w''(x_i)=f(x_i)
\end{gathered}$$
co można ubrać w równaniu drugim jako:
$$\begin{gathered}
w(x_{i-1}) \left[-\frac{c}{2h}-\frac{1}{h^2}\right]+w(x_i) \left[\frac{2}{h^2}\right]+w(x_{i+1})\left[\frac{c}{2h}-\frac{1}{h^2}\right]=f(x_i)-c
\end{gathered}$$

jeśli sie przyjrzymy temu co dostaliśmy to mamy układ równań $n+1$ równań liniowych o $n+1$ niewiadomych - taki układ można rozwiązać przy pomocy algorytmów np eliminacji Gaussa.

Powyższe można rozciągnąć na to co było w rurach 6 z pochodnymi dystrybucyjnymi przy wielowymiarowej funkcji...


