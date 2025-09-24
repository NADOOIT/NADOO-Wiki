# <p align="center">Debugging und Fehlerbehandlung in Briefcase und Toga</p>

Fehler sind ein natürlicher Teil des Entwicklungsprozesses. Sie zeigen dir, wo du deine Annahmen überprüfen und deinen Code verbessern musst. In diesem Abschnitt wirst du lernen, wie du Fehler effektiv identifizierst, analysierst und behebst.

## Ein fehlerhaftes Beispielprogramm

Lass uns ein einfaches Briefcase/Toga-Programm erstellen, das absichtlich einige Fehler enthält. Erstelle zunächst eine neue Briefcase-App:

```bash
briefcase new
```

Folge den Anweisungen und nenne die App "BuggyApp". Öffne dann die Datei `src/buggyapp/app.py` und ersetze den Inhalt durch folgenden Code:

```python
# Fehler 1: Fehlender Import
# Dies ist ein häufiger Fehler. Wenn Du eine Bibliothek oder ein Modul verwendest, 
# aber vergisst, es zu importieren, erhältst Du einen NameError.
# from toga.style.pack import COLUMN, ROW

import toga
from toga.style import Pack

class BuggyApp(toga.App):
    def startup(self):
        # Fehler 2: Verwendung eines nicht importierten Moduls
        # Dies führt zu einem NameError, da COLUMN nicht definiert ist
        main_box = toga.Box(style=Pack(direction=COLUMN))

        name_label = toga.Label('Your name: ')
        self.name_input = toga.TextInput()

        button = toga.Button('Say Hello', on_press=self.say_hello)
        
        main_box.add(name_label)
        main_box.add(self.name_input)
        main_box.add(button)

        self.main_window = toga.MainWindow(title=self.formal_name)
        self.main_window.content = main_box
        self.main_window.show()

    def say_hello(self, widget):
        name = self.name_input.value
        # Fehler 3: Falscher Zuweisungsoperator
        # Dies ist ein SyntaxError. In Python wird '==' für Vergleiche verwendet, 
        # während '=' für Zuweisungen reserviert ist.
        if name = "":
            greeting = f"Hello, {name}!"
        # Fehler 4: Fehlender Doppelpunkt
        # Dies ist ein SyntaxError. In Python muss nach einem 'else' immer ein ':' folgen.
        else
            greeting = "Please enter your name."
        
        # Fehler 5: Tippfehler im Variablennamen
        # Dies führt zu einem NameError, da 'greting' nicht definiert ist.
        # Solche Fehler sind oft schwer zu erkennen, besonders in größeren Codebasen.
        self.main_window.info_dialog('Greeting', greting)

        # Fehler 6: Inkonsistente Einrückung
        # Dies würde einen IndentationError verursachen. Python verwendet Einrückungen
        # zur Strukturierung des Codes, daher ist konsistente Einrückung entscheidend.
         print("This line is incorrectly indented")

    # Fehler 7: Unvollständige Funktion
    # Dies würde einen IndentationError verursachen, da Python erwartet, 
    # dass eine Funktion mindestens eine Anweisung enthält.
    def unfinished_function():

# Fehler 8: Falsche Methodensignatur
# Dies würde zu einem TypeError führen, da die Methode 'main' in der Klasse 'toga.App'
# keine Argumente erwartet, hier aber eines übergeben wird.
def main(unused_arg):
    return BuggyApp('Buggy App', 'org.example.buggyapp')

if __name__ == '__main__':
    main().main_loop()
```

## Fehler identifizieren und verstehen

Versuche nun, die App zu starten:

```bash
briefcase dev
```

Du wirst mehrere Fehler sehen. Lass uns diese analysieren:

1. **Syntaxfehler**: Python wird einen SyntaxError in der Zeile `if name = "":` melden. Der korrekte Vergleichsoperator in Python ist `==`, nicht `=`.

2. **Einrückungsfehler**: Nach dem `else` fehlt ein Doppelpunkt `:`. Python verwendet Einrückungen zur Strukturierung des Codes, daher ist dies ein kritischer Fehler.

3. **Namenfehler**: In der letzten Zeile der `say_hello`-Methode gibt es einen Tippfehler: `greting` statt `greeting`.

## Fehler beheben

Lass uns diese Fehler Schritt für Schritt beheben:

1. Ändere `if name = ""` zu `if name == ""`.
2. Füge einen Doppelpunkt nach `else` hinzu: `else:`.
3. Korrigiere den Tippfehler: Ändere `greting` zu `greeting`.

## Debugging-Techniken

### Print-Anweisungen

Eine einfache, aber effektive Methode zum Debuggen ist das Einfügen von Print-Anweisungen. Füge zum Beispiel folgende Zeile am Anfang der `say_hello`-Methode hinzu:

```python
print(f"Debug: Name eingegeben: {name}")
```

### Logging

Für fortgeschritteneres Debugging und dauerhafte Aufzeichnungen kannst du das `logging`-Modul verwenden. Füge am Anfang der Datei hinzu:

```python
import logging

logging.basicConfig(level=logging.DEBUG, filename='app.log', filemode='w',
                    format='%(name)s - %(levelname)s - %(message)s')
```

Und in der `say_hello`-Methode:

```python
logging.debug(f"Name eingegeben: {name}")
```

Dies schreibt Debug-Informationen in eine Datei namens `app.log`.

## Fazit

Fehler sind ein wichtiger Teil des Lernprozesses. Sie zeigen dir, wo du deine Fähigkeiten verbessern kannst. Mit der Zeit und mehr Erfahrung wirst du in der Lage sein, komplexere Features zu entwickeln und weniger Fehler zu machen. Dennoch bleiben Fehler ein natürlicher Teil des Entwicklungsprozesses, selbst für erfahrene Programmierer.

Erinnere dich:

- Lies Fehlermeldungen sorgfältig. Sie enthalten oft wertvolle Informationen über den Ort und die Art des Problems.
- Nutze Print-Anweisungen und Logging, um den Zustand deines Programms zu verschiedenen Zeitpunkten zu überprüfen.
- Mach dir keine Sorgen über Fehler. Jeder Fehler ist eine Gelegenheit zu lernen und deinen Code zu verbessern.

In zukünftigen Tutorials werden wir fortgeschrittenere Techniken zur Fehlervermeidung und zum Schreiben von robusterem Code kennenlernen. Bis dahin: Fürchte dich nicht vor Fehlern, sondern nutze sie als Lernchancen!

Ein spannendes Video, das von den berühmtesten und größten Bugs berichtet:

[https://www.youtube.com/watch?v=Iq_r7IcNmUk](https://www.youtube.com/watch?v=Iq_r7IcNmUk)

---

**Dieses Thema beinhaltet folgende Kapitel:**
---

🔹 [**Briefcase**](/docs/06-entwicklung/01-dokumentation/README.md)<br>
🔹 [**Toga**](/docs/06-entwicklung/02-clean_architecture/README.md) <br>
🔹 [**Zusammenspiel**](/docs/06-entwicklung/02-clean_architecture/README.md) <br>
🔹 [**Debugging**](/docs/06-entwicklung/02-clean_architecture/README.md) <br>

---

<p align="center">
<a href="/docs/06-entwicklung/06-frameworks/02-briefcase_und_toga/03-zusammenspiel/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/07-digitale_produktentwicklung/README.md"><strong>Weiter</strong></a>
</p>