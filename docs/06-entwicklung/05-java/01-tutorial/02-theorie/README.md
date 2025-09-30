# 🏰 **LEVEL 2: Denke in Objekten**  
> *Ein einzelnes Schwert ist gut. Eine ganze Waffenkammer – das ist besser.  
> Doch was wäre eine Waffenkammer ohne Ordnung, ohne Pläne, ohne ein System?*  
>  
> In diesem Level lernst du, wie du die Welt deines Codes nicht nur in einzelne Werte,  
> sondern in **echte Gegenstände** – in **Objekte** – denken kannst.

---

## 🎭 **2.1 Erstelle deine erste `class` mit Feldern und Methoden**

> *„Ein Ghul ist kein Vampir. Ein Wyvern ist kein Nekker. Aber alle sind Monster.“*  
> Genauso wie in der Welt von The Witcher gibt es auch im Code **Dinge, die etwas gemeinsam haben**, aber dennoch eigene Eigenschaften besitzen.

In Java baust du dir deine eigenen Baupläne für solche Dinge. Diese Pläne heißen **Klassen** (engl. `class`). Eine Klasse beschreibt **was ein Ding ist** und **was es tun kann**.

---

### 🧱 **Was ist eine Klasse?**

Eine Klasse ist wie ein Bauplan für etwas in deiner Welt. Zum Beispiel ein Monster:

```java
public class Monster {
    // Eigenschaften (Felder)
    String name;
    int lebensPunkte;

    // Fähigkeiten (Methoden)
    void angreifen() {
        System.out.println(name + " greift an!");
    }
}
```

> 💡 Stell dir vor:  
> Die Klasse `Monster` ist der Bauplan.  
> Ein **konkretes Monster**, zum Beispiel ein Ghul, ist dann ein **Objekt** aus diesem Bauplan.

---

### 🐺 **Objekt erstellen („Instanzieren“) – Der Ghul wird lebendig:**

```java
Monster ghul = new Monster();
ghul.name = "Ghul";
ghul.lebensPunkte = 80;
ghul.angreifen();
```

> Ausgabe:
```
Ghul greift an!
```

---

### ⚡ **Warum braucht man Klassen?**

Weil du so **komplexe Zusammenhänge** abbilden kannst:  
- Ein Monster hat einen Namen.  
- Es hat Lebenspunkte.  
- Es kann angreifen.  
- Vielleicht kommen später noch Spezialfähigkeiten dazu.  

Wenn du stattdessen alles mit einzelnen Variablen machen würdest, wäre das Chaos vorprogrammiert.

---

## 🧭 **2.2 Verstehe `this`, `constructor`, Überladung, `toString()`**

### 🪄 **`this`: Wenn sich das Monster selbst meint**

Manchmal muss das Monster **über sich selbst sprechen**. Dafür gibt es `this`:

```java
void anzeigen() {
    System.out.println("Ich bin ein " + this.name + " mit " + this.lebensPunkte + " Lebenspunkten.");
}
```

Wenn du in deiner Klasse das Wort `this` benutzt, beziehst du dich auf **das aktuelle Objekt**.

---

### 🏗️ **Constructor – Wie wird ein Monster geboren?**

Ein Constructor ist eine **besondere Methode**, die aufgerufen wird, wenn ein neues Objekt entsteht:

```java
public class Monster {
    String name;
    int lebensPunkte;

    // Constructor
    public Monster(String name, int lebensPunkte) {
        this.name = name;
        this.lebensPunkte = lebensPunkte;
    }

    void angreifen() {
        System.out.println(name + " greift an!");
    }
}
```

> Jetzt kannst du direkt ein Monster erschaffen, ohne die Felder extra zu setzen:

```java
Monster vampir = new Monster("Vampir", 120);
vampir.angreifen();
```

---

### 💎 **Überladung – Mehrere Wege, ein Monster zu bauen**

Manchmal willst du verschiedene Arten, etwas zu erzeugen:

```java
public Monster(String name) {
    this.name = name;
    this.lebensPunkte = 100;  // Standard-Lebenspunkte
}
```

Jetzt hast du **zwei Constructoren**:  
- Einen für Name + Lebenspunkte  
- Einen nur für den Namen, mit Standardwerten

---

### 🪞 **`toString()` – Schön formatiert ausgeben**

Standardmäßig zeigt Java bei `System.out.println(objekt)` nur so etwas wie `Monster@6d06d69c`.  
Nicht sehr leserlich, oder? Mit `toString()` kannst du das ändern:

