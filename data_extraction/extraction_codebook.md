# Extraction Codebook

## Purpose

This codebook defines the main coding rules used during data extraction.

Only fields requiring standardised interpretation are included here. Bibliographic fields and straightforward free-text fields are defined in `data_extraction_schema.md`.

---

## General Coding Rules

Use:

- `NR` = Not reported
- `NA` = Not applicable
- `UNC` = Unclear or ambiguous

Multiple applicable values are separated by semicolons.

```text
Water; Energy
```

Coding should be based on information reported in the full text. Reviewer interpretation should remain conservative.

---

# RQ0 — MAS Application and Scope

## `System_Integration_Scope`

| Value | Definition |
|---|---|
| `Single-domain` | One main agricultural function or subsystem is addressed. |
| `Multi-domain` | Two or more agricultural functions are connected. |
| `Integrated-system` | The MAS represents a broader farm, value-chain, or social-ecological system. |
| `UNC` | Scope cannot be determined reliably. |

## `Contribution_Type`

Use one or more where applicable:

- `Architecture`
- `Algorithm`
- `Coordination mechanism`
- `Decision-support system`
- `Control system`
- `Simulation model`
- `Optimisation method`
- `Platform/framework`
- `Other`

## `Implementation_Maturity`

| Value | Definition |
|---|---|
| `Conceptual` | Proposed model or architecture without substantive experimental implementation. |
| `Simulation` | Evaluated primarily through simulation. |
| `Prototype` | Implemented prototype or proof of concept. |
| `Controlled experiment` | Evaluated in laboratory or controlled conditions. |
| `Field pilot` | Tested in an agricultural field/farm setting on a limited scale. |
| `Operational` | Used in a real operational environment. |

Use the highest maturity level demonstrated in the paper.

---

# RQ1 — Agents, Architecture, and Decision-Making

## `MAS_Architecture`

| Value | Definition |
|---|---|
| `Centralised` | A central agent/controller makes the main system decisions. |
| `Decentralised` | Decision authority is distributed among agents without a dominant central controller. |
| `Hierarchical` | Agents operate at explicitly different control or decision levels. |
| `Hybrid` | Centralised/hierarchical and decentralised components are combined. |
| `UNC` | Architecture cannot be determined reliably. |

## `Agent_Paradigm`

Use only when identifiable from the paper:

- `Reactive`
- `Rule-based`
- `Utility-based`
- `BDI`
- `Learning-based`
- `Hybrid`
- `Other`
- `NR`

Do not infer a formal paradigm from general agent behaviour alone.

## `Decision_Mechanism`

Examples include:

- `Rules`
- `Optimisation`
- `Planning`
- `Machine learning`
- `Reinforcement learning`
- `MARL`
- `MPC`
- `Auction/market-based`
- `Hybrid`
- `Other`

Record the mechanism actually used for decision-making.

---

# RQ2 — Coordination and Resource Management

## `Interaction_Type`

Use one or more:

- `Communication`
- `Information sharing`
- `Cooperation`
- `Coordination`
- `Negotiation`
- `Competition`
- `Task allocation`

Do not code simple message exchange as `Negotiation` unless agents actively bargain, bid, propose, counter-propose, or use an explicit negotiation mechanism.

## `Coordination_Mechanism`

Examples include:

- `Priority/rule-based`
- `Auction`
- `Contract-net`
- `Market-based`
- `Utility-based`
- `Consensus`
- `Optimisation`
- `Scheduling`
- `MARL`
- `Central coordinator`
- `Other`

Use the terminology reported by the authors where possible.

## `Resource_Scarcity_or_Constraint_Modelled`

| Value | Definition |
|---|---|
| `Yes` | Limited resource availability, capacity, competition, or scheduling constraints are explicitly represented. |
| `No` | The resource/task is modelled without meaningful scarcity or capacity constraints. |
| `NA` | No resource or task-allocation problem is involved. |
| `UNC` | Constraint handling cannot be determined. |

## `Allocation_or_Coordination_Objective`

Examples include:

- `Efficiency`
- `Cost`
- `Profit`
- `Productivity`
- `Fairness`
- `Resource utilisation`
- `Sustainability`
- `Animal welfare`
- `Conflict reduction`
- `Multi-objective`
- `Other`

Multiple objectives may be recorded.

---

# RQ3 — Outcomes and Sustainability

## `Sustainability_Addressed`

| Value | Definition |
|---|---|
| `Direct` | Sustainability or environmental performance is explicitly modelled, optimised, or evaluated. |
| `Indirect` | Resource efficiency or related benefits are reported, but sustainability is not explicitly evaluated. |
| `Not addressed` | No substantive sustainability/environmental outcome is investigated. |

Do not classify a study as `Direct` only because terms such as *sustainable* or *smart agriculture* appear in the introduction.

## `Quantitative_Results`

Record key results using the original values and units reported by the authors.

Example:

```text
Water use reduced by 18% compared with baseline.
```

Do not normalise or recalculate results during extraction.

## `Tradeoffs_Reported`

Record only trade-offs explicitly analysed or discussed by the authors, such as:

```text
Water saving vs crop yield
Cost vs animal welfare
Energy use vs productivity
```

Use `NR` if no trade-off is reported.

---

# RQ4 — Evaluation and Research Gaps

## `Evaluation_Type`

Use one or more:

- `Simulation`
- `Analytical`
- `Case study`
- `Controlled experiment`
- `Laboratory experiment`
- `Field experiment`
- `Pilot deployment`
- `Real-world deployment`

## `Real_World_Deployment`

| Value | Definition |
|---|---|
| `Yes` | The system was used or evaluated in an actual operational agricultural environment. |
| `Partial` | Some real-world components/data were used, but the complete MAS was not operationally deployed. |
| `No` | Evaluation was simulation-, laboratory-, or model-based only. |
| `UNC` | Deployment status is unclear. |

## `Code_Available` / `Data_Available`

Use:

- `Yes`
- `No`
- `NR`

Use `Yes` only when the paper provides or clearly identifies accessible code/data.

## `Limitation_Categories`

Use one or more where supported:

- `Scalability`
- `Uncertainty`
- `Explainability`
- `Interoperability`
- `Environmental modelling`
- `Computational requirements`
- `Reproducibility/data availability`
- `Deployment cost`
- `Real-world validation`
- `Adoption/usability`
- `Other`

Categories should be assigned only when the limitation is explicitly reported or clearly demonstrated by the study design.

## `Reported_Limitations`

Record the authors' stated limitations in concise paraphrased form.

## `Reported_Research_Gaps`

Record explicitly stated future work, unresolved problems, or research gaps.

Do not create speculative research gaps during extraction. Cross-study gaps will be identified later during synthesis.

---

# Evidence Locators

For `RQ1_Evidence_Locator` to `RQ4_Evidence_Locator`, record the most useful supporting location.

Examples:

```text
p. 7
pp. 6–8
Section 3.2
Table 4
Section 4.1; Figure 5
```

Exact quotations are not required.

---

# Study Families

Assign the same `Study_Family_ID` only when publications are confirmed to describe closely related work, such as:

- the same MAS or platform;
- the same experimental dataset;
- a conference paper later extended as a journal article;
- an explicitly extended version of an earlier included study.

Similar titles or topics alone are insufficient.

Related publications remain separate extraction records.

---

# Pilot and Finalisation

This codebook will first be tested on three included studies.

Any ambiguous or impractical coding rule identified during the pilot may be revised.

After the pilot:

- the schema and codebook will be frozen as Version 1.0;
- the same coding rules will then be applied to all 34 included publications.
