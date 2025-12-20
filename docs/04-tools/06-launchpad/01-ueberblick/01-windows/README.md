# <p align="center">Installation [Windows]</p>

<!-- Der Part "Important &nbsp;🛠️" scheint neu zu sein und war vorher nicht notwendig, um das Launchpad auf Windows zu installieren. Ggf. bei Christoph nachfragen, ob das jetzt der korrekte erste Schritt ist oder ob weiterhin mit "1. Anmelden oder Acc. erstellen" begonnen werden soll. -->
> **Important &nbsp;🛠️**  
> Enable Windows long-path support *once* before cloning. This prevents the
> classic *“Filename too long / Path too long”* errors when working with deep
> project trees. You will experience this error if you try to clone the repository with a deep project tree.
>
> 1. Open **PowerShell as Administrator** and run:
>
>    ```powershell
>    New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
>                     -Name LongPathsEnabled -Value 1 -PropertyType DWORD -Force
>    ```
> 2. Reboot Windows.
>
> (GUI alternative: **gpedit.msc → Computer Configuration → Administrative Templates → System → Filesystem → Enable Win32 long paths → Enabled**.)
> 
> Also you need to change you git config to use the long path support:
> 
>     ```powershell
>     git config --global core.longpaths true
>     ```
> This is only needed once. 

---

## 1. Anmelden oder einen Account erstellen

Melde Dich bei GitHub an oder erstelle einen neuen Account.

