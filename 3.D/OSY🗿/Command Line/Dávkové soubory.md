#bat #dávkové-soubory

# Dávkové soubory

-   přípona .BAT (batch)
-   textový soubor
-   obsahuje příkazy příkazového procesoru
-   jména externích programů
-   je spustitelný
-   interpretován řádek po řádku — příkazovým procesorem
-   Příkazový procesor obsahuje i příkazy pro řízení chodu dávkových souboru
-   Podmíněný příkaz nepodmíněný skok, cyklus

### Užití

-   automatizace opakovaných činností správce
-   usnadnění činnosti uživatelům
-   řešení naplánovaných úloh
-   hromadné operace

### Historie

-   UNIX, Linux, Shell: bsh, bash, ksl, csh
-   MS - DOS : 32bit [COMMAND.COM](http://COMMAND.COM), CMD.EXE 64bit CMD.EXE PowerShell
-   omezené možnosti

> Výkonný a bohatý skriptovací jazyk

### ECHO
- příkaz `echo` vypíše řetězec
	- proměnná `%promenna%`
- vstup dat:
	1. jako parametry při spuštění `SET /P`
	2. `SET /P N=Zadej cislo:`
	3. přiřazení `SET N=50`
	4. podmínka `IF EXIST/ERRORLEVEL cislo/string1==string2 příkaz`
		- ERRORLEVEL zkoumá return hodnotu
		- větev else
	5. `GOTO`
	6. `SHIFT`
	7. cyklus `FOR`
		- `FOR %variable IN (set) DO command`
			- název proměnné je jen **1 písmeno**
			- seznam/set mohou být:
				- hodnoty vypsané přímo do seznamu
				- seznam souborů vytvořený pomocí zástupci znaků
			- potom cyklus `FOR` zpracuje všechny soubory v dané cestě
			- `FOR %F in (10 20 30) DO @ECHO %F`
			- `FOR %F in (*.TXT) DO @ECHO %F`
			- atributy
				- `FOR /D` nezpracuje soubory, ale složky.
				- `FOR /R` uvedena jednotka a cesta
				- `FOR /L` jako ve vyšším jazyku (start, step, end)