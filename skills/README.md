# Team Skills

Repeatable thinking tools the whole team shares. Each skill is a folder with a `SKILL.md` (and optional `reference.md` / `examples.md`).

**Building or reviewing a skill? Use the `skill-builder` skill** (or read its `reference.md`). It encodes our standards, drawn from Anthropic's "Complete Guide to Building Skills" and Thariq's "Lessons from Building Claude Code."

## What goes here
Team-level skills, not personal ones. For example:
- **skill-builder** — how we build and review skills to a consistent standard (the nine categories, lean SKILL.md, trigger-rich descriptions, gotchas, progressive disclosure). Based on Anthropic's skill guide and Thariq's lessons. Use it before making any new skill.
- **brand-designer** — a senior 7shifts brand designer with point of view. Produces on-brand assets (social, slides, web, illustration, swag, co-brands) and pushes back on off-brand requests. Pulls the visual system from `context/brand-guidelines.md` and copy voice from `context/voice.md`.
- **lifecycle-campaign-strategy** — pressure-tests campaign strategy before build: problem-first design framework, the 11-question pressure test, measurement layers, and the evolve/retire/rebuild call. The thinking layer above execution. (Rebuilt from the team's Lifecycle & Campaign Strategy doc into proper skill shape.)
- **share-learning** — gets a durable learning or campaign record from someone's local work into this shared brain (`learnings.md` / `campaigns/`), handling the format and the git push so non-technical users never touch git. Checks the learning is durable, transferable, and evidenced first.
- **clear-communications-v2** — rate and improve any writing with the Pyramid Principle (answer first, SCQA). Generic clarity tool, useful for readouts and memos. (Shared from the CMO OS; team repo is now its canonical home.)
- **session-log** — keep a per-session work log, one dated file per session in the project's `sessions/` folder, and read the last few to pick up where you left off. Writes the file only, never commits.
- **campaign-orchestration** (Tamara) — drop the skill folder here.
- Any skill more than one person should run the same way.

## What does NOT go here
- Personal-voice skills. `justin-voice` is Justin's and lives in `7shifts-cmo-os`. The team's writing voice is `../context/voice.md`, the 7shifts brand voice.

## How skills load into Claude Code
The canonical source lives here in the repo. Claude Code only loads a skill once it's linked into `~/.claude/skills/`. This one command links every skill in this folder (safe to re-run; it skips any you already have):

```
mkdir -p ~/.claude/skills && cd ~/7shifts-marketing-os && for s in skills/*/; do n=$(basename "$s"); [ -e ~/.claude/skills/"$n" ] && echo "skip $n" || ln -s "$PWD/$s" ~/.claude/skills/"$n"; done
```

Edit the skill **here**, not in `~/.claude/skills/`. That way changes are version-controlled and the whole team gets them on `git pull`.
