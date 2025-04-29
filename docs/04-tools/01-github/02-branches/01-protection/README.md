# 3.1.2.1 GitHub Branch Protection: Sicherheit und Qualität im Entwicklungsprozess

## Einführung

Branch Protection in GitHub ist ein mächtiges Werkzeug, um die Integrität und Qualität des Codes in einem Repository zu gewährleisten. Dieser Wiki-Beitrag erklärt, warum und wie wir Branches schützen, sowie die verschiedenen Einstellungsmöglichkeiten und ihre Auswirkungen auf den Entwicklungsprozess.

## Warum Branches schützen?

Branchschutz bietet mehrere Vorteile:

1. **Qualitätssicherung**: Erzwingt Code-Reviews und verhindert direkte Änderungen an wichtigen Branches.
2. **Konsistenz**: Gewährleistet einheitliche Entwicklungspraktiken im gesamten Team.
3. **Sicherheit**: Schützt vor versehentlichen oder unbefugten Änderungen.
4. **Transparenz**: Fördert offene Kommunikation und Zusammenarbeit im Entwicklungsprozess.

## Einrichten von Branch Protection Rules

Um Branch Protection Rules einzurichten, folgen Sie diesen Schritten:

1. Navigieren Sie zu Ihrem Repository auf GitHub.
2. Klicken Sie auf "Settings" in der oberen Menüleiste.
3. Wählen Sie "Branches" in der linken Seitenleiste.
4. Unter "Branch protection rules", klicken Sie auf "Add rule".
5. Geben Sie den Branch-Namen ein, den Sie schützen möchten (z.B. "main").
6. Konfigurieren Sie die gewünschten Schutzregeln.

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

1. Passen Sie die Regeln an die Bedürfnisse Ihres Teams und Projekts an.
2. Schulen Sie alle Teammitglieder in den festgelegten Prozessen.
3. Überprüfen und aktualisieren Sie die Regeln regelmäßig.
4. Balancieren Sie Sicherheit mit Entwicklungsgeschwindigkeit.

## Übung: Branch Protection in der Praxis

Als Teil des Onboarding-Prozesses empfehlen wir folgende Übung:

1. Richten Sie Branch Protection für den main-Branch Ihrer ersten Übungs-App ein.
2. Konfigurieren Sie mindestens drei verschiedene Schutzregeln.
3. Bitten Sie Ihren Lernpartner, zu versuchen, eine der Regeln zu brechen (z.B. direkter Push auf main).
4. Diskutieren Sie die Ergebnisse und Erfahrungen im Team.

Diese praktische Übung hilft, die Wichtigkeit und Funktionsweise von Branch Protection zu verstehen und fördert gleichzeitig die Zusammenarbeit im Team.