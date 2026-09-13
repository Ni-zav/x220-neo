---
title: Mechanical Integration
updated: 2026-09-13
---

# Mechanical Integration

## Mechanical architecture

The project treats the X220 exterior as a **human-interface shell**, not as a fixed motherboard tray.

### Preserve
- keyboard plane;
- palmrest ergonomics;
- hinge axis;
- lid proportions;
- TrackPoint button geometry.

### Redesign
- internal midframe;
- motherboard mounting bosses;
- bottom/D-cover;
- airflow openings;
- I/O cutouts;
- SSD/RAM access;
- display-controller mount.

## Reference material before modelling

Use the curated [X220 visual reference set](../media/reference/README.md) to understand the original assembly, bottom-case ribs/bosses, keyboard-bezel underside, motherboard cavity, cooler/exhaust area and hinges.

Use the [CAD reference registry](../cad/reference-meshes/README.md) for explicitly licensed third-party geometry/generators. These references are for topology and block-out work only; measured physical geometry remains authoritative.

## CAD workflow

1. Completely disassemble one X220.
2. Establish a master datum.
3. Measure keyboard underside, palmrest, hinges and screw bosses.
4. Disassemble K8 Plus only after full bench validation.
5. Measure board outline and all maximum component heights.
6. Scan/photograph orthographically with a ruler for reference.
7. Model simple bounding boxes first.
8. Run interference checks.
9. Print only critical fit-test coupons before a whole D-cover.
10. Build a coarse PETG shell.

For a Blender-first mock-up, make separate collections/objects for the X220 shell, keyboard/hinges, donor board/cooler, service keep-outs, and new Neo parts. The first scene should answer **what collides with what**, not attempt to be photorealistic.

## Required physical measurements

See [Measurement Sheet](../reference/Measurement-Sheet.md). The most important early dimensions are:

- `TBD-MEASURE` naked K8 PCB X/Y outline;
- `TBD-MEASURE` PCB mounting holes;
- `TBD-MEASURE` maximum component height top/bottom;
- `TBD-MEASURE` cooler total Z height;
- `TBD-MEASURE` blower inlet diameter/clearance;
- `TBD-MEASURE` keyboard underside keep-out;
- `TBD-MEASURE` hinge sweep volume;
- `TBD-MEASURE` panel-controller dimensions.

## Prototype materials

- **PETG:** recommended for inexpensive fit prototypes and early functional shells.
- **PA12/SLS or nylon-based print:** candidate final printed structural parts.
- **Aluminium sheet/rails:** recommended where hinge loads or palmrest flex require reinforcement.

Avoid relying on printed plastic alone for high-cycle hinge load until tested.

## Spare-shell strategy

A sacrificial X220 lower case is cheap enough in Indonesia that irreversible cutting should be performed on the spare first.
