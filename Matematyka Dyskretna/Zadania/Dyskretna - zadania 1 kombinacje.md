### Kombinatoryka
#### 2024-10-09
##### Lekcja: [[Dyskretna - 1]]

#kombinatoryka #matematyka_dyskretna  

---
#### Zadania z pdf Fortuny
###### 1. Ile jest permutacji zbioru $\{1,2,...,2n\}$ takich że żadne dwie liczby parzyste nie są sąsiednie?
$$
n!\cdot n!\cdot \binom{n+1}{n}
$$
$n!\cdot n!$ wynika oczywiście z rozkładu liczb parzystych i nieparzystych ($n!$) sposobów na rozkład nieparzystych i analogicznie dla parzystych 

**Jednakże -** ${n+1 \choose n}$ wynika z przypadku na przykład: $\{2,3,1,4\}$ gdzie liczby nieparzyste stoją obok siebie co nie przeczy przecież warunkom zadania. Także $n+1$ to ilość miejsc gdzie można postawić liczby parzyste PO rozstawieniu liczb nieparzystych (skrajne końce stąd +1) i $n$ bo tyle jest liczb parzystych.

---
###### 2. Ile jest sposobów na które możemy podzielić 2n osób na pary?

$$
\frac{(2n)!}{2^n\cdot n!}
$$

$(2n)!$ - liczba permutacji (po prostu bierzemy te osoby i je ustawiamy w szeregu na każdy sposób), by je później przydzielić w pary (ludzi stojących obok siebie). 
$2^n$ - bo każda para może być w dowolnej kolejności więc dzielimy przez 2, $n$ razy - czyli tyle ile jest par. 
$n!$ - dzielimy przez silnia n bo kolejność par nie ma znaczenia
**Swoją drogą ten wzór to iloczyn liczb nieparzystych bo to to samo co:**
$$(2n-1)\cdot(2n-3)...5\cdot3\cdot1$$Ponieważ to tak jakby każda osoba sobie wybierała pare i następna nie miała już możliwości wyboru dwóch poprzednich tzn: $(2n-1)$ bo nie może wybrać samego siebie $(2n-3)$ bo nie może wybrać nikogo z poprzedniej pary. (coś jak wybór do drużyny na wfie czy coś)

---
###### 3. Na ile sposobów można wybrać z n osób komitet, a z komitetu jego zarząd, jeśli zarówno komitet, jak i zarząd mogą liczyć od 0 do n osób?
$$
3^n
$$
Ponieważ każda osoba może mieć 3 różne role (choć to nie intuicyjne przez to jak zagmatwana jest treść zadania), przynajmniej wiemy że zarówno komitet jak i zarząd mogą liczyć od 0 do n osób także daje nam to pewną sugestie że to $3^n$. 

**Inny sposób:**
$$
\sum_{k=0}^{n}({n \choose j} \sum_{i=0}^k {k \choose i} \cdot 1^i \cdot 1^{k-i})=\sum_{k=0}^{n} {n \choose k} \cdot 2^i \cdot 1^{n-k} = (1+2)^n 
$$
---
###### 4.Ile jest permutacji zbioru $\{1,2,...,8\}$, w których każda liczba nieparzysta poprzedza (niekoniecznie bezpośrednio) liczbę o 1 od niej większą?
$$
\frac{8!}{2^4}
$$
Rozwiązanie wynika z tego że na każdą permutacje przypada taka z odwrotną parą czyli taka permutacja która nie spełnia warunków zadania: $\{3,4,1,2,5,6,7,8\}$ --> $\{4,3,1,2,5,6,7,8\}$

---
###### 5. Na ile sposobów można rozsadzić n osób wokół okrągłego stołu z $n+w$ miejscami?
$$
{n+w-1 \choose n-1} \cdot (n-1)!
$$
Wybór miejsc: ${n+w-1 \choose n-1}$ bo na początku sadzamy jedną która jest naszym punktem odniesienia a potem wybieramy resztę miejsc.
Permutacja siedzących osób: $(n-1)!$

---
###### 6. Na ile sposobów można zrobić ciągów binarnych o a zerach i b jedynkach?
$$
{a+b \choose b}={a+b \choose a}
$$
Ustalamy sobie liczbę możliwych rozstawień (wyborów miejsc na) jedynki/zera. A zera/jedynki - są już ustawione na podstawie jedynek/zer ponieważ nie ma innej opcji już.

---
###### 7. Na ile sposobów można pomalować n różnych liczb k kolorami?
$$
k^n
$$
Każda liczba może mieć $k$ różnych kolorów także $k \cdot k \cdot k \cdot k ....$ 

