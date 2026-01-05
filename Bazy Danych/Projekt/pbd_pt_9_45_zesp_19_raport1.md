
dzień i godz zajęć: pt. 9:45
nr zespołu: 19
Autorzy: 
Bartłomiej Król
Filip Śledziński 
Michał Fedczyna
### 1. Wymagania i funkcje systemu

#### 1.1 Cel systemu
Celem systemu jest zapewnienie kompletnego środowiska dla osób pracujących w firmie produkcyjno-usługowej produkującej i sprzedającej meble dla pomieszczeń posiadających sprzęt komputerowy.

System obejmuję baze danych wraz z narzędziami do jej obsługi.
#### 1.2 Wymagania

##### 1.2.1 Wymagania ogólne:

- System jest zaimplementowany przy użyciu MS SQL Server.
- Baza danych ma posiadać integralność danych między innymi:
  - Jednoznaczna identyfikalność każdego rekordu w każdej z tabel
  - Integralność referencyjna (np. nie mogą istnieć w bazie danych zamówienia których foreign key wskazuje na klienta którego w tej bazie nie ma)
  - Dane muszą być poprawnego typu oraz w dozwolonyn zakresie

##### 1.2.2 Obsługa Produkcji i Asortymentu

| Wymaganie                   | Opis                                                                                                                                      |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Definicja Produktów         | System musi przechowywać opis każdego produktu (mebla) i jego skład (części metalowe, tworzywowe, elementy łączące).                      |
| Definicja Składników        | System musi zarządzać listą wszystkich dostępnych części (typ i ilość).                                                                   |
| Kalkulacja Kosztów          | System musi obliczać jednostkowy koszt produkcji produktu, uwzględniając koszty części i robocizny.                                       |
| Planowanie Produkcji        | System musi umożliwiać planowanie produkcji w oparciu o bieżące braki magazynowe i zamówienia klientów (uwzględnienie mocy przerobowych). |
| Ewidencja Mocy Przerobowych | System musi uwzględniać moce przerobowe firmy w jednostce czasu, by szacować realny termin realizacji zamówień.                           |
| Śledzenie statusu produkcji | Każda zlecona produkcja produktu może mieć statusy np "w trakcie", "przerwano" itd                                                        |

##### 1.2.3 Obsługa Magazynu

| Wymaganie             | Opis                                                                                          |
| --------------------- | --------------------------------------------------------------------------------------------- |
| Bieżący Stan Magazynu | System musi na bieżąco śledzić stan magazynowy gotowych produktów (redukcja po zamówieniach). |
| Zaplanowane Produkty  | System musi rejestrować produkty zaplanowane do produkcji.                                    |

##### 1.2.4 Obsługa Sprzedaży i Zamówień

| Wymaganie                                                     | Opis                                                                                                                   |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Rejestracja Klientów                                          | System musi rejestrować klientów indywidualnych i firmowych.                                                           |
| Składanie Zamówień                                            | System musi umożliwiać składanie zamówień na produkty dostępne w magazynie lub planowanie produkcji w przypadku braku. |
| Obsługa Rabatu (procentowego)                                 | System musi umożliwiać przydzielanie jednostkowego rabatu do składanego zamówienia.                                    |
| Szacowanie Czasu Realizacji                                   | System musi oszacować i podać klientowi czas realizacji zamówienia (zwłaszcza przy planowanej produkcji).              |
| Zapewnianie zwrotu pieniędzy w przypadku przerwanej produkcji | System musi mieć możliwość zmienienia statusu zamówienia i zapewnienia zwrotu pieniędzy.                               |
| Zarządzanie płatnościami                                      | System musi mieć możliwość zmiany statusu płatności w zamówianich.                                                     |
##### 1.2.5 Raportowanie

