# Probe IPA

## Grobbeschrieb

### Titel

OKR-Tool: Alignment Verlinkung über das Frontend verwalten können

### Beschreibung

Der Benutzer soll im Frontend vom OKR-Tool KeyResults und Objectives verlinken können.

---

## Detailbeschrieb

### Titel der Arbeit

OKR-Tool: Alignment Verlinkung über das Frontend verwalten können

### Ausgangslage

Das Puzzle OKR-Tool wurde von den Lernenden im zweiten Halbjahr 2023 umgesetzt und dient zum Verwalten von Objectives und KeyResults. Seit Mitte Dezember ist dieses Tool bei Puzzle ITC im produktiven Einsatz.

Das Datenbank-Schema ermöglicht es heute schon, ein Objective mit einem KeyResult oder mit einem anderen Objective zu verlinken.
Aktuell ist im Frontend und im Backend diese Verlinkung nicht umgesetzt.
Mit dieser Probe-IPA soll die Möglichkeit geschaffen werden, Verlinkungen über das Frontend zu verwalten, und somit Daten für die IPA auf einfache Weise vorbereiten zu können.

Das Tool besteht aus einem Java Backend mit PostgreSQL Datenbank und einem Angular Frontend.

### Detaillierte Aufgabenstellung

#### Funktionale Anforderungen

Es existieren zwei Anforderungen:

**Frontend erweitern**

* Im Dialog zum Erstellen / Bearbeiten eines Objectives soll eine Verlinkung zu einem KeyResult oder zu einem andern Objective definieren werden können. 
* Die Verlinkung ist optional und muss bei Bedarf auch entfernt werden können. 
* Die Auswahl eines KeyResults oder Objectives wird aktuell mit einer einfachen DropDown Liste (ohne Typeahead) umgesetzt, welche alle möglichen KeyResult oder Objective enthält.

**Backend erweitern**

* Das Rest-Interface muss erweitert werden, damit eine Liste von möglichen Objectives und KeyResults für die DropDown-Liste im Frontend abgerufen werden kann.
* Beim Speichern eines Objectives soll das Backend die optionale Verlinkung in den dazu vorgesehenem existierendem Model speichern oder löschen. 
* Die Verlinkung soll auch beim Laden eines Objectives an das Frontend weitergereicht werden.
* Das Backend stellt sicher:
  * dass ein Objective nicht auf sich selber Verlinken kann.
  * dass ein Objectives sich nur zu einem KeyResult oder zu einem Objective verlinken kann.
  * dass ein Objective die Verlinkung auch entfernen kann.

#### Nicht funktionale Anforderungen
* Alle Codeänderungen sind mit UnitTest und im Frontend mit E2E-Tests getestet.
* Code-Formatierung wird durch die im Projekt enthaltenen Formatierer sichergestellt.
* Code-Convention von Puzzle werden eingehalten.

#### Out of Scope - wird erst nach der Probe IPA umgesetzt

* Autovervollständigung der DropDown-Liste in der Erstellen / Bearbeiten Maske eines Objective (Typeahead).

### Individuelle Beurteilungskriterien

keine für diese Probe-IPA, nur Standard-Kriterien

### Mittel und Methoden

Technologie und Plattform:

* Angular, TypeScript, HTML, SCSS
* Java, SpringBoot, Hibernate, Flyway, Swagger
* PostgreSQL
* Jest, Cypress

Entwicklungsumgebung:

* IntelliJ IDEA
* Git, Github
* NPM, Maven
* Sonar, Linter

Textverarbeitung und Diagramme:

* Latex
* draw.io / PlantUML

Projektmethode:

* [Scrum IPA](https://github.com/puzzle-bbt/docs/blob/master/ipa/scrum-ipa.md)

Konventionen:

* Backend: Puzzle / Projekt Konvention
* Frontend: Puzzle / Projekt Konvention

### Vorkenntnisse

Lias arbeitet an der Umsetzung des OKR-Tools mit und kennt die Implementierung gut. 
Er kennt alle einzusetzenden Technologien.

### Vorarbeiten

* keine

### Neue Lerninhalte

* keine

### Arbeiten in den letzten 6 Monaten

* Umsetzung des OKR-Tools

### Bemerkungen
