# Changelog

## vu 36, 2026-11-27

`vu-36.zip`: only `vu.pack` is new (34 -> 36; vu 35 was never released), the looks are vu 34's files. **HELP** on the
mixer's levels page opens a picker of the looks installed (1st knob moves, a click picks, HELP closes; shift + HELP
stays TUNE's). A **tap of the mixer key** now turns the picked look on and off (OFF = TE's own mixer) instead of
stepping through the looks. Nothing picked yet: SUNDOWN or the first look installed; the picked look's pack removed:
the first look installed. On / OFF and the pick come back at the next start (`user/pf/vu/look.txt`, every base); on a
base with option words, settings > packs > vu > look is the picked look. Upgrade: copy `vu.pack` over the old one.

## tape views 1, 2026-11-27

The tape screen, in `tape-views-1.zip`: **lanes 98** (waveforms, a height zoom and, new, **tall lanes** on TE's own
tape screen: settings > PACKS > lanes, off at first; TE's deck small in the centre, the timecode top right; with markers too), **markers 96** (markers: set, name, cue, jump,
loop, move; a new tape no longer takes an old tape's markers; over tall lanes its flags hang above the moved ruler), **perform 6** (the PERFORM face and the song arranger), **punch 3** (14
punch-in effects on the white keys), **themes 11** with the looks **theme_89mph 5** (89MPH) and **theme_console 6**
(CONSOLE; TE's count-in shows in the look), **miditracks 47** (MIDI tracks on the tape, outputs MIDI / SYNTH / DRUM /
BOTH / PUNCH; CHERD's chains onto a MIDI track). On open-field's stock base there is no theme setting (the look
installed is on) and the files kept per tape don't follow TE's copy and delete. Replaces the pre-release
lanes-87-experimental.

## vu 34, 2026-11-26

The first vu release: the mixer's visualizers, in `vu-34.zip`, named after `vu.pack`'s version. **vu 34** (`vu.pack`) is
the host; each look is its own pack. Core: **vu_sundown 1** (SUNDOWN, a synthwave sunset over mirrored mountains made of
the bands), **vu_spectrum 6** (SPECTRUM), **vu_classic 4**, **vu_lcd 5**, **vu_meter 4** (VU). Optional: **vu_console 4**
(CONSOLE, a retro sci-fi computer panel), **vu_bella 10** (BELLA), **vu_andy 8** (ANDY), **vu_goodtimes 3** (GOOD TIMES)
and **vu_scope 3** (SCOPE). Tap the mixer key on the levels page for the next look; the
knobs on a look turn TE's master EQ. With punch 3+ the white keys hold punch's effects on a look: no strip while held,
one thin line while its knobs turn. With markers 94+, shift + a key on a look cues a marker. Settings under settings >
packs > vu: EQ knobs (on), punch keys (off), and on bases with option words look (by name) and classic (bars / dots /
lines); on other bases those two rows don't show and the tap changes the look (`user/pf/vu/look.txt` keeps it).
Pick the one or two looks you like and copy just those plus vu.pack; the zip has all ten to choose from.

## engines 2, 2026-11-26

The first engines release, `engines-2.zip`: **lilith 16**, **clarinet 16** and **boarder 22**, synth engines in the
unit's engine list, **native**: they render in the unit's own voices through open-field's engine interface. TE's T3
effect, snowtrain and fx train apply to them directly (synthbus is no longer needed: delete `synthbus.pack` if you have
it); TE's velocity changes lilith's loudness; TE's pitch bend and glide reach the clarinet, hole by hole. The engines sit
at TE's engine level; the clarinet's and boarder's sounds have a raised volume (sounds an earlier version wrote into
`user/synth_presets/<engine>/` stay: delete that folder to get the new ones). Saved sounds keep working.

## CHERD 57 and recstart 13, 2026-11-26

**CHERD 57** (`cherd-57.zip`, cherd.pack 57; named after the pack's version, as CHERD 37 was). Since CHERD 37: **NEXT**
(the likeliest next chords by name under the chord, ranked on the key picture), fakebook spelling, every held flavor
combination named and sounded, **LOCK** (HELP held + a flavor key; LOCK / UNLOCK flashes on the top line), HELP on
CHERD's page is CHERD's alone, OCT shown under the 4th knob, about 60 KB less room. Chains are not in this release.

**recstart 13** (`recstart-13.zip`), a new pack: with REC held on a stopped tape, the first sound over the input
threshold starts the take. WAITING: INPUT flash with the level; settings > PACKS > RECSTART: auto start, threshold (TE
or -60 to -24 dBFS).

## fx 1.1 and CHERD 37, 2026-11-24

**fx 1.1:** snowtrain 17, wagons 13, beignet 2 (the fx 1.0 files, byte for byte) and **TUNE 28**, whose file is now
`tune.pack` (formerly autotune.pack). The page, the effect `tune` and its sound are the same; sounds that use the
effect keep it. **Upgrading:** delete `autotune.pack` from the unit's `packs` folder when you copy `tune.pack`; with
both there the loader runs the earlier file by name (`autotune.pack`) and leaves `tune.pack` out. TUNE keeps no files
and no settings, so nothing resets.

**CHERD 37** is its own release (it was the optional partner in fx 1.0): `cherd-37.zip` with cherd.pack 37 (the same
file as in fx 1.0), the CHERD manual, LICENSE, NOTICE, THIRD-PARTY, OFL.txt (Field Sans) and SHA256SUMS. GATE, FREEZE
and TUNE still follow its chord when it is installed.

## fx 1.0, 2026-11-24

The first release: snowtrain 17, wagons 13, beignet 2, TUNE 27, and cherd 37 as their optional partner.

- **snowtrain 17:** graceful on Faust's stock base (a new rack record only once the knob rests; NO MEMORY less often,
  a restart clears it), tape track trains hidden where stock 8 tracks would leave them silent.
- **wagons 13:** GATE lighter (30000 cycles declared), TAPE declares 84000.
- **beignet 2:** presets page, FX OFF / FX ON flash.
- **TUNE 27:** the page titled TUNE.
- **cherd 37:** settings follow the tape; the chord font is Field Sans (from Petaluma Script, OFL), inside the pack.
