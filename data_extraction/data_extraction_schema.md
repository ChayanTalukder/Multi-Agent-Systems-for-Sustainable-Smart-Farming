# Data Extraction Schema

## Version

**Version:** 1.0 — Frozen  
**Date:** 3 October 2026  
**Extraction status:** S01–S34 complete; S35–S53 added following supplementary citation searching and pending full structured extraction.

---

# Purpose

This file defines the structured data-extraction schema for the Systematic Literature Review (SLR) on **Multi-Agent Systems (MAS) for sustainable smart farming**.

The schema is designed to support the review objective and Research Questions **RQ0–RQ4** defined in `protocol/research_questions.md`.

The extraction framework follows the main analytical chain of the review:

**Agent Architecture → Communication and Coordination → Resource Management → Agricultural/Livestock/Environmental Outcomes → Evaluation and Research Gaps**

The schema will be applied consistently to all studies included after full-text screening.

The current working full-text corpus contains **53 included publications**: 34 identified through the primary database-search pathway and 19 additional publications identified through supplementary citation searching.

---

# Research-Question Alignment

The extraction schema is organised around the following research questions.

## RQ0 — Primary Research Question

**How have Multi-Agent Systems been designed, implemented, and evaluated for coordinated decision-making in smart agriculture, particularly for irrigation, shared-resource allocation, livestock management, and environmental sustainability?**

RQ0 provides the overall synthesis framework and is supported by RQ1–RQ4.

## RQ1 — MAS Architectures, Agent Roles, and Decision-Making

**What types of agents, architectures, and decision-making approaches are used in Multi-Agent Systems for smart agriculture?**

## RQ2 — Coordination, Negotiation, and Shared-Resource Management

**How do agricultural agents communicate, coordinate, cooperate, or negotiate when managing shared and limited farm resources?**

## RQ3 — Agricultural, Livestock, Resource, and Environmental Outcomes

**What agricultural, livestock-welfare, resource-efficiency, and environmental outcomes are reported for MAS-based smart-farming approaches?**

## RQ4 — Evaluation, Limitations, and Research Gaps

**How are agricultural Multi-Agent Systems evaluated, and what methodological, technical, and practical limitations or research gaps are reported in the literature?**

---

# Unit of Extraction

The primary unit of extraction is the **included publication**.

Each included publication receives one row in the main extraction dataset. The current corpus contains 53 publications.

Each publication will be assigned a unique identifier:

```text
S01
S02
S03
...
S53
```

Related publications will not automatically be merged during extraction.

When two or more publications are confirmed to report the same underlying system, experiment, dataset, or research programme, they will be assigned a common `Study_Family_ID`.

This allows each publication to remain traceable while reducing the risk of treating overlapping results as completely independent evidence during synthesis.

Similarity of titles alone is not sufficient to assign publications to the same study family. Relationships must be confirmed from the full texts, authorship, methodology, system description, dataset, experiments, or explicit references to earlier/extended work.

---

# General Extraction Rules

The same extraction fields and coding rules will be applied to every included publication.

## Missing and Non-Applicable Information

The following codes will be used:

| Code | Meaning |
|---|---|
| `NR` | Not reported in the publication |
| `NA` | Not applicable to the publication |
| `UNC` | Relevant information is present but remains unclear or ambiguous after full-text inspection |

Empty cells should be avoided.

A value of `No` should only be used when absence can reasonably be established. It should not be used simply because information was not reported.

---

## Multiple Values

Where a field contains multiple applicable values, entries will be separated using a semicolon:

```text
Water; Energy; Machinery
```

The detailed controlled vocabulary for categorical fields will be defined in `extraction_codebook.md`.

---

## Author-Reported Information vs Reviewer Coding

Extraction should distinguish between:

1. information explicitly reported by the authors; and
2. structured classifications assigned by the reviewer using the predefined codebook.

Reviewer interpretation should remain conservative and should not attribute mechanisms, outcomes, or limitations that are not supported by the publication.

For example, exchange of messages between agents should not automatically be coded as negotiation unless negotiation is explicitly described or clearly implemented.

---

## Numerical Results

Quantitative findings will initially be recorded using the values and units reported in the publication.

For example:

```text
Water consumption reduced by 23%
```

or:

```text
Yield increased from 4.1 to 4.7 t/ha
```

Values will not be normalised or transformed during the initial extraction stage.

Any later harmonisation or derived calculations will be performed during synthesis and documented separately.

---

## Evidence Traceability

