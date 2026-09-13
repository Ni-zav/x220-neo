# Build 01 — Bench validate the donor

## Goal

Prove the K8 Plus is healthy **before modifying it**.

## Procedure

1. Photograph serial/board revision labels.
2. Boot using stock 120 W adapter.
3. Update firmware only if necessary and documented.
4. Confirm both SO-DIMM slots.
5. Confirm both NVMe slots.
6. Confirm HDMI, DP/USB4 video, USB-A, audio, Wi-Fi, Bluetooth, Ethernet.
7. Confirm OCuLink only if an eGPU setup is already available; otherwise leave it untouched.
8. Run memory and CPU/GPU stability tests.
9. Log temperatures/noise/power behaviour.

## Pass criteria

- no crashes under sustained load;
- all required I/O works;
- fan control behaves normally;
- no SSD/RAM errors.

Only after passing: disassemble donor and measure it.
