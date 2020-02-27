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

Puzzle betreibt seit ein bis zwei Jahren einen Keycloak Server um Single-Sign-On (SSO) für die internen Web-Dienste zu ermöglichen. Auch für Cryptopus soll es künftig möglich sein sich über SSO anzumelden ohne das der Benutzer jedesmal seine Credentials eingeben muss. Ziel dieser IPA ist diese Integration zu implementieren. 
Die sensitiven Daten werden in Cryptopus verschlüsselt in der Datenbank abgelegt. Bei der heutigen Implementation ist Cryptopus auf das Benutzer-Passwort angewiesen um die RSA Private Keys zu entschlüsseln. 
Vorgängig wurde bereits konzipiert wie sich dieses Problem lösen lässt. In Keycloak wird ein spezielles Benutzer-Attribut konfiguriert in welchem eine entsprechende Passphrase gespeichert wird. 
Sylvain wird einige vorbereitenden Arbeiten als Basis für diese IPA erledigen da die Komplexität und der Aufwand den Rahmen einer IPA sonst sprengen würden.

#### Nicht funktionale Anforderungen
* Zusammentragen/Beschreiben der heute realisierten Features
* Migrationskonzept für die Umstellung von der LDAP Authentifizierung auf SSO mit Keycloak

#### Funktionale Anforderungen
* Falls der Benutzer auf Cryptopus zugreift ohne das er sich vorher am Keycloak Server authentifiziert hat, wird er auf die Login-Maske des Keycloak Servers umgeleitet
* 
* API-Accounts können sich immer noch direkt an Cryptopus für den Zugriff auf /api ohne Keycloak authentifizieren
* Es wird keine Login-Maske in Cryptopus angezeigt falls die Authentifizierung via Keycloak/OpenID erfolgt
* Die Login-Maske kann von einer lokalen IP aufgerufen werden um sich per root einzuloggen. (Fallback Login wenn Keycloak nicht mehr verfügbar)

### Individuelle Beurteilungskriterien
* 235 - Entwurf mit UML
* 166 - Lesbarer Code
* 162 - SW-Architektur
* 170 - Systematik Lösung
* 124 - Testfälle (Programmierung)
* 192 - IT-Sicherheitskriterien
* 230 - Migration

### Mittel und Methoden

### Vorkenntnisse

### Vorarbeiten
* Aufbau der benötigten lokalen Entwicklungs-Infrastruktur mit Keycloak
* Systemübersicht der beteiligten Systeme und Schnittstellen
* Auswahl und Studium der zu verwendenden Ruby Library (Gem) für die Authentifizierung via Keycloak
* Proof of Concept für die Authentifizierung in Rails über Keycloak
* Proof of Concept für das schreiben und lesen von Benutzer-Attributen in Keycloak

### Neue Lerninhalte

### Arbeiten in den letzten 6 Monaten

* Einführung in die Entwicklung mit Ruby, Ruby on Rails
* Umsetzung, Konzeption von neuen Features in Cryptopus
* Bugfixing Cryptopus
* Workshop zu Keycloak Setup/Administration
* LDAP Config über ENV-Variablen anstatt DB-Settings
* Probe-IPA im Bereich Authentifizierung in Cryptopus

### Bemerkungen
