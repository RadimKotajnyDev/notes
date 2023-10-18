# Vlastnosti a rozdělení OS
## Asymetrický proces
- jedno jádro může být nadřazené
## Symetrický proces
- každý proces může být přiřazen k jádru. Jádra jsou symetrická.
## Podle počtu současně spuštěných procesů
### Víceprogramové
- CPU musí podporovat přemístění programů na jinou adresu (relokalizace)
## Jednoprogramové
- MS-DOS

## Univerzální OS
- Windows, MacOS, Linux
## Speciální OS
- Novell NetWare, Symbian
## Správce technických prostředků (CPU, RAM) počítače musí:
- mít přehled o prostředcích
- realizovat pravidla kterému procesu bude prostředek udělen
## Základní funkce OS:
- Správa paměti
- správa souborů
## další funkce
- správa zařízení / periferií
	- tiskárny, atd.
- softwarové rozhraní
- ![[Pasted image 20230411095343.png]]
- **Předán** – okamžik, kdy OS zaregistruje požadavek na vytvoření procesu.
	- Požadavek může pocházet od uživatele nebo od jiného procesu. 
	- Pro vytvoření procesu v OS jsou k dispozici jádra (2) - funkce EXEC, FORK.
- **Přijat** – OS začne procesu přidělovat paměť.
	- Když paměti není dostatek, ohlásí se chyba vytváření procesu. 
	- Kód programu je nahrán do operační paměti a přidělí se paměť pro statická data a zásobník.
	- Proces se zaeviduje do tabulky procesů a přidělí se mu číslo procesu (PID).
	- Je-li vše připraveno, proces se přidělí do stavu Připraven (přiděleno vše kromě CPU)
- **Připraven** (přiděleno vše kromě CPU)
- **Probíhající** – u jedno úlohových OS téměř ihned u více úlohových OS až na ně dojde řada.
	- V tomto stavu se instrukce vykonávají.
	- Z čekajícího se dostane z připraven
- **Čekající** – proces se zde může dostat, když čeká na dokončení jiného procesu nebo I/O operace.
	- je předán procesu, který s tím může pracovat IDK
- **Dokončen** – proces se zde dostane, tak že provede veškeré instrukce nebo ho uživatel řádně ukončí.
	- <u>Normální ukončení</u>
		- OS funkce
		- normálně ukončený proces musí OS vrátit všechny prostředky, které měl přiděleny. (program musí být správně napsán)
	- <u>Abnormální ukončení</u>
		- dochází k němu v případě chyby, kdy OS proces násilně ukončí
		- když uživatel ukončí proces přes správce úloh (program neodpovídá)
		- OS násilně odebere prostředky
		- mohou se poškodit data
		- **TODO: ve skriptu si přečíst důvody abnormálního ukončení**
			- Proces šahá na neexistující RAM
			- nedostatek RAM
			- freeze programu
- Princip multitaskingu spočívá v tom, že OS bez uživatele přehazuje procesy mezi stavy ***Připraven*** a ***Probíhající***
- PCB – *Process Control Block*
	- datová struktura RAM kde jsou uloženy informace o procesu
	- každý proces má svůj PCB
	- OS je běžící proces identifikován PID
## Způsoby rozdělení procesů
- většina OS má 2 různé služby pro vytvoření nového procesu.
	- FORK
		- ![[Pasted image 20230419081757.png]]
	- EXEC
		- nahrazuje se proces
		- ![[Pasted image 20230419081850.png]]
## Způsoby běhu procesu v různých systémech
### Sekvenční
- ![[Pasted image 20230419082818.png]]
- Přesně takto to funguje v OS jednoprogramovém.
- Také to takhle funguje v OS víceprogramovém, ale jednoúlohovém (MS-DOS) za předpokladu, že z procesu nespouštíme další program
### Paralelní
- ![[Pasted image 20230419083125.png]]
## Sekvenčně-paralelně
![[Pasted image 20230419083529.png]]
- takto běží při multitaskingu více procesů na jednom jádře
## Přepnutí procesu
![[Pasted image 20230425095944.png]]
- přepnutí procesu se zahájí přerušením od systémového časovače, což je __hardwarový obvod__
- přepnutí procesu je řešeno obsluhou přerušení
- při přepnutí se musí uložit kontext procesu, kterému se procesor právě odebírá a - , který bude nově běžící
- kontext procesu je tvořen především obsahem registrů CPU
- kontext procesu se ukládá do PC
## Nejobvyklejší algoritmus přepínání procesu je cyklický
 ![[Pasted image 20230425101013.png]]
 __ROUND ROBIN__
 - V OS může administrátor obměnit na kolik budou jednotlivé procesy využívat CPU
 - Časové kvantum přidělované procesům musí být optimální (ani moc malé, ani moc velké)
## Druhy multitaskingu
### pseudomultitasking
- není to skutečný multitasking, protože procesy přepíná uživatel pomocí hotkey  
	- ten potom je běžící
	- bylo to zavedeno v MS-DOSu
	- DOSSWAP.EXE
### Kooperativní multitasking
- je celkem <span style="color: red; text-decoration: underline">nespolehlivý</span>
- programy musí na přepínání spolupracovat a na toto musí být softwarově upraveny
- program, který je na popředí zpravidla obsluhuje uživatelské rozhraní (UI)
- při nečinnosti uživatele odevzdá procesor -> OS, který mu propůjčí některého z pozadí, ten musí po uplynutí krátkého času procesor sám vrátit OS a když se to nestane, tak OS zamrzne
- nejsou-li programy na __kooperativní multitasking__ připraveny, tak v takovém OS funguje __pseudomultitasking__
-