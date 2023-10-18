---
> BCD = 8421 binery coded to decimal = zápis dekadickéhého čísla ve dvojkové soustavě, tak že každou číslici zapíšeme ve dvojkové soustavě pomocí 4 bitu. 128(decimal) = |0001|0010|1000(bcd) = 10000000 (b) 1 2 8 používá se při 4bitovém spracování čísel. a to bylo ve 4 bitových mikroporcesorech také se BCD používá V Hardwarových řešeních při potřebě přímé návaznosti na decimalní soustavu

# Kódování záporných čísel ve dvojkové soustavě

-   Kód Přímý
    
    65 D
    
    0
    
    1
    
    0
    
    0
    
    0
    
    0
    
    0
    
    1
    
    B
    
    -65 D
    
    1
    
    1
    
    0
    
    0
    
    0
    
    0
    
    0
    
    1
    
    B
    
    -   ABS. hodnota čísla
    -   N (náleží) < -127, 127>
    -   -0 existuje
    -   První bit je značkový bit
        -   0-kladné
        -   1-mínus
-   Kód inverzní ( = jedničkový doplněk)
    
    65 D
    
    0
    
    1
    
    0
    
    0
    
    0
    
    0
    
    0
    
    1
    
    B
    
    -65 D
    
    1
    
    0
    
    1
    
    1
    
    1
    
    1
    
    1
    
    0
    
    B
    
    -   Invertuji všechny bity
        -   N (náleží) < -127, 127>
        -   -0 = existuje
-   Kód doplňkový (=dvojkový doplněk)
    
    65 D
    
    0
    
    1
    
    0
    
    0
    
    0
    
    0
    
    0
    
    1
    
    B
    
    -65 D inv. kód
    
    1
    
    0
    
    1
    
    1
    
    1
    
    1
    
    1
    
    0
    
    B
    
    ```
                                                            +         1
    ```
    
    -65D doplň.kód
    
    1
    
    0
    
    1
    
    1
    
    1
    
    1
    
    1
    
    1
    
    B
    
    -   záporné číslo má 1.
    -   V doplňkovém kódu sečtením čísla a čísla k němu opačnému dostaneme číslo 0
    -   N (náleží) < -128, 127>
    -   -0 neexistuje. protože kdybychom chtěli -0 zakódovat dostaneme kladnou 0
-   Kód s posunutou nulou
    
    -   záporná čísla vyjadřují pomocí čísel kladných a nejmenší záporné číslo se vyjádří číslem 0 - tím je dáno posunutí. a tím pádem číselný rozsah si můžeme zvolit. nejobvyklejší posunutí je o +128 N(náleží) < -128, 127>
        
        -   ve výpočetní technice se pro zobrazení celých čísel používá doplňkový kód číselný rozsah závisí na počtu baitu (char, int 16 32 64)
        -   se zápornými čísly pracuje transpartně při sčítání a odčítání
        
        Číslo k zaokrouhlení
        
        Číslo s posunutím
        
        -128
        
        0
        
        0
        
        +128
        
        +127
        
        +255
        
        -65
        
        65
        
        _
        
        0
        
        0
        
        0
        
        0
        
        0
        
        0
        
        0
        
        0
        
        1
        
        0
        
        0
        
        0
        
        0
        
        0
        
        0
        
        0
        
        1
        
        1
        
        1
        
        1
        
        1
        
        1
        
        1
        
        1
        
        0
        
        0
        
        1
        
        1
        
        1
        
        1
        
        1
        
        1