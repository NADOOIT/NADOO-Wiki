# <p align="center">Das Terminal — die Grundlagen</p>

Willkommen zu den Terminal Grundlagen! Diese Seite dient als Einführung in die wichtigsten Konzepte und Funktionen des Terminals. Hier lernst du, wie du ein Terminal startest, die Benutzeroberfläche verstehst und grundlegende Navigationsbefehle anwendest.

---

## Inhalte

- Terminal starten
- Benutzeroberfläche verstehen
- Grundlegende Navigation

---

## Terminal starten

Das Terminal, auch als Kommandozeile, Shell oder Konsole bekannt, ist ein leistungsstarkes Werkzeug zur Interaktion mit deinem Betriebssystem. Es ermöglicht dir, Befehle direkt einzugeben und auszuführen. Hier sind die Methoden zum Öffnen des Terminals auf verschiedenen Betriebssystemen:

### Windows:
- Drücke die Windows-Taste + R, gib "cmd" ein und drücke Enter.
- Alternativ kannst du auch PowerShell verwenden, indem du im Startmenü nach "PowerShell" suchst.

### macOS:
- Öffne das Launchpad und suche nach "Terminal".
- Alternativ kannst du auch Spotlight (cmd + Leertaste) verwenden und "Terminal" eingeben.

### Linux:
- Die meisten Linux-Distributionen ermöglichen das Öffnen eines Terminals mit der Tastenkombination Strg + Alt + T.
- Du kannst auch im Anwendungsmenü nach "Terminal" oder "Konsole" suchen.
- Viele Linux-Distributionen bieten eine Schaltfläche oder Verknüpfung auf dem Desktop oder im Anwendungsmenü zum Starten des Terminals.

### Visual Studio Code:
Da du bereits Visual Studio Code installiert hast, kannst du das integrierte Terminal wie folgt öffnen:
1. Öffne Visual Studio Code.
2. Wähle `View > Terminal` aus dem Menü oder verwende die Tastenkombination:
   - Windows/Linux: ``Ctrl+` / Ctrl+ö``
   - macOS: ``Cmd+` ``

---

## Benutzeroberfläche verstehen

Wenn du ein Terminal öffnest, siehst du in der Regel folgende Elemente:

1. **Prompt** (Eingabeaufforderung): 
   - Zeigt oft deinen Benutzernamen, Computernamen und das aktuelle Verzeichnis an
   - Endet normalerweise mit einem `$` (Linux/macOS) oder `>` (Windows)
   - Beispiel: `benutzer@rechner:~$` oder `C:\Users\Benutzer>`

2. **Cursor**: 
   - Blinkender Unterstrich oder Block (`_` oder `|`)
   - Zeigt die aktuelle Einfügeposition an
   - Wird automatisch nach dem Prompt platziert

3. **Ausgabebereich**: 
   - Zeigt die Ergebnisse von Befehlen an
   - Scrollt automatisch nach unten bei neuer Ausgabe
   - Behält die Befehlsverlauf bei (abhängig von der Terminal-Konfiguration)

4. **Scrollbalken**: 
   - Erscheint, wenn der Inhalt länger ist als das sichtbare Fenster
   - Ermöglicht das Durchsuchen früherer Ausgaben
   - Kann mit der Maus oder Tastatur (Bild auf/Bild ab) bedient werden

5. **Fenster-Titel** (optional):
   - Zeigt oft das aktuelle Verzeichnis oder den laufenden Prozess an
   - Kann je nach Terminal-Einstellungen variieren

## Grundlegende Navigation

Hier sind einige grundlegende Befehle zur Navigation im Terminal:

- `cd` (Change Directory): Wechselt das aktuelle Verzeichnis.
  Beispiel: `cd Documents` wechselt in den Ordner "Documents".

- `cd ..`: Wechselt in das übergeordnete Verzeichnis.

- `ls` (List): Zeigt den Inhalt des aktuellen Verzeichnisses an.
  Unter Windows verwendest du stattdessen `dir`.

