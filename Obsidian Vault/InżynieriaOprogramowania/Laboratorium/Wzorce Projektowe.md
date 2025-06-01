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

# Strukturalne
---

### Fasada
- Jedna główna klasa która ukrywa skomplikowaną strukturę klas której używa
![[Pasted image 20250522224944.png]]
### Kompozyt
- Chodzi o to że traktujemy zbiór elementów tak samo jak jeden element.
![[Pasted image 20250531153756.png]]

### Singleton
- Antywzorzec 
- Chodzi o to że możemy stworzyć tylko jedną instancje danej klasy 
- Ma prywatny konstruktor i publiczną metode getInstance
- ma statyczne pole instance

### Dekorator

![[Pasted image 20250531152016.png]]


### Proxy

![[Pasted image 20250601180342.png]]

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