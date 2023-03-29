---

## Typy disků
### disk na magnetickém principu (pevný disk)
- otáčky kolem 7200 ot/min (násobky 3600)
- Geometrie jedné plotny pevného disku
![[Pasted image 20221122100558.png]]
- modrá je sektor
- cylindry
- červená je fyzický blok
	- Fyzický blok obsahuje **512 Bytů** dat dostupných programově
	- kromě toho obsahuje další data nutná pro fungování samotného pevného disku a ta jsou programově nedostupná. Pracuje s ními elektronika samotného pevného disku. (pomocná data, aby to elektronika přečetla)
	- aby byla hustota záznamu na stopě optimální, tak se používá **vzorový záznam**.
- Zelená 
- Disk je rozdělen na zóny, a ve vnějších zónách je více sektorů, než v těch vnitřních
- Elektronika HDD používá technologii S.M.A.R.T.
- *Self Monitoring, Analysis, and Reporting Technology*
	- Kritické chyby jsou předávány do BIOSU a OS
	- Důležitou funkcí S.M.A.R.T. je tzv. přemapování fyzických bloků
	- Říká se, že na disku je cca **10% volného místa** navíc. (neuvádí výrobce)
	- Když některé bloky mají problémy se zápisem a čtením, pevný disk je sám přesměruje do rezervního místa. Na venek to nepoznáme, adresa bloku se nemění.
	- Nověji se používá velikost fyz. bloku **4kB**, takový disk umí pracovat se <u>starou</u> velikostí fyz. bloku
- Z technicý důvodů OS sdružují fyzické bloky do tzv. alokačních jednotek je tvořena 2^N fyzických bloků
	- Alokační jednotka je nejmenší část disku se kterou pracuje operační systém v případě, že pracuje s logickým diskem.
#### Adresa místa na disku
- Kompletní fyz. blok je určen CHS (*Cyllinder head sector*)
	- nevýhoda
		- závisí na fyzické adresaci disku
		- velikost čísel sys. naráží na limity v BIOSu, ale specifikaci rozhraní HDD ATA/IDE
		- CHS je limitován max. do **8GB**
- Nový systém je adresa **LBA** (*Logical Block Addressing*)
	- počítá od 0 lineárně
	- zákl. délka adresy 28 bitů, což se počítá 2^28. 
	- Adresa má až 48 bitů, což max je 128GB.
	- Adresa současně má 128bitů, max dat = 128 PiB
### disk ve formě polovodičů (SSD)
- také mají sektory (stránky)
- SSD je *Solid State Drive*
- neobsahuje točivé části
- data se ukládají do polovodičové části
	- ta je elektricky zapisovatelná a mazatelná EEPROM
	- paměťové buňky jsou organizovány po stránkách
		- (stránka funguje jako fyz. blok u HDD)
	- mazání je po stránkách z důvodu rychlosti
	- paměť uchovává el. náboj
- SSD mají S.M.A.R.T.
- Na fyzickém médiu může být jedna nebo i více logických diskových jednotek.
- FLOPPY disky nebyl důvod rozdělovat
- U pevných disků jsou k rozdělování tyto <u>důvody</u>:
	- oddělení OS a uživ. data na 2 log. jednotky
	- mít v PC více OS
	- historický důvod:
		- souborové systémy měli menší kapacitu, než fyz. disk
#### Příznak aktivního oddílu
- logická hodnota (je nebo není)
- Aktivní může být jenom 1/4 oddílů
	- z aktivního se bootuje OS
- pozn. (CHS bylo používano MS-DOS a ve Win95 se přešlo na LBA)
- Začátek oddílu k souřadnici CHS
- Konec oddílu k souřadnici CHS
- Začátek oddílu k souřadnici LBA
- Velikost oddílu k počtu fyzických bloků
- MBR podporuje disky do velikosti 2TB
	- Na větším disku více, než 2TB nelze použít
- Oddíly jsou :
	- **primární** (právě 1 logická jednotka)
	- **rozšířené** (logická jednotka => písmenko disku)
	- ![[Snímek obrazovky 2022-11-30 v 8.22.41.jpg]]
#### Rozdělení MBR
- znamená ***Master Boot Record***
- hlavní záznam je uložen na adrese LBA=0
- zabírá 512 Bitů
- <table style="color: aqua;">
	<thead>
		<tr style="font-weight: 800;">
			<td>Popis</td>
			<td>velikost v Bytech</td>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>code area (zavaděč)</td>
			<td style="text-align: center;">440</td>
		</tr>
		<tr>
			<td>Disk Signature (volitelné)</td>
			<td style="text-align: center;">4</td>
		</tr>
		<tr>
			<td>usually nulls; 0x0000</td>
			<td style="text-align: center;">2</td>
		</tr>
		<tr>
			<td><b>Table of primary partitions</b></td>
			<td style="text-align: center;">64</td>
		</tr>
	</tbody>
</table>
- V oblasti kódu je uložen tzv. hlavní zavaděč. a je to malý program.
- Při startu PC Windows načte do RAM celý MBR a spustí kód hlavního zavaděče
- hlavní zavaděč najde v tabulce rozdělení tzv. aktivní oddíl, z něho načte **Boot Sector** a spustí kód obsažený v <u>code area</u>; druhý zavaděč zavede z daného oddílu konkrétní OS.
- tabulka rozdělení obsahuje 4 stejné záznamy tak, že na disku jde vytvořit 1 - 4 oddíly
- MBR <u style="color: red;">problémy</u>:
	- s velikostí disku (2TB max)
	- omezený počet oddílů
	- problematické rozšířené oddíly
	- nízká bezpečnost (data nemají zálohu)
	- Kód v MBR může být infikován virem
		- proto s příchodem UEFI přišlo GPT
