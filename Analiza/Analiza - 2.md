### Funkcje elementarne, odwrotne do tryg.
#### 2024-10-09
##### Zadania: [[Analiza zadania - indukcja, złożenie, granice ciągu i funkcji, ciągłość]]
##### Następna: [[Analiza - 3]]
##### Poprzednia: [[Analiza - 1]]

#arcusy #analiza #funkcje_elementarne #ciagi #granice
konsultacje 13-15 p. 305b A3- A4

--- 
### Funkcje elementarne:
##### 1.  Wielomiany:
$$\begin{gathered}
f(x)=a_nx^n+...+a_0
\end{gathered}$$
##### 2. Wymierne:
$$\begin{gathered}
f(x)=\frac{p(x)}{q(x)}, \ f(x), \ q(x) \ - \ wielomiany \\
Przyklad:\\\\
y=\frac{2x-3}{x-2}\\\\
x=-2, \ as. \ pionowa \ wynika \ z \ dziedziny \\
y=2, \ as. \ pozioma \ bo \ \frac{2}{1}=2

\end{gathered}$$

##### 3. Potęgowa:
$$\begin{gathered}
f(x)=x^a, \ a \in \mathbb{R} \\
Dziedzina \ zalezy \ od \ a: \\
np: \ f(x)=x^{-\frac{1}{2}}=\sqrt{x}, \ \mathbb{D}=[0,+\infty]\\
lub: \ f(x)=x^{-a}=\frac{1}{x^a}, \ \mathbb{D}=\mathbb{R}-\{0\}
\end{gathered}$$
##### 4. Wykładnicza:
$$\begin{gathered}
f(x)=a^x, \ a\gt 0, \ a\neq1\\
f: \mathbb{R} \rightarrow (0,+\infty)
\end{gathered}$$

##### 5. Logarytmiczna:
$$\begin{gathered}
c=\log_a{b} \leftrightarrow a^c=b, \ a\gt0, \ a\neq0, \ b\gt 0\\
f(x)=\log_ax, \ \mathbb{D}: (0, +\infty)\\
f: (0,+\infty) \rightarrow \mathbb{R}\\\\
\ln x=log_ex, \ e=2,71...  \ - \ stala \ Eulera
\end{gathered}$$

##### 6. Funkcje cyklometryczne (odwrotne do tryg.)
###### $\arcsin{x}$:
Całego sinusa nie da się odwrócić bo nie jest różnowartościowy
ale "kawałek" od $[-\frac{\pi}{2}, \frac{\pi}{2}]$ możemy

---

$\sin{x}$
![[diagram-20241012 (2).png]]

---

$\arcsin{x}$
![[diagram-20241012 (4).png]]

---

**Jest to funkcja odwrotna do sinusa więc jak sinus dla danego x daje y to arccos dla  y daje parametr x. Innymi słowy odpowiedzią na pytanie dla jakiego x sinus jest równy $\frac{\sqrt{3}}{2}$ jest: $x=\arcsin{\frac{\sqrt{3}}{2}}$.**

$$\begin{gathered}
\sin: [-\frac{\pi}{2}, \frac{\pi}{2}] \rightarrow [-1,1]\\
\arcsin: [-1,1] \rightarrow [-\frac{\pi}{2}, \frac{\pi}{2}]\\
y=\arcsin{x}, x\in[-1,1] \leftrightarrow \sin{y}=x \land y\in [-\frac{\pi}{2}, \frac{\pi}{2}] \\
\end{gathered}$$
Przykłady:
$\arcsin{1}=\frac{\pi}{2} \ bo \ sin{\frac{\pi}{2}}=1$
$\arcsin{2} \ - \ nie \ istnieje.$
$\arcsin{\frac{1}{2}}=\frac{\pi}{2} \ bo \ sin{\frac{\pi}{2}}=\frac{1}{2}$

###### $\arccos{x}$:
**Analogicznie, z tym że nasz wybrany kawałek to $[0,\pi]$ (żeby zawrzeć wszystkie możliwe wartości - tak jak w $\arcsin{x}$)**

