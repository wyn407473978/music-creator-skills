# music-2.6 Instrumental Prompt Templates

Core rule: generate **pure instrumental DJ / rock / impact BGM**, not songs with lyrics.

Use structured control:

```text
style + mood + bpm + key + instruments + rhythm_design + riff_motif + drop_plan + arrangement_arc + edit_points + mix + avoid
```

## Standard Instrumental Template

```json
{
  "style": "{DJ / EDM / electronic rock / cinematic rock / hardstyle / phonk}",
  "mood": "{powerful, aggressive, epic, dark, energetic}",
  "bpm": 128,
  "key": "E minor",
  "duration": "45-60s",
  "instrumental_only": true,
  "vocals": "none, no lead vocal, no lyrics",
  "instruments": ["heavy kick", "snare", "sub bass", "distorted electric guitar", "synth lead", "riser", "impact FX"],
  "rhythm_design": {
    "drum_pattern": "four-on-floor or half-time rock hybrid",
    "kick": "punchy and sidechained",
    "snare_clap": "wide snare/clap on strong beats",
    "percussion": "snare roll before drop, crash at impact",
    "groove_feel": "tight, aggressive, edit-friendly"
  },
  "riff_motif": {
    "type": "distorted guitar riff + synth stab",
    "description": "short 1-2 bar original riff, memorable and loopable",
    "repeat_pattern": "repeat every 2 bars with small variation",
    "variation": "add octave layer at second hit"
  },
  "drop_plan": {
    "first_impact": "0-3s huge impact hit + riff preview",
    "build_up": "5-10s riser + snare roll + filter lift",
    "main_drop": "10-15s full drums + sub bass + guitar riff",
    "second_hit": "20s bigger crash + wider synth/guitar layer",
    "loop_point": "clean 4-bar loop ending"
  },
  "arrangement_arc": "impact intro -> build-up -> main drop -> bigger second hit -> loopable aftershock",
  "edit_points": [
    {"time": "0-3s", "cue": "impact hook", "use": "opening cut"},
    {"time": "10-15s", "cue": "main drop", "use": "transition / reveal"},
    {"time": "20s", "cue": "second hit", "use": "climax / speed ramp"}
  ],
  "mix": "loud, punchy, wide, heavy low end, clear kick/snare, no muddy low mids",
  "quality": "high",
  "avoid": [
    "lyrics",
    "lead vocal",
    "soft ballad",
    "long intro",
    "weak drop",
    "flat loop",
    "muddy bass",
    "generic melody",
    "copied riff",
    "overcrowded mix"
  ]
}
```

## Template 1: DJ震撼Drop

Use for festival, car edit, party, transformation, product reveal, fast cuts.

```json
{
  "style": "festival EDM, big room DJ instrumental",
  "mood": "explosive, powerful, energetic",
  "bpm": 128,
  "key": "E minor",
  "duration": "45-60s",
  "instrumental_only": true,
  "vocals": "none, only optional short crowd shout FX without words",
  "instruments": ["festival kick", "sub bass", "supersaw synth", "snare roll", "riser", "impact FX"],
  "rhythm_design": {
    "drum_pattern": "four-on-floor",
    "kick": "huge punchy kick on every beat",
    "snare_clap": "wide clap/snare on 2 and 4",
    "percussion": "fast snare roll and crash before drop",
    "groove_feel": "festival jump energy"
  },
  "riff_motif": {
    "type": "synth stab hook",
    "description": "short aggressive original synth motif",
    "repeat_pattern": "repeat every 2 bars",
    "variation": "add octave and wider stereo at 20s"
  },
  "drop_plan": {
    "first_impact": "0-3s impact + synth hook preview",
    "build_up": "5-10s riser + snare roll + filter opening",
    "main_drop": "10-15s full kick + bass + supersaw hook",
    "second_hit": "20s bigger impact + extra synth layer",
    "loop_point": "clean 4-bar ending"
  },
  "arrangement_arc": "instant hook -> rising tension -> huge drop -> second hit -> loop",
  "edit_points": [
    {"time": "0-3s", "cue": "impact hook", "use": "opening punch"},
    {"time": "10-15s", "cue": "drop", "use": "reveal / transition"},
    {"time": "20s", "cue": "second hit", "use": "climax cut"}
  ],
  "mix": "club loudness, heavy sub, sharp transient, wide synth, clean low mids",
  "quality": "high",
  "avoid": ["lyrics", "lead vocal", "weak drop", "soft intro", "flat loop", "muddy bass"]
}
```

