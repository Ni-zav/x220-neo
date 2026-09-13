---
title: X220 Neo Home
tags: [x220-neo, dashboard]
updated: 2026-09-12
---

# X220 Neo — Home

## Objective

Build a modern, repairable computer inside the physical/interaction language of the ThinkPad X220 without paying for an exotic bespoke X220 motherboard.

## Target V1

| Subsystem | Target |
|---|---|
| Compute | GMKtec K8 Plus donor motherboard |
| CPU | AMD Ryzen 7 8845HS, 8C/16T |
| iGPU | Radeon 780M, RDNA 3, 12 CU |
| RAM | 32 GB DDR5-5600 as **2×16 GB**; board supports up to 96 GB |
| Storage | 1 TB PCIe 4.0 NVMe; second M.2 retained if possible |
| Display | 12.5" FHD IPS eDP, 30-pin |
| Keyboard | Original X220 7-row |
| Pointing | Original TrackPoint + buttons |
| Cooling | Original K8 Plus copper/VC cooler + blower |
| Power V0 | Stock 19 V / 6.32 A / 120 W adapter |
| Power V2 | Battery only after dedicated design review |
| External GPU | OCuLink PCIe 4.0 ×4, optional |
| Chassis | Original upper identity + custom internal frame / D-cover |
| OS | Ubuntu/Linux first; Windows optional |

## Current build gates

- [ ] Buy / obtain sacrificial spare X220 bottom case before irreversible cutting.
- [ ] Acquire donor compute platform.
- [ ] Bench-test donor completely before disassembly.
- [ ] Measure naked donor PCB and cooler.
- [ ] Prototype keyboard/TrackPoint over USB.
- [ ] Prototype FHD eDP panel on bench.
- [ ] Create first CAD envelope model.
- [ ] Print low-cost PETG fit prototype.
- [ ] Complete V0 transplant using external 120 W adapter.
- [ ] Thermal/load validation.
- [ ] Only then design carrier PCB and battery phase.

## Navigation

### Technical
- [System architecture](docs/01-system-architecture.md)
- [X220 baseline](docs/02-x220-baseline.md)
- [K8 Plus donor](docs/03-k8-plus-donor.md)
- [Mechanical integration](docs/04-mechanical-integration.md)
- [Display](docs/05-display-system.md)
- [Keyboard + TrackPoint](docs/06-keyboard-trackpoint.md)
- [Power + battery](docs/07-power-and-battery.md)
- [Cooling](docs/08-thermal-cooling.md)
- [Audio / wireless / I/O](docs/09-audio-wireless-io.md)
- [Carrier PCB](docs/10-carrier-pcb.md)
- [OCulink eGPU](docs/11-oculink-egpu.md)
- [Software / firmware](docs/12-software-firmware.md)

### Planning & buying
- [BOM](purchasing/BOM.md)
- [Tools](purchasing/Tools.md)
- [Price snapshot](purchasing/Price-Snapshot-2026-09-12.md)
- [Indonesia buying strategy](purchasing/Shopping-Strategy-Indonesia.md)
- [Milestones](planning/Milestones.md)
- [Backlog](planning/Backlog.md)
- [Risks](planning/Risk-Register.md)
- [Unknowns to measure](planning/Unknowns-To-Measure.md)
