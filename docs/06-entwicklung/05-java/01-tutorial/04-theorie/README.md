# 🛡️ **LEVEL 4: Schütze deinen Code**

> *„Ein Hexer kämpft nicht nur mit Schwert und Zeichen – er schützt sein Wissen, seine Artefakte und seine Gefährten.“*  
>  
> Genauso schützt ein sauberer Entwickler seinen Code:  
> - Wer darf was sehen?  
> - Wo dürfen Informationen fließen?  
> - Wie organisierst du dein Wissen in klaren Kammern (Paketen)?  
>  
> In diesem Level geht es um **Sichtbarkeit, Kapselung und Strukturierung**.

---

## 🗝️ **4.1 Alle Zugriffsmodifikatoren verstehen – `public`, `private`, `protected`, default**

### 📜 **Was sind Zugriffsmodifikatoren?**

Sie steuern, **wer auf Felder und Methoden zugreifen darf**:

| Modifikator | Wer darf zugreifen? |
|-------------|---------------------|
| `public`    | Jeder, überall        |
| `private`   | Nur innerhalb der eigenen Klasse |
| `protected` | In der Klasse **und** in allen Unterklassen |
| *(default)* | Innerhalb desselben Pakets (kein Schlüsselwort nötig) |

---

### 🧩 **Beispiele:**

#### `public` – Freier Zugang

```java
public String name;
```
> Überall sichtbar – manchmal notwendig, aber vorsichtig einsetzen.

---

#### `private` – Geheimer Schatz

```java
private int lebensPunkte;
```
> Nur die eigene Klasse kennt diese Information.

---

#### `protected` – Familiengeheimnis

```java
protected int magischeKraft;
```
> Nur die eigene Klasse **und** alle direkten Nachkommen können darauf zugreifen.

---

#### *(kein Modifikator)* – Paket-Sichtbarkeit

```java
int monsterZahl;
```
> Nur für Klassen im **gleichen Paket** sichtbar – oft genutzt, wenn Module zusammengehören.

---

## 🛡️ **Warum überhaupt einschränken?**

- **Schutz vor versehentlichen Änderungen:** Niemand sollte deine wichtigen Felder einfach ändern können.
- **Klare Schnittstellen:** Du gibst nur preis, was wirklich gebraucht wird.
- **Flexibilität:** Du kannst die Implementierung ändern, ohne dass fremder Code auseinanderbricht.

> 💡 **Faustregel:**  
> „So viel abschotten wie möglich, so viel öffnen wie nötig.“

---

## 🏆 **Deine XP-Quest:**

1. Baue eine Klasse `HexerGeheimnisse`:
   - Ein `private String` `geheimeFormel`.
   - Ein `protected int` `zauberKraft`.
   - Eine `public` Methode `zeigeGeheimnis()`, die nur den Text `"Vertraue niemandem."` ausgibt.

2. Schreibe eine Unterklasse `SchülerHexer`, die auf `zauberKraft` zugreift und ihn nutzt.

💥 **Bonus-XP:**  
Erzeuge eine Klasse im selben Paket, die testet, ob sie auf `zauberKraft` zugreifen kann (Spoiler: geht nicht direkt!).

---

> 🛡️ **+100 XP für Sichtbarkeit und Schutz gesammelt!**  
> **Nächstes Ziel:** Kapsle alles. Keine Leaks. Keine Gnade.

---

# 🛡️ **LEVEL 4.2: Kapsle alles – Keine Leaks. Keine Gnade.**

> *„Dein Wissen gehört dir. Dein Inventar gehört dir.  
> Teile nur das, was andere wissen müssen – und nichts darüber hinaus.“*  
>  
> In der Welt des Codes heißt das: **Kapselung**.  
> Ein Hexer öffnet nur so viele Türen, wie er muss – und verschließt alles andere sorgfältig.

---

## 🏰 **Was bedeutet Kapselung in Java?**

**Kapselung** bedeutet:
- **Felder (Daten)** sind **privat**.
- Zugriff erfolgt **nur über kontrollierte Methoden** (`getters` und `setters`).
- Du entscheidest, welche Regeln beim Lesen oder Schreiben gelten.

