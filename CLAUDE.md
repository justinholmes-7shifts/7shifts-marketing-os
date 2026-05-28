# Claude Context — 7shifts Marketing OS

This repo is the 7shifts marketing team's shared brain. One source of truth for who we sell to, how we sound, what we've shipped, and what we've learned. Everyone on the team clones it and works out of it, so context and learnings compound instead of scattering across individual cloud Projects.

This file loads on every session. Keep it curated. Durable team truth lives here. Anything that's only sometimes relevant lives in `context/` or `learnings.md`, not here.

## How to work in this repo
- **Start here, then pull what you need.** This file orients you. The deep reference lives in `context/`. Reference these when the task needs them:
  - `context/company-context.md` — what 7shifts is, business model, products, proof points, strategy
  - `context/positioning.md` — value prop, differentiators, competitors, messaging pillars, ROI stats
  - `context/icp.md` — segments (Best/Strong/Emerging/Selective fit), market size, GTM motion by segment
  - `context/personas.md` — the 7 buyers and users (Chloe, Mike, Olivia, Daniel, George, Michelle, Jason)
  - `context/framework.md` — shared vocabulary: lifecycle stages, program types, channels
  - `context/voice.md` — how we write: tone, banned words, AP style, the tone scale
  - `context/brand-guidelines.md` — the visual system: color, type, logo, photography, bento
  - `context/source/` — the raw 2025 Product Messaging Guide (xlsx + dump) behind positioning
- **Tool choice.** A one-off you can finish in a chat, do it in chat. Anything ongoing that needs memory and this shared context, work in Claude Code with the brain loaded. Start without skip-permissions, then turn it on once you trust it (your files are git-backed, so a wrong move is an undo).
- **Brand is not optional.** Any visual or written artifact pulls styling from `context/brand-guidelines.md` and tone from `context/voice.md`. Do not invent colors, fonts, layout, or voice defaults.
- **Write learnings back.** When a campaign or piece of research teaches us something durable (a subject line that won, a segment that converted, a channel that flopped), add a line to `learnings.md`. That is how the brain compounds.
- **One file per campaign.** Working notes and outcomes for a campaign go in `campaigns/`. That's the running log. Distil the durable parts up into `learnings.md`.

## The three layers (why content is split)
- **CLAUDE.md (this file)** — loaded in full every session, so it stays small and durable. Standing team truth only.
- **context/** — the deep reference. Loaded when a task needs it, so it can be detailed.
- **learnings.md + campaigns/ + research/** — the accumulating memory. The raw log distils up into `learnings.md` and, when structural, into this file.

## Relationship to other repos
- `7shifts-cmo-os` is Justin's **personal** operating system (his voice, his planning). Not the team brain. Do not copy personal-voice skills into this repo.
- The team voice in `context/voice.md` is the **7shifts brand voice**, which is distinct from any one person's writing voice.

## Skills
- Team skills live in `skills/` (e.g. campaign orchestration). The canonical source is here; symlink into `~/.claude/skills/` so Claude Code loads them everywhere. Edit them here, not in `~/.claude/skills/`.

## Notes
- This is a docs/ops repo, not an app. No stack, no deploy. Mostly markdown.
- Work in Claude Code with the brain loaded for anything ongoing (see Tool choice above). Quick one-offs are fine in chat. Same files either way.
