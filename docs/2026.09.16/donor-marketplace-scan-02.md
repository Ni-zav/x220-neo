---
title: Donor Marketplace Scan 02 — 2026-09-16
date: 2026-09-16
status: living-snapshot
currency: IDR
scope: Additional X220 Neo donor candidates seen on Indonesian marketplace listings
---

# Donor Marketplace Scan 02 — 2026-09-16

Continuation of `donor-marketplace-scan.md` for additional candidates found later on 16 September 2026.

## Quick comparison

| Candidate | Listing price | Board / CPU class | Power | Mechanical fit | Performance / expansion fit | X220 Neo action |
|---|---:|---|---|---|---|---|
| GMKtec G3 Plus, Intel N150, 32 GB DDR4 | Rp6,000,000 mini-PC package | compact soldered N150 mini-PC board | 12 V / 3 A; 6 W CPU TDP | **Very good** | Low-medium | Keep as low-power branch; skip at Rp6m for main build |
| “Intel NUC i5 Gen 7 / 16 GB / 512 GB” listing | Rp4,500,000 | **identity/spec mismatch in listing** | unknown until exact model verified | potentially good | low even if i5-7200U | **Do not buy / verify first** |

---

# 4. GMKtec G3 Plus — Intel N150 / 32 GB DDR4

## Listing snapshot

Seller asks **Rp6,000,000 for the mini-PC package**. The supplied listing states:

- GMKtec G3 Plus;
- Intel Twin Lake N150;
- G.Skill Ripjaws 32 GB DDR4-3200 SO-DIMM;
- seller describes the mini-PC + RAM as already assembled and not sold separately;
- listing is part of a former NAS/home-server project;
- the Orico 2-bay DAS is listed separately at Rp2,050,000;
- the overall listing headline displays Rp8,000,000 because multiple package/variant options are being sold.

The seller-provided photo of the open unit shows the expected compact mini-PC layout with one SO-DIMM and M.2 storage area.

## Verified GMKtec specifications

GMKtec's current product page lists the G3 Plus as:

- Intel N150, 4 cores / 4 threads;
- up to 3.6 GHz;
- 6 MB cache;
- **6 W CPU TDP**;
- soldered FCBGA1264 package;
- Intel integrated graphics, 24 EUs, up to 1.0 GHz;
- **1× DDR4-3200 SO-DIMM**, up to 32 GB;
- **1× M.2 2280 PCIe 3.0 NVMe** storage slot;
- **1× M.2 2242 SATA** expansion slot;
- dual HDMI, up to 4K;
- Wi-Fi 6 / Bluetooth 5.2;
- Intel i226-V 2.5 GbE;
- **12 V / 3 A DC input**;
- assembled chassis dimensions **114 × 106 × 42.5 mm**.

Official source:
- https://www.gmktec.com/products/nucbox-g3-plus-enhanced-performance-mini-pc-with-intel-n150-processor

## Why this is interesting for X220 Neo

Mechanically and electrically, this is one of the easiest donor classes we have seen.

### Strong positives

- Very small complete system envelope.
- Very low CPU power compared with the 35–70 W class K8 Plus or 65 W desktop donors.
- Native DC input; no ATX/SFX PSU required.
- SO-DIMM is low-profile.
- Integrated graphics means no mandatory dGPU.
- Two physically separate M.2 storage paths.
- 2.5 GbE, Wi-Fi 6 and Bluetooth are modern enough for daily use.
- 12 V input is attractive for a future custom battery/DC architecture because the required system power is modest.

### What still does not connect directly

- X220 panel: G3 Plus exposes HDMI, not native laptop eDP, so the build still needs HDMI -> eDP conversion.
- X220 keyboard/TrackPoint: still needs a USB keyboard controller.
- X220 battery: still requires BMS, charging, protection and regulated system power; 12 V DC merely makes the load easier than a high-power desktop donor.
- Stock mini-PC cooling/chassis geometry cannot be assumed to fit under the X220 palmrest without physical measurements.

