---
-   proměnné jsou uloženy dalkové části příkazového procesoru také se jim říká proměnné prostředí
-   jsou uloženy jako text
-   ve formátu název proměné a hodnota
-   systémové a uživatelské
-   nadstavuje samotný operační system a obsahují údaje o takzvané konzultaci prostředí
-   uživatelské proměnné vytvařejí a používají administrátoři hlavně v tak zvaně dávkových souborech.

### Práce s proměnými prostředí

-   SET(enter) - vypíše proměnné prostředí
-   přístup k hodnotě proměné na příkazovém řádku nebo k hodnotě souboru = %jmeno_promenn%
-   %PATH% všechny cesty pro spuštění proto při spouštění nemusíme psát plné cesty
-   SET /p promena=vyzva - slouží pro vstup z klávesnice, používá se v dávkových souborech
-   SET /A 1 + 1 - vyčísluje aritmetické výrazy
-   ECHO (enter) - vypíše aktuální nastavení ozvěny
-   ECHO OFF - vypne ozvěnu
-   ECHO. - vypíšse prázdný řádek
    -   příkaz echo můžeme použítvat zaměnné a proměnné parametry
    -   používá se v dávkových souborech

## Zaměnitelné parametry

-   Slouží k předávání hodnot dodávkovým souborům pomocí parametru při spuštění

`//Vypíše parametry

@ECHO OFF
ECHO %0
ECHO %1 //vypíše chtěný parametr
ECHO %2
ECHO %3 ECHO %* //vypíše všechny parametry`