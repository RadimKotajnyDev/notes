# Sdílení souborů v OS Windows
## NETBIOS
- protokol IPX
- Win95 – TCP/IP
- SMB – *Server Message Block*
	- více zatěžuje SMB oproti jiným protokolům
	- dále řeší šifrování dat
	- odolný přenos souborů
	- odolnost proti výpadkům
	- ověřování uživatelů k přístupu k veřejným prostředkům
	- způsoby ověřování
		- pro sdílený prostředek existuje společné heslo (nepoužívá se)
- pro Unix / Linux existuje SMB server, který se jmenuje Samba (reverse engineering)
## ověřování
- 1) zadává se pouze heslo
- 2) jméno a heslo
	- malé firmy
	- ověření na řadiči domény
- 3) vypne se sdílení chráněné heslem
## Oprávnění pro sdílení
- přežitek z doby, kdy ve Windowsech nebylo NTFS oprávnění
- oprávnění ke sdílení lze přidělit uživatelům a skupinám, ale pro __celý__ sdílený prostředek, nelze ho aplikovat pod podsložky a soubory
- úrovně
	- Úplné řízení (umožňuje změnu oprávnění na sdíleném prostředku a to včetně NTFS oprávnění)
	- změnit
	- číst
- když potřebujeme přidělat oprávnění na podsložky (i soubory) to sdílené složky, tak použijeme NTFS oprávnění
- __efektivní oprávnění ke sdílení je logický součin oprávnění ke sdílení a NTFS oprávnění__ (z důvodu kompatibility)
### připojení ke sdílenému prostředku
1) průzkumník windows