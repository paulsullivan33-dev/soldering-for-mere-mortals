# Power Supplies

Every circuit needs power with the right voltage, enough current,
and the correct polarity. Get any of the three wrong and things
break — quietly or dramatically.

## The options

| Source | Voltage | Current | Best for |
|--------|---------|---------|----------|
| AA batteries (4×) | ~6V fresh | ~1A | Portable prototypes |
| 9V battery | 9V | ~500mA, low capacity | Quick tests (dies fast) |
| USB (5V) | 5V | 500mA–2A+ | Arduino/logic projects |
| Wall wart (regulated 5V/12V) | Fixed | 1–3A typical | Permanent projects |
| Bench supply | Adjustable | Amps, with current limit | The lab luxury (buy last) |

**mAh is capacity, A is delivery.** A 2000 mAh battery holds 2000
milliamp-hours of charge; whether it can *deliver* 2A right now is a
separate question (see the draw in [Ohm's Law](ohms-law.md) — a
9V battery sags under loads a wall wart shrugs at).

## Polarity: the killer

**Center-positive** barrel jacks are the near-universal standard —
but "near" isn't "always." Reversed polarity kills unprotected
circuits instantly and silently. Defenses, in order of preference:

1. **Check before connecting.** Meter the supply; read the label.
   Ten seconds, every time, with a new supply.
2. **A series diode** in your circuit — backwards power simply
   doesn't flow (costs ~0.7V drop).
3. **Polarized connectors** — JST, barrel jacks: physically can't
   plug in backwards.

## Regulators: making the voltage you need

A **linear regulator** (7805: 7–12V in → 5V out) burns the excess
as heat. Fine for small drops and currents; wasteful for big ones
(12V→5V at 1A = 7W of heat — that's a heatsink, not a component).

A **buck converter** (switching regulator) chops and smooths —
~90% efficient, tiny, a few dollars. For battery projects or big
voltage drops, buck wins. The trade: slightly noisier output (fine
for digital, occasionally not for sensitive analog).

## Decoupling: the capacitor that prevents ghosts

Digital chips gulp current in nanosecond spikes the supply can't
track — voltage droops, chips glitch. The fix: a **0.1µF ceramic
capacitor** physically close across each chip's power pins. It
supplies the spikes locally. When a circuit "mostly works but acts
weird," a missing decoupling cap is suspect #1. It's a 2-cent part;
sprinkle generously.

## Grounding: one reference

All your supplies' grounds should connect together — the Arduino's
GND, the motor supply's GND, the sensor's GND. Voltages are
*relative*; without a shared ground, "5V" on one supply is
meaningless to another. **Common ground first, signals second.**

**Next:** [Safety](safety.md)
