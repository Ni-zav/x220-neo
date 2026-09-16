---
title: Donor Marketplace Scan 04 — 2026-09-16
date: 2026-09-16
status: living-snapshot
currency: IDR
scope: K8 Plus-class 8845HS and G10 3500U donor candidates
---

# Donor Marketplace Scan 04 — 2026-09-16

Continuation of the 16 September 2026 donor ledger.

## Quick comparison

| Candidate | Displayed price | Realistic interpretation | X220 Neo role | Current action |
|---|---:|---|---|---|
| GMKtec Ryzen 7 8845HS, 32 GB DDR5, 2 TB NVMe, OCuLink/USB4 | `Rp13.000` shown | Seller says price by DM, so actual price is **unknown**; if seller means ~Rp13m, it is strong | **Primary/final-build class** | Contact seller; verify exact model/price/SSD/warranty |
| GMKtec G10 Ryzen 5 3500U, 16 GB, 512 GB | `Rp4.300` shown | Interpreted as ~Rp4.3m marketplace shorthand | Cheap prototype / lower-cost donor | Fair-to-good used price; negotiate toward Rp3.8–4.0m |

---

# 8. GMKtec Ryzen 7 8845HS / 32 GB / 2 TB — likely K8 Plus

## Listing snapshot

Seller states:

- AMD Ryzen 7 8845HS, 8C/16T;
- 32 GB DDR5-5600, dual SO-DIMM;
- 2 TB M.2 2280 PCIe 4.0 NVMe;
- Wi-Fi 6 / Bluetooth 5.2;
- 2.5 GbE;
- OCuLink;
- USB-C / USB4;
- HDMI 2.1;
- DisplayPort 2.1;
- 3.5 mm audio;
- Windows 11 Pro;
- personal use, only used a few times;
- complete accessories;
- seller explicitly says **price by DM / negotiable**.

The displayed `Rp13.000` should therefore be treated as a **placeholder, not a verified Rp13m asking price**.

## Model identification

The combination of Ryzen 7 8845HS + Radeon 780M + 2× DDR5 SO-DIMM + dual 2.5 GbE + dual USB4 + OCuLink + HDMI 2.1 + DP 2.1 matches the **GMKtec NucBox K8 Plus** specification very closely. Exact bottom-label model should still be verified before purchase.

Official K8 Plus specification:
- Ryzen 7 8845HS, Zen 4, 8C/16T;
- Radeon 780M;
- DDR5-5600, 2× SO-DIMM;
- 2× M.2 2280 PCIe 4.0 NVMe;
- 2× USB4 40 Gbps;
- OCuLink PCIe 4.0 ×4;
- 2× Intel I226-V 2.5 GbE;
- 19 V / 6.32 A, 120 W adapter;
- assembled size 132 × 125 × 58 mm.

Source:
- https://www.gmktec.com/products/gmktec-nucbox-k8-plus-mini-pc-amd-ryzen%E2%84%A2-7-8845hs

## Why this is highly relevant

This is not merely a donor candidate; it is essentially the **already-documented primary X220 Neo architecture**.

Compared with the low-cost donors, it gives us:

- enough CPU headroom to justify the fabrication effort;
- Radeon 780M strong enough for a real daily-use X220 Neo;
- native OCuLink for future eGPU;
- dual USB4;
- dual NVMe;
- dual DDR5 SO-DIMM;
- external 19 V DC architecture;
- compact mini-PC board and laptop-class thermals.

## Price assessment

Current Indonesian references found during this scan:

- GMKtec Indonesia K8 Plus listing, 32 GB / 1 TB family: **Rp11.99m–15.99m depending variant**, currently out of stock on the surfaced page;
- another K8 Plus listing: **Rp14.299m–22.199m depending variant**;
- a third-party 32 GB / 1 TB listing: **Rp19.329m+**, clearly a poor comparison point;
- official GMKtec global store currently lists K8 Plus barebone at US$399.99 and a configured variant around US$479.99, before Indonesian import/local-market effects.

Therefore, if this seller's actual DM price is approximately:

- **≤ Rp12m:** excellent used buy, assuming clean tests;
- **Rp12m–13.5m:** strong value, especially with a genuine useful 2 TB SSD;
- **Rp13.5m–14.5m:** fair-to-good if warranty/receipt, SSD quality and condition are strong;
- **Rp14.5m–15.5m:** compare directly with new/local-warranty K8 Plus and the Rp10m K12 candidate before committing;
- **> Rp15.5m:** difficult to justify used unless the 2 TB SSD is premium and warranty is unusually good.

These are X220 Neo project thresholds rather than universal used-market values.

## Critical verification

Before assigning value to the 2 TB claim, ask for:

1. exact model sticker / `NucBox K8 Plus` confirmation;
2. actual DM asking price;
3. receipt / warranty status;
4. CrystalDiskInfo showing **SSD brand, exact model, power-on hours, total writes, temperature and health**;
5. CPU-Z / HWiNFO memory page confirming 32 GB and dual-channel configuration;
6. a short OCCT/Cinebench stability run with temperatures;
7. USB4 device test if possible;
8. OCuLink/eGPU test if seller has hardware available;
9. photo of original 120 W adapter label.

