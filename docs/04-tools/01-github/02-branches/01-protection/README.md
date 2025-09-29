# <p align="center">GitHub Branch Protection: Sicherheit und Qualität im Entwicklungsprozess</p>

## Einführung

Branch Protection in GitHub ist ein mächtiges Werkzeug, um die Integrität und Qualität des Codes in einem Repository zu gewährleisten. Dieser Wiki-Beitrag erklärt, warum und wie wir Branches schützen sowie die verschiedenen Einstellungsmöglichkeiten und ihre Auswirkungen auf den Entwicklungsprozess.

## Warum Branches schützen?

Branchschutz bietet mehrere Vorteile:

1. **Qualitätssicherung**: Erzwingt Code-Reviews und verhindert direkte Änderungen an wichtigen Branches.
2. **Konsistenz**: Gewährleistet einheitliche Entwicklungspraktiken im gesamten Team.
3. **Sicherheit**: Schützt vor versehentlichen oder unbefugten Änderungen.
4. **Transparenz**: Fördert offene Kommunikation und Zusammenarbeit im Entwicklungsprozess.

## Einrichten von Branch Protection Rules

Um Branch Protection Rules einzurichten, folge diesen Schritten:

1. Navigiere zu deinem Repository auf GitHub.
2. Klicke auf "Settings" in der oberen Menüleiste.
3. Wähle "Branches" in der linken Seitenleiste.
4. Unter "Branch protection rules" klicke auf "Add rule".
5. Gib den Branch-Namen ein, den du schützen möchtest (z.B. "main").
6. Konfiguriere die gewünschten Schutzregeln.

## Wichtige Branch Protection Rules

### Require pull request before merging
- **Menüname**: "Require a pull request before merging"
- **Beschreibung**: Erzwingt, dass Änderungen über Pull Requests eingebracht werden müssen.
- **Empfehlung**: Aktivieren, um Code-Reviews zu fördern.

### Required number of approvals
- **Menüname**: "Required approvals"
- **Beschreibung**: Legt fest, wie viele Genehmigungen ein Pull Request benötigt.
- **Empfehlung**: Mindestens 1, idealerweise 2 für wichtige Branches.

### Dismiss stale pull request approvals
- **Menüname**: "Dismiss stale pull request approvals when new commits are pushed"
- **Beschreibung**: Setzt Genehmigungen zurück, wenn neue Commits gepusht werden.
- **Empfehlung**: Aktivieren, um sicherzustellen, dass die neuesten Änderungen überprüft werden.

### Require status checks to pass
- **Menüname**: "Require status checks to pass before merging"
- **Beschreibung**: Erfordert erfolgreiche CI/CD-Checks vor dem Mergen.
- **Empfehlung**: Aktivieren, wenn CI/CD-Pipelines vorhanden sind.

### Restrict who can push
- **Menüname**: "Restrict who can push to matching branches"
- **Beschreibung**: Begrenzt, wer direkt in den Branch pushen kann.
- **Empfehlung**: Aktivieren und auf Administratoren beschränken.

## Potenzielle Herausforderungen

- **Verzögerungen**: Strenge Regeln können den Entwicklungsprozess verlangsamen.
- **Komplexität**: Neue Teammitglieder müssen sich an den Prozess gewöhnen.
- **Overhead**: Erhöhter Verwaltungsaufwand für Code-Reviews und Pull Requests.

## Best Practices

1. Passe die Regeln an die Bedürfnisse deines Teams und Projekts an.
2. Schule alle Teammitglieder in den festgelegten Prozessen.
3. Überprüfe und aktualisiere die Regeln regelmäßig.
4. Balanciere Sicherheit mit Entwicklungsgeschwindigkeit.

## Übung: Branch Protection in der Praxis

Als Teil des Onboarding-Prozesses empfehlen wir folgende Übung:

1. Richte Branch Protection für den main-Branch deiner ersten Übungs-App ein.
2. Konfiguriere mindestens drei verschiedene Schutzregeln.
3. Bitte deine Lernpartner zu versuchen, eine der Regeln zu brechen (z.B. direkter Push auf main).
4. Diskutiere die Ergebnisse und Erfahrungen im Team.

Diese praktische Übung hilft, die Wichtigkeit und Funktionsweise von Branch Protection zu verstehen und fördert gleichzeitig die Zusammenarbeit im Team.

