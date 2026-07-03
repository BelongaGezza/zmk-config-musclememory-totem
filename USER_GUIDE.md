# User Guide — Muscle Memory Home Row Mods (TOTEM)

## Notation

```
KEY          plain key
KEY ▾MOD     hold-tap: tap = KEY, hold = MOD
▽            transparent — passes through to the layer below
·            no action
```

Hold-tap keys activate their modifier (MOD) when held while pressing a key
on the **opposite hand**. Tapping them quickly produces the primary character (KEY).

---

## Keyboard layout reference

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  0  │  1  │  2  │  3  │  4  │   │  5  │  6  │  7  │  8  │  9  │  ← position index
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │ 20 │ 21  │ 22  │ 23  │ 24  │ 25  │   │ 26  │ 27  │ 28  │ 29  │ 30  │ 31 │
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │ 32  │ 33  │ 34  │   │ 35  │ 36  │ 37  │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

Row 10–19 is the home row. The outer pinky keys on row 2 are positions 20 (left) and 31 (right).

---

## Layer 0 — BASE

**Active by default.**

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  Q  │  W  │  E  │  R  │  T  │   │  Y  │  U  │  I  │  O  │  P  │
         ├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
         │  A  │  S  │  D  │  F  │  G  │   │  H  │  J  │  K  │  L  │  ;  │
         │▾SFT │▾RALT│▾SYMB│▾CTL │▾ALT │   │▾ALT │▾CTL │▾SYMB│▾RALT│▾SFT │
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │TAB │  Z  │  X  │  C  │  V  │  B  │   │  N  │  M  │  ,  │  .  │  /  │ENT │
    │▾SFT│     │     │     │▾GUI │     │   │     │▾GUI │     │     │     │▾SFT│
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │  FN │ ESC │ SPC │   │ SPC │ BSP │ CMP │
                        │ sl  │▾MOU │▾GUI │   │▾GUI │     │▾NPD │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

**Thumb keys:**

| Key | Tap | Hold |
|-----|-----|------|
| FN | enter FUNC layer (sticky) | — |
| ESC | Escape | enter MOUSE layer |
| SPC (left) | Space | GUI (⌘/⊞) |
| SPC (right) | Space | GUI (⌘/⊞) |
| BSP | Backspace | — |
| CMP | Compose / App key | double-tap: lock NUMPAD |

**Home row modifiers** fire when you hold a key and press a key on the opposite hand:

| Left key | Hold = | | Right key | Hold = |
|----------|--------|-|-----------|--------|
| A | Shift | | ; | Shift |
| S | AltGr | | L | AltGr |
| D | SYMB layer | | K | SYMB layer |
| F | Ctrl | | J | Ctrl |
| G | Alt | | H | Alt |
| V | GUI | | M | GUI |
| outer TAB | Shift | | outer ENT | Shift |
| SPC | GUI | | SPC | GUI |

---

## Layer 1 — SYMB (symbols, numbers, arrows)

**Access:**
- Hold `D` or `K` (momentary, cross-hand)
- Pinch `ESC` + `BSP` to toggle on/off

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  1  │  2  │  3  │  4  │  5  │   │  6  │  7  │  8  │  9  │  0  │
         ├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
         │ ESC │ INS │ DEL │ TAB │ BSP │   │  ←  │  ↓  │  ↑  │  →  │ ENT │
         │▾SFT │▾RALT│▾NPD │▾CTL │▾ALT │   │▾ALT │▾CTL │▾NPD │▾RALT│▾SFT │
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │ ▽  │  `  │  -  │  =  │  [  │  ]  │   │  \  │  '  │  ,  │  .  │  /  │ ▽  │
    │    │     │     │     │▾GUI │     │   │     │▾GUI │     │     │     │    │
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │  ▽  │BASE │  ▽  │   │  ▽  │  ▽  │BASE │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

**Notes:**
- Shifted symbols (`!`, `@`, `#` … `+`, `_`, `{`, `}` etc.) are reached by holding `A` (Shift) while tapping the number or bracket key on this layer.
- Arrow keys `←↓↑→` are on `H J K L` (Vim-style). They carry the same modifiers as in BASE, so you can hold `H` for Alt+Arrow, `J` for Ctrl+Arrow, etc.
- `ESC` thumb tap or `CMP` thumb tap both return to BASE when used in toggle mode.

