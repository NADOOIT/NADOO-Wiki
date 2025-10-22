# <p align="center">Windsurf: Datenschutz, Sicherheit und Datenhaltung</p>

### 📃 Einleitung: Windsurf als KI-Native IDE

Windsurf positioniert sich als einer der weltweit fortschrittlichsten **KI-Code-Assistenten** für Entwickler und Unternehmen und gilt als die erste AI-native IDE, die darauf ausgelegt ist, Entwickler im sogenannten "**Flow**"-Zustand zu halten. 

Diese fortschrittliche Nutzung **generativer Künstlicher Intelligenz** direkt in der Entwicklungsumgebung markiert einen signifikanten Paradigmenwechsel, der neue und erhöhte Anforderungen an die Vertraulichkeit von Quellcode, **geistigem Eigentum (IP)** und proprietären Daten stellt. Die Fähigkeit der IDE, tiefgreifendes Kontextverständnis der Codebasis zu erlangen, erfordert einen ständigen Datenfluss, der strenge Sicherheits- und **Datenschutzmechanismen** zwingend notwendig macht.

---

### Regulatorische Verpflichtungen und Governance

Das Unternehmen **Exafunction, Inc.**, welches hinter Windsurf steht, betont die Wichtigkeit von Transparenz und umfassenden Sicherheitsansätzen, insbesondere angesichts der Handhabung kritischen geistigen Eigentums von Einzelpersonen und Großunternehmen.

Die Bereitstellung von dedizierten Rechenzentren innerhalb Europas, speziell in **Frankfurt, Deutschland**, impliziert die direkte Anwendung und Einhaltung europäischer Datenschutzgesetze wie der **Datenschutz-Grundverordnung (DSGVO)**. Das Bekenntnis zu Governance und Compliance, einschließlich Zertifizierungen wie **SOC 2 Type II** und **FedRAMP High**, dient als Grundlage, um Vertrauen bei regulierten Unternehmen aufzubauen.

---

### Balance zwischen KI-Flow und Datensouveränität

Der zentrale Konflikt, der bei KI-gestützten Entwicklungsumgebungen entsteht, liegt in der Notwendigkeit, den vollständigen Code-Kontext in Echtzeit bereitzustellen, um einen nahtlosen "**Flow**" der KI-Unterstützung zu gewährleisten, während gleichzeitig sichergestellt werden muss, dass dieser sensitive Code **nicht persistent gespeichert** oder zur nachträglichen Schulung der KI-Modelle verwendet wird. Die Lösung dieses Konflikts wird technisch durch das **Zero-Data Retention (ZDR)-Modell** definiert.

Die Architektur des ZDR-Modus und die Wahl des Deployment-Tiers (**Cloud, Hybrid oder Self-Hosted**) sind daher die wichtigsten Prüfpunkte für Organisationen, die Windsurf in sensiblen oder regulierten Umgebungen einführen möchten. Die technische Integrität des ZDR-Mechanismus ist die primäre Voraussetzung für die Wahrung der **Datensouveränität** in Cloud-basierten Deployments.

---

### 🛡️ Sicherheitsarchitektur und Zertifizierungen (Sicherheitspostur)

### Compliance-Zertifizierungen und Audits

Die formelle Sicherheitspostur von Windsurf ist durch strenge **Compliance-Maßnahmen** gekennzeichnet. Das Unternehmen verfügt über die **SOC 2 Type II Zertifizierung**, die die Wirksamkeit der Kontrollen hinsichtlich Sicherheit, Verfügbarkeit, Verarbeitungsintegrität, Vertraulichkeit oder Datenschutz über einen längeren Zeitraum bestätigt (zuletzt abgeschlossen am 13. Februar 2025).

Zusätzlich betont Windsurf die Verfügbarkeit der **FedRAMP High Akkreditierung**. Hierbei handelt es sich um eine besonders strenge Anforderung der US-Regierung, die weit über SOC 2 hinausgeht. Die Einhaltung dieser Vorgaben führt zu einer internen Stärkung der Prozesse, die allen Kunden zugutekommt, auch jenen außerhalb des GovCloud-Bereichs. FedRAMP-Anforderungen umfassen beispielsweise einen detaillierten Code-Review-Prozess, der den Sicherheits-Impact von Änderungen hervorhebt, die Pflicht zur Einhaltung von Sicherheitsverfahren (wie Company MDM, Posture Management, Active EDR auf allen Mitarbeitergeräten und Zero Trust VPN) sowie das Training der relevanten Entwickler für Disaster Recovery und Informationssicherheits-Notfallpläne.

