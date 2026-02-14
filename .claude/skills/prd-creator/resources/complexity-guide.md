# Complexity Assessment Guide

## Overview

이 가이드는 프로젝트 복잡도를 평가하여 PRD 작성의 깊이와 모드를 결정합니다.

---

## Mode Selection

| Score | Mode | Description |
|-------|------|-------------|
| 7-10 | **Simple Mode** | 단계 병합, 질문 축소, 빠른 진행 |
| 11-16 | **Standard Mode (Medium)** | 전체 9단계, 표준 질문 |
| 17+ | **Standard Mode (Complex)** | 전체 9단계, 확장 질문, 상세 분석 |

> See `modes/simple-mode.md` and `modes/standard-mode.md` for detailed configurations.

---

## Complexity Levels

### Simple (Score: 7-10)

**Characteristics:**
- Single user type
- Single clear problem
- Standalone functionality
- Limited integrations
- Personal or small team use

**Indicators:**
| Signal | Example |
|--------|---------|
| "Just for me/my team" | Personal productivity tool |
| "One main thing" | Single-purpose app |
| "Simple and fast" | Quick utility |
| No mention of roles/permissions | Basic access |
| No external dependencies | Self-contained |

**PRD Approach (Simple Mode):**
- 5 merged steps (vs 9 standard)
- 15 questions (vs 48-73)
- 1 persona (brief)
- 1 user journey (optional)
- 1-2 epics, 3-5 features
- 8-15 user stories
- Basic success metrics
- Compact document

**Examples:**
- Personal to-do app
- Timer/stopwatch
- Note-taking tool
- Single-purpose calculator
- Personal habit tracker

---

### Medium (Score: 11-16)

**Characteristics:**
- 2-3 user types
- Related problem set
- Multiple connected features
- Some integrations
- Small business or team use

**Indicators:**
| Signal | Example |
|--------|---------|
| "Different types of users" | Admin vs regular user |
| "Multiple features" | 5-10 distinct capabilities |
| "Integrates with..." | External services |
| "Teams/collaboration" | Multi-user scenarios |
| "Dashboard/reports" | Data aggregation needs |

**PRD Approach (Standard Mode):**
- Full 9-step process
- 48-73 questions
- 1-2 detailed personas
- 2-3 user journeys
- 2-4 epics, 6-12 features
- 20-40 user stories
- Detailed success metrics
- Standard document

**Examples:**
- Team task management
- Small SaaS application
- E-commerce store (small)
- Content management system
- Customer feedback tool

---

### Complex (Score: 17+)

**Characteristics:**
- Multiple user types with distinct roles
- Complex business processes
- Extensive integrations
- Regulatory/compliance needs
- Enterprise or marketplace use

**Indicators:**
| Signal | Example |
|--------|---------|
| "Enterprise/marketplace" | B2B, multi-tenant |
| "Roles and permissions" | RBAC, complex access |
| "Compliance/regulations" | HIPAA, GDPR, PCI |
| "Multiple integrations" | Many external systems |
| "Workflow automation" | Multi-step processes |
| "Billing/subscriptions" | Complex monetization |
| "Analytics/reporting" | Advanced data needs |

**PRD Approach (Standard Mode + Extended):**
- Full 9-step process with probing
- Extended question sets
- 2-4 detailed personas
- 3-5 user journeys
- 4-8 epics, 13-30 features
- 50+ user stories
- Comprehensive metrics & OKRs
- Risk assessment
- Detailed document with appendices

**Examples:**
- Enterprise SaaS platform
- Marketplace (buyers + sellers)
- Healthcare application
- Financial services app
- Multi-tenant platform

---

## Scoring System

### Detection Questions

| Question | Simple (1pt) | Medium (2pt) | Complex (3pt) |
|----------|--------------|--------------|---------------|
| **User Types** | Single user type | 2-3 user types | 4+ user types or complex roles |
| **Problem Scope** | One clear problem | Related problems | Complex business process |
| **Feature Count** | 3-5 features | 6-12 features | 13+ features |
| **Integrations** | None or 1 | 2-4 integrations | 5+ integrations |
| **Compliance** | None | Basic (GDPR opt-in) | Regulated industry |
| **Monetization** | Free or simple | Basic paid tiers | Complex billing |
| **Data Needs** | Simple storage | Reports/dashboards | Analytics/ML |

