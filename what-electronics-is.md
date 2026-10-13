# What Electronics Is

**The one-sentence version:** Electronics is controlling the flow
of electric charge to do useful things — and nearly all of it comes
down to three quantities: voltage, current, and resistance.

## The three quantities

| Quantity | Unit | Water analogy | What it is |
|----------|------|---------------|------------|
| Voltage (V) | Volts | Water pressure | How hard charge is pushed |
| Current (I) | Amps | Flow rate | How much charge flows per second |
| Resistance (R) | Ohms (Ω) | Pipe narrowness | How much the flow is opposed |

The water analogy isn't perfect (electrons don't pool and leak like
water), but it carries you surprisingly far: high voltage is high
pressure, a resistor is a narrow pipe section, and a short circuit
is a burst pipe — all the water rushing where it shouldn't.

## The one rule of circuits

**Current needs a complete loop.** Charge flows from the power
source, through your components, and *back* to the source. Break the
loop anywhere and everything stops. Every circuit you'll ever build
is a loop — battery (+) → components → battery (−). When something
doesn't work, "where's the loop broken?" is the first question.

(Ground, marked **GND**, is the agreed-upon zero point — the
reference everything is measured against. In a battery circuit,
it's the negative terminal's job title.)

## DC vs. AC

- **DC** (direct current) — flows one direction. Batteries,
  Arduinos, USB: everything in this guide.
- **AC** (alternating current) — flips direction 50/60 times per
  second. Wall outlets. **Not in this guide** — mains electricity
  can kill you, and working on it is electrician territory. See
  [Safety](safety.md).

## Why low voltage is forgiving (and where it isn't)

At 5V, mistakes mostly cost components, not fingers — you can touch
a 5V circuit and feel nothing. That's what makes this a safe hobby
*at these voltages*. The unforgiving parts at low voltage: **heat**
(soldering irons, shorted batteries), **eyes** (clipped wire ends
fly), and **lithium batteries** (punctured ones burn). All covered
in [Safety](safety.md).

## What electronics is not

- **Not magic.** Every behavior in this guide follows from
  V = I × R and the loop rule. When confused, return to those.
- **Not just Arduino.** Arduino is a *user* of electronics; this
  guide is the layer underneath — useful with or without a
  microcontroller.
- **Not mains wiring.** Repeating because it matters: wall-outlet
  electricity is a different subject with lethal failure modes.

**Next:** [Ohm's Law](ohms-law.md)
