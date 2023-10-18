 
#sběrnice #PCIE 
# Typy sběrnic na MB
---
Z hlediska norem, které byly v průběhu let zavedeny
// zde vložit obrátek

## Sběrnice ISA
- počátky počítače PC
- dnes některé průmyslové PC
- 16 bit data, 24 bit adresy => 40 vodičů
- Přenosová f: 8MHz, paralelní
---
## Sběrnice PCI
- dnes na některých MB
- 64bit i 32bit verze
- paralelní 
- prac. f: 66 MHz
- přenos. rychlost 528 MB/s
- SW - plug&play - OS rozpozná a instaluje ovladače
- Typ rozhodování dle IRQ – prioritní
---
## Sběrnice PCI-X
- nástupce PCI
- 64 bit
- přenosová rychlost 4 GB/s
- f = 533 MHz
---
## Sběrnice PCI-E (Express)
- typ přenosu dat – sériová sběrnice
- PCI-EX linky zabírají méně prostoru na MB
- Vyšší přenosové f => vyšší rychlost přenosu

### Specifikace
- Sériový přenos dat
- Full Duplex - v jeden čas
	- 1 Vysílání data do sběrnice TX – Transmit
	- 2 Přijímání data ze sběrnice RX - Recieve
-   Vysoké přenosové rychlosti - dle verze (např 8Gb/s Half Duplex)
-   Vysoké přenosové f
-   SW kompatibilita s PCI
-   Sbt je schopná přenést vysoké napájení

-   Přípojení PCI - ex
    -   Video PCIE -Ex Severní můstek, či CPU (North bridge)
    -   Většina PCI - ex Jižní můstek (South Bridge)
-   Klasifikace datových vodičů
    1.  LINK - komunikační kanál mezi zařízeními
    2.  LANE - diferenciální pár vodičů
        1.  RX
        2.  TX


### Dvoučipové řízení sběrnice
![[dvoucipove-rizeni-sbernice 1.png]]
- CPU přebírá North Bridge