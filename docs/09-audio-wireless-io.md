---
title: Audio Wireless and IO
updated: 2026-09-12
---

# Audio, wireless and external I/O

## Audio

Fastest V0 path:

```mermaid
flowchart LR
    JACK[K8 3.5 mm audio out] --> AMP[Small stereo amplifier]
    AMP --> SPK[X220 or replacement speakers]
```

A PAM8403-class module is fine for bench prototyping **only after speaker impedance and supply voltage are verified**. Final audio may use a cleaner USB audio / amplifier board if noise becomes a problem.

## Wi-Fi

The K8 Plus includes an Intel AX200 Wi-Fi 6 module. Do not buy an AX210 immediately.

Tasks:
- reuse or replace antenna pigtails as needed;
- place antennas in the display lid where practical;
- keep antennas away from large grounded metal reinforcement;
- only upgrade to AX210/Wi-Fi 6E if there is a real requirement.

## Webcam / microphone

V1 options:

1. keep K8 onboard mic only for bench use;
2. install a thin USB webcam module in the X220 lid;
3. reverse-engineer/reuse original camera only if it saves space.

The webcam is not a V0 blocker.

## Port exposure strategy

### Priority external ports
- one USB4 Type-C;
- two USB-A;
- 3.5 mm audio;
- OCuLink;
- DC input;
- one diagnostic display output if space allows.

### Low priority
- both 2.5GbE ports;
- every original X220 port opening.

Trying to preserve the exact 2011 port map creates unnecessary mechanical constraints.
