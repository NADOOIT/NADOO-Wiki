# 🧨 **LEVEL 5: Werde Fehlermeister**

> *„Ein guter Hexer verlässt sich nicht darauf, dass alles glatt läuft.  
> Er ist vorbereitet, wenn ein Trank explodiert oder ein Monster stärker ist als gedacht.“*  
>  
> In Java heißt das: **Ausnahmen erkennen, behandeln und gezielt werfen**.  
> Du wirst lernen, wie du dein Programm **robust und fehlertolerant** machst – ohne Kontrollverlust.

---

## ⚠️ **5.1 `try`, `catch`, `finally` – Mit Bedacht**

### 🧭 **Was sind Exceptions (Ausnahmen)?**

Ausnahmen sind **besondere Ereignisse**, die deinen Code unterbrechen, wenn **etwas schiefgeht**.

Beispiel:
```java
int zahl = Integer.parseInt("abc");  // ❌ Fehler! Keine Zahl!
```

Das wirft eine Exception (`NumberFormatException`). Wenn du sie **nicht fängst**, fliegt dir dein Programm um die Ohren.

---

## 🛡️ **Fehler abfangen mit `try` und `catch`**

```java
try {
    int zahl = Integer.parseInt("abc");
    System.out.println("Zahl: " + zahl);
} catch (NumberFormatException e) {
    System.out.println("Fehler beim Umwandeln! Eingabe war keine Zahl.");
}
```

> 💡 **Erklärung:**
> - `try`: Bereich, in dem ein Fehler auftreten *könnte*.
> - `catch`: Wird aktiviert, **wenn** der Fehler auftritt.
> - Du kannst dann **kontrolliert reagieren**, statt dass dein Programm abstürzt.

---

## 🔄 **`finally` – Der Teil, der immer ausgeführt wird**

```java
try {
    // gefährlicher Code
} catch (Exception e) {
    // Fehlerbehandlung
} finally {
    // Wird immer ausgeführt – egal ob Fehler oder nicht
}
```

Typischer Anwendungsfall: **Ressourcen schließen**, z. B. Dateien, Streams, Verbindungen.

---

## 🧪 **Beispiel: Hexer-Zahleneingabe**

```java
Scanner scanner = new Scanner(System.in);
try {
    System.out.print("Gib eine Zahl ein: ");
    int level = Integer.parseInt(scanner.nextLine());
    System.out.println("Hexer-Level: " + level);
} catch (NumberFormatException e) {
    System.out.println("Ungültige Eingabe. Bitte nur ganze Zahlen.");
} finally {
    scanner.close();  // Wird immer geschlossen!
}
```

---

## 🧠 **Welche Exceptions gibt es?**

Java kennt zwei Hauptarten:

| Typ            | Beschreibung                              |
|----------------|-------------------------------------------|
| **Unchecked**  | Laufzeitfehler (z. B. `NullPointerException`, `IndexOutOfBoundsException`) |
| **Checked**    | Müssen *zwingend* behandelt werden (z. B. `IOException`, `SQLException`) |

> Du wirst beide Typen in deinem Hexerleben begegnen – manche sind vorhersehbar, andere überraschend.

---

## 🏆 **Deine XP-Quest:**

1. Baue eine Methode `parseLevel(String eingabe)`, die versucht, einen String in eine Zahl umzuwandeln – mit `try-catch`.  
   Gib eine freundliche Fehlermeldung aus, wenn es schiefläuft.

2. Baue ein `finally`, das `"Levelprüfung abgeschlossen."` ausgibt – **immer**, egal ob erfolgreich oder nicht.

💥 **Bonus-XP:**  
Simuliere eine Benutzereingabe mit `"abc"` und `"5"` und teste beide Fälle.

---

> 🛡️ **+100 XP für kontrollierte Fehlerbeherrschung gesammelt!**  
> **Nächstes Ziel:** Unterschied zwischen `throw` und `throws` – Wirf deine eigenen Ausnahmen!

---

# 🧨 **LEVEL 5.2: Unterschied zwischen `throw` und `throws` – Wirf deine eigenen Ausnahmen**

> *„Ein Hexer wartet nicht auf das Unvermeidliche.  
> Er spricht den Zauber der Warnung – und unterbricht, bevor es zu spät ist.“*  
>  
> In Java kannst du nicht nur Ausnahmen **fangen**, sondern auch **selbst auslösen**.  
> Dafür brauchst du:  
> - `throw`: Um **eine bestimmte Ausnahme zu werfen**  
> - `throws`: Um **anzukündigen, dass eine Methode eine Ausnahme werfen könnte**

