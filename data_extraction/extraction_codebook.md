# Extraction Codebook

**Version:** 1.0 — Frozen  
**Date:** 3 October 2026  
**Status:** Final coding rules following three-study pilot testing

---

## Purpose

This codebook defines the main coding rules used during data extraction.

Only fields requiring standardised interpretation are included here. Bibliographic fields and straightforward free-text fields are defined in `data_extraction_schema.md`.

---

# General Coding Rules

Use:

- `NR` = Not reported
- `NA` = Not applicable
- `UNC` = Unclear or ambiguous

Multiple applicable values are separated by semicolons.

Example:

```text
Water; Energy
```

Coding should be based on information reported in the full text. Reviewer interpretation should remain conservative.

Do not infer mechanisms, outcomes, or system properties that are not sufficiently supported by the publication.

---

# RQ0 — MAS Application and Scope

## `System_Integration_Scope`

| Value | Definition |
|---|---|
| `Single-domain` | One main agricultural function or subsystem is addressed. |
| `Multi-domain` | Two or more agricultural functions are connected. |
| `Integrated-system` | The MAS represents a broader farm, value-chain, human-water, or social-ecological system. |
| `UNC` | Scope cannot be determined reliably. |

---

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

---

## `Implementation_Maturity`

| Value | Definition |
|---|---|
| `Conceptual` | Proposed model or architecture without substantive experimental implementation. |
| `Simulation` | Evaluated primarily through simulation. |
| `Prototype` | Implemented prototype or proof of concept. |
| `Controlled experiment` | Evaluated in laboratory or controlled conditions. |
| `Field pilot` | Tested in an agricultural field/farm setting on a limited scale. |
| `Operational` | Used in a real operational environment. |

Use the highest maturity level demonstrated in the publication.

---

# RQ1 — Agents, Architecture, and Decision-Making

## `MAS_Architecture`

| Value | Definition |
|---|---|
| `Centralised` | A central agent/controller makes or coordinates the main system decisions. |
| `Decentralised` | Decision authority is distributed among agents without a dominant central controller. |
| `Distributed` | Computation or decision-making is explicitly decomposed across multiple interacting agents/components. |
| `Hierarchical` | Agents operate at explicitly different control or decision levels. |
| `Hybrid` | Centralised/hierarchical and decentralised or distributed components are combined. |
| `UNC` | Architecture cannot be determined reliably. |

---

## `Agent_Paradigm`

Use only when identifiable from the publication:

- `Reactive`
- `Rule-based`
- `Utility-based`
- `BDI`
- `Learning-based`
- `LLM-based`
- `Hybrid`
- `Other`
- `NR`

Do not infer a formal paradigm from general agent behaviour alone.

For example, optimisation of an objective function does not automatically mean that the system implements a formal utility-based agent architecture.

---

## Multiple Agent Levels

If a publication contains different kinds of agents at different system levels, distinguish them explicitly within `Agent_Types` and `Agent_Roles`.

Example:

```text
Decision-support agents: Supervisor; Research; Simulation
Domain/simulation agents: Cow agents
```

Do not treat different agent levels as equivalent unless the publication does so.

---

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
- `LLM-based reasoning`
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

Do not code simple message exchange or bidding as `Negotiation` unless agents actively bargain, bid competitively, propose/counter-propose, or use an explicit negotiation mechanism.

---

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
- `Shared-state coordination`
- `Environment-mediated coordination`
- `Other`

Use the terminology reported by the authors where possible.

---

## `Communication_Mechanism`

Communication may be:

- `Direct/message-based`
- `Peer-to-peer`
- `Shared-state/blackboard`
- `Environment-mediated/indirect`
- `Market/bid-based`
- `Other`
- `NR`

Direct agent-agent messaging is not required for coordination. Interaction may instead occur through a shared environment, shared system state, market, or central coordination mechanism.

---

## `Resource_Scarcity_or_Constraint_Modelled`

| Value | Definition |
|---|---|
| `Yes` | Limited resource availability, capacity, competition, or scheduling constraints are explicitly represented. |
| `No` | The resource/task is modelled without meaningful scarcity or capacity constraints. |
| `NA` | No resource or task-allocation problem is involved. |
| `UNC` | Constraint handling cannot be determined reliably. |

Scarcity does not have to mean physical shortage alone. Limited machine capacity, scheduling capacity, or competing demands may also qualify.

---

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
- `Task completion`
- `Response quality`
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
| `Not addressed` | No substantive sustainability or environmental outcome is investigated. |

Do not classify a study as `Direct` only because terms such as *sustainable*, *green*, or *smart agriculture* appear in the introduction.

---

## `Quantitative_Results`

Record key agricultural, livestock, resource-efficiency, or environmental results using the original values and units reported by the authors.

Example:

```text
Water use reduced by 18% compared with baseline.
```

Do not normalise or recalculate results during extraction.

System-performance results such as routing accuracy, algorithm accuracy, latency, or ablation performance should instead be recorded under `Evaluation_Results`.

---

## `Tradeoffs_Reported`

Record only trade-offs explicitly analysed or discussed by the authors.

Examples:

```text
Water saving vs crop yield
Cost vs animal welfare
Energy use vs productivity
Accuracy vs computational latency
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

A real-world case-study setting or use of real historical data does not automatically mean that the MAS itself was deployed in the real world.

---

## `Real_World_Deployment`

| Value | Definition |
|---|---|
| `Yes` | The complete system was used or evaluated in an actual operational agricultural environment. |
| `Partial` | Some real-world components were used, but the complete MAS was not operationally deployed. |
| `No` | Evaluation was simulation-, laboratory-, model-, or prototype-based only. |
| `UNC` | Deployment status is unclear. |

---

## `Code_Available` / `Data_Available`

Use:

- `Yes`
- `No`
- `NR`

Use `Yes` only when the publication provides or clearly identifies accessible code or data.

Use `NR` when availability cannot be established from the publication.

---

## `Evaluation_Results`

Record key MAS/system-level evaluation findings that are not agricultural, livestock, resource-efficiency, or environmental outcomes.

Examples include:

```text
Routing accuracy = 100%
Task success = 85%
RMSE = 0.42
Average query latency = 58 s
Proposed method outperformed baseline X
```

Baseline and ablation results may also be recorded here.

Do not duplicate agricultural or environmental outcomes already recorded under RQ3.

---

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
- `Data quality/representativeness`
- `Other`

Categories should be assigned only when the limitation is explicitly reported or clearly supported by the study design.

---

## `Reported_Limitations`

Record the authors' stated limitations in concise paraphrased form.

Do not reproduce long passages from the publication.

---

## `Reported_Research_Gaps`

Record explicitly stated future work, unresolved problems, or research gaps.

Do not create speculative research gaps during extraction.

Cross-study gaps will be identified later during synthesis.

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

The codebook was tested on three deliberately different included publications covering:

- distributed resource allocation and irrigation;
- reinforcement-learning water management;
- LLM-based livestock decision support.

Pilot testing resulted in minor clarifications to:

- MAS architecture;
- agent paradigm;
- indirect/shared-state communication;
- multiple agent levels;
- separation of RQ3 outcomes from system-level evaluation results.

**Version 1.0 is now frozen and will be applied consistently to all 34 included publications.**
