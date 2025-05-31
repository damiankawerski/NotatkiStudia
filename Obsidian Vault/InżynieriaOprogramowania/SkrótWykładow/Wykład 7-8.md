
# Wstęp

- *Typowy cykl życia wyrobu*
![[Pasted image 20250525222149.png]]

---

# Model dojrzałości (CMM/CMMI)

- Jest to model opisujący kluczowe elementy efektywnego procesu konstruowania oprogramowania.
- *Ogólna reprezentacja modelu dojrzałości*
![[Pasted image 20250526101102.png]]

- CMMI jest pięciostopniową skalą oceniającą podejście organizacji do projektów informatycznych.
- Poziomy określamy kluczowymi obszarami procesowymi KPA
	- *Początkowy* - proces jest nieprzewidywalny i słabo kontrolowany.
	- *Zarządzany jakościowo (powtarzalny)* - organizacja reaguje dopiero, gdy wystąpią problemy (KPAs: zarządzanie wymaganiami, planowanie i śledzenie projektów tworzenia oprogramowania, zarządzanie dostawcami, zapewnienie jakości oprogramowania, zarządzanie konfiguracją).
	- *Zdefiniowany* - organizacja jest proaktywna (KPAs: organizacja zorientowana procesowo, definicja procesów, program treningów, zarządzanie integracją oprogramowania, inżynieria tworzenia oprogramowania, koordynacja międzygrupowa, przeglądy dokumentacji).
	- *Zarządzany ilościowo* - Zarządzany ilościowo - proces jest mierzalny i kontrolowany (KPAs: pomiary i analiza procesów, zarządzanie jakością, zapobieganie defektom).
	- *Optymalizowany* - wysiłki organizacji są ukierunkowane na ciągłe doskonalenie (KPAs: innowacje technologiczne, zarządzanie zmianami procesów).


--- 

# Metodyki
- SDLC - System Development Life Cycle

- **Metodyka jest ustandaryzowanym dla wybranego obszaru wiedzy/nauki podejściem do rozwiązywania właściwych problemów. Metodyki abstrahują od merytorycznego kontekstu danego obszaru, a skupiają się na metodach realizacji zadań związanych z zarządzaniem projektem informatycznym.**
- Metodyka to spójny, logicznie uporządkowany zestaw metod i procedur technicznych oraz organizatorskich służących zespołowi wykonawczemu do analizy rzeczywistości a także projektowania pojęciowego, logicznego i/lub fizycznego;
- Metodyka jest to zestaw pojęć, notacji, modeli, języków, technik i sposobów postępowania służący do analizy dziedziny stanowiącej przedmiot projektowanego systemu oraz do projektowania pojęciowego, logicznego i/lub fizycznego.
- Metodyka jest powiązana z notacją służącą do dokumentowania wyników faz projektu (pośrednich, końcowych) jako środek wspomagający ludzką pamięć i wyobraźnię i jako środek komunikacji w zespołach oraz pomiędzy projektantami i klientami.

- *Składniki metodyki*
	- Formalizmy, modele dziedziny problemu, jej statyki i dynamiki
	- Strukturalizacja procesu (cykl życia)
	- Szczegółowe metody i techniki dokumentowania
	- Narzędzia
	- Wymagania merytoryczne
	- Kryteria oceny jakości projektu
	- Zasady planowania i kierowania rozwojem systemu

- *Ogólna reprezentacja cyklu wdrażania systemów informatycznych SDLC*
![[Pasted image 20250526102319.png]]


### Metoda biznesowa lub proces biznesowy

- Seria powiązanych ze sobą działań lub zadań które rozwiązują określony problem lub prowadzą do osiągnięcia określonego efektu.

- **Definiowalność** - proces powinien mieć jasno zdefiniowane granice, wejście oraz wyjście
- **Porządek** - Proces powinien składać się z działań uporządkowanych według ich usytuowania w czasie i przestrzeni
- **Klient** - Musi być odbiorca rezultatów procesu
- **Zwiększanie wartości** - Transformacja w trakcie procesu powinna dawać odbiorcy dodatkową wartość.
- **Osadzenie** - Proces nie może egzystować samodzielnie - musi być wbudowany w strukturę organizacyjną
- **Wielofunkcyjność** - Proces nie może egzystować samodzielnie - musi być wbudowany w strukturę organizacyjną