Important RQ1–RQ4 extraction decisions should be linked to their location in the full text.

Evidence locators may use:

```text
p. 6
pp. 6–8
Section 3.2
Table 4
Figure 5
pp. 7–8; Section 4.1
```

Where page numbers are unavailable or unreliable, section, table, or figure identifiers should be used.

Evidence locators are intended to support later verification and report writing. They are not intended to contain long quotations.

---

# A. Study Identification and Descriptive Metadata

These fields identify each publication and describe its agricultural context.

| Field | Type | Description |
|---|---|---|
| `Study_ID` | Identifier | Unique SLR identifier assigned to the publication, e.g. `S01`–`S53`. |
| `Rayyan_ID` | Identifier | Rayyan record identifier from the final included-study export. |
| `PDF_Filename` | Text | Filename of the full-text PDF used for extraction. |
| `Title` | Text | Full publication title. |
| `Authors` | Text | Authors as recorded in the bibliographic metadata. |
| `Year` | Integer | Publication year. |
| `Venue` | Text | Journal, conference, book, or other publication venue. |
| `Publication_Type` | Categorical | Publication type, such as journal article, conference paper, or book chapter. |
| `DOI` | Text | Normalised DOI where available; otherwise `NR`. |
| `Geographical_Context` | Text / categorical | Country, region, farming area, or geographical setting studied, where applicable. |
| `Agricultural_Domain` | Multi-value categorical | Main agricultural context of the study, such as irrigation/water management, crops, livestock/dairy, greenhouse management, farm energy, workforce/harvesting, manure/nutrient management, land use, social-ecological systems, value chains, or integrated farming. |
| `Study_Objective` | Short text | Concise summary of the research problem or objective addressed by the publication. |
| `Study_Family_ID` | Identifier | Identifier linking publications confirmed to belong to the same research/system/experimental family. Publications without confirmed related papers receive their own family identifier. |
| `Related_Publication_IDs` | Multi-value identifier | Other included `Study_ID` values confirmed to be related to the same system, experiment, dataset, or research programme; otherwise `NA`. |

---

# B. RQ0 — Overall MAS Application and Scope

RQ0 provides the overall picture of how MAS are used in smart agriculture.

The following fields capture the purpose, scope, contribution, and implementation maturity of each system.

| Field | Type | Description |
|---|---|---|
| `MAS_Application_Purpose` | Short text | Concise description of what the MAS is intended to accomplish in the agricultural system. |
| `System_Integration_Scope` | Categorical | Whether the system addresses a single agricultural function, multiple connected functions, or a broader integrated farm/social-ecological system. |
| `Contribution_Type` | Multi-value categorical | Main contribution of the publication, such as MAS architecture, algorithm, simulation model, decision-support framework, coordination mechanism, optimisation method, control system, or implemented platform. |
| `Implementation_Maturity` | Categorical | Stage at which the proposed MAS is demonstrated, such as conceptual/model-level, simulation, prototype, controlled experiment, field pilot, or operational deployment. |

RQ0 will primarily be synthesised using these fields together with the more detailed evidence extracted for RQ1–RQ4.

---

# C. RQ1 — MAS Architectures, Agent Roles, and Decision-Making

RQ1 examines how agricultural MAS are structured and what forms of intelligence and autonomy are used.

| Field | Type | Description |
|---|---|---|
| `Agent_Types` | Multi-value text/categorical | Types of agents represented in the system, such as farmer, crop, field, irrigation, water/resource, livestock, pasture, sensor, machinery, energy, market, coordinator, or environmental agents. |
| `Agent_Roles` | Structured text | Main responsibilities and functions assigned to the identified agents. |
| `MAS_Architecture` | Categorical | Overall organisational architecture of the MAS, such as centralised, decentralised, distributed, hierarchical, or hybrid. |
| `Agent_Paradigm` | Multi-value categorical | Agent design paradigm where identifiable, such as reactive, rule-based, utility-based, BDI, learning-based, or other explicitly described architecture. |
| `Decision_Mechanism` | Multi-value categorical/text | Main mechanism used by agents to make decisions, such as rules, optimisation, planning, machine learning, reinforcement learning, MARL, MPC, auction-based decision making, or hybrid methods. |
| `Agent_Autonomy_Description` | Short text | Description of what decisions agents can make independently and where central or external control remains. |
| `Input_Information` | Multi-value text | Information used by agents for decision-making, such as sensor measurements, weather, soil moisture, crop demand, prices, livestock state, resource availability, or forecasts. |
| `MAS_Platform_Technology` | Multi-value text | Implementation or simulation technologies reported, such as JADE, GAMA, MATLAB, Python, custom MAS platforms, IoT infrastructure, or other frameworks. |
| `RQ1_Evidence_Locator` | Text | Page, section, table, or figure locations supporting the main RQ1 extraction. |

