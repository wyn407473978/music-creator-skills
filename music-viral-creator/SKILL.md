---
name: music-viral-creator
description: Viral short-video music creation workflow for Hermes Agent using minimax2.7. Use when analyzing popular songs, abstracting music market trends, modeling hit-song structures, writing spreadable Chinese lyrics, analyzing lyric prosody into natural melody direction, generating controllable music prompts, scoring release potential, making generate/no-generate decisions, planning cold-start tests, cloning hit-song patterns into original works, slicing rhythm/edit points, planning derivative/UGC adaptation, designing AI cover/remix strategies, creating A/B music versions, controlling generation cost, building account-matrix publishing plans, writing release copy, reviewing post-publish metrics, or learning from comments and music heat for short-video music.
---

# Music Viral Creator

Use this skill to turn market signal into a controlled, publishable short-video music concept. Optimize for patterns, hooks, emotional transmission, and remix/edit suitability rather than generic songwriting.

For full deliverables, follow the output contract in `references/output-contract.md`. For music-2.6 generation prompts, use `references/music-2-6-prompt-templates.md`. For lyric-to-melody alignment and natural vocal phrasing, use `references/lyric-melody-alignment.md`. For heat scoring, viral scoring, viral decision, cold-start, hit cloning, rhythm slicing, A/B selection, metric review, comment learning, and batch production rules, use `references/decision-rules.md`.

## Operating Rules

- Prefer Chinese output unless the user asks otherwise.
- Treat minimax2.7 as a strong planner but keep outputs structured, explicit, and checkable.
- If the user provides a list of songs, analyze it directly. If fewer than 30 songs are provided, mark confidence as low/medium and avoid pretending the sample represents the whole market.
- If the user asks for current market analysis and browsing/tools are available, gather dated platform signals first. Include platform and date in the source summary.
- Output laws and creative rules, not raw tables. The user needs reusable patterns such as "80-100 BPM is dominant" and "hook enters within 8 seconds".
- Never stop at lyrics. Always connect lyrics to structure, generation prompt, score, and二创传播场景 when creating a song plan.
- Avoid copying real lyrics, melodies, or protected expressive details from reference songs. Use references only as high-level style signals.
- Before consuming generation quota, run the cost gate. If heat, score, or confidence is below threshold, do not generate audio; revise concept or collect more signal first.

## Workflow

1. **Trend abstraction**
   - Input: ideally 100 trending songs or platform chart samples.
   - Output: emotion distribution, BPM range, hook timing, structure pattern, lyric themes, sonic palette, and platform fit.
   - Convert evidence into rules, for example: "前8秒必须出现Hook", "80-100 BPM更适合伤感共鸣", "副歌第一句要能独立做文案".

2. **Viral structure modeling**
   - Build a time-coded structure for 0-30 seconds first, then extend to full song if needed.
   - Required short-video template:
     - `[0-5秒]` 抓耳Hook：必须有记忆点，可哼唱或可引用。
     - `[5-15秒]` 情绪铺垫：补充人物、场景、矛盾。
     - `[15-25秒]` 副歌爆点：旋律/歌词/鼓点一起抬升。
     - `[25秒+]` 情绪延续 or 反转：给剪辑二次转场空间。
   - State the reason for each segment and the intended user reaction.

3. **Spreadable lyric generation**
   - Every 4 lines must include at least 1 "金句".
   - Lines should be截断可传播: usable alone as captions, comments, thumbnails, or chorus overlays.
   - Emotional intensity must progress: scene -> wound -> confession -> release/反转.
   - Mark strong lines with labels:
     - `标签：孤独 / 可做文案 / 强共鸣`
     - Example format: `你走之后 连影子都不属于我`
   - Keep chorus lines simpler, sharper, and more repeatable than verse lines.

4. **Lyric-to-melody alignment**
   - Before generating any music prompt, analyze the lyrics for natural singing.
   - Use `references/lyric-melody-alignment.md` to produce:
     - 每句字数/节奏密度.
     - 语义重音 and words that must land on strong beats.
     - 情绪峰值 line and required pitch lift.
     - 换气点 and phrase length.
     - Verse/pre-chorus/chorus pitch contour.
     - Safe vocal range, avoiding unnatural high/low jumps.
   - If a lyric line is too long for the target BPM, rewrite or split it before music generation.
   - The chorus melody must follow the strongest lyric line, not random high notes.