$$\begin{gathered}
\cos: [0,\pi] \rightarrow [-1,1]\\
\arccos: [-1,1] \rightarrow [0,\pi]\\
y=\arccos{x}, x\in[-1,1] \leftrightarrow x=\cos{y} \land y\in[0,\pi]\end{gathered}$$

---
$\cos{x}$
![[diagram-20241012 (3).png]]

---
$\arccos{x}$
![[diagram-20241012 (5).png]]

---

###### $\arctan{x}$
**Analogicznie, jednakże należy pamiętać o tym że tanges nie ma ograniczonego zbioru wartości - więc jego arcus nie ma ograniczonej dziedziny tj:**

$$\begin{gathered}
\tan{x}: (-\frac{\pi}{2},\frac{\pi}{2}) \rightarrow \mathbb{R}\\
\arctan{x}: \mathbb{R} \rightarrow (-\frac{\pi}{2}, \frac{\pi}{2})\\
y=\arctan{x}, x\in \mathbb{R} \leftrightarrow x=\tan{x} \land y \in (-\frac{\pi}{2}, \frac{\pi}{2})\end{gathered}$$
---
$\tan{x}$
![[diagram-20241013.png]]

---
$\arctan{x}$
![[diagram-20241013 (2).png]]

---
###### $arcctg{x}$ 
Analogicznie do $\arctan{x}$.

---
##### Podstawowe tożsamości:
$\arcsin{x} + \arccos{x} = \frac{\pi}{2}$
$\arctan{x} + arcctg{x} = \frac{\pi}{2}$

Wynikają one z tego że cosinus z sinusem, tanges z cotangensem to praktycznie te same funkcje przesuniete o $\frac{\pi}{2} \ tzn. \  \sin{(x+\frac{\pi}{2})} = \cos{x}$

No i oczywiście:
$\sin{(\arcsin{y})}=y, \ \arcsin{(sin{x})}=x$

---
**Jeżeli nie pamiętamy jaki jest wykres funkcji cyklometrycznej wystarczy obrócić sobie wykres jej funkcji trygonometrycznej o 90$\degree$ i odbić lustrzanie.

---
**Złożenie, suma, różnica, iloczyn, iloraz dowolnej ale skończonej liczby funkcji elementarnych jest funkcją elementarną**

---
### Ciągi:

$a(n) \equiv a_n$

Ciąg to funkcja określona na zbiorze liczb naturalnych $\mathbb{N}$

---
#### Monotoniczność ciągu:

Ciąg $a_n$ jest *rosnący* $\Leftrightarrow \forall n \in \mathbb{N} \ a_{n+1} \gt a_n$
Ciąg $a_n$ jest *malejący* $\Leftrightarrow \forall n \in \mathbb{N} \ a_{n+1} \lt a_n$
Ciąg $a_n$ jest *niemalejący* $\Leftrightarrow \forall n \in \mathbb{N} \ a_{n+1} \geq a_n$
Ciąg $a_n$ jest *nierosnący* $\Leftrightarrow \forall n \in \mathbb{N} \ a_{n+1} \leq a_n$

Czyli następne elementy *ZAWSZE* są w pewnej nierówności do poprzednich.
###### Przykład udawadniania monotoniczności:
Czy ciąg o wyrazie ogólnym $a_n = \sqrt{n+1} - \sqrt{n}$ jest monotoniczny?
$$\begin{gathered}
a_{n+1} \leq a_n \\
\end{gathered}$$
Więc ciąg $a_n$ jest malejący. (Ciężko to wykazać w tym przypadku na podstawie $a_{n+1}-a_n$, więc można np. korzystać z pochodnej lub męczyć się z upraszczaniem do momentu aż mianownik na pewno będzie dodatni i sprawdzimy znak licznika) 

---
#### Ograniczenia ciągu:

