# field-packs releases

Packs for the **OP-1 Field** on **OS 1.7.3+0** with Faust's [open-field](https://github.com/LaP0573/open-field), by
hasis. This repository holds the released pack files only (no sources). Two releases:

## fx 1.1: four effect packs

| Pack | What it does | Version |
| --- | --- | --- |
| [snowtrain](packs/snowtrain/README.md) | A light fx train: on each synth and drum sound, TE's T3 effect plus three pack effects as wagons; trains on tape tracks too. Presets. | 17 |
| [wagons](packs/wagons/README.md) | Five effects in TE's own effect lists: BOOST, GATE, FREEZE, TAPE, JUNEAUX. | 13 |
| [beignet](packs/beignet/README.md) | BEIGNET, a mastering sweetener for the master slot: glue, tone, width, loud, a -1 dBFS limiter; presets. | 2 |
| [TUNE](packs/tune/README.md) (`tune.pack`) | Pitch correction on the live input (shift + HELP) with harmonies, and a TUNE effect. | 28 |

GATE, FREEZE and TUNE follow CHERD's chord when CHERD is installed.

| snowtrain | |
| --- | --- |
| ![the train](docs/screens/snowtrain-train.png) | ![a wagon's values](docs/screens/snowtrain-values.png) |
| ![presets](docs/screens/snowtrain-presets.png) | |

| beignet | TUNE |
| --- | --- |
| ![BEIGNET on the master](docs/screens/beignet.png) | ![TUNE](docs/screens/tune.png) |
| ![BEIGNET's presets](docs/screens/beignet-presets.png) | |

| wagons | |
| --- | --- |
| ![GATE](docs/screens/gate.png) | ![TAPE](docs/screens/tape.png) |
| ![JUNEAUX](docs/screens/juneaux.png) | |

Screens captured on an OP-1 Field.

## CHERD 37: the chord sequencer

[CHERD](packs/cherd/README.md) (`cherd.pack`, version 37): chords from one key, a sequencer in the synth's sequencer
list, with flavors, strum, comp, arp and a FEEL page. **[The CHERD manual](packs/cherd/MANUAL.md)**; a one-page
[quick start](docs/CHERD-quickstart.pdf). The chord font (Field Sans) is inside the pack: nothing else to copy.

| | |
| --- | --- |
| ![CHERD](docs/screens/cherd.png) | ![CHERD, another flavor](docs/screens/cherd2.png) |

## Experimental: lanes 87 (pre-release)

Waveforms and a vertical zoom on the Field's own tape screen: `waveform` on in settings > PACKS > LANES, then hold
**HELP** and turn the **4th knob** for 8 / 4 / 2 / 1 lanes. Not in it: the PERFORM face and the 89MPH / CONSOLE looks
(separate packs, later). Download it from the
[lanes 87 pre-release](https://github.com/hasis/field-packs-releases/releases/tag/lanes-87-experimental), and please
[open an issue](https://github.com/hasis/field-packs-releases/issues/new) with anything odd: what you did, a photo of
the screen, your open-field version and other packs.

## Install

1. **Requirements:** an OP-1 Field on **OS 1.7.3+0** (not 1.7.3+1) with open-field installed by Faust's install page
   (it puts the loader and `base.pack` on the unit; open-field's `docs/guide.md`). Nothing else.
2. Download `fx-1.1.zip` and / or `cherd-37.zip` from this repository's **Releases** and unzip it (check the files
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
(Field Sans inside cherd.pack, OFL: [OFL.txt](OFL.txt)). History: [CHANGELOG.md](CHANGELOG.md).
