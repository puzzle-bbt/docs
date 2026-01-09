# Probe IPA

## Grobbeschrieb

### Titel

Hitobito: Pausierbare und abbrechbare Hintergrundjobs

### Beschreibung

Hitobito verwendet DelayedJob Worker für lang laufende Hintergrundjobs. Als Vorbereitung für das UI für Hintergrundjobs
soll ein Konzept entworfen und eine Job Basisklasse geschrieben werden für Jobs, welche sich pausieren und abbrechen lassen.

## Detailbeschrieb

### Titel der Arbeit

Hitobito: Pausierbare und abbrechbare Hintergrundjobs

### Ausgangslage

Hitobito verwendet DelayedJob für lang laufende Hintergrundjobs. Jobs werden von der Rails Application oder von anderen Jobs enqueued, d.h. es wird eine Delayed::Job Instanz in die Datenbank persistiert.
In separaten Prozessen laufen DelayedJob Workers, welche die Job Instanzen aus der Datenbank laden und verarbeiten. Es gibt aus der Rails Applikation keine generische Möglichkeit, die Verarbeitung eines Jobs zu beeinflussen.

Mit seiner IPA implementiert jp ein UI mit welchem die Hintergrundjobs aufgelistet werden können. Es ist vorgesehen, dass es da auch die Möglichkeit geben soll, Jobs abzubrechen oder zu pausieren.

### Detaillierte Aufgabenstellung

Mit dieser Probe-IPA soll als Vorbereitung für das UI für Hintergrundjobs ein Konzept entworfen und eine Job Basisklasse geschrieben werden für Jobs, welche sich pausieren und abbrechen lassen.

#### PoC

Dokumentation PoC

#### Out of Scope - wird nicht oder erst nach der Probe IPA umgesetzt

* es wird kein UI implementiert

### Individuelle Beurteilungskriterien

13. G04: Überprüfung der technischen Machbarkeit
14. G10: Einrichtung der Entwicklungs- und Laufzeitumgebung
15. Versionsverwaltung mit Git (Source Code) 
16. Wartbarkeit des Codes
17. Automatisierte Tests mit rspec
18. Bewertung von Aussagen
19. G01: Dokumentation fachlicher und technischer Anforderungen
20. G08: Erarbeitung von Umsetzungsvarianten
21. G11: Konforme Implementierung und Versionierung
22. G16: Fehlerbehandlung und Protokollierung

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails
* Javascript, Hotwire
* Active Record, PostgreSQL

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

Es gilt die Rubocop Konfiguration des Projektes. Was nicht durch die Rubocop Konfiguration abgedekt ist, soll gemäss Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide) und der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) gehandhabt werden.
* Git Commit Messages: https://docs.puzzle.ch/qm-guide/latest/source-code-management/index.html#_konvention_commit_message (eine Kopie im IPA Dokument ablegen da nicht öffentlich)

Code der während dieser Probe IPA entsteht soll auf ein privates Github Repo gepushed werden. Die VFs haben dabei stets Lese-Rechte

### Vorkenntnisse

Jannik arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten

* Vorbereitung Dokumentvorlage

### Neue Lerninhalte

* Eigenständigs Entwerfen der Datenstruktur/Klassen

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features für Hitobito (Ruby on Rails)

### Bemerkungen
