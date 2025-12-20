# 🧙‍♂️ **LEVEL 1: Meistere die Grundlagen**

> *Bevor du die großen Monster jagst, musst du dein Schwert führen können.  
> Bevor du mächtige Zauber webst, musst du die Runen kennen.*  
>  
> **Willkommen in deinem Trainingslager, Rekrut.**  
> Hier lernst du die Basics. Die Dinge, die jeder Hexer beherrschen muss, bevor er sich hinaus in die Welt des Codes wagt.

---

## 🧪 **1.1 Variablen deklarieren und nutzen – Dein Inventar befüllen**

Stell dir vor, du bist unterwegs in den Sümpfen von Velen. Deine Taschen sind voll mit Tränken, Bomben und seltsamen Kräutern. Aber wie viele Tränke hast du noch? Und ist dein Schild-Zauber eigentlich aktiv?

In deinem Kopf weißt du das vielleicht – aber dein Code weiß es nicht, solange du es ihm nicht sagst.

### 🧰 Variablen: Die Inventar-Slots deines Codes

Eine **Variable** ist nichts anderes als ein Speicherplatz. Ein Slot in deinem Inventar, dem du einen Namen gibst und in den du genau sagst, was hineingehört. So wie „3 Blitz-Bomben“ oder „Schild aktiv: ja“.

In Java sagst du das so:
```java
int anzahlTraenke = 3;
String charakterName = "Geralt";
boolean schildAktiv = true;
```

Was passiert hier?
- Du **wählst den Typ** der Information (z. B. `int` für ganze Zahlen).
- Du **gibst dem Slot einen Namen** (z. B. `anzahlTraenke`).
- Du **füllst den Slot mit einem Wert** (`3`).

---

### 🌱 **Primitive Datentypen – Die Alchemie des Codes**

In Java gibt es acht **primitive Datentypen**. Sie heißen so, weil sie die einfachsten Bausteine der Sprache sind – klein, schnell, direkt auf die Maschine übertragbar. Keine unnötigen Umwege, keine große Magie.

| Typ        | Bedeutung                        | Beispiel                    |
|------------|-----------------------------------|----------------------------|
| `int`      | Ganze Zahl (z. B. Trankanzahl)    | `int anzahlTraenke = 3;`    |
| `double`   | Kommazahl (z. B. Goldmenge)       | `double hexerGold = 1250.75;` |
| `boolean`  | Wahr oder falsch (z. B. Schild aktiv) | `boolean schildAktiv = true;` |
| `char`     | Einzelnes Zeichen (z. B. Runen-Symbol) | `char runensymbol = 'R';`  |
| `byte`     | Kleine ganze Zahl (−128 bis 127)  | `byte kleineZahl = 100;`    |
| `short`    | Etwas größere ganze Zahl          | `short klingenanzahl = 1200;` |
| `long`     | Sehr große ganze Zahl             | `long monsterZaehler = 999999L;` |
| `float`    | Weniger präzise Kommazahl als `double` | `float trankStaerke = 12.5f;` |

> 🧙‍♂️ **Warum gibt es so viele Zahlen-Typen?**
> Weil Speicher kostbar ist, mein junger Hexer. Wenn du nur 5 Tränke hast, brauchst du keinen Speicherplatz für eine Monsterzahl wie 2 Milliarden. Das spart Zeit und Platz – und in manchen Situationen (z. B. bei großen Programmen) macht das einen echten Unterschied.

---

### 🧵 **`String`: Der Zauberspruch unter den Datentypen**

Jetzt kommt ein Sonderfall: der `String`. Damit speicherst du Texte – also etwa den Namen deines Charakters oder einen fiesen Fluch.

```java
String charakterName = "Geralt";
```

Technisch gesehen ist `String` **kein primitiver Datentyp**, sondern eine **Klasse** (mehr dazu später im Objektzauberei-Level). Aber weil Texte so grundlegend sind, benutzen wir sie schon jetzt.

---

### 🎯 **Deine erste XP-Quest:**

Erstelle Variablen für:
- Die Anzahl deiner Bomben (`int`)
- Den Namen deines Pferdes (`String`)
- Ob dein Schild aktiv ist (`boolean`)

Schreibe eine Ausgabe wie:
```java
System.out.println(pferdename + " steht bereit mit " + anzahlBomben + " Bomben.");
```

💥 **Bonus-XP:**  
Füge dein aktuelles Gold (`double`) hinzu und erweitere die Ausgabe.

---

> 🛡️ **+50 XP gesammelt!**  
> Auf zur nächsten Übung: **Operatoren meistern!**

---

## 🗡️ **1.2 Operatoren meistern – Dein Schwert schärfen**

> *Ein stumpfes Schwert schneidet keinen Greifen.*  
> Im Code sind **Operatoren** deine Klinge – damit rechnest du, vergleichst du, verknüpfst du Dinge.

