---
title: Donor Marketplace Scan — 2026-09-16
date: 2026-09-16
status: living-snapshot
currency: IDR
scope: X220 Neo donor candidates seen on Indonesian marketplace listings
---

# Donor Marketplace Scan — 2026-09-16

This is a dated decision log for donor hardware considered for **X220 Neo**. It records the listing price, what is technically reusable, integration penalties, and the price at which a platform becomes interesting.

The current primary architecture remains the **GMKtec K8 Plus / Ryzen 7 8845HS** documented in `../03-k8-plus-donor.md`. These marketplace machines are alternatives, experimental branches, or potential cheap donors — not automatic replacements for the K8 Plus design.

## Quick comparison

| Candidate | Listing price | Board class | Compute | Power architecture | X220 donor fit | Current action |
|---|---:|---|---|---|---|---|
| HP EliteDesk 800 G2 Mini | Rp1,950,000 | proprietary mini-PC | i5-6500T, 4C/4T | external DC, desktop-mini | Low | Skip at listed price |
| Colorful B460I ITX build | Rp6,500,000 | Mini-ITX 170×170 mm | i3-10100F + GTX 1650M | ATX/SFX | Medium as board experiment | Do not buy whole system as donor; ask for split |
| ASRock DeskMini X300 package | Rp6,820,000 | Mini-STX 140×147 mm | Ryzen 5 3400G / Vega 11 | **native 19 V DC** | **High mechanically / medium overall** | Best architecture of these three; only buy PC portion at the right price |

## What X220 Neo wants from a donor

A donor becomes more attractive when it has:

1. small PCB footprint and low connector Z-height;
2. laptop-like DC power rather than a full ATX PSU;
3. SO-DIMM rather than tall desktop DIMMs;
4. integrated graphics good enough to avoid a mandatory discrete GPU;
5. serviceable RAM and NVMe;
6. low enough sustained power for a custom laptop cooling system;
7. a practical route to the internal panel through HDMI/DP/USB-C -> eDP;
8. a practical route to the X220 keyboard/TrackPoint through USB;
9. optional high-speed PCIe/OCuLink expansion rather than mandatory internal dGPU;
10. enough performance uplift to justify fabrication effort.

---

# 1. HP EliteDesk 800 G2 Mini — i5-6500T / 8 GB / 128 GB

## Listing snapshot

- Asking price: **Rp1,950,000**
- HP EliteDesk 800 G2 Mini
- Intel Core i5-6500T
- 8 GB RAM
- 128 GB SSD
- Wi-Fi + Bluetooth
- seller advertises USB-C / USB 3.0 and internal speaker

A current Indonesian Shopee result showed an 8 GB + 128 GB variant around **Rp1.83m**, while another 8 GB + 256 GB listing was around **Rp2.75m**. That makes Rp1.95m plausible as a complete usable mini-PC, but this is the wrong reason to buy it for X220 Neo: we would be paying normal complete-PC money for an old donor.

## Compatibility

### Can reuse

- motherboard + CPU;
- DDR4 memory;
- SSD;
- Wi-Fi/Bluetooth module;
- stock blower/heatsink as a reference or possibly in a thick custom base;
- speaker / small internal harnesses if useful.

### Cannot use directly

- X220 LCD: requires an external-display-to-eDP/LVDS controller path;
- X220 battery: HP board has no ThinkPad battery/BMS interface;
- X220 keyboard/TrackPoint: requires a USB controller/interface;
- stock X220 cooling assembly: not designed for the HP board/socket layout;
- modern GPU expansion: this platform has no useful native laptop-friendly high-bandwidth expansion path.

## Main penalties

- Skylake i5-6500T is only 4 cores / 4 threads and is old enough that fabrication effort is difficult to justify.
- Proprietary board layout and connectors reduce reuse outside this exact platform.
- No native internal laptop display path.
- No native laptop battery management.
- Limited upgrade ceiling compared with the other candidates.

## Decision

**Skip at Rp1.95m.**

Interesting only as a very cheap sacrificial donor, roughly if the board/CPU/cooler bundle appeared far below complete-system pricing. It is better preserved as a functioning mini-PC than destroyed for X220 Neo at the current asking price.

### Price reference

- Shopee, EliteDesk 800 G2 Mini i5-6500T 8 GB + 128 GB variant: ~Rp1.83m at scan time.
- Shopee, EliteDesk 800 G2 Mini i5-6500T 8 GB + 256 GB: ~Rp2.75m at scan time.

Sources:
- https://support.hp.com/id-en/product/setup-user-guides/hp-elitedesk-800-35w-g2-desktop-mini-pc/7633266
- https://shopee.co.id/HP-EliteDesk-800-G2-Mini-i5-Gen-6-Bekas-Like-New-%E2%80%93-Cocok-Kantor-Usaha%21-Bergarnsi-i.1590032125.55306269476
- https://shopee.co.id/MINI-PC-HP-ELITEDESK-800-G2-I5-6500T-RAM-8GB-SSD-256GB-i.561405179.21788445367

