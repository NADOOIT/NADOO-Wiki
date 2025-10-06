# <p align="center">Installation und Einrichtung</p>

## **Download:**

Gehe zur offiziellen Seite von JetBrains und lade den Installer herunter:
**Download-Link:** [IntelliJ IDEA](https://www.jetbrains.com/idea/download/?section=windows)

> Verwende die „Community Edition“, wenn du kostenlos starten möchtest. Die „Ultimate Edition“ ist kostenpflichtig!

### **Installation:**

1. **Installer starten** (Doppelklick auf die heruntergeladene `.exe`-Datei)
2. Wähle die gewünschte Sprache und bestätige.
3. **Zielordner ändern:**
   - Ändere den Installationspfad auf:  
     `C:\Programmierung\IntelliJ`
4. Optional: Aktiviere Desktop-Shortcut oder Dateizuordnungen.
5. Installation starten und warten, bis sie abgeschlossen ist.
6. IntelliJ starten und ggf. JetBrains-Konto überspringen oder einloggen.

---

## 2. Java 25 (JDK) installieren

### **Download:**

Lade die **JDK 25** Version (z. B. von Oracle, Eclipse Temurin oder OpenJDK) als **Installer**:
**Download-Link:** [`<JDK 25>`](https://www.oracle.com/java/technologies/downloads/#jdk25-windows)

_BILD_

### **Installation:**

1. Starte den **JDK 25 Installer**.
2. Wähle beim Setup die Option „Benutzerdefinierte Installation“ (Custom).
3. **Installationsverzeichnis anpassen:**
   - Gib folgendes Zielverzeichnis an:  
     `C:\Programmierung\Java\JDK25`

_BILD_

4. Weiterklicken und Installation abschließen.

> Nach der Installation kannst du in IntelliJ unter **Project Structure > SDKs** den JDK-Pfad manuell hinzufügen:  
`C:\Programmierung\Java\JDK25`

_BILD_
---

## 3. Maven manuell installieren

### **Download:**
Lade das **ZIP-Archiv von Apache Maven** herunter (nicht den Installer):
**Download-Link:** [`<Maven>`](https://maven.apache.org/download.cgi)

_BILD_

### **Installation (manuell, aber ohne Kommandozeile):**

1. Entpacke das ZIP-Archiv mit einem Rechtsklick → „Alle extrahieren“.
2. Wähle als Ziel:  
   `C:\Programmierung\Java`
3. Benenne den extrahierten Ordner in `Maven` um

_BILD_

4. Achte darauf, dass die Struktur so aussieht:  
   `C:\Programmierung\Java\Maven\bin\mvn.cmd`

### **Einbindung in IntelliJ IDEA:**

1. Öffne IntelliJ IDEA.
2. Gehe zu **File > Settings > Build, Execution, Deployment > Build Tools > Maven**

_BILD_

_BILD_

3. Unter „Maven home path“:
   - Wähle:  
     `C:\Programmierung\Java\Maven`
4. Bestätige mit Apply und dann OK.

---

## 4. JavaFX Scene Builder mit Windows Installer in `/Programmierung/Java/Scene Builder` installieren

### **Download:**
Besuche die offizielle Seite von GluonHQ und lade den Scene Builder herunter:  
**Download-Link:** [Scene Builder](https://gluonhq.com/products/scene-builder/#download)

_BILD_

> Wähle die **Windows Installer (.msi)** Datei aus.

---

### **Installation mit benutzerdefiniertem Pfad (via Eingabeaufforderung):**

Da der offizielle Installer standardmäßig in `C:\Program Files` installiert und keine Pfadangabe im Assistenten erlaubt, kannst du stattdessen folgenden Weg nutzen:

1. Öffne die **Eingabeaufforderung mit Administratorrechten**  
   (z. B. „Eingabeaufforderung (Administrator)“ oder „Windows Terminal (Admin)“).
2. Wechsle in das Verzeichnis, in dem sich die `.msi`-Datei befindet, z. B.:

   ```bat
   cd C:\Users\DeinName\Downloads
   ```

3. Starte die Installation mit dem gewünschten Zielpfad:

   ```bat
   msiexec /i SceneBuilder-23.0.1.msi INSTALLDIR="C:\Programmierung\Java\Scene Builder"
   ```

   > Passe den Dateinamen an deine heruntergeladene Version an.


---

### **Integration in IntelliJ IDEA:**

1. Öffne IntelliJ IDEA.
2. Gehe zu:  
   **File > Settings > Languages & Frameworks > JavaFX**
3. Unter **Path to SceneBuilder**:  
   Klicke auf das Verzeichnis-Symbol und wähle:

   C:\Programmierung\Java\Scene Builder\SceneBuilder.exe


4. Bestätige mit **OK**.

---

<p align="center">
<a href="/docs/04-tools/03-intellij/01-ueberblick/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/04-windsurf/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/03-intellij/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zur Kapitel-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