### 🧭 Rechnen wie ein Hexer

Die klassischen **Rechenoperatoren**:
```java
+   // Addition
-   // Subtraktion
*   // Multiplikation
/   // Division
%   // Modulo (Rest einer Division)
```

> ⚔️ Beispiel:
> ```java
> int monsterKills = 7;
> int goldProKill = 25;
> int gesamtGold = monsterKills * goldProKill;
> System.out.println("Du hast " + gesamtGold + " Gold verdient.");
> ```
> Ausgabe:
> ```
> Du hast 175 Gold verdient.
> ```

---

### 🧿 Vergleichen – Ist das Monster noch am Leben?

Vergleichsoperatoren:
```java
==   // Gleich
!=   // Ungleich
>    // Größer als
<    // Kleiner als
>=   // Größer oder gleich
<=   // Kleiner oder gleich
```

> Beispiel:
> ```java
> int lebenMonster = 0;
> if (lebenMonster == 0) {
>     System.out.println("Das Monster ist besiegt.");
> }
> ```

---

💥 **+50 XP gesammelt!**  
**Nächstes Ziel:** Kontrollstrukturen meistern.

---

## 🧭 **1.3 Kontrollstrukturen – Entscheiden wie ein Hexer**

> *Ein Hexer ist kein stumpfer Schläger. Er beobachtet, wägt ab, entscheidet.*  
> So auch dein Code: Er muss oft prüfen, was gerade los ist – und darauf reagieren.  
>  
> „Wenn das Monster tot ist, dann feiere. Wenn nicht, dann greife an.“  
>  
> Willkommen bei den **Kontrollstrukturen**.

---

### ⚖️ **`if`, `else` – Dein Entscheidungsbaum**

Die einfachste Entscheidung in Java ist das klassische **Wenn-Dann**:

```java
if (bedingung) {
    // Tu etwas, wenn die Bedingung wahr ist
} else {
    // Tu etwas anderes, wenn die Bedingung falsch ist
}
```

> Beispiel:
```java
int lebenMonster = 0;

if (lebenMonster == 0) {
    System.out.println("Das Monster ist besiegt.");
} else {
    System.out.println("Das Monster lebt noch! Angriff!");
}
```

### ⚡ XP-Quest: Berechne das Gesamteinkommen deines Hexers aus Monsterjagden und prüfe, ob das Gold für einen neuen Satz Bomben reicht (jede Bombe kostet 30 Gold).

> 💡 **Wichtig:**  
> Die Bedingung in den runden Klammern (`lebenMonster == 0`) muss ein **`boolean`** sein – also etwas, das entweder `true` oder `false` ergibt. Vergleiche (`==`, `!=`, `>`, `<`, …) liefern genau solche Wahrheitswerte.

---

### 🌀 **Mehrere Möglichkeiten: `if`, `else if`, `else`**

Manchmal gibt es mehr als nur „ja“ oder „nein“. Vielleicht willst du je nach Monsterart unterschiedlich reagieren:

```java
String monsterArt = "Ghul";

if (monsterArt.equals("Vampir")) {
    System.out.println("Setze den Igni-Zauber ein!");
} else if (monsterArt.equals("Ghul")) {
    System.out.println("Nutze das Silberschwert.");
} else {
    System.out.println("Greife mit normaler Klinge an.");
}
```

> 🧙‍♂️ **Achtung:**  
> Bei `String`-Vergleichen nutzt man `.equals()` statt `==`.  
> Warum? Weil `==` prüft, ob zwei Dinge dieselbe Stelle im Speicher belegen, nicht ob die Texte inhaltlich gleich sind.

---

### 🧭 **`switch`: Der Code-Schalter**

Wenn es viele Fälle gibt, wird `if` schnell unübersichtlich. Dafür gibt es den **`switch`-Block**:

```java
String monsterArt = "Ghul";

switch (monsterArt) {
    case "Vampir":
        System.out.println("Feuerzauber wirkt am besten.");
        break;
    case "Ghul":
        System.out.println("Silberschwert bereithalten.");
        break;
    default:
        System.out.println("Normale Klinge verwenden.");
}
```

> 🔥 **Wichtig:**  
> Ohne das `break` würde der Code einfach alle folgenden Fälle durchlaufen – das nennt man „fall-through“. Das ist manchmal gewollt, oft aber ein Stolperstein.

---

## 🔁 **1.4 Schleifen – Wiederholung wie beim Training**

> *Kein Hexer wird Meister durch einen einzigen Schlag.*  
> Auch dein Code muss Dinge oft **wiederholen** – bis etwas geschafft ist.

---

### 🌀 **`for`-Schleife – Zähle, wiederhole, siege**

