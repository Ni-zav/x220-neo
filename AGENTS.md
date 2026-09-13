# AGENTS.md — rules for AI/coding agents working on X220 Neo

## Source-of-truth hierarchy

1. Physical measurements recorded in `reference/Measurement-Sheet.md` and `media/`.
2. Manufacturer documentation in `reference/Sources.md`.
3. Tested community technical documentation.
4. Marketplace listing data only for price/availability, not electrical truth.

## Non-negotiable rules

- Never invent naked K8 Plus PCB dimensions, screw-hole coordinates, connector heights, or power-button pinout. Mark them `TBD-MEASURE` until physically measured.
- Never assume the K8 Plus USB4 ports can power the board. The verified input is the **19 V / 6.32 A DC input**.
- Never hot-plug OCuLink; GMKtec explicitly warns against it.
- Never design a custom lithium battery pack as a casual next step. Battery work requires a dedicated power/safety review.
- Preserve the donor CPU cooler until thermal validation proves an alternative is better.
- Keep all destructive chassis modifications reversible until the donor, keyboard, and display work on a bench.
- Prefer standard Markdown + Mermaid so the documentation works in both GitHub and Obsidian.
- When updating prices, preserve the old snapshot and create a new dated snapshot.

## CAD conventions

- Millimetres only.
- Master coordinate system: rear-left inner chassis datum unless changed by a recorded decision.
- Every dimension must be tagged as one of: `MEASURED`, `MANUFACTURER`, `DERIVED`, `ESTIMATE`.
- Maintain at least one interference-check assembly containing board, cooler, fan intake, display cable path, keyboard underside, hinges, and port extensions.

## Electronics conventions

- Each power rail must document source, nominal voltage, maximum expected current, protection, connector, and wire gauge.
- Do not power a display-controller board until its input voltage/polarity is verified from the actual purchased board.
- USB data and power are separate design concerns; avoid back-powering hosts/hubs.

## Definition of done for a subsystem

A subsystem is not "done" until it has:
1. a wiring/interface description;
2. a physical mounting description;
3. a test procedure;
4. a pass/fail criterion;
5. a rollback / failure note.
