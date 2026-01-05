
Liczby 3 cyfrowe niepodzielne przez 3 i 7


900 liczb trzycyfyfrowych

podziel 3 = $A_3$

$|A_3|=\frac{900}{3}=300$

podziel 7$=A_7$
$|A_7|=\lfloor \frac{900}{7} \rfloor=128$

podziel 21=$A_3 \cap A_7=A_{21}$ bo $NWD(3,7)=21$

$|A_{21}|=\lfloor \frac{900}{21} \rfloor=42$

$900-(300+128-42)=514$

---

Nie jest $a^2, a^3$ w $[1,\dots,10 \ 000]$

$$\begin{gathered}
a^2\in [1,\dots,10\ 000] \Leftrightarrow a\in [1,100]\\
a^3\in [1,\dots,10\ 000] \Leftrightarrow a\in [1,\dots,\lfloor \sqrt[3]{10 \ 000}\rfloor]=[1,...,21]\\
a: a^2\in [1,\dots,10\ 000] \land a^3\in [1,\dots,10\ 000]=b^6\in [1,\dots,10\ 000]\\
b\in [1,2,3,4]
\\\\\
10\ 000-(100+21-4)=9 \ 877
\end{gathered}
$$
---
$$
\begin{gathered}
x_1+x_2+x_3+x_4=12\\\\
x_i\geq 0\\
x_i \leq 5, i=1,\dots,4\\\\
\text{Wszystkie bez warunków}:\\\\
\binom{12+4-1}{4-1}=\binom{15}{3}=\binom{15}{12}=\frac{13\cdot 14\cdot 15}{3!}=\dots=a\\\\
x_1\text{ napewno przekroczyło 5}:\\\\
(x_1+6)+x_2+x_3+x_4=6\\\\
\binom{6+4-1}{6}=\binom{9}{6}=b_1\\
b=b_1+b_2+b_3+b_4=4\cdot \binom{9}{6}\\\\
x_1,x_2 \text{ przekroczyło}:\\\\
(x_1+6)+(x_2+6)+x_3+x_4=2\\\\
c=\binom{4}{2}\\\\
a-b+c
\end{gathered}
$$





---