Das schützt:
- Deine Daten vor versehentlichen Änderungen
- Deine Logik vor unkontrollierten Zugriffen
- Deine Architektur vor Chaos

---

## 🛡️ **Beispiel für perfekte Kapselung:**

```java
public class Trank {
    private String name;
    private int wirkstaerke;

    public Trank(String name, int wirkstaerke) {
        this.name = name;
        setWirkstaerke(wirkstaerke);  // Nutzung des Setters im Konstruktor
    }

    public String getName() {
        return name;
    }

    public int getWirkstaerke() {
        return wirkstaerke;
    }

    public void setWirkstaerke(int wirkstaerke) {
        if (wirkstaerke >= 0) {
            this.wirkstaerke = wirkstaerke;
        } else {
            throw new IllegalArgumentException("Wirkstärke darf nicht negativ sein!");
        }
    }
}
```

### ⚔️ Wichtige Punkte:
- **Alle Felder sind privat.**
- **Getter und Setter entscheiden**, wie Zugriff funktioniert.
- Validierung findet **zentral** statt (hier im Setter).
- Die Klasse **kontrolliert ihre eigenen Daten.**

---

## 🧙‍♂️ **Warum ist Kapselung so wichtig?**

| Ohne Kapselung                      | Mit Kapselung                         |
|--------------------------------------|---------------------------------------|
| Jeder kann Felder beliebig verändern | Nur kontrollierte Änderungen möglich |
| Gefahr von fehlerhaften Zuständen    | Schutz durch Prüfungen und Regeln     |
| Schwer wartbar und unsicher          | Klar strukturierte Verantwortung      |

---

## 🧩 **Sonderfall: Nur Getter, kein Setter**

Manchmal willst du, dass ein Wert **nur gelesen**, aber **nicht mehr verändert** werden kann (nachdem er gesetzt wurde):

```java
private final String rezeptName;

public String getRezeptName() {
    return rezeptName;
}
```

So machst du ein Feld **read-only** (nur lesbar).

---

## 🛡️ **Kapselungstaktiken für Hexer:**

- Felder grundsätzlich **`private`**.
- Zugriff nur über **`public` Getters/Setters** – und dort ggf. Regeln einbauen.
- Setter **nur da, wo wirklich sinnvoll** (z. B. manche Werte sollten sich nach dem Erzeugen nicht mehr ändern).
- Validierungen konsequent im Setter durchführen.

---

## 🏆 **Deine XP-Quest:**

1. Baue eine Klasse `MonsterInventar`:
   - `private int anzahlBomben`
   - `private List<String> bombenListe`
   - Getter für beide Felder
   - Setter für `anzahlBomben` (mit Überprüfung: darf nicht negativ sein)
   - Methode `fügeBombeHinzu(String bombe)`, die die Bombe in die Liste aufnimmt.

2. Verhindere, dass jemand von außen die Bombenliste direkt manipulieren kann:
   - Gib eine **Kopie** der Liste zurück, nicht das Original!

💥 **Bonus-XP:**  
Schreibe die Getter so, dass sie eine **unveränderbare Kopie** (`Collections.unmodifiableList`) zurückgeben.

---

> 🛡️ **+150 XP für vollständige Kapselungsbeherrschung gesammelt!**  
> **Nächstes Ziel:** `package` und `import` meistern – deine Codewelt strukturieren.

---

# 📦 **LEVEL 4.3: `package` und `import` meistern – Struktur für deine Welt**

> *„Ein Hexerkloster hat Schlafsäle, Waffenlager, Alchemie-Labore.  
> Und ein kluger Hexer weiß genau, wo er was finden kann.“*  
>  
> In Java strukturierst du deinen Code in **Pakete** –  
> damit du und andere sich auch in riesigen Projekten schnell zurechtfinden.

---

## 🧭 **Was ist ein `package`?**

Ein **Paket** ist einfach ein **Ordner** (eine logische Gruppe) für verwandte Klassen.

