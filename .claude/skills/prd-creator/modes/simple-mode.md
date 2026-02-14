# Simple Mode

## Overview
Simple Mode는 소규모 프로젝트나 MVP를 빠르게 정의할 때 사용합니다.
단계를 병합하고 질문을 축소하여 효율적인 PRD 작성을 지원합니다.

---

## Activation Conditions

### Score-based (7-10 points)
| Signal | Points |
|--------|--------|
| Single user type | 1 |
| 3-5 features | 1 |
| No integrations | 1 |
| No compliance needs | 1 |

### Keyword-based
- "personal", "just me", "simple", "quick", "basic"
- "one thing", "single purpose"
- "MVP only", "prototype", "proof of concept"
- "no login", "offline"

### Explicit Request
- User says "Simple mode" or "빠르게 진행"
- User mentions tight timeline

---

## Step Mapping

### Merged Steps (5 total)

| Simple Step | Original Steps | Content |
|-------------|----------------|---------|
| 1 | 1+2 | Welcome & Problem |
| 2 | 3 | Users (간소화) |
| 3 | 5 | Requirements (핵심만) |
| 4 | 6+7+8 | Scope & Rules |
| 5 | 9 | Generate |

### Skipped Steps
- **Step 4 (Journey Mapping)**: 생략

---

## Simplified Questions per Step

### Step 1: Welcome & Problem (통합)
```
Let's quickly define your product:

1. Product name?
2. 30-second description (elevator pitch)?
3. What problem does it solve, and what's wrong with current solutions?
4. Core value and key differentiators?
```

**Questions**: 4 (vs Standard: 7+7=14)

### Step 2: Users (간소화)
```
Who is your user?

1. Primary user (role, situation)?
2. Top 3 goals and frustrations?
3. A typical quote about their frustration?
```

**Questions**: 3 (vs Standard: 11)

### Step 3: Requirements (핵심만)
```
What can users do?

1. Main goals users can achieve (Epics)?
2. Features needed for each goal?
3. Success criteria for each feature?
4. Must-have vs nice-to-have?
```

**Questions**: 4 (vs Standard: 22)

### Step 4: Scope & Rules (통합)
```
Let's finalize scope:

1. MVP must-haves (P0)?
2. Features for later (P1+)?
3. What should the product NEVER do?
4. Any major risks?
```

**Questions**: 4 (vs Standard: 4+9+7=20)

### Step 5: Generate
- Same as Standard Mode

---

## A/P/R/C Menu (Simplified)

```
---
Step [X] complete!

[C] Continue (default) | [A] Advanced | [P] Previous | [R] Research

Your choice (Enter for Continue):
```

- **Default action**: Continue (no input needed)
- **Other options available but not emphasized**

---

## Output Files

| Step | Filename |
|------|----------|
| 1 | `01-welcome-v{N}-{YYYYMMDD}.md` (includes Problem) |
| 2 | `03-users-v{N}-{YYYYMMDD}.md` |
| 3 | `05-requirements-v{N}-{YYYYMMDD}.md` |
| 4 | `06-scope-v{N}-{YYYYMMDD}.md` (includes Rules & Risks) |
| 5 | `PRD-{ProjectName}-v{N}-{YYYYMMDD}.md` |

**Note**: Files `02-problem`, `04-journeys`, `07-success`, `08-rules` are NOT created in Simple Mode.

---

## PRD Template Adjustments

### Simplified Sections
- 1 persona (brief)
- No user journey section
- 1-2 epics, 3-5 features
- 8-15 user stories
- Basic success metrics (merged into Scope)
- Compact document

### Omitted Sections
- Detailed journey mapping
- Comprehensive OKRs
- Detailed assumptions validation

---

## Time Estimate

| Mode | Estimated Time |
|------|----------------|
| Simple | 15-30 minutes |
| Standard | 45-90 minutes |

---

## When to Upgrade to Standard

If during Simple Mode any of these emerge:
- Multiple distinct user types discovered
- Complex integrations mentioned
- Compliance/regulations needed
- User requests deeper analysis

Prompt:
```
I noticed this project might need more detailed analysis.
Would you like to switch to Standard Mode for deeper exploration?

[Y] Yes, switch to Standard Mode
[N] No, continue with Simple Mode
```
