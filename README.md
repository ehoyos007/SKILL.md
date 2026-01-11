# Claude Code Skills Library

A collection of skills for [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

## What are Skills?

Skills are reusable prompts that extend Claude Code's capabilities. Each skill is defined in a `SKILL.md` file with frontmatter metadata and instructions that guide Claude's behavior for specific tasks.

## Installation

Install skills using [upd-skill](https://github.com/anthropics/agent-skills-upd):

```bash
# Install a specific skill globally
uvx upd-skill <username>/<skill-name> --repo <repo-name> --global

# Install a specific skill to current project
uvx upd-skill <username>/<skill-name> --repo <repo-name>
```

## Creating a Skill

Each skill is a directory containing at minimum a `SKILL.md` file:

```
my-skill/
  SKILL.md           # Required: Skill definition
  references/        # Optional: Reference documents
  scripts/           # Optional: Helper scripts
  src/               # Optional: Source code
```

### SKILL.md Format

```markdown
---
name: my-skill
description: "Brief description of what the skill does and when to use it."
license: MIT
---

Instructions for Claude when this skill is activated.

## Section 1
Detailed guidance...

## Section 2
More instructions...
```

### Frontmatter Fields

| Field | Required | Description |
|-------|----------|-------------|
| `name` | Yes | Skill identifier (kebab-case) |
| `description` | Yes | When/how to use the skill (shown in skill list) |
| `license` | No | License identifier or reference |

## Skills in This Library

| Skill | Description |
|-------|-------------|
| [compound-engineering](./compound-engineering/) | Compound Engineering workflow for AI-assisted development |
| [dev-browser](./dev-browser/) | Browser automation with persistent page state |
| [docx](./docx/) | Document creation, editing, and analysis for .docx files |
| [frontend-design](./frontend-design/) | Create distinctive, production-grade frontend interfaces |
| [pdf](./pdf/) | PDF manipulation toolkit for text extraction, creation, and forms |
| [prd](./prd/) | Generate Product Requirements Documents |
| [ralph](./ralph/) | Set up Ralph for autonomous feature development |
| [session-start-hook](./session-start-hook/) | Startup hooks for Claude Code on the web |

## License

See individual skill directories for licensing information.
