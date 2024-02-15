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
Die Verbindungen zwischen den Objectives und KeyResults sollen visuell in einem Diagramm darstellen werden.

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
Es existiert ein Filter, welche die Daten nach Quartal, Teams und einer Titel-Suche filtert.
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
* Es wird immer nur eine Darstellung (aktuelle Übersicht oder Visualisierung) der Daten angezeigt.
* Der Header insbesondere der Filter im Header bleibt beim Umschalten unverändert.
* Der Filter wirkt sich auf beiden Darstellungen aus.
* Ändert der Benutzer den Filter, aktualisiert sich die momentane Darstellung.
* Auch nach dem Umschalten der Darstellungen müssen die Daten der Filtereinstellung entsprechen.

Visualisieren:

* Für die Visualisierung wird die OpenSource JavaScript Library Cytoscape.js eingesetzt.
* Ein Objective enthält folgende Informationen:
  * Titel
  * Team
  * Status (Icon)
* Ein KeyResult enthält folgende Informationen:
  * Titel
  * Team
  * Status (Icon)
* Optisch sollen sich die beiden Verbindungsarten (Alignment, Zugehörigkeit) unterscheiden.

**Beschaffung und Bereitstellung der Daten für die Visualisierung**

* Die bestehende REST-Schnittstelle wird um einen Endpunkt erweitert, welches die Daten zur Visualisierung bereitstellt.
* Diese Daten müssen aus der Datenbank gelesen und im Backend aufbereitet werden.
* Das Frontend sollte mit einem oder wenigen Aufrufe auf die REST-Schnittstelle alle benötigten Daten zur Visualisierung erhalten.

---
Die Daten bestehen aus Teilen der Entitäten Teams, Objectives und KeyResults und weisen folgende Verbindungen auf:

* Ein Objective kann entweder mit einem KeyResult oder mit einem anderen Objective verlinken werden (Alignment).
* Die Verlinkungen sind nur innerhalb des gleichen Quartals zulässig.
* Diese Verlinkung ist optional.

* Visuellen Vorgaben von UX.
* Funktionale Vorgaben vom PO des Projektes.
---

#### Nicht funktionale Anforderungen
* Alle Codeänderungen sind mit UnitTest und im Frontend mit E2E-Tests getestet.
* Code-Formatierung wird durch die im Projekt enthaltenen Formatierer sichergestellt.
* Code-Convention von Puzzle werden eingehalten.

#### Out of Scope - wird erst nach der IPA umgesetzt

* Autovervollständigung der DropDown-Liste in der Erstellen / Bearbeiten Maske eines Objective

### Individuelle Beurteilungskriterien

1. 250 Schichtentrennung (Applikation)
2. 166 Coding-style - lesbarer Code
3. 165 Implementierung von Lösungen (Programmieren)
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

Entwicklungsumgebung:

* IntelliJ IDEA
* Git, Github
* NPM, Maven
* Sonar?, Linter?

Textverarbeitung und Diagramme:

* Latex
* draw.io / PlantUML / 

Projektmethode:

* [Scrum IPA](https://github.com/puzzle-bbt/docs/blob/master/ipa/scrum-ipa.md)

Konventionen:

* Backend: Puzzle / Projekt Konvention
* Frontend: Puzzle / Projekt Konvention

### Vorkenntnisse

* Lias arbeitete an der Umsetzung des OKR-Tools mit und kennt die Implementierung gut.
* Mit Ausnahme der Visualisierung-Library Cytoscape.js kennt Lias sich mit den einzusetzenden Technologien gut aus.

### Vorarbeiten
* Vorbereitung der Dokumentvorlage
* In einem PoC wurden verschiedene Visualisierung-Libraries validiert. Somit konnte Lias erste Erfahrungen mit Cytoscape.js machen.

### Neue Lerninhalte

* Visualisierung mit Cytoscape.js

### Arbeiten in den letzten 6 Monaten

* Umsetzung des OKR-Tools
* Probe-IPA: Erfassen von Alignment im OKR-Tool

### Bemerkungen

Zusätzliche Verantwortliche Fachkraft: Paco Eggimann
