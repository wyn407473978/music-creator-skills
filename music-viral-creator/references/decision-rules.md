# Decision Rules

Use these rules to reduce subjective decisions in market analysis, cost control, viral decisions, cold-start testing, hit-pattern cloning, rhythm slicing, A/B testing, post-publish iteration, and comment/heat learning.

## Heat Score

Calculate `热度分` out of 10:

```text
热度分 =
平台热度 * 0.30 +
近期增长 * 0.25 +
评论共鸣 * 0.20 +
可改编性 * 0.15 +
竞争拥挤度反向 * 0.10
```

Score each sub-item from 0-10:

- 平台热度：chart position, usage count, search volume, playlist/chart presence.
- 近期增长：7-day or recent rise; if unknown, mark confidence lower.
- 评论共鸣：comments contain personal stories, quotes, repeat requests, or emotional identification.
- 可改编性：can become piano, LoFi, anime, electronic, cover, or UGC versions.
- 竞争拥挤度反向：10 means still open/less crowded; 0 means overly saturated.

Confidence:

- 高：50+ samples or clear multi-platform evidence.
- 中：15-49 samples or one strong platform signal.
- 低：fewer than 15 samples or mostly intuition.

## Cost Gate

- `热度分 < 6` or confidence low: do not generate full music.
- `热度分 6-7`: generate lyrics, prompt, and optionally one 15-second demo only.
- `热度分 >= 7` and viral score >= 32/50: generate A/B versions.
- Any copyright/similarity risk high: stop generation until rewritten or licensed.

## Viral Decision Engine

After viral scoring, apply this hard rule:

```text
if 爆款评分 < 30:
    不生成音乐
elif 爆款评分 >= 30 and 爆款评分 <= 40:
    只生成1个版本
else:
    生成3个版本 + 推流测试
```

Overrides:

- High copyright/similarity risk: do not generate.
- Cold-start first 100 posts: do not kill style lanes too early; generate low-cost tests for coverage.
- Budget pressure: if score 30-40, generate a 15-30s test version before full song.

## Cold-Start Strategy

Use when the account has fewer than 100 published pieces or no stable performance history.

- First 100 pieces are for data collection.
- Force style coverage: emotional piano, anime pop, electronic beat-sync, LoFi, cover/remix-inspired original.
- Do not permanently kill a lane from fewer than 10 tests.
- Keep generation cheap: short versions, one version per concept, no heavy push unless early data is unusually strong.
- After 100 pieces, summarize winning emotion, voice, BPM, structure, video scene, and copy angle.

## Hit-Pattern Cloning

When given a viral song/audio, extract the pattern but generate original works.

Extract:

- Emotion
- BPM
- Key
- Hook timing
- 0-30s structure
- Lyric theme and sentence style
- Vocal timbre
- Instrument palette
- Video scenes using the audio

Generate 3 same-class original works:

- Keep: emotional function, approximate BPM band, hook timing, scene use.
- Change: lyrics, melody, title, story angle, arrangement details, vocal identity.
- Always run similarity risk check.

## Rhythm Slicing Rules

Output slices for editing systems:

- `0-5s`: Hook point; must contain vocal, melody motif, sound logo, or lyric line.
- `10-15s`: beat-sync or transition point; use drum entry, bass hit, lyric turn, or riser.
- `20s`: chorus peak; use strongest lyric/beat/emotional lift.

Each slice must include:

- Timestamp
- Beat/musical action
- Lyric cue
- Visual cue
- Editor instruction

## Viral Scoring Anchors

Score 0-10 for each dimension:

- 8-10: strong, immediately usable, clear viral signal.
- 5-7: usable but needs sharpening.
- 0-4: weak; fix before spending quota.

Dimension anchors:

- 抓耳度（前5秒）：8-10 means hook appears within 5s and is repeatable; 5-7 means emotional but not sticky; 0-4 means intro is slow or generic.
- 情绪感染力：8-10 means one clear emotion and strong scene; 5-7 means emotion is understandable but broad; 0-4 means vague mood words only.
- 副歌记忆点：8-10 means the first chorus line can be quoted alone; 5-7 means melodic lift exists but lyric is average; 0-4 means no clear chorus phrase.
- 二创适配：8-10 means clear edit points and multiple scene uses; 5-7 means fits one scene; 0-4 means hard to clip or remix.
- 平台适配：8-10 means format fits the chosen platform; 5-7 means platform fit is plausible; 0-4 means wrong tempo, scene, or audience.