5. **Music generation prompt structure**
   - Do not give a vague prompt such as "写一首伤感歌".
   - Always use the control formula: `风格 + 情绪 + 节奏 + 调性 + 乐器 + 结构 + 人声 + 歌词韵律 + 旋律走向 + 参考`.
   - Pick the closest base template from `references/music-2-6-prompt-templates.md`, then adapt it to the current trend, lyric, and platform.
   - Include `lyric_prosody`, `melody_plan`, `vocal_range`, `phrasing`, and `singing_constraints` in the prompt.
   - Always output a controllable JSON-like prompt for the music generator:

```json
{
  "style": "动漫伤感",
  "mood": "sad, emotional, dreamy",
  "bpm": 90,
  "key": "C minor",
  "duration": "60-90s",
  "instruments": ["piano", "strings", "soft drums"],
  "structure": "0-5s vocal hook -> 5-15s emotional build -> 15-25s chorus peak -> 25s+ lingering outro",
  "reference": "YOASOBI high-level emotional pop energy, original melody and lyrics",
  "vocal": {
    "gender": "female",
    "tone": "clear, youthful",
    "emotion": "hopeful sadness",
    "range": "A3-E5, avoid strained high notes"
  },
  "lyric_prosody": {
    "language": "Chinese Mandarin",
    "line_density": "short lines, 7-11 Chinese characters per phrase",
    "stress_words": ["走之后", "影子", "不属于我"],
    "breath_points": "breathe after each lyric line; do not run two lines together",
    "pronunciation": "clear consonants, natural Mandarin phrasing"
  },
  "melody_plan": {
    "verse": "low-mid register, mostly stepwise motion, conversational",
    "pre_chorus": "gradual rising contour, increase tension without big jumps",
    "chorus": "highest note only on the strongest golden line, repeatable 3-5 note motif",
    "cadence": "resolve downward at line endings for sadness"
  },
  "lyrics": "paste final lyrics here",
  "quality": "high",
  "mix": "front vocal, warm piano, soft sidechain drums, cinematic strings",
  "singing_constraints": [
    "melody must follow lyric stress and sentence meaning",
    "one syllable per note for dense Chinese lines unless a held vowel is natural",
    "avoid random octave jumps",
    "avoid placing weak particles like 的/了/吗 on the highest note",
    "keep chorus singable and easy to hum"
  ],
  "avoid": ["overcrowded arrangement", "long intro", "unclear hook", "copied melody", "melody fighting the lyrics", "unnatural high notes", "wrong lyric stress", "rushed pronunciation"]
}
```

6. **Cost control gate**
   - Decide whether to spend generation quota before creating audio.
   - Calculate heat score with the formula in `references/decision-rules.md`; do not invent it subjectively.
   - Use this rule unless the user provides different thresholds:

```text
if 热度分 < 6/10 or 趋势可信度 == "低":
    不生成音乐，先补市场样本或重写选题
elif 爆款预测分 < 32/50:
    不生成完整音乐，只生成/优化歌词和Prompt
else:
    生成音乐，并进入A/B多版本测试
```

   - Always output:
     - `是否生成：是/否`
     - `原因：`
     - `省配额动作：跳过生成 / 只生成15秒demo / 只生成Prompt / 进入多版本`

7. **Viral scoring**
   - Score 5 dimensions, each 0-10:
     - 抓耳度（前5秒）
     - 情绪感染力
     - 副歌记忆点
     - 二创适配
     - 平台适配（抖音/小红书等）
   - Use the scoring anchors in `references/decision-rules.md`; every score needs a one-line reason.
   - Output total as `/50`.
   - Decision:
     - `40-50`: 强烈建议发布，可做A/B封面和剪辑点测试。
     - `32-39`: 可发布，但先按建议优化。
     - `24-31`: 暂不建议发布，重写Hook或副歌。
     - `<24`: 方向不成立，重做定位。

