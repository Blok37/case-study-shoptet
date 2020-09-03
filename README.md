# Extension for Shoptet

## Business overview

Párování plateb pro e-shopy na platformě Shoptet (<https://www.shoptet.cz>)

## Doplněk udělá párování plateb z banky za Vás. Nemusíte procházet transakční historii ve své bance, dopněk to udělá sám. Můžete se věnovat svému podnikání

* Doplněk označí zaplacené objednávky jako zaplacené
* Nastavit různé stavy pro jednotlivé druhy plateb (dobírka, převodem, kartou atd.), na které se má objednávka při přijetí přepnout.
* K Párování dochází na základě variabilního symbolu platby a částky platby

Podporované banky jsou

* Fio <https://www.fio.cz>
* Creditas
* Komerční banka
* další

## Requirements

### Zjednodušený Proces 

![Activity diagram](/img/activity.png)

1. Klient si objedná zboží.
2. Zaplatí objednávku.
3. Doplněk ověří platby v bance
 a) Pokud se shoduje objednávka (id objednavky, částka) a platba variabilní symbol a částka
 b) Přeplaceno -> vybrat stav, na který se to má přepnout
 c) Nedoplaceno -> vybrat stav, na který se to má přepnout  
4. Po příchozí platbě nastavit objednávku pro **způsob platby** nastav **stav objednávky**
5. Zboží je možné expedovat.

### Akceptační kritéria

### Parametry pro nastavení doplnku

#### nastavení pro banky

* fio - token + návod jak ho najít  
* creditas - token + jak ho najít  
* kb - tlačítko na připojení

#### frekvence pro zjištování nových plateb z banky

#### nastavení, co se mám stát s objednávkou při příchozí platbě

## IT Solution

* Shoptet API  Documentation (<https://shoptet.docs.apiary.io/>)

* načíst stavy objednávek, které e-shop používá, use API https://api.myshoptet.com/api/orders/statuses
* načíst číselník způsobů plateb), use API https://api.myshoptet.com/api/payment-methods
* pro připojení do banku je potřeba
  + fio: token
  + creditas: token
  + kb: OAuth2
* pravidelně po <parametr> se ověřují platby v bance (minimálně po 1 minutě) 
* pokud je zaplaceno -> vybrat stav, na který se to má přepnout  
* events při platbě

### Log doplnku

* budou zobrazeny informace, kdy doplněk provolával API
* Zobrazení v přehledu objednávek, aby uživatel byl schopný identifikovat zaplacené objednávky

## Documentation

* Dokumentace shoptet: <https://developers.shoptet.com>
* Dokumentace Fio: <https://www.fio.cz/docs/cz/API_Bankovnictvi.pdf>
