# Waveshare ESP32-P4-WIFI6-POE-ETH

## Identification

| Field | Value |
| --- | --- |
| Manufacturer | Waveshare |
| Model | ESP32-P4-WIFI6-POE-ETH with P4-Core and C6 wireless coprocessor |
| Sales kits | Basic SKU 32832; C 32833; D 32834. Owner accessory kit not established |
| Owner units | Two; referred to as Board 1 and Board 2 |
| Silicon revision | Both ESP32-P4 v1.3 read out; PCB revision unresolved |
| Primary technical documentation | [P4 board repository](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth) |
| Catalog status | 2026-10-30; existing owner evidence from 2026-10-29 reviewed |

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
| Next evidence needed | Board photos/markings, PoE setup, available equipment and a staged test plan | [Owner evidence checklist](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/07-evidence-checklist.md) |

## Owner evidence

Both P4s reported revision 1.3, 32 MiB flash and 32 MiB PSRAM. Flash was backed up locally before the earlier firmware installation. Boot, PSRAM startup test, DHCP, Ethernet application traffic, model storage and text generation including two-board operation are documented. Normal later LAN updates were also tested. The setup used computer USB-C power and Ethernet without PoE. Neither this catalog task nor its English translation accessed or modified the devices.

The existing [published research hardware summary](https://github.com/Mcgee1704/esp32-p4-llm-cluster-research/blob/0675f8687b9459fafa4545587ef14aedd118187d/docs/HARDWARE.md) and local historical bring-up records form the evidence basis. The [sanitized detailed record](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/05-own-boards.md) explains the limits. This is not a live display of installed firmware.

## Important differences and unresolved items

- The schematic identifies C6-MINI-1-N4; the current product page identifies C6-MINI-1U-H8. The exact owner C6 assembly remains unresolved.
- Old/new manufacturer header pictures show reversed left/right columns. Pin tables follow schematic numbering; physical pin-1 assignment has not been confirmed.
- The manufacturer FAQ permits USB-C and PoE together. Current budget and reverse-current behaviour of a multi-board USB-A-to-USB-C chain remain unqualified on the owner setup.
- PCB revision, H5 position, R12 population, PoE module and antenna need identification.
- WLAN/BLE, SD, audio, camera, display, USB OTG application use, complete GPIO coverage and long-duration operation remain untested.
- Physical revision-3.x testing, original-flash restoration, deliberate OTA interruption and automatic neighbour installation have not been established.

Start with the [identification photo list and setup questions](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/docs/07-evidence-checklist.md). Functional and electrical tests require their own suitable setup; catalog completeness does not require claiming that every function has been tested.

## Sources

Manufacturer sources reviewed on 2026-10-30: [overview](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH), [schematic](https://files.waveshare.com/wiki/ESP32-P4-WIFI6-POE-ETH/ESP32-P4-WIFI6-POE-ETH-Schematic.pdf), [FAQ](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH/FAQ), [ESP-IDF instructions](https://docs.waveshare.com/ESP32-P4-WIFI6-POE-ETH/ESP-IDF). Hashes, revision differences and Git commits are in the [source register](https://github.com/Mcgee1704/waveshare-esp32-p4-wifi6-poe-eth/blob/main/sources/README.md).

This catalog summarizes the evidence and points to the board repository for complete tables. MAC addresses, serial numbers, credentials, local network addresses, flash backups and raw logs remain private.

[Back to catalog](../README.md)