Beispiel:
```
monster/
    Vampir.java
    Ghul.java
trank/
    Heiltrank.java
    Stärketrank.java
```

Statt 1000 Dateien in einem Verzeichnis zu haben, gruppierst du sie sinnvoll.

---

### 📜 **So deklarierst du ein Paket:**

Am Anfang jeder Datei:

```java
package monster;
```

> Das zeigt:  
> Diese Klasse gehört zum Paket `monster`.

---

### 🚀 **`import` – Hol dir, was du brauchst**

Willst du eine Klasse aus einem anderen Paket benutzen? Dann musst du sie **importieren**:

```java
import trank.Heiltrank;

public class Vampir extends Monster {
    private Heiltrank heiltrank;
}
```

> 💡 Ohne `import` kennt Java nur Klassen im gleichen Paket und die Standardbibliothek (`java.lang`).

---

## 🧩 **Mehrere Klassen importieren**

- Einzelimport:
  ```java
  import trank.Heiltrank;
  import trank.Stärketrank;
  ```
- Oder alles aus einem Paket:
  ```java
  import trank.*;
  ```
  > **Hinweis:** `*` importiert **nur Klassen**, nicht Unterpakete.

---

## 🧙‍♂️ **Warum Pakete verwenden?**

| Vorteil                       | Erklärung                                        |
|-------------------------------|--------------------------------------------------|
| Bessere Übersicht             | Verwandte Klassen zusammen gruppiert             |
| Bessere Wartbarkeit           | Große Projekte bleiben verständlich              |
| Schutz auf Paketebene         | *(default)* Sichtbarkeit regelt Zugriff nur innerhalb eines Pakets |
| Namenskonflikte vermeiden     | Zwei Klassen können im Projekt denselben Namen haben, wenn sie in unterschiedlichen Paketen sind |

---

### ⚔️ **Beispiel: Zwei Klassen gleichen Namens in verschiedenen Paketen**

```
monster/Vampir.java
trank/Vampir.java
```

Geht problemlos!  
Im Code referenzierst du sie einfach eindeutig:

```java
monster.Vampir monsterVampir = new monster.Vampir();
trank.Vampir trankVampir = new trank.Vampir();
```

---

## 📦 **Namenskonventionen für Pakete**

- Alles **kleingeschrieben**.
- Keine Umlaute, Sonderzeichen oder Leerzeichen.
- Üblich ist eine Hierarchie, z. B.:
  ```
  com.hexerschule.monster
  com.hexerschule.trank
  ```

> Für kleine private Projekte reichen einfache Paketnamen (`monster`, `trank`, `hexer`).

---

## 🏆 **Deine XP-Quest:**

1. Erstelle zwei Pakete:
   - `monster` mit den Klassen `Ghul` und `Vampir`
   - `trank` mit den Klassen `Heiltrank` und `Stärketrank`

2. Lass `Vampir` einen `Heiltrank` verwenden.  
   Importiere die Klasse sauber.

💥 **Bonus-XP:**  
Erzeuge ein drittes Paket `hexer`, das einen `Hexer` enthält, der Monster jagt und Tränke sammelt.

---

> 🛡️ **+150 XP für Ordnung und Struktur gesammelt!**  
> **Nächstes Ziel:** String-Builder – mächtige Texte effizient bauen.

---

# 🛠️ **LEVEL 4.4: String-Builder – Texte effizient schmieden**

> *„Manchmal reicht es nicht, einen Trank zu brauen.  
> Man muss Zutaten mischen, rühren, abschmecken – und das effizient.“*  
>  
> Texte (Strings) im Code brauchen oft viele kleine Bearbeitungsschritte.  
> Mit `StringBuilder` arbeitest du schneller, sicherer und sauberer als mit purem Aneinanderkleben (`+`).

---

## 🧭 **Warum nicht einfach `+` benutzen?**

Klar, du kennst sowas:

```java
String botschaft = "Hexer " + name + " hat " + monsterKills + " Monster erledigt.";
```

Das funktioniert – aber **jedes `+` erzeugt intern einen neuen String**.  
Denn Strings sind in Java **unveränderlich** (*immutable*).

