# IPA MF 2020

## Grobbeschrieb

### Thematik

*Titel:* XML Validierung in einer bestehenden Java Spring Boot Applikation

*Beschreibung:*
Unsere Applikation soll im Preonboarding Bereich um eine SDAT XML Validierung erweitert werden, sodass Kunden automatisiert ihre Beispielsfiles am System testen können.


## Detailplanung

*Ausgangslage:*
*Hilfsfragen:* Gibt es eine Vorgeschichte zu dieser Facharbeit? Was sind die Gründe für dieses Projekt? Wie ist das Umfeld zu dieser Arbeit?

Aktuell arbeiten wir an einer Webapplikation (Spring Boot / Angular) bei welcher wir mit Stromdaten aus Smartmeter (Stromzähler) operieren. Ursprünglich kann sich ein Kunde registrieren und seine Koordinaten der Verbrauchsanlage (Anzahl produzierende und konsumierende Stromzähler usw.) angeben. Im Anschluss erhalten wir über eine definierte Schnittstelle (REST oder FTPS) Stromdaten zu den zuvor angegebenen Zählern und verarbeiten diese. Oftmals merken wir erst nach der Registrierung, dass das Datenformat von unserem von uns verlangtem Standard abweicht und somit nicht verarbeitet werden kann. Deshalb soll eine Validierung eingebaut werden, bei welcher man während der Registrierung seine Stromdaten validieren kann. In dieser Arbeit beschränken wir uns rein auf die Validierung von Daten im SDAT Format (https://www.strom.ch/de/media/8212/download).


*Dtaillierte Aufgabenstellung:*
*Hilfsfragen:* Welche Resultate erwartet der Auftraggeber? Welche prüfbaren/messbaren Ziele sind zu erreichen? Welche Tests sind durchzuführen? Was für eine Dokumentation ist zu erstellen? Für wen? (technische Dokumentation, Benutzerhandbuch, Designbeschreibung, ...)?

Ich möchte als Kunde die Möglichkeit haben nachdem ich alle Zähler und Infrastrukturdaten im Onboarding angegeben habe, optional ein Demo-SDAT-File hochzuladen, welches gegen unsere Schema Definition validiert wird. 

Konkrete Features zu implementieren:
Uploadmöglichkeit eines SDAT-Files in der Pre-onboarding Maske (Registrierungsprozess)
Validierung des XML Files gegen XSD
Rudimentäres Feedback zur Validation


*7 Kriterien:*


*Mittel und Methoden:*
*Hilfsfragen:* Aufzählung der hauptsächlichsten Mittel und Methoden (Hardware, Software, Programmiersprachen, Firmenvorgaben,...), welche für die Lösung erwartet oder vorgeschrieben werden.


*Vorkenntnisse:*
*Hilfsfragen:* Welche der geplanten Tätigkeiten/Produkte/Techniken sind schon bekannt? Wie häufig / wie lange hat der/die Lernende mit diesen schon gearbeitet?


*Vorarbeiten:*
*Hilfsfragen:* Welche Arbeiten werden als Vorbereitung schon vor der IPA ausgeführt?


*Neue Lerninhalte:*
*Hilfsfragen:* Welche Lerninhalte sind für die/den Lernende/n voraussichtlich neu und müssen erarbeitet werden? Welche Quellen stehen ihm zur Verfügung? Achtung: Zurückhaltung mit Unbekanntem!


*Arbeiten in den letzten 6 Monaten:*
*Hilfsfragen:* Welche Art von Arbeiten hat die/der Lernende im letzten Halbjahr durchgeführt? Welches waren die zwei grössten Aufträge? Wie viele Arbeitstage wurden dafür aufgewendet? Welche Tools wurden dafür eingesetzt?


*Bemerkungen:*
*Hilfsfragen:* Gibt es bereits bekannte Abwesenheiten des Fachvorgesetzten bis zur Facharbeit? Gibt es weitere terminliche Besonderheiten?