8. **Viral decision engine**
   - After scoring, make a hard generation decision. Do not only give advice.
   - Default rule:

```text
if 爆款评分 < 30:
    不生成音乐
elif 爆款评分 >= 30 and 爆款评分 <= 40:
    只生成1个版本
else:
    生成3个版本 + 推流测试
```

   - Output `决策`, `生成数量`, `推流动作`, `省配额原因`, and `下一步`.
   - If copyright risk is high, override the decision and do not generate until rewritten or licensed.

9. **Cold-start strategy**
   - Use when the account has fewer than 100 published pieces or lacks reliable historical metrics.
   - During the first 100 pieces:
     - 强制多风格测试.
     - 不按低分过早筛选方向.
     - 只做小成本数据收集.
     - Cover multiple lanes: 情绪钢琴、动漫、卡点电音、LoFi、翻唱/改编.
   - After 100 pieces, summarize account preference and switch to score-based filtering.

10. **Hit-pattern cloning**
   - Use when the input is one viral song or one viral short-video audio.
   - Extract:
     - 情绪
     - BPM
     - 调性
     - 结构
     - Hook位置
     - 歌词风格
     - 人声/音色
     - 乐器/编曲
     - 适配视频场景
   - Generate 3 same-class original works. Keep the pattern, but change lyrics, melody, arrangement, title, and story angle.
   - Run copyright/similarity check before generation.

11. **Rhythm slicing engine**
   - Output machine-usable edit points for the video/editing system.
   - Required slices:
     - `0-5秒`: Hook点.
     - `10-15秒`: 卡点/转场点.
     - `20秒`: 副歌爆点.
   - Include beat action, lyric cue, visual cue, and editor instruction for each slice.

12. **AI cover strategy**
   - Use when the input is an existing hit song, a melody concept, or a reusable lyric/hook for account-matrix publishing.
   - Output recommended vocal timbres:
     - 少女音：甜、脆、适合暗恋/动漫/治愈。
     - 御姐音：成熟、冷感、适合分手/反击/都市剧情。
     - 男低音：厚重、孤独、适合深夜/回忆/叙事。
     - 少年音：干净、青春、适合校园/成长。
   - Output recommended arrangement versions:
     - 钢琴版：适合伤感、独白、慢剪。
     - LoFi版：适合日常、回忆、学习陪伴。
     - 电音版：适合卡点、转场、舞蹈。
     - 弦乐版：适合剧情反转、影视感。
   - Warn when a cover/remix risks being too close to the reference. Keep melody, lyrics, and arrangement sufficiently original unless the user owns or has licensed the song.

13. **Multi-version A/B generation**
   - For the same lyric or hook, generate at least 3 versions when budget allows:
     - `版本A：伤感钢琴`
     - `版本B：电音卡点`
     - `版本C：LoFi氛围`
   - Each version must include a separate prompt structure, expected audience, best edit scene, and score.
   - Auto-select the best version using the weighted A/B formula in `references/decision-rules.md`.
   - Output `推荐主推版本` and `备用矩阵版本`.

14. **Derivative adaptation**
   - Say which scenes fit and do not fit.
   - Include recommended edit points with timestamps.
   - Include caption angles and short-video usage notes.
   - Example:
     - `适配场景：失恋回忆、深夜独白、剧情反转`
     - `不适合：搞笑整活、快节奏带货`
     - `推荐剪辑点：12秒进入副歌，适合卡点转场`

15. **Account matrix publishing**
   - Convert one song concept into multiple account lanes:
     - 情绪号：伤感钢琴、深夜文案、失恋回忆。
     - 动漫号：anime pop、角色主题曲、AI动漫剪辑。
     - 卡点号：electronic pop、转场、混剪、舞蹈。
     - LoFi号：学习陪伴、日常vlog、长尾BGM。
     - 翻唱/改编号：不同音色、不同编曲、热点借势。
   - For each lane, output platform, target audience, version to publish, hook line, and risk.

