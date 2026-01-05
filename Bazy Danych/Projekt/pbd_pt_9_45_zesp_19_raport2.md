dzień i godz zajęć: pt. 9:45
nr zespołu: 19
Autorzy: 
Bartłomiej Król
Filip Śledziński 
Michał Fedczyna

### 1. Opis funkcji 

System bazodanowy dla firmy produkcyjno-usługowej zajmującej się produkcją i sprzedażą mebli przeznaczonych do pomieszczeń wyposażonych w sprzęt komputerowy (sale dydaktyczne, biura). Asortyment obejmuje krzesła, biurka, biurka gamingowe, stoły, fotele biurowe, fotele gamingowe, ruchome stojaki na projektory oraz tablice interaktywne.

**Główne funkcjonalności systemu:**

- **Zarządzanie klientami** — obsługa klientów indywidualnych oraz firmowych z odrębnymi danymi (imię/nazwisko vs nazwa firmy)
- **Katalog produktów** — produkty pogrupowane w kategorie, każdy z definicją części składowych, czasem produkcji i kosztami
- **Magazyn** — śledzenie stanów magazynowych produktów gotowych z rozróżnieniem na ilość przechowywaną i zarezerwowaną
- **Zamówienia** — składanie zamówień przez klientów z możliwością przyznania indywidualnego rabatu, śledzenie statusu (placed → in_progress → finalized/canceled)
- **Płatności** — rejestracja płatności i zwrotów powiązanych z zamówieniami
- **Planowanie produkcji** — planowanie produkcji z uwzględnieniem dostępnych mocy przerobowych (minuty robocze na dzień), możliwość rozłożenia produkcji na wiele dni
- **Raportowanie** — raporty kosztów produkcji, stanów magazynowych, historii zamówień, sprzedaży według kategorii i okresów

### 2. Ostateczny schemat bazy danych 

![[obraz_2025-12-18_013251645-Photoroom.png]]

#### 2.1 Jak wygenerowane zostały dane?

Dane zostały wygenerowane w Pythonie między innymi przy pomocy biblioteki Faker zapewniającej łatwy sposób na generowanie imion, adresów, numerów telefonów (dla klientów), biblioteki random oraz pyodbc.

Przykładowo:
```python 
customer_ids = []
CUSTOMERS = 50
INDIVIDUAL_CUSTOMERS = 40

for i in range(CUSTOMERS):
    cursor.execute("""
        INSERT INTO Customers (address, phone)
        OUTPUT INSERTED.id
        VALUES (?, ?)
    """, fake.address(), fake.phone_number())

    cid = cursor.fetchone()[0]
    customer_ids.append(cid)

    if i < INDIVIDUAL_CUSTOMERS:
        cursor.execute("""
            INSERT INTO IndividualCustomers (customer_id, first_name, last_name)
            VALUES (?, ?, ?)
        """, cid, fake.first_name(), fake.last_name())
    else:
        cursor.execute("""
            INSERT INTO CompanyCustomers (customer_id, company_name)
            VALUES (?, ?)
        """, cid, fake.company())

conn.commit()
```

Analogicznie utworzono pozostałe tabele.

### 3. Kod DDL 

