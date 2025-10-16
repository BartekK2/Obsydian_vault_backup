##### Lekcja: [[Analiza - 2]]
#analiza  #indukcja #arcusy  #granica_funkcji 
###### 2024-10-12

###### 1. Udowodnij tezę $133| 11^{n+2}+12^{2n+1}$
dla $n=0$:
$133| 11^2+12^1 = 133$ :LiCheck:
Z: $133|11^{k+2}+12^{2k+1}, \ k \in \mathbb{N} \implies 11^{k+2}+12^{2k+1}=133a, \ a \in \mathbb{Z}$
T: 
$$\begin{gathered}
133|11^{k+3}+12^{2(k+1)+1}\\ \downarrow \\
133|11^{k+3}+12^{2k+3} \\ \downarrow \\
133|11^{k+2}\cdot11+12^2\cdot (133a-11^{k+2}) \\ \downarrow \\
133|12^2\cdot133a + (-144+11)\cdot 11^{k+2} \\ \downarrow \\
133|133(12^2\cdot a - 11^{k+2})
\end{gathered}$$ 
:LiCheck:

---
###### 2. Funkcja odwrotna od $f(x)=5x-1$ 
$$\begin{gathered}
y=5x-1\\
y+1=5x\\
\frac{y+1}{5}=x\\
f^{-1}(y) = \frac{y+1}{5}\\
f^{-1}(x)=\frac{x+1}{5}
\end{gathered}$$
###### 3. Sprawdź dziedzine funkcji $f(x)=\sqrt{\arccos{(log_{10}{(1-x)})}}$
$$\begin{gathered}
a(x)=log_{10}{(1-x)}, \ \mathbb{D}=(-\infty,1)\\
b(x)=\arccos{(x)}, \ \mathbb{D}=[-1,1]\\
c(x)=\sqrt{x}, \ \mathbb{D}=[0,+\infty) \\ \downarrow \\
f(x) = (c(x) \circ b(x)) \circ a(x), \mathbb{D} = ?\\
\\Z \ dziedziny \ \arccos{x}: \\\\
-1 \leq log_{10}{(1-x)} \leq 1\\
\frac{1}{10} \leq (1-x) \leq 1\\
x \geq 9 \ \land \ x \leq \frac{9}{10}\\
x \in [-9, \frac{9}{10}]\\
\\Z \ dziedziny \ \sqrt{x}: \\\\
\arccos{x} \geq 0, \ zawsze \ \geq \ 0

\end{gathered}$$
---
###### 4. Oblicz

- $$\begin{gathered}
\arccos{(-\frac{1}{2})}+arcctg(\tan{\frac{9\pi}{5}})+\sin{(\arcsin{\frac{\sqrt{3}}{2}})}+arcctg(-1)=\\
=\frac{2\pi}{3}+arcctg(\cot{\frac{\pi}{2}-\frac{9\pi}{5}})-\frac{\pi}{4}=...
\end{gathered}$$
- $$\begin{gathered}
\arccos{(-\frac{\sqrt{3}}{2})}+arcctg{(\cot{\frac{8\pi}{7}})}+sin{(\arcsin{-\frac{1}{2}})}+arcctg(-1)\\
\end{gathered}$$

---
##### Ćwiczenia 3
###### Na podstawie def. Couchyego wykaż że istnieje granica ciągu
$$\begin{gathered}
a_n = \frac{2}{\sqrt{n}}\\
lim_{n\to \infty} a_n =g \leftrightarrow \forall \epsilon \in \mathbb{R}: \epsilon \gt 0  \ \ \ \exists n_0 \in \mathbb{N}: \forall n>n_0 \ \ |a_n - g|<\epsilon\\
|\frac{2}{\sqrt{n}}-0|<\epsilon \\
\frac{|2|}{|\sqrt{n}|}\lt \epsilon \\
2 \lt \epsilon \cdot \sqrt{n}\\
\sqrt{n} \gt \frac{2}{\epsilon}\\
n \gt \frac{4}{\epsilon^2}\\
n_0 := \left\lceil{\frac{4}{\epsilon^2}}\right\rceil\\
n \gt n_0 \gt \frac{4}{\epsilon^2}
\end{gathered}$$

