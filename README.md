# Board Katalog

Zentrale Übersicht unserer Boards und ihrer technischen Dokumentation. Jedes Modell erhält einen eigenen Eintrag mit eindeutigem Namen, Quellen und Erfassungsstand. Umfangreiche technische Unterlagen können in einem verlinkten Board-Repository liegen.

## Boards

| Hersteller | Modell und Variante | Katalogeintrag | Technische Dokumentation |
| --- | --- | --- | --- |
| Waveshare | ESP32-S3-RS485-CAN-U | [Zum Eintrag](boards/waveshare-esp32-s3-rs485-can-u.md) | [Board-Repository](https://github.com/Mcgee1704/waveshare-esp32-s3-rs485-can-u) |

## Neues Board aufnehmen

1. [Board-Vorlage](templates/board.md) nach `boards/hersteller-modell-variante.md` kopieren. Dateinamen klein und mit Bindestrichen schreiben.
2. Hersteller, exakte Variante und bekannte Platinenrevision eintragen. Unbekannte Angaben als „nicht erfasst“ kennzeichnen.
3. Herstellerangaben und Beobachtungen am eigenen Exemplar getrennt dokumentieren. Quellen mit Link und Abrufdatum angeben; bei Git-Quellen möglichst einen Commit festhalten.
4. Den Eintrag in der Übersicht ergänzen und auf das führende technische Repository verweisen, falls eines existiert.

## Ablage und Erfassungsstand

- `boards/`: Ein Eintrag je Boardmodell und Variante. Mehrere eigene Exemplare werden im zugehörigen Eintrag ohne öffentliche Seriennummern unterschieden.
- `templates/`: Einheitliche Vorlage für neue Einträge.
- „Hersteller dokumentiert“ bedeutet eine belegte Angabe aus einer Quelle. „Am Exemplar bestätigt“ benötigt einen eigenen Sicht- oder Auslesenachweis. „Nicht erfasst“ bleibt ausdrücklich offen.
- Bus- oder Gegenstellentests sind keine Voraussetzung für die Aufnahme. Wenn es welche gibt, werden sie separat beschrieben.
- MAC-Adressen, Seriennummern, Zugangsdaten, private Flashabbilder und rohe Geräteprotokolle bleiben lokal. Originalunterlagen werden mit Quellen- und Lizenzangabe verlinkt; eine Veröffentlichung als Kopie erfordert passende Rechte.

Der Katalog ist eine Sammlung eigener technischer Notizen und Verweise, keine offizielle Veröffentlichung der jeweiligen Hersteller.
