---
share_link: https://share.note.sx/6kqxno2y#qfmLmtXZeujRverBoxzeZl1zHun3R883vUrhby8cUUI
share_updated: 2024-12-02T18:42:12+01:00
---

## Frydrych

### 2010/2011

---
###### 1. Dany jest ciąg rekurencyjny $x_1=6, x_{n+1}=\sqrt{6+x_n}$ dla $n\geq 1$ pokaż że ciąg $(x_n)$ jest zbieżny i znajdź jego granicę.

$$\begin{gathered}
\frac{x_{n+1}}{x_n}\leq 1\\
\sqrt{6+x_n}\leq x_n\\
6+x_n\leq x_n^2\\
x_n^2-x_n-6\geq 0\\
\Delta = 25\\
x_1=3\\
x_2=-2\\
Zatem \ kolejny \ wyraz \ jest \ mniejszy \ dla \ wyrazu \ wiekszego \ od \ 3.
\\\\
Ograniczenie:\\
1. \sqrt{6+6}\geq 3\\
2. \ x_n \geq 3\\
3. x_{n+1}=\sqrt{6+3}=3\geq 3\\
Ograniczenie \ dolne \ przez \ 3.\\
L=\sqrt{6+L}\\
L^2=6+L\\
L=3
\end{gathered}$$
---
###### 2. Wyznacz wszystkie asymptoty funkcji $f(x)=x\ln{\frac{2x}{x-2}}$
Ukośne:
$$\begin{gathered}
a=\lim_{x\to \infty}{\frac{f(x)}{x}}=\lim_{x\to \infty}{\ln{\frac{2x}{x-2}}}=\ln{2}\\
b=\lim_{x\to \infty}{f(x)-ax}=\lim_{x\to \infty}{x\ln{\frac{2x}{x-2}}-\ln{(2)}x}=\lim_{x\to \infty}{x\cdot (\ln{\frac{x}{x-2}})}=\\
=\lim_{x\to \infty}{\frac{\ln{\frac{x}{x-2}}}{\frac{1}{x}}}=\lim_{x\to \infty}\frac{x-2}{x}\cdot \frac{-2}{x^2-4x+4}\cdot -x^2=\frac{2x^3-4x^2}{x^3-4x+4}
=2\end{gathered}$$
Nie ma poziomych skoro jest ukośna no ale spróbujmy policzyć chociaż granice żeby to dowieść:
$$\begin{gathered}
\lim_{x\to \infty}{x\cdot \ln{\frac{2x}{x-2}}}=\infty
\end{gathered}$$
Pionowe:
$$\begin{gathered}
\mathbb{D}: 
\\x\neq 2\\
\frac{2x}{x-2}\gt 0\\
2x(x-2)\gt 0\\
x \in (-\infty, 0) \cup (2, \infty)\\
\lim_{x\to 0^-}{f(x)}=\lim_{x\to 0^-}{x\cdot \ln{\frac{2x}{x-2}}}=\lim_{x\to 0^-}{\frac{\ln{\frac{2x}{x-2}}}{\frac{1}{x}}}=\lim_{x\to 0^-}{\frac{x-2}{2x}\cdot \frac{-4}{x^2-2x+4}\cdot -x^2}=\\=\lim_{x\to 0^-}{(x^2-2x)\cdot \frac{2x}{x^2-2x+4}}=\lim_{x\to 0^-}{\frac{2x^3-4x^2}{x^2-2x+4}}=0\\\\
\lim_{x\to 2^+}{x\cdot \ln{\frac{2x}{x-2}}}=\infty\\
Wiec \ asymptota \ prawostronna \ w \ x=2
\end{gathered}$$
---
###### 3. Pokaż że dla każdego $x \gt 1$ zachodzi nierówność $2\ln{x} \lt x - \frac{1}{x}$
$$\begin{gathered}
Pochodne \ obu \ stron:\\
(2\ln{x})'=\frac{2}{x}\\
(x-\frac{1}{x})'=1+\frac{1}{x^2}\\
\frac{2}{x}-1-\frac{1}{x^2}\gt 0\\
t=\frac{1}{x}\\
-t^2+2t-1\gt 0\\
(t-1)^2\lt 0\\
Tylko \ nieprawdziwe \ d la \ t=1\\
\frac{1}{x}=1\\
x=1\\
Czyli \ 2\ln{x} \ zawsze \ rosnie \ szybciej \ od \ x-\frac{1}{x} \ jesli \ x\gt 1.\\
Pytanie \ tylko \ czy \ dla  \ x \ bliskiego \ 1 \ 2\ln{x} \leq x-\frac{1}{x}\\
\lim_{x\to 1}{2\ln{x}}=0\\
\lim_{x\to 1^+}{x-\frac{1}{x}}=0\\
Tak.\\
Wiec \ rowne \ dla \ x=1\ a \ potem \ x-\frac{1}{x}\ rosnie \ szybciej \ od \ \ln{x}.
\end{gathered}$$
---
###### 4. Wyznacz ekstrema lokalne i przedziały monotoniczności funkcji $f(x)=\arccos{(\frac{1-x^2}{1+x^2})}$

