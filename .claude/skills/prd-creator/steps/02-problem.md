# Step 2: Problem Discovery

## Purpose
문제 공간을 탐색하고, 현재 해결책의 한계와 타이밍을 파악합니다.

> **Note**: Simple Mode에서는 이 단계가 Step 1에 통합됩니다.

---

## Standard Mode Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q2.1 | How do users currently solve this problem? | 현재 사용자들은 이 문제를 어떻게 해결하나요? | Current state |
| Q2.2 | What's the biggest frustration with existing solutions? | 기존 해결책의 가장 큰 문제점은? | Pain points |
| Q2.3 | Why is NOW the right time? | 왜 지금이 적기인가요? | Timing |

### Advanced Questions (Optional)
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q2.4 | What happens if this problem isn't solved? | 이 문제가 해결되지 않으면 어떻게 되나요? | Stakes |
| Q2.5 | Who else is trying to solve this? | 누가 이 문제를 해결하려고 하나요? | Competition |
| Q2.6 | What trends make this problem more urgent? | 어떤 트렌드가 이 문제를 더 급하게 만드나요? | Market forces |
| Q2.7 | What's the cost of the problem? (Time, money, frustration) | 이 문제의 비용은? (시간, 돈, 스트레스) | Problem magnitude |

---

## Execution Flow

```
Great foundation! Now let's dive deeper into the problem:

1. How do users currently solve this problem? (Current solutions)
2. What's the biggest frustration with existing solutions?
3. Why is NOW the right time for this product? (Timing/opportunity)
```

---

## Output Template

**Filename**: `02-problem-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 2
step_name: "Problem Discovery"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 2: Problem Discovery

## Current Solutions
{{current_solutions}}

## Biggest Frustrations
{{frustrations}}

## Why Now (Timing/Opportunity)
{{timing}}

## Additional Insights (if explored)
### Stakes if Unsolved
{{stakes}}

### Competitors
{{competitors}}

### Market Trends
{{trends}}

### Problem Cost
{{cost}}
```

---

## Completion Criteria

1. All required fields are collected:
   - Current solutions
   - Biggest frustrations
   - Timing/opportunity
2. File saved to `docs/requirements/temp/02-problem-{project-slug}-v1-{DATE}.md`
3. Output: `✅ Step 2 saved → 02-problem-v1-{DATE}.md`
4. Show A/P/R/C menu

---

## Next Step
- **Standard Mode**: Step 3 (User Discovery)
