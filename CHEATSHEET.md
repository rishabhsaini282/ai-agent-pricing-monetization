# AI Agent Pricing — One-Page Cheatsheet

> Last updated: June 2026 | Source: [productleadersdayindia.org](https://productleadersdayindia.org/)

---

## Core Definitions

**Seat-based pricing** — charge per named user per month. Revenue is headcount-bound. Agents don't consume seats, so this model creates a revenue ceiling as AI automates tasks.

**Usage-based pricing** — charge per token, API call, or agent action executed. Revenue scales with compute. Best gross margin protection; worst revenue predictability.

**Outcome-based pricing** — charge per verified business result (e.g. resolved ticket, booked meeting, drafted contract). Revenue only recognized on success. Highest buyer appeal; highest attribution risk.

**Agent-as-FTE pricing** — price the agent as a fraction of the fully loaded salary of the human role it replaces. Taps headcount budgets (10x larger than IT/software budgets).

**Hybrid pricing (base + usage)** — fixed platform fee + metered overage above an included usage tier. Platform fee = predictable ARR. Overage = expansion. Projected at 61% SaaS adoption by 2027.

**Fully loaded cost** — salary + benefits + employer taxes + equipment + overhead. The benchmark for agent-as-FTE pricing conversations.

**Credit-based packaging** — buyer pre-purchases a compute budget (credits) that drawdown in real-time as the agent executes tasks. Gives vendors ARR predictability while maintaining usage alignment.

---

## Gross Margin Benchmarks

| Product Type | Healthy Gross Margin |
|---|---|
| Traditional SaaS | 75–85% |
| AI-native SaaS (at maturity) | 55–70% |
| Pure inference API | 40–60% |
| Outcome-based AI (high resolution rate) | 50–65% |
| Outcome-based AI (poor resolution rate) | Can go below 30% |

**The gap vs. traditional SaaS** exists because AI inference costs scale with usage in a way software licensing costs do not.

**AI COGS formula:**
`AI Gross Margin = (Revenue − Inference Costs − Storage − Support) / Revenue`

Never exclude inference costs from COGS. Teams that do overstate margins early and get a rude shock at scale.

---

## Margin Killers (In Order of Impact)

1. **Inference cost per query** — LLM API calls are the largest variable COGS line. Never price assuming tomorrow's cheaper models.
2. **Agentic chain length** — a 5-step agent costs 5x a single-call query. Multi-tool agents compound fast.
3. **Failure-state compute** — failed queries still consume tokens. Outcome models surface this; usage models don't.
4. **Context window size** — large RAG retrieval chunks per query are a hidden cost driver. Audit chunk sizes in production.

---

## Billing Platform Quick-Compare

| Platform | Core Architecture | Agent Credit Ledger | Outcome Event Hooks | Best For |
|---|---|---|---|---|
| Orb | Event-driven, real-time | ✅ Native | ✅ Configurable | Complex rating logic, hybrid models |
| Metronome | Event-driven, usage-first | ✅ Native | ⚠️ Partial | High-velocity developer APIs |
| Chargebee | Subscription-first + metered overlay | ⚠️ Add-on | ❌ Limited | Teams already on Chargebee needing basic metering |

**Must-have capabilities for AI billing:**
- Idempotent event ingestion (deduplication on retried agent actions)
- Real-time credit drawdown (not batch)
- Customer-facing consumption dashboards
- Audit logs for invoice disputes

---

## Pricing Model Selection at a Glance

| If your agent... | Consider |
|---|---|
| Replaces a specific human role clearly | Agent-as-FTE |
| Deflects support, qualifies leads, or produces deliverables | Outcome-based |
| Consumes variable compute across many customers | Usage-based or Hybrid |
| Is sold to enterprise buyers who need budget certainty | Hybrid (base + usage) |
| Augments many users without replacing any | Seat-based (with usage overlay) |

---

## The Seat-to-Usage Shift in Numbers

- Seat-based pricing market share: **21% → 15%** (one year decline)
- Hybrid pricing projected adoption: **61% of SaaS by 2027**
- Agent-as-FTE budget unlock: headcount budgets are typically **10x larger** than IT/software budgets for the same function

---

## Key Contract Clauses for Outcome-Based Deals

1. **Resolution definition** — explicit criteria (user confirmation OR N hours of inactivity post-response)
2. **Dispute window** — how long a buyer can contest a billed outcome (typically 30 days)
3. **Audit log access** — buyer right to inspect resolution event logs
4. **Failure-rate cap** — optional; some vendors cap monthly charges if resolution rate drops below a threshold
5. **Attribution exclusions** — outcomes caused by human agent involvement are not billed

---

## Sources

All figures and frameworks from [Product Leaders Day India](https://productleadersdayindia.org/blogs/ai-agent-pricing-monetization/ai-agent-pricing-monetization.html) — original research published June 2026.
