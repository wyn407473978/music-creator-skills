# music-2.6 Prompt Templates

Core rule: never prompt music-2.6 with only a vague request such as `写一首伤感歌曲`. Use structured control, and always align melody to the lyrics before generation:

```text
风格 + 情绪 + 节奏 + 调性 + 乐器 + 结构 + 人声 + 歌词韵律 + 旋律走向 + 情绪曲线 + 高潮设计 + 歌词 + 参考 + 质量 + 时长
```

Before using any template, create `lyric_prosody`, `melody_plan`, `emotional_arc`, and `climax_plan`. If the lyric is dense, reduce BPM or split the line. If the chorus has a golden line, place the highest note on the emotional keyword, not on weak particles such as 的、了、啊、吗.

## Standard Template

```json
{
  "style": "{音乐风格}",
  "mood": "{情绪}",
  "bpm": "{节奏速度}",
  "key": "{调性}",
  "structure": "{歌曲结构}",
  "instruments": ["{乐器1}", "{乐器2}"],
  "vocal": {
    "gender": "{male/female/none}",
    "tone": "{音色}",
    "emotion": "{演唱情绪}",
    "range": "{安全音域，例如 A3-E5；避免吃力高音}"
  },
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "{每句字数和节奏密度}",
    "stress_words": ["{必须落强拍的词}"],
    "breath_points": "{自然换气点}",
    "pronunciation": "clear Mandarin pronunciation, do not rush syllables"
  },
  "melody_plan": {
    "verse": "{主歌旋律走向}",
    "pre_chorus": "{预副歌如何上行铺垫}",
    "chorus": "{副歌最高音和金句如何对应}",
    "cadence": "{句尾如何解决}",
    "hook_motif": "{3-5个音的可哼唱动机说明}"
  },
  "emotional_arc": {
    "verse": "{主歌情绪强度与演唱方式}",
    "pre_chorus": "{预副歌如何制造紧张}",
    "chorus": "{副歌如何释放情绪}",
    "outro": "{高潮后如何收束}"
  },
  "climax_plan": {
    "entry_time": "{高潮进入时间，例如 15s}",
    "vocal_lift": "{副歌人声如何升高/加力}",
    "drums": "{鼓如何进入或加强}",
    "harmony": "{和声/叠唱如何增强}",
    "instrument_lift": "{钢琴/弦乐/合成器如何抬升}",
    "intensity_curve": "{verse 35%, pre-chorus 60%, chorus 90%, outro 55%}"
  },
  "arrangement_arc": "{从稀疏到高潮再回落的编曲层次}",
  "lyrics": "{歌词内容}",
  "reference": "{参考风格/歌手，只做高层风格参考，不复制旋律歌词}",
  "quality": "high",
  "duration": "60-120s",
  "singing_constraints": [
    "melody must follow lyric stress and sentence meaning",
    "keep pitch contour natural for Mandarin",
    "one syllable per note for dense Chinese lyric lines",
    "breathe at line breaks",
    "avoid random octave jumps",
    "avoid placing weak particles on the highest note",
    "make the chorus clearly more intense than the verse"
  ],
  "avoid": [
    "long intro",
    "muddy vocal",
    "generic melody",
    "over-complex arrangement",
    "copied melody",
    "unclear chorus",
    "weak first 5 seconds",
    "melody fighting the lyrics",
    "wrong lyric stress",
    "unnatural high notes",
    "rushed pronunciation",
    "flat emotional arc",
    "weak chorus lift",
    "same intensity throughout"
  ]
}
```

## Template 1: 抖音情绪爆款

Use for 失恋、回忆、深夜情绪号、伤感剧情剪辑.