$$\begin{gathered}
\mathbb{D}f(x):\\
\frac{1-x^2}{1+x^2}\leq1\\
1-x^2\leq 1+x^2\\
2x^2\geq 0\\
x \in \mathbb{R}\\
\land \\
\frac{1-x^2}{1+x^2}\geq -1\\
1-x^2\geq -1-x^2\\
x \in \mathbb{R}\\

\\\\
f'(x)=-\frac{1}{\sqrt{1-(\frac{1-x^2}{1+x^2})^2}}\cdot \frac{-2x\cdot (1+x^2)-2x\cdot (1-x^2)}{x^4+2x^2+1}=\\=
-\frac{1}{\sqrt{1-(\frac{1-x^2}{1+x^2})^2}}
\cdot \frac{-2x^3-2x+2x^3-2x}{x^4+2x^2+1}=\frac{1}{\sqrt{1-(\frac{1-x^2}{1+x^2})^2}}\cdot \frac{4x}{x^4+2x^2+1}=\\
=\frac{1}{\sqrt{\frac{x^4+2x^2+1-x^4+2x^2-1}{x^4+2x^2+1}}}\cdot \frac{4x}{x^4+2x^2+1}=\frac{1}{\sqrt{\frac{4x^2}{x^4+2x^2+1}}}\cdot \frac{4x}{x^4+2x^2+1}=\\
=\frac{1}{|\frac{2x}{x^2+1}|}\cdot \frac{4x}{x^4+2x^2+1}=|\frac{x^2+2x+1}{2x}|\cdot \frac{4x}{x^4+2x^2+1}=|\frac{(x+1)^2}{2x}|\cdot \frac{4x}{(x^2+1)^2}\\
f'(x)=\left\{
\begin{matrix}
2\cdot \frac{(x+1)^2}{(x^2+1)^2}, x \gt 0\\
-2\cdot \frac{(x+1)^2}{(x^2+1)^2}, x \lt 0

\end{matrix}
\right.
\\
\Leftrightarrow\\
f'(x)=0 \Leftrightarrow x=-1 \ A \ tak \ byc \ nie \ moze \ bo \ dziedzina \ pochodnej \ x\neq 1 \\ (z \ tamtego \ pierwiastka \ na \ poczatku.)\\
f'(x)\lt 0 \ dla \ x\lt 0\\
f'(x)\gt 0 \ dla \ x\gt 0\\
Wiec \ ekstremum \  (minimum) \ w\  x=0. \ f(x)=0
\end{gathered}$$

---
### 2011/2012
###### 1. Dany jest ciąg rekurencyjny $x_1=a,  \ x_{n+1}=\frac{1}{2}+\frac{1}{2}\cdot x_n^2$ dla $n\geq 1$. Zbadaj dla jakich wartości początkowych $a$ ciąg $(x_n)$ jest zbieżny, a dla jakich rozbieżny. W przypadkach gdy ciąg $(x_n)$ jest zbieżny oblicz jego granicę.

