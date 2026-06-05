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
Effective Deflection Rate = (DeflectionGoal%) × ScenarioMultiplier × AccuracyVariance
Adjusted Deflections      = TicketVolume × Effective Deflection Rate
Monthly Savings           = Pure Human Cost − Total Hybrid Cost


### Sunk Escalation Tax
Cost Per Escalated Session = SingleTurnCost × TurnsBeforeEscalation
Sunk Token Waste           = EscalatedTickets × Cost Per Escalated Session

> Most calculators assume failed AI interactions cost $0. They do not. 
> This is the #1 source of ROI overstatement in vendor materials.

### Churn Revenue Preservation
Monthly Hours Saved = (Deflections × AHT in minutes) / 60
FTEs Reclaimed      = Monthly Hours Saved / Productive Hours Per Month (default: 160)
Engineering Value   = FTEs Reclaimed × DevHourlyRate × ProductiveHours

> FTEs Reclaimed is a **capacity metric**, not a headcount reduction recommendation. 
> It represents reinvestable engineering bandwidth.

### Risk-Adjusted ROI

### True Loaded Cost Per Deflection
True Loaded Cost = (Token Costs + Platform + PII + Observability + HA) / Adjusted Deflections
> This is the CFO unit economics number. Not just token cost — all-in.

---

## Architecture

### Component Structure
LLMCostDashboard.tsx
│
├── SECTION 1: Type Definitions
│   ├── LLMModel            — Model registry shape
│   ├── DashboardInputs     — All user-controlled inputs (single typed object)
│   └── ComputedFinancials  — All engine output values
│
├── SECTION 2: Constants
│   ├── LLM_MODELS[]        — Model registry with 2026 API pricing
│   └── SCENARIO_MULTIPLIERS — Conservative/Base/Optimistic coefficients
│
├── SECTION 3: Computation Engine
│   └── computeFinancials() — Pure function, fully decoupled from UI
│       ├── Block A: Scenario Adjustment
│       ├── Block B: Volume Calculations
│       ├── Block C: Token Cost Layer
│       ├── Block D: Production Infrastructure & Compliance
│       ├── Block E: Human Cost Baseline vs Hybrid Model
│       ├── Block F: Primary Financial Outputs
│       ├── Block G: TEI — Churn Impact
│       ├── Block H: TEI — Engineering Reinvestment
│       ├── Block I: TEI — Composite Economic Value
│       └── Block J: Risk-Adjusted ROI
│
├── SECTION 4: UI Sub-Components
│   ├── MetricCard          — Badge-classified output card
│   ├── SectionHeader       — Consistent panel labeling
│   ├── SliderInput         — Range input with tooltip
│   └── NumberInput         — Precise numeric input with tooltip
│
└── SECTION 5: Main Dashboard Component
├── State Layer         — All useState declarations, grouped by domain
├── Input Object        — useMemo-consolidated DashboardInputs
├── Engine Call         — useMemo(computeFinancials, [inputs, model])
├── Chart Data          — Derived chart datasets via useMemo
└── Render Tree
├── Header Band
├── Executive Brief (3 KPI cards)
├── Left Panel: Inputs
│   ├── Operational Parameters
│   ├── TEI Inputs (Churn + Engineering)
│   ├── Production Infrastructure Sidebar (collapsible)
│   └── Advanced Token Parameters (collapsible)
└── Right Panel: Outputs
├── Sensitivity Engine / Stress Test
├── Metric Cards (8 cards, 2 rows)
├── 12-Month TCO Projection Chart
├── Token Spend Breakdown + Model Matrix
├── TEI Decomposition Chart
└── Assumptions Documentation Footer

### Design Principles

**Defensible Math First**  
Every formula is documented with business intent in the source. If a CFO asks 
"where does this number come from?" you can open the file and show them.

**Decoupled Computation**  
`computeFinancials()` is a pure function with no React dependencies. You can 
import and call it in a test file, a Node.js script, or a future API endpoint 
without touching the UI layer.

**Zero Flicker Reactivity**  
All derived state flows through `useMemo`. Moving any slider triggers a single 
synchronous recomputation with no intermediate renders.

