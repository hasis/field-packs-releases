# perform

The PERFORM face and the song arranger on the tape screen. Part of **tape views 1**. Version 6. **Needs
[markers](../markers/README.md).** Works with [themes](../themes/README.md) (the face in a look), [punch](../punch/README.md)
(effects on the face), [miditracks](../miditracks/README.md). Without markers it does not load; without themes it
draws its own plain face; without punch the face has no effects.

## The face

- On the tape screen, **click the 4th knob** (no shift, no HELP): the tape screen <-> PERFORM. Kept after a restart.
- The parts are the tape's markers in tape order: name, the bar it starts at, its length in bars. The playing part has a
  solid triangle and its bar filling up; the cued one a hollow triangle and a countdown (`B IN 1.1`).
- With the theme off (or no themes) perform draws its own **plain face**; with a look, the look draws it in full.
- shift + a marked key, TAPE + key and the program changes work as on the tape screen (markers').

## The song (arranger)

Up to 8 rows, each a marker's section, played **x1..x8**, **HOLD** (until you let it go) or **SKIP**, for its own
length or a number of bars. While the face is PERFORM the song plays, on any screen. A tape nobody arranged plays as it
lies. The last row, END, says what the end does (STOP, LOOP, ON).

**EDIT** (on the face): **hold HELP** (or **HELP + 4th click** to keep it open; the 4th click or a HELP tap closes it).

| Gesture | Does |
| --- | --- |
| 1st knob turn / click | PICK a row / CUE it (it plays when this pass ends; twice quickly: now) |
| 2nd knob turn / click | MOVE the row up or down / COPY it under itself |
| shift + 2nd click | OUT: remove the row |
| 3rd knob turn / click | TIMES: SKIP, x1..x8, HOLD / X2 |
| 4th knob turn | BARS: shorter or longer than the section |
| a marked key | ADD that section under the cursor |
| TE's undo | takes the last edit back (each edit is one step of TE's undo) |

The song is kept inside the tape. **EDIT has passed the computer tests only** so far.
