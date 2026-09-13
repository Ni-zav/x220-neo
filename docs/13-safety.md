---
title: Safety
updated: 2026-09-12
---

# Safety

## Electrical

- Disconnect AC and batteries before mechanical work.
- Use current-limited bench power for new low-voltage circuits where possible.
- Verify polarity with a multimeter before first power-on.
- Insulate exposed PCB backs from metal chassis parts.
- Use strain relief on DC input and high-current wiring.
- Never assume two visually similar LCD-controller boards use the same input voltage.

## Lithium batteries

Battery integration is a separate project phase. Do not:

- solder directly to random reclaimed cells;
- bypass pack protection;
- charge a pack with an unverified generic module;
- enclose an untested battery next to the CPU cooler;
- rely on software as the only over-current/over-temperature protection.

## Mechanical

- Wear eye protection when using a rotary tool.
- Secure the workpiece before cutting.
- Deburr metal edges.
- Vacuum/clean conductive metal dust before electronics return to the chassis.
- Carbon/nylon-composite sanding dust requires appropriate respiratory protection and cleanup.

## Thermal

- Do first full-load tests on a non-flammable surface.
- Monitor temperatures after every airflow/chassis revision.
- Do not block the donor blower inlet or exhaust.

## OCuLink

Do not hot-plug the K8 Plus OCuLink connection.
