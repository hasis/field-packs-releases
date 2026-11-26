# field-packs releases

Packs for the **OP-1 Field** on **OS 1.7.3+0** with Faust's [open-field](https://github.com/LaP0573/open-field), by
hasis. This repository holds the released pack files only (no sources). Four releases:

## fx 1.3: three effect packs

| Pack | What it does | Version |
| --- | --- | --- |
| [snowtrain](packs/snowtrain/README.md) | A light fx train: on each synth and drum sound, TE's T3 effect plus three pack effects as wagons; trains on tape tracks too. Presets. A click on a pack effect's wagon opens its values page. | 20 |
| [wagons](packs/wagons/README.md) | Seven effects in TE's own effect lists: BOOST, GATE, FREEZE, TAPE, JUNEAUX, ROTARY (a rotary speaker cabinet) and BEIGNET (a mastering sweetener: glue, tone, width, loud, a -1 dBFS limiter; presets). | 18 |
| [TUNE](packs/tune/README.md) (`tune.pack`) | Pitch correction on the live input (shift + HELP) with harmonies, and a TUNE effect. | 29 |

Upgrading from fx 1.2: copy `wagons.pack` and delete `beignet.pack` (BEIGNET now lives in wagons; saved sounds and presets keep working).

GATE, FREEZE and TUNE follow CHERD's chord when CHERD is installed.

