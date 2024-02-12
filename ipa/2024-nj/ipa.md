# IPA

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

Diese IPA befasst sich mit der Einführung von Fulltext Search mit PostgreSQL in Hitobito:

- Fokus auf Entität Person und Group sowie deren aktuell konfigurierten durchsuchbaren Attribute inkl. assozierte Models:
  - https://github.com/hitobito/hitobito/blob/master/app/indices/person_index.rb
  - https://github.com/hitobito/hitobito/blob/master/app/indices/group_index.rb
- Das bestehende Konzept mit den SearchStrategies kann entweder übernommen und angepasst oder gar komplett durch ein neues ersetzt werden
- Scope der IPA ist die Implementation mit pg_search, SQL oder andere Sucharten sollen vorerst nicht mehr unterstützt werden
- Für eine spätere Unterstützung von anderen Sucharten (z.B. via SQL oder Sphinx), soll der Code so aufgebaut werden das dieser zu einem späteren Zeitpunkt sinnvoll erweitert werden kann (z.B. via Base Class und Vererbung)
- Hitobito besitzt einen Core welcher mit Plugins (Wagons) erweitert wird. Für diese IPA soll der SAC/CAS Wagon inkl. Youth Wagon verwendet werden.
- Suchbare Felder sollen pro Entität konfiguriert werden können. Ausserdem müssen diese Felder in Wagons ergänzt oder gar überschrieben werden können.
- Die bestehenden Sphinx Indizes (indices) können für die IPA ignoriert werden und bleiben einfach vorerst im Repo bestehen. 
- Der Fokus der IPA liegt darin die Suche mal primär zu ermöglichen. Detailunterschiede zu der aktuellen Implementation mit Sphinx sollen im Bericht erwähnt werden, falls es sich als zu aufwändig herausstellt, diese innerhalb der IPA oder gar unmöglich ist, diese mit pg_search generell umzusetzen.  (z.B. Infix vs. Prefix Suche)

#### Out of Scope - wird erst nach der IPA umgesetzt

- Entitäten Event, Address, Invoice, usw.

### Individuelle Beurteilungskriterien

* Git Guidelines ?
* Eigene Meinung vs. Aussagen mit Belegen
* Testabdeckung

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

Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide) und der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) gemäss Rubocop Konfiguration des Projekts (https://github.com/hitobito/hitobito/blob/master/.rubocop.yml)
* Git Commit Messages: https://docs.puzzle.ch/qm-guide/latest/source-code-management/index.html#_konvention_commit_message (eine Kopie im IPA Dokument ablegen da nicht öffentlich)

Code der während dieser IPA entsteht soll auf ein privates Github Repo gepushed werden. Die VFs haben dabei stets Lese-Rechte

### Vorkenntnisse

Niklas arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt. In den Monaten vor der IPA hat es sich intensiv mit dem Thema PostgreSQL mit Hitobito befasst. Ausserdem hat er sich bereits mit pg_search vertraut gemacht.

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* Probe-IPA: PoC MySQL zu PostgreSQL
* Umstellung Hitobito von MySQL zu PostgreSQL (Anpassung vieler SQL Statements)
* Umstellung Hitobito Development Docker Setup von MySQL zu PostgreSQL

### Neue Lerninhalte

Bei der Erarbeitung der Probe-IPA konnte Niklas bereits einige Erfahrungen bei einer solchen Migration sammeln. Aufbauend darauf vertieft er sein Wissen mit dieser IPA rund um das Thema Fulltext search mit PostgreSQL.
Grundsätzlich ist Niklas aber bestens vetraut mit Hitobito, Ruby on Rails sowie dessen Datenbankanbindung.

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features und Bugfixes für Hitobito (Ruby on Rails)
* Probe-IPA: PoC MySQL zu PostgreSQL
* Umstellung Hitobito von MySQL zu PostgreSQL (Anpassung vieler SQL Statements)
* Umstellung Hitobito Development Docker Setup von MySQL zu PostgreSQL
* Bootstrap 5.3 Upgrade Hitobito

### Bemerkungen

Zusätzliche Verantwortliche Fachkraft: Robin Steiner 
