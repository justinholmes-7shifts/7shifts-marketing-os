# Set up your personal Claude Code workspace

Before the shared brain is useful, you need your own workspace: the folder where you actually work, with your own `CLAUDE.md` and memory. It lives on your machine and never gets shared. This takes about 15 to 20 minutes the first time. The commands here assume macOS; on Windows, run them inside WSL.

The restaurant version: this is your own station, set up the way you like it. The [Marketing OS](../README.md) is the walk-in the whole kitchen shares. Set up your station first, then connect the walk-in.

## 1. Install Claude Code

Two ways to run it. If you're new, start with the desktop app and add the terminal later.

- **Desktop app (recommended):** download from [claude.ai/code](https://claude.ai/code) and sign in with your 7shifts Google account.
- **Terminal (optional, more technical):** you'll need Homebrew ([brew.sh](https://brew.sh)) and Node. Install them with `brew install node gh`, then `npm install -g @anthropic-ai/claude-code`. Run `claude` inside any folder to start.

## 2. Make your workspace folder

Pick one home for your marketing work:

```
mkdir -p ~/marketing-workspace/Projects
cd ~/marketing-workspace
```

`Projects/` is where one folder per campaign lives, named to sort: `2026-Q3-summer-payroll-push`. One campaign, one folder. (Keep work-in-progress and anything people-related here, never in the shared brain.)

## 3. Create your CLAUDE.md

This is the file Claude reads first, every session. It holds your standing context: who you are, what you own, how you like to work. Create `~/marketing-workspace/CLAUDE.md` and start small:

```
# [Your name]'s Marketing Workspace

## Who I am
[Your role on the Growth Marketing team, what you own.]

## How I work
- [Preferences: how blunt you want feedback, formats you like, tools you use.]

## Current focus
- [What you're working on this quarter.]
```

Keep it short. Add to it whenever you catch yourself re-explaining the same thing twice.

## 4. Let Claude remember things

Claude Code keeps a memory across sessions. When you tell it something worth keeping ("we always use the Oxford comma," "my SDR counterpart is Kevin"), say "remember that" and it saves. You don't manage memory files by hand.

## 5. Connect the shared brain

Your station is ready. Go back to the [README](../README.md) "Start here" steps to set up the Marketing OS next to your workspace (from the zip Justin shared, or a git clone if you have access), point your CLAUDE.md at it, and install the team skills.

That's the whole setup: your station first, then the shared walk-in.
