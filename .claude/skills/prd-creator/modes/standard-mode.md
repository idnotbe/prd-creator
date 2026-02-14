# Standard Mode

## Overview
Standard Mode는 중간~복잡한 프로젝트에서 포괄적인 PRD를 작성할 때 사용합니다.
전체 9단계를 거치며 깊이 있는 요구사항 분석을 수행합니다.

---

## Activation Conditions

### Score-based (11+ points)
| Signal | Points |
|--------|--------|
| 2+ user types | 2 |
| 6+ features | 2 |
| External integrations | 2 |
| Compliance needs | 3 |
| Team/collaboration | 2 |
| Dashboard/reports | 2 |

### Keyword-based
- "team", "collaboration", "dashboard"
- "admin", "settings", "notifications"
- "integrations", "API"
- "enterprise", "marketplace", "platform"
- "roles", "permissions", "multi-tenant"

---

## Full Workflow (9 Steps)

| Step | Name | Questions | File |
|------|------|-----------|------|
| 1 | Welcome & Big Picture | 5-7 | `01-welcome-v{N}.md` |
| 2 | Problem Discovery | 3-7 | `02-problem-v{N}.md` |
| 3 | User Discovery | 6-11 | `03-users-v{N}.md` |
| 4 | Journey Mapping | 6 | `04-journeys-v{N}.md` |
| 5 | Requirements Elicitation | 11-22 | `05-requirements-v{N}.md` |
| 6 | Scope Definition | 4 | `06-scope-v{N}.md` |
| 7 | Success & Risks | 9 | `07-success-v{N}.md` |
| 8 | Rules & Constraints | 4-7 | `08-rules-v{N}.md` |
| 9 | Generate PRD | - | `PRD-{Name}-v{N}.md` |

---

## A/P/R/C Menu (Full)

After each step:

```
---
Step [X] complete!

[A] Advanced - Explore deeper with more questions
[P] Previous - Revise previous answers
[R] Research - Web search (competitors, market trends)
[C] Continue - Proceed to next step

Your choice:
```

### [A] Advanced Option
Triggers additional probing questions:
- Edge cases and exceptions
- Permissions per action
- Workflow states
- Integration points
- Error scenarios

### [P] Previous Option
- Show summary of previous step
- Allow editing specific answers
- Create new version (v1 → v2)

### [R] Research Option
```
What would you like to research?
1. Competitor analysis - Find similar products
2. Market trends - Industry insights
3. User research - Similar user problems
4. Custom search - Specify your query
```

---

## Question Framework

Each step has:
- **Core Questions**: Always asked
- **Advanced Questions**: Available via [A] option
- **Simple Mode Equivalent**: Condensed version

See `resources/question-framework.md` for the complete question bank.

---

## Output Structure

### Intermediate Files (8)
All saved to `docs/requirements/temp/` with project-slug in filename

### Final PRD
Full document with all sections:
1. Executive Summary
2. Target Users (2+ personas)
3. User Journeys (2-3 scenarios)
4. Product Requirements (Epics/Features/Stories)
5. Success Metrics (User + Business + OKRs)
6. Product Scope (MVP + Post-MVP + Future + Out of Scope)
7. Rules & Boundaries
8. Constraints & Assumptions (Dependencies, Risks, Assumptions)
9. Change History
10. Appendix (Glossary, Research, Competitors)

---

## Complexity Sub-levels

### Medium (11-16 points)
- 2-3 user types
- 6-12 features
- 20-40 user stories
- Standard question depth

### Complex (17+ points)
- 4+ user types or complex roles
- 13-30 features
- 50+ user stories
- Extended question sets with probing
- Risk assessment
- Detailed document with appendices

---

## Time Estimate

| Complexity | Estimated Time |
|------------|----------------|
| Medium | 45-60 minutes |
| Complex | 60-90+ minutes |

---

## When to Downgrade to Simple

If during Standard Mode:
- User mentions "MVP only" or "just the basics"
- Solo developer building for personal use
- Proof of concept or prototype
- Very tight timeline mentioned

Prompt:
```
This seems like a simpler project than initially thought.
Would you like to switch to Simple Mode for faster completion?

[Y] Yes, switch to Simple Mode
[N] No, continue with Standard Mode
```
