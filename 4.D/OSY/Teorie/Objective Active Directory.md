# Objective Active Directory
- **Organizational unit (OU)**
- object funguje jako složka tak, že může obsahovat další objekty včetně dalších OU
- tato struktura obvykle funguje idk organizační strukturu firmy / instituce... kde Active Directory zavádíme
- OU neslouží jako nositel oprávnění a práv
- Do OU umisťujeme objekty uživatel
--------------------------------------------------------------------
## Object počítač
- vzniká přidáním daného počítače do domény
- když počítač není v doméně (nemá svůj obraz v Active Directory), tak se na něm nedá přihlásit na doménové účty
- slouží k zabezpečení
## Object uživatel
- vzniká vytvořením uživatelského účtu
- obsahuje informace o uživateli
## Object skupina
- skupina (group) (doménové skupiny)
	- Distribuční (Exchange server)
	- Zabezpečovací
		- lokální - Doména
		- globální - LES
		- univerzální
- skupiny vnořené v Active Directory se nazývají doménové
- skupiny distribuční souvisí s Exchange serverem
	- Jsou to **distribuční seznamy elektronické pošty**
- <u>skupiny zabezpečovací slouží jako nositelé NTFS oprávnění a práv </u>
- tyto skupiny se liší rozsahem platnosti
- všichni členové doménových skupin se po přihlášení na počítač, který je v doméně je členem  a zároveň odpovídajících místních skupin v počítači. příklad:
	- DOMAIN USERS –> USERS
	- DOMAIN ADMINISTRATORS –> ADMINISTRATORS
## GPO – *Group Policy Object*
- Objekt skupinových politik
- Slouží k nastavení -,,-
- připojuje se na organizační jednotku (OU)
- slouží k centrálnímu a vzdálenému nastavování OS Windows na počítačích v doméně