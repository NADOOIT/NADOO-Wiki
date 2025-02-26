# 3.1.6 GitHub-Notifcations und Visual Studio Code

Um E-Mail-Benachrichtigungen für GitHub so weit wie möglich zu reduzieren oder ganz darauf zu verzichten, lohnt es sich, GitHub Notifications gezielt zu nutzen.

Eine effiziente Herangehensweise besteht darin, die Benachrichtigungen innerhalb von Visual Studio Code (VS Code) zu integrieren und so z. B. Pull Requests, Issues und Kommentare **direkt in der Entwicklungsumgebung zu bearbeiten**.

Im Folgenden findest Du eine Schritt-für-Schritt-Anleitung und einige Best Practices.

---

## 1 GitHub Benachrichtigungen verstehen und konfigurieren

### 1.1 Einstellungen für Benachrichtigungen in GitHub anpassen

#### 1.1.1 Benachrichtigungseinstellungen öffnen

- Klicke in GitHub (Weboberfläche) oben rechts auf dein Profilbild → Settings → Notifications.

---

#### 1.1.2 E-Mail-Benachrichtigungen reduzieren oder deaktivieren

- Wähle aus, bei welchen Aktionen du E-Mail-Benachrichtigungen erhalten möchtest.
- Passe ggf. auch die Option „Receive notifications for“ an und wähle Participating and @mentions oder Watching.
- Hier kannst du spezifisch auf Repository-Ebene einstellen, ob du Benachrichtigungen erhalten möchtest oder nicht.

---

#### 1.1.3 Filter anwenden

- Mit Filtern kannst du gezielt festlegen, welche Art von Meldungen (z. B. nur Pull-Request-Reviews) dich erreichen sollen.
- Dadurch reduzierst du Benachrichtigungen auf das Wesentliche.

---

## 1.2 Tabs und Filter in GitHub Notifications nutzen

### 1.2.1 Inbox-Pflege: Gewöhne dir an, die GitHub-„Inbox“ (Benachrichtigungsseite) regelmäßig aufzurufen.

### 1.2.2 Benachrichtigungen markieren

- Read / Unread: Filtere, welche Notifications schon gelesen sind.
- Saved: Merke dir wichtige Benachrichtigungen, um sie später erneut aufzurufen.

### 1.2.3 Direktes Reagieren

- Viele Aktionen (z. B. Issue schließen, Label zuweisen, Kommentar verfassen) sind direkt von der Notifications-Seite aus möglich.

Auf diese Weise erhältst du ohnehin deutlich weniger E-Mails, weil du GitHub als dein Benachrichtigungs-Dashboard nutzt. Doch noch effizienter wird es, wenn man VS Code zur Bearbeitung und zum Überblick über neue Vorgänge nutzt.

---

## 2 GitHub Notifications in Visual Studio Code integrieren

### 2.1 GitHub Extensions für VS Code

Um Benachrichtigungen oder Issues und Pull Requests **direkt in VS Code** anzuzeigen, stehen mehrere Extensions bereit. Zwei der gängigsten Optionen sind:

#### 2.1.1 GitHub Pull Requests & Issues (offizielle GitHub-Erweiterung)

- Diese Extension zeigt dir in einem separaten Panel im Explorer z. B. offene Pull Requests und Issues an.
- Du kannst Pull Requests kommentieren, reviewen und sogar mergen, ohne deinen Editor verlassen zu müssen.

---

#### 2.1.2 GitHub Notifications (Community-Projekt)

GitHub Notifications erlaubt es, GitHub-Benachrichtigungen **direkt in VS Code** einzusehen, sie als gelesen zu markieren und sogar per Klick den zugehörigen PR/Issue zu öffnen.

---

##### 2.1.2.1 Installation

1. Öffne in VS Code den Extensions-Bereich (Linke Seitenleiste, Symbol „Vier Quadrate“).
2. Suche nach “GitHub Pull Requests and Issues“ und installiere die Extension.
3. Analog kannst du nach einer GitHub Notifications Extension suchen und diese bei Bedarf installieren.

---

##### 2.1.2.2 Einrichtung der GitHub-Verbindung

