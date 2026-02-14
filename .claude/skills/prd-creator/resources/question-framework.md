# Question Framework for PRD Creation

## Overview

이 문서는 PRD 작성을 위한 질문 은행입니다. 질문은 단계별, 복잡도별로 구성되어 있습니다.

### Question ID Format
`Q{Step}.{Number}` - 예: Q1.1, Q2.3, Q5.15

---

## Step 1: Welcome & Big Picture

### Core Questions (All Modes)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q1.1 | What's the name of your product/project? | 제품/프로젝트의 이름은 무엇인가요? | Identification |
| Q1.2 | In 30 seconds, how would you describe it? | 30초 안에 설명한다면 어떻게 말씀하시겠어요? | Elevator pitch |
| Q1.3 | What problem does it solve? | 어떤 문제를 해결하나요? | Problem statement |
| Q1.4 | Why does this need to exist? | 왜 이 제품이 존재해야 하나요? | Value proposition |
| Q1.5 | What makes this different from existing solutions? | 기존 솔루션과 무엇이 다른가요? | Key Differentiators |

### Advanced Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q1.6 | What inspired this idea? | 이 아이디어는 어디서 영감을 받았나요? | Origin story |
| Q1.7 | What's your vision for 3 years from now? | 3년 후 비전은 무엇인가요? | Long-term vision |

---

## Step 2: Problem Discovery

> **Note**: Simple Mode에서는 Step 1에 통합됨

### Core Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q2.1 | How do users currently solve this problem? | 현재 사용자들은 이 문제를 어떻게 해결하나요? | Current state |
| Q2.2 | What's the biggest frustration with existing solutions? | 기존 해결책의 가장 큰 문제점은? | Pain points |
| Q2.3 | Why is NOW the right time? | 왜 지금이 적기인가요? | Timing |

### Advanced Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q2.4 | What happens if this problem isn't solved? | 이 문제가 해결되지 않으면 어떻게 되나요? | Stakes |
| Q2.5 | Who else is trying to solve this? | 누가 이 문제를 해결하려고 하나요? | Competition |
| Q2.6 | What trends make this problem more urgent? | 어떤 트렌드가 이 문제를 더 급하게 만드나요? | Market forces |
| Q2.7 | What's the cost of the problem? (Time, money, frustration) | 이 문제의 비용은? (시간, 돈, 스트레스) | Problem magnitude |

---

## Step 3: User Discovery

### Core Questions (All Modes)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q3.1 | Who is your primary user? | 주요 사용자는 누구인가요? | Primary persona |
| Q3.2 | What's their role/job/situation? | 그들의 역할/직업/상황은? | Demographics |
| Q3.3 | What are their top 3 goals? | 상위 3가지 목표는? | User goals |
| Q3.4 | What are their top 3 frustrations? | 상위 3가지 불만은? | Pain points |
| Q3.5 | How tech-savvy are they? | 기술에 얼마나 익숙한가요? | Tech proficiency |
| Q3.6 | What's a typical thing they would say? | 불만에 대해 보통 뭐라고 말하나요? | Representative Quote |

### Advanced Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q3.7 | Are there secondary user groups? | 부가 사용자 그룹이 있나요? | Secondary personas |
| Q3.8 | What tools do they currently use? | 현재 어떤 도구를 사용하나요? | Current tools |
| Q3.9 | What would make them switch to your solution? | 무엇이 그들을 당신의 솔루션으로 전환하게 할까요? | Switching triggers |
| Q3.10 | Who influences their decisions? | 누가 그들의 결정에 영향을 미치나요? | Decision makers |
| Q3.11 | What's their budget/willingness to pay? | 예산/지불 의향은? | Budget |

### Persona Template

```markdown
## Persona: [Name]

### Demographics
- **Role**: [Job title/situation]
- **Age Range**: [e.g., 25-35]
- **Tech Level**: [Beginner/Intermediate/Advanced]
- **Context**: [Where/when they encounter the problem]

### Goals
1. [Primary goal]
2. [Secondary goal]
3. [Tertiary goal]

### Pain Points
1. [Major frustration]
2. [Secondary frustration]
3. [Minor annoyance]

### Current Behavior
- **Current Solution**: [How they solve it now]
- **Workarounds**: [Hacks they use]
- **Time Spent**: [Time on problem weekly]

### Quotes (Representative)
> "[Typical thing they would say about the problem]"
```

---

## Step 4: Journey Mapping

> **Note**: Simple Mode에서는 생략됨

### Core Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q4.1 | Describe a typical day when the problem occurs | 문제가 발생하는 전형적인 하루를 설명해주세요 | Context |
| Q4.2 | What triggers the need for a solution? | 해결책이 필요한 순간의 트리거는? | Trigger |
| Q4.3 | How would they discover your product? | 어떻게 제품을 발견할까요? | Discovery |
| Q4.4 | What's their first action in the product? | 제품에서 첫 번째 행동은? | First use |
| Q4.5 | What's the "aha!" moment? | "아하!" 순간은 언제인가요? | Value realization |
| Q4.6 | What brings them back? | 무엇이 그들을 다시 오게 하나요? | Retention |

