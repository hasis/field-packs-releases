# OP-1 Field: Player's Guide to field-packs

Everything the released packs add to the OP-1 Field, and how to play them: OS 1.7.3+0 with Faust's open-field. **fx 1.1** (snowtrain, wagons, BEIGNET, TUNE) is section 3; **CHERD 37**, its own release with its own [manual](../packs/cherd/MANUAL.md), is section 2. Where a feature needs one of our forks of Faust's platform packs (fx train 18+, 8 tracks 13), the text says so; everything else runs on Faust's stock open-field. Pack versions: the [README](../README.md). Gestures were checked against each pack's input code (flash words are quoted as the code prints them).

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
| shift + HELP | the TUNE page (shift + HELP or plain HELP closes it) | tune |
| HELP at power-on | safe start: no packs load | base |

### Synth screens
| Gesture | Does | Pack |
|---|---|---|
| T3 list | BOOST, GATE, FREEZE, TAPE, JUNEAUX, TUNE, BEIGNET | wagons, tune, beignet |
| T3 | the train: TE's effect and three pack effects as wagons (knob N = wagon N) | snowtrain |
| HELP on the train | snowtrain's presets | snowtrain |
| sequencer list | CHERD | cherd |

### CHERD page
| Gesture | Does |
|---|---|
| left octave keys (F..E) | chord flavors (silent) |
| right octave keys | roots: each key plays a chord |
| 1st..4th turn | Key, Scale, Spread, Flow |
| 1st click | FEEL page on / off |
| 2nd click | strum: off, up, down, alt (on FEEL: SNAP grid) |
| 3rd click | comp on / off |
| 4th click | arp on / off |
| shift held | ARP page; shift + 4th click keeps it open |
| HELP | one step back: the latched ARP page, then FEEL |

---

## 1. Install, safe start, logs

