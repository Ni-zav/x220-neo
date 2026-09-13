# Port Map

## K8 Plus verified ports

- 2× USB4 40 Gbps / DP capability.
- 2× USB 3.2 Gen2 front.
- 2× USB 2.0 rear.
- HDMI 2.1.
- DisplayPort 2.1.
- 2× RJ45 2.5GbE.
- OCuLink PCIe 4.0 ×4.
- 3.5 mm audio.
- 19 V DC input.

## X220 Neo desired exposure

| Priority | Port | Strategy |
|---:|---|---|
| 1 | USB4 Type-C | direct opening if mechanically possible; avoid long passive extension |
| 1 | 2× USB-A | direct/short extension |
| 1 | DC input | mechanically supported panel access |
| 1 | OCuLink | direct opening strongly preferred |
| 1 | 3.5 mm audio | direct/short extension |
| 2 | HDMI/DP diagnostic | one exposed is enough |
| 3 | 2.5GbE | one exposed optional |
| 4 | second Ethernet / extra display | can remain inaccessible in first build |