## Major limitation: performance ceiling

The N150 is soldered. There is **no CPU upgrade path**.

This makes the G3 Plus a very different architecture from the primary K8 Plus donor:

- excellent for low heat, silence, battery-oriented experiments, office work, Linux, light coding and server workloads;
- weak as the long-term heart of an X220 Neo intended for Blender, heavier compilation, VM-heavy work, GPU compute or workstation-class use;
- no native OCuLink;
- no USB4;
- substantially less GPU capability than Radeon 780M-class donors.

The single SO-DIMM is not a seller mistake: GMKtec officially specifies one memory slot, so the supplied 32 GB module already fills the platform's published maximum capacity.

## Expansion note

Do **not** assume the M.2 2280 slot gives a clean eGPU path. It is specified as PCIe 3.0 NVMe storage, but exact lane width, firmware behavior and boot compatibility for M.2-to-OCuLink adapters would need bench validation. The second M.2 2242 slot is SATA, not a PCIe eGPU path.

## Pricing assessment

The Rp6m seller price is not absurd for a complete 32 GB G3 Plus in the local market, but it is not attractive **as a sacrificial X220 donor**.

Current reference points from this scan:

- GMKtec official EU storefront lists G3 Plus barebone at about EUR159.99 and 16 GB + 512 GB at about EUR269.99, before Indonesian import/local-market effects.
- A current Indonesian retail result surfaced a 16 GB / 512 GB G3 Plus around Rp6.5m.

So the issue is not that the seller is obviously overpricing the complete PC. The issue is that **Rp6m fabrication money should buy more compute headroom for X220 Neo**.

## Decision

**Donor architecture: good. Main-project value at Rp6m: poor.**

Keep this as an explicit project branch:

> **X220 Neo Low-Power / N150 branch** — prioritize low heat, low power and simple DC integration over workstation performance.

For the current main build, the K8 Plus remains materially stronger because the extra cost buys an 8C/16T Zen 4 CPU, Radeon 780M, dual DDR5, dual PCIe 4.0 NVMe, USB4 and native OCuLink.

---

# 5. “NUC Mini PC i5 Gen 7 / 16 GB / 512 GB” — identity mismatch

## Listing snapshot

- Asking price: **Rp4,500,000**
- title/description says Core i5 Gen 7;
- image artwork says **i5-7200U**, 16 GB and 512 GB SSD;
- same artwork prominently says **NUC7CJYH ORIGINAL PRODUCT**;
- artwork says **DDR3**;
- seller description says Intel HD graphics and includes adapter.

## Critical problem: the advertised model and CPU cannot both be correct

Intel's official NUC7CJYH technical specification says that model uses a **soldered Celeron J4005**, 2 cores / 2 threads, up to 10 W TDP, with UHD Graphics 600.

Official source:
- https://www.intel.com/content/dam/support/us/en/documents/mini-pcs/nuc-kits/NUC7xJY_TechProdSpec.pdf

Therefore a machine advertised simultaneously as:

- `NUC7CJYH`, and
- `Core i5-7200U`

is internally inconsistent.

There is a second inconsistency: the stock graphic says DDR3, while genuine 7th-generation Intel NUC boards in this family use DDR4-class SO-DIMM memory.

Intel's genuine 7th-generation Core i5 NUC family also does not resolve the listing cleanly. Intel documentation for NUC7i5BNH/BNK identifies a 4×4-inch (101.6 × 101.6 mm) NUC board with DDR4 SO-DIMMs and a 12–19 V DC input, but the later official specification identifies the i5 model as an **i5-7260U** board rather than the `NUC7CJYH + i5-7200U` combination shown in the seller image.

Official Core-i5 NUC specification:
- https://www.intel.com/content/dam/support/us/en/documents/boardsandkits/NUC7i5BN_NUC5i7BN_TechProdSpec.pdf

## What this probably means

One of the following is true:

