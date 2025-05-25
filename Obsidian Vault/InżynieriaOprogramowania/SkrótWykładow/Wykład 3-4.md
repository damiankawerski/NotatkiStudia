# Diagramy czynności

- Diagramy czynności tworzone są podczas analizy systemu i służą do modelowania przepływu sterowania wykonywanych czynności.
- Możemy je wykorzystać na dwa sposoby:
	- Po pierwsze mogą służyć do modelowania przepływu czynności między poszczególnymi częściami systemu. W tego rodzaju przypadkach diagram czynności można skojarzyć z klasą, interfejsem, przypadkiem użycia...
	- Po drugie te diagramy mogą być użyteczne do modelowania operacji, algorytmów.

- *Ogólny, szczegółowy diagram czynności*
![[Pasted image 20250519105602.png]]

- Przykłady diagramów czynności:

- *Ogólny sposób odpytania urządzenia peryferyjnego*
![[Pasted image 20250519110116.png]]

- *Ogólny sposób usuwania katalogu z zawartością*
![[Pasted image 20250519110206.png]]

- *Szczegółowy diagram czynności*
![[Pasted image 20250519110341.png]]

- *Na diagramach czynności możemy oznaczać punkty wysłania i odbierania sygnału. (Komunikatu)*

![[Pasted image 20250519110458.png]]

- *Diagramy czynności możemy wzbogacić o obsługę wyjątków*

![[Pasted image 20250519110626.png]]

- *Możemy również zapisać strukturalną obsługę wyjątków (wiele wyjątków na raz)*
![[Pasted image 20250519110919.png]]

### Diagramy czynności - ścieżki współbieżne

- *Gdy musimy wymodelować czynności które działają współbieżnie (wątki) które na końcowym etapie są ponownie scalane możemy to zapisać w taki sposób:*

![[Pasted image 20250519111312.png]]

- *Przykład diagramu współbieżnego dla sklepu*

![[Pasted image 20250519111417.png]]

---

# Diagramy obiektów

- Obiekt jest konkretnym wystąpieniem klasy  (przepisu)
- Obiekt hermetyzuje specjalnie utworzoną dla niego komórkę pamięci
- *Przykłady poprawnie przedstawionego obiektu nazwanego lub anonimowego*
![[Pasted image 20250519111715.png]]

-  *W UML możemy przedstawić wartości atrybutów w obiekcie*
![[Pasted image 20250519111959.png]]
- *Możemy także stworzyć obiekt anonimowy (wskaźnik). Robimy tak gdy mamy jedynie nazwę wskaźnika*
![[Pasted image 20250519112134.png]]
- *Na bazie jednej klasy możemy stworzyć wiele obiektów. Zwielokrotnione obiekty oznaczamy tak:*
![[Pasted image 20250519112231.png]]
- Obiekty na diagramach mogą tworzyć związki strukturowe, uczestnicząc w wiązaniach lub agregacjach.
- Wiązania są egzemplarzami powiązań dlatego możemy nadać im nazwę, kierunek, działania, role i właściwy stereotyp
- *Wiązanie obiektów oznaczamy za pomocą linii ciągłej*
![[Pasted image 20250519112605.png]]

- Standardowe typy stereotypów wiązań 
	- `<<association>>` - umieszczony na jednym końcu wiązania wskazuje że obiekt jest widoczny przez to wiązanie
	- `<<global>>` - umieszczony przy obiekcie na końcu wiązania oznacza że obiekt jest widoczny ponieważ jest w otaczającym zasięgu
	- `<<local>>` - obiekt jest widoczny bo jest w lokalnym zasięgu
	- `<<parameter>>` - obiekt jest widoczny, ponieważ jest parametrem
	- `<<self>>` - obiekt jest widoczny, ponieważ to właśnie on odebrał zlecenie wykonania danej operacji
---
# Diagramy stanów

