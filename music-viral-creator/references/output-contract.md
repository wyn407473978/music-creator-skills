# Output Contract

Use this template for English all-genre vocal song tasks.

## 0. Song Metadata

```json
{
  "project_id": "",
  "song_id": "",
  "title": "",
  "language": "English",
  "genre": "",
  "subgenre": "",
  "mood": "",
  "theme": "",
  "bpm": 0,
  "key": "",
  "duration": "",
  "version_name": "",
  "version_role": "main / alternate / demo / test",
  "hook_line": "",
  "target_platform": "",
  "usage_scene": "",
  "generation_status": "planned / prompt_ready / generated / published / archived"
}
```

## 1. 趋势抽象

- 样本说明：平台 / 时间 / 样本量 / 可信度
- 英文Hook类型：chant / slogan / emotional line / anthem chorus
- BPM规律：
- 结构规律：
- 声音主题：pop / rock / EDM / hip-hop / R&B / country / folk / indie / cinematic / lo-fi / dance
- 可复用结论：

## 2. 英文歌结构

```text
[0-5s] Hook：
目的：
歌词/声音动作：
剪辑用途：

[5-10s] Verse / Build：
目的：
歌词/声音动作：
剪辑用途：

[10-15s] Pre / Build / Drop Setup：
目的：
歌词/声音动作：
剪辑用途：

[15-25s] Chorus / Drop：
目的：
歌词/声音动作：
剪辑用途：

[25s+] Post-Chorus / Loop：
目的：
歌词/声音动作：
剪辑用途：
```

## 3. 英文歌词与Topline

```text
主题：
Hook line：
Verse：
Pre-Chorus：
Chorus：
Post-Chorus：
Rhyme scheme：
Stressed words：
Breath points：
Highest note word：
Caption line：
```

## 4. 编曲与高潮设计

```text
Drum groove：
Kick：
Snare/Clap：
Bass/Sub：
Lead instrument / Motif：
Build-up：
Chorus/Drop/Climax entry：
Second hit：
Mix direction：
```

## 5. music-2.6 Prompt

```json
{
  "song_metadata": {},
  "style": "",
  "mood": "",
  "bpm": 0,
  "key": "",
  "duration": "60-90s",
  "language": "English",
  "vocal": {
    "gender": "",
    "tone": "",
    "emotion": "",
    "range": ""
  },
  "lyrics": "",
  "lyric_phrasing": {
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
  "arrangement": {
    "drums": "",
    "bass": "",
    "chords": "",
    "lead_instrument": "",
    "texture": ""
  },
  "chorus_or_drop_plan": {
    "entry_time": "",
    "vocal_lift": "",
    "instrument_lift": "",
    "harmony": "",
    "second_hit": ""
  },
  "arrangement_arc": "",
  "edit_points": [],
  "mix": "",
  "quality": "high",
  "avoid": []
}
```

## 6. 成本控制与评分

```text
热度分：/10
趋势可信度：
爆款预测分：/50
是否生成：
生成数量：
原因：
```

评分维度：

- 前5秒Hook：/10
- 英文副歌记忆点：/10
- Chorus/Drop冲击：/10
- 剪辑适配：/10
- 平台适配：/10

## 7. A/B版本

```text
Version A: Pop Hook
Prompt：
Metadata：
Score：

Version B: Energetic / EDM / Rock
Prompt：
Metadata：
Score：

Version C: Emotional / R&B / Indie / Cinematic
Prompt：
Metadata：
Score：

推荐主推版本：
选择理由：
```

## 8. 节奏切片

```text
0-5s Hook：
10-15s Build/Drop：
20s Second Hit：
Loop点：
歌词字幕建议：
```

## 9. 发布与复盘

```text
标题：
封面文案：
置顶评论：
适配场景：
发布后关注数据：
- 完播：
- 重播：
- 收藏：
- 分享：
- Hook引用评论：
下一版调整：
```
