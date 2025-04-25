# 1.2.2 Dateinamen überprüfen

Dies ist ein Skript, das Du in Visual Studio Code einfügen kannst, um zu überprüfen, ob Deine Datei gemäß den Benennungsrichtlinien korrekt benannt wurde. Es dient als Beispiel dafür, wie ein Skript zur automatischen Validierung von Dateinamen funktioniert.

Skript:
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

So sollte es aussehen:
![image](https://github.com/user-attachments/assets/ac00367f-542f-48ca-80ef-7af5ef06cc0d)

1. Code in VSC mit copy paste einfügen.
2. In Zeile 31 (Screenshot unten) den Path eingeben, in dem sich Deine Dateien befinden.
3. Save As > check_filenames.py

![image](https://github.com/user-attachments/assets/5950250a-443e-4cd2-87e2-b8e4c36b45fd)

4. Play drücken (Dreieck)

![image](https://github.com/user-attachments/assets/985e8e4d-6826-44f9-9d5a-23fcb74f3930)

Im Terminal sollte das jetzt so aussehen:

![image](https://github.com/user-attachments/assets/3ee0c843-075b-4fe5-ab45-ec3f27257491)

Es ist deutlich erkennbar, was korrekt ist und was nicht. Die Benennung sollte entsprechend korrigiert werden.

Die neue Version wurde um eine zusätzliche Regel für die ID erweitert, da jeder Teilnehmer eine spezifische ID erhält. ( 01 bis 999 )

Eine vorherige Version des Skripts findest Du im Issue:
https://github.com/NADOOIT/NADOO-Launchpad/issues/463.