# punch

Punch-in effects on everything the unit plays, held on the keyboard while the PERFORM face is up. Part of **tape views
1**. Version 3. **Needs perform or vu to play:** the keys hold the effects on perform's face (plain or in a look) or on
a vu look with vu's **punch keys** on, not on TE's own mixer page. Without either, only a PUNCH lane (miditracks) plays
the effects; program changes count only while a face is up. Works with [perform](../perform/README.md) (the face),
[themes](../themes/README.md) (the strip drawn in a look), [miditracks](../miditracks/README.md) (PUNCH lanes).

## Play

On the PERFORM face, **hold one of the 14 white keys from the lowest F**; the effect is on while you hold it:

| Key | F | G | A | B | C | D | E | F | G | A | B | C | D | E |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Effect | LP | HP | JET | CRUSH | GATE | RISE | DUB | VERB | STUTR | GLITCH | DIVE | PUMP | ISO | SCRATCH |

- Up to **4 at once**; a 5th key shows **FULL** and does nothing.
- While you hold a key, the **1st..4th knobs** set that effect's four values (1st = where / time, 2nd = character, 3rd =
  shape, 4th = depth; ISO: LOW, MID, HIGH, crossover). The last key pressed owns the knobs. The values are kept per tape.
- shift + key (cue), HELP + key (marker), TAPE + key: as without punch. The black keys play the synth.
- **MIDI:** program changes hold and release the effects while the face is up (25-32 hold the first 8, 49-56 let them go;
  57-62 hold the other six, 65-70 let them go).
- **PUNCH lanes:** with miditracks, a MIDI track set to the output PUNCH plays effects from its notes while the tape
  plays; hold REC on that track on the face and play the effect keys to record them.
- With vu installed and its setting **punch keys** on, the keys hold the effects over vu's mixer looks too.

## Known limits

- The effects go to the speaker and the outputs; don't expect them on a tape recording.
- Nothing held and no tail ringing: the sound passes untouched.
