# AI Deflection TCO Intelligence Studio
### Production-Grade Total Economic Impact (TEI) Platform for AI Support Deflection

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-18.x-61DAFB?logo=react&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-green)
![Audience](https://img.shields.io/badge/audience-CFO%20%2F%20VP%20Executive-6366f1)

---

## Overview

The **AI Deflection TCO Intelligence Studio** is a CFO-defensible financial modeling 
platform built for CX and Support Engineering leaders who need to justify AI investment 
to executive stakeholders with **math they can stand behind in a board room.**

Most vendor-provided ROI calculators are optimistic, incomplete, and indefensible under 
scrutiny. This platform was built to close that gap by modeling the **Total Economic 
Impact (TEI)** of an AI deflection program — including costs that vendors never 
show you.

> **Built for:** Head of Support · Director of CX · VP of Engineering · FinOps · CFO  · AIOps  
> **Stack:** React 18 · TypeScript · Recharts · Lucide Icons · Tailwind CSS

---

## The Problem This Solves

When you present an AI deflection ROI to a CFO, they will ask questions that 
most calculators cannot answer:

| CFO Question | Typical Calculator | This Platform |
|---|---|---|
| "What happens if the AI underperforms by 15%?" | ❌ No scenario modeling | ✅ Stress Test Engine |
| "What about HIPAA/GDPR compliance costs?" | ❌ Not included | ✅ PII Redaction line item |
| "What does a failed AI conversation cost us?" | ❌ Assumed zero | ✅ Sunk Escalation Tax |
| "How does this affect customer churn?" | ❌ Not modeled | ✅ CLV Churn Impact Engine |
| "What engineering capacity does this free up?" | ❌ Not modeled | ✅ FTE Reclaimed Metric |
| "What's our observability/audit cost?" | ❌ Not included | ✅ LangSmith/Logging line item |
| "Can you show me worst-case and best-case?" | ❌ One number only | ✅ Conservative/Base/Optimistic modes |

---

## Key Features

### 💰 Total Economic Impact (TEI) Engine
Goes beyond simple cost-per-ticket math to model the full economic argument:
- **Direct Operational Savings** — Human cost reduction from AI deflection
- **Churn Revenue Preservation** — CLV-weighted value of prevented churn
- **Engineering Reinvestment Value** — FTE capacity reclaimed from manual work
- **Risk-Adjusted ROI** — Scenario-discounted return on CapEx investment

### 🧪 Sensitivity / Stress Test Engine
Built for board-level range presentation:
- **3-Mode Scenario Toggle** — Conservative (−25%), Base, Optimistic (+20%)
- **AI Accuracy Variance Slider** — ±15% delta on deflection rate
- **Churn Sensitivity Multiplier** — 0.25×–2.5× CLV-to-churn conversion scaling
- All outputs recalculate instantly via `useMemo` with zero UI flicker

### 🛡️ Production TCO Realism
Surfaces the infrastructure costs most calculators deliberately hide:
- **PII Redaction / Security Layer** — HIPAA, GDPR, SOC2 compliance tooling
- **Observability & Logging** — LangSmith, Helicone, or equivalent audit trail
- **High Availability Fallback** — Secondary model cost for SLA protection
- Every line item includes an **Executive Rationale** tooltip explaining *why* it exists

### 🤖 Multi-Model LLM Registry
Compare models across your real operational parameters:
- **5 production models** — GPT-4o, GPT-4o Mini, Claude 3.5 Sonnet, 
  Claude 3.5 Haiku, Gemini 1.5 Flash
- **Latency vs. Cost scatter matrix** — Visual model selection guidance
- **Tier-based routing strategy** — Tier 1/2/3 classification for intelligent 
  traffic routing

### 📊 Executive Visual Layer
- **Summary Executive Brief** — Net Annual TEI, FTEs Reclaimed, Risk-Adjusted ROI 
  at the top before any detail
- **12-Month Cumulative TCO Chart** — Legacy baseline vs. AI Hybrid with CapEx 
  loaded at M1
- **TEI Decomposition Bar Chart** — Monthly and annual value stack breakdown
- **Token Budget Allocation** — Resolved value vs. escalation sunk cost vs. 
  compliance overhead
- Every output card is labeled as either **Financial Projection** or 
  **Operational Metric**

---

## Defensible Math — Formula Reference

All calculations are documented in the source code. Key formulas:

### Core Deflection Economics
