 
###### 1. Dane są relacje $R=(\mathbb{N}, grR,\mathbb{N}),S=(\mathbb{N},grS,\mathbb{N})$, gdzie: 

$$
\begin{gathered}
grR=\{(1,1),(1,2),(3,2),(3,4),(3,7),(2,9),(5,3)\},\\ grS=\{(1,2),(1,7),(2,5),(2,4),(7,9),(4,10)\}
\end{gathered}
$$

Znajdź dziedziny i przeciwdziedziny tych relacji. Utwórz relacje $R\circ S$, $S\circ R$, $S^{-1}$, $R^{-1}$,$S^{-1}\circ R^{-1}, (S\circ R)^{-1}, S^{-1}\circ R$. Sprawdź, że $S^{-1}\circ R^{-1}=(R\circ S)^{-1}$

$$\begin{gathered}
R\circ S=\{(1,9),(2,3)\}\\
S\circ R=\{(1,2),(1,5),(3,5),(3,4),(3,9)\}\\
S^{-1}=\{(2,1),(7,1),\dots\}
\end{gathered}$$

---
###### 3. Wykaż, że dla relacji zwrotnej $R$, równość $R\circ R=R$ jest równoważna "przechodności" relacji $R$.

$$\begin{gathered}
R\circ R = R\implies \forall (x,y),(y,z)\in X\times Y: (x,y)\in grR
\ \ (x,z)\in grR\\\\
\text{Co jest definicją przechodności}
\end{gathered}$$

---
###### 8) Niech $p$ będzie elementem zbioru $X$. W zbiorze $2^X$ podzbiorów zbioru $X$ określamy relację $R=(2^X, grR, 2^X)$. Czy jest ona relacją równoważności?

$$\begin{gathered}
2^X=\{A: A\subseteq X\}\text{ - podzbiory zbioru X}
\\\\

grR:=\{(A,B)\in 2^X \times 2^X: (A=B)\vee (p\notin (A\cup B))\}\\\\
\text{Zbiory są ze sobą w relacji jeżeli są równe lub jakiś tam konkretny element nie należy do ich sumy.}\\\\
\text{Żeby to była relacja równoważności to:}\\
\forall x \in 2^X:\ xRx\\
\text{Jest to spełnione bo: }\forall A\in 2^X: A=A \Leftrightarrow ARA\\\\
\text{Musi być symetryczna: }\\
\forall x,y \in 2^X: xRy \implies yRx\\
\text{Jeżeli }xRy\text{ to oznacza że }x=y \vee p\notin (x\cup y)\\
x=y\implies y=x \land p\notin (x\cup y)\Leftrightarrow p\notin(y\cup x)\\\\
\text{Oraz przechodnia: }\\
\forall x,y,z \in 2^X: xRy \land yRz| x=y=z \vee p\notin (x\cup y\cup z)\implies x=z \vee p\notin (x\cup z)
\end{gathered}$$

---
###### 9) Dane jest odwzorowanie $f: \mathbb{R} \to \mathbb{R}$ takie, że $f(x)=x^3-x+2$. Niech $S=(\mathbb{R}, grS, \mathbb{R})$ będzie relacją taką, że $grS=\{(x,y): f(x)=f(y)\}$

a) Wykaż że $S$ jest relacją równoważności
$$\begin{gathered}
(a,b)\in grS \Leftrightarrow a^3-a+2=b^3-b+2\\\\
a^3-a=b^3-b\\\\
\forall x \in \mathbb{R}: f(a)=f(a) \Leftrightarrow xRx \ \text{ - zwrotność}\\\\
\forall x,y \in \mathbb{R}:( f(a)=f(b) \Leftrightarrow f(b)=f(a)) \leftrightarrow (aRb\leftrightarrow bRa)\\\\
\forall x,y,z: f(x)=f(y) \land f(y)=f(z) \Leftrightarrow f(x)=f(z) \leftrightarrow xRz
\end{gathered}$$

b) Niech $a\in \mathbb{R}$. Określ w zależności od $a$ liczebność klasy równoważności $[a]$

$$\begin{gathered}
f(x)=x^3-x+2\\
f'(x)=3x^2-1\\\\
3x^2-1\gt 0\\
x^2\gt \frac{1}{3}\\
x\gt \frac{1}{\sqrt{3}}\vee x\lt -\frac{1}{\sqrt{3}}\\\\
f(\frac{1}{\sqrt{3}})=\frac{1}{3\sqrt{3}}-\frac{3}{3\sqrt{3}}+\frac{6\sqrt{3}}{3\sqrt{3}}=\frac{4\sqrt{3}}{9}\\\\
f(-\frac{1}{\sqrt{3}})=-\frac{1}{3\sqrt{3}}+\frac{3}{3\sqrt{3}}+\frac{6\sqrt{3}}{3\sqrt{3}}=\frac{8\sqrt{3}}{9}\\\\
[a]=3\Leftrightarrow f(a)\in [\frac{4\sqrt{3}}{9},\frac{8\sqrt{3}}{9}] \\
[a]=1 \Leftrightarrow f(a)\notin [\frac{4\sqrt{3}}{9},\frac{8\sqrt{3}}{9}]
\end{gathered}$$
---
###### 13) Niech $S=(\mathbb{R}^2, grS, \mathbb{R}^2)$, gdzie: $(x_1,y_1)S(x_2,y_2)\Leftrightarrow \ln{(1+x_1^2+y_1^2)}=\ln{(1+x_2^2+y_2^2)}$. Czy tak określona relacja $S$ jest porządkiem w $\mathbb{R}^2$? Czy jest to relacja równoważności?

$$\begin{gathered}
\ln{(1+x_1^2+y_1^2)}=\ln{(1+x_2^2+y_2^2)}\\\\
x_1^2+y_1^2=x_2^2+y_2^2\\\\
\text{Zwrotność: } \\
x_1^2+y_1^2=x_1^2+y_1^2\\\checkmark\\\\
\text{Antysymetryczność: }\\
(x_1^2+y_1^2=x_2^2+y_2^2) \land 
(x_2^2+y_2^2=x_1^2+y_1^2)
\Leftrightarrow (x_1,y_1)=(x_2,y_2)?\\
\text{Nie, kontrprzykład: }\\
(2,3)R(3,2)\text{ bo: }2^2+3^2=3^2+2^2, \text{A }(3,2)\neq (2,3)\\\\
\text{ Jest relacją równoważności }
\end{gathered}$$

---
###### 1. Sprawdź jakie własności mają w $\mathbb{Z}$ następujące działania:
$$\begin{gathered}
\text{Łączne:}\\
a\circ b=a-b\\\\
(a\circ b)\circ z = a-b-z\\
a\circ (b\circ z)=a-(b-z)=a-b+z\\
\text{Zatem:}\\
(a\circ b)\circ z \neq a\circ (b\circ z)\\\\
\text{Przemienne:}\\
a\circ b=b\circ a\\
a-b\neq b-a\\
np. 2-3\neq 3-2\\\\
\text{Element neutralny:}\\
\text{Czy istnieje takie }e \in \mathbb{Z}\text{ że:}\\\\
\forall a\in \mathbb{Z}:a\circ e=e\circ a=e\\a-e=e-a=a\\\
a=e\\
\text{Element neutralny zależny od a więc nie ma jednego stałego neutralnego}
\end{gathered}$$


