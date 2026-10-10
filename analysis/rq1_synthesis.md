# RQ1 — MAS Architectures, Agent Roles, and Decision-Making

**RQ1:** *What types of agents, architectures, and decision-making approaches are used in Multi-Agent Systems for smart agriculture?*

The main analysis uses **53 publications**, with a sensitivity check across **44 reconciled study families**.

## MAS architectures

| Architecture | Original 34 | Final 53 | 44-family evidence |
|---|---:|---:|---:|
| Decentralised | 10 (29.4%) | 17 (32.1%) | 16 (36.4%) |
| Hybrid | 8 (23.5%) | 13 (24.5%) | 11 families contain the code |
| Hierarchical | 7 (20.6%) | 11 (20.8%) | 8 families contain the code |
| Centralised | 7 (20.6%) | 10 (18.9%) | 7 (15.9%) |
| Distributed | 2 (5.9%) | 2 (3.8%) | 2 (4.5%) |

Decentralised architecture is the largest individual category, but there is no single dominant architecture.

**SF42 contains paper-specific Hybrid and Hierarchical coding.** Family-level architecture should therefore not force SF42 into one uniquely settled class.

## Agent paradigms

Agent paradigms are multi-label.

| Paradigm | Original 34 | Final 53 | 44 families |
|---|---:|---:|---:|
| Rule-based | 22 (64.7%) | 37 (69.8%) | 31 (70.5%) |
| Utility-based | 11 (32.4%) | 20 (37.7%) | 17 (38.6%) |
| Learning-based | 10 (29.4%) | 11 (20.8%) | 10 (22.7%) |
| BDI | 2 (5.9%) | 2 (3.8%) | 1 (2.3%) |
| Reactive | 2 (5.9%) | 2 (3.8%) | 2 (4.5%) |
| Case-based reasoning | 1 (2.9%) | 1 (1.9%) | 1 (2.3%) |
| LLM-based | 1 (2.9%) | 1 (1.9%) | 1 (2.3%) |
| Not reported | 3 (8.8%) | 6 (11.3%) | 5 (11.4%) |

Rule-based and utility-based approaches therefore remain highly important despite the recent growth of learning-based systems.

## Manually adjudicated agent-role themes

| Role theme | 53 publications | 44 families |
|---|---:|---:|
| Farmer / household / agricultural producer | 33 (62.3%) | 28 (63.6%) |
| Manager / regulator / coordinating actor | 25 (47.2%) | 19 (43.2%) |
| Operational / field / irrigation / workforce / robot | 17 (32.1%) | 13 (29.5%) |
| Specialist software / analytical / advisory | 11 (20.8%) | 11 (25.0%) |
| Biophysical / herd / crop / environmental representation | 19 (35.8%) | 17 (38.6%) |
| Market / bidder / trader | 11 (20.8%) | 8 (18.2%) |

These categories overlap.

A modelled cow, crop, soil, field, canal, or environmental entity is not automatically an independently autonomous software agent. The categories describe the roles represented in the MAS and associated simulation environment.

## Decision-making mechanisms

The extracted literature contains several recurring approaches:

- rules, thresholds, and heuristics;
- mathematical and constrained optimisation;
- economic and utility-based decision models;
- reinforcement learning and MARL;
- Model Predictive Control;
- auctions, bidding, and market mechanisms;
- evolutionary and multi-objective optimisation;
- Bayesian or belief updating;
- LLM-based and knowledge-supported reasoning.

These mechanisms frequently coexist. For example, local agent decisions may be rule-based while a central layer performs optimisation, or learning agents may interact through a market-clearing mechanism.

Because the fine-grained decision-mechanism taxonomy was not independently full-text re-coded for all 53 publications, the final synthesis emphasises the extracted mechanism descriptions rather than presenting unsupported exclusive frequency counts.

## Autonomy

Autonomy varies substantially.

Some farmer or household agents make local decisions while interacting indirectly through shared environmental resources.

Other systems use decentralised agents but rely on a central auctioneer, market-clearing procedure, supervisor, optimiser, or higher-level regulatory agent.

Learning-based systems may use centralised training with decentralised execution.

Central MPC and scheduling systems can model multiple agents without giving those agents unrestricted local decision authority.

Therefore, simulation autonomy should not be interpreted as demonstrated real-world operational autonomy.

## Direct answer to RQ1

Agricultural MAS use heterogeneous agent representations and decision structures rather than a single standard architecture.

Farmer and producer agents are especially common, but management, regulatory, operational, market, software, livestock, crop, and environmental roles are also represented.

Rule-based and utility-based approaches remain widespread alongside optimisation, MPC, learning, market mechanisms, and newer AI-supported methods.

The dominant pattern is therefore **bounded autonomy**: local agent decisions operate within resource, institutional, market, environmental, or optimisation constraints rather than as completely unrestricted independent systems.
