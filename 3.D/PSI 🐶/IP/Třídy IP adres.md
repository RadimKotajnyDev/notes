# Třídy IP adres
- Normované rozdělení dle účelu a rozlehlosti sítí
- Třídy zn.
	- A, B, C,
		- Standardní
	- D, E
		- Speciální
- Část IP maj doporučenou
- Část MASKA určuje třídu IP
- 2 části
	- N - Net ID - část vyhrazena pro identifikaci sítě
	- H - Host ID - -,,- Hosta (uzlu) v této síti
- Net ID - jeho rozsah určuje log 1 v masce
- Host ID - -,,- log 0 v -,,-
## Třídy A, B, C mají
- masku určenou celočíselnými násobky 8 bitů
- A : maska 8 bit
- B : maska 16 bit
- C: maska 24 bit
# <u>Třída A</u>
![[Pasted image 20221208092232.png]]
## Rozsah
- IP 1.0.0.0 - 126.255.255.255
- Mask 255.0.0.0 - 255.0.0.0

- Třídu určuje rozsah masky, ten se pro danou třídu nemění
- Pro **Třídu A** je tedy maska vždy tvořena 8 log. 1

## Užití
- V ČR (internet) není žádná IP třídy A
- Vládní organizace, nadnárodní společnosti USA
- adresuje jen 126 sítí
- adresuje obrovské množství H v každé z těchto sítí H = 2<sup>PNM</sup> = 2<sup>24</sup>
## <u>Třída B IPv4</u>
![[Pasted image 20221214090701.png]]
- Rozsah Adres třídy B
	- IP 128.0.0.0 - 191.255.255.255
	- MASKA 255.255.0.0 - 255.255.0.0
- Př. Počet H v každé ze síti třídy B
	- H = 2<sup>16</sup>
- Použití - v ČR pro významné organizace
	- veřejn= adresy tř. B
## Třída C IPv4
- <b><u>-,,- Jen je NNNH</u></b>
- Rozsah třídy C
- IPv3 cl.C: 192.0.0.0 - 223.255.255.255
- Maska cl.C 255.255.255.0 - 255.255.255.0
	- <b>Př.</b> Počet H v každé ze sítí tř. C:
		- H = 2<sup>8</sup>
CLASS(CL)
- použití - V ČR je to většina veřejných IP tř. C
	- privátní - adresování v rámci LAN
## Speciální adresy IPv4
#### <u>Třída D</u>
- NNNH
- Maska 255.255.255.0
- Rozsah
	- IP 224.0.0.0 - 239.255.255.255
### D pokračování
- použití – hromadná vysílání zvuku, videa => MULTICASTING
- Rozsah - 224.0.0.0 až 239.0.0.0
	- 255.255.255.0 - 255.255.255.0
## <u>Třída E (speciální)</u>
- ![[Pasted image 20221215090912.png]]
- Použití: není pro běžnou adresaci uzlů (serverů) v internetu
- rozsah 240.0.0.0 až 248.255.255.255
	- 255.255.255.0 - 255.255.255.0
## Speciální adresa Broadcast
IP |N|N|N|H|
Mask 255.255.255.0

IP 255.255.255.|255| (HOST)
mask 255.255.255.0

- BroadCast
	- = všesměrové vysílání
	- = informace určena pro všechny uzly v síti
	- vysoká důležitost, konfigurace
- Přichází a je akceptována všemi uzly v síti
- Obecná Broadcast adresa
	- v části HOST obsahuje IP adresa samé bin 1
## Speciální adresa <u>Loop Back</u>
- IP |N|N|N|H|
- mask 255. 255.255.0
- Poze jedna adresa
- LB IP 127.0.0.1 (localhost)
- maska 255.255.255.0
- 