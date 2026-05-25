# kvidai-skills

Claude Code Agent Skills for the kvidai video platform.

## Directory Structure

```
kvidai-skills/
├── skills/
│   └── kvidai-video-project/      # Create projects, generate videos via AI agent (SSE)
│       ├── SKILL.md               # Skill definition (name, description, API reference)
│       └── scripts/
│           └── kvidai-client.mjs  # CLI client (Node.js 20+, no tsx needed)
├── AGENTS.md                      # This file (AI guide)
├── CLAUDE.md                      # Symlink → AGENTS.md
└── README.md                      # Human index
```

## Adding a New Skill

1. Create `skills/<skill-name>/SKILL.md` with frontmatter:
   ```yaml
   ---
   name: <skill-name>
   description: One-line description — used for skill discovery
   metadata:
     tags: tag1, tag2
   ---
   ```
2. Add any helper scripts to `skills/<skill-name>/scripts/`
3. Update `README.md` with the new skill entry

## Updating an Existing Skill

Work inside the submodule directory, then commit and push here.
The parent monorepo (`kvidai/`) will pick up the new ref on next `git submodule update --remote`.

```bash
# From kvidai monorepo root
cd skills/kvidai-skills
# ... edit ...
git add . && git commit -m "feat: ..."
git push

# Update submodule ref in parent
cd ../..
git add skills/kvidai-skills
git commit -m "chore: update kvidai-skills submodule"
```

## Skills Reference

| Skill | Trigger | Description |
|-------|---------|-------------|
| `kvidai-video-project` | generate video, create video project, kvidai API, 영상 생성 | Create project + AI agent SSE generate + status poll |
