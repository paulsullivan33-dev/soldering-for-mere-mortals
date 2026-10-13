# Soldering

**Soldering** joins metal parts with a melted filler alloy — an
electrical *and* mechanical connection in one. It's the skill that
turns a breadboard prototype into something permanent.

## What you need (the honest minimum)

- **Soldering iron** — a temperature-controlled station (~$30)
  beats a bare $10 stick enormously. Set ~350°C for lead solder,
  ~370°C for lead-free.
- **Solder** — 63/37 tin-lead, 0.8mm, rosin core. (Yes, lead —
  see [Safety](safety.md) for handling. Lead-free works but is
  fussier for beginners.)
- **Brass wool or damp sponge** — tip cleaner. Clean the tip
  *every few joints*.
- **Helping hands / PCB holder** — a third hand. Literally.
- **Ventilation** — a small fan blowing fumes away from your face.

Nice later: flux pen, solder sucker, good side cutters, safety
glasses.

## The joint, step by step

You're soldering a wire into a PCB hole (a "through-hole" joint —
where beginners start):

1. **Tin the tip.** Melt a little solder onto the clean iron tip —
   it should look shiny. A dry tip doesn't transfer heat.
2. **Heat the joint, not the solder.** Touch the tip so it contacts
   *both* the pad and the wire lead. Count to three — the parts
   must reach solder-melting temperature.
3. **Feed solder into the joint** — touch it to the heated parts
   (not the iron tip). It should melt and flow *around* the lead,
   wicking into the hole.
4. **Remove solder, then iron.** About a second apart — solder
   first, so the joint doesn't keep cooking.
5. **Don't move it.** Hold still for 2–3 seconds while it freezes.
   Moving makes a fractured "cold" joint.

Total heat time: ~3–5 seconds. Longer cooks the board and the
component; shorter doesn't flow.

## The mindset

**Solder follows heat.** It flows *toward* the hot metal. That's why
you heat the parts and feed solder to them — the solder chases the
heat into the joint. If your solder balls up on the iron tip, the
parts weren't hot enough. Nearly every beginner problem is some
version of "the parts weren't hot enough."

## Through-hole vs. surface-mount

- **Through-hole** — leads go through holes; solder on the other
  side. Big, forgiving, what this guide teaches.
- **Surface-mount (SMD)** — tiny parts soldered onto pads. Doable
  with tweezers, flux, and practice — but learn through-hole first.

## Practice before the real thing

Solder a row of spare resistors into perfboard and inspect every
joint (see [Reading Your Joints](joints.md)). Twenty practice
joints cost pennies and save your actual project. Your tenth joint
will embarrass your first — that's the expected curve.

**Next:** [Reading Your Joints](joints.md)
