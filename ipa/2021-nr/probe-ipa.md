# Probe IPA

## Grobbeschrieb

### Titel

Minimale Ansicht für Personen ohne Rollen

### Beschreibung

Personen ohne Rollen sollen künftig nur noch Zugriff auf eine minimale Ansicht in Hitobito haben.

## Detailbeschrieb

### Titel der Arbeit

Minimale Ansicht für Personen ohne Rollen

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde vor einigen Jahren von Puzzle ITC initiert und wird seither stets weiterentwickelt. 

Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript mit Ajax verwendet. 

### Detailierte Aufgabenstellung

Personen welche sich beispielsweise über die externe Event-Anmeldung neu registrieren haben noch keine Rolle im System. Etwas unschön ist das diesen Personen dann teilweise die Haupt-Navigation angezeigt wird. Der Zugriff ist heute schon ziemlich eingeschränkt, jedoch sieht die Person dann bereits Details wie beispielsweise die Gruppenstruktur der Organisation. 

Mit dieser Arbeit soll eine minimale Ansicht für Personen ohne Rollen realisiert werden. [Github Issue](https://github.com/hitobito/hitobito/issues/948)

#### Nicht funktionale Anforderungen

* Dokumentieren der sicherheitstechnischen Anforderungen
* Dokumentation der beteiligten Abläufe/Prozesse

#### Funktionale Anforderungen

* Personen ohne Rollen:
  * haben read/write Zugriff auf das eigene Profil (nur Info Tab)
  * keinen Zugriff auf "Eigenes Profil > Passwort setzen" falls noch nie ein Passwort gesetzt wurde
  * können die Anzeigesprache wechseln
  * sehen die Suchbar nicht und haben auch keinen Zugriff auf die Suchfunktion
  * sehen die Haupt-Navigation nicht und haben auch keinen Zugriff auf Gruppen, Anlässe, Einstellungen, usw.
* Bei der externen Event Anmeldung ist der Zugriff auf "Kontaktdaten erfassen", "Anmeldung als Teilnehmer" sowie "Anmeldedetails" möglich (Workflow Externe Event Anmeldung)
* Auf die Info Seite von Events mit externer Anmeldung kann ebenfalls zugegriffen werden

### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 166 - Lesbarer Code
* 162 - SW-Architektur
* 170 - Systematik Lösung
* 124 - Testfälle (Programmierung)
* 192 - IT-Sicherheitskriterien

### Mittel und Methoden
Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL
* HTML, HAML
* Sentry

Entwicklungsumgebung:

* vim
* git
* Rake
* Rubocop

Textverarbeitung und Diagramme:

* LibreOffice
* draw.io

Projektmethode:

* HERMES

Konventionen:

* Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide), der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) sowie die Projektdokumentation (https://github.com/hitobito/hitobito)

### Vorkenntnisse
Nils arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrungen in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten
* Vorbereitung Dokumentvorlage

### Neue Lerninhalte

* Devise Gem, Authentifizierung

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features Hitobito
* Umsetzung, Konzeption Command Line Client Cryptopus
* Bugfixing Cryptopus

### Bemerkungen