```sql
USE u_bkrol;
GO

-- Customers

CREATE TABLE Customers (
    id INT IDENTITY(1, 1) PRIMARY KEY,
    address VARCHAR(100),
    phone VARCHAR(20)
);

CREATE TABLE IndividualCustomers (
    customer_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    CONSTRAINT fk_individual_customer
        FOREIGN KEY (customer_id) REFERENCES Customers(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

CREATE TABLE CompanyCustomers (
    customer_id INT PRIMARY KEY,
    company_name VARCHAR(100),
    CONSTRAINT fk_company_customer
        FOREIGN KEY (customer_id) REFERENCES Customers(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

-- Products

CREATE TABLE Categories (
    id INT IDENTITY(1, 1) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    description VARCHAR(500)
);

CREATE TABLE Parts (
    id INT IDENTITY(1, 1) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    cost MONEY NOT NULL
);

CREATE TABLE Products (
    id INT IDENTITY(1, 1) PRIMARY KEY,
    category_id INT NOT NULL,
    name VARCHAR(100) NOT NULL,
    production_time_minutes INT NOT NULL,
    labor_cost MONEY NOT NULL,
    unit_price MONEY NOT NULL,
    CONSTRAINT chk_positive_production_time CHECK (production_time_minutes > 0),
    CONSTRAINT chk_positive_labor_cost CHECK (labor_cost > 0),
    CONSTRAINT chk_positive_unit_price CHECK (unit_price > 0),
    CONSTRAINT fk_product_category
        FOREIGN KEY (category_id) REFERENCES Categories(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

CREATE TABLE ProductsParts (
    product_id INT NOT NULL,
    part_id INT NOT NULL,
    quantity INT NOT NULL,
    CONSTRAINT chk_positive_parts_quantity CHECK (quantity > 0),
    CONSTRAINT pk_product_part PRIMARY KEY (product_id, part_id),
    CONSTRAINT fk_product_part_product
        FOREIGN KEY (product_id) REFERENCES Products(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE,
    CONSTRAINT fk_product_part_part
        FOREIGN KEY (part_id) REFERENCES Parts(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

CREATE TABLE Warehouse (
    product_id INT PRIMARY KEY,
    stored_amount INT NOT NULL DEFAULT 0,
    reserved_amount INT NOT NULL DEFAULT 0,
    CONSTRAINT chk_natural_stored_amount CHECK (stored_amount >= 0),
    CONSTRAINT chk_natural_reserved_amount CHECK (reserved_amount >= 0),
    CONSTRAINT chk_reserved_not_exceeds_stored CHECK (reserved_amount <= stored_amount),
    CONSTRAINT fk_warehouse_product
        FOREIGN KEY (product_id) REFERENCES Products(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

-- Orders

CREATE TABLE Orders (
    id INT IDENTITY(1, 1) PRIMARY KEY,
    customer_id INT NOT NULL,
    status VARCHAR(20) NOT NULL DEFAULT 'placed',
    created_at DATE NOT NULL DEFAULT GETDATE(),
    paid_at DATE,
    finalized_at DATE,
    canceled_at DATE,
    preferred_finalize_date DATE,
    estimated_finalize_date DATE,
    payment_status VARCHAR(20),
    CONSTRAINT chk_valid_order_status CHECK (status IN ('placed', 'in_progress', 'finalized', 'canceled')),
    CONSTRAINT chk_valid_payment_status CHECK (payment_status IS NULL OR payment_status IN ('completed', 'refund')),
    CONSTRAINT fk_order_customer
        FOREIGN KEY (customer_id) REFERENCES Customers(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

CREATE TABLE OrderDetails (
    order_id INT NOT NULL,
    product_id INT NOT NULL,
    quantity INT NOT NULL,
    unit_price MONEY NOT NULL,
    discount FLOAT NOT NULL DEFAULT 0,
    CONSTRAINT chk_positive_order_quantity CHECK (quantity > 0),
    CONSTRAINT chk_valid_discount CHECK (discount >= 0 AND discount <= 1),
    CONSTRAINT pk_order_detail PRIMARY KEY (order_id, product_id),
    CONSTRAINT fk_order_detail_order
        FOREIGN KEY (order_id) REFERENCES Orders(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE,
    CONSTRAINT fk_order_detail_product
        FOREIGN KEY (product_id) REFERENCES Products(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

-- Production

CREATE TABLE AvailableWorkForce (
    day DATE PRIMARY KEY,
    available_time_minutes INT NOT NULL,
    CONSTRAINT chk_natural_available_time CHECK (available_time_minutes >= 0)
);

CREATE TABLE ProductionPlan (
    id INT IDENTITY(1, 1) PRIMARY KEY,
    order_id INT,
    product_id INT NOT NULL,
    quantity_planned INT NOT NULL,
    quantity_produced INT NOT NULL DEFAULT 0,
    status VARCHAR(20) NOT NULL DEFAULT 'planned',
    created_at DATE NOT NULL DEFAULT GETDATE(),
    finalized_at DATE,
    canceled_at DATE,
    CONSTRAINT chk_positive_quantity_planned CHECK (quantity_planned > 0),
    CONSTRAINT chk_natural_quantity_produced CHECK (quantity_produced >= 0),
    CONSTRAINT chk_produced_not_exceeds_planned CHECK (quantity_produced <= quantity_planned),
    CONSTRAINT chk_valid_production_status CHECK (status IN ('planned', 'in_progress', 'finalized', 'canceled')),
    CONSTRAINT fk_production_order
        FOREIGN KEY (order_id) REFERENCES Orders(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE,
    CONSTRAINT fk_production_product
        FOREIGN KEY (product_id) REFERENCES Products(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);

CREATE TABLE ReservedWorkForce (
    plan_id INT NOT NULL,
    day DATE NOT NULL,
    time_minutes INT NOT NULL,
    CONSTRAINT chk_positive_reserved_time CHECK (time_minutes > 0),
    CONSTRAINT pk_reserved_workforce PRIMARY KEY (plan_id, day),
    CONSTRAINT fk_reserved_plan
        FOREIGN KEY (plan_id) REFERENCES ProductionPlan(id)
        ON UPDATE CASCADE
        ON DELETE CASCADE,
    CONSTRAINT fk_reserved_day
        FOREIGN KEY (day) REFERENCES AvailableWorkForce(day)
        ON UPDATE CASCADE
        ON DELETE CASCADE
);
```