--- 

# Proces (model) kaskadowy

- Proces projektowania z reguły iteracyjny.
- *Opracowanie kaskadowe*
![[Pasted image 20250526103014.png]]

- Iteracje są jednopoziomowe, nie możemy przeskoczyć z etapu n do n -2. Najwyżej do n - 1
-  Ścisła interpretacja modelu kaskadowego traktuje poszczególne fazy jako niezależne etapy realizacji przedsięwzięcia.
- Ich wykonanie przebiega sekwencyjnie 
- *Zalety modelu kaskadowego*
	- Łatwość zarządzania
	- Łatwość harmonogramowania
	- Łatwość określenia sumarycznych kosztów przedsięwzięcia
	- Łatwość tworzenia dokumentacji
- *Wady modelu kaskadowego*
	- Wysoki koszt błędów popełnionych we wstępnych fazach projektowania
	- Długa przerwa w kontaktach z klientem

--- 

# Proces (model) iteracyjny

- *Opracowanie iteracyjne*
![[Pasted image 20250526103716.png]]

### Koncepcja początkowa 

- Konceptualizacja. Faza ta ma na celu sprecyzowanie abstrakcyjnego pojęcia 

### Planowanie i analiza wymagań
- Jak program będzie używany i jak powinien działać:

	- Analiza przypadków użycia
	- Identyfikacja aktorów - zewnętrznych i współpracujących z systemem
	- Wyznaczenie pierwszych przypadków użycia
	- Szczegółowy model dziedziny problemu 
		- Jako część modelu dziedziny tworzone są obiekty dziedziny opisujące obiekty w przypadkach użycia,
		- Obiekty dziedziny nie są obiektami projektu.
		- Model dziedziny opisuje sposób funkcjonowania świata rzeczywistego
	- Tworzenie scenariuszy
		- Warunki wstępne - co musi być spełnione
		- Niezmienniki - warunki w trakcie trwania
		- Akcje jakie podejmuje aktor
		- Wyniki lub zamiany powodowane przez system
		- Informacje zwrotne
		- Informacje o występowaniu cyklicznym operacji
		- Schematyczny opis przebiegu scenariusza
		- Warunki powodujące zakończenie scenariusza
		- Warunki końcowe
	- *Tworzenie wytycznych dla udokumentowania każdego scenariusza*
	![[Pasted image 20250526104801.png]]
	- Analiza aplikacji - wymagania dot. oprogramowania itd...
	- Analiza systemów - szczegółowy zbiór informacji dotyczących systemów z którymi będzie współpracował projekt
	- Dokumentacja produktu
- *Skrót do wszystkiego*
![[Pasted image 20250526105047.png]]


### Projektowanie
- *Projektowanie* jest procesem przekształcenia zrozumienia wymagań w model który może być zaimplementowany w postaci oprogramowania.
- Dokument projektowy powinien być podzielony na 2 części:
	- Projekt klas - projekt statyczny czyli model klas oraz projekty dynamiczny - jak obiekty współpracują
	- Projekt mechanizmów architektury zawiera szczegóły dotyczące implementacji artefaktów systemu.


- Atrybuty - wewnętrzne dane abstrakcji które nie powinny być widoczne na zewnątrz
- Metody - wewnętrzny interfejs abstrakcji danych i powinne być dostępne dla wszystkich elementów programu odwołujących się do danej abstrakcji
- Identyfikacja wymaganych metod - proste, złożone, utwórz, pobierz, ustaw, powiąż, zwolnij itd...

- **Kontrola hermetyzacji** 
	- Polega na ograniczaniu dostępu do składowych klasy (atrybutów i operacji)

- **Projektowanie według kontraktu**
	-  Program jest poprawny jeżeli jego działanie odpowiada specyfikacji projektowej
	- Główną cechą tej metody jest to że użytkownik jest abstrakcją
	- Użytkownicy są zobowiązani zagwarantować że abstrakcja będzie wywoływana we właściwy sposób
	- DBC polega na spisaniu umowy danej funkcjonalności z resztą kodu. Składa się z 3 punktów:
		-  Warunki początkowe - opisują zobowiązania otoczenia wobec funkcjonalności na początku jej wykonywania
		- Warunki końcowe -  na końcu wykonywania
		- Niezmienniki - przez cały czas wykonywania

