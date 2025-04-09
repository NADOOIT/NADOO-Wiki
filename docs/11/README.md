# 11. Das NADOO-IT Framework

Das **NADOO-IT Framework** ist ein Ansatz zur Strukturierung von Projekten und zur Organisation von Code. Es basiert auf den bewährten Prinzipien von Briefcase und Toga und kombiniert diese mit weiteren Technologien wie ZMQ und unserem eigens entwickelten NADOO-IT-Launchpad.

---

## Was ist ein Framework?

Ein Framework stellt eine vorgegebene Struktur für die Entwicklung von Applikationen dar. Diese Struktur erleichtert den Austausch von Code zwischen Projekten, die derselben Konvention folgen, und ermöglicht es Entwicklern, sich schneller in fremde Projekte einzuarbeiten.  
Dabei ist zu beachten:  

- **Lesbarkeit und Verständlichkeit:** Der Großteil der Entwicklungszeit fließt in das Lesen und Verstehen von Code.  
- **Einheitliche Struktur:** Ohne Vorgaben zur Organisation des Codes entwickelt jeder Entwickler seinen eigenen Stil. Dies führt zu einer Vielzahl unterschiedlicher „Styles“, die das Übernehmen von Code erschweren können.  
- **Erfahrungsschatz:** Erfahrene Entwickler greifen oft auf Frameworks zurück, weil diese eine konsistente Struktur und zahlreiche Funktionen bieten, die die Entwicklungsarbeit beschleunigen – sei es beim Erstellen neuer Features oder beim Einarbeiten neuer Teammitglieder.

**Beispiele für Frameworks in anderen Sprachen:**  

- **JavaScript:** Node.js, Vue, React, Angular  
- **Java:** SpringBoot  
- **Python:** Django, Flask, FastAPI  
- **PHP:** WordPress, Laravel, Symfony

Ein weiterer Vorteil von Frameworks liegt darin, dass sie viele Anfängerfehler verhindern – sie basieren auf den Erfahrungen von Entwicklern, die bereits komplexe Herausforderungen gelöst haben.

---

## Das NADOO Framework im Überblick

Das NADOO Framework verfolgt einen „Batteries-included“-Ansatz und setzt sich zusammen aus:

- **Briefcase:**  
  Erstellen von nativen Installationsdateien für Plattformen wie macOS, Windows, Linux, Android, iOS, Web und Terminal.

- **Toga:**  
  Gestaltung von nativen Interfaces, die den jeweiligen Plattform-Standards entsprechen.

- **ZMQ:**  
  Ermöglicht die Kommunikation zwischen verschiedenen Applikationen im Netzwerk oder über das Internet und stellt Schnittstellen zu den von ZMQ unterstützten Programmiersprachen bereit.

- **NADOO Launchpad:**  
  Ein zentrales Entwicklungsunterstützungsprogramm, das den Entwicklungsprozess überwacht, managt und unterstützt. Es hilft, die Einhaltung der Framework-Regeln sicherzustellen – etwa indem es fehlende Funktionen automatisch importiert oder beim Anlegen neuer Funktionen direkt die entsprechenden Dateien anlegt und benennt.

---

## Die zentrale Idee: „Eine Funktion = Eine Datei“

Im NADOO Framework gilt die Regel: **Eine Funktion entspricht einer Datei.**  
Statt mehrere Funktionen in einer einzelnen .py-Datei zu bündeln, wird hier strikt jede Funktion in einer eigenen Datei definiert – und die Datei trägt exakt den Namen der Funktion.

**Vorteile dieser Regel:**

1. **Transparenz:**  
   Abhängigkeiten werden über Imports und Parameter sofort erkennbar.

2. **Übersichtlichkeit:**  
   Es entsteht kein unübersichtlicher Monolith, in dem man zwischen tausend Zeilen Code hin- und herspringen muss.

3. **Eindeutige Benennung:**  
   Der Dateiname entspricht immer dem Funktionsnamen – doppelte Namensgebungen werden vermieden.

