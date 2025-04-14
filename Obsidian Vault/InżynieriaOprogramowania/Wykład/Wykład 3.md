## 🔒 Enkapsulacja danych

- Enkapsulacja polega na **ukrywaniu implementacji** oraz **oddzieleniu interfejsu od implementacji**.
    
- Atrybuty klasy powinny być **prywatne** (`private`) i dostępne tylko za pomocą odpowiednich **metod publicznych** (np. gettery i settery).
    
- Każda operacja/metoda powinna być opisana przez:
    
    - **Warunki wejściowe** (input)
        
    - **Warunki wyjściowe** (output)
        

---

## 🧱 Typy klas

### 🔹 Klasy konkretne (implementacyjne)

- Wszystkie metody są **w pełni zaimplementowane**.
    
- Można tworzyć ich instancje.
    

### 🔸 Klasy polimorficzne

- Zawierają **przynajmniej jedną metodę wirtualną** (czyli deklarowaną jako `virtual` w C++).
    
- Umożliwiają **dziedziczenie i nadpisywanie metod**.
    

### 🔶 Klasy abstrakcyjne

- Posiadają **co najmniej jedną metodę czysto wirtualną** (`= 0` w C++).
    
- **Nie można utworzyć ich instancji**.
    
- **Mogą posiadać atrybuty** i inne (nieabstrakcyjne) metody.
    

### 🧩 Interfejsy

- Czysto abstrakcyjna forma klasy:
    
    - **Nie posiadają atrybutów**
        
    - Zawierają **wyłącznie metody czysto wirtualne**
        

---

## 🔗 Rodzaje powiązań między klasami

### 1. 🧬 Dziedziczenie (generalizacja)

- **Najsilniejsze powiązanie** między klasami.
    
- Jest **nierozerwalne** – klasa potomna dziedziczy cechy klasy bazowej.
    
- Umożliwia ponowne użycie kodu oraz polimorfizm.
    

### 2. ➡️ Zależność (ang. _dependency_)

- **Jednokierunkowe powiązanie między operacjami/metodami**.
    
- Może być zrealizowana **nawet jeśli klasa nie ma żadnych atrybutów**.
    
- Wpływ jednej klasy na drugą występuje **tylko w konkretnym kontekście operacji**.
    

### 3. 🔗 Asocjacja (ang. _association_)

- Powiązanie między klasami **realizowane przez atrybuty**.
    
- Jeśli klasy komunikują się poprzez **pola (atrybuty)**, to mamy do czynienia z asocjacją.
    
- Może być:
    
    - Jednokierunkowa
        
    - Dwukierunkowa
        

---

## 💡 Inne informacje

- **Wskaźnik na klasę** – utworzenie wskaźnika (np. `Class* obj = new Class();`) powoduje **stworzenie instancji obiektu**.
    
- **Związek zaprzyjaźnienia** w C++ (`friend`) pozwala jednej klasie/funkcji **mieć dostęp do prywatnych elementów** innej klasy.
    
- **Atrybuty powinny mieć kontraktację z funkcją**, tzn. dostęp do nich powinien być kontrolowany i zgodny z logiką biznesową.