$$\begin{gathered}
x_{n+1}-x_n=\frac{1}{2}\cdot x_n^2-x_n+\frac{1}{2}\geq 0\\
\Delta=1-1=0\\
x_n=1\\
Rosnie \ zawsze \ dla \ x_n\neq 1\\
Ograniczenie \ x_n\leq 1:\\
1.n=1\\ x_1=a\\
2.x_n\leq 1\\
3.\frac{1}{2}+\frac{1}{2}\cdot x_n\leq \frac{1}{2}+\frac{1}{2}\cdot 1\leq 1\\
Zatem \ musimy \ zalozyc \ ze \ jest \ ograniczony \ dla \ a\leq 1\\\\\
Co \ w \ przypadku \ gdy \ a\gt 1\\
Wtedy \ x_{2}=\frac{1}{2}+\frac{1}{2}\cdot 1^+\gt 1...\\
Kazdy \ kolejny \ wyraz \ wiekszy \ od \ poprzedniego \ wiec \ ograniczenie\ istnieje \ tylko\\ dla \ a\gt 1.
\\
Granica:\\
L=\frac{1}{2}+\frac{1}{2}\cdot L^2\\
\frac{1}{2}+\frac{1}{2}\cdot L^2-L=0\\
L=1
\end{gathered}$$
###### 2. Wyznacz ekstrema lokalne i przedziały monotoniczności funkcji $f(x)=\ln{(x^3-3x)}$.
$$\begin{gathered}
\mathbb{D}f(x):\\
x^3-3x\gt 0\\
x(x^2-3)\gt 0\\
x\in (-\sqrt{3},0)\cup (\sqrt{3},\infty)
\\
f'(x)=\frac{1}{x^3-3x}\cdot 3x^2-3=\frac{3x^2-3}{x^3-3x}\\
Przedzialy \ monotonicznosci:\\
f'(x)\lt 0\\
\frac{3x^2-3}{x^3-3x}\lt 0\\
(3x^2-3)(x^3-3x)\lt 0\\
3(x^2-1)x(x^2-3)\lt 0\\
x=1\vee x=-1\vee x=0\vee x=\sqrt{3}\vee x=-\sqrt{3}\\

\end{gathered}$$
![[diagram-20241201.png]]

$$\begin{gathered}
x\in (-\infty, -\sqrt{3})\cup (-1,0)\cup (1,\sqrt{3})\\
f'(x)\geq 0\\
x\in [-\sqrt{3},-1] \cup [0,1]\cup [\sqrt{3},\infty)\\
f'(x)=0 \Leftrightarrow x=1\\
Bo \ inne \ punkty \ nie \ naleza \ do \ dziedziny \ funkcji.\\
f(-1)=\ln{2}\ (maksimum)
\end{gathered}$$
###### 4. Wyznacz wszystkie asymptoty funkcji $f(x)=\frac{x}{x+2\sqrt{x^2-1}}$
$$\begin{gathered}
\mathbb{D}f(x):\\
x^2-1\geq 0\\
x^2\geq 1\\
x\geq 1\vee x\leq -1\\
x+2\sqrt{x^2-1}=0\\
2\sqrt{x^2-1}=-x\\
Zatem \ x\leq 0\\
4(x^2-1)=x^2\\
3x^2=4\\
x=-\sqrt{\frac{4}{3}}\\
Zatem \ x\neq -\sqrt{\frac{4}{3}}\\
x\in (-\infty,-\sqrt{\frac{4}{3}})\cup (-\sqrt{\frac{4}{3}}, -1] \cup [1, +\infty)
\end{gathered}$$

