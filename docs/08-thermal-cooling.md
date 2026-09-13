---
title: Thermal and Cooling
updated: 2026-09-12
---

# Thermal / Cooling

## V1 rule: preserve the donor cooler

The K8 Plus cooler is already engineered for the 8845HS. Do not replace it merely to make the mechanical design prettier.

Manufacturer and teardown information shows:

- 8845HS configurable TDP: 35–54 W;
- manufacturer peak figure: up to 70 W;
- blower/turbine cooling;
- VC heat-pipe/copper assembly;
- third-party measured heatsink section: roughly 90 × 37 × 13.5 mm;
- roughly 60 mm blower reported in teardown.

## Airflow target

```mermaid
flowchart LR
    IN[Bottom/side intake] --> FAN[Stock blower]
    FAN --> HS[Stock heatsink]
    HS --> DUCT[Foam-gasketed duct]
    DUCT --> OUT[Dedicated side/rear exhaust]
```

Avoid a cavity where the exhaust recirculates into the intake.

## Mechanical design priorities

1. Keep fan inlet unobstructed.
2. Provide a dedicated exhaust opening.
3. Prevent soft cables from entering the fan.
4. Keep keyboard foil/plastic away from hot areas.
5. Preserve service access to cooler screws.
6. Use foam gasketing/ducting only after temperature testing confirms it is safe.

## Validation

Test at multiple firmware power modes if available. Log:

- CPU package temperature;
- sustained package power;
- fan RPM if exposed;
- clock stability;
- SSD temperature;
- chassis contact temperature at palmrest/bottom;
- ambient temperature.

Run tests first with the shell open, then closed.

## Liquid cooling

Not planned. For a 35–54 W-class APU, liquid adds pump/radiator/leak complexity without solving the primary packaging problem better than the donor vapor-chamber/blower assembly.
