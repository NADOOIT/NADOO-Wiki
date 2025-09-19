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

### Kostenloses Kontingent (Free Tier)

- **Monatliches Limit:** Bis zu 1.000.000 Tokens pro Monat (prüfe die genauen Zahlen in der [offiziellen Dokumentation](https://ai.google.dev/gemini-api/docs/pricing?hl=de)).
- **Einsatzgebiet:** Geeignet für Entwicklung, Prototyping und kleinere Anwendungen.

### Ratenlimits im Free Tier

| Modell                | Anfragen pro Minute (RPM) | Tokens pro Minute (TPM) | Anfragen pro Tag (RPD) |
|-----------------------|---------------------------|--------------------------|------------------------|
| Gemini 2.0 Flash      | 15                        | 1.000.000                | 1.500                  |
| Gemini 2.0 Flash-Lite | 30                        | 1.000.000                | 1.500                  |
| Gemini 1.5 Flash      | 15                        | 1.000.000                | 1.500                  |

*Hinweis: Die genauen Limits können je nach Modell variieren. Für aktuelle Informationen konsultiere bitte die [offizielle Dokumentation](https://ai.google.dev/gemini-api/docs/rate-limits?hl=de).*

Diese Anleitung basiert auf Informationen aus der [offiziellen Gemini API-Dokumentation](https://ai.google.dev/gemini-api/docs/api-key?hl=de) und den [Preisinformationen](https://ai.google.dev/gemini-api/docs/pricing?hl=de).

---

**Dieses Thema beinhaltet folgende Kapitel:**
---

🔹 [**Leitfaden KI**](/docs/04-tools/06-ki/01-leitfaden/README.md) </br>
🔹 [**LLM-Mix**](/docs/04-tools/06-ki/02-llm-mlx/README.md) </br>
🔹 [**Gemini**](/docs/04-tools/06-ki/03-gemini/README.md) </br>

---
<p align="center">
📅 <strong>Dieses Dokument wurde bearbeitet am:</strong> 19.09.2025
<br>
✍️ <strong>Von:</strong> <a href="https://github.com/johkori">Johkori(Tim H.)</a> (GitHub)
</p>

---

<p align="center">
<a href="/docs/04-tools/06-ki/02-llm-mlx/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/05-kommunikation/README.md"><strong>Weiter</strong></a>
</p>
