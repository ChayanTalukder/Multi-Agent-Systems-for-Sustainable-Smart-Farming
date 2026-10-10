# Step 4 — Extraction and QA: Batch 2

## Batch scope

**S41–S46 (6 publications)**

| Study | Publication | QA |
|---|---|---:|
| S41 | A hybrid TOPSIS-agent-based framework for reducing the water demand requested by stakeholders with considering the agents' characteristics and optimization of cropping pattern | 13/14 |
| S42 | Fine spatio-temporal simulation of cropping and farming systems effects on irrigation withdrawal dynamics within a river basin | 13/14 |
| S43 | Agent-based spatial models applied to agriculture: a simulation tool for technology diffusion, resource use changes and policy analysis | 13/14 |
| S44 | SINUSE: A multi-agent model to negotiate water demand management on a free access water table | 13/14 |
| S45 | Agent based simulation of a small catchment water management in northern Thailand: Description of the CATCHSCAPE model | 13/14 |
| S46 | Suitability of Multi-Agent Simulations to study irrigated system viability: application to case studies in the Senegal River Valley | 13/14 |

## Main coding decisions

- **S41 — Hierarchical:** village-level agricultural agents respond to a government allocation/management layer, with TOPSIS-personalised behaviour and GA crop-pattern optimisation.
- **S42 — Hybrid:** MAELIA couples autonomous farmer crop/irrigation rules with hydrological and normative components; interaction is primarily shared-state/environment-mediated rather than direct farmer messaging.
- **S43 — Hybrid:** decentralised farm-household optimisation is combined with social diffusion, endogenous land/water markets and hydrological return-flow feedback.
- **S44 — Decentralised:** SINUSE represents direct farmer messages/cooperation plus neighbourhood imitation and shared-aquifer feedback without a central allocator.
- **S45 — Hierarchical:** CATCHSCAPE contains farmer agents plus autonomous canal-manager agents operating at multiple irrigation-management levels with explicit negotiation.
- **S46 — Hierarchical:** SHADOC represents farmer agents and autonomous group agents for water allocation, credit and pumping, with direct communication and collective rules.

## Representative extracted findings

- **S41:** requested water exceeded allocation by **7.6%, 18.2% and 45%** before ABM under wet/normal/drought conditions, versus **1.37%, 3.5% and 1.09%** afterward.
- **S42:** simulated annual irrigation withdrawals differed from agency records by about **10% on average**, with a maximum **23% underestimation in the extreme 2003 drought**.
- **S43:** under ideal technical change, roughly **half of irrigated area** adopts water-saving irrigation within 10 years, versus about **one-fifth** under bandwagon diffusion; nearly **6% of laggard commercial farms exit per year** in the bandwagon scenario.
- **S44:** SINUSE demonstrates a rebound effect: more efficient drip irrigation can improve farmer returns yet **worsen groundwater sustainability** when it stimulates further investment/irrigated-area expansion.
- **S45:** CATCHSCAPE uses **327 farmer agents**; simulated crop spatial patterns match observations at about **80% accuracy** and average yields at at least **70% accuracy**.
- **S46:** repeated SHADOC experiments show viability depends non-linearly on farmer-goal heterogeneity; among 72 scenarios with outside income, moderately heterogeneous populations have more viable outcomes than highly heterogeneous or homogeneous populations.

## QA

All six publications score **13/14**. The deductions are mainly for:
- unavailable/limited reproducibility artifacts (S41, S42, S44, S46);
- exploratory rather than strong predictive validation in S45;
- limitations reporting that is present but comparatively dispersed in S43.

## Foundational IC7 studies

S43–S46 are pre-2010 foundational publications retained under the frozen **IC7 foundational-study exception**. They remain clearly marked in the extraction notes.

## Deferred to Step 5

`Study_Family_ID` and `Related_Publication_IDs` are intentionally unassigned for S41–S46. Likely relationships (e.g. MAELIA and SHADOC/Senegal River Valley lines) will be reconciled only after all 19 citation-search inclusions are extracted.

## Validation

- S01–S40 remain unchanged.
- All substantive RQ0–RQ4 fields for S41–S46 are populated.
- QA totals were recalculated and verified.
- S47–S53 remain pending for Batch 3.
