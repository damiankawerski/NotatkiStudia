# MDA, MDD

- *Relacje między technologią a analitykiem/ekspertem/projektantem itd.*
![[Pasted image 20250628181442.png]]

- **MDA** - *Model-Driven Architecture* w rzeczywistości jest rozwinięciem opracowania iteracyjnego z wprowadzeniem mechanizmów automatycznej transformacji modeli.
- W praktyce użycie MDA sprowadza się do:
	- Przeniesienia ciężaru rozwoju systemu na wyższy poziom abstrakcji i nadanie modelowaniu centralnej roli
	- Ścisłego oddzielenia warstw systemu
	- Automatycznej generacji kodu z modelu
	- Wprowadzenie mechanizmów automatycznej weryfikacji i walidacji kodu

- Zgodnie z założeniami **OMG** - *Object Management Group* wyróżnia się cztery warstwy oprogramowania tworzonego zgodnie z wytycznymi MDA:
	- **CIM** - *Computation-Independent Model* - model dziedzinowy, nie pozostający w ścisłej relacji z technologią informatyczną; model biznesowy - zbiór powiązanych ze sobą działań lub zadań które rozwiązują określony problem lub prowadzą do osiągniecia konkretnego efektu. Model biznesowy często opisują diagramy czynności.
	- **PIM** - *Platform-Independent Model* - abstrakcyjna niezależna od platformy systemowej i programistycznej specyfikacja systemu wykorzystująca model.
	- **PSM** - *Platform-Specific Model* - model odwzorowany na konkretne rozwiązania wybranej platformy systemowej i programistycznej.
	- **Code** - automatycznie generowany kod niskopoziomowy.

- *Cykl życia oprogramowania tworzonego zgodnie ze standardem MDA*
![[Pasted image 20250628182242.png]]



- *Ogólne założenia MDA*
![[Pasted image 20250628182357.png]]


### Główne standardy przyjęte w metodyce MDA:
- UML jest standardowym językiem do definiowania metamodeli
- **XML Meta-Data Interchange XMI** jako standardowy mechanizm wymiany metadanych i metamodeli za pomocą XML pomiędzy różnymi narzędziami wizualnego modelowania
- **Common Warehouse Metamodel CWM** jako standardową specyfikacje do definiowania struktury i semantyki metadanych w hurtowniach danych i eksploracji danych.
- **MOF-to-IDL mapping** - standardowy mechanizm dostępu do metadanych za pomocą API (niezależnie od j. programowania i modelu obiektowego)
- Mapowanie metamodeli do języka Java - **MOF-to-Java mapping** jako standardowy dostęp do metamodeli w Javie.
- **QVT (Query/View/Transformation)** - jest standardem dla modelu transformacji, a ściślej mówiąc QVT jest językiem pozwalającym zaprojektować automatyczne transformacje między modelami UML.

--- 


# Metamodel

- *Model i metamodel*
![[Pasted image 20250628183329.png]]

![[Pasted image 20250628183353.png]]


- **Metamodel** to mechanizm/model który definiuje język i gramatykę służącą do wyrażania innych modeli. 

- *Stos metamodeli*
![[Pasted image 20250628183553.png]]


- Modele reprezentują zjawiska ze świata rzeczywistego i są egzemplarzami swoich własnych metamodeli. W terminologii tej języki są nazywane metamodelami, zaś stworzone w tych językach artefakty (włączając programy wykonywalne) nazywane są modelami.

- **MOF Meta-Object Facility** to model który definiuje język do opisu metamodeli - meta-metamodel (metajęzyk)
- MOF charakteryzuje mechanizmy niezbędne do przechowywania i uzyskiwania dostępu do różnych języków
- UML i MOF stanowią podstawę czteropoziomowego stosu modeli metodyki MDA.

