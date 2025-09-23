# 🗄️ **LEVEL 3: Baue dein Arsenal auf**

> *„Ein guter Hexer hat nicht nur ein Schwert.  
> Er weiß auch, wo seine Tränke lagern, wie viele Bomben er dabei hat  
> und welche Schwächen welches Monster besitzt.“*  
>  
> In diesem Level lernst du, wie du **Sammlungen von Dingen** verwalten kannst.  
> Und: Du erfährst, was es mit Wrapper-Klassen, Casting, Interfaces und abstrakten Klassen auf sich hat.  
> Stück für Stück wird dein Arsenal mächtiger.

---

## 🏹 **3.1 Collections kennenlernen – `Array`, `List`, `Map`, `Set`**

> *„Ein Hexer verlässt sich nicht auf Zufall. Er führt Buch über seine Tränke, Bomben, Monster und Runen.  
> Und genau das wirst du jetzt auch lernen: dein Arsenal zu verwalten.“*

In Java gibt es eine ganze Sammlung von **Datenstrukturen**, mit denen du **mehrere Elemente speichern** und gezielt verwalten kannst.  
Diese Gruppen nennt man **Collections** – und sie sind ein absolut essenzieller Teil deiner Hexerausrüstung.

---

## 🧭 **Warum Collections?**

Stell dir vor, du willst alle bekannten Monster speichern. Oder eine Liste deiner Bomben. Oder eine Tabelle, die zeigt, wogegen welcher Gegner empfindlich ist.

Einzelne Variablen reichen da nicht aus. Arrays kennst du schon – aber sie sind unflexibel. Wenn du **mehr als eine Handvoll Dinge** speichern willst, brauchst du die **Kraft der Java Collections**.

---

## 🏹 **Die vier Klassiker: Deine ersten Waffenkammern**

### ⚔️ **`Array` – Der starre Waffengurt**  
Das kennst du schon:
```java
String[] bomben = { "Samum", "Grapeshot", "Dancing Star" };
```
Gut, wenn du weißt, wie viele Items du hast – aber **nicht veränderbar in der Größe**.

---

### 🗃️ **`List` – Die flexible Bombentasche**

```java
import java.util.ArrayList;
import java.util.List;

List<String> bomben = new ArrayList<>();
bomben.add("Samum");
bomben.add("Grapeshot");
bomben.add("Dancing Star");
```

- Du kannst Elemente hinzufügen und entfernen.
- Die Reihenfolge bleibt erhalten.
- Zugriff über Index:
```java
System.out.println(bomben.get(1)); // Grapeshot
```

---

### 🗺️ **`Map` – Dein Monsterhandbuch**

Wenn du **Dinge einem Schlüssel zuordnen willst** (z. B. Monster → Schwäche), brauchst du eine Map.

```java
import java.util.HashMap;
import java.util.Map;

Map<String, String> monsterSchwaechen = new HashMap<>();
monsterSchwaechen.put("Vampir", "Feuer");
monsterSchwaechen.put("Ghul", "Silberschwert");

System.out.println(monsterSchwaechen.get("Ghul"));  // Silberschwert
```

---

### 🧿 **`Set` – Die Runensteinsammlung**

Sets sind **ungeordnete Sammlungen ohne doppelte Einträge** – praktisch für Listen, bei denen jedes Element nur einmal vorkommen darf:

```java
import java.util.HashSet;
import java.util.Set;

Set<String> zeichen = new HashSet<>();
zeichen.add("Igni");
zeichen.add("Yrden");
zeichen.add("Igni"); // wird ignoriert

System.out.println(zeichen);  // Ausgabe ohne Duplikate
```

---

## 🧩 **Welche Struktur für welchen Zweck?**