```java
@Override
public String toString() {
    return "Monster: " + name + " | Lebenspunkte: " + lebensPunkte;
}
```

Dann:
```java
System.out.println(vampir);
```

> Ausgabe:
```
Monster: Vampir | Lebenspunkte: 120
```

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine Klasse `Monster` mit:
   - den Feldern `name` und `lebensPunkte`
   - einem Constructor, um beides zu setzen
   - einer Methode `angreifen()`, die den Angriff ausgibt  
2. Erstelle zwei verschiedene Monster und lasse sie angreifen.  
3. Überschreibe `toString()`, damit eine schöne Ausgabe erscheint.

💥 **Bonus-XP:**  
Überlade den Constructor, sodass du auch ein Monster nur mit Namen erstellen kannst, das automatisch 100 Lebenspunkte bekommt.

---

> 🛡️ **+100 XP für Objektdenken gesammelt!**  
> **Nächstes Ziel:** Getters, Setters und Immutability – schütze, was dir gehört.

---

# 🛡️ **2.3 Getters, Setters, Immutability verstehen – Schütze, was dir gehört**

> *„Ein Hexer zeigt nicht jedem seine Karten. Und auch ein Monster offenbart seine Schwächen nur ungern.“*  
>  
> In der Welt des Codes bedeutet das: **Schütze deine Daten. Entscheide, wer was sehen und ändern darf.**

---

## 🏹 **Warum sollten Felder nicht einfach „public“ sein?**

Klar, es ist bequem, einfach zu schreiben:
```java
public int lebensPunkte;
```

Aber das ist, als würdest du deine Truhen offen auf dem Marktplatz stehen lassen – jeder könnte einfach reingreifen und Werte verändern, ohne dass du es mitbekommst.

Beispiel:
```java
vampir.lebensPunkte = -9999;  // Ups. Unsterblicher Vampir.
```

Um das zu verhindern, benutzt man in Java meist **`private`**:
```java
private int lebensPunkte;
```

Das heißt: **Nur die eigene Klasse selbst darf auf dieses Feld zugreifen.**

---

## 🗝️ **Getters und Setters – Die kontrollierten Zugangstore**

Aber wie kommt man dann an die Werte ran oder ändert sie?  
Richtig: Über **kontrollierte Methoden**, die du selbst schreibst – die sogenannten **Getter** (zum Lesen) und **Setter** (zum Schreiben).

```java
public int getLebensPunkte() {
    return lebensPunkte;
}

public void setLebensPunkte(int lebensPunkte) {
    if (lebensPunkte >= 0) {
        this.lebensPunkte = lebensPunkte;
    } else {
        System.out.println("Lebenspunkte können nicht negativ sein!");
    }
}
```

> 💡 **Wichtig:**  
> Du entscheidest, **was erlaubt ist**!  
> Im Setter kannst du z. B. verhindern, dass jemand negative Lebenspunkte setzt.

---

### 🏗️ **Getter und Setter für alle Felder**

Hier ein vollständiges Beispiel:
```java
public class Monster {
    private String name;
    private int lebensPunkte;

    public Monster(String name, int lebensPunkte) {
        this.name = name;
        this.lebensPunkte = lebensPunkte;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getLebensPunkte() {
        return lebensPunkte;
    }

    public void setLebensPunkte(int lebensPunkte) {
        if (lebensPunkte >= 0) {
            this.lebensPunkte = lebensPunkte;
        } else {
            System.out.println("Lebenspunkte können nicht negativ sein.");
        }
    }

    @Override
    public String toString() {
        return "Monster: " + name + " | Lebenspunkte: " + lebensPunkte;
    }
}
```

---

## 🧩 **Immutability – Wenn Dinge nicht verändert werden sollen**

> *„Es gibt Dinge, die unveränderlich sind. Die Gesetze der Alchemie. Die Schwäche eines Vampirs für Knoblauch.“*

In manchen Fällen willst du **gar nicht, dass sich etwas ändert**, nachdem es einmal gesetzt wurde.

Beispiel:
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

- Das Feld `name` ist hier **`final`**: Es **kann nur einmal gesetzt** werden – im Constructor.
- Es gibt **keinen Setter** – weil der Name eines Trankes sich nicht ändern soll.

Solche **unveränderlichen Objekte** nennt man **immutable**.