###### 9) Oblicz granicę ciągu:
###### a) 
$$\begin{gathered}
lim_{n \to \infty}a_n=\frac{1-2+3-4+5-6 ... -2n}{\sqrt{n^2+1}}\\
lim_{n \to \infty}a_n=\frac{-n}{\sqrt{n^2+1}}\\
lim_{n \to \infty}a_n=\frac{-n}{n\cdot \sqrt{1+\frac{1}{n^2}}}\\
lim_{n \to \infty}=-1
\end{gathered}$$
###### b)
$$\begin{gathered}
lim_{n\to \infty} b_n = \frac{4\cdot 3^{n+1}+2\cdot 4^n}{5\cdot 2^n + 4^{n+2}}\\
lim_{n\to \infty} b_n = \frac{12\cdot 3^{n}+2\cdot 4^n}{5\cdot 2^n + 16\cdot 4^{n}}\\
lim_{n\to \infty} b_n = \frac{4^n(12\cdot \frac{3}{4}^n +2)}{4^{n}(5\cdot \frac{2}{4}^n + 16)}\\
lim_{n\to \infty} b_n =\frac{2}{16}=\frac{1}{8}
\end{gathered}$$
###### c)
$$\begin{gathered}
c_n = \frac{\sqrt{n^2+5}-n}{\sqrt{n^2+2}-n}\\
lim_{n \to \infty} c_n = \frac{\sqrt{n^2+5}-n}{\sqrt{n^2+2}-n} \\
licznik=(\sqrt{n^2+5}-n)\cdot \frac{\sqrt{n^2+5}+n}{\sqrt{n^2+5}+n}=\frac{5}{\sqrt{n^2+5}+n}\\
mianownik=(\sqrt{n^2+2}-n)\cdot \frac{\sqrt{n^2+2}+n}{\sqrt{n^2+2}+n}=\frac{2}{\sqrt{n^2+2}+n}\\
lim_{n \to \infty} c_n = \frac{\frac{5}{\sqrt{n^2+5}+n}}{\frac{2}{\sqrt{n^2+2}+n}}=lim_{n \to \infty}\frac{5}{2} \cdot \frac{\sqrt{n^2+2}+n}{\sqrt{n^2+5}+n}\\
lim_{n \to \infty}=\frac{5}{2}\frac{n\cdot(\sqrt{1+\frac{2}{n^2}}+1)}{n\cdot(\sqrt{1+\frac{5}{n^2}}+1)}=\frac{5}{2}
\end{gathered}$$
Czyli symbol $\infty - \infty$ zamieniliśmy na sume $\infty + \infty$ żeby potem wyciągnąć n i skrócić ułamki.
###### d)
$$\begin{gathered}
d_n=n(\sqrt[3]{n^3+n}-n)\\

\end{gathered}$$
*DO DOMU - ROZSZERZENIE ZE WZORU* $A^3-B^3$

###### e)
$$\begin{gathered}
e_n = \sqrt[n]{\frac{(-1)^n}{n}+2n} \\ 
Z \ twierdzenia \ o \ 3 \ ciagach.\\
a_n=\sqrt[n]{-\frac{1}{n}+2n}\\
b_n=\sqrt[n]{\frac{1}{n}+2n}\\
a_n \leq e_n \leq b_n \implies e_n=lim_{n\to \infty}a_n = 1

\end{gathered}$$

###### f)
$$\begin{gathered}
f_n = \frac{1}{n^2+1}+\frac{2}{n^2+2}+...+\frac{n}{n^2+n}\\
ograniczamy:\\
a_n = \frac{1}{n^2+n}+\frac{2}{n^2+n}+...+\frac{n}{n^2+n}=\frac{n(n+1)}{2(n^2+n)}\\
c_n = \frac{1}{n^2}+\frac{2}{n^2}+...+\frac{n}{n^2}=\frac{n(n+1)}{2n^2}\\
a_n\leq f_n \leq c_n
\end{gathered}$$

###### g)
$$\begin{gathered}
g_n = (\frac{n+1}{n+2})^n \\
\lim_{n \to \infty} g_n  = \lim_{n \to \infty} (1+\frac{1}{-(n+2)})^n = \lim_{n \to \infty} [(1+\frac{1}{-(n+2)})^{n-2}]^a =\\= \lim_{n \to \infty} [(1+\frac{1}{-(n+2)})^{n-2}]^\frac{n}{-(n+2)}\\\\
gdzie \ dla \ kazdego \ a_n \ dla \ ktorego \ granica = \infty \\
\lim_{n \to \infty} (1+\frac{1}{a_n})^{a_n} = e \\\\
wiec \\
\lim_{n \to \infty} g_n = e^{-1} \ ( bo \frac{n}{-(n+2)} \ da \ nam \ -1 \ w \ potedze)
\end{gathered}$$