---

## 🗡️ **`throw` – Wirf eine Ausnahme**

Mit `throw` schleuderst du eine Exception wie einen magischen Splitter mitten in den Codefluss.

### 🧪 Beispiel:

```java
public void trankEinnehmen(int staerke) {
    if (staerke < 0) {
        throw new IllegalArgumentException("Ein Trank kann keine negative Stärke haben!");
    }
    System.out.println("Du hast einen Trank mit Stärke " + staerke + " eingenommen.");
}
```

> 💡 Du verwendest ein Objekt vom Typ `Exception` und **wirfst** es mit `throw`.

---

## 📜 **`throws` – Warnung im Methodenkopf**

Mit `throws` sagst du:  
> *„Diese Methode **kann** eine bestimmte Ausnahme werfen – sei vorbereitet!“*

Das ist besonders wichtig bei **Checked Exceptions**, die du nicht ignorieren darfst.

### Beispiel:

```java
public void liesMagieSpruch() throws IOException {
    BufferedReader reader = new BufferedReader(new FileReader("zauber.txt"));
    String spruch = reader.readLine();
    System.out.println("Spruch: " + spruch);
    reader.close();
}
```

Hier muss der Aufrufer mit `try-catch` arbeiten, weil `IOException` **gefangen oder weitergeworfen** werden muss.

---

## ⚔️ **`throw` vs. `throws` im Überblick**

| Schlüsselwort | Bedeutung                           | Wo wird’s geschrieben?               |
|---------------|--------------------------------------|--------------------------------------|
| `throw`       | Wirft eine **konkrete** Ausnahme     | **im Methodenrumpf**                 |
| `throws`      | Meldet an, dass eine Ausnahme **auftreten kann** | **im Methodenkopf**              |

---

## 🧙‍♂️ **Eigene Exceptions schreiben – Deine eigenen Warnzauber**

Du kannst eigene Exception-Klassen definieren – für spezifische Fälle:

```java
public class UngültigerTrankException extends Exception {
    public UngültigerTrankException(String message) {
        super(message);
    }
}
```

Verwendung:

```java
public void trankEinnehmen(int staerke) throws UngültigerTrankException {
    if (staerke <= 0) {
        throw new UngültigerTrankException("Ungültiger Trank! Stärke muss positiv sein.");
    }
}
```

---

## 🏆 **Deine XP-Quest:**

1. Schreibe eine Methode `wirfWennLeer(String text)`, die eine `IllegalArgumentException` **wirft**, wenn der übergebene Text leer ist.

2. Baue eine eigene Exception `VerbotenesZeichenException` und schreibe eine Methode `wirkeZeichen(String zeichen)`, die diese Ausnahme wirft, wenn `zeichen.equals("Avada Kedavra")`.

💥 **Bonus-XP:**  
Erweitere `wirkeZeichen()` so, dass sie mit `throws` im Methodenkopf deklariert und von `main()` mit `try-catch` behandelt wird.

---

> 🛡️ **+150 XP für gezielte Fehlererzeugung gesammelt!**  
> **Nächstes Ziel:** Eigene Exceptions schreiben wie Zaubersprüche – mit Stil und Aussagekraft.

---

# 🔮 **LEVEL 5.3: Eigene Exceptions schreiben – wie Zaubersprüche**

> *„Wer einen Fehler erkennt, soll ihn beim Namen nennen.  
> Nur so kann man ihn zähmen und verstehen.“*

In diesem Abschnitt lernst du, wie du:
- **Eigene Exception-Klassen** baust  
- **Spezifische Fehlertypen** unterscheidest  
- Deinen Code **lesbarer und robuster** machst

---

## 🛠️ **Warum eigene Exceptions?**

Statt pauschal `RuntimeException` oder `IllegalArgumentException` zu werfen,  
kannst du **konkrete, sprechende Fehlertypen** definieren.

Beispiele:
- `UnbekanntesMonsterException`
- `VerbotenesZeichenException`
- `HexerZuSchwachException`

Das macht deinen Code:
- **leichter zu verstehen**
- **zielgerichteter zu behandeln**
- **besser wartbar** (besonders bei größeren Systemen)

---

## 🧭 **So baust du eine eigene Exception:**

