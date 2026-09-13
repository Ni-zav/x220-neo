---
title: System Architecture
updated: 2026-09-12
---

# System Architecture

## V0/V1 architecture

```mermaid
flowchart LR
    AC[AC mains] --> PSU[GMKtec 120 W adapter\n19 V / 6.32 A]
    PSU --> DCIN[K8 Plus DC input]
    DCIN --> K8[K8 Plus motherboard\nRyzen 7 8845HS + Radeon 780M]

    K8 -->|HDMI 2.1| EDPCTRL[HDMI-to-eDP controller]
    EDPCTRL -->|30-pin eDP| PANEL[12.5 in FHD IPS panel]

    K8 -->|USB 2.0/3.x| HUB[Internal USB hub - optional]
    HUB --> KBDMCU[Keyboard controller\nTP Art or RP2040/QMK]
    KBDMCU --> KBD[X220 7-row keyboard]
    KBDMCU --> TP[TrackPoint + buttons]

    K8 -->|3.5 mm analog| AMP[Small stereo amplifier]
    AMP --> SPK[X220 / replacement speakers]

    K8 --> WIFI[AX200 Wi-Fi 6\nreplace later only if needed]

    K8 -->|PCIe 4.0 x4| OC[OCuLink port]
    OC -. optional .-> EGPU[External GPU dock + desktop GPU]
```

## Physical design philosophy

The donor board does **not** need to line up with original X220 ports. The board is positioned for:

1. cooler and fan clearance;
2. keyboard underside clearance;
3. hinge clearance;
4. display-cable routing;
5. SSD/RAM serviceability.

External ports are then exposed through one of three methods:

- direct cutout when a donor port naturally reaches the side wall;
- short high-quality panel-mount extension;
- future side daughterboard/carrier arrangement.

## Version boundaries

### V0 — bench / ugly-but-working
- Stock donor adapter.
- Donor cooler untouched.
- HDMI-to-eDP display board.
- USB keyboard controller.
- No battery.
- Cables can be externally visible.

### V1 — integrated laptop
- Custom PETG/PA chassis.
- Internal display controller.
- Proper fan duct.
- Clean port cutouts/extensions.
- Internal speakers.
- Serviceable RAM/SSD access.

### V2 — electrical refinement
- Custom carrier/controller PCB.
- Better status LEDs / power button handling.
- Possible battery power after dedicated review.
- Optional OCuLink docking workflow.