###### h)
$$\begin{gathered}
h_n = \frac{\ln{(2^n+e^n)}}{n}\\
\lim_{n \to \infty}{h_n} = \lim_{n \to \infty}{\frac{\ln{(2^n+e^n)}}{n}}:\\
\frac{\ln{(2^n+e^n)}}{n} = \ln{\sqrt[n]{2^n+e^n}}\\
wsadzamy \ limesa \ do \ funkcji \ \ln \\
\lim_{n \to \infty}{\sqrt[n]{2^n+e^n}} = e \\
bo \ z \ tw. \ 3 \ ciagow \\
\sqrt[n]{e^n} \leq \sqrt[n]{2^n+e^n} \leq \sqrt[n]{2 \cdot e^n}\\
zatem \ \lim_{n \to \infty} h_n = \ln{e} = 1
\end{gathered}$$

---
##### Zad 8
$$\begin{gathered}
a_n = \frac{2^n}{n!}\\
a_{n+1} \geq  a_n\\
\frac{2^n \cdot 2}{n! \cdot (n+1)} \leq \frac{2^n}{n!} \ /\cdot n!\\
\frac{2^n \cdot 2}{(n+1)} \leq 2^n \ /:2^n \\
\frac{2}{(n+1)} \leq 1, \forall n \in \mathbb{N}_{+}\\\\
Zatem \ ciag \ jest \ slabo \ malejacy.

\end{gathered}$$

Arytmetyka granic czy coś
$$\begin{gathered}
\lim_{n \to \infty} \sqrt[n]{\frac{1}{n}} \neq \sqrt[n]{\lim_{n \to \infty }{\frac{1}{n}}}\\
ale\\
\lim_{n \to \infty} (\frac{1}{n})^n = \lim_{n \to \infty} e^{\ln{(\frac{1}{n})^n}}=\lim_{n \to \infty} e^{n \cdot \ln{\frac{1}{n}}}=e^{\lim_{n \to \infty} n \ln{\frac{1}{n}}}
\end{gathered}$$

###### 11. Pokaż, że ciąg $a_n = (1+\frac{1}{n})^n$ jest rosnący.

$$\begin{gathered}
a_n=(1+\frac{1}{n})^n = (\frac{n+1}{n})^n\\
a_{n+1} = (\frac{n+2}{n+1})(\frac{n+2}{n+1})^n\\
\frac{a_{n+1}}{a_n} = \frac{(\frac{n+2}{n+1})^n (\frac{n+2}{n+1})}{(\frac{n+1}{n})^n}=(\frac{n^2+2n}{n^2+2n+1})^n(\frac{n+2}{n+1})=\\=(1-\frac{1}{n^2+2n+1})^n\cdot (\frac{n+2}{n+1})\\\\
z \ nierownosci \ bernoulliego:\\
(1+x)^n \geq 1+x\cdot n, \forall x: x \gt -1, n \in \mathbb{N}\\
mamy:\\
(1-\frac{1}{n^2+2n+1})^n \geq 1-\frac{n}{n^2+2n+1}(=)\frac{n^2+n+1}{n^2+2n+1}\\
podstawiajac:\\
\frac{a_{n+1}}{a_n} \geq \frac{n^2+n+1}{(n+1)^3}(n+2)=\frac{n^3+3n^2+3n+2}{n^3+3n^2+3n+1}\geq 1
\end{gathered}$$

###### 10. Udowodnij że $\forall n \in \mathbb{N}: (1+\frac{1}{n})^n \lt 3$

