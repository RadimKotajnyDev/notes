# <u>Adresace v Síti</u>
![[Pasted image 20221207090041.png]]
- Adresace v síti: tvar adres, adresát a příjemce
	- tvar adres se řídí normou
		- Norma určuje protokol: 
			- vlastnosti
			- název (IPV4, IPV6)
## <u>IPv4 Protokol verze 4</u>
- PDU - protocol data unit - Datagram v jehož hlavičce je IP adresa
- IPv4 adresa - tvar v paměti, PDU : binární číslo o vel. **32 bitů**
- má 2 části (neoddělitelné)
	- IP adresa 32 Bit
	- Maska sítě 32 Bit
10111011011011101110000111010110 - IP
1111111111111111111111111110000000 - MASKA
- Maska sítě dělí IP adresu na
	- Net
	- Host
- Maska vždy začíná log 1 a končí log 1, kde mezi počáteční a koncovou log 1 NENÍ obsažená log 0
- log 1 v MASCE – část IP vyhrazena pro NET
- log 0 -,,- HOST
- <span style="text-decoration: underline; color: aqua; font-weight: 800">První bit v IP je svázán s prvním v Masce</span>

### Zjednodušený zápis IPv4
- Používá se pro konfiguraci aktivních prvků sítě (síť. karta, router, switch)
- Tvar srozumitelnější pro člověka –> DEC tvar
- Pravidlo: Rozdělení 32 bit čísla na části po 8 bitech => těchto 8 bit převedeme
	- např. 192.168.2.5 –> IP v ec
		- 255.255.255.0 –> MASKa v DEC
- DÚ: převeďte do BIN
	- 11000000101010000010101
