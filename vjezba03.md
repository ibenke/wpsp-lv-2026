![Header VUV](/img/logo_header.png "Header VUV")

# 3. Laboratorijska vježba

## Sadržaj vježbe

* Zadaci za rad u laboratoriju

---

## Zadaci za rad u laboratoriju

### Zadatak 1

Kreirati skriptu:

```text
classes.php
```

Unutar skripte potrebno je deklarirati klasu:

```php
Zaposlenik
```

Klasa treba imati privatne podatkovne članove:

* `ime`
* `prezime`
* `oib`

Sva svojstva inicijalno imaju vrijednost:

```text
N/A
```

Svojstva klase potrebno je inicijalizirati u konstruktoru.

Parametri konstruktora imaju zadanu vrijednost:

```php
null
```

Konstruktor treba dodijeliti vrijednost svojstvu objekta samo ako je parametar proslijeđen, odnosno ako nije `null`.

---

### Zadatak 2

Kreirati skriptu:

```text
index.php
```

Unutar skripte potrebno je uključiti datoteku:

```text
classes.php
```

Instancirati **3 objekta** klase `Zaposlenik` i ispisati ih na ekran.

Instancirati još jedan objekt klase `Zaposlenik` kojemu nećete proslijediti parametre i također ga ispisati na ekran.

---

### Zadatak 3

Ispisati pozdravnu poruku za prvi objekt direktnim pristupom svojstvu, na sljedeći način:

```text
Hello Pero Perić (47384986407)
```

Zatim prepraviti program tako da radi pomoću **getter metoda** za svako svojstvo.

---

### Zadatak 4

Unutar klase `Zaposlenik` dodati javnu metodu:

```php
Hello()
```

Metoda treba ispisati na ekran poruku iz prethodnog zadatka.

Nad prvim objektom potrebno je pozvati tu metodu.

---

### Zadatak 5

Unutar klase dodati privatnu metodu:

```php
CheckOib()
```

Metoda treba provjeriti je li poslani OIB u ispravnom obliku.

Za provjeru koristiti gotovo rješenje dostupno na internetu, primjerice:

```text
https://markoivancic.from.hr/provjera-ispravnosti-oiba-u-php-u
```

Već definiranu klasu dodati u:

```text
classes.php
```

Objekt te klase:

```php
$oOibValidator
```

potrebno je instancirati unutar metode `CheckOib()`.

Ako proslijeđeni OIB nije u ispravnom obliku, potrebno je ispisati grešku na ekran.

Grešku u PHP-u moguće je ispisati na sljedeći način:

```php
throw new Exception('Oib nije ispravan');
```

---

### Zadatak 6

Unutar skripte:

```text
classes.php
```

kreirati dvije nove klase:

* `Nastavnik`
* `StrucnaSluzba`

Obje klase trebaju nasljeđivati klasu:

```php
Zaposlenik
```

Obje klase trebaju imati javnu metodu:

```php
Radi()
```

Metoda treba na ekran ispisati jednu od sljedećih poruka:

```text
Ime Prezime idi izvoditi nastavu
```

ili:

```text
Ime Prezime idi obavljati administrativne poslove
```

---

### Zadatak 7

Budući da obje izvedene klase imaju metodu:

```php
Radi()
```

i da sve izvedene klase iz klase `Zaposlenik` moraju imati tu metodu definiranu, potrebno je klasu `Zaposlenik` definirati kao:

```text
abstraktnu klasu
```

Unutar nje dodati apstraktnu metodu:

```php
Radi();
```

Nakon toga pokušati zakomentirati metodu `Radi()` u jednoj od child klasa i pokrenuti program.

---

### Zadatak 8

Definirati sučelje:

```php
INastavnik
```

koje sadrži metodu:

```php
DrziNastavu()
```

Kreirati praznu klasu:

```php
Predavac
```

koja implementira sučelje `INastavnik`.

Kreirati novi objekt klase `Predavac`.

Provjeriti pojavljuje li se greška.

Ispraviti grešku tako da se definira funkcija:

```php
DrziNastavu()
```

koja na ekran ispisuje poruku:

```text
Idi izvoditi predavanja
```

---

### Zadatak 9

Proširiti klasu:

```php
Predavac
```

na način da klasa nasljeđuje i klasu:

```php
Nastavnik
```

i sučelje:

```php
INastavnik
```

Proširiti metodu:

```php
DrziNastavu()
```

tako da se na ekran ispisuje poruka:

```text
Ime Prezime idi izvoditi nastavu
```

---

### Zadatak 10

Definirati sučelje:

```php
IAsistent
```

koje sadrži metode:

* `PripremiNastavu()`
* `CuvajIspit()`

Definirati klasu:

```php
Asistent
```

koja nasljeđuje klasu:

```php
Nastavnik
```

te implementira sučelja:

* `INastavnik`
* `IAsistent`

Definirati pripadajuće metode koje ispisuju poruke:

```text
DrziNastavu() - Ime Prezime idi izvoditi vježbe
PripremiNastavu() - Ime Prezime pripremi predavanja
CuvajIspit() - Ime Prezime idi čuvaj ispit
```

Kreirati objekt nad kojim ćete pozvati navedene metode.

---