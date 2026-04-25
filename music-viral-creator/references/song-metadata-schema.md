# Song Metadata Schema

Every generated song or version must output a metadata record. This lets Hermes save, compare, publish, and review songs consistently.

## Required Metadata

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
  "structure": "",
  "target_platform": "",
  "usage_scene": "",
  "vocal_type": "",
  "instruments": [],
  "prompt_summary": "",
  "generation_status": "planned / prompt_ready / generated / published / archived",
  "score": {
    "hook": 0,
    "chorus": 0,
    "impact": 0,
    "edit_fit": 0,
    "platform_fit": 0,
    "total": 0
  },
  "rights_notes": "original lyrics, original melody, high-level style references only",
  "created_at": "",
  "notes": ""
}
```

## Naming Rules

- `project_id`: stable id for one creative direction, e.g. `night-drive-anthem`.
- `song_id`: unique id for one song/version, e.g. `night-drive-anthem-vA-pop`.
- `title`: human-readable English title.
- `version_name`: clear variant name, e.g. `Pop Hook Version`, `EDM Drop Version`, `R&B Late Night Version`.

## Genre Examples

- Pop
- Rock
- EDM
- Dance
- Hip-hop
- R&B
- Country
- Folk
- Indie
- Lo-fi
- Cinematic
- Trailer Rock
- DJ Rock

## Status Rules

- `planned`: idea only.
- `prompt_ready`: metadata and prompt are ready.
- `generated`: audio generated.
- `published`: published to a platform.
- `archived`: stopped or not worth continuing.
