![Header VUV](/img/logo_header.png "Header VUV")

# 2. Laboratorijska vježba

## Sadržaj vježbe

* Zadaci za rad u laboratoriju

---

## Zadaci za rad u laboratoriju

### Zadatak 1

Kreirati skriptu:

```text
index.php
```

Skripta treba sadržavati **formu za prijavu korisnika**.

Pritiskom na gumb:

```text
Submit
```

skripta treba pozvati samu sebe koristeći:

```text
POST
```

metodu.

Za stiliziranje koristiti:

```text
Bootstrap
```

![Zadatak 1](/img/lv2_zadatak1.jpg "Forma za prijavu")

---

### Zadatak 2

Kreirati skriptu:

```text
functions.php
```

Unutar skripte potrebno je definirati funkciju:

```php
LoadUsers()
```

Funkcija treba vraćati **dvodimenzionalnu asocijativnu listu korisnika** učitanu iz datoteke:

```text
users.json
```

U datoteci `users.json` potrebno je kreirati najmanje **tri korisnika**.

Svaki korisnik treba sadržavati sljedeća svojstva:

* `id`
* `username`
* `email`
* `password`

Pomoć za učitavanje JSON datoteke:

```php
$string = file_get_contents("users.json");
$oUsers = json_decode($string, true);
```

---

### Zadatak 3

Unutar skripte:

```text
functions.php
```

kreirati funkciju:

```php
CheckUser($sUsername, $sPassword)
```

Funkcija kao parametre prima:

* korisničko ime
* lozinku

Funkcija treba pozvati:

```php
LoadUsers()
```

i provjeriti:

* postoji li korisnik
* je li uneseno korisničko ime ispravno
* je li unesena lozinka ispravna

Funkcija treba vratiti jednodimenzionalno polje:

```php
$oUser
```

koje se sastoji od asocijativnih polja:

* `user_id`
* `username`
* `email`

Ako korisnik ne postoji, sva polja trebaju imati vrijednost:

```text
NULL
```

---

### Zadatak 4

Unutar skripte:

```text
functions.php
```

kreirati funkciju:

```php
SetSessions($oUser)
```

Funkcija kao parametar prima jednodimenzionalno polje:

```php
$oUser
```

koje se sastoji od asocijativnih polja:

* `user_id`
* `username`
* `email`

Funkcija treba pročitati vrijednosti iz polja i spremiti ih u globalno polje:

```php
$_SESSION
```

---

### Zadatak 5

Unutar skripte:

```text
index.php
```

potrebno je provjeriti postoje li:

```php
$_POST
```

varijable.

Ako varijable postoje, potrebno je pozvati funkciju:

```php
CheckUser()
```

Ako funkcija `CheckUser()` vrati korisnika sa vrijednostima koje nisu `NULL`, potrebno je:

* pozvati funkciju za spremanje podataka u sesiju
* preusmjeriti skriptu na:

```text
users.php
```

---

### Zadatak 6

Unutar skripte:

```text
users.php
```

potrebno je ispisati sve korisnike u obliku:

```text
HTML tablice
```

Potrebno je dodatno obojati redak korisnika koji je trenutno prijavljen.

![Zadatak 6](/img/lv2_zadatak6.jpg "Tablica korisnika")

---