---
###### 8. Na ile sposobów można ustawić w ciąg liczby 0, 1, . . . , 9, tak by między 1 i 2 było dokładnie k innych liczb?
$$
8! \cdot (9-k)\cdot 2
$$
$(9-k)$ - ponieważ liczba 1 musi znajdować się na pozycji $i=10-(k+1),$ gdzie $i+(k+1)$ to pozycja liczby 2, razy 2 bo 1 niekoniecznie przed 2

---
###### 10. Ile jest dzielników liczby $10!$ ?
$10! = 1\cdot2\cdot3..\cdot10$, rozkład na liczby pierwsze: $\{2,3,2,2,5,2,3,7,2,2,2,3,3,5,2\}=\{2_8, 3_4, 5_2,7\}$
zatem każdy dzielnik musi być iloczynem pewnej wybranej liczby tych czynników pierwszych:
wzór na liczbę dzielników $(k_1+1)\cdot(k_2+1)\cdot(k_3+1)...\cdot(k_n+1)$ bo każdy dzielnik to: 
$p_1^{k_1}\cdot p_2^{k_2} \cdot p_3^{k_3} ... \cdot p_n^{k_n}$ więc dochodząc do konkluzji naszym wynikiem jest $9\cdot5\cdot3\cdot2=270$

---
###### 11. Ile jest punktów przecięcia n prostych, z których k jest wzajemnie równoległych, jeśli wiadomo, że żadne inne nie są równoległe i żadne trzy nie przecinają się w tym samym punkcie?

Chyba:
$$
k(n-k)+\frac{(n-k)(n-k-1)}{2}
$$
$k(n-k)$ liczba przecięć każdej równoległej z każdą nie równoległą
$\frac{(n-k)(n-k-1)}{2}$ - liczba przecięć każdej nierównoległej z każdą z nierównoległych

---
#### Zadania z pdf fortuny 2:
DO ZROBIENIA

---
#### Zadania z ćwiczeń:

###### 1. Na ile sposobów możemy do n szuflad wsadzić k identycznych kulek.
$$\begin{gathered}\binom{k+n-1}{n-1}
\end{gathered}$$
###### 2. Na ile sposobów może usiąść n kobiet i n mężczyzn przy okrągłym stole który ma 2n miejsc, gdzie żaden człowiek nie może usiąść obok kogoś o tej samej płci.
$$\begin{gathered}
n!\cdot n!\cdot 2
\end{gathered}$$

###### 3. Ile zer ma 1000! 
$$\begin{gathered}
\sum_{i=1}^{\lfloor \log_5{1000!}\rfloor}{\frac{1000}{5^i}}
\end{gathered}$$
###### 4. Na ile sposobów możemy wsadzić m listów do n skrzynek, gdzie co najmniej jedna skrzynka będzie pusta?
$$\begin{gathered}
n^m - \binom{m}{n}\cdot n!\cdot n^{m-n} \ chyba
\end{gathered}$$

###### 5. Na ile sposobów możemy ustawić p białych kulek i q czarnych kulek jeżeli dwie czarne nie mogą stać obok siebie?
$$\begin{gathered}
Zacznijmy \ od:\\
⚪⚪⚪⚪⚪⚪⚪⚪⚪ - p \ bialych \ kulek\\
Mamy \ p+1 \ miejsc \ na \ czarne \ kulki\\
i \ wybieramy \ q \ miejsc \ tyle \ ile \ kulek:\\
\binom{p+1}{q}\\
Np:
⚫⚪⚪⚫⚪⚪⚫⚪⚫⚪⚪⚪⚫⚪⚫
\end{gathered}$$
###### 6. Na ile sposobów możemy rozdać 12 jabłek i 1 gruszkę - trójce dzieci, wiedząc że mamy rozdać każdy z owoców?
$$
3\cdot 2\cdot 1 \cdot \binom{10+3-1}{3-1}
$$
###### 7. Na ile sposobów możemy przydzielić 6k osób do dwóch stołów 4k i 2k osobowych, gdzie wśród 6k osób jest pan A i pan B którzy muszą usiąść razem?
1) Jeśli usiądą przy 2k $\binom{6k-2}{2k-2}$
2) Jeśli usiądą przy 4k $\binom{6k-2}{4k-2}$
Więc wynik to: 
$$\begin{gathered}
\binom{6k-2}{2k-2}+\binom{6k-2}{4k-2}
\end{gathered}$$
###### 8. Ile istnieje rozwiązań $x_1+x_2+x_3+x_4=12$ gdzie każda z $x_n$ należy do liczb $\mathbb{Z}$, $\geq$ 0
$$\begin{gathered}
\binom{12+4-1}{4-1}=1365
\end{gathered}$$

---
#### Zadania z pdf fortuny 3

###### 1. Na ile różnych sposobów można rozsadzić przy okrągłym stole z k+m miejscami k kobiet i m mężczyzn, tak by wszystkie kobiety siedziały obok siebie.
Można potraktować grupę kobiet jako jednostkę i rozsadzić wszystkich $(m+1-1)!$ a potem spermutować kobiety $k!$ 

