

### Absolutne podstawy

**Deklaracja** - nazwanie zmiennej i przypisanie jej typu, bez konieczności dania jej wartości
**Inicjacja** - deklaracja zmiennej z nadaniem jej wartości
**Void** - typ funkcji która nic nie zwraca 

Wypisywanie na ekran nie jest z coutem bo tak jest w c++. Tutaj jest funkcja printf.

```c
printf("XD")
printf("%d, %s, %f", 10, "XD",0.01) 
// %d liczby dziesiętne %s string  %f double

```

**HELLO WORLD**:
```c
#include <stdio.h>

int main(void){
    printf("XDD");
    return 0;
}
```

**<stdio.h>** - standardowa biblioteka w C która obsługuje wejście/wyjście/bufor/pliki

```c
#include <stdio.h>
int main(void){
	int liczba;
	scanf("%lf", &liczba);
}
```

---
### Narzędzie Make

Make to jest po prostu narzędzie do automatyzacji kompilacji. Powiedzmy że chcemy różnie kompilować program, np wersje produkcyjną lub testową. Albo żeby automatycznie podpinać wszystkie potrzebne pliki nagłówkowe etc. To użyjemy tego.

Instrukcje tego programu obsługuje plik Makefile stworzony w folderze w jakim uruchamia się Make.

**Przykład 1:**

```sh
CC = gcc
CFLAGS = -std=c11 -pedantic -Werror=pedantic -Wall -Wextra

hello: hello.o
	$(CC) $(CFLAGS) -o hello hello.o
hello.o: hello.c
	$(CC) $(CFLAGS) -c hello.c

clean:
	rm -f hello hello.o
```

Najpierw definiujemy 2 zmienne które zawierają rzeczy które potem będziemy wstawiali w miejsce komendy.

Potem definiujemy w jaki sposób chcemy tworzyć pliki hello.exe, hello.o i jak je łączyć.

---

**Przykład 2:**

Do skompilowania programu (main.c) używamy dwóch innych plików zawierających funkcje "add" i "print_message". Pliki te to pliki "math_utils.c" oraz "utils.c". Należy zadeklarować te funkcje w pliku "main.c". Robimy to poprzez "#include utils.h" i tak dalej. Czyli jeżeli zadeklarujemy te funkcje kompilator wypełni je po skompilowaniu tamtych plików utils.c itd.

```c title="main.c"
#include <stdio.h>
#include "utils.h"
#include "math_utils.h"

int main(void){
    print_message();
    printf("2+3=%d\n",add(2,3));
    return 0;
}
```

```c title:math_utils.c
#include "math_utils.h"

int add(int a, int b) {
 return a + b;
}
```

```c title:math_utils.h
#ifndef MATH_UTILS_H
#define MATH_UTILS_H

int add(int a, int b);

#endif
```

```c title:utils.c
#include <stdio.h>
#include "utils.h"

void print_message(void){
    printf("Hello from utils\n");
}
```

```c title:utils.h
#ifndef UTILS_H
#define UTILS_H

void print_message(void);

#endif
```

Pliki .o nie wymagają tego żeby był już skompilowany inny plik będący zależnością do tego pliku. Chodzi o to że nawet jeżeli jeszcze nie skompilowaliśmy i nie wypełniliśmy danej funkcji to i tak możemy skompilować kod który uruchamia tą funkcje.

Trzeba na to spojrzeć pod kątem assemblera. To wtedy wiadomo o co chodzi. Jeżeli skompilujemy main.c do main.o to mamy jedynie powiedziane "aha ten kod będzie wywoływał funkcje add". To jest jak najbardziej poprawny kod po skompilowaniu. Oczywiście to samo nie wystarczy bo nie wiadomo co to za funkcja i co robi. Ale nie musimy kompilować wcześniej tamtych funkcji add. i tak dalej.

Zatem kompilacja wygląda tak:

```sh
gcc -std=c11 -pedantic -Werror=pedantic -Wall -Wextra -c main.c -o main.o

gcc -std=c11 -pedantic -Werror=pedantic -Wall -Wextra -c math_utils.c -o math_utils.o

gcc -std=c11 -pedantic -Werror=pedantic -Wall -Wextra -c utils.c -o utils.o

gcc -std=c11 -pedantic -Werror=pedantic -Wall -Wextra -o my_program main.o utils.o math_utils.o
```

:LiSmile:

---

**Przykład 3:**

**Biblioteka statyczna:** - zamiast kompilować każdy plik .c do pliku .o i łączyć je w kompilacji w jeden program można wszystkie potrzebne dodatkowe pliki dodawać do biblioteki statycznej (za pomocą komendy ar rcs rlibutils.a plik.o). Z tej biblioteki można potem listować użyte pliki, dodawać i usuwać pliki .o. Tą biblioteke można swobodnie używać też w innych projektach bez konieczności posiadania każdego pliku .o 

