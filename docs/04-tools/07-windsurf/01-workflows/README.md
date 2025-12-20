# <p align="center">Windsurf Workflows</p>

Wir nutzen standardisierte Workflows in Windsurf, um Qualität und Konsistenz zu sichern. Diese Workflows können direkt im Chat per Slash-Command aufgerufen werden.

## Standard-Prozess

Unser Entwicklungsprozess folgt immer dem Schema:
**Issue → Branch → Worktree → Docs → Tests → Implementation → Report**

### Verfügbare Workflows

| Befehl | Beschreibung | Wann nutzen? |
| :--- | :--- | :--- |
| `/create_feature` | Startet ein neues Feature (Issue anlegen, Branch, Worktree, Doku-Skeleton). | **Immer** beim Start einer neuen Aufgabe. |
| `/fix_bug` | Interaktiver Guide zum Beheben von Fehlern (Reproducing Test, Worktree). | Bei Bugs/Issues. |
| `/load_memories` | Importiert/Aktualisiert die Team-Memories (Regeln). | Beim Setup eines neuen Repos oder nach Updates. |
| `/create_issue` | Hilft beim Schreiben guter Issue-Beschreibungen (Patchnote-Style). | Wenn noch kein Issue existiert. |
| `/go_green` | Führt Tests aus und hilft beim Fixen, bis alles grün ist. | Vor dem Commit/Push. |
| `/create_release` | Erstellt Release-Notes und aktualisiert Versionen. | Beim Abschluss eines Meilensteins. |

## Detail-Beschreibung

### 1. `/create_feature`
Dieser Workflow ist der **Haupteinstieg**. Er zwingt uns in die saubere Struktur:
1. Fragt nach dem Issue (oder erstellt es).
2. Erstellt den Branch `feature/<id>-<slug>`.
3. Erstellt einen **Worktree**, damit wir isoliert arbeiten.
4. Legt Projekt-Doku an (`01_overview.md`, `02_plan.md`...).
5. **Docs-First:** Erinnert daran, erst die Doku zu schreiben.

### 2. `/fix_bug`
Ähnlich wie Feature, aber fokussiert auf Fehlerbehebung:
1. Erstellt Reproducing Test (muss erst rot sein).
2. Fix implementieren.
3. Test muss grün sein.

### 3. `/load_memories`
Synchronisiert das "Gehirn" von Windsurf. Lädt Regeln wie:
- Keine stillen Fehler (Tracebacks loggen).
- Trennung von Logic (`functions/`) und UI (`classes/`).
- Test-Pflicht.

---

<p align="center"><a href="../README.md"><strong>Zurück</strong></a> | <a href="../../../README.md"><strong>Zur Übersicht</strong></a></p>