Windsurf führt zudem **jährliche, externe Penetrationstests** durch und strebt die Einhaltung des **OWASP ASVS Level 1** an, mit einem geplanten Pfad zu Level 2 und 3, unterstützt durch Tooling wie Snyk. Die hohen Zertifizierungen belegen, dass Windsurf eine ausgereifte Governance- und Prozessstruktur zur Einhaltung von Sicherheitsstandards besitzt. Diese formellen Zusicherungen bilden ein starkes Fundament für die Vertrauenswürdigkeit im Unternehmenskontext.

---

### Technische Sicherheitsmaßnahmen

Hinsichtlich der technischen Kontrollen sind mehrere Schutzmechanismen implementiert. Obligatorisch ist die **TLS-Verschlüsselung (Transport Layer Security)**, die jegliche Datenkommunikation zwischen der Client-Maschine (der IDE) und den Windsurf-Servern schützt.

Im Entwicklungsprozess verfolgt das Unternehmen einen „**Security by Design**“-Ansatz, indem es einen Code-Review-Prozess nutzt, der die Sicherheitsauswirkungen von Änderungen bewertet und eine vorgeschriebene Anzahl von Reviewern durchsetzt. Ein weiterer Aspekt ist die Sicherstellung der Korrektheit von KI-generiertem Code. Es wird empfohlen, **Dynamic Application Security Testing (DAST)** in den Workflow zu integrieren, um zu validieren, ob die von der KI vorgeschlagenen Sicherheitsmaßnahmen (z.B. Authentifizierung oder Eingabevalidierung) in der laufenden Anwendung tatsächlich wie beabsichtigt funktionieren.

Es muss jedoch beachtet werden, dass die Infrastruktur derzeit nur eine **Multitenant-Architektur** unterstützt und **keine Single-Tenant-Option** zur Verfügung steht. Während die Einhaltung strenger Standards wie FedRAMP High auch in einer Multitenant-Umgebung strikte Isolierungskontrollen erfordert, kann das Fehlen einer Single-Tenant-Option für Hochsicherheitsbereiche, die eine vollständige physische Isolation benötigen, weiterhin eine Einschränkung darstellen.

Zur schnellen Orientierung über das Compliance-Niveau kann die folgende Übersicht dienen:

### Windsurf Compliance und Sicherheitsprofil (Stand 2025)

| Bereich | Status/Zertifizierung/Kontrolle | Relevanz für den Unternehmenseinsatz |
| :--- | :--- | :--- |
| **ISMS Governance** | SOC 2 Type II zertifiziert (Stand Q1 2025) | Hohe Zusicherung der Kontrollen (Sicherheit, Verfügbarkeit, Vertraulichkeit). |
| **Regulatorische Konformität (US-Gov)** | FedRAMP High Akkreditierung verfügbar | Etabliert strenge Governance- und SDLC-Praktiken, über SOC 2 hinausgehend. |
| **Verschlüsselung (In Transit)** | Obligatorische TLS-Verschlüsselung | Schutz der Code-Daten während der Übertragung zwischen Client und Server. |
| **Entwicklungssicherheit** | OWASP ASVS Level 1 (mit Pfad zu L2/L3) | Nachweis eines Fokus auf Anwendungssicherheit und Schwachstellenmanagement. |
| **Infrastrukturtyp (Standard)** | Multitenant-Architektur | Derzeit keine Single-Tenant-Isolation verfügbar, kritisch für höchste Isolation. |

---

## 🔐 Datenschutz und Datenverarbeitung (Datenschutz)

### Erhobene Datenkategorien und Verarbeitungszwecke

Windsurf erhebt verschiedene Kategorien von Informationen. Dazu gehören:
* Registrierungsinformationen
* Kommunikationsinformationen
* Log- und Nutzungsinformationen
* Informationen von Drittanbietern und von Community-Plattformen

Spezifisch für die KI-Assistenz werden auch **Prompts und Outputs** verarbeitet.

Die Verwendung dieser Daten erfolgt zu mehreren Geschäftszwecken. Hauptsächlich dienen sie der **Bereitstellung des Dienstes** (vertragliche Notwendigkeit), der Beantwortung von Anfragen und der Lösung potenzieller Probleme.

