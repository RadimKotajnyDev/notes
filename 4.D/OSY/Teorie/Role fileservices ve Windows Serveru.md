# Role fileservices ve Windows Serveru
- obsahují více služeb role
- tyto služby / role můžeme rozdělit do
	- Souborový server (File server)
	- podpora služby síťových uložišť
	- podpora distribuovaného souborového systému
## File server
- sdílení souborů a složek v lokální síti
- na klientovi se sdílená složka ze serveru jeví stejně jako by to byla složka lokální
## BranchCache for Network Files
- pobočková vyrovnávací paměť pro síťové soubory
## File Server Resource Manager
- umí omezovat uživatele
- kvóty na úroveň složky
- lze nastavit na úroveň uživatele a složky
- řízení podle přípony souboru (např. zákaz stahování videa)
---
- umí monitorovat využití serveru jednotlivými uživateli
- umí vytvářet přehledy pro správce
- umí správce případně upozorňovat na problémy emailem
---
## Network File Server
- je to unixový a linuxový subserver / služba
- umožňuje sdílení souborů typicky pro linuxové a unixové klienty
- Windows server s touto službou nabízí své složky a soubory ke sdílení unixovým / linuxovým klientům protokolem NFS
---
## Data Deduplication
- služba slouží k odstraňování duplicitních výskytů stejných souborů v souborovém systému Windows Serveru
## DFS Namespaces
- *distributed file system*
- podpora pojmenování souborů
## DFS Replication
- zrcadlení
- automatické replikování souborů na jiný server
## iSCSI
- protokol v síti SAN (*Storage Area Network*)
- pracuje na úrovni bloků (ne na úrovni souboru)
