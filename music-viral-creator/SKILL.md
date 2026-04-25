---
name: music-viral-creator
description: Viral instrumental short-video music creation workflow for Hermes Agent using minimax2.7. Use when creating pure instrumental DJ, EDM, rock, electronic rock, cinematic rock, hard-hitting BGM, beat-sync music, trailer music, sports/game/high-energy edits, rhythm slicing, drop design, riff design, cost-controlled generation, A/B versions, account-matrix publishing, release copy, post-publish metric review, or comment/heat learning for short-video instrumental music.
---

# Music Viral Creator

Use this skill to create **pure instrumental** short-video music: DJ, EDM, rock, electronic rock, cinematic rock, trailer-style impact BGM, and hard-hitting beat-sync tracks. Optimize for impact, rhythm, editability, replay value, and platform virality. Do not generate lyrics or lead vocals unless the user explicitly overrides the instrumental lane.

For full deliverables, follow `references/output-contract.md`. For music-2.6 prompt templates, use `references/music-2-6-prompt-templates.md`. For drop, riff, groove, and arrangement control, use `references/instrumental-arrangement-control.md`. For decision rules, use `references/decision-rules.md`.

## Operating Rules

- Default output language is Chinese.
- Default music type is **instrumental only**: no lyrics, no verse singing, no lead vocal.
- Use vocal chops, chants, shouts, risers, impacts, and crowd FX only as texture if useful; they must not become a sung lyric.
- Prioritize first-5-second impact, 10-15s transition/drop, 20s climax, and loopable structure.
- Build prompts with concrete production controls: BPM, key, drum pattern, bass, guitar riff, synth lead, drop timing, build-up, breakdown, impact FX, mix, and negative constraints.
- Before spending generation quota, run the decision engine and cost gate.
- Avoid copying melodies, riffs, drops, or distinctive arrangements from real tracks. References are high-level style signals only.

## Workflow

1. **Instrumental trend abstraction**
   - Input: trending BGM, DJ tracks, rock edits, game/sports/trailer music, or platform audio examples.
   - Output laws, not raw tables:
     - BPM distribution, e.g. `128-150 EDM/DJ`, `90-110 heavy rock/trailer half-time`, `160-180 drum-and-bass`.
     - Energy distribution: dark/heavy, heroic, aggressive, cyberpunk, explosive, party.
     - Drop timing: first impact within 3-5s, main drop by 10-15s, second hit around 20s.
     - Sound palette: kick, snare, sub bass, distorted guitar, synth brass, risers, impacts, tom fills.

2. **Viral instrumental structure**
   - Build a 0-30s short-video structure first:
     - `[0-5秒]` shock hook: impact hit, guitar riff, synth stab, drum fill, or bass drop.
     - `[5-10秒]` build-up: riser, tom fill, snare roll, guitar palm-mute, filter lift.
     - `[10-15秒]` first drop / beat-sync point: full drums + bass + riff.
     - `[15-25秒]` climax: bigger riff, wider synth, stronger drums, extra impacts.
     - `[25秒+]` loop/aftershock: keep energy or create a clean loop point.
   - State the intended edit use for each segment.

3. **Drop, riff, and groove design**
   - Use `references/instrumental-arrangement-control.md`.
   - Define:
     - Main riff or synth motif.
     - Drum groove and kick/snare pattern.
     - Bass movement and sub impact.
     - Build-up tools: riser, snare roll, filter sweep, reverse cymbal.
     - Drop moment: exact second, impact sound, rhythm action.
     - Rock layer: distorted guitar, power chords, palm mutes, or solo stab.
   - The track must feel like music for editing, not a flat loop.

4. **music-2.6 instrumental prompt**
   - Do not write vague prompts like `生成一首震撼纯音乐`.
   - Use this control formula:
     - `style + mood + bpm + key + instruments + groove + riff/motif + build-up + drop + climax + mix + duration + avoid`
   - Always output JSON-like prompt fields:
     - `style`, `mood`, `bpm`, `key`, `duration`
     - `instruments`
     - `rhythm_design`
     - `riff_motif`
     - `drop_plan`
     - `arrangement_arc`
     - `edit_points`
     - `mix`
     - `avoid`