$$\begin{gathered}
a\circ b=a^2+b^2\\\\
\text{łączne:}\\
a\circ (b\circ c)=(a\circ b)\circ c\\
a^2+(b^2+c^2)^2\neq (a^2+b^2)^2+c^2\\\\\
\text{Przemienne:}\\
a\circ b=b\circ a\\
\checkmark\\\\
a\circ e = e\circ a = a\\
e=0\\
ale \ nie \ ma \ el. \ symetrycznych
\end{gathered}$$

---
###### 2) W zbiorze liczb rzeczywistych określamy działanie $x\circ y=x+y+xy$. Czy $(\mathbb{R},\circ)$ jest grupą? Czy jest grupą para $(\mathbb{R}\setminus \{-1\},\circ)$?

$$\begin{gathered}
\text{Żeby to była grupa to:}\\
1) \forall a,b,c \in \mathbb{R} : a\circ (b\circ c)=(a\circ b)\circ c\\
a\circ (b+c+bc)=(a+b+ab)\circ c\\
a+b+c+bc+ab+ac+abc=a+b+c+ab+ac+bc+abc\\
\checkmark\\\\
2) \exists e \in \mathbb{R} : \forall x \in \mathbb{R}\ \ \ x\circ e=e\circ x=x\\\\
x+e+xe=x+e+xe=x\\
e=0\\\\
3) \exists x' \forall x\in \mathbb{R} : x\circ x'=x'\circ x=e\\
x+x'+xx'=x+x'+xx'=0\\\\
x'(1+x)=-x\\
x'=\frac{-x}{1+x}\\\\
\text{Istnieje ale nie dla }x=-1\\\\
\text{Gdy wyrzucimy }x=-1 \text{ z zbioru, to tak jest to grupa.}
\end{gathered}$$

---
###### 3) W zbiorze liczb całkowitych określamy działanie: $x\circ y=x+y+2$. Czy $(\mathbb{Z}, \circ)$ jest grupą?

$$\begin{gathered}
1)a\circ (b\circ c)=(a\circ b)\circ c???\\
a\circ (b+c+2)=(a+b+2)\circ c\\
a+b+c+2+2=a+b+2+c+2\\
\checkmark\\\\
2) \exists e\in \mathbb{Z}: \forall x\in \mathbb{Z}:\ \ e\circ x=x\circ e=x\\\\
e+x+2=x+e+2=x\\
x+e+2=x\\
e=-2\\\\
3) \forall x\in \mathbb{R}\ \  \exists x': x\circ x'=x'\circ x=e\\\\
x+x'+2=x'+x+2=-2\\
x'+x+2=-2\\
x'+x=-4\\
x'=-4-x\\
\checkmark
\end{gathered}$$

---
###### 4) Które z następujących zbiorów liczb są grupami:

a) Liczby wymierne ze względu na dodawanie

$$\begin{gathered}
a+(b+c)=(a+b)+c\\ \checkmark\\
\forall a \in \mathbb{Q} \ \ a+e=e+a=a \Leftrightarrow e=0\\ \checkmark\\
\forall x \in \mathbb{Q}\ \  \exists x'\in \mathbb{Q}: x+x'=x'+x=0\\
x'=-x\\
\checkmark
\end{gathered}$$

ze względu na mnożenie

też, mnożenie można łączyć / jest przemienne, można pomnożyć przez 1 zawsze otrzymując to samo i można pomnożyć razy 1/x otrzymując 1

b) liczby niewymierne ze względu na dodawanie

nie bo element neutralny jest wymierny (0)

na mnożenie:
tak samo

c) liczby zespolone o module równym 1 ze względu na mnożenie

$$\begin{gathered}
1) \forall a,b,c \in \mathbb{C}: a\circ (b\circ c)=(a\circ b)\circ c\\\\
\text{Mnożąc liczby zespolone jeżeli zapiszemy je w postaci wykładniczej}\\
\text{Mnożymy moduły (1) i dodajemy do siebie kąty }\varphi \\
\text{Czyli wszystko sprowadza się do dodawania}\\
\text{A dodawanie jest grupą}
\end{gathered}$$

d) liczby zespolone o module równym 1 ze względu na następujące działanie: $z_1\circ z_2=|z_1|z_2$

$$\begin{gathered}
\forall a,b,c \in \mathbb{C}: a\circ (b\circ c)=a\circ (|b|c)=|a\cdot b| \cdot c=(a\circ b)\circ c=(|a|b)\circ c=|a\cdot b|\cdot c\\
\checkmark\\\\
\exists e \in \mathbb{C}:\forall a\in \mathbb{C}: a\circ e=e\circ a=a\\
|a|e=|e|a=a\\
|e|a=a\implies e=e^{i\varphi }\text{\ \ Dowolne bo moduł miał być równy 1}\\
|a|e=a\\
e=a\\
\text{e zalezne od a wiec nie jest takie samo dla kazdego a wiec nie jest to grupa}
\end{gathered}$$

---
###### 5) Niech $E_n$ będzie zbiorem wszystkich pierwiastków $n$-tego stopnia (w $\mathbb{C}$) z jedności. Udowodnij że $(E_n, \cdot)$ jest grupą.

$$\begin{gathered}
E_n=\{(\cos{(\frac{2k\pi}{n}})+i\sin{(\frac{2k\pi}{n})}\}\\\\
bo: \sqrt[n]{z}=\sqrt[n]{r}(\cos{(\frac{\varphi+2k\pi}{n})+i\sin{(\frac{\varphi+2k\pi}{n})}})\\
a \ 1=cos(0)+isin(0)\\\\
\text{Czyli znowu wszystko sprowadza się do dodawania i mnożenia}\\\\
\forall a,b,c\in E_n\ \ \ a\cdot (b\cdot c)=(a\cdot b)\cdot c\\
\sqrt[n]{r_a\cdot r_b\cdot r_c}\cdot 
e^{i(\varphi_a+\varphi_b+\varphi_c)}=\sqrt[n]{r_a\cdot r_b\cdot r_c}\cdot e^{i(\varphi_a+\varphi_b+\varphi_c)}\\\\
\exists e\in E_n: \forall a\in E_n\ \ \ a\cdot e=e\cdot a=a\\
e=1\\\\
\forall x\in E_n\ \exists x'\in E_n:x\cdot x'=x'\cdot x=e\\
x'=\frac{1}{x}\\
\checkmark 
\end{gathered}$$

---
###### 7) Niech $\Delta$ oznacza różnicę symetryczną, tj. dla dowolnych zbiorów $A$ i $B$, $A\Delta B:=(A\setminus B)\cup (B\setminus A)$. Sprawdź, czy dla dowolnie ustalonego zbioru $X\neq \emptyset$, para $(2^X, \Delta)$ jest grupą abelową.

$$\begin{gathered}
A\Delta B=(A\cup B)\setminus (A\cap B)\\\\
1) \forall a,b,c \in 2^X, \forall X\neq \emptyset :\\
a\Delta (b\Delta c)=(a\Delta b)\Delta c\\
\checkmark \\\
2) e=\emptyset \\
3) x'=x
\end{gathered}$$
---
###### 9) Czy następujące zbiory są ciałami ze względu na dodawanie i mnożenie:

$$\begin{gathered}
P=\{a+b\sqrt[3]{5}:a,b\in \mathbb{Q}\}\\
(P,+,\cdot )\\\\
1)\ (P,+) \text{ - grupa}\\
2)\ (P,\cdot )\text{ - przemienne}\\\\
(a+b\sqrt[3]{5})(c+d\sqrt[3]{5})=ac+ad\sqrt[3]{5}+bc\sqrt[3]{5}+bd(\sqrt[3]{5})^2\\
\text{Ze względu na }bd\sqrt[3]{5}^2 \text{ nie zawsze mnożenie jest "zamknięte" więc to nie jest}\\
\text{pierścień a co za tym idzie ciało}
\end{gathered}$$

