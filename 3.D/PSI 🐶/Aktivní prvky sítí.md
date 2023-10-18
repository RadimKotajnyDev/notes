x# Aktivní prvky sítí
- je zdrojem užitečných signálů v síti
- nejjednodušší – dokáží sig. zesílit, obnovit průběh sig.
- pokročilé – dokáží "číst" v sig. (zpracování hlavičky PACKETU)
	- umí rozhodnout o pokračování - cestě sig. v síti
## Základní charakteristiky (APS)
### účel
1) Připojení uzlu do sítě
2) zvýšení počtu uzlů v síti
3) umožní funkci sítě (např. pro danou kategorii)
4) propojení sítí s různými architekturami (HUB<->STAR)
5) zvýšení dosahu sítě (repeater - opakovač)
6) propojení sítí s různým typem kabeláže (TP<->OPTIC)
7) Filtrování paketů pro různé podsítě
## Značky aktiv. prvků
![[Pasted image 20230419092341.png]]
### Opakovač - Repeater
- zvýšení dosahu - optic, koax. kabely (dnes anténní)
- pracuje a fyzické vrstvě ISO/OSI
- Příchozí sig. obnoví (zesílí) do původního průběhu
### Media converter - transciever
- Převodník - převod jednoho typu sig. na jiný
- jádro jeho repeater, ale umí pracovat s různými typy el., elmag. sig. na I/O TCP <-> OPTIC
# Síťový karta N.I.C
- Network Interface Controller
- Rozhraní pro komunikaci s uzly v síti 
- ![[Snímek obrazovky 2023-04-20 v 9.18.45.jpg]]
### Úlohy N.I.C
1) příprava dat
2) odesílání dat / příjem dat
3) kontrola toku dat
#### příprava dat
- příjem dat od CPU do Cache
- zajištění sériového toku dat
- převod dat do formátu dle nodem pro:
	- Ethernet kabel
	- Optic. kabel
- bin 1 a 0 je nutné převést
### Parametry posílání dat
- max. velikost odesílaných datových jednotek (PDU - packet - *protocol data unit*)
- časové intervaly mezi potvrzeními správnosti přenosu
- množství dat posílaných mezi potvrzeními
- platí potvrzený, spolehlivý přenos - TCP
### HUB
- aktivní prvek
- pracuje na fyzické vrstvě ISO / OSI
- vylazuje chování sítě zapojené jako BUS
- obrázek