# PRD Template

Use this template to generate Product Requirements Documents. Replace all `{{placeholders}}` with actual content.

---

```markdown
---
document_type: "Product Requirements Document"
project_name: "{{project_name}}"
version: "{{version}}"
created_date: "{{created_date}}"
last_updated: "{{last_updated}}"
language: "{{language}}"
complexity: "{{complexity}}"
author: "PRD Creator Skill"
status: "{{status}}"
---

# Product Requirements Document: {{project_name}}

## Document Info

| Field | Value |
|-------|-------|
| **Version** | {{version}} |
| **Created** | {{created_date}} |
| **Updated** | {{last_updated}} |
| **Status** | {{status}} |
| **Complexity** | {{complexity}} |

---

## 1. Executive Summary

### 1.1 Product Vision
{{product_vision}}

### 1.2 Problem Statement
{{problem_statement}}

### 1.3 Value Proposition
{{value_proposition}}

### 1.4 Target Launch
{{target_launch}}

### 1.5 Key Differentiators
{{key_differentiators}}

---

## 2. Target Users

### 2.1 Primary Persona: {{primary_persona_name}}

#### Demographics
- **Role/Job**: {{persona_role}}
- **Context**: {{persona_context}}
- **Tech Proficiency**: {{persona_tech_level}}

#### Goals
1. {{persona_goal_1}}
2. {{persona_goal_2}}
3. {{persona_goal_3}}

#### Pain Points
1. {{persona_pain_1}}
2. {{persona_pain_2}}
3. {{persona_pain_3}}

#### Current Solutions
{{persona_current_solutions}}

#### Representative Quote
> "{{persona_quote}}"

{{#if secondary_personas}}
### 2.2 Secondary Personas

{{#each secondary_personas}}
#### {{name}}
- **Role**: {{role}}
- **Key Need**: {{key_need}}
- **Relationship to Primary**: {{relationship}}
{{/each}}
{{/if}}

---

## 3. User Journeys

### 3.1 Journey: {{journey_name}}

**Persona**: {{journey_persona}}
**Scenario**: {{journey_scenario}}

#### Opening Scene (Problem Context)
{{journey_opening}}

- **Where**: {{journey_where}}
- **When**: {{journey_when}}
- **Emotion**: {{journey_emotion_start}}

#### Discovery
{{journey_discovery}}

- **Channel**: {{discovery_channel}}
- **Hook**: {{discovery_hook}}
- **Decision Trigger**: {{discovery_trigger}}

#### First Use
{{journey_first_use}}

- **First Action**: {{first_action}}
- **Learning Curve**: {{learning_curve}}
- **Quick Win**: {{quick_win}}

#### Core Usage Loop
{{journey_core_loop}}

- **Trigger**: {{loop_trigger}}
- **Action**: {{loop_action}}
- **Reward**: {{loop_reward}}
- **Investment**: {{loop_investment}}

#### Success Moment
{{journey_success}}

- **Aha Moment**: {{aha_moment}}
- **Outcome**: {{success_outcome}}
- **Emotion**: {{journey_emotion_end}}

#### Ongoing Value
{{journey_ongoing}}

{{#if additional_journeys}}
### 3.2 Additional Journeys

{{#each additional_journeys}}
#### Journey: {{name}}
{{description}}
{{/each}}
{{/if}}

---

## 4. Product Requirements

### Requirements Overview

| Metric | Count |
|--------|-------|
| **Epics** | {{epic_count}} |
| **Features** | {{feature_count}} |
| **User Stories** | {{story_count}} |
| **MVP Stories** | {{mvp_story_count}} |

---

{{#each epics}}
### Epic {{@index}}: {{name}}

> {{description}}

**Business Goal**: {{business_goal}}

{{#each features}}
#### Feature {{../../../@index}}.{{@index}}: {{name}}

- **Description**: {{description}}
- **Background**: {{background}}
- **User Value**: {{user_value}}
- **Alternatives Considered**: {{alternatives}}
- **Success Criteria**: {{success_criteria}}

##### User Stories

| ID | User Story | Acceptance Criteria | Priority |
|----|------------|---------------------|----------|
{{#each stories}}
| {{id}} | As a {{actor}}, I want to {{action}} so that {{benefit}} | {{acceptance_criteria}} | {{priority}} |
{{/each}}

{{/each}}

---
{{/each}}

### 4.X Edge Cases & Exceptions

| Scenario | Expected Behavior |
|----------|-------------------|
{{#each edge_cases}}
| {{scenario}} | {{behavior}} |
{{/each}}

### 4.Y Non-Functional Requirements (NFRs)

| Category | Requirement | Target |
|----------|-------------|--------|
{{#each nfrs}}
| {{category}} | {{requirement}} | {{target}} |
{{/each}}

---

## 5. Success Metrics

### 5.1 User Success Metrics

| Metric | Definition | Target | Measurement |
|--------|------------|--------|-------------|
{{#each user_success_metrics}}
| {{name}} | {{definition}} | {{target}} | {{measurement}} |
{{/each}}

### 5.2 Business Success Metrics

| Metric | Definition | Target | Measurement |
|--------|------------|--------|-------------|
{{#each business_success_metrics}}
| {{name}} | {{definition}} | {{target}} | {{measurement}} |
{{/each}}

### 5.3 Key Results (OKRs)

**Objective**: {{objective}}

| Key Result | Target | Measurement |
|------------|--------|-------------|
{{#each key_results}}
| {{description}} | {{target}} | {{measurement}} |
{{/each}}

---

## 6. Product Scope

### 6.1 MVP (Must-Have) - P0

These features are **required** for launch. Product fails without them.

{{#each mvp_features}}
- [ ] **{{name}}**: {{description}}
{{/each}}

### 6.2 Post-MVP (Nice-to-Have) - P1

Important features that can wait for v2.

{{#each post_mvp_features}}
- [ ] **{{name}}**: {{description}} | *Reason to defer*: {{defer_reason}}
{{/each}}

### 6.3 Future Considerations - P2+

Features for future versions.

{{#each future_features}}
- **{{name}}**: {{description}}
{{/each}}

### 6.4 Out of Scope

These will **NOT** be included.

{{#each out_of_scope}}
- **{{name}}**: {{reason}}
{{/each}}

---

## 7. Rules & Boundaries

### 7.1 Must-Have Rules

Critical rules the product must always follow.

| Rule | Reason |
|------|--------|
{{#each must_have_rules}}
| {{rule}} | {{reason}} |
{{/each}}

### 7.2 Things to Avoid

What the product should never do.

| Avoid | Reason |
|-------|--------|
{{#each things_to_avoid}}
| {{item}} | {{reason}} |
{{/each}}

---

## 8. Constraints & Assumptions

### 8.1 Constraints

| Type | Constraint | Impact |
|------|------------|--------|
{{#each constraints}}
| {{type}} | {{description}} | {{impact}} |
{{/each}}

### 8.2 Dependencies

| Dependency | Type | Status | Impact if Delayed |
|------------|------|--------|-------------------|
{{#each dependencies}}
| {{name}} | {{type}} | {{status}} | {{impact}} |
{{/each}}

### 8.3 Risks

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
{{#each risks}}
| {{description}} | {{probability}} | {{impact}} | {{mitigation}} |
{{/each}}

### 8.4 Assumptions

| Assumption | Validation Method | If False... |
|------------|-------------------|-------------|
{{#each assumptions}}
| {{assumption}} | {{validation}} | {{consequence}} |
{{/each}}

---

## 9. Change History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
{{#each change_history}}
| {{version}} | {{date}} | {{changes}} | {{author}} |
{{/each}}

---

## Appendix

### A. Glossary

{{#each glossary}}
- **{{term}}**: {{definition}}
{{/each}}

### B. Research Findings

{{research_findings}}

### C. Competitor Analysis

{{competitor_analysis}}

---

*Generated by PRD Creator Skill*
*Document Version: {{version}}*
```

---

## Template Usage Instructions

### Required Fields (Minimum)
- project_name
- version
- created_date
- problem_statement
- value_proposition
- primary_persona (name, goals, pain_points)
- At least 1 Epic with Features and Stories
- MVP scope

### Optional Fields
- Secondary personas
- Additional journeys
- Research findings
- Competitor analysis
- Glossary

### Complexity Adjustments

**Simple Projects:**
- 1 persona
- 1 journey
- 1-2 epics
- 3-5 features
- Basic metrics

**Medium Projects:**
- 1-2 personas
- 2-3 journeys
- 2-4 epics
- 6-12 features
- Detailed metrics

**Complex Projects:**
- 2+ personas
- 3+ journeys
- 4+ epics
- 13+ features
- Comprehensive metrics & risks

### Priority Definitions

| Priority | Label | Definition |
|----------|-------|------------|
| P0 | Must-Have | Required for MVP. Product fails without it. |
| P1 | Should-Have | Important but product works without it. |
| P2 | Nice-to-Have | Enhances experience but not essential. |
| P3 | Future | Not for this release. Future consideration. |