$$\begin{gathered}
a_n =(1+\frac{1}{n})^n=\sum_{k=0}^{n}\binom{n}{k}1^{n-k}(\frac{1}{n})^k=\sum_{k=0}^{n}\binom{n}{k}\frac{1}{n^k}=\sum_{k=0}^{n}\frac{n!}{k!\cdot (n-k)!}\frac{1}{n^k}\\
gdzie \ dla \ kazdego \ a :\\
\forall a \in \mathbb{R} \  \exists n | \  \forall k \gt n:  a^k \lt k!\\
\\
Zacznijmy \ najpierw \ od \ uwodonienia \ ze \ jest \ monotoniczny:\\
a_n =\sum_{k=0}^{n}\frac{1}{k!}\frac{n}{n}\frac{n-1}{n}...\frac{n-(k-1)}{n}=\sum_{k=0}^{n}\frac{1}{k!}\left(1-\frac{1}{n}\right)...\left(1-\frac{k-1}{n}\right)\\
Wiemy \ ze : \forall i \in \{1,2,...,(k-1)\}: \left(1-\frac{i}{n}\right)\lt\left(1-\frac{i}{n+1}\right) \\ oraz \ a_{n+1} \ ma \ jedno \
wyrazenie \ wiecej \ wiec \ jest \ rosnacy \\(granicy  \ szukamy \ dla\  n\to \infty)\\
Dla \ \forall k \in \{2,3,...,n\}: \frac{1}{k!}\lt \frac{1}{2^{k-1}} \\oraz\\
\frac{n(n-1)...(n-(k-1))}{n^k}\lt 1:\\
a_n\lt 1+\left(1+\frac{1}{2}+\frac{1}{2\cdot 2}+...+\frac{1}{2^{n-1}}\right)
\lt 1+\left(\frac{1-\frac{1}{2^n}}{1-\frac{1}{2}}\right)\lt 3-\frac{1}{2^{n-1}}\lt 3
\end{gathered}$$

**Inny ładniejszy sposób (z indukcją)**

$$\begin{gathered}
Jeżeli \ wezmiemy \ sobie \ cos \ takiego \ i \ to \ udowodnimy \ indukcyjnie:
\\\\
\left(1+\frac{1}{n}\right)^k\lt 1+\frac{k}{n}+\frac{k^2}{n^2}\\
1) \ k=1\\\\
\left(1+\frac{1}{n}\right)^1 \lt 1+\frac{1}{n}+\frac{1^2}{n^2}\\\\
2) zakladamy \ ze \ prawdziwe\\\\
3) \\
\left(1+\frac{1}{n}\right)^{k+1}\lt \left(1+\frac{k}{n}+\frac{k^2}{n^2}\right)\left(1+\frac{1}{n}\right)\\
\left(1+\frac{1}{n}\right)^{k+1}\lt 1+\frac{1}{n}+\frac{k}{n}+\frac{k}{n^2}+\frac{k^2}{n^2}+\frac{k^2}{n^3}\\
\left(1+\frac{1}{n}\right)^{k+1}\lt 1+\frac{k+1}{n}+\frac{k^2+k}{n^2}+\frac{k^2}{n^3}\\
\left(1+\frac{1}{n}\right)^{k+1}\lt 1+\frac{k+1}{n}+\frac{(k+1)^2}{n^2}+\frac{k(k-n)-n}{n^3}\\
gdzie \ dla \ k\leq n : \frac{k(k-n)-n}{n^3}\lt 0\\
wiec \ prawdziwe\\
w \ szczegolnosci \ dla \ n=k:\\
\left(1+\frac{1}{n}\right)^k\lt 1+\frac{k}{n}+\frac{k^2}{n^2}\\
\left(1+\frac{1}{n}\right)^n \lt 1+\frac{n}{n}+\frac{n^2}{n^2}=3
\end{gathered}$$

###### 12. Oblicz granicę ciągu rekurencyjnego: $a1 = 2, \ a_{n+1} = \frac{a_n}{1+a_n}$ . Wsk. Wyznacz wzór jawny na an i udowodnij metodą indukcji jego poprawność
$$\begin{gathered}
Test:\\
a_1=2, a_2=\frac{2}{3}, a_3=\frac{2}{5}, a_4=\frac{2}{7}\\
Zakladam \ ze \ a_n=\frac{2}{1+2\cdot(n-1)}\\
1) n=1, a_1=\frac{2}{1+0}=2\\\\
2) zakladam\\\\
3) a_{n+1}=\frac{a_n}{1+a_n}=\frac{\frac{2}{1+2\cdot(n-1)}}{1+\frac{2}{1+2\cdot(n-1)}}=\frac{\frac{2}{1+2\cdot(n-1)}}{\frac{2+1+2\cdot(n-1)}{1+2\cdot(n-1)}}=\frac{2}{3+2\cdot(n-1)}=\frac{2}{1+2+2\cdot(n-1)}=\\=\frac{2}{1+2\cdot n} \ TAK
\end{gathered}
$$

