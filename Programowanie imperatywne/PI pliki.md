


### Otwieranie pliku

```c
FILE *fopen(const char * restrict nazwa, const char * restrict tryb)

r - odczyt (+ błąd przy braku pliku)
w - zapis (dodanie x sprawia ze zaden inny program nie ma dostępu)
w+ - skasowanie pliku czyli stworzenie nowego
a - dodaj na Koniec
b - binarny
+ tryb odczytu/zapisu 

```

