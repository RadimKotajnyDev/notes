# Disková vyrovnávací paměť (Drive Cache)

- důvodem použití je, že CPU a RAM přesouvají data podstatně rychleji, než je přenosová rychlost pevných disků.
- principem je, že často používaná data se ponechávají operační paměti, aby se vyloučilo opakované fyzické čtení z disku. Toto je vyrovnávací paměť pro čtení.
- Data se nezapisují přímo na disk, ale nechávají se v RAM po zaplnění paměti nebo uplynutí času OS provede fyz. zápis na disk
	- Ten probíhá tak, aby se minimalizovaly pohyby raménka s hlavami HDD
- Zpožděný zápis je důvodem proč musíme korektně vypínat ty OS, které ho používají  
- Vyrovnávací paměť bývá realizována softwarově jako součást OS.
- Je taky realizována hardwarově a je součásti moderních pevných disků.
- Důvodem použití -,,- přímo v disku je to, že rozhraní pevného disku, např. SATA je podstatně rychlejší, než Fyz. zápis na plotny
# Algoritmus LRU (nepovinné)
-