# Breadboard to Permanent

**Breadboards** are for experimenting; **solder** is for keeping.
Knowing when to move — and what to move *to* — is the workflow.

## The progression

1. **Breadboard** — solderless, reusable, fragile. For figuring out
   the circuit. (See [Arduino for Mere
   Mortals](https://paulsullivan33-dev.github.io/arduino-for-mere-mortals/)'s
   wiring notes.)
2. **Perfboard/stripboard** — solder the same layout permanently.
   Cheap, hand-solderable, slightly ugly. For one-offs that need to
   survive handling.
3. **Custom PCB** — designed in software (KiCad, free), manufactured
   for a few dollars. For multiples, or when it must look real.

Most hobby projects live happily at step 2 forever. Step 3 is
easier than its reputation, but it's a separate skill (and guide).

## Perfboard technique

- **Plan on paper first.** Sketch the layout — which holes, where
  the traces run. Perfboard has no forgiveness for "I'll figure it
  out as I go."
- **Solder from the copper side**, components on the plain side.
- **Use the component leads as traces.** Bend a resistor's leg over
  to the next hole and solder both — free wiring.
- **Cut a trace** (stripboard) with a drill bit twist or a craft
  knife where you need a break. Verify the cut with a multimeter
  (continuity mode) — visual "looks cut" lies.

## Wire to board: strain relief

Wires soldered straight to a board break at the joint when flexed —
solder is stiff, wire is not, and the boundary fatigues. **Strain
relief**: loop the wire through a mounting hole first, or hot-glue
it to the board after soldering, so tugs pull on the glue/hole, not
the joint. Every "it worked until I moved it" failure is this.

## Connectors vs. hardwired

Solder wires directly for things that never disconnect. Use
**connectors** (pin headers, JST, screw terminals) for anything
you'll unplug: power, sensors you might swap, boards you might
replace. Desoldering a hardwired power lead for the tenth time is
how pads get lifted.

**Next:** [The Multimeter](multimeter.md)
