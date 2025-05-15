# <p align="center">Merge Konflikte</p>


## Merge-Konflikte nach einem Pull-Request auflösen (Best Practice)

Wenn nach einem erfolgreichen Pull-Request Merge-Konflikte entstehen, solltest du wie folgt vorgehen:

### 🔄 Schritt 1: Hole die neuesten Änderungen aus dem Haupt-Repository

```bash
git checkout main
git pull origin main
```

Wenn du mit einem anderen Branch wie `develop` arbeitest, ersetze `main` durch den entsprechenden Namen.

### 🌿 Schritt 2: Wechsle in deinen Feature-Branch und merge in den Haupt-Branch hinein

```bash
git checkout dein-feature-branch
git merge main
```

Nun zeigt dir Git die betroffenen Dateien mit Konflikten an. Öffne diese im Editor.

### 🛠️ Schritt 3: Bearbeite die Konfliktstellen

Git markiert die Konfliktstellen so:

```text
<<<<<<< HEAD
Dein Code
=======
Code aus dem Main-Branch
>>>>>>> main
```

Entferne alle `<<<<<<<`, `=======`, `>>>>>>>` und entscheide, welche Codezeilen übernommen werden sollen. Kombiniere ggf. beide Änderungen sinnvoll.

### ✅ Schritt 4: Markiere die Konflikte als gelöst

```bash
git add <konfliktdatei>
```

Wiederhole diesen Schritt für alle betroffenen Dateien.

### 💾 Schritt 5: Commit der Auflösung

```bash
git commit -m "Merge-Konflikte gelöst"
```

### ⬆️ Schritt 6: Push in deinen Branch

```bash
git push origin dein-feature-branch
```

### 📸 Beispielbild

![Merge-Konflikt im VS Code](/images/github_merge_konflikt.png)

Das Bild zeigt, wie ein Merge-Konflikt im Visual Studio Code aussieht. Du kannst hier bequem beide Seiten vergleichen und die gewünschten Änderungen übernehmen.

---

Damit ist dein Branch bereit für einen erneuten Merge ohne Konflikte.

## Weitere Informationen

[GitHub Docs: merge conflicts](https://docs.github.com/de/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/about-merge-conflicts)

---

<p align="center"><a href="/docs/04-tools/01-github/03-pull-requests/README.md"><strong>Zurück</strong></a> | <a href="/docs/04-tools/01-github/03-pull-requests/02-code-review/README.md"><strong>Weiter</strong></a></p>

