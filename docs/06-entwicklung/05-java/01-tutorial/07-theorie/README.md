# 🌌 **LEVEL 7: Meistere die Tiefe**

> *„Ein wahrer Hexer meistert nicht nur das Sichtbare –  
> sondern auch das, was zwischen den Zeilen liegt.“*  
>  
> Jetzt lernst du:
> - wie du **mit `Optional` der `null`-Falle entkommst**  
> - wie du mit der **Stream-API elegant und mächtig** Daten verarbeitest  
> - wie du mit **Method References** deinen Code noch lesbarer machst  
> - wie du Ressourcen **sicher und automatisch verwaltest**  
> - wie du **erste Schritte in die Parallelität (Concurrency)** wagst

---

## 🔍 **7.1 Optional<T> – Null vermeiden wie ein Profi**

> *„Null ist wie ein Hinterhalt: still, tödlich – und meist unsichtbar.“*

In Java lauert überall eine Gefahr: `NullPointerException`.  
Doch mit **`Optional<T>`** bekommst du ein Werkzeug, um **absichtlich und sicher mit leeren Werten umzugehen**.

---

## 🧱 **Was ist `Optional`?**

`Optional<T>` ist eine **Hülle um einen Wert** vom Typ `T` – oder auch kein Wert.  
Statt `null`, bekommst du **eine explizite Möglichkeit**, das Fehlen eines Werts zu behandeln.

Beispiel:
```java
Optional<String> trank = Optional.of("Heiltrank");
Optional<String> leer = Optional.empty();
```

---

## 🛠️ **Typische Nutzung:**

```java
Optional<String> monsterName = findeMonster("Wyvern");

if (monsterName.isPresent()) {
    System.out.println("Gefunden: " + monsterName.get());
} else {
    System.out.println("Kein Monster gefunden.");
}
```

> 💡 Aber: **`get()` ist gefährlich** – wir wollen elegantere Wege!

---

### 🧙‍♂️ Bessere Varianten:

#### `ifPresent(...)`
```java
monsterName.ifPresent(name -> System.out.println("Monster: " + name));
```

#### `orElse(...)`
```java
String name = monsterName.orElse("Unbekanntes Wesen");
```

#### `orElseThrow(...)`
```java
String name = monsterName.orElseThrow(() -> new RuntimeException("Monster nicht gefunden"));
```

---

### 🧪 Beispielmethode:

```java
public Optional<String> findeMonster(String name) {
    List<String> monster = List.of("Ghul", "Vampir", "Nekker");
    return monster.contains(name) ? Optional.of(name) : Optional.empty();
}
```

---

## 🏆 **Deine XP-Quest:**

1. Schreibe eine Methode `Optional<String> findeTrank(String name)` mit einer internen Trankliste.  
   Wenn gefunden: `Optional.of(name)`, sonst `Optional.empty()`.

2. Verwende `orElse()` und `ifPresent()`, um das Ergebnis sauber auszugeben.

💥 **Bonus-XP:**  
Verwende `orElseThrow(...)` und gib eine sprechende Fehlermeldung aus.

---

> 🛡️ **+100 XP für `null`-Freiheit und saubere Kontrolle gesammelt!**  
> **Nächstes Ziel:** Immutable Collections – schreibgeschützte Sammlungen mit Stil.

---

# 🧊 **LEVEL 7.2: Immutable Collections – Daten mit Siegel**

> *„Ein Hexer schreibt seine Einträge in Stein, wenn sie endgültig sind.  
> Wer sie ändern will, muss erst das Siegel brechen – oder besser: es gar nicht erst versuchen.“*

In Java kannst du mit `List.of()`, `Set.of()`, `Map.of()` schnell **unveränderliche Sammlungen** erstellen –  
das ist besonders nützlich, wenn du **feste Werte** übergeben willst, ohne Gefahr, dass jemand sie verändert.

---

## 🧭 **Was ist eine immutable Collection?**

Eine **immutable** Collection ist eine **unveränderbare Sammlung** – du kannst sie lesen, aber **nicht mehr ändern**:

- Keine `add()`  
- Kein `remove()`  
- Kein `clear()`

💥 Versuchst du es doch – bekommst du eine **`UnsupportedOperationException`**.

---

## 🛠️ **Beispiele:**

