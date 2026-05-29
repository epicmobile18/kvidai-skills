# kvidai-skills

Agent skills for the kvidai video platform.

## Skills

- [`kvidai-video-project`](skills/kvidai-video-project/) — Create projects, generate videos via AI agent (SSE), poll status
- [`video-use`](skills/video-use/) — Conversation-driven video editor: transcribe, cut, grade, subtitle, composite; hands off final timeline to kvidai web editor

## Installation

Copy the skill directory into `.claude/skills/` in your project:

```bash
cp -r skills/kvidai-video-project /your-project/.claude/skills/
cp -r skills/video-use /your-project/.claude/skills/
```

Or add this repo as a submodule:

```bash
git submodule add https://github.com/epicmobile18/kvidai-skills skills/kvidai-skills
```
