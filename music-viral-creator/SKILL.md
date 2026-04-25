---
name: music-viral-creator
description: Viral English song creation workflow for Hermes Agent using minimax2.7. Use when creating English songs across genres including pop, rock, EDM, hip-hop, R&B, country, folk, indie, cinematic, lo-fi, dance, DJ rock, and trailer music; generating natural English lyrics, vocal toplines, song metadata records, music prompts, structures, A/B versions, release copy, cost-controlled generation, post-publish metric review, or comment/heat learning for short-video English music.
---

# Music Viral Creator

Use this skill to create **English vocal songs across all genres**: pop, rock, EDM, hip-hop, R&B, country, folk, indie, cinematic, lo-fi, dance, DJ rock, and trailer music. Optimize for a strong English hook, natural vocal phrasing, clear genre identity, editability, and short-video virality.

For full deliverables, follow `references/output-contract.md`. For music-2.6 prompt templates, use `references/music-2-6-prompt-templates.md`. For English lyric/vocal and arrangement control, use `references/english-song-arrangement-control.md`. For song metadata persistence, use `references/song-metadata-schema.md`. For decision rules, use `references/decision-rules.md`.

## Operating Rules

- Default song language is **English**.
- Generate lyrics only in English unless the user explicitly asks otherwise.
- Avoid Chinese lyric phrasing, Chinglish grammar, stiff translation, and word-by-word singing.
- Every song needs a short, repeatable English hook that can work as a caption.
- Every generated song or version must include a `song_metadata` record with title, genre, mood, BPM, key, version, prompt id, target platform, usage scene, and status.
- Keep the first 5 seconds memorable: vocal hook, chant, riff, impact, or drop preview.
- Main chorus/drop should arrive by 10-20 seconds for short-video use.
- Build prompts with concrete controls: BPM, key, vocal style, lyric hook, rhyme, syllable fit, drum pattern, bass, guitar/synth riff, drop timing, climax, mix, and avoid.
- References are high-level style signals only. Do not copy lyrics, melodies, riffs, or distinctive arrangements.

## Workflow

1. **English song trend abstraction**
   - Analyze trending English songs across pop, rock, EDM, hip-hop, R&B, country, folk, indie, cinematic, lo-fi, dance, DJ, and trailer lanes.
   - Output laws:
     - Hook type: chant hook, one-line chorus, shouted slogan, emotional topline.
     - BPM: match genre, e.g. `70-90 ballad/R&B`, `90-120 pop/indie/country`, `120-150 dance/EDM/rock`, `60-85 lo-fi`.
     - Structure: hook within 5s when short-video focused; chorus/drop/climax by 10-25s.
     - Lyric themes: love, heartbreak, power, revenge, freedom, nostalgia, night drive, coming-of-age, party, healing.

2. **Song metadata record**
   - Before final output, create a metadata record for every song/version.
   - Required fields:
     - song_id, title, language, genre, subgenre, mood, theme, bpm, key, duration, version_name, hook_line, target_platform, usage_scene, generation_status, prompt_summary.
   - Use `references/song-metadata-schema.md`.
   - If multiple versions are generated, each version gets its own metadata but shares `project_id`.

3. **Viral English song structure**
   - Build 0-30s first:
     - `[0-5s]` vocal/riff hook.
     - `[5-10s]` verse or build-up.
     - `[10-15s]` pre-drop / chant / drum build.
     - `[15-25s]` chorus/drop climax.
     - `[25s+]` post-chorus hook / loop.
   - State the edit use for each segment.

4. **English lyrics and topline**
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

5. **Vocal phrasing and melody fit**
   - Use `references/english-song-arrangement-control.md`.
   - Define:
     - vocal range
     - verse/pre/chorus pitch contour
     - stressed syllables
     - phrase grouping
     - chant/shout vs sung line
     - chorus high note word
   - The vocal must sound like a song, not like reading lyrics.

6. **Genre-specific arrangement**
   - Define:
     - drum groove
     - bass/sub movement
     - guitar, synth, piano, pads, strings, 808, acoustic instruments, or genre-specific motif
     - build-up or pre-chorus tools
     - chorus/drop/climax entry
     - second hit around 20s
     - mix intensity
   - For soft genres, the lift may be emotional/harmonic instead of heavy drop.
   - For energetic genres, the lift should use drums, bass, guitars/synths, harmonies, and wider stereo.

7. **music-2.6 English song prompt**
   - Do not write vague prompts like `make an English song`.
   - Use:
     - `song_metadata + style + mood + bpm + key + vocal + lyrics + lyric_phrasing + rhythm_design + arrangement + chorus_or_drop_plan + edit_points + mix + avoid`.

8. **Cost control gate**
   - Score heat and concept potential before generating.
   - Weak concept: prompt or 15-30s demo only.

9. **Viral scoring**
   - Score 0-10:
     - first-5-second hook
     - English chorus memorability
     - drop/chorus impact
     - edit/UGC fit
     - platform fit
   - Total `/50`.

10. **Viral decision engine**
   - Apply:

```text
if score < 30:
    do not generate music
elif score >= 30 and score <= 40:
    generate 1 version
else:
    generate 3 versions + push test
```

11. **Cold-start strategy**
   - First 100 posts test multiple English lanes:
     - pop hook
     - R&B emotional
     - hip-hop melodic hook
     - EDM rock anthem
     - pop rock heartbreak
     - cinematic trailer rock
     - country/folk story
     - lo-fi indie

12. **Hit-pattern cloning**
   - Input: one viral English song/audio.
   - Extract BPM, key, hook type, chorus timing, vocal energy, riff/motif, drop, lyric theme, rhyme style, edit scenes.
   - Generate 3 same-class original English songs. Keep function/timing; change lyrics, melody, title, riff, and arrangement.

13. **Rhythm slicing engine**
   - Output:
     - `0-5s`: vocal/riff hook.
     - `10-15s`: build/drop/transition.
     - `20s`: chorus/drop second hit.
   - Include audio cue, lyric cue, visual cue, and editor instruction.

14. **Multi-version A/B generation**
   - Same hook concept -> 3 versions:
     - `Version A: Pop Hook`
     - `Version B: Energetic/EDM or Rock`
     - `Version C: Emotional/R&B/Indie or Cinematic`
   - Score and choose the best.

15. **Derivative/UGC adaptation**
   - Output suitable scenes: game highlight, sports montage, car edit, battle, transformation, night drive, gym, trailer, product reveal.
   - Recommend cut points, lyric overlay, and loop point.

16. **Account matrix publishing**
   - Lanes:
     - English pop hook account
     - English emotional/R&B account
     - English rock/EDM account
     - cinematic/trailer account
     - lo-fi/indie account
     - hip-hop hook account

17. **Release copy pack**
   - Generate English titles, cover text, pinned comments, UGC prompts, and bilingual platform titles when useful.

18. **Post-publish review and learning**
   - Review completion, rewatch, saves, shares, comments, hook quotes, and follower growth.
   - Update next batch: hook style, BPM, vocal tone, riff/drop design, lyric theme, and account lane.

## Quality Bar

A useful result must answer:

- What English song lane are we using?
- What is the song title, genre, BPM, key, version, and metadata record?
- What is the first 5-second hook?
- What is the chorus hook line?
- Does the English phrasing sound natural and singable?
- Where is the chorus/drop and why will it work for edits?
- What are the drums, bass, riff/synth, vocal, and climax doing?
- What exact music-2.6 prompt should be generated?
- Is it worth spending quota now?
- Which A/B version should publish first?

If any answer is missing, revise before finalizing.
