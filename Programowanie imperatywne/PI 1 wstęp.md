### Wstęp, gcc, make, helloworld
#### 2025-03-19
##### Następna: [[]]
##### Zadania: [[]]

#gcc #make #c 

---
### Od źródła do programu:

1. Preprocesor
2. Kompilacja 
3. Asemblacja
4. Linkowanie 
5. Ładowanie i uruchomienie

##### Preprocesor:

Przetwarza napisany kod

- Usunięcie komentarzy
- Wstawienie plików nagłówkowych w miejsce \#Include 
- rozwinięcie makr w miejscu \#define 
- przetworzenie dyrektyw warunkowych \#ifdef
- wykonanie dyrektyw preprocesora

```sh
gcc -E hello.c -o hello.i
# tylko preprocesor
```

w hello.i jest normalny tekst tylko przetworzony

##### Kompiler:
- parsowanie kodu (analiza składniowa)
- analiza semantyczna
- optymalizacja
- generowanie kodu assemblera

```sh
gcc -S hello.c -o hello.s # Asembler
```

##### Asembler:
- asemblacja (zamienia plik.s na plik.o/plik.obj)

```sh
gcc -c hello.c -o hello.o
```

##### Linker:
- łączenie plików \*.o, \*.obj
- dołączanie bibliotek
  - statycznych \*.a, \*.lib
  - dynamicznych \*.so, \*.dll, \*dylib
- generowanie kodu wynikowego


```sh
gcc hello.c -o hello
# tu dostaniemy .exe
```

---
### Plik make


##### Kompilator i flagi

```sh 
CC=gcc
CFLAGS=-std=c23 -pedantic...
```


##### Pliki źródłowe i obiektowe

```sh 
SRCS=main.c utils.c...
OBJS=$(SRCS:.c=.o)
```

##### Nazwa pliku wykonywalnego

```sh
TARGET=program
```

##### Reguła domyślna

```sh
all: $(TARGET)
```

##### Kompilacja plików z .c do .o

```sh
%.o:%.c
	$(CC) $(CFLAGS) -c $<-o $@
```

##### Czyszczenie plików tymczasowych

```sh
clean:
	rm -f $(OBJS) $(TARGET)
```

---
### Diagnostyka

```c
#define NDEBUG - wyłącza debugowanie
#undef NDEBUG - włącza ponownie debugowanie

assert(warunek); - przerywa działanie programu
```

---
### Typy danych

##### Void - brak argumentu lub brak zwracania

```c

void licz_do_10(void){
	printf("Liczymy");
	for(int i=1; i<11;i++){
		printf("%d\t", i);
	}
}
```

reszta trywialne

---