➡️ Viele `+`-Operationen = viele neue String-Objekte = unnötige Speicherbelastung.

Gerade bei vielen Textoperationen oder Schleifen wird das **sehr ineffizient**.

---

## ⚡ **Die Lösung: `StringBuilder`**

Ein `StringBuilder` ist wie eine **flexible Text-Klinge**:  
Du kannst ihn **verändern, anhängen, einfügen**, ohne ständig neue Objekte zu bauen.

---

### 🛠️ **Grundlegende Nutzung:**

```java
StringBuilder sb = new StringBuilder();
sb.append("Hexer ");
sb.append(name);
sb.append(" hat ");
sb.append(monsterKills);
sb.append(" Monster erledigt.");

String botschaft = sb.toString();
System.out.println(botschaft);
```

> 💡 `append()` fügt neuen Text an das Ende an.  
> `toString()` holt am Schluss den fertigen Text.

---

### 🧩 **Noch kompakter:**

```java
String botschaft = new StringBuilder()
    .append("Hexer ")
    .append(name)
    .append(" hat ")
    .append(monsterKills)
    .append(" Monster erledigt.")
    .toString();
```

---

## 🧙‍♂️ **Wann ist `StringBuilder` besser als `+`?**

| Situation | Empfehlung |
|-----------|-------------|
| Wenige, einzelne Verkettungen | `+` reicht völlig aus |
| Viele Verkettungen, Schleifen, dynamische Texte | **StringBuilder verwenden!** |

> Faustregel: **Wenn mehr als 2–3 Konkatenationen in Folge → StringBuilder.**

---

## ⚡ **Weitere nützliche Methoden von `StringBuilder`**

| Methode | Zweck |
|---------|-------|
| `insert(index, text)` | Text an bestimmter Stelle einfügen |
| `delete(start, end)` | Teilstring löschen |
| `replace(start, end, text)` | Teilstring ersetzen |
| `reverse()` | Text umkehren |

Beispiel:

```java
StringBuilder spruch = new StringBuilder("Igni");
spruch.reverse();
System.out.println(spruch);  // → "ingI"
```

---

## 🧩 **`StringBuffer` vs `StringBuilder`**

Vielleicht findest du auch `StringBuffer` im Internet?  
Kurz gesagt:
- `StringBuffer` ist **thread-sicher** (langsamer, synchronisiert).
- **`StringBuilder` ist schneller** und völlig ausreichend, wenn du keinen parallelen Zugriff brauchst.

**In fast allen Fällen nimmst du `StringBuilder`.**

---

## 🏆 **Deine XP-Quest:**

1. Baue eine Methode `baueMonsterMeldung(String name, int kills)`, die mit einem `StringBuilder` einen Satz erstellt:
   - `"Hexer Geralt hat 12 Monster erledigt."`

2. Schreibe eine Schleife, die mit `StringBuilder` eine Liste von Monstern zusammenbaut:
   - `"Gefundene Monster: Ghul, Vampir, Nekker."`

💥 **Bonus-XP:**  
Erweitere die Methode so, dass am Ende kein Komma hinter dem letzten Monster steht.

---

> 🛡️ **+100 XP für effizientes Textschmieden gesammelt!**  
> **Nächstes Ziel:** Garbage-Collector – Verstehe, wie Java deinen Speicher schützt.

---

# ♻️ **LEVEL 4.5: Garbage-Collector – Dein unsichtbarer Wächter**

> *„Ein Hexer tötet Monster.  
> Ein Garbage-Collector entfernt nutzlose Überreste.“*  
>  
> In Java musst du dich **nicht** wie in anderen Sprachen selbst darum kümmern, ungenutzte Objekte aus dem Speicher zu löschen.  
> **Der Garbage-Collector (GC)** erledigt diese Arbeit für dich –  
> leise, zuverlässig, im Hintergrund.

---

## 🧭 **Was ist der Garbage-Collector?**

