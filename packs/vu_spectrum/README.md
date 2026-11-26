# SPECTRUM and SUNDOWN (vu_spectrum.pack)

*Part of [field-packs](../../README.md), a look pack of [vu](../vu/README.md) 24. From the repository's root:
`OPEN_FIELD=<open-field> make vu_spectrum`; its host test is vu's (`bash tools/test_pack.sh vu`).*

Needs **vu.pack 24 or later** on the unit: the look registers with it at the first frame, and vu paints it on the mixer's
levels page, steps to it with a tap of the mixer key and turns TE's EQ with the knobs on it. Without vu 24 the pack does
nothing (an older vu does not know it).

| Where | What | Does |
| --- | --- | --- |
| settings | none of its own (since vu 25) | SPECTRUM and SUNDOWN in vu's round while installed |

## The look

- **SPECTRUM**: 32 bands, 40 Hz to 16 kHz, 24 segments of 2.5 dB each. Green at the bottom, then yellow, orange and
  red. Unlit segments stay dim. A peak segment holds for 0.7 s and then falls.
- **SUNDOWN** (vu 23): a synthwave sunset in LED segments. A striped sun sets on a neon horizon behind mountains made
  of the bands: 8 peaks a side, mirrored, the lows at the edges and the highs by the sun, each peak as high as the
  loudest of its 4 bands, a pale ridge on top. A kick swells the sun a little. Below, the reflection in dim rows.
  SUNDOWN is a look of its own after SPECTRUM.
  **vu_spectrum 2**: under the horizon the bands come alive too, a water reflection. The mountains mirrored downward,
  as tall as above, bright by the horizon and fading with depth, in LED rows 2 on 2 off, each row shifted a pixel or
  two on a ripple that runs with time (wider on a kick). The sun's reflection is broken stripes narrowing downward,
  4 to ~19 rows long with the lows' level. ~0.32 M average / 0.55 M worst on the calibrated model (was 0.30 / 0.52).

  ![SUNDOWN](pictures/sundown_2x.png)

