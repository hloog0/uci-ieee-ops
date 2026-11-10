# Project 1: LED There Be Light

**Status:** Complete (Oct 2026)
**Spec:** [OPS Project 1](https://ieee.ics.uci.edu/ops-program/project_1.html)

A switched LED circuit powered by a 9V battery: prototyped on a breadboard, then soldered onto perfboard.

**Demo video:** [perfboard-led-demo.mp4](media/perfboard-led-demo.mp4) (the switch toggling the soldered LED)

## Circuit

9V battery → slide switch → current-limiting resistor → LED → back to the battery.

The 9V snap connector plugs into a soldered female 1x2 header instead of being soldered directly, so the battery can be swapped.

## Resistor sizing

The LED has a forward voltage of about 2V and is run at 20 mA. The resistor drops the remaining voltage:

```
V_R = V_batt − V_f = 9 V − 2 V = 7 V
R   = V_R / I     = 7 V / 0.020 A = 350 Ω
```

A larger resistor dims the LED. A much smaller one pushes too much current and can burn it out.

## Build

1. Calculated the resistor value (above).
2. Built and tested the circuit on a breadboard.
3. Soldered the LED, resistor, switch, header, and wires onto perfboard.

## Parts

| Part | Qty |
|------|-----|
| 9V battery + snap connector | 1 |
| Female header, 2.54 mm, 1x2 | 1 |
| LED, ~2V forward voltage | 1 |
| Slide switch | 1 |
| Resistor (sized above) | 1 |
| Perfboard | 1 |

## Takeaways

- Perfboard soldering is the hard part. There are no traces, so every connection is a hand-routed wire or solder bridge.
