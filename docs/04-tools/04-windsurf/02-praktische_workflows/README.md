# <p align="center">Praktische Workflows (Slash Commands)</p>

Neben dem theoretischen Verständnis der [Workflows und Automatisierungsprozesse](../01-ueberblick/03-workflows_und_automatisierungsprozesse/README.md) nutzen wir im Alltag standardisierte **Slash Commands** in Windsurf, um Qualität und Konsistenz zu sichern.

## Standard-Prozess (The Golden Path)

Unser Entwicklungsprozess folgt immer dem Schema:
**Issue → Branch → Worktree → Docs → Tests → Implementation → Report**

### Verfügbare Workflows

Diese Befehle können direkt im Chat (Cascade) eingegeben werden:

| Befehl | Beschreibung | Wann nutzen? |
| :--- | :--- | :--- |
| `/create_feature` | Startet ein neues Feature (Issue anlegen, Branch, Worktree, Doku-Skeleton). | **Immer** beim Start einer neuen Aufgabe. |
| `/fix_bug` | Interaktiver Guide zum Beheben von Fehlern (Reproducing Test, Worktree, Docs-First). | Bei der Behebung von Bugs/Issues. |
| `/load_memories` | Importiert/Aktualisiert die Team-Memories (Regeln). | Beim Setup eines neuen Repos oder nach Updates der Regeln. |
| `/create_issue` | Hilft beim Schreiben guter Issue-Beschreibungen (Patchnote-Style). | Wenn noch kein Issue existiert. |
| `/go_green` | Führt Tests aus und hilft beim Fixen, bis alles grün ist. | Vor dem Commit/Push. |
| `/create_release` | Erstellt Release-Notes und aktualisiert Versionen. | Beim Abschluss eines Meilensteins. |

## Detail-Beschreibung der Kern-Workflows

### 1. `/create_feature`
Dieser Workflow ist der **Haupteinstieg**. Er zwingt uns in die saubere Struktur:
1. Fragt nach dem Issue (oder erstellt es).
2. Erstellt den Branch `feature/<id>-<slug>`.
3. Erstellt einen **Worktree**, damit wir isoliert arbeiten.
4. Legt Projekt-Doku an (`01_overview.md`, `02_plan.md`...).
5. **Docs-First:** Erinnert daran, erst die Doku zu schreiben.

### 2. `/fix_bug`
Ähnlich wie Feature, aber fokussiert auf Fehlerbehebung:
1. Erstellt Branch & Worktree.
2. Fordert **Reproducing Test** (muss erst rot sein).
3. Fix implementieren.
4. Test muss grün sein.

### 3. `/load_memories`
Synchronisiert das "Gehirn" von Windsurf. Lädt Regeln wie:
- Keine stillen Fehler (Tracebacks loggen).
- Trennung von Logic (`functions/`) und UI (`classes/`).
- Test-Pflicht.

---

<p align="center">
<a href="../01-ueberblick/03-workflows_und_automatisierungsprozesse/README.md"><strong>Zurück: Theorie</strong></a> | 
<a href="../../README.md"><strong>Zurück zur Übersicht</strong></a>
</p>
