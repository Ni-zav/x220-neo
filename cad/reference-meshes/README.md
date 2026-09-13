# CAD reference meshes and generators

This folder is for third-party geometry or geometry generators that are useful while building the X220 Neo digital mock-up.

**Nothing here is automatically authoritative dimensional truth.** Treat imported meshes as reference/block-out geometry until checked against physical measurements in `reference/Measurement-Sheet.md`.

See [`reference/ATTRIBUTIONS.md`](../../reference/ATTRIBUTIONS.md) for complete license/source records.

## Vendored: X220 DC-jack → USB-C adapter

Upstream: https://github.com/dayanegosha/thinkpad-x220-usb-c-adapter

License: **MIT**.

Local files:

```text
x220-usb-c-adapter/
├── LICENSE-MIT.txt
└── upstream/
    ├── adapter.py
    └── requirements.txt
```

The upstream project also publishes the generated binary STL:

https://github.com/dayanegosha/thinkpad-x220-usb-c-adapter/blob/main/stl/X220_USB_C_adapter.stl

The binary STL is intentionally not duplicated here at this stage. We vendor the inspectable parametric generator and dependency list instead. The local `adapter.py` keeps the upstream geometry, numeric parameters and generation logic; some explanatory comments were shortened during import. Use the canonical upstream repository for byte-for-byte comparison.

This model is especially useful because its source documents several X220 DC-jack pocket dimensions and expresses the housing parametrically. **Re-measure your own chassis before treating those values as manufacturing dimensions.**

### Regenerating the STL

From the vendored upstream directory, create a Python environment and install the requirements, then run:

```bash
python adapter.py
```

The generator expects an `stl/` output location relative to its project layout. If you alter the local output path or geometry, treat that as a project-owned derivative and record the change in `reference/ATTRIBUTIONS.md`.

## Verified-open external model: X220 hard-drive cover

**Thinkpad X220 Hard Drive Cover** by jws / `@jws_1754474`

https://www.printables.com/model/747619-thinkpad-x220-hard-drive-cover

The source page identifies it as the author's original creation and marks it **Creative Commons — Public Domain**, permitting sharing, remixing and commercial use. It is currently link-only here because the repository import should preserve a traceable original binary rather than scrape an unstable download endpoint.

This is potentially useful as a calibration/reference part around the X220 2.5-inch bay opening.

## Link-only references: license not verified for redistribution

Do not vendor these files until their explicit redistribution licenses are confirmed from the original author/source.

- Holder of HDD/SSD for X220/X230 (`.SLDPRT` + `.STL`), iasonov: https://cults3d.com/en/3d-model/home/holder-of-hdd-ssd-for-lenovo-thinkpad-x220-and-x230
- X220/X230 HDD cover (`.STL`), Nevyl: https://cults3d.com/en/3d-model/various/capot-hdd-thinkpad-x220-x230

## Blender use

For the first assembly mock-up, import/reference these only alongside simple measured envelopes for:

- X220 bottom case;
- keyboard + keyboard-bezel keep-out;
- left/right hinges and swept volumes;
- K8 Plus PCB and cooler;
- SO-DIMM service volumes;
- M.2 service volumes;
- display/controller board;
- exhaust and intake volumes.

The aim of the first Blender scene is **interference checking**, not photorealism.
