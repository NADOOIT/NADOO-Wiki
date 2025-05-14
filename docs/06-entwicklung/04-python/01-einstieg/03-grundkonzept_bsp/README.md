# Python-Grundkonzepte: Veranschaulichung anhand eines Beispielskripts

## Das Skript

Hier ist ein **umfassendes Beispielskript**, das **grundlegende Python-Konzepte** erklärt:

```python
# Dies ist ein umfassendes Beispielskript, das grundlegende Python-Konzepte erklärt.
# Zeilen, die mit '#' beginnen, sind Kommentare und werden von Python nicht ausgeführt.

# 1. Variablen und Zuweisungen
# Variablen sind wie Behälter, in denen wir Daten speichern können.
zahl = 10  # Integer (Ganzzahl)
kommazahl = 3.14  # Float (Gleitkommazahl)
text = "Hallo, Welt!"  # String (Zeichenkette)
liste = [1, 2, 3, 4, 5]  # Liste (veränderbare Sequenz von Elementen)

# Bei Zuweisungen wird zuerst der Ausdruck rechts vom '=' ausgewertet, 
# dann wird das Ergebnis der Variable links zugewiesen.
a = b = c = 1 + 2 * 3  # Zuerst 2*3, dann 1+6, dann Zuweisungen von rechts nach links
print(f"a = {a}, b = {b}, c = {c}")

# 2. Funktionen
# Funktionen sind wiederverwendbare Codeblöcke.
def addiere(a, b):
    return a + b  # 'return' gibt das Ergebnis der Funktion zurück

# Funktionen werden erst bei Aufruf ausgeführt, nicht bei der Definition
ergebnis = addiere(5, 3)
print(f"5 + 3 = {ergebnis}")

# 3. Kontrollstrukturen
# If-Anweisung: Bedingte Ausführung von Code
if zahl == 10:  # '==' wird für Vergleiche verwendet, '=' für Zuweisungen
    print("Die Zahl ist 10")
else:
    print("Die Zahl ist nicht 10")

# For-Schleife: Iteration über eine Sequenz
for i in range(5):  # 'range(5)' erzeugt die Zahlen 0, 1, 2, 3, 4
    print(f"Schleifendurchlauf: {i}")

# While-Schleife: Wiederholung, solange eine Bedingung wahr ist
counter = 0
while counter < 3:
    print(f"While-Schleife: Zähler = {counter}")
    counter += 1  # Erhöht den Zähler um 1

# 4. Klassen und Objekte
# Eine Klasse ist wie ein Bauplan für Objekte.
class Auto:
    def __init__(self, marke, modell):
        # '__init__' ist der Konstruktor, aufgerufen bei Objekterstellung
        # 'self' bezieht sich auf das aktuelle Objekt
        self.marke = marke
        self.modell = modell
    
    def fahren(self):
        print(f"{self.marke} {self.modell} fährt.")

# Objekterstellung und -verwendung
mein_auto = Auto("VW", "Golf")
mein_auto.fahren()

# Erklärung zu 'self':
# 'self' ist wie ein Zeiger auf das aktuelle Objekt.
# Es ermöglicht den Zugriff auf Attribute und Methoden des spezifischen Objekts.

# 5. Gültigkeitsbereich (Scope)
globale_variable = "Ich bin global"

def funktion_mit_lokaler_variable():
    lokale_variable = "Ich bin lokal"
    print(globale_variable)  # Zugriff auf globale Variable ist möglich
    print(lokale_variable)

funktion_mit_lokaler_variable()
# print(lokale_variable)  # Dies würde einen NameError verursachen

# 6. Ausführungsreihenfolge und Besonderheiten
print("\nAusführungsreihenfolge und Besonderheiten:")

def beispiel_funktion():
    print("Diese Funktion wurde aufgerufen")

# Funktionsdefinitionen werden gelesen, aber nicht sofort ausgeführt
print("1. Dies wird zuerst ausgeführt")

if False:
    print("2. Dieser Code wird nie ausgeführt")

for i in range(0):
    print("3. Dieser Code wird auch nie ausgeführt")

print("4. Dies wird als Zweites ausgeführt")

# Jetzt rufen wir die Funktion auf
beispiel_funktion()

print("\nProgramm beendet")
```

## Ausführung des Skripts

Nachdem wir das Skript erstellt haben, können wir es ausführen, um zu sehen, wie die verschiedenen Konzepte in der Praxis funktionieren.

### Schritte zur Ausführung:

1. Speicher den Code in einer Datei namens `python_grundlagen.py`.
2. Öffne das Terminal in VS Code oder nutze ein anderes Terminalfenster.
3. Stelle sicher, dass deine virtuelle Umgebung aktiviert ist.
4. Führen das Skript mit folgendem Befehl aus:

```bash
python python_grundlagen.py
```

### Ausgabe des Skripts mit Erklärungen:

