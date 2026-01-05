### 🚀 Ogólny Algorytm Rozwiązywania Liniowych Równań Rekurencyjnych

Ogólna forma rozwiązań to:
$$\begin{gathered}
x_n=x_n^{(h)}+x_n^{(p)}
\end{gathered}$$
gdzie $x_n^{(h)}$ jest rozwiązaniem ogólnym równania jednorodnego, a $x_n^{(p)}$ jest rozwiązaniem szczególnym równania niejednorodnego.

#### Jak rozwiązać jednorodne? $(x_n^{(h)})$

Na przykład mając:
$$\begin{gathered}
\text{Równanie: }x_n-6x_{n-1}+5x_{n-2}=0\\
\text{to naszym równaniem charakterystycznym będzie:}\\
x^2-6x+5=0\\\\
\text{którego rozwiązaniami są:}\\
x_1=1, x_2=5\\\\
\text{zatem rozwiazaniem ogólnym równania jednorodnego jest:}\\
x_n=A(1)^n+B(5)^n=A+B\cdot 5^n
\end{gathered}$$

Następnie korzystając z warunków początkowych możemy obliczyć $A,B$:

$$\begin{gathered}
x_0=3\\
x_1=7\\
A+1=3\\
A+5B=7\\
\downarrow\\
A=2, B=1
\end{gathered}$$

Zatem rozwiązaniem tego konkretnego równania rekurencyjnego będzie:
$$\begin{gathered}
x_n=2+5^n
\end{gathered}$$

##### Co jeżeli mamy pierwiastek stopnia większego niż jeden?

Wtedy zwiększamy też stopień wielomianu który stoi przed rozwiązaniem równania charakterystycznego to jest:
$$\begin{gathered}
x_n-4x_{n-1}+4x_{n-2}=0\\
x^2-4x+4=0\\
(x-2)^2=0\\
x_1=2, st:2\\
x_n=(A+Bn)2^n
\end{gathered}$$

##### A co jeżeli pierwiastek wyjdzie zespolony?

Jego też bierzemy pod uwagę, na przykład:

$$\begin{gathered}
x_n-2x_{n-1}+4x_{n-2}=0\\
x^2-2x+4=0\\
\Delta=-12\\
x_1=\frac{2+i\sqrt{12}}{2},
x_2=\frac{2-i\sqrt{12}}{2}\\
x_n=Ax_1^n+Bx_2^n
\end{gathered}$$

To i tak się zniesie po podstawieniu konkretnych $n$. 

#### Jak rozwiązać szczególne/niejednorodne? $(x_n^{(p)})$

Jeżeli rozwiązaliśmy już niejednorodne - chociaż nie znamy jeszcze współczynników bo te ogarniemy dopiero pod koniec skoro pojawia się też część niejednorodna to musimy rozwiązać (w sensie znaleźć postać niejednorodnego).

Jeśli mamy równanie postaci:
$$\begin{gathered}
x_n=ax_{n-1}+bx_{n-2}+f(n)
\end{gathered}$$

To musimy "zgadnąć" podobną ogólną forme rozwiązania niejednorodnego. Zapiszmy to sobie jako $Q(n)$.

$$\begin{gathered}
\text{Wielomian np. }3n^2-5\to an^2+bn+c\\
\text{Wykładnicza np. }5\cdot 3^n \to D\cdot a^n\\
\text{Iloczyn np. }(n+1)\cdot 4^n \to (an+b)\cdot 4^n
\end{gathered}$$

##### Rezonans? Czyli co jeśli coś w niejednorodnym pokrywać się może z jednorodnym?

Jeśli nic się nie pokrywa to nas ta część nie obchodzi :)

$$\begin{gathered}
an^2+bn+c \to \text{tutaj pokrywać się może c z }1^n\\
D\cdot a^n \to \text{tutaj pokrywać się może }a^n\\
(an+b)\cdot 4^n \to \text{tutaj pokrywać się może }4^n
\end{gathered}$$

Co robimy w takim przypadku? Możemy pomnożyć przez $n^m$ gdzie $m$ to stopień pierwiastka który się pokrywa.

**Na końcu po sprawdzeniu tego "Rezonansu" i naprawieniu go też podstawiamy pod tamto jak wcześniej (przykład niżej)**

Załóżmy przykład:
$$\begin{gathered}
x_n-5x_{n-1}+4x_{n-2}=-6n+8\\
x^2-5x+4=0\\
x_1=1,x_2=4\\
\end{gathered}$$
Mamy jednorodne rozwiązane i w postaci:
$$\begin{gathered}
x_n^h=A\cdot 1^n+B\cdot 4^n
\end{gathered}$$

Zgadujemy niejednorodne że to będzie:
$$\begin{gathered}
an+b
\end{gathered}$$
tutaj $b$ może nam się pokrywać z tamtym $A\cdot 1^n$ zatem musimy pomnożyć tą zgadniętą forme przez $n$.