Die `for`-Schleife nutzt du, wenn du genau weißt, **wie oft** etwas wiederholt werden soll:

```java
for (int i = 0; i < 5; i++) {
    System.out.println("Übung Nummer: " + (i));
}
```

> 📌 Erklärung:  
> - `int i = 0`: Start bei 0  
> - `i < 5`: Solange `i` kleiner als 5 ist, weitermachen  
> - `i++`: Nach jedem Durchgang `i` um 1 erhöhen

Ergebnis:
```
Übung Nummer: 1  
Übung Nummer: 2  
Übung Nummer: 3  
Übung Nummer: 4  
Übung Nummer: 5  
```

---

### 🐺 **`while`-Schleife – Solange das Monster lebt…**

Wenn du **nicht genau weißt, wie oft** etwas passieren wird, benutzt du `while`:

```java
int lebenMonster = 5;

while (lebenMonster > 0) {
    System.out.println("Monster wird angegriffen!");
    lebenMonster--;
}
System.out.println("Monster besiegt!");
```

---

### 🧩 **`do-while` – Mindestens einmal zuschlagen**

Ein `do-while` läuft **mindestens einmal**, egal was passiert:

```java
int lebenMonster = 0;

do {
    System.out.println("Ein letzter Schlag!");
} while (lebenMonster > 0);
```

Auch wenn das Monster schon tot ist, wird der Schlag wenigstens einmal ausgeführt.

---

## 🛡️ **XP-Quest:**

1. Schreibe eine `for`-Schleife, die von 1 bis 10 zählt und jedes Mal ausgibt:  
   `"Schlag Nummer X gegen den Trainingsdummy!"`

2. Schreibe eine `while`-Schleife, die einen Monster-Lebensbalken von 100 runterzählt – immer 10 Schaden pro Runde.  
   Bei jedem Schlag: `"Das Monster hat noch X Lebenspunkte."`  
   Wenn tot: `"Das Monster ist besiegt!"`

💥 **Bonus-XP:**  
Erstelle eine `switch`-Struktur für verschiedene Tranktypen (`Heiltrank`, `Blitztrank`, `Katzenauge`) und schreibe die passenden Effekte in die Konsole.

---

> 🎉 **+100 XP für Entscheidungslogik und Wiederholung gesammelt!**  
> **Nächstes Ziel:** Arrays – dein erster Datenspeicher.

---

## 🧺 **1.5 Arrays – Dein erster Datenspeicher**

> *Ein einzelner Trank macht noch keinen Hexer aus.  
> Wer auf Monsterjagd geht, braucht Vorräte – am besten gut sortiert und griffbereit.*  
>  
> In Java heißt das: **Arrays**.

---

### 🧱 **Was ist ein Array?**

Ein **Array** ist wie eine Reihe von Inventarslots.  
Stell dir vor, du hast fünf Bomben, die du einzeln erreichen willst – z. B. `"Samum"`, `"Grapeshot"`, `"Dancing Star"`, `"Northern Wind"`, `"Devil's Puffball"`.

Natürlich könntest du fünf einzelne `String`-Variablen dafür anlegen:
```java
String bombe1 = "Samum";
String bombe2 = "Grapeshot";
String bombe3 = "Dancing Star";
// ...
```

Aber das ist umständlich. Viel eleganter:
```java
String[] bomben = { "Samum", "Grapeshot", "Dancing Star", "Northern Wind", "Devil's Puffball" };
```

Jetzt hast du **eine Variable**, die **mehrere Werte** enthält.

---

### 🗺️ **So funktioniert’s:**

- `String[]`: sagt, es ist ein Array von `String`-Elementen.
- `bomben`: der Name deines Vorratsbeutels.
- `{ ... }`: die einzelnen Bomben, fein säuberlich in Reihenfolge.

Du greifst auf einen bestimmten Slot über seine **Position (Index)** zu:
```java
System.out.println(bomben[0]);  // Gibt "Samum" aus
```

> 🧙‍♂️ **Achtung:**  
> Der Index beginnt bei **0**!  
> Das heißt:  
> - `bomben[0]` → erstes Element  
> - `bomben[1]` → zweites Element  
> - `bomben[4]` → fünftes Element

---

### 🏹 **Arrays mit Zahlen – Beispiel: Schadenswerte deiner Bomben**

```java
int[] schaden = { 50, 40, 70, 60, 80 };
System.out.println("Schaden von Grapeshot: " + schaden[1]);
```

> Ausgabe:
> ```
> Schaden von Grapeshot: 40
> ```

---

### 🛠️ **Arrays ohne direkte Befüllung (mit fixer Größe):**

