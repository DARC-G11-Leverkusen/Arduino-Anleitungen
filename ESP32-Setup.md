# Konfiguration der Arduino-Oberfläche für den ESP32
Die folgende Anleitung beschreibt, wie man die Ardunio-IDE zur Unterstützung des ESP32 erweitert.


## IDE konfigurieren
### Voreinstellungen anpassen
- Datei / Voreinstellungen wählen

![Dateimenue](https://github.com/DARC-G11-Leverkusen/Arduino-Anleitungen/blob/master/A1.png)

1. Eingabe des Links zum Hersteller-Code:
```
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```
2. Wichtig: Updates aktivieren.
3. Optional: Nummeranzeige im Code aktivieren.
4. **Danach die Arduino-Software beenden und neu starten**

![Voreinstellungen](https://github.com/DARC-G11-Leverkusen/Arduino-Anleitungen/blob/master/A2.png)


### Das passende Board einstellen
- Aufrufen von Werkzeuge / Board: ... / Boardverwalter
![Werkzeuge](https://github.com/DARC-G11-Leverkusen/Arduino-Anleitungen/blob/master/A3.png)

- Nun `ESP32` in die Suchmaske eingeben und installieren. Es werden nun einmalig die speziellen Dateien des ESP32 aus dem Internet geladen. Je nach Datenrate benötigt das so seine Zeit!

![Boardmanager](https://github.com/DARC-G11-Leverkusen/Arduino-Anleitungen/blob/master/A4.png)


### Einstellen des richtigen Controllers
**Hinweis:** Das von uns genutzte Board TTGOv1.7 wird mit den Einstellungen wie im Bild konfiguriert. Dies kann bei anderen Produkten abweichen.

![Board waehlen](https://github.com/DARC-G11-Leverkusen/Arduino-Anleitungen/blob/master/A5.png)


## Sonderfall: Softwareupdate Over-the-Air (OTA)
In dem Projekt mit der [PingPong-LEDwall](https://github.com/DARC-G11-Leverkusen/PINGPONG-LEDWALL) wird der Controller sich immer mit dem WLAN verbinden, oder einen AccessPoint bereitstellen. Auf dem Controller läuft ein Webserver. Mit dem Webbrowser kann man die Software also ohne Kabel direkt einspielen. Zur Erzeugung der BIN-Datei nimmt man die folgende Option im Sketch-Menü.

![Sketch](https://github.com/DARC-G11-Leverkusen/Arduino-Anleitungen/blob/master/A6.png)

