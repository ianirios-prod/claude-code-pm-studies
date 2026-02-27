# PRD: AI Insights Feed — Personalization by Objective

**Status:** Draft
**Author:** PM
**Last Updated:** 2026-02-20
**Target Release:** Sprint 44 (2026-03-10)

---

## Problem Statement

DataFlow AI currently surfaces insights to all users in the same priority queue, regardless of their current business objectives. This results in 60% of insights being perceived as irrelevant (Priya Chen, Enterprise customer interview, Feb 2026).

**Core Problem:** Insight relevance is not personalized to what the user is trying to achieve right now.

---

## Goals

| Goal | Metric | Target |
|------|--------|--------|
| Increase insight engagement rate | % of insights acted upon | 15% → 35% |
| Reduce "irrelevant insights" feedback | Negative feedback rate | 60% → <20% |
| Improve NPS for AI Insights feature | Feature-level NPS | 12 → 40 |
| Reduce manual insight review (internal) | Hours/week of manual QA | 8h → 2h |

---

## Non-Goals
- Building a full OKR management system
- Replacing Jira/Linear for goal tracking
- Real-time OKR progress dashboards
- Sharing OKRs across users (each user sets their own objectives)

---

## User Stories

**As a PM**, I want to set my current objectives (e.g., "reduce churn", "improve activation") so that the insights I see are prioritized based on what matters to me right now.

**As a PM**, I want to understand *why* an insight was shown to me so that I can quickly decide if it's worth investigating.

**As a team lead**, I want to see insights ranked by their potential impact on my active OKRs so that my team focuses on what matters.

---

## Proposed Solution

### Phase 1 (Sprint 44): Objective Setting + Basic Prioritization
1. **Objective Picker:** Simple UI to select 1–3 current objectives from a predefined list (reduce churn, improve activation, increase DAU, improve retention, reduce time-to-value)
2. **Insight Scoring:** Score each insight based on relevance to selected objectives using a scoring model
3. **Visual Priority Indicator:** Tag insights with objective relevance badge

### Phase 2 (Sprint 45): Context Explanation
1. **"Why this insight" card:** For each insight, show: metric that triggered it, time window, magnitude vs. baseline
2. **Related metrics:** 2–3 metrics correlated with the insight

---

## Technical Approach

### Insight Scoring Model
- Input: User objectives (categorical), Insight metadata (affected metrics, segments, magnitude)
- Mapping: Predefined relevance matrix — e.g., "reduce churn" → high relevance for retention metrics, session frequency, support ticket volume
- Output: Relevance score (0–1) per insight per user

### Prompt Update
- Inject user objectives into the insight generation prompt
- Example: "The user's current objective is to reduce churn. Prioritize insights related to retention, engagement drop-offs, and at-risk segments."

### Infrastructure
- Store objectives in user profile table (new column: `user_objectives jsonb`)
- Compute relevance score at insight fetch time (not generation time — avoids regenerating all insights)

---

## Acceptance Criteria

- [ ] User can set 1–3 objectives from a predefined list
- [ ] Insights in the feed are sorted by relevance score to selected objectives
- [ ] Each insight shows a "relevance badge" indicating which objective it relates to
- [ ] Latency impact of relevance scoring: < 100ms (scored in-memory, not via LLM)
- [ ] Eval pipeline validates relevance scores on a sample of 50 insights/day
- [ ] Feature flag enabled: off by default, manual opt-in for Enterprise beta users

---

## Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Predefined objective list doesn't cover user needs | Medium | High | User research validation before shipping; allow free-text objective as fallback |
| Relevance scoring model has poor accuracy | Medium | High | Manual eval before launch; use eval pipeline from Sprint 43 |
| Users don't engage with objective setting | Medium | Medium | Default objectives inferred from usage patterns (fallback) |

---

## Dependencies
- Eval pipeline (Sprint 43) — must be in place before launch
- Prompt optimization (Sprint 43) — required to keep latency within target

---

## Open Questions
1. Should objectives be set at user level or workspace level?
2. Do we allow free-text objectives or only predefined? (Risk: LLM quality degrades with novel objectives)
3. Should we infer objectives from usage patterns for users who don't set them?