Wenn du ein Array wie int[] oder String[] verwendest, musst du entweder direkt die Inhalte angeben oder zumindest die Größe des Arrays festlegen – du kannst es also nicht einfach ohne Länge oder Werte deklarieren. Wenn du also schon weißt, wie viele Plätze dein Beutel haben soll, aber noch nicht, was genau hineinkommt, gib die Größe an:
```java
int[] monsterLebenspunkte = new int[3];
monsterLebenspunkte[0] = 100;
monsterLebenspunkte[1] = 80;
monsterLebenspunkte[2] = 150;
```

---

### 🚀 **Arrays in der Schleife:**

Willst du alle Bombennamen auflisten?
```java
for (int i = 0; i < bomben.length; i++) {
    System.out.println("Bombe " + (i + 1) + ": " + bomben[i]);
}
```

> 💡 **`bomben.length`** gibt dir die **Anzahl der Elemente** im Array zurück.

---

### 🎯 **Deine XP-Quest:**

1. Lege ein Array aus 4 Monsternamen an (`"Ghul"`, `"Vampir"`, `"Wyvern"`, `"Ekimma"`).  
2. Schreibe eine Schleife, die jedes Monster mit seiner Nummer ausgibt:  
   `"Monster 1: Ghul"`, `"Monster 2: Vampir"`, etc.

💥 **Bonus-XP:**  
Erstelle ein Array mit den Lebenspunkten dieser Monster und gib für jedes Monster seinen Namen plus Lebenspunkte aus.

---

> 🛡️ **+100 XP für Arrays und Datenspeicher gesammelt!**  
> **Nächstes Ziel:** Schreib kleine Tools. Zerstöre sie. Bau sie besser.

---

### ✍️ **1.6 Scanner – Sprich, Hexer!**

> *„Ein Hexer, der nicht zuhört, wird vom ersten Ghul überrascht.  
> Ein Hexer, der seine Umgebung befragt – der überlebt.“*

In Java bedeutet das: **Mit dem Spieler reden**.  
Du willst Eingaben bekommen? Dann brauchst du den **`Scanner`**.

---

## 🔍 **Was ist der Scanner?**

Der `Scanner` ist dein **magischer Ohrenspiegel**:  
Er lauscht auf das, was der Spieler eintippt – und liefert es dir als `String`, `int`, `double` oder `boolean`.

Importiere ihn so:

```java
import java.util.Scanner;
```

Dann erstelle ihn:

```java
Scanner scanner = new Scanner(System.in);
```

---

## 🎤 **Der Scanner hört, was du tippst**

### Beispiel: Eine Frage stellen

```java
System.out.print("Wie heißt du, Hexer? ");
String name = scanner.nextLine();
System.out.println("Willkommen, " + name + "!");
```

> `nextLine()` holt eine ganze Zeile Text (inkl. Leerzeichen).

---

### 🧙‍♂️ Zahlen lesen

```java
System.out.print("Wie alt bist du, Hexer? ");
int alter = scanner.nextInt();
System.out.println("Alter bestätigt: " + alter);
```

> Für Zahlen nutzt du `nextInt()`, `nextDouble()`, `nextBoolean()` usw.

---

## ⚠️ **Scanner-Fallen**

- Methoden wie nextInt() oder nextDouble() lesen nur den Wert, nicht aber den abschließenden Zeilenumbruch (\n). Dieser bleibt im Puffer und wird von der nächsten nextLine() sofort verarbeitet – oft ohne weitere Benutzereingabe. Dies führt dazu, dass die zu befülende Variable noch vor der Benutzereingabe mit einem Zeilenumbruch befüllt wird und nicht mit der gewünschten Eingabe. 
  ```java
  int zahl = scanner.nextInt();
  scanner.nextLine(); // Leert den Puffer, entfernt das '\n'

  String name = scanner.nextLine(); // Wartet korrekt auf Benutzereingabe
  ```
- Vergiss am Ende nicht:  
  ```java
  scanner.close();
  ```

---

## 🏆 **Deine XP-Quest:**

1. Frage den Benutzer nach:
   - seinem Hexernamen (`nextLine()`),
   - seiner Lieblingswaffe (`nextLine()`),
   - seinem aktuellen Level (`nextInt()`)

2. Gib die gesammelten Infos formatiert aus:
   ```
   Hexer Geralt kämpft mit Silberschwert auf Level 7.
   ```

💥 **Bonus-XP:**  
Füge eine zusätzliche Frage ein: „Bist du bereit für dein erstes Monster? (true/false)“ – lies die Antwort mit `nextBoolean()` und reagiere entsprechend.


> 🛡️ **+100 XP für Spielerinteraktion gesammelt!**  
> Mit dem Scanner kannst du nun mit der Welt sprechen – und die Welt spricht mit dir.

---

<p align="center">
<a href="/docs/06-entwicklung/05-java/01-tutorial/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/05-java/01-tutorial/02-theorie/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/05-java/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zum Inhaltsverzeichnis</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
