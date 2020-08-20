# Extension for Shoptet

## Business overview

Párování plateb pro e-shopy na platformě Shoptet (https://www.shoptet.cz)
Podporované banky jsou
- Fio https://www.fio.cz
- Creditas
- Komerční banka


## Requirements


### Parametry pro nastavení doplnku  

* frekvence pro zjištování nových plateb 
* nastavení, co se mám stát s objednávkou při příchozí platbě  
 *  pokud je zaplaceno -> vybrat stav, na který se to má přepnout  
 *  přeplaceno -> vybrat stav, na který se to má přepnout  
 * nedoplaceno -> vybrat stav, na který se to má přepnout  
* nastavení pro banky   
 * fio - token + návod jak ho najít  
 * creditas - token + jak ho najít  
 * kb - tlačítko na připojení  

### Log doplnku   
* budou zobrazeny informace, kdy doplněk provolával API  
* Zobrazení v přehledu objednávek, aby uživatel byl schopný identifikovat zaplacené objednávky   

# To-Do
* vyřešit, pokud to jde na dobírku nebo kartou, řešit pouze u plateb na účet  
* Vytvořit nápovědu  


# Documentation
* Dokumentace shoptet: https://developers.shoptet.com  
* Dokumentace Fio: https://www.fio.cz/docs/cz/API_Bankovnictvi.pdf  
