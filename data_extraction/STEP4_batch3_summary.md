# Step 4 — Extraction and QA: Batch 3

## Batch scope

**S47–S53 (7 publications)**

| Study | Publication | QA |
|---|---|---:|
| S47 | Simulating soil fertility and poverty dynamics in Uganda: A bio-economic multi-agent systems approach | 14/14 |
| S48 | An adaptive multi-agent model for water allocation under scarcity: application of bankruptcy methods | 14/14 |
| S49 | Optimal Irrigation Allocation for Large-Scale Arable Farming | 13/14 |
| S50 | Multi-Robot Task Allocation in Agriculture Scenarios Based on the Improved NSGA-II Algorithm | 12/14 |
| S51 | Fostering local crop-livestock integration via legume exchanges using an innovative integrated assessment and modelling approach based on the MAELIA platform | 14/14 |
| S52 | Multi-actor approach to manage the water-energy-food nexus at territory scale | 13/14 |
| S53 | Optimal irrigation management for large-scale arable farming using model predictive control | 13/14 |

## Main coding decisions

- **S47 — Decentralised MP-MAS:** heterogeneous farm households independently optimise investment/production/consumption; the main inter-agent mechanism in this Uganda application is peer technology diffusion.
- **S48 — Hybrid:** a reservoir-operation layer determines supply and coordinates 11 agricultural agents; ordinary scarcity uses decentralised penalties, while severe drought invokes bankruptcy/cooperative-game rules.
- **S49 — Centralised:** irrigation machinery are resource-delivery agents whose daily field assignments and irrigation amounts are jointly selected by a central MPC optimiser.
- **S50 — Centralised:** agricultural robots are centrally allocated field tasks using improved NSGA-II; the paper optimises travel distance and workload balance rather than autonomous robot negotiation.
- **S51 — Decentralised MAELIA application:** farm agents follow local technical rules; inter-farm coordination increases across coexistence, complementarity and synergetic feed/crop-exchange scenarios.
- **S52 — Hierarchical/multi-level:** MAELIA operational farm/water agents feed strategic AHP and Monte-Carlo decision layers for water-energy-food land allocation.
- **S53 — Centralised:** the earlier irrigation-MPC paper formulates irrigation machinery as agents and fields as clients in a multi-agent resource-allocation problem.

## Representative findings

- **S47:** poverty incidence falls from **28.9%** at baseline to **24.4%** with credit and **19.8%** with credit plus improved technology, but soil-N stocks do not improve enough to guarantee long-term ecological sustainability.
- **S48:** in severe drought, **FPS ($6.55M)** and **PPS ($6.53M)** deliver the highest total profits, while PRO has the highest Jain fairness index (**0.97** in Table 5); the paper explicitly quantifies the fairness-efficiency trade-off.
- **S49:** over 33 seasons, MPC gives a **5.31% higher objective**, **5.29% more yield** and **5.17% less water** than the heuristic; water-use efficiency improves **11.64%**.
- **S50:** on the real `farmdata40` case with three robots, INSGA-II reduces total travel to **19,262.47** versus **30,975.29** for NSGA-II and **26,310.72** for GA, although workload balance can worsen.
- **S51:** the synergetic crop-livestock scenario raises territorial gross margin by **€71/ha (4%)**, reduces N fertiliser by about **21 kg N/ha (11%)**, and reduces labour time by about **12 min/ha (5%)** while achieving local feed self-sufficiency.
- **S52:** the 800-km² WEF-nexus case contains **15,024 parcels**; a 10-year MAELIA run takes **31 h 22 min**, and the tested decision methods favour 100% PV under the chosen indicators, which the authors identify as unrealistic without better subsidy/social/food representation.
- **S53:** for 30 fields and three agents, MPC raises mean profit from **€22,405 to €26,099**, while irrigation falls from **2,779 to 1,922 mm** and irrigation events from **111.1 to 65.2**, at the cost of about **5% lower mean yield**.

## QA

Batch QA ranges from **12–14/14**.

- S47, S48 and S51 score 14 due to detailed methods, strong evaluation/reproducibility support and explicit limitations.
- S49, S52 and S53 score 13 primarily because implementation code/data availability is incomplete.
- S50 scores 12 because code and the real-farm dataset are not clearly released and limitations are discussed mainly as brief future-work items.

## Related-publication flags for Step 5

No family IDs are assigned yet, but the extraction notes flag likely relationships:

- **S49 ↔ S53**: later journal extension and earlier conference irrigation-MPC work.
- **S51**: MAELIA research line already represented by S13/S22/S42.
- **S52**: MAELIA-based multi-level WEF extension.
- **S47**: MP-MAS platform/application line represented elsewhere among citation-search papers.

These will be resolved systematically in **Step 5 — Study-family reconciliation**.

## Step 4 validation

- S01–S46 were preserved unchanged.
- S47–S53 have all substantive RQ0–RQ4 fields populated.
- S35–S53 are now fully extracted except the two family fields intentionally deferred to Step 5.
- QA1–QA7 and QA totals are complete and arithmetically valid for **all 53 publications**.
