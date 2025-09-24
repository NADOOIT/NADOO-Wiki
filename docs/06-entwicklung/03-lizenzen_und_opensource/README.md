# <p align="center">Lizenzen, Open Source und die Welt der Softwareabhängigkeiten</p>

---

Bevor du mit der Entwicklung deiner ersten eigenen App beginnst, solltest du dich mit der Thematik rund um Lizenzen und Softwareabhängigkeiten vertraut machen. Immerhin wirst du während dieses Prozesses verschiedene Softwarepakete nutzen müssen, die alle unter bestimmten Lizenzen veröffentlicht wurden. Lass uns einen Moment innehalten, um die Bedeutung dieser Lizenzen und die Welt der Open-Source-Software zu betrachten.

---

## Die Macht der Open-Source-Gemeinschaft

Zunächst einmal ist es wichtig, sich bewusst zu machen, welch enormer Wert dir durch Open-Source-Software zur Verfügung steht. Denke z.B. an die KI-Modelle von Meta, Microsoft, Google und viele andere, die Milliarden an Entwicklungskosten repräsentieren und nun frei zugänglich sind. Oder betrachte Projekte wie Briefcase und Toga, an denen Entwickler seit über einem Jahrzehnt arbeiten und von deren Arbeit wir nun profitieren können.

Diese Großzügigkeit und Zusammenarbeit in der Entwicklergemeinschaft ist beeindruckend und verdient unsere Dankbarkeit. Es ist wichtig, dass wir diese Dankbarkeit auch zum Ausdruck bringen, sei es durch Beiträge zur Dokumentation, Fehlermeldungen oder, wenn möglich, durch eigene Code-Beiträge.

---

## Verständnis von Softwarelizenzen

Jedes Softwarepaket, das du verwendest, kommt mit einer Lizenz. Hier sind einige der häufigsten:

1. **MIT-Lizenz**: Eine sehr permissive Lizenz, die fast alles erlaubt, solange der Urheberrechtshinweis und die Lizenz mitgeliefert werden.

2. **Apache-2.0-Lizenz**: Ähnlich permissiv wie MIT, bietet aber zusätzlichen Schutz vor Patentstreitigkeiten.

3. **BSD-Lizenzen**: Es gibt verschiedene BSD-Lizenzen, die alle relativ permissiv sind, mit leicht unterschiedlichen Anforderungen.

4. **GNU General Public License (GPL)**: Eine "Copyleft"-Lizenz, die verlangt, dass abgeleitete Werke unter derselben Lizenz veröffentlicht werden.

5. **GNU Affero General Public License (AGPL)**: Ähnlich wie die GPL, aber mit zusätzlichen Anforderungen für Software, die über ein Netzwerk bereitgestellt wird.

Es ist wichtig, die Lizenzen der von dir verwendeten Software zu verstehen und zu respektieren, um rechtliche Probleme zu vermeiden und die Open-Source-Gemeinschaft zu unterstützen.

---

## Die Rolle von Paketmanagern

Tools wie pip (oder das neuere uv) haben die Verwaltung von Abhängigkeiten erheblich vereinfacht. Sie ermöglichen es uns, schnell und einfach Pakete zu installieren und zu aktualisieren, was die Entwicklung beschleunigt und den Zugang zu einer Vielzahl von Bibliotheken erleichtert.

---

## Die Schattenseiten von Abhängigkeiten

Trotz der vielen Vorteile bringen Abhängigkeiten auch Risiken mit sich:

