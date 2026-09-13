# Decision Log

## ADR-001 — K8 Plus is primary donor
**Status:** accepted 2026-09-12

Reasons:
- Ryzen 7 8845HS performance;
- Radeon 780M;
- 2× SO-DIMM;
- 2× NVMe;
- OCuLink x4;
- standard mini-PC donor is more obtainable than boutique X220 boards.

## ADR-002 — no battery in V0
**Status:** accepted

Reason: eliminate charging/BMS/power-conversion risk until compute/display/thermal/mechanical systems work.

## ADR-003 — preserve stock K8 cooler
**Status:** accepted

Reason: known thermal solution for the APU, much lower risk than inventing a laptop cooler immediately.

## ADR-004 — external OCuLink GPU, not internal dGPU
**Status:** accepted

Reason: keeps mobile thermal/power design manageable.

## ADR-005 — HDMI-to-eDP for first display prototype
**Status:** accepted

Reason: cheap, observable, easy to debug; can optimize later.
