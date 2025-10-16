
### Kod uzupełnień do jedności ($U1$)

Pierwsza cyfra oznacza znak, gdy jest równa $0$ to wtedy jest to liczba dodatnia, gdy $1$ to jest to liczba ujemna. Żeby obliczyć wartość liczby zapisanej w $U1$, gdy jest ona dodatnia to wystarczy pozostałe cyfry zamienić z binarki. Gdy jest ona ujemna należy zastosować negacje pozostałych cyfr. Zatem negacja wartości jest jej ujemną wartością.

$$\begin{gathered}
0000 - 0\\
0001-1\\
0010-2\\
0011-3\\
\dots\\
0111-7\\
1000--7\\
1001--6\\
\dots \\
1111-0
\end{gathered}$$

#### Zadania:
###### 1. Cechami kodu uzupełnień do jeden są:
- symetryczny zakres kodu $\checkmark$
- pojedyńcza reprezentacja 0 $\times$
- żadne z pozostałych $\times$

### Kod uzupełnień do 2:

Teraz, gdy pierwsza cyfra jest równa 1 to podnosimy 2 do potęgi (jej miejsce) i odejmujemy to od wyniku, reszte cyfr dodajemy jak w binarce, jest lepszy do operacji arytmetycznych.

$$\begin{gathered}
0001-1\\
0010-2\\
0011-3\\
\dots \\
0111-7\\
1000--8\\
1001--7\\
1011--5\\
\dots \\
1111- -1
\end{gathered}$$
#### Zadania
###### Przy jakich operacjach na liczbach kodowanych w kodzie U2 może wystąpić nadmiar?
- Przy dodawaniu, odejmowaniu, mnożeniu, i dzieleniu.
- Tylko przy dodawaniu i mnożeniu.
- Tylko przy dodawaniu, odejmowaniu, i mnożeniu

Jeżeli dodamy do siebie np 7+7 (0111+0111) otrzymamy 14 którego nie zapiszemy na 4 bitach, podobnie z mnożeniem i odejmowaniem. Dzielenie raczej nie.

###### Jak w procesorze rozpoznawany jest nadmiar w obliczeniach stałopozycyjnych na liczbach kodowanych w U2?
- Wynik nie mieści się w rejestrze procesora $\times$
- Wynik nieoczekiwanie zmienia znak $\checkmark$
- Dwa ostatnie przeniesienia są różne $\times$

###### Liczba 10010 reprezentowana w systemie U2 ma wartość:
$$\begin{gathered}
-16+2=-14
\end{gathered}$$
###### Zakłada się, że zmienne typu int zajmują dwa bajty i są pamiętane w kodzie U2. Zakłada się ponadto, że komputer, na którym implementowany jest poniższy program nie sygnalizuje błędów spowodowanych przekroczeniem zakresu wartości. Podać wyniki działania poniższego programu.

```cpp
int x = -1;
int y = 0;
while (abs(x)-abs(y))>=1) {x--; y++;}
cout << x << " " << y << endl;
```

to będzie tak że x będzie sie coraz bardziej zmniejszał -1,-2,-3,-4 a y coraz bardziej zwiększał 1,2,3,4,5

Obie zmienne zajmują dwa bajty gdzie początkowo x=-1 $\to$ 111111111111 a y początkowo 000000000000. x wywali poza zakres więc należy zmienić znak czyli będzie równy 100000000 czyli -2^16 a y będzie musiał zmienić znak gdy będzie równy 0111111111111 czyli 2^16-1 
zatem wtedy x zamieni się na 1 czyli 0000001 a y zamieni się na 100000000000 co odpowiada -2^16, więc będzie wykonywał się w nieskończoność i guess.

### Syntaktyka, semantyka, pragmatyka

#### Syntaktyka:
Czy kod jest poprawnie napisany zgodnie z regułami składniowymi?
```Python 
print ["hello world"] # błąd składniowy (syntax error)
```

#### Semantyka: 

Czy program działa? Nie w kontekście tego czy jest dobrze składniowo napisany ale czy np dobrze są operowane typy itd.

```Python 
x="5"
x=x+5 # Type Error, bład synktaktyczny co prawda składniowo jest wszystko poprawnie, jednakże program nie zadziała
```

#### Pragmatyka: 

Czytelność kodu, dbanie o obsługę błędów, wybór optymalnych algorytmów.
Czyli myślenie o użyciu kodu w praktyce.

```Python
try:
    wynik = 10 / 0
except ZeroDivisionError:
    print("Nie można dzielić przez zero")  # Pragmatyczne rozwiązanie
```

#### Podsumowanie

```Python
x = input("Podaj liczbę: ")  # Syntaktycznie poprawne
y = x * 2  # Semantycznie błędne, jeśli użytkownik poda tekst, bo wynik to "teksttekst"
print(y) # Pragmatycznie: lepiej dodać sprawdzenie typu!
```