| Struktur   | Gut geeignet für …                                  |
|------------|------------------------------------------------------|
| `Array`    | feste Anzahl an Dingen, hohe Geschwindigkeit         |
| `List`     | dynamische, geordnete Listen                         |
| `Set`      | Mengen ohne Duplikate                                |
| `Map`      | Schlüssel-Wert-Paare (wie Lexika, Tabellen, Datenbanken) |

---

## 🧙‍♂️ **Wichtig zu wissen: Es gibt noch mehr!**

Das, was du hier lernst, sind die **grundlegenden Waffen** aus dem Java-Arsenal. Aber Java bietet noch viele weitere Collection-Typen:

- `LinkedList`: Listen mit besserer Einfüge-/Lösch-Performance
- `TreeSet`, `TreeMap`: sortierte Versionen von Set und Map
- `Queue`, `Deque`: Warteschlangen, Stapel
- `PriorityQueue`, `EnumSet`, `WeakHashMap`, u. v. m.

> Diese mächtigeren Werkzeuge lernst du in späteren Levels kennen – sobald du bereit bist, sie zu führen. 🧝‍♀️

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine `List` mit deinen Lieblingsbomben.  
   - Füge mindestens drei Bomben hinzu.  
   - Gib alle Bomben per Schleife aus.

2. Baue eine `Map`, die Monsterarten und ihre Schwächen enthält.  
   - Lass dir die Schwäche für ein bestimmtes Monster anzeigen.

💥 **Bonus-XP:**  
Baue ein `Set`, das die bekannten Hexer-Zeichen speichert (`Igni`, `Quen`, `Yrden`, `Axii`, `Aard`).  
Füge ein Zeichen doppelt hinzu – und beobachte, was passiert.

---

> 🛡️ **+100 XP für Sammlungsmagie und Inventarkontrolle gesammelt!**  
> **Nächstes Ziel:** Wrapper-Klassen – verwandle primitive Magie in Objektform.

---

# 🧙‍♂️ **LEVEL 3.2: Wrapper-Klassen – Primitive Magie in Objektform**

> *„Ein einzelner Tropfen Mutagen ist stark.  
> Doch in einer Phiole, mit Gravur und Verschluss, ist er handhabbar, haltbar – und kombinierbar.“*  
>  
> Primitive Datentypen wie `int`, `boolean` oder `char` sind roh, schnell und direkt.  
> Aber sie sind keine Objekte – und in vielen Situationen brauchst du genau das.

---

## 📦 **Was ist eine Wrapper-Klasse?**

Ein **Wrapper** „verpackt“ einen primitiven Datentyp in ein **vollwertiges Objekt**.

| Primitiv | Wrapper-Klasse |
|----------|----------------|
| `int`    | `Integer`      |
| `double` | `Double`       |
| `boolean`| `Boolean`      |
| `char`   | `Character`    |
| `byte`   | `Byte`         |
| `short`  | `Short`        |
| `long`   | `Long`         |
| `float`  | `Float`        |

> 💡 Diese Klassen befinden sich alle im Paket `java.lang`, also direkt verfügbar – du musst nichts extra importieren.

---

## 🧭 **Warum überhaupt Wrapper-Klassen verwenden?**

Hier ein paar typische Szenarien:

1. **Sammlungen (Collections)** können **nur Objekte speichern**, keine primitiven Werte.
   ```java
   List<Integer> monsterStufen = new ArrayList<>();
   monsterStufen.add(3);  // int → Integer (automatisch!)
   ```

2. Du willst einen primitiven Wert **als Objekt übergeben**, z. B. in Methoden oder generischen Klassen.

3. Du brauchst zusätzliche **Hilfsmethoden**, etwa:
   ```java
   Integer.parseInt("42");   // String → int
   Boolean.parseBoolean("true");
   ```

4. Du willst **null** als „nicht gesetzt“ nutzen.  
   Das geht mit Objekten, aber **nicht mit primitiven Datentypen** (z. B. `int` kann nicht `null` sein, `Integer` schon).

---