16. **Release copy pack**
   - Generate platform-ready copy:
     - 5个短视频标题。
     - 5个封面文案，each under 14 Chinese characters when possible.
     - 3条评论区置顶文案。
     - 3条引导二创文案。
     - 3个小红书笔记标题.
   - Copy must reuse the strongest lyric hooks and emotional keywords. Avoid generic phrases like "太好听了".

17. **Post-publish review loop**
   - When metrics are provided, diagnose performance and decide the next action.
   - Inputs: 播放量、完播率、点赞率、收藏率、评论率、转发率、涨粉、发布时间、平台、视频类型、评论关键词。
   - Use the metric thresholds and failure handling map in `references/decision-rules.md`.
   - Output:
     - `问题定位`: Hook弱 / 情绪不准 / 副歌太晚 / 标题弱 / 场景不匹配 / 平台不匹配.
     - `下一版动作`: 改Hook / 提前副歌 / 换音色 / 换编曲 / 换标题封面 / 停止该方向.
     - `是否继续消耗配额`: 是/否 and why.

18. **Copyright and similarity check**
   - Check every plan that uses references, covers, or existing hits.
   - Flag:
     - 原歌词是否使用。
     - 旋律是否过近。
     - 编曲是否过近。
     - 歌手/作品名是否作为 misleading marketing.
     - 是否具备授权或仅做原创风格参考。
   - Prefer "high-level style reference + original lyrics + original melody + original arrangement" for commercial or account-matrix use.

19. **Batch production mode**
   - Use when the user wants account-matrix scale or daily production.
   - Generate multiple concepts first, filter with heat and viral scores, then spend generation quota only on the survivors.
   - Default daily flow:
     - 10选题 -> heat score top 3.
     - Top 3 -> lyrics + structure + prompt.
     - Each survivor -> 3 A/B versions.
     - Publish top 2 total versions.
     - Feed post-publish metrics back into the next batch.

20. **Comment and heat learning loop**
   - Use when the user provides comments, comment keywords, platform heat changes, or performance history for released music.
   - Separate comments into:
     - 情绪共鸣：用户说被击中、想起某人、循环播放。
     - 歌词反馈：引用某句、说某句像自己、要求完整版。
     - 音色反馈：喜欢/讨厌少女音、御姐音、男低音、少年音等。
     - 编曲反馈：钢琴太单薄、鼓太吵、LoFi舒服、副歌不够炸。
     - 使用场景：失恋、回忆、剧情反转、动漫角色、学习、卡点。
     - 负面反馈：俗、吵、像某歌、听不清、人声假、前奏长。
   - Combine comment signals with heat movement:
     - 热度上升 + 正向评论集中：放大该风格/主题/音色。
     - 热度上升 + 负面评论集中：保留选题，修复生成质量或版权相似风险。
     - 热度下降 + 正向评论少：停止该方向或只做低成本测试。
     - 收藏/评论高但播放低：优化标题、封面、前3秒，而不是重写整首。
   - Output learned rules for the next batch:
     - `继续强化`
     - `需要修复`
     - `降低权重`
     - `停止尝试`
     - `下一批Prompt调整`

## Quality Bar

A useful result must answer:

- What trend law are we exploiting?
- What happens in the first 5 seconds?
- Which exact lyric line can spread by itself?
- How do the lyric stress, breath points, vocal range, and melody contour align?
- How should the music model be controlled?
- Is it worth publishing, and what must be improved before publishing?
- Should generation quota be spent now?
- What exact generation decision was made: no generation, 1 version, or 3 versions plus push test?
- If cold-starting, which style lanes are being tested before filtering?
- If cloning a hit, what pattern is reused and what is changed to stay original?
- What rhythm slices should the editing system use?
- Which cover voice/style or A/B version should be tested first?
- What video creators can do with it?
- Which account lane should publish it first?
- What title, cover text, and pinned comment should be used?
- After publishing, what metric says to iterate, scale, or stop?
- What did comments and heat teach us for the next batch?
- Is there any copyright or similarity risk?
- In batch mode, which ideas survive and which are killed before generation?

If any answer is missing, revise before finalizing.