- Na poziomie M0 występują konkretne realizacje modeli, na przykład konkretne obiekty generowane w trakcie wykonania programu. Na poziomie M1 występują modele, np. kody Object Pascala, Javy, C#, C++ generowane na podstawie diagramów klas. Na poziomie M2 mamy do czynienia z metamodelami, które odgrywają rolę gramatyk do definiowania modeli np. pojęcia generalizacji, powiązań i zależności klas. Na poziomie M3 występuje meta-metamodel. W standardzie MDA, MOF umożliwia definiowanie wielu metamodeli na poziomie M2.


- *Struktura warstwowa UML*
![[Pasted image 20250628183958.png]]

![[Pasted image 20250628184011.png]]


*Tabela M0-M3*

![[Pasted image 20250628184148.png]]
![[Pasted image 20250628184153.png]]

- Na poziomie M0 występują konkretne przypadki (realizacje) modeli, na przykład konkretne wykonanie programu w C++.
- Na poziomie M1 występują modele, na przykład program w C++.
- Na poziomie M2 występują metamodele, które odgrywają rolę gramatyk do definiowania modeli.
- Na poziomie M3 występuje meta-metamodel. W standardzie MDA, MOF umożliwia definiowanie wielu metamodeli na poziomie M2.

- *Relacje między UML, XMI a kodem*
![[Pasted image 20250628184330.png]]

- *Rola XMI*
![[Pasted image 20250628184458.png]]


- **DTD - Document Type Definition** celem tego jest definiowanie poprawnie zbudowanych bloków dokumentu XML. Określa ono strukturę dokumentu i listę poprawnych elementów
- Zalety DTD:
	- dzięki DTD każdy dokument XML może nieść ze sobą opis swojego własnego formatu.
	- niezależne grupy ludzi mogą ustalić jakiś DTD do wymiany danych między sobą.
	- można sprawdzić poprawność otrzymanych lub też swoich własnych danych.

 - **XML Schema** - jest standardem służącym do definiowania struktury dokumentów XML. XML Schema posiadając znacznie większe możliwości stanowi wygodną alternatywę dla DTD.
 - Zalety XML Schema:
	 - XML Schema jest częścią XML, w odróżnieniu od DTD nie będącego częścią standardu XML,
	 - dokumenty zawierające definicje XML Schema zapisuje się w odrębnych plikach .xsd (XML Schema Definition).

- *Struktura typowych środowisk MDA/MDD*
![[Pasted image 20250628184825.png]]


- *Odmiana "Translation" MDA*
![[Pasted image 20250628184901.png]]

- *Odmiana "Elaboration" MDA*
![[Pasted image 20250628184939.png]]


- *Typowa zawartość CIM*
![[Pasted image 20250628185008.png]]


- *Typowa zawartość PIM*
![[Pasted image 20250628185045.png]]

- *Typowa zawartość PSM*
![[Pasted image 20250628185103.png]]

--- 
# DSM - Domain Specific Modeling (Modelowanie dziedzinowe)

- *MDD/MDA -> DSM*
![[Pasted image 20250628185223.png]]

- Model systemu jest zapisywany w języku dziedzinowym DSL (dedykowanym języku specyficznym dla danej dziedziny problemu);
- Generator kodu automatycznie przekształca model w kod specyficzny dla platformy.

- Zalety:
	- Modelowanie przy użyciu naturalnych pojęć wprost z dziedziny problemu
	- Automatyczne generowanie kodu;
	- Przydatność w przypadku tzw. linii produktowych (software product line).
- Wady:
	- Konieczność opracowania specyficznego języka dziedzinowego oraz wbudowanego generatora kodu;
	- Duży zasób wiedzy oraz doświadczenie projektanta języka.

- *Porównanie modelowania tradycyjnego z MDA i DSM*
![[Pasted image 20250628185354.png]]


- *Tradycyjny sposób generowania kody wykonywalnego*
![[Pasted image 20250628185434.png]]


- *generowanie kodu w oparciu o mechanizmy MDA*
![[Pasted image 20250628185500.png]]

- **Mechanizmy MDA mogą służyć jako wsparcie dla każdej istniejącej metodyki tworzenia oprogramowania.**