# Budowanie modeli 

- Zaprojektowanie i wdrożenie projektu rozwiązującego dany problem sprowadza się do poprawnego rozwiązania problemu z punktu widzenia teorii, którą się posługujemy.
- Rozwiązanie problemu możemy podzielić na:
	- Zaprojektowanie architektury i abstrakcji programu w języku modelowania.
	- Stworzenie prawidłowej implementacji w języku programowania.
- Model rozumiemy jako zbiór ogólnych założeń, pojęć i zależności pozwalający w uproszczony sposób opisać wybrany aspekt rzeczywistości.
![[Pasted image 20250518003845.png]]

- Modele są tworzone z dwóch powodów:
	- Lepsze zrozumienie dziedziny problemu
	- Umożliwienie wymiany informacji w trakcie rozwiązywania problemy przez zainteresowane osoby
- Celem modelu jest stworzenie poprawnej abstrakcji rzeczywistego świata.
- Model powinien być możliwie mało skomplikowany.
- Model powinien poprawnie odzwierciedlać świat rzeczywisty
- Na podstawie modelu powinno móc się przewidzieć zachowanie bytów w prawdziwym świecie
- *System komputerowy to zbiór podsystemów sformowany w celu wykonania określonego zadania i opisany za pomocą pewnego zestawu modeli, z których każdy opisuje inny aspekt rzeczywistości.*

--- 
# UML jako język modelowania

- UML - Unified Modelling Languaged
- Związki pomiędzy strategią tworzenia, obiektowo-zorientowaną strukturą oraz cechami współczesnego oprogramowania: 
 ![[Pasted image 20250518005907.png]]
 
 - Związek pomiędzy językiem programowania a językiem modelowania: 
 ![[Pasted image 20250518010008.png]]
 --- 
# Zawartość UML

### Model UML może zawierać 5 perspektyw obrazujących różne aspekty systemu

- perspektywa przypadków użycia – opisuje zachowanie systemu z punku widzenia użytkowników, analityków oraz osób wykonujących testy. Zawiera zarówno elementy statyczne, opisane za pomocą diagramów przypadków użycia, jak i dynamiczne, opisane za pomocą diagramów przebiegu, kooperacji, stanów i czynności.

- perspektywa projektowa – uwzględnia opis klasy, interfejsów, sekwencji i kooperacji, które razem składają się na opis danego problemu oraz jego rozwiązanie. Elementy statyczne wyrażane są za pomocą diagramów klas i obiektów, dynamiczne – za pomocą diagramów interakcji, stanów i czynności.

- perspektywa procesowa – odzwierciedla mechanizm kreowania wątków i procesów w systemie. Elementy statyczne i dynamiczne wyrażanie są za pomocą diagramów klas, obiektów, interakcji, stanów i czynności, przy czym główny nacisk kładzie się na klasy aktywne.

- perspektywa implementacyjna – opisuje komponenty i artefakty, użyte do scalenia i fizycznego udostępnienia systemu. Wiąże się ona z zarządzaniem konfiguracją poszczególnych wersji systemu. Elementy statyczne wyrażanie są za pomocą diagramów komponentów i artefaktów.

- perspektywa wdrożeniowa – opisuje węzły modelujące sprzęt, na którym system będzie uruchomiony. Wiąże się ona głównie z rozmieszczeniem, dostarczeniem i instalacją części systemu fizycznego. Aspekty statyczne wyrażane są za pomocą diagramów wdrożenia.

- *UML definiuje 14 podstawowych typów diagramów opisujących dwa aspekty modelowanego systemu*

![[Pasted image 20250518010931.png]]

---
# Przypadki użycia

-  W trakcie analizy systemu należy zdefiniować wymagania stawiane systemowi.
-  Pozwala to zrozumieć jak system będzie się zachowywał w kluczowych fazach swojego działania.
-  Pozwala też wyznaczyć granicę oddziaływania świata rzeczywistego (Użytkownika) i systemu
-  Aktor (Użytkownik) komunikuje się z systemem poprzez zdefiniowane przypadki użycia
- *Najprostszy model przypadków użycia* 
 ![[Pasted image 20250518203023.png]]
-  Przypadki użycia mogą pozostawać w relacjach dziedziczenia lub zależności
-  Dziedziczenie pozwala na współdzielenie większości zachowania ogólnego przypadku
-  *Poprzez dziedziczenie możemy reprezentować tzw. przebiegi podstawowe i opcjonalne*
	
![[Pasted image 20250518203328.png]]


- W przebiegu podstawowym p1 jest przypadkiem bazowym i zawsze występuje jako 1 w kolejności
- P2 zawsze używa P1
- Stereotyp `<<include>>` wskazuje na wspólny fragment wielu przypadków użycia w przebiegach podstawowych w których wszystkie operacje powinny być zawsze wykonywane.
-  *Przebieg podstawowy*
 ![[Pasted image 20250518203731.png]]

