# Kreacyjne
---

### Metoda wytwórcza
- Polimorficzny wzorzec który obsługuje tworzenie obiektów 
`TUTAJ POWINIEN BYC RYSUNEK`


### Fabryka Abstrakcyjna

![[Pasted image 20250531151956.png]]

### Prototyp
- Tworzenie nowych obiektów poprzez klonowanie juz istniejącego ( tutaj za pomocą pointerów )
![[Pasted image 20250531152247.png]]


### Builder

- Do klas które potrzebują specjalnych metod budowania
- np StringBuilder
- Może to być klasa w klasie
- ![[Pasted image 20250607142651.png]]
# Strukturalne
---

### Fasada
- Jedna główna klasa która ukrywa skomplikowaną strukturę klas której używa
![[Pasted image 20250522224944.png]]
### Kompozyt
- Chodzi o to że traktujemy zbiór elementów tak samo jak jeden element.
![[Pasted image 20250602214756.png]]

### Singleton
- Antywzorzec 
- Chodzi o to że możemy stworzyć tylko jedną instancje danej klasy 
- Ma prywatny konstruktor i publiczną metode getInstance
- ma statyczne pole instance

### Dekorator

![[Pasted image 20250531152016.png]]


### Proxy

![[Pasted image 20250601180342.png]]


### Adapter

- Przykładem jest tworzenie adaptacji sterowników do nowego systemu. 
- Sterowniki działają tak samo ale nowy system używa innych nazw
- Chcemy wykorzystać stare funkcje w nowym systemie więc tworzymy Adapter
![[Pasted image 20250602215650.png]]


### Bridge

- Masz klasę z różnymi wariantami implementacji, np. różne sposoby rysowania figur – zamiast robić pierdyliard klas potomnych (jak w drzewie dziedziczenia), rozdzielasz **abstrakcję** i **implementację**.
![[Pasted image 20250615150944.png]]


### Flyweight
- Zakłada minimalizacje zużycia pamięci
- Dzielimy cechy między obiekty
- Fabryka która zwraca wskaźnik zamiast nowego obiektu
![[Pasted image 20250615154542.png]]




---





# Czynnościowe
---

### Obserwator na przykładzie
- Interfejs który powiadamia przeciwników o statusie bohatera
- W klasie bohatera trzymamy kolekcje polimorficznych klas obserwatora
- Relacja to będzie powiązanie bo wskaźnik
- Każdy przeciwnik implementuje obserwatora
- 



---

### Iterator

- Nazwa mówi sama za siebie, dostarczamy obiekt który pozwala przechodzić po kolejnych elementach jakiejś kolekcji
 ![[Pasted image 20250531160545.png]]

### Command
- Mamy interfejs który posiada metodę execute()
- Jakieś konkretne implementacje tego interfejsu wykonują konkretną komende
- Często wrzuca się to do kolejki
![[Pasted image 20250604201847.png]]


### Memento

- Możliwość tworzenia kopii zapasowych
![[Pasted image 20250604203746.png]]


### Mediator

- Mamy wiele klas w projekcie. Każda klasa komunikuje się z kilkoma innymi. W efekcie dostajemy mnóstwo powiązań i wzajemnych zależności. Do rozplątania tego rodzaju bałaganu może posłużyć Mediator.
- Mediator to klasa, która enkapsuluje komunikację między elementami systemu. Poszczególne klasy nie muszą niczego o sobie wiedzieć (brak bezpośrednich powiązań).
- Zamiast tego wywołują odpowiednie metody Mediatora, który załatwia resztę - zdobywa potrzebne informacje i przekazuje je tam gdzie trzeba.
![[Pasted image 20250607133958.png]]


### Interpeter

- Wzorzec dotyczy zagadnienia ewaluowania wyrażeń pewnego języka.
- W praktyce tak działa funkcaj eval w JS
- Interpretujemy jakieś wyrażenie 
- Działa na zasadzie kompozytu tj jak mamy wyrazenie to Suma i Odejmowanie też powinny implementować wyrazenie i działać jako kompozyt
![[Pasted image 20250607144321.png]]

### Strategia
- Jeden algorytm ale różne implementacje
- Tutaj weryfikacja przez różne klasy
- Dobrym przykładem będzie sortowanie czasami bedziemy potrzebować merge sorta a czasami insertion sorta czy coś takiego

![[Pasted image 20250611220328.png]]


### Chain of Responsibility
- Chodzi o to że mamy listę łańcuchów przetwarzających różne żądania
- Jeśli pierwszy obiekt nie obsłuży to obsłuży kolejny
- Struktura może być dynamicznie modyfikowana i rozszerzana o nowe obiekty przetwarzające żądania (także w trakcie działania programu).
![[Pasted image 20250611222142.png]]

### Metoda Szablonowa
- Mamy 2 wersje algorytmu
- Np sortowanie rosnąco i malejąco
- Zamiast implementować 2 wersje algorytmu wyciągamy go do klasy nadrzędnej
- Klasa nadrzędna posiada zarys algorytmu 
- tworzymy dwie klasy pochodne, w których implementujemy brakujący element - jedna klasa implementuje metodę porównaj() tak, aby pozwalała na sortowanie rosnąco, a druga malejąco.
![[Pasted image 20250611223050.png]]

### Stan

- Mamy klase która może zmieniać swój stan
- Np vendingMachine - wrzucimy monete mamy stan ze jest przepelniony bedzie mial inną zawartość metod
![[Pasted image 20250612195947.png]]


### Wizytator

- Wzorzec **Wizytator** (Visitor) to wzorzec **behawioralny** (zachowania). Umożliwia dodanie nowych operacji do obiektów bez zmieniania ich struktur (czyli klas). Działa poprzez przekazywanie wizytatora do akceptującego obiektu, który wywołuje odpowiednią metodę `visit()`.
- Klasy, na których wizytator ma działać, posiadają metodę accept(Visitor). Działanie takiej metody sprowadza się do wywołania visitor.visit(this).