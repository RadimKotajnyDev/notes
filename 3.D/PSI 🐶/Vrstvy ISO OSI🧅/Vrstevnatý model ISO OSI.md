# Vrstevnatý model ISO / OSI
Norma - závazný předpis definující základní vlastnosti entity v dané technické oblasti
## Organizace definující normy
- ISO - International Standard Organization
- ČAS - Česká agentura pro Standardizaci

## Normy
- ČSN - Česká státní norma
- OSI - Open System Interconnect ( by ISO ) => ISO / OSI

## OSI
Otevřený systém pro propojování - definuje HW a SW vlastnosti pro vzájemnou kompatibilitu síťových zařízení ( uzlů - aktivních prvku i pasivních prvku ) různých výrobců

## Před zavedení norem ISO
uživatelé síťových řešení byli závislí na specifické technologie jednoho výrobce => poruchy, výměny, upgrade řešil jen původní dodavatel --> technologie nebyly kompatibilní

## Vrstvy
7-5 - vrstvy orientované na Aplikace v OS => SW vrstvy
4 - na rozhraní SW a HW
3 - Přenosy LANx - LANy
2 - Přenosy LANx- LANx
1 - Převod do formát energie kompatibilní ho pro specifické přenosové médium ( kabel, optika, wifi )
3 - 1 - vrstvy určené pro přenos dat po a přístup k přenosovému médiu

### 7. Aplikační vrstva
### 6. Prezentační vrstva
### 5. Relační vrstva
### 4. Transportní vrstva
### 3. Síťová vrstva
### 2. Vrstva datových spojů (Linková)
### 1. Fyzická vrstva
---
## 7. Aplikační v.
- Aplikace c OS se umí v 7. napojit ( v případě potřeby )
- v 7. převezme  DATA app určené k přenosu
- v 7 = rozhraní pro odesílání dat po sítí
- App pouze umí poslat požadavky a data do v 7
- v 7 je SW vrstva
---
## 6. Prezenční v.
zajištění obecného drátového formátu
-> porozumění mezi různými platformami OS
- komprimace / dekomprimace dat
- šifrování / dešifrování dat
- V. 6 je SW
---
## 5. relační vrstva
- řízení komunikace mezi 2 aplikacemi na 2 různých uzlech
- volání vzdálených procedur 
	- zasílání/příjem požadavků na vzdálené spuštění činností
	- RPC – Remote Procedure Call
- QoS – Quality of Service
	- ověří, zda byla činnost na vzdáleném uzlu vykonána, případně zajistí nápravu.
---
## 4. Transportní v.
- mezivrstva 
	- SW
	- HW
- Adresování aplikací na daném uzlu pomocí čísel - portů
- Poskytuje služby 
	- spojově orientované (connection oriented)
	- nespojově orientované (connectionless or.)
- connection oriented - spolehlivé, ověřené doručování dat - protokol TCP
- Transmission Control Protocol
1) navázání komunikace
2) zasílání dat
3) ověření správného přenosu/Náprava chyb
- **TCP – pomalejší, ale spolehlivý**
- nespojové ori. služba - **protokol UDP (User Datagram Protocol)**
	- vyšle data, nestará se o správnost doručení a přenosovou cestu => nespolehlivý, ale rychlý přenos

## 3. Síťová 
- Jednotka přenosu dat (PDU) : PACKET
- Funkce - přenos dat mezi uzly BEZ přímého spojení
př) a) LAN 1 – ROUTER – LAN 2
	b) TODO: obrázek
- přenos probíhá přes libovolná počet uzlů
- klíčové uzly – Routery znají své okolí
- Routery provádí směrování paketů = routing
- Routing – hledání cesty k cíli
- Aktivní prvky na L3 (3. vrstvě)
	- Router
	- L3 switch
- Styl práce - spojové 
	- vytáčí před komunikací trasu přenosu
	- ověří kvalitu trasy
	- ověří data, jestli dorazily do cíle neporušena
- Nespojově - data mohou k cíli putovat po různých trasách
	- jednotlivé packety zaslaných dat mohou putovat jinými cestami
- ověření packetu není ověřováno