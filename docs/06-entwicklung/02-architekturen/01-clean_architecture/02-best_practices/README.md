# Best Practices und Tipps für Einsteiger

Für eine gelungene – also möglichst reibungslose – Umsetzung von Clean Architecture in einem Softwareprojekt, haben sich, insbesondere für Einsteiger, einige bewährte Praktiken und Tipps als extrem hilfreich erwiesen. Hier sind die wichtigsten Empfehlungen, die du bei der Anwendung beachten solltest:

---

### 1. Geschäftslogik zuerst: 
Konzentriere dich zunächst auf die Domäne und Use Cases, ohne von Anfang an in technischen Details zu denken. Clean Architecture erlaubt es, Entscheidungen über Datenbanken, Frameworks oder Bibliotheken auf einen späteren Zeitpunkt zu verschieben – nutze das aus, indem du **erst die Kernlogik sauber implementierst**. Technische Details kannst du dann später Schritt für Schritt hinzufügen.

---

### 2. Klare Schichtentrennung einhalten: 
Achte strikt darauf, **dass innere Schichten nichts von äußeren wissen**. Formuliere Schnittstellen für die Kommunikation zwischen den Schichten und halte dich an diese Verträge. Zum Beispiel kennt der Use Case nur das Interface TimeEntryRepository, aber nicht die konkrete Datenbankimplementierung. Diese Disziplin verbessert die Wartbarkeit und macht den Code unabhängig von Frameworks.

---

### 3. Dependency Injection nutzen: 
Um konkrete Implementierungen bereitzustellen, verwende Dependency Injection (wie im Beispiel via Konstruktoren gezeigt). Dadurch kannst du z.B. in Tests einen einfachen In-Memory-Adapter verwenden und in der Produktion eine echte Datenbank – **ohne den Use-Case-Code zu ändern**.

---

### 4. Kleine, fokussierte Klassen: 
Stelle sicher, dass jede Klasse eine klar umrissene Verantwortung hat (**Single Responsibility Principle**). Entitäten modellieren Fachkonzepte, Use Cases kapseln Anwendungslogik, Controller/Presenter bereiten Ein- und Ausgabe auf. **Vermische** diese **Zuständigkeiten nicht**.

---

### 5. Umfassend testen: 
Ein großer Vorteil von Clean Architecture ist die Testbarkeit. Nutze das, indem du die Kernlogik (Use Cases und Entities) mit **Unit-Tests** versiehst. Da diese **keinerlei Abhängigkeiten auf externe Systeme** haben, lassen sie sich sehr einfach und schnell testen. So stellst du sicher, dass die Geschäftsregeln korrekt funktionieren – unabhängig von UI oder Datenbank.

---

### 6. Schrittweise erweitern: 
Beginne mit einer **einfachen vertikalen Scheibe** deiner Anwendung – so wie wir es mit dem Use Case „Zeit erfassen“ demonstriert haben. Hast du diese zum Laufen gebracht, kannst du **iterativ** weitere Use Cases, Entities oder Adapter hinzufügen. Das schrittweise Vorgehen hilft, die **Struktur konsequent einzuhalten**, ohne von der Komplexität überwältigt zu werden.

---

### 7. Lesbare Architektur („Screaming Architecture“): 
**Benenne** Pakete, Ordner und Klassen **nach der Domäne**, nicht nach technischen Mustern. Zum Beispiel ist timeentry/ als Ordner mit Klassen wie TimeEntry oder TimeEntryRepository **selbsterklärender** als ein generisches data/ oder util/. Die oberste Projektstruktur sollte direkt erkennen lassen, worum es fachlich geht (sie soll förmlich schreien, was die Anwendung macht). So findet sich auch Team im Falle eines gemeinsamen Projekts besser zurecht und neue Entwickler verstehen schneller den Zweck des Systems.

---

### 8. Keine Überanpassung an ein Framework: 
Vermeide es, Code eines bestimmten Frameworks in deine Kernlogik einfließen zu lassen. **Halte framework-spezifische Details in der Framework-Schicht**. Wenn du z.B. ein Web-Framework nutzt, platziere dessen Annotationen und spezielle Typen nur in den Controller/Adapter-Klassen, nicht in deine Use Cases oder Entities. Dadurch bleibt dir die Flexibilität, das UI- oder DB-Framework bei Bedarf auszutauschen, ohne auch den Kern des Systems anpassen zu müssen.

---

Mit diesen Tipps sowie dem vorangehenden Leitfaden sollten du bzw. du und dein Entwicklungsteam auch ohne Vorerfahrung in der Lage sein, die Entwicklung einer ersten einfachen Anwendung nach Clean Architecture umzusetzen. Wichtig ist, die Trennung der Schichten konsequent umzusetzen – so werden die Vorteile Wartbarkeit, Testbarkeit und Flexibilität Schritt für Schritt erfahrbar. Viel Erfolg beim Ausprobieren!

---

## Fazit

Die Clean Architecture ist ein bewährtes Muster, um Softwareprojekte strukturiert und wartbar zu gestalten. Durch die Trennung von Domäne, Anwendungslogik und Infrastruktur wird die Flexibilität erhöht und die Testbarkeit verbessert. In diesem Beispiel haben wir eine einfache Zeiterfassungsanwendung Schritt für Schritt aufgebaut und dabei die Prinzipien der Clean Architecture angewendet. Mit den vorgestellten Best Practices und Tipps können auch Einsteiger in der Softwareentwicklung erfolgreich mit Clean Architecture arbeiten.

---


## Weiterführende Links

ℹ️ [Clean Architecture Buch von Robert C. Martin](https://www.oreilly.com/library/view/clean-architecture-a/9780134494272/) <br>
ℹ️ [Robert C. Martin auf Wikipedia](https://en.wikipedia.org/wiki/Robert_C._Martin)

---

<p align="center">
<a href="/docs/06-entwicklung/02-clean_architecture/01-praxisbeispiel/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/03-lizenzen_und_opensource/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/02-architekturen/01-clean_architecture/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>