# <p align="center">KI‐Nutzung: Ein umfassender Leitfaden</p>

Willkommen zu unserem Wiki-Artikel über die Nutzung von Künstlicher Intelligenz (KI). Dieser Leitfaden bietet einen Überblick über verschiedene KI-Tools und -Plattformen, ihre Anwendungen und Besonderheiten. Von API-basierten Diensten bis hin zu lokalen Modellen werden wir die wichtigsten Aspekte der KI-Nutzung beleuchten.

## Inhalte

1. **ChatGPT API**
   - Standard für KI-Interaktionen
   - Implementierung und Beispiele

2. **Lokale Modelle mit Ollama**
   - Vorteile und Einschränkungen
   - Verwendung ohne API-Schlüssel

3. **Modelle und Ressourcen**
   - Hugging Face als Modell-Quelle
   - GUI-Steuerung mit OmniParser

4. **Spezielle KI-Anwendungen**
   - Sprache zu Text
   - Text zu Sprache
   - Text zu Bild
   - Text zu Video

## Detaillierte Erklärungen

### 1. ChatGPT API
Die ChatGPT API von OpenAI hat sich als Standard für KI-gestützte Interaktionen etabliert. Sie bietet eine leistungsstarke Schnittstelle für die Integration von KI-Funktionen in verschiedene Anwendungen.

**Implementierung:**
```python
import openai

openai.api_key = 'Ihr-API-Schlüssel'

response = openai.ChatCompletion.create(
  model="gpt-4o-mini",
  messages=[
    {"role": "user", "content": "Hallo, wie geht es dir?"}
  ]
)

print(response.choices[0].message.content)
```

Dieses Beispiel zeigt, wie man eine einfache Anfrage an die ChatGPT API sendet und die Antwort erhält[1].

### 2. Lokale Modelle mit Ollama
Ollama ermöglicht die Nutzung von KI-Modellen lokal, ohne die Notwendigkeit eines API-Schlüssels. Dies bietet Vorteile in Bezug auf Datenschutz und Offline-Nutzung, jedoch mit Einschränkungen bei der Leistungsfähigkeit im Vergleich zu cloud-basierten Lösungen.

