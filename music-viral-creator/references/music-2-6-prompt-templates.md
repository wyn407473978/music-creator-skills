# music-2.6 English Song Prompt Templates

Core rule: generate **English vocal songs** with DJ/rock energy, not Chinese lyrics and not pure instrumental unless requested.

Use structured control:

```text
style + mood + bpm + key + vocal + lyrics + lyric_phrasing + rhythm_design + riff_motif + chorus_drop_plan + arrangement_arc + edit_points + mix + avoid
```

## Standard English Song Template

```json
{
  "style": "EDM rock / pop rock / cinematic rock",
  "mood": "powerful, emotional, anthemic",
  "bpm": 128,
  "key": "E minor",
  "duration": "60-90s",
  "language": "English",
  "vocal": {
    "gender": "female or male",
    "tone": "powerful, clear, modern",
    "emotion": "determined, emotional, explosive",
    "range": "A3-E5 female / A2-E4 male"
  },
  "lyrics": "{English lyrics here}",
  "lyric_phrasing": {
    "hook_line": "{short repeatable English hook}",
    "rhyme_scheme": "simple pop rhyme or slant rhyme",
    "stressed_words": ["{hook keyword}"],
    "breath_points": "short breath before chorus/drop, no hard pause after every line",
    "avoid_high_note_words": ["the", "a", "to", "and", "of"]
  },
  "topline_plan": {
    "verse": "lower, rhythmic, natural English phrasing",
    "pre_chorus": "rising tension",
    "chorus": "big melodic hook, strongest word gets highest note",
    "post_chorus": "repeat hook or chant",
    "hook_motif": "3-5 note repeatable vocal motif"
  },
  "rhythm_design": {
    "drum_pattern": "EDM-rock hybrid",
    "kick": "punchy",
    "snare_clap": "wide snare/clap",
    "percussion": "snare build before chorus/drop",
    "groove_feel": "tight, driving, edit-friendly"
  },
  "riff_motif": {
    "type": "guitar riff or synth hook",
    "description": "short original motif supporting the vocal hook",
    "repeat_pattern": "repeat every 2 bars",
    "variation": "bigger layer at second hit"
  },
  "chorus_drop_plan": {
    "entry_time": "15s",
    "vocal_lift": "chorus rises above verse with stronger projection",
    "drums": "full drums enter at chorus/drop",
    "bass": "sub bass supports downbeat",
    "guitar_or_synth": "distorted guitar or wide synth hook opens up",
    "harmony": "add vocal doubles/harmony on hook",
    "second_hit": "20s bigger crash and repeated hook"
  },
  "arrangement_arc": "hook intro -> verse/build -> pre-chorus lift -> chorus/drop -> post-chorus hook",
  "edit_points": [
    {"time": "0-5s", "cue": "vocal/riff hook", "use": "opening"},
    {"time": "10-15s", "cue": "build/drop", "use": "transition"},
    {"time": "20s", "cue": "second hit", "use": "climax"}
  ],
  "mix": "loud, punchy, wide, clear vocal, heavy drums, controlled low end",
  "quality": "high",
  "avoid": [
    "Chinese lyrics",
    "awkward translated English",
    "spoken recitation",
    "weak chorus",
    "late drop",
    "flat arrangement",
    "muddy vocal",
    "copied melody",
    "copied riff"
  ]
}
```

## Template 1: EDM Rock Anthem

Use for sports, game highlight, transformation, fast edits.

