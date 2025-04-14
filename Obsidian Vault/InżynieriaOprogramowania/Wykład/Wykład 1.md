# UML – Narzędzie modelowania

UML (Unified Modeling Language) nie jest celem samym w sobie, lecz **narzędziem do rozwiązywania problemów**. Służy do:

- Modelowania problemu  
- Tworzenia rozwiązania  
- Wdrażania systemu  

---

## 🎯 Metamodel
**Metamodel** to model oprogramowania – abstrakcyjny opis struktury i zachowania systemu, który służy do tworzenia konkretnych modeli.

---

## 🧭 Perspektywy modelowania UML

### 1. Perspektywa przypadków użycia
- Najwyższy poziom abstrakcji.  
- Przedstawia działanie systemu z punktu widzenia:
  - użytkowników,  
  - testerów.

### 2. Perspektywa projektowa
- Architektura systemu.  
- Komponenty i ich interakcje.

### 3. Perspektywa procesowa
- Zachowanie systemu w czasie działania.  
- Przepływ sterowania, interakcje, współbieżność.

### 4. Perspektywa implementacyjna
- Jak poszczególne elementy są kodowane.  
- Powiązania z językiem programowania.

### 5. Perspektywa wdrożeniowa
- Rozmieszczenie komponentów systemu w środowisku produkcyjnym.  
- Węzły, serwery, zależności.

---

## 🧱 Diagramy UML

### Diagramy struktury statycznej
- Opisują **strukturę systemu**.  
- Przykłady: diagram klas, diagram komponentów.

### Diagramy dynamiki
- Pokazują **zachowanie systemu w czasie**.  
- Przykłady: diagram sekwencji, diagram aktywności.

> 📝 Różne elementy mogą mieć te same pola, ale **nigdy nie są tożsame** – znaczenie zależy od kontekstu modelowania.

---

## 🧩 Dodatkowe informacje

- **Projekt to suma detali** – dokładność modelu ma znaczenie.  
- Na diagramach:
  - **Po lewej stronie** – użytkownik zewnętrzny.  
  - **Po prawej stronie** – użytkownik wewnętrzny (np. `User` vs `Administrator`).

---

## 🔁 Dziedziczenie i relacje

### Dziedziczenie
- **Strzałka niewypełniona** → wskazuje na typ ogólny.
  - `P2 → P1` oznacza, że `P2` jest **specjalną formą** `P1`.

### Stereotypy
- Zapisuje się w nawiasach `<< >>` (tzw. francuskie nawiasy).  
- Pomagają w oznaczeniu ról i funkcji elementów.

---

## 🔗 Relacje przypadków użycia

- `P1 <<include>> P2`  
  → `P2` jest **niezbędną częścią** `P1`.  
  → `P1` **nie wykona się**, jeśli `P2` nie zostanie wykonane.

- `P1 <<extends>> P2`  
  → `P2` to **rozszerzenie** `P1`.  
  → `P1` działa niezależnie, a `P2` dodaje funkcjonalność opcjonalnie.

---

## 📚 Materiał źródłowy

- *UML User Guide* – AGH, wersja PDF.
