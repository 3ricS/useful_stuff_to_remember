# Netzwerk
## SSH
- `ssh-keygen`:  
  SSH-Key erstellen
- `ssh-copy-id  user@hostname`:  
  Key auf entfernete Maschine kopieren
  `-i identityFile`: Neuen Key für entfernte Maschine erstellen

## Dateien übertragen
- `scp FROM TO`/`scp user@website.com:/path/on/server path/to/download`:  
  Dateien mit Zugriffsrechten des Nutzers auf bestimmten Pfad zu bestimmten Pfad kopieren

## IP-Adressen
- `ipcalc 192.168.0.1/29`:
  Berechne Adresse, Subnetzmaske, etc. für dieses Netz

## Windows
Zeige alle Netzwerke mit Verbindungsstärke an:  
`netsh wlan show all | more`

## Konfiguration
- `ip a`:  
  Netzwerkschnittstellen anzeigen
- `ip link show`:  
  Verbundene Netzwerkgeräte anzeigen

Netzwerkkonigurationsdatei unter `/etc/netplan/` (`.yaml`-Datei):  
- `netplan try`:  
  Konfigurationsdatei ausprobieren

- `netplan apply`:  
  Konfigurationsdatei neu laden und scharfschalten (Achtung: auch fehlerhafte Config-Dateien werden genutzt)

- `sudo ip link set ens192 address 02:f1:af:fe:af:fe`:  
  MAC-Adresse der Netzwerkschnittstelle `ens192` ändern (kein Neustart erforderlich)
  
- `macchanger -r ens192`:  
  Ändern der MAC-Adresse mit Programm `macchanger`

## DHCP
- `sudo dhclient -r eth0 && sudo dhclient eth0`:  
  Neue IP vom DHCP-Server anfordern. Alte IP releasen und neue anfordern.
- DHCP-Penetration Tool: `dhcpig`  
  Wegnehmen aller IPs -> Windows-Geräte offline
- Alle IP-leases löschen und neue IP bekommen:  
  `sudo dhclient -r ens192; sudo ip link set ens192 address 02:F1:AF:$[RANDOM%10]$[RANDOM%10]:$[RANDOM%10]$[RANDOM%10]:$[RANDOM%10]$[RANDOM%10]; sudo rm /var/lib/dhcp/dhclient.leases; sudo dhclient ens192`

## ARP
- ARP-Cache anschauen:  
  `arp -e`
- ARP-Cache löschen:  
  `sudo ip -s -s neigh flush all`

## Scan
- `nmap -sn 192.168.71.28-49`:  
  Erreichbare IP-Adressen in dem angegebenen Adressbereich  
  `-sn`: no port scan
  `-PU`: port list (UDP Ping)
  `-O`: Betriebssystemerkennung aktiviern
- `sudo arp-scan --interface=ens160 --localnet`:  
  Nach IP-Adressen & MAC-Adressen sowie die Hersteller des Interfaces

## Brandbreitenmessung
- `iperf -c <host> -e -i 1`:  
  Bandbreitenmessung zum iperf-Server `<host>`
