# IPA

## Grobbeschrieb

### Titel

Keycloak/OpenID Connect Integration Cryptopus

### Beschreibung

Erweiterung des Open Source Pasword Manager Cryptopus für Single-Sign-On via Keycloak/OpenID Connect

## Detailbeschrieb

### Titel der Arbeit

Keycloak/OpenID Connect Integration Cryptopus

### Ausgangslage

Cryptopus ist eine von Puzzle entwickelte Open Source Lösung für die Verwaltung vertrauter Daten wie Benutzernamen, Passwörtern sowie Dateien. Die verwalteten Zugangsdaten werden verschlüsselt in der Datenbank abgelegt. Beliebig viele Benutzer können sich den Zugriff auf die einzelnen Teams in welchen die Daten organisiert sind teilen.

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript mit Ajax verwendet. 

Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/puzzle/cryptopus

### Detailierte Aufgabenstellung

...

#### Nicht funktionale Anforderungen
* Zusammentragen/Beschreiben der heute realisierten Features
* Migrationskonzept für die Umstellung von der LDAP Authentifizierung auf SSO mit Keycloak

#### Funktionale Anforderungen
* API-Accounts können sich immer noch direkt an Cryptopus ohne Keycloak authentifizieren
* Es wird keine Login-Maske in Cryptopus angezeigt falls die Authentifizierung via Keycloak/OpenID erfolgt
* Die Login-Maske kann von einer lokalen IP aufgerufen werden um sich per root einzuloggen. (Fallback Login wenn Keycloak nicht mehr verfügbar)
* Login via Root generell nur noch von einer privaten IP aus

### Individuelle Beurteilungskriterien

### Mittel und Methoden

### Vorkenntnisse

### Vorarbeiten

### Neue Lerninhalte

### Arbeiten in den letzten 6 Monaten

### Bemerkungen