---

# 2. Colorful B460I Mini-ITX — i3-10100F + VenomRX GTX 1650M

## Listing snapshot

- Asking price: **Rp6,500,000**
- Intel Core i3-10100F, 10th gen
- V-GEN 16 GB DDR4-3200
- 256 GB SATA SSD
- Colorful B460I V20 motherboard with Wi-Fi/Bluetooth
- VenomRX GTX 1650M 4 GB GDDR6 PCIe graphics card
- FSP SFX 450 W 80+ Bronze PSU
- MetalFish T40 ITX case

The Colorful CVN B460I family is standard **Mini-ITX, 170×170 mm**, LGA1200, with DDR4 DIMMs, PCIe 3.0 x16, M.2, HDMI/DP and Wi-Fi capability. The i3-10100F is 4 cores / 8 threads and a **65 W** desktop CPU. The `F` CPU has no usable integrated graphics, so the listing's discrete GPU is mandatory unless the CPU is replaced.

The VenomRX GTX 1650M card is a desktop PCIe card built around a mobile GTX 1650 GPU. VenomRX lists **4 GB GDDR6, PCIe 3.0, ~50 W consumption, and no auxiliary GPU power connector**.

## Compatibility

### Can reuse

- Mini-ITX motherboard;
- socketed LGA1200 CPU platform;
- 16 GB DDR4;
- M.2 storage path;
- Wi-Fi/Bluetooth;
- PCIe x16 for experimental GPU / riser arrangements;
- GPU itself for a bench or dock experiment.

### Cannot use directly

- FSP SFX PSU inside an X220-sized chassis: far too large;
- MetalFish T40 case: irrelevant to the laptop conversion;
- stock desktop tower-style GPU placement: too tall for an X220 base;
- stock desktop CPU cooling: likely requires a custom low-profile thermal solution;
- X220 LCD/battery/keyboard: still need the same display controller, battery power architecture and keyboard controller used by other desktop-derived donors.

## Main penalties

### 1. Mandatory GPU with current CPU

The **i3-10100F has no iGPU**, so removing the GTX 1650M leaves no display engine. For an X220 build the CPU should be replaced with a non-F LGA1200 chip if integrated graphics are desired.

### 2. Thermal budget

Nominal platform load is already approximately:

- CPU TDP: **65 W**;
- GPU: **~50 W**;
- plus board, memory, storage, display conversion and charging losses.

That is a workstation/cyberdeck thermal problem, not a stock-laptop thermal problem.

### 3. Desktop mechanical stack

- 170×170 mm motherboard is physically possible within the X220 footprint, but large relative to Mini-STX/mini-PC boards.
- Desktop DIMMs add Z-height.
- 24-pin ATX + 8-pin CPU power wiring is bulky.
- PCIe GPU requires a riser and a second cooling zone.

## Decision

**Good technology, poor whole-system donor purchase at Rp6.5m.**

The interesting object is the **B460I motherboard**, not the complete PC. Ask the seller whether they will split:

- motherboard only;
- motherboard + RAM;
- motherboard + CPU + RAM without GPU/PSU/case.

Used i3-10100F listings scanned around **Rp450k–800k**; VenomRX's own GTX 1650M page listed **Rp1.854m** when scanned. This reinforces that a large part of the Rp6.5m package price is hardware we do not need inside the laptop.

### Experimental branch value

This platform is worth preserving in the project as an **"X220 Neo Mini-ITX / high-power branch"** because it offers real PCIe x16 and a socketed desktop CPU. It should not replace the main low-power mini-PC architecture unless the goal changes toward a thick workstation X220.

Sources:
- https://manualzz.com/doc/76614880/colorful-cvn-b460i-gaming-frozen-v20-motherboard-owner-s-...
- https://detail.zol.com.cn/1342/1341370/param.shtml
- https://www.intel.com/content/www/us/en/products/compare.html?productIds=203474%2C203473
- https://venomrxs.com/shop/product/gtx1650m-4gb-ddr6/overview
- https://shopee.co.id/CPU-Processor-Intel-i3-10100F-Bekas-i.124576737.41220434878

---

# 3. ASRock DeskMini X300 package — Ryzen 5 3400G

## Listing snapshot

- Asking price for the entire package: **Rp6,820,000**
- AMD Ryzen 5 3400G, purchased 29 Jan 2026; seller says receipt and warranty remain
- ASRock DeskMini X300, purchased 29 Jan 2026; seller says warranty remains
- Lexar NM620 NVMe SSD, seller reports 97% health and ~47 °C average; **capacity not visible in supplied screenshot and must be verified**
- Team Group 16 GB DDR4-3200, **single channel**
- Vortex Mono V1 keyboard
- PressPlay Atlas Lite mouse
- APC 700 VA / 360 W UPS, purchased 22 Jul 2026
- Acer 24-inch 100 Hz monitor, exact model not visible in supplied screenshot

