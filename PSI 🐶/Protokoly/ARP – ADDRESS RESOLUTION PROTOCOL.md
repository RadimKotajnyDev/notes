---
- slouží pro zjištění MAC adresy cílového zařízení u kterého známe IP adresu
- protokol dělá vazbu mezi síťovou 
- V počátcích internetu a protokolu TCP/IP bylo fyzické a linkové spojení *BOD - BOD* a linkové spojení nepoužívalo žádné adresy 
 ETHERNET - BUS
 ![[Pasted image 20221116091236.png]]
 ![[Pasted image 20221116090947.png]]
- Při prvním požadavku k odeslání dat Ethernetovým rámcem odesílající nezná Cílovou (DEST MAC) MAC adresu, ale zná cílovou  IP adresu
	- proto odešle ARP dotaz
		- Na linkové vrstvě je to BROADCAST
		- ARP DOTAZ PC1 -> PC4
			- DEST.MAC FFFFFFFFFF
			- SRC.MAC MAC PC1
			- DEST.IP IP PC4
			- SRC.IP IP PC1
		- ARP dotaz přijmou všechny počítače na daném segmentu LAN
		- odpověď pošle se svou MAC adresou pošle jenom jehož IP je DEST
		- další komunikace probíhá UNICAST s využitím cílové MAC adresy
		- Každý systém má ARP cache, kde si ukládá MAC i IP adresy, aby se vyloučily opakované dotazy
## RARP
- REVERSE ARP
- dneska se používá DHCP místo RARP
- ![[Pasted image 20221116093028.png]]