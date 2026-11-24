# Changelog

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
