
### Odwzorowania liniowe
#### 2025-01-30
##### Poprzednia: [[Algebra - 11]]
##### Następna: [[Algebra - 13]]
##### Zadania: [[]]

#odwzorowania_liniowe #algebra 

---
### Definicja 

**Def.**
Niech $V,W$ będą [[Algebra - 6#Definicja przestrzeni wektorowej|przestrzeniami wektorowymi]] nad **tym samym ciałem** $K$. **Odwzorowanie**:
$$\begin{gathered}
f: V\to W
\end{gathered}$$
nazywamy **liniowym** jeżeli:
$$\begin{gathered}
\forall u,v \in V: f(u+v)=f(u)+f(w)\\
\forall v\in V, \forall \alpha \in K: f(\alpha v)=\alpha \cdot f(v)
\end{gathered}$$
**Wniosek:**
Jeżeli $f: V\to W$ jest odwzorowaniem **liniowym**, to:
$$\begin{gathered}
\text{wektor zerowy pierwszej przestrzeni zamienia się na wektor zerowy drugiej}\\
f(\overline{0}_v)=\overline{0}_w\\\\
\forall v\in V: f(-v)=-f(v)
\end{gathered}$$
**Prosty przykład odwzorowania liniowego:** $f: \mathbb{R}^2 \to \mathbb{R}^2$ - symetria względem osi y=x
![[diagram-20250130 (1).png]]

---
**Przykład:**

Sprawdź dla jakich $a,b \in \mathbb{R}$ funkcja $f: \mathbb{R} \to \mathbb{R}$, gdzie $f(x)=ax+b$, określa odwzorowanie liniowe:

$$\begin{gathered}
1) \ f(x_1+x_2)=f(x_1)+f(x_2)\\
f(x_1+x_2)=a(x_1+x_2)+b=ax_1+b+ax_2+b\implies b=0\\\\
2)f(\alpha x)=\alpha f(x)\\
f(\alpha x)=a\alpha x+b=\alpha ax+b\implies a\in \mathbb{R}
\end{gathered}$$

---
**Równoważne założenia odwzorowania liniowego:** 

