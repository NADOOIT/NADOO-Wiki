> Muss einsortiert werden. Bezug auf Issue [#699](https://github.com/NADOOIT/NADOO-Launchpad/issues/699#issuecomment-2682854794) Im Launchpad Repo

# PowerShell-Befehl: `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`

## 1. Erklärung der einzelnen Teile
- **`Set-ExecutionPolicy`**  
  → Ändert die Richtlinie für die Ausführung von PowerShell-Skripten.  

- **`RemoteSigned`**  
  → Erlaubt lokale Skripte **ohne** Signatur, aber heruntergeladene Skripte müssen **digital signiert** sein.  

- **`-Scope CurrentUser`**  
  → Die Änderung gilt **nur** für den aktuellen Benutzer (keine Adminrechte nötig).  

---

## 2. Was bewirkt dieser Befehl?
Er erlaubt die **Ausführung von PowerShell-Skripten**, aber mit einer Einschränkung:
- **Lokale Skripte** (die du selbst erstellt hast) können **ohne Einschränkung** ausgeführt werden.
- **Skripte aus dem Internet** (heruntergeladen) müssen **signiert** sein, um ausgeführt zu werden.

Dies schützt vor **ungewollter oder unsicherer Skriptausführung**, aber erlaubt dir trotzdem, eigene Skripte zu nutzen.

---

## 3. Sicherheitsrisiko
- Wenn du **"Unrestricted"** setzen würdest, könnten **alle** Skripte (auch unsignierte) ausgeführt werden – das wäre gefährlich.  
- **"RemoteSigned"** ist ein sicherer Mittelweg für Entwickler und Administratoren.  
- Falls du ein heruntergeladenes Skript ohne Signatur ausführen willst, kannst du PowerShell mitteilen, dass du dem Skript vertraust, indem du es mit:
  ```powershell
  Unblock-File -Path C:\Pfad\zum\Skript.ps1```
entsperrst.

---

## 4. Alternative Execution Policies
Falls du es noch restriktiver oder offener einstellen willst, gibt es weitere Optionen:

   - `Restricted` → Standardwert, blockiert alle Skripte (nur interaktive Befehle erlaubt).
   - `AllSigned` → Alle Skripte müssen signiert sein (auch selbst erstellte).
   - `Unrestricted` → Alle Skripte werden ohne Einschränkung ausgeführt (nicht empfohlen!).

---

## 5. Solltest du diesen Befehl ausführen?
Ja, wenn du eigene PowerShell-Skripte ausführen möchtest, aber trotzdem eine Grundsicherheit gegen unsignierte, aus dem Internet heruntergeladene Skripte behalten willst.

Falls du Skripte von Drittanbietern nutzt, prüfe immer die Quelle und den Code, bevor du sie ausführst! 