---

# D. RQ2 — Communication, Coordination, Negotiation, and Resource Management

RQ2 examines how agents interact when making coordinated decisions or managing shared and constrained resources or tasks.

This section includes both physical resources and coordination problems such as workforce or agricultural task allocation.

| Field | Type | Description |
|---|---|---|
| `Interaction_Type` | Multi-value categorical | Forms of inter-agent interaction, such as communication, information sharing, cooperation, coordination, negotiation, competition, or task allocation. |
| `Coordination_Mechanism` | Multi-value categorical/text | Mechanism used to coordinate agents, such as priority rules, utility-based allocation, auctions, contract-net protocols, consensus, optimisation, scheduling, market mechanisms, MARL, or other approaches. |
| `Communication_Mechanism` | Multi-value text/categorical | How agents exchange information, such as direct messages, peer-to-peer exchange, agent communication protocols, shared environments, blackboards, markets, or indirect interaction. |
| `Information_Shared` | Multi-value text | Information exchanged among agents, such as resource requests, offers, bids, demand, availability, prices, sensor information, environmental state, or task status. |
| `Managed_Resource_or_Task` | Multi-value categorical/text | Resource or coordination target being managed, such as water, irrigation capacity, energy, feed, pasture, land, manure, machinery, labour/workforce, harvest tasks, or other farm resources/tasks. |
| `Resource_Scarcity_or_Constraint_Modelled` | Categorical | Whether limited availability, capacity, scarcity, competition, scheduling constraints, or comparable resource/task constraints are explicitly represented. |
| `Allocation_or_Coordination_Objective` | Multi-value text/categorical | Objective guiding coordination or allocation, such as efficiency, productivity, cost, profit, fairness, welfare, sustainability, resource utilisation, conflict reduction, or multi-objective optimisation. |
| `Conflict_Resolution` | Short text | Method used to resolve incompatible requests, competing objectives, resource conflicts, or task conflicts; `NR` or `NA` where appropriate. |
| `Competing_Agents_or_Demands` | Short text | Agents, stakeholders, farms, crops, livestock groups, tasks, or other demands competing for limited resources or attention. |
| `Irrigation_Decision_Inputs` | Multi-value text | For irrigation/water studies, information used in irrigation or water-allocation decisions, including soil moisture, crop water requirements, crop stress, rainfall, forecasts, drought, reservoir availability, or irrigation capacity. Use `NA` for non-irrigation studies. |
| `RQ2_Evidence_Locator` | Text | Page, section, table, or figure locations supporting the main RQ2 extraction. |

---

# E. RQ3 — Agricultural, Livestock, Resource-Efficiency, and Environmental Outcomes

RQ3 captures the outcomes reported after applying or evaluating the MAS.

Outcomes should be recorded as reported by the authors and should not be interpreted as improvements unless the study provides an appropriate comparison or other supporting evidence.

| Field | Type | Description |
|---|---|---|
| `Agricultural_Outcomes` | Multi-value text | Reported agricultural outcomes such as crop yield, crop health, crop stress, irrigation performance, production, unmet demand, farm utility, or productivity. |
| `Livestock_Outcomes` | Multi-value text | Reported livestock-related outcomes such as water demand, feed demand, animal health, heat stress, grazing, pasture allocation, welfare, or dairy-farm performance. Use `NA` when livestock is outside the study scope. |
| `Resource_Efficiency_Outcomes` | Multi-value text | Reported effects on water use, irrigation efficiency, energy use, resource utilisation, allocation fairness, workload, scheduling efficiency, or resource conflicts. |
| `Environmental_Outcomes` | Multi-value text | Reported environmental effects such as freshwater consumption, water scarcity, greenhouse-gas emissions, CO₂, CH₄, N₂O, manure impacts, energy consumption, fertiliser use, nutrient runoff, pollution, soil condition, land use, pasture, carbon resources, or ecosystem effects. |
| `Environmental_Mitigation_Mechanism` | Multi-value text | Mechanisms intended to reduce environmental impact, such as precision irrigation, demand-aware allocation, manure management, renewable-energy scheduling, improved feeding, nutrient management, grazing management, or carbon-aware decisions. |
| `Sustainability_Addressed` | Categorical | Degree to which sustainability is substantively addressed: direct, indirect, or not addressed. Detailed coding rules will be defined in the codebook. |
| `Quantitative_Results` | Structured text | Key numerical results relevant to RQ3, recorded with the values, units, and comparison context reported by the authors. |
| `Tradeoffs_Reported` | Multi-value text | Explicitly reported trade-offs between productivity, welfare, cost, resource efficiency, fairness, environmental performance, or other objectives. |
| `RQ3_Evidence_Locator` | Text | Page, section, table, or figure locations supporting the main RQ3 extraction. |

