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
  Ausgabe und Status des Dienstes anzeigen
- `sudo systemctl start NAME.service`:  
  Dienst starten
- `sudo systemctl list-timers --all`:  
  Alle Timer anzeigen

## Kommandozeilenhilfen
- `!l`:  
  Run last command starting with an l
- `grep`:  
  searching in lines
- `wc`:  
  Word Count  
  `-l`: cound lines
- `chsh -s /bin/bash`:  
  change shell to bash shell