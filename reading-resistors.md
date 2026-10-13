# Reading Resistors

Resistors are too small for printed numbers, so they wear their
value as **colored bands**. Learn the code once and you'll read
them at a glance.

## The code

| Color | Digit | Multiplier |
|-------|-------|------------|
| Black | 0 | ×1 |
| Brown | 1 | ×10 |
| Red | 2 | ×100 |
| Orange | 3 | ×1,000 |
| Yellow | 4 | ×10,000 |
| Green | 5 | ×100,000 |
| Blue | 6 | ×1,000,000 |
| Violet | 7 | — |
| Gray | 8 | — |
| White | 9 | — |
| Gold | — | ×0.1 (±5%) |
| Silver | — | ×0.01 (±10%) |

**How to read:** first two bands are digits, third is the
multiplier. (The gold/silver band at the end is tolerance — how far
off it may be — and goes on the right.)

## Worked examples (all verified)

- **Red, red, brown** → 2, 2, ×10 → **220Ω**
- **Brown, black, red** → 1, 0, ×100 → **1,000Ω = 1kΩ**
- **Yellow, violet, brown** → 4, 7, ×10 → **470Ω**
- **Orange, orange, red** → 3, 3, ×100 → **3,300Ω = 3.3kΩ**
- **Brown, black, orange** → 1, 0, ×1,000 → **10,000Ω = 10kΩ**

**Check:** red-red-brown is the LED resistor from [The LED
Circuit](led-circuit.md) — 220Ω. If your kit's "220Ω" reads
brown-black-red, that's 1kΩ, not 220Ω — close enough to dim an LED
noticeably, wrong enough to matter.

## The mnemonics (pick one)

"**B**ig **B**rown **R**abbits **O**ften **Y**ield **G**reat **B**ig
**V**ocal **G**roans **W**hen **G**ingerly **S**lapped" — Black,
Brown, Red, Orange, Yellow, Green, Blue, Violet, Gray, White, Gold,
Silver. Silly is the point; silly sticks.

## When bands lie to your eyes

Red vs. orange vs. brown under warm lighting is genuinely hard.
**The multimeter settles it** — measure the resistor (see [The
Multimeter](multimeter.md)). Beginners should verify-by-meter
whenever the circuit misbehaves; even experienced builders do when
the lighting is bad.

**E12 values:** resistors come in standard values (10, 12, 15, 18,
22, 27, 33, 39, 47, 56, 68, 82 per decade) — that's why it's always
220Ω and never 200Ω. If your calculation says 187Ω, you buy 180Ω or
220Ω and re-check the math.

**Next:** [The LED Circuit](led-circuit.md)
