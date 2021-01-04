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

* Dokumentation und Umsetzung der sicherheitstechnischen Aspekte (Login, Session, Attacken)
* Dokumentation der beteiligten Abläufe/Prozesse (Text, UML)

#### Funktionale Anforderungen

* Personen ohne Rollen:
  * haben read/write Zugriff auf das eigene Profil
  * haben read Zugriff auf Profil > Abos, Rechnungen, Verlauf, Log
  * keinen Zugriff auf "Eigenes Profil > Passwort setzen" falls noch nie ein Passwort gesetzt wurde
  * können die Anzeigesprache wechseln
  * sehen die Suchbar nicht und haben auch keinen Zugriff auf die Suchfunktion
  * sehen die Haupt-Navigation nicht und haben auch keinen Zugriff auf Gruppen, Anlässe, Einstellungen, usw.
* Bei der externen Event Anmeldung ist der Zugriff auf "Kontaktdaten erfassen", "Anmeldung als Teilnehmer" sowie "Anmeldedetails" möglich (Workflow Externe Event Anmeldung)
* Auf die Info Seite von Events mit externer Anmeldung kann ebenfalls zugegriffen werden
* Hat sich die Person über "Du hast noch kein Login?" angemeldet, wird das Session Timeout auf 10min gesetzt
* Besitzt eine Person bereits ein Login, kann diese sich nicht über "Du hast noch kein Login?" anmelden. (ggf. bereits vorhanden, verifizieren)

### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 192 - IT-Sicherheitskriterien
* 166 - Lesbarer Code
* 165 - Implementierung von Lösungen (Programmieren)
* 124 - Testfälle (Programmierung)

für die Probe IPA sind nur 5 anstatt 7 Kriterien vorhanden

### Mittel und Methoden
Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL
* HTML, HAML
* Sentry
* Gems: Devise, cancan

Entwicklungsumgebung:

* vim
* git
* Rake
* Rubocop

Textverarbeitung und Diagramme:

* LibreOffice
* draw.io

Projektmethode:

* tbd

Konventionen:

* Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide), der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) sowie die Projektdokumentation (https://github.com/hitobito/hitobito)

### Vorkenntnisse
Nils arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr viel Erfahrung in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten
* Vorbereitung Dokumentvorlage

### Neue Lerninhalte

* Devise Gem, Authentifizierung
* cancancan

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features Hitobito
* Umsetzung, Konzeption Command Line Client Cryptopus
* Bugfixing Cryptopus

### Bemerkungen
