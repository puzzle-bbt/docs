# Probe IPA

## Grobbeschrieb

### Titel

Hitobito: PoC Migration MySQL zu PostgreSQL

### Beschreibung

Hitobito wird zurzeit ausschliesslich mit MySQL betrieben. Aus verschiedenen Gründen planen wir schon länger eine Umstellung auf **PostgreSQL**.
Mit dieser Probe-IPA soll dazu ein PoC (Proof of Concept) erstellt werden welcher die Machbarkeit einer solchen Migration prüft.

## Detailbeschrieb

### Titel der Arbeit

Hitobito: PoC Migration MySQL zu PostgreSQL

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt. 

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript mit Ajax verwendet. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung

Hitobito wird zurzeit ausschliesslich mit MySQL betrieben. Aus verschiedenen Gründen planen wir schon länger eine Umstellung auf **PostgreSQL**.

Mit dieser Probe-IPA soll dazu ein PoC (Proof of Concept) erstellt werden welcher die Machbarkeit einer solchen Migration prüft.

Als Basis für dieses Experiment dient das [Docker Dev Setup](https://github.com/hitobito/development) von Hitobito mit dem Hitobito Core sowie dem Generic Wagon 

#### Out of Scope - wird erst nach der Probe IPA umgesetzt

* Datenmigration bestehender Daten/Instanzen
* Einführung von pg_search sowie Ablösung Sphinx als Indexer
* Sphinx kann für diese Arbeit ignoriert/deaktiviert werden
* Betriebliche Themen wie Backup usw.

#### 1 - Analyse

Eine kurze und knackige Analyse der Ausgangslage:

- Welche Teile der Applikation betrifft diese Umstellung?
- Was ist Rails ActiveRecord und wie funktioniert es?
- Rails DB-Migrations kurz vorgestellt
- Was ist die schema.rb und was für eine Rolle spielt sie bei der Umstellung?
- MySQL vs. PostgreSQL: die wichtigsten Unterschiede
- Das Datenbankschema von Hitobito: Standard vs. Spezialitäten, Anzahl Tabellen, Beziehungen usw.

Planung PoC: Setup, Anpassungen DB-Migrations, Anpassungen anderer Code-Teile

#### 2 - Durchführung PoC

Die 5 komplexesten Änderungen in der Code Basis sollen hier detailiert beschrieben werden.

Technischer Bericht wie der PoC verlief, z.B. Anzahl DB-Migrations die geändert werden konnten, Code-Teile die temporär auskommentiert werden mussten usw. Konnte die Applikation schlussendlich mit PostgreSQL betrieben werden? Laufen die specs oder braucht es dort noch Anpassungen?

#### 3 - Auswertung und Empfehlung

Aufwandschätzung




Diese Arbeit soll folgende Artifakte liefern:

- Aufwandschätzung Umstellung PostgreSQL Hitobito mit Generic Wagon 

- Die Code-Anpassungen die für diesen PoC gemacht wurden als Anhang



### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 159 - Problemanalyse (Programmieren)
* 166 - Lesbarer Code
* 162 - Entwurf SW-Architektur
* 161 - Entwurf, Design (Programmierung)
* 164 - Fehlerbehandlung
* 170 - Systematik der Lösungsfindung/Lösungsvorschläge

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL, PostgreSQL
* HTML
* Sentry

Entwicklungsumgebung:

* Rubymine
* Git, Github
* Rake
* Rubocop

Textverarbeitung und Diagramme:

* Latex
* draw.io

Projektmethode:

* [Scrum IPA](https://github.com/puzzle-bbt/docs/blob/master/ipa/scrum-ipa.md)

Konventionen:

* Backend: Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide) und der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) gemäss Rubocop Konfiguration des Projekts (https://github.com/puzzle/cryptopus/blob/master/.rubocop.yml)

### Vorkenntnisse

Niklas arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* ...

### Neue Lerninhalte

Grundsätzlich ist Niklas mit allen Komponenten die er für die Umsetzung der IPA benötigt mindestens in Berührung gekommen.

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features für Hitobito (Ruby on Rails)

### Bemerkungen
