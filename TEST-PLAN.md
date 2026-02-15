# TEST-PLAN.md -- prd-creator Validation Roadmap

This plugin is pure markdown with no executable code. Traditional unit/integration tests do not apply. Validation means verifying structural integrity: that the manifest is valid, file references resolve, and content is well-formed.

---

## P0: Structural Validation (Minimum Viable)

### validate.sh script
Create a shell script that checks:
1. **JSON validity**: plugin.json parses without errors
2. **Skill path resolution**: Every path in plugin.json skills array points to an existing directory
3. **File reference integrity**: All files referenced in SKILL.md (steps/, modes/, resources/) exist on disk
4. **Step completeness**: Step filenames (01 through 09) match the workflow tables in SKILL.md

### CI pipeline
- Add a GitHub Actions workflow (.github/workflows/validate.yml)
- Runs validate.sh on every push and pull request
- Fails the build if any structural check fails

---

## P1: Quality Assurance

### Fix invocation alignment
- Align SKILL.md name field with plugin.json name and README invocation command
- Either rename SKILL.md name to prd-creator or add explicit triggers including /prd-creator

### QA checklist (QA-CHECKLIST.md)
Manual smoke test procedures:
- Simple mode walkthrough (5 steps, end-to-end)
- Standard mode walkthrough (9 steps, end-to-end)
- Session recovery (interrupt mid-session, reopen, verify resume)
- A/P/R/C menu navigation (each option exercised at least once)
- File output verification (temp files created in docs/requirements/temp/, final PRD in docs/requirements/)

### CLAUDE.md
- Add project guidance file for contributors and Claude Code context (done if you are reading this)

---

## P2: Extended Validation

### Golden examples
- Save 1-2 example session transcripts and resulting PRDs as regression baselines
- Store in a tests/golden/ directory
- Document expected output structure for comparison

### Markdown linting
- Add .markdownlint.json configuration
- Include markdownlint in CI pipeline
- Check all 15+ markdown files for formatting consistency, broken headers, malformed tables

### Variable consistency check
- Verify template variables (like {project-slug}) are consistent across all step files
- Check that placeholder patterns in prd-template.md match what step files produce

---

## Out of Scope

The following are explicitly not part of the validation plan:
- Unit tests (no executable code to test)
- Integration tests (runtime behavior depends on Claude Code host)
- Performance tests (not applicable)
- End-to-end automation of the conversational workflow (would require LLM-in-the-loop testing)
