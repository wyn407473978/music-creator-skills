# English Song Arrangement Control

Use this before creating any music-2.6 prompt for English DJ rock, EDM rock, pop rock, cinematic rock, or high-energy short-video songs.

## Core Formula

```text
English hook -> verse/build -> pre-chorus/drop build -> chorus/drop -> post-chorus hook
```

The song must have natural English phrasing and a strong chorus/drop.

## English Lyric Rules

- Write lyrics directly in English. Do not translate Chinese sentence structures.
- Hook line should be short: 4-8 words.
- Prefer strong vowels for high/held notes: `I`, `fire`, `alive`, `tonight`, `rise`, `run`, `light`.
- Avoid awkward filler: "my heart is very pain", "I am so lonely in night".
- Use clear rhyme or slant rhyme, but do not force grammar.
- Keep verse lines singable: usually 6-12 syllables.
- Chorus lines can be shorter and more repeatable.

## Vocal Phrasing Rules

- Mark stressed syllables for the hook.
- Do not split connected English phrases unnaturally.
- Use breath before chorus/drop, not after every line.
- Use chant/shout for slogans, sung legato for emotional hooks.
- Highest chorus note should land on the strongest word, not on filler words like `the`, `a`, `to`, `and`.

## Vocal Range Defaults

- Female EDM/pop rock: A3-E5, occasional F5.
- Female cinematic rock: G3-D5, stronger chest/mix voice.
- Male rock: A2-E4, occasional F4.
- Male cinematic low: G2-D4.

## Chorus/Drop Rules

- First hook or riff within 0-5s.
- Main chorus/drop by 10-20s.
- Chorus/drop must lift with at least 3 of:
  - stronger drums
  - sub bass
  - distorted guitar
  - synth lead
  - vocal doubles/harmony
  - crash/impact
  - wider stereo
- Post-chorus should repeat the hook or riff for loopability.

## Prompt Fields

Always include:

```json
{
  "lyrics": "",
  "vocal": {
    "gender": "",
    "tone": "",
    "emotion": "",
    "range": ""
  },
  "lyric_phrasing": {
    "language": "English",
    "hook_line": "",
    "rhyme_scheme": "",
    "stressed_words": [],
    "breath_points": "",
    "avoid_high_note_words": ["the", "a", "to", "and", "of"]
  },
  "topline_plan": {
    "verse": "",
    "pre_chorus": "",
    "chorus": "",
    "post_chorus": "",
    "hook_motif": ""
  },
  "chorus_drop_plan": {
    "entry_time": "",
    "vocal_lift": "",
    "drums": "",
    "bass": "",
    "guitar_or_synth": "",
    "harmony": "",
    "second_hit": ""
  }
}
```

## Repair Rules

- Sounds like reading: shorten lines, add hook motif, reduce syllable density.
- Chorus weak: simplify hook, raise vocal intensity, add doubles/harmony and stronger drums.
- English awkward: rewrite natively, remove translation phrasing.
- Drop weak: add sub, crash, stronger snare/kick, guitar/synth layer.
- Vocal too high: lower key, narrow range, move high note to stronger vowel.
