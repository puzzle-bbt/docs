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
* Migrationskonzept für die Umstellung der LDAP Authentifizierung auf SSO mit Keycloak (Nur Konzept, keine technische Umsetzung)
* Eine Anleitung beschreibt wie man Cryptopus zusammen mit Keycloak einrichtet und betreibt

#### Funktionale Anforderungen
* Falls der Benutzer auf Cryptopus zugreift ohne das er sich vorher am Keycloak Server authentifiziert hat, wird er auf die Login-Maske des Keycloak Servers umgeleitet
* Der Benutzer wird nach erfolgreichem Login auf dem Keycloak Server auf die initial angefragte Cryptopus URL weitergeleitet
* Hat der Benutzer bereits eine gültige SSO Session, wird er bei Cryptopus automatisch angemeldet
* API-User können sich immer noch direkt an Cryptopus für den Zugriff auf /api ohne Keycloak authentifizieren
* Es wird keine Login-Maske in Cryptopus angezeigt falls die Authentifizierung via Keycloak/OpenID erfolgt
* Die Login-Maske kann von einer lokalen IP aufgerufen werden um sich per root einzuloggen. (Fallback Login wenn Keycloak nicht mehr verfügbar)
* Die generierte PK_SECRET_BASE welche auf dem Keycloak Server im Benutzer-Attribut abgespeichert wird soll ein Random Token sein der aktuellen Sicherheitsstandards entspricht (Länge, Komplexität)

### Individuelle Beurteilungskriterien
* 235 - Entwurf mit UML
* 166 - Lesbarer Code
* 162 - SW-Architektur
* 170 - Systematik Lösung
* 124 - Testfälle (Programmierung)
* 192 - IT-Sicherheitskriterien
* 230 - Migration

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL
* HTML, ERB
* Sentry
* Keycloak, OpenID Connect

Entwicklungsumgebung:

* Atom
* GIT
* Rake
* Rubocop

Textverarbeitung und Diagramme:

* LibreOffice
* draw.io

Projektmethode:

* HERMES

Konventionen:

* Backend: Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide) und der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) gemäss Rubocop Konfiguration des Projekts (https://github.com/puzzle/cryptopus/blob/master/.rubocop.yml)

### Vorkenntnisse
Sylvain hat für Cryptopus bereits einige Features umgesetzt. Mit Ruby bzw. Ruby on Rails Techstack arbeitet er seit Oktober 2019. Zum Thema Keycloak Setup und Administration besuchte er eine eintägige, interne Schulung. 

### Vorarbeiten
* Aufbau der benötigten lokalen Entwicklungs-Infrastruktur mit Keycloak
* Systemübersicht der beteiligten Systeme und Schnittstellen
* Auswahl und Studium der zu verwendenden Ruby Library (Gem) für die Authentifizierung via Keycloak
* Proof of Concept für die Authentifizierung in Rails über Keycloak
* Proof of Concept für das schreiben und lesen von Benutzer-Attributen in Keycloak

### Neue Lerninhalte
Grundsätzlich wird Sylvain bis zur IPA mit allen technologischen Elementen zumindest einmal in Berührung gekommen sein. Die Herausforderung dieser IPA wird vorallem darin bestehen die einzelnen Komponenten zu einem funktionierenden Gesamtsystem zu verbinden. Dies betrifft nicht nur die Umsetzung, sondern auch die vorangehende Konzeption.

### Arbeiten in den letzten 6 Monaten

* Einführung in die Entwicklung mit Ruby, Ruby on Rails
* Konzeption und Umsetzung des Ausbildungsplan Tools (Ruby, HTML) https://github.com/puzzle-bbt/ausbildungsplan
* Umsetzung, Konzeption von neuen Features in Cryptopus
* Bugfixing Cryptopus
* Workshop zu Keycloak Setup/Administration
* LDAP Config über ENV-Variablen anstatt DB-Settings
* Probe-IPA im Bereich Authentifizierung in Cryptopus

### Bemerkungen
