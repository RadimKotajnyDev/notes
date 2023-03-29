---
![[Pasted image 20221111130838.png]]
### Rámec PCI-E / Framing
CRC - Control Count
- Číselná kombinace bitů – ověření správnosti dat 
- Cyclic Redundancy Check
	- Data navíc
				1) odhalení chyby
				2) případné odstranění menších chyb (pár b)
- pozn. – při větších chybách, které nelze odstranit, dochází k opětovnému zasílání poškozeného FRAME (datová čísla)
### Disková Rozhraní 
1) Paralelní 
	- IDE, EIDE – P-ATA
	- odlišná barva
	- 2 zařízení najednou (master - slave)
	- Pokud byl disk na P-ATA kabelu sám – nastavení SINGLE - nutné nastavení na PINech disku
	- P-ATA Přenosová rychlost 133 MB/s
2) Sériové
	- S-ATA – sériová komunikace
	- 1 Kabel = 1 zařízení
	- S-ATA sběrnice na MB - až 4 sloty 
	- SATA kabel má **7** vodičů 
		- 4x aktivní
			- pro přenos DAT
			- RX, TX
		- 3x GND (zemnící)
		- Typ přenosu 
		- SATA1 – až 150MB/s (1,5Gb/s)
		- SATA2 – až 300MB/s
		- SATA3 – až 600MB/s
		- Možnosti **HOT PLUG** – možnost odpojení/připojení bez vypnutí PC
		- Typy SATA
			1) Na MB (4x na desce)
			2) SATA do slotu M.2
				- klíč odlišný pd PCI-E
			3) e-SATA – externí připojný konektor
				- obsahuje 
					- napájení
					- datový kabel
				- kombinuje USB + SATA
	- AHCI – Advanced Host Controller Inferface - pro SSD
	- NCQ – Native Comand Quering (efektivní zápis na disk)
	- rozhraní SCSI
		- Připojení pro disky i jiná zařízení
		- Když nejrychlejší připojení (dnes)
		- až 8 zařízení/8 řadič