```json
{
  "style": "pop ballad",
  "mood": "sad, emotional, nostalgic",
  "bpm": 85,
  "key": "C minor",
  "structure": "slow intro -> emotional build -> strong chorus at 15s",
  "instruments": ["piano", "strings", "soft drums"],
  "vocal": {
    "gender": "female",
    "tone": "soft, breathy",
    "emotion": "heartbroken",
    "range": "A3-E5, intimate and not strained"
  },
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "7-11 Chinese characters per phrase, do not rush",
    "stress_words": ["{歌词里的情绪关键词}"],
    "breath_points": "breathe after each lyric line",
    "pronunciation": "clear Mandarin, soft consonants, natural phrasing"
  },
  "melody_plan": {
    "verse": "low-mid register, speech-like and stepwise",
    "pre_chorus": "slowly rising emotional tension",
    "chorus": "highest note lands on the strongest sad keyword, repeatable hook motif",
    "cadence": "downward resolution at line endings",
    "hook_motif": "simple 3-5 note motif that follows the chorus golden line"
  },
  "emotional_arc": {
    "verse": "fragile and intimate, 35% intensity",
    "pre_chorus": "pain opens up, 60% intensity",
    "chorus": "heartbroken release, 90% intensity",
    "outro": "fall back to quiet regret, 55% intensity"
  },
  "climax_plan": {
    "entry_time": "15s",
    "vocal_lift": "chorus rises 3-5 semitones above verse, strongest word gets the highest note",
    "drums": "soft drums build before chorus, fuller downbeat at chorus",
    "harmony": "add subtle backing vocal/double on final chorus phrase",
    "instrument_lift": "strings swell and piano opens into higher octave",
    "intensity_curve": "verse 35%, pre-chorus 60%, chorus 90%, outro 55%"
  },
  "arrangement_arc": "piano and intimate vocal first, add strings in pre-chorus, full piano+strings+soft drums in chorus, strip back after climax",
  "lyrics": "{你的歌词}",
  "reference": "情绪流行, similar high-level energy to YOASOBI / Douyin sad pop, original melody and lyrics",
  "quality": "high",
  "duration": "60s",
  "singing_constraints": ["melody must follow lyric stress", "avoid random high notes", "avoid rushing Chinese syllables", "do not place weak particles on high notes", "chorus must feel emotionally bigger than verse"]
}
```

## Template 2: 短视频卡点爆款

Use for 剪辑视频、转场、节奏视频、舞蹈、燃向混剪.

```json
{
  "style": "electronic pop",
  "mood": "energetic, uplifting",
  "bpm": 110,
  "key": "A major",
  "structure": "fast intro -> drop at 10s -> repeatable hook",
  "instruments": ["synth", "bass", "kick"],
  "vocal": {
    "gender": "female",
    "tone": "bright",
    "emotion": "excited",
    "range": "B3-F5, bright but not shouted"
  },
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "short punchy phrases, 4-8 Chinese characters for hook lines",
    "stress_words": ["{卡点关键词}", "{动作关键词}"],
    "breath_points": "short breaths before drop and repeated hook",
    "pronunciation": "clear rhythmic Mandarin, tight consonants"
  },
  "melody_plan": {
    "verse": "short rhythmic notes, prepare for drop",
    "pre_chorus": "riser-like upward contour",
    "chorus": "repeatable hook on the drop, stable pitch center",
    "cadence": "clean cutoffs for edits",
    "hook_motif": "rhythmic 3-5 note motif matching kick/snare"
  },
  "emotional_arc": {
    "verse": "fast setup, 50% intensity",
    "pre_chorus": "rising excitement, 75% intensity",
    "chorus": "drop release, 95% intensity",
    "outro": "loopable energy, 70% intensity"
  },
  "climax_plan": {
    "entry_time": "10s",
    "vocal_lift": "hook becomes brighter and more projected on the drop",
    "drums": "kick and bass hit hard at drop",
    "harmony": "short vocal chops or doubles on hook",
    "instrument_lift": "synth/bass widen at drop",
    "intensity_curve": "intro 55%, build 75%, drop 95%, loop 75%"
  },
  "arrangement_arc": "tight intro, riser build, full synth+bass+kick drop, repeatable hook",
  "lyrics": "{你的歌词}",
  "reference": "Douyin beat-sync BGM, original melody and lyrics",
  "quality": "high",
  "duration": "45-60s",
  "singing_constraints": ["lyrics must lock to beat", "avoid dragging syllables across the drop", "keep hook easy to chant", "avoid over-high shouted notes", "drop must be clearly stronger than intro"]
}
```

## Template 3: 动漫风

Use for AI动漫视频、角色主题曲、青春成长、希望感伤.

