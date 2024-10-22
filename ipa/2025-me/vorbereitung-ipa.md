# Vorbereitung IPA

Aufbauend auf dem PoC der Probe-IPA sollen folgende Tasks noch vor der IPA erledigt werden:

## 1. Hitobito Docker Dev Setup

https://github.com/hitobito/development

- Neuer Branch **postgresql**
- Die DBs `hitobito_development` sowie `hitobito_test` werden automatisch beim Hochfahren des PostgreSQL-Containers erstellt falls diese nicht bereits vorhanden sind (analog bisherigem MySQL)
- docker-compose.yml soll MySQL (standardmässig disabled), sowie PostgreSQL als container beinhalten
- ggf Anpassung `./bin` DB-Helper scripts

## 2. Anpassungen Hitobito

- die schema.rb ist für postgresql generiert
- Webapp zum laufen bringen, sprich alle SQL probleme fixen (oft wird es einfach eine ergänzung im SELECT brauchen)
- sämtliche specs laufen mit postgresql (sphinx specs ausgenommen) aber auch mit mysql
- Core/Wagon Seeds
- virtual Attribute einfach mit SQL erstellen und als normales readonly_attr behandeln

## 3. Github CI-Builds

- Github CI-Builds laufen mit postgresql (falls einfacher, auch auf einem fork)

## 4. Cryptopus pg_search PR

- studieren: https://github.com/puzzle/cryptopus/pull/749/files
- rebasen
- local mal testen
- ggf noch ein paar specs ergänzen?
- dem BBT zum Fertigstellen übergeben
