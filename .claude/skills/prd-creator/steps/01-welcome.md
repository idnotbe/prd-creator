# Step 1: Welcome & Big Picture

## Purpose
프로젝트의 기본 정보와 핵심 가치를 수집합니다.

---

## Standard Mode Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q1.1 | What's the name of your product/project? | 제품/프로젝트의 이름은 무엇인가요? | Identification |
| Q1.2 | In 30 seconds, how would you describe it? | 30초 안에 설명한다면 어떻게 말씀하시겠어요? | Elevator pitch |
| Q1.3 | What problem does it solve? | 어떤 문제를 해결하나요? | Problem statement |
| Q1.4 | Why does this need to exist? | 왜 이 제품이 존재해야 하나요? | Value proposition |
| Q1.5 | What makes this different from existing solutions? | 기존 솔루션과 무엇이 다른가요? | Key Differentiators |

### Advanced Questions (Optional)
| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q1.6 | What inspired this idea? | 이 아이디어는 어디서 영감을 받았나요? | Origin story |
| Q1.7 | What's your vision for 3 years from now? | 3년 후 비전은 무엇인가요? | Long-term vision |

---

## Simple Mode Questions

Simple Mode에서는 Step 1과 Step 2가 통합됩니다.

| ID | Question | Purpose |
|----|----------|---------|
| Q1.1 | 제품 이름은? | Identification |
| Q1.2 | 30초 설명 (엘리베이터 피치) | Elevator pitch |
| Q1.3 | 어떤 문제를 해결하고, 기존 해결책의 문제점은? | Problem + Frustrations |
| Q1.4 | 핵심 가치와 차별점은? | Value + Differentiators |

---

## Execution Flow

### On First User Message
1. Detect language from user input
2. Greet in detected language
3. Ask initial questions:

```
Welcome! I'll help you create a detailed PRD for your product idea.

Let's start with the basics:
1. What's the name of your product/project?
2. In 30 seconds, how would you describe it to a friend? (Elevator pitch)
3. What specific problem does it solve?
4. Why does this product need to exist? (Core value)
5. What makes this different from existing solutions? (Key Differentiators)

Feel free to share any existing documents (research, briefs) if you have them.
```

### If User Provides Documents
- Read and analyze the content
- Extract key insights for PRD
- Reference findings in subsequent questions

---

## Output Template

**Filename**: `01-welcome-v{N}-{YYYYMMDD}.md`

```yaml
---
step: 1
step_name: "Welcome & Big Picture"
project_name: "{{project_name}}"
version: 1
created_at: "{{YYYY-MM-DD HH:mm}}"
status: "completed"
---

# Step 1: Welcome & Big Picture

## Project Name
{{project_name}}

## Elevator Pitch
{{elevator_pitch}}

## Problem Statement
{{problem_statement}}

## Value Proposition
{{value_proposition}}

## Key Differentiators
{{key_differentiators}}

## Documents Provided
{{documents_summary or "None"}}
```

---

## Completion Criteria

1. All required fields are collected:
   - Project name
   - Elevator pitch
   - Problem statement
   - Value proposition
   - Key differentiators
2. File saved to `docs/requirements/temp/01-welcome-{project-slug}-v1-{DATE}.md`
3. Output: `✅ Step 1 saved → 01-welcome-v1-{DATE}.md`
4. Show A/P/R/C menu (Standard) or simplified menu (Simple)

---

## Next Step
- **Standard Mode**: Step 2 (Problem Discovery)
- **Simple Mode**: Step 3 (User Discovery - 간소화)
