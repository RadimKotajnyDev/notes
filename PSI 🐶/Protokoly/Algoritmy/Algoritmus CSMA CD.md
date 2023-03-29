# Algoritmus CSMA/CD
- dělí se na 
	- CSMA - *Carrier sense Media Access*
	- CD - *Collision Detection*
- CSMA 
	- CS - "následování" (měření) nosného signálu
	- MA - *Media Access* - přístup k přenosovému médiu
1) Zjišťuje, zda je na médiu (kabelu) volno
2) Pokud je "volno" -> vyšle svá data ve formě nějakého druhu el.-mag. vlnění (el. signál) do média.
	- neřeší kolizi = dva nebo více uzlů začne vysílat současně => znehodnocení informace všech vysílajících
- K řešení kolizí slouží <u><b>CD</b></u> (nefunguje samostatně, jen spolu s CSMA)

## Činnost CD
 1) naslouchá, je-li vše OK
 2) Nastane-li kolize, CD vyšel do média signál JAM (nastane smíchání signálů)
 - Reakce vysílacích uzlů na JAM -> 
	 - DESYNCHRONIZACE ->
- výpočet <u>náhodné hodnoty času</u> (ms, ns)(NH)
- po uplynutí NG se pokouší o znovu vysílaní
- Pozn. - Typ řízení vysílání na základě náhodného čísla - STOCHASTICKÝ
- Použití - Ethernet, BUS, Wi-Fi (modifikovaná forma)
- ![[Snímek obrazovky 2022-11-30 v 9.31.27.jpg]]