4. **Schneller Zugriff:**  
   Mit Funktionen wie „cmd+p“ oder „Strg+p“ lässt sich die gewünschte Datei sofort öffnen.

5. **Vereinfachte Importe:**  
   Durch die identische Struktur der Dateinamen sind Importe konsistent (z. B. `from .get_app_name import *`).

6. **KI-Unterstützung:**  
   Künstliche Intelligenz braucht weniger Kontext, wenn die Struktur klar und eindeutig ist – das verhindert, dass bestehende Funktionen neu definiert oder unnötig dupliziert werden.

7. **Modularität:**  
   Einzelne Funktionalitäten können einfach kopiert und in andere Projekte übernommen werden.

**Der Nachteil – Boilerplate:**  
Das Aufsplitten in viele Dateien führt zu einem Mehraufwand an Boilerplate-Code. Während Python traditionell wenig Vorarbeit benötigt, erfordert das NADOO Framework für jede Funktion das Anlegen einer eigenen Datei sowie das Einhalten fester Namens- und Ordnerstrukturen.  

Doch hier kommt das **NADOO Launchpad** ins Spiel:

---

## NADOO Launchpad – Ihr Entwicklungsassistent

**NADOO Launchpad** ist unser zentrales Tool, das den Entwicklungsprozess unterstützt und die Einhaltung der Framework-Regeln automatisch überwacht. Es übernimmt Aufgaben wie:

- Automatisches Importieren von Funktionen, wenn diese im Code verwendet werden.
- Erstellen neuer Dateien, wenn eine neue Funktion definiert wird – inklusive automatischer Anpassung des Dateinamens.
- Konsistente Strukturierung des Codes, sodass alle Teammitglieder (und auch KI-Systeme) sofort verstehen, wie die verschiedenen Teile miteinander zusammenhängen.

So wird sichergestellt, dass sich Entwickler – auch bei Projekten mit umfangreichem Code – schnell zurechtfinden und neue Features ohne großen Aufwand umsetzen können.

---

## Ordnerstruktur und Codeorganisation

Wer bereits mit Briefcase und Toga gearbeitet hat, kennt die vorgegebene Ordnerstruktur. Das NADOO Framework baut auf dieser Struktur auf, geht jedoch einen Schritt weiter:

- **Klare Trennung:**  
  Code ist nicht in einem großen, monolithischen Script versteckt, sondern jede Funktion ist als eigene Datei sichtbar.

- **Struktur statt Konvention:**  
  Viele Frameworks verstecken Funktionalität in speziellen Ordnern (z. B. Routen in Webframeworks). Bei NADOO wird der Code so organisiert, dass alle Funktionen auf den ersten Blick erkennbar und zugänglich sind.

- **Lesbarkeit und Wartbarkeit:**  
  Durch die strikte Strukturierung und das festgelegte Benennungsschema wird die Lesbarkeit des Codes deutlich verbessert. Dies verhindert vorschnelle Optimierungen, die den Code unverständlich machen könnten.

---

## Fazit

Das NADOO Framework ist darauf ausgelegt, die schwierigsten Probleme der App-Entwicklung zu vereinfachen – vor allem die Herausforderung, Code lesbar und wartbar zu halten. Durch klare Regeln für die Strukturierung und Benennung von Funktionen wird nicht nur die Zusammenarbeit im Team erleichtert, sondern auch die Einbindung von KI-Unterstützung optimiert.

Wenn Sie diesen Wikieintrag lesen, haben Sie bereits zwei Frameworks kennengelernt, die entscheidend zur heutigen App-Entwicklung beitragen: Briefcase und Toga. Mit dem NADOO Framework verbinden wir diese Konzepte mit weiteren nützlichen Tools und einer klaren, vordefinierten Struktur, die Ihnen den Einstieg in und die Weiterentwicklung von Projekten erheblich erleichtern soll.

---

**Batteries included – für Entwickler, die sich auf das Wesentliche konzentrieren möchten.**

Viel Erfolg bei der Umsetzung und Weiterentwicklung Deiner Projekte mit dem NADOO-IT Framework!