$$\begin{gathered}
m!\cdot k!
\end{gathered}
$$
###### 2. Na ile różnych sposobów można rozsadzić przy okrągłym stole z $2n+1$ miejscami $n$ kobiet i $n$ mężczyzn, tak aby dwie osoby tej samej płci nie siedziały obok siebie.

$$\begin{gathered}
2 \cdot n!\cdot n!
\end{gathered}
$$

###### 3. Na ile różnych sposobów można rozmieścić m rozróżnialnych listów w m rozróżnialnych skrzynkach na listy, tak aby co najmniej 2 były puste?

$$
m^m-m!-m\cdot \binom{m}{2}(m-1)\cdot (m-2)!
$$
###### 4. Na ile różnych sposobów można wybrać na wyprawę k spośród n rycerzy okrągłego stołu, jeśli nie wolno wybrać żadnych dwóch sąsiadów?

$$\begin{gathered}
\binom{n-k-1}{k-1}+\binom{n-k}{k}\\\\
\end{gathered}
$$
Bo powiedzmy że jedzie rycerz Krzysiu. Więc pozostało nam $k-1$ osób do wybrania, jeśli ustawimy tych co nie jadą w szeregu to miejsc na tych co jadą jest $n-k-1$. Jeśli krzysiu nie jedzie to wiemy że zostało nam $n-1$ osób do wybrania, nie jedzie $n-1-k$ a pomiędzy każdym kto nie jedzie jest $n-k$ miejsc gdzie mogą siedzieć wybrani.

###### 5. Na ile różnych sposobów można rozdać 12 nierozróżnialnych jabłek, 1 gruszke, 1 śliwke trójce dzieci, tak aby każde dostało po przynajmniej jednym owocu.

$$\begin{gathered}
1) ktores \ z \ dzieci \ ma \ i \ gruszke \ i \ sliwke\\
3\cdot \binom{10+3-1}{3-1}\\
2) dzieci \ moga \ miec \ jablko \ LUB \ gruszke\\
3\cdot 2 \cdot \binom{11+3-1}{3-1}
\end{gathered}$$

###### 6. Ile jest różnych możliwych sposobów całkowitoliczbowych nieujemnych rozwiązań równania $x_1+x_2+x_3+ x_4 = 12$, takich, że $x_1\geq 1$ i $x_3 \geq ­ 2$?

$$\begin{gathered}
(x_1-1)+x_2+(x_3-2)+ x_4 = 9\\
y_1+y_2+y_3+y_4=9\\
\binom{9+4-1}{4-1}
\end{gathered}$$
###### 7.  Na ile sposobów można rozmieścić $6k$ osób przy dwóch prostokątnych stołach z ponumerowanymi miejscami mieszczących odpowiednio $4k$ i $2k$ osób, tak by dwie spośród nich, A i B, siedziały przy większym stole, a między nimi było dokładnie $k$ innych osób?

$$\begin{gathered}
Chyba:\\
4k \cdot \binom{6k-2}{4k-2}\cdot (4k-2)! \cdot (2k)!
\end{gathered}$$

###### 8. Ile jest najkrótszych dróg prowadzących do miejsca odległego o 5 przecznic na południe i 8 przecznic na wschód w mieście, w którym ulice tworzą idealnie równą kwadratową siatkę, jeśli z powodu upału nie da się iść dwie przecznice na południe pod rząd?

$$\begin{gathered}
.W.W.W.W.W.W.W.W.\\
\binom{9}{5}
\end{gathered}
$$
**Inne autorskie rozwiązanie:**
Z treści wynika że po ruchu na południe można już tylko iść na wschód. Zatem **nasze ruchy można inaczej przedstawić** jako ruch 1) pójście w **dół + prawo**, 2) pójście **tylko w prawo** .
Wtedy możemy **dotrzeć albo do punktu o przecznice w lewo od punktu docelowego, albo do punktu o przecnice wyżej niż docelowy**. W obu przypadkach uwzględniając nową definicje pojedynczego ruchu dotarcie na miejsce zajmuje nam **8 nie 13** ruchów, z czego w pierwszym przypadku musimy dołączyć jeden ruch w prawo, a w drugim przypadku jeden ruch w dół.

Więc wybór w:
1) przypadku miejsc do skrętu w prawo ogranicza się do $\binom{8}{3}$
2) prypadku miejsc do skrętu w prawo ogranicza się do $\binom{8}{4}$ 

Po zsumowaniu obu możliwości mamy:
$$\begin{gathered}
\binom{8}{3}+\binom{8}{4}=\binom{9}{5}
\end{gathered}$$
Czyli tyle ile w poprzednim sposobie.

![[diagram-20241115 (5).png]]

---
