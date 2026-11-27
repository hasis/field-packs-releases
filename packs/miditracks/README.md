# miditracks

Any tape track can be a MIDI track: record notes against the tape and play them to the synth, the drum or MIDI out.
Part of **tape views 1**. Version 47. Needs nothing else. Works with seqbank 20 (the insert browser; from the seq 20 release), themes (notes
drawn in the lanes), [punch](../punch/README.md) (PUNCH lanes), seqx (note lengths in EDIT), cherd. Any track 1-4 can
be a MIDI track without 8 tracks; 8 tracks adds tracks 5-8 (with our 8 tracks 13 / 14 they follow the mixer's mutes).
Without lanes it draws its notes itself; without punch a PUNCH track is silent.

## Play (tape screen)

| Gesture | Does |
| --- | --- |
| **shift + 4th click** | the selected track AUDIO <-> MIDI (flash e.g. `T2 CH1 SYNTH`) |
| **REC held** on a MIDI track | record: play keys or send MIDI in. Playing without REC only auditions |
| **shift + 1st click** | the insert browser (needs seqbank): genres, slots, NOW / MIDI FILES. In it, **3rd knob** = MIDI channel, **4th knob** = output: **MIDI, SYNTH, DRUM, BOTH, PUNCH**. A click on a slot inserts it (tape stopped) |
| **shift + 2nd click** | insert the last pick again |
| **shift + 3rd click**, twice within 1.5 s | clear the whole MIDI track (tape stopped) |
| mute, LIFT / DROP, TE's undo | as on an audio track |
| PATTERN screen: **shift + 4th click** | EDIT: the MIDI track's bar in TE's grid; again: write it back; shift + 4th turn: next bar |

Without seqbank there is no browser: on a MIDI track, shift + 1st / 2nd turn set its channel / output.

**PUNCH** (output): the track's notes hold punch's effects while the tape plays (the note = the effect's key). Has passed
the computer tests only so far.

## Files on the unit

`user/pf/miditracks/tape<N>.mtk`, one a tape. **On Faust's stock base (open-field 0.24, base 42, and older) these
files do not follow TE's tape copy and delete:** the base does not copy or remove them. miditracks catches a copy itself
when the original tape has been loaded once with miditracks installed (a tape copied before that starts empty), and a
deleted tape's file stays on the unit until a new tape takes that number (it starts empty). On a base with files per
tape (open-field PR #55, pending) the base copies and removes them with the tape. With Faust's 8 tracks a MIDI track on
5-8 can't be muted.
