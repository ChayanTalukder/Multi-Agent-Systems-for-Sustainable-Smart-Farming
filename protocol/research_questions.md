# Review Objective

The objective of this **Systematic Literature Review (SLR)** is to systematically identify, classify, and critically analyse existing research on **Multi-Agent Systems (MAS) for agricultural decision-making**.

The review focuses on the use of autonomous and interacting agents in smart farming, with particular attention to:

- crop and irrigation management;
- shared-resource allocation;
- agent communication, cooperation, coordination, and negotiation;
- livestock management and welfare;
- environmental sustainability;
- evaluation methods, practical limitations, and open research gaps.

The literature will be analysed through the following connected dimensions:

**Agent Architecture → Communication and Coordination → Resource Management → Agricultural Outcomes → Environmental Outcomes**

---

# Research Questions

## RQ0 — Primary Research Question

**How have Multi-Agent Systems been designed, implemented, and evaluated for coordinated decision-making in smart agriculture, particularly for irrigation, shared-resource allocation, livestock management, and environmental sustainability?**

This question provides the overall framework for the review and is supported by the secondary research questions below.

---

## Secondary Research Questions

## RQ1 — MAS Architectures, Agent Roles, and Decision-Making

**What types of agents, architectures, and decision-making approaches are used in Multi-Agent Systems for smart agriculture?**

The review will investigate aspects such as:

- weather agents;
- water/resource agents;
- crop or field agents;
- livestock agents;
- pasture agents;
- sensor agents;
- machinery agents.

Relevant architectural and decision-making approaches may include:

- reactive agents;
- rule-based agents;
- utility-based agents;
- Belief-Desire-Intention (BDI) architectures;
- hierarchical MAS;
- distributed MAS;
- planning and optimisation;
- machine learning;
- reinforcement learning;
- Multi-Agent Reinforcement Learning (MARL);
- Model Predictive Control (MPC);
- emerging LLM-based agent approaches.

This question will help identify how agricultural MAS are structured and what forms of intelligence are used by the agents.

---

## RQ2 — Coordination, Negotiation, and Shared-Resource Management

**How do agricultural agents communicate, coordinate, cooperate, or negotiate when managing shared and limited farm resources?**

The review will investigate mechanisms including:

- message exchange, information sharing;
- cooperation, coordination, negotiation;
- task allocation;
- conflict resolution;
- distributed decision-making;
- priority-based allocation;
- utility-based allocation;
- auction mechanisms;
- contract-net mechanisms;
- optimisation-based resource allocation.

The shared resources considered may include:

- water;
- irrigation capacity;
- feed;
- pasture;
- energy;
- agricultural land;
- machinery;
- other farm resources.

Particular attention will be given to irrigation and water scarcity, including how systems use information such as:

- soil moisture;
- crop water requirements;
- crop stress;
- rainfall and rainfall forecasts;
- drought conditions;
- reservoir availability;
- irrigation capacity.

This question will examine situations where crop and livestock agents compete for limited resources.

---

## RQ3 — Agricultural, Livestock, Resource, and Environmental Outcomes

**What agricultural, livestock-welfare, resource-efficiency, and environmental outcomes are reported for MAS-based smart-farming approaches?**

The review will investigate agricultural outcomes such as:

- crop yield;
- crop health;
- crop stress;
- irrigation performance;
- unmet resource demand;
- overall farm utility or productivity.

Livestock-related outcomes may include:

- water demand;
- feed demand;
- heat stress;
- animal health;
- grazing and pasture allocation;
- animal welfare.

Resource-efficiency outcomes may include:

- water-use efficiency;
- irrigation efficiency;
- energy efficiency;
- resource-allocation fairness;
- reduction in resource conflicts.

Environmental outcomes may include:

- freshwater consumption;
- water scarcity;
- greenhouse-gas emissions;
- CO₂ emissions;
- CH₄ emissions;
- livestock methane;
- manure-related emissions;
- N₂O emissions;
- farm and irrigation energy consumption;
- fertiliser use;
- nutrient runoff;
- water pollution;
- soil degradation;
- soil health;
- land and pasture impacts;
- ecosystem impacts.

The review will also examine environmental mitigation approaches such as:

- precision irrigation;
- demand-aware water allocation;
- efficient livestock feeding;
- manure management;
- fertiliser and nutrient management;
- renewable-energy scheduling;
- pasture and grazing management;
- carbon-aware decision-making;
- energy-efficient farm-resource scheduling.

Where relevant, the review will examine trade-offs between:

**Agricultural Productivity + Animal Welfare + Resource Efficiency + Environmental Sustainability**

---

## RQ4 — Evaluation, Limitations, and Research Gaps

**How are agricultural Multi-Agent Systems evaluated, and what methodological, technical, and practical limitations or research gaps are reported in the literature?**

The review will investigate evaluation approaches including:

- datasets;
- simulated environments;
- IoT and sensor systems;
- field experiments;
- experimental scenarios;
- baselines;
- evaluation metrics;
- real-world deployments.

The review will also analyse reported limitations related to:

- scalability;
- uncertainty;
- explainability;
- interoperability;
- environmental modelling;
- computational requirements;
- reproducibility;
- data availability;
- deployment cost;
- real-world adoption and validation.

The findings will be used to identify open research gaps in the design and application of integrated, sustainable smart-farm Multi-Agent Systems.

---

# Relationship Between the Research Questions

The research questions are organised around four main analytical dimensions:

```text
RQ0 — Overall MAS use in sustainable smart farming
        │
        ├── RQ1 — Agent architectures, roles, and intelligence
        │
        ├── RQ2 — Coordination, negotiation, and resource allocation
        │
        ├── RQ3 — Agricultural and environmental outcomes
        │
        └── RQ4 — Evaluation, limitations, and research gaps
```
