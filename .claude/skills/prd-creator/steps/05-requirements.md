# Step 5: Requirements Elicitation

## Purpose
Epic/Feature/User Story 구조로 핵심 요구사항을 추출합니다.

---

## Standard Mode Questions

### Epic Extraction
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.1 | What are the BIG goals users achieve? | 사용자가 달성하는 큰 목표는? | Epic identification |
| Q5.2 | What themes emerge from grouping features? | 기능 그룹화 시 어떤 테마가 나오나요? | Epic grouping |
| Q5.3 | What business objective does each goal support? | 각 목표가 지원하는 비즈니스 목표는? | Business alignment |

### Feature Extraction
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.4 | For [Epic], what capabilities are needed? | [Epic]을 위해 어떤 기능이 필요한가요? | Feature identification |
| Q5.5 | What can users DO with this feature? | 이 기능으로 사용자가 무엇을 할 수 있나요? | Feature definition |
| Q5.6 | What value does this feature provide? | 이 기능이 제공하는 가치는? | User value |
| Q5.7 | How would you know this feature works well? | 잘 작동한다는 것을 어떻게 알 수 있나요? | Success criteria |

### User Story Extraction
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.8 | Who specifically uses this feature? | 이 기능을 구체적으로 누가 사용하나요? | Actor |
| Q5.9 | What action do they want to take? | 어떤 행동을 하고 싶어하나요? | Action |
| Q5.10 | Why do they want to do this? | 왜 이것을 하고 싶어하나요? | Benefit |
| Q5.11 | What must be true for this to be "done"? | "완료"되려면 무엇이 참이어야 하나요? | Acceptance criteria |

### Background & Alternatives
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.12 | Are there other ways to solve this? | 다른 해결 방법이 있나요? | Alternatives |
| Q5.13 | Why this approach over others? | 왜 다른 방법 대신 이 방법인가요? | Rationale |
| Q5.14 | What options did you consider and reject? | 검토 후 제외한 방법은? | Rejected options |
| Q5.15 | What's the background for this requirement? | 이 요구사항의 배경은? | Background |

### Edge Cases & Exceptions
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.16 | What happens if the user does X incorrectly? | 사용자가 X를 잘못하면? | Error handling |
| Q5.17 | What are the boundary conditions? | 경계 조건은? | Edge cases |
| Q5.18 | How should the system behave unexpectedly? | 예상치 못한 상황에서 동작은? | Exceptional behavior |

### Non-Functional Requirements (User Perspective)
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.19 | How fast should it respond? | 얼마나 빨리 응답해야 하나요? | Performance |
| Q5.20 | What data needs protection? | 어떤 데이터가 보호되어야 하나요? | Security |
| Q5.21 | Any accessibility requirements? | 접근성 요구사항이 있나요? | Accessibility |
| Q5.22 | How many users should it support? | 몇 명의 사용자를 지원해야 하나요? | Scalability |

---

## Simple Mode Questions

| ID | Question | Purpose |
|----|----------|---------|
| Q5.1 | 사용자가 달성할 수 있는 주요 목표는? (Epics) | Epic identification |
| Q5.2 | 각 목표를 위해 필요한 기능은? (Features) | Feature extraction |
| Q5.3 | 각 기능의 성공 기준은? | Success criteria |
| Q5.4 | 필수 기능 vs 있으면 좋은 기능? | Priority |

---

## Execution Flow

```
Now let's define the requirements:

**Epics (Big Goals):**
1. What are the BIG goals users can achieve with your product?

**Features (Capabilities):**
2. For each goal, what capabilities/features are needed?

**User Stories (Detailed Requirements):**
3. For each feature, what specific actions can users take?
   Format: "As a [user], I want to [action] so that [benefit]"

**Success Criteria:**
4. For each feature, what defines success?
```

---

## Output Template

**Filename**: `05-requirements-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 5
step_name: "Requirements Elicitation"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
epic_count: {{epic_count}}
feature_count: {{feature_count}}
story_count: {{story_count}}
---

# Step 5: Requirements Elicitation

## Requirements Summary
- **Epics**: {{epic_count}}
- **Features**: {{feature_count}}
- **User Stories**: {{story_count}}

---

{{#each epics}}
## Epic {{@index}}: {{name}}
> {{description}}

**Business Goal**: {{business_goal}}
**Background**: {{background}}

{{#each features}}
### Feature {{../../../@index}}.{{@index}}: {{name}}
- **Description**: {{description}}
- **User Value**: {{user_value}}
- **Alternatives Considered**: {{alternatives}}
- **Why This Approach**: {{rationale}}
- **Success Criteria**: {{success_criteria}}

#### User Stories
| ID | Story | Acceptance Criteria | Priority |
|----|-------|---------------------|----------|
{{#each stories}}
| {{id}} | As a {{actor}}, I want to {{action}} so that {{benefit}} | {{acceptance_criteria}} | {{priority}} |
{{/each}}

{{/each}}
---
{{/each}}

## Edge Cases & Exceptions
| Scenario | Expected Behavior |
|----------|-------------------|
{{#each edge_cases}}
| {{scenario}} | {{behavior}} |
{{/each}}

## Non-Functional Requirements (NFRs)
| Category | Requirement | Target |
|----------|-------------|--------|
{{#each nfrs}}
| {{category}} | {{requirement}} | {{target}} |
{{/each}}
```

---

## Priority Definitions

| Priority | Definition |
|----------|------------|
| P0 | Must-have for MVP. Product fails without it. |
| P1 | Should-have. Important but product works without it. |
| P2 | Nice-to-have. Enhances but not essential. |
| P3 | Future consideration. Not for this release. |

---

## Completion Criteria

1. At least 1 Epic identified
2. Features mapped to Epics
3. User Stories in "As a... I want... so that..." format
4. Acceptance criteria defined for P0 stories
5. File saved to `docs/requirements/temp/05-requirements-{project-slug}-v1-{DATE}.md`
6. Output: `✅ Step 5 saved → 05-requirements-v1-{DATE}.md`
7. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 6 (Scope Definition)
- **Simple Mode**: Step 6 (Scope & Rules - 통합)