###### 13. Pokaż, że ciąg rekurencyjny: $a_1 = \frac{1}{4} , a_{n+1} = \frac{1}{4} + \frac{1}{2} a_n^2$ jest zbieżny i oblicz jego granicę.


$$\begin{gathered}
Zakladajac \ ze \ granica \ istnieje:\\

\lim_{n \to \infty}a_n=L=\frac{1}{4}+\frac{1}{2}L^2\\
2L^2-4L+1=0\\
\Delta=16-8=2\sqrt{2}\\
L=\frac{4+2\sqrt{2}}{4} \ \vee \ L=\frac{4-2\sqrt{2}}{4}\\
\\
Wiemy \ ze \ jest \ ograniczony \ od \ dolu \ bo \ kazdy \ wyraz \ ciagu \ jest \\
rowny \ badz \ wiekszy \ od \frac{1}{4}\\
A \ od \ gory \ przez \ granice \ jesli \ zbiezny\\

a_{n+1}-a_n=\frac{1}{4} + \frac{1}{2} a_n^2-a_n \gt 0 \Leftrightarrow\\

2x^2-4x+1\gt 0\\
\Delta=2\sqrt{2}\\
x_1=\frac{4+2\sqrt{2}}{4} \ \vee \ x_2=\frac{4-2\sqrt{2}}{4}\\
x \in (-\infty, \frac{4-2\sqrt{2}}{4}) \cup (\frac{4+2\sqrt{2}}{4}, +\infty)\\
Poczatkowe \ wyrazy \ zawieraja \ sie \ w \ tym \ przedziale \ wiec \ rosnacy.
\end{gathered}
$$
Zjebane to rozwiązanie znajdź lepsze od kogoś.

###### 14. Pokaż, że ciąg rekurencyjny: $a_1=2, a_{n+1}=\frac{1}{2}(a_n+\frac{1}{a_n})$ jest zbieżny i oblicz jego granicę.

$$\begin{gathered}
Ograniczenie:\\
Dolne:(\frac{1}{2})\\
Indukcja:\\
1) n=1, a_1=2\\
2) a_n\geq 1\\
3) a_{n+1}=\frac{1}{2}(a_n+\frac{1}{a_n})\\
Skoro \ a_n \geq 1, \frac{1}{a_n} \geq 0:\\
A \ srednia \ arytmetyczna \ dwoch \ liczb \ jednej \ wiekszej \ niz \ 1 \ a \ drugiej \ dodatniej \\ musi \ byc \ wieksza \ niz \frac{1}{2}
\\
\frac{1}{2}(a_n+\frac{1}{a_n})\geq\frac{1}{2}(1+0)\geq \frac{1}{2}
\\\\
Gorne: 2\\
Indukcja:\\
1) n=1, a_1=2\\
2) a_n\leq 2\\
3) \frac{1}{2}(a_n+\frac{1}{a_n})\leq \frac{1}{2}(2+\frac{1}{2})\leq \frac{5}{4}
\\\\
Monotonicznosc:\\
Udowodnilismy \ ze \ \frac{1}{2}\leq a_n \leq \frac{5}{4}\\
W \ najlepszym \ przypadku: (a_n=\frac{1}{2})\\
a_{n+1}=\frac{1}{2}(a_n+\frac{1}{a_n})=\frac{5}{4}\geq \frac{1}{2}\\\\
W \ najgorszym \ przypadku: (a_n=\frac{5}{4})\\
a_{n+1}=\frac{1}{2}(a_n+\frac{1}{a_n})=\frac{5}{4}\geq \frac{5}{4}
\\
Zatem \ rosnaca\\
\\
Granica:\\
L=\frac{1}{2}(L+\frac{1}{L})\\
\frac{1}{2}L-\frac{1}{2}=0\\
L=1
\end{gathered}
$$

###### Wyznacz granice górną i dolną ciągu $a_n=(1+\frac{1}{n})^n(-1)^n+\sin{\frac{n\pi}{4}}$

