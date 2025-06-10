# 🏰 **LEVEL 2 – Der Weg des Codemagiers**

> *„Ein Hexer mit einem Schwert kann kämpfen. Ein Hexer mit System kann Kriege entscheiden.“*

In diesem Level kehrst du zurück zu deinem ersten Spiel – aber diesmal mit **Ordnung, Struktur und echten Objekten**. Du nimmst, was du in Level 1 gebaut hast, und entwickelst es **weiter und größer**.

Statt eines einzigen Chaos-Blocks voller Code, wirst du nun mit **Klassen arbeiten**, mit eigenen **Dateien**, mit **Objekten**, **Vererbung** und dem ersten Hauch echter Softwarearchitektur.

---

## 🎯 **Deine Mission:**

Du nimmst dein Spiel aus **Level 1** und strukturierst es um – diesmal:
- in **mehrere Java-Dateien**
- mit **eigenen Klassen** (z. B. für Spieler, Gegner, Aktionen)
- und mit neuen **Fähigkeiten**, die dein Charakter erlernen kann.

Außerdem erweiterst du den Kampf um **verschiedene Angriffsarten**, die sich in Schaden und Ausdauerverbrauch unterscheiden, und um ein **Ausdauer-Regenerationssystem**.

---

## 🔨 **Was konkret zu tun ist:**

### 🧱 1. Strukturiere deinen Code um

Trenne deinen bisherigen Code in sinnvolle Java-Dateien auf. **Wie du das aufteilst, entscheidest du selbst** – aber hier ein paar Denkanstöße:

- Eine Klasse `Spieler` (oder `Charakter`) könnte alle Werte und Methoden rund um das Wesen enthalten (z. B. `angreifen()`, `trinkeTrank()`, `zeigeStatus()`).
- Eine Klasse `Aktion` könnte verschiedene Aktionen beschreiben.
- Eine Klasse `Kampf` oder `Spielablauf` könnte die Spielschleife und die Logik der Runden enthalten.
- Eine eigene `Main.java` dient als Einstiegspunkt (hier startet dein Spiel).

> 💡 Nutze Konstruktoren, um deine Objekte mit Startwerten zu versorgen. 
> Getter und Setter schützen deine Felder, `toString()` hilft bei Statusanzeigen.


---

### ⚔️ 2. Erweitere dein Kampfsystem

Es gibt jetzt mehrere Aktionen, die unterschiedliche Effekte und **unterschiedlichen Ausdauerverbrauch** haben. **Diese Logik musst du planen und strukturieren.**

#### Verfügbare Aktionen:

| Aktion             | Wirkung                         | Ausdauerkosten |
|-------------------|----------------------------------|----------------|
| Leichter Angriff  | z. B. 5–10 Schaden               | 2              |
| Schwerer Angriff  | z. B. 10–20 Schaden              | 4              |
| Blocken           | Schaden halbieren nächste Runde | 2              |
| Trank trinken     | +20 Leben (falls vorhanden)      | 1              |
| **Passen**        | keine Aktion, nur aussetzen      | 0              |

#### Weitere Spielregel:
- **Jede Runde regeneriert der Spieler automatisch 2 Ausdauerpunkte**, maximal bis zum ursprünglichen Startwert.
- Hat ein Spieler **nicht genug Ausdauer**, darf er **nur "Passen"** wählen.

> 💡 Die Entscheidung, **ob eine Aktion erlaubt ist**, könntest du z. B. in einer Methode `istAusfuehrbar()` prüfen.
> Du könntest dafür eine `Aktion`-Klasse oder ein `enum` nutzen, das Name, Kosten und Wirkung beschreibt.

---

## 🧠 **Techniken aus Level 2, die du gezielt anwenden kannst:**

| Technik              | Mögliche Anwendung                                                                 |
|----------------------|-----------------------------------------------------------------------------------|
| `class`              | Für `Spieler`, `Aktion`, `Gegner`, `Kampf`, ggf. `Spiel`                          |
| Konstruktoren        | Um Startwerte festzulegen (`new Spieler("Geralt", 100, 50)`)                      |
| Methoden             | Für Aktionen wie `angreifen()`, `blocken()`, `zeigeStatus()`, `regeneriere()`     |
| Getter/Setter        | Um Lebenspunkte und Ausdauer geschützt zu lesen/verändern                         |
| `toString()`         | Für schöne Statusausgaben                                                         |
| `private`/`public`   | Um interne Logik zu kapseln und eine saubere API zu schaffen                      |
| (Optional) `extends` | Wenn `Gegner` und `Spieler` sich z. B. eine gemeinsame Oberklasse `Charakter` teilen |

> 🧙‍♂️ Tipp: Überlege **vor dem Coden**, wie du die Aufgaben und Daten verteilen willst. Mach dir eine kleine Skizze deiner Klassen, Felder und Zuständigkeiten.

---

## 🧪 **Deine XP-Quest:**

1. Zerlege dein Spiel in **mehrere Java-Klassen** mit klarer Aufgabenverteilung.
2. Erweitere das Kampfsystem um:
   - **Unterschiedliche Angriffsarten mit Schadensberechnung**
   - **Unterschiedliche Ausdauerkosten**
   - **Automatische Ausdauer-Regeneration pro Runde** (bis zum Maximalwert)
   - **Zwang zum „Passen“, wenn keine Aktion mehr erlaubt ist**
3. Nutze die Techniken aus Level 2 sinnvoll und gezielt.

💥 **Bonus-XP:**
- Lasse Gegneraktionen zufällig oder abhängig von ihrer aktuellen Ausdauer entscheiden.
- Baue die Aktionen so, dass sie in einer eigenen Struktur verwaltet werden können (z. B. `List<Aktion>`).
- Trenne Anzeige (Textausgabe) und Spiellogik stärker (z. B. eigene `Statusanzeige`-Methode oder Klasse).

---

> 🧙‍♀️ *„Ein Codemagier schreibt nicht einfach Code – er entwirft ein System.“*
> **Bist du bereit für deinen ersten architektonisch durchdachten Zauber?**
