# Ohm's Law

One equation runs all of basic electronics:

```text
V = I × R
```

Voltage = Current × Resistance. Know any two, get the third. That's
it — everything else in this chapter is that sentence wearing
different clothes.

## The three arrangements

| You know | You want | Formula |
|----------|----------|---------|
| V and R | Current | I = V / R |
| I and R | Voltage | V = I × R |
| V and I | Resistance | R = V / I |

**Worked example:** 5V across a 220Ω resistor. Current?

```text
I = V / R = 5 / 220 = 0.0227 A = 22.7 mA
```

**Check (verified):** 22.7 mA. (Milliamps — a thousandth of an amp.
Electronics lives in mA the way cooking lives in teaspoons.)

## Power: the heat equation

Current through resistance makes **heat**. How much:

```text
P = V × I
```

Power in watts. This tells you whether a component survives:

**Worked example:** that 220Ω resistor with 22.7 mA through it:

```text
P = 5 V × 0.0227 A = 0.114 W
```

**Check (verified):** 0.114 W — well under a standard ¼ W (0.25 W)
resistor's rating. If the math said 0.5 W, you'd need a bigger
resistor — undersized resistors overheat, discolor, and fail.

## Series and parallel

**Series** (one path, components in a line):

```text
R_total = R1 + R2          →  220Ω + 220Ω = 440Ω
```

Same current everywhere; voltage divides across components.

**Parallel** (multiple paths):

```text
1/R_total = 1/R1 + 1/R2    →  1/220 + 1/220 → R_total = 110Ω
```

Same voltage everywhere; current divides across paths. Two equal
resistors in parallel halve the resistance — more paths, easier
flow, like adding lanes to a highway.

## The voltage divider

Two resistors in series split the voltage proportionally — the
cheapest "make a smaller voltage" trick there is:

```text
Vout = Vin × R2 / (R1 + R2)
```

**Worked example:** 5V in, two 10kΩ resistors:

```text
Vout = 5 × 10000 / (10000 + 10000) = 2.5 V
```

**Check (verified):** 2.5 V. (Caveat: dividers are for *signals*,
not power — anything you connect draws current and shifts the
ratio. For powering things, use a regulator — see [Power
Supplies](power-supplies.md).)

## Battery life estimation

```text
hours = battery_mAh / draw_mA
```

**Worked example:** 2000 mAh battery, circuit draws 20 mA:

```text
2000 / 20 = 100 hours
```

**Check (verified):** ~100 hours, in ideal conditions. Real life is
less (batteries fade, draw varies) — treat it as an upper bound,
not a promise.

**Next:** [Components](components.md)