### 📋 Unveränderliche Liste:

```java
List<String> zauber = List.of("Igni", "Quen", "Axii");
```

### 🔐 Unveränderliches Set:

```java
Set<String> zeichen = Set.of("Igni", "Quen", "Yrden");
```

### 🗺️ Unveränderliche Map:

```java
Map<String, String> monsterSchwaechen = Map.of(
    "Vampir", "Feuer",
    "Ghul", "Silberschwert"
);
```

---

## 🧙‍♂️ Vorteile:

| Vorteil                          | Erklärung                                |
|----------------------------------|------------------------------------------|
| Sicherheit                      | Niemand kann die Sammlung versehentlich ändern |
| Lesbarkeit                      | Signalisiert: „Diese Daten sind fix.“    |
| Gleichzeitiger Zugriff (Thread-Sicherheit) | Keine Sorge über parallele Änderungen    |
| Performance                     | Java kann optimierte Speicherstrukturen verwenden |

---

## ⚠️ Einschränkungen von `of()`-Methoden:

- **Kein `null` erlaubt!**  
  ```java
  List.of(null); // ❌ wirft NullPointerException
  ```

- `Map.of(...)` erlaubt nur bis zu 10 Paare → für mehr:
  ```java
  Map.ofEntries(
      Map.entry("Ghul", "Silber"),
      Map.entry("Vampir", "Feuer"),
      Map.entry("Nekker", "Aard")
  );
  ```

---

## 🧩 Wann solltest du `of()` verwenden?

- Wenn du **Konstanten übergeben willst**
- Wenn du in **Tests oder Beispielen** feste Daten brauchst
- Wenn du **öffentliches API-Verhalten absichern** willst

> 💡 **`List.of()`** ist nicht dasselbe wie `Arrays.asList()`  
> (Letzteres ist **modifizierbar**, aber fix in der Größe)

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine `List<String>` mit drei festgelegten Hexer-Zeichen (unveränderlich).

2. Versuche, nach dem Erstellen ein weiteres Element hinzuzufügen.  
   Was passiert?

💥 **Bonus-XP:**  
Erstelle eine `Map<String, String>` mit drei Monsterarten und Schwächen.  
Nutze `Map.ofEntries(...)` und gib alle Einträge sauber aus.

---

> 🛡️ **+100 XP für Datensiegel und Stabilität gesammelt!**  
> **Nächstes Ziel:** Stream API – filter, map, collect, reduce, fluent coding

---

# 🌊 **LEVEL 7.3: Stream API – filter, map, collect, reduce, fluent coding**

> *„Ein Hexer läuft nicht jeder Liste hinterher – er lässt sie an sich vorbeiziehen  
> und greift nur nach dem, was er braucht.“*  
>  
> Die Stream API erlaubt dir, **Sammlungen funktional zu verarbeiten**:  
> kurz, klar, elegant – ohne Schleifen und manuelles Herumgefrickel.

---

## 🧭 **Was ist ein Stream?**

Ein **Stream** ist eine **Verarbeitungskette von Daten**.  
Du nimmst z. B. eine `List<Monster>`, wandelst sie in einen Stream um – und sagst dann:

- Filtere nach starken Monstern  
- Nimm nur die Namen  
- Sortiere alphabetisch  
- Gib das Ergebnis als Liste zurück

### 🔧 Syntax:
```java
liste.stream()
    .filter(...)
    .map(...)
    .sorted()
    .collect(...)
```

---

## 🛠️ **Grundoperationen mit Beispielen**

### 🔍 `filter(...)` – Nur bestimmte Elemente behalten

```java
List<Monster> starke = monsterListe.stream()
    .filter(m -> m.getLebenspunkte() > 100)
    .collect(Collectors.toList());
```

---

### 🧙‍♂️ `map(...)` – Elemente umwandeln

```java
List<String> namen = monsterListe.stream()
    .map(Monster::getName)
    .collect(Collectors.toList());
```

---

### 🧾 `sorted()` – Sortieren

```java
List<Monster> sortiert = monsterListe.stream()
    .sorted(Comparator.comparing(Monster::getName))
    .collect(Collectors.toList());
```

---

### 💰 `reduce()` – Alles zu einem Wert zusammenfassen

```java
int gesamtLP = monsterListe.stream()
    .map(Monster::getLebenspunkte)
    .reduce(0, Integer::sum);
```

