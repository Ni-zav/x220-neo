---
title: Bill of Materials
updated: 2026-09-12
---

# Bill of Materials

Prices are planning values, not promises. See the dated price snapshot for exact sources.

## P0 — buy first

| Qty | Item | Target / spec | Budget | Why |
|---:|---|---|---:|---|
| 1 | Spare X220 bottom case | sacrificial D-cover | Rp105k–125k | cut this before original shell |
| 1 | K8 Plus donor | Ryzen 7 8845HS barebone | ~Rp8.4m before shipping estimate after normal import tax; local/used varies | main compute |
| 2 | DDR5 SO-DIMM | 16 GB DDR5-5600 each | ~Rp1.9m–5m total target depending seller | 32 GB dual-channel for iGPU bandwidth |
| 1 | NVMe SSD | 1 TB PCIe 4.0 M.2 2280 | ~Rp1.78m–1.85m | system storage |

> Dual-channel matters for an integrated GPU. Prefer **2×16 GB**, not 1×32 GB, unless there is a later 64/96 GB plan that justifies temporary single-channel operation.

## P1 — bench integration

| Qty | Item | Target | Budget |
|---:|---|---|---:|
| 1 | 12.5" FHD IPS panel | 1920×1080, 30-pin eDP | Rp735k–1.2m |
| 1 | HDMI-to-eDP controller | 1920×1080, 30-pin | Rp320k–360k |
| 1 | Keyboard controller | TP Art **or** DIY | US$59 imported **or** Rp80k–500k DIY |
| 1 | RP2040 dev board | if DIY | Rp40k–110k |
| 1 | Extra eDP cable / panel cable | controller-specific | Rp50k–150k allowance |
| 1 | Internal USB hub | only if port topology requires it | Rp50k–150k allowance |
| 1 | Small audio amp | only after speaker check | Rp10k–50k allowance |
| — | Wire, JST/connectors, heat-shrink, Kapton, VHB | mixed | Rp200k–500k allowance |

## P2 — mechanical

| Qty | Item | Budget |
|---:|---|---:|
| 1+ | PETG prototype prints | ~Rp350–930/g service rate | Rp250k–500k per large revision target |
| 1 | Laptop screw assortment | M2/M2.5/M3 | Rp48k–175k |
| 1 | Heat-set inserts | M2/M2.5/M3 mix | Rp50k–250k |
| — | Aluminium reinforcement / brackets | local fabrication | Rp100k–500k allowance |
| — | Foam gasket / rubber feet / adhesive | | Rp50k–150k |

## P3 — after V0 works

- final PA12/nylon/CF structural print;
- custom carrier PCB;
- clean port extensions/daughterboards;
- refined speaker solution;
- webcam;
- battery R&D;
- OCuLink eGPU dock.

## Do not buy early

- liquid cooling;
- desktop GPU/eGPU dock;
- expensive AX210 replacement;
- custom battery cells/BMS;
- final carbon/nylon chassis print;
- custom PCB before breadboard wiring is proven.
