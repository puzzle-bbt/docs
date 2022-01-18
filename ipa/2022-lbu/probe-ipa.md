# Probe IPA

## Grobbeschrieb

### Titel

Cryptopus: Migration FileEntry zu Encryptable::File mit EncryptedData

### Beschreibung

Die aktuell in FileEntry gespeicherten und verschlüsselten Dateien sollen in die neue Datenstruktur von Encryptables migriert werden.

## Detailbeschrieb

### Titel der Arbeit

Cryptopus: Migration FileEntry zu Encryptable::File mit EncryptedData

### Ausgangslage

Cryptopus ist eine von Puzzle entwickelte Open Source Lösung für die Verwaltung vertrauter Daten wie Benutzernamen, Passwörtern sowie Dateien. Die verwalteten Zugangsdaten werden verschlüsselt in der Datenbank abgelegt. Beliebig viele Benutzer können sich den Zugriff auf die einzelnen Teams in welchen die Daten organisiert sind teilen.

Die Basis für die Software bildet das Webframework Ruby on Rails. Das Frontend ist mit EmberJS realisiert und kommuniziert via JSON HTTP Api mit dem Backend. 

Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/puzzle/cryptopus

### Detailierte Aufgabenstellung

Ziel dieser Probe-IPA ist die bestehenden Datei-Einträge welche heute an Encryptable::Credentials hängen in die neue Datenstruktur von Encryptables zu migrieren. Ausserdem muss hier der API Endpoint sowie das UI entsprechend für die Anzeige/Auflistung der Dateien angepasst werden.

#### Nicht funktionale Anforderungen

* Die Umsetzung erfolgt auf dem bestehenden Gesamtkonzept von Cryptopus Encryptables
* Alle nicht mehr benötigten Code-Teile werden ausgebaut

#### Funktionale Anforderungen

* Dateien hängen neu an Ordnern (Folder) und nicht mehr an einem Encryptable::Credentials
* Dateien werden bei der Migration an den Ordner angehängt an dem zuvor der verlinkte Encryptable::Credentials angehängt war
* Die migrierten Dateien haben ein sinnvolles Label (z.B. Encryptable::Credentials Name + Dateiname), Varianten ausarbeiten, über Variantentscheid zu realisierende Lösung definieren
* Zugehörige Encryptable::Credentials welche keine Benutzernamen UND Passwort gespeichert haben, werden gelöscht
* Dateien werden unter einem Ordner wie die Zugangsdaten/OSE Secrets aufgelistet und haben ein entsprechendes Icon
* Dateien können maximal 10MB gross sein
* Dateien können über das Papierkorbsymbol gelöscht werden

#### Out of Scope - wird erst nach der Probe IPA umgesetzt

* Erstellen und Bearbeiten von Dateien
* Verschieben von Dateien in einen anderen Folder/Team
* Redirect URL bestehender API Endpoint File Entries

### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 159 - Problemanalyse (Programmieren)
* 166 - Lesbarer Code
* 124 - Testfälle (Programmierung) (ohne System Specs in Probe IPA)
* 170 - Systematik der Lösungsfindung/Lösungsvorschläge

### Mittel und Methoden

Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL
* HTML
* JavaScript, EmberJS, Handlebars
* Sentry

Entwicklungsumgebung:

* Rubymine
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

Luca arbeitet bereits seit einigen Monaten an Features von Cryptopus und konzipierte mit Unterstützung das neue Encryptables Feature. Ausserdem hat er bereits seit dem 2. Lehrjahr Erfahrung auch in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten

* Vorbereitung Dokumentvorlage
* Umsetzung Cryptopus Encryptables Basis Datenstruktur

### Neue Lerninhalte

Grundsätzlich ist Luca mit allen Komponenten die er für die Umsetzung der IPA benötigt mindestens in Berührung gekommen.

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features für Hitobito (Ruby on Rails)
* Konzeption und Umsetzung Teile von Cryptopus Encryptables
* Bugfixing Cryptopus

### Bemerkungen