## Template 2: 电子摇滚Riff

Use for game highlight, sports montage, battle scene, anime fight, speed ramp.

```json
{
  "style": "electronic rock instrumental, aggressive guitar and EDM drums",
  "mood": "intense, rebellious, powerful",
  "bpm": 140,
  "key": "D minor",
  "duration": "45-60s",
  "instrumental_only": true,
  "vocals": "none",
  "instruments": ["distorted electric guitar", "power chords", "electronic drums", "sub bass", "synth bass", "crash cymbal", "impact FX"],
  "rhythm_design": {
    "drum_pattern": "half-time rock groove with electronic kick",
    "kick": "deep punchy kick locked with guitar chugs",
    "snare_clap": "heavy snare on backbeat",
    "percussion": "tom fill before drop, crash on riff entry",
    "groove_feel": "tight aggressive rock energy"
  },
  "riff_motif": {
    "type": "distorted guitar riff",
    "description": "original 1-bar palm-muted riff with power chord answer",
    "repeat_pattern": "riff repeats every 2 bars",
    "variation": "add octave guitar and synth bass at 20s"
  },
  "drop_plan": {
    "first_impact": "0-3s guitar scrape + impact hit",
    "build_up": "5-10s palm-muted chugs + riser",
    "main_drop": "10-15s full guitar riff + drums + sub bass",
    "second_hit": "20s bigger riff variation + crash",
    "loop_point": "riff resolves cleanly for loop"
  },
  "arrangement_arc": "guitar impact -> chug build -> riff drop -> heavier second hit -> loopable riff",
  "edit_points": [
    {"time": "0-3s", "cue": "guitar impact", "use": "fight opening"},
    {"time": "10-15s", "cue": "riff drop", "use": "action transition"},
    {"time": "20s", "cue": "second riff hit", "use": "KO / speed ramp"}
  ],
  "mix": "wide guitars, punchy drums, controlled low end, aggressive but not muddy",
  "quality": "high",
  "avoid": ["lyrics", "lead vocal", "copied guitar riff", "thin guitars", "weak snare", "muddy low mids"]
}
```

## Template 3: 电影预告燃向摇滚

Use for trailer, heroic reveal, sports, epic montage, product launch.

```json
{
  "style": "cinematic trailer rock instrumental",
  "mood": "epic, heroic, dramatic, powerful",
  "bpm": 100,
  "key": "E minor",
  "duration": "60s",
  "instrumental_only": true,
  "vocals": "none, optional wordless choir texture only",
  "instruments": ["taiko drums", "cinematic toms", "distorted guitar", "orchestral strings", "brass hits", "sub boom", "impact FX"],
  "rhythm_design": {
    "drum_pattern": "half-time cinematic rock",
    "kick": "deep trailer boom layered with kick",
    "snare_clap": "huge snare/tom hits",
    "percussion": "rising tom pattern before climax",
    "groove_feel": "massive heroic march"
  },
  "riff_motif": {
    "type": "guitar + brass heroic motif",
    "description": "short original heroic motif answered by guitar power chords",
    "repeat_pattern": "motif repeats with larger orchestration",
    "variation": "add choir/brass layer at 20s"
  },
  "drop_plan": {
    "first_impact": "0-5s huge trailer hit + low guitar",
    "build_up": "5-12s toms + strings rising",
    "main_drop": "12-15s full drums + guitar + brass",
    "second_hit": "20s biggest trailer impact",
    "loop_point": "dramatic tail with clean re-entry"
  },
  "arrangement_arc": "massive hit -> cinematic build -> heroic drop -> second impact -> trailer tail",
  "edit_points": [
    {"time": "0-5s", "cue": "trailer hit", "use": "title reveal"},
    {"time": "12-15s", "cue": "heroic drop", "use": "main reveal"},
    {"time": "20s", "cue": "biggest impact", "use": "final transformation"}
  ],
  "mix": "cinematic wide mix, huge impacts, clear drums, controlled sub boom",
  "quality": "high",
  "avoid": ["lyrics", "lead vocal", "small drums", "weak impact", "thin guitars", "flat trailer loop"]
}
```

## Template 4: 黑暗赛博重低音

Use for night city, tech, car, cyberpunk, villain, dark product reveal.

