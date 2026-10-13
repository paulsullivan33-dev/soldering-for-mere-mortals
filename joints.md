# Reading Your Joints

A good solder joint is inspectable with your eyes. Learn the looks
and you'll diagnose your own work.

## The good joint

- **Shiny** (lead solder) — smooth, reflective surface
- **Concave** — curves inward like a tiny volcano, lead visible
  but covered
- **Wetted** — solder flows smoothly onto both pad and lead, no
  sharp edges where it "refused" to stick

If it looks like a tiny Hershey's Kiss that flowed into place, you
did it right.

## The bad joints

| Problem | Looks like | Cause | Fix |
|---------|-----------|-------|-----|
| **Cold joint** | Dull, gray, lumpy or cracked | Parts moved while cooling, or never got hot enough | Reheat fully until it flows, hold still |
| **Insufficient wetting** | Solder balled up, not flowing onto pad | Pad/lead not hot enough; dirty surfaces | Clean, reheat the *parts*, feed fresh solder |
| **Solder bridge** | Blob connecting two adjacent pads/pins | Too much solder | Wick it away with desoldering braid |
| **Too much solder** | Big ball hiding the lead | Overfeeding | It's ugly but often works; wick the excess |
| **Too little** | Lead barely covered, joint starved | Underfeeding | Add a touch more to a reheated joint |
| **Lifted pad** | Copper pad peeling off the board | Overheated (too long, too hot) | Hard to fix — prevention: 3–5 seconds max |

## The magnifier test

A $10 helping-hands magnifier (or your phone's camera zoomed in)
reveals what naked eyes miss: hairline cracks in cold joints,
bridges between fine-pitch pins. Inspect, don't assume — especially
before powering a board for the first time.

## Fixing mistakes

- **Desoldering braid (wick):** copper braid that drinks molten
  solder when heated — for bridges and excess.
- **Solder sucker:** spring-loaded vacuum that inhales molten
  solder — for clearing holes.
- **Just reheat:** most ugly-but-connected joints can be reheated
  with a touch of fresh solder (fresh rosin core brings fresh flux)
  and they'll flow into shape.

**The rule:** a joint you can see through to *both* metals, shiny
and still, is a joint you can trust. When in doubt, reheat it —
rework is normal, not failure.

**Next:** [Breadboard to Permanent](breadboard-to-permanent.md)