Mówimy że ciąg jest ograniczony *z góry* jeżeli istnieje taka liczba od której ciąg zawsze będzie mniejszy:
$$\begin{gathered}
a_n \ ograniczony \ z \ gory \Leftrightarrow \exists M \in \mathbb{R} \ \forall n \in \mathbb{N} \ a_n \leq M\\
\end{gathered}$$

A *z dołu* analogicznie czyli jeżeli ciąg jest zawsze większy od pewnej liczby to jest przez nią ograniczony:
$$\begin{gathered}
a_n \ ograniczony \ z \ dolu \Leftrightarrow \exists m \in \mathbb{R} \ \forall n \in \mathbb{N} \ a_n \geq m
\end{gathered}$$
Natomiast mówimy że jest *ograniczony* wtedy i tylko wtedy kiedy jest zarówno ograniczony *z dołu* jak i *z góry*.
###### Przykład wykazywania czy jest ograniczony:
Czy ciąg o wyrazie ogólnym $a_n=\sqrt{n+1}-\sqrt{n}$ jest ograniczony?
Wiem że ciąg jest monotoniczny więc tu wystarczy że oblicze pierwszy wyraz dla granicy górnej, wiem też że jest malejący ale $a_n \gt 0, \ \forall n \in \mathbb{N}$
$$\begin{gathered}
a_0 = 1, \ ograniczony \ z \ gory \ przez \ 1\\
\lim_{n \to \infty } a_n = 0, \ ograniczony \ z \ dolu \ przez \ 0
\end{gathered}$$
---
#### Granice:

*KAŻDY CIĄG MONOTONICZNY I OGRANICZONY MA OKREŚLONĄ GRANICE*

*Def. Couchy'ego granicy ciągu:*
$$ \lim_{a_n \to \infty} a_n=g \leftrightarrow \forall \epsilon \gt 0 \ \ \exists n_0 \in \mathbb{N} \ \  \forall n \geq n_0 \ |a_n-g| \lt \epsilon  $$

Innymi słowy ciąg ma granice g wtedy i tylko wtedy kiedy dla każdego $\epsilon$ większego od zera istnieje taki wyraz, dla którego każdy następny będzie w mniejszej odległości od g niż wybrany przez nas $\epsilon$.

---
*Twierdzenie o jednoznaczności granicy*
Jeśli ciąg posiada granicę, to tylko *jedną*.

---
*Twierdzenie o zachowaniu **słabej** nierówności*

Jeżeli zauważymy że ciąg zawsze jest mniejszy niż pewna liczba $M$ dla każdego $n_0$ większego od $n$ (czyli ograniczamy go) to granica musi być równa lub mniejsza danemu ograniczeniu (lub analogicznie większa).

$\exists M \in \mathbb{R} \ \exists n_0 \in \mathbb{N} \ \forall n \geq n_0 \ a_n \leq M \ \land \ \lim_{n \to \infty} a_n = g) \implies g \leq M$

*Czyli po prostu granica jest mniejsza lub równa ograniczeniu.*

---
*Kryterium zbieżności Couchy'ego / Alemberta*