### 🧱 Schritt 1: Neue Klasse anlegen

```java
public class VerbotenesZeichenException extends Exception {
    public VerbotenesZeichenException(String nachricht) {
        super(nachricht);
    }
}
```

- Erbt von `Exception` → das macht sie zu einer **Checked Exception**.
- Willst du lieber eine **Unchecked Exception** (keine `throws`-Pflicht),  
  dann erbe von `RuntimeException`.

---

### 🧙‍♂️ Schritt 2: Verwenden der Exception

```java
public void wirkeZeichen(String zeichen) throws VerbotenesZeichenException {
    if ("Avada Kedavra".equals(zeichen)) {
        throw new VerbotenesZeichenException("Das Zeichen '" + zeichen + "' ist verboten!");
    }
    System.out.println("Du wirkst: " + zeichen);
}
```

---

### 🔄 Schritt 3: Behandlung beim Aufrufer

```java
try {
    wirkeZeichen("Avada Kedavra");
} catch (VerbotenesZeichenException e) {
    System.out.println("⚠️ Zauberfehler: " + e.getMessage());
}
```

---

## 🧩 **Checked vs Unchecked – Wann was?**

| Eigenschaft               | Checked Exception (`extends Exception`) | Unchecked Exception (`extends RuntimeException`) |
|---------------------------|------------------------------------------|---------------------------------------------------|
| Muss mit `throws` deklariert werden? | ✅ Ja                       | ❌ Nein                                       |
| Muss abgefangen werden?   | ✅ Ja                       | ❌ Nein                                       |
| Wann verwenden?           | Für vorhersehbare Fehler                 | Für Programmierfehler oder seltene Sonderfälle  |

> 💡 Faustregel:  
> - Ist es **Teil der normalen Programmlogik**, nutze `Exception`.  
> - Ist es ein **Programmierfehler oder Sonderzustand**, nutze `RuntimeException`.

---

## 🧪 **Beispiel: `HexerZuSchwachException`**

```java
public class HexerZuSchwachException extends Exception {
    public HexerZuSchwachException(String message) {
        super(message);
    }
}
```

```java
public void oeffnePortal(int hexerLevel) throws HexerZuSchwachException {
    if (hexerLevel < 10) {
        throw new HexerZuSchwachException("Level zu niedrig für Portalmagie!");
    }
    System.out.println("Du öffnest ein Portal nach Kaer Morhen.");
}
```

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine eigene Exception `UnbekanntesMonsterException`.  
2. Schreibe eine Methode `jageMonster(String monsterArt)`,  
   die diese Exception wirft, wenn das Monster nicht `"Ghul"` oder `"Vampir"` ist.

3. Fange die Exception beim Aufrufer und gib eine Warnmeldung aus.

💥 **Bonus-XP:**  
Baue die Ausnahme als `RuntimeException` und teste, ob du sie auch **ohne `throws`** behandeln kannst.

---

> 🛡️ **+150 XP für magisch saubere Fehlerarchitektur gesammelt!**  
> **Nächstes Ziel:** `enum` – das Unveränderbare deklarieren.

---

# 🧭 **LEVEL 5.4: `enum` – Das Unveränderbare deklarieren**

> *„Ein Hexer hat viele Entscheidungen – aber manche Dinge sind gesetzt.  
> Die fünf Zeichen. Die Monsterarten. Die Tranktypen.  
> Dinge, die sich **nicht ändern**, sind am besten in Stein gemeißelt.“*

In Java benutzt du dafür: **`enum`**

---

## 🧱 **Was ist ein `enum`?**

Ein `enum` (kurz für *enumeration*) ist eine eigene Art von Klasse,  
mit der du eine **feste, unveränderbare Liste von Konstanten** definierst.

Beispiel:

```java
public enum Zeichen {
    IGNI,
    QUEN,
    AARD,
    YRDEN,
    AXII
}
```

> 💡 Du kannst es dir wie eine Liste vorstellen, in der **nur diese Werte erlaubt sind**.  
> Nichts anderes – keine „freien Strings“, keine Tippfehler, keine Überraschungen.

---

## 🧭 **Wann benutzt man `enum`?**

Immer dann, wenn du **aus einer festen Auswahl wählen** willst:

- Monsterarten: `GHUL`, `VAMPIR`, `NEKKER`
- Schwierigkeitsstufen: `LEICHT`, `NORMAL`, `HART`, `ALBTRAUM`
- Wetterarten, Tranktypen, Waffenarten, Statuswerte (AKTIV, INAKTIV)

