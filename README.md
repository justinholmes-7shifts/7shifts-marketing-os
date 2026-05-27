# 7shifts Marketing OS

The Growth Marketing team's shared brain: who we sell to, how we sound, what we've shipped, and what we've learned. Everyone clones it and works alongside it, so our context and learnings compound in one place instead of scattering across eight laptops.

## Start here (about 10 minutes)

New to Claude Code? Set up your personal workspace first with Tamara's "Claude Code Setup" doc, then do these three steps.

**1. Clone this as a sibling to your workspace** (not inside it, it's its own git repo):

```
cd ~
git clone https://github.com/justinholmes-7shifts/7shifts-marketing-os.git
```

You'll have two folders side by side: your personal `~/your-workspace/` and `~/7shifts-marketing-os/`.

**2. Point your CLAUDE.md at it.** Add this line so Claude reads the brain every session:

> The 7shifts Marketing OS team brain lives at `~/7shifts-marketing-os`. For anything involving brand, ICP, positioning, personas, voice, or a team skill, read from there first. It is the source of truth.

**3. Run `git pull` when you start working,** so you always have the latest.

## When to use the brain, and when not

- **Pull from it constantly.** Writing copy, planning a campaign, needing the ICP or a persona, checking positioning, running a team skill. Read from it, don't retype it.
- **Push to it deliberately.** When a campaign produces something durable (a reusable brief, a result, a learning), add the record to `campaigns/` and promote the lesson to `learnings.md`, then push.
- **Keep your work-in-progress on your own machine.** Drafts, notes, and anything people-related stay in your personal workspace, never here.

## Organizing your campaign work

One folder per campaign in your personal workspace under `Projects/`, named to sort (`YYYY-QN-name`). Do the work there. When it wraps or teaches you something, write the record into this brain's `campaigns/` (template in `campaigns/README.md`) and promote the lesson to `learnings.md`. Skip organizing by lifecycle stage, stage is a tag, not a folder.

## What's in here

| Folder | What it holds |
|---|---|
| `context/` | The reference brain: company-context, positioning, icp, personas, voice, brand-guidelines + assets, framework. |
| `skills/` | Team skills: brand-designer, lifecycle-campaign-strategy, clear-communications-v2. |
| `campaigns/` | The shared campaign record. You contribute here. |
| `learnings.md` | The team's accumulated lessons. You contribute here. |
| `docs/` | How this fits with your personal workspace, and other team notes. |

## Why this exists

Individual cloud Projects (and private local folders) are isolated containers. Each is a private copy that goes stale the moment someone updates the real thing somewhere else. Eight people, eight copies of the brand guidelines, and the day brand changes the palette, seven are quietly wrong. This repo fixes that: one living source everyone shares, that gets smarter every time someone feeds a learning back in.

## How this relates to the CMO OS

`7shifts-cmo-os` is Justin's personal operating system. This repo is the team's. They're separate on purpose: the team brain shouldn't inherit one person's writing voice or private planning. Shared assets like brand live here.
