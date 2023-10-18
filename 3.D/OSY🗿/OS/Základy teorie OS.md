# Základy teorie OS
## Základní pojmy 😱
- Technické prostředky
	- holý počítač => bez OS
	- periferní zařízení
	- počítačový síť
- Programové
	- OS
	- ostatní 
	- APV
- Definice OS
	- správce, který spravuje hardware počítače logickými prostředky (algoritmy)
	- je to  program, který je sada programů
- platforma
	- x86, x64 atd.
- OS poskytuje aplikacím své služby
- Virtuální počítač
	- holý počítač na kterém běží vývojové prostředí
- úloha
	- soubor činností
	- 1 úloha != 1 exe
- strojový program
	- vzniká přeložením z vyššího progr. jazyka
	- je závislý na konkrétní procesor, OS
- intepretované jazyky 🤖
	- nemusí se překládat do strojového kódu
- proces
	- vzniká spuštěním programu
	- je nutné rozlišit **víceprocesorový** a **vícejádrový** proces
	- signály, cache jsou stejné
- instrukce se nacházejí u CPU s chráněným režimem idk
- v chráněném režimu běží OS a sys. programy a tyto procesy mohou vykonávat privilegované instrukce (které nemohou vykonávat uživatelské procesy)
### Prostředky 
- složité logické obvody, které jsou v CPU
- CPU s chráněným režimem
- hlídají, aby si procesy vzájemně nezasahovaly do paměti
- výjimka: chybový stav CPU
	- vznikne např.
		- dělením nulou
		- porušení ochrany paměti
		- pokus vykonat neexistující instrukci
	- když nastane výjimka, tak 
	- výjimku lze ošetřit tak, že se ukončí proces vyvolávající chybový stav nebo že se OS zastaví
- technické přerušení
	- logický signál IRQ – Interrupt Request
- Obsluha přerušení
## tabulka přerušení
- CALL adresa
- INTR <číslo_přerušení>
## Rozdělení OS
