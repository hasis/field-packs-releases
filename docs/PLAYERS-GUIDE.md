# OP-1 Field: Player's Guide to field-packs

Everything the released packs add to the OP-1 Field, and how to play them: OS 1.7.3 (+0 or +1) with Faust's open-field. **fx 1.4** (snowtrain, wagons with BEIGNET, TUNE) is section 3; **CHERD 55** (cherd 55; named after the pack's version, as CHERD 37 was), its own release with its own [manual](../packs/cherd/MANUAL.md), is section 2; **engines 2** (native synth engines, each with its own manual: [lilith](../packs/lilith/MANUAL.md), the [clarinet](../packs/clarinet/MANUAL.md) and [boarder](../packs/boarder/MANUAL.md)) is sections 4 to 6; **recstart 1** is section 7; **seq 1** (seqx, seqbank) is section 8; **vu 34** (the mixer's visualizers, named after vu.pack's version) is section 9; **tape views 1** (the tape screen: lanes, markers, perform, punch, themes and its looks, miditracks) is section 10. Where a feature needs one of our forks of Faust's platform packs (fx train 18+, 8 tracks 13), the text says so; everything else runs on Faust's stock open-field. Pack versions: the [README](../README.md). Gestures were checked against each pack's input code (flash words are quoted as the code prints them).

**How to read the gestures**

