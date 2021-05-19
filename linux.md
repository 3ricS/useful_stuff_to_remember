# Linux

## Betriebssysteminformationen
- `uname -a`:  
  Betriebssystemversion anzeigen
- `dmesg`:  
  Bootinformationen

## Benutzerverwaltung
- `sudo adduser NAME sudo`:  
  Nutzer mit Adminrechten anlegen

## Services
Dienst unter `/etc/systemd/system` als `.service`-Datei anlegen ([Template](https://wiki.ubuntuusers.de/systemd/Service_Units/))
- `sudo systemctl daemon-reload`:  
  Dienste neuladen
- `sudo systemctl status NAME.service`:  
  Status des Dienstes anzeigen
- `sudo systemctl start NAME.service`:  
  Dienst starten

## Kommandozeilenhilfen
- `grep`:  
  Heraussuchen vom Zeilen
- `wc`:  
  Word Count  
  `-l`: Zeilen zählen