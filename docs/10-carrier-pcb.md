---
title: Carrier PCB
updated: 2026-09-12
---

# Custom Carrier / Controller PCB

## Purpose

The custom PCB should solve **integration**, not replace the x86 motherboard.

## Rev A scope

Possible functions:

- X220 keyboard connector;
- keyboard matrix interface to RP2040 or MCU;
- TrackPoint PS/2 CLK/DATA/RESET handling;
- TrackPoint buttons;
- Caps/mute/mic/status LEDs;
- USB connection to K8 Plus;
- ThinkLight control if desired;
- lid switch input;
- power-button interface **only after donor button circuitry is verified**;
- optional internal USB hub header;
- optional audio/control connectors.

## Intentionally excluded from Rev A

- CPU power conversion;
- battery charging;
- high-power 19 V regulation;
- USB4 retiming;
- PCIe/OCuLink rerouting;
- eDP signal conversion.

Those dramatically increase PCB risk.

## Development sequence

1. Breadboard / breakout proof of keyboard + TrackPoint.
2. Capture tested pinout in `reference/Connection-Map.md`.
3. KiCad schematic.
4. ERC.
5. PCB with debug pads and generous test points.
6. Order 5 inexpensive prototypes.
7. Bench-test outside the laptop.
8. Only then mechanically integrate.

## Design-for-debug features

- labelled test pads;
- reset/boot access for MCU;
- USB disconnect jumper;
- current-limited power input during first bring-up;
- connector orientation markings on silkscreen;
- spare GPIO pads.
