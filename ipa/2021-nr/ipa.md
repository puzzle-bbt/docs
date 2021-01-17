# IPA

## Grobbeschrieb

### Titel

Zwei-Faktor-Authentisierung für Hitobito

### Beschreibung

Hitobito ist eine Opensourcelösung für die Verwaltung von Mitglieder von Jungendverbänden, Parteien und anderen Organisationen. (hitobito.com, github.com/hitobito) Die Benutzerauthentifizierung von Hitobito soll mit einem zweiten Faktor erweitert werden. (Two Factor Authentication, 2FA)

## Detailbeschrieb

### Titel der Arbeit

Zwei-Faktor-Authentisierung für Hitobito

### Ausgangslage

Hitobito ist eine Open Source Webapplikation zum Verwalten von Mitgliedern, Events und vielem mehr. Die Ruby on Rails Applikation wurde vor einigen Jahren von Puzzle ITC initiert und wird seither stets weiterentwickelt. 

Der komplette Source-Code steht auf Github zur Verfügung: https://github.com/hitobito

Die Basis für die Software bildet das Webframework Ruby on Rails. Für das User Interface wird neben statischer Technologie wie HTML und CSS auch JavaScript mit Ajax verwendet. 

### Detaillierte Aufgabenstellung

Das zusätzliche Absichern von Logins mit einem zweiten Faktor erhöht die Sicherheit von Applikationen. Immer mehr Webapps bieten dieses Feature an um es Angreifern viel schwieriger zu machen mit geklauten Anmeldedaten in die Applikation einzubrechen. 

Mit dieser Arbeit soll Two Factor Authentication (2FA) in den Login Prozess von Hitobito integriert werden. 

#### Nicht funktionale Anforderungen

* Das Software Design der Lösung soll berücksichtigen das künftig weitere 2FA Provider wie z.B. SMS Code hinzugefügt werden können
* Es soll TOTP (Time-Based One-Time Password Algorithm) als 2FA verwendet werden: https://www.ietf.org/rfc/rfc6238.txt
* Als App für den User soll momentan ausschliesslich freeOTP unterstützt werden. https://freeotp.github.io/

#### Funktionale Anforderungen

* Jeder User hat die Möglichkeit 2FA für seinen Account zu aktivieren. Die Aktivierung erfolgt über einen QR Code welcher via Smartphone und der freeOTP App gelesen wird. 
* User können 2FA nicht selber deaktivieren
* Der User hat die Möglichkeit mehrere Endgeräte mit der freeOTP App für eine Hitobito Instanz zu registrieren
* Die Eingabe des 2FA Codes erfolgt nach erfolgreicher Prüfung von Benutzername/Passwort
* Die Eingabe des 2FA Codes soll ebenfalls über einen Brute-Force Schutz verfügen
* In der freeOTP App ist ersichtlich zu welcher Instanz welcher Code gehört
* Ein Admin User hat die Möglichkeit 2FA für einen anderen Benutzer zu deaktivieren
* 2FA kann für Personen mit definierten Rollen erzwungen werden. Die Konfiguration erfolgt dabei pro Instanz oder Wagon. (nicht im UI)
* Ist 2FA für einen User zwingend, muss dieser 2FA nach dem Login mit Benutzer/Passwort einrichten. Solange 2FA in diesem Fall nicht eingerichtet ist, hat er keinen Zugriff auf die aktuelle Hitobito Instanz. 
* Ein Admin User hat die Möglichkeit 2FA für einen anderen Benutzer zu resetten. Sobald sich der Benutzer nach dem Reset mit Benutzer und Passwort einloggt, muss er 2FA nochmals einrichten. Aktive Sessions des Benutzers werden beim Reset terminiert.
* Eine Anleitung für Betreiber/Admins beschreibt wie man 2FA einrichtet und gibt eine Empfehlung ab wie man bestehende Instanzen migriert. 

### Individuelle Beurteilungskriterien

* 235 - Entwurf mit UML
* 192 - IT-Sicherheitskriterien
* 166 - Lesbarer Code
* 165 - Implementierung von Lösungen (Programmieren)
* 124 - Testfälle (Programmierung)
* tbd

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
Nils arbeitet bereits seit einigen Monaten an Features von Hitobito. Ausserdem hat er bereits seit dem 2. Lehrjahr viel Erfahrung in anderen Ruby on Rails Projekten gesammelt. 

### Vorarbeiten
* Vorbereitung Dokumentvorlage
* Grundlagen 2FA

### Neue Lerninhalte

* tbd

### Arbeiten in den letzten 6 Monaten

* Probe IPA "Minimale Ansicht für Personen ohne Rollen" (Login/Session Thema)
* Umsetzung diverser Features Hitobito
* Umsetzung, Konzeption Command Line Client Cryptopus
* Bugfixing, Features Cryptopus (Ruby on Rails)

### Bemerkungen
