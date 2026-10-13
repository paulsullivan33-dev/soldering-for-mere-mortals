# The LED Circuit

Your first real electronics calculation, end to end. One LED, one
resistor, one battery — and every number justified.

## The circuit

```text
5V (+) ---[ 220Ω ]---+---[ LED >| ]--- GND (-)
                      (long leg)  (short leg)
```

Current flows: 5V → resistor → LED's long leg → LED → short leg →
GND. One loop, as promised in chapter 1.

## The calculation

The LED drops ~2V (its forward voltage — red LEDs ~2V, blue/white
~3V; the datasheet says exactly). The resistor must drop the rest:

```text
V_resistor = 5V - 2V = 3V
```

Pick a safe current — 15 mA is bright and comfortable:

```text
R = V / I = 3V / 0.015A = 200Ω
```

**Check (verified):** 200Ω. Nearest standard value: **220Ω**
(see [Reading Resistors](reading-resistors.md)).

Now verify with the actual 220Ω — what current really flows?

```text
I = 3V / 220Ω = 0.0136A = 13.6 mA
```

**Check (verified):** 13.6 mA — safely under the LED's typical
20 mA max and the Arduino pin's ~20 mA limit.

And the resistor's power:

```text
P = V × I = 3V × 0.0136A = 0.041 W
```

**Check (verified):** 0.041 W — a standard ¼ W resistor loafs along
at a sixth of its rating.

## What if there's no resistor?

The LED tries to drop its 2V across ~zero resistance:

```text
I = 3V / ~0Ω → enormous
```

In practice: very bright for a second, then the LED dies —
sometimes taking the Arduino pin with it. This is the single most
common beginner hardware death, and it's a 5-cent part away from
never happening.

## Varying the design

| Supply | LED drop | Target current | R = (Vs−Vf)/I | Use |
|--------|----------|----------------|---------------|-----|
| 5V | 2V | 15 mA | 200Ω | 220Ω |
| 3.3V | 2V | 10 mA | 130Ω | 150Ω |
| 9V | 2V | 15 mA | 467Ω | 470Ω |
| 5V | 3V (blue) | 15 mA | 133Ω | 150Ω |

**Check (verified):** (5−2)/0.015 = 200; (3.3−2)/0.01 = 130;
(9−2)/0.015 = 466.7; (5−3)/0.015 = 133.3. Same formula every time —
**R = (supply − LED drop) / current**. Memorize that line; it's the
most-used equation in hobby electronics.

**Next:** [Soldering](soldering.md)