![image](https://github.com/user-attachments/assets/1b080f41-d3ae-4397-89cb-fb6f3c8b38f9)

---

## 2. GitHub Desktop herunterladen und installieren (empfohlen)

Lade [GitHub Desktop](https://desktop.github.com/download/) herunter und installiere es.

ℹ️ GitHub Desktop ist eine einfache Möglichkeit, Git zu nutzen, ohne auf die Kommandozeile zurückzugreifen. Falls du Git bereits installiert hast und lieber die Kommandozeile nutzt, kannst Du auch den `git clone`-Befehl verwenden.

![image](https://github.com/user-attachments/assets/526c4c28-7e93-45a0-b6be-1b52cebac349)

---

## 3. ffmpeg Installation (neue Voraussetzung für Speech-to-Text)

Für die Nutzung der Speech-to-Text-Features ist ffmpeg erforderlich.

ℹ️ ffmpeg ist ein leistungsstarkes Open-Source-Tool, welches Dir erlaubt Audio- und Videodaten direkt aus der Kommandozeile heraus zu verarbeiten.

**Bitte führe für die Installation auf Windows folgende Schritte aus**:

1. Schließe alle Instanzen von Visual Studio Code sowie alle Terminals, die Du möglicherweise gerade geöffnet hast.

2. Öffne ein Terminal mit Administratorrechten (vorzugsweise PowerShell).

3. Führe den folgenden Befehl aus:

```bash
winget install --id Gyan.FFmpeg --scope machine
```

<br>
Schließe das Terminal nach erfolgreicher Installation. <br>
Visual Studio Code sollte ebenfalls nach wie vor geschlossen sein.

---

## 4. Repository klonen

1. Gehe zum [NADOO-Launchpad-Repository](https://github.com/NADOOIT/NADOO-Launchpad).

2. Klicke auf den grünen **"Code"**-Button.

3. Wähle die Option **"Open with GitHub Desktop"**, um das Repository mit GitHub Desktop zu klonen.

![03](https://github.com/user-attachments/assets/b546dcd9-be16-47b8-8127-4b96c86bb5c0)

4. Ein kleines Pop-up-Fenster wird angezeigt, klicke hier auf **"GitHubDesktop öffnen"**.

![04](https://github.com/user-attachments/assets/af23bcb7-6ef8-4e8c-b9cb-c1c376a6d58f)

5. Das GitHub Desktop-Fenster öffnet sich automatisch.

⚠️ **Wichtig**: Stelle sicher, dass Du den **im Bild gezeigten Pfad** verwendest, um Fehler während des Programmstarts zu vermeiden.

⚠️ **Wichtig**: Stelle sicher, dass **der ausgewählte Ordner nicht in OneDrive** liegt.

Gib diesen Pfad in das Feld ein und klicke dann auf den blauen Button **"Clone"**. Das Klonen kann einige Minuten dauern. Bitte habe etwas Geduld, während die Dateien auf Deinen Computer heruntergeladen werden.

![image](https://github.com/user-attachments/assets/b218989a-fa5f-45ca-84f8-6600d05b3af2)

---

## 4. Visual Studio Code öffnen

⚠️ **Wichtig**: Sollte VS Code an diesem Punkt aus irgendeinem Grund doch geöffnet sein, könnten hier Fehler auftreten. Vergewissere Dich also erneut, dass das Programm wirklich geschlossen ist.

Wenn das Projekt erfolgreich geklont wurde, klicke auf **"Open with Visual Studio Code"**.

![image](https://github.com/user-attachments/assets/b8eaae6b-79f1-4369-9d5a-f80d47d0ec1c)

> **Important Note About Auto-Save**
> 
> When working with NADOO Launchpad, please ensure that **auto-save is disabled** in your code editor (VS Code, etc.).
> - Auto-save can trigger unwanted background processing
> - In VS Code: Go to File > Auto Save and make sure it's unchecked
> - Save your work manually (Ctrl+S/Cmd+S) when you want to trigger processing

---

## 5. Terminal öffnen

Öffne in Visual Studio Code das **Terminal** über den Menüpunkt **"Terminal"**.

![10](https://github.com/user-attachments/assets/a52f1202-1f66-4af1-ac20-6ec66384c879)

Stelle sicher, dass Du im richtigen Projektverzeichnis bist. Dies erkennst du daran, dass im Terminal ein Ordnerpfad mit NADOO-Launchpad angezeigt wird:

![408181123-54000e92-703e-4622-90b8-2d4ba90bab54](https://github.com/user-attachments/assets/553bab66-5ee6-4553-9172-48170d5afd15)

⚠️**Wichtig**: Enthält der angezeigte Pfad nicht "NADOO-Launchpad", dann gehe zurück zu Punkt 4. Schließe VS Code und führe den Schritt erneut durch.

---

## 6. Installationsskript ausführen

1. Wähle im Repository-Explorer (linkes Auswahlmenü)
   **"++CLICK_THIS_FOR_WIN_INSTALL++"** aus.

   **Hinweis**: sollte der Explorer nicht angezeigt werden, kannst Du diesen öffnen, indem Du im Terminal den Pfad mit **ctrl+click** anklickst oder mit der Maus darüber hoverst - es sollte ein Pop-Up mit der Option **"Focus folder in explorer"** erscheinen.

   Sobald Du den Link anklickst, erscheint das Repository-Verzeichnis im Editor.
   
![Explorer anzeigen](https://github.com/user-attachments/assets/80324e31-1044-4ec3-a35e-cb5673758ae8)

2. Gib im Terminal den folgenden Befehl ein und drücke **Enter**:

```bash
 .\++CLICK_THIS_FOR_WIN_INSTALL++.ps1
```
**Wichtiger Hinweis (Fehlermeldung möglich)** : Solltest Du an diese Stelle eine Meldung wie (+ FullyQualifiedErrorId : UnauthorizedAccess) erscheinen, heißt das einfach, das Windows das Starten blockiert.
Um das zu lösen, gib bitte einmal folgende Befehl ein und drücke **Enter**
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

![11](https://github.com/user-attachments/assets/38bb4b0c-869b-45e8-84ed-2e68dd3dbf96)

3. **Alternativ** kannst Du die **NadooLaunchpad.bat**-Datei ausführen, welche Du im Verzeichnis des Repositories findest.

   Über die .bat-Datei kannst Du das Launchpad jederzeit per Doppelklick starten (öffnen).
   Dafür erstellst Du Dir am besten eine **Verknüpfung**, die Du bspw. auf Deinem Desktop ablegen kannst: Rechtsklick auf die .bat Datei, um das Kontextmenü zu öffnen, **"Verknüpfung erstellen"** anklicken und am gewünschten Ort lokal speichern.


⚠️**Wichtig**: Die folgende Meldung **verhindert die Installation** – unabhängig davon, ob du „Ja“ oder „Nein“ auswählst:
  

 <img width="796" height="202" alt="image" src="https://github.com/user-attachments/assets/38a8fe02-4a8a-4ad8-8593-ad6c77ebc188" />

<br> 

Erscheint sie bei dir, dann folge bitte den nächsten Schritten, um das Problem zu beheben:

**🔄 Repository neu klonen – Schritt für Schritt**


1. Öffne GitHub Desktop

2. Wähle das Repository „NADOO-Launchpad“ aus

3. Rechtsklick auf „NADOO-Launchpad“ in der Repository-Liste

4. Klicke auf „Repository entfernen“ (Remove) 

<img width="422" height="334" alt="image" src="https://github.com/user-attachments/assets/87adcb79-1b1c-4456-a170-6d6250381234" />


5. Bestätige die Meldung, dass du das lokale Repository löschen möchtest

6. Gehe erneut zu Schritt **## 4: Repository klonen**

7. **Wichtig**: Wähle beim Klonen keinen Speicherort in OneDrive!

---

## 7. Installation und Umgebung einrichten

Nun beginnt die Installation! Das Skript lädt und installiert alle erforderlichen Pakete und richtet die Entwicklungsumgebung für Dich ein. Keine Panik, das kann ein paar Minuten dauern. Nutze die Zeit, um Dir einen Kaffee oder Tee zu holen – eine kleine Pause tut immer gut. ☕️

![12](https://github.com/user-attachments/assets/3a453743-f161-4068-9bfd-486e40d507d1)

Sobald die Installation abgeschlossen ist, wird die Umgebung automatisch erstellt **und aktiviert**.

**Am Ende** öffnet sich das NADOO Launchpad-Fenster automatisch, und Du bist bereit, mit der Entwicklung zu starten! 🚀

![image](https://github.com/user-attachments/assets/0c7a9322-9d58-48d0-8aa8-0a2cd5b11259)

---

<p align="center">
<a href="/docs/04-tools/06-launchpad/01-ueberblick/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/06-launchpad/01-ueberblick/02-mac/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/06-launchpad/01-ueberblick/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