```json
{
  "style": "EDM rock anthem, English vocal",
  "mood": "powerful, victorious, explosive",
  "bpm": 128,
  "key": "E minor",
  "duration": "60s",
  "language": "English",
  "vocal": {
    "gender": "female",
    "tone": "clear, powerful, modern",
    "emotion": "unstoppable",
    "range": "A3-E5"
  },
  "lyrics": "Verse: We light the dark, we break the line\nPre: Feel the thunder getting closer\nChorus: We rise, we burn, we own the night\nPost: Own the night, own the night",
  "lyric_phrasing": {
    "hook_line": "We own the night",
    "rhyme_scheme": "simple anthem rhyme",
    "stressed_words": ["rise", "burn", "own", "night"],
    "breath_points": "breath before chorus, connect short hook phrases",
    "avoid_high_note_words": ["the", "we"]
  },
  "topline_plan": {
    "verse": "low-mid rhythmic vocal",
    "pre_chorus": "rising melody and tension",
    "chorus": "big hook, highest note on 'night'",
    "post_chorus": "chant repeat of hook",
    "hook_motif": "4-note rising anthem motif"
  },
  "rhythm_design": {
    "drum_pattern": "four-on-floor EDM rock",
    "kick": "punchy sidechained kick",
    "snare_clap": "wide clap/snare",
    "percussion": "snare roll before chorus",
    "groove_feel": "festival rock energy"
  },
  "riff_motif": {
    "type": "distorted guitar + synth stab",
    "description": "original 2-bar riff supporting the hook",
    "repeat_pattern": "repeat every chorus",
    "variation": "add octave layer at second hit"
  },
  "chorus_drop_plan": {
    "entry_time": "15s",
    "vocal_lift": "bigger belted chorus",
    "drums": "full kick/snare at chorus",
    "bass": "sub bass hits with downbeat",
    "guitar_or_synth": "wide guitar and supersaw open",
    "harmony": "vocal doubles on 'own the night'",
    "second_hit": "20s crash + hook repeat"
  },
  "arrangement_arc": "hook preview -> verse -> rising pre -> chorus/drop -> chant hook",
  "edit_points": [
    {"time": "0-5s", "cue": "hook preview", "use": "opening"},
    {"time": "15s", "cue": "chorus/drop", "use": "main reveal"},
    {"time": "20s", "cue": "hook repeat", "use": "climax"}
  ],
  "mix": "clear lead vocal, loud drums, wide guitars/synths, heavy but clean bass",
  "quality": "high",
  "avoid": ["Chinese lyrics", "weak chorus", "spoken vocal", "late drop", "copied melody"]
}
```

## Template 2: Pop Rock Heartbreak

Use for emotional edits, night drive, relationship story, cinematic short video.

```json
{
  "style": "English pop rock, emotional EDM-rock chorus",
  "mood": "heartbroken, cinematic, powerful",
  "bpm": 96,
  "key": "B minor",
  "duration": "60-90s",
  "language": "English",
  "vocal": {
    "gender": "female",
    "tone": "warm, emotional, strong chorus",
    "emotion": "heartbroken but rising",
    "range": "G3-D5"
  },
  "lyrics": "Verse: I kept your ghost in the passenger seat\nPre: Every red light brings you back to me\nChorus: I still hear you in the rain\nPost: In the rain, in the rain",
  "lyric_phrasing": {
    "hook_line": "I still hear you in the rain",
    "rhyme_scheme": "emotional slant rhyme",
    "stressed_words": ["still", "hear", "rain"],
    "breath_points": "soft breath before chorus, connect emotional phrases",
    "avoid_high_note_words": ["you", "in", "the"]
  },
  "topline_plan": {
    "verse": "intimate lower vocal",
    "pre_chorus": "gradual lift",
    "chorus": "wide emotional melody, highest note on 'rain'",
    "post_chorus": "repeat final phrase softly",
    "hook_motif": "falling 4-note emotional motif"
  },
  "rhythm_design": {
    "drum_pattern": "half-time pop rock",
    "kick": "warm deep kick",
    "snare_clap": "big emotional snare",
    "percussion": "subtle tom fill into chorus",
    "groove_feel": "cinematic night drive"
  },
  "riff_motif": {
    "type": "clean guitar arpeggio into distorted chorus",
    "description": "simple original guitar motif",
    "repeat_pattern": "verse arpeggio, chorus power chords",
    "variation": "add octave guitar at second chorus hit"
  },
  "chorus_drop_plan": {
    "entry_time": "18s",
    "vocal_lift": "chorus opens with stronger chest/mix voice",
    "drums": "full snare and crash at chorus",
    "bass": "warm bass follows root motion",
    "guitar_or_synth": "distorted guitar widens chorus",
    "harmony": "soft harmony on final hook phrase",
    "second_hit": "22s extra crash and guitar layer"
  },
  "arrangement_arc": "intimate verse -> emotional lift -> rock chorus -> soft post-hook",
  "edit_points": [
    {"time": "0-5s", "cue": "guitar/vocal mood hook", "use": "opening"},
    {"time": "18s", "cue": "chorus lift", "use": "memory reveal"},
    {"time": "22s", "cue": "second hit", "use": "emotional climax"}
  ],
  "mix": "front vocal, warm guitars, big snare, clean bass, cinematic width",
  "quality": "high",
  "avoid": ["Chinese lyrics", "awkward English", "flat chorus", "overcrowded vocal", "copied melody"]
}
```

