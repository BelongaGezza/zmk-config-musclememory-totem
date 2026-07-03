# Muscle memory friendly Home Row Mods for the TOTEM keyboard

This repository contains the implementation of a keyboard layout suitable for
40% keyboards, based on "home row mods". The layout is designed for software
developers and authors of multilingual texts. Particular emphasis was placed on
ease of learning. The layout presented here is implemented both as a Kanata
driver for standard keyboards on Linux, Mac, and Windows computers,
and as ZMK Firmware for the small 38 key column-staggered split
[TOTEM keyboard]. This way you benefit from ergonomic home row mods on all
your input devices.

Read the accompanying blog post here:
[Jens Getreu's blog - Muscle memory friendly home row mods](https://blog.getreu.net/20250826-muscle-memory-friendly-home-row-mods/)

![Base layer](./docs/images/base.svg)

![Symbol layer](./docs/images/symbols.svg)


[ZMK Firmware]: https://zmk.dev/
[Kanata]: https://github.com/jtroo/kanata
[zmk-config-totem/kanata/qwerty-home-row-mods.kbd]: https://github.com/getreu/zmk-config-totem/blob/master/kanata/qwerty-home-row-mods.kbd
[getreu/zmk-config-totem]: https://github.com/getreu/zmk-config-totem
[TOTEM keyboard]: https://github.com/GEIGEIGEIST/TOTEM


## Layout overview

### Extended home row modifiers

Modifiers sit on the home row and the inner column, held while typing with the
opposite hand:

| Key | Modifier | Hand |
|-----|----------|------|
| `A` | Shift | Left |
| `S` | AltGr | Left |
| `D` | Symbol layer | Left |
| `F` | Ctrl | Left |
| `G` | Alt | Left |
| `V` | GUI | Left (extended) |
| `Space` | GUI | Left (extended) |
| `H` | Alt | Right |
| `J` | Ctrl | Right |
| `K` | Symbol layer | Right |
| `L` | AltGr | Right |
| `;` | Shift | Right |
| `M` | GUI | Right (extended) |
| `Enter` | GUI | Right (extended) |

### Thumb cluster

```
┌──────┬──────────┬───────┐   ┌────────┬──────────┬─────────┐
│ FUNC │ MOUSE/ESC│ Space │   │ Space  │Backspace │ Compose │
│ (sl) │  (hold)  │ (GUI) │   │  (GUI) │          │/Numpad  │
└──────┴──────────┴───────┘   └────────┴──────────┴─────────┘
```

- **FUNC** (`sl`): sticky — tap then press F1–F24
- **MOUSE/ESC** (`lt`): hold for mouse layer, tap for Escape
- **Space / Enter**: tap for character; hold for GUI modifier (cross-hand shortcuts)
- **Backspace**: tap to delete; pinch Space+Backspace (right thumb) for sticky Navigation layer
- **Compose/Numpad**: tap for Compose (application key); double-tap to lock Numpad layer

### Layers

| # | Name | Access |
|---|------|--------|
| 0 | BASE | default |
| 1 | SYMB | hold `D` or `K`; or pinch `ESC`+`Backspace` to toggle |
| 2 | NPAD | double-tap Compose to lock; `to 0` to exit |
| 3 | FUNC | tap Compose (sticky) |
| 4 | NAVI | pinch right-thumb `Space`+`Backspace` (sticky) |
| 5 | MOUS | hold `MOUSE/ESC` thumb key |
| 6 | SYST | pinch `V`+`Space` or `M`+`Space` (momentary) |

### Numpad layer

The left side passes through to the base layer so home row modifiers remain
active while entering numbers. Arithmetic operators use tap-dance:

| Key | Single tap | Double tap |
|-----|-----------|------------|
| `-` | − | ÷ |
| `+` | + | × |
| `.` | . | , |
| `0` | 0 | = |

### System layer

Reached by simultaneously holding `V`+`Space` (left hand) or `M`+`Space`
(right hand). Contains Bluetooth profile selection, output switching
(USB/BLE), and media/brightness controls.

### Combos

| Keys | Output |
|------|--------|
| `Q`+`W`+`E`+`T` | Bootloader (left half) |
| `Y`+`I`+`O`+`P` | Bootloader (right half) |
| `FUNC`+`Compose` | Caps Lock |
| outer `Shift`+`Shift` | Caps Lock |
| `ESC`+`Backspace` | Toggle Symbol layer |
| right-thumb `Space`+`Backspace` | Sticky Navigation layer |


## HOW TO USE

- fork this repo
- `git clone` your fork to create a local copy
- adjust `config/totem.keymap` (find all keycodes on [the ZMK docs pages](https://zmk.dev/docs/codes/))
- `git push` to your fork
- on the GitHub page of your fork navigate to **Actions**
- scroll down and unzip the `firmware.zip` archive from the latest run
- connect the left half of the TOTEM to your PC, press reset twice
- the keyboard should appear as a mass storage device
- drag and drop `totem_left-xiao_ble__zmk-zmk.uf2` onto the storage device
- repeat with the right half using `totem_right-xiao_ble__zmk-zmk.uf2`

## Local build

Requires [Nix](https://nixos.org/) with flakes enabled.

```sh
nix develop          # enter dev environment
just init            # initialise west workspace (once)
just build all       # build both halves
just draw            # regenerate SVG keymap diagrams
```

Firmware is written to `firmware/`. See `just --list` for all available
recipes.

## ZMK revision

`config/west.yml` is pinned to a specific ZMK commit for reproducible builds.
To upgrade:

```sh
just update                        # fetch latest ZMK
just build all                     # verify it compiles
# then update the revision hash in config/west.yml
```
