# <p align="center">Rebase</p>

## <span style="color: green;">Was ist ein Rebase?</span>

Ein Rebase ist eine Git-Operation, bei der die Commit-Historie eines Branches neu geschrieben wird. Dabei werden die Commits eines Branches auf einen anderen Basis-Commit "umgepflanzt". Das Ergebnis ist eine lineare, saubere Commit-Historie ohne unnötige Merge-Commits.

---

## <span style="color: green;">Visualisierung: Vor und nach dem Rebase</span>

**Vor dem Rebase:**
```
main:    A --- B --- C
                 \
feature:          D --- E --- F
```

**Rebase-Befehl:**
```
git rebase main
```

**Nach dem Rebase:**
```
main:    A --- B --- C
                     \
feature:              D' --- E' --- F'
```

**Erklärung kurz:**

1. Vor dem Rebase sind die Commits der Feature-Branch „D, E, F" ab B abgezweigt.

2. Mit `git rebase main` werden die Feature-Commits oben auf die aktuelle main-Branch gesetzt.

3. Die Historie wird dadurch linear, keine Merge-Commits nötig.



---

## <span style="color: green;">Warum ist Rebase wichtig?</span>

- **Saubere Historie**: Erzeugt eine lineare Commit-Geschichte ohne Merge-Commits.
- **Übersichtlichkeit**: Erleichtert das Nachverfolgen von Änderungen im Projekt.
- **Konfliktlösung**: Ermöglicht es, Konflikte schrittweise bei jedem Commit zu lösen.
- **Pull Request Qualität**: Hält PRs übersichtlich und leichter zu reviewen.
- **Aktualisierung**: Bringt deinen Branch auf den neuesten Stand des Hauptzweigs.

---

## <span style="color: green;">Unterschied zwischen Merge und Rebase</span>

| Aspekt        | Merge                           | Rebase                        |
|---------------|--------------------------------|------------------------------|
| Was ist das?  | Verbindet zwei Branches         | Ordnet Commits neu            |
| Commit-Historie | Bleibt unverändert             | Wird sauber und linear        |
| Wann verwenden? | Bei gemeinsamer Teamarbeit     | Für den eigenen Branch        |
| Kurz gesagt   | „Branches zusammenführen"       | „Historie aufräumen"          |

---

## <span style="color: green;">Ablauf eines Rebase</span>

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

## <span style="color: green;">Tipps für sicheres Rebasen</span>

- **Niemals öffentliche Branches rebasen**: Rebase nur lokale oder eigene Feature-Branches.
- **Backup erstellen**: Erstelle vor dem Rebase einen Backup-Branch.
- **`--force-with-lease` verwenden**: Sicherer als `--force`, da es prüft ob andere Änderungen gepusht wurden.
- **Interaktives Rebase nutzen**: Mit `git rebase -i` kannst du Commits bearbeiten, zusammenfassen oder löschen.

---

## <span style="color: green;">Interaktives Rebase</span>

Interaktives Rebase erlaubt es, die letzten Commits zu bearbeiten (z. B. umbenennen, zusammenfassen oder loschen).

**Befehl**
```bash
git rebase -i HEAD~3
```

**Beispiel im Editor**
```
pick a1b2c3 Login-Formular hinzufugen
squash d4e5f6 Tippfehler beheben
pick g7h8i9 Passwortprufung hinzufugen
```

**Optionen im interaktiven Modus:**
| Befehl | Beschreibung |
|--------|--------------|
| **pick** | Commit beibehalten |
| **reword** | Commit-Nachricht ändern |
| **squash** | Mit vorherigem Commit zusammenfassen |
| **drop** | Commit entfernen |


## <span style="color: yellow;">Ergebnis: Weniger Commits, saubere Historie.</span>
---

## <span style="color: green;">Weitere Informationen</span>

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
