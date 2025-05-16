# <p align="center">**Debugging in Python**</p>

Debugging ist ein wesentlicher Teil des Programmierprozesses. In diesem Abschnitt werden wir verschiedene Debugging-Techniken anhand eines fehlerhaften Skripts erlernen.

## 1. Fehlerhaftes Beispielskript

Kopiere den folgenden Code in eine Datei namens `buggy_script.py`:

```python
# Dies ist ein Beispielskript mit verschiedenen Bugs und Grundkonzepten der Python-Programmierung

# Variablen: Behälter für Daten
zahl = 10
kommazahl = 3.14
text = "Hallo, Welt!"
liste = [1, 2, 3, 4, 5]

# Funktionen: Wiederverwendbare Codeblöcke
# Bug 1: Fehlender Doppelpunkt nach der Funktionsdefinition
def addiere(a, b)
    # Bug 2: Falsche Einrückung
  return a + b

# Kontrollstrukturen: Steuern den Programmablauf
# If-Anweisung: Bedingte Ausführung von Code
# Bug 3: Falscher Vergleichsoperator
if zahl = 10:
    print("Die Zahl ist 10")
else:
    print("Die Zahl ist nicht 10")

# For-Schleife: Iteration über eine Sequenz
# Bug 4: Fehlender Doppelpunkt nach der for-Schleife
# Bug 5: Verwendung einer nicht definierten Variable
for i in range(5)
    print(x)

# While-Schleife: Wiederholung, solange eine Bedingung wahr ist
# Bug 6: Endlosschleife
while True:
    print("Dies ist eine Endlosschleife")

# Klassen: Blaupausen für Objekte
class Auto:
    # Bug 7: Fehlender self-Parameter
    def __init__(marke, modell):
        self.marke = marke
        self.modell = modell
    
    # Bug 8: Falsche Methodendefinition
    def fahren()
        print(f"{self.marke} {self.modell} fährt.")

# Fehlerbehandlung: Umgang mit Ausnahmen
# Bug 9: Falsche Ausnahmebehandlung
try:
    resultat = 10 / 0
except:
    print("Ein Fehler ist aufgetreten")
finally
    print("Dies wird immer ausgeführt")

# Hauptprogramm
if __name__ == "__main__":
    # Bug 10: Falscher Funktionsaufruf
    ergebnis = addiere(5)
    print(f"Das Ergebnis ist: {ergebnis}")

    # Objekterstellung und -verwendung
    mein_auto = Auto("VW", "Golf")
    mein_auto.fahren()

print("Programm beendet")
```

## 2. Fehleranalyse

Führe das Skript aus und analysiere die Fehlermeldungen:

```bash
python buggy_script.py
```

Du wirst verschiedene Fehlermeldungen sehen. Lasse uns diese analysieren:

1. `SyntaxError`: Fehlender Doppelpunkt nach der Funktionsdefinition (Zeile 11)
2. `IndentationError`: Falsche Einrückung in der Funktion (Zeile 13)
3. `SyntaxError`: Falscher Vergleichsoperator (= statt ==) (Zeile 18)
4. `SyntaxError`: Fehlender Doppelpunkt nach der for-Schleife (Zeile 25)
5. `NameError`: Verwendung einer nicht definierten Variable x (Zeile 26)
6. Endlosschleife (kein Syntaxfehler, aber logischer Fehler) (Zeile 30-31)
7. `TypeError`: Fehlender self-Parameter in der Klassenmethode (Zeile 36)
8. `SyntaxError`: Fehlender Doppelpunkt nach der Methodendefinition (Zeile 41)
9. `SyntaxError`: Fehlender Doppelpunkt nach finally (Zeile 49)
10. `TypeError`: Falscher Funktionsaufruf (fehlender Parameter) (Zeile 54)

## 3. Debugging-Techniken

### 3.1 Print-Debugging

Print-Debugging ist die einfachste Methode zur Fehlersuche. Dabei fügst du print-Anweisungen in deinen Code ein, um Variablenwerte oder den Programmfluss zu überprüfen:

```python
print(f"Der Wert von zahl ist: {zahl}")
```

Diese Methode ist besonders nützlich für schnelle Überprüfungen, kann aber bei größeren Programmen unübersichtlich werden.

### 3.2 Logging

Logging ist eine fortgeschrittenere Form des Print-Debuggings. Es ermöglicht eine strukturiertere Ausgabe und kann leicht aktiviert oder deaktiviert werden:

```python
import logging

logging.basicConfig(level=logging.DEBUG, format='%(asctime)s - %(levelname)s - %(message)s')
logging.debug(f"Der Wert von zahl ist: {zahl}")
```

Logging bietet verschiedene Ausgabeebenen (DEBUG, INFO, WARNING, ERROR, CRITICAL) und kann in Dateien schreiben, was es ideal für größere Projekte macht.

### 3.3 Verwendung des Python Debuggers in VS Code

Der integrierte Debugger in VS Code ist ein mächtiges Werkzeug für die Fehlersuche:

