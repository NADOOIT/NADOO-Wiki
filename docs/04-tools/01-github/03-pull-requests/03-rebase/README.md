# <p align="center">Rebase</p>

## Was ist ein Rebase?

Ein Rebase ist eine Git-Operation, bei der die Commit-Historie eines Branches neu geschrieben wird. Dabei werden die Commits eines Branches auf einen anderen Basis-Commit "umgepflanzt". Das Ergebnis ist eine lineare, saubere Commit-Historie ohne unnötige Merge-Commits.

---

## Visualisierung: Vor und nach dem Rebase

**Vor dem Rebase:**
```
main:                A --- B --- C --- D
                          \
feature/user-login:        E --- F --- G
```

**Nach dem Rebase:**
```
main:                A --- B --- C --- D
                                        \
feature/user-login:                      E' --- F' --- G'
```

> Die Commits E, F, G werden auf den neuesten Stand von `main` (Commit D) "umgepflanzt" und erhalten neue Commit-IDs (E', F', G').

---

## Warum ist Rebase wichtig?

- **Saubere Historie**: Erzeugt eine lineare Commit-Geschichte ohne Merge-Commits.
- **Übersichtlichkeit**: Erleichtert das Nachverfolgen von Änderungen im Projekt.
- **Konfliktlösung**: Ermöglicht es, Konflikte schrittweise bei jedem Commit zu lösen.
- **Pull Request Qualität**: Hält PRs übersichtlich und leichter zu reviewen.
- **Aktualisierung**: Bringt deinen Branch auf den neuesten Stand des Hauptzweigs.

---

## Unterschied zwischen Merge und Rebase

| Aspekt | Merge | Rebase |
|--------|-------|--------|
| Historie | Behält alle Branches und Merge-Commits | Lineare Historie ohne Merge-Commits |
| Konflikte | Einmalige Konfliktlösung | Konfliktlösung pro Commit |
| Sicherheit | Originalhistorie bleibt erhalten | Historie wird umgeschrieben |

---

## Ablauf eines Rebase

**Beispiel:** Du arbeitest am Branch `feature/user-login` und möchtest ihn auf den neuesten Stand von `main` bringen.

1. **Aktuellen Branch auschecken**  
   Wechsle zu dem Branch, den du rebasen möchtest:
   ```bash
   git checkout feature/user-login
   ```

2. **Rebase auf den Zielbranch**  
   Führe den Rebase auf den Hauptzweig aus:
   ```bash
   git rebase main
   ```
   
   **Ausgabe bei Erfolg:**
   ```
   Successfully rebased and updated refs/heads/feature/user-login.
   ```

3. **Konflikte lösen (falls vorhanden)**  
   Falls Konflikte auftreten, zeigt Git dir die betroffenen Dateien:
   ```
   CONFLICT (content): Merge conflict in src/login.py
   error: could not apply E... Add login form
   ```
   Löse die Konflikte und fahre fort:
   ```bash
   git add src/login.py
   git rebase --continue
   ```

4. **Force Push (bei bereits gepushten Branches)**  
   Da die Historie neu geschrieben wurde, ist ein Force Push nötig:
   ```bash
   git push --force-with-lease origin feature/user-login
   ```

---

## Tipps für sicheres Rebasen

- **Niemals öffentliche Branches rebasen**: Rebase nur lokale oder eigene Feature-Branches.
- **Backup erstellen**: Erstelle vor dem Rebase einen Backup-Branch.
- **`--force-with-lease` verwenden**: Sicherer als `--force`, da es prüft ob andere Änderungen gepusht wurden.
- **Interaktives Rebase nutzen**: Mit `git rebase -i` kannst du Commits bearbeiten, zusammenfassen oder löschen.

---

## Interaktives Rebase

Mit `git rebase -i HEAD~n` kannst du die letzten n Commits bearbeiten:

```bash
git rebase -i HEAD~3
```

**Beispiel-Ausgabe im Editor:**
```
pick a1b2c3d Add login form
pick e4f5g6h Fix typo in login
pick i7j8k9l Add password validation

# Rebase abc123..i7j8k9l onto abc123 (3 commands)
#
# Commands:
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# s, squash = use commit, but meld into previous commit
# d, drop = remove commit
```

**Optionen im interaktiven Modus:**
| Befehl | Beschreibung |
|--------|--------------|
| **pick** | Commit beibehalten |
| **reword** | Commit-Nachricht ändern |
| **squash** | Mit vorherigem Commit zusammenfassen |
| **drop** | Commit entfernen |

---

## Weitere Informationen

- [GitHub Docs: About Git Rebase](https://docs.github.com/de/get-started/using-git/about-git-rebase)
- [Atlassian: Git Rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)

---

<p align="center">
<a href="/docs/04-tools/01-github/03-pull-requests/02-code-review/README.md"><strong>Zurück</strong></a> |
<a href="/docs/04-tools/01-github/04-issues/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/01-github/03-pull-requests/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
