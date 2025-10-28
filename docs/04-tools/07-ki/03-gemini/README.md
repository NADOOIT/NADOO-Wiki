# <p align="center">Nutzung der Gemini API – eine Anleitung</p>

Die Gemini API von Google ermöglicht Entwicklern den Zugriff auf fortschrittliche KI-Funktionen. Diese Anleitung bietet eine Übersicht zur Einrichtung und Nutzung der API, einschließlich Informationen zur Authentifizierung mittels API-Schlüssel, den verfügbaren kostenlosen Nutzungskontingenten und den entsprechenden Limits.

## 1. API-Schlüssel anfordern und einrichten

### Registrierung und API-Schlüssel erhalten

Um die Gemini API zu verwenden, benötigst du einen API-Schlüssel:

- **Registrierung**: Melde dich im [Google AI Studio](https://aistudio.google.com/) an.
- **API-Schlüssel erstellen**: Navigiere zu deinen Projekteinstellungen und generiere einen neuen API-Schlüssel.

### API-Schlüssel sicher aufbewahren

Es ist essenziell, deinen API-Schlüssel vertraulich zu behandeln:

- **Nicht im Code hinterlegen**: Vermeide es, den Schlüssel direkt im Quellcode zu speichern.
- **Umgebungsvariablen nutzen**: Speichere den Schlüssel in Umgebungsvariablen oder sicheren Konfigurationsdateien.

**Beispiel für Linux/macOS (Bash):**

```bash
export GEMINI_API_KEY=Dein_API_Schlüssel
```

**Beispiel für Windows:**

1. **Umgebungsvariable erstellen:**
   - Suche in den Systemeinstellungen nach "Umgebungsvariablen".
   - Erstelle eine neue Benutzervariable mit:
     - **Name:** `GEMINI_API_KEY`
     - **Wert:** Dein API-Schlüssel

## 2. Kostenlose Nutzung und Limits

Die Gemini API bietet ein kostenloses Nutzungskontingent (Free Tier), das ideal für Tests und kleinere Projekte geeignet ist.

- **Einsatzgebiet:** Geeignet für Entwicklung, Prototyping und kleinere Anwendungen.

### Ratenlimits im Free Tier

| Modell                | Anfragen pro Minute (RPM) | Tokens pro Minute (TPM) | Anfragen pro Tag (RPD) |
|-----------------------|---------------------------|--------------------------|------------------------|
| Gemini 2.0 Flash      | 15                        | 1.000.000                | 200                    |
| Gemini 2.0 Flash-Lite | 30                        | 1.000.000                | 200                    |
| Gemini 2.5 Pro        | 2                         | 125.000                  | 50                     |
| Gemini 2.5 Flash      | 10                        | 250.000                  | 250                    |
| Gemini 2.5 Flash-Lite | 15                        | 250.000                  | 1000                   |

*Hinweis: Die genauen Limits können je nach Modell variieren. Für aktuelle Informationen besuche: [offizielle Dokumentation]([https://ai.google.dev/gemini-api/docs/rate-limits?hl=de](https://ai.google.dev/gemini-api/docs/rate-limits?utm_source=chatgpt.com&hl=de#current-rate-limits)).*

Diese Anleitung basiert auf Informationen aus der [offiziellen Gemini API-Dokumentation](https://ai.google.dev/gemini-api/docs/api-key?hl=de) und den [Preisinformationen](https://ai.google.dev/gemini-api/docs/pricing?hl=de).

---

<p align="center">
<a href="/docs/04-tools/07-ki/02-llm-mlx/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/05-kommunikation/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/07-ki/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zur Kapitel-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
