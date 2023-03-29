# DNS
- *Domain Name System*
- Např. Doménové jméno Seznam.cz - IP 77.75.75.176
- DÚ: Google.com - 142.251.37.110
## Místní DNS server
- DHCP přidělí automaticky adresu místního DNS
	- a) router v domácí síti
	- b) dedikovaný server v síti (např. Win server)
## Cache DNS 
- nedávné překlady, které proběhly v rámci (naší) LAN jsou uloženy do paměti (tabulka DN a IP)
- urychluje překlad
- snižuje zátěže celého DNS v rámci internetu
## Kořenové DNS servery
- nachází se v internetu - drží důležité DNS záznamy
- Autorativní DNS servery - nachází se v internetu - drží okruhy DNS záznamů
## Systém Doménových Jmen
- pravidla pro tvar a velikost jmen v DNS
- FQDN - *Fully Qualified Domain Name* - určuje umístění serveru v struktuře DNS
- příklad: mapy.seznam.cz. 
	- mapy => (dom. jméno 3. úrovně)
	- seznam => (2. úrovně)
	- cz => TLD - *Top Level Domain*
	- . => Root Domain
- FQDN - posloupnost 

- Autorita nad doménou a zóny
	- hlídá dodržování prav. DNS
	- přiděluje/mění jména
	- zařizuje/ruší dílčí domény
	- autoritu nad dílčími doménami může delegovat (mapy deleguje na seznam)
	- udržuje databázi jmen
	- zabezpečuje překlad jmen na IP
- gTLD (generic)
	- com, gov, org, edu, info, int
- sTLD (sponsored)
	- museum, travel, jobs