A low-end 2 TB SSD should not be valued the same as a high-quality TLC drive.

## Relationship to the Rp10m K12 candidate

If this K8 Plus is really around Rp13m, the comparison is:

- K8 Plus: 8845HS, 32 GB, 2 TB, known X220 Neo architecture;
- K12 candidate: Ryzen 7 H 255, 16 GB, 512 GB, around Rp10m.

The K12 is cheaper as a base platform. The K8 Plus becomes compelling if the included 32 GB RAM + 2 TB SSD are genuinely useful, the SSD is good quality, and the seller's actual price stays near Rp12–13m.

For a final X220 Neo build, either is in the correct performance class; the K8 Plus has the advantage that the repository is already designed around it.

## Decision

**High-priority candidate. Contact seller. Do not treat the displayed Rp13.000 as confirmed price.**

---

# 9. GMKtec G10 — Ryzen 5 3500U / 16 GB / 512 GB

## Listing snapshot

- displayed price: `Rp4.300`, interpreted as approximately **Rp4.3m** in marketplace shorthand;
- Ryzen 5 3500U;
- 16 GB DDR4-2400, dual-channel according to listing;
- 512 GB NVMe;
- compact G10 chassis;
- seller links a Shopee escrow / rekber listing;
- claims official one-year warranty in description.

Official GMKtec G10 specifications:

- Ryzen 5 3500U, 4C/8T, up to 3.7 GHz;
- Vega 8;
- 25 W TDP, max 35 W;
- 2× DDR4 SO-DIMM, up to 64 GB;
- 2× M.2 2280 PCIe 3.0×4;
- HDMI + DP + USB-C display;
- 2.5 GbE;
- Wi-Fi 5 / Bluetooth 5.0;
- USB-C PD / 19 V 3.42 A power;
- assembled size 103 × 98 × 42 mm.

Source:
- https://www.gmktec.com/products/gmktec-g10-amd-ryzen-5-3500u-mini-pc

## Current price reference

Current Indonesian listings show the G10 16 GB / 512 GB around **Rp5.979m–5.999m new** from active sellers.

Sources:
- https://shopee.co.id/GMKTEC-Mini-PC-Gaming-G10-AMD-Ryzen-5-3500U-16GB-RAM-DDR4-512-SSD-NVME-4K-DISPLAY-WIN-11-PRO-i.1641418034.27742510202
- https://shopee.co.id/GMKTEC-G10-Mini-PC-AMD-Ryzen-5-3500U-RAM-16GB-DDR4-SSD-512GB-NVMe-4K-Display-Windows-10-Pro-i.977133992.41562711237

At Rp4.3m, the used listing is roughly **28% below current ~Rp6m new pricing**, before accounting for vouchers, warranty differences or SSD/RAM brand.

## Donor compatibility

### Positives

- exceptionally compact 103 × 98 mm footprint;
- low 25–35 W thermal class;
- 19 V USB-C power input;
- two SO-DIMM slots;
- two M.2 slots;
- HDMI/DP/USB-C display outputs;
- 2.5 GbE;
- much easier mechanically than Mini-ITX/Desktop donors.

### Limitations

- Ryzen 5 3500U is a 2019-era Zen+ 4C/8T platform;
- Vega 8 is far behind Radeon 780M;
- soldered CPU, no upgrade path;
- no native OCuLink;
- no USB4;
- PCIe 3.0 rather than PCIe 4.0;
- Wi-Fi 5 unless upgraded;
- fabrication effort is difficult to justify as the final X220 Neo brain when newer mini-PC donors exist.

## Price interpretation for X220 Neo

At approximately **Rp4.3m**, this is materially better than the earlier Rp6.5m G10 32 GB / 1 TB listing.

Project thresholds:

- **≤ Rp3.5m:** excellent cheap experiment / sacrificial donor;
- **Rp3.5m–4.0m:** good donor value;
- **Rp4.0m–4.3m:** acceptable if full-set, healthy and warranty is real;
- **Rp4.3m–4.8m:** okay as a complete mini-PC, but only marginal for X220 Neo;
- **≥ Rp5m:** buy a newer platform instead.

## Best role in this project

The G10 makes more sense as a **V0 cheap prototype donor** than as the final machine:

- validate X220 keyboard/TrackPoint USB controller;
- validate HDMI/DP-to-eDP display pipeline;
- prototype DC power and physical mounting;
- test airflow and chassis printing without risking a Rp10m–13m K8/K12 board.

However, mechanical mounts made specifically for the G10 will not transfer directly to K8/K12, so it is only useful if the cheap prototype itself has value to the project.

## Decision

**At Rp4.3m: fair-to-good used price, but negotiate.**

Suggested target:

- open around **Rp3.6m–3.8m**;
- settling around **Rp3.8m–4.0m** would be attractive;
- Rp4.3m is still defensible if receipt/warranty, RAM, SSD and adapter check out.

For the final X220 Neo, prefer K8 Plus/K12-class hardware.
