---
title: GMKtec K8 Plus Donor
updated: 2026-09-12
---

# GMKtec K8 Plus — donor platform

## Why it is the primary design

It combines laptop-class power consumption with desktop-mini-PC serviceability and an unusually useful OCuLink port.

## Verified manufacturer specifications

| Item | Specification |
|---|---|
| CPU | AMD Ryzen 7 8845HS |
| CPU | 8 cores / 16 threads, Zen 4 |
| Frequency | 3.8 GHz base, up to 5.1 GHz boost |
| CPU TDP | 35–54 W configurable; manufacturer lists peak up to 70 W |
| iGPU | Radeon 780M, RDNA 3, 12 CU |
| RAM | 2× DDR5-5600 SO-DIMM |
| Max RAM | 96 GB |
| Storage | 2× M.2 2280 PCIe 4.0 NVMe |
| Wi-Fi | Intel AX200 Wi-Fi 6 |
| Ethernet | 2× Intel I226V 2.5 GbE |
| Display outputs | HDMI 2.1, DP 2.1, 2× USB4 DP Alt Mode |
| USB4 | 2× 40 Gbps, manufacturer lists PD3.0 / DP1.4 capability |
| eGPU | OCuLink PCIe 4.0 ×4 |
| Audio | 3.5 mm jack + onboard digital mic |
| Verified power input | DC 19 V / 6.32 A |
| Adapter | 120 W |
| Full mini-PC dimensions | 132 × 125 × 58 mm |
| OS | Windows 11 / Linux supported |

## Critical integration note

The **132 × 125 × 58 mm measurement is the assembled mini-PC**, not the naked motherboard. Exact PCB outline, connector Z-height, mounting-hole positions, and cooler envelope are not published in the official spec and therefore remain `TBD-MEASURE`.

Do not create final CAD from photos.

## Cooling

GMKtec's teardown describes a turbine/blower + VC heat-pipe/copper cooling assembly. A detailed third-party teardown measured the heatsink portion at about **90 × 37 × 13.5 mm** and identified a roughly 60 mm blower. Those dimensions are useful planning references but the **complete cooler must still be measured physically**.

## Port strategy

### Keep accessible if practical
- one USB4;
- two USB-A;
- 3.5 mm audio;
- OCuLink;
- DC input;
- one display output for diagnostics.

### Can be hidden/internal or sacrificed in V1
- second Ethernet;
- second external display connector;
- Kensington lock.

## OCuLink warning

GMKtec explicitly states that OCuLink is **not hot-pluggable**. Power the machine off before connecting or disconnecting an eGPU cable.
