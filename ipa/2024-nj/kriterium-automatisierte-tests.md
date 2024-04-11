# Bezeichnung
Automatisierte Tests mit rspec

# Definition (Leitfrage)
Eine gute Testabdeckung ist essenziell für zuverlässige Features und eine gute Code-Qualität

## Gütestufe 3
1. Die Anforderungen sind mit genügend Unit-Tests abgedeckt
2. Es sind Controller, Integrations oder wo sinnvoll Feature (end-to-end) Tests vorhanden
3. Der Projektstandard wird bei den Tests eingehalten

### Ergänzung
- 1.1 Es gibt in beiden Wagons mind. 1 neuen Unit Test-Case (it block) der die spezifizierte Wagon-Erweiterbarkeit testet
- 1.2 Die bestehenden Sphinx Search Strategy Test Cases der Entität Person/Group laufen durch oder wurden durch neue Test Files sowie Cases ersetzt
- 2.1 Es gibt mind. 1 neuen Feature Test im Core der den kompletten Stack von der User-Eingabe zur DB bis zur Anzeige der Suchresultate testet (Person oder Group)
- 2.2 Die FullTextController Specs wurde angepasst und die bestehenden Test Cases für die Entität Person/Group laufen durch
- 2.3 Tests die Aufgrund der noch nicht vollständigen Migration zu Postgresql failen sind entsprechend skipped und kommentiert, der Build läuft komplett durch/ist grün

Neuer Test heisst hier auch der Ersatz/Umschreiben von bestehenden Tests die nach dem Umbau angepasst werden müssen

## Gütestufe 2
Zwei Aspekte sind gut erfüllt

## Gütestufe 1
Ein Aspekt ist gut erfüllt

## Gütestufe 0
Kein Aspekt ist gut erfüllt
