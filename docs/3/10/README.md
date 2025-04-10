# 3.10 Terminal Grundlagen

Willkommen zu den Terminal Grundlagen! Diese Seite dient als Einführung in die wichtigsten Konzepte und Funktionen des Terminals. Hier lernen Sie, wie Sie ein Terminal starten, die Benutzeroberfläche verstehen und grundlegende Navigationsbefehle anwenden.

## Inhalte

- Terminal starten
- Benutzeroberfläche verstehen
- Grundlegende Navigation

## Terminal starten

Das Terminal, auch als Kommandozeile, Shell oder Konsole bekannt, ist ein leistungsstarkes Werkzeug zur Interaktion mit Ihrem Betriebssystem. Es ermöglicht Ihnen, Befehle direkt einzugeben und auszuführen. Hier sind die Methoden zum Öffnen des Terminals auf verschiedenen Betriebssystemen:

### Windows:
- Drücken Sie die Windows-Taste + R, geben Sie "cmd" ein und drücken Sie Enter.
- Alternativ können Sie auch PowerShell verwenden, indem Sie im Startmenü nach "PowerShell" suchen.

### macOS:
- Öffnen Sie das Launchpad und suchen Sie nach "Terminal".
- Alternativ können Sie auch Spotlight (Cmd + Leertaste) verwenden und "Terminal" eingeben.
- Die Tastenkombination Cmd + Leertaste öffnet Spotlight, wo Sie dann "Terminal" eingeben können.

### Linux:
- Die meisten Linux-Distributionen ermöglichen das Öffnen eines Terminals mit der Tastenkombination Strg + Alt + T.
- Sie können auch im Anwendungsmenü nach "Terminal" oder "Konsole" suchen.
- Viele Linux-Distributionen bieten eine Schaltfläche oder Verknüpfung auf dem Desktop oder im Anwendungsmenü zum Starten des Terminals.

### Visual Studio Code:
Da Sie bereits Visual Studio Code installiert haben, können Sie das integrierte Terminal wie folgt öffnen:
1. Öffnen Sie Visual Studio Code.
2. Wählen Sie `View > Terminal` aus dem Menü oder verwenden Sie die Tastenkombination:
   - Windows/Linux: ``Ctrl+` ``
   - macOS: ``Cmd+` ``



Citations:
[1] https://serverspace.io/de/about/blog/basic-linux-commands-in-the-terminal/
[2] https://www.heise.de/tipps-tricks/Linux-Befehle-Die-20-wichtigsten-Kommandos-3843388.html
[3] https://www.linuxumsteiger.net/linux-terminal-befehle/
[4] https://kinsta.com/de/blog/linux-befehle/
[5] https://support.apple.com/de-de/guide/terminal/welcome/mac
[6] https://contabo.com/blog/de/linux-befehle/
[7] https://www.ionos.de/digitalguide/server/konfiguration/linux-befehle-terminal-kommandos-im-ueberblick/
[8] https://hsp.pages.cs.uni-duesseldorf.de/programmierung/website/lectures/progra/tutorials/terminal/

## Benutzeroberfläche verstehen

Wenn Sie ein Terminal öffnen, sehen Sie in der Regel folgende Elemente:

1. **Prompt**: Dies ist der Bereich, in dem Sie Befehle eingeben. Es zeigt oft Informationen wie den aktuellen Benutzernamen, Computernamen und das aktuelle Verzeichnis an.

2. **Cursor**: Ein blinkender Unterstrich oder Block, der anzeigt, wo Ihre Eingabe erscheinen wird.

3. **Ausgabebereich**: Hier werden die Ergebnisse Ihrer Befehle angezeigt.

4. **Scrollbalken**: Ermöglicht das Scrollen durch frühere Ausgaben und Befehle.

## Grundlegende Navigation

Hier sind einige grundlegende Befehle zur Navigation im Terminal:

- `cd` (Change Directory): Wechselt das aktuelle Verzeichnis.
  Beispiel: `cd Documents` wechselt in den Ordner "Documents".

- `cd ..`: Wechselt in das übergeordnete Verzeichnis.

- `ls` (List): Zeigt den Inhalt des aktuellen Verzeichnisses an.
  Unter Windows verwenden Sie stattdessen `dir`.

- `tree`: Zeigt die Verzeichnisstruktur als Baum an.
  Unter macOS müssen Sie möglicherweise zuerst `brew install tree` ausführen.

## Hilfreiche Ressourcen

### Deutsch:
- [Einführung in die Kommandozeile (Ubuntu)](https://wiki.ubuntuusers.de/Einsteiger/Kommandozeile/)
- [Terminal-Grundlagen (CHIP)](https://praxistipps.chip.de/terminal-grundlagen-die-wichtigsten-befehle_41343)

### Englisch:
- [Command Line Crash Course (freecodecamp)](https://www.freecodecamp.org/news/command-line-for-beginners/)

## Aufgabe: Bilder erstellen und hinzufügen

Um die Anleitungen zu vervollständigen, erstellen Sie Screenshots der beschriebenen Schritte:

1. Erstellen Sie Screenshots für das Öffnen des Terminals in Windows, macOS und Linux.
2. Machen Sie einen Screenshot der Terminal-Benutzeroberfläche und beschriften Sie die wichtigsten Elemente.
3. Zeigen Sie die Ausführung der grundlegenden Navigationsbefehle (`cd`, `ls`, `tree`) in Screenshots.

Fügen Sie die Bilder in das Repository ein, indem Sie sie im `images/`-Ordner speichern. Erstellen Sie anschließend einen Pull Request, um Ihre Änderungen vorzuschlagen.

## Dokumentation und Fragen

Es ist wichtig, dass Sie alle Fragen, die während der Bearbeitung dieses Abschnitts aufkommen, dokumentieren. Notieren Sie Ihre Fragen, bevor Sie sie an andere stellen. Diese Praxis der Dokumentation ist entscheidend für Entwickler, da sie uns hilft, Unklarheiten zu identifizieren und den Lehrgang kontinuierlich zu verbessern und zugänglicher zu gestalten.