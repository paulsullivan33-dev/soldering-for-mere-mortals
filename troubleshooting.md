# Troubleshooting

## The universal checklist (in order)

1. **Is it powered?** Meter the rails — actual volts, not "the LED
   on the supply is lit."
2. **Is the loop complete?** Power → components → ground, no
   breaks. Continuity mode finds opens.
3. **Polarity?** LED/diode/capacitor/electrolytic the right way
   round? Chip notch matching the board marking?
4. **Shorts?** Power off, continuity between 5V and GND — beep =
   don't power it.
5. **The right values?** Meter the resistors (color codes lie to
   eyes); check the math ([Ohm's Law](ohms-law.md)).

Most dead circuits confess by step 3.

## Symptom → fix

**Nothing happens at all**

Power first: supply voltage present? Switch on? Battery dead?
Then the loop: a single broken connection kills everything —
re-seat breadboard wires (they loosen), reflow suspect joints.

**LED doesn't light**

Resistor value correct? (Meter it.) LED polarity (long leg to
positive)? Pin actually driven (Arduino: `pinMode OUTPUT`)?
Try the LED + resistor straight across the supply — isolates the
LED from the rest of the circuit.

**Works on breadboard, dies soldered**

A solder bridge (continuity-test adjacent pins), a cold joint that
was a good breadboard contact, or a component cooked during
soldering (ICs and LEDs are heat-sensitive — 3–5 seconds max, use
a heatsink clip on delicate leads).

**Intermittent / works when touched**

The classic cold joint or loose breadboard wire — touching flexes
it into contact. Reflow every joint in the suspect area; replace
the wire. "Works until I move it" is a mechanical problem, not an
electrical one — see strain relief in [Breadboard to
Permanent](breadboard-to-permanent.md).

**Chip gets hot**

Something's drawing too much current: short downstream, backwards
power, or the chip driving a load it can't (a motor straight off a
logic pin). **Unplug immediately** — hot chips are telling you
exactly what's wrong. Find the excess current with the meter
before powering again.

**Right voltage in, wrong voltage out**

Voltage divider loaded down (see the caveat in [Ohm's
Law](ohms-law.md)), regulator overheating into thermal shutdown,
or the supply sagging under load (9V batteries are notorious).

**Analog readings are noisy/jumpy**

Missing decoupling capacitor, long unshielded wires acting as
antennas, or a floating input (nothing connected — it reads the
room's electromagnetic gossip). Add the 0.1µF cap, shorten wires,
tie unused inputs somewhere.

## The method

Halve the problem: power section vs. signal section, one half at a
time. Change one thing. Write down what you measured — "3.1V here,
0V there" beats "it doesn't work" every time, especially when you
ask for help (with photos of *both* sides of the board).

**Next:** [Glossary](glossary.md)
