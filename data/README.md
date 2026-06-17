# data/ — Column Definitions and Source Notes

## pricing-models-comparison.csv

This file contains a structured comparison of the five dominant AI agent pricing models as of June 2026. One row per model.

### Column Definitions

| Column | Type | Description |
|---|---|---|
| `model` | string | Name of the pricing model |
| `charge_basis` | string | The unit or event that triggers a charge |
| `best_fit_product_type` | string | Product categories where this model performs well |
| `gross_margin_protection` | string | Qualitative rating (Low / Medium / High) with brief rationale |
| `revenue_predictability` | string | How forecastable revenue is for the vendor |
| `sales_complexity` | string | Difficulty of selling and closing the model |
| `nrr_potential` | string | Net Revenue Retention ceiling under this model |
| `enterprise_fit` | string | How well the model maps to enterprise procurement norms |
| `buyer_budget_tapped` | string | Which buyer budget the model is sold against |
| `biggest_risk` | string | Primary failure mode or commercial risk |
| `real_world_example` | string | Named products or companies using this model publicly |

### Notes on Data Quality

- Gross margin ratings are qualitative based on the structural relationship between cost-to-serve and charge basis — not derived from any single company's financials.
- The 61% hybrid pricing adoption figure (referenced in the README) comes from the analysis in [Hybrid Pricing: How 61% of SaaS Will Charge](https://productleadersdayindia.org/blogs/ai-agent-pricing-monetization/hybrid-saas-pricing-model.html).
- The seat-based market share decline (21% → 15%) comes from [Seat vs. Usage Pricing: Why Seats Lost Ground](https://productleadersdayindia.org/blogs/ai-agent-pricing-monetization/seat-based-vs-usage-based-pricing.html).
- Intercom Fin's $0.99/resolution pricing is sourced from [Outcome-Based Pricing: What Intercom Won't Say](https://productleadersdayindia.org/blogs/ai-agent-pricing-monetization/outcome-based-pricing-examples.html).
- Healthy AI gross margin range (55–70%) is sourced from [AI Gross Margin: Why Yours Is Quietly Bleeding](https://productleadersdayindia.org/blogs/ai-agent-pricing-monetization/ai-gross-margin-cost-to-serve.html).

### Suggested Uses

- Paste into Google Sheets or Excel for internal pricing model evaluation
- Use `gross_margin_protection` and `revenue_predictability` columns together to plot a 2x2 for your leadership team
- Filter by `buyer_budget_tapped` to identify which pricing models unlock different budget pools in your target accounts

### Update Cadence

This data is reviewed quarterly. If a figure is outdated or a new model deserves a row, open an issue in the repo with a source link.