## ⚙️ **Autoboxing und Unboxing – Magie im Hintergrund**

Java ist so nett und erledigt die Umwandlung oft automatisch:

### 🔄 Autoboxing:
```java
int zahl = 5;
Integer verpackt = zahl; // automatisch: int → Integer
```

### 🔃 Unboxing:
```java
Integer level = 7;
int echt = level; // automatisch: Integer → int
```

> 💡 Das nennt man **Autoboxing** und **Unboxing** – Java konvertiert für dich zwischen den Welten.

Aber sei vorsichtig:  
```java
Integer x = null;
int y = x; // ❌ Fehler! NullPointerException!
```

---

## 📚 **Ein praktisches Beispiel: Liste mit Monster-Stufen**

```java
List<Integer> monsterStufen = new ArrayList<>();
monsterStufen.add(2);
monsterStufen.add(5);
monsterStufen.add(9);

for (Integer stufe : monsterStufen) {
    System.out.println("Monster-Stufe: " + stufe);
}
```

Hier könnten wir kein `List<int>` verwenden – `int` ist **kein Objekt**.  
Deshalb brauchen wir `Integer`.

---

## 🧪 **Zusätzliche Helfer in Wrapper-Klassen**

```java
int x = Integer.parseInt("123");
double y = Double.parseDouble("3.14");
boolean aktiv = Boolean.parseBoolean("true");
```

> Diese Methoden helfen dir, Texte aus z. B. Benutzereingaben umzuwandeln.

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine `List<Integer>`, die drei beliebige Level von Monstern enthält.  
   Gib alle Level mit einer Schleife aus.

2. Wandle einen `String` wie `"42"` mithilfe von `Integer.parseInt()` in eine Zahl um und gib sie aus.

💥 **Bonus-XP:**  
Teste, was passiert, wenn du `"abc"` in `Integer.parseInt("abc")` steckst.  
(Fang den Fehler mit `try-catch` ab, falls du schon mit Ausnahmen arbeitest – sonst merken wir uns das für später 😉)

---

> 🛡️ **+100 XP für Magie der Umwandlung gesammelt!**  
> **Nächstes Ziel:** Casten – verwandle Monster und Magie gezielt in andere Formen.

---

# 📜 **LEVEL 3.4: `interface` – Verträge definieren, nach denen du codest**

> *„Jeder Hexer kann Zeichen wirken. Wie genau – das ist seine Sache.  
> Aber wenn du ein Hexer bist, dann weiß man: Zeichen kannst du.“*  
>  
> Genauso ist es mit Interfaces in Java:  
> Sie schreiben **vor, was eine Klasse tun muss**,  
> aber **nicht wie sie es tut**.

---

## ⚖️ **Was ist ein Interface?**

Ein `interface` ist ein **Vertrag** in Java.  
Er sagt: „Wenn du diesen Vertrag implementierst, musst du folgende Methoden haben.“

Ein Interface ist **keine Klasse** – es enthält **nur Methodensignaturen**, **keinen Code** (zumindest nicht im klassischen Sinne – später lernst du auch `default`-Methoden kennen).

---

### 🧭 Beispiel: Ein Interface für alles, was Zaubern kann

```java
public interface Zauberfaehig {
    void zaubere();
}
```

Das bedeutet: **Jede Klasse, die `Zauberfaehig` implementiert**, muss eine Methode `zaubere()` haben.

---

### 🐺 Monster mit Zauberfähigkeiten

```java
public class Vampir extends Monster implements Zauberfaehig {
    @Override
    public void zaubere() {
        System.out.println("Der Vampir wirkt einen Blutnebel-Zauber!");
    }
}
```

> 💡 Das Schlüsselwort ist **`implements`**, nicht `extends`.  
> Denn du **implementierst einen Vertrag**, du **vererbst** ihn nicht.

---

### 🎭 Mehrere Interfaces? Kein Problem.

