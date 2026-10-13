# The Multimeter

A **multimeter** measures what your eyes can't: voltage, current,
resistance, and whether two points connect. A $20 one answers 95%
of beginner questions. Learn four modes and you're set.

## Voltage (V): "how hard is it pushing here?"

Probes across the two points (parallel — the meter sips almost no
current). Red to positive, black to ground.

```text
Meter across a AA battery → 1.5V (fresh) down to ~1.0V (dead)
Meter across your LED's resistor → ~3V (from the LED circuit math)
```

**Check:** your computed values from [The LED Circuit](led-circuit.md)
should roughly match the meter. "Roughly" — real components vary
±5–10%.

**Careful:** never measure voltage with the probes in the *current*
jacks (see below) — that's a short circuit across your probes.

## Resistance (Ω): "what is this thing?"

Power **off**, component **out of circuit** (or at least one leg
lifted — in-circuit resistors read low because of parallel paths).
Probes across the component.

```text
Red-red-brown resistor → ~220Ω on the meter
```

This is how you settle color-code arguments and identify mystery
parts. (From [Reading Resistors](reading-resistors.md): when bands
lie to your eyes, the meter tells the truth.)

## Continuity: "are these connected?"

The beep mode (diode symbol `•)))`). Probes on two points: beep =
connected, silence = not. Uses:

- Did my solder bridge those pins? (beep = yes, wick it)
- Is this trace actually cut? (silence = yes)
- Which wire in this bundle is which? (beep when you find it)

**The most-used mode in troubleshooting.** Before powering a new
board, continuity-check power rails for shorts (5V-to-GND beep =
don't plug it in).

## Current (A): "how much is flowing?"

The meter goes **in series** — it *becomes* part of the loop
(break the circuit, insert the meter). Start on the highest range
and work down.

**Careful — the blown-fuse classic:** measuring current means the
full circuit current flows *through the meter*. Exceed the jack's
rating (often 200mA on the small jack, 10A on the big one) and you
blow the meter's fuse — or the meter. And leaving the probes in the
current jacks, then measuring voltage next time, shorts the circuit
through the meter. **Move the red probe back to the voltage jack
when done.** Every multimeter owner learns this; learn it from
reading.

## Buying advice

$20–$40 gets auto-ranging (you don't pick the range — it does),
continuity beep, and diode test. That's all a beginner needs.
Expensive meters add precision and safety ratings you don't need
yet — spend the difference on components.

**Next:** [Power Supplies](power-supplies.md)