---

# F. RQ4 — Evaluation, Limitations, and Research Gaps

RQ4 captures how each MAS is evaluated and what methodological, technical, and practical limitations remain.

| Field | Type | Description |
|---|---|---|
| `Evaluation_Type` | Multi-value categorical | Main evaluation method, such as simulation, analytical evaluation, case study, controlled experiment, laboratory experiment, field experiment, pilot deployment, or real-world deployment. |
| `Evaluation_Environment` | Short text | Description of the farm, simulation, IoT, laboratory, field, social-ecological, or other environment used for evaluation. |
| `Data_Source` | Multi-value categorical/text | Origin of evaluation data, such as synthetic data, simulation-generated data, real sensor data, farm data, public datasets, historical data, surveys, or mixed sources. |
| `Experimental_Scenarios` | Multi-value text | Scenarios or conditions evaluated, such as normal operation, drought, scarcity, changing demand, uncertain environments, heat stress, different resource levels, or alternative management strategies. |
| `Baselines_Comparators` | Multi-value text | Algorithms, policies, existing practices, non-MAS approaches, control strategies, or other baselines used for comparison. |
| `Evaluation_Metrics` | Multi-value text | Metrics used to assess system or algorithm performance, such as accuracy, reward, latency, task success, computational performance, or other reported evaluation measures. |
| `Evaluation_Results` | Structured text | Key qualitative or quantitative MAS/system-evaluation results, including algorithmic performance, baseline comparisons, or ablation findings that are not agricultural, livestock, resource-efficiency, or environmental outcomes. 
| `Evaluation_Scale` | Short text | Scale of evaluation where reported, such as number of agents, farms, fields, animals, tasks, resources, simulation duration, geographical extent, or number of scenarios. |
| `Real_World_Deployment` | Categorical | Whether the system was evaluated in an actual operational or field setting rather than solely through simulation or synthetic experiments. |
| `Code_Available` | Categorical | Whether implementation/source code is publicly available or explicitly provided. |
| `Data_Available` | Categorical | Whether the dataset or sufficient underlying evaluation data are publicly available or explicitly provided. |
| `Limitation_Categories` | Multi-value categorical | Standardised categories assigned to limitations discussed or clearly evidenced in the publication, including scalability, uncertainty, explainability, interoperability, environmental modelling, computational requirements, reproducibility/data availability, deployment cost, real-world validation/adoption, or other limitations. |
| `Reported_Limitations` | Structured text | Limitations, constraints, or threats to validity explicitly reported by the authors. |
| `Reported_Research_Gaps` | Structured text | Future work, unresolved problems, open challenges, or research gaps explicitly identified by the publication. |
| `RQ4_Evidence_Locator` | Text | Page, section, table, or figure locations supporting the main RQ4 extraction. |

---

# G. General Extraction Notes

| Field | Type | Description |
|---|---|---|
| `Extraction_Notes` | Text | Short reviewer notes for unusual cases, ambiguous classifications, relationships between publications, or extraction decisions that require later verification. |

`Extraction_Notes` should not become a substitute for structured fields. It should only be used when information cannot be adequately represented elsewhere or when an extraction decision requires explanation.

---

# Relationship Between Extraction Fields and Research Questions

```text
Study identification and context
        │
        └── Descriptive characteristics of the 53 included publications

RQ0 — Overall MAS use in sustainable smart farming
        │
        ├── MAS application purpose
        ├── integration scope
        ├── contribution type
        └── implementation maturity

RQ1 — Agents, architecture, and intelligence
        │
        ├── agent types and roles
        ├── MAS architecture
        ├── agent paradigm
        ├── decision mechanisms
        ├── autonomy
        ├── input information
        └── platforms and technologies

RQ2 — Interaction and resource/task coordination
        │
        ├── communication
        ├── cooperation and coordination
        ├── negotiation
        ├── shared information
        ├── resource/task constraints
        ├── allocation mechanisms
        ├── conflict resolution
        └── irrigation/water decision inputs

RQ3 — Outcomes
        │
        ├── agricultural outcomes
        ├── livestock outcomes
        ├── resource efficiency
        ├── environmental outcomes
        ├── mitigation mechanisms
        ├── sustainability
        └── trade-offs

RQ4 — Evaluation and gaps
        │
        ├── evaluation design
        ├── data and scenarios
        ├── baselines and metrics
        ├── evaluation scale
        ├── real-world validation
        ├── code/data availability
        ├── limitations
        └── research gaps
```

