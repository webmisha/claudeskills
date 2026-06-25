# Claude Skills

Custom skills for Claude and other AI coding/product workflows. The repository is a small, practical toolkit for turning rough product ideas into clearer requirements, better user stories, sharper backlog items, and more polished frontend interfaces.

## What Is Inside

| Skill | Use it when you need to... |
| --- | --- |
| `brainstorming` | Explore an idea before implementation, compare approaches, clarify constraints, and shape a design through conversation. |
| `prd-creator` | Create a Product Requirements Document through guided discovery, scope sizing, and structured PRD generation. |
| `user-story-creator` | Write user stories, acceptance criteria, job stories, analytics stories, and technical stories using agile best practices. |
| `user-story-reviewer` | Review existing stories against INVEST, detect common story smells, score quality, and propose improvements. |
| `frontend-design` | Build distinctive, production-grade frontend UI with a strong visual direction and polished implementation details. |
| `humanizer` | Remove common signs of AI-generated writing and rewrite text so it reads more naturally. |

All skills live in [`skills/`](skills/).

## Repository Structure

```text
claudeskills/
├── README.md
└── skills/
    ├── brainstorming.skill
    ├── frontend-design.skill
    ├── humanizer.LICENSE
    ├── humanizer.skill
    ├── prd-creator.skill
    ├── user-story-creator.skill
    └── user-story-reviewer.skill
```

Most skills are plain text `.skill` files with YAML front matter and markdown instructions. `frontend-design.skill` is packaged as a zip-based skill bundle that contains `frontend-design/SKILL.md`.

## Installation

Clone the repository:

```bash
git clone https://github.com/webmisha/claudeskills.git
cd claudeskills
```

Then install the skills using the import flow supported by your Claude or agent environment. In most setups, that means importing or copying the files from the [`skills/`](skills/) directory into your local skills folder.

If your environment supports direct skill-file import, use the `.skill` files as-is. If it expects unpacked skill directories, unzip bundled skills such as `frontend-design.skill` before installing.

## Usage

Invoke a skill by asking for the matching workflow in natural language:

```text
Use brainstorming to explore a new onboarding feature.
```

```text
Create a PRD for a lightweight customer feedback portal.
```

```text
Review these user stories against INVEST and suggest improvements.
```

```text
Use frontend-design to build a polished dashboard mockup.
```

```text
Humanize this announcement and keep the original meaning.
```

The skills are designed to be conversational. Several of them intentionally start with discovery questions before producing the final output, because the quality of the result depends on understanding goals, users, constraints, and success criteria.

## Skill Guide

### Brainstorming

Use before creative or product work. It helps clarify the idea, inspect current project context, compare 2-3 possible approaches, and turn a loose request into a concrete design direction.

### PRD Creator

Use when you need a Product Requirements Document. It walks through discovery, recommends a PRD size based on complexity, and structures the document around goals, stories, requirements, UX, technical considerations, metrics, and milestones.

### User Story Creator

Use when creating backlog items from scratch. It emphasizes stories as conversation starters, supports user stories and job stories, and includes acceptance criteria patterns, INVEST validation, and story splitting strategies.

### User Story Reviewer

Use when improving existing backlog items. It scores stories against INVEST, detects smells such as over-specific UI details or hidden dependencies, and gives actionable rewrite recommendations.

### Frontend Design

Use when building web interfaces, pages, dashboards, posters, or components. It pushes for a clear aesthetic point of view, stronger typography, more intentional color, polished motion, and frontend work that feels designed rather than generic.

### Humanizer

Use when editing text that sounds AI-generated. It detects patterns such as inflated importance, promotional language, vague attributions, overused AI vocabulary, em dash overuse, formulaic conclusions, filler phrases, and other common tells. It then rewrites the text while preserving meaning and matching the intended voice.

## Contributing

1. Add or update a file in [`skills/`](skills/).
2. Keep each skill focused on one clear workflow.
3. Include front matter with at least `name` and `description`.
4. Write instructions that tell the agent when to use the skill, what process to follow, and what output to produce.
5. Test the skill with realistic prompts before opening a pull request.

Recommended front matter:

```yaml
---
name: example-skill
description: Short description of when this skill should be used.
---
```

## Maintenance Notes

- Keep skill names stable once published, because users may reference them directly.
- Prefer practical examples over abstract guidance.
- Avoid overlapping triggers between skills unless the workflows are intentionally complementary.
- Remove system files such as `.DS_Store` before publishing future updates.

## License

No repository-level license is currently included. Add a `LICENSE` file if you want to define reuse terms for the full collection.

The `humanizer` skill is based on [`blader/humanizer`](https://github.com/blader/humanizer) and is distributed under the MIT license included at [`skills/humanizer.LICENSE`](skills/humanizer.LICENSE).
