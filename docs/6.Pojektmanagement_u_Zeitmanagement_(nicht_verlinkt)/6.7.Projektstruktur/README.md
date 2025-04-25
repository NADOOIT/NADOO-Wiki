# 6.7 Projektstruktur

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
