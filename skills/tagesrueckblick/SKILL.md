---
name: tagesrueckblick
description: Kurzer Abend-Dialog — du erzählst, wie der Tag war, die KI destilliert das Wesentliche ins Gedächtnis und liefert später Wochen- oder Monatsrückblicke.
---

# Tagesrückblick

Ein kurzes Abendritual: Der Nutzer erzählt vom Tag, du hörst zu, fragst
sparsam nach und destillierst das Wesentliche ins Gedächtnis. Voraussetzung
ist ein verbundenes Gedächtnis-Repo.

## Der Dialog

- Startet mit „Tagesrückblick", „so war mein Tag" oder Ähnlichem. Stelle
  höchstens zwei kurze Nachfragen — etwa „Was war heute gut?" und „Was hat
  dich beschäftigt?". Kein Verhör, kein Fragenkatalog.
- Im Sprachdialog besonders knapp bleiben: Zuhören ist wichtiger als Reden.

## Ablage

- Ein Eintrag pro Tag: layer `epi`, topic `journal.<jjjj-mm-tt>` — das
  heutige Datum steht im System-Prompt. Salience 0.5.
- Der Wert ist die Essenz in ein bis zwei Sätzen, inklusive Grundstimmung:
  „Guter Tag: Projekt abgeschlossen, abends entspannt; Rückenschmerzen
  besser." Kein Protokoll, keine Uhrzeiten-Liste.
- Sticht etwas heraus, das für sich genommen merkwürdig ist (eine
  Entscheidung, ein besonderes Ereignis, eine neue Vorliebe), speichere es
  zusätzlich als eigenen Eintrag mit passendem Topic — nach den Regeln des
  Gedächtnis-Skills.

## Rückblicke

- „Wie war meine Woche?" / „Wie war mein Monat?" → recall auf `journal`,
  die betreffenden Tage zusammenfassen und Muster benennen: wiederkehrende
  Themen, Stimmungsverlauf, was besser geworden ist.
- Ehrlich bleiben: Tage ohne Eintrag sind Lücken, keine schlechten Tage.
