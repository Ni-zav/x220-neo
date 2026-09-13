---
title: Software and Firmware
updated: 2026-09-12
---

# Software / Firmware

## OS target

Ubuntu/Linux first because the current X220 is already in the user's Linux workflow and GMKtec explicitly lists Linux support.

## Donor validation before transplant

Capture:

```bash
uname -a
lscpu
lspci -nn
lsusb
lsblk -o NAME,SIZE,MODEL,TRAN
sudo dmidecode -t system -t baseboard
sensors
ip link
```

Run memory/storage diagnostics and a sustained CPU/GPU load before opening the donor.

## Keyboard firmware

DIY controller target: QMK on RP2040 where practical.

Repository references in `reference/Sources.md` include:

- X220 keyboard connector/matrix reverse engineering;
- `thinkpad-ec` matrix tables;
- RP2040/QMK classic ThinkPad keyboard projects;
- TrackPoint PS/2 integration resources.

## Version-control strategy

Keep hardware revisions tagged:

- `kbd-controller-r0-breadboard`
- `kbd-controller-r1-pcb`
- `chassis-p0-fit`
- `chassis-p1-functional`
- `v0-bench`
- `v1-integrated`

Photos and measurements should reference the same revision IDs.
