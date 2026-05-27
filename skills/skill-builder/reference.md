# Skill Builder: Reference

The full standard, from Anthropic's "Complete Guide to Building Skills" and Thariq's "Lessons from Building Claude Code: How We Use Skills." SKILL.md has the workflow and the rules; this is the detail.

## The nine skill categories (what's worth making)

The best skills fit cleanly into one. Use this list to spot gaps in what the team has. Most of ours will be categories 1, 4, 5, and 6.

1. **Library & API reference** — how to correctly use a library, CLI, or system, with reference snippets and gotchas. *Our marketing version:* `brand-designer` (how to use the 7shifts design system).
2. **Product verification** — how to test or verify that something works, often paired with a tool. *Marketing version:* a pre-launch campaign-QA checklist.
3. **Data fetching & analysis** — connect to data and monitoring; canonical tables, dashboard IDs, common queries.
4. **Business process & team automation** — turn a repetitive workflow into one command. *Ours:* `share-learning`.
5. **Code scaffolding & templates** — generate boilerplate for a recurring structure. *Marketing version:* a campaign-brief or readout template.
6. **Code quality & review** — enforce standards and review work. *Ours:* `clear-communications-v2` (reviews writing clarity).
7. **CI/CD & deployment** — fetch, push, deploy. Less relevant for marketing.
8. **Runbooks** — take a symptom, walk a multi-tool investigation, produce a structured report.
9. **Infrastructure operations** — routine maintenance, with guardrails on destructive actions.

## Authoring tips

- **Don't state the obvious.** Claude has strong defaults. A knowledge skill should push it off them (our voice, banned words, brand system), the way Anthropic's frontend-design skill steers Claude away from Inter and purple gradients.
- **The Gotchas section is the highest-signal content.** Build it from real failures and keep adding as Claude hits new edges. Most skills start as a few lines and one gotcha.
- **Use the filesystem and progressive disclosure.** A skill is a folder. Split detail into `reference.md`, put output templates in `assets/`, put helpers in `scripts/`. Tell Claude what's in the folder and it reads files at the right time.
- **Avoid railroading.** Skills are reusable, so over-specific instructions break on cases you didn't foresee. Give the information and the room to adapt.
- **Think through setup.** If a skill needs user-specific context (a Slack channel, a path), store it in a `config.json` in the skill and have Claude ask for it when it's missing. Use the `AskUserQuestion` tool for structured choices.
- **The description field is for the model.** Claude scans every skill's description to decide what to load. It's a description of when to trigger, not a human summary.
- **Memory and stored data.** A skill can keep state (an append-only log, JSON, even SQLite) so it learns from its own history. Store it in a stable location, not the skill folder, which can be wiped on upgrade.
- **Store scripts and generate code.** Helper functions let Claude spend its turns composing rather than rewriting boilerplate.
- **On-demand hooks.** A skill can register hooks that live only for the session it's invoked in, useful for opinionated guardrails you don't want on all the time.

## Testing

- **Triggering tests.** 10 to 20 phrasings. Should fire on obvious and paraphrased asks, stay quiet on unrelated topics. Undertriggering means the description needs more detail and keywords; overtriggering means add negative cases and tighten it.
- **Functional tests.** Does it produce the right output, handle errors, cover edge cases.
- **Performance comparison.** Same task with and without the skill: fewer clarifying questions, fewer retries, fewer tokens, more consistent output.

Iterate on a single hard case until it works, then generalize.

## Frontmatter fields

- **name** (required) — kebab-case, matches the folder, no "claude" or "anthropic".
- **description** (required) — what it does + when to use it, with trigger phrases, under 1024 characters, no angle brackets.
- **license** (optional) — if open-sourcing.
- **compatibility** (optional, 1 to 500 chars) — environment requirements.
- **metadata** (optional) — author, version, etc.

## Distribution and curation

- **Small team across few repos (that's us): check skills into the repo** under `skills/`. Simple, everyone gets them on clone. Every checked-in skill adds a little to context, so keep the set curated.
- **At scale: a plugin marketplace** lets people choose what to install. Find the useful skills organically: park a new one, point people to it, promote it once it gets traction. Curate before release, it's easy to make redundant or low-quality skills.

## Composing skills

Skills can depend on each other. There's no formal dependency system, you reference another skill by name and Claude invokes it if it's installed. Example: `share-learning` could call a future `campaign-recap` skill to format the record before pushing.
