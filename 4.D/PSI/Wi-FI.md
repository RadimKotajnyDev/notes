todo: dopsat

- Access Point
	- 1 port
- AP client
	- pracovní režim, který se používá pro připojení PC do Wi-Fi sítě
- Funkční schéma Wi-Fi Routeru
	- ![[Pasted image 20231003090659.png]]
- Wi-Fi síťový most
	- slouží pro propojení dvou sítí LAN, které z nějakého důvodu nejde spojit kabelem
### Podnikové Wi-Fi Sítě
- větší počet přístupových bodů (AP)
- síť se musí chovat jako jeden celek
- jednotné ověřování v síti
- automatické předávání pohybujících se klientů – roaming
	- k tomu se používá Wi-Fi Controller
	- řadič v cloudu
- o podnikových sítí s více uživateli není vhodné sdílené heslo na Wi-Fi
- WPA-2 ENTERPRISE + RADIUS SERVER
- ![[Pasted image 20231010085857.png]]
- WPA2 - PERSONAL – V podnikové wifi síti s centrálním řadičem může být sdílené heslo (sdílený síťový klíč), které je pro všechny uživatele stejné a je uloženo v controlleru a tam probíhá ověření
	- nevhodné pro hodně uživatelů
- WPA2 - ENTERPRISE – Na radius serveru je jméno a heslo (není společný síťový klíč)
	- radius server pod switchem (LAN)
- WEP
	- už se nepoužívá, není bezpečné
	- sdílená data tam, kde kabel dosáhne