## Why this is technically important

This is the **best donor-board architecture of the three listings scanned today**.

The DeskMini X300 uses ASRock's **X300M-STX Mini-STX motherboard**, approximately **140 × 147 mm**. That is materially smaller than a 170 × 170 mm Mini-ITX board and is very attractive for the X220 footprint.

Most importantly, the board already uses a **19 V DC input**. ASRock specifies a 120 W adapter for 65 W CPUs and a 90 W adapter for 35 W CPUs. This is much closer to laptop/mini-PC power architecture than the B460I + SFX PSU approach and conceptually matches the existing 19 V K8 Plus project architecture.

Official X300 family characteristics include:

- AM4 socket;
- APU support up to 65 W;
- 2× DDR4 SO-DIMM;
- up to 64 GB on the original DeskMini X300 family;
- 2× M.2 2280 storage slots;
- 2× 2.5-inch SATA support;
- M.2 Key-E Wi-Fi/Bluetooth slot;
- HDMI + DisplayPort + D-Sub;
- front USB-C and USB-A;
- 19 V DC input;
- internal front-panel / speaker / audio / USB headers.

ASRock's current DeskMini X300 page lists support for **Cezanne, Renoir, Picasso and Raven Ridge APUs up to 65 W**, so the platform has a useful upgrade path beyond the included 3400G. Exact motherboard revision and BIOS version must be checked before purchasing a newer APU.

## Included Ryzen 5 3400G

AMD specifies the Ryzen 5 3400G as:

- Zen+ / Picasso;
- 4 cores / 8 threads;
- 3.7 GHz base, up to 4.2 GHz boost;
- Radeon RX Vega 11 integrated graphics;
- 65 W default TDP;
- 45–65 W configurable TDP.

The CPU is adequate for an experimental build but not compelling enough by itself to justify major fabrication. The **X300 board is the valuable part** because the APU can later be changed.

## Compatibility

### Strong positives

- **140 × 147 mm Mini-STX PCB:** far easier to package than Mini-ITX.
- **19 V DC input:** eliminates the need for an internal ATX/SFX PSU.
- **SO-DIMM:** much lower Z-height than desktop DIMMs.
- **Integrated graphics:** no mandatory internal GPU card.
- **Socketed AM4 APU:** upgradeable.
- **2× M.2:** one can remain storage while the second becomes an experimental PCIe expansion path.
- **Internal headers:** easier to adapt power button / USB / audio than many proprietary mini-PC boards.

### Still requires engineering

- X220 internal display still needs HDMI/DP -> eDP conversion unless a different panel/controller architecture is chosen.
- X220 keyboard + TrackPoint still require the existing USB-controller approach.
- X220 battery still needs a proper battery/BMS/DC power design; 19 V input makes the conversion cleaner but does not make the battery plug-and-play.
- Stock DeskMini cooler is too tall to assume it fits under an X220 keyboard/palmrest; custom blower/heatpipe work or a thicker bottom chassis is likely.
- Original DeskMini X300 documentation states **S3 sleep is not supported**. For laptop behavior we may rely on hibernate/modern OS behavior instead; this must be tested.

## Single-channel RAM problem

The seller's 16 GB is one module. For an APU, this is an avoidable performance penalty because the iGPU shares system memory bandwidth. If this donor is used, plan for a second matched SO-DIMM or replace the kit with dual-channel memory.

## GPU / OCuLink possibilities

There is no native PCIe x16 slot and no native OCuLink port. However, the X300 exposes M.2 PCIe lanes. An experimental branch could use one M.2 M-key slot with an M.2-to-OCuLink / PCIe adapter for an external GPU.

Treat this as **experimental, not guaranteed**:

- sacrifices one M.2 slot;
- PCIe generation is older than the K8 Plus native OCuLink path;
- cable routing and boot compatibility need bench validation;
- not hot-plug by default.

The K8 Plus remains much cleaner for eGPU use because OCuLink is native and documented.

## Pricing assessment

The Rp6.82m asking price is for a **bundle**, not just the donor PC. That matters.

Current comparison points found during this scan:

- New ASRock DeskMini X300 barebone listing: **from ~Rp2.55m** depending variant.
- Used DeskMini X300 + 16 GB (2×8 GB) + adapter listing: **Rp2.50m**.
- Used Ryzen 5 3400G listings: roughly **Rp800k–1.15m**.

