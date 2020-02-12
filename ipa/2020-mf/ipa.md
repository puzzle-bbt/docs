# IPA Marc Detailplanung

## Ausgangslage:
*Hilfsfragen:* Gibt es eine Vorgeschichte zu dieser Facharbeit? Was sind die Gründe für dieses Projekt? Wie ist das Umfeld zu dieser Arbeit?

Aktuell arbeiten wir an einer Webapplikation (Spring Boot / Angular) bei welcher wir mit Stromdaten aus Smartmeter (Stromzähler) operieren. Ursprünglich kann sich ein Kunde registrieren und seine Koordinaten der Verbrauchsanlage (Anzahl produzierende und konsumierende Stromzähler usw.) angeben. Im Anschluss erhalten wir über eine definierte Schnittstelle (REST oder FTPS) Stromdaten zu den zuvor angegebenen Zählern und verarbeiten diese. Oftmals merken wir erst nach der Registrierung, dass das Datenformat von unserem von uns verlangtem Standard abweicht und somit nicht verarbeitet werden kann. Deshalb soll eine Validierung eingebaut werden, bei welcher man während der Registrierung seine Stromdaten validieren kann. In dieser Arbeit beschränken wir uns rein auf die Validierung von Daten im SDAT Format (https://www.strom.ch/de/media/8212/download).


## Detaillierte Aufgabenstellung:
*Hilfsfragen:* Welche Resultate erwartet der Auftraggeber? Welche prüfbaren/messbaren Ziele sind zu erreichen? Welche Tests sind durchzuführen? Was für eine Dokumentation ist zu erstellen? Für wen? (technische Dokumentation, Benutzerhandbuch, Designbeschreibung, ...)?

Ich möchte als Kunde die Möglichkeit haben nachdem ich alle Zähler und Infrastrukturdaten im Onboarding angegeben habe, optional ein Demo-SDAT-File hochzuladen, welches gegen unsere Schema Definition validiert wird. 

*Konkrete Features zu implementieren:*
Uploadmöglichkeit eines SDAT-Files in der Pre-onboarding Maske (Registrierungsprozess)
Validierung des XML Files gegen XSD
Rudimentäres Feedback zur Validation

Optional kann die Validierung noch durch weitere Features erweitert werden:
Validierung der einzelnen Smartmeter Punkte im File
Detailliertes Feedback über Validation des Files
Akzeptieren mehrer Files als Archiv 


## 7 individuellen Kriterien


225: Leitfrage Versionsverwaltung mit Verwaltungs-SW
231: Projektjournal
124: Testfälle
250: Schichtentrennung
162: Entwurf - SW-Architektur
165: Implementierung von Lösungen
166: Codingstyle - lesbarer Code


## Mittel und Methoden:
Hilfsfragen: Aufzählung der hauptsächlichsten Mittel und Methoden (Hardware, Software, Programmiersprachen, Firmenvorgaben,...), welche für die Lösung erwartet oder vorgeschrieben werden.

*Stack:*
Java 11 mit Spring Boot 2
Angular 8
PostgreSQL

Als Entwicklungsumgebung wird hauptsächlich IntelliJ Ultimate verwendet.
Als Vorlage für die allgemeinen Code Conventions werden die Standards für Java und Angular. Java (https://google.github.io/styleguide/javaguide.html) und Angular (https://angular.io/guide/styleguide)


## Vorkenntnisse
*Hilfsfragen:* Welche der geplanten Tätigkeiten/Produkte/Techniken sind schon bekannt? Wie häufig / wie lange hat der/die Lernende mit diesen schon gearbeitet?

*Fachliche Vertrautheit:* Der Lernende arbeitet seit Mitte September im Projekt und kennt die fachliche Welt.
*XML XSD Validation:* Der Lernende kennt die Validierungstechniken noch nicht und hat noch keine XML Validierung implementiert.
*Backend REST Schnittstellen implementieren:* Implementation von REST Schnittstellen nach Boundary/Control/Entity Schema ist dem Lernenden bekannt.
*Angular Frontend:* Das Arbeiten mit dem Angular Framework und unserem Frontend ist dem Lernenden bekannt.


## Vorarbeiten:
*Hilfsfragen:*Welche Arbeiten werden als Vorbereitung schon vor der IPA ausgeführt?

Erstellen der Templates für die Dokumentation. Einlesen und Testen von Libraries für die Validierung der XML Files gegen XSD.


## Neue Lerninhalte:
*Hilfsfragen:* Welche Lerninhalte sind für die/den Lernende/n voraussichtlich neu und müssen erarbeitet werden? Welche Quellen stehen ihm zur Verfügung? Achtung: Zurückhaltung mit Unbekanntem!

Validation von XML Files gegen XSD. Hierzu gibt es genügend Beispiele und Tutorials im Internet.


## Arbeiten in den letzten 6 Monaten:
*Hilfsfragen:* Welche Art von Arbeiten hat die/der Lernende im letzten Halbjahr durchgeführt? Welches waren die zwei grössten Aufträge? Wie viele Arbeitstage wurden dafür aufgewendet? Welche Tools wurden dafür eingesetzt?

In den letzten 6 Monaten hat der Lernende aktiv in unserem Entwicklungsteam an der Applikation weiterentwickelt. Seine Tätigkeiten reichten von Bugfixes bis zur Implementation und Erweiterung unserer Schnittstellen für weitere fachliche Anforderungen. 

## Bemerkungen:
*Hilfsfragen:* Gibt es bereits bekannte Abwesenheiten des Fachvorgesetzten bis zur Facharbeit? Gibt es weitere terminliche Besonderheiten?

Der Fachvorgesetzte ist vom 20.2.-1.3. abwesend. 