Podobnie jak w podprzestrzeniach wektorowych dwa warunki związane z sumą i iloczynem przez skalar zawarliśmy w [[Algebra - 6#Równoważna charakterystyka podprzestrzeni|jednym warunku]] tutaj również można tak zrobić:

$$\begin{gathered}
f: V\to W - odwzorowanie \ liniowe \Leftrightarrow\\\\
f(\alpha x_1+\beta x_2)=\alpha f( x_1)+\beta f( x_2)
\end{gathered}$$

**Dowód analogiczny do tego z podprzestrzeni:**
$$\begin{gathered}
\text{Zakładając }\alpha=\beta=1:\\
f(\alpha x_1+\beta x_2)=\alpha f( x_1)+\beta f( x_2)\to f(x_1+x_2)=f(x_1)+f(x_2)\\\\
\text{Zakładając }x_2=\overline{0}\\
f(\alpha x_1+\beta x_2)=\alpha f( x_1)+\beta f( x_2)=\alpha f(x_1)+\beta \overline{0}_W=\alpha f(x_1)=f(\alpha x_1)
\end{gathered}$$
---
**Przykład:**
Sprawdź czy $f: \mathbb{R}^3 \to \mathbb{R}^2$, gdzie $f(x,y,z)=(2x+y-z,x-3z)$ określa odwzorowanie liniowe:

$$\begin{gathered}
f(\alpha v_1+ \beta v_2)=f([\alpha x_1+\beta x_2, \alpha y_1+\beta y_2, \alpha z_1+\beta z_2])=\\=(2\alpha x_1+2\beta x_2+\alpha y_1+\beta y_2-\alpha z_1-\beta z_2, \alpha x_1+\beta x_2-3\alpha z_1-3\beta z_2)\\\\

\alpha f(v_1)+\beta f(v_2)=\alpha [2x_1+y_1-z_1,x_1-3z_1]+\beta [2x_2+y_2-z_2, x_2-3z_2]=\\
=[2\alpha x_1+\alpha y_1-\alpha z_1+2\beta x_2+\beta y_2-\beta z_2, \alpha x_1-3\alpha z_1+\beta x_2-3\beta z_2]\\\\
f(\alpha v_1+\beta v_2)=\alpha f(v_1)+\beta f(v_2) \checkmark \implies f - odwzorowanie \ liniowe
\end{gathered}$$

---
**Twierdzenie:**

Pierwotną definicje można bardziej rozciągnąć korzystając z własności przestrzeni wektorowych, sumy i iloczynu skalarów z wektorami:

$$\begin{gathered}
\forall v_1,v_2,\dots v_n\in V \ \forall \alpha_1,\alpha_2,\dots,\alpha_n\in K:\\\\
f(\alpha_1v_1+\alpha_2v_2+\dots+\alpha_nv_n)=\alpha_1f(v_1)+\alpha_2f(v_2)+\dots +\alpha_nf(v_n)
\end{gathered}$$

**Wniosek:**
Odwzorowanie liniowe $f$ jest **jednoznacznie określone** przez **wartości $f$ na wektorach bazowych z dziedziny** bo możemy wybrać wektory z bazy, z których kombinacją liniową tworzymy każdy wektor należący do podprzestrzeni $V$.

---
### Obraz i jądro

**Def.**

Niech $f: V\to W$ będzie odwzorowaniem liniowym.
-  **Jądrem** odwzorowania $f$ nazywamy zbiór:
$$\begin{gathered}
Kerf:=\{v\in V:f(v)=\overline{0}_W\}
\end{gathered}$$
- **Obrazem odwzorowania** $f$ (**zbiorem wartości**) nazywamy zbiór:
$$\begin{gathered}
Imf:=\{w\in W:\exists v\in V: w=f(v)\}
\end{gathered}$$

**Twierdzenie:**
$Kerf$ jest podprzestrzenią wektorową przestrzeni $V$
$Imf$ jest podprzestrzenią wektorową przestrzeni $W$

---
##### Wymiary obrazu i jądro 

**Wniosek:**
Jeżeli $f: V\to W$ jest odwzorowaniem liniowym, a $B$ jest bazą przestzeni $V$, to:
$$\begin{gathered}
Imf=Linf(B)
\end{gathered}$$
(bo przecież z bazy możemy wygenerować każdy wektor z $V$)

**Def.**

**Wymiar obrazu** odwzorowania liniowego $f$ (jeżeli jest skończony) nazywamy **rzędem odwzorowania** $f$ i oznaczamy $r(f)$, gdzie $r(f)=\dim Imf$

---

**Przykład:**
Wyznacz jądro i obraz, oraz ich bazy i wymiary, odwzorowania liniowego $f:\mathbb{R}^3\to \mathbb{R}^2$, gdzie $f(x,y,z)=(2x+y-z,x-3z)$

$$\begin{gathered}
Kerf=\{(x,y,z)\in \mathbb{R}^3: f(x,y,z)=\overline{0}_W=(0,0)\}\\\\
(2x+y-z,x-3z)=0\\\\
\left\{
\begin{matrix}
2x+y-z=0\\
x-3z=0
\end{matrix}
\right.
\left\{
\begin{matrix}
y=-5z\\
x=3z\\
z\in \mathbb{R}
\end{matrix}
\right.\\\\
Kerf=\{(3z,-5z,z):z\in \mathbb{R}\}=\{z(3,-5,1): z\in \mathbb{R}\}=Lin(\{3,-,5,1\})\\\\
B_{Kerf}=\{(3,-5,1)\}\implies dim Kerf=1\\\\
\end{gathered}$$
$$\begin{gathered}
Imf=\{w\in W: \exists v\in V: f(v)=w\}\\\\
Imf=\{(2x+y-z,x-3z): x,y,z\in \mathbb{R}\}\\\\
Imf=\{x(2,1)+y(1,0)+z(-1,-3): x,y,z\in \mathbb{R}\}=Lin\{(2,1),(1,0),(-1,3)\}\\\\
gdzie: (-1,3)\ mozna \ wygenerowac \ za \ pomoca \ (2,1),(1,0)\\\\
\text{zatem}\\
B_{Imf}=\{(2,1),(1,0)\}\implies \dim Imf=2
\end{gathered}$$

---
**Twierdzenie:**

Zakładając że $V,W$ to przestrzenie wektorowe nad ciałem $K$, $\dim V\lt \infty$, a $f:V\to W$ to odwzorowanie liniowe:
$$\begin{gathered}
\dim V=\dim Kerf+\dim Imf
\end{gathered}$$

---
### Rodzaje odwzorowań liniowych

Mówimy że odwzorowanie $f: V\to W$ jest:

- **monomorfizmem**, jeżeli jest **injektywne** (różnowartościowe)
  Czyli $f(v_1)=f(v_2) \Leftrightarrow v_1=v_2$
  
- **epimorfizmem**, jeżeli jest **surjektywne** ($Imf=W$)
  Dla każdego wektora $w$ w $W$ istnieje wektor $v$ w $V$ taki że $f(v)=w$
  
- **izomorfizmem**, jeżeli jest **bijektywne**
  Czyli takie które jest jednocześnie monomorfizmem i epimorfizmem
  
- **endomorfizmem**, jeżeli $V=W$ 
  Po prostu działamy na tych samych zbiorach.
  
- **automorfizmem**, jeżeli jest **endomorfizmem bijektywnym**
  Czyli taki endomorfizm który jest jednocześnie izomorfizmem, oraz istnieje takie odwzorowanie które cofnie pierwotne odwzorowanie.
  
- **formą liniową**, jeżeli $W=K$
  Czyli wektor z podprzestrzeni ze zbioru $V$ którego skalary są $K$ to jest to odwzorowanie które taki wektor zamienia na skalar. Np takie odwzorowanie które zwraca sume składowych wektora. $f((x,y,z))=x+y+z$

---
**Twierdzenia:**

Niech $f:V\to W$ będzie odwzorowaniem liniowym, gdzie $\dim V=n, \dim W=m$. Wówczas:
1) $f$ jest **epimorfizmem** $\Leftrightarrow$ $r(f)=m$ 
2) następujące warunki są równoważne:
   - $f$ jest **automorfizmem**
   - $Kerf=\{\overline{0}\}$
   - $r(f)=n$

---
### Przestrzenie izomorficzne

**Def.**
Dwie przestrzenie wektorowe $V$ i $W$ nad tym samym ciałem $K$ nazywamy **izomorficznymi**, jeżeli **istnieje izomorfizm** (dwa wektory wygenerują to samo tylko wtedy kiedy są równe i każdy wektor z $W$ da się wygenerować) jednej przestrzeni na drugą, co zapisujemy $V \textasciitilde W$. 

**Uwaga:**
Jeżeli $f:V\to W$ jest **izomorfizmem** to $f^{-1}: W\to V$ też jest **izomorfizmem**

**Twierdzenie:**
Z: $V,W$ - przestrzenie wektorowe o skończonych wymiarach nad ciałem $K$
T: $V\textasciitilde W \Leftrightarrow \dim V=\dim W$

**Twierdzenie:**
Niech $V,W$ będą (ustalonymi) przestrzeniami wektorowymi nad ciałem $K$. Struktura $(L(V,W),K,+,\cdot)$, gdzie:
$$\begin{gathered}
L(V,W):=\{f: V\to W| f- odwzorowanie \ liniowe\}
\end{gathered}$$
+, oznacza dodawanie odwzorowań, a $\cdot$ mnożenie odwzorowań przez skalary z ciała $K$, jest **przestrzenią wektorowymi**.

**Uwaga:**
Złożeniem odwzorowań liniowych jest odwzorowaniem liniowym.

---
