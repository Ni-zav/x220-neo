# Connection Map

This file becomes the authoritative wiring table **after physical validation**.

| From | Signal / interface | To | Status | Notes |
|---|---|---|---|---|
| GMKtec PSU | 19 V DC | K8 DC input | VERIFIED SPEC | stock 6.32 A / 120 W adapter |
| K8 HDMI | HDMI | display controller | PLANNED | V0 path |
| display controller | 30-pin eDP | FHD panel | PLANNED | exact cable depends on controller/panel |
| K8 USB | USB | keyboard controller | PLANNED | direct or internal hub |
| keyboard controller | matrix lines | X220 keyboard | SOURCE-DOCUMENTED / VERIFY | exact connector orientation must be measured |
| keyboard controller | PS/2 CLK/DATA/RESET | TrackPoint | SOURCE-DOCUMENTED / VERIFY | verify voltage/pinout |
| K8 3.5 mm | analog audio | amplifier | PLANNED | optional V1 |
| amplifier | speaker out | X220 speakers | TBD-MEASURE | verify impedance |
| K8 OCuLink | PCIe 4.0 ×4 | eGPU dock | VERIFIED SPEC | NOT HOT-PLUGGABLE |
| K8 AX200 | RF | lid antennas | PLANNED | antenna routing TBD |
