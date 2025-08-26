# Gmail Smart Summaries (PRD Project)

**One-liner:** AI-powered Gmail feature that condenses long emails into 2–3 key sentences directly in the inbox preview.

This repo contains a concise Product Requirement Document (PRD), mockup flow notes, metrics plan, and privacy considerations
for a PM portfolio project. It’s idea-first (not code-first) and demonstrates product thinking: problem definition, MVP vs. v2,
user stories, success metrics, and tradeoffs.

---

## 📌 Overview
- **Problem:** People lose time parsing long emails; subjects/previews often lack actionable context.
- **Solution:** Summaries under the subject line showing key details and action items.
- **MVP:** English-only, summarize emails >200 words, shown in preview + banner in open email.
- **V2:** Action-item extraction, multi-language, searchable summaries, per-label controls.
- **KPIs:** Adoption, engagement (time-to-first-action), 30-day retention, CSAT.

---

## 🗂 Repo Structure
- `PRD.md` — Full 1-page PRD.
- `MOCKUPS.md` — Flow notes + Figma link placeholder.
- `METRICS.md` — Events, dashboards, success targets.
- `PRIVACY.md` — Consent, data handling, opt-out.

---

## 🔗 Portfolio Links
- **Figma (add your link):** https://www.figma.com/file/ADD-YOUR-FILE
- **Live PRD (optional):** Publish `PRD.md` as a Notion/Docs public page and link it here.

---

## 🧪 A/B Test Plan (MVP)
- **Experiment:** 5% → 25% → 100% rollout if KPIs pass.
- **Primary metric:** **Time-to-first-action** on summarized emails (target −20% vs. control).
- **Guardrails:** Reply rate unchanged or improved; no increase in unsubscribe/spam marks.

---

## 🛡 Privacy
- **Opt-in** toggle in Settings; clear explanation of what’s summarized.
- **Server-side processing** within Gmail infra; no third-party sharing.
- **Easy disable** and per-label exemptions (v2).