1. the seller used the wrong stock image;
2. the seller wrote the wrong processor/model;
3. this is a third-party NUC-style mini-PC rather than the Intel model shown;
4. the hardware has been misidentified by the reseller.

Do not choose between these possibilities without evidence.

## Required verification before considering it

Ask the seller for **all** of the following:

1. real photo of the exact unit being sold, not catalogue artwork;
2. photo of the bottom product label showing model / product code;
3. BIOS main page photo;
4. CPU-Z CPU tab or Windows Task Manager CPU page;
5. CPU-Z Memory/SPD tab showing DDR generation and module configuration;
6. CrystalDiskInfo / SSD model and health;
7. photo of internals with bottom cover removed.

If the bottom sticker really says `NUC7CJYH`, treat the CPU claim as wrong: genuine NUC7CJYH is J4005.

## X220 Neo compatibility if it really is a 7th-gen Core i5 NUC

A genuine 4×4 Intel NUC board would actually be mechanically attractive:

- approximately 101.6 × 101.6 mm board;
- low-profile SO-DIMMs;
- M.2 storage;
- integrated graphics;
- 12–19 V DC input;
- internal USB / front-panel headers on some NUC boards.

But even a legitimate i5-7200U/i5-7260U-era NUC is still a poor main donor in 2026:

- only 2 cores / 4 threads;
- soldered CPU;
- old integrated graphics;
- limited modern expansion;
- no reason to spend substantial fabrication time around it when newer N100/N150/Ryzen mini-PC boards are available.

It still requires external-display -> eDP conversion, keyboard/TrackPoint USB conversion and a custom battery power architecture.

## Pricing reality

At **Rp4.5m**, reject it regardless of which interpretation is correct.

Current Indonesian search results show genuine NUC7CJYH/J4005 systems far below this asking price; one second-hand 4 GB / 500 GB unit appeared around Rp1m, while older new/old-stock retailer pages for the J4005 kit are roughly Rp2.0m–2.4m. Those are not direct comparisons to a genuine Core-i5 NUC, but they demonstrate why the exact identity must be resolved before assigning value.

Sources:
- https://shopee.co.id/Mini-pc-Intel-BOXNUC7CJYHN-NUC-Kit-Intel-Celeron-J4005-Processor-i.24539943.23326438194
- https://shopee.co.id/Mini-PC-INTEL-NUC7CJYHN-Celeron-J4005-Windows-11-PRO-NUC-7CJYHN-i.272073158.20169769315

## Decision

**Hard skip at Rp4.5m. Identity must be verified before it is even treated as a valid donor candidate.**

This listing is useful to the project mainly as a warning: for marketplace donor research, **model label + CPU + RAM generation must agree before price analysis begins**.

---

# Updated donor categories after five listings

| Architecture | Examples scanned | Project interpretation |
|---|---|---|
| Modern high-performance mini-PC | GMKtec K8 Plus | Primary direction: strongest compute/expansion balance |
| Ultra-low-power mini-PC | GMKtec G3 Plus N150 | Excellent mechanical/power branch, limited compute ceiling |
| Mini-STX socketed APU | ASRock X300 | Very interesting experimental donor, especially at used-PC-only pricing |
| Mini-ITX desktop | B460I + 10100F + 1650M | High-power workstation/cyberdeck branch, mechanically expensive |
| Old proprietary mini-PC | HP EliteDesk 800 G2 | Only worth investigating if extremely cheap |
| Old / unverified NUC | “NUC7CJYH i5-7200U” listing | Reject until identity is proven; poor main donor even if genuine 7th-gen i5 |

## Current practical lesson

For X220 Neo, **small size alone is not enough**. The best donor combines small PCB, low-profile memory, DC input, modern integrated graphics, enough CPU headroom to justify fabrication, and a useful PCIe/USB4/OCuLink expansion story. This is why an N150 board can be mechanically easier than the K8 Plus yet still be a weaker main-project choice.
