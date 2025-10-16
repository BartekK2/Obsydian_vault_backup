
### Definicja 

**Programowanie dynamiczne to sposób na rozwiązywanie problemów, w których można wynik dużego problemu zbudować z wyników mniejszych problemów i nie trzeba tych mniejszych liczyć więcej niż raz, bo ich wyniki zapisujemy.**


## Problem imprezy firmowej

**Chyba najprostszy przykład tego**

Wyobraź sobie, że jest impreza firmowa i pracownicy są zorganizowani w strukturę drzewa — szef ma podwładnych, oni mają swoich podwładnych itd.

Każdy pracownik ma wartość "towarzyską" (liczbę punktów za bycie na imprezie).

**Zasada**:
Jeśli dany pracownik przychodzi na imprezę, jego bezpośredni podwładni nie mogą — żeby nie było niezręcznie.

**Cel**:
Wybrać takich pracowników, żeby suma punktów towarzyskich była jak największa, przestrzegając powyższej zasady.


### Opisane rozwiązanie:

$v$ - węzeł drzewa
$f(v)$ - wartość najlepszej imprezy dla drzewa ukorzonionego w $v$
$g(v)$ - j.w gdy $v$ nie jest zaproszony

### Zapis rekurencyjny

```python title=klasa_pracownika.py

class Employee:
	def __init__(self, fun):
		self.emp = []
		self.fun = fun 
		self.f = -1
		self.g = -1
```

$g(v)=\sum_{u \text{ pracownik }v}{f(u)}$
$f(v)=\max\{g(v), fun(v)+\sum_{u \text{ pracownik }v}{g(u)}\}$

Czyli albo pracownicy albo on i pracownicy pracowników.

### Implementacja

```python title=rozwiazanie.py

def f(v):
	if v.f >= 0:
		return v.f
	x=g(v)
	y=v.fun 
	for u in v.emp:
		y+=g(u)
	y.f=max(x,y)
	return v.f

def g(v):
	if v.g >= 0:
		return v.g
	v.g=0
	for u in v.emp:
		v.g += f(u)
	return v.g
```

**Czyli właściwie zrobiliśmy dokładnie to samo co w rekurencyjnej wersji, a wyniki przechowujemy w obiektach pracowników**

---
## Problem plecakowy

Mamy $N$ różnych przedmiotów każdy ma:
- wagę $w[i]$
- wartość $v[i]$

Oraz mamy plecak o pojemności $W$

**Cel:**
Mamy wybrać taki zestaw przedmiotów, żeby **wartość była jak największa** ale **suma wag nie przekroczyła** $W$.

### Opisane rozwiązanie:

$B$ - pojemność plecaka
$f(i,B)$ - rozwiązanie problemu plecakowego ze zbioru $\{0,\dots,i\}$, których waga nie przekracza $B$

### Zapis rekurencyjny

$$\begin{gathered}
f(i,b)=max(\begin{matrix}
f(i-1,b),\\
f(i-1,b-w(i))+p(i), b-w(i)\geq 0
\end{matrix})
\end{gathered}$$
$b-w(i)\geq 0$ żeby zablokować możliwość że wzięcie danego przedmiotu przekroczy pojemność plecaka

Wynik to $f(n-1,B)$

$$\begin{gathered}
f(0,b)=\left\{
\begin{matrix}
p(0), \ \ w(0)\leq b\\
0, \ \ w(0)\gt b
\end{matrix}
\right.
\end{gathered}
$$
### Implementacja

```python title=rozwiazanie.py

def backpack(W,P,B):
	n=len(W)
	F=[[0 for b in range(B+1)] for i in range(n)]
	for b in range(B+1):
		for i in range(1,n):
			F[i][b]=F[i-1][b]
			if b-W[i]>=0:
				F[i][b]=max(F[i][b], F[i-1][b-W(i)]+P[i])
	return F[n-1][B]
```

