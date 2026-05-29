---
name: session-log
description: Write or review per-session work logs. One dated file per session in the project's sessions/ folder, never one growing file. Invoke with '/session-log', 'log this session', 'close out the session', 'write the session log', 'wrap the session', 'check the last session', 'check the last couple of sessions', 'where did we leave off', or 'catch me up on recent sessions'.
---

# Session Log

Keep a per-session work log: **one file per session** in `<project>/sessions/`, named
`YYYY-MM-DD-<short-slug>.md`. A new file each session, never append to an old one. Read the last few
on command to pick up where you left off.

Why per-file: each session file is small and self-contained, and session files are **never
auto-loaded into context** (only read on command), so the history can grow forever without burning
tokens at session start. Current *state* belongs in the memory file (lean, overwritten); *history*
belongs here.

## Pick the mode from the request

### Mode A: WRITE a session log
Triggers: "/session-log", "log this session", "close out", "wrap the session", "write the session log".
1. Find the project dir: `git rev-parse --show-toplevel` (else the cwd).
2. `mkdir -p sessions`.
3. Summarize THIS session from the conversation, tight and specific (real numbers, file names,
   decisions, no fluff): What we did / Decisions / Findings / Next steps / Files touched.
4. Write `sessions/<YYYY-MM-DD>-<short-kebab-slug>.md` (slug = 2-4 words on the session's focus). If
   that exact name exists, append `-2`, `-3`. Use the template below.
5. Update the project memory file / `CLAUDE.md` "Current Focus" **only if state materially changed**.
   Keep those lean; the detail lives in this session file.

Just write the file. Do NOT commit to git. Committing is a separate decision the user makes when
they're ready, not something this skill does.

### Mode B: REVIEW recent sessions
Triggers: "check the last session", "the last couple of sessions", "where did we leave off", "catch me up".
1. List `sessions/*.md`, sort by filename (date prefix sorts chronologically).
2. Read the last N (default 2; honor "last 3", "this week", etc.).
3. Lead with **what to do next** (the most recent file's Next steps), then a 2-3 line recap of where
   things stand and any open decisions. Don't dump the files verbatim.

## Session file template
```
# Session <YYYY-MM-DD>: <focus>

## What we did
- ...

## Decisions
- ...

## Findings / numbers
- ...

## Next steps
- ...

## Files touched
- path: one-line what changed
```

## Rules
- One file per session. Never edit or append a prior session's file. History is immutable.
- Session files are reference-only history, not auto-loaded. Keep current state in the memory file.
- Be specific: numbers, names, file paths. Strip AI-fluff (no "delve", "leverage", em dashes).
- Lead Mode B with the next action, not a chronological recap.

## Gotchas
- Not in a git repo: write to `./sessions/` in the cwd and say so.
- Already logged this session: update today's file's Next steps rather than creating a duplicate,
  unless the user wants a separate one.
- This is a lightweight per-file log, not a full close-out. Durable, shareable lessons still belong
  in the brain's `learnings.md` (the `share-learning` skill handles that); session files are your own
  working history.
