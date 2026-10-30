# Waveshare ESP32-P4-WIFI6-POE-ETH

## Identification

| Field | Value |
| --- | --- |
| Manufacturer | Waveshare |
| Model | ESP32-P4-WIFI6-POE-ETH with P4-Core and C6 wireless coprocessor |
| Sales kits | Basic SKU 32832; C 32833; D 32834. Owner accessory kit not established |
| Owner units | Two; referred to as Board 1 and Board 2 |
| Silicon revision | Both ESP32-P4 v1.3 in historical readouts; separate from PCB revision |
| PCB revision | Board 1: Rev2.0 in the 2026-10-30 photographs; Board 2: owner reports no differences, without independent revision reading |
| Primary technical documentation | [P4 board repository](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth) |
| Catalog status | 2026-10-30; historical software evidence, Board 1 photo identification and Board 2 owner comparison |

## Specifications and detailed documentation

| Topic | Summary | Primary reference |
| --- | --- | --- |
| Processor | Dual-core RISC-V P4; 360 MHz in the board profile and existing setup; LP core up to 40 MHz | [Hardware](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/01-hardware.md) |
| Memory | P4 flash 32 MiB, PSRAM 32 MiB; owner startup tests passed | [Owner boards](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/05-own-boards.md) |
| Wireless | Wi-Fi 6 / BLE through C6 and SDIO; not integrated in the P4 | [Hardware and assembly differences](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/01-hardware.md) |
| Ethernet | IP101GRI, RMII, 100-Mbit/s port; PoE module interface | [Programming](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/04-firmware.md) |
| USB | USB-C: power and CH343P UART; USB-A: native P4 HS OTG | [USB and boot](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/04-firmware.md) |
| Connectors | 40-pin header with 28 GPIO nets, I2C, UART, MicroSD, MIPI-DSI/CSI, microphone and speaker | [Contacts and GPIO conflicts](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/02-pinout.md) |
| Power | USB-C 5 V, 5-V connector and PoE path; H1/H2 supply selected through H5; 3.3-V logic | [Power and current budgets](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/03-power.md) |
| Audio | ES8311 codec, NS4150B amplifier, H4 differential output | [Hardware](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/01-hardware.md) |
| Mechanics | Manufacturer drawing: 55 × 68 mm, mounting centres 48 × 33 mm; not measured by the owner | [Source register](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/sources/README.md) |
| Firmware basis | Existing verified setup: ESP-IDF 5.5.4, revision-1.x configuration | [Project profile](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/04-firmware.md) |
| Other projects | Manufacturer platform, ESP-IDF, ESP-Hosted/MCU, two KVM projects and owner cluster research | [Git projects with pinned commits](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/06-git-projects.md) |
| Structured data | JSON, 94 connector contacts and GPIO0–54 usage/conflicts | [Board JSON](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/data/board.json), [pin CSV](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/data/pinout.csv), [GPIO CSV](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/data/gpio-usage.csv) |
| Next evidence needed | Board 1 photos reviewed; Board 2 owner comparison recorded; component identification, independent Board 2 assembly verification and electrical evidence remain open | [Owner evidence checklist](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/07-evidence-checklist.md) |

## Owner evidence

Both P4s reported revision 1.3, 32 MiB flash and 32 MiB PSRAM. Flash was backed up locally before the earlier firmware installation. Boot, PSRAM startup test, DHCP, Ethernet application traffic, model storage and text generation including two-board operation are documented. Normal later LAN updates were also tested. The setup used computer USB-C power and Ethernet without PoE. Neither this catalog task nor its English translation accessed or modified the devices.

The existing [published research hardware summary](https://github.com/Mcgee1704/esp32-p4-llm-cluster-research/blob/0675f8687b9459fafa4545587ef14aedd118187d/docs/HARDWARE.md) and local historical bring-up records form the evidence basis. The [sanitized detailed record](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/05-own-boards.md) explains the limits. This is not a live display of installed firmware.

## Board 1 photo findings

The [sanitized visual record](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/08-board1-visual-record.md) identifies Rev2.0, a coloured header, an ESP32-P4-Core shield marked ESP32-P4NRW32 / Flash 32MB, an ESP32-C6-MINI-1U with attached antenna cable, a visible 0-ohm link on H5's 3V3 side, an unpopulated R12 reference footprint, U2 top code P3HE and an attached speaker. These are Board 1 observations only; no new electrical or functional test was performed. The exact U2 ordering part remains unresolved because the reviewed DIOO table lists W3HE for the schematic part. Original photos and private source records remain local.

## Board 2 owner comparison

On 2026-10-30 the owner reopened Board 2 documentation and reported no differences from Board 1. The [dedicated Board 2 record](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/09-board2-owner-comparison.md) completes the descriptive entry as an attributed owner report. No independent Board 2 photo review or per-component marking transcription was performed; the existing 18 photos remain Board 1 evidence. Earlier Board 2 runtime/readout evidence remains separate. No new electrical or functional test was performed.

## Important differences and unresolved items

- The schematic identifies C6-MINI-1-N4; the current product page identifies C6-MINI-1U-H8. Board 1 photos identify the MINI-1U family and antenna cable; exact memory variant/firmware remain unresolved. Board 2 is owner-reported to have no differences, without independent assembly verification.
- Old/new manufacturer header pictures show reversed left/right columns. Pin tables follow schematic numbering; physical pin-1 assignment has not been confirmed.
- The manufacturer FAQ permits USB-C and PoE together. Current budget and reverse-current behaviour of a multi-board USB-A-to-USB-C chain remain unqualified on the owner setup.
- Board 1 PCB revision, H5 link, R12 population and antenna-cable assembly are visually recorded. Complete PoE identity, exact U2 part and measured voltage/current behaviour remain open; Board 2 has an owner-reported comparison, with independent assembly verification still open.
- WLAN/BLE, SD, audio, camera, display, USB OTG application use, complete GPIO coverage and long-duration operation remain untested.
- Physical revision-3.x testing, original-flash restoration, deliberate OTA interruption and automatic neighbour installation have not been established.

Continue from the Board 1 visual record, Board 2 owner comparison and the [remaining evidence checklist](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/07-evidence-checklist.md). Functional and electrical tests require their own suitable setup; catalog completeness does not require claiming that every function has been tested.

## Sources

Manufacturer sources reviewed on 2026-10-30: [overview](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH), [schematic](https://files.waveshare.com/wiki/ESP32-P4-WIFI6-POE-ETH/ESP32-P4-WIFI6-POE-ETH-Schematic.pdf), [FAQ](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH/FAQ), [ESP-IDF instructions](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH/ESP-IDF). Hashes, revision differences and Git commits are in the [source register](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/sources/README.md).

This catalog summarizes the evidence and points to the board repository for complete tables. MAC addresses, serial numbers, credentials, local network addresses, flash backups and raw logs remain private.

[Back to catalog](../README.md)