Nowa forma niejednorodnego:
$$\begin{gathered}
an^2+bn
\end{gathered}$$
Teraz wstawiamy to do równania jakie mamy $(x_n-5x_{n-1}+4x_{n-2}=-6n+8)$:
$$\begin{gathered}
an^2+bn-5a(n-1)^2-5b(n-1)+4a(n-2)^2+4b(n-2)=-6n+8\\\\
\text{uporządkujmy:}\\
an^2+bn-5a(n-1)^2-5b(n-1)+4a(n-2)^2+4b(n-2)=\\
an^2+bn-5a(n^2-2n+1)-5b(n-1)+4a(n^2-4n+4)+4b(n-2)=\\
n^2(0a)+n(-6a)+11a-3b=n(-6a)+11a-3b\\
\downarrow\\
n(-4b-6a)+11a-3b=-6n+8\\
\left\{
\begin{matrix}
-6a=-6\\
11a-3b=8
\end{matrix}
\right. \ \
\left\{
\begin{matrix}
a=1\\
b=1
\end{matrix}
\right.
\end{gathered}$$

Zatem naszą ostateczną postacią niejednorodnego będzie:
$$\begin{gathered}
x_n^p=n^2+n
\end{gathered}$$

I na końcu rozwiązujemy równanie łącząc oba równania i niejednorodne i jednorodne:
$$\begin{gathered}
x_n=A+B\cdot 4^n+n^2+n\\
\text{podstawiamy początkowe i mamy wszystko}
\end{gathered}$$

#### Podsumowanie:

1. Najpierw rozwiązujemy jednorodne 
	1.1 Jeśli nie mamy niejednorodnego to wystarczy podstawić wyrazy początkowe **KONIEC**
2. Jeśli mamy niejednorodne to zgadujemy postać:
	2.1 Jeśli coś się pokrywa z jednorodnym (albo nawet jak przypuszczamy że tak może być a pewności nie mamy) to mnożymy przez $n^k$ gdzie $k$ to krotność tego pierwiastka co się może powtarzać.
3. Podstawiamy uogólniony (zgadnięty) wzór niejednorodnego do równania 
4. obliczamy współczynniki niejednorodnego
5. wracamy do naszego równania które chcemy rozwiązać i dajemy niejednorodne też
6. podstawiamy wyrazy początkowe oraz wyliczamy współczynniki **KONIEC**

**Jeszcze jest taki niuans co jeśli kilka składników powoduje ten "rezonans" - wtedy możemy rozpatrywać każdy składnik osobno (w ogóle ogólnie możemy rozpatrywać niejednorodne po każdym składniku z osobna co pozwoli łatwiej nam liczyć )**



### Zadania przykładowe 

###### a)

$$\begin{gathered}
x_n=2x_{n-1}+x_{n-2}-2x_{n-3},x_0=0,x_1=2,x_2=0\\\\\
x^3-2x^2-x+2=0\\
(x^2-1)(x-2)=0\\
x_1=1,x_2=-1,x_3=2\\\\
x_n=A+B\cdot (-1)^n+C\cdot 2^n\\\\
x_0=0=A+B+C\\
x_1=A-B+2C=2\\
x_2=A+B+4C=0\\\\
A+B=-C\to (A+B)+4C=0\to 3C=0\to C=0\\\

A=-B\\
A=1, B=-1\\\\
x_n=1-(-1)^n
\end{gathered}$$


###### b)
$$\begin{gathered}
x_n=x_{n-1}+x_{n-2},x_0=0,x_1=1\\\\
x^2-x-1=0\\
\Delta=1+4=5\\
x_1=\frac{1-\sqrt{5}}{2},x_2=\frac{1+\sqrt{5}}{2}\\\\
x_n=Ax_1^n+Bx_2^n\\
x_0=0\\
A+B=0\implies A=-B\\
x_1=1\\
1=A \left(\frac{1-\sqrt{5}}{2}-\frac{1+\sqrt{5}}{2} \right)\\\\
1=A\cdot (-\sqrt{5})\\
A=-\frac{1}{\sqrt{5}}\\
B=\frac{1}{\sqrt{5}}
\end{gathered}$$


###### c)
$$\begin{gathered}
x_{n+2}-5x_{n+1}+6x_n=2^n,x_0=0,x_1=1\\\\
x^2-5x+6=0\\
\Delta=25-24=1\\
x_1=3, x_2=2\\\\
x_n^h=A\cdot 3^n+B\cdot 2^n\\\\
x_n^j=An\cdot 2^n\\\\
4A(n+2)\cdot 2^n-10A(n+1)\cdot 2^n+6An\cdot 2^n=2^n\\
4A(n+2)-10A(n+1)+6An=1\\
8A-10A=1\\
A=-\frac{1}{2}\\\\\
x_n=A\cdot 3^n+B\cdot 2^n-\frac{1}{2}n\cdot 2^n\\\\\
x_0=0=A+B\implies A=-B\\\\
x_1=1=3A+2B-1\\
\left\{
\begin{matrix}
A=-B\\
3A+2B-1=1
\end{matrix}
\right.\ \ 
\left\{
\begin{matrix}
B=-2\\
A=2
\end{matrix}
\right.\\\\
x_n=2\cdot 3^n-2\cdot 2^n-\frac{1}{2}n\cdot 2^n
\end{gathered}$$

###### d)

$$\begin{gathered}
x_{n+2}-5x_{n+1}+6x_n=5^n+n, x_0=0,x_1=1\\\\
x^2-5x+6=0\\
x_1=3,x_2=2\\\\
x_n^h=A\cdot 3^n+B \cdot 2^n\\\\
x_n^p=C\cdot 5^n+Dn+E\\\\
25C\cdot 5^n-25C\cdot 5^n+6C\cdot 5^n=5^n\\
C=\frac{1}{6}\\\\
D(n+2)-5D(n+1)+6Dn+3E=n\\
2Dn-3D+3E=n\\
D=\frac{1}{2},E=\frac{1}{2}\\\\
x_n=A\cdot 3^n+B\cdot 2^n+\frac{1}{2}n+\frac{1}{2}\\
x_0=0=A+B+\frac{1}{2}\\
x_1=1=3A+2B+\frac{3}{2}\\
A=-B-\frac{1}{2}\\
-3B-\frac{3}{2}+2B+\frac{3}{2}=1\implies B=-1\implies A=\frac{1}{2}\\
x_n=\frac{1}{2}3^n-2^n+\frac{1}{2}n+\frac{1}{2}
\end{gathered}$$