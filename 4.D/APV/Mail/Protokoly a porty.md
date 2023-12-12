# Protokoly a porty
---
## Porty
### SMPT
- 520 nezabezpečená
- 465 zabezpečená SSL
- 587 zabezpečená TLS
### POP3 
- 110 nezabezpečený
- 995 zabezpečený SSL
- 110 zabezpečený TLS
### IMAP4
- 143 neza.
- 993 zab. SSL
- 143 zab. TLS
---
## SSL
- *secure sockets layer*
- šifrování a auth.
- HTTPS
- mezi TCP/IP a HTTP
### SSL certifikáty
- online obchodování
## TLS 
- *transport layer security*
- minimální rozdíl s SSL
---
## Digitální ID
- pomáhá potvrdit identitu odesílatele a příjemce mailu
- chrání zprávy přidáním digitální podpis
## Digitální vs. elektronický podpis
- digitální je v USA
- elektronický v EU
- drobné rozdíly
## Co je to elektronický podpis
- nedá se zfalšovat
- obdoba klasického podpisu převedena do elekt. podoby
### princip fungování
- velké číslo (1024 nebo 2048 bitů) => neprolomitelné hrubou silou
- Hashovací funkce
## získání podpisu
- porgramem pro vytváření a ověřování podpisu -> program vygeneruje dvojici soukromého a veřejného klíče -> veřejný klíč se předloží CA -> CA vystaví certifikát