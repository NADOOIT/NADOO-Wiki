# Praktikanten-Quest-Workflow

Der **Praktikanten-Quest-Workflow** beschreibt, wie wir aus einer Idee oder einem Bug ein lehrreiches, gut strukturiertes Projekt für Praktikant:innen machen.

Ziel:

- Praktikant:innen haben einen klaren Einstieg in echte Projekte (Launchpad, Sir-Nadoo, Academy, Wiki).
- Jede Quest erzeugt **Doku mit Lehrcharakter** (Junior-Level, mit Glossar, UML/SQL-Ankern).
- Aus der Arbeit entstehen neue **Sidequests** (Issues), die weitere Lernchancen eröffnen.

---

## 1. Master-Issue anlegen

1. Ausgangspunkt wählen (Idee, Bug, Kundenwunsch, interner Bedarf).
2. Master-Issue im passenden Repo anlegen (typisch: NADOO-Launchpad):
   - Titel im Stil: `Quest: <kurze Beschreibung>`
   - Inhalt:
     - **Hintergrund** (woher kommt die Idee?)
     - **Problem / Bedarf**
     - **Zielbild** (User-Sicht + Ausbildungs-Sicht)
     - **Nicht-Ziele / Abgrenzung**
   - Quelle verlinken (Meeting-Notizen, Discord-Thread, E-Mail, Screenshot …).
3. Sinnvolle Labels vergeben, z.B. `quest`, `intern`, `onboarding`, `teaching`.

Das Master-Issue ist der Anker für **Branch**, **Projektordner** und alle späteren Sidequests.

---

## 2. Branch und Projektordner im Launchpad

Wir nutzen `NADOO-Launchpad/agent/projects` als Sammelstelle für Projekt-Dokumentation.

1. Branch erstellen:
   - `quest/<issue-id>-<kurzer-slug>`
   - Beispiel: `quest/234-berichtsheft-aus-discord`.
2. Projektordner anlegen:
   - `agent/projects/<issue-id>_<kurzer-slug>/`
   - Beispiel: `agent/projects/234_berichtsheft_discord/`.
3. **An der Struktur von `agent/projects/outbox_timeline` orientieren** (bewährtes Beispiel):
   - `README.md` – Einstieg für Junior-Dev (Ziel, Scope, Lernziele)
   - `01_interview_template.md` / Interview-Notizen
   - `02_flichtenheft.md`
   - `03_technical_design.md`
   - `04_ui_ux_design.md`
   - `05_process_report.md`
   - weitere projektbezogene Artefakte (z.B. RFCs, Risikoanalyse, Produktbriefing)

Im `README.md` wird immer das Master-Issue (`Parent Issue: #<id>`) referenziert.

---

## 3. Interview mit Issue-Ersteller

Bevor eine Praktikantin loslegt, wird der Kontext sauber eingesammelt.

1. Kurzes Interview (Sync oder asynchron) mit der Person, die die Idee eingebracht hat.
2. Antworten dokumentieren (z.B. in `01_interview_template.md` oder `context.md`):
   - Warum ist dieses Projekt wichtig (für Kund:innen / Team / System)?
   - Welche Ergebnisse wünschen wir uns?
   - Welche Randbedingungen gelten (Tech-Stack, Performance, Datenschutz …)?
   - Gibt es ähnliche bestehende Features oder Code-Stellen?
3. `02_flichtenheft.md` und `03_technical_design.md` anhand des Interviews ausarbeiten.

Ziel: Eine Junior-Entwicklerin soll nach Lesen der Doku **ohne direkte Rückfrage** loslegen können.

---

## 4. Lehr-Doku für Junior-Entwickler:innen

Doku ist nicht nur für uns, sondern hat explizit **Lehrcharakter**:

- Sprache: einfach, klar, ohne unnötigen Jargon.
- Fachbegriffe sofort erklären (Glossar / Wortkatalog aufbauen).
- Konkrete Beispiele geben (Befehle, Workflows, typische Stolperfallen).
- **UML-/SQL-Elemente** bewusst einbauen:
  - Klassendiagramm / Sequenzdiagramm (wo sinnvoll)
  - SQL-Skizzen oder Beispielabfragen für neue Tabellen/Views
- Bezug zum **Berichtsheft** herstellen:
  - Welche Tätigkeiten lassen sich als Berichtsheft-Einträge nutzen?

Je mehr Wiedererkennung es zwischen Projekten gibt, desto leichter lernen Praktikant:innen Struktur.

---

## 5. Quest für Praktikant:innen „öffnen“

Wenn Projektordner und Grund-Doku stehen:

1. Master-Issue aktualisieren:
   - Link zum Projektordner
   - Kurz-Überblick: welche Dateien besonders wichtig sind
   - konkrete Aufgabenliste für Praktikant:innen (Tests, GUI, Code …)
2. Status kennzeichnen, z.B.:
   - Label `Ready for Praktikant:innen` oder eigener Abschnitt im Issue.
3. Bei größeren Themen:
   - Unter-Issues für Teilaufgaben anlegen (Frontend/Backend/Tests/Doku), alle mit Verweis auf das Master-Issue.

---

## 6. Rolle der Praktikant:innen

Praktikant:innen fokussieren sich auf:

- Schreiben und Erweitern von **Tests**
- Bauen von **GUIs / CLI-Flows** (wo passend)
- Implementieren von **Produktionscode** innerhalb des klar definierten Scopes

Dazu gehört auch, die Doku zu pflegen:

- neue Begriffe → ins Glossar aufnehmen
- geänderte Architektur → in `technical_design`/`architecture` aktualisieren
- neue Randfälle → im Pflichtenheft ergänzen

So lernen sie nicht nur Coding, sondern auch **saubere Software-Projektarbeit**.

---

## 7. Sidequests: neue Issues aus dem Projekt

Während der Bearbeitung sollen Praktikant:innen bewusst nach **Sidequests** suchen:

- "Das wäre ein eigenes, kleines Feature"
- "Hier könnte man die Architektur verbessern"
- "Hier fehlen Tests/Doku/Refactoring"

Für jede Sidequest:

1. eigenes Issue anlegen (z.B. Titel `Sidequest: <Thema>`)
2. Parent-Issue referenzieren (`Parent: #<master-issue-id>`)
3. kurz begründen, warum es sich lohnt.

Empfehlung: Sidequests mit Windsurf-Sprachinput + GitHub-MCP erfassen, um **Sprachtraining** und **Issue-Schreibtraining** zu kombinieren.

---

## 8. Review, Merge, Lernmaterial

Am Ende einer Quest:

- Code-Review mit Fokus auf Lesbarkeit, Tests und Robustheit.
- Doku-Review mit Fokus auf Verständlichkeit für Junior-Entwickler:innen.
- Master-Issue schließen und Projektordner ggf. im Wiki/Academy verlinken.
- Relevante Inhalte in **Berichtsheft** und **Wortkatalog** übernehmen.

Der Praktikanten-Quest-Workflow verbindet damit **Produktentwicklung** und **Ausbildung** in einem wiederverwendbaren Muster.
