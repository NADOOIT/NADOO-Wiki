# <p align="center">Überprüfung der Dateinamen</p>

Im Folgenden siehst du ein **Skript**, das du in Visual Studio Code einfügen kannst, um zu **überprüfen, ob deine Datei** gemäß den Benennungsrichtlinien **korrekt benannt wurde**. Es dient außerdem als Beispiel dafür, wie ein Skript zur **automatischen Validierung** von Dateinamen funktioniert.

## Das Skript:
<br>

```python
import os

import re

def check_filename(filename):

    # Regel 1: Monat als Zahl, keine führenden Nullen (months 1-9 should not have leading zeros)
    if re.search(r"zeitnachweis_\d{4}_(0[1-9]|[1-9][0-9])\.pdf", filename):
        if re.search(r"zeitnachweis_\d{4}_(0[1-9])\.pdf", filename):
            print(f"Ungültiger Monat in Datei: {filename} (Keine führenden Nullen erlaubt)")
            return False

    # Regel 2: KW 1 bis 52, keine führenden Nullen
    if re.search(r"berichtsheft_\d{4}_kw0[1-9]\.pdf", filename):  # Reject weeks with leading zero
        print(f"Ungültige KW in Datei: {filename} (Keine führenden Nullen erlaubt)")
        return False

    # Regel 3: Alle Buchstaben klein
    if not filename.islower():
        print(f"Ungültige Großbuchstaben in Datei: {filename}")
        return False

    # Regel 4: ID > Nachname > Name > Berichtsheft/Zeitrachnweis > Jahr > KW/Monat
    pattern = r"^(0?[1-9]|[1-9][0-9]{0,2})_[a-z]+_[a-z]+_(zeitnachweis_\d{4}_([1-9]|1[0-2])|berichtsheft_\d{4}_kw[1-5]?[0-9])\.pdf$"
    if not re.match(pattern, filename):
        print(f"Dateiname entspricht nicht der korrekten Reihenfolge: {filename}")
        return False

    print(f"Dateiname ist gültig: {filename}")
    return True


directory = "C:/Users/loren/Desktop/uuu"  # Verzeichnis, in dem die Dateien sind

for filename in os.listdir(directory):

    if filename.endswith(".pdf"):
        check_filename(filename)
```
<br>

### So sollte es aussehen:

<br>

![image](https://github.com/user-attachments/assets/ac00367f-542f-48ca-80ef-7af5ef06cc0d)

#

### Und so wendest du es an:
<br>

🎯 **1. Code in Visual Studio Code** via Copy-Paste **einfügen**.

🎯 **2.** In **Zeile 31** (Screenshot unten) den **Path eingeben**, in dem sich deine Dateien befinden.

<br>

![image](https://github.com/user-attachments/assets/5950250a-443e-4cd2-87e2-b8e4c36b45fd)

<br>

🎯 **3. Save As** > ***check_filenames.py***

🎯 **4. Play** drücken (Dreieck)

<br>

![image](https://github.com/user-attachments/assets/985e8e4d-6826-44f9-9d5a-23fcb74f3930)

#

#### Im Terminal sollte das jetzt so aussehen:

<br>

![image](https://github.com/user-attachments/assets/3ee0c843-075b-4fe5-ab45-ec3f27257491)

<br>

#

➡️ Es ist deutlich **erkennbar, was korrekt ist und was nicht**. Die Benennung sollte **entsprechend korrigiert** werden.

Die **neue Version** wurde um eine zusätzliche Regel für die ID **erweitert**, da jeder Teilnehmer eine spezifische ID (01 bis 999) erhält. 

💡 Eine **vorherige Version** des Skripts findest du im [**Issue #463**](
https://github.com/NADOOIT/NADOO-Launchpad/issues/463).

---

<p align="center">
<a href="/docs/01-organisation/03-zeit_und_ausbildungsnachweise/02-dateibenennung/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/01-organisation/04-urlaub/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/01-organisation/03-zeit_und_ausbildungsnachweise/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zur Kapitel-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>

---

<details>
<summary>Kompletten Themenbereich anzeigen</summary>
<br>

  &nbsp;&nbsp;🔹 [Arbeitszeit und Pausen](docs/01-organisation/01-arbeits_und_pausenzeiten/README.md) <br>
  &nbsp;&nbsp;🔹 [Erfassung deiner Arbeits- und Pausenzeiten mit dem NADOO-Launchpad](docs/01-organisation/02-zeiterfassung/README.md) <br>
#
📄 [zum Thema **Zeit- und Ausbildungsnachweise:**](docs/01-organisation/03-zeit_und_ausbildungsnachweise/README.md) <br>
  &nbsp;&nbsp;🔹 [Beispiele für Ausbildungs- und Zeitnachweise](docs/01-organisation/02-zeit_und_ausbildungsnachweise/01-beispiele/README.md) <br>
  &nbsp;&nbsp;🔹 [Dateibenennungsrichtlinien](docs/01-organisation/02-zeit_und_ausbildungsnachweise/02-dateibenennung/README.md) <br>
  &nbsp;&nbsp;🔹 [Überprüfung der Dateinamen](/docs/01-organisation/02-zeit_und_ausbildungsnachweise/03-ueberpruefung/README.md) <br>
#
  &nbsp;&nbsp;🔹 [Regelungungen für Urlaub und Freistellungen](docs/01-organisation/04-urlaub/README.md) <br>
  &nbsp;&nbsp;🔹 [Ablauf bei Krankmeldungen](docs/01-organisation/05-krankmeldungen/README.md) <br>
  &nbsp;&nbsp;🔹 [Gesetzliche Regelungen zu Mutterschutz und Elternzeit](/docs/01-organisation/06-mutterschutz_und_elternzeit/README.md) <br>
  &nbsp;&nbsp;🔹 [Umgang mit Unternehmensdaten bei Christoph Backhaus IT — Sicherheit und Vertraulichkeit als oberste Priorität](/docs/01-organisation/07-datenschutz/README.md) <br>
  #
📄 [zum Thema **Umgang und Kultur bei Christoph Backhaus IT — unsere Firmenphilosophien:**](docs/01-organisation/03-zeit_und_ausbildungsnachweise/README.md) <br>
  &nbsp;&nbsp;🔹 [Unsere Verhaltensregeln](/docs/01-organisation/08-firmenphilosophie/01-verhaltensregeln/README.md) <br>
  &nbsp;&nbsp;🔹 [Meinungsaustausch bei Christoph Backhaus IT: eine Kultur, die von Feedback lebt](/docs/01-organisation/08-firmenphilosophie/02-feedback-kultur/README.md) <br>
  &nbsp;&nbsp;🔹 [KAIZEN bei Christoph Backhaus IT: eine Kultur der kontinuierlichen Verbesserung](/docs/01-organisation/08-firmenphilosophie/03-kaizen/README.md) <br>

</details>