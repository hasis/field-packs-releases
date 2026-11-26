# LCD (vu_lcd.pack)

*Part of [field-packs](../../README.md), a look pack of [vu](../vu/README.md) 24. From the repository's root:
`OPEN_FIELD=<open-field> make vu_lcd`; its host test is vu's (`bash tools/test_pack.sh vu`).*

Needs **vu.pack 24 or later** on the unit: the look registers with it at the first frame, and vu paints it on the mixer's
levels page, steps to it with a tap of the mixer key and turns TE's EQ with the knobs on it. Without vu 24 the pack does
nothing (an older vu does not know it).

| Where | What | Does |
| --- | --- | --- |
| settings | none of its own (since vu 25) | in vu's round while installed |

## The look

- **LCD**: a backlit dot-matrix panel of 120 × 54 chunky dots, with the unlit dots visible (vu_lcd 3: the backlight dimmed to about half the light, the lit dots nearly black). The top line scrolls the
  tape, BPM, play state and MASTER MIX. Under it, the tape's time, the tape number and BPM, then 30 bars with peak dots.

