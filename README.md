# 7shifts Marketing OS

The Growth Marketing team's shared brain: who we sell to, how we sound, what we've shipped, and what we've learned. Everyone works alongside it, so our context and learnings compound in one place instead of scattering across eight laptops.

## Start here (about 10 minutes)

New to Claude Code? Set up your own personal workspace first ([`docs/set-up-your-workspace.md`](docs/set-up-your-workspace.md), about 15 to 20 minutes the first time). The commands below assume macOS. On Windows, run them inside WSL.

You've got the zip Justin shared. Here's the 10-minute setup, and you don't need GitHub access for any of it yet.

**1. Unzip it into your home folder so you end up with `~/7shifts-marketing-os`.** It sits next to your workspace, not inside it. If the unzipped folder has a longer name, rename it to `7shifts-marketing-os`.

> Already have GitHub access and prefer git? Skip the zip: `cd ~ && git clone https://github.com/justinholmes-7shifts/7shifts-marketing-os.git`

**2. Point your CLAUDE.md at it.** Add this line so Claude reads the brain every session:

> The 7shifts Marketing OS team brain lives at `~/7shifts-marketing-os`. For anything involving brand, ICP, positioning, personas, voice, or a team skill, read from there first. It is the source of truth.

**3. Install the team skills.** They live in the folder, but Claude Code only loads them once they're linked into `~/.claude/skills/`. This one command links all of them. It's safe to run again, and it leaves alone any skill you already have:

```
mkdir -p ~/.claude/skills && cd ~/7shifts-marketing-os && for s in skills/*/; do n=$(basename "$s"); [ -e ~/.claude/skills/"$n" ] && echo "skip $n (already there)" || ln -s "$PWD/$s" ~/.claude/skills/"$n"; done
```

Now `brand-designer`, `lifecycle-campaign-strategy`, `clear-communications-v2`, `share-learning`, and `skill-builder` work in any session. Already have your own skill with one of those names? It's left untouched. To use the team version instead, remove yours first (`rm ~/.claude/skills/<name>`) and run the command again. Edit skills in the folder, not in `~/.claude/skills/`. (More in [`skills/README.md`](skills/README.md).)

**4. Run a starter play** from [`docs/starter-plays.md`](docs/starter-plays.md) to feel the payoff in week one.

## Getting updates and pushing your learnings back

The copy Justin shared is connected to the live repo, so once he gives you access you can pull updates and contribute back.

- **Get the latest:** from inside `~/7shifts-marketing-os`, run `git pull`.
- **Push a learning or campaign record:** tell Claude "share this learning" and it handles the commit and push for you. You never touch git.

Justin is sorting out repo access. If a `git pull` or push asks you to sign in, install the GitHub CLI (`brew install gh`), run `gh auth login` (pick HTTPS), or just ping Justin. If your copy turns out not to be connected to git, ping Justin and he'll swap you onto one that is.

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
| `skills/` | Team skills: brand-designer, lifecycle-campaign-strategy, clear-communications-v2, share-learning, skill-builder. |
| `campaigns/` | The shared campaign record. You contribute here. |
| `learnings.md` | The team's accumulated lessons. You contribute here. |
| `docs/` | How it fits with your personal workspace (`how-this-fits-with-your-workspace.md`, plus a shareable HTML version `how-it-fits.html`), and other team notes. |

**The team skills** (fuller write-ups in [`skills/README.md`](skills/README.md)):

- **brand-designer** — a senior 7shifts designer with a point of view. On-brand social posts, slides, web modules, and ad creative, and it pushes back on off-brand asks.
- **lifecycle-campaign-strategy** — pressure-tests a campaign before you build it: the customer outcome, the one business metric, the audience, and the kill condition.
- **clear-communications-v2** — tightens any writing with the Pyramid Principle, answer first. Good for readouts and memos.
- **share-learning** — gets a durable learning or campaign record into the brain and does the git push for you, so you never touch a command line.
- **skill-builder** — how we build and review new skills to one standard, from Anthropic's skills guide. Use it before you make a new one.
- **session-log** — keeps a per-session work log, one dated file per session, so you (or the next session) can pick up where you left off. Writes the file only, never commits.

## Why this exists

Individual cloud Projects (and private local folders) are isolated containers. Each is a private copy that goes stale the moment someone updates the real thing somewhere else. Eight people, eight copies of the brand guidelines, and the day brand changes the palette, seven are quietly wrong. This repo fixes that: one living source everyone shares, that gets smarter every time someone feeds a learning back in.

## How this relates to the CMO OS

`7shifts-cmo-os` is Justin's personal operating system. This repo is the team's. They're separate on purpose: the team brain shouldn't inherit one person's writing voice or private planning. Shared assets like brand live here.
