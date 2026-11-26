# Third-party notices

The packs are MIT ([LICENSE](LICENSE)), 2026 hasis, except for the parts below built into them, which keep their own
licences.

| Part | In | Licence |
| --- | --- | --- |
| **Field Sans**, glyphs made from Petaluma Script, © 2018 Steinberg Media Technologies GmbH, Reserved Font Name "Petaluma" (a Modified Version, renamed as the OFL asks) | `cherd.pack` (its chord names) | SIL Open Font License 1.1, [OFL.txt](OFL.txt) |
| OP-XY SDK headers (integer types, fixed-point helpers), Open-XY contributors | `cherd.pack`, `tune.pack`, `lilith.pack` | MIT, [licenses/open-xy.txt](licenses/open-xy.txt) |
| The pitch tracking and correction of TUNE (`tuner.hpp`), from the Auto Tune extension by **Kristaps Dreija** in [xy-machines](https://github.com/kristapskristaps/xy-machines) (release tag `autotune-v0.2.0`): the sound of TUNE | `tune.pack` | MIT, [licenses/xy-machines.txt](licenses/xy-machines.txt) |

**Published science, no code.** The clarinet's reed and bore follow the model published by Ph. Guillemain, J. Kergomard and Th. Voinier, "Real-time synthesis of clarinet-like instruments using digital impedance
models", J. Acoust. Soc. Am. 118 (1), 2005.
The code is hasis's own, written from the paper's equations; no code was taken from the paper's authors or from any other
synthesizer. clarinet.pack holds no third-party code.

**Published descriptions, no code.** boarder is written from published descriptions of how tonewheel organs and
transistor combo organs work, inspired by setBfree's published design. The code, tables and sounds are hasis's own;
no code was taken from any organ, emulation or open-source organ project (setBfree's included); boarder.pack holds no third-party code.

**Published science, no code.** ROTARY (in wagons.pack) follows published descriptions of the rotary speaker cabinet
(J. Smith, S. Serafin, J. Abel and D. Berners, DAFx 2002, on Doppler simulation of rotary speakers). The code is hasis's own;
no code was taken from the paper's authors or from any other effect.

**open-field.** Every pack is a pack for [open-field](https://github.com/LaP0573/open-field) by Faust (LaP0573): its
base, loader, pack format and build tools make these packs possible (MIT). The packs here were built with its stock
tools (vu.pack, lanes.pack, themes.pack and miditracks.pack with our fork of them at base 34, which adds
the look and theme lists by name and files per tape; on Faust's stock base those asks are left aside).

**Not included.** No Teenage Engineering firmware, firmware bytes or unit files are in these packs or this repository.

**Whose work this is.** Every pack here was written by hasis: the effects (snowtrain, the wagons BOOST, GATE, FREEZE,
TAPE, JUNEAUX and ROTARY, BEIGNET, TUNE's page and harmonies), the engines (lilith, the clarinet, boarder), CHERD,
recstart, seqx and seqbank (and the patterns in seqbank's banks, written for it; no copied melodies), the tape views (lanes, themes and its looks 89MPH and CONSOLE, perform, punch, markers, miditracks;
the punch-in effects and the looks' art are our own, no code taken from any effect, DJ mixer or console), vu and its
looks (the characters BELLA and ANDY, the looks' art and the old desktop players' looks are our own riffs: no names,
logos, skins or assets of theirs). lilith, Oberon and
CHERD's chord rules started as hasis's own OP-XY machines (in hasis's own fork of open-xy, MIT; never part of open-xy itself) and
were ported to the Field by hasis. The only parts by others are the ones in the table above.
