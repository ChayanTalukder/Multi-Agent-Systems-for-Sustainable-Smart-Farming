# Step 6H — Formal MAS Taxonomy and Evidence Mapping

## 1. Scope

Step 6H organises the final SLR corpus into a formal, evidence-grounded taxonomy and maps where the literature is concentrated or sparse.

The analysis uses:

- **53 included publications (S01–S53)** as the primary unit of analysis;
- **44 reconciled study families** as an evidence-independence sensitivity layer;
- the final Step 5 extraction dataset;
- the manually adjudicated RQ1 agent-role and RQ2 coordination-mechanism classifications;
- the adjudicated RQ3 outcome-direction and RQ4 comparator classifications;
- the completed quality-assessment dataset.

No screening, inclusion, exclusion, extraction, or study-family decisions are changed in this step.

## 2. Taxonomy design principles

The taxonomy separates **what a MAS is designed to do and how it is organised** from **how strongly it has been evaluated**.

The formal MAS taxonomy therefore uses six analytical axes:

1. **Application domain** — the primary agricultural setting.
2. **Functional purpose** — the dominant function served by the MAS.
3. **Agent roles** — the functional types of actors/entities represented.
4. **MAS architecture** — how decision authority is organised.
5. **Decision paradigm** — the decision logic used by agents.
6. **Coordination mechanism** — how agents or organisational layers interact to manage tasks/resources.

Evaluation maturity, sustainability coding, RQ3 outcome direction, comparator type, deployment, reproducibility, and QA are treated as an **evidence overlay**, not as taxonomy axes.

### Counting rules

- Application domain, functional purpose, and architecture are single-valued at the publication level.
- Agent roles, decision paradigms, coordination mechanisms, and comparator categories are multi-label.
- Family-level counts are **evidence-presence counts**: a family is counted when at least one publication in that family supports the relevant category or category pair.
- Family-level categories are not always mutually exclusive. In particular, **SF42 contains both Hybrid and Hierarchical architecture evidence in different publications**, and it also spans irrigation/water and energy/WEF primary-domain coding.
- Family co-occurrence counts are sensitivity evidence, not claims of independent replication.

## 3. Formal MAS taxonomy

### Axis 1 — Application domain

| Category | Publications | Family evidence |
|---|---:|---:|
| Irrigation / water management | 24 (45.3%) | 20 |
| Crop / farm management | 8 (15.1%) | 8 |
| Livestock / integrated farming | 6 (11.3%) | 6 |
| Workforce / robotics / task allocation | 6 (11.3%) | 4 |
| Energy / WEF nexus | 5 (9.4%) | 3 |
| Soil / nutrient / environmental management | 4 (7.5%) | 4 |

Irrigation/water management is the largest and most diverse application domain.

### Axis 2 — Functional purpose

| Category | Publications | Family evidence |
|---|---:|---:|
| Operational resource allocation, scheduling and control | 21 (39.6%) | 17 |
| Policy, scenario and socio-ecological impact assessment | 17 (32.1%) | 15 |
| Trading, negotiation and collective-resource governance | 13 (24.5%) | 10 |
| Decision support, monitoring and diagnosis | 2 (3.8%) | 2 |

This confirms two broad traditions in the corpus: operational/engineering coordination and socio-ecological/policy modelling, with a substantial market/governance strand between them.

### Axis 3 — Agent roles

The manually adjudicated role categories are multi-label.

| Agent role | Publications | Family evidence |
|---|---:|---:|
| Farmer / household / agricultural producer | 33 (62.3%) | 28 |
| Manager / regulator / central coordinating actor | 25 (47.2%) | 19 |
| Biophysical, herd, crop or environmental representation | 19 (35.8%) | 17 |
| Operational field / irrigation / workforce / robot agent | 17 (32.1%) | 13 |
| Specialist software / analytical / advisory agent | 11 (20.8%) | 11 |
| Market / bidder / trading role | 11 (20.8%) | 8 |

Farmer/producer agents are the most widespread role, but the evidence base is not exclusively farmer-centric. A substantial fraction of the corpus combines human decision actors with managers, operational agents, and explicit biophysical/environmental representations.

### Axis 4 — MAS architecture

| Architecture | Publications | Family evidence* |
|---|---:|---:|
| Decentralised | 17 (32.1%) | 16 |
| Hybrid | 13 (24.5%) | 11 |
| Hierarchical | 11 (20.8%) | 9 |
| Centralised | 10 (18.9%) | 7 |
| Distributed | 2 (3.8%) | 2 |

\*Family evidence is non-exclusive because related publications can use different architecture codes; SF42 contributes to both Hybrid and Hierarchical evidence.

There is no single dominant architecture. Decentralised systems form the largest individual category, but hybrid, hierarchical, and centralised designs are all substantial.

### Axis 5 — Decision paradigm