- Diagramy stanów obrazują sposób w jaki elementy modelu zmieniają w czasie swoje własności w odpowiedzi na różnego rodzaju zdarzenia.
- Podstawowym elementem tego diagramu jest ikona stanu.
- Przedstawiona w uproszczony sposób - poprzez podanie nazwy  stanu
- Przedstawiona w sposób szczegółowy - z dodatkowym wyróżnieniem wartości atrybutów oraz podstawowych aktualnie wykonywanych operacji
- *Przykład modelowania obiektu, którego stan opisują wartości przypisane atrybutom, przejścia wewnętrzne, operacje odroczone oraz operacje wykonywane w trakcie trwania stanu*
![[Pasted image 20250519124519.png]]
- *Stan może posiadać aktywne podstany z zaznaczonymi punktami wejścia i wyjścia z sekwencji podstanów*
![[Pasted image 20250519124614.png]]
- *Oprócz prostych przejść UML pozwala na modelowanie alternatywnych przejść pomiędzy stanami przy wykorzystaniu tzw. punktów wyjścia*
![[Pasted image 20250519124835.png]]
---
# Diagramy sekwencji (przebiegu)

- Diagramy sekwencji służą do prezentowania struktury logicznej aplikacji
- Pozwalają modelować wzajemną interakcje obiektów w funkcji czasu jej trwania.
- interakcja traktowana jest jako ciąg zdarzeń występujących w czasie w określonym logicznym  porządku
- Diagram sekwencji składa się z:
	-  Osi czasu (linii życia)
	- Standardowej postaci obiektów
	- Komunikatów
- Obiekty mogą na siebie wzajemnie oddziaływać modyfikując stan atrybutów lub  wywołując różne operacje
- Żądanie wykonania operacji nazywane są komunikatami i składają się z trzech elementów:
	- Wskazania docelowego obiektu do którego komunikat jest skierowany
	- Wskazania udostępnianej przez obiekt docelowy operacji 
	- Dodatkowych (opcjonalnych) informacji określających sposób realizacji żądanej usługi. Przekazywane są jako parametry wywołania.
- Do obiektu źródłowego przesyłana jest wartość zwrotna 
- Operacje która powoduje oczekiwanie obiektu źródłowego nazywamy blokującą albo synchroniczną 
- Operacje która zwraca sterowanie natychmiast po jej wywołaniu nazywamy asynchroniczną albo nieblokującą
- *UML definiuje 3 rodzaje komunikatów*
	- Synchroniczny: 
		![[Pasted image 20250519143943.png]]
	- Zwrotny:
		![[Pasted image 20250519144000.png]]
	- Asynchroniczny:
		![[Pasted image 20250519144021.png]]
- Przykładami komunikatów asynchronicznych są wywołania konstruktora i destruktora.
- *Typowy ogólny diagram przebiegu*
![[Pasted image 20250519144229.png]]

- *Szczegółowy diagram przebiegu*
![[Pasted image 20250519144354.png]]
- *Na diagramie sekwencji możemy zaznaczyć wywołania rekurencyjne*
![[Pasted image 20250519144800.png]]

- Na diagramach sekwencji zazwyczaj korzystamy z poziomych linii, prostopadłymi do linii życia obiektu ale istnieje możliwość dokładniejszego określenia zależności czasowych dla przesyłania komunikatów
- *Robimy to poprzez jawne podanie odpowiednich przedziałów czasowych*
![[Pasted image 20250519145010.png]]

- **Bloki** na diagramach sekwencji definiują grupę komunikatów wspólnie posiadającą pewną właściwość

- Operatory Interakcji:
	- alt (alternative) - określający warunek wykonania bloku operacji, odpowiadający instrukcji if-else; warunek umieszcza się wówczas wewnątrz bloku w nawiasach kwadratowych,
	- opt (optional) - reprezentujący instrukcję if (bez else),
	- par (parallel) - nakazujący wykonać operacje równolegle,
	- critical - blok atomowy, oznaczający obszar krytyczny o najwyższym priorytecie wykonania. Obiekty nie mogą uczestniczyć w innych zadaniach.
	- loop - definiujący pętlę typu for (o określonej z góry liczbie iteracji) lub while (wykonywanej dopóki pewien warunek jest prawdziwy),
	- break - wykonanie fragmentu i zakończenie interakcji,
	- neg – funkcjonalności nieprawidłowe – wskazuje na wyjątki, które muszą zostać obsłużone
	- strict – ścisłe uporządkowanie komunikatów
	- seq - słabe uporządkowanie dotyczy komunikatów z kilku lini mogących wystąpić w dowolnym porządku,
	- ignore – komunikaty nie mają istotnego wpływu na całość komunikacji,
	- consider – istotność – komunikaty muszą zostać wykonane.

![[Pasted image 20250519145818.png]]

