# Branch prediction
- do speciální paměti se ukládá inf. o instrukcích, které v minulosti (ms) vykonaly skok
- další výskyt shodných instrukcí => předpoklad skok
- předpověď nevychází vždy
- správné předpovědi převažují –> celkové urychlení vykonávání úst.
## Spekulativní vykonávání instrukcí
- navazuje, spolupracuje s BRANCH PREDICTION
- zpracovávání instrukcí následujících po větvení –> v době, kdy větvení ještě nenastalo
- bylo-li B.P správné –> urychlení práce | BP nesprávné - anulování výsledků, práce CPU navíc (= zpomalí)
