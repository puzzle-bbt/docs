# IPA

## Grobbeschrieb

### Titel

Zwei-Faktor-Authentisierung für Hitobito

### Beschreibung

Hitobito ist eine Open Source Community Management Lösung für die Verwaltung von Mitglieder von Jungendverbänden, Parteien und anderen Organisationen. (hitobito.com, github.com/hitobito) Die Benutzerauthentifizierung von Hitobito soll mit einem zweiten Faktor erweitert werden. (Two Factor Authentication, 2FA)

## Detailbeschrieb

### Titel der Arbeit

Zwei-Faktor-Authentisierung für Hitobito

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde 2012 von Puzzle ITC initiiert und wird stets weiterentwickelt. Durch die wachsende Community steigen auch die Anforderungen, insbesondere bezüglich Sicherheit. Aktuell wird für ein Zugang ein Benutzername und Passwort benötigt. Entsprechende Passwortregeln sind definiert. Eine erweiterte Sicherheit für den Authentifizierungsprozess sind gewünscht. Die gespeicherten Daten nehmen tendenziell zu und gewisse Benutzer haben weitreichende Berechtigungen. Besonders diese User gilt es besser besser zu schützen.

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript mit Ajax verwendet. Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

### Detaillierte Aufgabenstellung

Das zusätzliche Absichern von Logins mit einem zweiten Faktor erhöht die Sicherheit von Applikationen. Immer mehr Applikationen bieten dieses Feature an um es potentiellen Angreifern viel schwieriger zu machen mit geklauten Anmeldedaten unberechtigten Zugriff zu erlangen. 

Mit dieser Arbeit soll Two Factor Authentication (2FA) in den Login Prozess von Hitobito integriert werden. 

#### Nicht funktionale Anforderungen

* Das Software Design der Lösung soll berücksichtigen das künftig weitere 2FA Provider wie z.B. SMS Code hinzugefügt werden können
* Es soll TOTP (Time-Based One-Time Password Algorithm) als 2FA verwendet werden: https://www.ietf.org/rfc/rfc6238.txt
* Als App für den User soll momentan ausschliesslich freeOTP unterstützt werden: https://freeotp.github.io/
* Für TOTP soll ein etabliertes und aktuelles Gem (Ruby Libs) wie beispielsweise rotp verwendet werden
* Generien von QR Codes z.B. mit dem Gem rqrcode
* Die 2FA muss durch die User intuitiv eingerichtet werden können
* Sicherheitskriterien und entsprechende Massnahmen sind für dieses Feature definiert und umgesetzt

#### Funktionale Anforderungen

* Jeder User hat die Möglichkeit 2FA für seinen Account zu aktivieren. Die Aktivierung erfolgt über einen QR Code welcher via Smartphone und der freeOTP App gelesen wird. 
* User können 2FA nicht selber deaktivieren
* Der User hat die Möglichkeit mehrere Endgeräte mit der freeOTP App für eine Hitobito Instanz zu registrieren
* Die Eingabe des 2FA Codes erfolgt nach erfolgreicher Prüfung von Benutzername/Passwort
* Die Eingabe des 2FA Codes soll ebenfalls über einen Brute-Force Schutz verfügen
* In der freeOTP App ist ersichtlich zu welcher Instanz welcher Code gehört
* Ein Admin User hat die Möglichkeit 2FA für einen anderen Benutzer zu deaktivieren falls die Rollen des Users kein 2FA erzwingen
* 2FA kann für Personen mit definierten Rollen erzwungen werden. Die Konfiguration erfolgt dabei pro Instanz oder Wagon. (nicht im UI)
* Ist 2FA für einen User zwingend, muss dieser 2FA nach dem Login mit Benutzer/Passwort einrichten. Solange 2FA in diesem Fall nicht eingerichtet ist, hat er keinen Zugriff auf die aktuelle Hitobito Instanz. 
* Ein Admin User hat die Möglichkeit 2FA für einen anderen Benutzer zu resetten. Sobald sich der Benutzer nach dem Reset mit Benutzer und Passwort einloggt, muss er 2FA nochmals einrichten. Aktive Sessions des Benutzers werden beim Reset terminiert.
* Eine Anleitung für Betreiber/Admins beschreibt wie man 2FA einrichtet und gibt eine Empfehlung ab wie man bestehende Instanzen migriert
* Wird einem Benutzer eine Rolle zugewiesen welche 2FA erzwingt, muss der User beim nächsten Login 2FA einrichten

### Individuelle Beurteilungskriterien

* 235 - [Entwurf mit UML](https://github.com/puzzle-bbt/docs/blob/master/ipa/beurteilungskriterien.md)
* 192 - [IT-Sicherheitskriterien](https://github.com/puzzle-bbt/docs/blob/master/ipa/beurteilungskriterien.md)
* 166 - Lesbarer Code
* 165 - Implementierung von Lösungen (Programmieren)
* 124 - Testfälle (Programmierung)
* 170 - Systematik der Lösungsfindung/Lösungsvorschläge
* 194 - Plausibilisierung der Benutzer-Eingaben

### Mittel und Methoden
Technologie und Plattform:

* Ruby, Ruby on Rails, Active Record
* MySQL
* HTML, HAML
* Sentry
* Gems: Devise, cancan

Entwicklungsumgebung:

* vim
* git
* Rake
* Rubocop

Textverarbeitung und Diagramme:

* Latex
* draw.io

Projektmethode:

* Scrum

Konventionen:

* Es gilt der Ruby Style Guide (https://github.com/rubocop-hq/ruby-style-guide), der Rails Style Guide (https://github.com/rubocop-hq/rails-style-guide) sowie die Projektdokumentation (https://github.com/hitobito/hitobito)

### Vorkenntnisse
Nils arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr viel Erfahrung in anderen Ruby on Rails Projekten gesammelt. Puzzle intern wird für gewisse Services 2FA bereits vorausgesetzt.

### Vorarbeiten
* Vorbereitung Dokumentvorlage
* Grundlagen 2FA

### Neue Lerninhalte

Grundsätzlich wird Nils bis zur IPA mit allen Elementen des Features in Berührung gekommen sein. 

### Arbeiten in den letzten 6 Monaten

* Probe IPA "Minimale Ansicht für Personen ohne Rollen" (Login/Session Thema)
* Umsetzung diverser Features Hitobito
* Umsetzung, Konzeption Command Line Client Cryptopus
* Bugfixing, Features Cryptopus (Ruby on Rails)

### Bemerkungen
