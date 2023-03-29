2022/10/07|1241
# Sběrnice
Význam
		- Komunikační cesty ( HW )
		- Přenosové protokoly ( SW )
		- Přenosové metody ( HW + SW )

Zajišťují 
	- napájení komponentů MB
	- komunikační a energetické toky MB

## Sběrnice dle účelů
1. adresová
	- přenos adresy ( lokality dat )
	- umístění na paměťové médium ( RAM, SSD, ...)
2. datová
	- Tady se přenáší data 
3. řídící
	- řízení přenosu ( kdo kdy komunikuje )

## Druhy komunikace
### Paralelní
data posílána po více vodičích najednou

### Sériová
data posílána po jednom vodiči dat. sb. za sebou --> bit po bitu

## Časování
systémové hodiny ( clock - clk )
	- synchronizace činností na sběrnici MB
	- časování práce komponentů na MB

### Paralelní sběrnice
desítky vodičů rozdělených do 3 skupin ( A, D, Ř )

A - udává množství adresovatelné paměti Pp
	šířka = počet vodičů = N
	`Pp = Z^N bitů`

D - kolik dat najednou lze přenést ( 256 bitů, 128b )
	v jednom synchronním taktu ( u sběrnice synchronní )

#### Synchronní sběrnice
- činnosti probíhají dle clock
#### Asynchronní sběrnice
- činnost rozlišena oddělovači bitových intervalů

### Řídicí sběrnice
1. Memory Write
2. -||- Read
3. Žádost o sběrnici
4. Povolení přenosu - udělení sběrnice
5. I / O Write
6. I / O Read
7. Hodinové pulsy


## Řízení sběrnice 
BUS Controller - CHIPSET
Rozhodování   - Prioritní - dle priority ( důležitosti ) komunikace a zařízení
( CPU <=> RAM ), důležitějšímu zařízení sběrnice přidělena i když žádalo později
						- Spravedlivé - Náhodně - dle aktuální potřeby zařízení 

Prioritní - centrální ( Chipset )
Spravedlivé - Decentrilizované - logika komunikace je v koncových prvcích

### IRQ
Interrupt Request
pro obsluhu externích zařízení CPU
![[Pasted image 20221111124829.png]]