**Install** open-field 0.12 first, with its install page ([open-field](https://github.com/LaP0573/open-field), `docs/guide.md`). Then take the packs you want:

- **With the install page's packs section**, once these packs are in its catalog.
- **fx 1.1 / CHERD 37:** download `fx-1.1.zip` or `cherd-37.zip` from the repository's Releases, unzip, and copy the `.pack` files from its `packs/` folder. Coming from fx 1.0: delete `autotune.pack` (TUNE is `tune.pack` now; with both there the loader keeps `autotune.pack` and leaves `tune.pack` out).
- **By hand:** put the unit into disk mode, copy the `.pack` files (from the release zip, or built) into the folder `packs`, leave disk mode, switch the unit off and on. In the bootloader's drive mode the folder is `user/pk`. To take a pack away, delete its file there.

**Safe start.** Hold **HELP** while you power on. No packs load. Use this when a pack stops the unit from starting; the disk mode still shows the folder `packs`, so you can delete or replace the file.

**Logs.** Every pack writes to TE's log (`/logs` on the unit, read over dev-mode MTP).

---

## 2. CHERD: chords from one key

CHERD is a sequencer. With it on, every key plays a full chord from the key and scale you set. It is its own release (`cherd-37.zip`). The full manual, chords, flows, scales and all: [packs/cherd/MANUAL.md](../packs/cherd/MANUAL.md); one-page quick start: [CHERD-quickstart.pdf](CHERD-quickstart.pdf). This chapter is the short version.

**Turn it on.** In synth mode, open the sequencer list (shift + the sequencer key). CHERD is the eighth entry. Switching the sequencer off keeps CHERD's page.

**The keyboard.**

- **Left octave (F to E): flavors.** These are silent. Hold one or more while you play a root.
  F add6, F# dim, G sus2, G# minor, A sus4, A# major, B add9, C 9th, C# ALT, D 7th, D# dom7, E Spice.
  A quality (major, minor, dim, sus2, sus4) is one key, the latest held. Extensions add up.
  A flavor held when you strike a root stays with that chord until you let go of the root. A flavor pressed after the strike only lasts while you hold it (tap sus4, let go to resolve).
- **Right octave: roots.** Each key plays its chord.
- **Octave arrows** work over a held chord.
- **Recording.** With **REC** held, the flavor keys go to CHERD only. Only a root starts the tape.

**Main page knobs.**

| Knob | Turn | Click |
|---|---|---|
| 1st | **Key** (circle of fifths) | FEEL page on / off |
| 2nd | **Scale**: off, major, minor, dorian, mixolydian, lydian, phrygian, locrian, harmonic, melodic, and 25 more (the screen shortens them: dor, mixo, lyd, phr, loc, harm, mel) | **Strum**: off, up, down, alt |
| 3rd | **Spread**: close, open, wide, bass, lead (lead = single notes) | **Comp** on / off |
| 4th | **Flow**: off, color, jazz, pop, soul, gospel (gosp), bossa, ambient (amb), blues, rock, monk, django | **Arp** on / off |

Chord names show in fakebook style (Field Sans, from Petaluma Script). The font is inside cherd.pack (cherd 37): nothing to copy.

**FEEL page (1st click).** The knobs become Smooth (voice leading), Swing (even, swing, triplet), Human (tight, loose, drunk) and the comp pattern (stab, chrl, pump, sync, pompe; *pompe* is gypsy-jazz la pompe). The 2nd click on FEEL cycles **SNAP**: OFF, 1/16, 1/8, 1/4, 1/32, 1/8T, 1/16T. (While the tape records, the chords wait for the next grid line.)

**ARP page.** Hold **shift** on the CHERD page. The knobs become mode (up, down, up-down, random), rate (1/4, 1/8, 1/8T, 1/16, 1/16T, 1/32), gate (10-100 %) and octaves (1-3). **shift + 4th click** keeps the ARP page open, so you can play with both hands; shift + 4th click again lets it go. While the ARP page is up, the 1st click only closes it. The 2nd and 3rd clicks stay strum and comp on the ARP page (the 2nd is SNAP if the FEEL page is under it).

**HELP** steps back: first the kept ARP page, then the FEEL page. On the main page HELP is TE's own.

**Saved:** `user/pf/cherd/cherd.bin`. Key, scale, flow and smooth are shared by all synth slots. Spread, strum, comp, arp and feel are per slot.

**Works with:** GATE, FREEZE and TUNE follow CHERD's chord or scale when CHERD is installed.

---

## 3. The fx packs: snowtrain, wagons, BEIGNET, TUNE

The **fx** release (fx 1.1): four effect packs that work together, on Faust's stock open-field and on ours. GATE,
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
- **Tape tracks:** on the mixer, **shift + the Nth knob's click** opens track N's train (mixer key held: tracks 5-8);
  four of TE's effects (delay, fazer, grid, phone, punch), the same keys, presets in `user/pf/snowtracks/`, kept with
  the tape; the mixer key goes back, then out. They need no 8 tracks, or our 8 tracks 13: with Faust's 8 tracks 11
  they are not offered (shift + click stays the unit's).
- **Not beside fx train:** both use the same two places in the firmware; the loader keeps fx train. Take one off.
- The base's install question (T1 / T2) and its options page show over the train; snowtrain comes back after.

### 3.2 wagons: five effects in TE's lists

Five effects in one pack (**wagons**), plus **TUNE** from tune.pack. They show up in TE's own effect lists (T3) for every synth sound, every drum sound and the master. They save with the sound, and TE's LFOs can move them. Each one shows its own face on T3, rides snowtrain's wagons by name, and on fx train 18+ shows its own wagon picture (Faust's fx train 17 draws the TE effect it rides).

| Effect | 1st knob | 2nd knob | 3rd knob | 4th knob |
|---|---|---|---|---|
| **BOOST** (drive, rocket face) | drive | tone | level (to +12 dB) | mix |
| **GATE** (tempo-synced chopper) | depth | pattern: 1/4, 1/8, 1/16, 1/8t, stab, chrl, sync, trnc | length | smooth |
| **FREEZE** | hold | pitch | follow | smear |
| **TAPE** | wow | flutter | saturate | age |
| **JUNEAUX** (Juno chorus) | mode: I, II, I+II | mix | depth | tone |
| **TUNE** (tune.pack, 3.4) | tune | retune | harmony | blend |

To leave an effect page, press **T3**. The knob clicks do nothing on effect pages, as on TE's own.

**Limits.** Each effect stands in for one of TE's effects inside the firmware (BOOST: punch, GATE: nitro, FREEZE: grid, JUNEAUX: CWO, TAPE and TUNE: phone). It still appears under its own name.

### 3.3 BEIGNET: a mastering sweetener (beignet.pack)

**BEIGNET** (beignet.pack) is a mastering sweetener for the whole mix. On the mixer, open the master effect's list (T3) and pick `beignet`. It also shows in every synth and drum sound's list. Knobs: 1st GLUE (compressor), 2nd TONE (dark to bright tilt), 3rd WIDTH (mono to x2, the lows stay mono), 4th LOUD (drive and saturation). A -1 dBFS limiter is always on. **HELP** on its page opens the presets list, as on snowtrain: 1st knob turn moves, click loads, shift + click saves (twice over a full slot), HELP or T3 goes back. Files are `user/pf/beignet/NN.txt`, with nine factory presets: PLAIN, POWDERED, GOLDEN, CRISPY, PUFFY, LOFI, CLUB, DRUM BUS, EXTRA SUGAR. The face shows the preset's name top right, with `*` once you've turned a knob away from it. T3 switches it off and on, and the page flashes `FX OFF` / `FX ON`. Its face is a beignet: puffier with GLUE, a darker crust with TONE, wider with WIDTH, more sugar with LOUD. It rides punch.

### 3.4 TUNE: pitch correction (tune.pack)

**shift + HELP** in any mode opens the TUNE page. Plain HELP or shift + HELP closes it.

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

## 4. Notes

- **Where files live:** everything of ours is under `user/pf/<pack>/`, visible in disk mode.
- Not yet tried on the unit: wagon pictures in fx train 18+.