> 💡 `reduce()` ist wie ein mächtiger alchemistischer Destillationsprozess.

---

## 📦 **`collect(...)` – Das Ergebnis einsammeln**

Zum Abschluss eines Streams sammelst du das Ergebnis ein:

| Ziel                 | Methode                                 |
|----------------------|------------------------------------------|
| Liste                | `Collectors.toList()`                   |
| Set                  | `Collectors.toSet()`                    |
| Map                  | `Collectors.toMap(keyMapper, valueMapper)` |
| String zusammenfügen| `Collectors.joining(", ")`              |

---

## 🧩 Kombinierte Anwendung:

```java
String beschreibung = monsterListe.stream()
    .filter(m -> m.getLebenspunkte() > 90)
    .map(Monster::getName)
    .sorted()
    .collect(Collectors.joining(", "));
```

Ergebnis:
```
"Nekker, Vampir, Wyvern"
```

---

## 🧙‍♂️ Vorteile der Stream API

| Vorteil                         | Warum es dich interessiert |
|----------------------------------|-----------------------------|
| Kein manuelles Schleifen mehr    | Weniger Code, mehr Klarheit |
| Funktionaler Stil                | Kompakt und lesbar          |
| Leicht kombinierbar              | Bausteine statt Blockcode   |
| Optional parallelisierbar        | `.parallelStream()`         |

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine `List<Monster>` mit verschiedenen Monstern und Lebenspunkten.

2. Nutze einen Stream, um:
   - Alle Monster mit > 90 LP zu finden
   - Nur deren Namen als `List<String>` zu sammeln
   - Alphabetisch zu sortieren

💥 **Bonus-XP:**  
Berechne mit `reduce()` die Summe aller Lebenspunkte.

---

> 🛡️ **+150 XP für flüssige Datenverarbeitung gesammelt!**  
> **Nächstes Ziel:** Method References – das Sahnehäubchen auf Lambdas.

---

# 🪄 **LEVEL 7.4: Method References – das Sahnehäubchen auf Lambdas**

> *„Ein Hexer spricht nicht immer den ganzen Zauber –  
> manchmal genügt ein Fingerzeig, und die Magie fließt von selbst.“*  
>  
> Method References sind **verknappte Lambda Expressions**,  
> die einfach sagen: „Nimm genau diese Methode.“

---

## 🧭 **Was ist eine Method Reference?**

Statt:
```java
monsterListe.stream()
    .map(monster -> monster.getName())
```

…kannst du schreiben:
```java
monsterListe.stream()
    .map(Monster::getName)
```

> 💡 Beide tun das Gleiche – aber Method References sind **lesbarer** und **präziser**,  
> wenn du **eine Methode 1:1 weiterreichst**, ohne sie zu verändern.

---

## 🔧 **Vier Typen von Method References**

| Art                             | Syntax                       | Beispiel                         |
|----------------------------------|-------------------------------|----------------------------------|
| 1. **Instanzmethode eines Objekts** | `objekt::methode`              | `System.out::println`            |
| 2. **Instanzmethode einer beliebigen Instanz** | `Typ::methode`                 | `String::toUpperCase`            |
| 3. **Statische Methode**          | `Klasse::statischeMethode`    | `Math::random`                   |
| 4. **Konstruktor-Referenz**       | `Klasse::new`                 | `Monster::new`                   |

---

## 🧪 **Beispiele in Aktion**

### 🧙‍♂️ Statt Lambda:

```java
List<String> namen = monsterListe.stream()
    .map(monster -> monster.getName())
    .collect(Collectors.toList());
```

### 🪄 Method Reference:

```java
List<String> namen = monsterListe.stream()
    .map(Monster::getName)
    .collect(Collectors.toList());
```

---

### 🧪 Statische Methode:

```java
List<String> namen = List.of("geralt", "yennefer");
namen.stream()
    .map(String::toUpperCase)
    .forEach(System.out::println);
```

---

### 🪄 Konstruktorreferenz:

```java
List<String> namen = List.of("Ghul", "Vampir");

List<Monster> monster = namen.stream()
    .map(Monster::new)  // erwartet: Monster(String name)
    .collect(Collectors.toList());
```

> 💡 Du brauchst dafür einen passenden Konstruktor in `Monster`.

