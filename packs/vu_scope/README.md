# SCOPE (vu_scope.pack)

*Part of [field-packs](../../README.md), a look pack of [vu](../vu/README.md) 24. From the repository's root:
`OPEN_FIELD=<open-field> make vu_scope`; its host test is vu's (`bash tools/test_pack.sh vu`).*

Needs **vu.pack 24 or later** on the unit: the look registers with it at the first frame, and vu paints it on the mixer's
levels page, steps to it with a tap of the mixer key and turns TE's EQ with the knobs on it. Without vu 24 the pack does
nothing (an older vu does not know it).

| Where | What | Does |
| --- | --- | --- |
| settings | none of its own (since vu 25) | in vu's round while installed |

## The look

- **SCOPE**: two CRT screens in green phosphor, an old terminal (inspired by the look, nothing of anyone's): green bezels,
  scanlines, darker curving corners, a slight flicker, labels in the pixel font. Out of phase is shown by a hatched half
  and the words OUT and MONO, not by a hue.
  - **The wave**: on the left, a graticule of 10 × 8 divisions with minor ticks on the axes. The trace is phosphor green
    with a glow and fades over a few frames. It starts on a rising zero crossing, so a steady tone stands still. The
    gain finds the loudest of the last 23 ms (from x1 to x32): down at once, back up over about a second. GAIN shows it.
  - **The goniometer**: a round CRT on the right with rings and the L, R and M axes. Its phosphor dots fade.
  - **The phase meter**: a recessed scale from -1 (out of phase, hatched) through 0 to +1 (mono), with a bright marker.
  - The still parts of both looks (faces, scales, bezels, graticules) are drawn on the Mac (`meter_art.py`, 28 KB of
    column runs). Only the needles, lamps and traces are drawn on the unit.
- vu 24: its two phosphor pictures are its own memory (18 KB); in vu 23 it borrowed GOOD TIMES'.