**Asymptoty:**
$$\begin{gathered}
Pozioma:\\
\lim_{x\to \infty}{\frac{x}{x+2\sqrt{x^2-1}}}=\lim_{x\to \infty}{\frac{x}{x+2|x|(\sqrt{1-\frac{1}{x^2}})}}=\frac{1}{3}\\
\lim_{x\to -\infty}{\frac{x}{x+2\sqrt{x^2-1}}}=\lim_{x\to -\infty}{\frac{x}{x+2|x|(\sqrt{1-\frac{1}{x^2}})}}=\lim_{x\to -\infty}{\frac{x}{x-2x(\sqrt{1-\frac{1}{x^2}})}}=-1\\
y=\frac{1}{3}, y=-1\\
Pionowe:\\
\lim_{x\to -\sqrt{\frac{4}{3}}^-}{\frac{x}{x+2\sqrt{x^2-1}}}=\lim_{x\to -\sqrt{\frac{4}{3}}^-}{\frac{-\sqrt{\frac{4}{3}}}{-\sqrt{\frac{4}{3}}+2\cdot \sqrt{\frac{4}{3}-1}}}=[\frac{-\sqrt{\frac{4}{3}}}{0}]=-\infty\\
x=-\sqrt{\frac{4}{3}}\\
\lim_{x\to -1^+}{f(x)}=1\\
\lim_{x\to 1^+}{f(x)}=1\\
\\
Ukośne:\\
Skoro \ byly \ poziome \ to \ nie \ ma \ poziomych.
\end{gathered}$$

---
### 2012/2013

###### 1. zadanie identyczne jak w 2010/2011
###### 2. Pokaż że dla każdego $x \in (-1, +\infty)$ zachodzi nierówność $\ln{(1+x)}\geq \frac{x}{x+1}$
$$\begin{gathered}
(\ln{(1+x)})'=\frac{1}{1+x}\\
(\frac{x}{x+1})'=\frac{x+1-x}{x^2+2x+1}=\frac{1}{x^2+2x+1}\\\\
\ln{(1+x)}\geq \frac{x}{x+1}\\
\ln{(1+x)}-\frac{x}{x+1}\geq 0\\
(\ln{(1+x)}-\frac{x}{x+1})'=\frac{1}{1+x}-\frac{1}{(x+1)^2}=\frac{x}{(x+1)^2}\\
\frac{x}{(x+1)^2}\gt 0 \Leftrightarrow x\gt 0\\
\frac{x}{(x+1)^2}\lt 0 \Leftrightarrow x\lt 0\\
\frac{x}{(x+1)^2}= 0 \Leftrightarrow x= 0\\
Czyli \ minimum \ jest \  w \ punkcie \ x=0.\\
\ln{(1+0)}-\frac{0}{0+1}=0\\
Zatem \ w \ najgorszym \ przypadku \ln{(1+x)}-\frac{x}{x+1}=0\\
Ale \ nigdy \ln{(1+x)}- \frac{x}{x+1}\lt 0\\
Co \ implikuje  \ ze: \ln{(1+x)}\geq \frac{x}{x+1}, \forall x \in (-1,+\infty)

\end{gathered}$$
###### 3. Wyznacz wszystkie asymptoty funkcji $f(x)=\frac{x}{x+2\sqrt{x^2}-1}$

$$\begin{gathered}
f(x)=\frac{x}{x+2\sqrt{x^2}-1}=\frac{x}{x+2|x|-1}\\
Ukośne:\\
a=\lim_{x\to \infty}{\frac{f(x)}{x}}=\lim_{x\to \infty}{\frac{1}{x+2x-1}}=0\\
Zatem \ poziome:\\
\lim_{x\to \infty}{f(x)}=\lim_{x\to \infty}{\frac{x}{x+2|x|-1}}=\lim_{x\to \infty}{\frac{x}{x+2x-1}}=\frac{1}{3}\\
\lim_{x\to -\infty}{f(x)}=\lim_{x\to -\infty}{\frac{x}{x+2|x|-1}}=\lim_{x\to -\infty}{\frac{x}{x-2x-1}}=-1\\
Pionowe:\\
\mathbb{D}f(x):\\
x+2|x|-1=0\\
Dla \ x \lt 0\\
x-2x=1\\
-x=1\\
x=-1\\
Dla \ x \geq 0\\
x+2x=1\\
x=\frac{1}{3}\\\\
\lim_{x\to -1}{\frac{x}{x-2x-1}}=\frac{-1}{-1+2-1}=-\infty\\
\lim_{x\to \frac{1}{3}}{\frac{x}{x+2x-1}}=\frac{\frac{1}{3}}{\frac{3}{3}-1}=\infty\\
Zatem \ asymptoty:\\
y=-1\\
y=\frac{1}{3}\\
x=\frac{1}{3}\\
x=-1
\end{gathered}$$