### Score Interpretation

| Total Score | Complexity Level | Mode |
|-------------|------------------|------|
| 7-10 | Simple | Simple Mode |
| 11-16 | Medium | Standard Mode |
| 17+ | Complex | Standard Mode (Extended) |

---

## Automatic Detection Signals

### Keywords Indicating Simple Mode
- "personal", "just me", "simple", "quick", "basic"
- "one thing", "single purpose"
- "no login", "offline"
- "MVP only", "prototype", "proof of concept"
- "tight timeline", "just the basics"

### Keywords Indicating Standard Mode (Medium)
- "team", "collaboration", "dashboard"
- "admin", "settings", "notifications"
- "integrations", "API"

### Keywords Indicating Standard Mode (Complex)
- "enterprise", "marketplace", "platform"
- "roles", "permissions", "multi-tenant"
- "compliance", "audit", "security"
- "workflow", "automation", "rules engine"
- "billing", "subscriptions", "invoicing"

---

## Adjustment Rules

### Upgrading Complexity
If any of these are true, upgrade one level:
- User mentions compliance/regulations
- Multiple distinct user roles with different permissions
- Real-time collaboration features
- Payment processing
- Multi-tenant architecture

### Downgrading Complexity
If any of these are true, downgrade one level:
- "MVP only" or "just the basics"
- Solo developer building for personal use
- Proof of concept or prototype
- Very tight timeline mentioned

---

## Mode Switching During Session

### From Simple to Standard
If during Simple Mode session:
- Multiple user types discovered
- Complex integrations mentioned
- Compliance requirements emerge
- User requests deeper analysis

**Prompt:**
```
I noticed this project might need more detailed analysis.
Would you like to switch to Standard Mode for deeper exploration?

[Y] Yes, switch to Standard Mode
[N] No, continue with Simple Mode
```

### From Standard to Simple
If during Standard Mode session:
- Project simpler than initially thought
- User mentions "just MVP" or "basics only"
- Tight timeline constraints

**Prompt:**
```
This seems like a simpler project than initially thought.
Would you like to switch to Simple Mode for faster completion?

[Y] Yes, switch to Simple Mode
[N] No, continue with Standard Mode
```

---

## PRD Structure by Mode

### Simple Mode PRD
```
1. Executive Summary (brief)
2. Target User (single persona)
3. User Journey (optional, one scenario)
4. Requirements (1-2 epics, 3-5 features)
5. Success Metrics (2-3 metrics)
6. MVP Scope & Rules (combined)
```

### Standard Mode PRD (Medium)
```
1. Executive Summary
2. Target Users (1-2 personas)
3. User Journeys (2-3 scenarios)
4. Requirements (2-4 epics, 6-12 features)
5. Success Metrics (5-8 metrics)
6. Product Scope (MVP + Post-MVP)
7. Rules & Constraints
8. Dependencies & Risks
```

### Standard Mode PRD (Complex)
```
1. Executive Summary
2. Target Users (2-4 personas with relationships)
3. User Journeys (3-5 detailed scenarios)
4. Requirements (4-8 epics, 13-30 features)
5. Success Metrics (10+ metrics, OKRs)
6. Product Scope (MVP + Roadmap)
7. Rules & Constraints
8. Dependencies & Risks
9. Assumptions & Validation
10. Appendices (Glossary, Research, Competitors)
```

---

## Question Depth by Mode

### Step 5 (Requirements) Example

**Simple Mode:**
- "What are the main things users can do?" (3-5 answers)
- Brief acceptance criteria

**Standard Mode (Medium):**
- "Let's break down each user goal into features"
- "For each feature, what actions can users take?"
- Detailed acceptance criteria

**Standard Mode (Complex):**
- Deep dive into each epic
- Edge cases and exceptions
- Permissions per action
- Workflow states
- Integration points
- Error scenarios

---

## Time Estimates by Mode

| Mode | Estimated Time |
|------|----------------|
| Simple | 15-30 minutes |
| Standard (Medium) | 45-60 minutes |
| Standard (Complex) | 60-90+ minutes |
