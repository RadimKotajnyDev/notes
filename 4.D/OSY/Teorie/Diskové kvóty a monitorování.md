# Diskové kvóty a monitorování
--- 
- disková kvóty je nástroj pro omezení místa na logickém disku pro konkrétní uživatele
- podpora kvót je zabudována v souborovém sys. NTFS
- kvóta se počítá podle vlastníka souboru
## Základní řešení kvót ve Windows
- se počítá na celý logický disk podle vlastníka souboru
- správce může definovat dva druhy kvót
	- měkká kvóta => upozorní na překročení, ale neblokuje
	- tvrdá kvóta => blokuje ukládání
- dobrá praxe je, že měkkou kvótu nastavujeme na 80-90% tvrdé kvóty
	- Na serveru je vhodné mít domácí disky uživatelů na samostatném logickém disku a tam aplikovat kvóty
- Když potřebujeme kvóty nastavovat na úroveň složky je třeba nainstalovat roli **File Server Resource Manager (FSRM)**