# Step 8: Rules & Constraints

## Purpose
제품 규칙, 경계, 제약 조건을 정의합니다.

> **Note**: Simple Mode에서는 이 단계가 Step 6에 통합됩니다.

---

## Standard Mode Questions

### Core Rules
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q8.1 | What rules must the product always follow? | 제품이 반드시 따라야 하는 규칙은? | Must-have rules |
| Q8.2 | What should the product never do? | 제품이 절대 하면 안 되는 것은? | Things to avoid |
| Q8.3 | Any legal, ethical, or policy constraints? | 법적/윤리적/정책적 제약이 있나요? | Compliance |
| Q8.4 | Any budget, timeline, or regulatory constraints? | 예산, 일정, 규제 제약이 있나요? | Constraints |

### Advanced Questions (Optional)
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q8.5 | What data must be kept private? | 어떤 데이터를 비공개로 유지해야 하나요? | Privacy rules |
| Q8.6 | Are there age or geographic restrictions? | 연령 또는 지역 제한이 있나요? | Access rules |
| Q8.7 | What actions require explicit user consent? | 어떤 행동에 명시적 동의가 필요한가요? | Consent rules |

---

## Execution Flow

```
Let's establish the rules and constraints:

1. What rules must the product always follow? (Must-have rules)
2. What should the product never do? (Things to avoid)
3. Any legal, ethical, or policy constraints? (Compliance)
4. Any budget, timeline, or regulatory constraints? (Constraints)
```

---

## Output Template

**Filename**: `08-rules-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 8
step_name: "Rules & Constraints"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 8: Rules & Constraints

## Must-Have Rules
Critical rules the product must always follow.

| Rule | Reason |
|------|--------|
{{#each must_have_rules}}
| {{rule}} | {{reason}} |
{{/each}}

## Things to Avoid
What the product should never do.

| Avoid | Reason |
|-------|--------|
{{#each things_to_avoid}}
| {{item}} | {{reason}} |
{{/each}}

## Compliance & Legal
{{#each compliance}}
- **{{type}}**: {{description}}
{{/each}}

## Constraints
| Type | Constraint | Impact |
|------|------------|--------|
{{#each constraints}}
| {{type}} | {{description}} | {{impact}} |
{{/each}}
```

---

## Common Constraint Types

| Type | Examples |
|------|----------|
| **Budget** | Development budget limit, Infrastructure costs |
| **Timeline** | Launch deadline, Sprint cycles |
| **Regulatory** | GDPR, HIPAA, PCI-DSS |
| **Legal** | Terms of service, Privacy policy |
| **Ethical** | Data usage, User consent |
| **Technical** | Browser support, Device compatibility |

---

## Completion Criteria

1. Must-have rules documented
2. Things to avoid listed
3. Compliance requirements identified (if any)
4. Constraints documented
5. File saved to `docs/requirements/temp/08-rules-{project-slug}-v1-{DATE}.md`
6. Output: `✅ Step 8 saved → 08-rules-v1-{DATE}.md`
7. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 9 (Generate PRD)
