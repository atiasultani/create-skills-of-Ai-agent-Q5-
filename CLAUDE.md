# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working in this repository.

## Repository Overview

This is a **Claude Code skills collection** — a repository of reusable skills (agent plugins) for Claude Code. Skills are stored under `.claude/skills/` as directories containing a `SKILL.md` file with a YAML frontmatter block and markdown body.

There is no build system, test suite, or traditional application code here. The "artifacts" are skill definitions.

## Skill Structure

Each skill lives in `.claude/skills/<skill-name>/` and consists of:

- **`SKILL.md`** — The skill definition file with:
  - **Frontmatter** (YAML `---` block): `name` and `description` fields. The `description` is what Claude matches against when deciding whether to invoke the skill.
  - **Body** (Markdown): Instructions, frameworks, and guidelines the skill provides to Claude when active.

## Existing Skills

| Skill | Location | Purpose |
|---|---|---|
| `canva-creator-and-canva-designer` | `.claude/skills/canva-creator-and-canva-designer/SKILL.md` | Expert Canva design guidance — templates, brand kits, social media, presentations, marketing materials, marketplace assets |
| `linkedin-post-creator` | `.claude/skills/linkedin-post-creator/SKILL.md` | LinkedIn content creation — professional posts, thought leadership, project showcases, career milestones |

## Working with Skills

### Adding a New Skill

1. Create a directory under `.claude/skills/<skill-name>/`.
2. Write a `SKILL.md` with YAML frontmatter (`name`, `description`) and a markdown body containing the skill's instructions.
3. The `description` field is critical — it's how Claude determines when to activate the skill. Make it specific and comprehensive.

### Editing a Skill

Modify the `SKILL.md` directly. The frontmatter `description` controls triggering; the body controls behavior when active.

### Skill Design Principles

- The `description` should clearly describe **when** the skill should be used and **what** it covers.
- The body should provide concrete frameworks, checklists, and output formats — not vague advice.
- Include "Always" / "Never" sections for clear behavioral boundaries.
- Specify an output format so responses are consistent.

## Configuration

- `.claude/settings.json` — Project-level Claude Code settings (currently empty).
