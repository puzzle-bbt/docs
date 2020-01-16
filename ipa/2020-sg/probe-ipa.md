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
* Beschreiben der benötigten Basics/Komponenten von https://github.com/heartcombo/devise
* Konzeption Integration/Refactoring Devise
* Planung der Umsetzung PoC
* Durchführen PoC
* Auswertung/Fazit PoC

#### Funktionale Anforderungen
* Aussagekräftigere Notifications beim Logout/Login: z.B. beim [automatischen Logout](https://github.com/puzzle/cryptopus/issues/169)
* Die LDAP Einstellungen sollen künftig nicht mehr übers UI sondern nur noch über Umgebungsvariablen oder Configfiles konfiguriert werden

### Individuelle Beurteilungskriterien

### Mittel und Methoden

### Vorkenntnisse

### Vorarbeiten

### Neue Lerninhalte

### Arbeiten in den letzten 6 Monaten

### Bemerkungen