---

## ⚔️ **Vorteile von Method References**

| Vorteil             | Beschreibung                                   |
|---------------------|-----------------------------------------------|
| Kürzer              | Spart unnötige Wiederholung                   |
| Lesbarer            | Man erkennt sofort, **was** passiert          |
| Besser kombinierbar | Besonders stark in `stream()`-Ketten          |

---

## 🏆 **Deine XP-Quest:**

1. Baue eine `List<Monster>` und nutze eine Method Reference, um nur deren Namen auszugeben (`Monster::getName`).

2. Erstelle eine `List<String>` mit Monster-Namen und verwandle sie per Konstruktor-Referenz in `List<Monster>`.

💥 **Bonus-XP:**  
Benutze `System.out::println` als direkte Action in `.forEach(...)`.

---

> 🛡️ **+100 XP für meisterhafte Eleganz gesammelt!**  
> **Nächstes Ziel:** `try-with-resources` – Ressourcen sicher und sauber verwalten.

---

# 🧳 **LEVEL 7.5: `try-with-resources` – Ressourcen sicher und sauber verwalten**

> *„Ein Hexer schließt jedes Portal, das er öffnet.  
> Wer das vergisst, zieht Chaos nach sich.“*

In Java bedeutet das:  
**Dateien, Streams, Reader, Writer, Datenbankverbindungen** –  
sie alle müssen **geschlossen werden**, sobald du sie nicht mehr brauchst.

---

## 🧭 **Was ist `try-with-resources`?**

Ein spezieller `try`-Block, der **automatisch Ressourcen schließt**,  
sobald der Block verlassen wird – **auch bei Fehlern**.

---

## 🛠️ **Beispiel: Ohne try-with-resources (Fehleranfällig)**

```java
BufferedReader reader = new BufferedReader(new FileReader("zauber.txt"));
try {
    String line = reader.readLine();
    System.out.println(line);
} finally {
    reader.close();  // musst du selbst dran denken!
}
```

---

## ✨ **Mit try-with-resources:**

```java
try (BufferedReader reader = new BufferedReader(new FileReader("zauber.txt"))) {
    String line = reader.readLine();
    System.out.println(line);
} catch (IOException e) {
    System.out.println("Fehler beim Lesen: " + e.getMessage());
}
```

> 💡 **`reader` wird automatisch geschlossen**, auch wenn ein Fehler auftritt.

---

## 📦 **Welche Klassen kannst du verwenden?**

Alle Klassen, die **`AutoCloseable`** implementieren – also:
- `BufferedReader`
- `PrintWriter`
- `Scanner`
- `InputStream`, `OutputStream`
- `Connection`, `PreparedStatement` (Datenbank)
- … praktisch alles, was du „öffnest“

---

## 🧙‍♂️ Mehrere Ressourcen auf einmal?

Kein Problem:

```java
try (
    BufferedReader reader = new BufferedReader(new FileReader("monster.txt"));
    PrintWriter writer = new PrintWriter(new FileWriter("bericht.txt"))
) {
    String zeile;
    while ((zeile = reader.readLine()) != null) {
        writer.println("Gefunden: " + zeile);
    }
}
```

> Beide Ressourcen werden automatisch geschlossen – **in umgekehrter Reihenfolge**.

---

## 🛡️ Warum ist das wichtig?

| Ohne try-with-resources     | Mit try-with-resources         |
|-----------------------------|-------------------------------|
| Ressourcen werden vergessen | Automatisches Schließen       |
| Speicherlecks               | Sichere Ressourcenverwaltung  |
| Lange, verschachtelte `finally`-Blöcke | Klare Struktur                |

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine Methode `leseDatei(String pfad)`,  
   die mit `BufferedReader` jede Zeile ausgibt – per `try-with-resources`.

2. Schreibe eine Methode `kopiereDatei(String quelle, String ziel)`,  
   die zeilenweise mit `BufferedReader` und `PrintWriter` arbeitet – und beide sicher verwaltet.

💥 **Bonus-XP:**  
Füge Fehlerbehandlung hinzu, z. B. `"Datei nicht gefunden"` oder `"Schreibfehler"` – aber elegant!

---

