# PRD Creator - Claude Code Plugin

Creates Product Requirements Documents (PRD) through interactive conversation. Guides users through Epic/Feature/Story structure with progressive disclosure.

## Overview

PRD Creator is a Claude Code plugin that acts as a professional Product Manager, collaborating with you to create comprehensive PRDs. It focuses exclusively on **user-perspective requirements** -- what users need, not how to build it.

### Key Features

- **Two Modes**: Simple (5 steps, ~15-30 min) and Standard (9 steps, ~45-90 min) based on project complexity
- **Guided Workflow**: Step-by-step questions with A/P/R/C menu (Advanced, Previous, Research, Continue)
- **Agile Structure**: Outputs organized as Epic > Feature > User Story
- **Session Recovery**: Saves progress to files, automatically resumes interrupted sessions
- **Multilingual**: Detects and responds in the user's language

### Workflow

| Step | Name | Mode |
|------|------|------|
| 1 | Welcome & Big Picture | All |
| 2 | Problem Discovery | Standard |
| 3 | User Discovery | All |
| 4 | Journey Mapping | Standard |
| 5 | Requirements Elicitation | All |
| 6 | Scope Definition | All |
| 7 | Success & Risks | Standard |
| 8 | Rules & Constraints | Standard |
| 9 | Generate PRD | All |

## Installation

### As a Claude Code Plugin

Add to your project's `.claude/plugins.json`:

```json
[
  {
    "url": "https://github.com/idnotbe/prd-creator"
  }
]
```

Or if the repo is cloned locally alongside your project, Claude Code will auto-discover it from the VS Code workspace.

### Manual Setup

Copy the skill files into your project:

```bash
cp -r .claude/skills/prd-creator /path/to/your/project/.claude/skills/
```

## Usage

Invoke the skill by asking Claude Code to create a PRD:

```
/prd-creator
```

Or naturally:
- "Create a PRD for my project"
- "I need to define product requirements"
- "Help me plan my MVP features"

## Output

- **Working files**: Saved to `docs/requirements/temp/` during the session
- **Final PRD**: Saved to `docs/requirements/PRD-{ProjectName}-v{N}-{YYYYMMDD}.md`

## What's In Scope

- User requirements (WHAT users need)
- Problem definition (WHY it matters)
- User personas and journeys
- Feature priorities (MVP vs Post-MVP)
- Success metrics (user-facing outcomes)

## What's Out of Scope

- Technical architecture (database, API, infrastructure)
- Programming languages or frameworks
- UI wireframes or mockups
- Deployment or DevOps concerns

## Validation

This is a pure-markdown plugin with no executable code. Traditional unit/integration tests do not apply.

Structural validation (plugin.json integrity, file reference checks, step completeness) should be used instead. See [test-plan.md](action-plans/test-plan.md) for the full validation roadmap and [CLAUDE.md](CLAUDE.md) for contributor guidance.

**Known issue**: The README documents /prd-creator as the invocation command, but SKILL.md uses name: creating-prds. See action-plans/test-plan.md P1 for the fix plan.

## License

MIT License - See [LICENSE](LICENSE) for details.
