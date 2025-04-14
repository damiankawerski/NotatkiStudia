# Diagramy UML – Notatki

## Relacja `<<include>>`
- `<<include>>` jest **relacją prostą** w diagramach przypadków użycia (use case).
- Używana do **włączenia funkcjonalności jednego przypadku użycia do drugiego**.
- Reprezentuje **bezwarunkowe rozszerzenie** funkcji – zawsze jest wykonywana, gdy główny przypadek użycia jest wykonywany.
- Przykład: logowanie zawiera uwierzytelnienie hasła → logowanie `<<include>>` uwierzytelnianie.

---

## Stopnie szczegółowości diagramów
Diagramy powinny być tworzone ze **zdrowym rozsądkiem**, odpowiednio do potrzeb:
- **Stopień ogólny** – przedstawia **podstawowy zarys systemu**. Używany na wczesnym etapie projektowania lub do komunikacji z klientem.
- **Stopień szczegółowy** – zawiera **relacje szczegółowe i opcjonalne**. Używany do implementacji i dokumentacji wewnętrznej.

---

## Klasa w UML
Klasa to **szablon (przepis)** na obiekty, który zawiera:
- **Atrybuty** (ang. *attributes*) – odwzorowywane w kodzie jako **pola**.
- **Operacje** (ang. *operations*) – odwzorowywane w kodzie jako **metody**.

### Budowa klasy
Każda klasa w UML składa się z trzech części:
1. **Nagłówek** – nazwa klasy.
2. **Lista atrybutów** – zmienne przechowywane w obiekcie.
3. **Lista operacji** – funkcje możliwe do wykonania przez obiekt.

### Przykład klasy (UML)
## | Uzytkownik |

## | - imie: String | | - email: String | | - haslo: String |

## | + zaloguj(): void | | + wyloguj(): void |



---

## Dodatkowe wskazówki
- **Nie przesadzaj ze szczegółowością** – nie wszystko musi być pokazane na jednym diagramie.
- **Podziel diagramy tematycznie**, jeśli są zbyt rozbudowane.
- **Stosuj konwencje UML** – poprawna składnia i znaczniki (`+`, `-`, `#`) pomagają w zrozumieniu.

---

## Tagowanie
`#UML` `#Diagramy` `#OOP` `#InżynieriaOprogramowania`
