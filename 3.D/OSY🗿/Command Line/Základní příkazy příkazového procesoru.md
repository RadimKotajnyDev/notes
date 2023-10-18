# Základní příkazy příkazového procesoru
- Adresář a složka je to samé.
	- GUI je složka; V příkazovém řádku adresář.
## znaky
- – Aktuální adresář
.. – nadřízený adresář
\\ – kořenový adresář
\* – skupina znaků
? – jeden znak

## Značení diskových jednotek
- Písmeno, dvojtečka, backslash,
	`C:\`
- A, B je vyhrazené pro floppy disky

## Základní příkazy pro práci s adresáři a soubory
- `help` vypíše příkazy (nápovědu)
- `dir <cesta>` vypíše obsah adresáře
- `cd <cesta>` změna aktuálního adresáře – "change directory"
- `md <název>` nebo `mkdir <název>` vytvoří adresář – "make directory"
- `rd <název` nebo `rmdir <název>` smazání složky – "remove directory"
	- atribut `/S` smaže celý obsah adresáře
- `del` - vymaže soubor nebo soubory
- `type` - vypíše obsah txt souboru
- `ren` - přejmenovat soubor
- `copy` - kopíruje 1 nebo více souborů do nového umístění
	když je 1 zdrojoví soubor tak cílové umístění může být složka nebo soubor
	více zdrojových souborů lze zadat pomocí zástupných znaků
- `xcopy` - kopíruje celý adresářový strom, používá se podobně jako copy
- `tree` - graficky vypíše systém podsložek
- `move` - přemístí soubor, proběhne rychle protože se změní jen záznamy v adresářích
- `attrib` - pracuje s atributy souboru
- `comp`, `fc` - slouží k porovnávání obsahu souborů
- `find`, `findstr` - vyhledávání řetězce v textovém souboru
- `more` 
- `subs` - namapuje složku jako diskovou jednotku
- `ECHO` - vypíše nastavení ozvěny
- `ECHO OFF` - nevypisuje výzvu
- `ECHO <string>` vypíše řetězec na obrazovku
- 
