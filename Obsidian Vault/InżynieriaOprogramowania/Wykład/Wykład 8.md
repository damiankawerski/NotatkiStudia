# 📚 Notatki UML, Metodyki i Artefakty

## 📊 Diagramy UML

### Diagramy kooperacji vs diagramy sekwencji

- **Diagramy kooperacji** są **równoważne** z **diagramami sekwencji** — oba służą do modelowania interakcji między obiektami.
    
- Różnica leży głównie w **sposobie prezentacji**:
    
    - Diagramy sekwencji kładą nacisk na **czas** (układ pionowy).
        
    - Diagramy kooperacji skupiają się na **strukturze** współpracy między obiektami.
        

### Diagramy komponentów

- **Komponent** to implementacja jednej lub większej ilości klas.
    
- Komponenty komunikują się **wyłącznie przez interfejsy**.
    
- Zasada:
    
    - **Komponent** posiada wiedzę o **rozwiązaniu problemu**.
        
    - **Interfejs** posiada wiedzę o tym, że **problem istnieje**.
        

---

## 🧠 Byty logiczne i fizyczne

- **Byty logiczne** istnieją **w głowie** (w sferze koncepcji, projektów, modeli).
    
- **Byty fizyczne** istnieją **w komputerze** (kod źródłowy, bazy danych, aplikacje).
    

### Manifestacja

- To **wyrażenie bytu logicznego** w **bycie fizycznym**.
    
- Przykład: Klasa w UML (byt logiczny) → Kod w C++/Java (byt fizyczny).
    

---

## 🗂️ Artefakty

- **Artefakty** to rzeczy **pochodzenia nienaturalnego** — wszystko, co zostało stworzone w procesie wytwarzania oprogramowania.
    
- Przykłady:
    
    - Dokumenty (np. specyfikacja wymagań),
        
    - Diagramy UML,
        
    - Kod źródłowy,
        
    - Pliki binarne.
        

---

## 🔄 Metodyki wytwarzania oprogramowania

### Metodyki standardowe (klasyczne)

- Oparte na podejściu **kaskadowym** (Waterfall).
    
- Fazy są przechodzone **jeden raz** w ustalonej kolejności.
    
- Przykłady:
    
    - Waterfall,
        
    - V-Model.
        

### Metodyki zapętlone (iteracyjne)

- Oparte na **wielokrotnym powtarzaniu** faz (iteracjach).
    
- Często używane w metodykach **zwinnych**.
    
- Przykłady:
    
    - RUP (Rational Unified Process),
        
    - Spiral Model.
        

### Metodyki zwinne (agile)

- Oparte na **iteracjach** i **przyrostowym rozwoju** produktu.
    
- Silny nacisk na:
    
    - **Bliską współpracę** z klientem,
        
    - **Elastyczność** wobec zmian,
        
    - **Częste dostarczanie** działającego oprogramowania.
        
- Przykłady:
    
    - Scrum,
        
    - Kanban,
        
    - XP (Extreme Programming).
        

---

## 📈 Diagramy fazowe

- **Diagramy fazowe** pokazują, jak **byty** przechodzą przez **różne fazy** podczas swojego życia.
    
- Używane do modelowania:
    
    - Stanów obiektów,
        
    - Cyklu życia procesów,
        
    - Przepływu dokumentów.