| Paradigm | Publications | Family evidence |
|---|---:|---:|
| Rule-based | 37 (69.8%) | 31 |
| Utility / economic | 20 (37.7%) | 17 |
| Learning-based | 11 (20.8%) | 10 |
| BDI | 2 (3.8%) | 1 |
| Reactive | 2 (3.8%) | 2 |
| Case-based reasoning | 1 (1.9%) | 1 |
| LLM-based | 1 (1.9%) | 1 |
| Other | 1 (1.9%) | 1 |
| Not reported | 6 (11.3%) | 5 |

The literature remains dominated by explicit rules and economic/utility logic. Learning-based methods are important but do not replace these older paradigms; they coexist with them.

### Axis 6 — Coordination mechanism

The manually adjudicated mechanisms are multi-label.

| Coordination mechanism | Publications | Family evidence |
|---|---:|---:|
| Hierarchical / supervisory / shared-controller orchestration | 25 (47.2%) | 19 |
| Environment- or shared-resource-mediated interaction | 20 (37.7%) | 18 |
| Operational allocation / optimisation / task scheduling | 16 (30.2%) | 12 |
| Auction / bidding / market / price-based exchange | 15 (28.3%) | 10 |
| Social-network information diffusion / peer exchange | 13 (24.5%) | 13 |
| Learning-based adaptive coordination / MARL | 9 (17.0%) | 8 |
| Direct negotiation / collective agreements | 8 (15.1%) | 7 |

Two safeguards remain important: market/auction mechanisms are not automatically coded as direct negotiation, and environment-mediated interaction is not treated as direct messaging.

## 4. Cross-classification findings

### 4.1 Domain × functional purpose

The application domains have distinct functional profiles.

- **Irrigation/water management:** 11/24 operational allocation/control, 8/24 trading/governance, 5/24 policy/socio-ecological assessment.
- **Crop/farm management:** 6/8 policy/socio-ecological assessment and 2/8 operational allocation/control.
- **Livestock/integrated farming:** evenly divided across policy/socio-ecological assessment (2), trading/governance (2), and decision support/monitoring (2).
- **Workforce/robotics/task allocation:** all 6 publications are operational allocation/control.
- **Energy/WEF nexus:** 3/5 trading/governance, 1 operational, and 1 policy/socio-ecological.
- **Soil/nutrient/environmental management:** 3/4 policy/socio-ecological and 1/4 operational.

The two decision-support/monitoring publications occur in the livestock/integrated domain.

### 4.2 Domain × architecture

Irrigation/water management is the most architecturally diverse domain:

| Domain | Decentralised | Hybrid | Hierarchical | Centralised | Distributed |
|---|---:|---:|---:|---:|---:|
| Irrigation / water | 8 | 4 | 8 | 3 | 1 |
| Crop / farm | 3 | 4 | 1 | 0 | 0 |
| Livestock / integrated | 3 | 0 | 0 | 2 | 1 |
| Workforce / robotics | 1 | 0 | 0 | 5 | 0 |
| Energy / WEF | 0 | 4 | 1 | 0 | 0 |
| Soil / nutrient / environmental | 2 | 1 | 1 | 0 | 0 |

The concentration is especially clear in two domains: workforce/robotics is strongly **centralised**, whereas energy/WEF is strongly **hybrid** in the publication-level evidence.

### 4.3 Domain × coordination mechanism

The strongest publication-level co-occurrences are:

- irrigation × hierarchical/supervisory orchestration: **13** publications;
- irrigation × environment/shared-resource-mediated interaction: **10**;
- irrigation × optimisation/scheduling: **7**;
- irrigation × learning/MARL: **6**;
- irrigation × direct negotiation/agreements: **6**;
- workforce/robotics × optimisation/scheduling: **6**;
- crop/farm × environment-mediated interaction: **4**;
- crop/farm × peer diffusion/exchange: **4**;
- workforce/robotics × auction/market: **4**.

At family level, the broad pattern remains: irrigation contributes the largest number of distinct families across almost every coordination mechanism.

### 4.4 Architecture × coordination mechanism

The architecture and coordination mechanisms form interpretable combinations:

- **Hierarchical architecture** is strongly associated with hierarchical/supervisory orchestration (11 publications).
- **Decentralised architecture** is strongly associated with environment-mediated interaction (9) and peer diffusion/exchange (7).
- **Centralised architecture** is strongly associated with operational optimisation/scheduling (7) and supervisory orchestration (7).
- **Hybrid architecture** combines several mechanism types, including hierarchical orchestration (7), learning/MARL (5), environment-mediated interaction (5), and auction/market exchange (5).

This supports treating architecture and coordination as separate taxonomy axes: the same architecture can use several coordination mechanisms, and the same mechanism can appear under several architectures.

### 4.5 Agent role × coordination mechanism