```json
{
  "style": "anime pop",
  "mood": "emotional, dreamy",
  "bpm": 90,
  "key": "D minor",
  "structure": "piano intro -> build -> emotional chorus",
  "instruments": ["piano", "strings", "drums"],
  "vocal": {
    "gender": "female",
    "tone": "clear, youthful",
    "emotion": "hopeful sadness",
    "range": "B3-F5, youthful and clear, avoid repeated strained top notes"
  },
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "medium density, 7-10 Chinese characters per phrase",
    "stress_words": ["{角色情绪词}", "{希望/遗憾关键词}"],
    "breath_points": "breathe between scene line and emotional line",
    "pronunciation": "clear Mandarin with anime-pop brightness"
  },
  "melody_plan": {
    "verse": "gentle mid register, slightly floating",
    "pre_chorus": "clear upward lift into chorus",
    "chorus": "wide but singable emotional arc, highest note on the main character/emotion word",
    "cadence": "resolve with hopeful lift or soft fall",
    "hook_motif": "memorable 4-note anime-style motif"
  },
  "lyrics": "{你的歌词}",
  "reference": "Japanese anime OP/ED high-level style, original melody and lyrics",
  "quality": "high",
  "duration": "60-90s",
  "singing_constraints": ["do not overuse high notes", "keep Mandarin words intelligible", "melody follows character emotion", "avoid copied anime melody"]
}
```

## Template 4: LoFi 放松

Use for 学习、背景音乐、日常vlog、长尾流量.

```json
{
  "style": "lofi",
  "mood": "calm, relaxed",
  "bpm": 70,
  "key": "F major",
  "structure": "loopable chill pattern",
  "instruments": ["piano", "vinyl noise", "soft beat"],
  "vocal": {
    "gender": "none",
    "tone": "instrumental",
    "emotion": "peaceful",
    "range": "instrumental"
  },
  "lyric_prosody": {
    "language": "none",
    "line_density": "instrumental, no lyrics",
    "stress_words": [],
    "breath_points": "loop breathing every 4 or 8 bars",
    "pronunciation": "none"
  },
  "melody_plan": {
    "verse": "soft loopable piano motif",
    "pre_chorus": "none",
    "chorus": "subtle motif variation, no vocal peak",
    "cadence": "smooth loop resolution",
    "hook_motif": "simple 3-5 note instrumental motif"
  },
  "lyrics": "",
  "reference": "lofi study music",
  "quality": "high",
  "duration": "90s",
  "singing_constraints": ["instrumental only", "avoid vocal artifacts", "keep motif loopable"]
}
```

## Template 5: 翻唱改编

Use for AI翻唱、账号矩阵、爆款歌曲二次演绎. Only use original lyrics when the user owns or has licensed them; otherwise rewrite lyrics and keep only high-level style direction.

```json
{
  "style": "acoustic cover",
  "mood": "emotional",
  "bpm": 80,
  "key": "original",
  "structure": "simple guitar + vocal",
  "instruments": ["acoustic guitar"],
  "vocal": {
    "gender": "female",
    "tone": "warm",
    "emotion": "gentle",
    "range": "A3-D5, warm and conversational"
  },
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "natural cover phrasing, split long lyric lines",
    "stress_words": ["{授权歌词或改写歌词中的情绪关键词}"],
    "breath_points": "breathe at sentence boundaries",
    "pronunciation": "clear intimate Mandarin"
  },
  "melody_plan": {
    "verse": "simple near-speech melody",
    "pre_chorus": "small lift only if lyrics need it",
    "chorus": "gentle repeatable contour, avoid copying original melody",
    "cadence": "soft acoustic resolution",
    "hook_motif": "original 3-5 note motif, not the source melody"
  },
  "lyrics": "{原歌词或授权歌词；无授权时改写为原创歌词}",
  "reference": "acoustic cover style, original arrangement",
  "quality": "high",
  "duration": "60s",
  "singing_constraints": ["do not copy source melody", "melody must match rewritten lyric stress", "avoid unnatural high notes", "keep delivery intimate"]
}
```

## Selection Rules

- 伤感/失恋/回忆：start from Template 1.
- 卡点/剪辑/转场：start from Template 2.
- 动漫/角色/二次元：start from Template 3.
- 放松/学习/长尾BGM：start from Template 4.
- 翻唱/矩阵/改编：start from Template 5.
- If generating A/B versions, keep lyrics constant and vary `style`, `bpm`, `instruments`, `vocal`, and `structure`.
- For short-video virality, require a hook or drop before 15s; for emotional accounts, prefer chorus at 12-18s.
