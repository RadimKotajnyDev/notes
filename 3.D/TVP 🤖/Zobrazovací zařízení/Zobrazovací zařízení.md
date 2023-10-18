# Zobrazovací zařízení
## Pixel
- bod celkového obrazu s definovanou polohou (x, y) s přesně danými barevnými vlastnostmi
- 3 SUBpixely - RGB
-  Subpix - SW. definován rozsahem 0-255  musí se převést na fyzikální parametr - dle technologie monitoru
- Na základě intenzity záření jednotlivých SUBpixelů získá PIXEL požadovanou barvu
- A – Jasná složka PIXELU jako Celku
## CRT Technologie
- Cathode Ray Tube – trubice s katodovým zářením - velká "elektronka"
- Obraz vzniká předáním energie proudu e- (elektron) do SUBpixelu
- SUBpixel tvořen chem. látkou – **Luminofor** – která při dodání energie začne vyzařovat  viditelné světlo
	- dle dodané energie pak SUBpixel září přesně definovanou intenzitou
	- Luminofor po dodání energie září v řádech ms – mohou mít pohyblivý obraz - v dalším čase mohou změnit parametry záření SUBpixelu.
	- ![[Pasted image 20230322133534.png]]
## LCD Technologie
- Liquid Crystal Display => zobrazovací zařízení na principů tekutých krystalů
- původně v přenosné elektronice - displeje kalkulaček, dig. hodinek, budíků... většinou černobílé, segmentové displeje
- **Tekutý krystal**
	- kapalině podobná látka, která obsahuje částice - krystaly
	- pokud krystaly volně plavou - jsou neuspořádané
	- lze je uspořádat = natočit krystaly v jednom směru -> mohou blokovat průchod světla
	- krystaly mají tvar stejně dlouhých tyčinek
	- natočení krystalů se řídí napájením elektrod, mezi kterými je tekutina s krystaly
- LCD subpixel Zelený
- //TODO: dopsat polarizační filtr (obrázek)
- Tvar propouštěného kmitání se vybírá natočením filtru
- V LCD se používají 2 filtry navzájem otočený o 90 stupnu
## Parametry LCD
- velikost: dle úhlopříčky v palcích
- poměr stran: 4:3, 16:9 atd.
- rozlišení - FHD
## Doba odezvy - ms
- čas potřebný na změnu PIX z červené na bílou a zpět
## Gammit
- % z sRGB, %AdobeRGB
- definuje 
## LCD
### VA - Vertical Alignment
- Dobré pozorovací úhly (horší, než IPS)
- lepší zobrazení černé barvy než IPS
### QLED
- Quantum Pot LED
- speciální vrstva miniaturních teček
- vylepšení:
	- pozorovacích úhlů
	- zobrazení černé barvy
	- RGB
## <u>Kontrast</u>
- poměr svítivosti bílého a černého bodu obrazu
### Dynamický kontrast
- v závislosti na čase mění kontrast
- závisí na funkcí vypínání části podsvícení
- podsvícení rozděleno na matrici čtvercových oblastí, které lze vypínat
## <u>Podsvícení</u>
### LED
- bílé barvy
- 1) hranové podsvícení
	- ![[Snímek obrazovky 2023-03-31 v 12.58.34.jpg]]
- 2) matricové - skupiny LED - matrice
	- 1 segment se vypíná/zapíná dle rozboru obrazu -> převažují černá v ploše segmentu = vypnutí podsvícení
## Jas
- maximální svit bílé v obrazovém bodu (PIX)
- může být regulován na základě okolního světla
## OLED
- *Organic Light Emitting Diode*
- Subpixel
	- vrstva organické látky a průhledná anoda
	- nepotřebuje podsvícení ––> je sám zdrojem světla (RGB)
	- => výborné pozorovací úhly, nízká spotřeba, možnost pružného displeje, věrné barvy ––> široký gamut
- Nevýhody - kratší životnost organických vrstev -> zvláště BLUE
	- náchylnost k "vypálení" statického obrazu
## Digitální projektory
![[Pasted image 20230422210609.png]]