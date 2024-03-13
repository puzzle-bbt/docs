# Probe IPA

## Grobbeschrieb

### Titel

Visualisierung der Objectives und KeyResults

### Beschreibung

Das bestehende OKR-Tool von Puzzle ITC soll mit einer neuen Ansicht zur Visualisierung der Teams mit ihren Objectives und KeyResults ergänzt werden.
Zum Inhalt dieser IPA gehört neben dem Bau der neuen Ansicht auch das Lesen und Aufbereiten der Daten aus der Datenbank, sowie das Ausliefern an das Frontend.
Das OKR-Tool besteht aus einem Spring Boot Backend, einer PostgreSQL DB, sowie einem Angular Frontend.
Für die Visualisierung im Frontend wird eine JavaScript Bibliothek verwendet.

### Arbeitsgebiet

Applikationsentwicklung OO

### Plattform

UNIX / Linux

### Programmiersprache

JavaScript

---

## Detailbeschrieb

### Titel der Arbeit

OKR-Tool: Visualisierung der Objectives und KeyResults

### Ausgangslage

Das Puzzle OKR-Tool wurde von den Lernenden im zweiten Halbjahr 2023 umgesetzt und dient zum Verwalten von Objectives und KeyResults. Seit Mitte Dezember ist dieses Tool bei Puzzle ITC im produktiven Einsatz.
Als nächste Erweiterung möchte man das Tool um eine weitere Ansicht ergänzen:
Die Alignment-Verbindungen zwischen den Objectives und KeyResults sollen visuell in einem Diagramm darstellen werden.

Das OKR-Tool besteht aus einem Spring Boot Backend, einer PostgreSQL DB, sowie einem Angular Frontend, welches die Daten über eine RESTful-Schnittstelle vom Backend bezieht.

Zum Umfang der Arbeit gehört neben der neuen Ansicht auch das Beschaffen der Daten aus der Datenbank.

Die für diese Arbeit benötigten Entitäten und ihre Beziehungen: 
* Ein Objective gehört zu einem Team.
* Ein KeyResult gehört zu einem Objective.
* Ein Objective gehört immer zu einem Quartal.
* Ein KeyResult gehört immer zu einem Quartal.
* Ein ObjectiveAlignment verlinkt ein Objective zu einem anderen Objective.
* Ein KeyResultAlignment verlinkt ein Objective zu einem KeyResult.

Die aktuelle Übersicht listet die KeyResults gruppiert in Teams und Objectives auf.
Es existiert ein Filter, welcher die Daten nach Quartal, Teams und einer Objective-Titel-Suche filtert.
Es werden nur Daten angezeigt, welche zum gleichen Quartal gehören.

### Detaillierte Aufgabenstellung

#### Funktionale Anforderungen

Die Aufgabenstellung umfasst folgende Teilaufgaben:

* Erstellen der neuen Ansicht mit der Visualisierung im Frontend
* Beschaffung und Bereitstellung der Daten für die Visualisierung

**Erstellen der neuen Ansicht mit der Visualisierung im Frontend**

Umschalten:

* Beim Aufruf des OKR-Tools wird die aktuelle Übersicht angezeigt.
* Ein neuer Umschalter unterhalb des Headers erlaubt es, zwischen der aktuellen Übersicht und der neuen Visualisierung umzuschalten.
* Es wird immer nur eine Darstellung (existierende Übersicht oder neue Visualisierung) der Daten angezeigt.
* Der Header insbesondere der Filter im Header bleibt beim Umschalten unverändert.
* Der Filter wirkt sich auf beiden Darstellungen aus.
* Ändert der Benutzer den Filter, aktualisiert sich die momentane Darstellung.
* Auch nach dem Umschalten der Darstellungen müssen die Daten der Filtereinstellung entsprechen.

Visualisieren:

* Für die Visualisierung wird die OpenSource JavaScript Library Cytoscape.js eingesetzt.
* Folgende Daten werden bei der Visualisierung angezeigt:
  1. Alle Objectives anhand des eingestellten Filters
  2. Optional alle KeyResults anhand des eingestellten Filters
  3. Alle Objectives und KeyResults, auf welche die Objectives aus Punkt 1 verweisen (Alignment)
  4. Optional alle Objectives, zu welchen die KeyResults aus Punk 3 gehören
* Die Darstellung eines Objective enthält folgende Informationen:
  * Titel
  * Team
  * Status (Icon)
* Die Darstellung eines KeyResult enthält folgende Informationen:
  * Titel
  * Team
  * Status (Hintergrundfarbe)