---

## 🧪 **Enum verwenden:**

```java
Zeichen zeichen = Zeichen.IGNI;

if (zeichen == Zeichen.QUEN) {
    System.out.println("Schutz aktiviert!");
} else {
    System.out.println("Du wirkst: " + zeichen);
}
```

> Enums sind **typsicher** – du kannst sie **nicht versehentlich mit einem String verwechseln**.

---

### 🧙‍♂️ **Enum in Methoden verwenden:**

```java
public void wirkeZeichen(Zeichen zeichen) {
    switch (zeichen) {
        case IGNI -> System.out.println("Flammenstoß!");
        case QUEN -> System.out.println("Schutzschild!");
        case AXII -> System.out.println("Geistige Kontrolle!");
        default -> System.out.println("Unbekanntes Zeichen.");
    }
}
```

---

## 💎 **Enums mit eigenen Feldern und Methoden (fortgeschritten)**

Enums können auch **eigene Eigenschaften und Verhalten** haben:

```java
public enum MonsterArt {
    GHUL("Silber", 80),
    VAMPIR("Feuer", 120);

    private final String schwäche;
    private final int lebensPunkte;

    MonsterArt(String schwäche, int lp) {
        this.schwäche = schwäche;
        this.lebensPunkte = lp;
    }

    public String getSchwaeche() {
        return schwäche;
    }

    public int getLebenspunkte() {
        return lebensPunkte;
    }
}
```

Nutzung:

```java
MonsterArt m = MonsterArt.GHUL;
System.out.println("Schwäche: " + m.getSchwaeche());
```

---

## 🧩 **Vorteile von `enum` gegenüber `String`**

| `String`                               | `enum`                                 |
|----------------------------------------|----------------------------------------|
| Fehleranfällig durch Tippfehler        | Typsicher – Compiler prüft gültige Werte |
| Keine Struktur, keine Logik            | Kann Methoden, Felder, Konstruktoren enthalten |
| Nicht dokumentiert                     | Zeigt dem Entwickler direkt alle möglichen Werte |

---

## 🏆 **Deine XP-Quest:**

1. Erstelle ein `enum Zeichen` mit den fünf bekannten Hexer-Zeichen.

2. Schreibe eine Methode `wirkeZeichen(Zeichen z)`, die eine passende Nachricht für jedes Zeichen ausgibt.

3. Erstelle ein `enum MonsterArt` mit `GHUL` und `VAMPIR`,  
   inkl. Schwäche (als `String`) und Lebenspunkten (als `int`).

💥 **Bonus-XP:**  
Nutze in einer `switch`-Struktur das Enum `MonsterArt`, um je nach Monster eine geeignete Taktik auszugeben.

---

> 🛡️ **+150 XP für konstante Wahrheit und typsichere Ordnung gesammelt!**  
> 🎉 **Glückwunsch! Du hast Level 5: Werde Fehlermeister vollständig abgeschlossen!**

---

**Dieses Thema beinhaltet folgendes Tutorial:**
---

🔹 [**Theorie 01**](/docs/06-entwicklung/05-java/01-tutorial/01-theorie/README.md) </br>
🔹 [**Theorie 02**](/docs/06-entwicklung/05-java/01-tutorial/02-theorie/README.md) </br>
🔹 [**Theorie 03**](/docs/06-entwicklung/05-java/01-tutorial/03-theorie/README.md) </br>
🔹 [**Theorie 04**](/docs/06-entwicklung/05-java/01-tutorial/04-theorie/README.md) </br>
🔹 [**Theorie 05**](/docs/06-entwicklung/05-java/01-tutorial/05-theorie/README.md) </br>
🔹 [**Theorie 06**](/docs/06-entwicklung/05-java/01-tutorial/06-theorie/README.md) </br>
🔹 [**Theorie 07**](/docs/06-entwicklung/05-java/01-tutorial/07-theorie/README.md) </br>
🔹 [**Praxis 01**](/docs/06-entwicklung/05-java/01-tutorial/08-praxis-1/README.md) </br>
🔹 [**Praxis 02**](/docs/06-entwicklung/05-java/01-tutorial/09-praxis-2/README.md) </br>

---

<p align="center">
<a href="/docs/06-entwicklung/05-java/01-tutorial/04-theorie/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/06-theorie/README.md"><strong>Weiter</strong></a>
</p>