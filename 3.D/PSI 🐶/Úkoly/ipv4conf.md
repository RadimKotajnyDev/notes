# IPv4 konfigurace a výpočty
## 1) IP a maska
- IPv4 Address => 192.168.10.185
    -  Subnet Mask => 255.255.255.0
    -  DHCP => 192.168.10.1
    - Výchozí brána (default gateway) => 192.168.10.1 
        - (=> což je adresa routeru, přes který počítač komunikuje s internetem.)
    - Doba pronájmu IP adresy se nazývá DHCP lease a v mém případě je tato adresa platná do 21. března 2023 20:17:28.
    - Adresa DNS serveru => 78.157.167.7 a 78.157.167.57. 
        - (=> DNS server slouží k překladu názvů domén na IP adresy a umožňuje počítači komunikovat se servery pomocí názvů místo IP adres.)

## 2)
- Adresa byla uzlu přidělena pomocí DHCP protokolu, což znamená, že router přiřadil počítači tuto IP adresu automaticky.

## 3) 
- IP adresa v DEC formátu je 192.168.10.185 a maska sítě je 255.255.255.0.
- IP adresa v BIN formátu: 11000000 10101000 00001010 10111001
- Maska sítě v BIN formátu: 11111111 11111111 11111111 00000000
## 4) Broadcastová adresa
 - 192.168.10.255 v DEC
- 11000000 10101000 00001010 11111111 v BIN
## 5) 
- Jedna možnost masky sítě, která umožní vytvořit více než 4 podsítě a splňuje požadavky, je 255.255.255.192.
## 6)
- Adresa 14. podsítě a 8. uzlu v této podsíti v BIN formátu je: 00001110 00000010 00001010 00001000.

## 7)
- Adresa 14. podsítě a 8. uzlu v této podsíti v DEC formátu je: 192.168.10.136.

## 8)
- Broadcastová adresa 10. podsítě v BIN formátu je: 00001010 00001010 00001000 01111111.

## 9)
- Broadcastová adresa 10. podsítě v DEC formátu je: 10.10.8.127.

## 10) V příloze.