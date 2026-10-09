# Multi-Agent Systems for Sustainable Smart Farming

## A Systematic Literature Review of Cooperative Irrigation, Resource Allocation, Livestock Management, and Environmental Sustainability

This repository contains the materials, methodology, data extraction, analysis, and results for a **Systematic Literature Review (SLR)** on the use of **Multi-Agent Systems (MAS) in Sustainable Smart Farming**.

The project focuses on how autonomous and heterogeneous agents are used to support agricultural decision-making involving:

* irrigation and water management;
* crop management;
* livestock management and welfare;
* shared-resource allocation;
* agent communication and coordination;
* cooperation and negotiation;
* environmental sustainability.

---


## Current Review Status

**Last updated: 9 October 2026**

The primary database-search pathway initially produced **34 included publications**.

A subsequent one-generation backward and forward citation search identified **24 additional unique candidate records**. After supplementary screening:

- 3 records were excluded at title/abstract screening;
- 21 reports were sought for full-text retrieval;
- 1 report could not be retrieved;
- 20 reports were assessed at full text;
- 1 report was excluded after full-text assessment;
- 19 additional publications were included.

The current working review corpus therefore contains:
34 publications from the primary database-search pathway + 19 publications identified through citation searching = 53 included publications

---


## 1. Background and Motivation

Modern agriculture involves several interconnected decision-making processes. Crop irrigation, livestock water demand, weather variability, energy consumption, and resource availability cannot always be treated independently.

For example:

* several crop zones may require irrigation simultaneously;
* livestock may compete with crops for limited water resources;
* droughts and heatwaves may increase resource demand;
* rainfall forecasts may reduce or postpone irrigation requirements;
* farming decisions may influence water consumption, energy use, greenhouse-gas emissions, soil quality, and ecosystem impacts.

These characteristics make agriculture a suitable application domain for **Multi-Agent Systems**, where autonomous agents can perceive local conditions, maintain individual goals or states, communicate with one another, cooperate, negotiate, and coordinate decisions.

Existing studies address areas such as smart irrigation, water allocation, intelligent crop management, livestock monitoring, and agricultural decision support. However, these areas are often investigated separately.

This SLR therefore examines MAS research from an **integrated farm-level perspective**.

---

## 2. Main Research Question

> **How have Multi-Agent Systems been designed, implemented, and evaluated for coordinated decision-making in smart agriculture, particularly for irrigation, shared-resource allocation, livestock management, and environmental sustainability?**
---

## 3. Review Objectives

The review aims to:

1. identify how Multi-Agent Systems are currently used in smart agriculture;
2. classify the types and roles of agricultural agents;
3. analyse agent architectures and decision-making mechanisms;
4. investigate communication, cooperation, coordination, and negotiation between agents;
5. examine how MAS handle scarce and competing resources;
6. study irrigation and water-allocation approaches under water scarcity;
7. analyse MAS and intelligent-agent approaches for livestock management and welfare;
8. investigate how environmental sustainability is considered;
9. compare different coordination and decision-making strategies;
10. identify common datasets, simulation environments, evaluation metrics, and deployment approaches;
11. identify limitations and open research gaps in the existing literature.

---

## 4. Main Review Dimensions

The literature is analysed through the following connected dimensions:

```text
Agent Architecture
        ↓
Communication & Coordination
        ↓
Resource Management
        ↓
Agricultural Outcomes
        ↓
Environmental Outcomes
```

A typical MAS decision cycle is considered as:

```text
Environment / Sensors
        ↓
Agent Perception
        ↓
Local State / Beliefs
        ↓
Need / Goal / Utility Assessment
        ↓
Agent Communication
        ↓
Coordination / Negotiation
        ↓
Resource Allocation / Action
        ↓
Farm + Environmental Outcomes
        ↓
Updated Environment
```

---

## 5. Agricultural MAS Scope

The review considers systems containing roles such as:

```text
                       Farm-Management Agent
                                │
              ┌─────────────────┼─────────────────┐
              │                 │                 │
              ▼                 ▼                 ▼
        Weather Agent     Water / Resource    Livestock Agent
                               Agent
                                │
                   ┌────────────┼────────────┐
                   ▼            ▼            ▼
               Crop /       Crop /       Crop /
               Field A      Field B      Field C
                Agent        Agent        Agent
```

The purpose of this architecture is not to assume that every reviewed system contains all these agents. Instead, it provides a conceptual framework for identifying:

* which agent types appear in existing research;
* which agricultural components are integrated;
* how agents interact;
* which components are typically studied separately.

