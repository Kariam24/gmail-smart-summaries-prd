
---

### `PRD.md`
```markdown
# Product Requirement Document (PRD) — Gmail Smart Summaries

**Owner:** Kariám Rodríguez  
**Last updated:** 2025-08-26

## 1) Problem & Goal
Users waste time parsing long emails; subjects/previews lack actionable context.  
**Goal:** Reduce time-to-first-action on long/important emails by surfacing 2–3 sentence summaries in the inbox preview.

## 2) Users & JTBD
- **Students / knowledge workers:** “When I get long announcements/invites, I need a quick gist so I don’t miss deadlines.”
- **Ops / admin:** “I need critical details (dates/amounts) fast without opening every message.”

## 3) Scope
### MVP
- Summarize **emails >200 words**, English-only.
- Show a **2–3 sentence summary** under subject in inbox; show a banner in open email.
- Server-side processing within Gmail infra; Settings toggle to enable/disable.

### V2+
- Multi-language support, action-item extraction (“RSVP by Friday”), searchable summaries, per-label controls.

## 4) Requirements
### Functional
- Toggle on/off in **Settings → Smart features**.
- Generate summary on message receipt or first open; cache result.
- Display summary in list preview and as an expandable banner in message view.

### Non-functional
- Latency: summary appears ≤2s after open (precompute on receipt when feasible).
- Accuracy: user “usefulness” rating ≥ 4.3/5.
- Accessibility: screen reader friendly; keyboard navigable.

## 5) User Stories (with acceptance criteria)
- **Enable feature**: Given summaries are off, when I enable them, then long emails show a 2–3 sentence summary in preview.
- **Switch off**: Given summaries are on, when I disable them, then previews revert to default for all threads.
- **View details**: Given a summarized email, when I open it, then an “AI Summary” banner appears with expand/collapse.

## 6) Metrics & Targets
- **Adoption:** ≥ 15% of WAUs enable the feature in test cohort.
- **Engagement:** **−20%** median time-to-first-action on summarized emails.
- **Retention:** ≥ 80% of adopters keep it enabled after 30 days.
- **Satisfaction:** ≥ 4.3/5 prompt score; complaint rate not increased.

## 7) Experiment & Rollout
- 5% → 25% → 100% if KPIs pass; guardrails on reply rate and spam marks.

## 8) Risks & Mitigations
- **Over-trust of summaries** → Include “See full email” affordance; conservative phrasing.
- **Privacy concerns** → Opt-in, clear copy, within-Google processing.
- **Internationalization** → Stage rollout; add i18n in V2 based on demand.

## 9) Open Questions
- Should summaries differ by label (Promotions vs. Primary)?
- Ideal refresh cadence for updated threads?