### 4. Widoki/Procedury/Funkcje/Triggery 

#### 4.1 Widoki

| Nazwa                         | Opis                                                                                                                                                                                                                    |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `vw_WarehouseStatus`          | Aktualny stan magazynu dla każdego produktu: ilość przechowywana (stored_amount), zarezerwowana (reserved_amount) oraz dostępna do sprzedaży (stored - reserved). Zawiera także nazwę produktu i kategorii.             |
| `vw_CustomerOrderHistory`     | Historia zamówień klientów. Łączy dane klienta (indywidualnego lub firmowego), zamówienia i szczegóły pozycji. Pokazuje produkty, ilości, ceny jednostkowe, rabaty oraz kwoty po rabacie.                               |
| `vw_PlannedProduction`        | Produkty aktualnie znajdujące się w kolejce produkcyjnej (status 'planned' lub 'in_progress'). Zawiera ilości zaplanowane, wyprodukowane oraz daty zarezerwowane w ReservedWorkForce.                                   |
| `vw_MonthlySales`             | Sprzedaż zagregowana według kategorii produktów i miesiąca. Pokazuje liczbę zamówień, łączną ilość sprzedanych produktów oraz przychód (po uwzględnieniu rabatów). Bazuje na zamówieniach ze statusem 'finalized'.      |
| `vw_WeeklySales`              | Sprzedaż zagregowana według kategorii produktów i tygodnia. Analogiczny do vw_MonthlySales, ale z podziałem na tygodnie.                                                                                                |
| `vw_MonthlyProductionCosts`   | Koszty produkcji zagregowane według kategorii i miesiąca. Uwzględnia koszt robocizny (labor_cost × quantity) oraz koszt części (z tabeli ProductsParts × Parts.cost). Bazuje na ProductionPlan ze statusem 'finalized'. |
| `vw_QuarterlyProductionCosts` | Koszty produkcji zagregowane według kategorii i kwartału. Struktura analogiczna do vw_MonthlyProductionCosts.                                                                                                           |
| `vw_YearlyProductionCosts`    | Koszty produkcji zagregowane według kategorii i roku. Struktura analogiczna do vw_MonthlyProductionCosts.                                                                                                               |

#### 4.2 Funkcje

| Nazwa                         | Parametry         | Zwraca  | Opis                                                                                                                                                                         |
| ----------------------------- | ----------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `fn_CalculateProductCost`     | `@product_id INT` | `MONEY` | Oblicza całkowity koszt produkcji jednej sztuki produktu. Sumuje koszt robocizny (labor_cost) oraz koszt wszystkich części składowych (ProductsParts.quantity × Parts.cost). |
| `fn_CalculateOrderTotal`      | `@order_id INT`   | `MONEY` | Oblicza całkowitą kwotę zamówienia po uwzględnieniu rabatów. Formuła: SUM(quantity × unit_price × (1 - discount)).                                                           |
| `fn_GetAvailableStock`        | `@product_id INT` | `INT`   | Zwraca ilość produktu dostępną do sprzedaży (stored_amount - reserved_amount).                                                                                               |
| `fn_GetRemainingWorkforce`    | `@day DATE`       | `INT`   | Zwraca liczbę wolnych minut roboczych dla danego dnia. Oblicza: available_time_minutes - SUM(zarezerwowane minuty w ReservedWorkForce).                                      |
| `fn_EstimateFinalizationDate` | `@order_id INT`   | `DATE`  | Szacuje datę zakończenia realizacji zamówienia. Znajduje najpóźniejszą datę w ReservedWorkForce dla wszystkich planów produkcji powiązanych z zamówieniem.                   |

