# Netzwerk
## SSH
- `ssh-keygen`:  
  SSH-Key erstellen
- `ssh-copy-id  user@hostname`:  
  Key auf entfernete Maschine kopieren
  `-i identityFile`: Neuen Key für entfernte Maschine erstellen

### Dateien übertragen
- `scp FROM TO`/`scp user@website.com:/path/on/server path/to/download`:  
  Dateien mit Zugriffsrechten des Nutzers auf bestimmten Pfad zu bestimmten Pfad kopieren

## Windows
Zeige alle Netzwerke mit Verbindungsstärke an:  
`netsh wlan show all | more`

## Linux
### Konfiguration
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

### Scan
- `nmap -sn 192.168.71.28-49`:  
  Erreichbare IP-Adressen in dem angegebenen Adressbereich  
  `-sn`: no port scan
  `-PU`: port list (UDP Ping)
- `sudo arp-scan --interface=ens160 --localnet`:  
  Nach IP-Adressen & MAC-Adressen sowie die Hersteller des Interfaces