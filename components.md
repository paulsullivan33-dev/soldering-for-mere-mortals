# Components

The cast of characters. Each one does *one* thing — learn the thing,
and schematics stop looking like hieroglyphs.

## Resistor: the flow limiter

The narrow pipe. Drops voltage and limits current, turning the
excess into heat. Marked in **ohms** (Ω, kΩ, MΩ).

```text
---[====]---     (schematic symbol)
```

Uses: LED current limiting (see [The LED Circuit](led-circuit.md)),
voltage dividers, pull-ups. The most common component you'll touch.

## Capacitor: the tiny rechargeable bucket

Stores charge, then releases it. Blocks DC (once charged, no more
flows) but passes AC — which makes it useful for smoothing power
supplies and timing circuits. Marked in **farads** (µF, nF, pF —
*very* small numbers).

```text
---[||]---       (schematic symbol)
```

**Two kinds:** ceramic (small values, no polarity — either way
works) and electrolytic (large values, **polarized** — the stripe
marks negative; backwards = venting or popping). When a circuit
"mostly works but glitches," a missing decoupling capacitor across
the power rails is a prime suspect.

## Diode: the one-way valve

Lets current through in one direction, blocks it in the other. The
stripe marks the **cathode** (the "out" side for conventional flow).

```text
---|>|---        (schematic symbol, current flows with the arrow)
```

Uses: reverse-polarity protection (a diode in series means a
backwards battery simply doesn't connect), and...

## LED: a diode that glows

A Light-Emitting Diode — a diode that spends its ~2V forward drop
as light instead of just heat. **Polarized**: long leg (anode) to
positive, short leg (cathode, flat side) to ground.

**Always with a resistor.** An LED without current limiting draws
everything available — bright for a second, then dead. The
calculation is in [The LED Circuit](led-circuit.md); the rule is
here: **no LED without a resistor** (except Arduino's built-in one,
which has its own).

## Transistor: the electronic switch (and amplifier)

Three legs; a small current (or voltage) at the middle leg controls
a large current through the other two. It's how a 20 mA Arduino pin
switches a 500 mA motor: the Arduino tickles the transistor, the
transistor handles the heavy lifting.

Two common families: **BJT** (current-controlled: NPN/PNP) and
**MOSFET** (voltage-controlled — the better switch for most
beginner projects; an IRLZ44N driven straight from a 5V pin is the
classic). Transistors are also how *all* digital logic is built —
your computer is billions of them.

## The supporting cast (you'll meet them)

| Component | Does | Note |
|-----------|------|------|
| Potentiometer | Variable resistor (a knob) | Three legs; the middle wiper divides voltage |
| Pushbutton | Momentary connection | Press = closed, release = open |
| Buzzer/piezo | Makes noise from voltage | Active (just add power) vs. passive (needs a signal) |
| Voltage regulator | Fixed output voltage from a higher input | 7805: 7–12V in, 5V out (wastes the rest as heat) |
| Crystal/oscillator | Precise clock signal | Why your Arduino runs at exactly 16 MHz |

You don't need to memorize these — you need to recognize them in a
kit and know which chapter to open. Datasheets (the component's
official spec document) answer the rest; "learn to skim a
datasheet" is a genuine beginner superpower.

**Next:** [Reading Resistors](reading-resistors.md)
