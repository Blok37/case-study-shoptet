# Extension for Shoptet

## Business overview

Párování plateb pro e-shopy na platformě Shoptet (https://www.shoptet.cz)

**Doplněk vám ušetří spoustu času. Čas jsou peníze a malá investice do doplňku se vám rychle vrátí v energii, kterou budete moci věnovat důležitějším věcem, než je dohledávání, zda byla objednávka už uhrazena nebo ne.**

* Doplněk označí objednávky jako zaplacené
* Nastavit různé stavy pro jednotlivé druhy plateb (dobírka, převodem, kartou atd.), na které se má objednávka při přijetí přepnout. odkaz na obraaozcku níže
* V přehledu objednávek vizuálně označí uhrazené / neuhrazené objednávky
* K Párování dochází na zaákladě variabilního symbolu platby

Podporované banky jsou

* Fio <https://www.fio.cz>
* Creditas
* Komerční banka
* další

![Activity diagram](/img/activity.png)

### Akceptační kritéria

## Requirements

### Parametry pro nastavení doplnku

* frekvence pro zjištování nových plateb z banky
* nastavení, co se mám stát s objednávkou při příchozí platbě
 * pokud je zaplaceno -> vybrat stav, na který se to má přepnout  
 * přeplaceno -> vybrat stav, na který se to má přepnout  
 * nedoplaceno -> vybrat stav, na který se to má přepnout  

* nastavení pro banky
 * fio - token + návod jak ho najít  
 * creditas - token + jak ho najít  
 * kb - tlačítko na připojení

 TODO jak bude vypadat nastavení
 TODO jak bude vypadat přehled s platbou  
 TODO testovscí eshop a testovaci token

### Log doplnku

* budou zobrazeny informace, kdy doplněk provolával API
* Zobrazení v přehledu objednávek, aby uživatel byl schopný identifikovat zaplacené objednávky

## To-Do

* vyřešit, pokud to jde na dobírku nebo kartou, řešit pouze u plateb na účet
* Vytvořit nápovědu  

## Documentation

* Dokumentace shoptet: https://developers.shoptet.com
* Dokumentace Fio: https://www.fio.cz/docs/cz/API_Bankovnictvi.pdf
