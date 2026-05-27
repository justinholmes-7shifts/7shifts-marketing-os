# Team Skills

Repeatable thinking tools the whole team shares. Each skill is a folder with a `SKILL.md` (and optional `reference.md` / `examples.md`).

## What goes here
Team-level skills, not personal ones. For example:
- **brand-designer** — a senior 7shifts brand designer with point of view. Produces on-brand assets (social, slides, web, illustration, swag, co-brands) and pushes back on off-brand requests. Pulls the visual system from `context/brand-guidelines.md` and copy voice from `context/voice.md`.
- **lifecycle-campaign-strategy** — pressure-tests campaign strategy before build: problem-first design framework, the 11-question pressure test, measurement layers, and the evolve/retire/rebuild call. The thinking layer above execution. (Rebuilt from the team's Lifecycle & Campaign Strategy doc into proper skill shape.)
- **share-learning** — gets a durable learning or campaign record from someone's local work into this shared brain (`learnings.md` / `campaigns/`), handling the format and the git push so non-technical users never touch git. Checks the learning is durable, transferable, and evidenced first.
- **clear-communications-v2** — rate and improve any writing with the Pyramid Principle (answer first, SCQA). Generic clarity tool, useful for readouts and memos. (Shared from the CMO OS; team repo is now its canonical home.)
- **campaign-orchestration** (Tamara) — drop the skill folder here.
- Any skill more than one person should run the same way.

## What does NOT go here
- Personal-voice skills. `justin-voice` is Justin's and lives in `7shifts-cmo-os`. The team's writing voice is `../context/voice.md`, the 7shifts brand voice.

## How skills load into Claude Code
The canonical source lives here in the repo. Symlink each one into `~/.claude/skills/` so Claude Code loads it everywhere:

```
ln -s "$(pwd)/skills/campaign-orchestration" ~/.claude/skills/campaign-orchestration
```

Edit the skill **here**, not in `~/.claude/skills/`. That way changes are version-controlled and the whole team gets them on `git pull`.
