# Lyric Melody Alignment

Use this before creating any music-2.6 prompt with lyrics. The goal is to make the generated vocal melody follow the lyric meaning, Mandarin stress, breath, natural vocal range, and emotional climax.

## Core Rule

Do not ask the music model to invent melody from style alone. First convert the lyrics into a singable plan:

```text
lyrics -> phrase length -> stress words -> breath points -> pitch contour -> vocal range -> prompt
```

For emotional songs, also plan:

```text
verse restraint -> pre-chorus tension -> chorus release -> post-chorus/outro afterglow
```

## Lyric Prosody Checklist

For each lyric line:

- Count Chinese characters. Prefer 7-11 characters per sung phrase for 80-100 BPM emotional pop.
- Mark semantic stress words: nouns, verbs, emotional images, and the "pain point" of the line.
- Mark weak particles: 的、了、着、啊、吗、呢. Avoid placing these on the highest or longest note.
- Add breath points after complete semantic units.
- If a line is longer than 13 Chinese characters, split it or use faster rap-like delivery intentionally.
- If two consecutive lines have very different lengths, adjust melody rhythm or rewrite one line.

## Melody Contour Rules

- Verse: low-mid register, speech-like, mostly stepwise motion.
- Pre-chorus: gradual upward contour; build tension without large interval jumps.
- Chorus: use a short repeatable motif; place the highest note on the strongest emotional word.
- Climax chorus: raise vocal intensity and melodic range together; do not rely on high notes alone.
- Sad songs: resolve line endings downward or suspend briefly before falling.
- Sweet songs: allow upward endings and lighter repeated notes.
- Energetic songs: use clearer rhythmic repetition and shorter note values.

## Emotional Climax Rules

A more emotional and激昂 chorus needs all of these, not just louder singing:

- Pitch lift: chorus sits 3-5 semitones higher than verse, with the highest note on the emotional keyword.
- Rhythm lift: pre-chorus shortens note values or increases rhythmic urgency before the chorus.
- Drum lift: add fuller kick/snare or stronger downbeat at the chorus entry.
- Harmony lift: add backing vocal, doubled lead, octave layer, or simple harmony on the chorus hook.
- Instrument lift: open piano octave, add strings/pads, or add bass movement at chorus.
- Dynamic contrast: keep verse sparse so the chorus feels bigger.

Intensity guide:

```text
verse: 30-40%
pre-chorus: 55-70%
chorus: 85-95%
post-chorus/outro: 50-65%
```

If the song feels emotionally flat, reduce verse density and increase pre-chorus/chorus contrast before changing the whole style.

## Vocal Range Rules

Default safe ranges:

- Female soft pop: A3-E5, occasional F5 only if the chorus requires lift.
- Female anime pop: B3-F5, avoid repeated strained F5/G5.
- Male low emotional: G2-D4, chorus can rise to E4.
- Male pop: A2-E4, occasional F4.

Use a narrower range when lyrics are dense. Dense lyrics plus high notes often creates unnatural singing.

## Mandarin Singing Rules

- Keep important words clear; do not rush consonants.
- Prefer one syllable per note for dense lines.
- Use melisma only on open vowels or simple emotional words, not on complex phrases.
- Do not stretch short function words.
- Avoid sudden octave jumps unless the lyric meaning is shock, release, or a chorus explosion.

## Prompt Fields To Add

Always add these fields to the music prompt:

```json
{
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "",
    "stress_words": [],
    "breath_points": "",
    "pronunciation": ""
  },
  "melody_plan": {
    "verse": "",
    "pre_chorus": "",
    "chorus": "",
    "cadence": "",
    "hook_motif": ""
  },
  "emotional_arc": {
    "verse": "",
    "pre_chorus": "",
    "chorus": "",
    "outro": ""
  },
  "climax_plan": {
    "entry_time": "",
    "vocal_lift": "",
    "drums": "",
    "harmony": "",
    "instrument_lift": "",
    "intensity_curve": ""
  },
  "arrangement_arc": "",
  "singing_constraints": []
}
```

## Bad vs Good Prompt Control

Bad:

```text
sad pop, female vocal, piano, sing these lyrics
```

Good:

```text
sad pop, 86 BPM, C minor, female A3-E5.
Verse stays low-mid and speech-like.
Pre-chorus rises gradually.
Chorus highest note lands on "不属于我".
Do not place high notes on 的/了.
Breathe after each line.
Use a 3-5 note repeatable hook motif.
Build from 35% verse intensity to 90% chorus intensity with drums, harmony, and strings entering at chorus.
```

## Repair When Melody Does Not Match Lyrics

If generated audio sounds wrong:

- Melody too high: lower key, narrow vocal range, say "no strained high notes".
- Lyrics rushed: reduce BPM or split lines.
- Wrong word emphasized: list `stress_words` and `avoid_high_note_words`.
- Chorus not memorable: define a 3-5 note hook motif and repeat it.
- Chorus not激昂: add `climax_plan`, raise chorus intensity to 85-95%, add drum/harmony/instrument lift.
- Vocal sounds unnatural: reduce melisma, require clear Mandarin pronunciation, add breath points.
- Verse and chorus feel disconnected: specify shared motif between verse ending and chorus opening.
- Whole song feels flat: make verse sparser and pre-chorus more tense before the chorus.
