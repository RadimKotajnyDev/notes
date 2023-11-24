# Pošta MAIL
![[Pasted image 20231109094632.png]]
---
![[Pasted image 20231109094413.png]]
## Struktura dopisu
- obálka – neviditelná, vzniká a zaniká při SMTP
- hlavičky – popisné informace dopisu (kdo, kdy)
- tělo – vlastní nesená zpráva
---
- sedmibitová omezení
- MIME 
- problémy se znaky
---
## Poštovní klienti
dnes obvykle součásti systému
- MS Outlook
- Mozilla thunderbird
- Opera
- Webmain
---
## Kódování
### SMTP
- Simple Mail Transfer Protocol
- Pošta mezi odesílatelem a příjemcem (odesílání)
- TCP protokol
- doručování pomocí
	- MUA – *Mail User Agent* => zpracovává zprávy u uživatele
	- MTA – *Mail Transfer Agent* => server, který se stará o doručování zprávy na cílový systém adresáta
	- MDA – *Mail Delivery Agent* => Lokální doručování, zpracovávání, ukládání zpráv
### IMAP
- příchozí pošta
- *Internet Message Access Protocol*
- TCP (:143)
- stahuje si nezbytné informace
- uchovává stav důležitý
### POP
- *Post Office Protocol* – POP3
- stahuje všechny zprávy, včetně spamu
- výhodný pro časově omezené nebo nestálé připojení k internetu
- zprávy stáhne a odpojí se
- server nepustí 2 klienty na stejném mailu
- maily uchovává pouze na počítači a na serveru bude místo
## Výhody IMAP oproti POP3
- způsoby připojení
	- POP3 na dobu stažení pošty
	- IMAP dokud je aktivní rozhraní
- více klientů ke stejné schránce
- Přístup ke zprávám ve formátu MIME
- Informace o stavu zprávy
	- IMAP udržuje přehled o stavu zprávy (přečtena)
### MIME 
- *Multipurpose Internet Mail Extensions*
- Standart pro zasílání zpráv obsahující
	- text s diakritikou
	- přílohu
	- digitální podpis
### kódování
- quoted printable
	- kóduje jen znaky, které nejsou v ASCII tabulce
- Base64
	- překóduje všechny znaky včetně sedmibitových
### šifrování
- asymetrická kryptografie
	- jiný klíč pro šifrování i dešifrování
	- alg. AES (256 bit) nebo slabší 3DES, RC2
- pro zaslání šifrovaného emailu, musíme vlastnit šifrovací certifikát (veřejný klíč)
	- dešifrování pomocí odpovídajícího privátního klíče
### Kryptologie
- šifrování
- **šifrovací algoritmus** – funkce na matematickém základě
- **šifrovací klíč** – říká alg. jak dešifrovat
- **délka klíče** – ovlivňuje čas prolomení hrubou silou (všechny kombinace)
- **nešifrovaný text**
- příklady šifrovacích algoritmů
	- pouze privátní klíč
	- veřejný klíč
	- kryptografické kontrolní součty
	- symetrické šifry sestavené z jediné matematické operace XOR
#### symetrické šifrování
- nejstarší technika
- 1. nosí klíč, 2. nosí šifrovaný text
- výhody
	- nízká náročnost
- nevýhody
	- sdílení tajného klíče
		- odesílatel a příjemce zprávy se domluví na klíči
		- často se používají společně s asymetrickými
	- proudové šifry – zpracovává text po jedn. bitech
	- blokové šifry – rozdělí text na stejně velké bloky a doplní poslední blok na stejnou velikost
#### asymetrické šifrování
- dvojice klíčů na 1 odpověď
- veřejný klíč je dostupný pro odesílání dat
- všechny zprávy, které jsou šifrovány veřejným klíčem, lze dešifrovat pouze soukromým klíčem
- Elektronický podpis
- - rychlost
- - výpočetně náročné
#### Digitální certifikát
- balíček identifikující uživatele nebo server
- obsahuje informace
- obsahuje veřejný klíč
### Maildir a MBOX
- formáty pro uložení email zpráv