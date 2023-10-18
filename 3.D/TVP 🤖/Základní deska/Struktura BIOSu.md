- ovladače komponentů, spec. BIOS některých komp.
- Konfigurace MB uložená v CMOS vzniká automaticky (rozeznání CPU, RAM nebo uživ.)
- Základní konf. "holý", nezměněný
## BIOS
- Kód uložen v paměti typu ROM - EEPROM, flash PROM (možný update)
- <u>nedílná součást</u> MB
- Bez BIOSu
	- nejsou identifikovány komponenty (CPU, RAM, ...)
	- nezavede se OS 
- BIOS je konfigurovatelný - ukládá se do CMOS RAM (3V baterie)
### Posloupnost činností BIOSu:
1) Vynuluje registry CPU
2) nastaví v registrech adresu, na které je BIOS
3) spustí POST (*Power-On Self Test*)
4) kontrola CPU (post)
5) kontrola sběrnice (post)
6) kontrola obvodů připojených na sběrnici (post)
7) kontrola časovače - systémové hodiny (CLK)
8) kontrola video paměti
9) připojení videopaměti paměťového fondu
10) kontrola RAM
11) kontrola klávesnice
12) kontrola dalších zařízení (SATA, disky, USB)
13) Pokud mají zařízení svůj BIOS, začlení jej do hlavního

- Proběhl POST a je známa konf. systému a vše funguje => může být zaveden OS
- Pokud jsou odhaleny chyby - proces se zastaví a jsou oznámeny chyby (zvuk, LED)

14) V BIOSu nastaveno odkud je povoleno zavádět OS
15) BIOS spustí program BOOTSTRAP LOADER
16) najde se zavádějící záznam na médiu (SSD, USB disk)
17) zaváděcímu záznamu se předá řízení
18) dále již pracuje zaváděcí záznam OS - práce BIOSu ukončena (BIOS je stále k dispozici)
### Typy startu PC
A) cold - po připojení PC k síti proběhnou všechny kroky BIOSu
B) hot - po restartu - vynechání POST (body 3-12 se neprovádí, kromě 9)

### Typy UI BIOSu
1) textové - ovládán pouze klávesnicí
2) -,,- s poč. myší
3) grafické - nadstavba BIOSu - EFI

## UEFI
- *Unified Extensible Firmware Interface*
- grafické rozhraní s ovládáním myší
- může obsahovat jednoduché aplikace:
	- ladění výkonu PC
	- Overclocking
	- řízení aktivního chlazení - větráků (křivky - výkon/hlučnost)
	- řízení LED RGB
	- webový prohlížeč
## Rysy moderních CPU
- činnost CPU
	- zpracovávání instrukcí
	- probíhá instrukční cyklus
- kroky instrukčního cyklu:
1) výběr instrukce z paměti
2) dekódování instrukce
3) příprava operandů
4) vykonání funkce
5) zápis výsledků do registrů CPU (paměti)

- registr - nejmenší paměť v CPU - např. 64bit CPU má typicky registry o velikosti 64b
- CPU má desítky takovýchto registrů pro zprac. instrukcí
## Rozdělení cpu dle instrukčních sad
- CISC - *Complex Instruction Set Computing*
	- komplexní instrukční sada
	- von Neumann koncepce
	- 1 instrukce je zpracována v jednom, či více hodinovém taktu
	- Instrukce jsou obsáhlé - umí řešit složitější úkoly
	- nevýhody CISC
		- 