Darüber hinaus werden die Daten für andere Geschäftsziele genutzt, wie Datenanalyse, Identifizierung von Nutzungstrends, Bestimmung der Wirksamkeit von Werbekampagnen und die allgemeine Bewertung und Verbesserung der Dienste und der Benutzererfahrung. Dabei werden Informationen in **aggregierter und anonymisierter Form** gespeichert und verwendet, um sie von individuellen Endbenutzern zu entkoppeln und sicherzustellen, dass keine personenbezogenen Daten enthalten sind.

---

### Rechtsgrundlagen der Verarbeitung (DSGVO-Konformität)

Für Nutzer mit Sitz im Europäischen Wirtschaftsraum (EWR), der Schweiz oder dem Vereinigten Königreich führt Windsurf die Verarbeitung personenbezogener Daten nur durch, wenn eine **gültige Rechtsgrundlage** vorliegt. Die genannten Rechtsgrundlagen sind:

* **Einwilligung** (*Consent*)
* **Vertragliche Notwendigkeit** (*Contractual Necessity*) zur Erbringung der Dienste.
* Erfüllung einer **Gesetzlichen Pflicht** (*Compliance with a Legal Obligation*).
* **Berechtigtes Interesse** (*Legitimate Interests*), das das Interesse von Windsurf oder eines Dritten an der Nutzung der personenbezogenen Daten darstellt.

Die Berufung auf "**Berechtigte Interessen**" zur Speicherung von Nutzungsmetadaten ist ein gängiger Ansatz zur Serviceverbesserung, erfordert jedoch eine sorgfältige Abwägung nach DSGVO-Grundsätzen. Dieses Risiko wird für Unternehmenskunden erheblich gemindert, da Windsurf versichert, **nicht auf "nicht-permissiven Daten" zu trainieren**, und die **Zero-Data Retention-Politik** die Menge an potenziell sensiblen Code-Daten, die verarbeitet werden, minimiert.

Die Weitergabe der Daten erfolgt nur an bestimmte Kategorien Dritter, darunter Partner und verbundene Unternehmen, Dienstleister (Vendors, Consultants) sowie Cloud-Dienstleister (z.B. Website Hosting Service Providers, Cloud Computing Services und Customer Intelligence Platforms).

---

### Rechte der Betroffenen (*Data Subject Rights*)

Basierend auf den geltenden Gesetzen des jeweiligen Landes haben Nutzer das Recht, **Zugang** zu den gesammelten persönlichen Daten zu verlangen, diese zu **ändern** oder unter bestimmten Umständen zu **löschen** (*Recht auf Review, Update, Delete*). Zur Ausübung dieser Betroffenenrechte, einschließlich des **Widerrufs der Einwilligung**, können sich Nutzer über die Windsurf-Kontaktseite melden.

---

## 🗄 Datenhaltung und Speichermodelle (Datenhaltung)

Dieser Abschnitt beleuchtet die entscheidenden Aspekte der **Datenresidenz** und des Mechanismus, der den Schutz des **geistigen Eigentums** in der Cloud gewährleisten soll.

### Deployment-Modelle und Datenlokalisierung

Um unterschiedliche regulatorische Anforderungen und Präferenzen hinsichtlich der Datenresidenz zu erfüllen, bietet Windsurf mehrere **Deployment-Optionen** an:

* **Standard Cloud**: Server werden von Windsurf verwaltet und sind in den **Vereinigten Staaten** lokalisiert.
* **EU Cloud**: Server werden von Windsurf verwaltet und befinden sich in **Frankfurt, Deutschland**. Dies ist die empfohlene Option für europäische Unternehmen, die eine Einhaltung der Datenresidenz-Anforderungen wünschen.
* **FedRAMP High**: Server werden in einer AWS GovCloud-Umgebung über Palantir's FedStart-Programm verwaltet.

Für maximale Datensouveränität stehen die Enterprise-Tiers zur Verfügung:

* **Enterprise Hybrid Tier**: Ein Teil der Infrastruktur wird vom Kunden selbst gehostet.
* **Enterprise Self-hosted Tier**: Sämtliche Compute- und Datendienste werden beim Kunden gehostet, wodurch die Daten zu **100% On-Premise** verbleiben.

Die aktuelle Infrastruktur unterstützt standardmäßig jedoch nur eine **Multitenant-Architektur**. Eine Single-Tenant-Option ist derzeit nicht verfügbar. Die Tatsache, dass trotz dieser Multitenancy-Einschränkung eine FedRAMP High Akkreditierung angestrebt wird, unterstreicht die Robustheit der internen Isolierungs- und Governance-Kontrollen, schließt aber möglicherweise Umgebungen mit regulatorisch bedingter Forderung nach dedizierter Hardware aus.