```json
{
  "style": "dark cyberpunk bass instrumental, industrial EDM rock",
  "mood": "dark, futuristic, heavy, dangerous",
  "bpm": 132,
  "key": "F minor",
  "duration": "45-60s",
  "instrumental_only": true,
  "vocals": "none, optional robotic FX without words",
  "instruments": ["industrial kick", "distorted bass", "metallic percussion", "dark synth lead", "electric guitar texture", "riser", "impact FX"],
  "rhythm_design": {
    "drum_pattern": "heavy four-on-floor with industrial percussion",
    "kick": "deep distorted kick",
    "snare_clap": "metallic snare hit",
    "percussion": "glitch fills and reverse impacts",
    "groove_feel": "dark mechanical drive"
  },
  "riff_motif": {
    "type": "distorted bass motif",
    "description": "short dark original bass pattern with synth stab answer",
    "repeat_pattern": "repeat every 2 bars",
    "variation": "add harsher distortion at second hit"
  },
  "drop_plan": {
    "first_impact": "0-3s sub boom + metallic hit",
    "build_up": "5-10s filter rise + glitch percussion",
    "main_drop": "10-15s distorted bass + kick + dark synth",
    "second_hit": "20s heavier bass distortion and impact",
    "loop_point": "dark 4-bar loop"
  },
  "arrangement_arc": "sub impact -> mechanical build -> dark bass drop -> heavier second hit -> loop",
  "edit_points": [
    {"time": "0-3s", "cue": "sub boom", "use": "dark opening"},
    {"time": "10-15s", "cue": "bass drop", "use": "car/tech reveal"},
    {"time": "20s", "cue": "distortion hit", "use": "villain/impact cut"}
  ],
  "mix": "heavy sub, gritty distortion, clear kick, wide dark synth, no muddy low mids",
  "quality": "high",
  "avoid": ["lyrics", "lead vocal", "happy pop", "weak bass", "muddy distortion", "flat loop"]
}
```

## Template 5: 硬核摇滚鼓点卡点

Use for gym, fight, extreme sports, speed edits, mechanical edits.

```json
{
  "style": "hard rock instrumental with punchy breakbeat",
  "mood": "raw, aggressive, high-adrenaline",
  "bpm": 150,
  "key": "A minor",
  "duration": "45-60s",
  "instrumental_only": true,
  "vocals": "none",
  "instruments": ["distorted guitar", "live rock drums", "breakbeat layer", "bass guitar", "crash cymbals", "riser", "impact FX"],
  "rhythm_design": {
    "drum_pattern": "rock drums with breakbeat fills",
    "kick": "fast punchy kick",
    "snare_clap": "cracking rock snare",
    "percussion": "snare fills and crash hits for cuts",
    "groove_feel": "driving and physical"
  },
  "riff_motif": {
    "type": "power chord riff",
    "description": "short original power chord riff with syncopated rests",
    "repeat_pattern": "repeat with drum fills every 4 bars",
    "variation": "add lead guitar stab at second hit"
  },
  "drop_plan": {
    "first_impact": "0-3s drum fill + guitar hit",
    "build_up": "5-10s snare fill + rising guitar noise",
    "main_drop": "10-15s full riff + breakbeat drums",
    "second_hit": "20s crash + lead guitar stab",
    "loop_point": "riff loop ending"
  },
  "arrangement_arc": "drum/guitar hit -> snare build -> riff drop -> second crash -> loop",
  "edit_points": [
    {"time": "0-3s", "cue": "drum fill hit", "use": "opening action"},
    {"time": "10-15s", "cue": "riff drop", "use": "main movement"},
    {"time": "20s", "cue": "crash + guitar stab", "use": "impact frame"}
  ],
  "mix": "raw guitars, cracking snare, punchy kick, energetic stereo, no vocal",
  "quality": "high",
  "avoid": ["lyrics", "lead vocal", "soft ballad", "weak drums", "copied riff", "loose timing"]
}
```

## Selection Rules

- 车、派对、转场、产品揭示：Template 1.
- 游戏、战斗、燃剪、运动：Template 2 or 5.
- 电影感、英雄感、大场面：Template 3.
- 赛博、暗黑、科技、夜景：Template 4.
- 健身、极限运动、硬核剪辑：Template 5.

For A/B tests, keep the same concept and vary `style`, `bpm`, `riff_motif`, `drop_plan`, and `mix`.
