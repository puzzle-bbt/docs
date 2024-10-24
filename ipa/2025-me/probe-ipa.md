# Probe IPA

## Grobbeschrieb

### Titel

Hitobito: Neue Generation von Personen-Filtern

### Beschreibung

Eines der Kernfunktionalitäten von Hitobito ist das Filtern via vom Benutzer definierten Kriterien von Personen auf Personenlisten und Abos. Diese Funktionalität ist in den über 10 Jahren seit es Hitobito gibt oft erweitert worden. Durch die vielen neuen Filtermöglichkeiten wurde speziell das UI immer komplexer und unübersichtlicher. Die Personen-Filteroptionen für Personenlisten und die der Abos sehen ähnlich aus, weisen aber diverse nicht offensichtliche Unterschiede auf.
Mit dieser Probe-IPA soll für den Backendteil der Abos (MailingLists) eine neue Generation von Personen-Filtern für Hitobito entwickelt werden. 

## Detailbeschrieb

### Titel der Arbeit

Hitobito: Neue Generation von Personen-Filtern

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt. 

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript oder Hotwire verwendet. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung

PoC Datenmodell Filterparameter


#### Out of Scope - wird erst nach der Probe IPA umgesetzt

* ...


### Individuelle Beurteilungskriterien

keine für diese Probe-IPA, nur Standard-Kritieren

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record

Entwicklungsumgebung:

* VS Code
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

Marc arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* Ist-Analyse Personen-Filter Personen-Listen/Abos

### Neue Lerninhalte

* Eigenständigs Entwerfen der Datenstruktur/Klassen

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features für Hitobito (Ruby on Rails)
* Postgresql Migration Hitobito

### Bemerkungen