---

### Der Mechanismus der Zero-Data Retention (ZDR)

Der **Zero-Data Retention (ZDR)-Modus** ist der zentrale Mechanismus zum Schutz des Quellcodes in der Cloud und ist standardmäßig für Teams- und Enterprise-Kunden aktiv. Das Ziel des ZDR-Modus ist die **sofortige Bereinigung** des Prompts und des Codes aus dem Speicher, sobald die KI-Antwort generiert wurde.

Technisch gesehen sind die Code-Daten für die **Lebensdauer der Anfrage** (*Lifetime of the Request*) im Speicher (*in memory*) der Windsurf-Server sichtbar. Sie können für einen kurzen Zeitraum, typischerweise in der Größenordnung von **Minuten bis Stunden**, für Prompt-Caching existieren. Entscheidend für das Vertrauensmodell ist die Zusage, dass Code-Daten von ZDR-Nutzern **niemals zur Modell-Schulung** verwendet werden.

Im Gegensatz dazu muss bei **Individual Plänen** ohne aktivierten ZDR-Modus beachtet werden, dass Protokolle (*Logs*), die zur Nutzungsanalyse dienen, Code-Snippets und Benutzerverläufe enthalten können. Obwohl individuelle Nutzer den ZDR-Modus manuell aktivieren können, ist dies keine Standardeinstellung, was ein operatives Risiko für Einzelentwickler darstellt, die mit sensiblem Code arbeiten. Bei aktiver ZDR werden lediglich **Nutzungsmetadaten** (keine Code-Daten) in GCP BigQuery zu Analysezwecken protokolliert.

---

### Protokollierung und Audit-Fähigkeiten

Für **Enterprise Hybrid** und **Self-hosted Deployments** sind **Audit Logs** verfügbar. Diese Protokolle bieten Unternehmen einen Prüfpfad der KI-Generierungen, indem sie jeden akzeptierten Autocomplete-Vorschlag und jede Chat-Konversation protokollieren. Diese Audit Logs werden vollständig innerhalb der Kundenkomponente (*Private Tenant*) gespeichert, was die Kontrolle des Unternehmens über die Nutzungsdaten maximiert.

---

### Lokale Datenhaltung und "Memories"

Die agentische Funktionalität der IDE (*Cascade, Memories*) stützt sich auf lokale Datenhaltung für Kontext und Einstellungen. Regeln (*"Rules"*) werden typischerweise in Verzeichnissen wie `.windsurf/rules` im aktuellen Workspace oder in übergeordneten Git-Repositorys gespeichert. Wichtiger ist, dass persönliche **"Memories" und Projekt-Embeddings** (die das kontextuelle Wissen der KI über das Projekt speichern) in einem lokalen Datenbankordner abgelegt werden, meist im `.codeium` Verzeichnis. Dies ist für die Funktionalität des agentischen "**Flows**" essentiell.

Die Konsequenz dieser lokalen Speicherung ist, dass das Backup und die Migration dieser wertvollen, mühsam trainierten Kontextdateien (z.B. beim Wechsel des Entwicklercomputers) ein rein **manueller Prozess** bleibt, der vom Entwickler selbst durchgeführt werden muss.

---

### Datenhaltung und Zero-Data Retention (ZDR) nach Windsurf-Tarif

| Tarifmodell | Zero-Data Retention (ZDR) Status | Speicherung von Code-Snippets | Audit Logs verfügbar | Datenlokalisierung |
| :--- | :--- | :--- | :--- | :--- |
| **Individual Plan** (Ohne ZDR-Toggle) | Optional, muss aktiviert werden. | Können in Logs gespeichert werden (für Serviceverbesserung). | Nein (Nur Usage Metadaten). | Standardmäßig US-Cloud. |
| **Teams/Enterprise Cloud Plan** | Standardmäßig aktiv. | Nur kurzzeitig im Speicher (Caching), kein Training. | Ja (Akzeptierte Vorschläge, Chats). | US (Standard) oder EU (Frankfurt). |
| **Enterprise Hybrid Tier** | Standardmäßig aktiv. | Code verbleibt in der Kundenumgebung (lokal gehosteter Teil). | Ja (Audit Logs im privaten Tenant gespeichert). | Kundendefiniert (Hybrid). |
| **Enterprise Self-Hosted Tier** | Standardmäßig aktiv. | Keine Windsurf-Server involviert. Daten bleiben On-Premise. | Ja (Vollständige Kontrolle beim Kunden). | Ausschließlich On-Premise. |

