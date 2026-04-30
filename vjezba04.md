![Header VUV](/img/logo_header.png "Header VUV")

# 4. Laboratorijska vježba

## Sadržaj vježbe

* Zadaci za rad u laboratoriju

---

## Zadaci za rad u laboratoriju

Prije početka vježbe potrebno je napraviti import baze:

```text
employees
```

---

### Zadatak 1

Kreirati skriptu:

```text
classes.php
```

Unutar skripte potrebno je definirati klasu:

```php
Configuration
```

Klasa treba imati svojstva:

* `host`
* `dbname`
* `username`
* `password`

Potrebno je definirati i konstruktor.

Svojstvima dodijeliti zadane vrijednosti.

---

### Zadatak 2

Kreirati skriptu:

```text
connection.php
```

Unutar skripte potrebno je definirati konekciju na bazu podataka.

Za parametre connection stringa koristiti objekt klase kreirane u prethodnom zadatku.

---

### Zadatak 3

Unutar skripte:

```text
classes.php
```

kreirati klasu:

```php
Employee
```

Klasa treba sadržavati svojstva prema tablici iz baze podataka.

---

### Zadatak 4

Kreirati skriptu:

```text
json.php
```

Skripta treba, ovisno o parametru:

```php
$_GET['json_id']
```

vratiti odgovarajuću JSON datoteku.

Potrebno je uključiti odgovarajuća zaglavlja.

Napraviti `switch` naredbu koja će, ovisno o parametru `$_GET['json_id']`, vratiti JSON zaposlenika.

Za vraćanje svih zaposlenika `json_id` ima vrijednost:

```text
get_all_employees
```

Unutar `case` grane `get_all_employees` potrebno je napraviti SQL upit koji će pročitati sve zaposlenike iz tablice:

```text
employees
```

Koristiti klasu:

```php
Employee
```

Putanja za dohvat svih zaposlenika:

```text
localhost/wpsp_lv4/json.php?json_id=get_all_employees
```

---

### Zadatak 5

Kreirati skriptu:

```text
actions.php
```

Skripta treba, ovisno o parametru:

```php
$_POST['action_id']
```

izvršavati određeni SQL upit.

Za dodavanje novog zaposlenika `$_POST` polje mora sadržavati sva svojstva iz klase:

```php
Employee
```

Za dodavanje zaposlenika `action_id` treba imati vrijednost:

```text
dodaj_employee
```

Potrebno je kreirati i izvršiti pripremljeni upit za dodavanje novog zaposlenika u tablicu.

Putanja za spremanje novog zaposlenika:

```text
localhost/wpsp_lv4/actions.php
```

---

### Zadatak 6

Proširiti skriptu iz 4. zadatka dodavanjem još jedne `case` grane, gdje je:

```text
json_id=get_employee_by_id
```

Dodatni parametar koji se šalje uz `json_id` je:

```text
employee_id
```

Ovisno o poslanom `employee_id` parametru, potrebno je kreirati JSON datoteku zaposlenika.

Putanja za prikaz zaposlenika prema ID-u:

```text
localhost/wpsp_lv4/json.php?json_id=get_employee_by_id&employee_id=10300
```

---

### Zadatak 7

Proširiti skriptu:

```text
actions.php
```

dodavanjem novog `case` dijela koji će izvršavati upit za ažuriranje zaposlenika.

Za ažuriranje zaposlenika `$_POST` polje mora sadržavati sva svojstva iz klase:

```php
Employee
```

Potrebno je kreirati i izvršiti pripremljeni upit za ažuriranje zaposlenika.

---

### Zadatak 8

Proširiti skriptu:

```text
actions.php
```

dodavanjem novog `case` dijela koji će izvršavati upit za brisanje zaposlenika.

Za brisanje zaposlenika `$_POST` polje mora sadržavati ID zaposlenika.

Potrebno je kreirati i izvršiti pripremljeni upit za brisanje zaposlenika.

---

### Zadatak 9

Kreirati skriptu:

```text
index.php
```

Za dizajn koristiti:

```text
Bootstrap 4.6
```

U toj skripti potrebno je prikazati tablicu zaposlenika.

Predložak HTML strukture:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/fontawesome@4.7.0/css/font-awesome.min.css">
  <link rel="stylesheet"
        href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css"
        integrity="sha384-xOolHFLEh07PJGoPkLv1IbcEPTNtaed2xpHsD9ESMhqIYd0nLMwNLD69Npy4HI+N"
        crossorigin="anonymous">
  <title>Zaposlenici</title>
</head>
<body>
  <script src="https://cdn.jsdelivr.net/npm/jquery@3.7.1/dist/jquery.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/js/bootstrap.bundle.min.js"
          integrity="sha384-Fy6S3B9q64WdZWQUiU+q4/2Lc9npb8tCaSX9FK7E8HnRr0Jz8D6OP9dO5Vg3Q9ct"
          crossorigin="anonymous"></script>