---

## 6. Topics of Interest

### Agent Architecture

The review considers approaches including:

* reactive agents;
* rule-based agents;
* utility-based agents;
* BDI agents;
* hierarchical MAS;
* distributed MAS;
* planning and optimisation;
* model-predictive control;
* machine learning;
* reinforcement learning;
* multi-agent reinforcement learning;
* emerging LLM-based agent systems.

### Agent Interaction

The review investigates:

* communication;
* cooperation;
* coordination;
* negotiation;
* task allocation;
* conflict resolution;
* resource requests and offers;
* auction mechanisms;
* priority-based allocation;
* utility-based allocation;
* contract-net-style mechanisms.

### Agricultural Resources

Resources may include:

* water;
* irrigation capacity;
* feed;
* pasture;
* energy;
* agricultural land;
* machinery;
* other shared farm resources.

### Irrigation Decision Variables

Irrigation-related studies are also analysed according to the information used by agents when making water-allocation decisions, including:

* **soil moisture**;
* **crop water demand and crop requirements**;
* rainfall and rainfall forecasts;
* drought conditions;
* **reservoir availability and current water capacity**;
* irrigation capacity;
* crop stress and urgency.

This helps identify how MAS integrate environmental sensing, crop requirements, and water availability when coordinating irrigation decisions.

---

## 7. Environmental Sustainability

Environmental sustainability is treated as a major review dimension rather than as a separate secondary topic.

The review investigates whether MAS approaches model, evaluate, or attempt to reduce:

* freshwater consumption;
* water scarcity;
* inefficient irrigation;
* greenhouse-gas emissions;
* CO₂ emissions;
* livestock methane emissions;
* manure-related emissions;
* N₂O associated with agricultural activities;
* farm and irrigation energy consumption;
* fertiliser use;
* nutrient runoff;
* water pollution;
* soil degradation;
* soil-health impacts;
* land and pasture pressure;
* wider ecosystem impacts.

### Environmental Mitigation Mechanisms

The review also investigates how agents are used to actively reduce environmental impacts through mechanisms such as:

* **precision irrigation**;
* **demand-aware water allocation**;
* **efficient livestock feeding strategies**;
* **manure management**;
* **fertiliser and nutrient management**;
* **renewable-energy scheduling**;
* **pasture and grazing management**;
* **carbon-aware decision-making**;
* energy-efficient farm-resource scheduling.

The review additionally examines how MAS handle trade-offs between:

```text
Productivity
     +
Animal Welfare
     +
Resource Efficiency
     +
Environmental Sustainability
```

---

## 8. Systematic Review Methodology

The review follows a predefined and reproducible protocol and uses **PRISMA 2020** principles for reporting study identification, screening, eligibility, and inclusion.

### Publication Period

```text
2010–2026
```

Earlier foundational work may be identified through backward citation searching where relevant.

### Primary Databases

The final primary database search was conducted using:

* Scopus;
* Web of Science Core Collection;
* IEEE Xplore;
* ScienceDirect;
* SpringerLink.

ACM Digital Library was originally planned but was removed from the primary database set because the available interface did not support a reproducible implementation of the frozen title/abstract search strategy. The decision is documented in `protocol/protocol_notes.md`.

### Supplementary Citation Searching

After the initial database-screening phase, one generation of supplementary backward and forward citation searching was conducted from the initially included publications.

Backward searching used the reference lists of included publications. Forward searching used publicly accessible citation-index, publisher, and web citation information.
The supplementary search identified 24 new records that were screened using the same predefined eligibility criteria as the primary database records.

Earlier publications outside the primary 2010–2026 search window were eligible only under the predefined IC7 foundational-study exception.

---

## 9. Search Strategy

A conceptual master search strategy combines three main groups:

```text
MULTI-AGENT SYSTEMS
        AND
AGRICULTURE / FARMING
        AND
COORDINATION / RESOURCE MANAGEMENT / SUSTAINABILITY
```

Indicative terms include:

```text
("multi-agent system*" OR
 "multi agent system*" OR
 "multi-agent" OR
 "intelligent agent*" OR
 "agent-based decision*")

AND

(agricultur* OR
 farm* OR
 "smart farm*" OR
 "precision agriculture" OR
 irrigation OR
 livestock OR
 "precision livestock")

AND

(coordination OR
 cooperation OR
 negotiation OR
 "resource allocation" OR
 decision* OR
 water OR
 sustainab* OR
 environment*)
```

The exact query syntax is adapted for each database.

For example, where wildcard restrictions apply:

```text
sustainab*
```