1. **Sicherheitslücken**: Jede Abhängigkeit kann potenziell Sicherheitslücken enthalten. Ein beeindruckendes Beispiel dafür findest du in [diesem Video](https://www.youtube.com/watch?v=yewkv8pTAu0).

2. **Update-Druck**: Mit mehr Abhängigkeiten steigt der Druck, immer auf dem neuesten Stand zu bleiben. Dies kann zeitaufwändig und manchmal problematisch sein.

3. **Kompatibilitätsprobleme**: Große Umstellungen wie der Wechsel von Python 2 zu Python 3 können erhebliche Probleme verursachen und werden von vielen Entwicklern als schwierige Phase erinnert.

## Die Bedeutung von Frameworks

Briefcase, was du unter Umständen bereits verwendet hast, ist ein Framework. Frameworks geben eine Struktur vor, nach der Projekte organisiert sein müssen. Dies mag zunächst einschränkend erscheinen, bietet aber viele Vorteile:

1. **Verbesserte Code-Lesbarkeit**: Durch einheitliche Strukturen wird es einfacher, sich in fremdem Code zurechtzufinden.

2. **Effizientere Zusammenarbeit**: Wenn alle dasselbe Framework nutzen, ist es leichter, Code zu teilen und gemeinsam zu entwickeln.

3. **Bewährte Praktiken**: Frameworks bündeln oft jahrelange Erfahrungen und bewährte Praktiken.

Andere beliebte Frameworks in der Python-Welt sind Django, Flask und FastAPI für Webentwicklung.

<!--bisher nur Fokus auf Python, muss mit der Zeit nochmal überarbeitet werden (Stand: 13.05.25)-->

## Blick in die Zukunft: Mojo

Während Python eine großartige Sprache zum Lernen und für viele Anwendungen ist, hat es Nachteile in Bezug auf Geschwindigkeit und Energieeffizienz. Deshalb werden wir in Zukunft auf Mojo umsteigen, eine Sprache, die du im Verlauf dieses Lehrgangs kennenlernen wirst. Mojo verspricht, die Vorteile von Python mit deutlich verbesserter Performance zu kombinieren.

<!--Plan vermutlich nicht mehr aktuell, da auf Java umgestiegen wird (Stand: 13.05.25)-->

## Fazit

Die Welt der Softwareentwicklung ist komplex und voller Nuancen. Während wir die enormen Vorteile von Open-Source-Software und Frameworks genießen, müssen wir uns auch der Verantwortung und potenziellen Risiken bewusst sein. Indem wir diese Aspekte verstehen und respektvoll mit den Werkzeugen umgehen, die uns zur Verfügung stehen, können wir nicht nur bessere Software entwickeln, sondern auch zur Weiterentwicklung der Entwicklergemeinschaft beitragen.


### Quellen

[1] <https://pypi.org/project/uv/0.1.16/> <br>
[2] <https://blog.kusho.ai/uv-pip-killer-or-yet-another-package-manager/> <br>
[3] <https://astral.sh/blog/uv> <br>
[4] <https://blog.streamlit.io/python-pip-vs-astral-uv/> <br>
[5] <https://docs.astral.sh/uv/pip/dependencies/> <br>
[6] <https://github.com/astral-sh/uv/issues/1870> <br>
[7] <https://github.com/astral-sh/uv/actions/runs/8210006157/job/22456810854> <br>
[8] <https://www.ingenieur.de/technik/fachbereiche/kuenstliche-intelligenz/kuenstliche-intelligenz-diese-15-ki-tools-sollten-sie-kennen/> <br>

---

**Dieser Themenbereich beinhaltet folgende Themen:**
---

🔹 [**Dokumentation**](/docs/06-entwicklung/01-dokumentation/README.md)<br>
🔹 [**Clean Architecture**](/docs/06-entwicklung/02-clean_architecture/README.md) <br>
🔹 [**Lizenzen und Open Source**](/docs/06-entwicklung/03-lizenzen_und_opensource/README.md) <br>
🔹 [**Python**](/docs/06-entwicklung/04-python/README.md) <br>
🔹 [**Java**](/docs/06-entwicklung/05-java/README.md) <br>
🔹 [**Frameworks**](/docs/06-entwicklung/06-frameworks/README.md) <br>
🔹 [**Digitale Produktentwicklung**](/docs/06-entwicklung/07-digitale_produktentwicklung/README.md) <br>
🔹 [**CMS**](/docs/06-entwicklung/08-cms/README.md) <br>

---

<p align="center">
<a href="/docs/06-entwicklung/02-clean_architecture/02-best_practices/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/04-python/README.md"><strong>Weiter</strong></a>
</p>

