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
#### kódování
- quoted printable
	- kóduje jen znaky, které nejsou v ASCII tabulce
- Base64
	- překóduje všechny znaky včetně sedmibitových
#### šifrování
- asymetrická kryptografie