- `tree`: Zeigt die Verzeichnisstruktur als Baum an.
  Unter macOS musst du möglicherweise zuerst `brew install tree` ausführen.

---

## Hilfreiche Ressourcen

### Deutsch:
- [Einführung in die Kommandozeile (Ubuntu)](https://wiki.ubuntuusers.de/Einsteiger/Kommandozeile/)
- [Terminal-Grundlagen (CHIP)](https://praxistipps.chip.de/terminal-grundlagen-die-wichtigsten-befehle_41343)

### Englisch:
- [Command Line Crash Course (freecodecamp)](https://www.freecodecamp.org/news/command-line-for-beginners/)

---

## Praktische Übung: Terminal erkunden

### Aufgabe 1: Terminal starten
1. Öffne das Terminal auf deinem Betriebssystem
2. Mache einen Screenshot des geöffneten Terminals
3. Speichere den Screenshot als `terminal-windows.png` (oder `-macos`/`-linux`)

### Aufgabe 2: Benutzeroberfläche verstehen
1. Erstelle einen Screenshot deines Terminals
2. Beschrifte folgende Elemente:
   - Prompt
   - Cursor
   - Ausgabebereich
   - Scrollbalken
   - Fenster-Titel (falls sichtbar)
3. Speichere den Screenshot als `terminal-ui.png`

### Aufgabe 3: Navigation üben
Führe folgende Befehle aus und mache jeweils einen Screenshot:
1. `pwd` (zeigt das aktuelle Verzeichnis an)
2. `ls` oder `dir` (listet den Verzeichnisinhalt auf)
3. `cd` in ein anderes Verzeichnis wechseln
4. `cd ..` ins übergeordnete Verzeichnis wechseln
5. `tree` Verzeichnisstruktur anzeigen (falls verfügbar)

### Abgabe der Aufgabe
1. Erstelle einen Ordner `images/terminal` in diesem Verzeichnis
2. Speichere alle Screenshots im `images/terminal`-Ordner
3. Aktualisiere diese README, um auf die neuen Bilder zu verweisen
4. Erstelle einen neuen Branch: `git checkout -b feature/terminal-screenshots`
5. Committe deine Änderungen: `git add .` und `git commit -m "Hinzufügen von Terminal-Screenshots"`
6. Pushe den Branch: `git push origin feature/terminal-screenshots`
7. Erstelle einen Pull Request auf GitHub

### Bewertungskriterien
- [ ] Alle geforderten Screenshots sind vorhanden
- [ ] Die Bilder sind klar und gut lesbar
- [ ] Die Beschriftungen sind korrekt und verständlich
- [ ] Die Befehle wurden korrekt ausgeführt
- [ ] Die Änderungen wurden in einem separaten Branch vorgenommen

---

#### Quellen

[1] https://serverspace.io/de/about/blog/basic-linux-commands-in-the-terminal/ <br>
[2] https://www.heise.de/tipps-tricks/Linux-Befehle-Die-20-wichtigsten-Kommandos-3843388.html <br>
[3] https://www.linuxumsteiger.net/linux-terminal-befehle/ <br>
[4] https://kinsta.com/de/blog/linux-befehle/ <br>
[5] https://support.apple.com/de-de/guide/terminal/welcome/mac <br>
[6] https://contabo.com/blog/de/linux-befehle/ <br>
[7] https://www.ionos.de/digitalguide/server/konfiguration/linux-befehle-terminal-kommandos-im-ueberblick/ <br>
[8] https://hsp.pages.cs.uni-duesseldorf.de/programmierung/website/lectures/progra/tutorials/terminal/ <br>

---

<p align="center">
<a href="/docs/04-tools/04-windsurf/01-ueberblick/04-datenschutz_sicherheit_und_datenhaltung/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/06-launchpad/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/README.md/#dieser-themenbereich-beinhaltet-folgende-themen"><strong>Zurück zur Themen-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>