### Techniki tworzenia diagramów sekwencji:
- ustalenie otoczenia (operacje, przypadki użycia, itp.)
- zidentyfikowanie obiektów biorących udział w operacji (od lewej umieszczane są obiekty najważniejsze).
- narysowanie linii życia obiektów (jeśli są tworzone i niszczone - dodanie odpowiednich komunikatów).
- dodanie komunikatu inicjującego, kolejne komunikaty pod nim (dodanie parametrów do komunikatów (jeżeli jest to wymagane)).
- dodanie aktywacji (ośrodka sterowania)

--- 

# Diagramy komunikacji (kooperacji)

- Diagramy komunikacji umożliwiają pokazanie kolejności wysyłania komunikatów
- Kolejność obrazowana jest poprzez numery umieszczane na początku etykiet nazwy i ew. listę argumentów (sygnaturę) odpowiedniego komunikatu
- *Notacja stosowana na typowych diagramach komunikacji*
![[Pasted image 20250519152400.png]]


- Diagramy komunikacji pozwalają wymodelować interakcje zachodzącą między obiektami lub/i użytkownikiem systemu.
- W odróżnieniu od diagramów przebiegu obrazują  interakcje obiektów w funkcji czasu
- *Szczegółowy diagram komunikacji obrazujący kolejność kreacji i destrukcji*
![[Pasted image 20250519153626.png]]


- *Zdarza się że obiekt komunikat wysyła do wielu innych obiektów tej samej klasy*

![[Pasted image 20250519154629.png]]


- *Jeżeli komunikat ma być wysłany do dokładnie wszystkich obiektów w systemie i ważna jest kolejność wysyłania. Warunek pętli while oznaczany jest gwiazdką*

![[Pasted image 20250519154805.png]]


---


# Przykłady modelowania systemu

- **Diagram klas dla systemu opisującego pojazd**

![[Pasted image 20250519153816.png]]

- **Diagram sekwencji dla przypadku uruchamiania pojazdu**

![[Pasted image 20250519153932.png]]

- **Diagram kooperacji odpowiadający diagramowi sekwencji** 

![[Pasted image 20250519154100.png]]

---

### Kolejne przykłady

- **Diagram sekwencji**

![[Pasted image 20250519154207.png]]


- **Równoważny diagram komunikacji**

![[Pasted image 20250519154452.png]]


---


# Diagramy współpracy

- Diagramy współpracy pozwalają wymodelować interakcje zachodzącą między obiektami.
- W odróżnieniu do diagramów sekwencji obrazujących przebieg obiektów w funkcji czasu, diagramy współpracy pokazują otoczenie i ogólną organizacje obiektów uczestniczących w konkretnym typie  interakcji np powiązaniu.
- *Definiowanie rodzaju współpracy dwóch obiektów*
![[Pasted image 20250519155413.png]]

- *Ogólna idea używania definicji współpracy obiektów*

![[Pasted image 20250519155458.png]]

---

# Komponenty

- W UML 1.x pliki danych, pliki z kodami programu, programy wykonywalne, biblioteki dołączane dynamicznie, pliki zawierające dane powstałe w wyniku wykonania programu itp. definiowane były odpowiednio jako komponenty procesu wytwórczego, wdrożenia oraz komponenty będące rezultatem wykonania programu.
- Wszelkiego rodzaju fizycznie istniejące pliki na dysku określane są mianem artefaktów i mogą być oznaczane stereotypem `<<artifact>>`
- Komponent jest implementacją przynajmniej jednej liczby klas
- Artefakt (jeśli jest wykonywalny) może być implementacją komponentu
- Stereotyp `<<implement>>` używany jest w przypadku gdy plik wykonywalny implementuje komponent
- Stereotyp `<<manifest>>` używany jest w przypadku gdy chcemy pokazać że komponent wyrażany jest poprzez pliki zawierające jego kod źródłowy
- *Na diagramach UML komponent może być reprezentowany na sposoby*
![[Pasted image 20250519160221.png]]


- Interfejsy są elementami za pomocą których komponenty współpracują.
- *Komponenty i  Interfejsy*
![[Pasted image 20250519161135.png]]

- Komponent to grupa klas pozostających ze sobą w dobrze zdefiniowanych relacjach i służących jednemu celowi.
- *Hierarchiczna struktura komponentów*
![[Pasted image 20250519161607.png]]

- *Niekompozycyjna struktura komponentów*
![[Pasted image 20250519161633.png]]

- **Przykład diagramu wdrożenia**
 ![[Pasted image 20250519161742.png]]