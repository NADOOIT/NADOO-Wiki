# 🧭 **LEVEL 6: Organisiere dein Chaos**

> *„Ein guter Hexer weiß: Ordnung ist nicht Luxus – sie ist Überleben.“*  
>  
> In diesem Level lernst du:
> - wie du deinen Code **nach Verantwortung und Bedeutung gliederst**  
> - wie du **funktionale Programmierung mit Lambdas** nutzt  
> - wie du mit **Dateien arbeitest** – lesen, schreiben, speichern.

---

## 🧱 **6.1 Code in sinnvolle Domänen gliedern – `model`, `service`, `main`**

### ⚔️ **Warum ist Struktur wichtig?**

In kleinen Projekten wirkt Chaos harmlos. Aber bei größeren Systemen entsteht schnell Unübersichtlichkeit.  
Die Folge: schwer wartbarer, fehleranfälliger Code.

> Deshalb: **Trenne Code nach Funktion – nicht nach Technik oder Zufall.**

---

## 🧭 **Die drei häufigsten Domänen im Java-Alltag:**

| Paket/Ordner     | Inhalt                                           |
|------------------|--------------------------------------------------|
| `model`          | **Datenmodelle**, z. B. `Monster`, `Trank`, `Hexer` |
| `service`        | **Logik und Regeln**, z. B. `KampfService`, `InventarVerwaltung` |
| `main` oder `app`| **Startpunkt**, Benutzeroberfläche, Einstieg     |

---

### 🗃️ Beispielstruktur:

```
hexerprojekt/
├── model/
│   ├── Monster.java
│   ├── Trank.java
├── service/
│   ├── KampfService.java
│   ├── TrankVerwaltung.java
├── main/
│   ├── HexerApp.java
```

---

## 🔍 **Beispiele für saubere Verantwortung:**

- `Monster.java` → enthält **nur die Felder und Methoden**, die das Monster selbst betreffen.
- `KampfService.java` → enthält Methoden wie `kaempfe(Monster a, Monster b)`
- `HexerApp.java` → startet die Anwendung, steuert den Ablauf.

> 💡 Damit ist klar:  
> - **Was ist was?**  
> - **Wer macht was?**  
> - **Wohin gehört neue Logik?**

---

## 🛡️ **Was du vermeiden solltest:**

- Alles in einer Datei  
- Klassen mit dem Namen `Helper`, `Util`, `Stuff` ohne klare Verantwortung  
- Wild zusammengewürfelte Methoden

---

## 🏆 **Deine XP-Quest:**

1. Baue ein Miniprojekt mit:
   - Paket `model` für `Monster` und `Trank`
   - Paket `service` mit einer Klasse `KampfService`, die Monster gegeneinander antreten lässt
   - Paket `main` mit einer `HexerApp`, die den Kampf ausführt

💥 **Bonus-XP:**  
Erweitere das `model.Monster` um eine Methode `istSchwachGegen(String schwaeche)`  
und nutze diese Logik in `KampfService`.

---

> 🛡️ **+100 XP für Ordnung und Verantwortungsstruktur gesammelt!**  
> **Nächstes Ziel:** Lambda Expressions – ein Hauch von funktionalem Flow.

---

# 🌀 **LEVEL 6.2: Lambda Expressions – ein Hauch von funktionalem Flow**

> *„Manchmal ist ein Hexer schneller, wenn er nicht nach dem Namen des Zaubers fragt,  
> sondern ihn direkt wirkt.“*  
>  
> Lambdas sind **kurze, präzise Funktionsausschnitte**,  
> die du wie Daten behandeln kannst.  
> Sie helfen dir, **Verhalten flexibel und knapp zu schreiben** – besonders bei Listen, Filtern, Sortieren und Ereignisreaktionen.

---

## 🧭 **Was ist eine Lambda Expression?**

Eine **Lambda Expression** ist ein kurzer Codeblock, der wie eine Methode funktioniert –  
aber **ohne einen Namen**, und direkt im Code übergeben werden kann.

### 🔧 Syntax:
```java
(parameter) -> { Code }
```

Beispiele:

```java
(int x, int y) -> { return x + y; }
s -> System.out.println(s)
() -> System.out.println("Hallo Welt")
```

---

### 💡 **Warum Lambdas?**

Weil du damit:
- Code **verkürzen** kannst
- **Verhalten** wie Daten übergeben kannst
- Besonders gut mit **Collections** und **Streams** arbeiten kannst

---

## 🧪 **Ein erstes Beispiel: Monster filtern**

Stell dir vor, du hast eine Liste von Monstern:

```java
List<Monster> monsterListe = List.of(
    new Monster("Ghul", 80),
    new Monster("Vampir", 120),
    new Monster("Nekker", 50)
);
```

Und du willst nur die starken anzeigen:

```java
monsterListe.stream()
    .filter(monster -> monster.getLebenspunkte() > 80)
    .forEach(monster -> System.out.println(monster.getName()));
```

> 💡 Das ist eine **Lambda Expression**:  
> `monster -> monster.getLebenspunkte() > 80`

---

## 🔍 **Was passiert hier?**

- `.stream()` → wandelt die Liste in einen Datenfluss um  
- `.filter(...)` → gibt nur Elemente weiter, die die Bedingung erfüllen  
- `.forEach(...)` → wendet etwas auf jedes verbleibende Element an

---

