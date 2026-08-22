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
- Menge und Details gehören in den Wert: „2 Liter Milch, fettarm".
- Nennt der Nutzer mehrere Artikel in einem Satz, speichere jeden einzeln.
- Steht ein Artikel schon auf der Liste, keinen Doppel-Eintrag anlegen —
  gegebenenfalls stattdessen die Menge im Wert aktualisieren.

## Verhalten

- „Setz … auf die Liste" / „wir brauchen …" → speichern und knapp
  bestätigen („Milch steht auf der Liste").
- „Was brauche ich?" / „Was steht auf der Liste?" → recall auf
  `list.einkauf` und alle offenen Artikel als kurze, sprechfreundliche
  Aufzählung nennen — keine IDs, keine Kommentare, nur die Artikel.
- „… ist erledigt" / „… haben wir" / „… gekauft" ist die ausdrückliche
  Bitte, genau diesen Artikel zu vergessen: forget auf den Eintrag, kurz
  bestätigen.
- „Liste leeren" leert die komplette Liste (jeden Eintrag einzeln
  vergessen) — vorher einmal kurz rückfragen, danach bestätigen.