#### 4.3 Procedury

| Nazwa                       | Parametry                                                              | Opis                                                                                                                                                                                                                                  |
| --------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `sp_PlaceOrder`             | `@customer_id INT`, `@preferred_date DATE`, `@order_id INT OUTPUT`     | Tworzy nowe zamówienie ze statusem 'placed'. Ustawia preferred_finalize_date jeśli podano. Zwraca ID utworzonego zamówienia.                                                                                                          |
| `sp_AddOrderItem`           | `@order_id INT`, `@product_id INT`, `@quantity INT`, `@discount FLOAT` | Dodaje pozycję do zamówienia. Pobiera aktualną cenę produktu (unit_price) z tabeli Products. Waliduje czy zamówienie istnieje i ma status 'placed'.                                                                                   |
| `sp_CalculateEstimatedDate` | `@order_id INT`                                                        | Oblicza szacowaną datę realizacji zamówienia BEZ tworzenia planu produkcji. Sprawdza dostępność w magazynie, symuluje alokację mocy produkcyjnych. Aktualizuje pole estimated_finalize_date w Orders.                                 |
| `sp_ProcessPayment`         | `@order_id INT`                                                        | Przetwarza płatność za zamówienie. Ustawia payment_status='completed', paid_at=GETDATE(), status='in_progress'. Rezerwuje produkty z magazynu (zwiększa reserved_amount). Dla produktów niedostępnych wywołuje sp_ScheduleProduction. |
| `sp_ScheduleProduction`     | `@order_id INT`, `@product_id INT`, `@quantity INT`                    | Tworzy plan produkcji dla podanej ilości produktu. Tworzy rekord w ProductionPlan oraz odpowiednie wpisy w ReservedWorkForce, rozkładając produkcję na dni z dostępnymi mocami przerobowymi.                                          |
| `sp_CancelOrder`            | `@order_id INT`                                                        | Anuluje zamówienie. Zwalnia rezerwacje magazynowe (zmniejsza reserved_amount). Anuluje powiązane plany produkcji (status='canceled'). Jeśli zamówienie było opłacone, ustawia payment_status='refund'.                                |
| `sp_RecordDailyProduction`  | `@plan_id INT`, `@day DATE`, `@actual_quantity INT`                    | Rejestruje faktyczną produkcję danego dnia. Zwiększa quantity_produced w ProductionPlan. Jeśli quantity_produced < quantity_planned po wykorzystaniu wszystkich zarezerwowanych dni, planuje dodatkowe dni produkcji.                 |
| `sp_FinalizeOrder`          | `@order_id INT`                                                        | Finalizuje zamówienie (wysyłka). Zmniejsza stored_amount i reserved_amount w magazynie. Ustawia status='finalized', finalized_at=GETDATE().                                                                                           |
| `sp_AddWarehouseStock`      | `@product_id INT`, `@quantity INT`                                     | Dodaje wyprodukowane produkty do magazynu (zwiększa stored_amount). Wywoływane po zakończeniu produkcji.                                                                                                                              |

#### 4.4 Triggery

| Nazwa | Tabela | Zdarzenie | Opis |
|-------|--------|-----------|------|
| `trg_PreventNegativeStock` | `Warehouse` | AFTER UPDATE | Blokuje operację jeśli aktualizacja spowodowałaby stored_amount < 0 lub reserved_amount > stored_amount. Zapewnia spójność stanów magazynowych. |
| `trg_PreventOverReservation` | `ReservedWorkForce` | AFTER INSERT, UPDATE | Blokuje operację jeśli suma zarezerwowanych minut dla danego dnia przekroczyłaby available_time_minutes w AvailableWorkForce. Chroni przed przekroczeniem mocy produkcyjnych. |
| `trg_UpdateProductionStatus` | `ProductionPlan` | AFTER UPDATE | Automatycznie ustawia status='finalized' i finalized_at=GETDATE() gdy quantity_produced osiągnie quantity_planned. Upraszcza logikę procedur. |
| `trg_SyncOrderStatus` | `ProductionPlan` | AFTER UPDATE | Gdy wszystkie plany produkcji dla danego zamówienia mają status 'finalized', automatycznie aktualizuje status zamówienia. Zapewnia synchronizację między produkcją a zamówieniami. |