> 💡 Vorteile von Immutability:
> - Fehlerquellen werden reduziert (nichts ändert sich heimlich).
> - Besser für parallele Programmierung (keine Race Conditions).
> - Sicher und stabil (gut für Werte, die sich nie ändern sollen).

---

## 🛡️ **Deine XP-Quest:**

1. Baue die Klasse `Monster` so um, dass:
   - `lebensPunkte` **private** ist,
   - es einen **Getter** und **Setter** dafür gibt,
   - der Setter verhindert, dass `lebensPunkte` negativ werden.

2. Erstelle zusätzlich eine Klasse `Trank`, die:
   - einen `final`-Namen besitzt,
   - keinen Setter hat (immutable),
   - den Namen über einen Getter ausgibt.

💥 **Bonus-XP:**  
Lass dir eine Fehlermeldung ausgeben, wenn jemand versucht, dem Monster negative Lebenspunkte zu geben.

---

> 🛡️ **+100 XP für saubere Datenverwaltung gesammelt!**  
> **Nächstes Ziel:** Logische Operatoren meistern – baue Bedingungen mit „und“ und „oder“.

---

# 🧠 **2.4 Logische Operatoren meistern – Verknüpfe Bedingungen wie ein Hexer**

> *„Wenn das Monster ein Vampir ist **und** es Nacht ist – dann besser Igni bereithalten.  
> Wenn das Monster ein Nekker ist **oder** ein Ghul – dann reicht das Silberschwert.“*  
>  
> Entscheidungen sind selten nur schwarz oder weiß. Oft musst du mehrere Informationen zusammenbringen. Dafür brauchst du die logischen Operatoren.

---

## 🔥 **Das Arsenal der logischen Operatoren**

| Operator | Bedeutung                  | Beispiel                |
|----------|----------------------------|------------------------|
| `&&`     | **und** – beide Bedingungen müssen wahr sein | `leben > 0 && waffeBereit == true` |
| `||`     | **oder** – mindestens eine Bedingung muss wahr sein | `monsterArt.equals("Ghul") || monsterArt.equals("Nekker")` |
| `!`      | **nicht** – kehrt eine Bedingung um            | `!schildAktiv` (wenn das Schild *nicht* aktiv ist) |

---

### ⚔️ **`&&` (Und) – Beide müssen stimmen**

Ein Angriff ist nur dann möglich, wenn das Monster lebt **und** die Waffe bereit ist:

```java
if (monster.lebensPunkte > 0 && waffeBereit) {
    System.out.println("Angriff starten!");
} else {
    System.out.println("Kein Angriff möglich.");
}
```

> 💡 **Merke:**  
> Wenn auch nur **eine** der beiden Bedingungen falsch ist, läuft der `else`-Zweig.

---

### 🧿 **`||` (Oder) – Mindestens eine reicht**

Ein Silberschwert wird benötigt, wenn das Monster ein Ghul **oder** ein Nekker ist:

```java
if (monsterArt.equals("Ghul") || monsterArt.equals("Nekker")) {
    System.out.println("Silberschwert einsetzen!");
} else {
    System.out.println("Normale Klinge reicht.");
}
```

> 💡 **Merke:**  
> Sobald **eine** der beiden Bedingungen wahr ist, reicht das.

---

### 🌑 **`!` (Nicht) – Umkehr der Wahrheit**

Manchmal willst du etwas prüfen, das **nicht** der Fall ist:

```java
if (!schildAktiv) {
    System.out.println("Schild aktivieren!");
}
```

> Bedeutet: **Wenn das Schild nicht aktiv ist**, dann aktiviere es.

---

### 🧩 **Kombinationen – Mehrere Bedingungen clever verknüpfen**

Natürlich kannst du auch kombinieren:

```java
if ((monsterArt.equals("Vampir") || monsterArt.equals("Fleder")) && nacht) {
    System.out.println("Feuerzeichen bereit machen!");
}
```

> **Nur wenn:**  
> - das Monster ein Vampir **oder** Fleder ist  
> **und gleichzeitig**  
> - Nacht herrscht  
> …dann wird das Feuerzeichen vorbereitet.

---

### ⚠️ **Achte auf Klammern!**

Wie in der Alchemie: Reihenfolge ist alles.

Ohne Klammern:
```java
if (monsterArt.equals("Vampir") || monsterArt.equals("Fleder") && nacht)
```

Das prüft zuerst `monsterArt.equals("Fleder") && nacht`,  
**nicht** was du vielleicht beabsichtigt hast.

Darum immer **mit Klammern** arbeiten, wenn es um mehrere Bedingungen geht.

