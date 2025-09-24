# <p align="center">Design und Theme-Anpassung</p>

---
<!-- Kapitel Design und Theme-Anpassung -->

WordPress bietet eine Vielzahl von Themes, die das Design und Layout der Website bestimmen. Die Anpassung von Themes ermöglicht es, das Erscheinungsbild individuell zu gestalten und an die Bedürfnisse der Website anzupassen.

## Child-Themes

Child-Themes sind eine empfohlene Methode, um Änderungen an einem bestehenden Theme vorzunehmen, ohne die Originaldateien zu verändern. Dadurch bleiben Anpassungen auch bei Theme-Updates erhalten.

### Vorteile von Child-Themes

- **Sicherheit bei Updates**: Änderungen gehen nicht verloren, wenn das Parent-Theme aktualisiert wird.
- **Einfache Anpassungen**: Child-Themes ermöglichen es, CSS, Templates und Funktionen zu erweitern oder zu überschreiben.

### Erstellung eines Child-Themes

1. **Ordner erstellen**: Im `wp-content/themes`-Verzeichnis einen neuen Ordner für das Child-Theme anlegen, z. B. `mein-child-theme`.
2. **style.css**: Eine `style.css`-Datei im Child-Theme-Ordner erstellen mit folgendem Inhalt:

   ```css
   /*
   Theme Name: Mein Child Theme
   Template: parent-theme-folder-name
   */
   ```

   Ersetze `parent-theme-folder-name` durch den Ordnernamen des Parent-Themes.

3. **functions.php**: Eine `functions.php`-Datei im Child-Theme-Ordner erstellen, um zusätzliche Funktionen hinzuzufügen oder Parent-Theme-Funktionen zu erweitern.
4. **Aktivierung**: Im WordPress-Dashboard unter "Design" > "Themes" das Child-Theme aktivieren.

---

## Theme Customizer

Der Theme Customizer ist ein integriertes Tool in WordPress, das es ermöglicht, das Design der Website in Echtzeit anzupassen. Über den Customizer können Farben, Schriftarten, Layouts und andere Designelemente geändert werden.

### Nutzung des Theme Customizers

1. **Zugriff**: Im WordPress-Dashboard unter "Design" > "Customizer" öffnen.
2. **Anpassungen vornehmen**: Verschiedene Bereiche wie "Allgemeine Einstellungen", "Farben", "Schriftarten" usw. anpassen.
3. **Vorschau**: Änderungen werden in Echtzeit angezeigt, bevor sie veröffentlicht werden.
4. **Veröffentlichen**: Nach Abschluss der Anpassungen auf "Veröffentlichen" klicken, um die Änderungen live zu schalten.

---

## Barrierefreiheit und CI-konformes Design

Barrierefreiheit (Accessibility) und CI-konformes Design sind wichtige Aspekte bei der Gestaltung von WordPress-Websites.

### Barrierefreiheit

Barrierefreiheit bedeutet, dass Websites für alle Nutzer zugänglich sind, einschließlich Menschen mit Behinderungen.  
Wichtige Punkte sind:

- **Semantisches HTML**: Verwendung von korrekten HTML-Tags (z. B. Überschriften, Listen), um die Struktur der Seite klar zu definieren.
- **Alt-Texte für Bilder**: Beschreibende Alt-Texte für alle Bilder hinzufügen, um deren Inhalt zu erklären.
- **Kontraste**: Ausreichende Farbkontraste zwischen Text und Hintergrund, um die Lesbarkeit zu verbessern.
- **Tastaturnavigation**: Sicherstellen, dass alle interaktiven Elemente (z. B. Links, Formulare) auch über die Tastatur erreichbar sind.

### CI-konformes Design

CI-konformes Design bezieht sich auf die Einhaltung der Corporate Identity (CI) des Unternehmens oder der Organisation.  
Wichtige Aspekte sind:

- **Farbpalette**: Verwendung der festgelegten Farben des Corporate Designs.
- **Typografie**: Einhaltung der definierten Schriftarten und -größen.
- **Logo und Branding**: Konsistente Verwendung des Logos und anderer Branding-Elemente.
- **Layout**: Einheitliche Gestaltungselemente, die das Corporate Design widerspiegeln.

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
<a href="/docs/06-entwicklung/08-cms/05-erweiterung_plugins/README.md"><strong>Zurück</strong></a> | 
<a href="/docs/06-entwicklung/08-cms/07-pruefungsvorbereitung/README.md"><strong>Weiter</strong></a>
</p>
