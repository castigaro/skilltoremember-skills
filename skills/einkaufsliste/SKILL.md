---
name: einkaufsliste
description: Führt eine Einkaufsliste im Gedächtnis — auf Handy und Uhr dieselbe. „Setz Milch auf die Liste", „Was brauche ich?", „Milch ist erledigt".
---

# Einkaufsliste

Eine Einkaufsliste, die im Gedächtnis lebt: unterwegs an der Uhr diktiert,
im Laden am Handy oder Handgelenk abgefragt — überall dieselbe Liste.
Voraussetzung ist ein verbundenes Gedächtnis-Repo.

## Ablage

- Ein Eintrag pro Artikel: layer `sem`, topic `list.einkauf.<artikel>`
  (Artikelname klein und einfach, z. B. `list.einkauf.milch`), salience 0.6.
  Der letzte Topic-Teil ist IMMER der Artikelname selbst — nie ein anderes
  Wort in den Wert eines fremden Topics schreiben.
- Menge und Details gehören in den Wert: „2 Liter Milch, fettarm".
- Nennt der Nutzer mehrere Artikel in einem Satz, speichere jeden einzeln
  (je ein remember-Aufruf); die App bündelt den Abgleich selbst.
- Steht ein Artikel schon auf der Liste und ändert sich Menge oder Detail:
  ERST den alten Eintrag per forget auf seine ID vergessen (die ID steht im
  recall-Ergebnis vor jedem Treffer), DANN neu speichern. Nur den Wert neu
  zu speichern legt sonst einen zweiten Eintrag daneben.

## Verhalten

- „Setz … auf die Liste" / „wir brauchen …" → per remember speichern und
  erst NACH dem erfolgreichen Aufruf knapp bestätigen („Milch steht auf
  der Liste"). Niemals bestätigen, ohne gespeichert zu haben.
- „Was brauche ich?" / „Was steht auf der Liste?" → recall auf topic
  `list.einkauf` mit `limit: 50` und `bump: false` — die Liste soll
  vollständig kommen, und bloßes Vorlesen ist kein Wiederlernen. Alle
  offenen Artikel als kurze, sprechfreundliche Aufzählung nennen — keine
  IDs, keine Kommentare, nur die Artikel.
- „… ist erledigt" / „… haben wir" / „… gekauft" ist die ausdrückliche
  Bitte, genau diesen Artikel zu vergessen: forget auf den Eintrag, kurz
  bestätigen.
- „Liste leeren" leert die komplette Liste (jeden Eintrag einzeln
  vergessen) — vorher einmal kurz rückfragen, danach bestätigen.
