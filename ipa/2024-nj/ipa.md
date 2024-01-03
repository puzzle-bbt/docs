# Probe IPA

## Grobbeschrieb

### Titel

Hitobito: Einführung von PostgreSQL Fulltext Search

### Beschreibung

Hitobito wird zurzeit ausschliesslich mit MySQL betrieben. Aus verschiedenen Gründen planen wir schon länger eine Umstellung auf **PostgreSQL**.
Zusammen mit dieser Umstellung soll ebenfalls die Suche mit dem Fulltext Search feature von PostgreSQL möglich sein. Damit wäre dann auch Sphinx als Search-Indexer obsolet was das gesamte Deployment bzw. das Setup der Produktionsumgebungen vereinfachen würde.

## Detailbeschrieb

### Titel der Arbeit

Hitobito: Einführung von PostgreSQL Fulltext Search

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt. 
Die Basis für die Software bildet das Webframework Ruby on Rails. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung


#### Out of Scope - wird erst nach der Probe IPA umgesetzt

<!--* Datenmigration bestehender Daten/Instanzen-->
<!--* Einführung von pg_search sowie Ablösung Sphinx als Indexer-->
<!--* Sphinx kann für diese Arbeit ignoriert/deaktiviert werden-->
<!--* Betriebliche Themen wie Backup usw.-->


<!--### Individuelle Beurteilungskriterien-->

<!--keine für diese Probe-IPA, nur Standard-Kritieren-->
* Git Guidelines ?
* Eigene Meinung vs. Aussagen mit Belegen

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL, PostgreSQL

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
* Git Commit Messages: https://docs.puzzle.ch/qm-guide/latest/source-code-management/index.html#_konvention_commit_message (eine Kopie im IPA Dokument ablegen da nicht öffentlich)

Code der während dieser IPA entsteht soll auf ein privates Github Repo gepushed werden. Die VFs haben dabei stets Lese-Rechte

### Vorkenntnisse

Niklas arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* Probe-IPA: PoC MySQL zu PostgreSQL

### Neue Lerninhalte

Bei der Erarbeitung der Probe-IPA konnte Niklas bereits einige Erfahrungen bei einer solchen Migration sammeln. Aufbauend darauf kommen jetzt neue Themen wie Datenmigration sowie Search-Indexing dazu.
Grundsätzlich ist Niklas aber bestens vetraut mit Hitobito, Ruby on Rails sowie Rails DB Migrations.

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features für Hitobito (Ruby on Rails)

### Bemerkungen

Zusätzliche Verantwortliche Fachkraft: Robin Steiner 
