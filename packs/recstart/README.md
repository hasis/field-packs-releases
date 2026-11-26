# recstart.pack

**Quick start (one page):** [docs/recstart-quickstart.pdf](../../docs/recstart-quickstart.pdf).

**recstart: sound starts the recording.** With REC held and the tape stopped, TE starts recording on the first key.
recstart lets **incoming sound** start it too: when the input goes over TE's THRESHOLD, it presses PLAY for you. Good for
an MPC, a drum machine or any gear on line in or USB: hold REC, start your gear, and the take begins with its first
sound.

Version 13, level 6, for OS 1.7.3+0 with open-field 0.12. Released as **recstart 13** (its own small release).

Screenshots: none yet. Its only drawing is a small flash in the top right corner of TE's tape screen while it
waits, saying what it waits for: WAITING: INPUT TE -24 (TE's THRESHOLD) or WAITING: INPUT -36 dB (its own).

## Gestures

1. Stop the tape, pick an audio track, and have a source on the input (TE's input screen: line in, USB or the mic).
2. Set TE's **THRESHOLD** on the input screen (its knob: -24 to 0, -12 by default; the knob's number x 2 is dBFS, so
   -48 to 0 dBFS). recstart uses the same level, or its own (Settings below).
3. Hold **REC**. recstart shows **WAITING: INPUT** and the level (TE -24, or -36 dB) in the top right corner of the tape screen. A key still starts the
   take, as on TE's own.
4. Play your source. The first sound over the threshold starts the take: recstart presses PLAY for you, once per REC hold.

When the take starts the flash goes. Let go of REC before any sound and nothing happens. Hold REC again to wait again.

Knobs are the 1st to 4th encoder from the left; "A + B" means hold A, then press B.

## Settings

In TE's settings (shift + COM, then T1), PACKS, RECSTART (the base keeps them in `user/pf/.options`):

| Option | Choices | What it does |
| --- | --- | --- |
| auto start | **on** / off | off: recstart does nothing, REC behaves as stock (miditracks then says WAITING: KEY OR PLAY) |
| threshold | **TE**, -60, -54, -48, -42, -36, -30, -24 | TE: TE's THRESHOLD (-48 to 0 dBFS). A number: recstart's own level in dBFS, below TE's reach down to -60 |

Eight words is the most a list may have; for a level above -24 dBFS use TE's THRESHOLD. On a base before 32 there is no
settings entry: auto start on, threshold TE.

## Needs and works with

- Needs: base.pack (level 6; the settings entry from base 32, Faust's stock open-field included). Nothing else: it draws its own waiting flash.
- Works with (optional, none needed): cherd (recstart's PLAY goes through CHERD's key entry when both are there; nothing
  to set).

## Files on the unit

None of its own. Its two settings are lines `recstart/auto start=...`, `recstart/threshold=...` in the base's
`user/pf/.options`.

## Install

With the install page of open-field (its packs section, once listed), or by hand: unit in disk mode, copy
`recstart.pack` into the folder `packs` (drive mode: `user/pk`), leave disk mode, switch the unit off and on. **Holding
HELP while switching on starts with no packs.**

**Remove:** delete `recstart.pack` from `packs` and restart. It leaves nothing behind.
