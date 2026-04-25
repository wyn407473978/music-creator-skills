# Decision Rules

Use these rules for English DJ/rock vocal songs.

## Heat Score

```text
热度分 =
平台热度 * 0.30 +
近期增长 * 0.25 +
Hook评论/引用 * 0.20 +
剪辑适配 * 0.15 +
竞争拥挤度反向 * 0.10
```

## Viral Scoring

Score 0-10:

- 前5秒Hook：English vocal/riff hook appears immediately.
- 英文副歌记忆点：hook line is short, repeatable, and captionable.
- Chorus/Drop冲击：drums, bass, vocal, guitar/synth lift together.
- 剪辑适配：clear cuts at 0-5s, 10-15s, 20s.
- 平台适配：fits target short-video lane.

## Decision Engine

```text
if score < 30:
    do not generate music
elif score >= 30 and score <= 40:
    generate 1 version
else:
    generate 3 versions + push test
```

## Failure Handling

- English awkward: rewrite lyrics natively, not translated.
- Hook weak: shorten chorus line to 4-8 words.
- Vocal stiff: reduce syllables, add chant or repeated hook.
- Chorus weak: add vocal doubles, stronger drums, bass, guitar/synth lift.
- Drop late: move chorus/drop to 10-20s.
- Mix muddy: clear vocal, separate kick/sub, reduce low mids.
- Not edit-friendly: add 0-5s hook, 10-15s drop, 20s second hit.

## Cold Start

First 100 posts test:

- EDM rock anthem
- Pop rock heartbreak
- Cinematic trailer rock
- Dark cyberpunk vocal hook
- DJ chant/drop song

Do not kill a lane from fewer than 10 tests.
