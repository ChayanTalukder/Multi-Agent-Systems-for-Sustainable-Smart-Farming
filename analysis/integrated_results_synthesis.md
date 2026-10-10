# Integrated Results and Synthesis

## 1. Analysis Status

The final working analytical corpus contains **53 included publications representing 44 reconciled study families**.

The primary database-search pathway produced **34 included publications**, while one-generation backward and forward citation searching contributed **19 additional included publications**.

The analytical workflow completed before this synthesis includes:

- structured data extraction for S01–S53;
- quality assessment for S01–S53;
- study-family reconciliation;
- descriptive analysis;
- RQ0–RQ4 synthesis;
- cross-RQ consistency checking;
- RQ3 outcome-direction adjudication;
- RQ4 comparator-strength adjudication;
- manual RQ1/RQ2 thematic review;
- targeted verification of selected high-impact primary-source claims;
- final Step 6G reconciliation.

The current synthesis therefore supersedes the earlier preliminary analysis of the original 34-publication corpus.

The next analytical stages are:

1. **Step 6H — MAS Taxonomy and Evidence Mapping**;
2. **Step 6I — Consolidated Research Gaps**.

PRISMA 2020 reporting follows those two stages.

---

## 2. Counting and Evidence Rules

The review uses two complementary units of analysis.

### Publication level

The primary descriptive corpus is:

```text
n = 53 publications
```

Publication-level statistics describe the literature as published.

### Study-family level

Study-family reconciliation identified:

```text
n = 44 distinct study families
```

Seven families contain multiple related publications.

The family-level analysis is used as a sensitivity check to reduce the risk that closely related publications, reused datasets, extensions, or repeated case studies artificially strengthen a conclusion.

A family is counted for a characteristic when at least one publication in that family contains the relevant evidence.

Family-level multi-label counts are therefore not necessarily mutually exclusive.

Study-family aggregation is **not** a meta-analysis and does **not** establish independent replication of an effect.

---

## 3. Evidence Precedence

Where preliminary and adjudicated analyses differ, the following precedence is used.

1. The reconciled 53-publication extraction dataset is authoritative for study-level extracted facts.
2. The manually reviewed RQ1/RQ2 coding is authoritative for the final agent-role and coordination-theme classifications.
3. The RQ3/RQ4 adjudication is authoritative for outcome-direction interpretation and comparator-strength safeguards.
4. Targeted primary-source checks take precedence over simplified earlier interpretations of specific high-impact claims.
5. Preliminary keyword-derived thematic classifications must not override the manually reviewed classifications.
6. The current integrated synthesis takes precedence over the earlier 34-publication integrated synthesis.

---

## 4. Characteristics of the Final Evidence Base

Citation searching increased the corpus from **34 to 53 publications**, a gain of **19 publications (+55.9%)**.

The expanded corpus also increased the number of distinct study families from **27 to 44**.

The publication-year range expanded from:

```text
2010–2026
```

to:

```text
2001–2026
```

because five pre-2010 foundational studies were retained under the predefined IC7 citation-search exception.

The median publication year shifted from **2022 to 2020**, reflecting the addition of older foundational work.

The mean quality-assessment score changed from approximately **12.76/14** in the original 34-publication corpus to **12.94/14** in the final 53-publication corpus, while the median remained **13/14**.

Citation searching therefore broadened the historical and methodological evidence base without materially lowering assessed methodological quality.

---

## 5. RQ0 — Overall MAS Application Landscape and Purpose

Multi-Agent Systems are used in sustainable smart farming for two broad and overlapping traditions.

### Operational and engineering applications

These include:

- irrigation scheduling;
- water allocation;
- machinery allocation;
- agricultural robotics;
- labour and harvest scheduling;
- energy trading;
- resource optimisation;
- decision support;
- model-predictive control;
- learning-based allocation.

### Socio-ecological and policy applications

These include:

- farmer decision modelling;
- technology adoption;
- collective-action problems;
- water governance;
- markets;
- land use;
- policy interventions;
- crop-soil-hydrological interaction;
- livelihood modelling;
- environmental sustainability.

The primary functional-purpose distribution is:

| Primary functional purpose | Final 53 | 44 families |
|---|---:|---:|
| Operational resource allocation, scheduling and control | 21 (39.6%) | 17 (38.6%) |
| Policy, scenario and socio-ecological impact assessment | 17 (32.1%) | 15 (34.1%) |
| Trading, negotiation and collective-resource governance | 13 (24.5%) | 10 (22.7%) |
| Decision support, monitoring and diagnosis | 2 (3.8%) | 2 (4.5%) |

Operational resource allocation remains the largest single purpose, but citation searching substantially strengthens the representation of foundational policy, governance, collective-action, and socio-ecological modelling.

### Agricultural domains

Irrigation and water management remain the largest primary application domain:

- **24/53 publications (45.3%)**;
- **20/44 study families (45.5%)**.

Other application areas include:

- crop and farm management;
- soil and nutrient management;
- livestock and dairy systems;
- crop-livestock integration;
- farm energy systems;
- renewable-energy / WEF planning;
- workforce management;
- agricultural robotics and task allocation.

Integrated-system studies account for **27/53 publications (50.9%)**, indicating substantial interest in models that connect several technical, biological, environmental, economic, or institutional components.

---

## 6. RQ1 — Agents, Architectures, and Decision-Making

Agricultural MAS use heterogeneous architectures rather than one standard system design.

The source-coded architecture distribution is:

| Architecture | Publications |
|---|---:|
| Decentralised | 17 (32.1%) |
| Hybrid | 13 (24.5%) |
| Hierarchical | 11 (20.8%) |
| Centralised | 10 (18.9%) |
| Distributed | 2 (3.8%) |

No single architecture dominates the evidence base.

The manually reviewed agent-role themes show frequent representation of:

| Agent-role theme | Publications | Families |
|---|---:|---:|
| Farmer / household / agricultural producer | 33 (62.3%) | 28 (63.6%) |
| Manager / regulator / coordinating actor | 25 (47.2%) | 19 (43.2%) |
| Operational / field / irrigation / workforce / robot | 17 (32.1%) | 13 (29.5%) |
| Specialist software / analytical / advisory | 11 (20.8%) | 11 (25.0%) |
| Biophysical / herd / crop / environmental representation | 19 (35.8%) | 17 (38.6%) |
| Market / bidder / trader | 11 (20.8%) | 8 (18.2%) |

These categories overlap.

A modelled environmental, crop, field, livestock, or spatial entity is not automatically an autonomous software agent.

### Agent paradigms

Rule-based reasoning remains especially common:

- Rule-based: **37/53**;
- Utility-based: **20/53**;
- Learning-based: **11/53**.

The literature also contains BDI, reactive, case-based, LLM-based, optimisation-driven, MPC, market, and other hybrid approaches.

The dominant pattern is therefore **bounded autonomy**.

Agents commonly make local decisions, but their actions are constrained by:

- resource availability;
- institutional rules;
- market conditions;
- shared environmental states;
- central supervisors;
- optimisation procedures;
- physical infrastructure.

Simulation autonomy must not therefore be interpreted automatically as real-world operational autonomy.

A known family-level qualification remains for **SF42**, whose related publications contain different Hybrid/Hierarchical architecture coding. The review retains that publication-specific difference rather than forcing an arbitrary single family label.

---

## 7. RQ2 — Communication, Coordination, and Shared Resources

Coordination is a defining characteristic of the corpus.

Source-coded interaction evidence includes:

| Interaction | Publications | Families |
|---|---:|---:|
| Coordination | 47 (88.7%) | 38 (86.4%) |
| Information sharing | 33 (62.3%) | 30 (68.2%) |
| Communication | 30 (56.6%) | 24 (54.5%) |
| Competition | 23 (43.4%) | 17 (38.6%) |
| Cooperation | 18 (34.0%) | 17 (38.6%) |
| Task allocation | 13 (24.5%) | 10 (22.7%) |
| Negotiation | 9 (17.0%) | 6 (13.6%) |

The manually reviewed coordination themes identify several recurring mechanisms:

| Coordination theme | Publications | Families |
|---|---:|---:|
| Hierarchical / supervisory / shared-controller | 25 (47.2%) | 19 (43.2%) |
| Environment- or shared-resource-mediated | 20 (37.7%) | 18 (40.9%) |
| Operational allocation / optimisation / scheduling | 16 (30.2%) | 12 (27.3%) |
| Auction / bidding / market / price exchange | 15 (28.3%) | 10 (22.7%) |
| Peer diffusion / information exchange | 13 (24.5%) | 13 (29.5%) |
| Learning-based adaptive coordination | 9 (17.0%) | 8 (18.2%) |
| Direct negotiation / collective agreements | 8 (15.1%) | 7 (15.9%) |

These themes are overlapping.

Two distinctions are especially important:

- an **auction or market mechanism is not automatically direct negotiation**;
- agents affecting one another through groundwater, canals, pasture, environmental state, or other shared resources are **not automatically communicating directly**.

Resource scarcity or another explicit operational constraint is represented in **50/53 publications (94.3%)** and **41/44 families (93.2%)**.

Scarce or shared resources include:

- irrigation water;
- groundwater;
- reservoir and canal capacity;
- land and pasture;
- energy;
- battery capacity;
- nutrients and manure;
- machinery;
- robots;
- agricultural tasks;
- workforce capacity.

The evidence therefore supports a broad interpretation of agricultural MAS coordination: coordination may occur through direct communication, central orchestration, optimisation, markets, learning, peer exchange, institutional rules, or indirect environmental feedback.

---

## 8. RQ3 — Agricultural and Sustainability Outcomes

Outcome fields are widely populated across the corpus, but the presence of a reported outcome does **not** imply that the outcome improved.

Evidence coverage includes:

| Outcome indicator | Final 53 | 44 families |
|---|---:|---:|
| Agricultural outcomes described | 51 (96.2%) | 42 (95.5%) |
| Livestock outcomes described | 7 (13.2%) | 7 (15.9%) |
| Resource-efficiency outcomes described | 48 (90.6%) | 40 (90.9%) |
| Environmental outcomes described | 38 (71.7%) | 32 (72.7%) |
| Environmental mitigation mechanism described | 41 (77.4%) | 34 (77.3%) |
| Quantitative results reported | 47 (88.7%) | 39 (88.6%) |
| Trade-offs described | 45 (84.9%) | 38 (86.4%) |

Direct sustainability coding occurs in **39/53 publications (73.6%)**.

However, direct sustainability coding indicates that sustainability was explicitly modelled, evaluated, or discussed. It does not establish a verified real-world environmental benefit.

### Adjudicated outcome direction

The Step 6G reviewer adjudication classifies the 53 publications as:

```text
Favourable / conditional             24
Mixed / trade-off / scenario-based   21
Descriptive / feasibility             7
No direct agricultural outcome        1
```

This distribution shows why simple positive/negative counting would be misleading.

Many agricultural MAS results depend on:

- the chosen objective function;
- resource scarcity;
- behavioural assumptions;
- environmental conditions;
- policy settings;
- allocation rules;
- comparator choice;
- economic or fairness criteria.

Important examples include:

- profitability versus equitable water allocation;
- crop production versus water use;
- staff effort versus execution time;
- environmental restrictions versus farm income;
- renewable-energy value versus food production;
- performance versus computational cost.

Specific evidence also requires family-level caution.

**S49 and S53** belong to the same irrigation-MPC study family and should not be treated as independent replications.

**S25 and S33** report different harvest-allocation comparisons and their metric-specific findings must not be conflated.

**S04** reports decision-support system performance, including routing and response-quality measures, but these metrics do not demonstrate improved cattle welfare in operational farming.

Overall, the literature demonstrates promising resource-management and decision-support potential, but it does not establish universal agricultural or environmental improvements.

---

## 9. RQ4 — Evaluation, Maturity, and Evidence Strength

The evidence base is strongly simulation-oriented.

Implementation maturity is:

| Implementation maturity | Publications | 44-family evidence |
|---|---:|---:|
| Simulation | 46 (86.8%) | 39 (88.6%) |
| Prototype | 4 (7.5%) | 3 families |
| Field pilot | 2 (3.8%) | 2 families |
| Controlled experiment | 1 (1.9%) | 1 family |

