# Role windows serveru v síti
- role je jedna služba nebo více souvisejících služeb, které server poskytuje klientům.
- skládá se z 1 nebo více služeb
- po instalaci nejsou aktivní žádné role
- administrátor je nainstaluje a nakonfiguruje
- OS je role vykonávaná 1 nebo více běžícími procesy (proces vzniká spuštěním programu)
- drobné funkce se nazývají vlastnosti = features

- role poskytuje funkci do tzv. doménového řadiče
	- doménový řadič je centrální místo v síti, které slouží k ověřování uživatelů a zařízení v síti a může sloužit i k centralizované zprávě OS na počítačích v doméně
	- ADDC (domain controller)
	- Microsoft Azure Active Directory
	- Active Directory Lightweight Directory Services – role komunikace s řadičem domény LDAP 
		- (*Lightweight Directory Access Protocol*)
	- aplikační protokol k tzv. adresovacím službám
	- je to průmyslová standart
	- slouží pro propojení domény i se zařízeními, kde není OS windows
		- typicky se používá na připojení kopírek systému docházkových a řízení přístupu, které potom mohou ověřovat uživatelé na řadiči domény

- FAX server
	- virtuální tiskárna
- File and storage services (to nevím jestli je správně)
	- obsahuje větší počet služeb
		- nejhlavnější je File Server
- Hyper-V (<span style="color: red;">Nejnáročnější – umět odůvodnit</span>)
	- virtualizace od MS
	- součást windows serverů
- Network Policy and Access Services
	- slouží pro ověřování v síti a používá se např. ve Wi-Fi sítích
	- uživatel se přihlašuje účtem v Active Directory
	- nepoužívá se veřejné heslo
- Print and Document Services
	- sdílené síťové tiskárny a řízení uživatelů přes Active Directory
- Remote Access => Vzdálený přístup
	- scanování
- Web Server (IIS) – internet information services

- některé role nemohou spolu být na jednom serveru (i virtuálním) a u některých rolí se doporučuje instalace na samostatný server
	- např. Active Directory, Web Server