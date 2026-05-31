# ZMK Config — Eyelash Sofle

ZMK firmware configuration for the [Eyelash Sofle](https://github.com/EyelashPeripherals/eyelash_sofle) split keyboard, built on the nice!nano v2 controller with nice!view displays.

## Features

- **5 layers** — default, function/mouse, Bluetooth/settings, and two spare layers
- **Encoders** — left encoder scrolls by default
- **Mouse keys** — via pointer/movement behaviors on layers 1 and 2
- **RGB underglow** — WS2812 strip, off by default, auto-off on idle/USB disconnect
- **Per-key backlight** — enabled on start
- **ZMK Studio** — live keymap editing via USB
- **Soft off** — hold three thumb keys to power down

## Display

Uses the [nice-view-gem](https://github.com/M165437/nice-view-gem) shield for custom display widgets:

- **Left half (central)** — connection type (BLE/USB), battery gauge, WPM line graph, active layer name
- **Right half (peripheral)** — spinning crystal animation

Animation is set to 30 fps (`1920` ms across 16 frames) to save battery.

## Building

This repo uses [GitHub Actions](https://github.com/zmkfirmware) to build the firmware. Push to `main` and download the UF2 artifacts from the Actions tab.

Flash each half by double-tapping reset and dragging the UF2 file onto the USB mass storage device.

## Layout

```
Layer 0 — Default
┌──────┬──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┬──────┬──────┐
│ ESC  │  1   │  2   │  3   │  4   │  5   │   │  ↑   │  6   │  7   │  8   │  9   │  0   │ BKSP │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┼──────┤
│ TAB  │  Q   │  W   │  E   │  R   │  T   │   │  ↓   │  Y   │  U   │  I   │  O   │  P   │  \   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┼──────┤
│ CAPS │  A   │  S   │  D   │  F   │  G   │   │  ←   │  H   │  J   │  K   │  L   │  ;   │  '   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┼──────┤
│ LSFT │  Z   │  X   │  C   │  V   │  B   │   │  →   │  N   │  M   │  ,   │  .   │  /   │ ENT  │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┼──────┤
│ MUTE │ LCTL │ LGUI │ LALT │  MO1 │ SPC  │   │ ENT  │ SPC  │ ENT  │ MO2  │ RSFT │ DEL  │      │
└──────┴──────┴──────┴──────┴──────┴──────┘   └──────┴──────┴──────┴──────┴──────┴──────┴──────┘
```