**Verwendung:**
1. Installiere Ollama von [ollama.com](https://ollama.com/)
2. Lade ein Modell herunter: `ollama pull mistral`
3. Starte eine Konversation: `ollama run mistral`

### 3. Modelle und Ressourcen
[Hugging Face](https://huggingface.co/) ist eine zentrale Plattform für das Herunterladen und Teilen von KI-Modellen. Es bietet eine breite Palette von vortrainierten Modellen für verschiedene Aufgaben[5].

**GUI-Steuerung mit OmniParser:**
OmniParser von Microsoft ist ein umfassendes Tool zur Analyse von Benutzeroberflächen-Screenshots. Es konvertiert UI-Screenshots in eine strukturierte Darstellung der interaktiven Elemente und ihrer Funktionen[1][3]. OmniParser besteht aus zwei Hauptkomponenten:

1. Ein Detektionsmodell zur Erkennung interaktiver Bereiche
2. Ein Captioning-Modell zur Beschreibung der Funktionalität der erkannten Elemente

OmniParser verbessert signifikant die Fähigkeit von Modellen wie GPT-4V, präzise Aktionen auf Benutzeroberflächen auszuführen[1].

### 4. Spezielle KI-Anwendungen

#### Sprache zu Text
Das Whisper-Modell von OpenAI ist ein leistungsfähiges Tool für die Umwandlung von Sprache in Text:

```python
import whisper

model = whisper.load_model("base")
result = model.transcribe("audio.mp3")
print(result["text"])
```

#### Text zu Sprache
Die Coqui TTS-Bibliothek ermöglicht die Generierung von Sprache aus Text:

```python
from TTS.api import TTS

tts = TTS("tts_models/de/thorsten/tacotron2-DDC")
tts.tts_to_file(text="Hallo, dies ist ein Test.", file_path="output.wav")
```

#### Text zu Bild

OmniGen ist ein fortschrittliches Modell für einheitliche Bildgenerierung, das eine Vielzahl von Bildgenerierungsaufgaben in einem einzigen Framework bewältigen kann. Hier ist ein Beispiel für die Verwendung:

```python
from OmniGen import OmniGenPipeline

pipe = OmniGenPipeline.from_pretrained("Shitao/OmniGen-v1")

# Text zu Bild
images = pipe(
    prompt="Ein futuristisches Stadtbild bei Nacht mit fliegenden Autos",
    height=1024,
    width=1024,
    guidance_scale=2.5,
    seed=0,
)
images[0].save("futuristische_stadt.png")

# Multimodal zu Bild
images = pipe(
    prompt="Ein Mann in einem schwarzen Hemd liest ein Buch. Der Mann ist der rechte Mann in <img><|image_1|></img>.",
    input_images=["./pfad/zum/bild/zwei_männer.jpg"],
    height=1024,
    width=1024,
    guidance_scale=2.5,
    img_guidance_scale=1.6,
    seed=0
)
images[0].save("lesender_mann.png")
```

OmniGen zeichnet sich durch folgende Eigenschaften aus:

1. **Vielseitigkeit**: Es unterstützt nicht nur Text-zu-Bild-Generierung, sondern auch Bildbearbeitung, subjektgesteuerte Generierung und bildbedingte Generierung.

2. **Einfachheit**: Keine zusätzlichen Plugins oder Operationen sind erforderlich. OmniGen kann automatisch die erforderlichen Merkmale (z.B. Objekte, menschliche Posen, Tiefenkarten) in Eingabebildern entsprechend dem Textprompt identifizieren.

3. **Flexibilität**: Du kannst mehrere Bilder als Eingabe und einfache, allgemeine Sprache verwenden, um auf Objekte in diesen Bildern zu verweisen.

OmniGen vereinfacht den Workflow der Bildgenerierung erheblich und repräsentiert einen bedeutenden Schritt in Richtung eines universellen Bildgenerierungsmodells. Es ist besonders nützlich für komplexe Aufgaben, die normalerweise mehrere spezialisierte Modelle erfordern würden.

Citations:
[1] https://github.com/staoxiao/OmniGen

#### Text zu Video
Die Erstellung von Videos aus Textbeschreibungen ist dank der Kombination zweier GitHub-Repositories einfacher geworden:

1. [NADOOITChristophBa/models](https://github.com/NADOOITChristophBa/models)
2. [NADOOITChristophBa/ComfyUI-MochiWrapper](https://github.com/NADOOITChristophBa/ComfyUI-MochiWrapper)

Diese Tools ermöglichen es, Text-zu-Video-Konvertierungen mit relativ geringem Aufwand durchzuführen[3][4].


#### Text zu Bild und Audio mit Hallo

https://github.com/fudan-generative-vision/hallo

Hallo ist ein fortschrittliches Projekt, das es ermöglicht, statische Bilder mit Audiodateien zu kombinieren, um den Eindruck zu erwecken, dass das Bild spricht. Hier ist eine umfassende Anleitung zur Verwendung von Hallo:

1. **Installation und Einrichtung**

```bash
git clone https://github.com/fudan-generative-vision/hallo.git
cd hallo
conda create -n hallo python=3.10
conda activate hallo
pip install -r requirements.txt
pip install .
apt-get install ffmpeg
git lfs install
git clone https://huggingface.co/fudan-generative-ai/hallo pretrained_models
```

2. **Ausführung der Inferenz**

Für eine einfache Inferenz kannst du folgenden Befehl verwenden:

```bash
python scripts/inference.py --source_image examples/reference_images/1.jpg --driving_audio examples/driving_audios/1.wav
```

Für mehr Kontrolle über den Prozess kannst du zusätzliche Parameter verwenden:

```bash
python scripts/inference.py \
  --source_image path/to/image.jpg \
  --driving_audio path/to/audio.wav \
  --output output_video.mp4 \
  --pose_weight 0.5 \
  --face_weight 0.5 \
  --lip_weight 1.0 \
  --face_expand_ratio 1.2
```

3. **Vorbereitung der Trainingsdaten**

Wenn du Hallo mit eigenen Daten trainieren möchtest, folge diesen Schritten:

a. Organisiere deine Videos mit Hilfe folgender Struktur:
```
dataset_name/
|-- videos/
    |-- 0001.mp4
    |-- 0002.mp4
    |-- ...
```

b. Verarbeite die Videos:
```bash
python -m scripts.data_preprocess --input_dir dataset_name/videos --step 1
python -m scripts.data_preprocess --input_dir dataset_name/videos --step 2
```

c. Generiere Metadaten:
```bash
python scripts/extract_meta_info_stage1.py -r path/to/dataset -n dataset_name
python scripts/extract_meta_info_stage2.py -r path/to/dataset -n dataset_name
```

4. **Training**

a. Aktualisiere die Datenpfade in den Konfigurationsdateien `configs/train/stage1.yaml` und `configs/train/stage2.yaml`.

b. Starte das Training:
```bash
accelerate launch -m \
  --config_file accelerate_config.yaml \
  --machine_rank 0 \
  --main_process_ip 0.0.0.0 \
  --main_process_port 20055 \
  --num_machines 1 \
  --num_processes 8 \
  scripts.train_stage1 --config ./configs/train/stage1.yaml
```

5. **Integration in Python-Code**

Für eine einfache Integration in bestehende Python-Projekte kannst du folgende Funktion verwenden:

```python
import subprocess

def run_hallo(image_path, audio_path, output_path):
    command = [
        "python", "scripts/inference.py",
        "--source_image", image_path,
        "--driving_audio", audio_path,
        "--output", output_path
    ]
    subprocess.run(command, check=True)

# Beispielaufruf
run_hallo("path/to/image.jpg", "path/to/audio.wav", "output_video.mp4")
```

Beachte die Anforderungen an das Eingabebild und die Audiodatei:
- Das Bild sollte quadratisch zugeschnitten sein, mit dem Gesicht als Hauptfokus (50-70% des Bildes).
- Das Gesicht sollte frontal ausgerichtet sein, mit einem Rotationswinkel von weniger als 30°.
- Die Audiodatei muss im WAV-Format vorliegen und klare englische Sprache enthalten.

Hallo eröffnet faszinierende Möglichkeiten für die Erstellung von animierten Präsentationen, virtuellen Sprechern oder kreativen Multimedia-Projekten. Mit der Möglichkeit des eigenen Trainings kannst du das Modell an deine spezifischen Bedürfnisse anpassen.

---

## Aufgabe: Experimentieren mit KI-Tools

1. Implementiere das ChatGPT API-Beispiel und stelle eine eigene Frage.
2. Installiere Ollama und führe ein lokales Modell aus.
3. Lade ein Modell von Hugging Face herunter und experimentiere damit.
4. Versuche, mit einem der speziellen KI-Anwendungsbeispiele zu arbeiten (z.B. Text-zu-Sprache).

---

## Dokumentation und Fragen

Während du mit diesen KI-Tools experimentierst, notiere deine Erfahrungen und Fragen. Erstelle für jede wichtige Erkenntnis oder Herausforderung ein separates Issue in unserem Repository. Dies hilft nicht nur dir, sondern verbessert auch die Dokumentation für zukünftige Nutzer.

---

## Ziel

Nach Abschluss dieser Übungen wirst du ein grundlegendes Verständnis verschiedener KI-Anwendungen und -Tools haben. Du wirst in der Lage sein, KI-Modelle für verschiedene Aufgaben zu nutzen und die Vor- und Nachteile verschiedener Ansätze zu verstehen.

Viel Erfolg beim Erkunden der faszinierenden Welt der KI-Nutzung!

PS: 

Wenn du genauer wissen willst, wie KI funktioniert, ist folgendes Video empfehlenswert:

https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=1

---

### Quellen:
[1] https://www.microsoft.com/en-us/research/articles/omniparser-for-pure-vision-based-gui-agent/
[2] https://huggingface.co/papers/2408.00203
[3] https://microsoft.github.io/OmniParser/
[4] https://huggingface.co/microsoft/OmniParser
[5] https://arxiv.org/abs/2408.00203
[6] https://www.youtube.com/watch?v=KOHfJprfN60
[7] https://openaccess.thecvf.com/content/CVPR2024/papers/Wan_OmniParser_A_Unified_Framework_for_Text_Spotting_Key_Information_Extraction_CVPR_2024_paper.pdf
[8] https://www.psychology.hu-berlin.de/de/prof/ingpsy/inpsy_old/forschung/tools/literatur/fuhrmann-2010-entwicklung-eines-gui-fur-die-konfiguration-der-software-komponente-zur-systemprozessuberwachung-und-kontrolle-in-einer-psychologischen-versuchsumgebung.pdf


---

**Dieses Thema beinhaltet folgende Kapitel:**
---

🔹 [**Leitfaden KI**](/docs/04-tools/06-ki/01-leitfaden/README.md) </br>
🔹 [**LLM-Mix**](/docs/04-tools/06-ki/02-llm-mlx/README.md) </br>
🔹 [**Gemini**](/docs/04-tools/06-ki/03-gemini/README.md) </br>

---

<p align="center">
<a href="/docs/04-tools/07-ki/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/07-ki/02-llm-mlx/README.md"><strong>Weiter</strong></a>
</p>