# PostgreSQL

- `sudo -u postgres psql [-U username] [-h hostname] [dbname]`:  
  Anmelden (Aufsühren von `psql` mit Unix-Nutzer `postgres`)

  Sinnvolle Angaben:  
  - Auf welchem Rechner/Server befindet sich das DBMS (falls nicht lokal): `-h hostname`
  - Als welcher Datenbankbenutzer möchte ich mich anmelden: `-U`
    Standardmäßig bei PostgreSQL Nutzer `postgres`
  - Passwort
  - Mit welcher Datenbank möchte ich mich verbinden: Angabe hinter `psql`, hier `DATABASENAME`
  
  Falls Fehler `psql: error: FATAL: Peer authentication faild for user "username"`: [hier](https://stackoverflow.com/questions/18664074/getting-error-peer-authentication-failed-for-user-postgres-when-trying-to-ge)
  
- `\l`:  
  alle Datenbanken anzeigen

## Hilfe
- `\?`:  
  Hilfe über Befehle
- `\h ALTER TABLE`:  
  Hinweise zu `ALTER TABLE` anzeigen lassen

## Benutzerverwaltung
- `CREATE USER user CREATEDB PASSWORD 'pass'`:  
  Anlegen eines Nutzers  
  Berechtigungen: `CREATEDB`
- `\du`:  
  Rollen anzeigen
- `ALTER USER user role`:  
  Rollen ändern  
  Mögliche Berechtigungen `role`: `Superuser`, `CREATEROLE`, `CREATEDB`, `Replication`, `Bypass RLS`

## SQL-Skripte
Endung `.sql` mit SQL-Anweisungen  
Danach ist die Datenbank in einem definierten Zustand

- Skript ausführen:  
  In PostgreSQL-Shell: `\i 'skriptname.sql'`
  In Ubuntu Shell:  `psql -U username < path/to/skript.sql`