---

<p align="center">
<a href="/docs/04-tools/01-github/02-branches/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/01-github/03-pull-requests/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/01-github/02-branches/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>

---

<details>
<summary>Kompletten Themenbereich anzeigen</summary>
<br>

🟦 [**Du befindest dich im Themenbereich: Tools und Technologien**](/docs/04-tools/README.md)

---

📄 [zum Thema **Versionsverwaltung mit GitHub:**](/docs/04-tools/01-github/README.md) 

  &nbsp;&nbsp;🔹 [**Repository**](/docs/04-tools/01-github/01-repository/README.md) <br>
  &nbsp;&nbsp;🔹 [**Branches**](/docs/04-tools/01-github/02-branches/README.md) <br>
    &emsp;&emsp;◻️ [GitHub Branch Protection: Sicherheit und Qualität im Entwicklungsprozess](/docs/04-tools/01-github/02-branches/01-protection/README.md) <br>

  &nbsp;&nbsp;🔹 [**Pull Requests**](/docs/04-tools/01-github/03-pull-requests/README.md) <br>
    &emsp;&emsp;◻️ [Merge Konflikte](/docs/04-tools/01-github/03-pull-requests/01-merge-konflikte/README.md) <br>
    &emsp;&emsp;◻️ [Code Reviews](/docs/04-tools/01-github/03-pull-requests/02-code-review/README.md) <br>

  &nbsp;&nbsp;🔹 [**Issues**](/docs/04-tools/01-github/04-issues/README.md) <br>
    &emsp;&emsp;◻️ [Selbstständig Veränderungen innerhalb des Wikis vornehmen: ein kleiner Guide](/docs/04-tools/01-github/04-issues/01-wiki-guide/README.md) <br>
    &emsp;&emsp;◻️ [Labels](/docs/04-tools/01-github/04-issues/02-labels/README.md) <br>
    &emsp;&emsp;◻️ [Types](/docs/04-tools/01-github/04-issues/03-types/README.md) <br>
    &emsp;&emsp;◻️ [Assignees](/docs/04-tools/01-github/04-issues/04-assignees/README.md) <br>
    &emsp;&emsp;◻️ [Milestones](/docs/04-tools/01-github/04-issues/05-milestones/README.md) <br>
    &emsp;&emsp;◻️ [Projects](/docs/04-tools/01-github/04-issues/06-projects/README.md) <br>
      &emsp;&emsp;&emsp;▪ [Fokus: Zeitplanung und Meilensteine mit GitHub Projects](/docs/04-tools/01-github/04-issues/06-projects/01-zeitplanung/README.md) </br>
    &emsp;&emsp;◻️ [Discussions](/docs/04-tools/01-github/04-issues/07-discussions/README.md) <br>
    &emsp;&emsp;◻️ [Templates](/docs/04-tools/01-github/04-issues/08-templates/README.md) <br>

  &nbsp;&nbsp;🔹 [**Actions**](/docs/04-tools/01-github/05-actions/README.md) <br>
  &nbsp;&nbsp;🔹 [**GitHub-Notifications und Visual Studio Code**](/docs/04-tools/01-github/06-notifications/README.md) <br>
  &nbsp;&nbsp;🔹 [**Die GitHub-Suchfunktion effizient nutzen**](/docs/04-tools/01-github/07-suche/README.md) <br>
  &nbsp;&nbsp;🔹 [**Markdown**](/docs/04-tools/01-github/08-markdown/README.md) <br>

  &nbsp;&nbsp;🔹 [**Organisationen und Teams auf GitHub**](/docs/04-tools/01-github/09-organizations-teams/README.md) </br>
    &emsp;&emsp;◻️[**Schritt-für-Schritt-Anleitung zur NADOO-IT-Organisation und den Teams auf GitHub**](/docs/04-tools/01-github/09-organizations-teams/01-nadooit-guide/README.md) </br><br>

  &nbsp;&nbsp;🔹 [**GitHub Einführung (Video)**](/docs/04-tools/01-github/10-github-einfuehrung/README.md) </br>