---

## 📉 Disaster Recovery und Business Continuity

Die Fähigkeit zur **Wiederherstellung** und zur Gewährleistung der **Geschäftskontinuität** ist ein wesentlicher Bestandteil der zugesicherten Compliance (**SOC 2 Type II** und **FedRAMP**).

Windsurf loggt Nutzungsanalysen in **GCP BigQuery**. Diese Cloud-Datenbank erfordert spezifische und robuste Backup- und Wiederherstellungsstrategien, um Datenverlust im Falle eines regionalen Ausfalls zu verhindern.

Obwohl keine öffentlichen Zahlen zu den Wiederherstellungszielen genannt werden, impliziert die **FedRAMP High Akkreditierung** die Existenz dokumentierter, getesteter **RPO** (*Recovery Point Objective*) und **RTO** (*Recovery Time Objective*) Ziele. Der RPO definiert die maximale Menge an tolerierbarem Datenverlust, während der RTO die maximale Zeitspanne definiert, bis ein Geschäftsprozess nach einem Ausfall wiederhergestellt sein muss. Diese Ziele müssten von Enterprise-Kunden im Rahmen der Due Diligence über das Trust Center angefordert werden, um die Belastbarkeit der Cloud-Dienste zu validieren.

Die erweiterte "**Agentic Experience**" (z.B. *Cascade*) ist derzeit nur auf **Cloud- und Hybrid-Plänen** verfügbar und nicht in den reinen IDE-Erweiterungen. Dies bedeutet, dass die Verfügbarkeit der erweiterten KI-Funktionalität direkt an die Stabilität und Wiederherstellbarkeit der Windsurf-Cloud-Infrastruktur gekoppelt ist. Die Wiederherstellung lokaler Entwicklerdaten (*Memories, Rules*) bleibt, wie bereits erwähnt, in der **Verantwortung des Entwicklers selbst** und muss in die individuellen oder organisatorischen Backup-Strategien integriert werden.

## 📊 Kritische Sicherheitsbewertung und Risiken (Due Diligence)

Die positiven Compliance-Zertifikate (Abschnitt II) müssen kritisch gegen die fundamentalen Architekturschwächen abgewogen werden, die sich aus der Basis der IDE ergeben.

---

### Supply Chain Risiken durch die VS Code Fork-Architektur

Windsurf basiert als AI-native IDE auf einem **Fork** der populären **VS Code IDE**. Diese Architektur führt zu einem erheblichen "**Patch-Debt**"-Problem.

Die Analyse zeigt, dass die Windsurf IDE auf einer **veralteten VSCode-Version** (1.99.3) basiert, die vier Minor-Versionen hinter dem aktuellen VS Code Release (1.103.2) liegt.

Besonders kritisch ist die transitive Abhängigkeit von der Rendering-Engine **Chromium**. Windsurf verwendet Chromium-Versionen, die **sechs Hauptversionen** hinter der aktuellen Abhängigkeit von VS Code zurückliegen.

Diese Versionsverzögerung führt zur Akkumulation von **Sicherheitsschwachstellen**, die in der Basis-VS Code-Version bereits behoben wurden, aber in Windsurf weiterhin bestehen. Entwickler arbeiten dadurch potenziell mit einer erheblich größeren **Angriffsfläche**, da bekannte, aber ungepatchte Risiken im Unterbau vorhanden sind.

---

### OpenVSX Marketplace: Der VSXPloit-Angriffsvektor

Die moderne KI-gestützte Entwicklungsumgebung stützt sich stark auf **Erweiterungen** (*Extensions*) für Basisfunktionalitäten wie Syntax-Highlighting und Linting. Diese Erweiterungen laufen mit **vollen Berechtigungen** auf der Entwicklermaschine.

Ein kritischer Zero-Day, bekannt als **VSXPloit**, wurde kürzlich in **OpenVSX** entdeckt, dem Open-Source-Marktplatz, der Erweiterungen für VS Code Forks wie Windsurf bereitstellt. Dieser Fehler hätte einem Angreifer ermöglicht, die Kontrolle über den gesamten Marktplatz zu erlangen und bösartige Updates unter vertrauenswürdigen Konten zu veröffentlichen. Wäre diese Schwachstelle ausgenutzt worden, hätte sie zu einem "**Supply Chain Armageddon**" führen können, bei dem Millionen von Entwicklermaschinen, die Windsurf nutzen, über eine **kompromittierte Extension** übernommen werden könnten. Die Gefahr rührt nicht nur vom Kernprodukt, sondern von der gesamten, hochprivilegierten **Entwicklungs-Lieferkette** her.

