# lanes

Waveforms and a height zoom on the OP-1 Field's own tape screen, in TE's look. Part of **tape views 1**.

Version 94, OS 1.7.3 (the +0 and +1 releases both work), open-field. Needs nothing else; works alone.

## What it does

- **Waveforms** inside TE's clip bars. Settings > PACKS > lanes > **waveform** on (off at first). The tape has to have
  been heard first: a part not played since the switch shows a dotted middle line until the tape plays over it. After
  that the waveform is kept per tape.
- **wave fill** (settings > PACKS > lanes, off at first): with the tape stopped, lanes reads the rest of the tape in the
  background (about 80 s for a 2-minute song) so the whole waveform fills in by itself.
- **Height zoom:** hold **HELP** and turn the **4th knob** (from the left): 8 / 4 / 2 / 1 tracks (turning right shows
  more). The page follows the selected track, so TE's track keys scroll it. A short flash names what you see:
  `LANES 8`, `LANES 5-8`, `LANE 6`.
- **tall lanes** (settings > PACKS > lanes, off at first): on TE's own tape screen TE's header stays, its ruler moves up
  under it and the lanes fill the screen below (8 tracks: about 15 px a lane instead of 5), with the waveform and MIDI
  notes; TE's whole deck, small, sits in the centre over the play-head and TE's timecode moves top right. The zoom (HELP + 4th turn) then runs tall 8 / 4 / 2 / 1, `TAPE`
  (TE's screen with its 8 rows), `TAPE 1-4` / `TAPE 5-8`. Tall lanes stay off while a theme paints the tape screen. With
  **markers** installed its flags hang above the moved ruler (at the `TAPE` steps in TE's own layout again).
- With **miditracks** installed, MIDI tracks' notes are drawn in TE's rows.
- With **themes** and a look installed, the look draws the tape screen; lanes then gives it the waveform and the zoom.
- **Without the others:** no markers = no flags (lanes then does markers' time zoom, HELP + 2nd turn, itself); no
  miditracks = no notes; no 8 tracks = 4 lanes.

## Files on the unit

`user/pf/lanes/`: the kept waveforms, one file a tape. On open-field 0.24 and older they stay when you delete a tape and
are not copied with a tape copy (the copy's waveform fills in again as it plays). On a base with files per tape
(open-field PR #55, pending) they follow the tape.

## Known limits

- On TE's own screen a clip narrower than about 8 px may show no waveform.
- wave fill has passed the computer tests only.
- tall lanes cost processor time (about 0.88 M cycles a frame on the unit).
