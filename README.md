# Willkommen

Herzlich willkommen zu Deinem Einstieg in die IT-Karriere bei [Christoph Backhaus IT](https://wirrettendeinezeit.de).  

- Wir freuen uns 😊, Dich (you) auf Deinem Weg in die Welt der Anwendungsentwicklung und die Zukunft der IT 🍀 begleiten zu dürfen 🙏.

- Das "#globalyou" oder auch "#gerneperdu" ist bei uns Programm.

- Wir sind ein junges, dynamisches [Team](https://github.com/orgs/NADOOIT/people) - ergänzt um erfahrene Mitarbeitende - welches es sich auf die Fahnen geschrieben hat, mit Innovationen die  IT-Welt voranzubringen und damit einen __wertvollen__ Beitrag zum __dringend notwendigen Bürokratie-Abbau__ in Deutschland zu leisten.

- Wir sind __multikulturell__, __multilingual__ und __international__ aufgestellt und freuen uns über jede/n, der/die sich uns anschließen möchte.
- Bei uns werden unterschiedliche Kulturen und Sprachen gelebt und geschätzt, wie das auch in der IT-Welt üblich ist.

---

## NADOO-Wiki

Klicke auf 📖 [__Wiki__](https://github.com/NADOOIT/NADOO-Wiki/wiki/1.-Willkommen-bei-NADOO%E2%80%90Wiki) um gemeinsam und unterstützt durch uns in den __innovativen Lehrgang__ zu starten.

---

## Wiki V2

- 📖 Wiki V2 ist ein neues Projekt, das auf dem 📖 Wiki V1 aufbaut.

- Im Vergleich zu V1 ist es ein statisches Wiki, das auf [Markdown](https://docs.github.com/de/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)-Dateien basiert und mit [GitHub Pages](https://pages.github.com) gehostet wird.

- 📖 Wiki V2 bietet eine automatisch generierte Navigation
- Basis ist Ordnerstruktur der Markdown-Dateien
- Die Navigation wird mithilfe eines Python-Skripts generiert, das bei Änderungen an den Markdown-Dateien automatisch ausgeführt wird.
- Die im Wiki generierten Inhalte werden über GitHub Actions mit unserem innovativem Framework __NADOO-Launchpad__ synchronisiert.

---

### Übersicht der Inhalte

#### [1. Organisatorische Grundlagen & Bewerbungsprozess](docs/1/README.md)

##### [1.1 Onboarding und Probemonat](docs/1/1/README.md)

##### [1.2 Abgabe von Zeit- und Ausbildungsnachweisen](docs/1/2/README.md)

##### [1.3 Verhaltensregeln und Umgang miteinander](docs/1/3/README.md)

##### [1.4 Jobrotation & Weiterbildung](docs/1/4/README.md)

---

#### [2. Meeting Strukturen]()

>muss noch ergänzt werden

##### [2.1 Erweiterte 11er-Meetings]()

##### [2.2 33er-Meetings]()

##### [2.3 Breakout-Phasen]()

---

#### [3. Technische Grundlagen & Praktische Anwendung]()

>muss noch ergänzt werden

##### [3.1 GitHub]()

##### [3.2 GitHub-Issue-Tracking]()

##### [3.3 Visual Studio Code]()

##### [3.4 Python]()

##### [3.5 Briefcase]()

##### [3.6 Toga]()

##### [3.6 Pair-Programming]()

##### [3.7 Code-Reviews]()

##### [3.8 Dokumentation]()

---

#### [4. Kommunikation & Zusammenarbeit]()

>muss noch ergänzt werden

##### [4.1 GitHub-Issues]()

##### [4.2 Discord]()

##### [4.3 Video/Avatar-Pflicht]()

##### [4.4 Feedback-Kultur]()

---

#### [5. Weiterbildung & Karriereentwicklung]()

>muss noch ergänzt werden

##### [5.1 Präsentationstraining]()

##### [5.2 Assessmentcenter-Ansatz]()

---

### [6. Projektmanagement & Zeitmanagement]()

#### [6.1 Zeitmanagement]()

#### [6.2 Projektmanagement]()

#### [6.3 Scrum]()

#### [6.4 Kanban]()

#### [6.5 Projektplanung](docs/6/5/1/README.md)

##### [6.5.1 Projektantrag]()

#### [6.6 Projektphasen]()

#### [6.7 Projektstruktur]()

#### [6.8 Projektziele]()

#### [6.9 Projektbudget]()

#### [6.10 Projektcontrolling]()

#### [6.11 Projektabschluss]()

---

## Projektstruktur

```plaintext
NADOO-Wiki/
├── docs/
│   ├── README.md                # Zentrale TOC-Datei (wird vom Skript generiert)
│   └── 1/
│       ├── README.md            # Enthält eigene Überschriften (Kapitel)
│       ├── 1/
│       │   └── README.md        # Unterkapitel mit eigenen Überschriften
│       └── 2/
│           ├── README.md        # Unterkapitel mit eigenen Überschriften
│           └── 1/
│               └── README.md    # Weiteres Unterkapitel
├── scripts/
│   └── generate_wiki_navigation.py   # Skript zur Erzeugung des TOC basierend auf den Headings in den README.md
└── README.md                    # Projektbeschreibung / Einstieg ins Repository
```

---