---

## 🏆 **Deine XP-Quest:**

1. Schreibe eine Methode `checkAngriff()`, die entscheidet:
   - Ein Angriff ist nur möglich, wenn das Monster lebt **und** das Schild aktiviert ist.
   - Wenn das Monster ein Ghul **oder** ein Nekker ist, soll eine Warnung erscheinen: `"Silberschwert empfohlen!"`.

2. Teste die Methode mit verschiedenen Monstern und Schild-Status.

💥 **Bonus-XP:**  
Erweitere die Methode so, dass sie zusätzlich prüft, ob Nacht ist – und Vampiren nur dann Feuerzauber empfohlen wird.

---

> 🛡️ **+100 XP für logisches Denken gesammelt!**  
> **Nächstes Ziel:** Lerne `public` und `private` – öffne und schütze bewusst.

---

# 🔐 **2.5 Lerne `public` und `private` – öffne und schütze bewusst**

> *„Vertrau nicht jedem. Teile dein Wissen mit Bedacht.“*  
>  
> In Java entscheidest **du selbst**, welche Teile deines Codes sichtbar und benutzbar sind – und welche nicht.  
> Das Zauberwort dafür heißt: **Zugriffsmodifikatoren**.

---

## 🏰 **Zugriffsmodifikatoren – Wer darf rein, wer bleibt draußen?**

| Schlüsselwort  | Bedeutung                                   |
|----------------|---------------------------------------------|
| `public`       | Jeder darf darauf zugreifen                 |
| `private`      | Nur innerhalb der eigenen Klasse sichtbar   |
| `protected`    | Nur innerhalb der eigenen Klasse **und** Unterklassen (kommt später) |
| *(kein Modifikator)* | Zugriff nur innerhalb des gleichen Pakets (ebenfalls später) |

In **Level 2** konzentrieren wir uns auf **`public`** und **`private`** – das sind die beiden wichtigsten für den Anfang.

---

### 🛡️ **`private`: Mein Geheimnis bleibt mein Geheimnis**

Wenn du ein Feld oder eine Methode als `private` deklarierst,  
ist es **nur innerhalb der eigenen Klasse sichtbar**.

Beispiel:
```java
public class Monster {
    private int lebensPunkte;

    public Monster(int lebensPunkte) {
        this.lebensPunkte = lebensPunkte;
    }

    private void regenerieren() {
        lebensPunkte += 10;
        System.out.println("Das Monster heilt sich heimlich...");
    }
}
```

Hier kann **nur die Klasse selbst** die Methode `regenerieren()` aufrufen.

---

### ⚔️ **`public`: Willkommen, komm rein!**

`public` macht ein Feld oder eine Methode für **alle anderen Klassen** zugänglich:

```java
public void anzeigen() {
    System.out.println("Lebenspunkte: " + lebensPunkte);
}
```

> 💡 Das ist dein **offizieller Zugang** für andere Teile deines Programms.

---

### 🧭 **Kombination mit Gettern und Settern**

Das ist auch der Grund, warum Felder meist **`private`** sind  
– aber die **Getter und Setter `public`**:

```java
public int getLebensPunkte() {
    return lebensPunkte;
}

public void setLebensPunkte(int lebensPunkte) {
    if (lebensPunkte >= 0) {
        this.lebensPunkte = lebensPunkte;
    }
}
```

> 🛡️ **Deine Daten sind geschützt, aber kontrolliert zugänglich.**

---

## 🧪 **Warum überhaupt schützen?**

Weil du so **Fehler vermeidest und Kontrolle behältst**.

⚠️ Stell dir vor:
```java
vampir.lebensPunkte = -5000;
```

Wenn `lebensPunkte` einfach `public` wäre, könnte jeder das tun – auch aus Versehen.  
Mit `private` + `Setter` kannst du das verhindern.

---

## 🏆 **Deine XP-Quest:**

1. Erstelle eine Klasse `HexerInventar` mit:
   - einem privaten `int`-Feld `anzahlTraenke`,
   - einem `public`-Getter für die Anzahl,
   - einem `public`-Setter, der verhindert, dass die Anzahl negativ wird.

2. Baue eine Methode `zeigeInventar()`, die den aktuellen Stand ausgibt.

💥 **Bonus-XP:**  
Füge ein privates Feld `geheimeFormel` (vom Typ `String`) hinzu.  
Schreibe eine private Methode `zeigeFormel()`, die nur innerhalb der Klasse selbst benutzt werden darf.

