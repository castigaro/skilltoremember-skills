# SkillToRemember — Skill-Bibliothek

Fertige Skills für [SkillToRemember](https://appsonar.de/apps/skilltoremember.html),
den KI-Chat mit Gedächtnis. Jeder Skill ist eine `SKILL.md` im Format des
Agent-Skills-Standards (YAML-Frontmatter mit `name` und `description`,
danach die Anleitung) und nutzt das Gedächtnis der App — ein verbundenes
Gedächtnis-Repo ist also Voraussetzung.

## Skills installieren

**Einzeln:** Im [Release „latest"](../../releases/latest) die ZIP des
gewünschten Skills herunterladen, dann in der App: Skills → ⋮ →
„ZIP importieren". Alternativ `alle-skills.zip` für die komplette Bibliothek.

**Alles auf einmal, direkt von GitHub:** Oben rechts „Code → Download ZIP" —
auch dieses Archiv versteht der Import der App.

Nach dem Import sind die Skills in der Skill-Liste aktivierbar; der Chat
lädt sich ihre Anleitung bei Bedarf selbst nach.

## Die Skills

| Skill | Kurzbeschreibung |
| --- | --- |
| **vergissmeinnicht** | Merkhilfe für den Alltag: Ablageorte, Geburtstage, Zusagen, offene Erinnerungen — strukturiert gespeichert, auf Zuruf wiedergefunden. |
| **einkaufsliste** | Eine Einkaufsliste im Gedächtnis — auf Handy und Uhr dieselbe. Diktieren, abfragen, abhaken. |
| **tagesrueckblick** | Kurzes Abendritual: erzählen, wie der Tag war; später Wochen- und Monatsrückblicke mit Mustern. |
| **geschenke-merker** | Sammelt übers Jahr beiläufig erwähnte Geschenkideen pro Person — zum Anlass wieder abrufbar. |

## Eigene Skills beitragen

Neuer Ordner unter `skills/<name>/` mit einer `SKILL.md` (Frontmatter:
`name` und `description` jeweils einzeilig). Beim nächsten Push auf `main`
baut die CI automatisch die Einzel-ZIPs und aktualisiert das Release.

## Lizenz

Copyright © 2026 Torsten Klein

Dieses Projekt steht unter der **GNU Affero General Public License v3.0 oder
später** (AGPL-3.0-or-later), siehe [LICENSE](LICENSE): Wer die Skills — auch
verändert — weiterverbreitet, muss sie unter derselben Lizenz offenlegen.
Eine kommerzielle Lizenz ist auf Anfrage möglich.
