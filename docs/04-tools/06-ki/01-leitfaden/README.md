# <p align="center">Launchpad AI-Funktionen</p>

---

<p align="center">Dieser Beitrag ist durch eine KI generiert.</p>

---

# Launchpad Wiki: AI-Funktionen – Kurzleitfaden
Dieser Artikel gibt einen prägnanten Überblick über die AI-Funktionen im Launchpad, mit Fokus auf get_text_for_prompt_local_with_llama und die Prompt-Naming-Conventions. Er dient als schneller Praxis-Leitfaden.

---

## Ziel der Funktion
get_text_for_prompt_local_with_llama ermöglicht lokale Textgenerierung über llama-cpp (GGUF-Modelle). Sie unterstützt klassische Completions, Chat, strukturierte JSON-Ausgaben sowie toolgestützte Function Calls – ohne Cloud-Abhängigkeit.

---

## Kernfähigkeiten
- Modi: completion, chat, json, json_schema, function_call
- Steuerung: max_tokens, temperature, top_p, top_k, repeat_penalty, stop, stream
- Chat-Kontext: system + messages, optionales chat_format (z. B. llama-2, chatml)
- Strukturierte Antworten: response_format (JSON/Schema)
- Tools: Übergabe von tools für function_call
- Performance: n_gpu_layers, Kontextfenster, Batch, Mirostat (optional)
- Modellverwaltung: lädt lokales GGUF-Modell per Modelldateiname

---

## Wann welchen Modus verwenden
- completion: Freitext-Vervollständigung, Ein-Prompt.
- chat: Mehrturn-Dialog, Rollen (system/user/assistant).
- json / json_schema: Erzwingt strukturierte, maschinenlesbare Ausgaben.
- function_call: Lässt das Modell Funktionen/Tools vorschlagen/aufrufen.

---

## Minimalbeispiele (Pseudocode)
- Completion: kurzer Prompt, optional Stop-Sequenzen für saubere Abschlüsse.
- Chat: system festlegt Verhalten, messages hält Verlauf.
- JSON: response_format vorgeben, um Schlüssel/Typen zu sichern.
- Function Call: tools bereitstellen, Ergebnis aus message/Tool-Aufruf auswerten.

---

## Empfohlene Parameter-Defaults
- max_tokens: 256–512 für Antworten, 64–128 für kurze Extraktionen.
- temperature: 0.2–0.7 (niedriger = präziser, höher = kreativer).
- top_p: 0.9–0.95; top_k: 40–100; repeat_penalty: 1.05–1.2.
- stop: bei completion definieren (z. B. Zeilenumbruch oder Trennmarker).

---

## Prompt-Naming-Conventions (Leitfaden)
Konsistente Namen erleichtern Wiederverwendung, Automatisierung und Tests. Empfohlenes Schema:
- Kategorie: Zweck oder Domäne (dev, docs, test, ux, data, codegen)
- Kontext: Ziel oder Input-Quelle (cli, api, file, element)
- Modus: output- oder Interaktionsform (completion, chat, json, fc für function_call)
- Ziel: gewünschter Output-Typ (summary, plan, fix, schema, extract, critique)

Format:
- snake_case für interne Bezeichner, kebab-case für Dateinamen.
- Präfixe für Modalität: chat_, json_, fc_, plain_
- Suffixe für Output-Typen: _summary, _schema, _extract, _plan, _steps

Beispiele:
- chat_docs_summary
- json_code_review_schema
- fc_cli_action_select
- plain_dev_fix_suggestion

Tipps:
- Ein Prompt = ein klarer Job (Atomicität).
- Explizite Constraints (Formate, Längen, Stil).
- Trennmarker für Abschnitte (z. B. === Kontext ===).
- Bei JSON: Schlüssel und Typen knapp, deterministisch.

---

## Best Practices für zuverlässige Outputs
- Rolle definieren: system nutzen, um Verhalten/Regeln zu fixieren.
- Beispiele minimieren, aber repräsentativ halten.
- Output-Validierung: bei JSON stets prüfen (Parser/Schema).
- Streaming nur für UI/Progress, final dennoch sammeln/prüfen.
- Stop-Sequenzen nutzen, um „Ausschwingen“ zu vermeiden.
- Kleines Temperatur-Tuning zuerst (0.3–0.5), dann top_p/top_k.

---

## Performance- und Modellhinweise
- n_gpu_layers je nach Hardware erhöhen (schneller, aber VRAM-abhängig).
- Kontextlänge (n_ctx) passend zum Use Case (lange Chats vs. kurze Tasks).
- Batch und verbose nur bei Bedarf anpassen.
- Modellwahl: kleine Modelle für Utility/Extraktion, größere für komplexe Aufgaben.

---

## Qualitätssicherung im Projektfluss
- Prompts als wiederverwendbare Artefakte benennen/versionieren.
- Unit-Tests für deterministische Aufgaben (json/json_schema).
- Logging der Parameter (temperature, top_p, Modellpfad) für Reproduzierbarkeit.
- Dokumentiere die beabsichtigte Ein-/Ausgabe je Prompt-Namen.

---

## Troubleshooting (kurz)
- Leere Ausgabe: max_tokens erhöhen, stop prüfen.
- Halluzinationen: temperature senken, Constraints präzisieren.
- Ungültiges JSON: kürzere Antworten, strengeres response_format, geringere Temperatur.
- Langsamkeit: n_gpu_layers erhöhen, kleineres Modell testen, Kontext kürzen.

---

## Checkliste vor dem Einsatz
- Klarer Modus gewählt?
- Prompt nach Naming-Conventions benannt?
- System- und Stop-Regeln gesetzt?
- Strukturierter Output nötig? → json/json_schema + response_format
- Tools vorbereitet? → function_call + tools
- Parameter geloggt? → Reproduzierbarkeit sichern

Für Rückfragen oder Erweiterungen: Siehe Projektdokumentation (Guides, Concepts, Dev-Docs) und integrierte Test- und Logging-Mechanismen. Mein Name ist AI Assistant.

---

**Dieses Thema beinhaltet folgende Kapitel:**
---

🔹 [**Leitfaden KI**](/docs/04-tools/06-ki/01-leitfaden/README.md) </br>
🔹 [**LLM-Mix**](/docs/04-tools/06-ki/02-llm-mlx/README.md) </br>
🔹 [**Gemini**](/docs/04-tools/06-ki/03-gemini/README.md) </br>

---

<p align="center">
<a href="/docs/04-tools/06-ki/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/06-ki/02-llm-mlx/README.md"><strong>Weiter</strong></a>
</p>