Several role–mechanism relationships are particularly prominent:

- farmer/producer × environment-mediated interaction: **20 publications**;
- manager/regulator × hierarchical/supervisory orchestration: **19**;
- biophysical representation × environment-mediated interaction: **15**;
- manager/regulator × operational optimisation/scheduling: **13**;
- farmer/producer × peer diffusion/exchange: **12**;
- operational/robot agent × optimisation/scheduling: **11**;
- market/trader role × auction/market coordination: **11**.

These relationships provide a useful structural interpretation of the corpus: agent roles are not merely labels but are associated with characteristic coordination patterns.

## 5. Evidence mapping overlay

### 5.1 Implementation maturity by domain

| Domain | Simulation | Prototype | Field pilot | Controlled experiment |
|---|---:|---:|---:|---:|
| Irrigation / water | 23 | 0 | 1 | 0 |
| Crop / farm | 7 | 0 | 1 | 0 |
| Livestock / integrated | 4 | 2 | 0 | 0 |
| Workforce / robotics | 3 | 2 | 0 | 1 |
| Energy / WEF | 5 | 0 | 0 | 0 |
| Soil / nutrient / environmental | 4 | 0 | 0 | 0 |

Simulation dominates every application domain. Non-simulation evidence is concentrated in a small number of crop/farm, livestock, irrigation, and workforce/robotics publications.

### 5.2 RQ3 outcome direction by domain

| Domain | Favourable / conditional | Mixed / trade-off | Descriptive / feasibility | No direct outcome |
|---|---:|---:|---:|---:|
| Irrigation / water | 10 | 11 | 3 | 0 |
| Crop / farm | 3 | 4 | 1 | 0 |
| Livestock / integrated | 0 | 2 | 3 | 1 |
| Workforce / robotics | 5 | 1 | 0 | 0 |
| Energy / WEF | 4 | 1 | 0 | 0 |
| Soil / nutrient / environmental | 2 | 2 | 0 | 0 |

These categories describe the direction of the extracted/adjudicated evidence, not pooled effects. The apparently favourable profiles in workforce/robotics and energy/WEF remain largely simulation/algorithmic evidence and should not be interpreted as established field effectiveness.

### 5.3 Domain evidence profiles

Several coverage patterns are important for interpretation:

- **Irrigation/water** is both the largest domain and the most structurally diverse, but 23/24 publications are simulation maturity.
- **Crop/farm management** is dominated by policy/socio-ecological simulation and peer/environmental interaction.
- **Livestock/integrated farming** contains more prototype/decision-support activity than most domains, but the RQ3 evidence is mostly descriptive or mixed rather than directly favourable.
- **Workforce/robotics** has the strongest concentration of non-simulation evaluation (two prototypes and one controlled experiment), but it has no direct-sustainability-coded publications in the current extraction.
- **Energy/WEF** is entirely simulation-based and concentrated in three study families despite five publications.
- **Soil/nutrient/environmental management** is small (four publications/families) and entirely simulation-based, although all four directly address sustainability.

## 6. Coverage matrix interpretation

For Step 6H, evidence density is interpreted descriptively:

- **Absent:** no publication/family in the corpus occupies the combination;
- **Sparse:** one or two families;
- **Moderate:** three to five families;
- **Dense:** six or more families.

These labels describe **coverage**, not methodological quality or scientific importance.

The strongest dense family-level areas are concentrated around irrigation/water management, especially hierarchical/supervisory coordination and environment/shared-resource interaction. Several other domain–mechanism and domain–architecture cells are sparse or absent.

Those sparse cells are **signals for Step 6I**, not automatic research gaps. Step 6I must check whether a sparse combination is conceptually meaningful, whether authors themselves report the need, and whether the absence follows naturally from the problem structure.

## 7. Step 6H conclusion

The formal taxonomy shows that agricultural MAS research is best represented as a multi-dimensional design space rather than a single progression from simple to advanced systems.

The dominant evidence structure is:

1. a large irrigation/water-management core;
2. farmer/producer agents embedded in socio-ecological and shared-resource interactions;
3. managers/supervisors associated with hierarchical coordination;
4. operational/robot agents associated with optimisation and task scheduling;
5. market/trader agents associated with auctions and price-mediated exchange;
6. persistent use of rule-based and utility/economic decision logic alongside newer learning-based methods;
7. extensive simulation evidence but limited non-simulation and real-world validation.

The study-family sensitivity maps preserve these broad conclusions and show that they are not merely an artefact of multiple related publications.

The next analytical step is **Step 6I — Consolidated Research Gaps**, which should use this taxonomy and evidence map together with RQ0–RQ4, reported limitations, and author-reported research gaps to distinguish:

- author-reported gaps;
- corpus-level evidence gaps;
- synthesis-derived gaps;
- and priorities that are sufficiently supported to include in the final SLR.