- **Model Dynamiczny**
	- Oprócz modelowania relacji ważne jest wymodelowanie tego jak obiekty ze sobą współpracują. 
	- Możemy to zrobić za pomocą diagramu sekwencji które kładą nacisk na kolejność zdarzeń
	- Lub za pomocą diagramów współpracy (komunikacji) które kładą nacisk na obrazowanie współdziałania między klasami

- **Implementacja**
	-  Każda klasa powinna mieć swój plik nagłówkowy
	- Pliki implementacyjne (pliki fizyczne systemu) nazywamy manifestacją plików logicznych (klas)
	- Wyraża się to za pomocą `<<manifest>>`
	- Artefakt zawierający definicje klasy (plik nagłowkowy) oznaczamy `<<header>>`
	- Artefakt zawierający kod źródłowy oznaczamy `<<code>>`


--- 


# Testowanie

- **Weryfikacja oprogramowania** jest procesem sprawdzania czy wytwarzane oprogramowanie jest zgodne z wytycznymi zasad programowania. 
- Weryfikacja dokonywana jest podczas testów systemowych pojedynczego produktu,
- oraz testów integracyjnych, po wprowadzeniu produktu do istniejącego już i działającego środowiska informatycznego.

- Weryfikacje można przeprowadzić na 2 spsoby:
	- Statyczny - inspekcja kodu
	- Dynamiczna - po skompilowaniu z użyciem danych testowych

- **Walidacja oprogramowania** jest procesem sprawdzania czy oprogramowanie jest zgodne z oczekiwaniami użytkownika.
- Największe znaczenie mają analiza dokumentacji oraz testy akceptacyjne przeprowadzone przez użytkownika.

### Planowanie testów

- Skonstruowanie odpowiedniej sekwencji (planu) testów, opartej na cyklu produkcyjnym oprogramowania, pozwala na wydajne zarządzanie czasem i zasobami ludzkimi
- Ogólne planowanie testów należy rozpocząć już na etapie analizy wymagań
- Szczegółowy plan testów wykonuje już po zweryfikowaniu całości dokumentacji i wyraźnym wyspecyfikowaniu elementów systemu podlegających testom.


### Główne etapy testowania

- **Analiza dokumentacji** - powinna stanowić najwcześniejszy etap kontroli jakości tworzonego oprogramowania. 
- Wykonuje się ją przed przystąpieniem do generowania kodu.
- Analiza dokumentacji powinna być wykonywana w oparciu o całość dokumentacji powstałej we wczesnej fazie projektu

- **Testy systemowe** - Ten rodzaj testów wykonuje się po zaimplementowaniu systemu/programu, ale przed jego wdrożeniem
- Zasadniczym celem jest sprawdzenie, czy w kodzie nie wystąpiły błędy mające wpływ na stabilność produktu

- **Testy integracyjne** - umożliwiają przetestowanie każdego nowego elementu włączanego do systemu
- Testuje się zarówno każdą istotnie nową funkcjonalność, jak i to, czy jej pojawienie się ma wpływ na wcześniejsze zachowanie się systemu traktowanego jako całość.

- **Testy regresji** - Regresja jest zjawiskiem niezamierzonej utraty jakiejś funkcjonalności powstałym w nowej wersji programu
- Testy regresji wykonuje się każdorazowo, gdy do systemu wprowadzamy nową funkcjonalność, moduł, bibliotekę lub komponent
- Celem testów regresji jest sprawdzenie, czy dokonane zmiany nie wpłynęły negatywnie na sposób funkcjonowania systemu

--- 

# Metryki oprogramowania

- *Metryka oprogramowania* jest miarą pewnej własności oprogramowania lub jego specyfikacji
- Metrykę określa się jako funkcje odwzorowującą jednostkę oprogramowania w wartość liczbową
- Ta wyliczona wartość jest interpretowalna jako stopień spełnienia pewnej własności jakości jednostki oprogramowania.

- Metryki dzielą się na:
	- Związane z analizą kodu źródłowego - statyczne
	- badające zachowanie uruchomionego programu - dynamiczne.

- 
