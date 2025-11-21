# IPA

## Grobbeschrieb

### Titel

Hitobito: UI für Hintergrundjobs

### Beschreibung

Hitobito bietet den Anwendern verschiedene Funktionen, welche mit langlaufenden Hintergrundjobs implementiert werden. Das können zum Beispiel Jobs sein, welche Dateien für den Datenexport generieren.
Bis jetzt gibt es für die Anwender kein UI, mit welchem sie den Status ihrer Hintergrundjobs sehen oder steuern können.
Mit dieser IPA wird ein UI implementiert, welches dem Anwender alle eigenen laufenden, abgeschlossenen und abgebrochenen Hintergrundjobs anzeigt. Zu jedem Job wird Start- und Endzeitpunkt sowie der Jobstatus angezeigt. Im Fehlerfall wird bei abgebrochenen Jobs die Fehlermeldung mit Details zum Fehler angegeben. Jobs die in Zukunft starten können abgebrochen werden.

## Detailbeschrieb

### Titel der Arbeit

Beschreibung Titel

### Ausgangslage
Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt.

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript oder Hotwire verwendet. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung

Mit dieser IPA soll...

#### Out of Scope - wird erst nach der IPA umgesetzt

- Out of Scope

### Individuelle Beurteilungskriterien

1. Entwurf, Design (Programmierung)
2. Dokumentation Datenbanken, Tabellen, etc.
3. Visualisierungen / UML
4. Bewertung von Aussagen
5. Problemanalyse (Programmieren)
6. Automatisierte Tests mit rspec
7. Versionsverwaltung mit Git (Source Code) 

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails, Hotwire, Active Record
* PostgreSQL

Entwicklungsumgebung:

* Intellij 
* Git, Github
* Rake
* Rubocop

Textverarbeitung und Diagramme:

* Latex
* draw.io

Projektmethode:

* [Scrum IPA](https://github.com/puzzle-bbt/docs/blob/master/ipa/scrum-ipa.md)

Konventionen:

Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide) und der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) gemäss Rubocop Konfiguration des Projekts (https://github.com/hitobito/hitobito/blob/master/.rubocop.yml)
* Git Commit Messages: https://docs.puzzle.ch/qm-guide/latest/source-code-management/index.html#_konvention_commit_message (eine Kopie im IPA Dokument ablegen da nicht öffentlich)

Code der während dieser IPA entsteht soll auf ein privates Github Repo gepushed werden. Die VFs haben dabei stets Lese-Rechte

### Vorkenntnisse

Jannik arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt.

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* Probe-IPA: TBD
* Entwurf eines Mockups

### Neue Lerninhalte

- Eigenständiges Umsetzen eines Designs nach gegebenem Mockup
- Eigenständiges Projektmanagement während der IPA

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features und Bugfixes für Hitobito (Ruby on Rails)
* Probe-IPA: TBD

### Bemerkungen
