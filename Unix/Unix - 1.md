### Wstęp
#### 2024-10-11
##### Ćwiczenia: [[]]
##### Zadania: [[]]

#informacje  #unix 

---
Krzysztof Boryczko, boryczko@agh.edu.pl Pok. 3. 43 (l.22) tel: 12 328 33 49
Materiały: http://galaxy.agh.edu.pl/~boryczko/UNIX 
użytkownik: unix, hasło: ala123

---
## Przygotowanie przed kolokwium

### Znaki przekierowania

```sh
>, uzywane np dla ls folder > sciezki.txt
|, uzywane np dla ls -d folder | grep '^d.\.h$'
```

### Komendy

#### Ls

```sh
ls -d, listuje tylko foldery
ls -I, ignoruje wielkie/male litery 
ls -s, posortuj po rozmiarze pliku
ls -t, posortuj po czasie utworzenia pliku
ls -R, rekurencyjnie wywoluj dla znalezionych folderow
ls -l, wypisuje prawa plików/folderów
ls -reverse, odwróć sortowanie
ls /usr/bin | grep '^z*d$', mozna przekierowac output do grepu ktoremu nastepnie podajemy regex
^, zaczyna się od
$, kończy się na
., jeden znak
\., kropka
.\{6\}, 6 pustych znaków

```

```sh
ls /usr/bin/z*b
```

Listuje wszystkie pliki zaczynające się na z i kończące się na b. Gwiazdka oznacza że cmd wrzuca tutaj cokolwiek.


```sh
ls /usr/bin/z???
```

Listuje wszystkie pliki zaczynające się na z, a następnie po z następują 3 znaki.

#### Tworzenie/usuwanie katalogów, operacje na plikach

```sh
cd (puste), powrót do katalogu home
cd folder, przejście do podanego folderu
cd /usr/bin, przejscie do waznego folderu ktorego sciezka jest znana systemowi
mkdir folder1 folder2, utworz foldery
rmdir folder, usun folder
pwd, wypisz aktualna sciezke
mv plik1 folder1, przenosi plik/folder do folderu

file plik, printuje nazwe i typ pliku
less plik, printuje plik w krótszej czytelniejszej formie
more plik, j.w 
cp plik1 plik2, kopiuje plik1 na plik 2
diff plik1, plik2
```

#### Prawa dostępu

```sh
chmod opcje plik/folder, zmien prawa dostępu
```

#### Wyszukiwanie pliku/folderu

```sh
find /usr -name "st*" -print, znajdź pliki o takiej nazwie i wypisz jakie są
find /usr -perm umask -exec ls -ld {}\;, znajdź pliki o takich uprawnieniach i uruchom to co potem napisane


```

#### Zużycie dysku

```sh
du folder, wypisz zajęcie dysku w tym folderze, dla folderów/plików
du -s folder, krótsze wypisanie
du -k, kilobajty -m megabajty -g gigabajty

Można dorzucić sorta z tailem żeby znaleźć największy/najmniejszy plik np:
du -sk /usr/* 2>/dev/null | sort -n | tail -1

```

#### Użytkownicy

```sh
who, wypisuje listę aktualnie zalogowanych użytkowników
/etc/passwd, lista użytkowników wraz z grupami do których są przypisani i ich opisem
last, ostatni zalogowani
```

#### Procesy

```sh
Po uruchomieniu procesu można go schować w tło
bg %1
Lub ponownie pokazywać go w konsoli
fg %1

jobs, aktualne procesy uruchomione z tej bieżącej konsoli
ps, wszystkie procesy systemowe i informacje o nich
-e, wszystkie procesy jakie są w systemie
-a, powiązane z terminalem
-u username, które uruchomił użytkownik
-x, niepowiązane z terminalem
```

