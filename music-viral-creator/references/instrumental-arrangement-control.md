# Instrumental Arrangement Control

Use this before creating any music-2.6 prompt for pure instrumental DJ, EDM, rock, electronic rock, or cinematic impact BGM.

## Core Formula

```text
impact hook -> build-up -> drop -> climax -> loop/aftershock
```

The music must be useful for short-video editing. It needs clear timestamps, strong transients, memorable motifs, and visible energy changes.

## Instrumental Design Checklist

- BPM: choose based on use case.
- Key/mode: minor for dark/heavy, major for heroic/bright, Phrygian/Locrian flavor for aggressive rock.
- Main motif: guitar riff, synth stab, bass motif, brass hit, or drum fill.
- Drum groove: four-on-floor, half-time rock, breakbeat, DnB, hardstyle kick, or trap hybrid.
- Bass: sub drop, distorted bass, sidechain pump, or guitar/bass unison riff.
- Build-up: riser, snare roll, tom fill, reverse cymbal, filter sweep, silence-before-drop.
- Drop: exact timestamp, impact sound, full rhythm entry, bass/guitar/synth action.
- Climax: second riff, wider harmony, extra cymbals, crash, crowd/impact FX.
- Loop point: clean 2-bar or 4-bar ending for repeated videos.

## BPM Guide

- DJ festival / EDM: 124-132 BPM.
- Hardstyle / rave: 145-160 BPM.
- Electronic rock: 120-150 BPM.
- Cinematic trailer rock: 90-110 BPM, often half-time.
- Phonk / drift: 130-160 BPM.
- Drum-and-bass: 160-180 BPM.
- Heavy sports/game montage: 95-115 BPM half-time or 140-150 BPM double-time.

## Drop and Climax Rules

- First shock must happen within 0-5s.
- Main drop should happen at 10-15s for short videos.
- A second hit or bigger layer should happen around 20s.
- Use silence or a micro-break before the drop when possible.
- The drop must add at least 3 of these: fuller drums, sub bass, distorted guitar, synth lead, crash/impact, wider stereo, extra percussion.
- Avoid a flat loop that never changes.

## Rock Riff Rules

- Use short 1-2 bar riffs that can loop.
- Prefer power chords, palm-muted rhythm, octave guitar, or distorted unison bass.
- For aggression, use syncopation and rests, not constant noise.
- For cinematic rock, combine low guitar chugs with strings/brass impacts.
- Keep riff original; do not copy famous guitar patterns.

## DJ/EDM Rules

- Use a clear kick and bass relationship.
- Drop should be rhythmically obvious for beat-sync edits.
- Use risers and filter automation during build-up.
- Use sidechain pumping for energy.
- Keep lead motif simple and repeatable.

## Mix Defaults

- Punchy kick, clear snare/clap, heavy but controlled sub bass.
- Distorted guitar should be wide but not hide the kick/snare.
- Synth lead or riff must be memorable within 2 bars.
- Avoid muddy low mids around 200-500 Hz.
- Keep transient hits sharp for video edits.

## Prompt Fields

Always include:

```json
{
  "rhythm_design": {
    "drum_pattern": "",
    "kick": "",
    "snare_clap": "",
    "percussion": "",
    "groove_feel": ""
  },
  "riff_motif": {
    "type": "",
    "description": "",
    "repeat_pattern": "",
    "variation": ""
  },
  "drop_plan": {
    "first_impact": "",
    "build_up": "",
    "main_drop": "",
    "second_hit": "",
    "loop_point": ""
  },
  "arrangement_arc": "",
  "edit_points": []
}
```

## Repair Rules

- Sounds weak: strengthen kick/snare transient, add sub drop, add impact hit.
- Drop too late: move main drop to 10-15s.
- Rock not heavy: add palm-muted guitar, distorted bass, crash cymbal, half-time drums.
- DJ not exciting: add riser, sidechain bass, synth stab, festival snare build.
- Too noisy: reduce layers in verse/build-up and reserve full density for drop.
- Not edit-friendly: add clear impacts at 0-5s, 10-15s, and 20s.