> 🛡️ **+100 XP für sichere Ressourcenmagie gesammelt!**  
> **Nächstes Ziel (finaler Schritt in Level 7):** Concurrency Basics – Threads, Runnable, ExecutorService, Future

---

# 🕰️ **LEVEL 7.6: Concurrency Basics – `Thread`, `Runnable`, `ExecutorService`, `Future`**

> *„Ein Hexer kämpft an vielen Fronten.  
> Und manchmal muss sein Code das auch.“*

Mit Concurrency kannst du:
- mehrere Dinge **parallel oder zeitversetzt** erledigen,
- Threads kontrollieren,
- Aufgaben im Hintergrund ausführen,
- Ergebnisse sammeln, **während dein Programm weiterläuft.**

---

## 🧭 **Was ist ein Thread?**

Ein **Thread** ist ein einzelner **Ausführungsstrang** deines Programms.  
Normalerweise läuft alles im **Haupt-Thread**. Mit Concurrency kannst du **weitere Stränge erzeugen**, die **unabhängig** arbeiten.

---

## 🛠️ **1. Thread mit `Runnable`**

```java
Runnable aufgabe = () -> {
    System.out.println("🧪 Nebenaufgabe gestartet...");
    try { Thread.sleep(1000); } catch (InterruptedException ignored) {}
    System.out.println("✅ Nebenaufgabe beendet.");
};

Thread thread = new Thread(aufgabe);
thread.start();
```

> 💡 `sleep(1000)` pausiert für 1000 Millisekunden (1 Sekunde).

---

## 🧙‍♂️ **2. `ExecutorService` – Der organisierte Hexer**

Statt Threads manuell zu starten, kannst du einen **Executor** verwenden:

```java
ExecutorService executor = Executors.newSingleThreadExecutor();

executor.submit(() -> {
    System.out.println("🎯 Aufgabe läuft...");
});

executor.shutdown();
```

> `submit(...)` übergibt die Aufgabe, `shutdown()` sagt: „Keine neuen Aufgaben mehr!“

---

## 🧪 **3. `Future` – Versprechen auf ein Ergebnis**

Du kannst Aufgaben ausführen **und später das Ergebnis abfragen**:

```java
Callable<String> zauber = () -> {
    Thread.sleep(500);
    return "🧙‍♂️ Zeichen erfolgreich gewirkt.";
};

ExecutorService executor = Executors.newSingleThreadExecutor();
Future<String> ergebnis = executor.submit(zauber);

System.out.println("...Zauber wird vorbereitet...");
String nachricht = ergebnis.get();  // blockiert, bis Ergebnis da
System.out.println(nachricht);

executor.shutdown();
```

> 💡 `Future.get()` blockiert, bis das Ergebnis bereit ist – wie das Warten auf einen Trank.

---

## 📚 Zusammenfassung:

| Technik              | Zweck                             |
|----------------------|------------------------------------|
| `Thread` + `Runnable`| Direktes Starten kleiner Aufgaben |
| `ExecutorService`    | Organisiertes Aufgaben-Management |
| `Future<T>`          | Ergebnis von Aufgaben später abrufen |
| `Callable<T>`        | Wie `Runnable`, aber mit Rückgabewert |

---

## ⚠️ Wichtige Hinweise:

- Immer `shutdown()` oder `shutdownNow()` auf dem Executor aufrufen.
- **Teile keine veränderbaren Daten zwischen Threads** ohne Synchronisation.
- **Fange Exceptions** bei `Future.get()`, da Fehler dort auftreten können.

---

## 🏆 **Deine XP-Quest:**

1. Starte einen neuen `Thread`, der 2 Sekunden wartet und dann `"Nebenaufgabe abgeschlossen"` ausgibt.

2. Nutze `ExecutorService`, um zwei Aufgaben zu starten:
   - eine gibt `"Trank gebraut"` aus,
   - eine zweite `"Monster analysiert"` – beide nach kleiner Verzögerung.

💥 **Bonus-XP:**  
Erstelle eine `Callable<String>`-Aufgabe, die `"Portal geöffnet"` zurückliefert – und gib das Ergebnis über `Future.get()` aus.

---

> 🛡️ **+150 XP für Kontrolle über Zeit und Ausführung gesammelt!**  
> 🎉 **Gratulation, Hexer! Du hast Level 7: Meistere die Tiefe vollständig abgeschlossen!**
