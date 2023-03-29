# BooP DHCP
- Informace jsou k uzlu přideleny dočasně - LEASE TIME
- Délka poskytování je volitelná -> od hodin, po dny
- LEASE TIME se volí - dle situace
	- např 1) restaurace - hosté v síti (i v restauraci) se mění často nemá cenu poskytovat ip adresu dlouho - volí se 2h

a) Pokud host je host přítomen - může zažádat o prodloužení pronájmu IP
b) Pokud již daný host odešel - jeho IP je k dispozici jiným hostům

2) firma - hosté(hosté v síti, PC, tiskárny..) jsou na svých pozicích stále, mění se výjimečně. Lease tune he volen ve dnech

POOL: je to rozsah IP adres, ze kterého DHCP server poskytuje IP adresy
rozsah může být např. 192.168.3.10 / 24 až 192.168.3.254
Postup DHCP žádosti a přidělování:
	1) DHCPdiscover - uzel hledá DHCP server v síti - broadcastovým vysiláním
	2) DHCPoffer - DHCP server nabízí IP adresu žádajícímu uzlu
	3) DHCPrequest - host (uzel) žádá pronájem nabídnuté IP adresy
	4) DHCPack - DHCP server zapíše do své tabulky hosta (IP+MAC+LEASE TIME) a potvrdí pronájem hostovi v síti

## Porty pro komunikaci
- UDP
- Client(host): 68
- Server(router): 68
## Síťové porty
- Socket
	- IP uzlu – analogie adresy panelového domu
	- Port – komunikace s určitou aplikací
		- adresace aplikací v rámci konkrétního uzlu (hosta) sítě
- zápis čísla portu IP:Port
	- 192.168.3.8:80
- V BIN je port 16 bit číslo => 2^16 => 0 až 65 535
- Protokoly
	- TCP (spojovaný, spolehlivý)
	- UDP (nespojovaný, vysílá bez ověření doručené)
	- oba mají porty 0 - 65535
## WKP
- *Well known ports*
- pro běžně uživáné služby jso určeny přesná čísla portů
- Rozsah WKP 0 až 1023

HTTP - TCP - 80
DHCP - UDP - 67
FTP - 20 - 20
HTTPS - TCP, UDP - 443 
