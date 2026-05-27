# Getting started with the Marketing OS

This is the team's shared brain: brand, ICP, positioning, personas, voice, and skills. You clone it once, work alongside it, and contribute back as you learn. About 10 minutes to wire up.

> New to Claude Code entirely? Set up your personal workspace first with Tamara's "Claude Code Setup" doc, then come back here. The two fit together, see [docs/how-this-fits-with-your-workspace.md](docs/how-this-fits-with-your-workspace.md).

## 1. Clone it as a sibling to your workspace

Clone the brain next to your personal workspace, not inside it. It's its own git repo, and nesting one repo inside another gets messy.

```
cd ~
git clone https://github.com/justinholmes-7shifts/7shifts-marketing-os.git
```

You should end up with two folders side by side:

```
~/your-workspace/           ← your personal workspace (from Tamara's setup)
~/7shifts-marketing-os/     ← the shared brain (this repo)
```

## 2. Point your CLAUDE.md at it

Add a line to your personal `CLAUDE.md` so Claude knows the brain exists and reads from it:

> The 7shifts Marketing OS team brain lives at `~/7shifts-marketing-os`. For anything involving brand, ICP, positioning, personas, voice, or a team skill, read from there first. It is the source of truth.

## 3. Keep it current

Run `git pull` when you start working. When someone updates the voice file or adds a learning, you get it. That is the whole point of one shared copy.

## When to use the brain, and when not

**Read from it (most substantive work).** Any time you write copy, plan a campaign, need the ICP or a persona, check positioning, or want a team skill (brand-designer, lifecycle-campaign-strategy, clear-communications). Pull from it, don't retype it.

**Write to it (deliberately).** When a campaign produces something durable: a final brief worth reusing, a result, a learning. Add the record to `campaigns/`, promote the lesson to `learnings.md`, then commit and push. That is how the team compounds.

**Don't put your day-to-day working files in it.** Drafts, notes, and half-built assets stay in your personal workspace. The brain holds the shared, finished, reusable stuff, not everyone's work-in-progress.

## Organizing your campaign work

One folder per campaign, in your personal workspace under `Projects/`. Name them so they sort: `YYYY-QN-name`.

```
~/your-workspace/Projects/
├── 2026-q3-summer-labor-cost/
│   ├── brief.md
│   ├── assets/
│   └── notes.md
└── 2026-q3-payroll-attach/
```

The flow:

1. Do the work in `Projects/<campaign>/`. This is yours: your drafts and notes.
2. When it wraps or teaches you something, write the record into this brain's `campaigns/` (one file per campaign, template in `campaigns/README.md`) and promote the durable lesson to `learnings.md`.
3. Push. Now the next person inherits it.

Skip organizing by lifecycle stage. Stage is a tag, not a folder. Keep the folders flat, one per campaign.

## What's in the brain

- `context/` — company context, positioning, ICP and segment sizing, personas, voice, brand guidelines and assets, framework vocabulary
- `skills/` — brand-designer, lifecycle-campaign-strategy, clear-communications-v2
- `campaigns/` — the shared campaign record (you contribute here)
- `learnings.md` — the team's accumulated lessons (you contribute here)
