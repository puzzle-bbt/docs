# Probe IPA

## Grobbeschrieb

### Titel

Hitobito: Migration MySQL zu PostgreSQL

### Beschreibung

Hitobito wird zurzeit ausschliesslich mit MySQL betrieben. Aus verschiedenen Gründen planen wir schon länger eine Umstellung auf **PostgreSQL**.

## Detailbeschrieb

### Titel der Arbeit

Hitobito: Migration MySQL zu PostgreSQL

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt. 

Die Basis für die Software bildet das Webframework Ruby on Rails. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung

Hitobito wird zurzeit ausschliesslich mit MySQL betrieben. Aus verschiedenen Gründen planen wir schon länger eine Umstellung auf **PostgreSQL**. Hitobito soll aber vorerst auch immer noch mit MySQL betrieben werden können. Damit wird sichergestellt das eine Migration nach und nach pro Umgebung gemacht werden kann.

SAC sowie youth wagon
<!--Mit dieser Probe-IPA soll dazu ein PoC (Proof of Concept) erstellt werden welcher die Machbarkeit einer solchen Migration prüft.-->

<!--Als Basis für dieses Experiment dient das [Docker Dev Setup](https://github.com/hitobito/development) von Hitobito mit dem Hitobito Core sowie dem Generic Wagon -->

#### Out of Scope - wird erst nach der Probe IPA umgesetzt

<!--* Datenmigration bestehender Daten/Instanzen-->
<!--* Einführung von pg_search sowie Ablösung Sphinx als Indexer-->
<!--* Sphinx kann für diese Arbeit ignoriert/deaktiviert werden-->
<!--* Betriebliche Themen wie Backup usw.-->

#### 

- Specs laufen durch
- Core/Wagon Seeds
- Github CI-Builds
- Ablösung Sequences table

#### Hitobito Docker Dev Setup

https://github.com/hitobito/development

- Die DBs `hitobito_development` sowie `hitobito_test` werden automatisch beim Hochfahren des PostgreSQL-Containers erstellt falls diese nicht bereits vorhanden sind (analog bisherigem MySQL)
- docker-compose.yml soll MySQL (standardmässig disabled), sowie PostgreSQL als container beinhalten
- Eine kurze Anleitung beschreibt wie man auf MySQL switchen kann
- ??? Anpassung `./bin` DB-Helper scripts

#### Github CI-Builds

#### Sphinx



#### Migration bestehender Daten

#### Planung Migration Integration/Produktion

- Aufwandschätzung sowie Termin-Plan Migration Produktion
- Welche Meilensteine müssen wann erreicht werden damit die Migration planmässig durchgeführt werden kann?

<!--#### 1 - Analyse-->

<!--Eine kurze und knackige Analyse der Ausgangslage:-->

<!--- Welche Teile der Applikation betrifft diese Umstellung?-->
<!--- Was ist Rails ActiveRecord und wie funktioniert es?-->
<!--- Rails DB-Migrations kurz vorgestellt-->
<!--- Was ist die schema.rb und was für eine Rolle spielt sie bei der Umstellung?-->
<!--- MySQL vs. PostgreSQL: die wichtigsten Unterschiede-->
<!--- Das Datenbankschema von Hitobito: Standard vs. Spezialitäten, Anzahl Tabellen, Beziehungen usw.-->

<!--Planung PoC: Setup, Anpassungen DB-Migrations, Anpassungen anderer Code-Teile-->

<!--#### 2 - Durchführung PoC-->

<!--Die 5 komplexesten Änderungen in der Code Basis sollen hier detailiert beschrieben werden.-->

<!--Technischer Bericht wie der PoC verlief, z.B. Anzahl DB-Migrations die geändert werden konnten, Code-Teile die temporär auskommentiert werden mussten usw. Konnte die Applikation schlussendlich mit PostgreSQL betrieben werden? Laufen die specs oder braucht es dort noch Anpassungen?-->

<!--Eine ToDO Liste mit den noch offenen Aufgaben.-->

<!--#### 3 - Auswertung und Empfehlung-->

<!--Eine Zusammenfassende Auswertung des PoC sowie eine Empfehlung ob so eine Migration gemacht werden sollte oder nicht.-->

<!--Ausserdem eine einfach Aufwandschätzung für das fertigstellen dieser Migration sodass diese Produktions-Ready ist. (ohne sphinx, daten migration, usw)-->

<!--### Individuelle Beurteilungskriterien-->

<!--keine für diese Probe-IPA, nur Standard-Kritieren-->

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
