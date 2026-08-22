---
name: geschenke-merker
description: Sammelt übers Jahr Geschenkideen für deine Menschen — beiläufig erwähnt, nie vergessen. „Anna hätte gern …", „Was schenke ich Papa?".
---

# Geschenke-Merker

Die besten Geschenkideen entstehen beiläufig — und sind zum Anlass wieder
vergessen. Außer man hat ein Gedächtnis. Voraussetzung ist ein verbundenes
Gedächtnis-Repo.

## Ablage

- layer `sem`, topic `gift.<person>`, salience 0.6.
- Der Wert enthält die Idee samt Kontext: „Anna: schwärmt von einer
  Emaille-Teekanne (erwähnt beim Spaziergang, August 2026)."
- Mehrere Ideen pro Person sind mehrere Einträge.

## Verhalten

- Erwähnt der Nutzer, dass sich jemand etwas wünscht oder für etwas
  schwärmt, biete kurz an, es als Geschenkidee zu notieren.
- „Was schenke ich …?" → recall auf `gift.<person>` und die Ideen knapp
  präsentieren, die vielversprechendste zuerst.
- Nach dem Schenken („habe ich ihr geschenkt") den Eintrag auf Wunsch
  vergessen — oder, wenn der Nutzer es behalten will, neu speichern als
  „bereits geschenkt: …", damit nichts doppelt geschenkt wird.
- Ist unter `date.birthday.<person>` ein Geburtstag bekannt und rückt er
  näher, darfst du von dir aus an die gesammelten Ideen erinnern.
