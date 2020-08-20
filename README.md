# Extension for Shoptet

## Business overview

Párování plateb pro e-shopy na platformě Shoptet (https://www.shoptet.cz)

**Doplněk vám ušetří spoustu času. Čas jsou peníze a malá investice do doplňku se vám rychle vrátí v energii, kterou budete moci věnovat důležitějším věcem, než je dohledávání, zda byla objednávka už uhrazena nebo ne.**
* Automaticky označovat také objednávky jako zaplacené 
* Nastavit různé stavy pro jednotlivé druhy plateb (dobírka, převodem, kartou atd.), na které se má objednávka při přijetí přepnout 
* Po spárování platby s objednávkou se u objednávky objeví zelený puntík značící, že je všechno v pořádku, zákazník zaplatil a vy můžete odeslat zboží. 

Podporované banky jsou
- Fio https://www.fio.cz
- Creditas
- Komerční banka

## Requirements
### Parametry pro nastavení doplnku  

* frekvence pro zjištování nových plateb 
* nastavení, co se mám stát s objednávkou při příchozí platbě 

TODO stavový diagram
 *  pokud je zaplaceno -> vybrat stav, na který se to má přepnout  
 *  přeplaceno -> vybrat stav, na který se to má přepnout  
 * nedoplaceno -> vybrat stav, na který se to má přepnout  
 * nastavení pro banky   
  * fio - token + návod jak ho najít  
  * creditas - token + jak ho najít  
  * kb - tlačítko na připojení

 TODO jak bude vypadat nastavení
 TODO jak bude vypadat přehled s platbou  

### Log doplnku   
* budou zobrazeny informace, kdy doplněk provolával API  
* Zobrazení v přehledu objednávek, aby uživatel byl schopný identifikovat zaplacené objednávky   

## To-Do
* vyřešit, pokud to jde na dobírku nebo kartou, řešit pouze u plateb na účet  
* Vytvořit nápovědu  


## Documentation
* Dokumentace shoptet: https://developers.shoptet.com  
* Dokumentace Fio: https://www.fio.cz/docs/cz/API_Bankovnictvi.pdf  