#### Zadania 
###### 3. Do opisu formalnej poprawności programu komputerowego niezbędna jest:
- pragmatyka $\times$
- semantyka $\times$
- syntaktyka $\checkmark$
###### 5. Jak inaczej określić składnię języka programowania?
- semantyka $\times$
- pragmatyka $\times$
- syntaktyka $\checkmark$ (syntax)

Bo chodzi o "formalnie poprawne" czyli żeby się w ogóle uruchomił.

---
### Odwrotna notacja polska / Reverse Polish Notation (ONP/RPN)

Jest to system zapisywania działań matematycznych w inny sposób niż normalny tzn.
$$\begin{gathered}
(x+y)*3\rightarrow xy+3*
\end{gathered}$$
Działa to w ten sposób że musimy ułożyć działanie w taki sposób by kolejno dodawane na stos elementy, gdy do stosu dodamy działanie (dodwanie, mnożenie itd)
to zdejmowało ze stosu 2 ostatnie elementy i zamieniało je na jedną liczbe z tego działania, i dodało na stos ponownie.

$$\begin{gathered}
(4-3)*(12+3)-1\\
\downarrow\\
43-12 \ 3+*1-\\\\
\end{gathered}$$
---
### Liczenie ile bitów potrzeba by (...)

#### Zadania 
###### 4. Ile bitów potrzeba do reprezentacji liczby z przedziału od $-10^3$ do $10^3$ z dokładnością do 2 cyfr dziesiętnych.

$$\begin{gathered}
\text{Całkowity zakres liczb: }10^3-(-10^3)=2000\\
\text{Dokładność do 2 cyfr dziesiętnych: }\frac{2000}{0.01}=200\ 000\\
2^n\gt 200 \ 000\\
n=18
\end{gathered}$$
###### 7. Jaka jest minimalna liczba bitów niezbędna do zapamiętywania temperatury z zakresu −50 do +50 stopni Celsjusza z dokładnością do jednego miejsca po przecinku?

$$\begin{gathered}
50-(-50)=100\\
\frac{100}{0.1}=1000\\
2^n\gt 1000\\
n=10
\end{gathered}$$
###### Zmienna typu wskaźnik zajmuje 4 bajty. Ile pamięci można zaadresować takim wskaźnikiem.

$$\begin{gathered}
4bajty=4\cdot 8b=32b\\
2^{32}\approx 4.294.967.296\ - \ 4gb\\
\end{gathered}$$
###### Od czego zależy zakres liczb zmiennopozycjnych w komputerze

- od ilości bitów cechy $\checkmark$
- od ilości bitów mantysy $\times$
- od ilości bitów cechy i mantysy $\times$

###### Zmienne typu short int zajmują 2 bajty i są pamiętane w kodzie U2. Stworzono nowy typ: struct real { short int mantysa; short int cecha; } reprezentujący liczby zmiennopozycyjne, których wartość jest równa $mantysa\cdot 2^{cecha}$. Z dokładnością do ilu cyfr dziesiętnych można reprezentować liczby typem real?

$$\begin{gathered}
2bajty=16bit\\
mantysa \ i \ cecha \  ma \ po \ 16 \ bitow\\
Z \ czego \ mantysa \ pozwala \ na \ dokladnosc \ do \ 1/65000
\end{gathered}$$

###### Zmienna typu int zajmuje 2 bajty, wskaźnik zajmuje 4 bajty. Ile bajtów zajmuje $int *t[200]$

To jest 200 elementowa tablica wskaźnikow, zatem po prostu $200\cdot 4=800$ 


### Kod Huffmana 

###### Teoria Informacji
> Wielkość Informacji zawarta w danym zbiorze jest miarą stopnia trudności rozpoznania elementów tego zbioru.

Ilością informacji zawartej w zbiorze
$$
X=\{ x_1, x_2 , ..., x_n \}
$$
nazywamy liczbę:
$$
H( X ) =-\sum_{i=1}^N {p_i} \cdot log_2(p_i)
$$
gdzie: 
$$
p_i (p_i>0, \sum{p_i=1})
$$
jest prawdopodobieństwem wystąpienia elementu $x_i$

**Przykłady**

{0.1} - 1 bit
{0..9} - 3.32 bita
zbiór liter języka ang. - 4.7 bita

###### Ile informacji zawiera 8-znakowe słowo, którego każdy znak jest jedną z liter A,B,C. Prawdopodobieństwo wystąpienia litery A wynosi 0.5, natomiast litery B i C wynosi 0.25.

A. 16 bitów
B. 12 bitów
C. 8 bitów

$$\begin{gathered}
H(X)=-(0.5\cdot \log_2(0.5)+0.25 \cdot \log_2(0.25)+0.25\cdot \log_2(0.25))\\
H=-(0.5 \cdot -1+0.25\cdot -2+0.25\cdot -2)\\
H=1.5 \ bita\\
H_{słowo}=8\cdot H=12 bit
\end{gathered}$$