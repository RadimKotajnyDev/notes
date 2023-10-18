# konfigurace sítě a firewallu
- na každém síťovém připojení lze konfigurovat síťové protokoly, síťové služby případně doporučuje se nepoužívané protokoly vypnout
- na tlačítku konfigurovat lze nastavit hw vlastnosti síťové karty
	- dú podívat
## základní nastavení firewallu
- odvíjí se od tzv. umístění v síti nebo-li síťového profilu
	- na windows serveru se profily rozlišují
		- profil veřejný
			- nedá se pingnout
			- v praxi se volí, když síťové rozhraní je připojeno na veřejnou IP
		- profil privátní (podniková síť)
			- není ochráněn firewallem
			- jen důvěryhodným počítačům na jedné síti
		- profil doménový
			- používá se na doménovém řadiči a na počítači připojeném v doméně
			- zpřístupní síťové služby řadiče domény
- firewall ve výchozím nastavení neomezuje odchozí provoz ze serveru.
- filtrování provozu lze upřesnit v pokročilém nastavení firewallu
## možnosti filtrování v provozu
- IP adresa (zdrojová, cílová)