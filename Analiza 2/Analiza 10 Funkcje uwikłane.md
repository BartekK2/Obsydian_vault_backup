### Funkcje uwikłane
#### 2025-05-28
##### Poprzednia: [[Analiza 9 Ekstrema warunkowe]]
##### Następna: [[Analiza 11 Całeczki]]
##### Zadania: [[Zadania rachunek różniczkowy]]

#rachunek_różniczkowy #funkce_uwikłane #funkcje_wielu_zmiennych #analiza2  

---
### Definicja 

##### Funkcja uwikłana to taka funkcja, której postać nie jest wyrażona jawnie w postaci $y=f(x)$, lecz jest określona pośrednio przez równanie zależności między zmiennymi np.:
$$\begin{gathered}
F(x,y)=0
\end{gathered}$$
##### wtedy zamiast bezpośredniego wzoru na $y$ w zależności od $x$, relacja między nimi określona jest przez to równanie.

###### Globalnie: nie zawsze da się przekształcić $F(x,y)=0$ na prostą postać y=f(x) dla całego zbioru wartości.

###### Lokalnie (w małym otoczeniu punktu $(x_0,y_0)$ - czasem się da.) Twierdzenie o funkcji uwikłanej powie nam, kiedy to jest możliwe.

**Formalnie:**
Niech $X,Y$ będą przestrzeniami unormowanymi $D\subseteq X\times Y$ oraz $f: D\to Y$ będzie ciągła. Każdą funkcję $\varphi: U\to Y$ gdzie $U$ jest pewnym podzbiorem $X$, spełniającą dla każdego $x\in U$ równanie $f(x,\varphi(x))=0$ nazywamy **funkcją uwikłaną** funkcjji $f$ albo funkcją uwikłaną określoną przez równanie $f(x,y)=0$.

**Przykład 1:**

$$\begin{gathered}
x^2+y^2=1\\
(x_0,y_0)=(0,1)\\
y=\sqrt{1-x^2}
\end{gathered}$$
**Przykład 2:**
$$\begin{gathered}
x^2y-xy^2=0\\
xy(x-y)=0
\end{gathered}$$
**Przykład 3:**
$$\begin{gathered}
xe^y-ye^x-e^{xy}=0
\end{gathered}$$

---
### WW na istnienie funkcji uwikłanej

Zał: $F: D\to \mathbb{R} \ \ \ D\subseteq \mathbb{R}^2$
$F(x,y)=0$
$F(x_0,y_0)=0$
$U$ - otoczenie punktu $(x_0,y_0)$
$F\in C^1(U)$
$\frac{\partial F}{\partial y}(x_0,y_0)\neq 0$

Teza: 
1) istnieje takie otoczenie $V$ punktu $x_0$ i takie otoczenie $W$ punktu $y_0$ oraz istnieje taka funkcja $y=V\to W$, że $\forall x \in V \ \ F(x,y(x))=0$
(czyli istnieje funkcja uwikłana $y=y(x)$ dana równaniem $F(x,y)=0$ w otoczeniu punktu $(x_0,y_0)$)

2) Ponadto 
   $y'(x_0)=-\frac{\frac{\partial F}{\partial x}(x_0,y_0)}{\frac{\partial F}{\partial y}(x_0,y_0)}$

3) A jeżeli $F\in C^2(U)$ oraz $y'(x_0)=0$
   to: $y''(x_0)=-\frac{\frac{\partial^2 F}{\partial x^2}(x_0,y_0)}{\frac{\partial F}{\partial y}(x_0,y_0)}$
---
### Twierdzenie o różniczkowalności funkcji złożonej 

Zał: $f: D\to \mathbb{R}^k, \ \ \ D\subset \mathbb{R}^n$
$g: E\to \mathbb{R}^m, \ \ \ E\subset \mathbb{R}^k$
$h=g\circ f: \ \ \ D\to \mathbb{R}^m$
$f$ jest różniczkowalna w $x_0\in U\in D$
$g$ jest różniczkowalna w $f(x_0)=y_0\in V \subset E$
Teza: funkcja złożona $g\circ f$ jest różniczkowalna w $x_0$ i $d(g\circ f)(x_0)=dg(y_0)\circ df(x_0)$

---