## A/B Selection Formula

For each version, calculate:

```text
A/B加权分 =
抓耳度 * 0.30 +
副歌记忆点 * 0.25 +
二创适配 * 0.20 +
平台适配 * 0.15 +
成本效率 * 0.10
```

Tie-breakers:

1. Higher first-5-second hook score.
2. Higher UGC/edit adaptability.
3. Lower generation cost or shorter test duration.

## Negative Prompt Defaults

Add these to `avoid` unless they conflict with the user request:

```json
[
  "long intro",
  "muddy vocal",
  "generic melody",
  "over-complex arrangement",
  "copied melody",
  "unclear chorus",
  "weak first 5 seconds",
  "overpowering reverb",
  "off-beat vocal timing"
]
```

## Post-Publish Metric Thresholds

Use platform norms when provided; otherwise use these rough thresholds:

- 完播率 > 35%：structure works; < 25%：intro too long, chorus too late, or scene mismatch.
- 点赞率 > 5%：emotion works; < 2%：emotion not sharp enough.
- 收藏率 > 2%：lyrics/scenario useful; < 1%：caption value weak.
- 评论率 > 0.5%：resonance works; < 0.2%：golden line is weak.
- 转发率 > 0.8%：UGC/spread works; < 0.3%：adaptation scene is weak.

## Failure Handling Map

- 前5秒差：rewrite hook, start with chorus phrase, remove long intro.
- 完播率差：move chorus to 10-15s, shorten build, add earlier drum or vocal entry.
- 点赞率差：make emotion more specific; replace abstract sadness with concrete scene.
- 评论率差：rewrite golden lines as first-person confessions or "替用户说出口" lines.
- 收藏率差：strengthen captionable lines and scene value.
- 转发率差：add clearer edit point, drop, transition, or reversal moment.
- 平台适配差：change version lane, not only the title.
- 版权风险高：rewrite lyrics, melody, arrangement, and keep only high-level reference.

## Comment and Heat Learning

Classify comments before drawing conclusions. Do not treat all positive comments equally.

Comment categories:

- 情绪共鸣：mentions crying, memory, someone, loneliness, repeat listening, "破防".
- 歌词反馈：quotes a line, asks for lyrics/full version, says a line fits them.
- 音色反馈：mentions voice type, vocal realism, gender, tone, breathiness, emotional delivery.
- 编曲反馈：mentions piano, drums, drop, chorus, noise, mix, intro, rhythm.
- 使用场景：mentions breakup, anime edit, study, night drive, transition, drama reversal.
- 负面反馈：generic, noisy, fake vocal, copied, unclear lyrics, long intro, weak chorus.

Learning rules:

- Heat rising + emotional comments concentrated: increase that emotion/theme weight in the next batch.
- Heat rising + lyric quotes concentrated: reuse the sentence pattern, not the exact line.
- Heat rising + negative quality comments: keep the direction, fix mix/vocal/structure first.
- Heat flat + high collection/comment rate: improve title, cover, and first 3 seconds before changing song direction.
- Heat falling + weak comments: reduce topic/style weight or stop after one low-cost retest.
- Comments mention "像某歌" or plagiarism: run similarity risk check and rewrite melody/arrangement/lyrics.

Preference update weights:

```text
下一批权重调整 =
情绪主题 +/- 20%
音色选择 +/- 15%
编曲风格 +/- 15%
歌词句式 +/- 20%
发布文案角度 +/- 15%
平台/账号 lane +/- 15%
```

Do not overfit from fewer than 20 comments. Mark learning confidence low and suggest collecting more data.

## Batch Production Mode

Default account-matrix flow:

1. Generate 10 candidate topics from current trends.
2. Score all 10 with heat score.
3. Keep top 3 only.
4. For each kept topic, create lyrics, structure, prompt, and viral score.
5. If viral score >= 32, create 3 A/B versions.
6. Publish only the top 2 weighted A/B versions.
7. Feed metrics back into the next batch.

Kill rules:

- Heat score < 6: kill before music generation.
- Viral score < 32: rewrite before music generation.
- High similarity/copyright risk: kill or rewrite.
- Two consecutive posts below all metric thresholds: stop that direction for the next batch.
