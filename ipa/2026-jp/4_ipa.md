# IPA

## Grobbeschrieb

### Titel

Hitobito: UI für Hintergrundjobs

### Beschreibung

Hitobito bietet den Anwendern verschiedene Funktionen, welche mit langlaufenden Hintergrundjobs implementiert werden. Das können zum Beispiel Jobs sein, welche Dateien für den Datenexport generieren.
Bis jetzt gibt es für die Anwender kein UI, mit welchem sie den Status ihrer Hintergrundjobs sehen oder steuern können.
Mit dieser IPA wird ein UI implementiert, welches dem Anwender alle eigenen laufenden, abgeschlossenen und abgebrochenen Hintergrundjobs anzeigt. Zu jedem Job wird Start- und Endzeitpunkt sowie der Jobstatus angezeigt. Im Fehlerfall wird bei abgebrochenen Jobs die Fehlermeldung mit Details zum Fehler angegeben. Jobs die in Zukunft starten können abgebrochen werden.

## Detailierte Aufgabenstellung

### Titel der Arbeit

Beschreibung Titel

### Ausgangslage
Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt.

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript oder Hotwire verwendet. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

Hitobito bietet den Anwendern verschiedene Funktionen, welche mit langlaufenden Hintergrundjobs implementiert werden. Das können zum Beispiel Jobs sein, welche Dateien für den Datenexport generieren.
Bis jetzt gibt es für die Anwender kein UI, mit welchem sie den Status ihrer Hintergrundjobs sehen oder steuern können.

### Detaillierte Aufgabenstellung

Mit dieser IPA wird ein UI implementiert, welches dem Anwender alle eigenen laufenden, abgeschlossenen und fehlgeschlagenen Hintergrundjobs anzeigt. Zu jedem Job werden Attribute wie Jobstatus, Startzeitpunkt und Fortschritt angezeigt. 

* Ein auf jeder Seite sichtbares Icon verlinkt auf die Jobs Ansicht.
* Die Jobs Ansicht listet alle vom Anwender gestarteten Jobs auf. Die Jobansicht aktualisiert sich regelmässig. Zu jedem Job sind folgende Angaben vorhanden:
  - ein geeignetes Icon zur Darstellung des Job Status: geplant, in Arbeit, abgeschlossen, error
  - die Bezeichnung des Jobs
  - ein Fortschittsbalken zur Anzeige des aktuellen Standes eines laufenden Jobs sofern dieser Fortschrittsinformationen bereitstellt. Es ist erkennbar, wenn der Job keinen Fortschritt ausweist.
  - ein Downloadbutton falls am Job eine Datei angehängt ist (z.B. die Exportdatei bei Export Jobs)
* Wenn ein Job abgeschlossen wird (erfolgreich oder mit Error), dann wird ein Toast angezeigt mit der Jobbezeichnung und einer Statusnachricht. Die Statusnachricht ist mit i18n übersetzt. Das Toast wird angezeigt unabhängig davon auf welcher Applikationsansicht der Anwender sich befindet.

Das Feature wird im Core Wagon implementiert und muss mit dem "Generic" Wagon zusammen funktionieren.

#### Out of Scope - wird erst nach der IPA umgesetzt

* Das Icon mit Link auf die Jobs Ansicht soll dynamisch anzeigen, ob für den Anwender Hintergrundjobs am Laufen sind. Im Rahmen der IPA wird ein statisches Icon eingebaut.
* Sortierbarkeit und Pagination der Jobs Liste 
* Anpassen des DownloadCleanerJob dass eine durch die Jobs definierte Aufbewahrungsfrist berücksichtigt wird.
* Anpassungen der bisher bestehenden Tests in Hitobito welche von den Anpassungen betroffen sind.
* Allfällige Anpassungen in den anderen Wagons abgesehen von "Generic" Wagon.

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

* Rubymine, VSCode
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

### Neue Lerninhalte

* Eigenständiges Projektmanagement während der IPA
* Dokumentation mit LaTex erstellen

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features und Bugfixes für Hitobito (Ruby on Rails)

### Bemerkungen
