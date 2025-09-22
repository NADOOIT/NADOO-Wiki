# <p align="center">Einrichtung und Konfiguration</p>

---
<!-- Kapitel Einrichtung und Konfiguration -->

## Lokale Entwicklungsumgebung (z. B. mit LocalWP oder Docker)

Für die Entwicklung mit WordPress empfiehlt sich eine lokale Umgebung, um unabhängig vom Live-Server arbeiten zu können.
Tools wie **LocalWP** ermöglichen eine schnelle Einrichtung mit grafischer Oberfläche, während **Docker** flexible und automatisierbare Setups bietet.
Beide Varianten eignen sich gut für Tests, Plugin-Entwicklung und Theme-Anpassungen.

---

## WordPress installieren & konfigurieren

Nach dem Einrichten der lokalen Umgebung erfolgt die Installation von WordPress. Bei LocalWP genügt meist ein Klick, um eine neue Site anzulegen. Bei Docker erfolgt die Einrichtung in der Regel über ein `docker-compose.yml`-File, das Webserver, PHP und Datenbank konfiguriert.

Nach der Installation:

- Aufruf der Installationsroutine im Browser
- Auswahl der Sprache, Festlegen von Website-Titel, Benutzername und Passwort
- Verbindung zur Datenbank einrichten (bei Docker manuell, bei LocalWP automatisch)

Anschließend kann das WordPress-Dashboard genutzt und mit der Konfiguration begonnen werden.

---

## Sicherheitseinstellungen (Updates, Passwörter, Plugins)

**WordPress-Websites sind häufig Ziel von Angriffen ❗** – daher ist die richtige Konfiguration entscheidend:

- **Updates**
  - Regelmäßige Aktualisierung von WordPress-Core, Themes und Plugins
  - Automatische Updates aktivieren, wenn möglich

- **Passwörter und Benutzerkonten**
  - Sichere Passwörter für Admin-Accounts verwenden (mind. 12 Zeichen, Sonderzeichen, keine Namen)
  - Zwei-Faktor-Authentifizierung (2FA) aktivieren, z. B. über Plugin wie "WP 2FA"

- **Plugins**
  - Nur Plugins aus vertrauenswürdigen Quellen verwenden
  - Regelmäßige Plugin-Checks auf Aktualität und Sicherheitslücken
  - Nicht benötigte Plugins vollständig entfernen

Weitere Sicherheitsmaßnahmen wie Firewalls, Login-Schutz oder IP-Sperren können über Sicherheitsplugins wie "Wordfence" oder "iThemes Security" ergänzt werden.

---

**Dieser Themenbereich beinhaltet folgende Themen:**
---

🔹 [**Einführung**](/docs/06-entwicklung/08-cms/01-einfuehrung/README.md)<br>
🔹 [**WP-Grundlagen**](/docs/06-entwicklung/08-cms/02-wp_grundlagen/README.md) <br>
🔹 [**Einrichtung**](/docs/06-entwicklung/08-cms/03-einrichtung/README.md) <br>
🔹 [**Inhalt Struktur**](/docs/06-entwicklung/08-cms/04-inhalt_struktur/README.md) <br>
🔹 [**Erweiterungen und Plugins**](/docs/06-entwicklung/08-cms/05-erweiterung_plugins/README.md) <br>
🔹 [**Design Themes**](/docs/06-entwicklung/08-cms/06-design_themes/README.md) <br>
🔹 [**Prüfungsvorbereitung**](/docs/06-entwicklung/08-cms/07-pruefungsvorbereitung/README.md) <br>
🔹 [**Tools und Ressourcen**](/docs/06-entwicklung/08-cms/08-tools_ressourcen/README.md) <br>

---

<p align="center">
📅 <strong>Dieses Dokument wurde bearbeitet am:</strong> 19.09.2025
<br>
✍️ <strong>Von:</strong> <a href="https://github.com/johkori">Johkori(Tim H.)</a> (GitHub)
</p>

---

<p align="center">
<a href="/docs/06-entwicklung/08-cms/02-wp_grundlagen/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/08-cms/04-inhalt_struktur/README.md"><strong>Weiter</strong></a>
</p>
