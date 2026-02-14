# Step 4: Journey Mapping

## Purpose
사용자의 여정을 내러티브 형식으로 캡처하여 주요 시나리오를 이해합니다.

> **Note**: Simple Mode에서는 이 단계가 **생략**됩니다.

---

## Standard Mode Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q4.1 | Describe a typical day when the problem occurs | 문제가 발생하는 전형적인 하루를 설명해주세요 | Context |
| Q4.2 | What triggers the need for a solution? | 해결책이 필요한 순간의 트리거는? | Trigger |
| Q4.3 | How would they discover your product? | 어떻게 제품을 발견할까요? | Discovery |
| Q4.4 | What's their first action in the product? | 제품에서 첫 번째 행동은? | First use |
| Q4.5 | What's the "aha!" moment? | "아하!" 순간은 언제인가요? | Value realization |
| Q4.6 | What brings them back? | 무엇이 그들을 다시 오게 하나요? | Retention |

---

## Execution Flow

```
Let's tell [Persona Name]'s story:

Walk me through a day in their life:
1. The moment they encounter the problem
2. How they discover your product
3. Their first experience using it
4. The "aha!" moment when it works
5. How their life changes after
```

---

## Output Template

**Filename**: `04-journeys-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 4
step_name: "Journey Mapping"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 4: Journey Mapping

## Journey: {{persona_name}} - {{scenario_name}}

### Opening Scene (Problem Context)
{{journey_opening}}
- **Where**: {{where}}
- **When**: {{when}}
- **Emotion**: {{emotion_start}}

### Discovery
{{discovery}}
- **Channel**: {{discovery_channel}}
- **Hook**: {{discovery_hook}}
- **Decision Trigger**: {{decision_trigger}}

### First Use
{{first_use}}
- **First Action**: {{first_action}}
- **Learning Curve**: {{learning_curve}}
- **Quick Win**: {{quick_win}}

### Core Usage Loop
{{core_loop}}
- **Trigger**: {{loop_trigger}}
- **Action**: {{loop_action}}
- **Reward**: {{loop_reward}}

### Success Moment
{{success_moment}}
- **Aha Moment**: {{aha_moment}}
- **Outcome**: {{outcome}}
- **Emotion**: {{emotion_end}}

### Ongoing Value
{{ongoing_value}}
```

---

## Completion Criteria

1. All required sections are completed:
   - Opening scene (problem context)
   - Discovery
   - First use
   - Core usage loop
   - Success moment
   - Ongoing value
2. File saved to `docs/requirements/temp/04-journeys-{project-slug}-v1-{DATE}.md`
3. Output: `✅ Step 4 saved → 04-journeys-v1-{DATE}.md`
4. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 5 (Requirements Elicitation)
