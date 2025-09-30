# <p align="center">[Feature-Guide] Watchdog</p>
<!-- "altes" Doc "Speech-to-Text"
-> Titelanpassung/inhaltliche Überarbeitung notwendig //
 ggf. Callback zum Basis-Ordner -->
## Einleitung
Das Speech-to-Text-Feature des NADOO Launchpad ermöglicht die automatische Umwandlung von Audiodateien in Text. Dadurch können beispielsweise Besprechungsaufnahmen, Präsentationen oder andere Sprachaufzeichnungen in bearbeitbare Dokumente konvertiert werden.

## Funktionsweise
Das System basiert auf einem Watchdog, der einen festgelegten Ordner überwacht. Sobald eine Audiodatei im **IN-Ordner** abgelegt wird, wird sie erkannt und automatisch verarbeitet. Dabei werden:
- Nicht-WAV-Dateien in das WAV-Format konvertiert,
- die Datei mittels eines vorgegebenen KI-Modells transkribiert,
- und das Ergebnis als Textdatei gespeichert.

## Ordnerstruktur
- **IN-Ordner:** Hier legst du die zu verarbeitenden Audiodateien ab (z. B. `.mp3`, `.wav`).
- **PROCESSED-Ordner:** Hier werden die Originaldateien abgelegt, nachdem sie vollständig bearbeitet wurden.
- **OUT-Ordner:** In diesem Ordner findest du die fertigen Textdateien sowie ggf. konvertierte WAV-Dateien.

## Anwendungsschritte
1. Öffne das NADOO Launchpad.
2. Aktiviere den Audio Converter Watchdog über die entsprechende Schaltfläche.
3. Über Einstellungen->Base Dir öffnen->Dir/converter/in 
4. Lege die gewünschte Audiodatei im **IN-Ordner** ab.
5. Der Watchdog erkennt die Datei, konvertiert sie bei Bedarf in WAV und startet die Transkription.
6. Nach Abschluss der Verarbeitung werden die Originaldateien in den **PROCESSED-Ordner** verschoben und im **OUT-Ordner** die fertigen Textdateien abgelegt.

## Anwendungsbeispiele
- **Automatisierte Dokumentation:**  
  Erstelle einen Wiki-Artikel, Protokolle oder Notizen aus Besprechungsaufnahmen.
  
- **KI-gestützte Weiterverarbeitung:**  
  Nutze den transkribierten Text als Basis, um Zusammenfassungen, Präsentationen oder Aufgabenlisten mithilfe weiterer KI-Tools zu generieren.
  
- **Archivierung und Suche:**  
  Durch die Umwandlung in Textform können Audiodateien leicht durchsucht und archiviert werden.

## Hinweise & Einschränkungen
- **Erstinstallation:**  
  Beim ersten Start wird das Speech-to-Text-Modell heruntergeladen, was ca. 15 Minuten in Anspruch nehmen kann.
  
- **Stabilität:**  
  Um Abstürze zu vermeiden, sollten derzeit nur einzelne Dateien nacheinander verarbeitet werden. Mehrere Dateien gleichzeitig können zu Problemen führen.
  
- **Verarbeitungszeit:**  
  - Kurze Audiodateien: wenige Minuten.  
  - Lange Aufnahmen (z. B. 1 Stunde): bis zu 45 Minuten, abhängig von Hardware und Betriebssystem.  
  - Hinweis: Windows arbeitet in der Regel schneller als macOS.

## Zusammenfassung
Das Speech-to-Text-Feature im NADOO Launchpad automatisiert die Umwandlung von Sprache in Text und spart so Zeit bei der Dokumentation. Es eignet sich hervorragend für Teams, die regelmäßig Besprechungen oder Präsentationen aufzeichnen und diese Inhalte anschließend weiterverarbeiten oder archivieren möchten. Beachte die anfängliche Downloadzeit und die aktuelle Limitierung bei der gleichzeitigen Verarbeitung mehrerer Dateien.

Für Fragen oder Probleme nutze bitte den Issue-Tracker im Repository des Projekts.

---

<p align="center">
<a href="/docs/04-tools/05-launchpad/02-features/07-wochenuebersicht/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/05-launchpad/02-features/09-create_snippets/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/05-launchpad/02-features/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