5. **Cost control gate**
   - Score heat and concept potential before generating.
   - If heat or score is weak, generate only a prompt or a 15-30s demo, not full versions.

6. **Viral scoring**
   - Score 0-10 for:
     - 前5秒冲击力
     - Drop记忆点
     - 节奏卡点适配
     - 震撼/燃感
     - 平台适配
   - Total `/50`.

7. **Viral decision engine**
   - Apply hard generation rules:

```text
if 爆款评分 < 30:
    不生成音乐
elif 爆款评分 >= 30 and 爆款评分 <= 40:
    只生成1个版本
else:
    生成3个版本 + 推流测试
```

   - High similarity/copyright risk overrides all decisions and blocks generation.

8. **Cold-start strategy**
   - First 100 posts are data collection, not final judgment.
   - Force multi-style testing:
     - DJ festival drop
     - electronic rock
     - cinematic trailer rock
     - dark cyberpunk bass
     - drum-and-bass / phonk / hardstyle variants
   - Use short, low-cost versions and collect completion, rewatch, save, and comment data.

9. **Hit-pattern cloning**
   - Input: one viral instrumental BGM.
   - Extract:
     - BPM, key, energy curve, first impact, build-up, drop, riff/motif, drum pattern, bass, edit scenes.
   - Generate 3 same-class original instrumental works.
   - Keep energy function and timing; change motif, riff, sound design, title, and arrangement details.

10. **Rhythm slicing engine**
   - Output machine-usable edit points:
     - `0-5秒`: shock hook / impact.
     - `10-15秒`: drop / transition / beat-sync.
     - `20秒`: second hit / climax / riff expansion.
   - For each point include beat action, audio cue, visual cue, and editor instruction.

11. **Multi-version A/B generation**
   - Same concept -> at least 3 instrumental versions when budget allows:
     - `版本A：DJ震撼Drop`
     - `版本B：电子摇滚Riff`
     - `版本C：电影预告燃向`
   - Score each version and auto-select the best for publishing.

12. **Derivative/UGC adaptation**
   - Output suitable scenes:
     - game highlight, sports montage, car edit, battle scene, product reveal, transformation, trailer, city night, gym, speed ramp.
   - Output unsuitable scenes.
   - Recommend cut points and loop points.

13. **Account matrix publishing**
   - Convert one instrumental concept into account lanes:
     - DJ卡点号
     - 摇滚燃剪号
     - 游戏/电竞号
     - 电影感预告号
     - 运动/健身号
   - For each lane, output platform, audience, version, hook sound, and risk.

14. **Release copy pack**
   - Generate:
     - 5 short-video titles
     - 5 cover texts
     - 3 pinned comments
     - 3 UGC/remix prompts
     - 3 Xiaohongshu/Bilibili titles
   - Copy should sell the feeling and use case, not lyrics.

15. **Post-publish review**
   - Use playback, completion, rewatch, save, comment, share, and follower growth data.
   - Diagnose:
     - intro too weak
     - drop too late
     - drums not hard enough
     - riff not memorable
     - bass muddy
     - not edit-friendly
     - wrong platform lane

16. **Comment and heat learning**
   - Classify comments:
     - drop feedback
     - riff feedback
     - bass/drum impact
     - edit scene requests
     - loop/replay comments
     - negative mix comments
   - Update next batch: BPM, drop timing, riff style, bass weight, rock/electronic ratio, and platform lane.

## Quality Bar

A useful result must answer:

- What instrumental trend are we exploiting?
- What happens in the first 5 seconds?
- Where is the drop and why will it work for edits?
- What is the main riff/motif?
- How do drums, bass, guitar/synth, and impacts build the climax?
- What exact music-2.6 prompt should be generated?
- Is it worth spending quota now?
- Which A/B version should be published first?
- What edit points should the video system use?
- What should be learned from comments and heat?

If any answer is missing, revise before finalizing.
