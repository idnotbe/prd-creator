# Step 6: Scope Definition

## Purpose
제품 범위를 정의하고 MVP, Post-MVP, Out of Scope를 명확히 합니다.

---

## Standard Mode Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q6.1 | What's absolutely required for MVP? (P0) | MVP에 절대 필요한 것은? | Must-have |
| Q6.2 | What can wait until v2? (P1) | v2까지 기다릴 수 있는 것은? | Post-MVP |
| Q6.3 | What features for future versions? (P2+) | 미래 버전에서 원하는 기능은? | Future |
| Q6.4 | What will you definitely NOT include? | 절대 포함하지 않을 것은? | Out of scope |

---

## Simple Mode Questions

Simple Mode에서는 Step 6, 7, 8이 통합됩니다.

| ID | Question | Purpose |
|----|----------|---------|
| Q6.1 | MVP 필수 기능은? (P0) | Must-have |
| Q6.2 | 나중에 추가할 기능은? (P1+) | Post-MVP + Future |
| Q6.3 | 제품이 절대 하면 안 되는 것은? | Out of scope + Rules |
| Q6.4 | 주요 위험 요소는? | Risks (from Step 7) |

---

## Execution Flow

```
Let's define the product scope:

1. MVP Must-Haves: What's absolutely required for launch? (P0)
2. Post-MVP Nice-to-Haves: What can wait until v2? (P1)
3. Future Considerations: What features would you like in future versions? (P2+)
4. Out of Scope: What will you definitely NOT include?
```

---

## Output Template

**Filename**: `06-scope-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 6
step_name: "Scope Definition"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 6: Scope Definition

## MVP Must-Haves (P0)
These features are **required** for launch. Product fails without them.

{{#each mvp_features}}
- [ ] **{{name}}**: {{description}}
{{/each}}

## Post-MVP Nice-to-Haves (P1)
Important features that can wait for v2.

{{#each post_mvp_features}}
- [ ] **{{name}}**: {{description}}
  - *Reason to defer*: {{defer_reason}}
{{/each}}

## Future Considerations (P2+)
Features for future versions.

{{#each future_features}}
- **{{name}}**: {{description}}
{{/each}}

## Out of Scope
These will **NOT** be included.

{{#each out_of_scope}}
- **{{name}}**: {{reason}}
{{/each}}
```

---

## Simple Mode Extended Template

Simple Mode에서는 Step 7, 8 내용도 포함:

```yaml
---
step: 6
step_name: "Scope & Rules (Simple Mode)"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
mode: "simple"
---

# Step 6: Scope & Rules (Simple Mode)

## MVP Must-Haves (P0)
{{mvp_features}}

## Post-MVP & Future (P1+)
{{post_mvp_and_future}}

## Out of Scope & Rules
### Things to Avoid
{{things_to_avoid}}

### Constraints
{{constraints}}

## Key Risks
| Risk | Mitigation |
|------|------------|
{{#each risks}}
| {{description}} | {{mitigation}} |
{{/each}}
```

---

## Completion Criteria

1. MVP features clearly identified (P0)
2. Post-MVP features listed with defer reasons
3. Out of scope items defined
4. File saved to `docs/requirements/temp/06-scope-{project-slug}-v1-{DATE}.md`
5. Output: `✅ Step 6 saved → 06-scope-v1-{DATE}.md`
6. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 7 (Success & Risks)
- **Simple Mode**: Step 9 (Generate PRD)