---
### 2013/2014

###### 1. Podobne było w poprzednich latach
###### 2. a) Sprawdź, dla jakich wartości $x$ zachodzi równość $\arcsin{x}=\arctan{\frac{x}{\sqrt{1-x^2}}}$
Najpierw zacznijmy od dziedziny:
$$\begin{gathered}
\arcsin{x} \implies x\in [-1,1]\\
\arctan{\frac{x}{\sqrt{1-x^2}}}\implies \sqrt{1-x^2}\neq 0 \implies x\neq 1 \land x\neq -1\\
Oraz\\
1-x^2\gt 0\\
x^2\lt 1\\
x\lt 1 \land x\gt -1\\
Ostatecznie \ dziedzina \ wychodzi:\\
x\in (-1,1)
\end{gathered}$$

W zadaniu innymi słowy pytają nas o to kiedy $\sin{y}=x \land \tan{y}=\frac{x}{\sqrt{1-x^2}}$:
$$\begin{gathered}
\tan{y}=\frac{\sin{y}}{\cos{y}}=\frac{\sin{y}}{\sqrt{1-\sin^2{y}}}=\frac{x}{\sqrt{1-x^2}}\\
\end{gathered}$$
Cóż, wychodzi na to że zawsze (oczywiście w dziedzinie).

###### 2. b) Oblicz granicę prawostronną w $x=0$ funkcji $f(x)=x^{\tan{(x)}}$

$$\begin{gathered}
\lim_{x\to 0^+}{x^{\tan{(x)}}}=
\lim_{x\to 0^+}{e^{\ln{x}\cdot \tan{(x)}}}=
\lim_{x\to 0^+}{e^{\frac{\ln{x}}{\cot{(x)}}}}=\\
Przenosimy \ limesa \ do \ wykladnika:\\
=e^{\lim_{x\to 0^+}{\frac{\ln{x}}{\cot{x}}}}\\
Korzystamy \ z \ reguly \ Hospitala \ [\frac{\infty}{\infty}]:\\
\lim_{x\to 0^+}{\frac{\ln{x}}{\cot{x}}}=
\lim_{x\to 0^+}{\frac{\frac{1}{x}}{-\frac{1}{\sin^2{x}}}}=
\lim_{x\to 0^+}{-\frac{\sin^2{x}}{x}}=\\
Dalej \ hospital \ [\frac{0}{0}]\\
=\lim_{x\to 0^+}{-\frac{2\sin{x}\cos{x}}{1}}=0\\
Zatem\\ \lim_{x\to 0^+}{x^{\tan{(x)}}}=e^0=1
\end{gathered}$$
###### 3. Oszacuj błąd wzoru przybliżonego $\sqrt[3]{1+x}\approxeq 1+\frac{x}{3}-\frac{x^2}{9}$ dla $|x|\leq \frac{1}{10}$

