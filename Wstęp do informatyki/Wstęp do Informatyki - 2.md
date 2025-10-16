### Subtytuł 
#### 2024-10-15
##### Poprzednia: [[Wstęp do Informatyki - 1]]
##### Następna: [[]]
##### Zadania: [[Wstęp do Informatyki-1 - zadania]]

#temat #WDI 

--- 
*ZRÓB ZADANIA !!!*

Zadanie 10:
```python title: czy_pierwsza.py
def czy_pierwsza(x):
	y=2
	if x<2: return False
	while y**2 <=x:
		if x%y==0:
			return False
		y +=1
	return True
```

```python title:zad17.py
from math import pi
def silnia(x):
    wynik=1
    for i in range(1,x+1):
        wynik*=i
    return wynik

def cos(x,eps):
	suma=0
	a = 2
	n=0
	while True:
		an = (-1)**n/silnia(2*n)*(x**(2*n))
		suma += an
		if abs(a-an)<eps:
		    return suma
		a=an
		n+=1
print(cos(pi/3, 1e-5))
```


```python title:trojkaty_pitagorejskie.py

def znajdz_trojkaty(n: int) -> int:
	if n<5:
		return 0 
	suma=0
	pierwiastek = sqrt(n)
	a,b=1,pierwiastek
	while a!=b:
		if a**2+b**2==n**2:
			suma+=1
			print(a,b,n)
		elif a**2+b**2<n**2:
			a+=1
		else a**2+b**2>n**2:
			b-=1
	return suma
```