| Wymaganie                 | Opis                                                                                                                |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Koszty Produkcji          | Generowanie raportów kosztów (jednostkowych i dla grup) w ujęciu kwartalnym, miesięcznym i rocznym.                 |
| Stan Magazynowy           | Generowanie raportów bieżących stanów magazynowych oraz produktów zaplanowanych do produkcji.                       |
| Historia Zamówień Klienta | Generowanie raportów dotyczących poprzednich zamówień klienta (w tym rabatów) w różnych przedziałach czasu.         |
| Sprzedaż dla Zarządu      | Generowanie raportów dla kadry zarządczej: sprzedaż grup produktów oraz koszty produkcji w tygodniach i miesiącach. |
| Plan Wytworzenia          | Generowanie raportu dotyczącego planu wytworzenia poszczególnych produktów w różnych przedziałach czasu.            |

#### 1.2 Wymagane funkcje systemu 

Funkcje te zostaną zaimplementowane za pomocą procedur składowanych, funkcji i triggerów.

##### 1.2.1 Funkcje dotyczące produkcji i asortymentu

| Nazwa                       | Opis                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------- |
| dodaj_produkt()             | Dodaje nowy produkt do bazy wraz z jego składem.                                      |
| aktualizuj_koszt_produktu() | Oblicza aktualny koszt jednostkowy produktu na podstawie części i robocizny.          |
| zaplanuj_produkcje()        | Tworzy zapis planowanej produkcji na podstawie braków magazynowych i zamówień.        |
| sprawdz_moce_przerobowe     | Automatycznie sprawdza dostępne moce przerobowe przed zatwierdzeniem planu produkcji. |

##### 1.2.2 Funkcje dotyczące magazynu


| Nazwa                      | Opis                                                |
| -------------------------- | --------------------------------------------------- |
| aktualizuj_stan_magazynu() | Zmniejsza stan magazynowy po utworzeniu zamówienia. |
| pobierz_stan_czesci()      | Udostępnia aktualną listę części z magazynu.        |
| rejestruj_dostawe()        | Dodaje nowe partie części do magazynu.              |
| sprawdz_stan_produktu()    | Zwraca ile produktów danego rodzaju jest na stanie. |

##### 1.2.3 Funkcje dotyczące sprzedaży i zamówień

| Nazwqa                    | Opis                                                                      |
| ------------------------- | ------------------------------------------------------------------------- |
| zarejestruj_klienta()     | Dodaje klienta indywidualnego lub firmowego.                              |
| zloz_zamowienie()         | Obsługuje proces składania zamówienia.                                    |
| oblicz_rabat()            | Wylicza należny rabat dla zamówienia.                                     |
| oszacuj_czas_realizacji() | Wylicza realny termin realizacji uwzględniając moce przerobowe i magazyn. |
##### 1.2.4 Funkcje raportowe

| Nazwa                      | Opis                                       |
| -------------------------- | ------------------------------------------ |
| raport_kosztow             | Zawiera dane do raportu kosztów produkcji. |
| raport_stanu_magazynu      | Zawiera aktualne stany magazynowe.         |
| generuj_raport_sprzedazy() | Tworzy raporty sprzedaży dla zarządu.      |

#### 1.3 Historyjki użytkownika - czyli jakie wymagania mają użytkownicy i jak powinno wyglądać korzystanie z dobrze zaimplementowanego systemu?

**Poniżej prezentowane są tylko pojedyncze use-casy. Mają one za zadanie jedynie zwizualizować koncept systemu i podkreślić to że z tego systemu musi się dać korzystać wygodnie a zestaw narzędzi ma być dostatecznie rozbudowany**

Jako projektant produktu, chcę dodać nowy produkt wraz z listą jego składników, aby firma mogła rozpocząć jego produkcję. 

Jako kierownik produkcji, chcę przeglądać listę dostępnych części i ich ilości, aby planować produkcję zgodnie z możliwościami magazynowymi.

Jako pracownik obsługi klienta, chcę rejestrować nowe firmy i osoby prywatne, aby móc przypisywać do nich zamówienia. 

Jako pracownik sprzedaży, chcę otrzymać informację, czy produkt jest dostępny w magazynie, aby wiedzieć, czy zamówienie zostanie zrealizowane od razu. 

### 2. Baza danych

#### 2.1 Diagram


![[obraz_2025-12-10_215545211-Photoroom.png]]