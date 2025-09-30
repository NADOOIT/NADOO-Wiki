# <p align="center">Installation [MAC]</p>

## 1. Anmelden oder einen Account erstellen

Melde Dich bei GitHub an oder erstelle einen neuen Account.

![image](https://github.com/user-attachments/assets/1b080f41-d3ae-4397-89cb-fb6f3c8b38f9)

---

## 2. GitHub Desktop herunterladen und installieren (empfohlen)

Lade [GitHub Desktop](https://central.github.com/deployments/desktop/desktop/latest/darwin) herunter und installiere es.

ℹ️ GitHub Desktop ist eine einfache Möglichkeit, Git zu nutzen, ohne auf die Kommandozeile zurückzugreifen. Falls Du Git bereits installiert hast und lieber die Kommandozeile nutzt, kannst Du auch den `git clone`-Befehl verwenden.

![image](https://github.com/user-attachments/assets/74a72eba-b560-46bd-bbf5-876df4fe12c0)

---

<<<<<<< HEAD:docs/04-tools/06-launchpad/01-ueberblick/02-mac/README.md

=======
## 3. ffmpeg Installation (neue Voraussetzung für Speech-to-Text)

Für die Nutzung der Speech-to-Text-Features ist ffmpeg erforderlich.

ℹ️ ffmpeg ist ein leistungsstarkes Open-Source-Tool, welches Dir erlaubt Audio- und Videodaten direkt aus der Kommandozeile heraus zu verarbeiten.

**Bitte führe für die Installation auf macOS folgende Schritte aus**:

1. Schließe alle Instanzen von Visual Studio Code sowie alle Terminals, die Du möglicherweise gerade geöffnet hast.

2. Öffne ein Terminal mit Administratorrechten (vorzugsweise PowerShell).

3. Auf macOS empfiehlt es sich, ffmpeg via Homebrew zu installieren - führe also den folgenden Befehl aus:

```bash
brew install ffmpeg
```

<br>
Schließe das Terminal nach erfolgreicher Installation. <br>
Visual Studio Code sollte ebenfalls nach wie vor geschlossen sein.

---

## 4. Repository klonen

1. Gehe zum [NADOO-Launchpad-Repository](https://github.com/NADOOIT/NADOO-Launchpad).

2. Klicke auf den grünen "Code"-Button.

3. Wähle die Option "Open with GitHub Desktop", um das Repository mit GitHub Desktop zu klonen.

![image](https://github.com/user-attachments/assets/d46ddeb9-5c56-4c8a-80df-78d74f39184f)

4. Ein kleines Pop-up-Fenster wird angezeigt, klicke hier auf "GitHubDesktop öffnen".

![image](https://github.com/user-attachments/assets/3fa08c52-4635-4d95-bc1d-9d7e87d52784)

5. Das GitHub Desktop-Fenster öffnet sich automatisch.

⚠️**Wichtig**: Stelle sicher, dass Du den im Bild gezeigten Pfad verwendest, um Fehler während des Programmstarts zu vermeiden.

Gib diesen Pfad in das Feld ein und klicke dann auf den blauen Button "Clone". Das Klonen kann einige Minuten dauern. Bitte habe etwas Geduld, während die Dateien auf Deinen Computer heruntergeladen werden.

![image](https://github.com/user-attachments/assets/d62354cf-fe8c-4edb-98a1-71d701ad3541)

---

## 5. Einfügen der **Large-Language-Model**-KI (**LLM**) ins Projekt 

Sobald das Projekt erfolgreich auf Deinen Rechner geklont wurde, öffnet sich Github Desktop mit neuen Optionen.

_Bevor_ Du hier weitermachst, lade zunächst das **Qwen2.5**-Model herunter und speichere es lokal bei Dir im **_models_**-Ordner ab. <br>
Den Ordner findest du im **_resources_**-Verzeichnis:

![kompletter Pfad zu resources-models](https://github.com/user-attachments/assets/76ee15bb-bce6-490e-a672-88f05b3161f0)

**Link zum Model**: https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-1M-GGUF

**Link für den direkten Download**: https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-1M-GGUF/blob/main/Qwen2.5-14B-Instruct-1M-Q4_0.gguf

---

## 6. Visual Studio Code öffnen

⚠️**Wichtig**: Sollte VS Code an diesem Punkt aus irgendeinem Grund geöffnet sein, könnten hier Fehler auftreten. Vergewissere Dich also nochmal, dass das Programm wirklich geschlossen ist.

Gehe nach erfolgreicher Integration des LLMs zurück zum Github Desktop-Fenster und klicke dort auf "**Open with Visual Studio Code**".

![image](https://github.com/user-attachments/assets/2b0cbbe7-7e35-46cc-a0c6-53e32ead5bfa)

---

## 7. Terminal öffnen

Öffne in Visual Studio Code das Terminal über den Menüpunkt "Terminal".

![image](https://github.com/user-attachments/assets/1040b91b-2752-4548-b8ff-5129aee54c27)

Stelle sicher, dass Du im richtigen Projektverzeichnis bist. Dies erkennst Du daran, dass im Terminal ein Ordnerpfad mit NADOO-Launchpad angezeigt wird:

![image](https://github.com/user-attachments/assets/bd8cd896-0412-438b-8c57-1bfe61bfd6ea)

⚠️**Wichtig**: Enthält der angezeigte Pfad nicht "NADOO-Launchpad", dann gehe zurück zu Punkt 6. Schließe VS Code und führe den Schritt erneut durch.

---

## 8. Installationsskript ausführen

1. Stelle zuerst sicher, dass Conda nicht verwendet wird, denn das NADOO Launchpad setzt das Tool nicht für seine virtuellen Umgebungen ein. Um zu vermeiden, dass die Conda-Basisumgebung versehentlich automatisch aktiviert wird, kannst Du diese mit dem folgenden Befehl deaktivieren:

```bash
conda config --set auto_activate_base false
```

Dadurch wird sichergestellt, dass die Conda-Umgebung die Einrichtung vom Launchpad nicht beeinträchtigt. Falls Du das Tool sowieso nicht installiert hast, kannst Du diesen Schritt einfach ignorieren.

2. Gib im Terminal den folgenden Befehl ein und drücke **Enter**:

```bash
  source ./++START_THIS_SCRIPT_FOR_MacOS_INSTALL++.sh
```

Soll die virtuelle Umgebung neu erstellt werden, kannst Du den folgenden Befehl verwenden:

```bash
  source ./++START_THIS_SCRIPT_FOR_MacOS_INSTALL++.sh -reinstall
```

![image](https://github.com/user-attachments/assets/eb11bcfb-a1c4-4e86-bdf9-541d5f16e532)

---

## 9. Installation und Umgebung einrichten

Nun beginnt die Installation! Das Skript lädt und installiert alle erforderlichen Pakete und richtet die Entwicklungsumgebung für Dich ein. Keine Panik, das kann ein paar Minuten dauern. Nutze die Zeit, um Dir einen Kaffee oder Tee zu holen – eine kleine Pause tut immer gut. ☕️

![Screenshot 2024-10-07 125411](https://github.com/user-attachments/assets/3a453743-f161-4068-9bfd-486e40d507d1)

Sobald die Installation abgeschlossen ist, wird die Umgebung automatisch erstellt **und aktiviert**.

**Am Ende** öffnet sich das NADOO Launchpad-Fenster automatisch, und Du bist bereit, mit der Entwicklung zu starten! 🚀

![image](https://github.com/user-attachments/assets/0c7a9322-9d58-48d0-8aa8-0a2cd5b11259)

### Nach der Installation: Launchpad CLI verwenden

Nach dem einmaligen Ausführen des Installationsskripts steht Dir die Launchpad CLI zur Verfügung. Verwende ab dann die folgenden Befehle (plattformübergreifend):

- Anwendung starten:
  ```bash
  launchpad start
  ```

- Tests ausführen (vollständige Test-Suite):
  ```bash
  launchpad run_tests
  ```

- Paket/Build erstellen (sofern unterstützt):
  ```bash
  launchpad package
  ```

Hinweise:
- Versionswechsel der Python-Umgebung oder Neuinstallation erfolgen weiterhin über das jeweilige Installationsskript (nur einmalig nötig). Für den täglichen Workflow nutze die CLI.

---

<p align="center"><a href="/docs/04-tools/06-launchpad/01-ueberblick/01-windows/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/06-launchpad/02-features/README.md"><strong>Weiter</strong></a></p>

<p align="center">
<a href="/docs/04-tools/06-launchpad/01-ueberblick/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
>>>>>>> main:docs/04-tools/05-launchpad/01-ueberblick/02-mac/README.md
