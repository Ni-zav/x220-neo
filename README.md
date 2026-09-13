# X220 Neo

A practical, Indonesia-first project to rebuild a ThinkPad X220 around modern compute hardware while preserving the parts that make the X220 feel like an X220: the 7-row keyboard, TrackPoint, lid/hinges, palmrest, proportions, and serviceable spirit.

**Current reference architecture:** GMKtec K8 Plus donor board (Ryzen 7 8845HS + Radeon 780M), original donor cooler, DDR5 SO-DIMM, NVMe, 12.5-inch FHD eDP display, original X220 keyboard/TrackPoint through a USB controller, custom lower chassis/midframe, external 19 V power for V0, optional OCuLink eGPU later.

> [!IMPORTANT]
> This repository intentionally separates **verified specifications**, **design decisions**, and **unknowns that must be measured on the physical donor**. Do not CAD around guessed motherboard dimensions.

## Start here

1. [Home](Home.md) — project dashboard.
2. [Project charter](docs/00-project-charter.md) — goals and non-goals.
3. [System architecture](docs/01-system-architecture.md) — how everything connects.
4. [BOM](purchasing/BOM.md) — what to buy, in what order.
5. [Price snapshot](purchasing/Price-Snapshot-2026-09-12.md) — researched Indonesia prices and links.
6. [Build sequence](planning/Milestones.md) — phased plan with stop/go gates.
7. [Unknowns to measure](planning/Unknowns-To-Measure.md) — do not skip this.
8. [Sources](reference/Sources.md) — source-of-truth links.

## Repository / Obsidian vault layout

```text
x220-neo/
├── Home.md
├── README.md
├── AGENTS.md
├── docs/                 # architecture and technical design
├── build/                # step-by-step build procedures
├── purchasing/           # BOM, tools, prices, buying strategy
├── planning/             # milestones, backlog, risks, decisions
├── reference/            # connections, measurements, tests, sources
├── templates/            # repeatable logging templates
├── cad/                  # future CAD source files
├── pcb/                  # future KiCad carrier-board files
├── firmware/             # future RP2040/QMK firmware
└── media/                # photos / measurements / teardown images
```

This folder is both **Git-repo ready** and **Obsidian-vault ready**. In Obsidian choose **Open folder as vault**. In Git, run `git init` at the root.

## Core principle

The project does **not** attempt to design a Ryzen motherboard from scratch. The custom engineering is concentrated where it is realistic and reusable:

- mechanical midframe / D-cover;
- port placement and extensions;
- keyboard + TrackPoint controller;
- future carrier/controller PCB;
- power distribution;
- display integration;
- thermal ducting;
- optional battery subsystem after V0 is stable.

## Current design status

- Architecture: **selected** — K8 Plus is primary donor.
- Donor exact PCB dimensions/hole coordinates: **must measure after purchase**.
- V0 power: **selected** — stock 120 W adapter.
- Display prototype: **selected** — HDMI-to-eDP + 12.5" FHD eDP panel.
- Keyboard: **two paths** — TP Art board for fastest success or RP2040/QMK for custom build.
- Battery: **deferred** until V0 passes thermal/stability testing.
- Internal dGPU: **not planned**; OCuLink eGPU is optional.

## Safety

Read [Safety](docs/13-safety.md) before cutting, soldering, or experimenting with batteries.
