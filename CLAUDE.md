# prd-creator -- Claude Code Plugin

## What This Is

A pure-markdown Claude Code plugin for guided PRD (Product Requirements Document) creation. Contains no executable code -- only markdown skill definitions, a JSON manifest, and supporting docs.

The plugin acts as an interactive Product Manager, guiding users through a stepwise conversation (Simple or Standard mode) to produce structured PRDs using Epic > Feature > User Story hierarchy.

## Repo Structure

- .claude/skills/prd-creator/ -- Skill definition (SKILL.md, 9 step files, 2 mode configs, 3 resource docs)
- .claude-plugin/plugin.json -- Plugin manifest
- README.md -- User-facing documentation
- LICENSE -- MIT license

## Validation

This is a markdown-only plugin. Traditional unit tests do not apply.

**All validation infrastructure belongs in this repo.** Currently none exists -- it needs to be built. See TEST-PLAN.md for the roadmap.

Validation for this plugin means **structural integrity**:
- plugin.json is valid JSON
- Paths in plugin.json skills array resolve to existing directories
- Files referenced in SKILL.md (steps, modes, resources) exist on disk
- Step numbering in filenames matches workflow tables in SKILL.md
- Optional: markdown linting for formatting consistency

Validation does **not** mean unit tests, integration tests, or runtime behavior checks. Runtime behavior depends on the Claude Code host, not this repo.

## Known Issues

- **Invocation mismatch**: README documents /prd-creator as the command, but SKILL.md frontmatter sets name: creating-prds. The plugin.json name is prd-creator. This should be aligned.

## Conventions

- Keep all internal paths relative
- Do not introduce executable code unless justified -- this is a markdown-only plugin
- Update cross-references (SKILL.md workflow tables, mode files, step files) when renaming or reordering
- All committed content must be in English
