# <p align="center">Phase 2: Von der Idee zur Umsetzung</p>

## 1. Finde eine App-Idee

Bevor du mit dem Programmieren beginnst, ist es wichtig, eine geeignete Idee für deine erste App zu finden. Hier sind einige Richtlinien:

- **Halte es einfach**: Deine erste App sollte überschaubar sein. Ziel ist es, das in den Tutorials Gelernte anzuwenden, nicht ein komplexes Projekt zu erstellen.

- **Einfache GUI**: Strebe eine einfache grafische Benutzeroberfläche an. Idealerweise sollte deine App nur ein Fenster haben oder maximal einen Fensterwechsel beinhalten.

- **Brainstorming**: Nimm dir Zeit, mehrere Ideen zu sammeln, bevor du dich für eine entscheidest. Qualität entsteht oft durch Quantität bei Ideen.

- **Alltags- oder Hobbybezug**: Schau dich in deinem Alltag oder deinen Hobbys um. Oft finden sich dort Probleme, die durch eine einfache App gelöst werden können.

### Beispiele für einfache App-Ideen

1. To-Do-Liste mit KI-gestützter Priorisierung
2. Einfacher Taschenrechner mit Spracherkennung
3. KI-gestützter Zufallszahlengenerator mit Mustervorhersage
4. Einheitenumrechner mit natürlichsprachlicher Eingabe
5. KI-unterstütztes Quiz-Spiel mit dynamischer Schwierigkeitsanpassung
6. Intelligente Stoppuhr oder Timer mit Sprachsteuerung
7. Notizapp mit automatischer Kategorisierung und Zusammenfassung
8. KI-gesteuerter Würfel-Simulator mit Wahrscheinlichkeitsanalyse
9. Datumszähler mit KI-basierter Ereignisvorhersage
10. KI-gestützter Passwortgenerator mit Sicherheitsbewertung

Beachte, dass viele dieser App-Ideen durch die Integration von KI-Funktionen erheblich verbessert werden können. Im Kapitel [KI-Nutzung: Ein umfassender Leitfaden](docs/04-tools/05-ki/README.md) lernst du, wie du KI in deine App implementieren kannst. Der Abschnitt bietet außerdem wertvolle Einblicke in verschiedene KI-Tools und -Plattformen, die deine App-Entwicklung auf ein neues Level heben können.

In Abschnitt [7.1]<!--alter Abschnitt - wo sind die Informationen jetzt? (Stand: 13.05.25)--> findest du umfassende Informationen zu:

- Nutzung der ChatGPT API für natürliche sprachliche Interaktionen
- Lokale KI-Modelle mit Ollama für datenschutzsensible Anwendungen
- Zugriff auf eine Vielzahl von KI-Modellen über Hugging Face
- Spezielle KI-Anwendungen für Konvertierungen von Sprache-zu-Text, Text-zu-Sprache und Text-zu-Bild

Diese KI-Tools sind oft überraschend benutzerfreundlich und können auch von Anfängern effektiv eingesetzt werden. Sie bieten eine hervorragende Möglichkeit, deine erste App mit fortschrittlichen Funktionen auszustatten, ohne tiefgreifende KI-Kenntnisse zu benötigen.

Denke daran, dass der Einsatz von KI deine App zwar leistungsfähiger machen kann, aber achte darauf, den Umfang deines ersten Projekts überschaubar zu halten. Wähle eine Idee, die dich begeistert und die gleichzeitig realistisch für deine erste App-Entwicklung ist.

## 2. Erstelle ein eigenes neues Repository

Für deine erste App ist es wichtig, ein eigenes Repository zu erstellen. Dies hilft dir, deine Arbeit zu organisieren und Versionskontrolle zu üben.

1. Gehe zu GitHub (oder deiner bevorzugten Git-Plattform).
2. Klicke auf "New Repository".
3. Gib deiner App einen Namen (z.B. "meine-erste-toga-app").
4. Wähle "Public" oder "Private" je nach deinen Präferenzen.
5. Initialisiere das Repository mit einer README-Datei.
6. Klicke auf "Create Repository".

## 3. Erstelle deine App

Nun ist es Zeit, deine App zu erstellen! Hier sind die grundlegenden Schritte:

1. Klone dein neues Repository auf deinen lokalen Computer.

2. Öffne ein Terminal und navigiere zum geklonten Repository.

3. Erstelle eine neue Briefcase-App:

```plain
briefcase new
```

Folge den Anweisungen und verwende den Namen deiner App.

4. Öffne das Projekt in Visual Studio Code:

```bash
code .
```

5. Navigiere zur `app.py`-Datei in deinem Projekt und beginne mit der Implementierung deiner App-Logik.

6. Teste deine App regelmäßig mit:

   ```
   briefcase dev
   ```

7. Wenn du mit deiner App zufrieden bist, committe und pushe deine Änderungen zurück zu GitHub:

   ```
   git add .
   git commit -m "Erste Version meiner App"
   git push origin main
   ```

## Tipps für die Entwicklung

- **Inkrementelle Entwicklung**: Entwickle deine App in kleinen Schritten. Implementiere eine Funktion nach der anderen und teste häufig.
- **Kommentare**: Kommentiere deinen Code, um deine Gedankengänge festzuhalten und den Code verständlicher zu machen.
- **Fehlerbehandlung**: Denke an mögliche Fehler und wie deine App damit umgehen soll.
- **Benutzerfreundlichkeit**: Achte auf eine intuitive Benutzeroberfläche, auch wenn die App einfach ist.
- **Dokumentation**: Aktualisiere die README-Datei deines Repositories mit einer kurzen Beschreibung deiner App und Anweisungen zur Ausführung.

Viel Erfolg bei der Erstellung deiner ersten App! Denke daran, dass der Lernprozess genauso wichtig ist wie das Endergebnis. Zögere nicht, Fragen zu stellen oder Hilfe zu suchen, wenn du auf Probleme stößt.

---

#### Quellen:

[1] <https://peras.de/hr-blog/detail/ki-tools-unternehmen> <br>
[2] <https://www.ai-universe.com/ki-tools> <br>
[3] <https://cocosolution.com/de/blog/ki-ai-tools/> <br>
[4] <https://www.ingenieur.de/technik/fachbereiche/kuenstliche-intelligenz/kuenstliche-intelligenz-diese-15-ki-tools-sollten-sie-kennen/> <br>
[5] <https://www.synthesia.io/de/post/ki-tools> <br>
[6] <https://digitalzentrum-berlin.de/ki-tools-fuer-den-arbeitsalltag> <br>
[7] <https://www.121watt.de/ki/ki-tools-fuer-unternehmen/> <br>
[8] <https://digitale-lehre.uni-siegen.de/wissensdatenbank/ki-tools/> <br>

---

<p align="center">
<a href="/docs/06-entwicklung/07-digitale_produktentwicklung/01-idee_und_vorbereitung/README.md"><strong>Zurück</strong></a> | 
<a href="docs/06-entwicklung/07-digitale_produktentwicklung/03-feedback_und_testing/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/07-digitale_produktentwicklung/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zur Kapitel-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>