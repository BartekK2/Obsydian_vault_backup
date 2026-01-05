
## Select

### Wybranie wszystkiego

```SQL
SELECT *
FROM tabela 
```

### Wybranie konkretnych kolumn 

```SQL
SELECT kolumna1,kolumna2
FROM tabela 
```

### Aliasowanie kolumn 


```SQL 
SELECT kolumna1 AS nazwa
FROM tabela 
```

**bez AS też zadziała**

### Aliasowanie tabel 


```SQL
SELECT t.kolumna1,t.kolumna2
FROM tabela t 
```

### Usuwanie duplikatów 


```SQL
SELECT DISTINCT kraj
FROM klienci
```

**dopiero po pobraniu potrzebnych danych tj. dane 2 rekordy w tabeli nie musza być duplikatami żebyśmy dostali jeden rekord po uzyciu distinct, wystarczy że dane które potrzebujemy i o które piszemy kwerende czyli sam kraj pochodzenia był duplikatem**
### Warunek (rekordy z jakimi wartościami chcemy)


```SQL
SELECT kolumna1,kolumna2
FROM tabela 
WHERE kolumna1='product'
```

**stringi w nawiasach pojedynczych** 

### Porównywanie tekstu (wzorcem)

```SQL
SELECT nazwa_produktu
FROM produkty
WHERE nazwa_produktu LIKE '%piwo%'
```

**% tutaj oznacza 0 lub więcej dowolnych znaków czyli w skrócie otrzymujemy jakiekolwiek nazwy zawierające "piwo"**

**- to pojedynczy znak**
**\[\] to zakres czyli np \[A-Z\]**
**\[^\] spoza zakresu**


### Lista 

```SQL 
SELECT nazwa_produktu
FROM produkty
WHERE nazwa_produktu in ('jablko','banan')
```

### IS NULL

Jeśli chcemy żeby dana kolumna była pusta to robimy

```SQL 
select companyname, fax
from suppliers
where fax is null
```

### Order by

```SQL 
select productid, productname, unitprice
from products
order by unitprice
```

rosnąco ^

```sql
select productid, productname, unitprice
from products
order by unitprice DESC
```

malejąco ^

```SQL 
select productid, productname, categoryid, unitprice
from products
order by categoryid, unitprice desc
```

dwa poziomy sortowania najpierw categoryid a tam gdzie są takie same sortuje po unitprice

### Kolumny wyliczane

```SQL 
select orderid, unitprice, unitprice * 1.05 as newunitprice
from [order details]
```

Notabene tabele z spacją w nazwie zapisujemy w kwadratowych nawiasach


### Operacja na napisach

```SQL 
select firstname + ' ' + lastname as imie_nazwisko
from employees
```

```SQL 
select concat(firstname,' ',lastname) as imie_nazwisko
from employees
```

te dwie kwerendy są równoważne

### CASE 

```SQL 
select orderid, freight,
	case
		when freight > 100 then 'high'
		when freight > 50 then 'medium'
		else 'low'
	end freightCategory
from orders

```

to nam da nową kolumne freightCategory zależną od freight (brak AS)

### Ograniczanie zbioru wynikowego
```SQL 
select top 5 orderid, productid, quantity
from [order details]
order by quantity desc
```

## GROUP BY

### Funkcje agregujące
Większość funkcji agregujących ignoruje wartości Null

COUNT $(*)$ - liczba wierszy
```SQL 
select count (*)
from employees
```

MIN - wartość minimalna
MAX - wartość maksymalna
SUM - suma
AVG - wartosć średnia

### Przykład + HAVING

```sql
select productid ,sum(quantity) as total_quantity
from orderhist
group by productid
```

agreguje dla każdego distinct productid tj. zwróci productid i dla każdego rekordu z tym productid policzy sume quantity tych rekordów

**Z warunkiem:**
```SQL 
select productid, sum(quantity) as total_quantity
from orderhist
where productid >= 2
group by productid
```

```SQL 
select productid, sum(quantity) as total_quantity
from orderhist
group by productid
having sum(quantity)>=30
```

w having najlepiej przepisać funkcje agregującą alias może nie zadziałać




## Funkcje 

### Tekstowe 

CONCAT - **Łączenie stringów**
SUBSTRING(tekst, start, długość) - **Wycinanie tekstu** (można start z minusem)
LEFT(tekst, liczba_znaków)
RIGHT(tekst, liczba_znaków) - **jak wyżej ale bez start**
REPLACE(tekst, szukany_fragment, nowy_fragment)
REPLICATE(tekst, liczba_powtorzen) - **powiela ten tekst ileś razy**
UPPER(tekst), LOWER(tekst)
RTRIM(tekst), LTRIM(tekst) - **usuwa spacje**


### Czasowe 
GETDATE() - aktualna data i czas serwera (lokalny)
GETUTCDATE() - aktualna data i czas w UTC
YEAR, MONTH, DAY
DATEADD(jednostka, ilość, data):
```sql
SELECT DATEADD(DAY, 7, GETDATE());   -- dzisiaj + 7 dni
SELECT DATEADD(MONTH, -2, GETDATE()); -- dzisiaj - 2 miesiące
SELECT DATEADD(YEAR, 1, '2025-12-03'); -- 2026-12-03
```
DATEDIFF(jednostka, data1, data2)
```SQL 
SELECT DATEDIFF(DAY, '2025-12-01', '2025-12-03'); -- 2 dni
SELECT DATEDIFF(MONTH, '2025-01-01', '2025-12-03'); -- 11 miesięcy
```

### Matematyczne 

RAND, ROUND, POWER, ABS
CEILING, FLOOR

### Inne 

CAST(wyrażenie AS typ_danych)
```SQL 
SELECT CAST(123 AS VARCHAR(10));       -- '123'
SELECT CAST(GETDATE() AS DATE);        -- 2025-12-03
```

ISNULL(wyrażenie, wartosc_domyslna)
```SQL 
SELECT ISNULL(NULL, 0);        -- 0
SELECT ISNULL(10, 0);          -- 10
SELECT ISNULL(kolumna, 'brak') FROM tabela;
```

IIF(warunek, wartosc_jesli_true, wartosc_jesli_false)
```SQL 
SELECT IIF(10 > 5, 'tak', 'nie');   -- 'tak'
SELECT IIF(kolumna IS NULL, 'brak', kolumna) FROM tabela;
```

COALESCE(wyrażenie1, wyrażenie2, ..., wyrażenieN)
```SQL 
SELECT COALESCE(NULL, NULL, 10, 20);  -- 10
SELECT COALESCE(NULL, 'brak', 'inny'); -- 'brak'
SELECT COALESCE(kolumna1, kolumna2, 'domyślna') FROM tabela;
```
