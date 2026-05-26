---
name: clear-communications-v2
description: "Rate and improve communication clarity using the Pyramid Principle. Invoke when user says 'use my clear communication skill', 'apply clear communications', or 'rate this with pyramid principle'. If user says 'rate this', 'how clear is this', 'review my message', or asks for feedback on written communication, ASK if they want to apply this skill before proceeding."
---

# Clear Communications

Rate any written communication on a 1-5 scale for clarity and structure using the Pyramid Principle.

## Steps

1. **Find the main message.** Can you state it in one sentence? Where does it appear? It should be first. If someone only read the first line, would they know what this is about?

2. **Check structure.** Does it follow SCQA (Situation → Complication → Question → Answer)? Are supporting points grouped logically (2-4 points, same kind)? Is there a clear ask or next step?

3. **Score it.** Load [reference.md](reference.md) for the rating scale and output format. Score 1-5 based on where the main message appears and how clear the ask is. Load [examples.md](examples.md) for before/after calibration if needed.

4. **Deliver feedback.** Use the output format from reference.md: rating with label, what's working, what to change to reach the next level, and a rewritten opening that leads with the answer.

## Gotchas
- SCQA is a thinking tool, not a writing format -- the output should read naturally, not like a filled-in template with headers labeled "Situation" / "Complication"
- Justin's Pyramid Principle confidence is ~60% -- skill should model the framework correctly even when the input is informal
- Short Slack messages (1-3 sentences) don't need full SCQA analysis -- just check that the ask is clear and the main point is first
- Don't rewrite the entire message in the feedback -- rewrite only the opening to show the principle, then let Justin adapt the rest
- "Rate this" without context means "rate this communication" -- ask if they want this skill applied, don't assume