## 🎯 **Typische Anwendungsbereiche für Lambdas:**

| Bereich          | Beispiel                                      |
|------------------|-----------------------------------------------|
| Filtern           | `.filter(m -> m.getLebenspunkte() > 100)`     |
| Sortieren         | `.sorted((a, b) -> a.getName().compareTo(b.getName()))` |
| Mappen (umwandeln)| `.map(m -> m.getName().toUpperCase())`       |
| Aktionen          | `.forEach(m -> System.out.println(m))`       |

---

### 🧙‍♂️ Lambdas brauchen Interfaces!

Lambdas funktionieren nur mit sogenannten **Functional Interfaces**:  
→ Interfaces mit **genau einer Methode**.

Beispiel: `Runnable`, `Comparator<T>`, `Predicate<T>`, `Function<T, R>`, `Consumer<T>`

---

### 🧩 Eigene Functional Interfaces (optional):

```java
@FunctionalInterface
public interface MonsterAktion {
    void ausführen(Monster m);
}
```

```java
MonsterAktion aktion = monster -> System.out.println(monster.getName() + " brüllt!");
aktion.ausführen(new Monster("Ghul", 80));
```

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine `List<Monster>` mit mehreren Einträgen.  
2. Nutze `.stream()` und eine Lambda Expression, um:
   - alle Monster mit mehr als 90 Lebenspunkten zu filtern
   - ihre Namen in Großbuchstaben auszugeben

💥 **Bonus-XP:**  
Schreibe eine eigene Methode `bearbeiteMonster(List<Monster>, Predicate<Monster>)`  
und rufe sie mit verschiedenen Lambdas auf, z. B. „zeige nur Vampire“, „zeige alle mit gerader Lebenszahl“.

---

> 🛡️ **+150 XP für funktionalen Flow gesammelt!**  
> **Nächstes Ziel:** Dateizugriff & File-API (`java.nio.file`) – Dateien lesen und schreiben.

---

# 📜 **LEVEL 6.3: Dateizugriff & File-API – Dateien lesen und schreiben**

> *„Was du nicht aufschreibst, wird vergessen.  
> Was du speicherst, lebt weiter – selbst wenn dein Programm längst beendet ist.“*  
>  
> In diesem Abschnitt lernst du:
> - Wie man mit Java **Dateien liest und schreibt**  
> - Welche Klassen dir dabei helfen  
> - Worauf du bei Dateipfaden achten musst

---

## 📦 **Was ist `java.nio.file`?**

Das Paket `java.nio.file` ist der **moderne Weg**, um in Java mit Dateien zu arbeiten.

Die wichtigsten Klassen:
- `Path`: Repräsentiert einen Pfad im Dateisystem
- `Files`: Enthält **statische Hilfsmethoden**, um Dateien zu lesen, schreiben, prüfen

---

## 🛠️ **Schreiben in eine Datei:**

```java
import java.nio.file.*;
import java.io.IOException;
import java.util.List;

public class Grimoire {
    public static void main(String[] args) throws IOException {
        Path pfad = Paths.get("monster.txt");
        List<String> monsterListe = List.of("Ghul", "Vampir", "Nekker");

        Files.write(pfad, monsterListe);
        System.out.println("Monsterliste gespeichert.");
    }
}
```

> 💡 `Files.write()` schreibt automatisch Zeile für Zeile.

---

## 📖 **Lesen aus einer Datei:**

```java
List<String> zeilen = Files.readAllLines(Paths.get("monster.txt"));
for (String zeile : zeilen) {
    System.out.println("Gefunden: " + zeile);
}
```

---

## ⚠️ **Was du beachten solltest:**

- `IOException` kann auftreten → du musst sie **fangen oder weiterwerfen** (`throws`)
- Die Datei wird **überschrieben**, wenn sie bereits existiert
- Verwende `StandardOpenOption.APPEND`, wenn du **anhängen** willst:

```java
Files.write(pfad, List.of("Wyvern"), StandardOpenOption.APPEND);
```

---

## 🧙‍♂️ **Dateien prüfen, löschen, erstellen**

```java
Path pfad = Paths.get("truhen.txt");

if (Files.exists(pfad)) {
    System.out.println("Datei existiert!");
}

Files.delete(pfad);  // Achtung: löscht ohne Rückfrage!
```

---

## 🔒 **Sonderfall: Ressourcen auslesen (z. B. in JAR-Dateien)**

> Hinweis: Wenn du mit `getClass().getResourceAsStream(...)` arbeiten willst,  
> brauchst du andere Mechanismen – **das behandeln wir später bei modularen Projekten.**

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine `List<String>` mit deinen Lieblingsmonstern und speichere sie in `monster.txt` mit `Files.write()`.

2. Lies die Datei anschließend mit `Files.readAllLines()` und gib jede Zeile aus.

💥 **Bonus-XP:**  
Füge einen neuen Eintrag (`"Basilisk"`) mit `StandardOpenOption.APPEND` hinzu, **ohne die Liste zu löschen**.


> 🛡️ **+150 XP für bleibende Artefakte gesammelt!**  
> 🎉 **Glückwunsch, Hexer! Du hast Level 6: Organisiere dein Chaos vollständig abgeschlossen!**

---

<p align="center">
<a href="/docs/06-entwicklung/05-java/01-tutorial/05-theorie/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/07-theorie/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/05-java/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zum Inhaltsverzeichis</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>