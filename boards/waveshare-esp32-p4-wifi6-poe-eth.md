# Waveshare ESP32-P4-WIFI6-POE-ETH

## Identifikation

| Feld | Angabe |
| --- | --- |
| Hersteller | Waveshare |
| Modell | ESP32-P4-WIFI6-POE-ETH mit P4-Core und C6-Funkcoprozessor |
| Verkaufspakete | Basic SKU 32832; C 32833; D 32834. Zubehörpaket der eigenen Exemplare nicht erfasst |
| Eigene Exemplare | Zwei; im Katalog als Board 1 und Board 2 bezeichnet |
| Siliziumrevision | Beide ESP32-P4 v1.3 ausgelesen; Platinenrevision weiterhin offen |
| Führende technische Dokumentation | [P4-Board-Repository](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth) |
| Katalogstand | 30.10.2026; vorhandene eigene Nachweise vom 29.10.2026 ausgewertet |

## Technische Daten und Detaildokumentation

| Thema | Zusammenfassung | Führende Details |
| --- | --- | --- |
| Prozessor | Dual-Core-RISC-V-P4; 360 MHz im Boardprofil und bisherigen Aufbau; LP-Kern bis 40 MHz | [Hardware](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/01-hardware.md) |
| Speicher | P4-Flash 32 MiB, PSRAM 32 MiB; eigene Starttests erfolgreich | [Eigene Boards](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/05-own-boards.md) |
| Funk | Wi-Fi 6 / BLE über C6 und SDIO; nicht vom P4 selbst bereitgestellt | [Hardware und Bestückungsunterschiede](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/01-hardware.md) |
| Ethernet | IP101GRI, RMII, 100-Mbit/s-Port; PoE-Modulanschluss | [Programmierung](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/04-firmware.md) |
| USB | USB-C: Versorgung und CH343P-UART; USB-A: nativer P4-HS-OTG-Port | [USB und Boot](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/04-firmware.md) |
| Anschlüsse | 40-poliger Header mit 28 GPIO-Netzen, I2C, UART, MicroSD, MIPI-DSI/CSI, Mikrofon und Lautsprecher | [Alle erfassten Kontakte und GPIO-Konflikte](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/02-pinout.md) |
| Versorgung | USB-C 5 V, 5-V-Anschluss und PoE-Pfad; H1/H2-Versorgung per H5 wählbar; 3,3-V-Logik | [Versorgung und Strombudgets](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/03-power.md) |
| Audio | ES8311-Codec, NS4150B-Verstärker, H4 als differenzieller Ausgang | [Hardware](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/01-hardware.md) |
| Mechanik | Herstellerzeichnung: 55 × 68 mm, Lochmitten 48 × 33 mm; nicht selbst vermessen | [Quellenregister](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/sources/README.md) |
| Firmwaregrundlage | Eigener belegter Stand ESP-IDF 5.5.4 und Rev-1.x-Konfiguration | [Projektprofil](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/04-firmware.md) |
| Weitere Projekte | Herstellerplattform, ESP-IDF, ESP-Hosted/MCU, zwei KVM-Projekte und eigene Cluster-Forschung | [Git-Projekte mit Commitständen](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/06-git-projects.md) |
| Strukturierte Daten | JSON, 94 Anschlusskontakte und GPIO0–54 mit Nutzung/Konflikten | [Board-JSON](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/data/board.json), [Pin-CSV](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/data/pinout.csv), [GPIO-CSV](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/data/gpio-usage.csv) |

## Eigene Nachweise

Beide P4s meldeten Revision 1.3, 32 MiB Flash und 32 MiB PSRAM. Vor der damaligen Firmwareinstallation wurde der Flash vollständig lokal gesichert. Boot, PSRAM-Starttest, DHCP, Anwendungsverkehr über Ethernet, Modellablage und Textgenerierung einschließlich Zweierbetrieb sind dokumentiert. Normale spätere LAN-Updates wurden ebenfalls geprüft. Der Aufbau nutzte USB-C-Strom vom Rechner und Ethernet ohne PoE. Für diese Katalogaufnahme wurde kein Gerät neu ausgelesen oder verändert.

Die vorhandene [öffentliche Hardware-Zusammenfassung der Forschung](https://github.com/Mcgee1704/esp32-p4-llm-cluster-research/blob/0675f8687b9459fafa4545587ef14aedd118187d/docs/HARDWARE.md) und lokale historische Inbetriebnahmeunterlagen sind die Grundlage. Der [bereinigte Detailstand](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/05-own-boards.md) nennt die Grenzen. Dies ist keine Live-Anzeige der momentan installierten Firmware.

## Wichtige Unterschiede und offene Punkte

- Der Schaltplan nennt C6-MINI-1-N4, die aktuelle Produktseite C6-MINI-1U-H8. Die konkrete C6-Bestückung der eigenen Exemplare bleibt offen.
- Alte und neue Hersteller-Headerbilder zeigen linke/rechte Spalten vertauscht. Die Pinliste verwendet Schaltplannummern; physische Pin-1-Zuordnung am eigenen Board noch nicht bestätigt.
- Die Hersteller-FAQ erlaubt USB-C plus PoE. Strombudget und Rückstromverhalten einer USB-A-zu-USB-C-Boardkette sind am eigenen Aufbau nicht abgenommen.
- Platinenrevision, H5-Stellung, R12-Bestückung, PoE-Modul und Antenne sind noch zu erfassen.
- WLAN/BLE, SD, Audio, Kamera, Display, USB-OTG-Anwendung, vollständige GPIO-Prüfung und Langzeitlast sind offen.
- Reale Tests für P4-Revision 3.x, Originalflash-Wiederherstellung, absichtliche OTA-Unterbrechung und automatische Nachbarinstallation sind nicht bestätigt.

## Quellen

Herstellerquellen am 30.10.2026 abgeglichen: [Boardübersicht](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH), [Schaltplan](https://files.waveshare.com/wiki/ESP32-P4-WIFI6-POE-ETH/ESP32-P4-WIFI6-POE-ETH-Schematic.pdf), [FAQ](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH/FAQ), [ESP-IDF-Anleitung](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH/ESP-IDF). Hashes, Revisionsunterschiede und Git-Commitstände stehen im [Quellenregister](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/sources/README.md).

Der Katalog führt die Zusammenfassung und verweist für die vollständigen Tabellen auf das Board-Repository. MAC-Adressen, Seriennummern, Zugangsdaten, lokale Netzadressen, Flashsicherungen und Rohprotokolle bleiben privat.

[Zurück zum Katalog](../README.md)
