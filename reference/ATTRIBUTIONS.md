# Third-party asset attributions

Last reviewed: **2026-09-13**.

This file records third-party images, CAD/reference models, and other assets used or linked by X220 Neo. Asset-specific licenses apply to those assets only; they do **not** automatically relicense the rest of this repository.

## Wikimedia Commons — X220 disassembly reference set

The following photographs are embedded remotely from Wikimedia Commons in `media/reference/README.md`. They are not copied into this repository. Each source page identifies the work as the uploader's own work and licenses it under **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

License: https://creativecommons.org/licenses/by-sa/4.0/

| Reference | Author / uploader | Original source | Repository use | Changes |
|---|---|---|---|---|
| Fully disassembled X220, components laid out | Siarhei V | https://commons.wikimedia.org/wiki/File:Disassembled_Lenovo_ThinkPad_X220_with_components_laid_out.jpg | Remote thumbnail/reference | None |
| Inside of X220 magnesium-alloy bottom case | Siarhei V / Siarhei Besarab | https://commons.wikimedia.org/wiki/File:Inside_of_a_Lenovo_ThinkPad_X220_magnesium_alloy_bottom_case.jpg | Remote thumbnail/reference | None |
| Bottom of X220 keyboard support bezel, AP0S1000300 | Siarhei V / Siarhei Besarab | https://commons.wikimedia.org/wiki/File:Bottom_view_of_Lenovo_ThinkPad_X220_keyboard_bezel_PN_AP0S1000300.jpg | Remote thumbnail/reference | None |
| X220 motherboard with keyboard bezel removed | Siarhei V / Siarhei Besarab | https://commons.wikimedia.org/wiki/File:Disassembled_Lenovo_ThinkPad_X220_motherboard_without_keyboard_bezel.jpg | Remote thumbnail/reference | None |
| X220 CPU cooling system / fan + heatsink | Siarhei V / Siarhei Besarab | https://commons.wikimedia.org/wiki/File:ThinkPad_X220_CPU_cooling_system_(fan_and_heatsink_assembly).jpg | Remote thumbnail/reference | None |
| X220 LCD hinges, Kashui 04W2185 vs Foxconn 04W1406 | Siarhei V | https://commons.wikimedia.org/wiki/File:Lenovo_ThinkPad_X220_LCD_hinges_Kashui_FRU_04W2185_vs_Foxconn_FRU_04W1406.jpg | Remote thumbnail/reference | None |

The broader source category contains additional useful X220 teardown photographs:
https://commons.wikimedia.org/wiki/Category:Disassembled_ThinkPad_X220

If any of these images are later cropped, annotated, or otherwise modified and committed locally, record that modification here and preserve the applicable CC BY-SA terms for the derivative image.

## ThinkPad X220 USB-C adapter — vendored parametric source

- Upstream project: https://github.com/dayanegosha/thinkpad-x220-usb-c-adapter
- Upstream author: **dayanegosha**
- Upstream-derived files here:
  - `cad/reference-meshes/x220-usb-c-adapter/upstream/adapter.py`
  - `cad/reference-meshes/x220-usb-c-adapter/upstream/requirements.txt`
  - `cad/reference-meshes/x220-usb-c-adapter/LICENSE-MIT.txt`
- Upstream generated STL: https://github.com/dayanegosha/thinkpad-x220-usb-c-adapter/blob/main/stl/X220_USB_C_adapter.stl
- License: **MIT License**
- Copyright: `Copyright (c) 2026 dayanegosha (https://github.com/dayanegosha)`
- Local changes: `requirements.txt` and the MIT license text are preserved; `adapter.py` retains the upstream geometry, parameters and generation logic, with some explanatory comments shortened during import. No intentional geometry/parameter changes were made.

The original MIT notice is retained verbatim in `LICENSE-MIT.txt`. The parametric Python source can regenerate the STL using its documented dependencies. For byte-for-byte upstream comparison, use the canonical upstream repository above.

## ThinkPad X220 Hard Drive Cover — verified open, link-only

- Author: **jws / @jws_1754474**
- Source: https://www.printables.com/model/747619-thinkpad-x220-hard-drive-cover
- Source status: the model page states it is the author's original creation.
- License stated by source: **Creative Commons — Public Domain**
- Source explicitly permits sharing without attribution, remixing, and commercial use.
- Repository status: **link-only**; no binary has been mirrored here.

Attribution is retained voluntarily even though the source states attribution is not required.

## Link-only models — redistribution license not verified

These may be useful dimensional/printing references, but the model pages available during this review did not expose a sufficiently clear redistribution license. Do **not** mirror their files into this repository without re-checking the original license.

| Model | Author | Source | Status |
|---|---|---|---|
| Holder of HDD/SSD for Lenovo ThinkPad X220/X230 (`.STL` + `.SLDPRT`) | iasonov | https://cults3d.com/en/3d-model/home/holder-of-hdd-ssd-for-lenovo-thinkpad-x220-and-x230 | Link only; redistribution unverified |
| ThinkPad X220/X230 HDD cover (`.STL`) | Nevyl | https://cults3d.com/en/3d-model/various/capot-hdd-thinkpad-x220-x230 | Link only; redistribution unverified |

## Rules for future additions

Before adding a third-party binary or image to the repository:

1. Record the original author and canonical source URL.
2. Verify an explicit license that allows redistribution.
3. Preserve required copyright/license notices beside the asset.
4. Record whether the local file is unchanged, resized, cropped, annotated, converted, or otherwise modified.
5. If the license is unclear, keep it **link-only** until permission is verified.
