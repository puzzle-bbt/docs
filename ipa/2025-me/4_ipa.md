# IPA (ENTWURF)

## Grobbeschrieb

### Titel

Hitobito: Neue Generation von Personen-Filtern

### Beschreibung

Eines der Kernfunktionalitäten von Hitobito ist das Filtern via vom Benutzer definierten Kriterien von Personen auf Personenlisten und Abos. Diese Funktionalität ist in den über 10 Jahren seit es Hitobito gibt oft erweitert worden. Durch die vielen neuen Filtermöglichkeiten wurde speziell das UI immer komplexer und unübersichtlicher. Die Personen-Filteroptionen für Personenlisten und die der Abos sehen ähnlich aus, weisen aber diverse nicht offensichtliche Unterschiede auf.
Mit dieser IPA soll eine neue Generation von Personen-Filtern für Hitobito entwickelt werden. Die bestehenden Filter im UI sollten überarbeitet und nach neuem Mockup umgesetzt werden, so dass sowohl Abo- wie auch Personenfilter nach dem gleichen Muster aufgebaut sind.

Die technische Grundlage dazu wurde bereits als Vorbereitung gemacht. 

## Detailbeschrieb (ENTWURF)

### Titel der Arbeit

Hitobito: Neue Generation von Personen-Filtern

### Ausgangslage
Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt.

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript oder Hotwire verwendet. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung

Mit dieser IPA soll ein neues UI mit Hotwire für die Persistierung von Filter-Parametern im Hitobito Generic-Wagon erstellt werden (rein Frontend). 
- Die Personenlisten- und Abonnementenansicht werden mit dem neuen UI ersetzt.
- Die neue Ansicht wird nach einem gegebenen Mockup umgesetzt.
- Filter Personen-Listen: Funktionalität bleibt wie bisher bestehen und wird durch das neue UI nicht beeinträchtigt.
- Filter Abos: Die Globalen Bedingungen werden für die Filterung angepasst, ausgeschlossen von den Anpassungen sind die Filterung
durch die Rolle, Gruppen, Events, People oder die Exclusion von People.

#### Out of Scope - wird erst nach der IPA umgesetzt

- Filterung für Rollen, Gruppen, Events, People bei Abonnementen.
- Anpassungen der Ansicht in den anderen Wagons.
- Anpassungen der bisher bestehenden Tests in Hitobito welche die zu erweiternden Ansichten betreffen.

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

Marc arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt.

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* Probe-IPA: Vereinheitlichung der Personenlisten- und Abonnementenfilterlogik
* Entwurf eines Mockups

### Neue Lerninhalte

- Eigenständiges Umsetzen eines Designs nach gegebenem Mockup
- Eigenständiges Projektmanagement während der IPA

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features und Bugfixes für Hitobito (Ruby on Rails)
* Probe-IPA: Vereinheitlichung der Personenlisten- und Abonnementenfilterlogik
* Postgresql Migration Hitobito
* Ruby on Rails Migration Hitobito

### Bemerkungen