Anders als bei Klassen kannst du **mehrere Interfaces gleichzeitig implementieren**:

```java
public interface Unsichtbar {
    void verstecken();
}

public class Nekker extends Monster implements Zauberfaehig, Unsichtbar {
    public void zaubere() {
        System.out.println("Der Nekker wirft eine Illusionskugel.");
    }

    public void verstecken() {
        System.out.println("Der Nekker verschmilzt mit dem Schatten.");
    }
}
```

> 💡 In Java darf eine Klasse **nur eine andere Klasse erweitern (`extends`)**,  
> aber sie darf **beliebig viele Interfaces implementieren.**

---

## 🧩 **Warum Interfaces?**

- Sie erlauben es dir, **auf Verhalten zu programmieren, nicht auf konkrete Klassen.**
- Sie trennen **„Was soll getan werden?“** (Interface) von **„Wie wird es gemacht?“** (Klasse).
- Sie helfen beim **Testen, Austauschen und Erweitern**.

Beispiel:
```java
public void zauberWirken(Zauberfaehig wesen) {
    wesen.zaubere();  // egal ob Vampir, Nekker oder sonstwas
}
```

> Diese Methode funktioniert mit **jedem Wesen**, das `Zauberfaehig` ist – unabhängig von der konkreten Klasse.

---

## 🏆 **Deine XP-Quest:**

1. Erstelle ein Interface `Zauberfaehig` mit einer Methode `zaubere()`.  
2. Lass zwei Monsterklassen (`Vampir`, `Nekker`) dieses Interface implementieren – mit jeweils eigener Zauber-Art.  
3. Baue eine Methode `wirkeZauber(Zauberfaehig ziel)`, die `ziel.zaubere()` aufruft.

💥 **Bonus-XP:**  
Erstelle ein zweites Interface `Heilbar` mit der Methode `heile()`.  
Lass `Nekker` sowohl `Zauberfaehig` als auch `Heilbar` implementieren.

---

> 🛡️ **+150 XP für Interface-Magie gesammelt!**  
> **Nächstes Ziel:** Abstrakte Klassen – erschaffe Strukturen mit Freiraum.

---

# 🏰 **LEVEL 3.5: `abstract class` – Strukturen erschaffen**

> *„Alle Hexer haben Zeichen gelernt. Doch jeder entscheidet selbst,  
> wie er sie im Kampf einsetzt.“*  
>  
> **Abstrakte Klassen** sind wie die Grundausbildung für Monster oder Hexer:  
> Sie geben den **Rahmen** vor, aber die konkrete Ausführung bleibt den Kindern überlassen.

---

## 🧭 **Was ist eine abstrakte Klasse?**

Eine **abstrakte Klasse** ist ein **Bauplan**, der teilweise schon Code enthält, aber auch Stellen offenlässt, an denen die Kindklassen selbst entscheiden müssen.

- Sie kann **normale Methoden** enthalten (mit Code).
- Sie kann **abstrakte Methoden** enthalten (ohne Code → nur die Signatur).
- Sie kann **Felder** besitzen, genau wie normale Klassen.

Das Schlüsselwort dafür: `abstract`.

---

### 🧪 **Beispiel: Die abstrakte Klasse `Monster`**

```java
public abstract class Monster {
    private String name;
    private int lebensPunkte;

    public Monster(String name, int lebensPunkte) {
        this.name = name;
        this.lebensPunkte = lebensPunkte;
    }

    public void anzeigen() {
        System.out.println(name + " | Lebenspunkte: " + lebensPunkte);
    }

    public abstract void angreifen();  // Kein Code hier – Pflicht für die Kindklassen!
}
```

> 💡 Hier gibt es:
> - **eine konkrete Methode** (`anzeigen()`)  
> - **eine abstrakte Methode** (`angreifen()`, ohne Code)

---

### 🐺 **Kindklassen müssen die abstrakten Methoden umsetzen:**