### Journey Template

```markdown
## Journey: [Persona] - [Scenario Name]

### Opening Scene (Problem Context)
[Narrative description]
- **Where**: [Location/context]
- **When**: [Time/situation]
- **Emotion**: [How they feel]

### Discovery
- **Channel**: [How they hear about it]
- **Hook**: [What catches attention]
- **Decision**: [Why they try it]

### First Use
- **First Action**: [What they do first]
- **Learning Curve**: [How easy to understand]
- **Quick Win**: [Immediate value]

### Core Loop
- **Trigger**: [What brings them back]
- **Action**: [What they do]
- **Reward**: [What they get]

### Success Moment
- **Aha Moment**: [When they "get it"]
- **Outcome**: [Result achieved]
- **Emotion**: [How they feel]
```

---

## Step 5: Requirements Elicitation

### Epic Extraction Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.1 | What are the BIG goals users achieve with your product? | 사용자가 제품으로 달성하는 큰 목표는? | Epic identification |
| Q5.2 | Group related features - what themes emerge? | 관련 기능을 그룹화하면 어떤 테마가 나오나요? | Epic grouping |
| Q5.3 | What business objective does each goal support? | 각 목표가 지원하는 비즈니스 목표는? | Business alignment |

### Feature Extraction Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.4 | For [Epic], what capabilities are needed? | [Epic]을 위해 어떤 기능이 필요한가요? | Feature identification |
| Q5.5 | What can users DO with this feature? | 이 기능으로 사용자가 무엇을 할 수 있나요? | Feature definition |
| Q5.6 | What value does this feature provide? | 이 기능이 제공하는 가치는? | User value |
| Q5.7 | How would you know this feature works well? | 이 기능이 잘 작동한다는 것을 어떻게 알 수 있나요? | Success criteria |

### User Story Extraction Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.8 | Who specifically uses this feature? | 이 기능을 구체적으로 누가 사용하나요? | Actor |
| Q5.9 | What action do they want to take? | 어떤 행동을 하고 싶어하나요? | Action |
| Q5.10 | Why do they want to do this? | 왜 이것을 하고 싶어하나요? | Benefit |
| Q5.11 | What must be true for this to be "done"? | "완료"되려면 무엇이 참이어야 하나요? | Acceptance criteria |

### Background & Alternatives Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.12 | Are there other ways to solve this problem? | 이 문제를 해결하는 다른 방법이 있나요? | Alternatives |
| Q5.13 | Why this approach over others? | 왜 다른 방법 대신 이 방법인가요? | Rationale |
| Q5.14 | What options did you consider and reject? | 검토 후 제외한 방법은? | Rejected options |
| Q5.15 | What's the background for this requirement? | 이 요구사항의 배경은 무엇인가요? | Background |

### Edge Cases & Exceptions Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.16 | What happens if the user does X incorrectly? | 사용자가 X를 잘못하면 어떻게 되나요? | Error handling |
| Q5.17 | What are the boundary conditions? | 경계 조건은 무엇인가요? | Edge cases |
| Q5.18 | How should the system behave unexpectedly? | 예상치 못한 상황에서 시스템은 어떻게 동작해야 하나요? | Exceptional behavior |

### Non-Functional Requirements Questions (User Perspective)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q5.19 | How fast should it respond? | 얼마나 빨리 응답해야 하나요? | Performance |
| Q5.20 | What data needs protection? | 어떤 데이터가 보호되어야 하나요? | Security |
| Q5.21 | Any accessibility requirements? | 접근성 요구사항이 있나요? | Accessibility |
| Q5.22 | How many users should it support? | 몇 명의 사용자를 지원해야 하나요? | Scalability |

### Priority Definitions

| Priority | Definition (EN) | Definition (KO) |
|----------|-----------------|-----------------|
| P0 | Must-have for MVP. Product fails without it. | MVP 필수. 없으면 제품 실패 |
| P1 | Should-have. Important but product works without it. | 중요하지만 없어도 작동 |
| P2 | Nice-to-have. Enhances but not essential. | 있으면 좋음. 필수 아님 |
| P3 | Future consideration. Not for this release. | 향후 고려. 이번 릴리스 아님 |

---

## Step 6: Scope Definition

### Core Questions (All Modes)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q6.1 | What's absolutely required for MVP? (P0) | MVP에 절대 필요한 것은? | Must-have |
| Q6.2 | What can wait until v2? (P1) | v2까지 기다릴 수 있는 것은? | Post-MVP |
| Q6.3 | What features for future versions? (P2+) | 미래 버전에서 원하는 기능은? | Future |
| Q6.4 | What will you definitely NOT include? | 절대 포함하지 않을 것은? | Out of scope |

---

## Step 7: Success & Risks

> **Note**: Simple Mode에서는 Step 6에 통합됨

