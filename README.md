# 7shifts Marketing OS

The Growth Marketing team's shared brain: who we sell to, how we sound, what we've shipped, and what we've learned. Everyone clones it and works alongside it, so our context and learnings compound in one place instead of scattering across eight laptops.

## Start here (about 10 minutes)

New to Claude Code? Set up your own personal workspace first ([`docs/set-up-your-workspace.md`](docs/set-up-your-workspace.md), about 15 minutes), then do these four steps.

**Before you clone, get access.** This is a private repo. Ask Justin for a GitHub invite to `justinholmes-7shifts/7shifts-marketing-os` and accept it. Then connect git on your machine the easy way (install the GitHub CLI first if you need it with `brew install gh`, and pick HTTPS when asked):

```
gh auth login
```

**1. Clone this as a sibling to your workspace** (not inside it, it's its own git repo):

```
cd ~
git clone https://github.com/justinholmes-7shifts/7shifts-marketing-os.git
```

You'll have two folders side by side: your personal `~/your-workspace/` and `~/7shifts-marketing-os/`.

**2. Point your CLAUDE.md at it.** Add this line so Claude reads the brain every session:

> The 7shifts Marketing OS team brain lives at `~/7shifts-marketing-os`. For anything involving brand, ICP, positioning, personas, voice, or a team skill, read from there first. It is the source of truth.

**3. Install the team skills.** They live in the repo, but Claude Code only loads them once they're linked into `~/.claude/skills/`. One command links all of them:

```
mkdir -p ~/.claude/skills && cd ~/7shifts-marketing-os && for s in skills/*/; do ln -s "$(pwd)/$s" ~/.claude/skills/"$(basename "$s")"; done
```

Now `brand-designer`, `lifecycle-campaign-strategy`, `clear-communications-v2`, `share-learning`, and `skill-builder` work in any session. Edit them in the repo, not in `~/.claude/skills/`, so a `git pull` keeps everyone current. (More in [`skills/README.md`](skills/README.md).)

**4. Run `git pull` when you start working,** so you always have the latest.

Set up? Run your first play from [`docs/starter-plays.md`](docs/starter-plays.md) to feel the payoff in week one.

## When to use the brain, and when not

- **Pull from it constantly.** Writing copy, planning a campaign, needing the ICP or a persona, checking positioning, running a team skill. Read from it, don't retype it.
- **Push to it deliberately.** When a campaign produces something durable (a reusable brief, a result, a learning), add the record to `campaigns/` and promote the lesson to `learnings.md`, then push.
- **Keep your work-in-progress on your own machine.** Drafts, notes, and anything people-related stay in your personal workspace, never here.

## Organizing your campaign work

One folder per campaign in your personal workspace under `Projects/`, named to sort (`YYYY-QN-name`). Do the work there. When it wraps or teaches you something, write the record into this brain's `campaigns/` (template in `campaigns/README.md`) and promote the lesson to `learnings.md`. Skip organizing by lifecycle stage, stage is a tag, not a folder.

## Contributing back to the brain

The Marketing OS is its own git repo, separate from your workspace. Anything you add or change here is local until you push it, so the team only sees it once you do. Two ways to push, depending on what you're contributing.

**The easy path (learnings and campaign records).** Tell Claude "share this learning" or "log this campaign." The `share-learning` skill checks it's worth keeping, writes it in the right place, and runs the pull, commit, and push for you. You never touch git.

**The general path (editing a shared file like positioning or voice).** Bigger changes follow the normal git flow, and Claude can run it for you if you ask ("commit and push this to the brain"):

1. `git pull` first, so you're working off the latest.
2. Make the change.
3. `git add`, commit with a clear message, then `git push`.

The one rule either way: **pull before you push.** Several people contribute to this repo, so starting from the latest copy keeps it conflict-free.

## What's in here

| Folder | What it holds |
|---|---|
| `context/` | The reference brain: company-context, positioning, icp, personas, voice, brand-guidelines + assets, framework. |
| `skills/` | Team skills: brand-designer, lifecycle-campaign-strategy, clear-communications-v2. |
| `campaigns/` | The shared campaign record. You contribute here. |
| `learnings.md` | The team's accumulated lessons. You contribute here. |
| `docs/` | How it fits with your personal workspace (`how-this-fits-with-your-workspace.md`, plus a shareable HTML version `how-it-fits.html`), and other team notes. |

## Why this exists

Individual cloud Projects (and private local folders) are isolated containers. Each is a private copy that goes stale the moment someone updates the real thing somewhere else. Eight people, eight copies of the brand guidelines, and the day brand changes the palette, seven are quietly wrong. This repo fixes that: one living source everyone shares, that gets smarter every time someone feeds a learning back in.

## How this relates to the CMO OS

`7shifts-cmo-os` is Justin's personal operating system. This repo is the team's. They're separate on purpose: the team brain shouldn't inherit one person's writing voice or private planning. Shared assets like brand live here.