---

> 🛡️ **+100 XP für sicheres Öffnen und Schließen gesammelt!**  
> **Nächstes Ziel:** Nutze `extends` für Vererbung – baue Monsterfamilien und Hierarchien.

---

# 🧬 **2.6 Nutze `extends` für Vererbung – baue Monsterfamilien**

> *„Ein Ghul ist ein Monster. Ein Vampir ist ein Monster. Aber nicht jedes Monster ist ein Ghul.“*  
>  
> In Java kannst du solche **„Ist-ein“-Beziehungen** direkt im Code abbilden:  
> Das nennt man **Vererbung**.

---

## 🏰 **Was bedeutet Vererbung in Java?**

Du kannst eine neue Klasse erschaffen, die von einer bestehenden Klasse **erbt** – und damit alles übernimmt, was die Elternklasse (die sogenannte **Superklasse**) schon hat.

Das Schlüsselwort dafür: `extends`.

---

### 🐺 **Beispiel: Eine Monster-Basis-Klasse**

```java
public class Monster {
    private String name;
    private int lebensPunkte;

    public Monster(String name, int lebensPunkte) {
        this.name = name;
        this.lebensPunkte = lebensPunkte;
    }

    public void angreifen() {
        System.out.println(name + " greift an!");
    }

    public String getName() {
        return name;
    }

    public int getLebensPunkte() {
        return lebensPunkte;
    }
}
```

---

### 🩸 **Ein Ghul ist auch nur ein Monster: `extends Monster`**

```java
public class Ghul extends Monster {

    public Ghul() {
        super("Ghul", 80);  // ruft den Constructor der Elternklasse auf
    }

    public void schreien() {
        System.out.println("Der Ghul schreit wild!");
    }
}
```

---

### 🧪 **Was passiert hier genau?**
- Die Klasse `Ghul` **erbt** alle Felder und Methoden von `Monster`.  
- Das heißt, `Ghul` hat automatisch:
  - den Namen,
  - die Lebenspunkte,
  - die Methode `angreifen()`  
- **Zusätzlich** hat der Ghul seine eigene Methode `schreien()`.

---

### ⚔️ **Objekte aus Kindklassen erzeugen:**

```java
Ghul ghul = new Ghul();
ghul.angreifen();   // von Monster geerbt
ghul.schreien();    // eigene Methode
```

> Ausgabe:
```
Ghul greift an!
Der Ghul schreit wild!
```

---

## 🌑 **Weitere Kinder: Vampir, Wyvern, Nekker…**

```java
public class Vampir extends Monster {
    public Vampir() {
        super("Vampir", 120);
    }

    public void saugeBlut() {
        System.out.println("Der Vampir saugt Blut...");
    }
}
```

---

## 🎯 **Warum Vererbung nutzen?**

> 💡 **Vorteil:**  
> Gemeinsamkeiten schreibst du **einmal** in die Elternklasse.  
> Die Kindklassen bekommen alles automatisch – und können **eigenes Verhalten hinzufügen**.

Ohne Vererbung müsstest du z. B. die Methode `angreifen()` immer wieder neu schreiben.  
Mit Vererbung: **Einmal gebaut, überall nutzbar.**

---

## 🏆 **Deine XP-Quest:**

1. Baue eine Elternklasse `Monster` mit:
   - `name` und `lebensPunkte`,
   - einer Methode `angreifen()`.

2. Erstelle mindestens zwei Kindklassen (`Ghul`, `Vampir`) mit:
   - eigenem Constructor (nutze `super()`),
   - je einer zusätzlichen Spezialmethode.

---

> 🛡️ **+150 XP für Blutlinien und Vererbung gesammelt!**  
> **Nächstes Ziel:** Überschreibe Methoden. Respektiere `super`.

---

# 🌀 **2.7 Überschreibe Methoden. Respektiere `super`.**

> *„Der Vampir greift anders an als der Ghul. Aber beide wissen, wie ein Angriff grundsätzlich funktioniert.“*  
>  
> Manchmal reicht das, was die Elternklasse vorgibt, einfach nicht aus. Vielleicht soll ein Monster aggressiver angreifen. Oder es soll zusätzlich eine Spezialfähigkeit einsetzen.

In Java kannst du das **vererbte Verhalten verändern** – und dabei trotzdem auf das Wissen der Eltern zurückgreifen.  
Das nennt man **Methoden überschreiben** (engl. *Override*).

---

