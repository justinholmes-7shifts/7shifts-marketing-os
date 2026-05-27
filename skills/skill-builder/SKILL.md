---
name: skill-builder
description: "How we build and review team skills in this repo, following Anthropic's skill guide and Thariq's 'Lessons from Building Claude Code.' Use when creating a new skill, reviewing or refactoring an existing one, or deciding whether a workflow is worth turning into a skill. Triggers on 'create a skill', 'build a skill', 'new skill', 'write a skill for', 'review this skill', 'is this skill any good', 'refactor this skill', or 'make this a team skill'. Enforces our conventions: kebab folder, lean SKILL.md, a trigger-rich description, progressive disclosure, a Gotchas section, and pull-from-the-brain over duplication."
---

# Skill Builder

How we build and review skills in this repo. Based on Anthropic's "Complete Guide to Building Skills" and Thariq's "Lessons from Building Claude Code: How We Use Skills," plus our house conventions. The full reference (the categories, the tips, distribution) is in [reference.md](reference.md).

A skill is a folder, not just a markdown file. It can hold reference docs, scripts, assets, and data that Claude discovers and uses. Treat the whole folder as context engineering.

## Before you build: is it worth a skill?

The best skills fit cleanly into one category (see reference.md for the nine). If a workflow is repeatable, has gotchas Claude keeps hitting, or encodes taste and standards Claude doesn't have by default, it's a candidate. If it straddles three categories, it's probably two skills.

Don't build a skill that states the obvious. Claude already knows general marketing and writing. A good skill pushes Claude off its defaults (our voice, our banned words, our brand system, our segments), or encodes a workflow it would otherwise rebuild from scratch each time.

## The build

1. **Name the use cases and when it should trigger.** Two or three concrete things a person would ask that should fire this skill. This becomes the description.
2. **Structure it.** Kebab-case folder, a `SKILL.md` (exact name), and optional `reference.md` / `scripts/` / `assets/`. No `README.md` inside the skill folder.
3. **Write the frontmatter.** `name` (kebab-case, matches the folder). `description` covering what it does AND when to use it, with real trigger phrases, under 1024 characters, no angle brackets. The description is what Claude scans to decide whether to load the skill, so write it for the model, not as a summary.
4. **Keep SKILL.md lean (progressive disclosure).** Core instructions only. Push detail (long tables, examples, full references) into `reference.md` and point to it. Pull shared facts from the brain (`context/`) instead of copying them, so there's one source of truth.
5. **Write a Gotchas section.** The highest-signal part of any skill. Seed it with the failure points you already know, and grow it every time Claude trips on something.
6. **Give information, not a railroad.** State what Claude needs, then leave room to adapt. Overly rigid step-by-step instructions break on the cases you didn't foresee.
7. **Test the trigger.** Fire 10 to 20 phrasings: it should load on the obvious asks and the paraphrased ones, and stay quiet on unrelated topics.

## Critical rules (the skill won't work otherwise)

- `SKILL.md` named exactly, case-sensitive.
- Folder is kebab-case (`brand-designer`, not `Brand Designer` or `brand_designer`).
- No angle brackets in the frontmatter, and no "claude" or "anthropic" in the skill name (reserved).
- No `README.md` inside the skill folder. Docs go in SKILL.md or reference files.

## House conventions for this repo

- Skills live in `skills/`, one folder each, and get an entry in `skills/README.md`.
- To load a skill in Claude Code, symlink it into `~/.claude/skills/` (pattern in `skills/README.md`). Edit it here, not there.
- No em dashes anywhere.
- Don't duplicate the brain. If a skill needs the ICP, voice, or brand, it reads `context/`, it doesn't copy it.

## Gotchas

- The number-one reason a skill silently never runs: missing or weak frontmatter, or a description with no trigger phrases. Check that first.
- A 300-line monolithic SKILL.md is a structure problem, not a content problem. Split it: lean SKILL.md plus reference.md.
- Data stored inside a skill folder can be wiped on upgrade. For anything that must persist, use a stable location, not the skill directory.
- Skills reference each other by name. If one skill should call another, name it and Claude will invoke it when it's installed.

See [reference.md](reference.md) for the nine skill categories, the full authoring tips, testing depth, and how we distribute and curate skills.