may be expanded to:

```text
(sustainability OR sustainable)
```

The exact search string, database, search date, search fields, and retrieved record count will be documented for reproducibility.

---

## 10. Screening Strategy

If the initial **deduplicated corpus exceeds approximately 100 records**, the search will be refined to the closest available equivalents of:

```text
Title
Abstract
Keywords
```

while retaining the same conceptual search terms.

### General Inclusion Criteria

Studies are considered when they:

* concern agriculture, farming, irrigation, or livestock;
* involve multiple interacting or autonomous agents;
* describe a MAS or meaningful agent-based decision architecture;
* address coordination, cooperation, negotiation, decision-making, or resource allocation;
* provide sufficient methodological information;
* are peer-reviewed research papers or conference papers;
* are available in English.

### General Exclusion Criteria

Studies may be excluded when they:

* only perform IoT monitoring;
* use conventional machine learning without meaningful agent interaction;
* only collect sensor data without coordinated decision-making;
* do not concern an agricultural domain;
* do not provide sufficient methodological information.

---

## 11. Review Workflow

```text
Research Questions & Protocol
        ↓
Primary Database Searches
        ↓
Export and Merge Records in Rayyan
        ↓
Cross-Database Deduplication
        ↓
Title / Abstract Screening
        ↓
Full-Text Retrieval and Screening
        ↓
34 Initially Included Publications
        ↓
One-Generation Backward / Forward Citation Searching
        ↓
24 New Citation-Search Records
        ↓
Supplementary Screening and Full-Text Assessment
        ↓
19 Additional Included Publications
        ↓
53-Publication Working Corpus
        ↓
Structured Data Extraction + Quality Assessment
        ↓
Study-Family Reconciliation
        ↓
Descriptive Analysis + RQ0–RQ4 Synthesis
        ↓
Taxonomy / Evidence Mapping
        ↓
Research Gaps
        ↓
PRISMA 2020 Reporting
        ↓
Final Report and Presentation
```

---

## 12. Reference Management and PRISMA Workflow

Two complementary tools are used.

### Rayyan

Rayyan is used for the systematic-review workflow:

* importing database records;
* duplicate identification;
* title and abstract screening;
* full-text screening;
* inclusion/exclusion decisions;
* exclusion reasons;
* PRISMA-related study counts.

### Zotero

Zotero is used as the reference-management system for:

* organising included literature;
* storing PDFs;
* managing bibliographic metadata;
* research notes and annotations;
* citation management;
* bibliography generation.

The main screening and deduplication record is maintained in **Rayyan** to avoid inconsistent PRISMA counts across multiple applications.

---

## 13. Quality Assessment

Included studies are assessed according to criteria such as:

* clarity of research objectives;
* clarity of agent roles and autonomy;
* specification of communication mechanisms;
* specification of coordination or negotiation mechanisms;
* description of the agricultural environment;
* description of datasets or simulation data;
* quality of experimental evaluation;
* reproducibility;
* acknowledgement of limitations.

---

## 14. Data Extraction

A structured extraction dataset is maintained for the included studies.

Typical fields include:

| Category                 | Examples                                                                                                  |
| ------------------------ | --------------------------------------------------------------------------------------------------------- |
| Agricultural domain      | Irrigation, crops, livestock, mixed farming                                                               |
| Agent types              | Crop, weather, livestock, water, manager                                                                  |
| Agent architecture       | Reactive, BDI, utility, hierarchical, distributed                                                         |
| Coordination             | Cooperation, negotiation, auction, contract-net                                                           |
| AI technique             | Rules, optimisation, ML, RL/MARL, MPC, LLM                                                                |
| Resources                | Water, feed, energy, pasture, land, machinery                                                             |
| Environmental conditions | Drought, heatwave, rainfall, scarcity                                                                     |
| Deployment               | Simulation, IoT, cyber-physical, field deployment                                                         |
| Agricultural outcomes    | Yield, crop stress, livestock welfare                                                                     |
| Sustainability outcomes  | Water, GHG, energy, soil, pollution                                                                       |
| Evaluation               | Dataset, metrics, baselines, scenarios                                                                    |
| Limitations              | Scalability, uncertainty, **explainability**, interoperability, environmental modelling, deployment, cost |

---

## 15. Analysis and Synthesis

The literature is compared across four broad classes of coordination:

1. **Independent / decentralised decision-making**
2. **Centralised / hierarchical coordination**
3. **Cooperative / negotiated multi-agent allocation**
4. **Learning / adaptive approaches**

The review considers reported outcomes such as:

* water-use efficiency;
* unmet resource demand;
* crop yield and crop stress;
* livestock welfare and heat stress;
* resource conflicts;
* allocation fairness;
* overall farm utility;
* economic outcomes;
* communication overhead;
* computational requirements;
* energy consumption;
* greenhouse-gas reduction;
* pollution reduction;
* soil and land impacts.

Where quantitative results are sufficiently comparable, they will be summarised descriptively.

Due to expected differences between agricultural domains, MAS architectures, datasets, and metrics, the primary synthesis will use:

* structured thematic analysis;
* evidence mapping;
* taxonomy construction;
* comparative analysis.

---

## 16. Agricultural Scenarios of Interest

The review pays particular attention to research studying situations such as:

```text
Normal Conditions
        │
Water Scarcity
        │
Severe Drought
        │
Heatwaves
        │
Unexpected Rainfall
        │
Crop–Livestock Resource Competition
        │
Environmental Resource Constraints
```

These scenarios are particularly relevant when analysing coordination and shared-resource allocation between autonomous agricultural agents.

---

## 17. Expected Outcomes

The project is expected to produce:

* a reproducible SLR of MAS in smart agriculture;
* a taxonomy of agricultural agents and MAS architectures;
* a classification of coordination and negotiation mechanisms;
* analysis of irrigation and shared-water allocation;
* synthesis of MAS approaches to livestock management;
* an environmental-sustainability evidence map;
* comparison of decentralised, centralised, cooperative, and adaptive approaches;
* identification of commonly used datasets and simulations;
* classification of evaluation metrics;
* analysis of real-world versus simulated deployment;
* identification of methodological and technical limitations;
* identification of open research gaps.

---

## 18. Repository Structure

```text
Multi-Agent-Systems-for-Sustainable-Smart-Farming/
│
├── README.md
│
├── proposal/
│   └── Project_Proposal.pdf
│
├── protocol/
│   ├── ProjectScope_Extended.pdf
│   ├── research_questions.md
│   ├── inclusion_exclusion.md
│   ├── quality_assessment.md
│   └── protocol_notes.md
│
├── searches/
│   ├── master_search_strategy.md
│   ├── scopus/
│   ├── web_of_science/
│   ├── ieee_xplore/
│   ├── science_direct/
│   └── springer_link/
│
├── rayyan/
│   └── cross_database_deduplication.md
│
├── citation_chasing/
│   ├── citation_chasing_log.md
│   ├── citation_chasing_log.csv
│   ├── citation_chasing_dedup_log.md
│   ├── citation_chasing_log_deduplicated.csv
│   ├── citation_chasing_fulltext_screening_batch1.csv
│   ├── citation_chasing_fulltext_screening_batch2.csv
│   ├── citation_chasing_fulltext_screening_batch3.csv
│   ├── citation_chasing_screening_final.csv
│   └── citation_chasing_screening_final_summary.md
│
├── data_extraction/
│   ├── data_extraction_schema.md
│   ├── extraction_codebook.md
│   ├── extraction_template_updated6(final).csv
│   └── quality_assessment_updated6(final).csv
│
└── analysis/
    ├── descriptive_analysis.md
    ├── rq0_synthesis.md
    ├── rq1_synthesis.md
    ├── rq2_synthesis.md
    ├── rq3_synthesis.md
    ├── rq4_synthesis.md
    ├── integrated_results_synthesis.md
    └── slr_descriptive_analysis.xlsx
```

The exact repository structure may evolve as the review progresses.

---

## 19. Single-Reviewer Consideration

This SLR is conducted by a single researcher.

Single-reviewer screening is therefore recognised as a methodological limitation. To improve transparency and consistency:

* inclusion and exclusion criteria are predefined;
* criteria are piloted before full screening;
* exclusion reasons are recorded;
* ambiguous studies are reconsidered during full-text assessment;
* screening decisions are maintained in Rayyan;
* selected records may be re-screened to check intra-reviewer consistency.

---

## 20. Project Timeline

### September 2026

* finalise the SLR protocol;
* finalise research questions;
* pilot database-specific searches;
* execute database searches;
* export records;
* merge records in Rayyan;
* deduplicate studies;
* begin title/abstract screening.

### October 2026

* complete title/abstract screening;
* complete full-text screening;
* record exclusion reasons;
* perform quality assessment;
* complete structured data extraction;
* construct the MAS taxonomy;
* perform evidence synthesis;
* analyse environmental sustainability;
* identify research gaps;
* complete PRISMA documentation;
* prepare the final report and presentation.