1. $\lim_{n \to \infty}{\sqrt[n]{|a_n|}}\lt 1 \implies lim_{n \to \infty}{a_n}=0 \ \ \ Couchy$
2. $\lim_{n \to \infty}{|\frac{a_{n+1}}{a_n}|} \lt 1 \implies \lim_{n \to \infty} a_n=0 \ \ \ Alambert$
###### Przykład zastosowania
Oblicz $\lim_{n \to \infty}{\frac{n^2}{2^n}}$
$$\begin{gathered}
a_n = \frac{n^2}{2^n}\\
\frac{a_{n+1}}{a_n} = \frac{(n+1)^2}{2^{n+1}} \cdot \frac{2^n}{n^2}=\frac{n^2+2n+1}{2n^2}\\
lim_{n \to \infty}{|\frac{a_{n+1}}{a_n}|}=\frac{1}{2} \lt 1 \implies \lim_{n \to \infty}{a_n} = 0
\end{gathered}$$
---
*Granice $\sqrt[n]{a}$*
1. $\lim_{n \to \infty}{\sqrt[n]{a}} = 1, \ \ a \gt 0$
2. $\lim_{n \to \infty}{\sqrt[n]{n}} = 1, \ \ w \ szczegolnosci$
---
*Twierdzenie o działaniach arytmetycznych na ciągach*
Założenia: $\lim_{n \to \infty} a_n=a, \lim_{n \to \infty} b_n=b$
Twierdzenie: ^6a1c39
$$\begin{gathered}
1. \lim_{n \to \infty}{(a_n \pm b_n)}=\lim_{n\to \infty} a_n \pm \lim_{n \to \infty }{b_n}=a\pm b\\
2. \lim_{n \to \infty}{(a_n \cdot b_n)}=\lim_{n\to \infty} a_n \cdot \lim_{n \to \infty }{b_n}=a\cdot b\\
3. \lim_{n \to \infty}{\frac{a_n}{b_n}}=\frac{\lim_{n\to \infty} a_n}{ \lim_{n \to \infty }{b_n}}=\frac{a}{b} \ (oczywiscie \ jesli \ b_n \neq 0 )\\
\end{gathered}$$

---
*Twierdzenie o trzech ciągach:*
Jeżeli ciąg $a_n$ i $c_n$ mają taką samą granice ale każdy wyraz $n$ tych ciągów jest mniejszy bądź równy od $b_n$ dla $c_n$ i większy bądź równy od $b_n$ dla $a_n$ to $b_n$ ma taką samą granice jak te ciągi: ^89a611

$$\begin{gathered}
1. \ lim_{n \to \infty} a_n=\lim_{n \to \infty} c_n=g \\
2. \ \exists n_0 \ \forall n\gt n_0:  a_n\leq b_n \leq c_n\\
\\ lim_{n \to \infty} \ \ \  b_n = g 
\end{gathered}$$
Przykład:
$$\begin{gathered}
b_n = \sqrt[n]{n+2^n} \\ 
lim_{n \to \infty} b_n = ?\\
\\
a_n=\sqrt[n]{2^n}, \ c_n=\sqrt[n]{2\cdot2^n}\\
lim_{n \to \infty} a_n = 2, \ \lim_{n \to \infty} c_n = 2 \implies \lim_{n \to \infty} c_n = 2

\end{gathered}$$
---
*Twierdzenie o ciągu ograniczonym i zbieżnym do 0:*
Założenia
1. $a_n$ - ograniczony
2. $\lim_{n \to \infty} b_n = 0$
Teza:
$\lim_{n\to \infty}{a_n \cdot b_n} = 0$
###### Przykład:
Oblicz granicę ciągu $\frac{n^2 \sin{n}}{n^3+2n-1}$:
$$\begin{gathered}
a_n=\sin{n}\\\\
b_n = \frac{n^2}{n^3+2n-1}\\
\lim_{n \to \infty}{b_n} = \frac{1}{n+\frac{2}{n}-\frac{1}{n^2}}=\frac{1}{n}=0\\\\
\lim_{n \to \infty}{\frac{n^2 \sin{n}}{n^3+2n-1}} = \lim_{n \to \infty}{(a_n \cdot b_n)} = 0 
\end{gathered}$$
---
#### Stała Eulera:
1. $lim_{n \to \infty}{(1+\frac{1}{n})}^n=e=2,718...$
2. Analogicznie dla $a_n$:  $\lim_{n \to \infty}{(1+\frac{1}{a_n})^{a_n}} = e$
---
#### Symbole nieoznaczone:

^669a6f

