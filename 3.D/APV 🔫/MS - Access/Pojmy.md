# MS Access pojmy
## Databáze
- souhrn uložených dat majících vztah k určitému celku
	- př. zákazníci firmy, knihy v databázi
- systém s uspořádanými daty, organizované ukládání, výběr předepsaných pravidel
- použití při evidenci většího množství dat
## Redundance
- stejné data se vícekrát opakují
- **databáze má být neredundantní**
## Entropie
- rozházenost / chaos
## Relační databáze
- umožňuje propojovat hodnoty mezi sebou pomocí relací (vazeb), které jsou společné
## Další pojmy
- **Entita** – objekt dané databáze (př. student)
- **Atribut** – vlastnost entity (př. rodné číslo (vlastnost studenta))
- **Relace** – vztah mezi objekty (entitami) 
- **klíč** (atribut) – identifikuje <span style="color: red;">JEDNOZNAČNĚ</span> objekt - entitu.
	- Student má primární klíč atribut Rodné číslo.
- **Primární klíč** – pole nebo kombinace polí jednoznačně identifikuje záznam v databázi 
- **Cizí klíč** – převzaté, spojení sloupců se sloupci jiné tabulky
- **Alternativní klíč** – kandidátní klíč, který není primární
- **Kandidátní klíč** – sloupec nebo sloupce, ve kterých mají také všechny řádky tabulky své hodnoty unikátní
## Kardinalita
- vlastnost vztahu (relace) – kolik entit může být v jednom vztahu s několika jinými entitami
	- Student – Škola
		- N:1
	- Ředitel – Škola
		- 1:1
	- Student – Hospoda
		- N:N 
## Struktura databáze
- tabulka s daty
- data mohou být ve více tabulkách
- Tabulky
- Data 
- Řádek tabulky
	- záznam
	- info o entitě
- Sloupce tabulky
	- atributy
	- pole jedné určité kategorie záznamu
## obsluha databáze