```java
public class Vampir extends Monster {
    public Vampir() {
        super("Vampir", 120);
    }

    @Override
    public void angreifen() {
        System.out.println("Der Vampir setzt seinen Blutbiss ein!");
    }
}
```

---

## 🗝️ **Warum abstrakte Klassen nutzen?**

- Du gibst **eine gemeinsame Basis vor** (z. B. Name, Lebenspunkte).
- Du kannst **Code wiederverwenden** (z. B. `anzeigen()`).
- Du zwingst die Kinder dazu, **bestimmte Methoden selbst zu definieren**.

> 🧙‍♂️ **Abstrakte Klassen sind ideal, wenn es Gemeinsamkeiten gibt, aber auch Pflichtunterschiede.**

---

## 💎 **Das Diamant-Problem – und warum Java es nicht hat**

> *„Man sagt, zwei Ahnenstränge könnten sich kreuzen – und dann weiß das Kind nicht mehr, welchen Weg es folgen soll.“*  
>  
> Das ist das **Diamant-Problem**, das in manchen Sprachen (wie C++) bei **Mehrfachvererbung von Klassen** entsteht:

### 🌑 Beispiel (theoretisch, in Sprachen mit Mehrfachvererbung):

```
          Lebewesen
         /          \
     Monster     MagischesWesen
         \          /
			Vampir
```

- **Problem:** Beide Eltern (`Monster` und `MagischesWesen`) haben z. B. eine Methode `angreifen()`.  
- **Was passiert, wenn `Vampir` diese Methode erbt?** Von welcher Klasse?

In Java gibt es das **nicht**, weil:
- Java **erlaubt nur einfache Vererbung für Klassen** (`extends` nur einmal).  
- Für gemeinsame Verträge gibt es stattdessen **Interfaces**.

> 🛡️ Das schützt dich als Hexer vor diesem Chaos. Du kannst **nur eine abstrakte Klasse erweitern** – aber beliebig viele Interfaces implementieren.

---

## 🧩 **Wann benutze ich `abstract class`, wann `interface`?**

|           | `abstract class`                                | `interface`                                 |
|-----------|--------------------------------------------------|----------------------------------------------|
| Vererbung | Nur eine Klasse kann erweitert werden (`extends`) | Mehrere Interfaces können implementiert werden |
| Code      | Kann Code enthalten                              | Enthält meist nur Methodensignaturen        |
| Felder    | Kann Felder und Konstruktoren haben              | Keine Konstruktoren, nur Konstanten (`public static final`) |
| Ziel      | Gemeinsame Basis mit Pflicht zur eigenen Umsetzung | Verhalten vorschreiben, aber ohne Implementierung |

---

## 🏆 **Deine XP-Quest:**

1. Baue eine **abstrakte Klasse `Monster`**:
   - mit den Feldern `name` und `lebensPunkte`,
   - einer konkreten Methode `anzeigen()`,
   - einer abstrakten Methode `angreifen()`.

2. Erstelle zwei Kindklassen (`Ghul`, `Vampir`), die `angreifen()` jeweils auf ihre Weise umsetzen.

💥 **Bonus-XP:**  
Baue ein Interface `Zauberfaehig` und lasse `Vampir` zusätzlich das Interface implementieren, um einen Zauber zu wirken.

---

> 🛡️ **+150 XP für stabile Strukturen gesammelt!**  
> **Nächstes Ziel:** `record`: Daten mit Stil schreiben.

---

# 📜 **LEVEL 3.6: `record` – Daten mit Stil schreiben**

> *„Manchmal brauchst du kein ganzes Arsenal.  
> Ein sauber beschriftetes Fläschchen reicht.“*  
>  
> In Java gibt es für **einfache Datenobjekte** eine schlanke, schöne Lösung:  
> Das Schlüsselwort `record`.  
>  
> Damit schreibst du **klare Datenstrukturen** mit minimalem Aufwand –  
> und bekommst gleich Methoden wie `toString()`, `equals()` und `hashCode()` geschenkt.

