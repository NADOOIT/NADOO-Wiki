# <p align="center">Architekturstile in der Anwendungsentwicklung</p>
<p align="center"><a href="#dieses-thema-beinhaltet-folgende-kapitel">🚀 Direkt zur Kapitel-Übersicht</a></p>

Jedes System ist ein Zusammenspiel aus einer Reihe von Komponenten. Ein gutes Beispiel, um diesen Grundsatz visuell zu verinnerlichen, ist ein Haus, denn dieses setzt sich – stark vereinfacht – aus den folgenden Komponenten zusammen: Fundament, Wände, Böden, Dach. Genau dasselbe Prinzip wird auch im Kontext von IT-Systemen und -Anwendungen angewandt. Wenn neue Software enwickelt wird, wird diese auf Basis sogenannter Architekturstile nach einer festen Struktur aufgebaut. 

Da IT-Anwendungen aber keine Häuser sind, stellt sich hier nun natürlich die Frage: **Welche Komponenten sind für Software relevant?** Die Antwort darauf ist leider nicht ganz so simpel wie bei einem Haus, denn im Gegensatz zu physischen Strukturen sind die Komponenten von Software abstrakt und variieren je nach Zielsetzung des Projekts, wie z.B. Benutzerinteraktion oder Datenverarbeitung. Allgemein lässt sich aber sagen, dass typischerweise die folgenden Elemente eine entscheidende Rolle spielen:

### 📲 Präsentationsschicht (Benutzeroberfläche):

Diese Komponente ist für die **Interaktion mit dem Benutzer** zuständig, z.B. durch grafische Oberflächen, Webseiten oder Eingabeformulare. 
Sie stellt also die **Schnittstelle zwischen Nutzer und System** dar und ist folglich essentiell für die Benutzerfreundlichkeit einer Anwendung.

➡️ **Beispiel:** Ein Web-Frontend mit HTML/CSS/JavaScript oder eine Desktop-App mit Java/JavaFX.

---

### 🛠️ Anwendungslogik (Geschäftslogik):

Diese Komponente enthält die **Kernfunktionen der Software**, also die **Regeln und Prozesse**, die das System ausführt (z.B. Berechnungen, Datenverarbeitung). Sie definiert, _**was** die Software **tut**_, und arbeitet häufig unabhängig vom Benutzer-Interface (UI) und/oder der Datenbank.

➡️ **Beispiel:** Logik zum Erstellen eines Projekts, Validierung von Eingaben oder Zuweisung von Teammitgliedern.

---

### 💾 Datenspeicherung (Datenbank):

Diese Komponente **verwaltet die Speicherung, Abfrage und Aktualisierung von Daten**, z.B. in relationalen Datenbanken, NoSQL oder Dateisystemen.
Sie stellt sicher, dass Daten **dauerhaft** gespeichert und **verfügbar** sind.

➡️ **Beispiel:** Eine MySQL-Datenbank, die Projektdaten speichert oder ein Dateisystem für Konfigurationsdaten.

---

### 🔗 Schnittstellen (APIs oder Kommunikationsschicht):

Diese Komponente ermöglicht die **Kommunikation zwischen verschiedenen Teilen des Systems** oder mit **externen Systemen**, z.B. über REST-APIs, GraphQL oder Message Queues. Sie ermöglicht **Modularität** (Zerlegung komplexer Software in unabhängige, wiederverwendbare Komponenten) sowie die **Verbindung** mit anderen Systemen.

➡️ **Beispiel:** Eine REST-API, die Daten zwischen Frontend und Backend austauscht oder ein Webhook zu einem externen Tool.

---

## Die Bedeutung von Software-Architekturen

Maßgeblich lässt sich also sagen, dass Softwarearchitekturen die grundlegenden Strukturen eines Softwaresystems definieren, Schnittstellen zwischen den verschiedenen Komponenten beschreiben sowie Prinzipien für das Design und die Evolution des Systems festlegen. Eine gut durchdachte Architektur bietet die folgenden Vorteile:

✅ **Verbesserte Wartbarkeit:** Klare Strukturen erleichtern Anpassungen und Erweiterungen, ohne dass der gesamte Code überarbeitet werden muss. <br>
✅ **Skalierbarkeit:** Eine flexible Architektur ermöglicht es, das System intuitiv zu erweitern – sei es durch mehr Benutzer oder zusätzliche Funktionen. <br>
✅ **Zuverlässigkeit:** Eine solide Architektur minimiert die Ausfallzeiten und verbessert die Systemstabilität. <br>

Auf lange Sicht betrachtet, ergeben sich aus der Architektur-gestützten Entwicklung heraus folglich weitere wertvolle Nutzen, darunter:

💰 **Kosteneffizienz:** Durch die Reduktion von Komplexität und die Verbesserung der Wiederverwendbarkeit von Komponenten werden Entwicklungs- und Wartungskosten optimiert.

💬 **Teamübergreifende Kommunikation:** Eine einheitliche Architektur fördert die Zusammenarbeit zwischen verschiedenen Teams, da alle Beteiligten ein gemeinsames Verständnis von der Struktur und den Abläufen haben.

