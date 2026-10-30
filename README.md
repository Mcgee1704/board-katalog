# Board Catalog

Central index of our boards and their technical documentation. Each model has a dedicated entry with an exact name, sources and an evidence status. Detailed technical material is maintained in linked board repositories.

## Boards

| Manufacturer | Model and variant | Catalog entry | Technical documentation |
| --- | --- | --- | --- |
| Waveshare | ESP32-S3-RS485-CAN-U | [Entry](boards/waveshare-esp32-s3-rs485-can-u.md) | [Board repository](https://github.com/Mcgee1704/waveshare-esp32-s3-rs485-can-u) |
| Waveshare | ESP32-P4-WIFI6-POE-ETH | [Entry](boards/waveshare-esp32-p4-wifi6-poe-eth.md) | [Board repository](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth) |

## Adding a board

1. Copy the [board template](templates/board.md) to `boards/manufacturer-model-variant.md`. Use lowercase filenames with hyphens.
2. Record manufacturer, exact variant and known PCB revision. Mark unknown values as “not recorded”.
3. Separate manufacturer statements from observations on the physical board. Include source links and retrieval dates; pin Git sources to a commit where possible.
4. Add the board to this index and link its primary technical repository if one exists.

## Storage and evidence status

- `boards/`: one entry per model/variant. Multiple owner units are identified without public serial numbers.
- `templates/`: a consistent template for new entries.
- “Manufacturer documented” means a sourced specification. “Confirmed on the unit” requires a visual/readout/measurement record. “Not recorded” remains explicitly unresolved.
- Bus or counterpart tests are optional for catalog inclusion. Existing functional tests are documented separately.
- MAC addresses, serial numbers, credentials, private flash images and raw logs remain local. Link original documents with source/license information; redistributing copies requires suitable rights.

This catalog is a collection of independent technical notes and links, not an official publication of the manufacturers.
