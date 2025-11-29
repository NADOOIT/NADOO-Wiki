# <p align="center">Erfassung deiner Arbeits- und Pausenzeiten mit dem NADOO-Launchpad</p>

Die Erfassung deiner **Arbeits- und Pausenzeiten** erfolgt über unsere Software [**NADOO-Launchpad**](https://github.com/NADOOIT/NADOO-Launchpad).

Sie ist für dich als Neueinsteiger einer der wichtigsten Punkte, der keine Sorgen auslösen oder missverständlich sein sollte. Hier erklären wir dir, wie du unser Tool - das [**NADOO-Launchpad**](https://github.com/NADOOIT/NADOO-Launchpad) - richtig für das Erfassen deiner Arbeits- und Pausenzeit verwendest und wie du Einblick in die erfassten Zeiten erhältst. <p>**Vorab - alle erfassten Zeiten werden in einer CSV-Datei lokal gespeichert und sind manipulierbar, was insbesondere an deinem ersten Tag relevant sein könnte.** <p> <small>Wie du das Launchpad zum ersten Mal startest bzw. installierst, wird dir in der [**README des Launchpad-Repositories**](https://github.com/NADOOIT/NADOO-Launchpad/blob/main/README.md) erklärt. Hier zeigen wir dir, wie du deine Zeiten richtig erfassen kannst. </small> <p>Nachdem du das Launchpad gestartet hast, sollte sich folgendes GUI öffnen: ![alt text](image.png) <br><small>
Auf diesem Bild siehst du, wie es aussieht, wenn bereits Zeiten vorhanden sind.</small> <p>Im oberen Bereich sind 4 Buttons, die mehr oder weniger die gesamte Zeiterfassung ausmachen und abgesehen vom "Statistik"-Button selbsterklärend sind. Der Button "Pause starten" wird zu "Pause beenden", sobald dieser ausgewählt wurde.![alt text](image-1.png)   <p>Der ‘Statistik’-Button öffnet ein weiteres Fenster, in dem eine detaillierte Darstellung der Arbeitszeit in frei wählbaren Zeitabschnitten angezeigt wird. <br> ![alt text](image-2.png) <br> An dieser Stelle wurde der Zeitraum 1. April bis 30. April gewählt. Nachdem du das zu bestimmende Zeitfenster für dich gewählt hast, klickst du auf "Aktualisieren", damit eine Statistik zu diesem erstellt wird. Auch Auswertungen zu einzelnen Tagen sind möglich.  <p> Wenn du die CSV-Datei mit den Zeiten zur Anschau oder gegebenenfalls für deren Bearbeitung öffnen möchtest, ohne lange nach dem Ablageort zu suchen, ist folgender Schritt interessant für dich: <br>![alt text](image-3.png) <br>Wähle dazu, wie im Screenshot abgebildet, <br>Optionen --> Basis Ordner öffnen <br> aus, um das Verzeichnis mit den gespeicherten Zeiten zu öffnen. ![alt text](image-4.png) <small>Der Ordner "Data" enthält alle deine Stempelzeiten als CSV-Datei </small>![alt text](image-5.png) <br> Wie du diese öffnest, bleibt dir überlassen. In folgendem Beispiel nutzen wir VSC. ![alt text](image-6.png) Hier kannst du aktiv die Zeiten bearbeiten und durch "speichern" werden diese auch im Launchpad aktualisiert. <p>Das war's auch schon. Aktuell sind dies alle Funktionen, die das Launchpad zur Zeiterfassung bietet. Für deinen ersten Tag vielleicht auch noch ganz interessant: <br><strong>Da die Zeiten lokal auf deinem PC gespeichert werden, hat kein Zweiter Zugriff darauf.</strong><p>Dadurch, dass das Launchpad in der Entwicklung ist, kommen immer wieder neue Funktionen hinzu und alte Funktionen werden überarbeitet oder verschwinden. Aus diesem Grund könnten sich das hier gezeigte Interface oder bestimmte Schritte gegebenfalls von deinem aktuellen Ist-Zustand unterscheiden.

Alle weiteren Funktionen des Tools, wie es aufgebaut ist und wie du es richtig anwendest, erklärt dir unser [**Launchpad-Guide**](/docs/04-tools/05-launchpad/README.md).

---

Hinweis für Tag 1:

- Folge vor dem ersten Einstempeln der [**First‑Day Contract Intake Checklist**](/docs/00-willkommen/01-leitfaden/README.md#3-vertragsdaten-erfassen--firstday-contract-intake-checklist), damit alle Vertrags‑ und Kalenderdaten sofort korrekt erfasst werden.
- Nutze am ersten Tag von **12:00–16:30 Uhr** gezielt die Zeit, um deine **Vertragsdaten einzutragen** (per E‑Mail‑Betreffs, siehe oben) und dich mit dem **Wiki** vertraut zu machen ([Leitfaden](/docs/00-willkommen/01-leitfaden/README.md)).

## Pflicht: E-Mail-Messaging parallel zur Stempeluhr

Zusätzlich zum Einstempeln in Launchpad sendest du eine kurze E‑Mail über unser Messaging‑System. Diese E‑Mails werden automatisch verarbeitet und dienen als nachvollziehbare Bestätigung. 

Verwende folgende Betreff‑Schemata (müssen exakt passen):

- Einstempeln (START): ``[MitarbeiterID]_START_[YYYY]_[MM]_[DD]_[HH]_[MM]``
- Ausstempeln (ENDE): ``[MitarbeiterID]_ENDE_[YYYY]_[MM]_[DD]_[HH]_[MM]``

Beispiele:

```
1234_START_2025_09_15_08_00
1234_ENDE_2025_09_15_16_30
```

Hinweise:

- Pausen werden derzeit nicht per separater E‑Mail gemeldet. Maßgeblich sind START/ENDE.
- In Zukunft kann Launchpad diese E‑Mails optional automatisch versenden. Bis dahin bitte manuell senden und gern Automations‑Ideen als Issue vorschlagen.
- Aktuelle Routine: **08:00–16:30 Uhr** Arbeitszeit, **11:30–12:00 Uhr** feste Pause.
- Meetings: **10:14–10:30 Uhr** Netzwerken & Anwesenheitscheck; **10:30–11:30 Uhr** Daily Team‑Meeting.

## Anforderungen & Nachweise (vom Bildungsträger)

Je nach Bildungsträger unterscheiden sich die geforderten Nachweise. Typische Varianten sind:

- Monatlicher Zeitnachweis (Zeitenübersicht)
- Wöchentliche Berichtshefte
- Monatliche Anwesenheitsliste

Setze deine persönlichen Anforderungen mit diesem Betreff (Schema muss exakt passen):

``
[ID]_ANFORDERUNGEN_ZEITNACHWEIS_JA|NEIN_BERICHTSHEFTE_JA|NEIN_ANWESENHEITSLISTE_JA|NEIN
``

Beispiel: `1234_ANFORDERUNGEN_ZEITNACHWEIS_JA_BERICHTSHEFTE_JA_ANWESENHEITSLISTE_NEIN`

### Weitere beantragbare/zu meldende Ereignisse (per E‑Mail‑Betreff)

Alle Betreffs müssen exakt dem Schema entsprechen:

- Messebesuch (ein Tag): ``[ID]_MESSEBESUCH_[YYYY]_[MM]_[DD]``  Beispiel: `1234_MESSEBESUCH_2025_10_02`
- Praktikum Start: ``[ID]_PRAKTIKUM_START_[YYYY]_[MM]_[DD]``  Beispiel: `1234_PRAKTIKUM_START_2025_09_16`
- Praktikum Ende: ``[ID]_PRAKTIKUM_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_PRAKTIKUM_ENDE_2025_12_20`
- Prüfung (ein Tag): ``[ID]_PRUEFUNG_[YYYY]_[MM]_[DD]``  Beispiel: `1234_PRUEFUNG_2025_11_05`
- Prüfung (Zeitraum): ``[ID]_PRUEFUNG_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_PRUEFUNG_START_2025_11_05_ENDE_2025_11_06`
- Krankmeldung (Zeitraum): ``[ID]_KRANKMELDUNG_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_KRANKMELDUNG_START_2025_09_14_ENDE_2025_09_16`
- Krankes Kind (ein Tag): ``[ID]_KRANKESKIND_[YYYY]_[MM]_[DD]``  Beispiel: `1234_KRANKESKIND_2025_10_03`
- Krankes Kind (Zeitraum): ``[ID]_KRANKESKIND_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_KRANKESKIND_START_2025_10_03_ENDE_2025_10_04`
- Entschuldigt (ein Tag): ``[ID]_ENTSCHULDIGT_[YYYY]_[MM]_[DD]``  Beispiel: `1234_ENTSCHULDIGT_2025_10_07`
- Entschuldigt (Zeitraum): ``[ID]_ENTSCHULDIGT_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_ENTSCHULDIGT_START_2025_10_07_ENDE_2025_10_08`
- Unentschuldigt (ein Tag): ``[ID]_UNENTSCHULDIGT_[YYYY]_[MM]_[DD]``  Beispiel: `1234_UNENTSCHULDIGT_2025_10_09`
- Unentschuldigt (Zeitraum): ``[ID]_UNENTSCHULDIGT_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_UNENTSCHULDIGT_START_2025_10_09_ENDE_2025_10_10`
- Schule (Zeitraum): ``[ID]_SCHULE_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_SCHULE_START_2025_09_22_ENDE_2025_09_26`
- Anwesenheitsliste (monatlich): ``[ID]_[optionalNameSlug]_ANWESENHEITSLISTE_[YYYY]_[M]``  Beispiel: `1234_fritz_mueller_ANWESENHEITSLISTE_2025_9`
- Anforderungen setzen: ``[ID]_ANFORDERUNGEN_ZEITNACHWEIS_JA|NEIN_BERICHTSHEFTE_JA|NEIN_ANWESENHEITSLISTE_JA|NEIN``  Beispiel: `1234_ANFORDERUNGEN_ZEITNACHWEIS_JA_BERICHTSHEFTE_JA_ANWESENHEITSLISTE_NEIN`
- Entwickler‑Accounts (GitHub): ``[ID]_SET_DEV_GITHUB_[Username]``  Beispiel: `1234_SET_DEV_GITHUB_nadoouser`
- Entwickler‑Accounts (GitHub Bestätigung): ``[ID]_CONFIRM_DEV_GITHUB_[Username]``  Beispiel: `1234_CONFIRM_DEV_GITHUB_nadoouser`
- Entwickler‑Accounts (Discord Name): ``[ID]_SET_DEV_DISCORD_NAME_[Name]``  Beispiel: `1234_SET_DEV_DISCORD_NAME_fritz#1234`
- Entwickler‑Accounts (Discord ID): ``[ID]_SET_DEV_DISCORD_ID_[ID]``  Beispiel: `1234_SET_DEV_DISCORD_ID_123456789012345678`
- Stammdaten setzen: ``[ID]_SET_(NAME|ROLLE|INSTITUTE|COUNTRY|STATE|START|ENDE|EMAIL)_[WERT]``  Beispiel: `1234_SET_NAME_Fritz_Mueller`
- Neuer Mitarbeiter (Onboarding, mit Signup‑Code): ``NEUER_MITARBEITER_[Name_Slug]_CODE_[SignupCode]``  Beispiel: `NEUER_MITARBEITER_Fritz_Mueller_CODE_AB12CD34`
- Urlaubsantrag (Zeitraum): ``[ID]_URLAUBSANTRAG_START_[YYYY]_[MM]_[DD]_ENDE_[YYYY]_[MM]_[DD]``  Beispiel: `1234_URLAUBSANTRAG_START_2025_09_21_ENDE_2025_09_25`

## GO Silent – Ausstempeln ohne Meeting

Wenn du vor dem täglichen Abschluss-Meeting (GO) gehen musst, kannst du **GO Silent** nutzen. Damit stempelst du aus, ohne am Meeting teilzunehmen.

### So funktioniert's:

1. Schreibe eine E-Mail an: **go@nadooit.de**
2. **Betreff:** `GO silent`
3. **Body:** Leer lassen

Das System erkennt die E-Mail und stempelt dich ordnungsgemäß aus, ohne dass du am Meeting teilnehmen musst.

> **Hinweis:** Nutze GO Silent nur, wenn es wirklich notwendig ist. Die täglichen Meetings sind wichtig für den Teamzusammenhalt und die Kommunikation.

<p align="center">
<a href="/docs/01-organisation/README.md"><strong>Zurück</strong></a> | <a href="/docs/01-organisation/02-zeit_und_ausbildungsnachweise/README.md"><strong>Weiter</strong></a>
</p>