## ⚔️ **Was bedeutet „Methode überschreiben“?**

> Überschreiben = Eine Methode aus der Elternklasse durch eine eigene Version in der Kindklasse ersetzen.

Wenn die Eltern sagen:
```java
public void angreifen() {
    System.out.println(name + " greift an!");
}
```

…kann das Kind sagen:
```java
@Override
public void angreifen() {
    System.out.println(getName() + " setzt einen Blutbiss ein!");
}
```

Das passiert, **ohne dass du die Elternklasse ändern musst**.  
Die Eltern geben den Standard vor – das Kind darf es anpassen.

---

## 🧩 **Warum `@Override`?**

Das `@Override`-Annotation ist wie ein Ehrenzeichen:  
Es sagt dem Compiler (und auch dir selbst):  
„Diese Methode ist absichtlich überschrieben.“

Wenn du dich vertippst, zum Beispiel:
```java
public void Angreifen() { ... } // falsches großes A!
```
…würde das **ohne `@Override`** einfach eine neue Methode sein,  
aber **nicht die alte überschreiben**.

Mit `@Override` würde der Compiler sagen:  
„Hey, das war wohl nicht so gemeint!“ – und dir einen Fehler anzeigen.

---

## 🛡️ **`super` – Der Ehrenkodex gegenüber den Eltern**

> *„Auch wenn ich es anders mache – ich vergesse nicht, was meine Vorfahren mir beigebracht haben.“*

Wenn du das Verhalten der Eltern **nicht komplett ersetzen**,  
sondern **ergänzen** willst, nutzt du `super`:

```java
@Override
public void angreifen() {
    super.angreifen();  // Erst die Standardaktion der Eltern…
    System.out.println(getName() + " nutzt zusätzlich seinen Blutzauber!");
}
```

---

## 🧪 **Beispiel in voller Schönheit:**

```java
public class Monster {
    private String name;
    private int lebensPunkte;

    public Monster(String name, int lebensPunkte) {
        this.name = name;
        this.lebensPunkte = lebensPunkte;
    }

    public void angreifen() {
        System.out.println(name + " greift an!");
    }

    public String getName() {
        return name;
    }
}
```

```java
public class Vampir extends Monster {
    public Vampir() {
        super("Vampir", 120);
    }

    @Override
    public void angreifen() {
        super.angreifen();  // Respektiere die Eltern!
        System.out.println("…doch der Vampir setzt einen tödlichen Biss ein!");
    }
}
```

---

## 🧭 **Einsetzen und testen:**

```java
public class Main {
    public static void main(String[] args) {
        Monster ghul = new Monster("Ghul", 80);
        Vampir vampir = new Vampir();

        ghul.angreifen();
        vampir.angreifen();
    }
}
```

> Ausgabe:
```
Ghul greift an!
Vampir greift an!
…doch der Vampir setzt einen tödlichen Biss ein!
```

---

## 💎 **Wann solltest du `super` nutzen?**

- Wenn du **das Verhalten erweitern** willst, aber nicht alles selbst neu schreiben möchtest.
- Wenn die Elternklasse etwas tut, das **immer passieren soll**,  
  aber dein Kind danach **etwas Zusätzliches** tun muss.

---

## 🏆 **Deine XP-Quest:**

1. Baue die Klasse `Monster` mit einer Methode `angreifen()`.  
2. Erstelle die Kindklassen `Ghul` und `Vampir`:  
   - Beide sollen die Methode `angreifen()` **überschreiben**.  
   - Der `Ghul` soll einfach nur `"Der Ghul schlägt wild um sich!"` ausgeben.  
   - Der `Vampir` soll zuerst das Standardverhalten der Eltern aufrufen (mit `super.angreifen()`) und danach `"…doch der Vampir setzt einen tödlichen Biss ein!"` ergänzen.

💥 **Bonus-XP:**  
Baue zusätzlich eine Methode `spezialAktion()`, die nur in der Kindklasse existiert (z. B. `saugeBlut()` beim Vampir oder `schreien()` beim Ghul).


> 🛡️ **+150 XP für mächtige Vererbung und Respekt vor den Eltern gesammelt!**  
> **Damit ist Level 2 abgeschlossen! 🎉**  
>  
> Bist du bereit, in **Level 3: Baue dein Arsenal auf** aufzusteigen?

---

<p align="center">
<a href="/docs/06-entwicklung/05-java/01-tutorial/01-theorie/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/03-theorie/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/05-java/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zum Inhaltsverzeichis</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>