💎 **Qualitätsverbesserung:** Durch die Einhaltung von Architekturstandards werden Qualitätskriterien besser erfüllt, was sich positiv auf die Benutzererfahrung auswirkt.

🤸‍♂️ **Technologische Flexibilität:** Eine durchdachte Architektur ermöglicht es, verschiedene Technologien zu kombinieren und schneller auf Änderungen in den Marktanforderungen zu reagieren.

---

## Welche Arten von Architekturstilen gibt es in der Softwareentwicklung?

Wie in der schnellebigen und dynamischen Welt der IT üblich, existiert eine große Auswahl unterchiedlicher Architekturstile, an welcher sich Entwickler bedienen können, um unterschiedliche Anforderungen und Herausforderungen zu adressieren. Hier ist eine kurze Übersicht einiger bekannter Typen:
<br>

### Die Monolithische Architektur

Prinzip: Die gesamte Anwendung ist als eine einzige, große Einheit aufgebaut. Es existiert also genau ein Anwendungs-Stack, der alle benötigten Funktionen innerhalb dieser einen Anwendung umfasst. 

Vorteile: Einfach zu entwickeln und zu warten für kleinere Projekte, da alle Komponenten gemeinsam "in einer Schublade" liegen. 

Nachteile: Das Aktualisieren oder Skalieren einzelner Aspekte einer monolithischen Anwendung hat Auswirkungen auf das gesamte System und dessen zugrunde liegenden Infrastruktur, was wenig Flexibilität und eine erschwerte Wartbarkeit zur Folge hat. Diese Methode gilt heutzutage daher eher als veraltet.

---

### Die Microservices-Architektur

**Prinzip:** Eine Anwendung wird in viele kleine, unabhängige Dienste zerlegt, die jeweils eine bestimmte Geschäftsfunktion erfüllen und über APIs kommunizieren.

**Vorteile:** Fördert Skalierbarkeit, Widerstandsfähigkeit und Flexibilität. 

**Nachteile:** Kann komplexer zu verwalten und zu koordinieren sein. 

---

### Die Client-Server-Architektur

**Prinzip:** Clients (z.B. Webbrowser) fordern Dienste von einem zentralen Server an, der die Ressourcen bereitstellt.

**Vorteile:** Ermöglicht den Austauschbarkeit von Komponenten und eine zentrale Datenverwaltung. 

---

### Die Ereignisgesteuerte Architektur (Event-Driven Architecture / EDA)

**Prinzip:** Komponenten kommunizieren und lösen Aktionen basierend auf dem Auftreten von Ereignissen aus. Ereignisse können hier sowohl durch interne als auch externe Eingaben verursacht werden können. 

**Vorteile:** Fördert eine flexible und reaktionsschnelle Systemintegration. 

---

### Die Layered-Architektur

**Prinzip:** Die Anwendungslogik ist in verschiedene Schichten aufgeteilt, z.B. eine Präsentationsschicht, eine Geschäftslogikschicht und eine Datenschicht.

**Vorteile:** Verbessert die Modularität und Wartbarkeit, da Änderungen in einer Schicht die anderen Schichten möglichst wenig beeinflussen sollten. 

---

### Das Model-View-Controller-Modell (MVC): 

**Prinzip:** Trennt Daten (Model), Benutzeroberfläche (View) und Anwendungslogik (Controller) für eine bessere Strukturierung von Anwendungen. Frontend- und Backend-Teile des Quellcodes werden also in unterschiedliche Komponenten unterteilt.

**Vorteile:** Erleichtert die Handhabung des gesamten Codes und macht es einfacher, einzelne Teile der Lösung (Backend und Frontend) separat voneinander anzupassen.

---

## Fazit

Wie du siehst, ist das Thema Architekturstile ziemlich umfangreich. Die Wahl des richtigen Stils hängt stark von den spezifischen Anforderungen, der Komplexität und den Zielen des jeweiligen Projekts ab. Es ist wichtig, die Vor- und Nachteile jedes Stils sorgfältig abzuwägen und zu verstehen, wie sie sich auf die Entwicklung, Wartung und Skalierbarkeit der Software auswirken können. Damit du dir ein besseres Bild davon machen kannst, wie die Anwendung von Architekturen konkret in der Praxis aussehen kann, gehen wir in den nächsten Kapiteln tiefer auf ein paar ausgewählte Beispiele ein.

---

#### Quellen

[1] https://conport.de/die-bedeutung-von-softwarearchitektur-in-der-modernen-softwareentwicklung/ <br>
[2] https://www.redhat.com/de/topics/cloud-native-apps/what-is-an-application-architecture#schichten--oder-n-tier-architektur <br>
[3] https://innowise.com/de/blog/best-software-architecture-patterns/ <br>

---

### <p align="center">Dieses Thema beinhaltet folgende Kapitel:</p>

---

 🔹 [**Clean Architecture**](/docs/06-entwicklung/02-architekturen/01-clean_architecture/README.md) </br>

---

<p align="center">
<a href="/docs/06-entwicklung/01-dokumentation/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/02-architekturen/01-clean_architecture/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/README.md/#dieser-themenbereich-beinhaltet-folgende-themen"><strong>Zurück zur Themen-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>