### Argumenty polecenia make
#### 2025-03-20
##### Następna: [[]]
##### Zadania: [[]]

#gcc #make #c 

---
### Typ wyliczeniowy (enum)

```c

enum dni {pon, wt, śr, czw, pt, sob, niedz};

int main(void){
	enum dni dzien = pon;
	printf("%d", dzien); // 0
}
```

```c

enum dni {pon=1, wt, śr, czw, pt, sob, niedz};

int main(void){
	enum dni dzien = pon;
	printf("%d", dzien); // 1
	
	dzien = śr;
	printf("%d", dzien); // 3
}
```


```c

typedef enum {pon=1, wt, śr, czw, pt, sob, niedz} dni;

int main(void){
	dni dzien = pon;
	printf("%d", dzien); // 1
}
```


---
### Struktura 

```c
struct nazwa {pola_składowe};
typedef struct {pola_składowe} nazwa;

struct t_miejsce{
	char nazwa[40];
	float dlug_geo;
	float szer_geo;
	int ocena;
};

struct t_miejsce Kalisz={"Kalisz", 19.011, 51.02, 5};
Kalisz.ocena=1;
struct t_miejsce Kolobrzeg = {0};

struct t_miejsce Gdansk = {"Gdansk", ocena=10};
```