Der **Garbage-Collector** ist ein Teil der Java Virtual Machine (JVM).  
Sein Job:
- **Alte, nicht mehr benötigte Objekte erkennen**.
- Diese Objekte **automatisch aus dem Speicher entfernen**.
- So verhindern, dass dein Programm langsam wird oder abstürzt, weil der Speicher voll läuft.

---

## 🗝️ **Wann wird ein Objekt Müll („garbage“)?**

Ein Objekt wird dann zu Müll, wenn es **keine erreichbaren Verweise (Referenzen)** mehr hat.

Beispiel:

```java
Monster ghul = new Monster("Ghul", 80);
ghul = null;  // Referenz weg!
```

- Früher zeigte `ghul` auf ein Monster im Speicher.
- Jetzt zeigt `ghul` auf nichts (`null`).
- Das ursprüngliche `Monster`-Objekt existiert noch **irgendwo** – aber niemand hat mehr eine Adresse dazu.

➡️ Der Garbage-Collector wird es **früher oder später** aufspüren und entsorgen.

---

### 🛡️ **Wichtig:**  
Du musst **niemals selbst `delete` oder `free` aufrufen** wie in C oder C++.  
Java regelt die Speicherbereinigung automatisch.

---

## ⚡ **Wann genau räumt der Garbage-Collector auf?**

Ganz wichtig:  
> Der Garbage-Collector arbeitet **asynchron** und **unvorhersehbar**.

- **Nicht sofort**, wenn du `null` setzt.
- Er entscheidet **selbst**, wann es sinnvoll ist.
- Meistens, wenn der Speicher knapp wird oder wenn dein Programm ein bisschen Luft hat.

> **Fazit:** Du solltest dich **auf die Logik deines Codes konzentrieren**, nicht auf Speicherbereinigung.

---

## 🧩 **Wie kannst du helfen, Müll zu vermeiden?**

- **Unnötige Referenzen abbauen:**
  ```java
  monster = null;  // Nur nötig, wenn sehr große Datenstrukturen manuell freigegeben werden sollen
  ```
- **Kurze Lebenszeiten für Objekte:**  
  Objekte nur so lange leben lassen, wie sie wirklich gebraucht werden.
- **Vermeide unnötige große Datenstrukturen, die lange hängen bleiben.**

---

## 🧙‍♂️ **Was du NICHT tun solltest:**

- Keine wilden Versuche, den Garbage-Collector selbst zu zwingen (`System.gc()` aufrufen).
- Keine Angst haben, viele kleine Objekte zu erzeugen – Java ist dafür gebaut.

---

## 🛡️ **Zusammengefasst:**

| Gut                                        | Schlecht                                       |
|--------------------------------------------|------------------------------------------------|
| Objekte lokal in Methoden anlegen          | Riesige, langlebige Sammlungen ohne Sinn       |
| Großes Zeug auf `null` setzen, wenn klar ist, dass es nicht mehr gebraucht wird | Mit `System.gc()` versuchen, den GC manuell zu starten |
| Speicher den Java-Mechanismen überlassen   | Panik und übermäßige Optimierung versuchen     |

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine Methode `erschaffeMonster()`, die lokal ein `Monster`-Objekt anlegt und danach verschwindet.

2. Weise in einer anderen Methode einem `Monster`-Objekt `null` zu und kommentiere, **was dann passiert**.

💥 **Bonus-XP:**  
Erkläre mit eigenen Worten, warum du in Java keine Angst vor Speicherlöchern (Memory Leaks) haben musst – aber auch warum sie trotzdem manchmal entstehen können.

---

> 🛡️ **+100 XP für Verständnis von Speichermagie gesammelt!**  
> **Damit hast du Level 4: Schütze deinen Code vollständig abgeschlossen! 🎉**

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
📅 <strong>Dieses Dokument wurde bearbeitet am:</strong> 19.09.2025
<br>
✍️ <strong>Von:</strong> <a href="https://github.com/johkori">Johkori(Tim H.)</a> (GitHub)
</p>

---

<p align="center">
<a href="/docs/06-entwicklung/05-java/01-tutorial/03-theorie/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/05-theorie/README.md"><strong>Weiter</strong></a>
</p>
