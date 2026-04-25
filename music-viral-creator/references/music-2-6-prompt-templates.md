# music-2.6 English All-Genre Song Prompt Templates

Core rule: generate **English vocal songs across genres**, not only DJ/Rock. Always include `song_metadata`.

Use structured control:

```text
song_metadata + style + mood + bpm + key + vocal + lyrics + lyric_phrasing + rhythm_design + arrangement + chorus_or_drop_plan + edit_points + mix + avoid
```

## Standard English Song Template

```json
{
  "song_metadata": {
    "project_id": "{project id}",
    "song_id": "{song id}",
    "title": "{song title}",
    "language": "English",
    "genre": "{Pop / Rock / EDM / Hip-hop / R&B / Country / Folk / Indie / Cinematic / Lo-fi / Dance}",
    "subgenre": "{specific subgenre}",
    "mood": "{emotional mood}",
    "theme": "{song theme}",
    "bpm": 0,
    "key": "{key}",
    "duration": "60-90s",
    "version_name": "{version name}",
    "version_role": "main",
    "hook_line": "{short repeatable English hook}",
    "target_platform": "{TikTok / Reels / Shorts / Xiaohongshu / Bilibili}",
    "usage_scene": "{edit scene}",
    "generation_status": "prompt_ready"
  },
  "style": "{genre and style}",
  "mood": "{mood}",
  "bpm": 0,
  "key": "{key}",
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
  "arrangement": {
    "drums": "{genre-appropriate drums}",
    "bass": "{bass movement}",
    "chords": "{chord progression}",
    "lead_instrument": "{piano / guitar / synth / strings / 808 / etc.}",
    "texture": "{pads / acoustic / distorted / warm / cinematic}"
  },
  "chorus_or_drop_plan": {
    "entry_time": "15s",
    "vocal_lift": "{how chorus lifts}",
    "instrument_lift": "{how arrangement gets bigger}",
    "harmony": "add vocal doubles/harmony on hook",
    "second_hit": "20s repeated hook or bigger moment"
  },
  "arrangement_arc": "hook intro -> verse -> pre-chorus/build -> chorus/drop -> post-chorus hook",
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
    "late hook",
    "flat arrangement",
    "muddy vocal",
    "copied melody",
    "copied riff"
  ]
}
```

## Template 1: Pop Hook

Use for broad short-video appeal, lifestyle, travel, beauty, emotional but accessible content.

```json
{
  "song_metadata": {
    "project_id": "bright-night-pop",
    "song_id": "bright-night-pop-vA",
    "title": "Bright Tonight",
    "language": "English",
    "genre": "Pop",
    "subgenre": "Dance Pop",
    "mood": "bright, confident, catchy",
    "theme": "living in the moment",
    "bpm": 118,
    "key": "A major",
    "duration": "60s",
    "version_name": "Pop Hook Version",
    "version_role": "main",
    "hook_line": "We shine so bright tonight",
    "target_platform": "TikTok / Reels / Shorts",
    "usage_scene": "lifestyle, travel, transformation",
    "generation_status": "prompt_ready"
  },
  "style": "modern English dance pop",
  "mood": "bright, catchy, uplifting",
  "bpm": 118,
  "key": "A major",
  "duration": "60s",
  "language": "English",
  "vocal": {
    "gender": "female",
    "tone": "clear, powerful, modern",
    "emotion": "unstoppable",
    "range": "A3-E5"
  },
  "lyrics": "Verse: City lights are waking up with me\nPre: I feel the rhythm underneath my feet\nChorus: We shine so bright tonight\nPost: So bright, so bright tonight",
  "lyric_phrasing": {
    "hook_line": "We shine so bright tonight",
    "rhyme_scheme": "simple anthem rhyme",
    "stressed_words": ["shine", "bright", "tonight"],
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
  "arrangement": {
    "drums": "clean dance-pop groove",
    "bass": "warm sidechain bass",
    "chords": "bright pop progression",
    "lead_instrument": "plucky synth hook",
    "texture": "wide modern pop pads"
  },
  "chorus_or_drop_plan": {
    "entry_time": "15s",
    "vocal_lift": "chorus becomes brighter and more open",
    "instrument_lift": "bigger drums, bass, and synth hook",
    "harmony": "vocal doubles on hook",
    "second_hit": "20s crash + hook repeat"
  },
  "arrangement_arc": "hook preview -> light verse -> pre lift -> bright chorus -> post hook",
  "edit_points": [
    {"time": "0-5s", "cue": "hook preview", "use": "opening"},
    {"time": "15s", "cue": "chorus/drop", "use": "main reveal"},
    {"time": "20s", "cue": "hook repeat", "use": "climax"}
  ],
  "mix": "clear lead vocal, polished pop drums, wide synths, controlled bass",
  "quality": "high",
  "avoid": ["Chinese lyrics", "weak chorus", "spoken vocal", "late drop", "copied melody"]
}
```

## Template 2: R&B / Pop Heartbreak

Use for emotional edits, night drive, relationship story, cinematic short video.