---

# Relationship to Quality Assessment

Data extraction and quality assessment are related but separate activities.

The extraction dataset records:

> **What the study did, how the MAS works, how it was evaluated, and what it reported.**

The quality-assessment dataset records:

> **How clearly and adequately the study describes and evaluates that work.**

For example, a publication may report:

```text
Coordination_Mechanism = Contract-net protocol
```

while receiving:

```text
QA3 = 1
```

if the coordination mechanism is mentioned but insufficiently described.

Quality scores therefore must not be inserted into the main data-extraction fields.

QA1–QA7 will be recorded separately in:

```text
data_extraction/quality_assessment_updated6(final).csv
```

according to:

```text
protocol/quality_assessment.md
```

---

# Extraction Procedure

The extraction procedure will be conducted as follows:

1. verify bibliographic metadata and assign permanent `Study_ID` values to all 53 included publications;
2. complete `extraction_codebook.md` to define controlled values and field-specific coding rules;
3. pilot the schema on three deliberately different included publications;
4. review ambiguous, redundant, missing, or impractical fields identified during the pilot;
5. document justified schema/codebook changes;
6. freeze the extraction schema and codebook as **Version 1.0**;
7. extract all 53 included publications using the frozen Version 1.0 framework;
8. perform the QA1–QA7 quality assessment;
9. check the completed datasets for missing values, inconsistent coding, and related-publication overlap;
10. proceed to RQ0–RQ4 synthesis only after the extraction dataset has been validated.

---

# Pilot Testing

The extraction framework was pilot-tested on three deliberately different included publications:

1. **Heterogeneous multi-agent resource allocation through multi-bidding with applications to precision agriculture** — resource allocation, irrigation, distributed optimisation, and multi-bidding.
2. **Assessing Adaptive Irrigation Impacts on Water Scarcity in Nonstationary Environments—A Multi-Agent Reinforcement Learning Approach** — adaptive RL agents, shared water scarcity, and coupled human-water modelling.
3. **CowNet-AI: A Multi-Agent Decision Support Framework for Social Network–Driven Welfare Insights in Dairy Cattle** — LLM-based agents, livestock welfare, explainability, and decision support.

The pilot confirmed that the overall RQ0–RQ4 extraction structure was suitable.

Minor revisions identified during pilot testing were incorporated before freezing Version 1.0.
---

# Schema Stability

Version 1.0 is frozen following completion of the three-study pilot. The extraction fields and coding rules should remain stable throughout extraction of the 53 included publications.

If an unforeseen issue requires a substantive change after extraction has begun:
1. the reason for the change must be documented;
2. the schema/codebook version must be updated;
3. previously extracted studies must be reviewed against the new rule;
4. the change must be applied consistently across the complete dataset.

This avoids applying different extraction criteria to different publications.

---

# Version History

| Date | Version | Change | Reason |
|---|---|---|---|
| 3 Oct 2026 | 0.1 | Initial pre-pilot schema aligned with RQ0–RQ4 and the 34-publication corpus. | Establish the candidate extraction framework. |
| 3 Oct 2026 | 1.0 | Schema frozen after three-study pilot; added `Evaluation_Results`. | Separate system/algorithm evaluation findings from agricultural and sustainability outcomes. |
| 9 Oct 2026 | 1.0 | Working corpus extended from 34 to 53 included publications following supplementary citation searching. Study IDs S35–S53 were added; no extraction fields or coding rules were changed. | Preserve the frozen post-pilot schema while incorporating supplementary-search inclusions. |
---

# Current Status
**Full-text screening:** Complete  
**Included publications:** 53
**Corpus verification:** Complete  
**Three-study extraction pilot:** Complete  
**Data-extraction schema:** Version 1.0 — Frozen  
**Extraction codebook:** Version 1.0 — Frozen  
**Next step:** Complete extraction and quality assessment for S35–S53 using the frozen Version 1.0 schema, then reconcile study families across the complete 53-publication corpus.