---
$$\begin{gathered}
P=\{a: a\in \mathbb{Q} \land a\notin \mathbb{Z}\}\\
1) \dots\\
2) \neg \forall a,b \in P \ \ \ a\cdot b\in P\implies (P,+,\cdot )\text{ nie jest pierścieniem}\\
\text{kontrprzykład: }\frac{3}{2}\cdot \frac{2}{3}=1
\end{gathered}$$

---
$$\begin{gathered}
P=\{a+ib\sqrt{2}, \ a,b\in \mathbb{Q}\}\\
1) (P,+)\text{ grupa abelowa}\\
2) +,\cdot\text{ rozdzielne }\\
3) (P,\cdot )\text{ łączność}\\\\
\text{Pozostaje się dowiedzieć czy jest jedynka}\\
(a+ib\sqrt{2})(c+id\sqrt{2})=1\\
ac+iad\sqrt{2}+ibc\sqrt{2}-2bd=1\\
\left\{
\begin{matrix}
ac-2bd=1\\
ad+bc=0\\

\end{matrix}
\right.
\left\{
\begin{matrix}
ac-2bd=1\\
d=\frac{-bc}{a}\\

\end{matrix}
\right.
\left\{
\begin{matrix}
c=\frac{1}{a+\frac{2b^2}{a}}\\
d=\frac{-bc}{a}\\
\end{matrix}
\right.\\\\
\text{Istnieje element symetryczny działania multiplikatywnego}
\end{gathered}$$
---
###### 11) Udowodnij że odwzorowanie $f: x=a+b\sqrt{3}\to \overline{x}=a-b\sqrt{3}$ jest automorfizmem pierścienia $(A,+,\cdot)$ w siebie.

$$\begin{gathered}
f(x+y)=f(x)+f(y)?\\
f((a_1+a_2)+(b_1+b_2)\sqrt{3})=a_1-b_1\sqrt{3}+a_2-b_2\sqrt{3}\\
a_1+a_2-b_1\sqrt{3}-b_2\sqrt{3}=a_1-b_1\sqrt{3}+a_2-b_2\sqrt{3}\\\\
\checkmark\\\\
f(a\cdot b)=f(a)\cdot f(b)\\
f(a_1a_2+a_1b_2\sqrt{3}+a_2b_1\sqrt{3}+3b_1b_2)=a_1a_2+3b_1b_2-\sqrt{3}(a_1b_2+a_2b_1)=\\=f(a_1+b_1\sqrt{3})+f(a_2+b_2\sqrt{3})\\\\
f(x_1)=f(x_2)\Leftrightarrow x_1=x_2\text{ Iniekcja}\\
\text{Suriekcja}
\end{gathered}$$

---

###### 5) Zbadaj, które z układów wektorów należących do $\mathbb{R}^3$ są liniowo niezależne:

a) $B_1: (1,4,3,),(-1,2,1),(0,6,4)$
$$\begin{gathered}
\alpha(1,4,3)+\beta(-1,2,1)+\gamma (0,6,4)=\overline{0}\Leftrightarrow \alpha=\beta=\gamma=\boldsymbol{0}?\\\\
\left\{
\begin{matrix}
\alpha-\beta=0\\
4\alpha+2\beta+6\gamma =0\\
3\alpha+\beta+4\gamma=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\alpha=\beta\\
\alpha =-\gamma\\
4\alpha-4\alpha=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\alpha=\beta=t\\
\gamma=-t\\
\end{matrix}
\right.\\\\
\text{Dla testa:}\\
3(1,4,3)+3(-1,2,1)-3(0,6,4)=(0,0,0)\\\\
B_1 \text{ nie stanowi układy wektorów liniowo niezależnych}
\end{gathered}$$
---

b) $B_2: (2,3,-1),(2,0,0),(0,3,1)$
$$\begin{gathered}
\alpha(2,3,-1)+\beta(2,0,0)+\gamma(0,3,1)=\overline{0}=(0,0,0)\\
\Leftrightarrow\\
\alpha=\beta=\gamma=\boldsymbol{0}=0?\\\\
\left\{
\begin{matrix}
2\alpha+2\beta=0\\
3\alpha+3\gamma =0\\
-\alpha+\gamma=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\beta=0\\
\alpha =0\\
\gamma=\alpha=0
\end{matrix}
\right.\\\\
\text{Tak }B_2 \text{ stanowi układ wektorów liniowo niezleżnych}
\end{gathered}$$

---
c) $B_3: (2,-7,2),(0,2,4),(2,-1,5)$
$$\begin{gathered}
\alpha(2,-7,2)+\beta(0,2,4)+\gamma(2,-1,5)=\overline{0}=(0,0,0)\\
\Leftrightarrow\\
\alpha=\beta=\gamma=\boldsymbol{0}=0?\\\\
\left\{
\begin{matrix}
2\alpha+2\gamma=0\\
-7\alpha+2\beta-\gamma=0\\
2\alpha+4\beta+5\gamma=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\alpha=-\gamma\\
-6\alpha+2\beta=0\\
-6\alpha+4\beta=0
\end{matrix}
\right.
\left\{
\begin{matrix}
\gamma=0\\
\alpha=0\\
\beta=0
\end{matrix}
\right.\\
\text{Ta}\\\\
\alpha(2,-7,2)+\beta(0,2,4)+\gamma(2,-1,5)=(1,1,1)\\\\
\left\{
\begin{matrix}
\alpha=-\frac{1}{2}\\
\gamma=1\\
\beta=-\frac{3}{4}
\end{matrix}
\right.
\end{gathered}$$
---
###### 6) Sprawdź liniową zależność wektorów $\sqrt{2}$ i 2 w przestrzeni $(\mathbb{R},+,\cdot)$ nad ciałem $\mathbb{Q}$ oraz w przestrzeni $(\mathbb{R},+,\cdot)$ nad ciałem $\mathbb{R}$

$$\begin{gathered}
\alpha\cdot \sqrt{2}+\beta \cdot 2=0, \ \alpha,\beta \in \mathbb{Q}\\
\alpha\cdot \sqrt{2}+\beta\sqrt{2}\cdot \sqrt{2}=0\\
\beta\sqrt{2}=\alpha\implies \alpha,\beta \notin \mathbb{Q}\\
\text{Zatem jedyne rozwiązanie nie należy do zbioru ciała}\\
\text{Więc są to wektory liniowo niezależne w ciele o zbiorze }\mathbb{Q}\\
\text{jednakże istnieje rozwiązanie dla rzeczywistych }
\end{gathered}$$

---
###### 7) Dla jakiej wartości parametru $k$ wektor $v=(1,-2,k)\in \mathbb{R}^3$ jest kombinacją liniową wektorów $u_1=(1,1,1)$ i $u_2=(1,2,3)$ ?

$$\begin{gathered}
\alpha\cdot u_1+\beta\cdot u_2=v\\
\alpha\cdot (1,1,1)+\beta\cdot (1,2,3)=(1,-2,k)\\\\
\left\{
\begin{matrix}
\alpha+\beta=1\\
\alpha+2\beta =-2\\
\end{matrix}
\right.
\left\{
\begin{matrix}
\beta=-3\\
\alpha=4\\
\end{matrix}
\right.

\\\\
\alpha+3\beta=k\\
4+3\cdot -3=-5=k

\end{gathered}$$

---
###### 8) Sprawdź czy następujące funkcje są liniowo niezależne w przestrzeni $F(\mathbb{R}, \mathbb{R})$
a) $f(x)=x, g(x)=\sin{x}, h(x)=\cos{x}$
b) $f(x)=1,g(x)=\sin{x}, h(x)=\cos{x}, p(x)=sin^2{x}, q(x)=\cos^2{x}$

$$\begin{gathered}
ax+b\sin{x}+c\cos{x}=0\\
a+b\cos{x}-c\sin{x}=0\\
-b\sin{x}+c\cos{x}=0\\
-b\sin{0}+c\cos{0}=0 \implies c=0\\
-b\sin{\frac{\pi}{2}}+c\cos{\frac{\pi}{2}}=0\implies b=0\\
a+0\cos{x}-c\sin{x}=0\implies a=0\\\\
\end{gathered}$$
---
###### 10) Udowodnij że zbiór $A=\{(x_1,x_2,x_3,x_4)\in \mathbb{R}^4: x_1+x_2-3x_3-3x_4=0 \land x_1-x_2+3x_3+x_4=0\}$ jest podprzestrzenią przestrzeni $\mathbb{R}^4$. 

Czy podprzestrzeń?
$$\begin{gathered}
\forall a,b\in A \ \ \ a+b=(a_1+b_1,a_2+b_2,a_3+b_3,a_4+b_4):\\
a_1+b_1+a_2+b_2-3a_3-3b_3-3a_4-3b_4=\\=(a_1+a_2-3a_3-3a_4)+(b_1+b_2-3b_3-3b_4)=0+0=0\\
\checkmark\\
\\
\forall \alpha \in \mathbb{R}, \forall x \in A\ \ \ \ \alpha\cdot x=
(\alpha x_1,\alpha x_2, \alpha x_3, \alpha x_4): \alpha (x_1+x_2-3x_3-3x_4)=0\\
\checkmark\\\\
\end{gathered}$$
Wyznacz bazę:
$$\begin{gathered}
\left\{
\begin{matrix}
x_1+x_2-3x_3-3x_4=0\\
x_1-x_2+3x_3+x_4=0
\end{matrix}
\right.\
\left\{
\begin{matrix}
x_1=x_4\\
x_2=-2x_4-3x_3\\
\end{matrix}
\right.
\
\left\{
\begin{matrix}
x_1=x_4=s\\
x_2=-2s-3t\\
x_3=t
\end{matrix}
\right.\\\\
s(1,-2,0,1)+t(0,-3,1,0)\\\\
B=\{(1,-2,0,1),(0,-3,1,0)\}\\
\end{gathered}$$
---
###### 11) Dane są dwa układy wektorów: $B_1:(1,i,1+i),(i,-1,2-i),(0,0,3)$ i $B_2:(2i,1,0),(2,-i,1),(0,1+i,1-i)$.

a) Sprawdź czy któryś z tych układów stanowi bazę przestrzeni $\mathbb{C}^3(\mathbb{C})$ lub $\mathbb{C}^3(\mathbb{R})$

$$\begin{gathered}
\alpha(1,i,1+i)+\beta(i,-1,2-i)+\gamma(0,0,3)=(x,y,z)\\\\
\left\{
\begin{matrix}
\alpha+\beta i=x\\
\alpha i -\beta=y=i(\alpha +i\beta)=ix\\
\end{matrix}
\right.\\\\
\text{Zatem ten układ wektorów generuje jedynie te z wektorów z przestrzeni}\\
\mathbb{C}^3(\mathbb{C})\text{ które spełniaja }ix=y \text{ zatem nie jest to baza}\\\\
\alpha(2i,1,0)+\beta(2,-i,1)+\gamma(0,1+i,1-i)=(x,y,z)\\\\
\left\{
\begin{matrix}
2\alpha i+2\beta=x\\
\alpha-i\beta+\gamma +i\gamma =y\\
\beta+\gamma-i\gamma =z
\end{matrix}
\right.\
\left\{
\begin{matrix}
2\alpha i+2\beta=x\\
\gamma=\frac{y-x}{(2i-2)}\\
\beta+\gamma-i\gamma =z
\end{matrix}
\right.\\\\
\text{Jest to baza}\\\\
\text{Można to było łatwiej udowodnić na podstawie tego że sa liniowo niezależne}\\
\text{a z twierdzenia mówiącego że jeżeli zbiór wektorów liniowo niezależnych}\\
\text{ ma taki sam rozmiar jak wymiar zbioru to jest on bazą}\\\\
\left\{
\begin{matrix}
i\alpha=-\beta\\
\alpha-i\beta+(1+i)\gamma=0\\
\beta+\gamma(1-i)=0
\end{matrix}
\right.\\
\left\{
\begin{matrix}
\alpha=i\beta\\
\gamma=0\\
\beta=0\\
\alpha=0
\end{matrix}
\right.
\end{gathered}$$

---
###### 12) Niech będzie dana następująca podprzestrzeń $U$ przestrzeni wektorowej $\mathbb{C}^2(\mathbb{R})$, gdzie $p$ jest pewną liczbą rzeczywistą:

$$\begin{gathered}
U:=Lin\{(pi,(p-1)i),(p-2-pi,p),(-1-pi,2p)\}
\end{gathered}$$
Zbadaj dla jakich wartości parametru rzeczywistego $p$, zachodzi:
$$\begin{gathered}
(3-2p,p-1+(1-p)i)\in U
\end{gathered}$$

$$\begin{gathered}
U=\alpha(pi,pi-i)+\beta(p-2-pi,p)+\gamma(-1-pi,2p), \alpha,\beta,\gamma\in \mathbb{R}\\\\

\left\{
\begin{matrix}
\alpha pi+\beta p-2\beta -2\beta pi-\gamma -\gamma pi =3-2p\\
\alpha pi-i\alpha +\beta p+2\gamma p=p-1+i-pi
\end{matrix}
\right.\\
i(\alpha p-2\beta p-\gamma p)-2\beta-\gamma=3-2p\implies\\ \implies
(p=0 \vee \alpha-2\beta-\gamma=0) \land -2\beta-\gamma=3\\\\
\land\\
i(\alpha p-\alpha)+\beta p+2\gamma p=p-1+i(1-p)\implies\\
\alpha(p-1)=1-p\land \beta p+2\gamma p=p-1\\\\
p(\beta + 2\gamma-p)=1 \implies p\neq 0\\\\

\left\{
\begin{matrix}
\alpha-2\beta-\gamma=0\\
-2\beta-\gamma=3\\
\alpha(p-1)=1-p\\
p(\beta+2\gamma-1)=-1
\end{matrix}
\right.\ \ 
\left\{
\begin{matrix}
\alpha-2\beta-\gamma=0\\
-2\beta-\gamma=3\\
(\alpha+1)(p-1)=0\implies p=1\vee \alpha=-1\\
p(\beta+2\gamma-1)=-1
\end{matrix}
\right.\\\\
\text{z 1 i 2 równania wiemy że }\alpha\neq -1 \text{zatem }p=1\\\\
\left\{
\begin{matrix}
\alpha=-3\\
\gamma=1\\
p=1\\
\beta=-2
\end{matrix}
\right.\\
\end{gathered}$$

Dla wszystkich takich wartości parametru $p\in \mathbb{R}$, wyznacz $\dim U$
$$\begin{gathered}
p=1\\
U:=Lin\{(i,0),(-1-i,1),(-1-i,2)\}\\\\
\alpha(i,0)+\beta(-1-i,1)+\gamma(-1-i,2)=\overline{0}\Leftrightarrow\alpha=\beta=\gamma=0?\\\\
\left\{
\begin{matrix}
\alpha i-\beta-i \beta-\gamma-i \gamma=0\\
\beta+2\gamma=0
\end{matrix}
\right.
\left\{
\begin{matrix}
i(\alpha-\beta-\gamma) -\beta-\gamma=0\\
\beta+2\gamma=0
\end{matrix}
\right.
\\\\
\left\{
\begin{matrix}
i(\alpha-\beta-\gamma)=0\\
-\beta-\gamma=0\\
\beta+2\gamma=0
\end{matrix}
\right.

\\\\
\left\{
\begin{matrix}
\alpha=0\\
\beta=0\\
\gamma=0\\
\end{matrix}
\right.\\\\
\dim U=3
\end{gathered}$$

---
###### 14) W przestrzeni wielomianów $\mathbb{R}[x]_2$ dana jest baza $B_1=(1,x,x^2)$. Wykaż, że układ $B_2=(1,x-2,(x-2)^2)$ stanowi bazę $\mathbb{R}[x]_2$. Podaj współrzędne wielomianu $P(x)=2x^2+3$ względem obu baz. Czy zbiór $A=\{p\in \mathbb{R}[x]_2: p(1)=p'(0)\}$ stanowi podprzestrzeń tej przestrzeni? Jeżeli tak, wyznacz jej bazę i wymiar.

Wykaż, że układ $B_2=(1,x-2,(x-2)^2)$ stanowi bazę $\mathbb{R}[x]_2$:

$$\begin{gathered}
\text{Na mocy twierdzenia że każdy zespół n wektorów liniowo niezależnych}\\
\text{w V generuje nam V.}\\\\
\text{Wystarczy że sprawdzimy czy są liniowo niezależne}\\\\
\alpha\cdot 1+\beta(x-2)+\gamma(x-2)^2=\overline{0}\Leftrightarrow \alpha=\beta=\gamma=0\\
\alpha\cdot 1+\beta(x-2)+\gamma(x-2)^2=\alpha+\beta x-2\beta+\gamma x^2-4\gamma x+4\gamma

\\\\
\left\{
\begin{matrix}
\alpha-2\beta+4\gamma=0\\
\beta-4\gamma=0\\
\gamma=0
\end{matrix}
\right.\\
\left\{
\begin{matrix}
\alpha=0\\
\beta=0\\
\gamma=0
\end{matrix}
\right.\\\\
\checkmark
\end{gathered}$$
Podaj współrzędne wielomianu $P(x)=2x^2+3$ względem obu baz:

$$\begin{gathered}
\text{Względem pierwszej bazy:}\\
(3,0,2)\\\\
\alpha\cdot 1+\beta(x-2)+\gamma(x-2)^2=2x^2+3\\\\
\left\{
\begin{matrix}
\alpha-2\beta+4\gamma=3\\
\beta-4\gamma=0\\
\gamma=2
\end{matrix}
\right.\\\\
\left\{
\begin{matrix}
\alpha=11\\
\beta=8\\
\gamma=2
\end{matrix}
\right.\\\\
(11,8,2)
\end{gathered}$$

Czy zbiór $A=\{p\in \mathbb{R}[x]_2: p(1)=p'(0)\}$ stanowi podprzestrzeń tej przestrzeni? 

$$\begin{gathered}
p(1)=\alpha+\beta+\gamma\\
p'(0)=\beta\\\\
\alpha+\beta+\gamma=\beta\\
\alpha=-\gamma\\
A=\{p:\mathbb{R}[x]_2:p=\alpha+\beta x-\alpha x^2, \alpha,\beta\in \mathbb{R}\}\\\\
\forall p_1,p_2\in A\ \ \ p_1+p_2=\alpha_1+\alpha_2+(\beta_1+\beta_2)x-(\alpha_1+\alpha_2)x^2\in A\\\\
\forall a\in \mathbb{R}, \forall p\in A \\ \alpha\cdot p\in A
\end{gathered}$$

Wyznacz jej bazę i wymiar:

$$\begin{gathered}
\alpha(1,0,-x^2)+\beta(0,1,0)=p\implies \dim V=2\land B=\{(1,0,-x^2),(0,1,0)\}
\end{gathered}$$

---
###### 1) Zbadaj rzędy następujących macierzy:
$$\begin{gathered}
A=\begin{bmatrix}
2&6&-1&4&3\\
1&4&2&-1&0\\
0&-2&-5&6&3\\
3&10&1&3&3
\end{bmatrix}\\\\
\downarrow\\\\
A=\begin{bmatrix}
-2&6&-1&4&3\\
0&10&1&3&3\\
0&0&0&0&0\\
0&0&0&0&0
\end{bmatrix}\\
r(A)=2\\\\
\end{gathered}$$
$$\begin{gathered}
B=\begin{bmatrix}
3&1&2&-1&7\\
-3&-1&-1&4&2\\
0&1&0&2&1\\
3&2&2&1&8\\
0&1&1&5&4
\end{bmatrix}\\\\
\downarrow\\\\\
B=\begin{bmatrix}
3&1&2&-1&7\\
0&1&1&5&4\\

0&0&1&3&9\\
0&0&0&0&6\\
0&0&0&0&0\\

\end{bmatrix}
\end{gathered}$$

$$\begin{gathered}
C=\begin{bmatrix}
2&1&1&1\\
1&3&1&1\\
1&1&4&1\\
1&1&1&5\\
1&2&3&4\\
1&1&1&1
\end{bmatrix}\\\\
\downarrow\\\\
C=\begin{bmatrix}
2&1&1&1\\
0&6&2&2\\
0&0&12&66\\
0&0&0&-64\\
0&0&0&0\\
0&0&0&0
\end{bmatrix}
\end{gathered}$$

---
###### 2) Wyznacz rzędy następujących macierzy w zależności od parametru rzeczywistego $p$$:

$$\begin{gathered}
A=\begin{bmatrix}
1-p&2&1&p\\
1&2-p&1&0\\
1&2&1-p&p
\end{bmatrix}\\\\
A=\begin{bmatrix}
-2p&2&1&0\\
0&2-p&1&0\\
0&0&0&p
\end{bmatrix}\\\\
r(A)=1\Leftrightarrow p=1\\
r(A)=3 \Leftrightarrow p\neq 1
\end{gathered}
$$
###### 3) Dla jakich wartości parametru $a \in \mathbb{R}$, rząd macierzy jest najmniejszy, a dla jakich największy.

$$\begin{gathered}
A=\begin{bmatrix}
-2&-1-a&1\\
a&0&-a\\
-1&a+a^2&1
\end{bmatrix}
\\\\
\downarrow \ R_3-aR_1, \ K_2\leftrightarrow K_1\\\\
A=\begin{bmatrix}
-1-a&-2&1\\
0&a&-a\\
0&-1+2a&1-a
\end{bmatrix}
\\\\
\downarrow\ K_2+2K_3
\\\\
A=\begin{bmatrix}
-1-a&0&0\\
0&-a&0\\
0&0&1-a
\end{bmatrix}
\\\\
\downarrow\\
a=-1\implies r(A)=2\\
a=0\implies r(A)=2\\
a\notin \{-,1,0\}\implies r(A)=3

\end{gathered}$$
---
###### 4) Oblicz wyznacznik macierzy i jeśli jest ona nieosobliwa, znajdź macierz do niej odwrotną:

$$\begin{gathered}
\begin{vmatrix}
1&0&1\\
1&1&2\\
0&1&1
\end{vmatrix}=
\begin{vmatrix}
1&0&1\\
0&1&1\\
0&0&0
\end{vmatrix}=0
\end{gathered}
$$
$$\begin{gathered}
\begin{vmatrix}
1+i&-1\\
0&2
\end{vmatrix}=2+2i\\\\

\begin{vmatrix}
\begin{array}{cc|cc}
1&0&\frac{1+i}{2}&\frac{1+i}{4}\\
0&1&0&\frac{1}{2}
\end{array}
\end{vmatrix}
\end{gathered}
$$

---
###### 5) Niech $A$ będzie macierzą kwadratową. Udowodnij że:

a) jeżeli $A^2-A+I=0$, to $A$ jest nieosobliwa i $A^{-1}=I-A$

$$\begin{gathered}
A(A-I)=-I\\\\
\left\{
\begin{matrix}
A(I-A)=I\\
AA^{-1}=I\
\end{matrix}\implies A^{-1}=I-A
\right.\\

\end{gathered}$$
b) jeżeli $A^k=\boldsymbol{0}$, to $(I-A)^{-1}=I+A+A^2+\dots+A^{k-1}$

$$\begin{gathered}
(I-A)(I-A)^{-1}=(I-A)(I+A+A^2+\dots+A^{k-1})=\\
=I+A+A^2+\dots+A^{k-1}-A-A^2\dots -A^k=I\\
\checkmark
\end{gathered}$$
###### 6) Jakie są możliwe wartości wyznacznika macierzy rzeczywistej $A$ stopnia $n$, jeżeli:

a) $A^2=A^T$

$$\begin{gathered}
\det{A^2}=\det{A^T}\\
(\det{A})^2=\det A\\
d^2-d=0\\
d(d-1)=0\\
d=0 \vee d=1
\end{gathered}$$
b) $A^T=A^{-1}$

$$\begin{gathered}
A^TA=I\\
d^2=1\\
d=1\vee d=-1
\end{gathered}$$

---
###### 8) Niech będzie dany następujący podzbiór $N$ zbioru $M_{2\times 2}(\mathbb{C})$. Sprawdź, czy para $(N,\cdot)$, gdzie "$\cdot$" oznacza mnożenie macierzy, jest grupą abelową.

$$\begin{gathered}
N=\left\{\begin{bmatrix}
x&ix\\
-ix&x
\end{bmatrix}:x\in \mathbb{R}\setminus \{0\}
\right\}
\end{gathered}
$$

Żeby pewna struktura była grupą abelową to:

1. musi być łączne działanie 
2. musi istnieć element neutralny
3. element symetryczny dla każdego
4. przemienność

$$\begin{gathered}
1)\\
\text{Mnożenie macierzy jest łączne}\\
4)\\
\begin{bmatrix}
a&ia\\
-ia&a
\end{bmatrix}\cdot 
\begin{bmatrix}
b&ib\\
-ib&b
\end{bmatrix}=
\begin{bmatrix}
2(a\cdot b)&2i(a\cdot b)\\
-2i(a\cdot b)&2(a\cdot b)
\end{bmatrix}\\\\
\text{więc przemienne bo mnożenie przemienne}\\\\
2)\

e=\begin{bmatrix}
\frac{1}{2}&i\frac{1}{2}\\
-i\frac{1}{2}&\frac{1}{2}
\end{bmatrix}\\\\
3) x'=
\begin{bmatrix}
\frac{x}{2}&i\frac{x}{2}\\
-i\frac{x}{2}&\frac{x}{2}
\end{bmatrix}\\\\
\end{gathered}$$

ta to grupa abelowa

---
###### Dla dowolnych liczb zespolonych $z,z'\in \mathbb{C}$ oznaczamy:
$$\begin{gathered}
z\circ z'=Im(z)\cdot Re(z')+Re(z)+i\cdot Im(z)\cdot Im(z')\\
\text{lub równoważnie:}\\
(x+iy)\circ (x'+iy')=yx'+x+iy'y
\end{gathered}$$
Sprawdź, czy dla:
$$\begin{gathered}
A:=\{z\in \mathbb{C}: Im (z)\neq 0\}
\end{gathered}$$
para $(A,\circ)$ tworzy grupę

Żeby to była grupa to musi być łączne, el. neutr, i symetryczne:

$$\begin{gathered}
z\circ e=e\circ z=z\\
(x+iy)\circ (e_x+ie_y)=ye_x+x+ie_yy\\
(e_x+ie_y)\circ (x+iy)=e_yx+e_x+iye_y\\\\

\left\{
\begin{matrix}
ye_x+ie_yy=iy\\
e_yx+e_x+iye_y=x+iy
\end{matrix}\implies e_y=1, e_x=0
\right.\\\\
e=i\\\\
\text{Czy dla kazdego }x \exists x': x\circ x'=x'\circ x=e\\
yx'+x+iy'y=y'x+x'+iyy'=i\\
\left\{
\begin{matrix}
yx'+x+iy'y=i\\
y'x+x'+iyy'=i\\
\end{matrix}\implies y'=\frac{1}{y}
\right.\\
\left\{
\begin{matrix}
yx'+x=0\\
\frac{1}{y}x+x'=0\\
\end{matrix}
\right.\implies x'\in \mathbb{C}\\\\
\forall x\in \mathbb{C}: x=(a+bi) \ \ \exists x': x'=(c+\frac{1}{b}i)
\end{gathered}$$

Podaj definicje podprzestrzeni przestrzeni liniowej oraz twierdzenie o równoważnej charakterystyce podprzestrzeni. Udowodnij ich równoważność.

$$\begin{gathered}
U-\text{przestrzeń liniowa o skalarach ze zbioru }A\\
K-\text{podprzestrzeń U}\\
\text{K jest podprzestrzenią przestrzeni liniowej U}\Leftrightarrow
\forall a,b\in K \ \ a+b\in K\\
K\subset U, \forall \alpha \in A, \forall v \in K \ \ \ \alpha \cdot k \in K
\\\\
\text{twierdzenie o równoważnej charakterystyce przestrzeni mówi że te warunki}\\
\text{możemy zredukować do warunków:}\\
K\subset U \land \forall \alpha,\beta \in A, \forall v_1,v_2\in K \ \ \ 
\alpha \cdot v_1+\beta\cdot v_2\in K\\\\
\text{Dowód równoważności:}\\\\
\beta=0\implies \alpha v_1+0\cdot v_2\in K\\
\alpha,\beta=1\implies v_1+v_2\in K
\end{gathered}$$

---
###### 1) Rozwiąż układy równań:

$$\begin{gathered}
\left\{
\begin{matrix}
x_1+x_2+x_3+x_4+x_5=8\\
x_1-x_2-x_3+x_4+x_5=0\\
2x_1-x_2+2x_3-x_4+2x_5=7\\
x_1-4x_2+x_3-2x_4-x_5=-9\\
-x_1+x_2-x_3+x_4+x_5=2\\
\end{matrix}
\right.\Leftrightarrow

\begin{bmatrix}
\begin{array}{ccccc|c}
1&1&1&1&1&8\\
1&-1&-1&1&1&0\\
2&-1&2&-1&2&7\\
1&-4&1&-2&-1&-9\\
-1&1&-1&1&1&2
\end{array}
\end{bmatrix}\\\\\\
\begin{bmatrix}
\begin{array}{ccccc|c}
1&1&1&1&1&8\\
0&-2&-2&0&0&-8\\
0&0&1&-1&0&1\\
0&0&0&4&-4&-4\\
0&0&0&0&2&4
\end{array}
\end{bmatrix}\\\\
\left\{
\begin{matrix}
x_5=2\\
x_4=1\\
x_3=2\\
x_2=2\\
x_1=1
\end{matrix}
\right.
\end{gathered}
$$


$$\begin{gathered}
\left\{
\begin{matrix}
x_1+x_2+x_3+x_4+x_5=8\\
x_1-x_2-x_3+x_4+x_5=0\\
2x_1-x_2+2x_3-x_4+2x_5=7\\
x_1-4x_2+x_3-2x_4-x_5=-9\\
-x_1+x_2-x_3+x_4-x_5=-2
\end{matrix}
\right.\Leftrightarrow

\begin{bmatrix}
\begin{array}{ccccc|c}
1&1&1&1&1&8\\
1&-1&-1&1&1&0\\
2&-1&2&-1&2&7\\
1&-4&1&-2&-1&-9\\
-1&1&-1&1&-1&-2
\end{array}
\end{bmatrix}\\\\
\begin{bmatrix}
\begin{array}{ccccc|c}
1&1&1&1&1&8\\
0&-2&-2&0&0&-8\\
0&0&10&-6&-4&38\\
0&0&0&4&-4&-52\\
0&0&0&0&0&-150\\
\end{array}
\end{bmatrix}\text{sprzeczny na podstawie twierdzenia kronecker-capallie}
\end{gathered}
$$


$$
\begin{gathered}
\left\{
\begin{matrix}
-3x+6y-3z=2\\
3x-6y+3z=-3
\end{matrix}
\right.\text{    sprzeczne}
\end{gathered}
$$
$$\begin{gathered}
\left\{
\begin{matrix}
2x+y=-3\\
3x+4y=1\\
5x-y=6
\end{matrix}
\right.\Leftrightarrow

\begin{bmatrix}
\begin{array}{cc|c}
2&1&-3\\
3&4&1\\
5&-1&6
\end{array}
\end{bmatrix}\\\\\\
\begin{bmatrix}
\begin{array}{cc|c}
0&0&-\frac{40}{14}\\
0&1&-\frac{1}{14}\\
1&0&\frac{6}{14}
\end{array}
\end{bmatrix}\text{ sprzeczny}

\end{gathered}
$$

$$\begin{gathered}
\left\{
\begin{matrix}
2x_1+7x_2+3x_3+x_4=6\\
3x_1+5x_2+2x_3+2x_4=4\\
9x_1+4x_2+x_3+7x_4=2
\end{matrix}
\right.\Leftrightarrow
\begin{bmatrix}
\begin{array}{cccc|c}
2&7&3&1&6\\
3&5&2&2&4\\
9&4&1&7&2
\end{array}
\end{bmatrix}\\\\
\begin{bmatrix}
\begin{array}{cccc|c}
3&5&2&2&4\\
0&11&5&-1&10\\
0&0&0&0&0
\end{array}
\end{bmatrix}, \\\\
\text{ na podstawie twierdzenia mówiącego że jeżeli }r(A)=r(A|B)=r\lt n\\
\text{to układ jest nieoznaczony, zależnie od }n-r \text{ parametrów:}\\\\
x_3=s, x_4=t\\
\left\{
\begin{matrix}
3x_1+5x_2+2s+2t=4\\
11x_2+5s-t=10\\
x_3=s\\
x_4=t
\end{matrix}
\right.
\end{gathered}$$

---
###### 2) Znajdź bazę podprzestrzeni wektorowej przestrzeni $\mathbb{R}^3$ rozwiązań następującego układu:

$$\begin{gathered}
\left\{
\begin{matrix}
x+2y-z=0\\
2x+7y-2z=0\\
-x+3y+z=0
\end{matrix}
\right.\\\\
\begin{bmatrix}
\begin{array}{ccc|c}
1&2&-1&0\\
0&1&0&0\\
0&0&0&0
\end{array}
\end{bmatrix}\\
\left\{
\begin{matrix}
x_2=0\\
x_1=x_3
\end{matrix}
\right.\\\\
B=\{(1,0,1)\}
\end{gathered}
$$
###### 3) Zbadaj w zależności od parametru $k$ ilość rozwiązań układu równań:
$$\begin{gathered}
\left\{
\begin{matrix}
kx+y+z=1\\
x+ky+z=k\\
x+y+kz=k^2
\end{matrix}
\right.
\\\\
\det(A)=\begin{vmatrix}
k&1&1\\
1&k&1\\
1&1&k
\end{vmatrix}=k\begin{vmatrix}
k&1\\
1&k
\end{vmatrix}-1
\begin{vmatrix}
1&1\\
1&k
\end{vmatrix}+
1\begin{vmatrix}
1&k\\
1&1
\end{vmatrix}=\\\\
=k(k^2-1)-(k-1)+(1-k)=k(k-1)(k+1)-2(k-1)=\\\\
=(k-1)(k^2+k-2)\\\\
k=1\vee k=-2\\\\
\text{Układ jest układem Cramera czyli }\det(A)\neq 0\\
\text{gdzie A to jest macierz niewiadomych (bez wyrazów wolnych)}\\
\text{dla }k=1\vee k=-2\\
\text{a wtedy na podstawie twierdzenia ma dokładnie jedno rozwiązanie}\\\\
\text{Pozostało podstawić k=1,k=-2 do tego i sprawdzić ile ma wtedy rozwiązań.}
\end{gathered}$$

---
###### 1) Sprawdź czy:

a) wektory $u=[-1,3,-5]$, $v=[1,-1,1]$, $w=[4,-2,0]$ są współpłaszczyznowe

$$
\begin{gathered}
(u\times v)\circ w=
\begin{vmatrix}
i&j&k\\
-1&3&-5\\
1&-1&1
\end{vmatrix}\circ w=[-2,-4,-2]\circ [4,-2,0]=-16\neq 0\\\\
\implies u,v,w \text{ nie są współpłaszcyznowe}
\end{gathered}
$$

b) punkty $P=(0,0,0)$, $Q=(-1,2,3)$, $R=(2,3,-4)$, $S=(2,-1,5)$ są współpłaszczyznowe

$$\begin{gathered}
\vec{PQ}=[-1,2,3], \ \vec{PR}=[2,3,-4], \ \vec{PS}=[2,-1,5] \\\\
\begin{vmatrix}
-1&2&3\\
2&3&-4\\
2&-1&5\\
\end{vmatrix}=-80\neq 0
\end{gathered}$$

---
###### 2) Trójkąt $ABC$ rozpięty jest na wektorach $\vec{AB}=[1,5,-3], \vec{AC}=[-1,0,4]$. Oblicz wysokość tego trójkąta opuszczoną z wierzchołka $C$.

$$\begin{gathered}
d=\vec{AB}\times \vec{AC}=
\begin{vmatrix}
i&j&k\\
1&5&-3\\
-1&0&4
\end{vmatrix}=[20,-1,5]\\\\
|d|=\sqrt{426}\\\\
P_{\triangle}=\frac{|d|}{2}\\\\
|AB|=\sqrt{1+25+9}=\sqrt{35}\\\\
H=\frac{P_\triangle}{2|AB|}
\end{gathered}$$

---
###### 3) Proste $l_1$ i $l_2$ dane są równaniami parametrycznymi:

$$\begin{gathered}
l_1:\left\{
\begin{matrix}
x=1-4t\\
y=-2t\\
z=2+4t
\end{matrix}
\right., \ \ \ \ t\in \mathbb{R},  \ \ \ \ 
l_2:\left\{
\begin{matrix}
x=6+6t\\
y=4+3t\\
z=-6t
\end{matrix}
\right.
\end{gathered}$$

Wykaż, że $l_1$ i $l_2$ są równoległe. Oblicz odległość między nimi. Znajdź równanie ogólne ich wspólnej płaszczyzny.

$$\begin{gathered}
t_1=[-4,-2,4], t_2=[6,3,-6]\\\\
t_1=-\frac{3}{2}t_2, \text{zatem są równoległe}\\\\
\text{Jeżeli proste są równoległe to odległość między nimi jest odległością}\\
\text{punktu położonego na jednej z tych prostych do drugiej prostej}\\
d(P,l)=\frac{||\overrightarrow{P_0P}\times v||}{||v||}\\\\
d(l_1,l_2)=d(P,l)=\frac{||[5,4,-2]\times [6,3,-6]||}{\sqrt{81}}=
\frac{||[-18,18,-9]||}{9}=\frac{27}{9}=3
\end{gathered}$$
---
###### 5) Zbadaj wzajemne położenie prostych

$$\begin{gathered}
l_1:\left\{
\begin{matrix}
x=1+2t\\
y=t\\
z=2
\end{matrix}
\right.\ \ \ \ t\in \mathbb{R}\ \ \ \ 
l_2:\left\{
\begin{matrix}
x=3\\
y=t\\
z=-t
\end{matrix}
\right.\\\\
AB=(2,0,-2)\\\\
\begin{vmatrix}
2&1&0\\
0&1&-1\\
2&0&-2
\end{vmatrix}=-6\neq 0\implies \text{proste nie są współpłaszczyznowe}
\end{gathered}$$

---
###### 6) Napisz równanie ogólne płaszczyzny $\pi$ przechodzącej przez punkty $A=(-1,2,4), B=(2,1,3), C=(3,-1,5)$. Wyznacz odległość punktu $Q=(5,0,8)$ od płaszczyzny $\pi$ oraz znajdź punkt symetryczny od punktu $Q$ względem tej płaszczyzny.

$$\begin{gathered}
AB=[3,-1,-1], \ AC=[4,-3,1]\\\\
n=\begin{vmatrix}
i&j&k\\
3&-1&-1\\
4&-3&1
\end{vmatrix}=[-4,-7,-5]\\\\
\pi: [x-3,y+1,z+1]\circ [-4,-7,-5]=0\\\\
-4x+12-7y-7-5z-5=0\\
-4x-7y-5z=0
\end{gathered}$$

$$\begin{gathered}
d(P,\pi)=\frac{|Ax+By+Cz+D|}{\sqrt{A^2+B^2+C^2}}=\frac{60}{\sqrt{90}}=
2\sqrt{10}
\end{gathered}$$

$$\begin{gathered}
\text{normalizacja wektora do długości }4\sqrt{10}\text{ czyli odległości punktu Q pomnożonej razy 2}\\\\
\text{o ile trzeba pomnożyć wektor n by był tej długości?}\\\\
a\cdot \sqrt{90}=4\sqrt{10}\\
a\cdot 3\sqrt{10}=4\sqrt{10}\\
a=\frac{4}{3}\\\\
Q'=Q+\frac{4}{3}\cdot n\\\\
Q'=(5,0,8)+[-4,-7,-5]\cdot \frac{4}{3}=(5,0,8)+[\frac{-16}{3},-\frac{28}{3},-\frac{20}{3}]=(-\frac{1}{3},-\frac{28}{3},\frac{4}{3})

\end{gathered}$$

---
###### 2) Dane są w przestrzeni $E_3$ wierzchołki czworościanu $ABCD$ 
$$\begin{gathered}
A=(1,3,2),\ B=(1,5,4), \ C=(3,3,4), \ D=(4,6,2)
\end{gathered}$$

Wyznacz miarę kąta wewnętrznego trójkąta $ABC$ przy wierzchołku $A$ 

$$\begin{gathered}
\vec{AB}=(0,2,2), \ \vec{AC}=(2,0,2)\\\\

\cos{\varphi}=\frac{u\circ v}{||u||\cdot ||v||}\\\\
\cos{\angle A}=\frac{0+0+4}{\sqrt{8}\cdot \sqrt{8}}=\frac{1}{2}\implies \angle A=\frac{\pi}{3}
\end{gathered}$$

Wyznacz równanie ogólne płaszczyzny $\pi$ zawierającej podstawę $ABC$ danego czworościanu oraz rzut prostokątny $D'$ wierzchołka $D$ na tę płaszczyznę.

$$\begin{gathered}
\left\{
\begin{matrix}
x=1+t(0,2,2)+s(2,0,2)\\
y=3+t(0,2,2)+s(2,0,2)\\
z=2+t(0,2,2)+s(2,0,2)
\end{matrix}
\right.\\\\
n=t\times s=\begin{vmatrix}
i&j&k\\
0&2&2\\
2&0&2
\end{vmatrix}=[4,4,-4]\\\\
\pi:(x-x_0,y-y_0,z-z_0)\circ n=4x-4+4y-4-4z+4=4x+4y-4z-4=0\\\\
d(D,\pi)=\frac{|Ax_1+By_1+Cz_1+D|}{\sqrt{A^2+B^2+C^2}}\\\\
d(D,\pi)=\frac{|16+24-8-4|}{\sqrt{16+16+16}}=\frac{28}{4\sqrt{3}}=\frac{7\sqrt{3}}{3}\\\\

a\cdot |n|=\frac{7\sqrt{3}}{3}\\
a\cdot 4\sqrt{3}=\frac{7\sqrt{3}}{3}\\
a=\frac{7}{12}\\\\

D'=D+n\cdot 2a=(4,6,2)+\frac{7}{6}\cdot [4,4,-4]=
\end{gathered}$$

$$\begin{gathered}
(\frac{24}{6},\frac{36}{6},\frac{12}{6})+\frac{7}{6}[4,4,-4]=(\frac{52}{6},\frac{64}{6},-\frac{16}{6})
\end{gathered}$$


---
Oblicz ile razy dłuższa jest wysokość główna danego czworościanu wychodząca z wierzchołka $D$ od odległości między prostymi zawierającymi krawędzie $AB$ i $CD$.

$$\begin{gathered}
H=d(D,\pi)=\frac{|16+24-8-4|}{\sqrt{16+16+16}}=\frac{7\sqrt{3}}{3}\\\\
d(l_1,l_2)=\frac{|(v_1\times v_2)\circ \overrightarrow{P_1P_2}|}{||v_1\times v_2||}\\\\
\overrightarrow{P_1P_2}=[3-1,3-3,4-2]=[2,0,2]\\\\
(v_1\times v_2)=
\begin{vmatrix}
i&j&k\\
0&2&2\\
1&3&-2
\end{vmatrix}=[-10,2,-2]\\\\
d(l_1,l_2)=\frac{24}{6\sqrt{3}}=\frac{4\sqrt{3}}{3}\\\\
\frac{H}{d(l_1,l_2)}=\frac{7\sqrt{3}}{3}\cdot \frac{3}{4\sqrt{3}}=\frac{7}{4}
\end{gathered}
$$