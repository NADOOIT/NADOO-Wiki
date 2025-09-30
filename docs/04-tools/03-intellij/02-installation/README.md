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

## 2. Java 21 (JDK) installieren

### **Download:**

Lade die **JDK 21** Version (z. B. von Oracle, Eclipse Temurin oder OpenJDK) als **Installer**:
**Download-Link:** [`<JDK 21>`](https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html)

![Image](https://github.com/user-attachments/assets/18fcb1bc-df68-4b65-a871-263612fefc1f)

### **Installation:**

1. Starte den **JDK 21 Installer**.
2. Wähle beim Setup die Option „Benutzerdefinierte Installation“ (Custom).
3. **Installationsverzeichnis anpassen:**
   - Gib folgendes Zielverzeichnis an:  
     `C:\Programmierung\Java\JDK21`

![Image](https://github.com/user-attachments/assets/4dfcfb7d-ba93-4f10-aa37-af399ac73dc4)

4. Weiterklicken und Installation abschließen.

> Nach der Installation kannst du in IntelliJ unter **Project Structure > SDKs** den JDK-Pfad manuell hinzufügen:  
`C:\Programmierung\Java\JDK21`

![Image](https://github.com/user-attachments/assets/e9a31019-dafe-4f7e-a349-b746ba4a03aa) ![Image](https://github.com/user-attachments/assets/bcfe79c7-b1c8-4a79-8c35-eb4900fffa1c)

---

## 3. Maven manuell installieren

### **Download:**
Lade das **ZIP-Archiv von Apache Maven** herunter (nicht den Installer):
**Download-Link:** [`<Maven>`](https://maven.apache.org/download.cgi)

![Image](https://github.com/user-attachments/assets/fe4f776f-16f6-4ba3-8619-f4a77aa182e6)

### **Installation (manuell, aber ohne Kommandozeile):**

1. Entpacke das ZIP-Archiv mit einem Rechtsklick → „Alle extrahieren“.
2. Wähle als Ziel:  
   `C:\Programmierung\Java`
3. Benenne den extrahierten Ordner in `Maven` um

![Image](https://github.com/user-attachments/assets/d7238d05-b300-41b7-9cab-d2adc19f03c8)

4. Achte darauf, dass die Struktur so aussieht:  
   `C:\Programmierung\Java\Maven\bin\mvn.cmd`

### **Einbindung in IntelliJ IDEA:**

1. Öffne IntelliJ IDEA.
2. Gehe zu **File > Settings > Build, Execution, Deployment > Build Tools > Maven**
![Image](https://github.com/user-attachments/assets/c1acc247-01aa-45b4-a7ae-8306964d8699)

![Image](https://github.com/user-attachments/assets/4561e3b1-6089-42ff-b22e-de1a764c4dab)

3. Unter „Maven home directory“:
   - Wähle:  
     `C:\Programmierung\Java\Maven`
4. Bestätige mit OK.

---

## 4. JavaFX Scene Builder mit Windows Installer in `/Programmierung/Java/Scene Builder` installieren

### **Download:**
Besuche die offizielle Seite von GluonHQ und lade den Scene Builder herunter:  
**Download-Link:** [Scene Builder](https://gluonhq.com/products/scene-builder/#download)

![Image](https://github.com/user-attachments/assets/8a60148c-96e5-4c40-94d8-215cac09099b)

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

![Image](https://github.com/user-attachments/assets/8ed5db9b-33b2-40e6-bbce-cca14bf3d8ff)

---

### **Integration in IntelliJ IDEA:**

1. Öffne IntelliJ IDEA.
2. Gehe zu:  
   **File > Settings > Languages & Frameworks > JavaFX**
3. Unter **Path to SceneBuilder**:  
   Klicke auf das Verzeichnis-Symbol und wähle:

   C:\Programmierung\Java\Scene Builder\SceneBuilder.exe

![Image](https://github.com/user-attachments/assets/6ff9f471-c689-43c1-9dba-328e51b03195)

4. Bestätige mit **OK**.

---

<p align="center">
<a href="/docs/04-tools/03-intellij/01-ueberblick/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/04-windsurf/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/03-intellij/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zur Kapitel-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
