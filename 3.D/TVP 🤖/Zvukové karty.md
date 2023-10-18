# Zvukové karty
- Převod binární informace z CPU na analog. výstup (i digitál)
- výstupy digitální mohou být zpracovávány exter. zařízeními
- Výstupy analog. mohou být
	- ponechány – sluchátka
	- zesíleny – výstup audia (reproduktory)
- slouží i k opačnému převodu – analog. sig. (z mikrofonu) převede na digitální.
	- analog. vstup je možné skrz zvuk. kartu dále zpracovat v bin. podobě
- Jádrem je zvukový čip
	- integrován na MB – levnějšís
	- jako PCI-E karta – kvalitnější
	- externí zvuk karty (FireWire port)
## Barevné značení analog. vstupů
- Pink – analog. (mikrofon)
- Light Blue – analog. (nemusí být vždy)
- Green – analog. (sluchátka)
- Orange – 
![[Pasted image 20230308135328.png]]
## FM syntéza
- základní zvuk. průběhy – sinus, pila, trojúhelník
- signály jsou tvořeny matematickým skládáním průběhů
- tóny mohou být čisté – sin bez modulace
- nebo nosič + modulátor
- modulátor je lib. signál, jeho tvar má vliv na rychlost kmitání nosiče
- čím větší je amplituda modulátoru –> tím vyšší je frekvence nosiče –> frekvenční modulace tedy FM
## Wavetable syntéza
- využívá zvuky skutečných nástrojů nahraných a uloženích v EPROM
- každý zvuk a jeho výška má své číslo a spolu se vzorkem organizován v EPROM
- Paleta tónů nástroje je docílena změnou rychlost