1. Authentication: Beim ersten Start wirst du in der Regel aufgefordert, dich über OAuth in GitHub anzumelden.
2. Berechtigungen erteilen: Akzeptiere die benötigten Zugriffsrechte, damit die Erweiterung deine Benachrichtigungen lesen bzw. verwalten kann.

---

##### 2.1.2.3 Nutzung im VS Code-Alltag

- Panel „GitHub Pull Requests & Issues“: Hier bekommst du einen Überblick über neue Pull Requests und offene Issues in deinen Projekten.
- Benachrichtigungen-Panel (falls vorhanden): Je nach Extension erhältst du eine Liste deiner GitHub-Notifications und kannst sie als gelesen markieren, kommentieren etc.
- Statusbar-Hinweise: Manche Erweiterungen bieten eine Anzeige in der VS Code-Statusleiste. Dadurch siehst du sofort, ob neue Benachrichtigungen vorliegen.

---

## 3 Empfohlene Arbeitsweise

### 3.1 Erster Check am Morgen

- Öffne VS Code und schau ins Notifications-Panel bzw. in „GitHub Pull Requests & Issues“.
- So siehst du auf einen Blick, ob es neue Merge-Konflikte, zu beantwortende Reviews oder Fragen in Issues gibt.

---

### 3.2 Regelmäßige Inbox-Hygiene

- Ähnlich wie im E-Mail-Postfach: Markiere irrelevante oder erledigte Meldungen als gelesen, damit dein### 3.B achrichtigungsfeed übersichtlich bleibt

---

### 3.3 Arbeiten direkt in VS Code

- in der Pull-Request-Ansicht; du musst nicht mehr in den Browser wechseln.
- Wechsle bei einem Review nahtlos in den Code, um Änderungen nachzuvollziehen und zu kommentieren.

---

### 3.4 Gezielte Filterung

- Achte auch in VS Code darauf, nur Benachrichtigungen für bestimmte Projekte oder Themen zu abonnieren.
- Damit sparst du dir unnötige Ablenkungen.

---

### 3.5 Nutze Labels und Zuweisungen

- Weise dir selbst Issues zu, die du bearbeiten möchtest, oder nutze Labels, um Projekte zu strukturieren.
- So siehst du in VS Code schnell deine aktuellen Aufgaben.

---

## 4.  Vorteile und Effekte

- **Reduktion von E-Mail-Flut:** Indem du kaum noch E-Mails empfängst, wirst du weniger abgelenkt und kannst dich aufs Wesentliche konzentrieren.
- **Schnellere Reaktionszeiten** Du wirst über VS Code direkt informiert, wenn etwas Relevantes geschieht.
- **Effizienter Workflow** Anstatt erst den Browser und das GitHub-Interface zu öffnen, kannst du in derselben Umgebung (VS Code) direkt kommentieren, reviewen und commiten.
- **Zentrale Übersicht:** Sowohl Code als auch Pull Requests und Benachrichtigungen laufen in einer Ansicht zusammen, statt über verschiedene Tools verteilt zu sein.

---

## 5. Fazit

Wer GitHub Notifications konsequent nutzt und gleichzeitig in VS Code integriert, kann seinen Arbeitsalltag **spürbar** vereinfachen und E-Mail-Benachrichtigungen **drastisch reduzieren oder sogar ganz darauf verzichten**. Die richtigen Einstellungen und Erweiterungen helfen dabei, den Überblick zu behalten und effizient zu arbeiten.

Das Wichtigste ist, dass du dir in GitHub klare Filter und Benachrichtigungseinstellungen vornimmst, sodass nur wirklich relevante Benachrichtigungen zu dir durchdringen. Mit den richtigen Extensions in VS Code hast du dann alles Wichtige im Blick und kannst direkt dort handeln, wo du entwickelst – **ohne erst in den Browser wechseln zu müssen.**

Kurz gesagt: Stelle GitHubs Benachrichtigungen so ein, dass du nur relevante Ereignisse mitbekommst, und nutze eine VS-Code-Integration für Pull Requests, Issues und ggf. Notifications. Damit machst du deinen Entwicklungsworkflow schlanker und eliminierst störende E-Mail-Fluten.

---

| [Weiter](/7/README.md)