# 🗡️ **LEVEL 1 – Der erste Schlag: Baue deinen Charakter, kämpfe gegen dein Spiegelbild**

> *„Bevor du Magie webst oder Artefakte schmiedest, brauchst du eins: Ein Schwert.  
> Und das lernst du heute zu führen.“*  
>  
> *„Ein Hexer wird nicht geboren – er wird erschaffen.  
> Und der erste Test ist der Kampf gegen sich selbst.“*

---

## 🎯 **Deine Mission:**

Du baust ein einfaches Konsolen-Kampfsystem in **einer einzigen Java-Datei**.  
Noch ohne Klassen, Methoden oder saubere Struktur – dafür mit **Logik, Kontrolle und ersten Entscheidungen**.

Ziel: **Du kämpfst gegen einen Gegner**, der genau dieselben Startwerte wie du besitzt. Jeder von euch kann **angreifen, blocken oder einen Heiltrank trinken** – bis einer von euch besiegt ist.

---

## 🔧 **Setup – Was du vorbereiten musst:**

1. **Charakterwerte für dich selbst definieren:**
   - `String name` → über die Konsole eingeben
   - `int lebensPunkte` → z. B. 100
   - `int ausdauer` → z. B. 50
   - `String[] inventar` → z. B. `{"Heiltrank", "Heiltrank", "Heiltrank"}`

2. **Gegner initialisieren:**
   - Name: `"Dunkler Spiegel"`
   - Lebenspunkte, Ausdauer und Inventar sind **Kopien deiner Werte**

---

## 🕹️ **Spielmechanik – Dein erster Duell-Zauber**

Jede Runde läuft wie folgt ab:

- Spieler wählt eine Aktion (über Zahleneingabe mit `Scanner`):
  1. **Angriff** – Gegner verliert z. B. 10 Lebenspunkte, du verlierst 5 Ausdauer
  2. **Blocken** – Der nächste gegnerische Angriff macht nur halben Schaden
  3. **Heiltrank verwenden** – Nur wenn im Inventar vorhanden → +20 Lebenspunkte, Trank wird entfernt

- Danach führt der Gegner seine Aktion aus (z. B. immer Angriff oder zufällig)

- Beide Statuswerte werden angezeigt

- Spiel endet, wenn **einer von euch 0 oder weniger Lebenspunkte** hat

---

## 📜 **Regeln & Details:**

- Angriffe machen standardmäßig 10 Schaden
- Block reduziert den nächsten gegnerischen Schaden um die Hälfte (z. B. nur 5 statt 10)
- Heiltränke wirken nur, wenn noch vorhanden
- Wenn kein Trank mehr da ist, soll das Programm das erkennen und einen Hinweis ausgeben
- Nutze einfache `if`, `else`, `switch`, `while`-Strukturen
- Es reicht, wenn alles in der `main`-Methode steht!

---

## 🧠 **Wichtige Techniken, die du dabei übst:**

| Thema               | Anwendung im Spiel                                  |
|---------------------|-----------------------------------------------------|
| Variablen           | Lebenspunkte, Ausdauer, Name                        |
| Datentypen          | `int`, `String`, `String[]`, `boolean`             |
| Kontrollstrukturen  | `if`, `else`, `switch`, `while`                    |
| Operatoren          | `-`, `+`, `==`, `>=`, `<`, `!=`                     |
| Arrays              | Inventarverwaltung mit `String[]`                  |
| Eingabe & Ausgabe   | `Scanner`, `System.out.println()`                  |
| Zufall (optional)   | `Random` für Gegneraktionen (`import java.util.*`) |

---

## 🧪 **Deine XP-Quest:**

1. Baue alle Startwerte (Spieler und Gegner)
2. Schreibe eine Spielschleife, die jede Runde:
   - deinen Status anzeigt
   - eine Aktion abfragt
   - die gewählte Aktion ausführt
   - den Gegenzug ausführt
   - prüft, ob jemand besiegt ist
3. Zeige am Ende eine Sieges- oder Niederlagenmeldung

💥 **Bonus-XP:**

- Zähle, wie viele Heiltränke noch im Inventar sind  
- Entferne verbrauchte Tränke aus dem Array (z. B. durch `"leer"` ersetzen)  
- Lass den Gegner zufällig zwischen Angriff und Block wählen  
- Füge einen kleinen Verzögerungseffekt mit `Thread.sleep(1000);` ein

---

### 🧙‍♀️ **Hinweis für den Kodex-Lehrling:**
> Alles darf, nichts muss. Dieses Level ist dein Sandkasten.  
> Du brauchst keine Klassen, Methoden oder Modularisierung – es geht um das **Verständnis von Ablauf und Logik**.

---

> 🛡️ **+150 XP gesammelt für deinen ersten siegreichen Kampf!**  
> 🏰 **Nächstes Ziel:** In **Level 2** wirst du deinem Charakter eine eigene Klasse schenken – und damit zum wahren Codemagier. 🧙‍♂️

---

<p align="center">
<a href="/docs/06-entwicklung/05-java/01-tutorial/07-theorie/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/09-praxis-2/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/05-java/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zum Inhaltsverzeichis</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>