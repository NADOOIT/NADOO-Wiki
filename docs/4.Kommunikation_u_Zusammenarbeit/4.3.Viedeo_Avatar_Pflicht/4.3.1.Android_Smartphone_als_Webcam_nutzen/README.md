# 4.3.1 Android - Smartphone als Webcam nutzen

## DroidCam Webcam-App installieren

Lade die DroidCam Webcam-App von Dev47Apps aus dem Google Play Store auf Dein Smartphone herunter und installiere sie.  
![image](https://github.com/user-attachments/assets/79ac1c4b-46ee-45b6-b90a-37d3a96169db)

## Desktop-Version herunterladen

Lade die Desktop-Version von DroidCam für Windows von der offiziellen Website herunter und installiere sie auf Deinem Computer:  
[https://www.dev47apps.com/](https://www.dev47apps.com/)

![image](https://github.com/user-attachments/assets/9c9455cd-606f-4dc0-9eb9-558c121039f7)

## Smartphone mit dem Computer verbinden

Öffne nach der Installation die App auf Deinem Smartphone. Du solltest nun einen Bildschirm sehen, auf dem verschiedene Verbindungsdetails angezeigt werden. Kopiere die WiFi-IP-Adresse, die auf Deinem Smartphone angezeigt wird, in das Feld **Device IP** im DroidCam-Client auf Deinem Windows-Computer.

![image](https://github.com/user-attachments/assets/afa87e96-60a5-4b40-97af-0b7340ea4a4c)  
![image](https://github.com/user-attachments/assets/b4229799-fcc6-4387-b140-2e42dc976877)

## Verbindung starten

Klicke auf **Start**, um die Verbindung herzustellen. Deine Kamera sollte jetzt bereit sein.

## Wie funktioniert DroidCam?

- Die App wird genutzt, um Dein Smartphone als Webcam mit Deinem Computer zu verbinden, entweder über WLAN, USB oder LAN.
- Video- und Audiostreams werden in der Regel lokal innerhalb Deines Netzwerks übertragen.
- Eine Internetverbindung ist für die Nutzung nicht erforderlich, was das Risiko verringert, dass Daten an externe Server gesendet werden.

## Sendet DroidCam Daten an externe Adressen?

Basierend auf der offiziellen Dokumentation und dem Design der App:

1. **Lokale Nutzung**: DroidCam arbeitet primär über das lokale Netzwerk und erfordert keine Verbindung zu externen Servern, um Video- oder Audiostreams zu übertragen. Das bedeutet, dass Deine Daten im lokalen Netzwerk bleiben sollten.
2. **Datenschutzrichtlinie**: Laut der Datenschutzrichtlinie von Dev47Apps werden keine personenbezogenen Daten ohne Deine Zustimmung an Dritte weitergegeben (z. B. durch optionale Analysefunktionen).

## Wie kannst Du sicherstellen, dass keine Daten extern übertragen werden?

Um sicherzugehen, dass keine unerwarteten Datenübertragungen stattfinden, kannst Du Folgendes tun:

- **Netzwerkverkehr überwachen**:  
  Verwende Tools wie Wireshark, um den Netzwerkverkehr zu analysieren und nach Verbindungen zu unbekannten externen IP-Adressen zu suchen.

- **Firewall konfigurieren**:  
  Richte Deine Firewall so ein, dass sie ausgehende Verbindungen von DroidCam blockiert, falls Du Bedenken hast.

- **App-Berechtigungen prüfen**:  
  Überprüfe auf Deinem Smartphone, welche Berechtigungen die App hat (z. B. Kamera, Mikrofon, lokales Netzwerk) und entferne nicht benötigte Zugriffe.

## Fazit

DroidCam gilt als sichere App, die Daten normalerweise nur lokal verarbeitet. Wenn Du jedoch Bedenken hast, kannst Du zusätzliche Maßnahmen wie Netzwerküberwachung oder die Nutzung der USB-Verbindung ergreifen, um sicherzustellen, dass keine Daten Dein lokales Netzwerk verlassen.