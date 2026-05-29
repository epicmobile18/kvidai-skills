---
name: kvidai-skills
description: "kvidai platform skill hub. Use for any kvidai API task: video project creation, AI video generation, media upload/management, preset CRUD, or conversation-driven video editing. Delegates to sub-skills: kvidai-video-project (generate), kvidai-media (upload/manage), kvidai-preset (presets), kvidai-video-use (edit pipeline). Triggers on: kvidai, kvid.ai, 영상 생성, 프로젝트 생성, 미디어 업로드, 프리셋."
metadata:
  tags: kvidai, video, ai, media, preset
---

# kvidai-skills

kvidai platform skills. Each sub-skill lives under `skills/`.

## Sub-Skills

| Skill | Path | Use when |
|-------|------|----------|
| `kvidai-video-project` | `skills/kvidai-video-project/` | Create project, AI generate video, poll status |
| `kvidai-media` | `skills/kvidai-media/` | Upload media, presigned URL, list/delete assets |
| `kvidai-preset` | `skills/kvidai-preset/` | Create/list/update/delete presets |
| `kvidai-video-use` | `skills/kvidai-video-use/` | Transcribe → cut → grade → subtitle → kvidai handoff |

## Setup (kvidai monorepo)

Symlinks in `.claude/skills/` point to each sub-skill:

```bash
ln -s ../../skills/kvidai-skills/skills/kvidai-video-project .claude/skills/kvidai-video-project
ln -s ../../skills/kvidai-skills/skills/kvidai-media         .claude/skills/kvidai-media
ln -s ../../skills/kvidai-skills/skills/kvidai-preset        .claude/skills/kvidai-preset
ln -s ../../skills/kvidai-skills/skills/kvidai-video-use     .claude/skills/kvidai-video-use
ln -s ../../skills/kvidai-skills                             .claude/skills/kvidai-skills
```
