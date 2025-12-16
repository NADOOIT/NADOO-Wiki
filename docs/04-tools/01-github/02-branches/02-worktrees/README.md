# <p align="center">Git Worktrees</p>

Git Worktrees ermöglichen es, **mehrere Arbeitsverzeichnisse (Checkouts)** desselben Repositories parallel zu nutzen.
Das ist besonders nützlich, wenn mehrere Personen oder Agenten gleichzeitig an unterschiedlichen Features arbeiten.

---

## Warum Worktrees nutzen?

- **Parallele Arbeit ohne Konflikte:** Jede Aufgabe / jeder Agent bekommt einen eigenen Ordner.
- **Saubere Trennung:** Ein Worktree pro Issue/Branch reduziert das Risiko, im falschen Ordner zu speichern.
- **Schnell & ressourcenschonend:** Worktrees teilen sich das `.git`-Objekt-Repository (kein Full-Clone nötig).

---

## Unser Standard-Workflow (Team/Agenten)

1. **Issue erstellen** (GitHub)
2. **Issue zuweisen** (Assignee setzen)
3. **Feature-Branch** erstellen: `feature/<issue>-<slug>`
4. **Worktree anlegen** (ein Worktree pro Issue / pro Agent)
5. **Änderungen nur im Worktree** durchführen
6. **Pull Request** erstellen, Review, Merge
7. **Worktree entfernen** und aufräumen

### Pfad-Convention (Repo-spezifisch)

- **NADOO-Launchpad:** `~/Documents/GitHub/launchpad-worktrees/<issue>-<slug>`
- **NADOO-Wiki:** `~/Documents/GitHub/wiki-worktrees/issue-<issue>-<slug>`

---

## Standard-Kommandos

### Worktrees anzeigen

```bash
git worktree list
```

### Worktree für einen neuen Feature-Branch anlegen

```bash
git fetch origin

git worktree add -b feature/<issue>-<slug> \
  ~/Documents/GitHub/<repo>-worktrees/issue-<issue>-<slug> \
  origin/main
```

### Beispiel: NADOO-Wiki

```bash
git fetch origin

git worktree add -b feature/742-git-worktrees \
  ~/Documents/GitHub/wiki-worktrees/issue-742-git-worktrees \
  origin/main
```

### Beispiel: NADOO-Launchpad

```bash
git fetch origin

git worktree add -b feature/<issue>-<slug> \
  ~/Documents/GitHub/launchpad-worktrees/<issue>-<slug> \
  origin/main
```

### Worktree entfernen (nach Merge)

```bash
git worktree remove ~/Documents/GitHub/<repo>-worktrees/issue-<issue>-<slug>
```

### Aufräumen (verwaiste Worktrees entfernen)

```bash
git worktree prune
```

---

## Best Practices / Stolperfallen

- **Ein Worktree = ein Branch:** Ein Branch kann nicht gleichzeitig in zwei Worktrees ausgecheckt sein.
- **Nicht im falschen Ordner speichern:** IDE/Terminal immer auf den Worktree-Pfad ausrichten.
- **Nach Merge aufräumen:** Worktree entfernen und ggf. lokale Branches löschen.
- **Keine "Debug-Skripte" einchecken:** Einmalige Hilfsskripte nur lokal nutzen und vor PR entfernen.

---

## Agenten-Workflow (Interview → Issue → Worktree → Prompt)

Wenn wir mit mehreren Agenten parallel arbeiten, sollte die Arbeit pro Feature/Issue immer in einem **dedizierten Worktree** stattfinden.

1. **Interview/Notizen (Audio oder Text)** sammeln
2. **Issue erstellen** + **Assignee setzen**
3. **Branch** `feature/<issue>-<slug>` erstellen
4. **Worktree** anlegen (Pfad-Convention beachten)
5. **Handoff-Prompt** an einen Agenten geben, der ausschließlich in diesem Worktree arbeitet

### Handoff-Prompt Template

- **Issue:** <link>
- **Branch:** `feature/<issue>-<slug>`
- **Worktree-Pfad:** `<absoluter_pfad_zum_worktree>`
- **Ziel:** <1 Satz>
- **Akzeptanzkriterien:**
  - <...>
  - <...>
- **Nicht anfassen:**
  - keine Änderungen außerhalb des Worktree-Pfads
  - keine parallelen Harness-Tests (wenn Git-State betroffen ist)
- **Build/Test:** <z.B. `pytest -k ...` / `cargo build`>

Der Agent liefert am Ende:
- Liste der geänderten Dateien
- kurze Begründung der Lösung
- Hinweise, wie man testet

### Copy/Paste Prompt (z.B. für GPT‑5.2 X‑High Reasoning)

```text
Rolle: Senior Engineering Agent (konservativ, sauberer Git-Workflow)

WICHTIG:
- Arbeite ausschließlich im folgenden Worktree-Pfad:
  <ABSOLUTER_WORKTREE_PFAD>
- Nichts außerhalb dieses Ordners ändern oder speichern.
- Erstelle keine Einmal-Skripte im Repo. Falls du temporäre Hilfsdateien brauchst, nutze lokale/temporäre Pfade und entferne sie vor PR.

Start-Check:
1) Führe `git status -sb` aus und bestätige Branch + sauberen Status.
2) Wenn du nicht auf dem erwarteten Branch bist, stoppe und frage nach.

Aufgabe:
- Issue: <ISSUE_LINK>
- Ziel: <1 Satz>
- Akzeptanzkriterien:
  - <...>
  - <...>

Definition of Done:
- Änderungen sind minimal und nachvollziehbar.
- Lokale Checks/Build sind grün (sofern angegeben).
- Ergebnis enthält:
  - kurze Zusammenfassung
  - Liste der geänderten Dateien
  - Test-/Run-Anleitung
```

---

<p align="center">
<a href="/docs/04-tools/01-github/02-branches/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/01-github/02-branches/01-protection/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/01-github/02-branches/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
