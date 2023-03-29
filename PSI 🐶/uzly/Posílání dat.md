## Posílání dat:

1.  v jedno čase možná komunikace pouze mezi 2 uzly
2.  V jednom čase může vyslat do busu signál pouze jeden uzel
3.  V speciálních případech přijímají všechny uzly na BUS —> BROADCAST = všesměrové vysílaní
4.  Řeší Algoritmus přístup k médiu (např. = síť kabel)

### Výhody:

-   snadné připojení U
-   — || — BROADCAST
-   ¨Výpadek U neohrozí celou síť

### Nevýhody:

1.  -   ↑Počet uzlů —> ↑pravděpodobnost
    -   tzv. KOLIZE v BUS —>
    -   v 1. okamžik potřebuje vyslat více U
2.  1.  V 1 —||— je v síti pouze 1 informace

> u = uzel

# 3. Ring - KRUH

![[kruh.png]]
## Posílání Dat:

1.  Pouze jedním definovaným směrem
2.  Jsou přeposílány mezi lehkými U
3.  Pouze adresát (cílový U) si data přebírá

### Řešení kolizí

-   Existuje pouze 1TOKEN —> jednoduché právo využití sítě(vysílání do sítě)

### Výhody -

-   Signál zesílen průchodem U
-   Nevznikají kolize

### Nevýhody

Výpadek U = pád sítě