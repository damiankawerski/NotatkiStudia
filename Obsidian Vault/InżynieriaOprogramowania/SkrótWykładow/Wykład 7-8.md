
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
- 