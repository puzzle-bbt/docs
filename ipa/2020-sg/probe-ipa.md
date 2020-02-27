# Probe IPA

## Grobbeschrieb

### Titel

Standardisierung Authentifizierung und Sessionmanagement Cryptopus - PoC

### Beschreibung

Die heute teilweise selbst entwickelte Authentifizierung und Sessionmanagement soll durch eine Standardlibrary ersetzt werden. 

## Detailbeschrieb

### Titel der Arbeit

Standardisierung Authentifizierung und Sessionmanagement Cryptopus - PoC

### Ausgangslage

Cryptopus ist eine von Puzzle entwickelte Open Source Lösung für die Verwaltung vertrauter Daten wie Benutzernamen, Passwörtern sowie Dateien. Die verwalteten Zugangsdaten werden verschlüsselt in der Datenbank abgelegt. Beliebig viele Benutzer können sich den Zugriff auf die einzelnen Teams in welchen die Daten organisiert sind teilen.

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript mit Ajax verwendet. 

Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/puzzle/cryptopus

### Detailierte Aufgabenstellung

Ziel dieser Probe-IPA ist die Authentifizierung und das Sessionmanagement neu zu konzipieren und basierend darauf ein Proof of Concept (PoC) zu realisieren:

(Alle Anforderungen beziehen sich auf den Bereich Authentifizierung/Sessionmanagement und die angrenzenden Komponenten)

#### Nicht funktionale Anforderungen
* Zusammentragen/Beschreiben der heute realisierten Features
* Dokumentieren der Sicherheitstechnischen Anforderungen
* Dokumentation der beteiligten Abläufe/Prozesse
* Visualisierung und Beschreibung der bestehenden Komponenten
* Beschreiben der benötigten Basics/Komponenten von [Devise](https://github.com/heartcombo/devise)
* Konzeption Integration/Refactoring Devise
* Planung der Umsetzung Proof of Concept (PoC)
* Durchführen PoC
* Auswertung/Fazit PoC

#### Funktionale Anforderungen
* Aussagekräftigere Notifications beim Logout/Login: z.B. beim [automatischen Logout](https://github.com/puzzle/cryptopus/issues/169)
* Login via Root generell nur noch von einer privaten IP aus

### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 166 - Lesbarer Code
* 162 - SW-Architektur
* 170 - Systematik Lösung
* 124 - Testfälle (Programmierung)
* 192 - IT-Sicherheitskriterien
* ohne 230 - Migration (dies wird nur in der IPA selber bewertet da es hier keine Migration gibt)

### Mittel und Methoden
Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL
* HTML, ERB
* Sentry

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
-

### Vorarbeiten
-

### Neue Lerninhalte

* Devise Gem
* PoC mit Auswertung

### Arbeiten in den letzten 6 Monaten

* Einführung in die Entwicklung mit Ruby, Ruby on Rails
* Umsetzung, Konzeption von neuen Features in Cryptopus
* Bugfixing Cryptopus
* Workshop zu Keycloak Setup/Administration
* LDAP Config über ENV-Variablen anstatt DB-Settings

### Bemerkungen