## Template 3: Cinematic Trailer Rock Song

Use for trailer, heroic reveal, product launch, sports montage.

```json
{
  "style": "cinematic trailer rock with English vocal hook",
  "mood": "epic, heroic, dramatic",
  "bpm": 100,
  "key": "D minor",
  "duration": "60s",
  "language": "English",
  "vocal": {
    "gender": "male",
    "tone": "deep, powerful, cinematic",
    "emotion": "heroic",
    "range": "A2-E4"
  },
  "lyrics": "Verse: We were born from the fire\nPre: Hear the drums call our name\nChorus: We are legends tonight\nPost: Legends tonight",
  "lyric_phrasing": {
    "hook_line": "We are legends tonight",
    "rhyme_scheme": "anthemic simple rhyme",
    "stressed_words": ["legends", "tonight"],
    "breath_points": "strong breath before chorus",
    "avoid_high_note_words": ["we", "are"]
  },
  "topline_plan": {
    "verse": "low cinematic vocal",
    "pre_chorus": "rising chant-like delivery",
    "chorus": "big heroic hook, highest note on 'tonight'",
    "post_chorus": "choir-like repeat",
    "hook_motif": "bold 3-note heroic motif"
  },
  "rhythm_design": {
    "drum_pattern": "half-time trailer rock",
    "kick": "deep trailer boom",
    "snare_clap": "huge cinematic snare",
    "percussion": "toms rising into chorus",
    "groove_feel": "massive heroic march"
  },
  "riff_motif": {
    "type": "guitar + brass motif",
    "description": "original heroic motif supporting vocal hook",
    "repeat_pattern": "repeat with larger orchestration",
    "variation": "add choir/brass at 20s"
  },
  "chorus_drop_plan": {
    "entry_time": "15s",
    "vocal_lift": "heroic chorus projection",
    "drums": "full trailer drums",
    "bass": "sub boom on downbeat",
    "guitar_or_synth": "wide guitar and brass hits",
    "harmony": "choir texture under hook",
    "second_hit": "20s biggest trailer impact"
  },
  "arrangement_arc": "dark verse -> drum build -> heroic chorus/drop -> choir post-hook",
  "edit_points": [
    {"time": "0-5s", "cue": "deep vocal/trailer hit", "use": "title reveal"},
    {"time": "15s", "cue": "heroic chorus", "use": "main reveal"},
    {"time": "20s", "cue": "biggest hit", "use": "final transformation"}
  ],
  "mix": "huge cinematic drums, clear male vocal, wide guitars/brass, controlled sub",
  "quality": "high",
  "avoid": ["Chinese lyrics", "thin vocal", "weak trailer impact", "copied melody", "flat chorus"]
}
```

## Selection Rules

- Sports/game/transformation: Template 1.
- Emotional/night/relationship: Template 2.
- Trailer/heroic/product reveal: Template 3.
- For more rock: increase distorted guitars, live drums, lower BPM or half-time feel.
- For more DJ: increase four-on-floor kick, synth lead, riser, sidechain bass.