Z wzoru Maclaurina
$$\begin{gathered}
f(x)=f(0)+\frac{f'(0)}{1!}\cdot x+\frac{f''(0)}{2!}\cdot x^2+R_n(x)\\
\sqrt[3]{1+x}\approxeq 1+\frac{x}{3}-\frac{x^2}{9}+R_3(x)\\
R_3(x)=\dfrac{10}{27\,\left({x+1}\right)^{\frac{8}{3}}}\cdot \frac{1}{6}\cdot x^3\\
Reszta \ najwieksza \ dla \ x=\frac{1}{10}\\
R_3(x)\approx cos \ tam
\end{gathered}$$

###### 4. Wyznacz liczbę rozwiązań równania $\ln{x} = ax$ w zależności od parametru $a$. Wsk. Zbadaj (pobieżnie) przebieg zmienności odpowiedniej funkcji.

Przedstawmy sobie równanie $\ln{x} = ax$ jako $\ln{x} -ax=0$. A następnie sprawdźmy ile miejsc zerowych ma funkcja $\ln{x} -ax$ w zależności od parametru $a$.

$$\begin{gathered}
f(x)=\ln{x}-ax, \mathbb{D}=(0,+\infty)\\
f'(x)=\frac{1}{x}-a\\
Znak \ pochodnej \ (zakladajac \ a \gt 0).\\
\frac{1}{x}-a\gt 0 \Leftrightarrow \frac{1}{x}\gt a \Leftrightarrow x\lt \frac{1}{a}\\
\frac{1}{x}-a\lt 0 \Leftrightarrow \frac{1}{x}\lt a \Leftrightarrow x\gt \frac{1}{a}\\
Czyli \ dla \ a\gt 0 \ funkcja \ rosnie \ w \ przedziale \ (0,\frac{1}{a})\ a \ maleje \ dla \ (\frac{1}{a}, +\infty)\\\\
Wtedy \ maksimum \ lokalne \ jest \ dla\ x=\frac{1}{a}.\\
Jezeli \ f(\frac{1}{a})\gt 0\ to \ 2 \ miejsca \ zerowe.\\
Jezeli \ f(\frac{1}{a})= 0\ to \ 1 \ miejsca \ zerowe.\\
Jezeli \ f(\frac{1}{a})\lt 0\ to \ 0 \ miejsca \ zerowe.\\
f(\frac{1}{a})=\ln{\frac{1}{a}}-a\cdot \frac{1}{a}=-\ln{a}-1\\
-\ln{a}-1\gt 0\\
\ln{a}\lt -1\\
a\lt \frac{1}{e}\\
-\ln{a}-1=0\\
a= \frac{1}{e}\\
-\ln{a}-1\lt 0\\
a\gt \frac{1}{e}\\
Zatem: \\
\ln{x}=ax \ ma \ 2 \ rozwiazania \ dla \ a \in (0,\frac{1}{e})\\
\ln{x}=ax \ ma \ 1 \ rozwiazania \ dla \ a = \frac{1}{e}\\
\ln{x}=ax \ ma \ 0 \ rozwiazania \ dla \ a \in (\frac{1}{e}, +\infty)


\end{gathered}$$

Musimy tylko teraz sprawdzić co sie stanie dla $a\lt 0$

$$\begin{gathered}
Wtedy \ pochodna \ f'(x)=\frac{1}{x}-a\ jest \ zawsze \ dodatnia.\\
Wiec \ zawsze \ jedno \ miejsce \ zerowe.
\end{gathered}
$$

---
## Banaśkiewicz

### 2023/2024

###### 1. Oblicz granice:

$$\begin{gathered}
\lim_{x\to 0}{\frac{\arcsin{x^2}}{x^2}}\\
Mozemy \ zalozyc \ ze \ to \ to \ samo \ co:\\
\lim_{x\to 0}{\frac{\arcsin{x}}{x}}\\
bo \ x \to 0=x^2\to 0\\
A \ wtedy \ wiemy \ ze \lim_{x\to 0}{\arcsin{x}}=\lim_{x\to 0}{x}\\\\
\lim_{x\to 0}{\frac{\arcsin{x^2}}{x^2}}=1\\\\
Lub \ bardziej \ po \ bożemu:\\
\lim_{x\to 0}{\frac{\arcsin{x^2}}{x^2}}=[\frac{0}{0}]=\lim_{x\to 0}{\frac{\frac{1}{\sqrt{1-x^2}}\cdot 2x}{2x}}=\lim_{x\to 0}{\frac{1}{\sqrt{1-x^2}}}=1
\end{gathered}$$
###### 2. Wyznacz granice:

Na podstawie twierdzenia o 3 ciągach/funkcjach.
$$\begin{gathered}
\lim_{n \to \infty}{\sum^{n}_{i=1}{\frac{i\sin{(i)}}{n^3}}}\\
\sin{i}\leq 1 \implies \lim_{n \to \infty}{\sum^{n}_{i=1}{\frac{i\sin{(i)}}{n^3}}}\leq \lim_{n \to \infty}{\sum^{n}_{i=1}{\frac{i}{n^3}}}=\lim_{n\to \infty}{\frac{\frac{n^2+n}{2}}{n^3}}=\lim_{n\to \infty}{\frac{n^2+n}{2n^3}}\\
\sin{i}\geq -1 \implies \lim_{n \to \infty}{\sum^{n}_{i=1}{\frac{i\sin{(i)}}{n^3}}}\geq -\lim_{n \to \infty}{\sum^{n}_{i=1}{\frac{i}{n^3}}}=-\lim_{n\to \infty}{\frac{\frac{n^2+n}{2}}{n^3}}=-\lim_{n\to \infty}{\frac{n^2+n}{2n^3}}\\
\\
-\frac{n^2+n}{2n^3}\leq {\sum^{n}_{i=1}{\frac{i\sin{(i)}}{n^3}}}\leq \frac{n^2+n}{2n^3}\\
\lim_{n \to \infty}\frac{n^2+n}{2n^3}=-\lim_{n\to \infty}{\frac{n^2+n}{2n^3}}=0 \implies \lim_{n \to \infty}{\sum^{n}_{i=1}{\frac{i\sin{(i)}}{n^3}}}=0
\end{gathered}$$
## Bratuszeeeeee

### 2023/2024

###### 1. Oblicz $\cos{(2\cdot \arcsin{\frac{2}{3}})}$
$$\begin{gathered}
Korzystamy \ z \ zaleznosci/wzoru: \ \cos{(2\alpha)}=2\cos^{2}{(\alpha)}-1=1-2\sin^2{(\alpha)}\\
\cos{(2\cdot \arcsin{\frac{2}{3}})}=1-2\sin^2{(\arcsin{\frac{2}{3}})}=1-2\cdot (\frac{2}{3})^2=1-\frac{8}{9}=\frac{1}{9}
\end{gathered}$$
###### 2. Robiłem podobne albo takie samo gdzieś wyżej.

###### 3. Oblicz granice ciągów:

$a_n=\frac{3^n\cdot n!}{(2n)^n}$
Korzystamy z własności Alamberta
$\lim_{n \to \infty}{|\frac{a_n+1}{a_n}|} \lt 1 \implies \lim_{n \to \infty} a_n=0 \ \ \ Alambert$
$$\begin{gathered}
\frac{a_{n+1}}{a_n}=\frac{3\cdot 3^n\cdot n!\cdot (n+1)}{2^{n+1}\cdot (n+1)^{n+1}}\cdot \frac{2^n\cdot n^n}{3^n\cdot n!}=\frac{3\cdot (n+1)}{2}\cdot \frac{n^n}{(n+1)^n\cdot (n+1)}=\frac{3}{2}\cdot (\frac{n}{n+1})^n\\\\
\lim_{n\to \infty}{\frac{3}{2}\cdot (\frac{n}{n+1})^n}=\frac{3}{2}\cdot \lim_{n \to \infty}{(1-\frac{1}{n+1})^n}=\frac{3}{2}\cdot \lim_{n \to \infty}{(1+\frac{1}{-n-1})^{(-n-1)\cdot -1 - 1}}=\\=\frac{3}{2}\cdot e^{-1}\cdot \lim_{n\to \infty}{\frac{n+1}{n}=\frac{3}{2e}}\lt 1 \implies \lim_{n\to \infty}{a_n}=0
\end{gathered}$$

---
$b_n=n\cdot \cos{(n\cdot \pi)}$
Mamy twierdzenie że jeśli podciągi mają różną granice to ten ciąg nie ma żadnej granicy.
Przyjmując $n=2k$
$b_{2k}=2k\cdot \cos{(2k\cdot \pi)}$
$\lim_{k \to \infty}{b_{2k}}=\lim_{k\to \infty}2k=\infty$
Przyjmując $n=2k+1$
$b_{2k+1}=(2k+1)\cdot \cos{((2k+1)\cdot \pi)}$
$\lim_{k \to \infty}{b_{2k+1}}=\lim_{k\to \infty}-2(k+1)=-\infty$

Różne więc granica nie istnieje.

---

$c_n=\sqrt[n]{2n-\cos{n}}$

Tu od razu widać że wychodzi 1, ale pewnie trzeba to wykazać zatem:

$$\begin{gathered}
\lim_{n\to \infty}{\sqrt[n]{2n-\cos{n}}}=\lim_{n\to \infty}e^{\frac{\ln{2n-\cos{n}}}{n}}\\
Przerzucamy \ limesa \ do \ wykladnika:\\
e^{\lim_{n\to \infty}{\frac{\ln{(2n-\cos{n})}}{n}}}\\
Z \ tw. \ 3 \ ciagow:\\
\frac{\ln{(2n-1)}}{n}
\lt \frac{\ln{(2n-\cos{n})}}{n}\lt
\frac{\ln{(2n+1)}}{n}\\\\
\lim_{n\to \infty}\frac{\ln{(2n-1)}}{n}=[\frac{\infty}{\infty}]H=\lim_{n\to \infty}\frac{1}{2n-1}\cdot 2=0=\lim_{n\to \infty}\frac{\ln{(2n+1)}}{n}\\\\
Zatem \lim_{n\to \infty}{\sqrt[n]{2n-\cos{n}}}=e^0=1
\end{gathered}$$

---
$d_n=(1+\sin{\frac{1}{n}})^n$

Wiemy że sinus dla małych wartości zachowuje sie jak to co w środku sinusa. To znaczy:
$\lim_{x\to 0}{\sin{x}}=\lim_{x\to 0}{x}$
Zatem mamy:

$\lim_{n\to \infty}{d_n}=\lim_{n\to \infty}(1+\frac{1}{n})^n=e$

---

###### 4. Wiedząc że $\forall x\gt -1:  \ln{(1+x)}\leq x$ pokaż że ciąg $a_n=(1+\frac{1}{3})(1+\frac{1}{9})(1+\frac{1}{9})\dots (1+\frac{1}{3n})$ jest zbieżny.

$$\begin{gathered}
\ln{(1+x)}\leq x\\
\ln{(1+x)}\leq \ln{e^x}\\
1+x\leq e^x\\
a_n\leq e^{\frac{1}{3}}\cdot e^{\frac{1}{9}}\dots e^{\frac{1}{3n}}\\
a_n\leq e^{\frac{1}{3}+\frac{1}{9}+\dots+\frac{1}{3n}}\\

Suma \ ciagu \ geometrycznego: \frac{1}{3}+\frac{1}{9}+\dots+\frac{1}{3n}=\\=\frac{\frac{1}{3}}{1-\frac{1}{3}}=\frac{1}{2}\\
Zatem \ ciag \ a_n\ jest \ ograniczony \ przez \ e^\frac{1}{2}\\
\frac{a_{n+1}}{a_n}=1+\frac{1}{3n+3}\geq 1\\
Wiec \ rosnie \ i \ jest \ ograniczony  \implies \ jest \ zbiezny.
\end{gathered}$$
### Kolokwium 1, grupa 6,8a

###### 2. Sprawdź, czy ciąg rekurencyjny $x_1=6, \ x_{n+1}=\sqrt{x_n+12}$ jest zbieżny i wyznacz granicę.
$$\begin{gathered}
x_1=6, \ x_{n+1}=\sqrt{x_n+12}\\
Ograniczenie:\\
x_n\geq 4\\
1.x_1=6\geq 4\\
2. Zakladamy \ ze \ x_n\geq 4\\\\
3. x_{n+1}=\sqrt{x_n+12}\geq \sqrt{4+12}=4\\\\
\frac{x_{n+1}}{x}=\frac{\sqrt{x_n+12}}{x_n}\leq 1\\
x_n+12\leq x_n^2\\
x_n^2-x_n-12\geq 0\\
x\in [4, +\infty] \ tak \ bo \ kazdy \ wyraz\ dodatni\ i \ wiekszy \ od \ 4.\\
Maleje \ i \ ograniczone.\\
L=\sqrt{L+12}\\
L^2-L-12=0\\
L=4
\end{gathered}$$