---

## 🧭 **Was ist ein `record`?**

Ein `record` ist eine **spezielle Art von Klasse**, die dafür gedacht ist, **Daten zu speichern** – nicht mehr, nicht weniger.

Beispiel:

```java
public record Trank(String name, int wirkstaerke) { }
```

Was passiert hier?

- Du sagst:  
  „Ein `Trank` besteht aus einem `name` und einer `wirkstaerke`.“
- Java baut automatisch:
  - einen Constructor,  
  - `get`-Methoden (`name()`, `wirkstaerke()`),  
  - `toString()`,  
  - `equals()` und  
  - `hashCode()`.

Und das alles ohne den ganzen üblichen „Setter-Getter-Boilerplate“.

---

## 🧪 **Beispiel in Aktion:**

```java
Trank heiltrank = new Trank("Heiltrank", 50);

System.out.println(heiltrank);  
```

> Ausgabe:
```
Trank[name=Heiltrank, wirkstaerke=50]
```

---

### 🛡️ **Was du bekommst – ohne es schreiben zu müssen:**

```java
heiltrank.name();          // → "Heiltrank"
heiltrank.wirkstaerke();   // → 50

System.out.println(heiltrank);  // → automatisch gutes toString()
```

> **Vergleich:**  
> Zwei Tränke mit denselben Werten sind **automatisch gleich**:

```java
Trank t1 = new Trank("Heiltrank", 50);
Trank t2 = new Trank("Heiltrank", 50);

System.out.println(t1.equals(t2));  // true!
```

---

## 🌿 **Warum `record` und nicht `class`?**

| Wenn du …                                         | Dann nimm …     |
|---------------------------------------------------|-----------------|
| Verhalten (Logik, Methoden) brauchst              | `class`         |
| Vererbung, abstrakte Methoden, Verhaltensverträge brauchst | `abstract class` oder `interface` |
| **Nur Daten** ohne viel Logik speichern willst    | `record`        |

> **`record` = die perfekte Wahl für reine Datenobjekte**, wie:
> - Tränke  
> - Positionsdaten (z. B. `Koordinate(x, y)`)  
> - Einträge in einer Highscore-Liste  
> - Monster-Statistiken

---

## ⚠️ **Was du mit `record` nicht kannst:**

- Kein `extends` anderer Klassen  
- Kein eigenes `Setter` (alle Felder sind **final**)  
- Aber: Du kannst **Interfaces implementieren**, wenn du magst.

---

### 🧩 **Custom Constructor möglich:**

Wenn du eigene Regeln für die Erzeugung brauchst, geht auch das:

```java
public record Trank(String name, int wirkstaerke) {
    public Trank {
        if (wirkstaerke < 0) {
            throw new IllegalArgumentException("Wirkstaerke darf nicht negativ sein!");
        }
    }
}
```

> Das ist ein sogenannter **Compact Constructor**:  
> Er prüft die übergebenen Werte, bevor das Objekt gebaut wird.

---

## 🏆 **Deine XP-Quest:**

1. Baue ein `record` `MonsterStat`, das speichert:
   - den Namen des Monsters,  
   - seine Stufe (`int`),  
   - und die Anzahl der besiegten Gegner (`int`).

2. Erstelle zwei `MonsterStat`-Objekte mit denselben Werten –  
   prüfe mit `.equals()`, ob sie gleich sind.

💥 **Bonus-XP:**  
Baue einen Compact Constructor, der verbietet, dass ein Monster eine negative Stufe haben darf.

---

> 🛡️ **+100 XP für elegante Datenbehälter gesammelt!**  
> **Nächstes Ziel:** `static` und `final` – Macht und Konstanz verstehen und einsetzen.

---