#### Rozdělení GPT
- *GUID (Global unique ID) Partition Table*
- nahrazuje **MBR**
- umožňuje rozdělit disky >2TB+
- součastí UEFI BIOSu
- tabulka rozdělení má 128 položek (až 128 oddílů)
- ![[Pasted image 20221206100539.png]]
- oddíly jsou primární, nelze je dělit
- nepoužívá se <strong><u>Hlavní zaváděcí záznam</u></strong>
- Boot Sector akt. oddílu je načten přímo BIOSem
- případně BIOS načte přímo zavaděč windowsu
- GPT a UEFI podporují tzv. Secure Boot a šifrování pomocí Bitlockeru
#### Souborový systém FAT
- způsob uspořádání dat na disku, aby se uživ. jevili jako soubory a složky
	- k tomu se používají **METADATA**, která ukládájí jména souborů a složek, další informace o souboru jako např. velikost, datum vytvoření, atributy, oprávnění pro přístup a hlavně ukládají informace o tom ve kterých místech v disku je soubor fyz. umístěn
- existují různé souborové systémy a liší se rozsahem Metadat, jejich formátem a způsobem ukládání informací o místech uložení jednotlivých souborů
- souborové systémy
	- FAT – DOS
	- exFAT
	- NTFS – Windows
	- ext2, ext3, jfs – Linux/unix 
- FAT = *File Allocation Table*
- souborový systém vzniká formátováním, tím vytvoří na disku Metadata
- <div style="font-size: 25px; font-weight: 700">Nejmenší souborová část je alokační jednotka, obsahuje 2^n fyz. bloků</div>
- struktura oddílu s FAT
	- ![[Pasted image 20221207080715.png]]
	- BS obsahuje metadata, kód zavaděče (formát OS)
	- FAT - *File Allocation table*
		- funguje jako mapa dat. části disku
		- každému číslu FAT odpovídá 1 alokační jednotka
		- FAT12, FAT16, FAT32 (**Číslo znamená kolik má bitů položka ve FAT**)
	- Kořenový adresář
		- každý soubor nebo podadresář v -,,-, tak tam má 1 záznam
		- stejně jako -,,- fungují i všechny podadresáře
		- 8 + 3 <dopsat>
		- potom jsou tam uloženy atributy souboru
			- A (archive), H (hidden), R (read-only), S (sys), D (dir)
		- pozn. Windows nepodporuje dlouhé názvy na FAT12
		- když ve FAT jsou logické 1 (FFFF<sub>h</sub> = EOF; 0000<sub>h</sub> = FREE)
		- ideální je kdyby alokační jednotky každého souboru byly za sebou. Protože soubory neustále mažeme a vytváříme, tak na disku ubývá souvislého místa (fragmentace disku)
			- fragmentace zpomaluje výkon hlavně u HDD
				- proto se dělá defragmentace
		- Kořenový adresář je uložen v datové části jako normální soubor, takže není omezen počtem položek
#### NTFS
- *New Technology File System*
- Vzniklo pro Windows NT (sys pro servery)
- Postupem času se vyvíjel souběžně s Windows Server
- Aktuální verze Windows NT je 6
- NTFS přináší nové vlastnosti důležité pro Servery: ⬇
	- Přístupová práva k souborům a složkám
	- Eviduje vlastníka
	- Eviduje 3 časové údaje
		- kdy byl vytvořen, poslední změna, poslední otevření
	- Podpora UNICODE
	- Žurnál => změny <= crash = obnovení
	- Komprese funguje ONLINE
	- Klíč je vytvořen z hesla uživatele
	- Co uživatel zašifruje tak nepřečte Admin
	- Podporá symbolických pevných linků jako v Linuxu
		- ln = soubor s cestou k jinému souboru/složce
		- pevný link = spojení souborového souboru na úrovni systémového
	- Diskové kvóty
		- nástroj pro vymezení místa na disku pro uživatele
- K ukládání METADAT používá systémové soubory
#### Souborové systém v Unixu a Linuxu
- Použivají se I-uzly
- Unix 
	- víceúčelový, síťový, 
	- 1969 - Kevin Thompson, Denis Ritchie
- Prvotní souborový systém Unixu se jmenoval "*UFS*")
	- UFS -> EXT2 (->JFS) -> EXT3 -> -> EXT4
	- JFS = *Journaling File System* -> OS IBM AIX
- UNIX sys. jsou navrženy POSIX (*Portable Operating System Interface*)
#### Společné vlastnosti Unixových a Linuxových FS (file sys)
- eviduje vlastníka souboru a jeho skupinu
- vlastnosti souboru jsou přístupová práva
	- r/w/x (read/write/execute) => 1 bit
		- vlasník, skupina, ostatní
	- Unixové soubor. sys. podporují symbolický i pevný link
	- podobně jako NTFS evidují 3 čas. údaje
	- i-uzel
- ![[Pasted image 20221212115936.png]]