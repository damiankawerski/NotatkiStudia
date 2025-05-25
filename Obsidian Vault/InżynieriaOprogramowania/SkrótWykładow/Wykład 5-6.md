# Relacje wyrażania (manifest) elementów logicznych

- Związek pomiędzy klasą a jej plikami implementacyjnymi nazywamy pokazywaniem, manifestacja lub wyrażaniem.
- Na diagramach UML związek ten w postaci zależności oznaczamy stereotypem `<<manifest>>`
- Artefakt zawierający definicje klasy (plik nagłówkowy) oznacza się stereotypem `<<header>>`
- Artefakt zawierający implementacje metod klasy oznacza się stereotypem `<<code>>`
- *Wyrażanie elementu logicznego przez artefakty C++*
![[Pasted image 20250525212500.png]]

- *Dla javy*
![[Pasted image 20250525212820.png]]

--- 


# Pakiety

- Pakiety służą do grupowania i systematyzowania składników modelu o podobnym przeznaczeniu we wspólnej przestrzeni nazw.
- Wszystkie elementy pakietu muszą posiadać unikatowy identyfikator.
- *Podstawowa reprezentacja pakietu*
![[Pasted image 20250525213458.png]]

- Artefakt to plik - oznaczamy go stereotypem `<<artifact>>`
- Oprócz artefaktów można grupować klasy, interfejsy, komponenty, operacje, przypadki użycia, diagramy lub inne pakiety.
- Pakiety mogą udostępniać swoje elementy innym pakietom lub importować z innych pakietów.
- *Operacje na pakietach*
![[Pasted image 20250525213645.png]]

- Na obrazku widać zasady importowania pakietów za oznaczane stereotypami `<<import>>` oraz `<<access>>`
- Jeżeli element jest widoczny tylko w obrębie macierzystego pakietu nazywamy go prywatnym, jeśli można do niego dostać dostęp do jest publiczny
- *Przykład wizualizacji zawartości pakietów*
![[Pasted image 20250525213854.png]]

--- 

# Diagramy wdrożenia

- Diagramy wdrożenia służą do zobrazowania fizycznej architektury projektowanego systemu.
- Podstawowym elementem wdrożenia jest węzeł.
- Podstawowymi stereotypami są:
	- `<<proccessor>>` który może wykonać kod programu lub komponentu
	- `<<device>>` które jest przyłączane do węzła i współpracuje z programem (drukarka)
- Możemy także oznaczyć konkretny sprzęt:
	- `<<pc server>>`
	- `<<pc client>>`
	- `<<user pc>>`
- W trakcie modelowania struktury programowej podstawowymi stereotypami są:
	- `<<artefact>>`
	- `<<executable>>`
	- `<<database>>`
	- `<<library>>`
	- itp..
- *Przykładowy diagram wdrożenia*
![[Pasted image 20250525214458.png]]

- *Alternatywna notacja dla węzłów*
![[Pasted image 20250525214544.png]]

- *Przykład diagramu wdrożenia*
![[Pasted image 20250525214719.png]]

--- 

# Diagramy harmonogramowania zadań

- Diagramy te mają szczególne zastosowanie podczas modelowania oprogramowania obsługującego systemy wbudowane.
- Doskonale opisują interakcje obiektu stworzonego na bazie klasy w aspekcie czasu trwania sekwencji zmian wartości w czasie.
- *Podstawowa notacja stosowana na diagramach harmonogramowania
![[Pasted image 20250525214946.png]]

---

# Mechanizmy rozszerzania

- UML nie może przewidzieć potencjalnych problemów mogących powstać w trakcie budowania modelu dowolnego systemu. 
- Standard UML umożliwia jego rozbudowywanie w kontrolowany sposób dopuszczając stosowanie następujących mechanizmów:
	- Stereotypy
	- Notatki
	- Metki
	- Ograniczenia
- *Stereotypy umożliwiają rozszerzenie notacji UML*
- *Notatki umożliwiają rozszerzenie listy właściwości dowolnego bloku UML*
![[Pasted image 20250525215338.png]]
- *Ograniczenie jest przedstawiane jako łańcuch znaków przedstawionych w nawiasach {}*
![[Pasted image 20250525215443.png]]

- Metki mogą być rozszerzalnymi elementami modelu w którym używany jest stereotyp zawierający ich definicje 
- Oznaczenie metki zawiera znacznik znak równości oraz wartość `znacznik = wartosc`
	- Znacznik jest nazwą metki
	- Wartość to przypisany literał
- *Na rysunku zastosowano stereotyp* `<<property>>` *do określenia rodzaju operacji wykonywanych przez własność tablicową name - ogólny przykład metki*
![[Pasted image 20250525215908.png]]

---

# Refaktoryzacja kodu


- Refaktoryzacja to proces wprowadzania zmian w projekcie/programie w wyniku których nie zmienia się funkcjonalność systemu.
- W ramach refaktoryzacji podejmowane są następujące dwa głowne typy działań:
	- Modyfikowanie elementów systemu w celu dostosowania przyjętych standardów lub/i wzorców programowania
	- Poszukiwanie nowych standardów i wzorców które pojawiły się w systemie w trakcie jego rozwoju i ich definiowanie.
- *Przykład refaktoryzacji kodu*
![[Pasted image 20250525220227.png]]

- **Reguła DRY** - nie powtarzaj się
- Należy separować często powtarzający się kod i jedynie się do niego odwoływać

--- 


# Klasyfikacja przekształceń według sposobu weryfikacji 

- Przekształcenia proste, które można zweryfikować poprzez sprawdzenie określonych warunków początkowych i końcowych. Do kategorii tej należą m.in. przekształcenia, których poprawność można stwierdzić poprzez kompilację – niepowodzenie oznacza, że zostały przeprowadzone nieprawidłowo;

- Przekształcenia o znanym zakresie testowania, które wymagają przeprowadzenia określonych testów jednostkowych.

- Przekształcenia o nieznanym zakresie testowania, które również wymagają testowania, jednak z powodu ich ogólności (wpływu wielu trudno kontrolowalnych czynników), nie można wskazać uniwersalnego zbioru testów niezbędnych do zweryfikowania poprawności kodu.