$$\begin{gathered}
a_n:\\
k \in \mathbb{Z}\\
n=8k, \ \ a_n=(1+\frac{1}{8k})^{8k}(-1)^{8k}+\sin{\frac{8k\pi}{4}}\\
\lim_{k \to \infty}{a_n}=e\\
n=8k+1, \ \ a_n=(1+\frac{1}{8k+1})^{8k+1}(-1)^{8k+1}+\sin{\frac{(8k+1)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=-e+\frac{\sqrt{2}}{2}\\
n=8k+2, \ \ a_n=(1+\frac{1}{8k+2})^{8k+2}(-1)^{8k+2}+\sin{\frac{(8k+2)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=e+1\\
n=8k+3, \ \ a_n=(1+\frac{1}{8k+3})^{8k+3}(-1)^{8k+3}+\sin{\frac{(8k+3)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=-e+\frac{\sqrt{2}}{2}\\
n=8k+4, \ \ a_n=(1+\frac{1}{8k+4})^{8k+4}(-1)^{8k+4}+\sin{\frac{(8k+4)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=e+0\\
n=8k+5, \ \ a_n=(1+\frac{1}{8k+5})^{8k+5}(-1)^{8k+5}+\sin{\frac{(8k+5)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=-e-\frac{\sqrt{2}}{2}\\
n=8k+6, \ \ a_n=(1+\frac{1}{8k+6})^{8k+6}(-1)^{8k+6}+\sin{\frac{(8k+6)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=e-1\\
n=8k+7, \ \ a_n=(1+\frac{1}{8k+7})^{8k+7}(-1)^{8k+7}+\sin{\frac{(8k+7)\pi}{4}}\\
\lim_{k \to \infty}{a_n}=-e-\frac{\sqrt{2}}{2}\\\\\\
\lim_{n \to \infty}{sup \ a_n}=e+1\\
\lim_{n \to \infty}{inf \ a_n}=-e-\frac{\sqrt{2}}{2}
\end{gathered}$$

###### Oblicz granice funkcji (nie korzystając z reguły de L'Hospitala)

$$\begin{gathered}
\lim_{x\to -1}{\frac{x^4+3x^2-4}{x+1}}=\lim_{x\to -1}{
x^3-x^2+4x-4}=-10
\end{gathered}$$
---
$$\begin{gathered}
\lim_{x\to \frac{\pi}{4}}{\frac{\cos{2x}}{\sin{x}-\cos{x}}}=
\lim_{x\to \frac{\pi}{4}}{\frac{\cos{x}^2-\sin{x}^2}{\sin{x}-\cos{x}}}=
\lim_{x\to \frac{\pi}{4}}{\cos{x}+\sin{x}}=\sqrt{2}
\end{gathered}$$
---
$$\begin{gathered}
\lim_{x\to \infty}{x \cdot \sin{\frac{1}{x}}}=
\lim_{x\to \infty}{x} \cdot \lim_{x\to \infty}{\sin{\frac{1}{x}}}=
\lim_{x\to \infty}{x \cdot \frac{1}{x}}=1
\end{gathered}$$
---
$$\begin{gathered}
\lim_{x\to \infty}{\sqrt{x}\sin(\sqrt{x+1}-\sqrt{x})}=
\lim_{x\to \infty}{\sqrt{x}\cdot (\sqrt{x+1}-\sqrt{x})}=\\
\lim_{x\to \infty}{\sqrt{x}\cdot \frac{x+1-x}{\sqrt{x+1}+\sqrt{x}}}=
\lim_{x\to \infty}{\frac{\sqrt{x}}{\sqrt{x+1}+\sqrt{x}}}=\\
\lim_{x\to \infty}{\frac{1}{\sqrt{1+\frac{1}{x}}+\sqrt{1}}}=\frac{1}{2}
\end{gathered}$$
---
$$\begin{gathered}
\lim_{x\to 0}{e^{-\frac{1}{x}}}=
\lim_{x\to 0}{\frac{1}{\sqrt[x]{e}}}=0

\end{gathered}$$
---
$$\begin{gathered}
\lim_{x\to -2}{\frac{\arcsin{(x+2)}}{x^2+2x}}\\
Gdzie:\\
\lim_{x\to 0}{\arcsin{(\sin{x})}}=\lim_{x\to 0}{\arcsin{x}}=x\\
\lim_{x\to -2}{\frac{x+2}{x^2+2x}}=
\lim_{x\to -2}{\frac{1}{x}}=-\frac{1}{2}
\end{gathered}$$
---
$$\begin{gathered}
\lim_{x\to \infty}{\sin{x}} \ - \ nie \ istnieje \ bo \ sin \ nie \ zbiezne
\end{gathered}$$
---
###### 17. Narysuj wykres oraz zbadaj ciągłość w całej dziedzinie funkcji $f(x)$
$$\begin{gathered}
f(x)=
\left\{
\begin{array}{1}
\sin{x}, \ x\leq 0\\
x-x^2, \ 0\lt x \lt 1\\
\ln{x}, \ x\geq 1
\end{array}
\right.

\end{gathered}$$![[diagram-20241118.png]]
$$\begin{gathered}
\lim_{x\to 0^-}{\sin{x}}=0\\
sin(0)=0\\
\lim_{x\to 0^+}{x-x^2}=0\\
\lim_{x\to 1^-}{x-x^2}=0\\
\lim_{x \to 1^+}{\ln{x}}=0\\
Ciagla
\end{gathered}$$

---
###### 18. Dla jakiej wartości parametru $a$ funkcja $f(x)$ jest ciągła w całej dziedzinie?
$$\begin{gathered}
f(x)=
\left\{\begin{array}{1}
\frac{\sqrt{1+x}-1}{x}, \ x \neq 0\\
a, \ x=0
\end{array}
\right.\\\\
Zeby \ byla \ ciagla \ to:\\
\lim_{x\to 0^-}{\frac{\sqrt{1+x}-1}{x}}=\lim_{x\to 0^+}{\frac{\sqrt{1+x}-1}{x}}\\
Wiec \ mozemy \ zalozyc \ ze \ tak \ jest:\\
\lim_{x\to 0}{\frac{\sqrt{1+x}-1}{x}}=
\lim_{x\to 0}{\frac{x}{x\cdot (\sqrt{1+x}+1)}}=
\lim_{x\to 0}{\frac{1}{\sqrt{1+x}+1}}=\frac{1}{2}\\\\
Zatem \ a=\frac{1}{2}
\end{gathered}$$
###### 19. Oblicz pochodne funkcji:

$$\begin{gathered}
f(x)=(4x^3-2x+5)e^x\\
f'(x)=(4x^3-2x+5)'\cdot e^x + (4x^3-2x+5) \cdot (e^x)'=\\
=(12x^2-2)\cdot e^x + (4x^3-2x+5)\cdot e^x=\\
=e^x\cdot (4x^3+12x^2-2x+3)
\end{gathered}$$
---
$$\begin{gathered}
f(x)=2\sqrt[3]{x}-\frac{4}{x^4}\\
f(x)=2x^{\frac{1}{3}}-4x^{-4}\\
f'(x)=\frac{2}{3}x^{-\frac{2}{3}}+16x^{-5}=
\frac{2}{3\sqrt[3]{x^2}}+\frac{16}{x^5}
\end{gathered}$$
---
$$\begin{gathered}
f(x)=\frac{\ln{x}}{1+x^2}\\
f'(x)=\frac{\frac{1}{x}\cdot (1+x^2)-\ln{x}\cdot 2x}{(1+x^2)^2}=
\frac{x+\frac{1}{x}-2\ln{x}\cdot x}{x^4+2x^2+1}
\end{gathered}$$
---
$$\begin{gathered}
f(x)=x\cdot \arcsin(x)+\sqrt{1-x^2}\\
g(x)=x\cdot \arcsin{x}\\
h(x)=\sqrt{1-x^2}\\
f(x)=g(x)+h(x)\\
f'(x)=g'(x)+h'(x)\\
f'(x)=\arcsin{x}+\frac{x}{\sqrt{1-x^2}}+h'(x)\\
gdzie:\\
h(x)=a(b(x))\\
gdzie:\\
a(x)=\sqrt{x}\\
b(x)=1-x^2\\
h'(x)=a'(b(x))\cdot b'(x)\\
h'(x)=-\frac{x}{\sqrt{1-x^2}}\\
f'(x)=\arcsin{x}+\frac{x}{\sqrt{1-x^2}}-\frac{x}{\sqrt{1-x^2}}=\arcsin{x}\\
\end{gathered}$$
---
$$\begin{gathered}
f(x)=\arcsin{\frac{1}{x}}\\
h(x)=\arcsin{x}\\
g(x)=\frac{1}{x}\\
f(x)=h(g(x))\\
f'(x)=h'(g(x))\cdot g'(x)\\
f'(x)=\frac{1}{\sqrt{1-\frac{1}{x^2}}}\cdot - \frac{1}{x^2}=
-\frac{1}{\sqrt{x^4-x^2}}
\end{gathered}$$
---
$$\begin{gathered}
f(x)=e^{\sin{x}}\\
h(x)=e^x\\
g(x)=\sin{x}\\
f(x)=h(g(x))\\
f'(x)=h'(g(x))\cdot g'(x)\\
f'(x)=e^{\sin{x}}\cdot \cos{x}
\end{gathered}$$
---
$$\begin{gathered}
f(x)=\cos(x)^{\sin{x}}\\
f(x)=e^{\ln{\cos{x}}\cdot \sin{x}}\\
g(x)=e^x\\
h(x)=\ln{\cos{x}}\cdot \sin{x}\\
f'(x)=g'(h(x))\cdot h'(x)\\
f'(x)=e^{\ln{\cos{x}}\cdot \sin{x}}\cdot (\ln{\cos{x}}\cdot \sin{x})'\\
f'(x)=e^{\ln{\cos{x}}\cdot \sin{x}}\cdot ((\ln{\cos{x}})'\cdot \sin{x}+\ln{\cos{x}}\cdot \cos{x})\\
(\ln{\cos{x}})'=-\frac{\sin{x}}{\cos{x}}\\
...
\end{gathered}$$
---
###### 20. Zbadaj różniczkowalność w całej dziedzinie funkcji $f(x)$ Czy $f \in C^1(\mathbb{R})$?
$C^{n}(A)$ - zbiór funkcji $n$-krotnie różniczkowalnych na $A$ i takich, że $f^{(N)}$ jest ciągła na $A$.
$$\begin{gathered}
f(x)=\left\{
\begin{array}{1}
x^2\cdot \arctan{\frac{1}{x}}, \ x \neq 0\\
0, x=0
\end{array}
\right.\\
Czy \ f \in C^1(\mathbb{R})?\\\\
\lim_{x\to 0^-}{x^2\cdot \arctan{\frac{1}{x}}}=0\\
\lim_{x\to 0^+}{x^2\cdot \arctan{\frac{1}{x}}}=0\\
Wiec \ ciagla.\\
f'(x)=2x\cdot \arctan{\frac{1}{x}}+x^2\cdot (\frac{1}{1+\frac{1}{x^2}}\cdot - \frac{1}{x^2})=2x\arctan{\frac{1}{x}}\cdot -\frac{1}{1+\frac{1}{x^2}}\\
Czy \ pochodna \ istnieje \ w \ punkcie \ x=0?\\
f'(0)=\lim_{x\to 0}{\frac{f(x)-f(0)}{x-0}}=\lim_{x\to 0}x\cdot \arctan{\frac{1}{x}}\\
\lim_{x\to 0^-}x\cdot \arctan{\frac{1}{x}}=-1=\lim_{x\to 0^+}x\cdot \arctan{\frac{1}{x}}\\
Czy \ pochodna \ ciagla?\\
f'(0)=-1\neq 
\end{gathered}$$
###### Dla jakich wartości parametrów $a,b,c$ funkcja $f(x)$ jest różniczkowalna w całej dziedzinie?

$$\begin{gathered}
f(x)=\left\{
\begin{array}{1}
\sin{x}, \ x\lt 0\\
ax^2+bx+c, \ x \geq 0
\end{array}
\right.\\\\
Czy \ funkcja \ ciagla?\\\\
\lim_{x\to 0^-}{f(x)}=0\\
\lim_{x\to 0^+}{f(x)}=c\\
c=0\\\\
Czy \ pochodna \ ciagla?\\\\
f'(x)=\cos{x}, f'(0^-)=\cos{0}=1\\
f'(x)=2ax+b, f'(0^+)=b\\
b=1
\end{gathered}$$

**Z definicji pochodnej korzystamy przy trudniejszych funkcjach, przy prostszych wystarczy sprawdzić równość pochodnych z obu stron.**
