---
name: music-viral-creator
description: Viral English song creation workflow for Hermes Agent using minimax2.7. Use when creating English DJ rock songs, EDM rock songs, pop rock anthems, cinematic rock songs, hard-hitting English hooks, natural English lyrics, vocal toplines, chorus/drop structures, rhythm slicing, A/B versions, cost-controlled generation, account-matrix publishing, release copy, post-publish metric review, or comment/heat learning for short-video English music.
---

# Music Viral Creator

Use this skill to create **English vocal songs** with DJ, EDM, rock, electronic rock, pop rock, cinematic rock, or trailer-rock energy. Optimize for a strong English hook, natural vocal phrasing, big chorus/drop, editability, and short-video virality.

For full deliverables, follow `references/output-contract.md`. For music-2.6 prompt templates, use `references/music-2-6-prompt-templates.md`. For English lyric/vocal and arrangement control, use `references/english-song-arrangement-control.md`. For decision rules, use `references/decision-rules.md`.

## Operating Rules

- Default song language is **English**.
- Generate lyrics only in English unless the user explicitly asks otherwise.
- Avoid Chinese lyric phrasing, Chinglish grammar, stiff translation, and word-by-word singing.
- Every song needs a short, repeatable English hook that can work as a caption.
- Keep the first 5 seconds memorable: vocal hook, chant, riff, impact, or drop preview.
- Main chorus/drop should arrive by 10-20 seconds for short-video use.
- Build prompts with concrete controls: BPM, key, vocal style, lyric hook, rhyme, syllable fit, drum pattern, bass, guitar/synth riff, drop timing, climax, mix, and avoid.
- References are high-level style signals only. Do not copy lyrics, melodies, riffs, or distinctive arrangements.

## Workflow

1. **English song trend abstraction**
   - Analyze trending English pop, EDM rock, pop rock, trailer rock, DJ songs, game/sports edits.
   - Output laws:
     - Hook type: chant hook, one-line chorus, shouted slogan, emotional topline.
     - BPM: `120-150` for EDM/rock energy, `90-110` for cinematic half-time.
     - Structure: hook within 5s, pre/drop by 10-15s, chorus/climax by 15-25s.
     - Lyric themes: power, heartbreak, revenge, freedom, night drive, battle, transformation.

2. **Viral English song structure**
   - Build 0-30s first:
     - `[0-5s]` vocal/riff hook.
     - `[5-10s]` verse or build-up.
     - `[10-15s]` pre-drop / chant / drum build.
     - `[15-25s]` chorus/drop climax.
     - `[25s+]` post-chorus hook / loop.
   - State the edit use for each segment.

3. **English lyrics and topline**
   - Write natural English lyrics, not translated Chinese.
   - Chorus must have 1 repeatable hook line, ideally 4-8 words.
   - Use strong vowel sounds for high notes and held notes.
   - Keep line lengths singable. Avoid stuffing too many syllables into fast sections.
   - Mark:
     - hook line
     - rhyme pattern
     - stressed words
     - breath points
     - chorus slogan/caption line

4. **Vocal phrasing and melody fit**
   - Use `references/english-song-arrangement-control.md`.
   - Define:
     - vocal range
     - verse/pre/chorus pitch contour
     - stressed syllables
     - phrase grouping
     - chant/shout vs sung line
     - chorus high note word
   - The vocal must sound like a song, not like reading lyrics.

5. **DJ/Rock arrangement**
   - Define:
     - drum groove
     - bass/sub movement
     - guitar riff or synth motif
     - build-up tools
     - chorus/drop entry
     - second hit around 20s
     - mix intensity
   - Chorus/drop should lift with drums, bass, guitars/synths, harmonies, and wider stereo.

6. **music-2.6 English song prompt**
   - Do not write vague prompts like `make an English rock song`.
   - Use:
     - `style + mood + bpm + key + vocal + lyrics + lyric_phrasing + rhythm_design + riff_motif + chorus_drop_plan + arrangement_arc + edit_points + mix + avoid`.

7. **Cost control gate**
   - Score heat and concept potential before generating.
   - Weak concept: prompt or 15-30s demo only.

8. **Viral scoring**
   - Score 0-10:
     - first-5-second hook
     - English chorus memorability
     - drop/chorus impact
     - edit/UGC fit
     - platform fit
   - Total `/50`.

9. **Viral decision engine**
   - Apply:

```text
if score < 30:
    do not generate music
elif score >= 30 and score <= 40:
    generate 1 version
else:
    generate 3 versions + push test
```

10. **Cold-start strategy**
   - First 100 posts test multiple English lanes:
     - EDM rock anthem
     - pop rock heartbreak
     - cinematic trailer rock
     - dark cyberpunk vocal hook
     - DJ chant/drop song

11. **Hit-pattern cloning**
   - Input: one viral English song/audio.
   - Extract BPM, key, hook type, chorus timing, vocal energy, riff/motif, drop, lyric theme, rhyme style, edit scenes.
   - Generate 3 same-class original English songs. Keep function/timing; change lyrics, melody, title, riff, and arrangement.

12. **Rhythm slicing engine**
   - Output:
     - `0-5s`: vocal/riff hook.
     - `10-15s`: build/drop/transition.
     - `20s`: chorus/drop second hit.
   - Include audio cue, lyric cue, visual cue, and editor instruction.

13. **Multi-version A/B generation**
   - Same hook concept -> 3 versions:
     - `Version A: EDM Rock Anthem`
     - `Version B: Pop Rock Chorus`
     - `Version C: Cinematic Trailer Rock`
   - Score and choose the best.

14. **Derivative/UGC adaptation**
   - Output suitable scenes: game highlight, sports montage, car edit, battle, transformation, night drive, gym, trailer, product reveal.
   - Recommend cut points, lyric overlay, and loop point.

15. **Account matrix publishing**
   - Lanes:
     - English DJ hook account
     - Rock anthem edit account
     - Game/esports account
     - Trailer/cinematic account
     - Gym/sports account

16. **Release copy pack**
   - Generate English titles, cover text, pinned comments, UGC prompts, and bilingual platform titles when useful.

17. **Post-publish review and learning**
   - Review completion, rewatch, saves, shares, comments, hook quotes, and follower growth.
   - Update next batch: hook style, BPM, vocal tone, riff/drop design, lyric theme, and account lane.

## Quality Bar

A useful result must answer:

- What English song lane are we using?
- What is the first 5-second hook?
- What is the chorus hook line?
- Does the English phrasing sound natural and singable?
- Where is the chorus/drop and why will it work for edits?
- What are the drums, bass, riff/synth, vocal, and climax doing?
- What exact music-2.6 prompt should be generated?
- Is it worth spending quota now?
- Which A/B version should publish first?

If any answer is missing, revise before finalizing.
