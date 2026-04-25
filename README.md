# Music Viral Creator Skill

`music-viral-creator` is a Hermes Agent skill for English short-video songs across genres: pop, rock, EDM, hip-hop, R&B, country, folk, indie, cinematic, lo-fi, dance, DJ rock, and high-impact English hooks. It is designed for agents using minimax2.7 and music generation models such as music-2.6.

## What It Does

- English song trend abstraction
- Viral all-genre English song structure modeling
- English lyric and topline generation
- Song metadata records for every generated song/version
- Drop, riff, groove, and climax design
- Structured music-2.6 English song prompt generation
- Instrumental drop, riff, groove, and climax control
- Viral scoring and hard generation decisions
- Cost control before spending generation quota
- Cold-start testing for new music accounts
- Hit-pattern cloning into original same-class works
- Rhythm slicing for video editing systems
- Multi-version A/B testing
- Derivative/UGC adaptation planning
- Account-matrix publishing strategy
- Release title, cover copy, pinned comment, and Xiaohongshu copy generation
- Post-publish metric review
- Comment and heat learning loop
- Copyright and similarity risk checks
- Batch production mode for daily content pipelines

## Directory Structure

```text
music-viral-creator/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── decision-rules.md
    ├── music-2-6-prompt-templates.md
    └── output-contract.md
```

## Core Workflow

1. Analyze English song trends and extract reusable rules.
2. Create song metadata: title, genre, mood, BPM, key, version, target platform, and status.
3. Model the 0-30s viral English song structure.
4. Write a short, natural English hook and chorus.
5. Design genre-specific arrangement, groove, climax, and edit points.
6. Generate a structured music-2.6 English song prompt.
5. Score the concept and run the decision engine.
6. Generate one or more versions only when the score justifies it.
7. Create edit slices, release copy, and account-matrix plans.
8. Learn from published comments and heat metrics to improve the next batch.

## Viral Decision Rules

```text
if score < 30:
    do not generate music
elif score >= 30 and score <= 40:
    generate 1 version
else:
    generate 3 versions + push test
```

High copyright or similarity risk overrides the decision and blocks generation until the concept is rewritten or licensed.

## Cold Start

For the first 100 posts on a new account, the skill prioritizes data collection:

- Force multi-style testing
- Avoid killing lanes too early
- Test emotional piano, anime pop, electronic beat-sync, LoFi, and cover/remix-inspired originals
- Use low-cost short versions where possible
- Summarize winning style, emotion, voice, BPM, and copy angles after 100 posts

## music-2.6 Prompt Principle

Avoid vague prompts such as:

```text
make an English rock song
```

Use structured control:

```text
song_metadata + style + mood + bpm + key + vocal + lyrics + lyric_phrasing + arrangement + chorus_or_drop_plan + arrangement_arc + edit_points + mix + avoid
```

See `music-viral-creator/references/music-2-6-prompt-templates.md` for ready-to-use templates.

Default output is English vocal music. Focus on a short English hook, natural phrasing, chorus/drop impact, second hit, loop point, and edit-friendly transients.

## Using With Hermes

Point Hermes Agent at the skill folder and invoke:

```text
Use $music-viral-creator to analyze a viral song, generate three original same-class music concepts, create music-2.6 prompts, score them, and decide which versions to generate.
```

For full output formatting, use:

```text
music-viral-creator/references/output-contract.md
```

For scoring, cost control, cold-start, A/B, and learning rules, use:

```text
music-viral-creator/references/decision-rules.md
```
