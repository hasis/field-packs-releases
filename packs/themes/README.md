# themes

Draws the tape screen, the PERFORM face and TE's mixer levels page in a look. Part of **tape views 1**.

Version 11, OS 1.7.3 (the +0 and +1 releases both work), open-field. **Needs a look pack**: [theme_89mph](../theme_89mph/README.md) and / or
[theme_console](../theme_console/README.md). themes alone has no look of its own: with no look on, every screen is TE's. Without lanes a look has no waveform and
no height zoom; without markers no flags, sections or cue; without perform no PERFORM face.

## Choosing a look

- **On Faust's stock base (open-field 0.24, base 42, and older):** there is **no theme setting** (that base does not
  show settings with words). The look is **on whenever installed**: the look packs you install decide it. Install
  **one** look pack only; to go back to TE's screen, remove themes.pack (or the look).
- **On a base with option words (open-field PR #56, pending):** settings > PACKS > themes > **theme**: off, or one of
  the looks installed (89MPH, CONSOLE). Off = TE's own tape screen (with lanes' waveform, zoom and tall lanes).

## What a look draws

- The **tape screen**: header (time, bar.beat, transport, tempo, the selected track), marker flags, ruler, loop, 8 lanes
  with clips, MIDI notes (lanes, which adds the waveform and the height zoom, follows in a later release).
- The **PERFORM face** (with perform): the parts as a set list, the song, EDIT, the punch-in strip.
- **TE's mixer** levels page in the 89MPH look (CONSOLE leaves the mixer TE's).
- TE's count-in while it counts (`COUNT 3`), in the look's own letters.
- It steps back for TE's dialogs and menus; engines, sequencers and CHERD are never drawn over.

The word at the right edge says what the 4th knob's click does: `4TH: PERFORM` on the tape screen, `4TH: LANES` on the face.

## Known limits

- A look costs more processor time than TE's screen; 89MPH the most. If the unit feels slow, try CONSOLE or off.
- The 89MPH mixer shows tracks 5-8 (hold the mixer key) only with an 8 tracks that hands over their levels (our 8
  tracks 13, not public yet); otherwise tracks 1-4.