* Optisch wird die Visualisierung nach den Vorgaben des PO und UX vom OKR-Tools umgesetzt.
* Beim der Library Cytoscape.js lässt sich der Inhalt (Text) in einem Node nicht formatieren. Als Lösung wird der Inhalt jedes einzelnen Nodes in einem SVG-Bild generiert und als Hintergrund des Node gesetzt.
* Ein Klick auf ein Objective oder KeyResult öffnet die bestehende Detailansicht des Objectives oder KeyResults.* Ein Editieren eines Objective oder eines KeyResult löst ein neues Rendern der Visualisierung aus. Die Skalierung sowie Positionierung wird dabei von der Library wieder neu berechnet und kann sich ändern.

**Beschaffung und Bereitstellung der Daten für die Visualisierung**

* Die bestehende REST-Schnittstelle wird um einen Endpunkt erweitert, welcher die Daten zur Visualisierung bereitstellt.
* Diese Daten müssen aus der Datenbank gelesen und im Backend aufbereitet werden.
* Das Frontend sollte mit einem oder wenigen Aufrufe der REST-Schnittstelle alle benötigten Daten zur Visualisierung erhalten.

#### Nicht funktionale Anforderungen
* Alle Codeänderungen sind mit Unit- und Integrations-Tests getestet.
* Änderungen am Frontend sind mit sinnvollen E2E-Tests getestet.
* Code-Formatierung wird durch die im Projekt enthaltenen Formatierer sichergestellt.
* Der Programm-Code wird regelmässig und in logischen Einheiten in das GIT-Repository des Projekts in einem separaten Branch eingecheckt und gepusht.
* Die Dokumentation wird regelmässig und in logischen Einheiten in ein eigenes GIT-Repository eingecheckt und gepusht.
* Die REST-Schnittstelle zwischen Frontend und Backend wird mit dem im Projekt vorhandenen Swagger UI dokumentiert

#### Out of Scope - wird erst nach der IPA umgesetzt
* Die Anordnung des Diagrams wird von der Library Cytoscape.js eigenständig durchgeführt und wird in der IPA nicht angepasst.
* Wörter im Diagram, welche auf einer Zeile keinen Platz finden, sollten umgebrochen werden.
* Die neue Visualisierung erhält eine Legende. 
* Die Visualisierung soll auch auf dem Smartphone funktionieren.
* Erfassen und Anzeigen der Alignment Verbindungen in den bestehenden Formularen und Ansichten.

### Individuelle Beurteilungskriterien

1. 250 Schichtentrennung (Applikation)
2. 166 Coding-style - lesbarer Code
3. Performante Datenbeschaffung im Backend
4. 164 Codierung: Fehlerbehandlung
5. Versionsverwaltung mit Git (Source Code)
6. Automatisierte Tests Backend + Frontend
7. Dokumentation der REST-Schnittstellen Erweiterung im Swagger

### Mittel und Methoden

Technologie und Plattform:

* Angular, TypeScript, HTML, SCSS
* Java, Spring Boot, Hibernate, Flyway, Swagger
* PostgreSQL
* Jest, Cypress
* Visualisierung: Cytoscape.js

Entwicklungsumgebung:

* IntelliJ IDEA
* Git, Github
* NPM, Maven
* Linter

Textverarbeitung und Diagramme:

* LaTex
* draw.io

Projektmethode:

* [Scrum IPA](https://github.com/puzzle-bbt/docs/blob/master/ipa/scrum-ipa.md)

Konventionen:

* Backend: Projekt Konvention / Puzzle
* Frontend: Projekt Konvention / Puzzle
* Git Commit Messages: Projekt Konvention / https://docs.puzzle.ch/qm-guide/latest/source-code-management/index.html#_konvention_commit_message (eine Kopie im IPA Dokument ablegen da nicht öffentlich)

### Vorkenntnisse

* Lias arbeitete an der Umsetzung des OKR-Tools mit und kennt die Implementierung gut.
* Mit Ausnahme der Visualisierung-Library Cytoscape.js kennt Lias sich mit den einzusetzenden Technologien gut aus.

### Vorarbeiten
* Vorbereitung der Dokumentvorlage
* In einem PoC wurden verschiedene Visualisierung-Libraries validiert. Somit konnte Lias erste Erfahrungen mit Cytoscape.js machen.

### Neue Lerninhalte

* Visualisierung mit Cytoscape.js
* Dokumentation mit LaTex erstellen

### Arbeiten in den letzten 6 Monaten

* Umsetzung des OKR-Tools
* Probe-IPA: Erfassen von Alignment im OKR-Tool

### Bemerkungen

Zusätzliche Verantwortliche Fachkraft: Paco Eggimann

Wunschtermine für den 3. Expertenbesuch (Präsentationstermin der IPA-Arbeit):
- Montag 22.4.2024: 8:00 Vormittag oder 13:00 Nachmittag
- Donnerstag 25.4.2024: 8:00 Vormittag