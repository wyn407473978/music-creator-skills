# Decision Rules

Use these rules for pure instrumental DJ / rock / impact BGM decisions.

## Heat Score

```text
热度分 =
平台热度 * 0.30 +
近期增长 * 0.25 +
评论/重播共鸣 * 0.20 +
可剪辑性 * 0.15 +
竞争拥挤度反向 * 0.10
```

Score each sub-item from 0-10.

Confidence:

- 高：50+ samples or strong multi-platform signal.
- 中：15-49 samples or one strong platform signal.
- 低：fewer than 15 samples.

## Cost Gate

- Heat < 6 or confidence low: do not generate full music.
- Heat 6-7: prompt or 15-30s demo only.
- Heat >= 7 and viral score >= 32/50: generate A/B versions.
- High similarity risk: stop until rewritten.

## Viral Scoring Anchors

Score 0-10:

- 前5秒冲击力：impact, riff, hit, or bass hook appears immediately.
- Drop记忆点：main drop is clear, repeatable, and strong.
- 节奏卡点适配：clear edit points and transients.
- 震撼/燃感：energy curve, drums, bass, riff, and climax work together.
- 平台适配：fits target lane and video scene.

## Viral Decision Engine

```text
if 爆款评分 < 30:
    不生成音乐
elif 爆款评分 >= 30 and 爆款评分 <= 40:
    只生成1个版本
else:
    生成3个版本 + 推流测试
```

Overrides:

- Similarity risk high: do not generate.
- Cold-start first 100 posts: low-cost tests across lanes.

## A/B Selection Formula

```text
A/B加权分 =
前5秒冲击力 * 0.25 +
Drop记忆点 * 0.25 +
节奏卡点适配 * 0.20 +
震撼/燃感 * 0.20 +
成本效率 * 0.10
```

Tie-breakers:

1. Stronger 0-5s impact.
2. More obvious 10-15s drop.
3. Cleaner loop/edit point.

## Cold Start

First 100 posts:

- Test DJ drop, electronic rock, cinematic trailer rock, dark cyberpunk bass, hard rock beat.
- Do not kill a lane from fewer than 10 tests.
- Generate short versions first.
- Track completion, rewatch, save, share, and comments.

## Failure Handling

- Intro weak: add impact hit, riff preview, or bass boom in first 3s.
- Drop late: move main drop to 10-15s.
- Drop weak: add fuller kick, sub bass, crash, synth/guitar layer.
- Rock weak: add palm-muted riff, power chords, half-time snare.
- DJ weak: add riser, snare roll, sidechain bass, wider synth.
- Mix muddy: reduce low mids, separate kick/sub, simplify layers.
- Not edit-friendly: add clear hits at 0-5s, 10-15s, 20s.

## Comment and Heat Learning

Classify:

- Drop feedback
- Riff feedback
- Bass/drum impact
- Scene requests
- Loop/replay comments
- Negative mix comments

Learning rules:

- Heat rising + drop praise: keep drop timing and sound palette.
- Rewatch high + comments ask for full version: make longer loop and variations.
- Saves high + shares low: improve edit points and title/cover.
- Comments say "不够炸": strengthen drop, drums, sub, impact FX.
- Comments say "太吵": simplify layers and clean mix.
- Comments say "像某歌": rewrite riff/motif and run similarity check.
