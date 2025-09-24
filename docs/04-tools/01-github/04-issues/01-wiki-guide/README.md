# <p align="center">Selbstständig Veränderungen innerhalb des Wikis vornehmen (später auch am Launchpad): ein kleiner Guide</p>
<!-- Verweis auf dieses Doc an passender Stelle im Styleguide einbinden-->

An dieser Stelle zeigen wir dir, wie du aktiv an der Gestaltung des Wiki mitwirken kannst und wie du bereits jetzt schon Issues, die das Wiki betreffen, bearbeiten und auch vielleicht schon lösen kannst. Möglicherweise hast du noch nicht die Berechtigungen, um im Wiki verschiedene Funktionen zu nutzen. Ist dies der Fall, melde dich bitte bei [Christoph](mailto:Christoph.backhaus@nadooit.de) mit deinem GitHub Namen, damit er sie dir erteilen kann.

## Issue erstellen

Solltest du auf Unklarheiten stoßen, möchtest neue Inhalte hinzufügen, bestehende Inhalte verändern oder sogar löschen, dann erstellst du zu allererst ein Issue innerhalb des Wiki-Repository und beschreibst dort dein Anliegen.

![Image](https://github.com/user-attachments/assets/eea54f62-a29e-4ae1-9f78-fe1865ef2dd0)

![Image](https://github.com/user-attachments/assets/0caccfbd-1e07-46bf-941b-c51ff612b303)

Wenn du ein bereits bestehendes Issue bzgl. des Wiki bearbeiten willst, fällt der erste Schritt weg und du wählst das Issue im Wiki-Repository aus.

## Branch aus dem Issue erstellen

Sind die ersten Schritte getan, kannst du aus dem Issue heraus eine Branch erstellen, was bedeutet, dass du das Wiki-Repository klonst. Durch diesen Schritt kannst du am Wiki in einer isolierten Umgebung arbeiten, ohne dass Veränderungen direkt an der Main des Wiki vorgenommen werden.

![Image](https://github.com/user-attachments/assets/1f45ac25-4cb1-4fbc-99ca-eb50bdc07215)

Hier gehst du auf die Fläche "create a Branch" und wählst "Branch mit GitHub-Desktop öffnen"

![Image](https://github.com/user-attachments/assets/272d1d5e-ec87-4cfd-843f-013682048196)

Auf der Desktop-Version von GitHub überprüfst du nun, ob du im richtigen Repository und Issue bist.

Wenn du richtig bist, wählst du "open in Visual Studio Code" aus.

![Image](https://github.com/user-attachments/assets/efd10356-827b-4f86-8043-01c3f65a2369)

Jetzt öffnet sich dein VSC mit dem Wiki. An dieser Stelle überprüfst du unten links am Rand, ob du im richtigen Verzeichnis bist.

![Image](https://github.com/user-attachments/assets/0bb51499-f4ec-4a99-a30d-faede3486df4)

Ist alles in Ordnung, kannst du mit der Veränderung loslegen. Achte darauf, alle Veränderungen im Markdown-Format zu verfassen.
Jetzt stellt sich die Frage, ob du bestehende Inhalte ergänzen willst oder neue hinzufügen möchtest.

Wenn du bestehende Inhalte nur ergänzen willst, suchst du innerhalb der Ordnerstruktur den Beitrag raus, gehst auf die README.md vom entsprechenden Beitrag und nimmst dort deine Veränderungen vor.

![Image](https://github.com/user-attachments/assets/46e1b2c7-ba5b-4be7-9f36-dc30b84898f4)
![Image](https://github.com/user-attachments/assets/10d3f09f-4b0c-4db2-95f9-ee1f7432c7df)

Möchtest du allerdings komplett neue Inhalte hinzufügen, dann musst du die bestehenden Ordner um weitere Ordner ergänzen. **Achte auf sinnvolle Gliederung**. In dem neu erstellten Ordner musst du ein File (diesen nennst du README.md) hinzufügen, in welchem du deinen Inhalt einfügst.

![Image](https://github.com/user-attachments/assets/93f96e7c-2e29-4a49-8248-99cd1ba96b49)
![Image](https://github.com/user-attachments/assets/e4cfe551-5365-4880-a52c-8fb4fa4d62f1)
In diesem Beispiel wird ein Unterordner 7 mit dem File README.md im Ordner 1 erstellt (es wird somit der Abschnitt 1.7 erzeugt.)

Gegebenenfalls muss auch das Inhaltverzeichnis ergänzt werden. Hierfür klappst du die komplette Doc-Struktur ein und wählst die letzte README.md (hier befindet sich das Inhaltsverzeichnis des Wiki). Ergänze hier deinen neuen Abschnitt inklusive Verlinkung.

![Image](https://github.com/user-attachments/assets/fddb57b1-2a2a-4b69-82e7-3dda903c9e1e)

Sind diese Schritte getan, kannst du durch die Vorschau-Funktion überprüfen, wie deine Veränderung aussieht und gegebenfalls Verlinkungen überprüfen.
Ist alles in Ordnung, speicherst du (strg+s /cmd +s) die Veränderungen und wechselst wieder auf GitHub Desktop. Hier solltest du sehen, dass die Veränderungen synchronisiert worden sind. Jetzt musst du noch auf der linken Seite (Commit to main) beschreiben, was genau du verändert hast. Anschließend wählst du die blaue Schaltfläche "push Origin".
Ist dies getan, wählst du in derselben Schaltfläche den Dropdown-Pfeil und gehst auf "create pull request"

<img width="1135" alt="Image" src="https://github.com/user-attachments/assets/0d966914-3150-4d29-934c-dc0bd0c759e6" />

<img width="1083" alt="Image" src="https://github.com/user-attachments/assets/a3d276b0-14ee-43b4-ab5a-7fece889a746" />

<img width="671" alt="Image" src="https://github.com/user-attachments/assets/10c48536-822b-4499-b624-e362aa37fc4c" />

## Reviewer hinzufügen und Mergen

Wenn du bis hier hin alles richtig gemacht hast, sollte sich automatisch GitHub im Browser öffnen (mit deinem geöffneten Pull Request). Hier fügst du 3 Reviewer hinzu (6 Augen Pinzip), welche deine Veränderung überprüfen sollen. Erst wenn diese ihr "Ok" gegeben haben, kannst du deinen Pull Request "mergen", was bedeutet, dass deine Veränderungen in die Wiki-main aufgenommen werden.

<img width="451" alt="Image" src="https://github.com/user-attachments/assets/fd59b6fc-2800-4488-95f2-c552cbadfce5" />
<img width="876" alt="Image" src="https://github.com/user-attachments/assets/8c4049c8-1bf4-4284-8cef-edc1b9c75edc" />
<img width="869" alt="Image" src="https://github.com/user-attachments/assets/e06a1e2c-c8a3-4fea-b0d1-3f281a543015" />

### Das war´s auch schon. Ich hoffe, du konntest dich gut zurechtfinden und erste Eindrücke und Erfahrungen im Umgang mit GitHub sammeln

---

**Dieses Thema beinhaltet folgende Kapitel:**
---

🔹 [**Wiki-Guide**](/docs/04-tools/01-github/04-issues/01-wiki-guide/README.md) </br>
🔹 [**Labels**](/docs/04-tools/01-github/04-issues/02-labels/README.md) </br>
🔹 [**Types**](/docs/04-tools/01-github/04-issues/03-types/README.md) </br>
🔹 [**Assignees**](/docs/04-tools/01-github/04-issues/04-assignees/README.md) </br>
🔹 [**Milestones**](/docs/04-tools/01-github/04-issues/05-milestones/README.md) </br>
🔹 [**Projects**](/docs/04-tools/01-github/04-issues/06-projects/README.md) </br>
🔹 [**Discussions**](/docs/04-tools/01-github/04-issues/07-discussions/README.md) </br>
🔹 [**Templates**](/docs/04-tools/01-github/04-issues/08-templates/README.md) </br>

---

<p align="center">
<a href="/docs/04-tools/01-github/04-issues/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/01-github/04-issues/02-labels/README.md"><strong>Weiter</strong></a>
</p>

