# <p align="center">Installation und Erstellung der virtuellen Umgebung</p>

---

## Installation von Python 3.11 mit uv

1. Öffne das Terminal in Visual Studio Code (View > Terminal oder ``Ctrl+` ``).

2. Installiere uv:

   Für macOS und Linux:
   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

   Für Windows (in PowerShell):
   ```powershell
   Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

   ```powershell
   irm https://astral.sh/uv/install.ps1 | iex
   ```

3. Installiere Python 3.11:
   ```bash
   uv python install 3.11
   ```

4. Überprüfe die Installation:
   ```bash
   uv python --version
   ```

---

## Erstellen einer virtuellen Umgebung

1. Erstelle eine virtuelle Umgebung:
   ```bash
   uv venv -p 3.11
   ```

2. Aktiviere die virtuelle Umgebung:

   Für macOS und Linux:
   ```bash
   source .venv/bin/activate
   ```

   Für Windows:
   ```bash
   .\.venv\Scripts\activate
   ```

---

**Dieses Thema beinhaltet folgende Kapitel:**
---

🔹 [**Virtuelle Umgebungen**](/docs/04-tools/06-ki/01-leitfaden/README.md) </br>
🔹 [**Installation**](/docs/04-tools/06-ki/01-leitfaden/README.md) </br>
🔹 [**Grundkonzept (Beispiel)**](/docs/04-tools/06-ki/01-leitfaden/README.md) </br>

---

<p align="center">
<a href="/docs/06-entwicklung/04-python/01-einstieg/01-virtuelle_umgebungen/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/04-python/01-einstieg/03-grundkonzept_bsp/README.md"><strong>Weiter</strong></a>
</p>