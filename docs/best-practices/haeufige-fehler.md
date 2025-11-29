# Häufig vorkommende Fehler

Lernen aus Fehlern ist eine unserer stärksten Fähigkeiten. Diese Seite sammelt typische Stolpersteine aus dem Alltag – nicht um Schuld zu verteilen, sondern um gelassen und professionell damit umzugehen und sie künftig seltener passieren zu lassen.

> Kurzprinzip: Fehler gehören dazu. Wichtig ist, wie wir reagieren, lernen und verbessern.

---

## 1) Direkter Merge in `main` statt Feature‑Branch + Pull Request

### Kurzfassung
- Arbeiten bitte immer über Issue‑Branch → Pull Request → Review → Merge.
- Direkte Commits auf `main` vermeiden (Branch‑Protection hilft!).

### Woran erkenne ich das?
- In GitHub ist ein Commit/Push direkt auf `main` ohne PR‑Historie sichtbar.
- Lokal zeigt `git log --graph --decorate --oneline -n 20` einen Commit auf `main`, der nicht über einen Merge‑Commit aus einem Feature‑Branch kam.

### Wenn es passiert ist – Sofortmaßnahmen
1. Ruhe bewahren – es ist nicht schlimm und lässt sich beheben.
2. Transparenz im Team schaffen (kurzer Hinweis im Stand‑up oder Discord).
3. Korrigierende Schritte (abhängig vom Kontext):
   - Option A: GitHub „Revert“ auf die/n betroffenen Commit(s).
   - Option B: Einen Fix‑Branch erstellen, den Zustand korrigieren und einen PR stellen.
   - Option C (Admin): Falls noch niemand gepullt hat, kann ein Reset sinnvoll sein (vorher absprechen!).
4. Danach: Kurze Notiz im PR, warum es passierte und wie wir vorbeugen.

### Prävention
- Standard‑Workflow leben:
  1. Issue anlegen/auswählen
  2. Branch erstellen (z. B. `feature/<issue-id>-kurztitel`)
  3. Commits
  4. Pull Request
  5. Review & Merge (Squash oder Merge je nach Policy)
- PR‑Template und Checkliste nutzen (Akzeptanzkriterien, Tests, Screenshots, etc.).
- Branch‑Protection in GitHub aktivieren:
  - Direkte Pushes auf `main` verbieten
  - Mindestens 1 Review verlangen
  - Status Checks (CI) erzwingen
- Lokale Guardrails (optional):
  - Pre‑commit‑Hooks
  - Git‑Config so wählen, dass „versehentliche“ Pushes weniger wahrscheinlich sind

### Nützliche Befehle
```bash
# Neuen Feature‑Branch anlegen und wechseln
git switch -c feature/123-fix-login

# Letzte 20 Commits kompakt und mit Grafik anzeigen
git log --graph --decorate --oneline -n 20

# Commit rückgängig machen (Revert erzeugt neuen Gegen‑Commit)
git revert <commit-sha>
```

### Hilfe holen (schnell!)
- Frag im Discord‑Server „NADOO‑IT“ nach Unterstützung.
- Einladung: https://discord.gg/jyrSNKf2
- Kurze Beschreibung: Was ist passiert, welche Dateien sind betroffen, gewünschter Zielzustand.

---

## Weitere häufige Fehler (Platzhalter)
- PR ohne verknüpftes Issue
- CI ist rot, aber es wird trotzdem gemergt
- Force‑Push auf gemeinsame Branches
- Fehlende Labels/Reviewers
- Unvollständige PR‑Beschreibung (kein Kontext, keine Akzeptanzkriterien)

Ergänzungen sehr willkommen – bitte Beispiele, Lösungen/Workarounds und Präventions‑Tipps hinzufügen.

---

## Was wir gelernt haben: Struktur vs. Freiheit

### Hintergrund
Im letzten Jahr haben wir sehr freie Arbeit zugelassen. Das hat vielen Spaß gemacht und die Ausbildung hat funktioniert – gleichzeitig fühlten sich einige zeitweise „verloren“. Diese Rückmeldungen nehmen wir ernst. Darum haben wir mehr Struktur eingeführt – ohne die Neugier und Freude am Entdecken zu verlieren.

### Zielbild: „strukturierte Freiheit“
- Klare Leitplanken (kleine, greifbare Aufgaben; gut definierte Ziele; sichtbarer Fortschritt)
- Innerhalb der Leitplanken: Autonomie, Experimente, Verantwortung
- Standard‑Takt: fokussierte Arbeitsblöcke (z. B. Pomodoro), eindeutige Ziele pro Block, kurze Retrospektiven

### Konkrete Maßnahmen
- Issue‑first‑Workflow: kleine Arbeitspakete mit Akzeptanzkriterien statt „vage große Themen“
- Tagesplan: 1–3 Issues auswählen, pro Block ein kurzes Ziel formulieren
- Block‑Rituale: kurzer „Intent“ am Anfang, kurze „Outcome‑Notiz“ am Ende (Bullet Points)
- Wenn blockiert → aktiv Hilfe anfordern (Launchpad‑Button „Decision Request“ / Discord)
- Wöchentliche Retro: „Was hat geholfen? Was verbessern wir nächste Woche?“

### Flexibilität beibehalten
- Explorations‑Slots (opt‑in), um Neues zu testen – dokumentiert mit kurzer Lern‑Notiz
- Paar‑/Mob‑Programming je nach Bedarf
- „Podcast: Ich bin bereit“ als niedrigschwellige Möglichkeit, Erfahrungen zu teilen

### Messung & Feedback
- Leading‑Indikatoren: weniger Blocker‑Zeit, mehr kleine PRs, mehr bestätigte Bullets pro Tag, Zufriedenheit
- Lagging‑Indikatoren: Time‑to‑Merge sinkt, Onboarding wird schneller

### Nächste Schritte
- 4‑Wochen‑Zyklus: Praktiken ausprobieren, Signale sammeln, justieren
- Experimente willkommen: Wenn etwas nachweislich bessere Ergebnisse bringt, integrieren wir es
