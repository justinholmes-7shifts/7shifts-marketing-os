---
name: share-learning
description: "Captures a durable team learning or campaign record and contributes it to the shared 7shifts Marketing OS brain, handling the format and the git push so the user never touches git. Use when a campaign wraps, a test produces a keepable result, or the user says 'share this learning', 'push this to the brain', 'add this to learnings', 'log this campaign', or 'the team should know this'. First checks the learning is durable and transferable, not personal work-in-progress."
---

# Share Learning

Gets a durable learning from someone's local work into the shared Marketing OS brain, so the next person inherits it. You handle the judgment, the format, and the git. The user just says what they learned.

The brain repo is at `~/7shifts-marketing-os` by default. If it isn't there, ask where they cloned it.

## First, does it belong in the brain?

Push it only if it passes all three:

- **Durable:** true beyond this one campaign or this week.
- **Transferable:** the next person could actually use it.
- **Evidenced:** tied to a result or a real observation, not a hunch.

The one-line test: **would the next person running a similar campaign want to know this before they start?** If yes, push it. If it only matters to this person, or only this week (a reminder, a draft, a workflow note), it's personal memory, not a team learning. Route it to their personal memory and leave the brain alone.

When it's borderline, ask the user one question to decide. Don't guess, and don't push half-formed hunches. Evidence, or it waits.

## Where it goes

- **A single lesson** → append to `learnings.md` under the right heading (Messaging & copy, Channels, Segments & targeting, Creative & format, or What didn't work).
  Format: `YYYY-MM-DD | [channel or campaign] | what we learned, with the evidence. (name)`
- **A whole campaign wrap** → a new file in `campaigns/` (template in `campaigns/README.md`), then promote the one or two durable lines up to `learnings.md`.

## Steps

1. Confirm it passes the test above.
2. `cd ~/7shifts-marketing-os && git pull --rebase` first, so you're appending to the latest copy (this is what avoids conflicts when several people contribute).
3. Append the entry to `learnings.md` (or write the campaign file). One line, atomic.
4. `git add`, commit with a clear message (e.g. `learning: GM subject line lift`), and `git push`.
5. Tell the user exactly what you shared and where, and that the team gets it on their next `git pull`.

## Gotchas

- Always pull before you write. Several people push to this repo, so a stale write causes conflicts.
- Keep entries short and atomic. A learning is one line, not a paragraph.
- If it's personal or work-in-progress, it does not go here. That's what personal memory is for.
