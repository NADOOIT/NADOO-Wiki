# Willkommen

Herzlich willkommen zu Ihrem Einstieg in die IT-Karriere bei [Christoph Backhaus IT](https://wirrettendeinezeit.de).  
Wir freuen uns, Sie auf Ihrem Weg in die Welt der Anwendungsentwicklung begleiten zu dürfen.

---

## NADOO-Wiki

Kicken Sie auf [__Wiki__](https://github.com/NADOOIT/NADOO-Wiki/wiki/1.-Willkommen-bei-NADOO%E2%80%90Wiki) um mit unserem Lehrgang zu starten.

---

## Wiki V2

Das Wiki V2 ist ein neues Projekt, das auf dem Wiki V1 aufbaut. Es ist ein statisches Wiki, das auf Markdown-Dateien basiert und mit [GitHub Pages](https://pages.github.com) gehostet wird.

Das Wiki V2 bietet eine automatisch generierte Navigation, die auf der Ordnerstruktur der Markdown-Dateien basiert. Die Navigation wird mithilfe eines Python-Skripts generiert, das bei Änderungen an den Markdown-Dateien automatisch ausgeführt wird.

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
