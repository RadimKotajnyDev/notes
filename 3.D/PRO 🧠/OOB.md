# Úvod do objektově orientovaného programování (OOP)

Jedná se o způsob programování

Dané způsoby:

1.  Strojovým kódem (pomocí přepínačů - složité)
2.  Jazyk symbolických instrukcí = assembler (potřeba překladače - lehčí - pro nás čitelné díky anglický instrukcím které se následně překládají do strojového kódu)
3.  Jazyk vysoké úrovně = Fortran ( pro výpočet matematických operací a vzorců = možné dělat složitější programy)
4.  Vyšší strukturovací programovací jazyky = ALGOL, COBOL, BASIC, PASCAL, C,…. (Strukturové bloky programu, minimalizují se skoky goto, jednoduché pro používání a vytváření složitějších programů)
5.  OOP = Python, PHP, Java, C++, C# (Přehlednější pro větší kódy, kód se píše vstříc programátora)

## OOP

-   Objekt - náhrada objektu z reality
    
    -   Data - Uvádějí vlastnosti objektu
        -   atribut = pojmenování vlastnosti objektu
    -   Metody - Udávají chování objektu
-   Zapouzdření
    
    -   mechanismus, který svazuje dohromady kód a data a zabezpečuje je před vnějšíma zásahy
    
![[oob.png]]
    
    -   Data jsou uvnitř metoy
    ![[oob2.png]]

    
    -   Výhody
        -   zatajování informací
        -   Modulovat
            -   každý program lze udrožovat nezávisle na jiném objektu
    -   Realizace
        -   Srytí všech implementačních detailů
        -   Nastavení přéstupu k Datům pouze pomocí speciálních metod
        -   Používání rozhraní pro vzájemnou komunikaci objektů
        -   Opatrně využívání dědičnosti a chráneného přístupu k datům které může použít zapouzdření
-   Polymorfismus
    
-   Dědičnost