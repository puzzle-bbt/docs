# IPA

## Grobbeschrieb

### Titel

Cryptopus: Neuverschlüsselung der bestehenden Encryptables Daten

### Beschreibung

Der Opensource Password Manager Cryptopus soll so erweitert werden das beliebige Objekte mit der gleichen Datenstruktur gespeichert werden. Neben Benutzer/Passwort sowie Dateien soll es auch möglich sein andere vetrauenswürdige Inhalte wie Tokens, PINs, usw. zu speichern.

## Detailbeschrieb

### Titel der Arbeit

Cryptopus: Neuverschlüsselung der bestehenden Encryptables Daten

### Ausgangslage

Cryptopus ist eine von Puzzle entwickelte Open Source Lösung für die Verwaltung vertraulicher Daten wie beispielsweise Benutzernamen, Passwörtern sowie Dateien. Die verwalteten Zugangsdaten werden verschlüsselt in der Datenbank abgelegt. Beliebig viele Benutzer können sich den Zugriff auf die einzelnen Teams in welchen die Daten organisiert sind teilen.

Die Basis für die Software bildet das Webframework Ruby on Rails. Das Frontend ist mit EmberJS realisiert und kommuniziert via JSON HTTP Api mit dem Rails Backend. 

Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/puzzle/cryptopus

### Detailierte Aufgabenstellung

Die von Cryptopus verwalteten Zugangsdaten werden aktuell mit AES256-CBC verschlüsselt in der DB abgelegt. Um die Sicherheit der Daten zu erhöhen soll die Verschlüsselung mit einem zusätzlichen Initialization Vector (IV) erfolgen. Dazu müssen die Daten neu verschlüsselt werden was nur möglich ist während ein Benutzer eingeloggt ist. Die Verwendung von IV für die Verschlüsselung ist einer der Verbesserungspunkte die aus dem Security Audit von Cryptopus hervorgegangen sind. 

#### Anforderungen

* Die Umsetzung erfolgt auf dem bestehenden Gesamtkonzept von Cryptopus Encryptables (https://github.com/puzzle-bbt/kon-cryptopus-encryptables)
* Alle verschlüsselten Daten (Encryptable), welche noch nicht auf dem neuesten Stand sind, werden nach dem Login eines Benutzers neu verschlüsselt
* Mit einem Variantenvergleich soll entschieden werden ob der Recrypt nur im Backend gemacht wird oder ob es im UI einen Dialog gibt bei dem der User den Recrypt starten kann und über den Fortschritt informiert wird. Ausserdem soll definiert werden ob der Recrypt automatisch nach dem Login erfolgt oder ob der User diesen manuell startet.
* Für die Neuverschlüsselung wird pro Team ein neues Teampasswort generiert (reset Teampassword)
* Bestehende Openshift Secrets mit alter Datenstruktur werden ebenfalls neu verschlüsselt und mit der neuen Datenstruktur abgelegt (EncryptedData)
* Im UI wird auf dem Team angezeigt mit welchem Algorithmus die Daten verschlüsselt sind und wie lange der verwendete Schlüssel (Teampasswort) ist
* Die Recrypt Logik soll auch für künftige Recrypts verwendet werden können (neuere Verschlüsselungsalgorithmen)
* Der verwendete Algorithmus bzw. die Encryption Klasse wird auf jedem Encryptable als auch auf dem Team selber gespeichert
* Schlägt ein Recrypt eines einzelnen Encryptable Entry fehl, werden alle Encryptables des Teams wieder auf den alten Stand zurück gesetzt (DB transaction). In diesem Fall wird bei einem erneuten Recrypt das fehlgeschlagene Team nicht mehr neu verschlüsselt sondern behält die aktuelle Verschlüsselung. Dies soll verhindern das bei einem Recrypt Fehler Cryptopus für den User unbrauchbar wird.

#### Out of Scope - wird erst nach der IPA umgesetzt

* Weitere Attributtypen unterstützen wie PIN, Token, usw.

### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 159 - Problemanalyse (Programmieren)
* 166 - Lesbarer Code
* 124 - Testfälle (Programmierung)
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
* Umsetzung Cryptopus diverser Features rund um die neuen Encryptables

### Neue Lerninhalte

* Eigenständig Domain Klassen rund um Recrypt definieren und umsetzen (design, naming)

Grundsätzlich ist Luca mit allen Komponenten die er für die Umsetzung der IPA benötigt mindestens in Berührung gekommen.

### Arbeiten in den letzten 6 Monaten

* Umsetzung diverser Features für Hitobito (Ruby on Rails)
* Konzeption und Umsetzung Teile von Cryptopus Encryptables
* Bugfixing Cryptopus

### Bemerkungen