Nie zawsze jest to potrzebne ani konieczne. Ale gdy tych plików jest dużo bądź często należy je rekompilować albo gdy wiemy że chcemy to potem wielokrotnie używać należałoby stworzyć tą biblioteke. 

Biblioteka nie aktualizuje sie automatycznie po zmianie w kodzie. Należy zrekompilować dany plik do .o i go ponownie dopiąć do biblioteki. 


**Tworzenie biblioteki statycznej:**
```sh
gcc -std=c11 ... -c utils.c -o utils.o
gcc -std=c11 ... -c math_utils.c -o math_utils.o
ar rcs libutils.a utils.o math_utils.o
```

r - wstawia pliki do archiwum
c - tworzy nowe archiwum, jeśli jeszcze nie istnieje
s - tworzy indeks w archiwum co pozwala na szybsze linkowanie

**Linkowanie programu z biblioteką:**

```sh
gcc -std=c11 -o my_program main.o matma.o -L. -lutils
```

tutaj rozdzielamy co chcemy mieć z .o a co z biblioteki, flaga -L. mówi żeby szukać biblioteki w tym folderze

-lutils oznacza libutils.a (lib i .a są domyślne)

**Aktualizacja biblioteki po zmianach w pliku / dodanie nowego pliku:**

```sh
gcc -std=c11 -c utils.c -o utils.o
ar rcs libutils.a utils.o
```

**Wylistowanie plików w bibliotece:**

```sh
ar t libutils.a
```

**Usunięcie pliku .o z biblioteki:**

```sh
ar d libutils.a xd.o
```

---
### Argumenty make

Make raczej nie obsługuje argumentów pozycyjnych, (coś jak args w pythonie) ale raczej argumenty-klucze jak kwargs.

Można podać i użyć argumenty w taki sposób:

```c
CC=gcc
CFLAGS=-std=c11

all:
	echo Kompiluje wersje: $(build)
	$(CC) $(CFLAGS) main_v$(build).c -o main_v$(build)
```

```sh
make build=1.12
```


Teoretycznie można tu się pobawić w jakieś obejście tego że make nie obsługuje argumentów pozycyjnych: (popatrz niżej w wartości specjalne jeśli nie rozumiesz)

```c
.PHONY: default // nawet jeśli będziemy mieli plik default, make nie uzna go za cel (bo niżej mamy default: mejkowe)

default:
	echo "Kompiluje wersje $(firstword $(MAKECMDGOALS))"
	gcc -c main$(firstword $(MAKECMDGOALS)).c -o main$(firstword $(MAKECMDGOALS)).o
	gcc -o main$(firstword $(MAKECMDGOALS)) main$(firstword $(MAKECMDGOALS)).o

// jeżeli nie znajdzie takiego pliku jaki jest dany jako cel (czyli w naszym przypadku argument pozycyjny)
%:
	@true // to nie robi nic (true to komenda, @ wyłącza wypis do cmd)
```

```sh
make 5
"
Kompiluje wersje 5
gcc -c main5.c ...
"
```

Jak to działa?

1. Make szuka pliku 5.c
2. Nie znajduje go więc uruchamia regułe ogólną (default), nawet jeżeli istnieje default.c bo mamy go pominiętego dzięki .PHONY
3. Pobiera pierwsze słowo z celów czyli bierze "5" jako zmienną
### Wartości specjalne i funkcje w Makefile

```c
.PHONY: default // mówi make-owi że "default" nie będzie nazwą pliku tylko jakąś komendą

default: // domyślny plik jeśli sie nie poda żadnego

%: // jeżeli nie znajdzie celu (pliku)

%:
	@true // @ przed komendą oznacza że nie wyświetli jej w terminalu a true to podstawowa komenda która zwraca sukces (0)

program: main.o util.o
	gcc -o $@ $^  # $@ → program, $^ → main.o util.o
	// Czyli $@ zwraca aktualny cel a $^ zależności
	
$(patsubst file.c,file.o,main.c) // main.o
$(wildcard *.c)	// wszystkie pasujące pliki .c
$(notdir src/main.c) // usuwa katalog ze ścieżki -> main.c
$(dir src/main.c) // sam katalog -> src 
$(basename main.c) // nazwa pliku bez rozszerzenia
$(suffix main.c) // samo rozszerzenie

```

### Warunki w make

```C
ifeq ($(CC),gcc)
    CFLAGS += -Wall
else
    CFLAGS += -Wextra
endif

// system
UNAME := $(shell uname)

ifeq ($(UNAME), Linux)
	CC = gcc
else
	CC = clang
endif
```

$$\begin{gathered}
\int^{1}_{0}{x^2 + \ln{x}\ dx}=0\\


\end{gathered}$$