---

## 📓 Fazit und Handlungsempfehlungen

### Zusammenfassende Bewertung der Sicherheitspostur

Die Analyse zeigt eine **Dualität**:

1.  **Stärken (Governance & Datenschutz):** Windsurf bietet eine hochentwickelte, prozessorientierte Governance-Struktur (**SOC 2 Type II, FedRAMP-Orientierung**) und robuste, vertragsbasierte Datenschutzmechanismen (**Zero-Data Retention, EU-Datenlokalisierung**). Diese Maßnahmen adressieren die zentralen Bedenken hinsichtlich des Schutzes des geistigen Eigentums in Cloud-Umgebungen.

2.  **Schwächen (Architektur & Operation):** Diesen Stärken stehen signifikante, unmittelbare operative Risiken gegenüber, die aus der technischen Architektur resultieren. Kritisch sind insbesondere der **Versionsrückstand** des zugrunde liegenden VS Code Forks und der veralteten **Chromium-Abhängigkeit**. Darüber hinaus stellt die Abhängigkeit vom **OpenVSX-Ökosystem** und die damit verbundenen **Supply-Chain-Risiken** eine kritische Bedrohung dar, da Erweiterungen mit vollen Systemberechtigungen ausgeführt werden.

---

### Empfehlungen für die Einführung

Basierend auf dieser Bewertung werden folgende Handlungsempfehlungen für Organisationen abgeleitet:

1.  **Priorisierung der Deployment-Wahl:** Für regulierte Umgebungen oder Projekte mit höchster Sensibilität des Quellcodes wird dringend die Nutzung des **Enterprise Self-Hosted** oder **Hybrid Tiers** empfohlen. Dies umgeht die Einschränkung der Multitenancy und bietet die maximale Datensouveränität.

2.  **DSGVO-Konformität und Datenresidenz:** Europäische Unternehmen sollten primär die **EU Cloud-Region (Frankfurt)** wählen, um die Anforderungen an die Datenresidenz und die DSGVO-Konformität bestmöglich zu erfüllen.

3.  **Pflicht zur ZDR-Aktivierung bei Einzelnutzern:** Entwickler auf **Individual Plänen** müssen angewiesen werden, den **Zero-Data Retention Modus** explizit und sofort im Benutzerprofil zu aktivieren. Andernfalls besteht das Risiko der unbeabsichtigten Speicherung von Code-Snippets in den Windsurf-Logs.

4.  **Minderung des Supply-Chain-Risikos:** Die DevSecOps-Abteilung muss die Endpoint-Security auf Entwickler-Workstations verstärken (z.B. durch **Active EDR und Application Control**), um die Ausführung von bösartigem Code, der durch Schwachstellen wie **VSXPloit** über den Extension-Marktplatz eingeschleust werden könnte, zu verhindern. **Strenges Whitelisting** von IDE-Erweiterungen ist erforderlich.

5.  **Due Diligence bei Audits:** Organisationen sollten die aktuellen **SOC 2 Type II** und **FedRAMP Audit-Berichte** über das Trust Center anfordern, um die spezifischen Kontrollen zur Minderung des Multitenancy-Risikos und die internen **RPO/RTO-Ziele** detailliert zu prüfen.

6.  **Betriebliche Verantwortung:** Entwickler müssen in die manuelle Sicherung und Migration ihrer lokalen Kontextdateien (**Memories** und **Rules** im `.codeium`-Verzeichnis) geschult werden, da diese nicht automatisch gesichert werden.

---

<p align="center">
<a href="/docs/04-tools/04-windsurf/01-ueberblick/03-workflows_und_automatisierungsprozesse/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/04-tools/05-terminal/README.md"><strong>Weiter</strong></a>
</p>

<p align="center">
<a href="/docs/04-tools/04-windsurf/README.md/#dieses-thema-beinhaltet-folgende-kapitel"><strong>Zurück zur Kapitel-Übersicht</strong></a> | <a href="/docs/00-willkommen/README.md"><strong>Zurück zur Startseite des Wikis</strong></a>
</p>