$[\frac{0}{0}], [\frac{\infty}{\infty}], [0\cdot \infty], [1^{\infty}], [0^0], [\infty^0]$
---
### Podciągi:
*Def.* $(a_n)_{n \in \mathbb{N}}$ - ciąg
Ciąg $(a_{n_k})_{k \in \mathbb{N}}$ nazywamy podciągiem ciągu $(a_n)_{n \in \mathbb{N}}$ 
###### Przykład
$a_n = 1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4},...,\frac{1}{n}$
$n_k: 2,4,6,... czyli \ n_k=2k$
$a_{n_k}=\frac{1}{2}, \frac{1}{4}, \frac{1}{6}...$
$(a_{2k})_{k \in \mathbb{N}}: \ a_{2k}=\frac{1}{2k}$ 
---
#### Twierdzenie o granicy podciągu
Jeśli $\lim_{n\to \infty}{a_n} = g$ to dla każdego podciągu $\lim_{k \to \infty}{a_{n_k}} = g$
Więc jeśli ciąg jest zbieżny do g, to każdy podciąg tego ciągu też jest zbieżny do g (ale nie w drugą strone).

---
#### Wniosek z poprzedniego twierdzenia - Twierdzenie o różnych granicach podciągu implikujących że ciąg nie jest zbieżny.

Jeśli istnieją dwa podciągi $(a_{n_k}), \ (a_{n_i})$ ciągu $(a_n)$ takie, że $\lim_{k\to \infty}{a_{n_k}} \neq \lim_{i\to \infty}{a_{n_i}}$ to ciąg $(a_n)$ nie jest zbieżny.
###### Przykład
Pokaż że ciąg $a_n=cos(n\pi)$ nie jest zbieżny.
$a_{n_k}, \ n_k=2k$
$\lim_{k \to \infty}{a_{n_k}} = 1$
$a_{n_i}, \ n_i=2i+1$
$\lim_{n_i \to \infty}{a_{n_i}} = -1$
![[diagram-20241031.png]]

---
#### Tw. Bolzano-Weierstrassa
Jeśli ciąg jest ograniczony, to ma podciąg zbieżny (do granicy właściwej).
(Granica właściwa - to taka która jest liczbą)

*Prz.*
Z ciągu $a_n=n$ nie da się wybrać podciągu zbieżnego (do granicy właściwej).

---
#### Limes Superior, Limes Inferior
$\lim_{n \to \infty}{sup \ a_n} = sup\{g: g \ jest \ granica \ podciagu \ zbieznego \ ciagu \  a_n\}$
$\lim_{n \to \infty}{inf \ a_n} = inf\{g: g \ jest \ granica \ podciagu \ zbieznego \ ciagu \ a_n\}$

Innymi słowy $sup \ a_n$ jest największą z granic każdego z podciągów. (Dla $\cos{x}$ jest to 1).
Analogicznie $inf \ a_n, \ a_n=\cos{x}$ to -1. 

---
### Zasada indukcji matematycznej:

1. T(1) -  sprawdzamy czy twierdzenie jest poprawne dla pewnego elementu (zazwyczaj pierwszego)
2. $\forall n \in \mathbb{N} \ \ (T(n))$ - zakładamy że twierdzenie jest poprawne dla danego $n$ 
3. $\forall n \in \mathbb{N} \ \ (T(n)) \implies T(n+1))$ - udowadniamy że jak jest poprawne dla n to będzie też poprawne dla $n+1$ (korzystając z tezy)
###### Przykłady:
1. T: $1+2+3+...+n = \frac{n(n+1)}{2}$
sprawdzamy czy prawdziwe dla $n=1$
Z: $1=\frac{1(1+1)}{2}$ :LiCheck:
2. zakładamy że prawdziwe dla każdego k:
$1+2+3+...+k=\frac{k(k+1)}{2}$, T(k) - zakładamy że :LiCheck:
3. udowadniamy na podstawie założeń że prawdziwe również dla $k+1$
$1+2+3+...+k+(k+1) = \frac{k(k+1)}{2} + (k+1) = \frac{k(k+1)+2(k+1)}{2}=\frac{(k+2)(k+1)}{2}$ :LiCheck:
udowodniliśmy że jeśli teza jest prawdziwa dla k to prawdziwa też dla k+1, a skoro T(1) jest prawdziwe to każde następne T(n) też więc udowodniliśmy indukcją tą tezę :LiMSquare:

---
