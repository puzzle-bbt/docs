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

Als Basis für dieses Experiment dient das [Docker Dev Setup](https://github.com/hitobito/development) von Hitobito mit dem Generic Wagon 

#### Phase 1 - Analyse

- Was ist ActiveRecord und wie funktioniert es?

Planung PoC: Setup, Anpassungen DB-Migrations, Anpassungen andere Code-Teile

#### Phase 2 - Durchführung PoC

Aufzeigen Anpassungen DB Migrations


#### Phase 3 - Auswertung und Empfehlung

Aufwandschätzung




Diese Arbeit soll folgende Artifakte liefern:

- Auflistung von je 3-5 Pro und Kontras im Bezug auf eine solche Umstellung
- Eine Empfehlung ob eine solche Umstellung gemacht werden sollte oder eben nicht

- Die Code-Anpassungen die für diesen PoC gemacht wurden


#### Out of Scope - wird erst nach der Probe IPA umgesetzt

* Datenmigration bestehender Instanzen
* Einführung von pg_search sowie Ablösung Sphinx als Indexer
* Betriebliche Themen wie Backup usw.

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