---

## Layer 2 — NPAD (numpad)

**Access:**
- Double-tap `CMP` (Compose key) to lock on
- Tap `CMP` again (or `ESC` thumb) to exit (`to BASE`)

The left half is fully transparent — all home row modifiers remain accessible from BASE while entering numbers.

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  ▽  │  ▽  │  ▽  │  ▽  │  ▽  │   │  -  │  7  │  8  │  9  │  0  │
         │     │     │     │     │     │   │ (÷) │     │     │     │ (=) │
         ├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
         │  ▽  │  ▽  │  ▽  │  ▽  │  ▽  │   │NLCK │  4  │  5  │  6  │KPENT│
         │     │     │     │     │     │   │     │     │▾SYMB│     │     │
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │ ▽  │  ▽  │  ▽  │  ▽  │  ▽  │  ▽  │   │  +  │  1  │  2  │  3  │  .  │ ▽  │
    │    │     │     │     │     │     │   │ (×) │     │     │     │ (,) │    │
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │  ▽  │  ▽  │  ▽  │   │  ▽  │  ▽  │BASE │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

**Tap-dance operators** — tap once for primary, tap twice for secondary:

| Key | Single tap | Double tap |
|-----|-----------|-----------|
| `-` | − (minus) | ÷ (divide) |
| `+` | + (plus) | × (multiply) |
| `.` | . (decimal) | , (comma) |
| `0` | 0 | = (equals) |

Because the left side is transparent, you can type e.g. Ctrl+numpad-5 by holding `F` (Ctrl) and tapping `5` on the right.

---

## Layer 3 — FUNC (function keys)

**Access:** tap `FN` thumb key (sticky — tap once, then press an F-key, returns to BASE automatically).

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  F1 │  F2 │  F3 │  F4 │  F5 │   │  F6 │  F7 │  F8 │  F9 │ F10 │
         ├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
         │ F11 │ F12 │ F13 │ F14 │ F15 │   │ F16 │ F17 │ F18 │ F19 │ F20 │
         │▾SFT │▾RALT│     │▾CTL │▾ALT │   │▾ALT │▾CTL │     │▾RALT│▾SFT │
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │ ▽  │ F21 │ F22 │ F23 │ F24 │  ·  │   │  ·  │RGUI │  ·  │  ·  │  ·  │ ▽  │
    │    │     │     │     │▾GUI │     │   │     │     │     │     │     │    │
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │  ▽  │  ▽  │  ▽  │   │  ▽  │  ▽  │  ▽  │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

F11/F12 carry Shift and AltGr holds, allowing modified F-key combos (e.g. Shift+F11 via `FN` then hold `A` + tap `F11`-position).

---

## Layer 4 — NAVI (navigation)

**Access:** pinch right-thumb `SPC` + `BSP` simultaneously (sticky — stays active for one keypress).

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  ·  │  ·  │  ·  │  ·  │  ·  │   │HOME │ DEL │ INS │ END │ BSP │
         ├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
         │ ESC │ INS │ DEL │ TAB │ BSP │   │  ←  │  ↓  │  ↑  │  →  │ ENT │
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │ ▽  │  ·  │  ·  │  ·  │  ·  │  ·  │   │  ·  │PGDN │PGUP │  ·  │  ·  │ ▽  │
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │  ▽  │  ▽  │  ▽  │   │  ▽  │  ▽  │  ▽  │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

Thumb keys are transparent in this layer, so you can still hold `SPC` for GUI while a navigation key is active (see workflows below).

---

## Layer 5 — MOUS (mouse)

**Access:** hold `ESC` thumb key.

