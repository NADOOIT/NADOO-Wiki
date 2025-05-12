# Python
<!-- Text ggf. anpassen und Kapitelübersicht hinzufügen -->
## Python und virtuelle Umgebungen — ein Überblick

Bevor wir mit dem Coding beginnen, installieren wir Python 3.11 mithilfe von uv und erstellen eine virtuelle Umgebung.

### Warum virtuelle Umgebungen?

Virtuelle Umgebungen haben eine Reihe von Vorteilen, die für das Arbeiten in Projekten essentiell sind. Es ist wichtig, sich das arbeiten in virtuellen Umgebungen so früh wie irgend möglich anzugewöhnen, um spätere Umgewöhnung und dadurch enstehende Schleifpunkte, zu vermeiden.

1. **Isolierung von Projekten:**  
Jede virtuelle Umgebung ist isoliert und enthält ihre eigene Python-Version, sowie spezifische Bibliotheken. Dadurch wird verhindert, dass Abhängigkeiten zwischen verschiedenen Projekten Konflikte verursachen.

> Abhängigkeiten(Dependencies), sind externe Bibliotheken, Frameworks oder Module, die in ein Softwareprojekt himzugefügt werden können, um vorgefertigte Funktionen, die den Entwicklungsaufwand reduzieren können, zu liefern. Sie machen die Software aber abhängig von sich selbst, und können zu Fehlern führen, da sie sich mit Updates ändern, was zu  schwerwiegenden Problemen führen kann.

2. **Unabhängigkeit von System-Python:**  
Virtuelle Umgebungen erlauben es, eine bestimmte Python-Version und Abhängigkeiten zu verwenden, ohne das System-Python zu beeinträchtigen oder dessen Version zu ändern. Dies ist besonders hilfreich, wenn verschiedene Projekte unterschiedliche Versionen erfordern.

3. **Einfache Verwaltung von Abhängigkeiten:**  
In virtuellen Umgebungen kann man genau steuern, welche Bibliotheken und deren Versionen installiert werden. Mit Tools wie pip und einer `requirements.txt`-Datei lässt sich der gesamte Abhängigkeitsbaum einfach reproduzieren, was die Installation und das Setup auf anderen Maschinen erleichtert.

4. **Konsistenz zwischen Entwicklungs- und Produktionsumgebung:**  
Virtuelle Umgebungen gewährleisten, dass der Code sowohl in der Entwicklungsumgebung als auch in der Produktionsumgebung mit den gleichen Abhängigkeiten läuft. Dies reduziert „funktioniert-nur-bei-mir“-Probleme und sorgt für stabile, reproduzierbare Umgebungen.

5. **Erhöhte Sicherheit:**  
Da virtuelle Umgebungen isoliert sind, wird das Risiko verringert, dass unsichere oder inkompatible Bibliotheken das System oder andere Projekte beeinträchtigen. Änderungen an einer virtuellen Umgebung betreffen nur dieses eine Projekt.

6. **Einfache Zusammenarbeit:**  
Durch die Verwendung von virtuellen Umgebungen und gemeinsamen Konfigurationsdateien (wie `requirements.txt`) können Teams sicherstellen, dass alle Entwickler die gleiche Version der Abhängigkeiten verwenden, was zu weniger Fehlern und Konflikten führt.