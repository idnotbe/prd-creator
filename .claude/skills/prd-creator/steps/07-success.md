# Step 7: Success & Risks

## Purpose
성공 지표를 정의하고 의존성, 위험, 가정을 파악합니다.

> **Note**: Simple Mode에서는 이 단계가 Step 6에 통합됩니다.

---

## Standard Mode Questions

### Success Metrics
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q7.1 | How will you measure user success? | 사용자 성공을 어떻게 측정할 건가요? | User Metrics |
| Q7.2 | How will you measure business success? | 비즈니스 성공을 어떻게 측정할 건가요? | Business Metrics |
| Q7.3 | What key results are you aiming for? (OKRs) | 목표하는 핵심 결과는? | OKRs |

### Dependencies
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q7.4 | What other systems/teams does this depend on? | 의존하는 시스템/팀은? | Dependencies |
| Q7.5 | What must be completed before this can start? | 먼저 완료되어야 하는 것은? | Prerequisites |

### Risks & Assumptions
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q7.6 | What could go wrong? | 무엇이 잘못될 수 있나요? | Risks |
| Q7.7 | What's the mitigation plan for each risk? | 각 위험의 완화 계획은? | Mitigation |
| Q7.8 | What assumptions are you making? | 어떤 가정을 하고 있나요? | Assumptions |
| Q7.9 | How will you validate each assumption? | 가정을 어떻게 검증할 건가요? | Validation |

---

## Execution Flow

```
Let's define success and identify risks:

**Success Metrics:**
1. How will you measure user success? (User Metrics)
2. How will you measure business success? (Business Metrics)
3. What key results are you aiming for? (OKRs)

**Dependencies:**
4. What other systems/teams does this depend on?

**Risks & Assumptions:**
5. What could go wrong? (Risks)
6. What's the mitigation plan for each risk?
7. What assumptions are you making?
8. How will you validate each assumption?
```

---

## Output Template

**Filename**: `07-success-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 7
step_name: "Success & Risks"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 7: Success & Risks

## Success Metrics

### User Success Metrics
| Metric | Definition | Target | Measurement |
|--------|------------|--------|-------------|
{{#each user_metrics}}
| {{name}} | {{definition}} | {{target}} | {{measurement}} |
{{/each}}

### Business Success Metrics
| Metric | Definition | Target | Measurement |
|--------|------------|--------|-------------|
{{#each business_metrics}}
| {{name}} | {{definition}} | {{target}} | {{measurement}} |
{{/each}}

### Key Results (OKRs)
**Objective**: {{objective}}

| Key Result | Target | Measurement |
|------------|--------|-------------|
{{#each key_results}}
| {{description}} | {{target}} | {{measurement}} |
{{/each}}

## Dependencies
| Dependency | Type | Status | Impact if Delayed |
|------------|------|--------|-------------------|
{{#each dependencies}}
| {{name}} | {{type}} | {{status}} | {{impact}} |
{{/each}}

## Risks
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
{{#each risks}}
| {{description}} | {{probability}} | {{impact}} | {{mitigation}} |
{{/each}}

## Assumptions
| Assumption | Validation Method | If False... |
|------------|-------------------|-------------|
{{#each assumptions}}
| {{assumption}} | {{validation}} | {{consequence}} |
{{/each}}
```

---

## Success Metrics Categories

| Category | Examples |
|----------|----------|
| **User Success** | Task completion rate, Time to value, User satisfaction |
| **Business Success** | Signups, Active users, Retention, Revenue |
| **Product Success** | Feature adoption, NPS, Support tickets |

---

## Completion Criteria

1. User success metrics defined
2. Business success metrics defined
3. At least 1 OKR identified
4. Dependencies listed
5. Risks identified with mitigation plans
6. Assumptions documented
7. File saved to `docs/requirements/temp/07-success-{project-slug}-v1-{DATE}.md`
8. Output: `✅ Step 7 saved → 07-success-v1-{DATE}.md`
9. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 8 (Rules & Constraints)
