# CHERD manual

**Chords from a key, a scale and a genre, on the OP-1 Field.** cherd.pack 57, for OP-1 Field OS 1.7.3 (+0 or +1) with Faust's
[open-field](https://github.com/LaP0573/open-field) 0.12 or later.

Press one key and a whole chord plays. The left hand picks what kind of chord, the right hand picks the root. CHERD
knows the key and the scale you are in, so one finger already plays the right chord; a genre dresses it; the left hand
bends it wherever you want. On the Field, CHERD is a synth sequencer: it plays chords on whatever synth the slot has.

Knobs are named by position: the **1st knob** is the leftmost encoder, the **4th** the rightmost. A **click** is a press
on the encoder. **A + B** means hold A, then press B. The chord logic is the same as hasis's OP-XY Cherd, so both play the same chords.

**Contents:** 1 Quick start · 2 The keyboard · 3 The controls · 4 Building chords · 5 Alt, the altered dominants ·
6 Spice · 7 Flow, the genres · 8 Scales · 9 Strum, comp and feel · 10 The arpeggiator · 11 Reading the screen ·
12 Playing real tunes · 13 Modes at a glance · 14 Install, settings, limits · 15 Reference card

## 1. Quick start

1. Copy `cherd.pack` into the unit's folder `packs` (chapter 14) and switch the unit off and on.
2. In synth mode, open the sequencer list (shift + the sequencer key) and pick **CHERD**, the eighth entry. Any synth
   engine works. With the sequencer off, keys play single notes as usual (the page says SEQ OFF - KEYS PLAY NOTES).
3. On the CHERD page set the Key (1st knob) and the Scale (2nd knob). Start with Key C and Scale major.
4. Press a key in the right-hand octave. You play the chord that belongs to that note in your key: C gives C, D gives
   Dm, G gives G, B gives Bdim.
5. Hold a left-hand key while you press a root to change the chord: hold 7th and C becomes Cmaj7; hold minor and it
   becomes Cm.
6. Turn the 4th knob, Flow, to a genre (try jazz) and the same keys play fuller chords with no extra fingers.

> **The idea in one line.** With no left key held, CHERD plays the chord your key and scale give that note. A left key
> overrides it. Flow dresses what you did not choose. Alt turns any root into a dominant, altered.

### What stays the same wherever you are

- Left-hand keys never sound. They only change the chord (held chords change under your finger).
- Smooth is on from the start: each chord takes the inversion nearest the last one, so changes move by steps. Set it to
  jump on the FEEL page for root-position blocks.
- The octave arrows move the chords, as on TE's own keyboard.
- A left key held when you strike a root stays with that chord until you let go of the root, so lifting the left hand
  early does not change it. A left key pressed after the strike only lasts while you hold it (tap sus4 over a chord,
  let go to resolve).
- Every chord depends only on where its root sits in the key, so a tune can be moved to any key by changing the Key knob.
- The page names the chord it plays in fakebook style: ^7 major seventh, -7 minor seventh, O7 half-diminished,
  o7 diminished, + augmented.
- **Recording is deliberate.** With REC held, the left-hand flavor keys go to CHERD only and never start the tape; only
  a root, the chord that sounds, starts the recording.
- Every setting is saved, and follows the tape (chapter 14).

## 2. The keyboard

The Field's 24 keys run F to E twice. CHERD splits them in the middle: the lower octave (at the current octave setting) holds the flavors, the upper one the roots.

### Left octave: twelve silent keys

| Key | Role | What it does |
|---|---|---|
| F | add6 | adds the major sixth, on any chord |
| F# | dim | diminished (b3, b5) |
| G | sus2 | suspended second (1 2 5, on any root) |
| G# | minor | minor third |
| A | sus4 | suspended fourth (1 4 5, on any root) |
| A# | major | major third |
| B | add9 | adds the ninth |
| C | 9th | seventh and ninth |
| C# | **ALT** | altered dominant (chapter 5) |
| D | 7th | adds the seventh |
| D# | dom7 | dominant seventh |
| E | Spice | the rich chord (chapter 6) |

### Right octave: the roots

The key you press is the root of the chord. The twelve notes are the twelve roots, from F to E, and the chord that sounds is built on that note's pitch class. The octave arrows shift both halves together (-4 to +4), even over a held chord: it keeps sounding and the next chord plays in the new octave; the octave shows for a moment as a small **+1**, **-2** or **0** beside the chord name.

### Qualities and extensions

Five keys pick the **quality** of the triad: `major` `minor` `dim` `sus2` `sus4`. If you hold two, the latest wins. The others are **extensions**; they stack, and any number can be held at once.

## 3. The controls

On the CHERD page the four encoders are CHERD's. Turn them to set a value; **click** them for the extras.

### Main page

| Knob | Name | Choices | What it does |
|---|---|---|---|
| 1st | Key | C G D A E B Gb Db Ab Eb Bb F | The key you play in. The keys run round the circle of fifths, so one step is a neighbouring key. |
| 2nd | Scale | off + 34 scales | Which notes are in the key. With a scale set, each root gets its diatonic chord. Off plays plain major chords. |
| 3rd | Spread | close, open, wide, bass, lead | The shape of the chord, or lead: single notes locked to the Key and Scale. |
| 4th | Flow | 12 genres | A genre that dresses the chords you did not choose: off, color, jazz, pop, soul, gospel, bossa, ambient, blues, rock, monk, django. |

### Clicks and keys

| Gesture | Does | Shown |
|---|---|---|
| 1st click | the FEEL page on / off | the top line shows smooth, swing, human and the comp pattern |
| 2nd click | strum: off, up, down, alt. On the FEEL page: SNAP (below) | UP / DOWN / ALT under the 2nd knob |
| 3rd click | comp on / off (the pattern is picked on the FEEL page) | the pattern's name under the 3rd knob |
| 4th click | arp on / off (chapter 10) | the arp's mode and rate under the 4th knob |
| shift held | the ARP page (chapter 10) | the ARP page over the screen |
| shift + 4th click | keeps the ARP page open, so both hands can play while you turn its knobs; again to let it go | the ARP page |
| HELP (let go, no key under it) | one step back: the kept ARP page, then the FEEL page; on the main page nothing | |
| HELP held + a left key | LOCK: that flavor stays on every chord until HELP + the key again (below) | |
| *internal builds:* HELP held + 1st / 2nd / 3rd / 4th click | CHAINS: play / stop, save, to PATTERN or a MIDI lane, clear (chapter 10b) | PLAY, SAVE, TO PATTERN / TO LANE, CLEAR in the band under the knobs |
| *internal builds:* HELP held + 2nd / 3rd / 4th turn | CHAINS: the step's length, the 3rd click's target, the slot (chapter 10b) | STEP, TARGET, SLOT in the line above them |
| *internal builds:* HELP held + a root (right-octave key) | STEP ENTRY: that chord becomes the chain's next step (chapter 10b) | STEP 3/16 G7 2 BARS at the top |

### FEEL page

Click the 1st knob: the knobs become the feel of the playing. Click it again (or HELP) to go back.

| Knob | Name | Choices | What it does |
|---|---|---|---|
| 1st | Smooth | smooth (default), jump | Smooth picks the inversion nearest the last chord, so changes move by steps; with five notes it drops the fifth, as a pianist does. On the Bass shape it plays a close chord led over the root an octave below. Jump builds every chord up from its root. |
| 2nd | Swing | even, swing, trip | Moves comp off-beats late (about 58%, or a full triplet). On pompe it lays 2 and 4 back a touch. |
| 3rd | Human | tight, loose, drunk | Small differences in loudness and timing from string to string and hit to hit, like a real hand. |
| 4th | Comp | stab, chrl, pump (default), sync, pompe | Which rhythm the 3rd click turns on (chapter 9). Shown top right. |

**SNAP** (the 2nd click on the FEEL page): OFF, 1/16, 1/8, 1/4, 1/32, 1/8T, 1/16T, shown under the 2nd knob. While the
tape records, the chords you play wait for the next grid line. With snap.pack on the unit this is snap's own setting
(per tape, the same as the tape screen's 3rd click); without it CHERD keeps its own.

### Voicing shapes

| Shape | Sounds like |
|---|---|
| close | All notes within about an octave above the root. The default. |
| open | Root, fifth, then the third an octave up: a spread, airy chord. |
| wide | Upper extensions lifted an octave; triads double the fifth. |
| bass | Wide, plus the root an octave below: a chord with a bass note under it. With Smooth, a close chord led over that root. |

### Lead

The **lead** step turns the keyboard into single notes locked to the Key and Scale, for a melody. All 24 keys play,
left octave included, and the left keys no longer pick chords. The 14 white keys are the scale's degrees: the key under
C is always the tonic, so the fingering is the same in every key (in C major they are exactly the white keys). A black
key plays the note a semitone above the white key below it. Flow does not apply.

## 4. Building chords

Hold any combination of left keys, then press a root. This is what each combination plays on C, with Scale off and Flow off, so you can see the chord itself. The numbers are the notes above the root.

| Hold | Chord on C | Notes |
|---|---|---|
| (none) | C | 1 3 5 |
| Major | C | 1 3 5 |
| Minor | C- | 1 b3 5 |
| Dim | Co | 1 b3 b5 |
| Sus2 | CSUS2 | 1 2 5 |
| Sus4 | CSUS4 | 1 4 5 |
| 7th | C^7 | 1 3 5 7 |
| Minor + 7th | C-7 | 1 b3 5 b7 |
| Major + 7th | C^7 | 1 3 5 7 |
| Dom7 | C7 | 1 3 5 b7 |
| Sus4 + 7th | C7SUS4 | 1 4 5 b7 |
| Sus4 + 9th | C9SUS4 | 1 4 5 b7 9 |
| Sus4 + 7th + add6 | C13SUS4 | 1 4 5 b7 13 |
| Sus2 + 7th | C7SUS2 | 1 2 5 b7 |
| Sus2 + add6 | C6SUS2 | 1 2 5 6 |
| Dim + 7th | CO7 | 1 b3 b5 b7 |
| Dim + add6 | Co7 | 1 b3 b5 6 |
| Dim + 9th | CO9 | 1 b3 b5 b7 9 |
| 9th | C^9 | 1 3 5 7 9 |
| Minor + 9th | C-9 | 1 b3 5 b7 9 |
| Major + 9th | C^9 | 1 3 5 7 9 |
| add9 | CADD9 | 1 3 5 9 |
| add6 | C6 | 1 3 5 6 |
| Minor + add6 | C-6 | 1 b3 5 6 |
| Minor + add9 + add6 | C-6/9 | 1 b3 5 6 9 |
| add9 + add6 | C6/9 | 1 3 5 6 9 |
| Dom7 + add6 | C13 | 1 3 5 b7 13 |
| Major + 7th + add6 | C^13 | 1 3 5 7 13 |
| Minor + 7th + add6 | C-13 | 1 b3 5 b7 13 |
| Spice | C^13 | 1 3 7 9 13 |
| Minor + Spice | C-11 | 1 b3 b7 9 11 |
| Major + Spice | C^13 | 1 3 7 9 13 |
| Alt | C7b9 | 1 3 5 b7 b9 |
| Alt + add9 | C7#9 | 1 3 5 b7 #9 |
| Alt + add6 | C7#5 | 1 3 #5 b7 |
| Alt + Dim | C7b5 | 1 3 b5 b7 |
| Alt + Sus4 | C7#11 | 1 3 5 b7 #11 |
| Alt + Sus4 + add9 | C7#9#11 | 1 3 5 b7 #9 #11 |
| Alt + 9th + add9 | C7ALT | 1 3 b7 b9 #9 |
| Alt + 9th + Sus4 | C7b9#11 | 1 3 5 b7 b9 #11 |
| Alt + add9 + add6 | C7#5#9 | 1 3 #5 b7 #9 |
| Alt + Spice | C7ALT | 1 3 b7 b9 #9 b13 |

### The rules in short

- Quality + 7th: minor + 7th is m7, major + 7th is always maj7, sus4 + 7th is 7sus4, dim + 7th is half-diminished (m7b5).
- Dom7 is always the dominant seventh. 9th is the seventh plus the ninth. add9 and add6 add just their note.
- **LOCK** (cherd 50): hold HELP and press a left key to lock that flavor in: every chord plays as if you held it, until HELP + the same key again. Any number of extensions and one quality can be locked (a new locked quality replaces the old; a quality you hold wins over it; keys you hold add on top). A locked key is a large white dot on the key picture, and LOCK with the names flashes on the top line for a moment (UNLOCK when you clear one); with Spice locked the dots ripple through its colours as while it is held. The locks are saved with the tape.
- **Every key you hold sounds** (cherd 49), and the name says exactly those notes. A sixth beside a seventh is a thirteenth (dom7 + add6 is C13). The only notes left out, on purpose: Spice's fifth; the ninth over Sus2 (it is the second itself); with no quality held, the 9th key's ninth where the scale's is a flat or sharp nine, and add6 over an augmented triad.
- Sus2 and Sus4 are fixed, as Major, Minor and Dim are: 1 2 5 and 1 4 5 on any root, even where the key's own second or fourth is another note (Esus2 in C major has F#). add6 is the major sixth on any degree (Am6 in C major; on a diminished triad it makes the diminished seventh). Over Dim and the suspensions the seventh is the flat one.
- No quality held: extensions stack on the chord your key and scale give that note, so they stay in the scale.
- With a quality held: extensions stack on that triad.
- Flow stays underneath: a genre's colour (a seventh, a ninth, a suspension) joins what you hold.

## 5. Alt: the altered dominants

> Alt is the key at C# in the left octave. Hold it with a root and the root becomes a dominant seventh, altered. It ignores the key, the scale and the genre: a dominant is a dominant anywhere, so Alt plays the same chord on that root every time.

Alt alone plays the 7b9, the most common alteration. Each other key beside it then adds the altered twin of what it normally adds:

| Hold with Alt | Alteration | On C | Notes |
|---|---|---|---|
| (nothing) | flat nine | C7b9 | 3 5 b7 b9 |
| 9th | flat nine (said out loud) | C7b9 | 3 5 b7 b9 |
| add9 or minor | sharp nine | C7#9 | 3 5 b7 #9 |
| add6 | sharp five | C7#5 | 3 #5 b7 |
| dim | flat five | C7b5 | 3 b5 b7 |
| sus4 | sharp eleven | C7#11 | 3 5 b7 #11 |
| add9 + add6 | sharp nine and sharp five | C7#5#9 | 3 #5 b7 #9 |
| 9th + add6 | flat nine and sharp five | C7#5b9 | 3 #5 b7 b9 |
| dim + add9 | flat five and sharp nine | C7b5#9 | 3 b5 b7 #9 |
| sus4 + 9th | sharp eleven and flat nine | C7b9#11 | 3 5 b7 b9 #11 |
| Spice | the full altered chord | C7ALT | 3 b7 b9 #9 b13 (no fifth) |

7th, dom7, major and sus2 add nothing under Alt: the chord is a dominant already. The keys stack fully (cherd 49): sus4 + add9 is C7#9#11, dim + add6 both altered fifths (C7ALT). A chord with both ninths is a 7alt and has no natural fifth; a chord is five notes above its root, so with both ninths and the sharp five the flat five (or sharp eleven) gives way. Spice with Alt is always the full altered chord.

### Why it works this way

Each key does what you already know, one half-step altered. 9th gives the ninth, so Alt makes it the flat ninth. add9 adds the ninth, so Alt makes it sharp. Minor, whose third is the sharp nine over a major third, gives the sharp nine too. The dim key's flat five becomes the flat five of the dominant.

### Where you will use it

- V in a minor key: Alt alone, G7b9 resolving to Cm.
- Secondary dominants: hold Alt (or dom7) on the root before the chord you are heading for: D7b9 before Gm.
- Tritone substitutions: Alt + dim, or Alt alone, on the root a tritone from the V.
- Altered V: Alt + add9 + add6 for the 7#5(#9) that many minor tunes write.

## 6. Spice

> Spice is the E key. It plays the full, rich version of the chord for that note: a seventh chord with its ninth, and on major and dominant chords the thirteenth (on minor chords the eleventh) in place of the fifth.

On C major with Flow off every degree gets the Spice chord of its mode:

| Degree | Chord | What Spice plays | Why |
|---|---|---|---|
| I (C) | Cmaj13 | 3 7 9 13 | a major chord takes the thirteenth |
| ii (D) | Dm11 | b3 b7 9 11 | a minor chord takes the eleventh |
| iii (E) | Em7 | b3 5 b7 | the flat ninth over iii is an avoid note, so it is left out |
| IV (F) | Fmaj13 | 3 7 9 13 | lydian: the thirteenth is available |
| V (G) | G13 | 3 b7 9 13 | a dominant takes the thirteenth |
| vi (A) | Am11 | b3 b7 9 11 | a minor chord takes the eleventh |
| vii (B) | Bm7b5 | b3 b5 b7 | no ninth over a diminished fifth |

### Spice follows the key and the scale

Spice only plays notes that belong to the scale, so it always sounds right in the key. Where the scale gives a dominant its flat nine (the V of harmonic minor, the I of Phrygian dominant) that flat nine is the chord's colour, so Spice plays the 7b9 there, not a plain seventh. Spice is never thinner than the 7th (cherd 49): where a major seventh chord's scale has no natural ninth (the bVI of harmonic minor, the bII of Phrygian dominant) it takes the sharp eleven the scale does give: Abmaj7(#11) in C harmonic minor.

### Spice and Flow

With Flow off, Spice is always the full chord. With Flow on, Spice follows the chord's job: the full chord on the V and on a chord that resolves down a fifth, the ninth chord on the IV, the seventh chord on the ii and vi, and the plain triad on the I at rest, the iii and the vii. So a run of Spice chords leans toward the dominant and settles on the tonic, as a tune does.

### Spice and Alt

Alt wins. Alt + Spice is the full altered chord (7ALT). Spice alone is the diatonic rich chord. When the Spice key is the last one you pressed, the page background starts to shimmer through seven colours while you hold it.

## 7. Flow: the genres

Flow dresses the chords you did not choose. It decides from the chord's job in the key (the one, the four, the five and so on), so it works in every scale. If you hold left keys, they win, and the genre's colour joins them.

| Flow | I | ii | iii | IV | V | vi | vii |
|---|---|---|---|---|---|---|---|
| off | C | D- | E- | F | G | A- | Bo |
| color | C | D- | E- | F | G7 | A- | Bo |
| jazz | C^9 | D-9 | E-7 | F^9 | G9 | A-9 | BO7 |
| pop | CADD9 | D- | E- | FADD9 | G | A- | Bo |
| soul | C^7 | D-7 | E-7 | F^7 | G7 | A-7 | Bo |
| gospel | C^9 | D-9 | E-7 | F^9 | GSUS4 | A-9 | BO7 |
| bossa | C6 | D-7 | E-7 | F6 | G9 | A-7 | BO7 |
| ambient | CADD9 | DSUS2 | ESUS4 | FADD9 | GSUS4 | ASUS2 | Bo |
| blues | C7 | D- | E- | F7 | G7 | A- | Bo |
| rock | C5 | D- | E- | F5 | G5 | A- | Bo |
| monk | C69 | D-9 | E-7 | F^#11 | G7b9 | A7b9 | BO7 |
| django | C69 | D-7 | E-7 | F69 | G7 | A7 | BO7 |

C major, each chord played alone. - is minor, ^ is major seventh, O7 is half-diminished, o a diminished triad.

### What each genre does

- off: plain diatonic triads.
- color: the five gets its seventh, and any chord a fifth below the last one gets its seventh (a resolution).
- jazz: a seventh chord on every degree, with the ninth where it is not a flat ninth. In a minor key the V is the dominant with its flat nine (G7b9 in C minor), the harmonic minor's tonic is a minor seventh, and the root a semitone above the tonic is the Neapolitan major seventh.
- pop: open triads with a ninth on the one and the four. soul: a seventh chord on every degree. gospel: ninths, and the five suspended. bossa: sixths on the one and four, a ninth on the five.
- ambient: suspended and open. blues: dominant sevenths on the one, four and five. rock: power chords on the one, four and five. monk: six-nine, major seventh sharp eleven, and flat nines on the dominants.
- django: the Django sound, taken from the Gypsy Jazz Songbook charts. The tonic is a six chord, never a seventh (C6/9, Am6), the minor four is a minor six (Dm6 in A minor), and the dominants are plain sevenths (E7, A7). A root outside the key is a dominant seventh leading in (Bb7 E7 Am, Eb7 D7 Gm6); a passing one, and the flat three of a major key, is a diminished seventh (G, Bbdim, Am7).

### Scale off with a genre

The genre plays in its own home scale: soul in dorian, ambient in lydian, rock in mixolydian, django in harmonic minor (Minor Swing, Dark Eyes), the others in major.

### A minor key, jazz

In A natural minor with Flow jazz the chords come out as A-9 BO7 C^9 D-9 E7b9 F^9 G9: the V is E7b9, the half-diminished is on the ii, and the tonic is a minor ninth.

## 8. Scales

Scale off plays plain major chords on every root. Set a scale and each root inside it gets its own chord stacked from the scale's notes; roots outside the scale get a sensible chord (a major chord, or a passing diminished one on the leading tone, the tritone and, in a minor key, the raised third and sixth: C#dim and F#m7b5 in A minor).

Harmonic minor is there for its major V and diminished vii; its i and III are the natural minor's (Am and C, not AmM7 and Caug). With Flow on color, the natural minor's V becomes the dominant seventh (E7 in A minor).

The bebop scales (bopD, bopM, bopDo) are a mode plus one passing note: their chords are the mode's (bebop dominant's tonic is C7, bebop dorian's Cm7). The altered scale (alt) is played over a dominant: its tonic is the altered dominant (C+ alone, C7#5 with the 7th, C7ALT with the 9th, Spice or Flow jazz). In scales that are not seven notes the 7th key looks for a real seventh first (half-whole diminished: C7) and takes the sixth only where there is none (pentatonic: C6).

| # | Header | Scale | Notes (from the tonic) |
|---|---|---|---|
| 1 | major | Major (Ionian) | 1 2 3 4 5 6 7 |
| 2 | minor | Natural minor (Aeolian) | 1 2 b3 4 5 b6 b7 |
| 3 | dor | Dorian | 1 2 b3 4 5 6 b7 |
| 4 | mixo | Mixolydian | 1 2 3 4 5 6 b7 |
| 5 | lyd | Lydian | 1 2 3 #4 5 6 7 |
| 6 | phr | Phrygian | 1 b2 b3 4 5 b6 b7 |
| 7 | loc | Locrian | 1 b2 b3 4 b5 b6 b7 |
| 8 | harm | Harmonic minor | 1 2 b3 4 5 b6 7 |
| 9 | mel | Melodic minor | 1 2 b3 4 5 6 7 |
| 10 | phrD | Phrygian dominant | 1 b2 3 4 5 b6 b7 |
| 11 | pent | Major pentatonic | 1 2 3 5 6 |
| 12 | mpent | Minor pentatonic | 1 b3 4 5 b7 |
| 13 | blues | Blues | 1 b3 4 b5 5 b7 |
| 14 | whole | Whole tone | 1 2 3 #4 #5 b7 |
| 15 | dimin | Diminished (whole-half) | 1 2 b3 4 b5 b6 6 7 |
| 16 | mblue | Major blues | 1 2 b3 3 5 6 |
| 17 | hmaj | Harmonic major | 1 2 3 4 5 b6 7 |
| 18 | lydD | Lydian dominant | 1 2 3 #4 5 6 b7 |
| 19 | alt | Altered | 1 b2 b3 3 b5 b6 b7 |
| 20 | dimHW | Diminished (half-whole) | 1 b2 b3 3 b5 5 6 b7 |
| 21 | hung | Hungarian minor | 1 2 b3 #4 5 b6 7 |
| 22 | dharm | Double harmonic | 1 b2 3 4 5 b6 7 |
| 23 | hira | Hirajoshi | 1 2 b3 5 b6 |
| 24 | insen | In sen | 1 b2 4 5 b7 |
| 25 | iwato | Iwato | 1 b2 4 b5 b7 |
| 26 | kumoi | Kumoi | 1 2 b3 5 6 |
| 27 | nikr | Nikriz | 1 2 b3 #4 5 6 b7 |
| 28 | bopD | Bebop dominant | 1 2 3 4 5 6 b7 7 |
| 29 | bopM | Bebop major | 1 2 3 4 5 b6 6 7 |
| 30 | bopDo | Bebop dorian | 1 2 b3 3 4 5 6 b7 |
| 31 | lydA | Lydian augmented | 1 2 3 #4 #5 6 7 |
| 32 | mixb6 | Mixolydian b6 | 1 2 3 4 5 b6 b7 |
| 33 | loc2 | Locrian #2 | 1 2 b3 4 b5 b6 b7 |
| 34 | dorb2 | Dorian b2 | 1 b2 b3 4 5 6 b7 |

Pentatonic and other five- and six-note scales take the major or minor third and the perfect fifth when the scale has them (C major pentatonic: C, Am, Dsus4), and stack what they have otherwise.

## 9. Strum, comp and feel

Click the 2nd knob for a **strum**: the notes of the chord start one after another instead of together. How hard you hit the key sets the speed: soft is a slow strum, hard a fast one (the same curve as Cherd Play on the OP-XY).

| How hard (velocity) | Time between notes |
|---|---|
| 8 | about 46 ms |
| 20 | about 40 ms |
| 40 | about 33 ms |
| 60 | about 28 ms |
| 80 | about 24 ms |
| 100 | about 20 ms |
| 127 | about 16 ms |

### Directions

- UP: lowest note first.
- DOWN: highest note first.
- ALT: up, then down on the next chord, and so on.

### Comp: a held chord on a rhythm

Click the 3rd knob to turn comp on or off; pick the pattern with the 4th knob on the FEEL page. A held chord is played again and again on a one-bar rhythm, like a rhythm player comping. While the tape rolls it stays on the transport's bar, so a chord pressed a little late does not drag the groove late; with the tape stopped the bar starts with your first chord. The press itself is a short hit shaped like the pattern. Changing chords mid-bar keeps the groove.

| Pattern | Rhythm | Feel |
|---|---|---|
| stab | the "and" of every beat | off-beat stabs (reggae, house) |
| chrl | beat 1 and the "and" of 2 | the charleston |
| pump | every beat | four on the floor |
| sync | 1, the "a" of 1, the "and" of 2, the "and" of 3 | a syncopated push |
| pompe | every beat, see below | Django's la pompe |

### La pompe

The gypsy-jazz rhythm guitar: a quick, light upstroke on the bass strings just before beats 1 and 3, then a full downstroke that rings briefly; on 2 and 4 a sharp downstroke choked short by the fretting hand. The timings were measured from Nousche Rosenberg's pompe lesson (about 35 ms grace, 110 ms ring, 60 ms chop) and do not stretch with tempo, like a real hand. Use a synth patch with a short release so the chops stay short.

### Feel (the FEEL page, 1st click)

- **Swing** moves comp off-beats late: swing is about 58%, trip a full triplet. Pompe has no off-beats, so there swing lays 2 and 4 back a little.
- **Human** gives every string a slightly different loudness and start, and lets the whole hand land a touch late: loose is subtle, drunk is obvious. It applies to strums, comp hits and plain chords.
- **Smooth** (on by default) voice-leads: each chord takes the inversion closest to the one before, holding shared notes (C, then Am as C-E-A, then F as C-F-A, then G as B-D-G).

### Live changes

Hold a root and press or release a left key, or turn Key, Scale, Spread, Flow or Smooth: the held chord changes under your finger. Notes that stay keep sounding.

### Holding several chords

Hold two roots whose chords share notes (C and Em share E and G) and let go of one: the other keeps every note.

## 10. The arpeggiator

CHERD has its own arpeggiator. Click the 4th knob on the CHERD page to turn it on or off. Hold **shift** for the ARP page, where the four knobs set it up; **shift + 4th click** keeps that page open so both hands are free to play (shift + 4th click again, or HELP, lets it go). While the ARP page is up the 1st click only closes it; the 2nd and 3rd clicks stay strum and comp. Hold a chord and CHERD plays its tones one after another on the sequencer clock instead of all together. No other sequencer is needed.

| Knob (ARP page) | Setting | Choices |
|---|---|---|
| 1st | Mode | UP, DOWN, UP-DOWN, RANDOM |
| 2nd | Rate | 1/4, 1/8, 1/8T, 1/16 (default), 1/16T, 1/32 |
| 3rd | Gate | 10% .. 100% of a step (default 50%) |
| 4th | Octaves | 1, 2, 3 |

- It plays only while you hold keys (no latch). Every held chord's tones are in the run.
- While the tape rolls its steps stay on the transport's grid.
- Key, Scale, Spread, Flow and Smooth all apply; change a flavour or a knob while holding and the run changes with it.
- Swing and Human apply to the arp. Comp is ignored while the arp is on.
- Lead mode is not arpeggiated: it plays single notes as usual.
- Its settings are kept per synth slot, like strum and comp, and follow the tape (chapter 14).

## 10b. Chains: a chain of Cherds

*Coming in a later release; internal builds only (`make cherd-internal`). CHERD 57's `cherd.pack` has no chains: there HELP held + a click or the 2nd..4th knob does nothing, and HELP + a root plays the chord.*

CHERD remembers what you play. Every chord you strike by hand is kept with its root, the flavors it was struck with
(held and locked) and when it came and how long you held it, to the nearest 16th. The kept chords are a **phrase**:
the last 16 of them. Two bars with no key held, and the next chord starts a new phrase.

Hold **HELP** and the band under the knobs shows two lines: the upper one what a **turn** sets, the lower one what a
**click** does (dim when there is nothing to do it to).

| Knob | Turn (upper line) | Click (lower line) |
|---|---|---|
| 1st | Key, as always | **PLAY / STOP** the slot's chain |
| 2nd | **STEP**: the length of a step you enter: 1/16, 1/8, 1/4, 1/2, 1 BAR, 2 BARS | **SAVE** the phrase you played into the slot (SAVED 4 CHORDS) |
| 3rd | **TARGET**: where the 3rd click sends the chain: PATTERN or a MIDI LANE | **TO PATTERN** / **TO LANE** |
| 4th | **SLOT**, 1 to 16 (CHAIN 3 at the top right) | **CLEAR** the slot: the first press says AGAIN TO CLEAR, a second one within a second and a half clears it |

**A chain plays the way keys do.** Each chord is struck as if you pressed its root with its flavors held: the Key,
Scale, Flow, Spread and Smooth you set now, strum, comp and the arp all apply. Turn the Scale while it plays and the
chain moves with it; hold a flavor (the 7th, Spice) and every chord of the chain takes it while you hold; play roots
over it, and your chords sound with it (they become the next phrase, not part of the chain). The loop is the phrase
rounded up to whole bars. It starts at once when the tape is stopped, on the next downbeat while it rolls.

**Step entry: a chain chord by chord, no timing needed.** Hold HELP and press a root: that chord is added behind the
slot's last one, one step long, and sounds while you hold the key. The top says what went in: STEP 3/16 G7 2 BARS
(the third of sixteen chords, its name, its length). Set the step's length first with HELP + the 2nd knob. Flavors:
the ones you hold when HELP goes down stay with the step, and so do the locked ones, so with HELP held a left key
(LOCK) then a root enters that flavor's chord; press the left key again to take it off for the next. A slot holds 16
chords and 16 bars: CHAIN FULL after that. Steps go straight into the slot (no SAVE); to start over, CLEAR it first.
A step is never part of the phrase you played.

**To PATTERN.** With the target on PATTERN, HELP + the 3rd click writes the chain into TE's PATTERN sequencer (synth
side, seqx needed), replacing what was there: each chord's notes on its step, folded into the pattern's two octaves at
the octave you are on, its length as seqx's note length, the pattern 16 steps long. A chain of one bar is one step a
16th; a longer chain is squeezed and the top says how long a step is (1/8 A STEP: set TE's pattern to 1/8 to hear it
in time). Save the pattern you had in seqbank first if you want to keep it.

**To a MIDI lane.** Turn the 3rd knob right with HELP held (TO LANE), then HELP + the 3rd click: the chain's chords
land as notes on the selected MIDI track of the tape, at the play-head, each chord as long as it is in the chain, at
the pitches CHERD plays (no strum, comp or arp: plain chords). It needs miditracks 47, a MIDI track selected and the
tape stopped; the play-head moves to the chain's end, so a second click writes the next pass behind it. The top says
IN LANE 12 NOTES, or why not: AUDIO TRACK, STOP TAPE FIRST, NO MIDITRACKS.

**Chains follow the tape.** Each tape has its own 16 slots (`user/pf/cherd/tape<N>.chn`), copied when you copy the
tape and gone when a new tape is made in its place, like CHERD's other settings. This needs a base that keeps files
per tape (our base 39); under Faust's stock base the chains stay one set for the unit, `user/pf/cherd/chains.bin`.
The first time CHERD 55 runs with files per tape, the chains you had (chains.bin) move into the tape that is mounted.

## 11. Reading the screen

- Top line: the four knob values, each above its knob in its colour (Key, Scale, Spread, Flow), or on the FEEL page
  Smooth, Swing, Human and the comp pattern.
- The big name in the middle is the chord you are playing, in fakebook style (Field Sans, made from Petaluma Script):
  the root, a flat or sharp, then the chord's symbol. Notes are spelled by what they do: borrowed chords on the flat 2,
  3, 6 and 7 are flats (Eb, Ab, Bb), passing and raised ones sharps (C#dim, F#dim, G# in A minor).
- **Spelling** (cherd 49). A Key keeps one name whatever the Scale: C Db D Eb E F F# G Ab A Bb B for scales with a
  major third, the same with C# and G# for scales with a minor third. Every scale note has its own letter, so some keys
  show B#, E#, Cb, Fb or a double sharp (G# harmonic minor: F##; its V7 is D# F## A# C#). Pentatonic and blues scales
  are spelled from their parent scale (the blue note is the flat five). A borrowed chord that would need a double flat
  takes the plain letter (bVI in Db major is A). A diminished chord that comes down a semitone is flat (Em7 Ebo7 Dm7).
  The letters on the key picture follow the same spelling.
- Under the 1st knob: the chord's numeral. A dominant keeps its 7 (I7, V7), a secondary dominant is V/ii, a slashed o
  is half-diminished (viiø7), o7 a diminished seventh, + an augmented chord.
- Under the chord, each under its knob: the strum (2nd), the comp pattern (3rd) and the arp (4th) when they are on; on
  the FEEL page, SNAP under the 2nd.
- The keyboard along the bottom shows the chord as it sounds. The root is brighter than the other notes.
- Holding a left key shows its name before you press a root. Holding Spice (the E) ripples the dots behind the name
  through seven colours.
- Before the first chord the page says **Cherd**. With the sequencer off it says SEQ OFF - KEYS PLAY NOTES.

### Chord symbols

| Shown | Meaning | Shown | Meaning |
|---|---|---|---|
| ^7 | major seventh | -7 | minor seventh |
| 7 | dominant seventh | O7 | half-diminished (m7b5) |
| 13, ^13, -11 | thirteenth, maj13, minor eleventh | 5 | power chord |
| 7b9 7#9 7#5 | altered dominants | 7ALT | full altered dominant |
| 7#5#9 7b5#9 7b9#11 7#5b9 7#9#11 | combined alterations | 7SUS4 | seventh, suspended fourth |
| 9SUS4 13SUS4 7SUS2 6SUS2 | suspended chords with extensions | -6/9 -13 | minor six-nine, minor thirteenth |
| O9 O13 | half-diminished with the ninth, thirteenth | 13(b9) ^13(#11) | Spice + add6 on a 7b9 / maj7#11 |

## 12. Playing real tunes

Pick the Key and Scale of the tune, set Flow to jazz, then play the roots. The diatonic chords come by themselves; hold a left key where a tune leaves the key.

| Tune shape | Setup | What you play |
|---|---|---|
| ii V I in major | Key C, Scale major, Flow jazz | D, G, C: you get Dm9, G9, Cmaj9 with nothing held. |
| minor ii V i | Key A, Scale minor, Flow jazz | B, E, A: Bm7b5, E7b9, Am9 with nothing held. |
| secondary dominant (D7 before Gm) | hold Alt or dom7 | press D: D7b9 or D7. |
| altered V (G7#5#9) | hold Alt + add9 + add6 | press G: G7#5#9. |
| borrowed minor (Ebm7 in C minor) | hold minor + 7th | press Eb: Ebm7. |
| 12-bar blues | Key C, Scale major, Flow blues | C, F, G: C7, F7, G7. |
| bossa | Key C, Scale major, Flow bossa | C, D, G: C6, Dm7, G9. |
| a groove, gypsy jazz | comp pattern pompe (FEEL page, 4th knob), comp on (3rd click), Flow django | hold the roots; the chord keeps time by itself. |

Checked against 21 tunes from The Real Book: Flow in jazz plays the right third and seventh for 63% of the chords on its own, the left hand reaches 99.8%, and with Alt the left hand reaches 99.7% of the exact chords, alterations included.

## 13. Modes at a glance

CHERD has several things that sound alike. This is what each one is for.

| Thing | What it is | When to use it |
|---|---|---|
| Scale | which notes are in the key | always: it decides each root's chord |
| Flow | a standing genre: dresses every chord you did *not* choose, by its job in the key | set and forget: jazz gives sevenths and ninths everywhere |
| Spice (E key) | a left key you hold *on purpose*: the richest version of this one chord | a moment of colour; with Flow on it adapts to the chord's job |
| Left keys | the exact chord, by hand: quality + extensions | when you want a specific chord |
| Alt (C# key) | turns the root into an altered dominant, ignoring key and genre | the V of a minor key, secondary dominants |
| Spread | the shape: close, open, wide, bass; or lead | how wide the chord sits; lead for melodies |
| Smooth | nearest inversion to the last chord | chord changes that move by steps |
| Strum | the notes one after another, speed from velocity | a guitar or harp gesture |
| Comp | a held chord repeated on a rhythm | a rhythm player under you; pompe for gypsy jazz |
| Swing / Human | timing and touch of the comp and strum | make it groove, make it breathe |
| Arp | the held chord's tones one after another on the clock | broken chords; mode, rate, gate and octaves on the ARP page (shift) |

### Spice or Flow jazz?

Flow is a setting: once on jazz, *every* chord you play without a left key gets its seventh and ninth, the right ones for its place in the key. Spice is a gesture: hold the E key and only the chords you play while holding it get the full treatment (seventh, ninth, and the thirteenth or eleventh). With Flow off, Spice is always the fullest chord; with Flow on, Spice follows the chord's job (full on the V, plain on the I at rest), so a run of Spice chords leans toward the dominant and settles on the tonic.

## 14. Install, settings, limits

### Install

CHERD is a pack for Faust's open-field 0.12 (base 30 or later) on an OP-1 Field running **OS 1.7.3** (the +0 and +1 releases both work).
Install open-field with its install page first. Then:

1. Unzip `cherd-57.zip` (check the files against `SHA256SUMS` if you like).
2. Put the unit into disk mode and copy `packs/cherd.pack` into the unit's folder **`packs`** (in the bootloader's
   drive mode: `user/pk`).
3. Leave disk mode, switch the unit off and on.

Or tick it on open-field's install page once it is listed there. The chord font (Field Sans) is inside the pack:
nothing else to copy. Coming from cherd 36 or older: `user/pf/cherd/field_sans.runs` (or `petaluma.runs`) is no longer
read and can go. **Safe start:** hold HELP while you switch the unit on and no pack loads; to take CHERD away, delete
`cherd.pack`.

### Settings: they follow the tape

- Key, Scale, Flow and Smooth are the song: one set for all synth slots. Spread, strum, comp, the arp (mode, rate, gate,
  octaves), swing and human are the playing style: each synth slot keeps its own, so a pad on one slot and a pompe
  guitar on another keep theirs.
- All of them are kept **with the tape** (in the tape's own file): load another tape and its key, scale and styles come
  back. A tape that has none yet takes what is set when it loads.
- `user/pf/cherd/cherd.bin` holds the last settings changed: what a new tape starts with, and what the unit starts
  with.

### Works with (optional)

- **snap.pack:** FEEL's SNAP is then snap's per-tape setting.
- CHERD's scale and sounding chord reach other packs that ask for it: TUNE (tune.pack) tunes the voice to it, wagons'
  GATE and FREEZE follow it.

### Limits worth knowing

- CHERD plays chords only while it is the synth's sequencer and the sequencer is on; with it off, keys are plain notes.
- Synth slots only (not the drum).
- Cherd Play's "follow another track" and Cherd's Target (OP-XY) have no Field equivalent.

## 15. Reference card

### Quality (latest wins)

`major` `minor` `dim` `sus2` `sus4`

### Extensions (stack)

`7th` `dom7` `9th` `add9` `add6` `Spice`

### Handy chords

| Chord | Hold |
|---|---|
| minor 7th | minor + 7th |
| major 7th | 7th |
| dominant 7th | dom7 |
| dominant 9th | dom7 + 9th |
| dominant 13th | dom7 + Spice |
| half-diminished | dim + 7th |
| diminished 7th | dim + add6 |
| 7sus4 | sus4 + 7th |
| 9sus4 | sus4 + 9th |
| minor 6/9 | minor + add9 + add6 |
| 13 (no ninth) | dom7 + add6 |
| minor 9th | minor + 9th |
| sixth / minor sixth | add6 / minor + add6 |

### Alt (altered dominants)

| Hold | Plays |
|---|---|
| Alt | 7b9 |
| Alt + add9 | 7#9 |
| Alt + add6 | 7#5 |
| Alt + dim | 7b5 |
| Alt + sus4 | 7#11 |
| Alt + add9 + add6 | 7#5#9 |
| Alt + Spice | 7ALT |

### Knobs and clicks

| Knob | Main page: turn | FEEL page: turn | ARP page (shift): turn | Click |
|---|---|---|---|---|
| 1st | Key | Smooth | Mode | FEEL page on / off (on the ARP page: closes it) |
| 2nd | Scale | Swing | Rate | strum: off, up, down, alt (on FEEL: SNAP) |
| 3rd | Spread (+ lead) | Human | Gate | comp on / off |
| 4th | Flow | Comp pattern | Octaves | arp on / off; shift + 4th click keeps the ARP page |

HELP steps back when you let it go: the kept ARP page, then FEEL. On the main page a HELP tap does nothing: on CHERD's page HELP is CHERD's alone. HELP held + a left key locks that flavor (HELP + the key again unlocks); HELP held + a root enters that chord as the chain's next step; HELP held + a click or the 2nd to 4th knob works the chain (chapter 10b).
