# <p align="center">E-Mail-Clients – Unternehmensrichtlinie</p>

>Dieser Wiki-Eintrag beschreibt, warum wir im Unternehmen E-Mail-Clients anstelle von webbasierten Oberflächen verwenden und wie wir diese künftig standardisiert einsetzen.

---
## Warum ein E-Mail-Client?

>E-Mail-Clients bieten mehrere Vorteile gegenüber browserbasierten Oberflächen:

- **Produktivität:** Schnellere Navigation, Tastenkürzel und einheitliche Oberfläche.

- **Offline-Verfügbarkeit:** E-Mails können gelesen, gesucht und vorbereitet werden, auch ohne Internetverbindung.

- **Erweiterte Suchfunktionen:** Lokale Indexierung ermöglicht sehr schnelle und präzise Suche.

- **Integration:** Einbindung von Kalender, Kontakten und Aufgaben in einer Anwendung.

- **Benachrichtigungen:** Systemweite, zuverlässige E-Mail-Benachrichtigungen.

- **Datensicherheit:** Lokale Speicherung, verschlüsselte Verbindungen und bessere Kontrolle über Daten.

---
### Betterbird ist ein sogenannter E-Mail-Client.

>Anders als webbasierte E-Mail-Anwendungen bietet Betterbird eine lokale, leistungsfähige und erweiterbare Oberfläche für das Verwalten von E-Mails, Kalender und Kontakten.

Betterbird bietet gegenüber anderen E-Mail-Clients:

- **Verbesserte Stabilität:** Schnellere Bereitstellung von Bugfixes als im Thunderbird-Hauptprojekt.

- **Zusätzliche Funktionen:** z. B. mehrzeilige Nachrichtenliste, erweiterte Sortierfunktionen, farbliche Kontenkennzeichnung.

- **Optimiertes Nutzererlebnis:** Verbesserte Bedienbarkeit und modernere Layout-Optionen.
  
- **Kompatibilität:** Voll kompatibel mit Thunderbird-Profilen und Add-ons.

- **Aktivere Weiterentwicklung:** Fokus auf praktische Verbesserungen für den täglichen Einsatz.

---
## Installation

<details><summary> **Windows:** </summary>

1. Installer von der offiziellen Betterbird-Website herunterladen.
<br>
2. Setup ausführen und den Installationsanweisungen folgen.
<br>
3. Betterbird starten und Konto einrichten.
</details>

<details><summary> **macOS:** </summary>

1. DMG-Datei herunterladen.
<br>
2. Betterbird in den Programme-Ordner ziehen.
<br>
3. Anwendung starten.
</details>

<details><summary> **Linux:** </summary>

- **Debian/Ubuntu:** `.deb`-Paket installieren.
<br>
- **Fedora/openSUSE:** `.rpm`-Paket installieren.
<br>
- **Andere Distributionen:** Tarball herunterladen und manuell entpacken.
</details>

---
## Warum Betterbird als Standard-Client ausgewählt wurde

>Betterbird wurde als  E-Mail-Client gewählt, da es in mehreren entscheidenden Bereichen objektive Vorteile gegenüber anderen gängigen Alternativen wie Mailspring, Geary, SeaMonkey, Claws Mail, Evolution, Outlook und eM Client bietet.

### **1. Plattformunterstützung**

> Betterbird ist auf **Windows, macOS und Linux** vollständig gleichwertig verfügbar.
    
- Viele Alternativen haben Einschränkungen:
    
    - **Mailspring**: funktioniert, aber eingeschränkte Protokollunterstützung.
        
    - **Geary**: primär für Linux, Ports auf andere Systeme sind inoffiziell oder unvollständig.
        
    - **Claws Mail**: Linux/Windows, aber macOS nur über komplizierte Wege.
        
    - **Evolution**: praktisch nur Linux.
        
    - **Outlook**: gute Windows-/macOS-Unterstützung, aber keine Linux-Version.
        
    - **eM Client**: nur Windows und macOS.
        
>- → **Betterbird bietet als einziger vollständigere 3-Plattform-Unterstützung ohne funktionale Nachteile.**


### **2. Sicherheit, Protokolle und Funktionsumfang**

Betterbird bietet im Unternehmensumfeld vor allem folgende Vorteile:

- **Sicherheit:** Native OpenPGP-Unterstützung, S/MIME, strikte TLS-Vorgaben und blockierte Remote-Inhalte sorgen für eine sichere Kommunikation.
- **Protokoll- & Server-Unterstützung:** Unterstützung aller gängigen Protokolle (IMAP, SMTP, POP3) sowie Kalender- und Adressbuchprotokolle (CalDAV, CardDAV) ermöglicht den Einsatz in verschiedensten Umgebungen.
- **Funktionsumfang:** Integrierter Kalender, Aufgabenverwaltung, Add-ons, Offline-Fähigkeit, leistungsstarke Suche, Mehrkontenverwaltung, lokale Archivierung und flexible Filterregeln machen Betterbird zu einem vollwertigen E-Mail-Client für den professionellen Einsatz.

Im Vergleich zu vielen Alternativen bietet Betterbird damit ein sehr ausgewogenes Paket aus Sicherheit, Funktionsumfang und Flexibilität – ohne zusätzliche Kosten.

---
## Richtlinien für die Nutzung von E-Mail-Clients

- **Verschlüsselte Kommunikation:** Nutzung von SSL/TLS für IMAP, SMTP und Kalenderdienste ist verpflichtend.
    
- **Passwortsicherheit:** Passwörter müssen den Unternehmensrichtlinien entsprechen und sollen im Passwortmanager gespeichert werden.
    
- **Zertifikate:** Falls erforderlich, müssen Firmenzertifikate eingebunden und vertraut werden.
    
- **DSGVO:** Lokale Daten auf Geräten müssen verschlüsselt sein; Weitergabe von E-Mails an externe Empfänger darf nur gemäß Datenschutzrichtlinien erfolgen.
    
- **Regelmäßige Updates:** Der Client muss stets aktuell gehalten werden, um Sicherheitslücken zu vermeiden.

---
<p align="center">
<a href="/docs/05-kommunikation/03-bekannte_probleme/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/05-kommunikation/README.md/#dieser-themenbereich-beinhaltet-folgende-themen"><strong>Zurück zur Themen-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>