```
         ┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
         │  ·  │  ·  │  ·  │  ·  │  ·  │   │  ·  │  ·  │  ·  │  ·  │  ·  │
         ├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
         │ MB4 │LCLK │MCLK │RCLK │ MB5 │   │ ◄   │ ▼   │ ▲   │ ►   │LCLK │
         │(bck)│     │     │     │(fwd)│   │move │move │move │move │     │
    ┌────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼────┐
    │ ▽  │  ·  │  ·  │  ·  │  ·  │  ·  │   │ ◄   │ ▼   │ ▲   │ ►   │  ·  │ ▽  │
    │    │     │     │     │     │     │   │scrl │scrl │scrl │scrl │     │    │
    └────┴─────┴─────┴──┬──┴─────┴─────┘   └─────┴─────┴──┬──┴─────┴─────┴────┘
                        │  ▽  │  ▽  │  ▽  │   │  ▽  │  ▽  │  ▽  │
                        └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

Mouse movement is on the right-hand home row; scroll wheel is on the right-hand bottom row. Left-hand home row holds mouse buttons.

---

## Layer 6 — SYST (system / Bluetooth)

**Access:** simultaneously hold `V` + left `SPC`  **or**  `M` + right `SPC` (momentary, both hands).

```
         ┌──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┐
         │BT_CLR│  ·   │  ·   │  ·   │RESET │   │RESET │BRI ↓ │BRI ↑ │  ·   │  ·   │
         ├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
         │  ·   │  ·   │ USB  │ BLE  │  ·   │   │MUTE  │VOL ↓ │VOL ↑ │  ·   │  ·   │
    ┌────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼────┐
    │CLR │ SEL0 │ SEL1 │ SEL2 │ SEL3 │ SEL4 │   │ PLAY │ PREV │ NEXT │  ·   │  ·   │ ·  │
    │ALL │      │      │      │      │      │   │      │      │      │      │      │    │
    └────┴──────┴──────┴──┬───┴──────┴──────┘   └──────┴──────┴──┬───┴──────┴──────┴────┘
                          │  ▽  │  ▽  │  ▽  │   │  ▽  │  ▽  │  ▽  │
                          └─────┴─────┴─────┘   └─────┴─────┴─────┘
```

| Key | Action |
|-----|--------|
| BT_CLR | Clear current BLE pairing |
| BT_CLR_ALL | Clear all BLE pairings |
| SEL 0–4 | Switch to Bluetooth profile 0–4 |
| USB / BLE | Force USB or BLE output |
| RESET | Soft reset (stays in firmware) |

---

## Combos

Combos fire when all listed keys are pressed within the timeout window.

| Keys | Timeout | Result |
|------|---------|--------|
| `Q` + `W` + `E` + `T` | 100 ms | Bootloader mode (left half) |
| `Y` + `I` + `O` + `P` | 100 ms | Bootloader mode (right half) |
| outer `TAB` + outer `ENT` | 100 ms | Caps Lock |
| `FN` + `CMP` | 100 ms | Caps Lock |
| `ESC` + `BSP` | 100 ms | Toggle SYMB layer |
| right `SPC` + `BSP` | 50 ms | Sticky NAVI layer |
| `V` + left `SPC` | 100 ms | Momentary SYST layer |
| `M` + right `SPC` | 100 ms | Momentary SYST layer |

---

## Common workflows

### Typing numbers and symbols

Enter SYMB by holding `D` (left hand) while typing numbers with the right hand, or toggle SYMB with `ESC`+`BSP` for extended sessions.

```
Type "hello, world!" on SYMB toggle:
  ESC+BSP      → toggle SYMB on
  H E L L O   → letters (same as BASE)
  ,            → comma (same position)
  [space]      → SPC thumb
  W O R L D
  A + 1        → hold A (Shift) + tap 1 = !
  ESC          → exit SYMB (returns to BASE)