```
a = 7, b = 7, c = 7
# Erklärung: Dies zeigt das Ergebnis der Mehrfachzuweisung. 2*3 wird zuerst berechnet (6), 
# dann 1+6 (7) und schließlich wird 7 allen drei Variablen zugewiesen.

5 + 3 = 8
# Erklärung: Dies ist das Ergebnis des Funktionsaufrufs addiere(5, 3).

Die Zahl ist 10
# Erklärung: Die if-Bedingung (zahl == 10) ist wahr, daher wird diese Zeile ausgegeben.

Schleifendurchlauf: 0
Schleifendurchlauf: 1
Schleifendurchlauf: 2
Schleifendurchlauf: 3
Schleifendurchlauf: 4
# Erklärung: Die for-Schleife läuft 5-mal (0 bis 4) und gibt jeden Durchlauf aus.

While-Schleife: Zähler = 0
While-Schleife: Zähler = 1
While-Schleife: Zähler = 2
# Erklärung: Die while-Schleife läuft 3-mal (0 bis 2) und gibt den Zählerstand aus.

VW Golf fährt.
# Erklärung: Dies ist die Ausgabe der fahren()-Methode des Auto-Objekts.

Ich bin global
Ich bin lokal
# Erklärung: Dies zeigt den Zugriff auf globale und lokale Variablen in der Funktion.

Ausführungsreihenfolge und Besonderheiten:
1. Dies wird zuerst ausgeführt
4. Dies wird als Zweites ausgeführt
Diese Funktion wurde aufgerufen
# Erklärung: Dies demonstriert die Reihenfolge der Codeausführung und dass Funktionen 
# erst bei Aufruf ausgeführt werden.

Programm beendet
# Erklärung: Dies ist die letzte Ausgabe des Skripts.
```

### Detaillierte Erklärung der Ausführung:

1. **Variablen und Zuweisungen**: 
   - Die Mehrfachzuweisung `a = b = c = 1 + 2 * 3` wird korrekt ausgewertet und zugewiesen.
   - Zuerst wird `2 * 3` berechnet (6), dann `1 + 6` (7) und schließlich wird 7 allen drei Variablen zugewiesen.

2. **Funktionen**: 
   - Die `addiere()`-Funktion wird aufgerufen und gibt das korrekte Ergebnis zurück.
   - Der Aufruf `addiere(5, 3)` führt zur Berechnung und Ausgabe von 8.

3. **Kontrollstrukturen**:
   - Die `if`-Anweisung führt den richtigen Block aus, da `zahl == 10` wahr ist.
   - Die `for`-Schleife iteriert wie erwartet über den Bereich von 0 bis 4, insgesamt 5-mal.
   - Die `while`-Schleife läuft 3-mal (0 bis 2), wie durch die Bedingung `counter < 3` festgelegt.

4. **Klassen und Objekte**: 
   - Ein `Auto`-Objekt wird erstellt und seine `fahren()`-Methode aufgerufen.
   - Dies demonstriert die Objekterstellung und den Methodenaufruf in der Praxis.

5. **Gültigkeitsbereich**: 
   - Die Funktion zeigt den korrekten Zugriff auf globale und lokale Variablen.
   - Die globale Variable ist außerhalb der Funktion sichtbar, während die lokale Variable nur innerhalb der Funktion existiert.

6. **Ausführungsreihenfolge**: 
   - Die Ausgabe demonstriert, dass der Code grundsätzlich von oben nach unten ausgeführt wird.
   - Funktionen werden erst bei Aufruf ausgeführt, nicht bei ihrer Definition.
   - Bedingte Anweisungen (`if False:`) und Schleifen mit 0 Durchläufen (`for i in range(0):`) werden übersprungen.

Diese praktische Ausführung hilft, die theoretischen Konzepte in Aktion zu sehen und zu verstehen, wie Python-Code tatsächlich abläuft. Es ist oft hilfreich, Codebeispiele selbst auszuführen und mit ihnen zu experimentieren, um ein tieferes Verständnis zu entwickeln.

### Tipps für die erfolgreiche Ausführung des Skripts:

1. **Korrekte Python-Version**: Stelle sicher, dass du die richtige Python-Version verwenden (in diesem Fall Python 3.11).
2. **Virtuelle Umgebung**: Aktiviere die virtuelle Umgebung vor der Ausführung des Skripts.
3. **Dateipfad**: Vergewissere dich, dass du dich im richtigen Verzeichnis befindest, wenn du das Skript ausführst.
4. **Berechtigungen**: Stelle sicher, dass du die nötigen Berechtigungen hast, um das Skript auszuführen.
5. **Fehlerüberprüfung**: Solltest du Fehlermeldungen haben, melde diese umgehend Christoph Backhaus.

Durch das Verstehen und Anwenden dieser Konzepte in der Praxis legst du eine solide Grundlage für deine weitere Python-Entwicklung.
