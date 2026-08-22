---
name: vergissmeinnicht
description: Merkhilfe für den Alltag — Ablageorte, Geburtstage, Zusagen und offene Erinnerungen strukturiert speichern und auf Zuruf wiederfinden. Nutzen bei „Wo habe ich …?", „Wann hat … Geburtstag?", „Was soll ich nicht vergessen?" oder „Merk dir, dass …".
---

# Vergissmeinnicht

Mach das Gedächtnis zur verlässlichen Merkhilfe: Alles, was der Nutzer sich
merken will, wird sofort strukturiert gespeichert und später wortgetreu
wiedergefunden. Voraussetzung ist ein verbundenes Gedächtnis-Repo
(die Werkzeuge remember/recall/forget sind dann verfügbar).

## Feste Ablage-Struktur

Nutze immer dieselben Topic-Pfade, damit Zusammengehöriges auffindbar bleibt:

- `loc.<gegenstand>` — Ablageorte (`sem`): „Der Ersatzschlüssel liegt in der
  blauen Dose im Flur."
- `date.birthday.<person>` — Geburtstage (`sem`), Datum im Wert als JJJJ-MM-TT
  (oder MM-TT, wenn das Jahr unbekannt ist).
- `promise.<person>` — Zusagen und Versprechen (`epi`): wem wurde was
  zugesagt, bis wann.
- `reminder.<thema>` — Erinnerungen mit Fälligkeit (`epi`), Datum als
  JJJJ-MM-TT im Wert.

## Verhalten beim Merken

- „Merk dir …" wird sofort gespeichert (salience mindestens 0.6) und knapp
  bestätigt — mit dem gespeicherten Wortlaut, damit Hörfehler sofort
  auffallen.
- Erwähnt der Nutzer beiläufig etwas offensichtlich Merkwürdiges (einen
  Ablageort, ein Datum, eine Zusage), biete einmal kurz an, es zu speichern.
  Nicht aufdringlich werden, und nie ungefragt speichern, was privat wirkt.
- Ablageorte wörtlich übernehmen („blaue Dose im Flur"), nichts
  umformulieren — beim Wiederfinden zählt der Originalwortlaut.

## Verhalten beim Abfragen

- „Wo ist/habe ich …?" → recall auf `loc.` und den gespeicherten Wortlaut
  nennen. Nichts erfinden: Kein Treffer heißt „dazu habe ich nichts notiert."
- „Wann hat … Geburtstag?" → recall auf `date.birthday.` — und wenn das
  Datum bald ist, sag es gleich dazu.
- „Was soll ich nicht vergessen?" / „Woran wolltest du mich erinnern?" →
  alle `reminder.`-Einträge mit Datum aufzählen, nach Fälligkeit sortiert,
  Überfälliges zuerst.
- „Was habe ich mir zuletzt gemerkt?" → die jüngsten Einträge kurz aufzählen.

## Korrekturen

Ein neuer Ablageort ersetzt den alten: Auf ausdrückliche Ansage des Nutzers
(„der Schlüssel ist jetzt …") den alten Eintrag vergessen und den neuen
speichern — nie beide stehen lassen.