1. Setze Breakpoints, indem du links neben die Zeilennummern in VS Code klickst.
2. Klicke auf "Run and Debug" in der Seitenleiste von VS Code.
3. Wähle "Python File" aus dem Dropdown-Menü.
4. Klicke auf den grünen Play-Button oder drücke F5.

Mit dem Debugger kannst du:

- Variablenwerte inspizieren
- Schrittweise durch den Code gehen (Step Over, Step Into, Step Out)
- Die Ausführung fortsetzen oder abbrechen

Dies ermöglicht eine detaillierte Analyse des Programmablaufs und ist besonders nützlich bei komplexen Fehlern.

## 4. Fehlerbehebung

Hier ist der korrigierte Code:

```python
def addiere(a, b):
    return a + b

if zahl == 10:
    print("Die Zahl ist 10")
else:
    print("Die Zahl ist nicht 10")

for i in range(5):
    print(i)

counter = 0
while counter < 5:
    print(f"Schleifendurchlauf {counter}")
    counter += 1

class Auto:
    def __init__(self, marke, modell):
        self.marke = marke
        self.modell = modell
    
    def fahren(self):
        print(f"{self.marke} {self.modell} fährt.")

try:
    resultat = 10 / 0
except ZeroDivisionError:
    print("Division durch Null ist nicht erlaubt")
finally:
    print("Dies wird immer ausgeführt")

if __name__ == "__main__":
    ergebnis = addiere(5, 3)
    print(f"Das Ergebnis ist: {ergebnis}")

    mein_auto = Auto("VW", "Golf")
    mein_auto.fahren()

print("Programm erfolgreich beendet!")
```

## 5. Debugging-Tipps

1. Lies die Fehlermeldungen sorgfältig. Sie enthalten oft wertvolle Informationen über den Ort und die Art des Problems.
2. Verwende print-Anweisungen oder Logging, um den Zustand von Variablen an kritischen Stellen zu überprüfen.
3. Nutze den VS Code Debugger, um komplexe Probleme zu lösen und den Programmablauf Schritt für Schritt nachzuvollziehen. 
4. Teste deinen Code regelmäßig in kleinen Abschnitten, um Fehler frühzeitig zu erkennen.
5. Kommentiere deinen Code ausführlich, aber halte die Kommentare prägnant und informativ, um die Lesbarkeit und das Verständnis zu verbessern.

Debugging ist eine Fähigkeit, die mit der Zeit und Übung verbessert wird. Je mehr du debuggst, desto besser wirst du darin, Fehler schnell zu identifizieren und zu beheben.

## 6. Weiterführende Ressourcen

### Deutsche Tutorials

- 🔗 [Python Debugging: Eine Einführung](https://www.python-lernen.de/debugging-in-python.htm)
- 🔗 [Debugging in Python mit pdb](https://www.digitalocean.com/community/tutorials/how-to-use-the-python-debugger-de)

### Englische Tutorials

- 🔗 [Real Python: Python Debugging With Pdb](https://realpython.com/python-debugging-pdb/)
- 🔗 [Visual Studio Code Python Debugging](https://code.visualstudio.com/docs/python/debugging)
- 🔗 [Bitecode: What's up Python? Better packaging and better debugging](https://www.bitecode.dev/p/whats-up-python-better-packaging)

### Video-Tutorials

- 🔗 [Python Debugging in VS Code (Deutsch)](https://www.youtube.com/watch?v=w8QHoVam1-I)
- 🔗 [Python Debugging Techniques (Englisch)](https://www.youtube.com/watch?v=_aCGeGvVoLk)

Diese Ressourcen bieten zusätzliche Einblicke und praktische Übungen, um deine Debugging-Fähigkeiten zu verbessern. Denke daran, dass effektives Debugging eine Kombination aus Wissen, Erfahrung und Geduld erfordert. Mit der Zeit wirst du immer besser darin, Fehler zu finden und zu beheben.

### Quellen

[1] <https://python.plainenglish.io/popular-and-easy-debugging-techniques-for-python-applications-79d6b8dd2999?gi=08e89f39b1d5> <br>
[2] <https://databasecamp.de/en/python-coding/debugging-en> <br>
[3] <https://apidog.com/blog/how-to-debug-in-python/> <br> 
[4] <https://www.linkedin.com/advice/0/what-some-common-debugging-tools-techniques-1f> <br>  
[5] <https://realpython.com/python-debugging-pdb/> <br> 
[6] <https://www.skillreactor.io/blog/how-to-debug-python-in-vscode/> <br>
[7] <https://www.fullstackpython.com/debugging.html> <br>
[8] <https://www.freecodecamp.org/news/python-debugging-handbook/> <br>

---

<p align="center"><a href="/docs/06-entwicklung/04-python/01-einstieg/03-grundkonzept_bsp/README.md"><strong>Zurück</strong></a> | <a href="/docs/06-entwicklung/05-java/README.md"><strong>Weiter</strong></a></p>