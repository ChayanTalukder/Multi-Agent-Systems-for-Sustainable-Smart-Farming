# Step 4 — Extraction and QA: Batch 1

## Batch scope

**S35–S40 (6 publications)**

| Study | Publication | QA |
|---|---|---:|
| S35 | An agent-based simulation model of human–environment interactions in agricultural systems | 14/14 |
| S36 | 'Smart' policies to reduce pesticide use and avoid income trade-offs: An agent-based model applied to Thai agriculture | 14/14 |
| S37 | Ex-ante assessment of soil conservation methods in the uplands of Vietnam: An agent-based modeling approach | 14/14 |
| S38 | An agent-based simulation of cooperation in the use of irrigation systems | 13/14 |
| S39 | Water management for irrigation, crop yield and social attitudes: a socio-agricultural agent-based model to explore a collective action problem | 13/14 |
| S40 | An agent-based model of farmer decision-making and water quality impacts at the watershed scale under markets for carbon allowances and a second-generation biofuel crop | 13/14 |

## Main coding decisions

- **S35 — Hybrid:** autonomous farm-household optimisation is combined with local market/auction interaction, technology diffusion and optional environmental coupling.
- **S36 — Decentralised:** individual farm optimisation with social/innovation-network IPM diffusion rather than a central allocator.
- **S37 — Hybrid:** farm optimisation, technology diffusion and spatial soil-fertility feedback are integrated.
- **S38 — Decentralised:** irrigation cooperation emerges through neighbourhood/social-network effects plus government subsidy.
- **S39 — Decentralised:** there is no direct farmer messaging; interaction is environment-mediated through a shared aquifer.
- **S40 — Decentralised; Utility-based + Learning-based:** farmers optimise expected utility, update beliefs with Bayesian inference and exchange information with neighbours.

## Representative findings

- **S36:** under the IPM + progressive-tax + 80% biopesticide-subsidy package, Table 9 reports period-5 reductions of **29.0% in total pesticide use** and **34.3% in highly toxic pesticide use**, while average household income is **8.7% above baseline**.
- **S37:** baseline soil loss is **29.97 t/ha/year for maize** and **26.64 t/ha/year for cassava**; approximately **12–16 USD per ton of soil saved** is estimated for about a **40±2% soil-loss reduction**.
- **S38:** government subsidy exceeding **50% of cooperation costs** produces roughly **80% eventual participation**; the model evaluates 38,400 parameter combinations with 100 repetitions each.
- **S39:** short-view behaviour accelerates groundwater decline; under extreme climate conditions, long-view behaviour becomes economically advantageous when the short-view share exceeds roughly **0.45**.
- **S40:** behavioural assumptions materially affect watershed nitrate loads; at miscanthus-price ratio 0.5 and zero carbon price, reported loads range from **6.30 to 10.12 ×10³ t N/year** across behavioural cases.

## QA

Scores range from **13–14/14**. Deductions concern mainly incomplete explicit limitations reporting (S38–S39) and reduced reproducibility for S40 because part of the full farmer-decision formulation is deferred and no code/data package is provided.

## Deferred to Step 5

`Study_Family_ID` and `Related_Publication_IDs` remain unassigned for S35–S40. They will be reconciled systematically after all 19 new publications have been extracted.

## Validation

- S01–S34 remain unchanged.
- All substantive RQ0–RQ4 fields for S35–S40 are populated.
- QA totals were recalculated and verified.
- S41–S53 remain pending for Batches 2–3.
