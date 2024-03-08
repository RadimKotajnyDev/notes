# Úloha 6. 3.
## konfigurace routeru
- nastavení rozhraní WAN
	- IP 192.168.255.[14]
	- výchozí brána 192.168.255.1
	- maska 255.255.255.0
	- DNS 8.8.8.8
- pracovní režim routeru NAT
	- zapnout DHCP server
	- jeden počítač bude mít pevnou IP adresu
	- rozsah DHCP 192.168.1.10 ... atd.
	- na PC - RADIM (pevnou adresou) zprovoznit Internet Information Services
		- z počítače udělat virtuální server, aby se jevil na IP adrese a WAN rozhraní na portu 80
	- musí být vypnutý managování adres z WAN
	- jednoduchou stránku