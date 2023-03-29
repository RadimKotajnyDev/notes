---

1. Vytvořte .bat, který vypíše hlášení:
	- "Na počítači (doplnit jméno PC) je příhlášen uživatel (doplnit jméno uživatele)"
	- doplnění použité dle sys. proměnných
	`echo off`
	`cls`
		`echo Na pocitaci %COMPUTERNAME% je prihlasen uzivatel %USERNAME%.`
		`echo.`
		`pause`
2. Vytvořte .bat pro zkopírování všech dokumentů wordu ze složky dokumenty přihlášeného uživatele na přenosný disk do složky záloha.
	- kopírování do E: 