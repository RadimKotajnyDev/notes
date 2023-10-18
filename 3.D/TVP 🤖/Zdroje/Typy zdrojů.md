#zdroj 
---
## Vysokofrekvenční Transformátor

-   Galvanicky oddělení primáru(vstupu) části zdroje od sekundáru (výstupní)
-   Výstupní filtr - odstranění případných rušivých signálu

### Nevýhody

-   vf rušivé sig do rozvondé sítě

## **Typy pc zdrojů**

1.  AT
    1.  Advanced Technology
    2.  HW vypínač, +12V, -12V, 5V
2.  ATX
    1.  Obsahuje spec. sig. pro komunikaci zdroj <——> MB ⇒ SW zap/vyp

## Parametry Zdroju

Tolerance Napětí:

-   +,- 5%
-   pro 12V je to +,- 10%

**Účinnost**

-   mění se v závislosti na zátěži zdroje
    
-   např
    
    1.  zátěž 10% —> účinnost 65%
    2.  -||- 50% —> —||— 80%
    3.  -||- 80% —> —||— 70%
-   Certifikace zdroju (gold, platina, bronze)
    

## Ochranné obvody

1.  Udržení výstupního nap. při výpadku (mikro sekundy)
    1.  -kondenzátory
2.  Ochranné obv. sekundáru nap.
    1.  přepěťová ochrana
    2.  Komparátory porovnávají skutečné nap. s výstupním
    3.  při překročení určeného může odpojit zátěž (cpu, ssd,…)
    4.  Proudová ochrana
        1.  jednotlivé větve mají sve max
        2.  odpojení zátěže z přechodu
3.  Protizkratová ochrana
    1.  zdroj před připojením výstupního np. na zátěž provede self-control