Reported evaluation descriptions frequently include simulation, case studies, benchmarking, scenario comparisons, sensitivity analysis, calibration, or validation.

However, these forms of evaluation differ substantially in evidential strength.

A scenario comparison is not automatically an experimental control.

Historical fit or calibration is not automatically evidence of intervention effectiveness.

An algorithmic benchmark demonstrates relative computational performance only within the tested setting.

### Real-world deployment

The source-coded deployment field contains:

```text
No        51
Yes        1
Partial    1
```

The apparent S02 `Yes` status remains independently unconfirmed after targeted source checking.

The final review should therefore describe real-world deployment as **rare and incompletely established**, rather than claiming two independently verified operational systems.

### Reproducibility

Reported availability remains limited:

- code available: **8/53 publications**;
- data available: **14/53 publications**.

Family-level values are:

- code: **8/44 families**;
- data: **13/44 families**.

The most frequent reviewer-coded limitation concerns the need for stronger real-world validation, with additional recurring limitations involving:

- uncertainty;
- reproducibility;
- environmental modelling;
- computational requirements;
- scalability.

The evidence base is therefore substantially more mature in **simulation, modelling, and algorithm development** than in operational agricultural validation.

---

## 10. Cross-RQ Interpretation

The five research questions converge on several broad findings.

### 10.1 Scarcity is a central organising problem

Resource scarcity or explicit operational constraints appear in **50/53 publications**.

MAS are therefore especially attractive when agricultural decisions involve:

- multiple users;
- heterogeneous objectives;
- constrained resources;
- competing demands;
- dynamic environmental conditions.

### 10.2 Coordination is the defining technical function

Explicit coordination occurs in **47/53 publications**.

The literature demonstrates that coordination does not require one universal protocol.

Different applications use:

- central supervision;
- local autonomous decisions;
- optimisation;
- auctions;
- markets;
- learning;
- peer communication;
- environmental feedback;
- institutional rules.

### 10.3 Water remains the dominant application domain

Irrigation and water management account for approximately **45% of the corpus** at both publication and family level.

Water management therefore remains the clearest and most mature application setting for agricultural MAS, although the corpus is diversifying into energy, labour, robotics, livestock, nutrient management, land use, and integrated farm systems.

### 10.4 The field contains two complementary research traditions

One strand focuses on **engineering and operational coordination**, including optimisation, scheduling, MPC, robotics, MARL, energy, and resource allocation.

The second focuses on **socio-ecological and policy modelling**, including heterogeneous farmer behaviour, markets, institutions, collective action, environmental feedback, and policy scenarios.

Recent integrated frameworks increasingly connect these traditions.

### 10.5 Sustainability is common as an objective but weaker as field evidence

Direct sustainability is coded in **39/53 publications**, and environmental outcomes are described in **38/53**.

However, most of this evidence remains simulation-based.

Accordingly, the literature contains substantial **sustainability-oriented modelling evidence**, but comparatively little independently verified evidence of sustained real-world environmental improvement.

### 10.6 The primary maturity gap is translation to practice

The corpus contains extensive algorithmic, modelling, and simulation work, but limited evidence of persistent operational deployment.

This is one of the strongest findings across the review because it remains visible after study-family reconciliation.

---

## 11. Effect of Citation Searching

Citation searching changed the evidence base in meaningful ways.

It:

- increased the corpus from 34 to 53 publications;
- expanded the study-family count from 27 to 44;
- recovered five pre-2010 foundational studies;
- increased the representation of socio-ecological, policy, environmental, and collective-resource research;
- increased the proportion of integrated-system studies;
- increased direct sustainability coverage;
- strengthened historical context for MAELIA, MP-MAS, SHADOC, irrigation governance, and related research lines.

At the same time, citation searching did **not** reverse the major conclusions of the original analysis.

Water management remains dominant.

Resource scarcity remains near-universal.

Simulation remains the dominant implementation maturity.

Operational deployment remains exceptional.

The expanded corpus therefore broadens and strengthens the interpretation without fundamentally changing the field-level picture.

