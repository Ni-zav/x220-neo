---
title: Project Charter
updated: 2026-09-12
---

# Project Charter

## Problem

The stock X220 is mechanically and ergonomically excellent but its Sandy Bridge platform is now the limiting factor. Bespoke modern X220/X210-style boards exist, but cost and Indonesia availability make them poor value for this project.

## Goal

Create an **X220 Neo** that keeps the classic ThinkPad interaction experience while replacing the compute platform with readily sourced modern hardware.

## Must keep

- X220 7-row keyboard feel and layout.
- TrackPoint and physical buttons.
- X220 lid / hinge visual identity where practical.
- X220-class footprint and portable-laptop form.
- Serviceability: removable RAM/SSD where donor supports it.

## May replace

- Original motherboard and EC.
- Original LCD panel/cable.
- Original bottom chassis and internal frame.
- Battery system.
- Speakers, webcam, microphones, Wi-Fi antennas if integration becomes easier with modern replacements.
- Original port layout.

## Explicit non-goals for V1

- Designing an x86 Ryzen/Intel motherboard from scratch.
- Internal discrete GPU.
- Liquid cooling.
- Reusing the original X220 battery charging architecture before the main build works.
- Perfect factory-OEM exterior on the first prototype.

## Success criteria

V1 is successful when the machine:

- boots Ubuntu reliably;
- sleeps/wakes reliably enough for daily use;
- has working keyboard, TrackPoint/buttons, display, Wi-Fi, audio, USB;
- sustains CPU/GPU load without thermal shutdown or unsafe chassis temperatures;
- is structurally safe to carry by the palmrest/lid;
- can be serviced without destroying the shell;
- has documented wiring and repeatable assembly steps.