```json
{
  "song_metadata": {
    "project_id": "rain-memory-rnb",
    "song_id": "rain-memory-rnb-vA",
    "title": "In The Rain",
    "language": "English",
    "genre": "R&B",
    "subgenre": "Alternative R&B Pop",
    "mood": "heartbroken, intimate, cinematic",
    "theme": "missing someone after love ends",
    "bpm": 86,
    "key": "B minor",
    "duration": "75s",
    "version_name": "Late Night R&B Version",
    "version_role": "main",
    "hook_line": "I still hear you in the rain",
    "target_platform": "TikTok / Reels / Shorts",
    "usage_scene": "night drive, breakup edit, memory video",
    "generation_status": "prompt_ready"
  },
  "style": "English alternative R&B pop",
  "mood": "heartbroken, cinematic, powerful",
  "bpm": 86,
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
  "arrangement": {
    "drums": "slow half-time R&B drums",
    "bass": "warm sub bass following emotional root movement",
    "chords": "minor seventh emotional progression",
    "lead_instrument": "soft electric piano and ambient guitar",
    "texture": "late-night pads and reverb"
  },
  "chorus_or_drop_plan": {
    "entry_time": "18s",
    "vocal_lift": "chorus opens with stronger chest/mix voice",
    "instrument_lift": "wider pads, stronger snare, warmer bass",
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
  "song_metadata": {
    "project_id": "legends-tonight-trailer",
    "song_id": "legends-tonight-trailer-vA",
    "title": "Legends Tonight",
    "language": "English",
    "genre": "Cinematic",
    "subgenre": "Trailer Rock",
    "mood": "epic, heroic, dramatic",
    "theme": "becoming legendary",
    "bpm": 100,
    "key": "D minor",
    "duration": "60s",
    "version_name": "Trailer Rock Version",
    "version_role": "main",
    "hook_line": "We are legends tonight",
    "target_platform": "TikTok / Reels / Shorts / Bilibili",
    "usage_scene": "heroic reveal, sports montage, trailer",
    "generation_status": "prompt_ready"
  },
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
  "arrangement": {
    "drums": "half-time trailer drums with toms",
    "bass": "sub boom on downbeats",
    "chords": "dark heroic minor progression",
    "lead_instrument": "electric guitar and brass motif",
    "texture": "cinematic strings and choir pad"
  },
  "chorus_or_drop_plan": {
    "entry_time": "15s",
    "vocal_lift": "heroic chorus projection",
    "instrument_lift": "full trailer drums, guitar, brass, strings",
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

## Template 4: Country Folk Story

Use for storytelling, road trip, warm lifestyle, emotional memory.

```json
{
  "song_metadata": {
    "project_id": "back-road-home",
    "song_id": "back-road-home-vA",
    "title": "Back Road Home",
    "language": "English",
    "genre": "Country",
    "subgenre": "Country Folk Pop",
    "mood": "warm, nostalgic, honest",
    "theme": "coming home and remembering where you belong",
    "bpm": 92,
    "key": "G major",
    "duration": "75s",
    "version_name": "Country Folk Version",
    "version_role": "main",
    "hook_line": "Take me down that back road home",
    "target_platform": "TikTok / Reels / Shorts",
    "usage_scene": "road trip, family, memory, countryside",
    "generation_status": "prompt_ready"
  },
  "style": "English country folk pop",
  "mood": "warm, nostalgic, heartfelt",
  "bpm": 92,
  "key": "G major",
  "duration": "75s",
  "language": "English",
  "vocal": {
    "gender": "male",
    "tone": "warm, honest, slightly raspy",
    "emotion": "nostalgic",
    "range": "A2-D4"
  },
  "lyrics": "Verse: Dust on my boots and gold in the sky\nPre: Every mile still knows my name\nChorus: Take me down that back road home\nPost: Back road home, back road home",
  "lyric_phrasing": {
    "hook_line": "Take me down that back road home",
    "rhyme_scheme": "simple country rhyme",
    "stressed_words": ["take", "back", "road", "home"],
    "breath_points": "natural breath at sentence endings",
    "avoid_high_note_words": ["me", "that"]
  },
  "topline_plan": {
    "verse": "conversational and warm",
    "pre_chorus": "slight lift",
    "chorus": "open singalong hook",
    "post_chorus": "soft repeat",
    "hook_motif": "simple 4-note singalong motif"
  },
  "arrangement": {
    "drums": "soft country groove",
    "bass": "warm acoustic bass",
    "chords": "G-D-Em-C style warm progression",
    "lead_instrument": "acoustic guitar and light pedal steel",
    "texture": "organic, warm, not overproduced"
  },
  "chorus_or_drop_plan": {
    "entry_time": "18s",
    "vocal_lift": "chorus opens into a singalong",
    "instrument_lift": "add harmony, light drums, wider acoustic guitar",
    "harmony": "simple country harmony on hook",
    "second_hit": "24s repeat hook with harmony"
  },
  "arrangement_arc": "warm guitar intro -> story verse -> lifted chorus -> soft hook repeat",
  "edit_points": [
    {"time": "0-5s", "cue": "acoustic hook", "use": "warm opening"},
    {"time": "18s", "cue": "chorus hook", "use": "memory reveal"},
    {"time": "24s", "cue": "harmony repeat", "use": "emotional close"}
  ],
  "mix": "warm vocal, acoustic guitar upfront, soft drums, organic space",
  "quality": "high",
  "avoid": ["Chinese lyrics", "fake country accent", "overly EDM drums", "awkward English"]
}
```

## Selection Rules

- Broad catchy short-video pop: Template 1.
- Emotional/night/relationship/R&B: Template 2.
- Trailer/heroic/product reveal: Template 3.
- Warm story/road/family/country: Template 4.
- For more rock: increase distorted guitars, live drums, lower BPM or half-time feel.
- For more DJ: increase four-on-floor kick, synth lead, riser, sidechain bass.