# 🗿 **LEVEL 3.7: `static` und `final` – Macht und Konstanz verstehen und einsetzen**

> *„Ein Hexer hat seine festen Grundsätze.  
> Und manche Dinge gelten für alle Monster – nicht nur für eines.“*  
>  
> Mit **`static`** und **`final`** entscheidest du:  
> - Was gehört **allen** und nicht nur einem Objekt?  
> - Was ist **unveränderlich** – ein ehernes Gesetz deines Codes?

---

## ⚡ **`static`: Die Macht aller – gehört zur Klasse, nicht zum Objekt**

Normalerweise gehören Felder und Methoden zu einem **bestimmten Objekt**.

Aber manchmal willst du etwas, das für **alle Instanzen gleich** ist.  
Beispiel: **die maximale Lebenspunkte für alle Ghule.**

```java
public class Ghul extends Monster {
    public static final int MAX_LEBENSPUNKTE = 100;

    public Ghul() {
        super("Ghul", MAX_LEBENSPUNKTE);
    }
}
```

> 💡 `static` bedeutet:  
> Dieses Feld gehört **der Klasse selbst**, nicht einem bestimmten Ghul.

Du greifst zu über:
```java
System.out.println(Ghul.MAX_LEBENSPUNKTE);
```

---

### 🛡️ **`static` für Methoden – Helfer ohne Objekt**

Willst du eine **Hilfsmethode**, die kein spezielles Objekt braucht? → `static`!

```java
public class MatheMagie {
    public static int verdopple(int zahl) {
        return zahl * 2;
    }
}
```

Nutzung:
```java
int ergebnis = MatheMagie.verdopple(5);  // 10
```

> Kein `new MatheMagie()` nötig – weil die Methode zur **Klasse selbst gehört**.

---

## 🗿 **`final`: Was einmal gesetzt ist, bleibt**

Wenn etwas **`final`** ist, kannst du es **nur einmal setzen** – danach ist es **unveränderlich**.

### 🪵 Beispiel: Ein unveränderlicher Trankname

```java
public class Trank {
    private final String name;

    public Trank(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}
```

> Das Feld `name` kann **nicht mehr geändert** werden, nachdem es im Constructor gesetzt wurde.

---

### 🧩 **`final` für Variablen:**

```java
final int maxTraenke = 5;
maxTraenke = 7;  // ❌ Compiler-Fehler! Nicht erlaubt!
```

> **`final` = „Nur einmal befüllbar.“**

---

## 🧙‍♂️ **Kombination: `static final` – Die unveränderliche Wahrheit für alle**

Viele Konstanten in Java werden so definiert:

```java
public static final int MAX_MONSTER_LEVEL = 10;
```

> Bedeutet:
> - **`static`:** Für die ganze Klasse gültig.  
> - **`final`:** Niemals veränderbar.

> 💡 Konstante Namen schreibt man in Java traditionell in **GROẞBUCHSTABEN**.

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine Klasse `MonsterWissen` mit:
   - einem `static final String HEXER_CODE = "Monster töten, Menschen schützen"`.
   - einer `static` Methode `zeigeHexerCode()`, die diesen Satz ausgibt.

2. Baue eine Monsterklasse mit einer `static final int MAX_LEBENSPUNKTE`,  
   die im Constructor als Lebenspunkte gesetzt wird.

💥 **Bonus-XP:**  
Erstelle eine Hilfsklasse `TrankRezept`, die eine `static` Methode `berechneWirkstaerke(int grundstaerke, int bonus)` hat.

---

> 🛡️ **+100 XP für kollektive Macht und Unveränderlichkeit gesammelt!**  
> 🎉 **Damit ist Level 3 abgeschlossen!**  
>  
> Bereit für **Level 4: Schütze deinen Code**?

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
<a href="/docs/06-entwicklung/05-java/01-tutorial/02-theorie/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/04-theorie/README.md"><strong>Weiter</strong></a>
</p>