### Success Metrics Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q7.1 | How will you measure user success? | 사용자 성공을 어떻게 측정할 건가요? | User Metrics |
| Q7.2 | How will you measure business success? | 비즈니스 성공을 어떻게 측정할 건가요? | Business Metrics |
| Q7.3 | What key results are you aiming for? (OKRs) | 목표하는 핵심 결과는? | OKRs |

### Dependencies Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q7.4 | What other systems/teams does this depend on? | 이것이 의존하는 시스템/팀은? | Dependencies |
| Q7.5 | What must be completed before this can start? | 무엇이 먼저 완료되어야 하나요? | Prerequisites |

### Risks & Assumptions Questions

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q7.6 | What could go wrong? | 무엇이 잘못될 수 있나요? | Risks |
| Q7.7 | What's the mitigation plan for each risk? | 각 위험의 완화 계획은? | Mitigation |
| Q7.8 | What assumptions are you making? | 어떤 가정을 하고 있나요? | Assumptions |
| Q7.9 | How will you validate each assumption? | 가정을 어떻게 검증할 건가요? | Validation |

### Success Metrics Categories

| Category | Examples (EN) | Examples (KO) |
|----------|---------------|---------------|
| **User Success** | Task completion rate, Time to value, User satisfaction | 작업 완료율, 가치 도달 시간, 사용자 만족도 |
| **Business Success** | Signups, Active users, Retention, Revenue | 가입, 활성 사용자, 리텐션, 매출 |
| **Product Success** | Feature adoption, NPS, Support tickets | 기능 채택률, NPS, 지원 티켓 |

---

## Step 8: Rules & Constraints

> **Note**: Simple Mode에서는 Step 6에 통합됨

### Core Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q8.1 | What rules must the product always follow? | 제품이 반드시 따라야 하는 규칙은? | Must-have rules |
| Q8.2 | What should the product never do? | 제품이 절대 하면 안 되는 것은? | Things to avoid |
| Q8.3 | Any legal, ethical, or policy constraints? | 법적/윤리적/정책적 제약이 있나요? | Compliance |
| Q8.4 | Any budget, timeline, or regulatory constraints? | 예산, 일정, 규제 제약이 있나요? | Constraints |

### Advanced Questions (Standard Mode)

| ID | Question (EN) | Question (KO) | Purpose |
|----|---------------|---------------|---------|
| Q8.5 | What data must be kept private? | 어떤 데이터를 비공개로 유지해야 하나요? | Privacy rules |
| Q8.6 | Are there age or geographic restrictions? | 연령 또는 지역 제한이 있나요? | Access rules |
| Q8.7 | What actions require explicit user consent? | 어떤 행동에 명시적 사용자 동의가 필요한가요? | Consent rules |

---

## Research Questions (On-Demand)

### Competitor Analysis

| ID | Question (EN) | Question (KO) |
|----|---------------|---------------|
| R1 | Who are the main competitors? | 주요 경쟁자는 누구인가요? |
| R2 | What do they do well? | 그들이 잘하는 것은? |
| R3 | What do they do poorly? | 그들이 못하는 것은? |
| R4 | What's your unique advantage? | 당신만의 장점은? |
| R5 | What can you learn from them? | 그들에게서 배울 점은? |

### Market Research

| ID | Question (EN) | Question (KO) |
|----|---------------|---------------|
| R6 | What's the market size? | 시장 규모는? |
| R7 | What trends affect this space? | 이 분야에 영향을 주는 트렌드는? |
| R8 | Who are the industry leaders? | 업계 리더는 누구인가요? |
| R9 | What regulatory factors exist? | 규제 요소는? |

---

## Elicitation Techniques

### 1. The 5 Whys
문제의 근본 원인을 파악:
- "Why is this a problem?" → Answer
- "Why does that happen?" → Answer
- (5회 반복)

### 2. Day-in-the-Life
여정 매핑용:
- "Walk me through a typical day..."
- "What happens next?"
- "How did that make you feel?"

### 3. Worst/Best Case
이해관계 파악:
- "What's the worst that could happen?"
- "What would the ideal outcome look like?"

### 4. Prioritization Matrix
범위 결정용:
- "If you could only have 3 features, which?"
- "What would you cut if you had half the time?"

### 5. Success Painting
성공 기준용:
- "It's launch day and it's a huge success. What do you see?"
- "A user just said 'this is amazing!' - what did they just do?"

---

## Question Count Summary

| Step | Standard Mode | Simple Mode |
|------|---------------|-------------|
| 1 | 5-7 | 4 (includes Step 2) |
| 2 | 3-7 | - (merged) |
| 3 | 6-11 | 3 |
| 4 | 6 | - (skipped) |
| 5 | 11-22 | 4 |
| 6 | 4 | 4 (includes 7,8) |
| 7 | 9 | - (merged) |
| 8 | 4-7 | - (merged) |
| **Total** | **48-73** | **15** |