</body>
</html>
```

---

### Zadatak 10

Kreirati datoteku:

```text
js/zaposlenici.js
```

Tu datoteku uključiti unutar skripte:

```text
index.php
```

Unutar JavaScript datoteke potrebno je kreirati funkciju:

```javascript
LoadEmployees()
```

Funkcija se poziva unutar:

```javascript
$(document).ready()
```

Za testiranje funkcije ispisati tekst:

```text
Hello World
```

u konzolu.

---

### Zadatak 11

Unutar skripte:

```text
index.php
```

kreirati Bootstrap HTML tablicu sa zaglavljem:

```html
<thead>
```

Zaglavlje treba sadržavati nazive kolona iz baze podataka te prazno tijelo tablice:

```html
<tbody>
```

Zaglavlje treba sadržavati i dvije dodatne kolone:

* prva za uređivanje podataka
* druga za brisanje podataka

Za ikonice koristiti:

```text
font-awesome
```

---

### Zadatak 12

Unutar funkcije:

```javascript
LoadEmployees()
```

iskoristiti AJAX `GET` metodu za poziv skripte:

```text
json.php
```

koja vraća sve zaposlenike u JSON formatu.

Koristeći `for` ili `foreach` petlju, kreirati redove za svakog zaposlenika i jQuery metodom dodati ih u tablicu iz prethodnog zadatka.

Predložak AJAX poziva:

```javascript
$.ajax({
    url: '',
    type: 'GET',
    success: function (oData) {
    }
});
```

---

### Zadatak 13

Kreirati skriptu:

```text
modals.php
```

Skripta treba, ovisno o GET parametru:

```php
modal_id
```

na ekran ispisivati HTML kod tijela modala.

`$_GET['modal_id']` može imati sljedeće vrijednosti:

* `new_employee`
* `edit_employee`
* `delete_employee`

Primjer HTML strukture modala:

```html
<div class="modal-header">
  <h5 class="modal-title" id="exampleModalLabel">Modal naslov</h5>
  <button type="button" class="close" data-dismiss="modal" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
</div>
<div class="modal-body">
  <div class="form-group">
    <label for="DeptNo">Dept no</label>
    <input type="text" class="form-control" id="DeptNo">
  </div>
  <div class="form-group">
    <label for="DeptName">Dept name</label>
    <input type="text" class="form-control" id="DeptName">
  </div>
</div>
<div class="modal-footer">
  <button type="button" class="btn btn-secondary" data-dismiss="modal">Odustani</button>
  <button type="button" class="btn btn-primary">Spremi</button>
</div>
```

---

### Zadatak 14

Kreirati skriptu:

```text
globals.js
```

Unutar skripte potrebno je definirati funkciju:

```javascript
GetModal(sHref)
```

`GetModal()` je custom funkcija koja korištenjem HTTP `GET` metode poziva link `sHref` na PHP skriptu koja sadrži tijelo modala.

Predložak:

```javascript
jQuery.extend(
{
    GetHTML: function (url) {
        var sHTML = "";
        $.ajax({
            url: url,
            type: 'post',
            dataType: 'html',
            async: false,
            success: function (oData) {
                sHTML = oData;
            }
        });
        return sHTML;
    }
});

function GetModal(sHref) {
    var sModalId = "modals";
    $('#' + sModalId).removeData('bs.modal');
    var sData = $.GetHTML(sHref);
    $('#' + sModalId + ' .modal-content').html(sData);
    $('#' + sModalId).modal({
        show: true,
        backdrop: 'static',
        keyboard: false
    });
}
```

Tijelo modala treba se prikazati u `div` elementu koji je potrebno napisati u skripti:

```text
index.php
```

```html
<div class="modal fade" id="modals" tabindex="-1" role="dialog" aria-labelledby="" aria-hidden="true">
  <div class="modal-dialog modal-lg">
    <div class="modal-content">
    </div>
  </div>
</div>
```

---

### Zadatak 15

Iznad tablice dodati gumbić koji otvara modal za dodavanje novog zaposlenika.

Pritiskom na ikonice za ažuriranje i brisanje zaposlenika potrebno je pozvati modal za:

* ažuriranje zaposlenika
* brisanje zaposlenika

---

### Zadatak 16

Unutar skripte:

```text
zaposlenici.js
```

definirati funkcije:

* `UpdateEmployee(nEmployeeID)`
* `AddNewEmployee()`
* `DeleteEmployee(nEmployeeID)`

Funkcije trebaju sadržavati AJAX pozive sa parametrima forme.

AJAX pozivom se poziva skripta:

```text
actions.php
```

koja ovisno o akciji izvršava upit nad bazom podataka.

Predložak AJAX poziva:

```javascript
$.ajax({
    url: 'action.php',
    type: 'POST',
    dataType: "html",
    data: {
        action_id: '',
        key1: value1,
        key2: value2
    },
    success: function(oData) {
    },
    error: function (XMLHttpRequest, textStatus, exception) {
        console.log("Ajax failure\n");
    },
    async: true
});
```
---
**Primjer dohvaćanja svih odjela:**

![Zadatak 16](/img/lv4_zadatak16a.jpg "Dohvaćanje odjela")

---

**Primjer dodavanja novog odjela:**

![Zadatak 16](/img/lv4_zadatak16b.jpg "Dohvaćanje odjela")

---