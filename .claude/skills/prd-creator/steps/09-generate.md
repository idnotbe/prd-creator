# Step 9: Generate PRD

## Purpose
모든 단계의 정보를 통합하여 최종 PRD 문서를 생성합니다.

---

## Execution Flow

### Step 9 Process

1. **Read all intermediate step files** from `docs/requirements/temp/`:
   - `01-welcome-{project-slug}-v*-*.md` → Project basics, differentiators
   - `02-problem-{project-slug}-v*-*.md` → Problem context (Standard only)
   - `03-users-{project-slug}-v*-*.md` → Personas, representative quote
   - `04-journeys-{project-slug}-v*-*.md` → User journeys (Standard only)
   - `05-requirements-{project-slug}-v*-*.md` → Epics/Features/Stories
   - `06-scope-{project-slug}-v*-*.md` → MVP, Post-MVP, Future, Out of scope
   - `07-success-{project-slug}-v*-*.md` → Success metrics, Dependencies, Risks (Standard only)
   - `08-rules-{project-slug}-v*-*.md` → Rules & constraints (Standard only)
   - `{project-slug}-research-*.md` → Research findings (if any)

2. **Merge data into PRD template** (`resources/prd-template.md`)

3. **Save final PRD**: `docs/requirements/PRD-{ProjectName}-v{N}-{YYYYMMDD}.md`

4. **Output summary to chat**

---

## Output Summary Format

```
## PRD Generation Complete!

### Summary
- **Project**: [Name]
- **Mode**: [Simple/Standard]
- **Complexity**: [Simple/Medium/Complex]
- **Epics**: X
- **Features**: Y
- **User Stories**: Z
- **MVP Scope**: [Key features]

### Source Files Used (from docs/requirements/temp/)
✅ 01-welcome-{project-slug}-v1-{date}.md
✅ 02-problem-{project-slug}-v1-{date}.md (Standard only)
✅ 03-users-{project-slug}-v1-{date}.md
✅ 04-journeys-{project-slug}-v1-{date}.md (Standard only)
✅ 05-requirements-{project-slug}-v1-{date}.md
✅ 06-scope-{project-slug}-v1-{date}.md
✅ 07-success-{project-slug}-v1-{date}.md (Standard only)
✅ 08-rules-{project-slug}-v1-{date}.md (Standard only)
📚 {project-slug}-research-*.md (if any)

### Final PRD Saved To
`docs/requirements/PRD-{ProjectName}-v1-{Date}.md`

Would you like to:
- [V] View full document
- [E] Edit specific sections
- [R] Run additional research
```

---

## Simple Mode Summary

Simple Mode에서는 소스 파일이 적음:

```
### Source Files Used (Simple Mode, from docs/requirements/temp/)
✅ 01-welcome-{project-slug}-v1-{date}.md (includes Problem)
✅ 03-users-{project-slug}-v1-{date}.md
✅ 05-requirements-{project-slug}-v1-{date}.md
✅ 06-scope-{project-slug}-v1-{date}.md (includes Rules & Risks)
```

---

## Final PRD Structure

See `resources/prd-template.md` for the complete template.

### Key Sections
1. Executive Summary
2. Target Users (Personas)
3. User Journeys
4. Product Requirements (Epics/Features/Stories)
5. Success Metrics
6. Product Scope (MVP/Post-MVP/Future/Out of Scope)
7. Rules & Boundaries
8. Constraints & Assumptions
9. Change History
10. Appendix (Glossary, Research, Competitors)

---

## Version Management

**File naming:**
- New PRD: `PRD-[ProjectName]-v1-[YYYYMMDD].md`
- Revision: `PRD-[ProjectName]-v2-[YYYYMMDD].md`

**Track changes:**
- Add "Change History" section in PRD
- Note version, date, and changes

---

## Post-Generation Options

### [V] View Full Document
- Display the entire PRD in chat (may be truncated if long)
- Alternative: Provide file path for user to open

### [E] Edit Specific Sections
```
Which section would you like to edit?
1. Executive Summary
2. Personas
3. Requirements
4. Scope
5. Success Metrics
6. Rules
```

### [R] Run Additional Research
```
What would you like to research?
1. Competitor analysis
2. Market trends
3. User research
4. Custom search
```

---

## Completion Criteria

1. All source files read and validated
2. Data merged into PRD template
3. PRD document generated with all sections
4. File saved to `docs/requirements/PRD-{ProjectName}-v1-{DATE}.md`
5. Summary displayed in chat
6. Post-generation options presented

---

## End of Workflow

PRD generation marks the completion of the PRD Creator skill workflow.

The user can:
- Start a new PRD for a different project
- Edit the generated PRD
- Use the PRD as input for technical architecture planning (separate process)
