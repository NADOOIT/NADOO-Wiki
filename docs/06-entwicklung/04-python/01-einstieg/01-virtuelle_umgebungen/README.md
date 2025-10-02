# <p align="center">Python und virtuelle Umgebungen — ein Überblick</p>

Bevor wir mit dem Coding beginnen, installieren wir nicht nur Python 3.11 mithilfe von uv, sondern erstellen außerdem eine **virtuelle Umgebung**.

---

## Was ist eine virtuelle Umgebung?
_tbd_
<!-- Definition nachtragen -->

---

## Warum virtuelle Umgebungen? – Die Vorteile:

Virtuelle Umgebungen bieten zahlreiche Vorteile, die für die effiziente Arbeit in Projekten unerlässlich sind. Daher ist es ratsam, sich frühzeitig an das Arbeiten in solchen Umgebungen zu gewöhnen, um spätere Anpassungsschwierigkeiten und mögliche Unterbrechungen im Workflow zu vermeiden. 

1. **Isolierung von Projekten:**  
Jede virtuelle Umgebung ist isoliert und enthält ihre eigene Python-Version sowie spezifische Bibliotheken. Dadurch wird verhindert, dass Abhängigkeiten zwischen verschiedenen Projekten Konflikte verursachen.
<br><br> 
ℹ️ **Abhängigkeiten (Dependencies)** sind externe Bibliotheken, Frameworks oder Module, die in ein Softwareprojekt hinzugefügt werden können, um vorgefertigte Funktionen, die den Entwicklungsaufwand reduzieren können, zu liefern. Sie machen die Software aber abhängig von sich selbst und können zu Fehlern führen, da sie sich mit Updates ändern, was zu schwerwiegenden Problemen führen kann.

2. **Unabhängigkeit von System-Python:**  
Virtuelle Umgebungen erlauben es, eine bestimmte Python-Version und Abhängigkeiten zu verwenden, ohne das System-Python zu beeinträchtigen oder dessen Version zu ändern. Dies ist besonders hilfreich, wenn verschiedene Projekte unterschiedliche Versionen erfordern.

3. **Einfache Verwaltung von Abhängigkeiten:**  
In virtuellen Umgebungen kann man genau steuern, welche Bibliotheken und deren Versionen installiert werden. Mit Tools wie **pip** und einer `requirements.txt`-Datei lässt sich der gesamte Abhängigkeitsbaum einfach reproduzieren, was die Installation und das Setup auf anderen Maschinen erleichtert.

4. **Konsistenz zwischen Entwicklungs- und Produktionsumgebung:**  
Virtuelle Umgebungen gewährleisten, dass der Code sowohl in der Entwicklungsumgebung als auch in der Produktionsumgebung mit den gleichen Abhängigkeiten läuft. Dies reduziert „funktioniert-nur-bei-mir“-Probleme und sorgt für stabile, reproduzierbare Umgebungen.

5. **Erhöhte Sicherheit:**  
Da virtuelle Umgebungen isoliert sind, wird das Risiko verringert, dass unsichere oder inkompatible Bibliotheken das System oder andere Projekte beeinträchtigen. Änderungen an einer virtuellen Umgebung betreffen nur dieses eine Projekt.

6. **Einfache Zusammenarbeit:**  
Durch die Verwendung von virtuellen Umgebungen und gemeinsamen Konfigurationsdateien (wie `requirements.txt`) können Teams sicherstellen, dass alle Entwickler die gleiche Version der Abhängigkeiten verwenden, was zu weniger Fehlern und Konflikten führt.

---

## Der nächste Schritt

Nun hast du eine grobe Vorstellung davon, was virtuelle Umgebungen sind und welchen Nutzen sie - vor allem im Zusammenhang mit Python - bringen. Im nächsten Abschnitt beginnen wir mit der praktischen Umsetzung in VS Code.
<!-- weiter zu Installation -->

---

<p align="center">
<a href="/docs/06-entwicklung/04-python/01-einstieg/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/04-python/01-einstieg/02-installation/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/06-entwicklung/04-python/01-einstieg/README.md/#dieses-kapitel-beinhaltet-folgende-abschnitte"><strong>Zurück zur Abschnitts-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>