- **Knobs** are the **1st, 2nd, 3rd and 4th encoder from the left**. "Turn" means turn the knob; "click" means press it.
- **A + B** means hold A, then press B.
- **T1-T4** are the four page keys under the screen (T1 the sound's engine, T3 its effect). The mode keys are synth, drum, tape and mixer.
- Key names: **HELP** (the ? key), **REC**, **PLAY**, **STOP**, **shift**, **LIFT**, **DROP**, **left / right arrows** (<< and >>), **TAPE** (the tape mode key).
- TE's own gestures stay TE's. Only the gestures listed here are new.

---

## Cheat sheet

### Any screen
| Gesture | Does | Pack |
|---|---|---|
| REC held, tape stopped (audio track) | WAITING: INPUT and the level; sound over the threshold (TE's input THRESHOLD or recstart's own) starts the take | recstart |
| shift + HELP | the TUNE page (shift + HELP or plain HELP closes it); tune 29: not on the tape screen while markers is there (markers' HELP there) | tune |
| HELP at power-on | safe start: no packs load | base |

### Synth screens
| Gesture | Does | Pack |
|---|---|---|
| T3 list | BOOST, GATE, FREEZE, TAPE, JUNEAUX, ROTARY, BEIGNET, TUNE | wagons, tune |
| T3 | the train: TE's effect and three pack effects as wagons (knob N = wagon N) | snowtrain |
| HELP on the train | snowtrain's presets | snowtrain |
| sequencer list | CHERD | cherd |
| shift + T1 | engine list: lilith | lilith |
| 1st..4th turn (+ shift) on lilith | cutoff, reso, eg amt, decay (tune, mix, wave, sync) | lilith |
| shift + T1 | engine list: clarinet | clarinet |
| 1st..4th turn (+ shift) on the clarinet | BREATH, BRIGHT, VIBRATO, REED (NOISE, RATE, SCOOP, LEGATO) | clarinet |
| shift + T1 | engine list: boarder | boarder |
| 1st..4th turn (+ shift) on boarder | LOW, MID, HIGH, PERC (CLICK, VIB, DRIVE, LEAK / MODE); in a combo mode the 4th is TONE | boarder |
| HELP on PATTERN, ENDLESS or FINGER | seqbank's banks of patterns | seqbank |
| PATTERN: hold a note's key + 2nd / 3rd / 4th turn | probability / ratchet / length of that note | seqx |

### Tape screen (tape views 1)
| Gesture | Does | Pack |
| --- | --- | --- |
| HELP + 4th turn | height zoom: 8 / 4 / 2 / 1 tracks (right = more), following the selected track | lanes |
| HELP + 4th turn, option *tall lanes* on (settings > packs > lanes) | tall 8 / 4 / 2 / 1 tracks, then TAPE (TE's screen, 8 rows), then TAPE 1-4 / 5-8 | lanes |
| HELP + a key | set that key's marker at the play-head, on the beat (keep HELP, turn the 1st knob: its name) | markers |
| HELP + shift + key | clear that marker | markers |
| shift + marked key | cue it (plays when this section ends); twice quickly: jump now; held 0.5 s: loop it | markers |
| HELP + left / right arrow | previous / next marker | markers |
| HELP + 2nd turn | time zoom: 1, 2, 4, AUTO, 8, 16, 32 bars | markers |
| HELP held: 3rd click, 3rd turn, 3rd click | arrange: pick a section, move it, commit (tape stopped; one undo takes it back) | markers |
| TAPE held + marked key (any screen) | cue that marker | markers |
| 4th click | tape screen <-> the PERFORM face | perform |
| PERFORM: hold HELP (HELP + 4th click keeps it) | EDIT the song: knobs PICK / MOVE / TIMES / BARS, clicks CUE / COPY / X2 / done, shift + 2nd click OUT, a marked key ADD | perform |
| PERFORM: hold one of the 14 white keys from the lowest F (+ 1st..4th turn) | a punch-in effect while held (and its four values) | punch |
| shift + 4th click | the selected track AUDIO <-> MIDI | miditracks |
| shift + 1st click | the insert browser (3rd knob = channel, 4th = output: MIDI, SYNTH, DRUM, BOTH, PUNCH) | miditracks + seqbank |
| shift + 2nd click / shift + 3rd click twice | insert the last pick again / clear the MIDI track | miditracks |
| REC held on a MIDI track | record notes (without REC: audition only) | miditracks |

### Mixer
| Gesture | Does | Pack |
| --- | --- | --- |
| tap the mixer key (levels page up) | the next vu look (vu 36: OFF <-> the look HELP picked) | vu |
| mixer key, theme 89MPH | TE's mixer in the 89MPH look | themes |
| 1st..4th turn on a look | TE's master EQ: LOW, MID, HIGH, ALL | vu |

### CHERD page
| Gesture | Does |
|---|---|
| left octave keys (F..E) | chord flavors (silent) |
| right octave keys | roots: each key plays a chord; the line under the name: the likely next chords, the big one first |
| 1st..4th turn | Key, Scale, Spread, Flow |
| 1st click | FEEL page on / off |
| 2nd click | strum: off, up, down, alt (on FEEL: SNAP grid) |
| 3rd click | comp on / off |
| 4th click | arp on / off |
| shift held | ARP page; shift + 4th click keeps it open |
| HELP | one step back: the latched ARP page, then FEEL |
| *internal builds:* HELP held + 1st / 2nd / 3rd / 4th click | CHAINS: play / stop the chain, save the phrase, chain to TE's PATTERN (seqx) or a MIDI lane (miditracks 47), clear the slot (twice) |
| *internal builds:* HELP held + 2nd / 3rd / 4th turn | CHAINS: the step's length, the 3rd click's target (PATTERN / LANE), the slot, 1 to 16 |
| *internal builds:* HELP held + a root | STEP ENTRY (cherd 55): that chord is the chain's next step |

---

## 1. Install, safe start, logs

**Install** open-field first (0.24, base 42, with loader N1 or N2; older bases from 38 work too), with its install page ([open-field](https://github.com/LaP0573/open-field), `docs/guide.md`). Then take the packs you want:

- **With the install page's packs section**, once these packs are in its catalog.
- **fx 1.4 / CHERD 57 / engines 2 / recstart 13 / vu 34:** download `fx-1.4.zip`, `cherd-57.zip`, `engines-2.zip`, `recstart-13.zip` or `vu-34.zip` from [the releases repository](https://github.com/hasis/field-packs-releases/releases), unzip, and copy the `.pack` files from its `packs/` folder (each zip's README says what is in it). Coming from fx 1.3: replace snowtrain.pack (snowtrain 24 fixes a freeze when a tape track's wagon changes). Coming from fx 1.2: replace wagons.pack and delete `beignet.pack` (BEIGNET is in wagons 18). Coming from fx 1.1: replace snowtrain.pack and wagons.pack too. Coming from fx 1.0: delete `autotune.pack` (TUNE is `tune.pack` now; with both there the loader keeps `autotune.pack` and leaves `tune.pack` out).
- **By hand:** put the unit into disk mode, copy the `.pack` files (from the release zip, or built) into the folder `packs`, leave disk mode, switch the unit off and on. In the bootloader's drive mode the folder is `user/pk`. To take a pack away, delete its file there.

**Safe start.** Hold **HELP** while you power on. No packs load. Use this when a pack stops the unit from starting; the disk mode still shows the folder `packs`, so you can delete or replace the file.

**Logs.** Every pack writes to TE's log (`/logs` on the unit, read over dev-mode MTP).

---

## 2. CHERD: chords from one key

CHERD is a sequencer. With it on, every key plays a full chord from the key and scale you set. It is its own release (`cherd-56.zip`; CHERD 37 before it). The full manual, chords, flows, scales and all: [packs/cherd/MANUAL.md](../packs/cherd/MANUAL.md); one-page quick start: [CHERD-quickstart.pdf](CHERD-quickstart.pdf). This chapter is the short version.

**Turn it on.** In synth mode, open the sequencer list (shift + the sequencer key). CHERD is the eighth entry. Switching the sequencer off keeps CHERD's page.

**The keyboard.**

- **Left octave (F to E): flavors.** These are silent. Hold one or more while you play a root.
  F add6, F# dim, G sus2, G# minor, A sus4, A# major, B add9, C 9th, C# ALT, D 7th, D# dom7, E Spice.
  A quality (major, minor, dim, sus2, sus4) is one key, the latest held. Extensions add up.
  A flavor held when you strike a root stays with that chord until you let go of the root. A flavor pressed after the strike only lasts while you hold it (tap sus4, let go to resolve).
- **LOCK (cherd 50): HELP + a flavor key.** Hold HELP and press a left key (Spice, 7th, minor ...): that flavor is locked in, on every chord, as if you kept holding it. HELP + the same key again lets it go. Lock as many extensions as you like and one quality (locking another quality replaces it); a quality you hold still wins over the locked one, and keys you hold add on top. A locked key is a large white dot on the key picture and the top line flashes LOCK SPICE for a moment (UNLOCK SPICE when you let it go; hints off too; cherd 57: it no longer covers the left octave); with Spice locked the colours ripple just as while you hold it (cherd 52). The locks are saved with the tape. With REC held the gesture works too and never starts the tape.
- **HELP alone** acts when you let it go: one step back (the latched ARP page, then FEEL); on the main page nothing. HELP with a key, click or turn under it does not step back. On CHERD's page HELP is CHERD's alone (cherd 54).
- **Right octave: roots.** Each key plays its chord.
- **Held flavors add up, all of them (cherd 49).** Every key you hold sounds and the name says it: sus4 + 9th is C9sus4, sus2 + 7th C7sus2, minor + add9 + add6 C-6/9, dom7 + add6 C13, dim + 9th the m9b5. Sus2 and Sus4 are fixed (1 2 5, 1 4 5) like Major and Minor; add6 is the major sixth on any degree. The few notes left out on purpose are listed in `packs/cherd/README.md` (Theory).
- **Spelling (cherd 49).** A Key keeps one name whatever the Scale (major-type scales: Db Eb F# Ab Bb; minor-type: C# Eb F# G# Bb), and every scale note its own letter, double sharps included (G# harmonic minor has F##). Pentatonic and blues scales are spelled from their parent (C# minor pentatonic: C# E F# G# B; the blue note is the flat five). Chords outside the scale are spelled by their job: borrowed bII bIII bVI bVII flat (Cb and Fb in Ab major), the tritone substitute flat, a diminished leading-tone chord sharp (B#o in C# minor), flat when it comes down a semitone (Em7 Ebo7 Dm7); a borrowed chord that would need a double flat takes the plain letter (bVI in Db major is A). 7alt is spelled 1 b9 #9 3 #11 b13 b7. The key picture's letters follow (B# on the C key). The numeral: I7 IV7 V7, V/ii, ø7 and o7, + for augmented. Names only: the notes are the same.
- **NEXT (cherd 47, in CHERD 55).** After a chord, the small line under its name is what to play next: the big white name first, then two smaller grey ones; play the key of a name's first letter or simply the key with the big white box 1 on the key picture (the Field's own keyboard, F to E twice, the right octave labelled with note names; 2 and 3 are the smaller grey boxes). To hide NEXT, the note names and the numeral: settings > PACKS > cherd > hints off. The names are the chords CHERD would play there now, flavors held included; before the first chord the line shows the key's own chord, with the sequencer off it is gone. They follow the chord's quality first (cherd 49: A7 goes to Dm, Db7 to C, the Neapolitan to V, G#o up to Am), then the key's harmony and the Flow (jazz: ii V and the tritone substitute; gospel: IV I; rock: I bVII IV; django: the Andalusian run ...). Under the 1st knob the page names the chord's place in the key (ii, V, bVII).
- **Octave arrows** work over a held chord. For a second the page shows the octave under the 4th knob: OCT +1, OCT 0, OCT -2.
- **Recording.** With **REC** held, the flavor keys go to CHERD only. Only a root starts the tape.

**Main page knobs.**

| Knob | Turn | Click |
|---|---|---|
| 1st | **Key** (circle of fifths) | FEEL page on / off |
| 2nd | **Scale**: off, major, minor, dorian, mixolydian, lydian, phrygian, locrian, harmonic, melodic, and 25 more (the screen shortens them: dor, mixo, lyd, phr, loc, harm, mel) | **Strum**: off, up, down, alt |
| 3rd | **Spread**: close, open, wide, bass, lead (lead = single notes) | **Comp** on / off |
| 4th | **Flow**: off, color, jazz, pop, soul, gospel (gosp), bossa, ambient (amb), blues, rock, monk, django | **Arp** on / off |

Chord names show in fakebook style (Field Sans, from Petaluma Script). The font is inside cherd.pack: nothing to copy.

**FEEL page (1st click).** The knobs become Smooth (voice leading), Swing (even, swing, triplet), Human (tight, loose, drunk) and the comp pattern (stab, chrl, pump, sync, pompe; *pompe* is gypsy-jazz la pompe). The 2nd click on FEEL cycles **SNAP**: OFF, 1/16, 1/8, 1/4, 1/32, 1/8T, 1/16T. (While the tape records, the chords wait for the next grid line.)

**ARP page.** Hold **shift** on the CHERD page. The knobs become mode (up, down, up-down, random), rate (1/4, 1/8, 1/8T, 1/16, 1/16T, 1/32), gate (10-100 %) and octaves (1-3). **shift + 4th click** keeps the ARP page open, so you can play with both hands; shift + 4th click again lets it go. While the ARP page is up, the 1st click only closes it. The 2nd and 3rd clicks stay strum and comp on the ARP page (the 2nd is SNAP if the FEEL page is under it).

**HELP** steps back: first the kept ARP page, then the FEEL page. On the main page a HELP tap does nothing.

**Saved:** `user/pf/cherd/cherd.bin`. Key, scale, flow and smooth are shared by all synth slots. Spread, strum, comp, arp and feel are per slot.

**Chains (cherd 51; steps, clear, lanes and per tape in cherd 55).** *Coming in a later release; internal builds only (`make cherd-internal`). CHERD 56's `cherd.pack` has no chains: there HELP held + a click or the 2nd..4th knob does nothing, and HELP + a root plays the chord.* CHERD keeps the phrase you play: the last 16 chords you struck
by hand, each with its root, the flavors it was struck with (held and locked), when it came and how long you held it
(to the 16th); two bars with no key held start a new phrase. Hold **HELP** and the band under the knobs shows two
lines: what a turn sets (STEP, TARGET, SLOT) over what a click does (PLAY, SAVE, TO PATTERN / TO LANE, CLEAR):

| Gesture | Does |
|---|---|
| HELP + 2nd click | saves the phrase as a chain in the slot (SAVED 4 CHORDS) |
| HELP + 4th turn | the slot, 1 to 16 (CHAIN 3 at the top right) |
| HELP + 1st click | the chain plays round and round on CHERD's clock; again to stop (at once with the tape stopped, on the next downbeat while it rolls) |
| HELP + 4th click, twice | clears the slot: AGAIN TO CLEAR, then within a second and a half CLEARED |
| HELP + a root | **step entry**: the chord goes in as the chain's next step and sounds while you hold it (STEP 3/16 G7 2 BARS). No timing needed. Flavors: hold them before HELP, or lock them (HELP + a left key) |
| HELP + 2nd turn | the length of a step: 1/16, 1/8, 1/4, 1/2, 1 BAR, 2 BARS |
| HELP + 3rd turn | the 3rd click's target: left TO PATTERN, right TO LANE |
| HELP + 3rd click | TO PATTERN: the chain becomes TE's synth PATTERN (needs seqx), replacing what was there: 16 steps, the chords' lengths as seqx's. TO LANE: the chords land as notes on the selected MIDI track at the play-head (needs miditracks 47, tape stopped): IN LANE 12 NOTES |

A chain plays the way keys do: Key, Scale, Flow, Spread, strum, comp, arp and the flavors you hold now all apply.
Save the pattern you had in seqbank first if you want to keep it. **Chains follow the tape** (16 slots a tape,
`user/pf/cherd/tape<N>.chn`, with a base that keeps files per tape: open-field PR #55, pending); without it they are one set
for the unit, `user/pf/cherd/chains.bin`. Details: [MANUAL.md, chapter 10b](../packs/cherd/MANUAL.md).

**Works with:** GATE, FREEZE and TUNE follow CHERD's chord or scale when CHERD is installed.

---

## 3. The fx packs: snowtrain, wagons (with BEIGNET), TUNE

The **fx** release (fx 1.4): three effect packs that work together (BEIGNET, beignet.pack in fx 1.2, is in wagons
18; upgrading: delete beignet.pack), on Faust's stock open-field and on ours. GATE,
FREEZE and TUNE follow CHERD's chord when CHERD (section 2) is installed.

### 3.1 snowtrain: a light fx train

A train on each synth and drum sound: the **locomotive** is the sound (its name and engine), **wagon 1** is TE's own T3
effect, **wagons 2 to 4** are any pack effects on the unit (the wagons below, BEIGNET, TUNE, anyone's). The **4th knob
is wagon 4**: knob N always acts on the wagon drawn above it.

- **Open:** **T3** on a synth or drum screen (on TE's effect page too). **T3 on the train** shows TE's effect page;
  T1, T2, T4 close the train and go on to TE.
- **Turn** knob N: pick wagon N's effect by name (wagon 1: TE's list, written after the knob rests; wagons 2 to 4:
  none, then every pack effect). A pick that would take the chain over its cycle budget is refused: **FULL**, and the
  LOAD bar turns orange.
- **Click** knob N: wagon N's values page (four gauges, the effect's own words: GATE's 1/4 .. TRNC, JUNEAUX's I / II /
  I+II, TUNE's HARD / SMOOTH). On a values page the knobs set the values; a click or T3 goes back.
- **Hold** knob N (0.4 s): wagon on / off. **shift + hold**: start values. **shift + click**: random values.
- **shift + turn** (wagons 2 to 4): move the wagon along the train (the knob carries it for 0.6 s).
- **HELP** or **shift + T3**: presets, `user/pf/snowtrain/01.txt` .. `32.txt`. 1st knob turn moves, click loads (TE's
  effect too), shift + click saves (a full slot at the second press), HELP again goes back. Sixteen factory chains
  land on the first start: DUB WASH, CASSETTE, GATE PMP, CHOIR, TRIAD, SPACE, CRUSH, WIDE PAD, SLAP, FREEZE, DRY+TUNE,
  OCTAVES, RADIO, DRUM BUS, STUTTER, SURF. An effect not on the unit shows **NO PACK**.
- **Kept** with each sound (and its presets). Nothing to set in settings.
- **A wagon's word:** OFF, NO PACK (its pack is not on the unit), WAIT, **NO MEMORY** or **CPU OFF**. On Faust's stock
  base these last two stay until the unit restarts: **restart the unit** (the base keeps a memory record for every
  effect ever picked into a wagon, and its cycle guard does not switch an effect back on). snowtrain only asks for a new
  record once the knob has rested 0.7 s, so scrolling through names is free.
- **Tape tracks:** on the mixer, **shift + the Nth knob's click** opens track N's train (mixer key held: tracks 5-8).
  On a track's train **T1..T4** open track 1..4's train, and the key of the track shown again its partner 5..8 (T1 on
  track 1: track 5; again: track 1): shift + 1st click, then T1, is track 5 with no key held. Opened with keys held,
  the train stays up when they are let go (snowtrain 22). Four of TE's effects (delay, fazer, grid, phone, punch), the same keys, presets in `user/pf/snowtracks/`, kept with
  the tape; the mixer key goes back, then out. They need no 8 tracks, or our 8 tracks 13: with Faust's 8 tracks 11
  they are not offered (shift + click stays the unit's).
- **Not beside fx train:** both use the same two places in the firmware; the loader keeps fx train. Take one off.
- The base's install question (T1 / T2) and its options page show over the train; snowtrain comes back after.

### 3.2 wagons: seven effects in TE's lists

Seven effects in one pack (**wagons**: the six below and BEIGNET, 3.3), plus **TUNE** from tune.pack. They show up in TE's own effect lists (T3) for every synth sound, every drum sound and the master. They save with the sound, and TE's LFOs can move them. Each one shows its own face on T3, rides snowtrain's wagons by name, and on our fx train fork (19) shows its own wagon picture (Faust's fx train, 17 and 18, draws the TE effect it rides).

On Faust's fx train 18 (the one the install page gives now) these effects, and BEIGNET, play on a wagon, but a tap on that wagon opens nothing: fx train 18 opens no pack effect's page, by its own rule. Pick the effect as the sound's own (shift + T3) or on the master to use its face; snowtrain shows a values page for the wagon.

| Effect | 1st knob | 2nd knob | 3rd knob | 4th knob |
|---|---|---|---|---|
| **BOOST** (drive, rocket face) | drive | tone | level (to +12 dB) | mix |
| **GATE** (tempo-synced chopper) | depth | pattern: 1/4, 1/8, 1/16, 1/8t, stab, chrl, sync, trnc | length | smooth |
| **FREEZE** | hold | pitch | follow | smear |
| **TAPE** | wow | flutter | saturate | age |
| **JUNEAUX** (Juno chorus) | mode: I, II, I+II | mix | depth | tone |
| **ROTARY** (rotary speaker cabinet) | speed: brake, chorale, tremolo | drive | balance (drum to horn) | accel (the rotors' weight) |
| **TUNE** (tune.pack, 3.4) | tune | retune | harmony | blend |

To leave an effect page, press **T3**. The knob clicks do nothing on effect pages, as on TE's own.

**Limits.** Each effect stands in for one of TE's effects inside the firmware (BOOST: punch, GATE: nitro, FREEZE: grid, JUNEAUX and ROTARY: CWO, TAPE and TUNE: phone). It still appears under its own name.

### 3.3 BEIGNET: a mastering sweetener (wagons.pack)

**BEIGNET** (in wagons.pack since wagons 18; it was beignet.pack: delete that file when upgrading, sounds and presets keep working) is a mastering sweetener for the whole mix. On the mixer, open the master effect's list (T3) and pick `beignet`. It also shows in every synth and drum sound's list. Knobs: 1st GLUE (compressor), 2nd TONE (dark to bright tilt), 3rd WIDTH (mono to x2, the lows stay mono), 4th LOUD (drive and saturation). A -1 dBFS limiter is always on. **HELP** on its page opens the presets list, as on snowtrain: 1st knob turn moves, click loads, shift + click saves (twice over a full slot), HELP or T3 goes back. Files are `user/pf/beignet/NN.txt`, with nine factory presets: PLAIN, POWDERED, GOLDEN, CRISPY, PUFFY, LOFI, CLUB, DRUM BUS, EXTRA SUGAR. The face shows the preset's name top right, with `*` once you've turned a knob away from it. T3 switches it off and on, and the page flashes `FX OFF` / `FX ON`. Its face is a beignet: puffier with GLUE, a darker crust with TONE, wider with WIDTH, more sugar with LOUD. It rides punch.

### 3.4 TUNE: pitch correction (tune.pack)

**shift + HELP** in any mode opens the TUNE page. Plain HELP or shift + HELP closes it. Since tune 29, on the tape screen while markers.pack is there, shift + HELP is markers' (HELP + shift + key clears a marker): open TUNE from any other screen.

| Knob | Turn | Click |
|---|---|---|
| 1st | **TUNE**, 15 steps, shown as "bypass" then 7 % to 100 %; shift + turn: **KEY** (chromatic, C-B major, C-B minor) | - |
| 2nd | **RETUNE**: smooth / hard | - |
| 3rd | **HARMONY**: off, 3rd up, 3rd down, double, thirds, triad, octaves, choir | **SNAP**: AUTO, SCALE, KEY |
| 4th | **BLEND**, 7 steps, shown as 0 % to 100 % (harmony level) | **MONITOR** on / off |

- **SNAP** here is where the target notes come from (not CHERD's SNAP on its FEEL page). **AUTO** follows CHERD (its sounding chord, else its scale) when CHERD is installed. **SCALE** follows CHERD's scale only. **KEY** uses the page's own key. The page does not print AUTO / SCALE / KEY: its bottom line shows the result, "cherd chord", "cherd scale", a key's name or "chromatic". So without CHERD, or with no key set, a 3rd click can leave the line unchanged.
- The 1st and 2nd clicks do nothing on this page.
- **MONITOR** sends the tuned voice through the synth bus, so T3 and fx train play on it. It only works in synth mode, and it also turns TE's input on.
- It starts bypassed at power-on. Settings last for the session only.

**TUNE as an effect:** TUNE is also in TE's T3 lists. Its page shows these knobs, as TE's knobs move them. The bottom line then starts with "effect" and has no MONITOR (that belongs to the input).

---

## 4. lilith: a synth engine (engines 2)

**lilith** (lilith.pack) is a mono virtual-analog bass engine: two oscillators (saw to square; the second tunable, with
hard sync) into a four-pole ladder low-pass in the Moog style, with a decay envelope on the cutoff. **shift + T1** opens
TE's engine list: pick **lilith**. T1 then shows her animated face. Her own [manual](../packs/lilith/MANUAL.md) has every
detail.

| Knob | Turn | shift + turn |
|---|---|---|
| 1st | **cutoff** | **tune**: the second oscillator, an octave down to an octave up, unison in the middle |
| 2nd | **reso** | **mix**: first oscillator, both, second |
| 3rd | **eg amt**: how far each note opens the filter | **wave**: saw to square |
| 4th | **decay** of that envelope | **sync**: off (lower half), on (upper half) |

- **Sounds:** acid, bass, brass, funk bass, glide lead, prog lead, seq bass, squelch, sync, tortoise, in
  `user/synth_presets/lilith/`. A sound saved on lilith keeps her.
- TE's T2 (amplitude envelope) and T4 (LFO) work on her as on any engine. CHERD plays on her.
- **T3:** TE's T3 effect, snowtrain and fx train work on her directly (native, as TE's own engines). TE's velocity sets
  her loudness.

---

## 5. clarinet: a synth engine (engines 2)

**clarinet** (clarinet.pack) is a clarinet in TE's engine list: a physical model of the reed and the bore, not samples,
with an animated face and five sounds. **shift + T1** opens TE's engine list: pick **clarinet**. Its own
[manual](../packs/clarinet/MANUAL.md) has every detail.

| Knob | Turn | shift + turn |
|---|---|---|
| 1st | **BREATH**: how hard you blow, soft and woody to loud and buzzing | **NOISE**: breath noise and turbulence |
| 2nd | **BRIGHT**: dark to bright | **RATE**: vibrato speed |
| 3rd | **VIBRATO**: depth; it grows into long notes | **SCOOP**: the bend up into each tongued note |
| 4th | **REED**: the embouchure, loose to firm | **LEGATO**: OFF or SLUR |

- **Playing:** one voice, the last key wins. Overlapping keys with LEGATO on SLUR slur (a hole opens, no glide);
  detached keys are tongued. Velocity is how hard you blow. Long notes swell, and the vibrato comes in late.
- **Sounds:** ballad, chalumeau, creole, klezmer, swing, in `user/synth_presets/clarinet/`. A sound saved on the clarinet keeps it.
- **T3:** TE's T3 effect, snowtrain and fx train work on it directly (native). TE's pitch bend and glide move it hole
  by hole. CHERD plays on it (a chord sounds its last note).

---

## 6. boarder: an organ engine (engines 2)

**boarder** (boarder.pack) is an organ in TE's engine list: tonewheels and two combo-organ modes, six voices, twenty
sounds, and an organist on T1 who plays what you play. **shift + T1** opens TE's engine list: pick **boarder**. Its own
[manual](../packs/boarder/MANUAL.md) has every detail.

| Knob | Turn | shift + turn |
|---|---|---|
| 1st | **LOW**: the bass drawbars, 16' then 5 1/3' | **CLICK**: key click |
| 2nd | **MID**: 8', then 2 2/3', then 4' | **VIB**: OFF, V1 to V3 (vibrato), C1 to C3 (chorus) |
| 3rd | **HIGH**: 1 3/5', 1 1/3', 1', then 2' | **DRIVE**: the preamp, clean to driven |
| 4th | **PERC**: OFF, 3RD / 2ND, FAST / SLOW, NORM / SOFT; the strip reads `3F NORM` ... `2S SOFT` (boarder 19; in a combo mode: **TONE**, flute to reed) | **LEAK**, then **MODE**: COMBO 1, COMBO 2 |

- **The strip** at the bottom shows the four knobs in order: LOW, MID and HIGH as small drawbars (longer = further
  out; digits for about a second while you turn), PERC in words. With shift: CLICK, VIB, DRIVE, LEAK or MODE.
- **Playing:** six voices; the key is a switch (the organ stops within ~6 ms of letting go). Percussion is
  single-trigger: it sounds when no other key is down. Pitch bend does not bend.
- **Combo modes:** shift + the 4th knob past LEAK: COMBO 1, then COMBO 2. Equal-tempered, no percussion or leakage.
- **Sounds:** twenty, in `user/synth_presets/boarder/` (fifteen tonewheel; combo, fire, sixties on COMBO 1; garage, surf
  on COMBO 2).
- **T3:** the ROTARY wagon, TE's T3 effect, snowtrain and fx train work on it directly (native). CHERD plays on it.

---

## 7. recstart: sound starts the recording (recstart.pack)

Normally, with REC held and the tape stopped, TE starts recording on the first key. recstart lets **incoming sound**
start it too: good for an MPC, a drum machine or any gear on line in or USB.

1. Stop the tape and pick an audio track. Have a source on the input (recstart looks only at the input's level).
2. Set TE's **THRESHOLD** on the input screen (-24 to 0; -12 by default; the number x 2 is dBFS). recstart uses the
   same level, or its own (below).
3. Hold **REC**. **WAITING: INPUT** and the level it waits for (TE -24: TE's THRESHOLD in dBFS; -36 dB: its own) show in the top right corner of the tape screen. A key still starts the take,
   as on TE's own.
4. The first sound over the threshold starts the take: recstart presses PLAY for you, once per REC hold.

The flash goes when the take starts.

Settings (shift + COM, T1, PACKS, RECSTART): **auto start** on / off (off: REC behaves as stock) and **threshold**:
TE (the default: TE's THRESHOLD) or its own -60, -54, -48, -42, -36, -30 or -24 dBFS, quieter than TE's knob reaches.
The base keeps them; no files of its own.

---

## 8. seq: TE's sequencers, extended (seqx, seqbank)

### 8.1 seqx: probability, ratchet and length on PATTERN (seqx.pack)

On the **PATTERN** screen (synth or drum), put TE's cursor on a step (**1st turn**), hold the key of a note on that
step, and turn:

| Knob | Does |
|---|---|
| 2nd turn | **probability**: 100, 75, 50, 25 % (the note plays that often) |
| 3rd turn | **ratchet**: 1 to 4 hits in the step |
| 4th turn | **length**: 1 to 16 steps (TE's own notes are one step) |

Hold several keys and one turn changes all their notes on the step (a chord). With no key held, or no note of the held
key on the step, the knobs are TE's. Turn back to 100 %, X1, 1 to take the extras off; TE's erase (shift + key) takes
the note and its extras.

While a key is held a lane under TE's grid shows that key's 16 steps large (bars = hits, fill = chance, a line = how
long it sounds), the grid's dots are cut to their chance with a tick per hit, and the top band names the knobs: STEP
and key, PROB, RATCHET, LENGTH. The extras are saved in `user/pf/seqx/seqx.bin` and follow their pattern.

**CHERD CHORDS (seqx 5, with cherd 51 or later; in seq 1).** settings > PACKS > seqx > **CHERD CHORDS**
(seqx 5: off at first; seqx 6: on at first whenever CHERD is installed, and a choice you made stays). With it on, a synth note you enter on a PATTERN step becomes CHERD's chord on that root (CHERD's Key,
Scale, Flow, Spread and LOCKs as set), its other notes written into the step's own cells, so TE shows, plays and saves
them and seqbank keeps them. One chord a step; erase the root (shift + key) and the notes it brought go too. CHERD's
HELP + 3rd click (chapter 2, Chains; internal CHERD builds only) also needs seqx 5: it writes a chain as the synth PATTERN.

### 8.2 seqbank: banks of patterns (seqbank.pack)

On the **PATTERN**, **ENDLESS** or **FINGER** screen, **HELP** opens the bank. TE's help does not show there.

1. A list of 8 genres. **1st turn** picks one; **1st click** enters it.
2. 16 slots. **1st turn** loads the slot under the cursor at once, so you hear it if TE is playing. An empty slot brings
   back your pattern from before.
3. **1st click** keeps what is loaded and closes. **HELP** goes back to the genres and restores your pattern; **HELP**
   again on the genre list closes the bank.
4. **shift + 1st click** saves your pattern from before into the slot. An empty slot saves at once ("mine NN"). A full
   slot says "again to replace" and needs a second shift + click ("saved").

A mode key, or anything else that closes the page, brings your old pattern back. It reopens on the last genre and slot.
With CHERD installed, a synth pattern lands in CHERD's key; with seqx, a slot's extras come back with it.

**The banks:** six files (PATTERN, ENDLESS, FINGER, each synth and drum), 128 slots each, shared by every project. The
zip's folder `seqbank/` holds them: copy them into the unit's folder `seqbank` (it shows in disk mode once seqbank has
started; drive mode: `user/pf/seqbank/`). Without them each bank starts empty and fills with what you save.

---

## 9. vu: visualizers on the mixer (vu.pack and its looks)

vu paints the **master mix** (after the master effect, summed) on TE's mixer levels page. `vu.pack` is the host; each
look is a small pack of its own, so copy only the looks you want: the core looks are SUNDOWN, SPECTRUM, CLASSIC, LCD and
VU; CONSOLE, BELLA, ANDY, GOOD TIMES and SCOPE are optional extras. With no look pack a tap says NO LOOKS.

| Pack | Look |
| --- | --- |
| `vu_sundown.pack` | **SUNDOWN**: a synthwave sunset over mirrored mountains made of the bands (in vu_spectrum until version 5) |
| `vu_spectrum.pack` | **SPECTRUM**: an LED analyser, 32 bands, falling peaks |
| `vu_classic.pack` | **CLASSIC**: 64 thin bars with peak caps, or the wave as dots or lines |
| `vu_lcd.pack` | **LCD**: a backlit dot-matrix panel with the tape, the BPM and 30 bars |
| `vu_meter.pack` | **VU**: two needle meters with PEAK lamps |
| `vu_console.pack` (optional) | **CONSOLE**: a retro sci-fi computer panel: a rounded frame and colour blocks, pill bars, a radar sweep with blips, scrolling hex, readouts |
| `vu_bella.pack` (optional) | **BELLA**: MARY BELLE the cow dancing on a 90s car stereo's LED panel |
| `vu_andy.pack` (optional) | **ANDY**: an orange tabby in a red 26 jersey who does the Griddy, plops when it goes quiet, MEOWs |
| `vu_goodtimes.pack` (optional) | **GOOD TIMES**: a feedback picture kicked by the beats, four presets |
| `vu_scope.pack` (optional) | **SCOPE**: the wave, a goniometer and a phase bar on phosphor screens |

| Where | Gesture | Does |
| --- | --- | --- |
| mixer, levels page up | **tap the mixer key** (let go within 0.3 s) | the next installed look: OFF, SPECTRUM, SUNDOWN, CLASSIC, LCD, CONSOLE, GOOD TIMES, BELLA, ANDY, VU, SCOPE, OFF; the name shows small at the top left for 1 s |
| mixer, levels page up | hold the mixer key | TE's (and 8 tracks') own: a hold is never a tap |
| on a look | **1st..4th turn** | TE's master EQ: LOW, MID, HIGH, ALL (the three together); one thin line at the bottom shows the values, gone 1.5 s after the last turn |
| on a look, punch keys on | hold a white key | that punch effect (needs punch 3): its name small at the top left, no strip; turning its knobs shows the thin line of its four values |
| on a look | **shift + a key** | markers' cue as on the tape screen: a press cues, twice jumps, held loops; the marker's name flashes (needs markers 94+) |
| on a look | knob click | TE's levels page for 1.5 s, then the look again |
| settings > packs > vu | **EQ knobs** (on) | off: the knobs stay TE's volumes on a look |
| settings > packs > vu | **classic** (bars; on a base with option words) | CLASSIC as bars, dots or lines; NOT INSTALLED without vu_classic |
| settings > packs > vu | **punch keys** (off) | on: the white keys hold punch's effects on a look (punch 3 or later) |
| settings > packs > vu | **look** (on a base with option words) | the look by name, from the looks installed; a tap changes it too |

**look** and **classic** appear in settings on bases with option words (open-field PR #56, pending). On other bases,
open-field 0.24 (base 42) and older among them, those two rows don't show: the mixer key's tap switches
looks and CLASSIC draws bars; everything else is the same. The released `vu.pack` (vu 34) carries both rows.
Change the look with the mixer key's tap; the last look is kept in `user/pf/vu/look.txt` and comes back at the next
start. **The mixer key's tap does not clash with Faust's sidechain**, which uses shift + mixer.

**Next, vu 36 (in the sources, not in the vu 34 zip):** pick one look, the mixer key switches it. **HELP** on the
mixer's levels page opens a picker of every look installed (the 1st knob moves, a click picks that look and shows it,
HELP again closes; shift + HELP stays tune's). From then on a **tap of the mixer key goes OFF (TE's mixer) and back to
the picked look**: it no longer steps through the looks. Nothing picked yet: SUNDOWN (or the first look installed);
the picked look's pack removed: the first look installed. **look** in settings is the picked look (no OFF there).
On / OFF and the pick come back at the next start (`user/pf/vu/look.txt`). Holding the mixer key, the EQ knobs, punch
keys and markers' cue are as above.

TE's mixer still works: T1..T4, shift + T1..T4 (mutes), holding the mixer key, shift + a knob click. vu stands back for
TE's popups, any pack's page and the base's top page. With OFF you get TE's mixer (or lanes') as before. To drop a
look, delete its pack.

---

## 10. tape views: the tape screen (tape views 1)

Eight packs for the tape screen, built to be taken in steps: **lanes** alone (waveforms, zoom, tall lanes, TE's look);
**+ markers + perform and punch** (sections, the PERFORM face, punch-in effects); **+ themes and one look** (the full
look); **miditracks** (MIDI tracks) on its own or with any of them. perform needs markers, a look needs themes. Everything
here is on the **tape screen** unless it says otherwise. Settings: shift + COM, the PACKS row, the pack.

### 10.1 lanes: waveforms, the height zoom and tall lanes (lanes.pack)

- **Waveform:** settings > PACKS > lanes > **waveform** on. Clips show their level a column, inside TE's clip bars (or
  in the look, with themes). Only what the tape has played since the switch is known; the rest is a dotted middle line
  until it plays. Kept per tape after that.
- **wave fill** on: with the tape stopped the rest of the tape is read in the background (about 80 s for 2 minutes of tape).
- **HELP + 4th turn:** 8 / 4 / 2 / 1 tracks; the page follows the selected track (TE's track keys scroll it). Flash:
  `LANES 8`, `LANES 5-8`, `LANE 6`.
- **tall lanes** (settings > PACKS > lanes, off at first; lanes 93, with markers since lanes 94, the deck in the centre since lanes 98): on TE's own tape screen TE's header stays, its
  ruler moves up under it and the lanes fill the screen below (8 tracks: about 15 px a lane instead of 5), with the
  waveform and MIDI notes; TE's whole deck, small, sits in the centre over the play-head, TE's timecode top right. HELP + 4th turn then runs tall 8 / 4 / 2 / 1,
  `TAPE` (TE's screen with its 8 rows), `TAPE 1-4` / `TAPE 5-8`. Off while a theme paints the tape screen. With markers.pack
  installed (markers 96) its flags hang above the moved ruler.
- On TE's own screen a clip narrower than about 8 px may show no waveform.

### 10.2 markers: sections on the tape (markers.pack)

Up to 16 markers a tape, one a keyboard key, kept in the tape.

- **Set:** HELP + a key, at the play-head, snapped to the beat. A key that has one is not moved (`A IS VERSE 5.1`);
  a beat that holds one is refused (`TAKEN: INTRO`). With 16 set: `MARKERS FULL`.
- **Name:** keep HELP held and turn the 1st knob: INTRO, VERSE, PRE, CHORUS, BRIDGE, BREAK, BUILD, DROP, SOLO, OUTRO, or
  a letter. HELP + 1st turn alone renames the section under the play-head.
- **Clear:** HELP + shift + key (`A CLEARED`). To move a marker: clear it, set it again.
- **Play:** shift + a marked key cues it (`A CUED`): the tape goes there when the section ends, without a gap; stopped,
  at once. Twice within 0.3 s: jump now. Held 0.5 s: loop that section (hold again inside it to release). From any
  screen: hold TAPE + the key.
- **Move:** HELP + left / right arrow: previous / next marker. HELP + 2nd turn: bars across the screen.
- **Arrange** (tape stopped, HELP held throughout): 3rd click picks the section, 3rd turn moves it, 3rd click commits.
  This moves audio on the tape; one TE undo takes it back. Try it on a copy of a tape first.

### 10.3 perform: the PERFORM face and the song (perform.pack, needs markers)

- **4th click** (no shift, no HELP): tape screen <-> PERFORM. Kept after a restart. With the theme off you get
  perform's plain face; with a look, the look draws it in full.
- The rows are the markers in tape order: name, bar, length. The playing part: a solid triangle, its bar filling up. The
  cued one: a hollow triangle and `IN bars.beats`. Played parts are dim.
- **The song:** up to 8 rows, each a section, played x1..x8, HOLD or SKIP, for its own length or a number of bars; an
  END row (STOP, LOOP, ON). While the face is PERFORM the song plays, on any screen; a tape nobody arranged plays as it lies.
  A cue (shift + key, a program change) still works: the song carries on from there.
- **EDIT:** hold HELP (HELP + 4th click keeps it; the 4th click or a HELP tap closes it).

| Gesture | Does |
| --- | --- |
| 1st turn / click | PICK a row / CUE it (twice quickly: now) |
| 2nd turn / click | MOVE the row / COPY it under itself |
| shift + 2nd click | OUT: remove the row |
| 3rd turn / click | TIMES: SKIP, x1..x8, HOLD (END: STOP, LOOP, ON) / X2 |
| 4th turn | BARS: a bar shorter / longer than the section |
| a marked key | ADD its section under the cursor (`SONG FULL` at 8) |
| TE's undo / redo | each edit is one step of TE's undo |

### 10.4 punch: punch-in effects (punch.pack)

On the PERFORM face, hold one of the **14 white keys from the lowest F**: LP, HP, JET, CRUSH, GATE, RISE, DUB, VERB,
STUTR, GLITCH, DIVE, PUMP, ISO, SCRATCH. Up to 4 at once (a 5th shows FULL). While a key is held, the 1st..4th knobs set
its four values (1st where / time, 2nd character, 3rd shape, 4th depth; ISO: LOW, MID, HIGH, crossover); the last key
pressed owns them; kept per tape. Program changes 25-32 / 57-62 hold, 49-56 / 65-70 release, while the face is up. The
effects go to the speaker and outputs, not to a tape recording. While EDIT is open the keys are not effects.

### 10.5 themes and the looks (themes.pack + theme_89mph.pack / theme_console.pack)

- **Faust's stock base (42):** no setting; the look is on whenever installed: install one look only.
  **A base with Faust's open-field pull requests #55 / #56 (ours, 43h):** settings > PACKS > themes > **theme**: off /
  89MPH / CONSOLE (only the looks installed are listed).
- TE's count-in shows in the look while it counts (`COUNT 3`).
- **89MPH:** segment readouts (the section's name, bar.beat, time), lamps PLAY / LOOP / CUE, a status line with where
  the tape goes next, dot-matrix lanes; the PERFORM face as a head unit; and **TE's mixer** levels page in the same look
  (meters with held peaks, pan, volume, MUTE).
- **CONSOLE:** an elbow header, pill lanes, a cue countdown (`> BRIDGE IN 3.2`), a set-list face. The mixer stays TE's.
- The word at the right edge says what the 4th click does: `4TH: PERFORM` / `4TH: LANES`. A look steps back for TE's
  dialogs; engines, sequencers and CHERD are never drawn over. 89MPH costs the most processor time.

### 10.6 miditracks: MIDI tracks on the tape (miditracks.pack)

- **shift + 4th click:** the selected track AUDIO <-> MIDI (`T2 CH1 SYNTH`).
- **REC held** on a MIDI track, play keys or MIDI in: notes are recorded. Without REC you only audition.
- **shift + 1st click:** the insert browser (needs seqbank 20, seq 20: section 8.2): genres, slots, NOW / MIDI FILES. **3rd knob** =
  MIDI channel, **4th knob** = output: **MIDI** (out only), **SYNTH**, **DRUM**, **BOTH** (synth and MIDI out), **PUNCH**.
  A click on a slot inserts it (tape stopped). **shift + 2nd click:** the last pick again. Without seqbank: on a MIDI
  track shift + 1st / 2nd turn set channel / output.
- **shift + 3rd click twice within 1.5 s:** clear the whole MIDI track (tape stopped).
- Mute, LIFT / DROP and TE's undo work as on audio. PATTERN screen, **shift + 4th click:** EDIT the track's bar in TE's
  grid (again: write it back; shift + 4th turn: next bar).
- **PUNCH output:** the track's notes hold punch's effects while the tape plays (a look draws them as named blocks). To
  record one: select it, go to the PERFORM face, hold REC and play the effect keys.

### 10.7 On a base without option words and files per tape (open-field 0.24 and older)

- **No theme setting:** the look is on whenever a look pack is installed (no theme words there): install one look.
- **Files kept per tape don't follow TE's copy and delete:** the stock base doesn't copy or remove
  `user/pf/miditracks/tape<N>.mtk` (nor lanes' `user/pf/lanes/`). miditracks copies the notes itself when the original
  tape was loaded once with it installed (a tape copied before that starts empty); a deleted tape's file stays until a
  new tape takes its number. markers, perform and punch keep their data inside the tape and follow on any base.
- With Faust's 8 tracks: tracks 5-8 show in the lanes but may look unmuted, a MIDI track on 5-8 can't be muted, and the
  89MPH mixer shows tracks 1-4.

Little time on a unit so far: the song's EDIT (partly passed), PUNCH lanes (partly passed), the 89MPH mixer.

---

## 11. Notes

- **Where files live:** everything of ours is under `user/pf/<pack>/`, visible in disk mode.
- Not yet tried on the unit: wagon pictures in fx train 18+.
