# 7shifts Marketing OS

The marketing team's shared brain. One place for who we sell to, how we sound, what we've shipped, and what we've learned. We all work out of the same repo so our context and our learnings compound instead of getting trapped in separate cloud Projects.

## Why this exists

Individual cloud Projects are isolated containers. Each one is a private copy of some files. Project A can't see what Project B learned, and the files inside go stale the moment you update them somewhere else. So knowledge fragments by design.

This repo fixes that. The brain is a set of living files everyone shares. Update the brand voice once and every future piece of work uses the new version. Finish a campaign and its learnings are there for the next person. The brain gets smarter every time someone uses it.

## How to use it

Two ways, same brain:

1. **Claude Code (best)** — clone the repo, open the folder, and the whole brain loads automatically every session. No clicking into a Project. This is the power path.
2. **Desktop app** — point Claude at these files, or drag the ones you need into a chat. Good starting point if you're not on the terminal yet.

Start in whichever feels comfortable. The files are the same either way, so moving up to Claude Code later costs you nothing.

## What's in here

| Folder | What it holds |
|---|---|
| `context/` | The reference brain. `company-context.md` (what 7shifts is), `positioning.md` (how we talk about it), `icp.md` (who we sell to), `personas.md` (the 7 buyers and users), `voice.md` (how we sound), `brand-guidelines.md` (how we look), `source/` (the raw messaging guide). |
| `skills/` | The team's repeatable thinking tools (e.g. campaign orchestration). Canonical source, symlinked into Claude Code. |
| `campaigns/` | One file per campaign. Working notes and outcomes. The running log. |
| `research/` | Deep research outputs that feed the brain. |
| `readouts/` | Shareable team-facing outputs. |
| `learnings.md` | The team's accumulated memory. What worked, what didn't, one line at a time. |

## The one rule that makes it work

**Write learnings back.** The brain only compounds if people feed it. When something teaches you a durable lesson, add a line to `learnings.md` or drop a campaign file in `campaigns/`. Take from the brain, give back to the brain.

## How this relates to the CMO OS

`7shifts-cmo-os` is Justin's personal operating system. This repo is the team's. They're separate on purpose: the team brain shouldn't inherit one person's writing voice or private planning. Shared assets (like brand) live here, in the team repo.