**Badge Classification System**  
Every output is labeled as either `Financial Projection` or `Operational Metric` — 
a deliberate UX decision to help executives understand the confidence level and 
nature of each number.

---

## Getting Started

### Prerequisites
```bash
node >= 18.0.0
npm >= 9.0.0

# Clone the repository
git clone https://github.com/your-org/ai-deflection-tco-studio.git
cd ai-deflection-tco-studio

# Install dependencies
npm install

# Start development server
npm run dev

{
  "dependencies": {
    "react": "^18.x",
    "react-dom": "^18.x",
    "recharts": "^2.x",
    "lucide-react": "^0.x"
  },
  "devDependencies": {
    "typescript": "^5.x",
    "tailwindcss": "^3.x",
    "@types/react": "^18.x"
  }
}

Configuration

Adding a New LLM Model

Edit the LLM_MODELS registry in the constants section:
{
  name: 'GPT-5',
  provider: 'OpenAI',
  inputCostPer1M: 5.00,        // $ per 1M input tokens
  outputCostPer1M: 20.00,      // $ per 1M output tokens
  averageLatencySeconds: 1.8,  // P50 response latency
  tier: 'Tier 3 (Reasoning/Complex)'
}
Adjusting Scenario Multipliers

Edit SCENARIO_MULTIPLIERS to align with your organization’s risk tolerance:

const SCENARIO_MULTIPLIERS = {
  conservative: 0.70,  // Your org may want 30% haircut vs. 25%
  base: 1.0,
  optimistic: 1.15,    // Cap optimism at 15% if your CFO is skeptical
};

Extracting the Computation Engine
The computeFinancials function has no React dependencies and can be moved to a shared utility:
// lib/financials.ts
export { computeFinancials };
export type { DashboardInputs, ComputedFinancials };

// Use in tests
import { computeFinancials } from '@/lib/financials';
const result = computeFinancials(mockInputs, mockModel);
expect(result.annualSavings).toBeGreaterThan(0);

| Feature | Status | Priority |
| --- | --- | --- |
| Export to PDF (Executive Report) | Planned | High |
| CSV Data Import (real ticket volume) | Planned | High |
| Unit test suite (Vitest) | Planned | High |
| Multi-model routing cost blending | Planned | Medium |
| Saved scenario comparison (A vs B) | Planned | Medium |
| REST API wrapper for computeFinancials | Planned | Medium |
| Shareable URL state (query params) | Planned | Low |
| JIRA/Confluence export integration | Planned | Low |



Use Cases
Pre-Sales / Business Case Development
Run the model with conservative assumptions before presenting to leadership.
Use the stress test panel to show you’ve already pressure-tested the numbers.

Quarterly Business Reviews (QBRs)
Plug in actual deflection rate and CSAT scores to show realized vs. projected TEI.

Vendor Evaluation
Swap model pricing in the LLM registry to compare total cost of ownership
across AI vendors under identical operational assumptions.

FinOps / Budget Planning
Use the infrastructure sidebar to build a realistic annual AI operations budget
including compliance costs for regulated industries.

Interview / Portfolio Demonstration
Demonstrates Staff-level thinking: decoupled architecture, typed interfaces,
executive communication, and business-aware engineering.

Contributing

1. Fork the repository
2. Create a feature branch: git checkout -b feature/pdf-export
3. Follow existing TypeScript patterns and document any new formula blocks with business intent comments
4. Submit a PR with a description of the financial logic change and

why the formula is defensible

If you add a new financial metric, it must include:
[ ] A JSDoc comment explaining the business intent
[ ] A formula comment in computeFinancials()
[ ] A tooltip in the UI with the Executive Rationale
[ ] A badge classification (Financial Projection or Operational Metric)

License
MIT — Use freely, fork openly, cite responsibly.

Author
Built by a CX Engineering leader with production experience scaling
AI-assisted support operations at SaaS and health-tech organizations.

“The goal isn’t to build the most optimistic ROI calculator.
It’s to build the one that holds up when the CFO pushes back.”

Pricing data reflects normalized 2026 API market rates.
Update the LLM_MODELS registry as vendor pricing evolves.