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

<p align="center"><img width="1832" height="977" alt="JDK 25 download" src="https://github.com/user-attachments/assets/d5fe5eba-9e2c-4103-b011-b8962af28175" /></p>

### **Installation:**

1. Starte den **JDK 25 Installer**.
2. Wähle beim Setup die Option „Benutzerdefinierte Installation“ (Custom).
3. **Installationsverzeichnis anpassen:**
   - Gib folgendes Zielverzeichnis an:  
     `C:\Programmierung\Java\JDK25`

<p align="center"><img width="492" height="372" alt="JDK 25 Verzeichnis auswahl" src="https://github.com/user-attachments/assets/a6c946e4-1bfd-43c9-9bc9-8bfe371bdd0c" /></p> <br>

<p align="center"><img width="492" height="374" alt="JDK 25 Verzeichnis eingabe" src="https://github.com/user-attachments/assets/a1871ef6-feb0-4e0b-9c3e-d763c009967f" /></p> <br>

<p align="center"><img width="493" height="375" alt="JDK 25 Verzeichnis weiter" src="https://github.com/user-attachments/assets/ecef782a-2113-48b9-8a83-833b5184aa4a" /></p> <br>

4. Weiterklicken und Installation abschließen.

> Nach der Installation kannst du in IntelliJ unter **Project Structure > SDKs** den JDK-Pfad manuell hinzufügen:  
`C:\Programmierung\Java\JDK25`

**Mit neuem Projekt:** 

<p align="center"><img width="1913" height="1025" alt="JDK 25 intellij projekt erstellen" src="https://github.com/user-attachments/assets/93ed01f4-ec69-45c9-9afa-c97fe3f1a167" /></p> <br>

<p align="center"><img width="1917" height="1024" alt="JDK 25 intellij auswahl bei neuem projekt" src="https://github.com/user-attachments/assets/b5582cff-c13f-4dc0-9846-710a0b324508" /></p> <br>

**Mit bestehendem Projekt:**

<p align="center"><img width="1919" height="1031" alt="JDK 25 intellij auswahl bei vorhandenem projekt" src="https://github.com/user-attachments/assets/d6100a32-ec38-4432-b8b6-2bc489da09d6" /></p> <br>

<p align="center"><img width="1022" height="857" alt="JDK 25 intellij JDK auswählen" src="https://github.com/user-attachments/assets/1e742481-7932-4b22-9b71-9b3da9a2066a" /></p> <br>



---

## 3. Maven manuell installieren

### **Download:**
Lade das **ZIP-Archiv von Apache Maven** herunter (nicht den Installer):
**Download-Link:** [`<Maven>`](https://maven.apache.org/download.cgi)

<p align="center"><img width="1898" height="979" alt="Maven download" src="https://github.com/user-attachments/assets/02a755b9-b1d5-4622-aed2-202eda4caad6" /></p> 


### **Installation (manuell, aber ohne Kommandozeile):**

1. Entpacke das ZIP-Archiv mit einem Rechtsklick → „Alle extrahieren“.
2. Wähle als Ziel:  
   `C:\Programmierung\Java`
3. Benenne den extrahierten Ordner in `Maven` um

<p align="center"><img width="1097" height="637" alt="Maven extrahieren" src="https://github.com/user-attachments/assets/a2bf8e64-e635-4802-9349-2ff16e3d33b0" /></p> <br>

<p align="center"><img width="610" height="446" alt="Maven pfad festlegung des entpackens" src="https://github.com/user-attachments/assets/db6a292d-60c2-4904-9911-536fc506d966" /></p> <br>

<p align="center"><img width="940" height="526" alt="Maven pfad bestätigen" src="https://github.com/user-attachments/assets/b98f5da4-63b5-469e-ad3e-0a687ecab35b" /></p> <br>

<p align="center"><img width="609" height="449" alt="Maven extrahieren klicken" src="https://github.com/user-attachments/assets/d8c702e7-1ff7-4c66-aae9-5ac515254f35" /></p> <br>

4. Achte darauf, dass die Struktur so aussieht:  
   `C:\Programmierung\Java\Maven\bin\mvn.cmd`

   

### **Einbindung in IntelliJ IDEA:**

1. Öffne IntelliJ IDEA.
2. Gehe zu **File > Settings > Build, Execution, Deployment > Build Tools > Maven**

<p align="center"><img width="704" height="404" alt="Intellij maven anbindung files" src="https://github.com/user-attachments/assets/0678b0bf-a1c4-49a4-bb72-2440c3a48452" /></p> <br>


<p align="center"><img width="493" height="584" alt="Intellij maven anbindung file settings" src="https://github.com/user-attachments/assets/1f691da5-93e7-4162-8138-5c372f51f901" /></p> <br>


3. Unter „Maven home path“:
   - Wähle:  
     `C:\Programmierung\Java\Maven`
4. Bestätige mit Apply und dann OK. <br>

<p align="center"><img width="979" height="728" alt="Intellij maven anbindung verzeichnis auswählen" src="https://github.com/user-attachments/assets/b27f70a2-711c-47b3-81a2-e0feee966bb4" /></p> <br>

---

## 4. JavaFX Scene Builder mit Windows Installer in `/Programmierung/Java/Scene Builder` installieren

### **Download:**
Besuche die offizielle Seite von GluonHQ und lade den Scene Builder herunter:  
**Download-Link:** [Scene Builder](https://gluonhq.com/products/scene-builder/#download)

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
