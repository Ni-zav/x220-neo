# CAD

Use this directory for editable CAD, measured reference geometry, and explicitly licensed third-party reference assets.

```text
cad/
  source/                 # project-owned editable CAD / Blender source
  reference-meshes/       # third-party/open reference geometry and generators
  exports/                # generated STL/STEP/OBJ; ignored where appropriate
  drawings/               # dimensioned drawings / sketches
```

## Reference assets

See [`reference-meshes/README.md`](reference-meshes/README.md) for the curated X220 geometry registry. It currently includes an MIT-licensed parametric X220 USB-C/DC-jack adapter generator, a verified-public-domain X220 HDD-cover reference link, and license-unverified models kept link-only.

Third-party licensing and attribution is tracked centrally in [`reference/ATTRIBUTIONS.md`](../reference/ATTRIBUTIONS.md).

## CAD rule

Do not begin detailed manufacturing CAD until the K8 PCB/cooler measurements in `reference/Measurement-Sheet.md` are populated. Third-party STL/CAD files are **reference geometry**, not measurement truth, unless independently checked against the physical X220.
