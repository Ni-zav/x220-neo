# Build 02 — Keyboard / TrackPoint prototype

## Option A — fastest

1. Connect X220 keyboard to TP Art controller.
2. Connect controller to another PC by USB.
3. Test every key.
4. Test TrackPoint and all buttons.
5. Test Fn/media combinations.

## Option B — DIY

1. Build/buy connector breakout.
2. Verify keyboard pinout against continuity measurements.
3. Bring up matrix scanning on RP2040/QMK.
4. Bring up TrackPoint CLK/DATA/RESET.
5. Add mouse buttons.
6. Expose USB HID.
7. Log pin assignments in `reference/Connection-Map.md`.

## Pass criteria

100% primary keys and TrackPoint functionality work outside the laptop before mechanical integration.
