![Header VUV](/img/logo_header.png "Header VUV")

# 1. Laboratorijska vježba

## Sadržaj vježbe

* Zadaci za rad u laboratoriju

---

## Zadaci za rad u laboratoriju

### Zadatak 1

Napisati PHP skriptu kojom ćete provjeriti je li varijabla:

```php
$x
```

cjelobrojna varijabla.

Ako je, potrebno ju je ispisati na ekran.

Ako nije, potrebno ju je pretvoriti u cjelobrojni tip podataka i zatim ispisati na ekran.

---

### Zadatak 2

Napisati program koji će provjeriti je li cjelobrojna varijabla:

```php
$x
```

djeljiva s:

```text
5
```

Ako nije, potrebno je ispisati prvi broj manji od unesene vrijednosti koji je djeljiv s 5.

---

### Zadatak 3

Generirati slučajan broj između:

```text
1 i 20
```

Koristeći `while` petlju, program treba ispisivati brojeve u novom redu sve dok slučajno generirani broj ne bude:

```text
10
```

---

### Zadatak 4

Napisati funkciju koja kao parametar prima:

```php
$n
```

a na ekran ispisuje brojeve od `1` do `$n` u sljedećem obliku:

```text
# 1 2 3 4 ... n
# ...
# 1 2 3
# 1 2
# 1
```

---

### Zadatak 5

Napisati funkciju koja će provjeriti je li zadani string `palindrom`.

> [!WARNING]
>Nije dopušteno koristiti funkciju:
>
>```php
>strrev()
>```
>
---

### Zadatak 6

Napraviti listu u kojoj ćete navesti predmete koje slušate u ovom semestru.

Kroz listu proći koristeći:

```php
for
```

petlju i za svaki element liste ispisati koliko slova sadrži.

---

### Zadatak 7

Kreirati dvije liste:

```php
$x
$y
```

koje se sastoje od 5 cjelobrojnih vrijednosti.

Napisati program koji će preko funkcije ispisati logičku vrijednost:

```text
true
```

ili:

```text
false
```

ovisno o tome jesu li dvije učitane liste `cirkularno identične`.

Primjeri:

* liste `[1, 2, 3, 4, 5]` i `[3, 4, 5, 1, 2]` su cirkularno identične
* liste `[1, 2, 3, 4, 5]` i `[2, 4, 3, 5, 1]` nisu cirkularno identične

> [!NOTE]
>Primjer:
>
>```text
>https://stackoverflow.com/questions/26924836/how-to-check-whether-two-lists-are-circularly-identical-in-python
>```

---

### Zadatak 8

Napisati funkciju koja će ispisivati matricu ako joj kao argumente proslijedimo:

* broj redaka
* broj stupaca
* polje koje sadrži poziciju i vrijednost nenultog elementa matrice

Primjer:

```text
Input: 3,3,[[0,0,1], [1,1,2], [1,2,3], [2,2,5]]
```

Očekivani ispis:

```text
1 0 0
0 2 3
0 0 5
```
---