That implies the donor-relevant X300 + 16 GB + 3400G core is roughly in the **low-to-mid Rp3m range before SSD**, based on the limited used-market samples above. SSD value cannot be assessed until capacity is known.

Therefore:

- **Rp6.82m bundle solely to harvest the X300:** no.
- **If you also genuinely need the 24-inch monitor, UPS, keyboard and mouse:** the complete bundle may be reasonable, but it should be judged as a workstation bundle, not as a donor.
- **If seller will split the PC:** this becomes interesting.

### Negotiation target for X220 Neo

For the **DeskMini X300 + Ryzen 5 3400G + 16 GB + adapter**, without monitor/UPS/peripherals:

- **≤ Rp3.5m:** attractive donor territory;
- **~Rp3.5m–4.0m:** potentially acceptable if SSD is useful capacity, warranty is real, board/adapter are complete and condition tests clean;
- **> Rp4.0m:** compare against newer mini-PC/APU donors before buying.

These are project buy targets, not claims of universal market value.

## Upgrade direction if acquired

The most X220-friendly version of this architecture would not necessarily keep the 3400G forever.

Preferred experiment:

```text
ASRock X300M-STX
    |
    +-- 35 W-class AM4 APU if supported by BIOS
    +-- 2x SO-DIMM dual channel
    +-- NVMe
    +-- HDMI/DP -> eDP controller -> 12.5-inch panel
    +-- USB -> X220 keyboard/TrackPoint controller
    +-- 19 V power architecture
    +-- custom low-profile blower / heatpipe
    +-- optional second M.2 -> experimental external PCIe/OCuLink adapter
```

A 35 W-class APU would be much more sensible for the final laptop than intentionally running a 65 W desktop APU at full power.

## Decision

**Do not buy the Rp6.82m package just to obtain the donor.**

But unlike the HP and unlike the complete B460I build, the **ASRock X300 itself is genuinely donor-worthy**. If the seller will split out the DeskMini PC around the target range above, this should be kept on the shortlist and measured physically.

It is currently the strongest alternative architecture found in today's local-market scan because it combines:

**Mini-STX size + 19 V DC + SO-DIMM + socketed AM4 APU + integrated graphics + dual M.2.**

Its primary disadvantages versus the K8 Plus are older compute/iGPU performance, no native OCuLink, no native internal eDP, no native laptop battery management, and a more difficult thermal envelope with a 65 W APU.

Sources:
- https://www.asrock.com/nettop/AMD/DeskMini%20X300%20Series/
- https://www.asrock.com/mb/AMD/x300m-stx/index.asp
- https://www.amd.com/en/support/downloads/drivers.html/processors/ryzen/ryzen-3000-series/amd-ryzen-5-3400g.html
- https://shopee.co.id/Asrock-Deskmini-X300-Barebone-Mini-PC-X-300-i.40255164.22257773933
- https://id.carousell.com/p/asrock-deskmini-x300-16gb-8x2-ddr4-1426350335/
- https://id.carousell.com/p/processor-amd-ryzen-5-3400g-bekas-1404365670/
- https://shopee.co.id/Processor-AMD-Ryzen-5-3400G-Bekas-i.19456227.24090622742

---

# Current shortlist after 2026-09-16 scan

## Primary architecture

**GMKtec K8 Plus / Ryzen 7 8845HS**

Best overall mix currently documented in the repo: modern Zen 4 performance, Radeon 780M, DDR5 SO-DIMM, 19 V input, compact mini-PC packaging and native OCuLink.

## Alternative A — ASRock X300 Mini-STX

Keep active as the **budget/socketed APU branch**.

Buy only when the donor PC is separated from unrelated bundle items and priced competitively. Especially interesting if a later 35 W APU can be sourced cheaply.

## Alternative B — B460I Mini-ITX

Keep as the **high-power / desktop modularity branch**.

Useful for learning, PCIe x16 and socketed CPU experimentation, but requires much more volume, power wiring and cooling work.

## Reject / sacrificial only — HP EliteDesk 800 G2

Do not design the project around it unless acquired extremely cheaply. The hardware works, but the performance age and proprietary platform do not justify the same mechanical/electrical effort.

---

# Questions to ask sellers before purchase

For future donor listings, collect these before paying:

- exact motherboard model / revision;
- BIOS version;
- exact CPU/APU;
- RAM module count and capacity per stick;
- SSD model + capacity + SMART/health;
- original power adapter voltage/wattage;
- Wi-Fi module model;
- whether every USB/display/audio port works;
- idle and load temperatures;
- whether BIOS can be entered normally;
- whether the machine survives a 20–30 minute CPU/iGPU stress test;
- whether seller will sell motherboard/PC separately from case/monitor/UPS/peripherals;
- clear top/bottom/internal photos with a ruler if physical dimensions are not published.

Every future listing should be appended to a dated scan rather than overwriting this historical snapshot.