```

### Cut, copy, paste (Ctrl+X/C/V)

`F` holds Ctrl. These letters are on the left hand, so the hold fires via tapping-term (hold `F` for ~280 ms then tap the letter):

```
Ctrl+Z   hold F, tap Z
Ctrl+X   hold F, tap X
Ctrl+C   hold F, tap C
Ctrl+V   hold F, tap V
```

Alternatively, use right-hand Ctrl (`J`) with the left hand for the letter — this is cross-hand and fires immediately on release:

```
Ctrl+Z   hold J, tap Z    ← cross-hand, most reliable
```

### Arrow keys

**Single presses** — use sticky NAVI (right-thumb `SPC`+`BSP` pinch):
```
SPC+BSP pinch → NAVI active for one key
← ↓ ↑ →       → H J K L on right hand
```

**Extended navigation** — toggle SYMB (`ESC`+`BSP`), then use `H J K L` for arrows continuously.

**Word-by-word** (Ctrl+Arrow) in SYMB:
```
Toggle SYMB, then hold J (Ctrl) + tap H or L (← →)
```

### Home, End, Page Up, Page Down

Use sticky NAVI (`SPC`+`BSP`), then:
- `Y` → Home
- `P` → Backspace
- `U` → Delete
- `I` → Insert
- `O` → End
- `;` position (row 1) → Enter
- `M` position → Page Down
- `,` position → Page Up

### GUI shortcuts (window management)

Hold either `SPC` thumb for GUI, then tap a key. For arrow-based window management (e.g. tiling WMs), toggle SYMB first so arrow keys are available:

```
Toggle SYMB (ESC+BSP)
Hold left SPC (GUI)
Tap H / J / K / L   → GUI+← / GUI+↓ / GUI+↑ / GUI+→
```

For `GUI+Tab` (application switcher):
```
Hold right SPC (GUI), tap left SPC (Space acts as plain Space here via cross-hand tap)
```
Or use the OS App Switcher via the `CMP` key (App/Compose key) if configured.

### Alt+Tab

`G` holds left Alt, and outer `TAB` (left pinky) taps Tab. Both are left-hand, so use tapping-term: hold `G` for ~280 ms then tap outer `TAB`. Alternatively, in SYMB, `G`-position gives `BSP`▾`ALT` and `F`-position gives `TAB`▾`CTL` — hold `G`-pos for Alt, tap `F`-pos for Tab (same-hand, tapping-term applies).

### Function keys

Tap `FN` (sticky), then tap the F-key. The layer auto-exits after one press.

```
FN tap, then F5        → F5
FN tap, then A+F1      → hold A (Shift) + tap F1 = Shift+F1
FN tap, then F+F5      → hold F (Ctrl) + tap F5 = Ctrl+F5
```

### Numpad entry

Double-tap `CMP` to lock NUMPAD. Left hand falls through to BASE, giving full access to home row modifiers alongside the right-hand numpad:

```
CMP CMP      → lock NUMPAD
3 . 1 4      → right hand: 3 . 1 4
F + 5        → hold F (Ctrl) + 5 = Ctrl+KP5
CMP          → exit back to BASE
```

Arithmetic tap-dance: pause briefly between two taps to avoid triggering the secondary operator.

### Bluetooth profile switching

Hold `V` + left `SPC` simultaneously to enter SYST (momentary):
```
V + SPC (hold both)
  SEL0 / SEL1 / SEL2  → switch profile
Release V + SPC        → exit SYST
```

To pair a new device, switch to an unused profile (e.g. SEL4) and then tap `BT_CLR` to clear any existing pairing on that slot before connecting.

---

## Layer access summary

| Layer | Method | Stays active |
|-------|--------|-------------|
| SYMB | Hold `D` or `K` | While held |
| SYMB | Pinch `ESC`+`BSP` | Until toggled off |
| NPAD | Double-tap `CMP` | Until `CMP` or `ESC` exits |
| FUNC | Tap `FN` (sticky) | One keypress |
| NAVI | Pinch `SPC`+`BSP` (sticky) | One keypress |
| MOUS | Hold `ESC` thumb | While held |
| SYST | Hold `V`+`SPC` or `M`+`SPC` | While both held |