-  W przebiegu opcjonalnym przypadek występujący pierwszy w kolejności działania (p1) jest czasami rozszerzany o p2), czyli p2 rozszerza p1
-  Przypadek opcjonalny oznaczamy stereotypem `<<extend>>`
- *Przebieg opcjonalny*

![[Pasted image 20250518204210.png]]


- Aktorzy mogą być:
	- Osobami wchodzącymi w interakcję z systemem,
	- Systemami zewnętrznymi
	- Częściami systemu, które mają wpływ na funkcjonowanie systemu, ale same przez ten system nie mogą być zmieniane (jak np. zegar systemowy).

- Aktorów rozpoznajemy następująco 
	- Kto będzie używał podstawowych funkcji?
	- Kto wymaga wspomagania w swej pracy i przy których zadaniach?
	- Kto ma administrować systemem, konserwować i utrzymywać w działaniu?
	- Jakimi urządzeniami zawiaduje system?
	- Z którymi systemami system ma współpracować (np. wymieniać dane)?
	- Kto jest zainteresowany rezultatami działania systemu?


- Model przypadków użycia dostarcza spojrzenia na system z pozycji aktorów i nie włącza zbyt wielu szczegółów działania samego systemu


### Przykłady szczegółowości diagramów przypadków użycia.

- *Prosty diagram przypadków użycia systemu  '''Restauracja''*

	![[Pasted image 20250518205139.png]]

- *Szczegółowy diagram przypadków użycia systemu ''Restauracja''* 

![[Pasted image 20250518205243.png]]

---

# Diagramy klas

- Klasa jest abstrakcją obiektów z modelowanej dziedziny problemu.
- W konwencji UML dane zdefiniowane w klasie nazywamy **Atrybutami (Pola)**
- Operujące na tych danych funkcje nazywamy **Operacjami (Metody)**
- Klasa w UML ma zazwyczaj 3 pola:
	-  Najwyższe pole - Nazwa 
	-  Środkowe pole - Atrybuty
	-  Najniższe pole - Operacje
- Opcjonalnie możemy rozszerzyć o jeszcze jedno 4 pole które zawiera informacje o zobowiązaniach tej klasy, czyli za co jest ona odpowiedzialna

- Operacje w klasie możemy oznaczyć ich typem:
	- Stereotyp `<<create>>` oznacza konstruktor klasy
	- Stereotyp `<<destroy>>` oznacza destruktor klasy
	- Stereotyp `<<update>>` oznacza operacje zdolną zmienić stan obiektu który będzie utworzony w bazie klasy np. setter
	- Stereotyp `<<query>>` oznacza operacje która nie zmienia stanu obiektu

- *Przykład zawartości ikony klasy UML*

	![[Pasted image 20250518210557.png]]


- Mimo że można stworzyć atrybuty publiczne, należy dążyć do tego aby były prywatne
- Prywatyzowanie atrybutów nazywamy enkapsulacją

### Deklaracja atrybutów: 

- ![[Pasted image 20250518211240.png]]

- Najczęściej stosowane ograniczenia to: 
	- {ordered} – obiekty reprezentowane przez atrybut są uporządkowane
	- {unordered} – obiekty są nieuporządkowane,
	- {unique} – obiekty nie powtarzają się,
	- {nonunique} – obiekty mogą się powtarzać
	- {readOnly} – wartość atrybutu przeznaczona jest tylko do odczytu
	- {frozen} – wartość atrybutu nie może być zmodyfikowana po jej przypisaniu

### Deklaracja operacji:

- ![[Pasted image 20250518211250.png]]

	gdzie lista parametrów operacji:
	![[Pasted image 20250518211454.png]]

- Tryb:
	- in – parametr wejściowy, nie może być modyfikowany
	- out – parametr wyjściowy, może być modyfikowany
	- inout – parametr wejściowy, wyjściowy, może być modyfikowany

- Właściwość:
	- leaf – funkcja niepolimorficzna (nie może być redefiniowana),
	- isQuerry – funkcja nie zmieniająca stanu obiektu,
	- sequental, guarded, concurent (mają zastosowanie przy operacjach współbieżnych).

### Typy operacji

- Konstruktor - wykorzystywany w momencie tworzenia obiektu
- Destruktor - wykorzystywany w momencie usunięcia obiektu z pamięci
- Mutator - operacja zmieniająca stan atrybutu w klasie `<<update>>`
- Akcesor - operacja odczytująca stan atrybutu w klasie `<<query>>`
- Iterator - przetwarzanie kolejnych elementów struktury danych
- Finalizator - w językach których jest garbage collector jest wywoływana jako swego rodzaju destruktor
- Operacja statyczna  - operacja która jest związana z klasą ale nie z konkretnym obiektem tej klasy. Przykładem jest getInstance() we wzorcu Singleton
- Własność - podobna jest do atrybutu ale może zachowywać się jak operacja

- *Możemy zdefiniować warunki wstępne i końcowe operacji które modelują wymagany stan systemu jak i oczekiwany stan systemu. Pozwala to na opisanie zadania realizowanego przez operacje*

### Rodzaje klas

- **Klasy konkretne** to klasy w której wszystkie operacje zostały zaimplementowane
- **Klasy polimorficzne** to klasy w których zdefiniowano przynajmniej jedną operacje wirtualną (abstrakcyjną). Są to między innymi interfejsy
- **Klasy abstrakcyjne** zawierają przynajmniej jedną operację czysto wirtualną (metody abstrakcyjne) 
	- W UML nazwę klasy abstrakcyjnej piszemy *kursywą* którą piszemy również nazwy operacji wirtualnych 
	- *Przykład klasy abstrakcyjnej
	
![[Pasted image 20250518213826.png]]
- **Metaklasa** to klasa dysponująca specjalnym zestawem metod odpowiadającym podstawowym operacjom klasy, takim jak: sposób tworzenia obiektów, destrukcja obiektów, wywoływanie metod, stosowanie mechanizmów dziedziczenia, przypisywanie wartości atrybutom, uzyskiwanie dostępu do atrybutów, mechanizmy posługiwania się wskaźnikami
- **Klasy aktywne** (stworzone na ich bazie obiekty) mogą być w projektowanym systemie źródłem nowego procesu lub wątków i oznacza się ję tak: 
	![[Pasted image 20250518214111.png]]

- **Typ wyliczeniowy** i **Struktura** to specjalne typy które będą z reguły agregować z klasami do których przekazują swoją zawartość w postaci parametrów 
![[Pasted image 20250518221417.png]]
---



# Związki w diagramach klas

### Generalizacja (dziedziczenie)

- Najbardziej oczywistą dla osób poznających UML jest relacja **dziedziczenia** (generalizacji). Do jej zaznaczenia wykorzystujemy **strzałkę z ciągłą linią i niezamalowanym, trójkątnym grotem**. Strzałka powinna być **skierowana w stronę klasy bazowej**. Dobrą praktyką jest umieszczanie klas pochodnych poniżej klasy bazowej.
![[Pasted image 20250518214616.png]]
### Realizacja (interfejsu)

- Drugi, dość podobny przypadek, dotyczy **realizacji interfejsu**. Strzałka również ma **trójkątny, niezamalowany grot**, ale **linia jest przerywana**. Grot znajduje się **po stronie interfejsu**.
![[Pasted image 20250518214710.png]]
### Kompozycja 

- Kolejny rodzaj relacji to **kompozycja**. Tutaj mówimy o sytuacji, w której jedna z klas stanowi nieodłączną część składową innej. Czas życia obiektów obu klas jest ściśle powiązany - obiekty są tworzone i usuwane w tym samym czasie (stworzenie całości wymaga stworzenia części składowej; usunięcie całości z pamięci pociąga za sobą usunięcie części składowej). Kompozycję oznacza się za pomocą **ciągłej linii z zamalowanym grotem w kształcie rombu**. Grot znajduje się po stronie klasy reprezentującej całość.

![[Pasted image 20250518214930.png]]
### Agregacja

- Podobną, ale nieco “luźniejszą” relacją jest **agregacja**. Również mówimy tutaj o formie relacji części do całości, jednak na znacznie luźniejszych zasadach. Obiekty obu klas mogą istnieć niezależnie od siebie. W praktyce zwykle wiąże się to z sytuacją, w której jedna z klas zawiera modyfikowalną kolekcję obiektów innej klasy. Agregację oznaczamy **ciągłą linią z pustym rombem** po stronie całości.
![[Pasted image 20250518215031.png]]
### Powiązanie

- Następny rodzaj relacji to **powiązanie**. Na poziomie implementacji określa się tak głównie sytuacje, w których jedna z klas zawiera w swoich polach referencję/wskaźnik na obiekt innej klasy. Powiązania mogą być jedno- lub dwustronne. Oznacza się je **ciągłą linią z otwartym grotem** wskazującym na kierunek powiązania (lub po prostu linią w przypadku powiązania dwustronnego).
![[Pasted image 20250518215103.png]]
- Możemy również zrobić powiązania dwustronne:
 ![[Pasted image 20250518220723.png]]
### Zależność

- **Zależność** między klasami dotyczy scenariusza, w którym jedna z klas w jakiś sposób używa obiektów innej klasy. Z reguły obiekty nie pamiętają o sobie (nie przechowują wzajemnych referencji, jak ma to miejsce w przypadku powiązania), a współpraca odbywa się jedynie na poziomie metod (np. metoda jednej z klas przyjmuje w argumencie referencję na obiekt innej klasy). Zależność oznacza się **przerywaną linią z otwartym grotem**. Grot powinien znajdować się po stronie klasy niezależnej (tej, której kod nie odwołuje się do drugiej klasy).
![[Pasted image 20250518215148.png]]
- Możemy wyróżnić **Zależność zaprzyjaźnioną** gdzie funkcje nienależące do danej klasy mogą uzyskiwać dostęp do jej elementów prywatnych.
![[Pasted image 20250518220509.png]]



