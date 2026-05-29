# kvidai-skills

Agent skills for the kvidai video platform — works with Claude Code, Codex, Goose, Copilot, and [50+ agents](https://github.com/vercel-labs/skills).

## Skills

| Skill | Description |
|-------|-------------|
| [`kvidai-video-project`](skills/kvidai-video-project/) | Create projects, generate videos via AI agent (SSE), poll status |
| [`kvidai-media`](skills/kvidai-media/) | Upload media, presigned URL, list/delete assets |
| [`kvidai-preset`](skills/kvidai-preset/) | Create, list, update, delete presets |
| [`video-use`](skills/video-use/) | Conversation-driven video editor: transcribe, cut, grade, subtitle, composite |

## Installation

### Option 1 — npx skills (recommended)

```bash
npx skills add epicmobile18/kvidai-skills
```

Installs all skills into the current project for all detected agents automatically.

### Option 2 — Symlink (kvidai monorepo)

```bash
ln -s ../../skills/kvidai-skills/skills/kvidai-video-project .claude/skills/kvidai-video-project
ln -s ../../skills/kvidai-skills/skills/kvidai-media         .claude/skills/kvidai-media
ln -s ../../skills/kvidai-skills/skills/kvidai-preset        .claude/skills/kvidai-preset
ln -s ../../skills/kvidai-skills/skills/video-use            .claude/skills/video-use
```

### Option 3 — Git submodule

```bash
git submodule add https://github.com/epicmobile18/kvidai-skills skills/kvidai-skills
# then add symlinks as in Option 2
```

## Environment Variables

```bash
export KVIDAI_API_KEY="<your-api-key>"
export KVIDAI_BASE_URL="https://api.kvid.ai"  # default if not set
export KVIDAI_USER_EMAIL="user@example.com"   # required for media upload
```
