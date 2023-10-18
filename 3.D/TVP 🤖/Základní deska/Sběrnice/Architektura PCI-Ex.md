#PCIE 
---
- podobné komunikace modelu v PSI
- rešení pomocí vrstev C jako ISO / OSI
- architektura Peer2Peer - rovný s rovným -> umožňuje nezávislou komunikaci PCI-Ex zařízení
![[IMG_5316 1.heic]]

## Vrstva 1 Transakční
- tvoří PCI-ex Packety
- rozdělí celístvý "balík" dat (připravený k odeslání) na menší celky
## Vrstva 2 Data Link (linková v.)
- zajištění INTEGRITY Dat
- Kontrola neporušenosti dat
- přidá kontrolní součet (CRC)
## Vrstva 3 Fyzická
- Obsahuje IO, el. obvody nutné k připojení PCI-Ex Link (základní sériový vodič)
- Původní logický tok dat (log != a log 1) je převeden na el. signály
- Tx – Transmit Obvod - vysílací
- Rx – Recieve -,,- přijímací
- El. sig. obsahuje el zálohovací data
	- sig. ozn. začátek/konec packetu
	- sig. pro synchronizaci komunikace