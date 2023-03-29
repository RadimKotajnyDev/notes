---
# Proměnné a zaměnitelné parametry
proměnné jsou uloženy v dávkové části příkazového procesoru - proměnné prostředí
uložené jako text
systémové a uživatelské
systémové nastavuje operační systém a obsahují údaje o takzvané konfiguraci prostředí
uživatelské proměnné vytvářejí a používají administrátoři hlavně v dávkových souborech

## práce s proměnnými prostředí
`SET` – bez parametrů vypíše proměnné prostředí
`SET jmeno_promenne=hodnota`
`SET /P promenna=vyzva` (výzva uživatele, použije se v .bat souborech)
`SET /A 1 + 1` (vyčísluje aritmetické výrazy)

## přístup k hodnotě proměnné
`%jmeno_promenne%` - hodnota proměnné

## PATH
obsahuje všechny cesty kde hledají programy pro spuštění
proto při spouštění nemusíme psát celé cesty

## Zaměnitelné parametry
- slouží k předávání hodnot do dávkových souborů pomocí parametrů při spuštění
	`ECHO OFF`
	`ECHO %0`
	`ECHO %1`
	`ECHO %2`
	`ECHO %3`
	`ECHO %*`
