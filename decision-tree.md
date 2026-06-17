# AI Agent Pricing Model Decision Tree

Work through these questions in order. Stop at the first branch that fits your product.

> Source analysis: [productleadersdayindia.org](https://productleadersdayindia.org/) | Last updated: June 2026

---

## Step 1: Does your agent clearly replace a human role?

**Question:** Can you name the specific job title this agent replaces or substantially augments — and would a buyer's HR or ops team recognize that replacement?

Examples of "yes":
- "This replaces a junior SDR making outbound calls"
- "This replaces an associate attorney doing contract review"
- "This replaces a financial analyst building weekly reports"

Examples of "no":
- "This makes everyone a little more productive"
- "This assists the team with various tasks"
- "This is a copilot for the whole department"

**→ If YES:** Consider **Agent-as-FTE pricing.**
- Anchor price to 20–40% of the fully loaded annual cost of the replaced role
- Sell into headcount / HR budgets, not IT budgets (typically 10x larger)
- Requires strong, documented ROI proof before expansion conversations
- Does not work if the agent is positioned as a copilot rather than a replacement

**→ If NO:** Proceed to Step 2.

---

## Step 2: Can you define a verifiable business outcome?

**Question:** Is there a single, unambiguous event that signals the agent delivered value — one that can be logged, audited, and agreed upon contractually?

Examples of verifiable outcomes:
- Customer support ticket resolved without human escalation
- Qualified sales meeting booked on a calendar
- Legal contract reviewed and returned with redlines
- Invoice processed and posted to the accounting system

Examples that are NOT verifiable outcomes (too fuzzy):
- "User felt more informed"
- "Response was helpful"
- "Team saved time" (how much time? whose time?)

**→ If YES:** Consider **Outcome-based pricing.**
- Define the resolution event in the contract before go-live (not after)
- Build audit logs from day one — you will need them for disputed invoices
- Price the outcome at 10–20% of the value the buyer receives per event
- Budget for margin erosion: failed queries still consume inference compute
- Include a dispute window (30 days is standard) and clear attribution exclusions

**→ If NO:** Proceed to Step 3.

---

## Step 3: Are you selling to enterprise buyers who need budget predictability?

**Question:** Will your deals be blocked or slowed by enterprise procurement teams who need a predictable, committed spend for their annual budget?

Signs you're in this situation:
- Deals require finance sign-off above a threshold (typically $25K+/year)
- Buyers ask for "what's the maximum I could spend?" in sales calls
- Procurement insists on MSAs with spend caps
- Your buyers run on fiscal-year budget cycles

**→ If YES:** Consider **Hybrid pricing (base + usage).**
- Set the platform fee to cover your fixed cost base (R&D allocation + support)
- Include a usage tier in the platform fee that covers the median customer's consumption
- Charge overage at a per-unit rate above the included tier
- The platform fee books as ARR; overage is expansion revenue
- Critical design rule: the platform fee must cover your fixed costs even at zero overage

**→ If NO:** Proceed to Step 4.

---

## Step 4: Is your primary buyer technical (developer or engineer)?

**Question:** Will the person evaluating your product be able to forecast their own token or API call consumption — and will they expect to pay proportionally to what they use?

Signs of a technical buyer:
- Your product is an API, SDK, or developer tool
- Buyers evaluate you through a sandbox before committing
- Buyers ask questions about rate limits and throughput
- Docs are more important than sales decks in your pipeline

**→ If YES:** Consider **Usage-based pricing with token or call billing.**
- Use tokens as the billing unit for developers who can forecast consumption
- Provide a pricing calculator in docs — remove purchase anxiety before it forms
- Offer committed spend discounts (pre-purchased credits) to build ARR
- Build a real-time usage dashboard — developers check this compulsively
- Watch for power users who consume 10x the average; they will test your margin

**→ If NO (buyer is business, not technical):** Proceed to Step 5.

---

## Step 5: Does your product have meaningful variation in per-user compute consumption?

**Question:** If you look at your actual or projected user base, do some users generate 5x or 10x the compute cost of the median user?

**→ If YES (high variance):** Consider **Usage-based pricing with action or task billing** (not tokens — business buyers don't understand tokens).
- Bill per agent action, per task completed, or per document processed
- These units are meaningful to a business buyer
- Offer monthly credit packages at a slight discount vs. pay-as-you-go
- Be prepared to explain overage clearly in the sales cycle

**→ If NO (low variance — most users consume roughly the same compute):** Consider **Seat-based pricing, with a usage overlay.**
- Seat pricing is defensible when per-user compute is roughly uniform
- Add a usage overlay (e.g., credits included per seat, overage charged per additional unit) to protect against outlier power users
- Review seat pricing annually — if AI automation reduces headcount at buyer, you will need to migrate to usage or hybrid before renewal

---

## Common Mistakes to Avoid

**Mistake 1: Using seat pricing for an autonomous agent.**
If your agent executes tasks without a human in the loop, there is no meaningful "seat." Revenue will plateau as AI handles more work.

**Mistake 2: Using outcome pricing without contractual resolution definitions.**
Defining "resolved" verbally during a sales call is not enough. You will dispute your first 10 invoices. Write it into the contract.

**Mistake 3: Setting the hybrid platform fee too low.**
The platform fee must cover fixed costs. Vendors who set it low and rely on overage to be profitable get hurt during the first 6 months of customer deployment when usage is ramping up.

**Mistake 4: Excluding inference costs from COGS.**
Every LLM call is a cost-of-revenue item. Teams that put inference in R&D or G&A overstate gross margin and underprice their product.

**Mistake 5: Pricing for today's model costs.**
Inference costs will fall, but they won't fall on your timeline. Price based on current costs with a margin buffer — you can always lower prices; restoring margin after underpricing is much harder.

---

## Quick Reference

| Pricing Model | Best Signal to Use It |
|---|---|
| Agent-as-FTE | Named human role being replaced; headcount budget available |
| Outcome-based | Verifiable success event; buyer motivated by "pay for results" |
| Hybrid (base + usage) | Enterprise procurement; need for predictable spend commitments |
| Usage-based (tokens/calls) | Developer buyers; high consumption variance |
| Seat + usage overlay | Low compute variance; augmentation not replacement |

---

**More detail on each model:** [AI Agent Pricing playbook](https://productleadersdayindia.org/blogs/ai-agent-pricing-monetization/ai-agent-pricing-monetization.html)
