# music-2.6 Prompt Templates

Core rule: never prompt music-2.6 with only a vague request such as `写一首伤感歌曲`. Use structured control:

```text
风格 + 情绪 + 节奏 + 调性 + 乐器 + 结构 + 人声 + 歌词 + 参考 + 质量 + 时长
```

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
    "emotion": "{演唱情绪}"
  },
  "lyrics": "{歌词内容}",
  "reference": "{参考风格/歌手，只做高层风格参考，不复制旋律歌词}",
  "quality": "high",
  "duration": "60-120s",
  "avoid": [
    "long intro",
    "muddy vocal",
    "generic melody",
    "over-complex arrangement",
    "copied melody",
    "unclear chorus",
    "weak first 5 seconds"
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
    "emotion": "heartbroken"
  },
  "lyrics": "{你的歌词}",
  "reference": "情绪流行, similar high-level energy to YOASOBI / Douyin sad pop, original melody and lyrics",
  "quality": "high",
  "duration": "60s"
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
    "emotion": "excited"
  },
  "lyrics": "{你的歌词}",
  "reference": "Douyin beat-sync BGM, original melody and lyrics",
  "quality": "high",
  "duration": "45-60s"
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
    "emotion": "hopeful sadness"
  },
  "lyrics": "{你的歌词}",
  "reference": "Japanese anime OP/ED high-level style, original melody and lyrics",
  "quality": "high",
  "duration": "60-90s"
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
    "emotion": "peaceful"
  },
  "lyrics": "",
  "reference": "lofi study music",
  "quality": "high",
  "duration": "90s"
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
    "emotion": "gentle"
  },
  "lyrics": "{原歌词或授权歌词；无授权时改写为原创歌词}",
  "reference": "acoustic cover style, original arrangement",
  "quality": "high",
  "duration": "60s"
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
