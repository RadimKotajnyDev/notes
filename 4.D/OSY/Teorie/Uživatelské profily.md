# Uživatelské profily
- je uložen na systémovém disku ve složce Users
```
%SYSTEMDRIVE%\Users\<username>
```
- uložení profilů
	- Local = místní
	- Roaming = cestovní 
	- Mandatory = povinný
## Local
- místní profil
- funguje na počítačích ve windows doméně úplně stejně jako bez windows domény
- pokud se profil nesynchronizuje jinými způsoby, tak je na každém počítači jiný
## Roaming
- cestovní profil
- používá se na windows doméně
- je uložen na windows serveru
- při přihlášení uživatele se profil zkopíruje nebo synchronizuje 
- v okamžiku odhlášení uživatele se místní kopie synchronizuje s profilem uživatele na serveru
- nevýhoda pomalé synchronizace, když uživatel stáhne velký soubor
	- řešení -> složky, kde očekáváme velké soubory buď to ponechat je lokálně nebo přesměrovat na síťový disk
## Mandatory
- povinný

- při přihlášení vzniká lokální kopie, ale provedené změny se neukládají zpět na server

- závěr: 
	- profily slouží k zajištění jednotného pracovního prostředí buď to na více počítačích nebo pro více uživatelů