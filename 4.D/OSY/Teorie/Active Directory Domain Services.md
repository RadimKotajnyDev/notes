# Active Directory Domain Services
- adresářová služba od MS
- je realizována stejnojmennou rolí ve windows
- hlavními úkoly v této roli je 
	- centrální ověřování a správa uživatelů
	- centrální správa dalších zařízení jako jsou např. počítače a tiskárny v doméně 
	- nastavování přístupových oprávnění a u počítačů s OS Windows i centralizovaná správa OS
	- řízení přístupu v počítačové síti
		- k tomu je potřeba NPS (*Network Policy Server*)
- hlavní službou role je **Řadič domény**
## Složení Active Directory
- skládá se z databáze – objektově orientovaná, stromovitě uspořádána (hierarchicky)
- základními objekty jsou např.
	- organizační jednotka OU (Org. Unit)
	- uživatel
	- skupina uživatelů
	- počítač
	- tiskárna
- u objektu se ukládají atributy
- výchozí definice všech objektů je v tzv. schématu
## Síťové služby Active Directory
- slouží k ověřování uživatelů na klientských počítačích
- poskytují aplikační rozhraní pro přístup k **AD**
### služba síťových politik
- slouží k centrálnímu řízení OS Windows na klientských počítačích
## Hlavní přínosy **Active Directory**
- uživatel se přihlašuje jediným heslem ke svému PC a zároveň k dalším zdrojům v síti
- centrální správa Windows pomocí skupinových politik
- Admin má přehled o technice a uživatelích v doméně
---
- běží na Win serveru a realizuje základní služby ADDC (*Active Directory Domain Controller*)
- IP adresa doménového řadiče musí být zapsána v SRV záznamu
- v jedné doméně se doporučuje mít 2 doménové řadiče pro případ selhání jednoho z nich
- data mezi doménovými řadiči se automaticky replikují
- někdy se používá *The read-only Domain Controller* – v něm se nedají měnit data a přebírá data z primárního data controlleru
	- používáme v nezabezpečených umístěních
- 