| snowtrain | |
| --- | --- |
| ![the train](docs/screens/snowtrain-train.png) | ![a wagon's values](docs/screens/snowtrain-values.png) |
| ![presets](docs/screens/snowtrain-presets.png) | |

| BEIGNET (in wagons) | TUNE |
| --- | --- |
| ![BEIGNET on the master](docs/screens/beignet.png) | ![TUNE](docs/screens/tune.png) |
| ![BEIGNET's presets](docs/screens/beignet-presets.png) | |

| wagons | |
| --- | --- |
| ![GATE](docs/screens/gate.png) | ![TAPE](docs/screens/tape.png) |
| ![JUNEAUX](docs/screens/juneaux.png) | |

Screens captured on an OP-1 Field.

## CHERD 57: the chord sequencer

[CHERD](packs/cherd/README.md) (`cherd.pack`, version 57; CHERD 37 was the release before): chords from one key, a
sequencer in the synth's sequencer list, with flavors, strum, comp, arp and a FEEL page. New since 37: **NEXT** (under
the chord's name, the likeliest next chords, by name, ranked on the key picture), fakebook spelling, and **LOCK** (HELP
held + a flavor key locks that flavor onto every chord). Chains are not in this release (coming in a later one). **[The CHERD manual](packs/cherd/MANUAL.md)**; a one-page
[quick start](docs/CHERD-quickstart.pdf). The chord font (Field Sans) is inside the pack: nothing else to copy.

| | |
| --- | --- |
| ![CHERD](docs/screens/cherd.png) | ![CHERD, another flavor](docs/screens/cherd2.png) |

## recstart 13: sound starts the recording

[recstart](packs/recstart/README.md) (`recstart.pack`, version 13): with REC held on a stopped tape, TE starts the take
on the first key; recstart starts it on the first **sound** over TE's input THRESHOLD too. For an MPC, a drum machine or
any gear on line in or USB: hold REC, start your gear, and the take begins with its first sound. While it waits,
WAITING: INPUT shows in the top right corner of the tape screen, with the level. Settings > PACKS > RECSTART: auto start
on / off, threshold TE or -60 to -24 dBFS. No files of its own; a one-page [quick start](docs/recstart-quickstart.pdf).

## engines 2: lilith, the clarinet and boarder, synth engines

Three engines in the unit's engine list (shift + T1), **native**: they render in the unit's own voices through
open-field's engine interface, so TE's T3 effect, snowtrain and fx train apply to them directly, as to TE's own engines.
TE's velocity sets lilith's loudness; TE's pitch bend and glide move the clarinet hole by hole. Saved sounds keep working.

| Pack | What it does | Version |
| --- | --- | --- |
| [lilith](packs/lilith/README.md) | A mono virtual-analog bass engine: two oscillators into a Moog-style ladder filter with its own decay envelope, an animated face, ten sounds. [Manual](packs/lilith/MANUAL.md), [quick start](docs/lilith-quickstart.pdf). | 16 |
| [clarinet](packs/clarinet/README.md) | A clarinet: a physical model of the reed and the bore, not samples, an animated face, five sounds. One voice; long notes breathe, slurs change holes. [Manual](packs/clarinet/MANUAL.md), [quick start](docs/clarinet-quickstart.pdf). | 16 |
| [boarder](packs/boarder/README.md) | An organ, six voices: tonewheels (nine drawbars, percussion, key click, scanner vibrato and chorus, a driven preamp) and two combo-organ modes; twenty sounds and an organist on T1. Made for the ROTARY wagon. [Manual](packs/boarder/MANUAL.md), [quick start](docs/boarder-quickstart.pdf). | 22 |

The engines sit at TE's own engine level; the clarinet's and boarder's sounds have a raised volume. Sounds an earlier
version wrote into `user/synth_presets/<engine>/` stay as they were: delete that folder before you restart to get these.
**synthbus is no longer needed:** if `synthbus.pack` is on your unit, delete it.

| lilith | clarinet | boarder |
| --- | --- | --- |
| ![lilith's face](docs/screenshots/lilith-face.png) | ![the clarinet's face](docs/screenshots/clarinet-face.png) | ![boarder's face](docs/screenshots/boarder-face-chord.png) |

## Experimental: lanes 87 (pre-release)

Waveforms and a vertical zoom on the Field's own tape screen: `waveform` on in settings > PACKS > LANES, then hold
**HELP** and turn the **4th knob** for 8 / 4 / 2 / 1 lanes. Optional: `markers.pack` + `perform.pack` (attached too) add a
plain PERFORM page (parts list, cues, countdown) on the 4th click. Not yet: punch-ins and the 89MPH / CONSOLE looks. Download it from the
[lanes 87 pre-release](https://github.com/hasis/field-packs-releases/releases/tag/lanes-87-experimental), and please
[open an issue](https://github.com/hasis/field-packs-releases/issues/new) with anything odd: what you did, a photo of
the screen, your open-field version and other packs.

## Install

1. **Requirements:** an OP-1 Field on **OS 1.7.3+0** (not 1.7.3+1) with open-field installed by Faust's install page
   (it puts the loader and `base.pack` on the unit; open-field's `docs/guide.md`). Nothing else.
2. Download `fx-1.3.zip`, `cherd-57.zip`, `recstart-13.zip` and / or `engines-2.zip` from this repository's **Releases** and unzip it (check the files
   against `SHA256SUMS` if you like). Or take the `.pack` files from [`packs/`](packs) here.
3. Put the unit into disk mode and copy the `.pack` files into the unit's folder **`packs`** (in the bootloader's drive
   mode: `user/pk`). Take only the ones you want.
4. Leave disk mode and switch the unit off and on.

Or, once the packs are listed there, tick them on Faust's install page ([catalog.json](catalog.json) holds the entries).
**If something goes wrong:** hold **HELP** while you switch the unit on and no pack loads; then delete the file that
misbehaves. **snowtrain and fx train cannot run together:** take fx train off, or the loader keeps fx train and leaves
snowtrain out.

How to play them: **[the Player's Guide](docs/PLAYERS-GUIDE.md)** and each pack's README.

**Support:** this repository's Discussions (questions, sounds, presets) and Issues (bugs).

**Unofficial.** Not made, endorsed or supported by Teenage Engineering, and not affiliated with them ([NOTICE](NOTICE)).
**At your own risk:** open-field changes your unit's firmware (see its guide). **A pack is a program that can read and
write the files on your unit: take packs only from people you trust.**

## Licence

MIT, [LICENSE](LICENSE), 2026 hasis. Third-party parts keep their own licences: [THIRD-PARTY.md](THIRD-PARTY.md)
(Field Sans inside cherd.pack, OFL: [OFL.txt](OFL.txt); the clarinet's and boarder's published sources). Not affiliated with Moog Music: "Moog-style" names a filter style only. History: [CHANGELOG.md](CHANGELOG.md).