#
📄 [zum Thema **Integrierte Entwicklungsumgebung (IDE) Visual Studio Code**](/docs/04-tools/02-vscode/README.md) <br>

  &nbsp;&nbsp;🔹 [Installation und Einrichtung](/docs/04-tools/02-vscode/01-installation/README.md) <br>
  &nbsp;&nbsp;🔹 [Plugins und Erweiterungen](/docs/04-tools/02-vscode/02-plugins/README.md) <br>
  &nbsp;&nbsp;🔹 [Workspaces (Arbeitsbereiche)](/docs/04-tools/02-vscode/03-workspaces/README.md) <br>
  &nbsp;&nbsp;🔹 [Editorfunktionen und IntelliSense](/docs/04-tools/02-vscode/04-editor/README.md) <br>
  &nbsp;&nbsp;🔹 [Terminal und Debugging](/docs/04-tools/02-vscode/05-debugging/README.md) <br>
#
📄 [zum Thema **Integrierte Entwicklungsumgebung (IDE) für Java: IntelliJ IDEA**](/docs/04-tools/03-intellij/README.md) <br>

  &nbsp;&nbsp;🔹 [IntelliJ IDEA — ein Überblick](/docs/04-tools/03-intellij/01-ueberblick/README.md) <br>
  &nbsp;&nbsp;🔹 [Installation und Einrichtung](/docs/04-tools/03-intellij/02-installation/README.md) <br>
#
  &nbsp;&nbsp;🔹 [Das Terminal — die Grundlagen](/docs/04-tools/04-terminal/README.md) <br>
#
📄 [zum Thema **Das NADOO-Launchpad — was es kann und wie es funktioniert**](/docs/04-tools/05-launchpad/README.md) <br>

  &nbsp;&nbsp;🔹 [**Das NADOO-Launchpad - ein grundlegender Überblick**](/docs/04-tools/05-launchpad/01-ueberblick/README.md) <br>
    &emsp;&emsp;◻️ [Installation [Windows]](/docs/04-tools/05-launchpad/01-ueberblick/01-windows/README.md) <br>
    &emsp;&emsp;◻️ [Installation [MAC]](/docs/04-tools/05-launchpad/01-ueberblick/02-mac/README.md) <br>

  &nbsp;&nbsp;🔹 [**Der Launchpad-Feature-Guide: Funktions- und Anwendungsweise aller Features und Komponenten**](/docs/04-tools/05-launchpad/02-features/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Menüleiste](/docs/04-tools/05-launchpad/02-features/01-menu/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Berechtigungen](/docs/04-tools/05-launchpad/02-features/02-berechtigungen/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Tokens](/docs/04-tools/05-launchpad/01-guide/03-tokens/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Erfassung der Arbeitszeiten](/docs/04-tools/05-launchpad/02-features/04-zeiterfassung/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Projektverwaltung](/docs/04-tools/05-launchpad/02-features/05-projektverwaltung/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Aktivitäten](/docs/04-tools/05-launchpad/02-features/06-aktivitaeten/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Wochenübersicht](/docs/04-tools/05-launchpad/02-features/07-wochenuebersicht/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Watchdog](/docs/04-tools/05-launchpad/02-features/08-watchdog/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Create Snippets](/docs/04-tools/05-launchpad/02-features/09-create_snippets/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Function Names](/docs/04-tools/05-launchpad/02-features/10-function_names/README.md) <br>
    &emsp;&emsp;◻️ [[Feature-Guide] Tokens versenden](/docs/04-tools/05-launchpad/02-features/11-t_bar_senden/README.md) <br>

  &nbsp;&nbsp;🔹 [**Video-Tutorials und Demonstrationen**](/docs/04-tools/05-launchpad/03-videos/README.md) <br>
#
📄 [zum Thema **Künstliche Intelligenz (KI)**](/docs/04-tools/06-ki/README.md) <br>

  &nbsp;&nbsp;🔹 [KI‐Nutzung: Ein umfassender Leitfaden](/docs/04-tools/06-ki/01-leitfaden/README.md) <br>
  &nbsp;&nbsp;🔹 [Large Language Model (LLM) und das Apple MLX (MacOS Silicon) Framework — ein Vergleich](/docs/04-tools/06-ki/02-llm-mlx/README.md) <br>
  &nbsp;&nbsp;🔹 [Nutzung der Gemini API – eine Anleitung](/docs/04-tools/06-ki/03-gemini/README.md) <br>

</details>