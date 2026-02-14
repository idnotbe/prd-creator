# Step 3: User Discovery

## Purpose
타겟 사용자를 이해하고, 상세한 페르소나를 구축합니다.

---

## Standard Mode Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q3.1 | Who is your primary user? | 주요 사용자는 누구인가요? | Primary persona |
| Q3.2 | What's their role/job/situation? | 그들의 역할/직업/상황은? | Demographics |
| Q3.3 | What are their top 3 goals? | 상위 3가지 목표는? | User goals |
| Q3.4 | What are their top 3 frustrations? | 상위 3가지 불만은? | Pain points |
| Q3.5 | How tech-savvy are they? | 기술에 얼마나 익숙한가요? | Tech proficiency |
| Q3.6 | What's a typical thing they would say? | 불만에 대해 보통 뭐라고 말하나요? | Representative Quote |

### Advanced Questions (Optional)
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q3.7 | Are there secondary user groups? | 부가 사용자 그룹이 있나요? | Secondary personas |
| Q3.8 | What tools do they currently use? | 현재 어떤 도구를 사용하나요? | Current tools |
| Q3.9 | What would make them switch? | 무엇이 전환하게 할까요? | Switching triggers |
| Q3.10 | Who influences their decisions? | 누가 결정에 영향을 미치나요? | Decision makers |
| Q3.11 | What's their budget/willingness to pay? | 예산/지불 의향은? | Budget |

---

## Simple Mode Questions

| ID | Question | Purpose |
|----|----------|---------|
| Q3.1 | 주요 사용자는 누구? (역할, 상황) | Primary persona |
| Q3.2 | 상위 3가지 목표와 불만은? | Goals + Pain points |
| Q3.3 | 대표적인 불만 표현은? (Quote) | Representative Quote |

---

## Execution Flow

```
Let's understand your users:

1. Who is your primary user? (Role, situation, characteristics)
2. What are their top 3 goals?
3. What are their top 3 frustrations/pain points?
4. What's a typical thing they would say about their frustration? (Quote)
5. How tech-savvy are they?
6. Are there secondary user groups? (If yes, describe briefly)
```

### Create Persona Summary
```markdown
## Primary Persona: [Name]
- **Who**: [Description]
- **Goals**: [1, 2, 3]
- **Pain Points**: [1, 2, 3]
- **Current Solution**: [How they solve it now]
```

---

## Output Template

**Filename**: `03-users-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 3
step_name: "User Discovery"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 3: User Discovery

## Primary Persona: {{persona_name}}

### Demographics
- **Role/Job**: {{persona_role}}
- **Context**: {{persona_context}}
- **Tech Proficiency**: {{persona_tech_level}}

### Goals
1. {{goal_1}}
2. {{goal_2}}
3. {{goal_3}}

### Pain Points
1. {{pain_1}}
2. {{pain_2}}
3. {{pain_3}}

### Representative Quote
> "{{representative_quote}}"

## Secondary Personas (if any)
{{secondary_personas or "None identified"}}
```

---

## Completion Criteria

1. All required fields are collected:
   - Primary persona (name, role, context)
   - Goals (at least 3)
   - Pain points (at least 3)
   - Representative quote
   - Tech proficiency
2. File saved to `docs/requirements/temp/03-users-{project-slug}-v1-{DATE}.md`
3. Output: `✅ Step 3 saved → 03-users-v1-{DATE}.md`
4. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 4 (Journey Mapping)
- **Simple Mode**: Step 5 (Requirements - 간소화)