---

## 12. Study-Family Sensitivity

The final 53 publications represent **44 independent study families**.

The seven multi-publication families are handled explicitly so that related papers are not automatically treated as independent corroboration.

Family-level sensitivity analyses broadly reproduce the publication-level patterns for:

- water-domain dominance;
- resource scarcity;
- direct sustainability;
- simulation maturity;
- coordination;
- environmental outcomes;
- code and data availability.

This indicates that the main review conclusions are not artefacts of repeated publication from a small number of research lines.

However, family aggregation should not be interpreted as:

- an effect-size meta-analysis;
- proof of independent replication;
- evidence that all publications in a family have identical methods;
- justification for collapsing contradictory publication-level classifications.

---

## 13. Evidence Qualifications

The following safeguards remain binding for subsequent taxonomy construction, research-gap analysis, PRISMA reporting, and final report writing.

1. **Outcome presence is not outcome improvement.**

2. **Simulation performance is not real-world effectiveness.**

3. **Scenario comparisons are not automatically rigorous experimental baselines.**

4. **Historical or observational fit supports model plausibility, not necessarily intervention effectiveness.**

5. **Family-level multi-label statistics are not mutually exclusive.**

6. **A modelled crop, cow, field, water body, or environmental entity is not automatically an autonomous software agent.**

7. **Auctions and markets should not automatically be classified as direct negotiation.**

8. **Environment-mediated interaction should not automatically be classified as direct communication.**

9. **SF42 retains paper-specific Hybrid/Hierarchical architecture differences.**

10. **S25 and S33 contain distinct harvest-comparison evidence and should not be conflated.**

11. **S49 and S53 belong to the same study family and should not be treated as independent replications.**

12. **S04 system-response metrics do not demonstrate improved cattle welfare.**

13. **S02 operational deployment remains independently unconfirmed.**

14. **Reviewer-coded limitation frequencies should not be presented as identical author statements.**

---

## 14. Overall Evidence Statement

The final Step 6G synthesis supports the following overall interpretation:

> **Multi-Agent Systems provide flexible mechanisms for representing heterogeneous agricultural decision-makers and coordinating constrained resources across irrigation, farm management, energy, labour, livestock, environmental, and socio-ecological settings. The evidence demonstrates substantial methodological and algorithmic maturity, but effectiveness is highly context dependent and remains supported predominantly by simulation rather than persistent real-world deployment.**

The strongest evidence concerns:

- constrained-resource coordination;
- irrigation and water management;
- operational allocation;
- decision support;
- socio-ecological simulation;
- policy and scenario analysis.

The evidence is weaker for:

- independently validated long-term operational deployment;
- generalisable causal claims;
- consistent livestock-welfare improvement;
- persistent environmental impact reduction;
- cross-site transferability;
- fully reproducible implementations.

The review therefore supports MAS as an important approach for agricultural coordination and sustainability-oriented decision modelling, while also identifying a substantial gap between **computational promise and operational evidence**.

---

## 15. Next Analytical Stages

The Step 6A–6G analytical synthesis is now reconciled and frozen for the next stages.

The next step is:

### Step 6H — MAS Taxonomy and Evidence Mapping

This stage will develop:

- the formal MAS taxonomy;
- architecture and agent-role cross-classifications;
- coordination and decision-mechanism mappings;
- agricultural-domain mappings;
- sustainability and outcome mappings;
- evidence-coverage matrices;
- publication-level and study-family evidence maps.

It will then be followed by:

### Step 6I — Consolidated Research Gaps

This stage will integrate:

- Step 6H evidence-map coverage;
- RQ0–RQ4 findings;
- reported limitations;
- author-reported future research needs;
- synthesis-derived evidence gaps.

Research gaps will be distinguished as:

1. **author-reported research gaps**;
2. **evidence-coverage gaps**;
3. **synthesis-derived gaps**.

Only after Steps **6H and 6I** are completed will the workflow proceed to:

```text
PRISMA 2020 reporting
        ↓
Zotero finalisation
        ↓
Final GitHub release update
        ↓
Final SLR report and presentation
```
