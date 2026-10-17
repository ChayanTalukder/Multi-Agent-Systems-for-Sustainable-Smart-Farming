# Step 6I — Consolidated Research Gaps

## 1. Scope and method

Step 6I consolidates the final review's research gaps after completion of the formal MAS taxonomy and evidence mapping.

The analysis uses three evidence layers:

1. **Author-reported research gaps** — manually coded from the `Reported_Research_Gaps` field in the final 53-publication extraction.
2. **Corpus-level evidence gaps** — derived from the Step 6H taxonomy, cross-classifications and evidence-maturity map.
3. **Synthesis-derived gaps** — derived from the reconciled RQ0–RQ4 findings and Step 6G evidence-strength safeguards.

The final corpus contains **53 publications representing 44 study families**. Substantive `Reported_Research_Gaps` text is available for **49/53 publications**; S23, S24, S31 and S32 are recorded as `NR`.

Author-gap categories are **multi-label reviewer-coded themes**. A count does not mean that every author used identical terminology. At family level, a family is counted once when at least one included publication in that family supports the theme.

Sparse or absent taxonomy cells are not treated automatically as research gaps.

## 2. Author-reported gap themes

| Code | Author-reported gap theme | Publications | Study families |
|---|---|---:|---:|
| G1 | Field, operational and longitudinal validation | 28/53 (52.8%) | 23/44 (52.3%) |
| G2 | Behavioural, stakeholder and social validity | 25/53 (47.2%) | 24/44 (54.5%) |
| G3 | Robustness, uncertainty and transferability | 29/53 (54.7%) | 28/44 (63.6%) |
| G4 | Comparative evaluation and alternative mechanisms | 9/53 (17.0%) | 7/44 (15.9%) |
| G5 | Scalability, sensing, computation and real-time operation | 14/53 (26.4%) | 13/44 (29.5%) |
| G6 | Biophysical/environmental realism and long-horizon sustainability | 23/53 (43.4%) | 22/44 (50.0%) |
| G7 | Cross-domain, whole-farm and multi-resource integration | 12/53 (22.6%) | 12/44 (27.3%) |
| G8 | Adaptive, distributed and institutionally realistic coordination | 19/53 (35.8%) | 16/44 (36.4%) |

The largest author-reported themes concern **robustness/transferability**, **field or operational validation**, **behavioural/stakeholder validity**, and **biophysical/environmental realism**. These themes appear across many independent study families rather than being confined to one publication line.

## 3. Final consolidated research-gap priorities

### RG1 — Field, operational and longitudinal validation — Priority A

The strongest gap is the transition from model-based evidence to credible operational evidence.

The corpus remains dominated by simulation, and most publications do not document real-world MAS deployment. Author-reported future work repeatedly calls for field trials, working-farm evaluation, independent datasets, multi-site testing, commercial deployment, stakeholder validation, or longitudinal evidence.

**Research priority:** evaluate MAS prospectively across multiple seasons, sites and operational conditions, and report sensing, communication, human decision, failure and maintenance conditions alongside outcome metrics.

**Boundary:** a field-related dataset, calibration exercise, prototype, or field-pilot label is not itself evidence of sustained operational effectiveness.

### RG2 — Robustness, uncertainty and transferability — Priority A

A second pervasive gap is the limited evidence that results transfer across weather, soil, crop, market, behavioural and sensing conditions.

The author-gap coding identifies this theme in **29/53 publications and 28/44 families**. The RQ3 synthesis also shows that many outcomes are mixed, trade-off-sensitive or scenario-dependent.

**Research priority:** use systematic uncertainty analysis, heterogeneous agents/environments, noisy sensing, multiple seasons and sites, and explicit transfer/generalisation tests.

**Boundary:** successful performance in one historical or simulated configuration should not be generalised automatically to other agricultural settings.

### RG3 — Behavioural, stakeholder and social validity — Priority A

Farmer, household, worker, manager and institutional agents are central to the taxonomy, but many studies rely on stylised decision rules, assumed preferences, simplified cooperation, or limited stakeholder authentication.

The author-gap coding identifies this theme in **25/53 publications and 24/44 families**.

**Research priority:** ground behavioural rules in interviews, surveys, historical decisions, participatory modelling, field observation or other empirical evidence; explicitly represent heterogeneity, preferences, learning, institutional rules, legitimacy and distributional consequences when relevant.

**Boundary:** adding behavioural complexity without empirical grounding does not automatically improve validity.

### RG4 — Biophysical/environmental realism and long-horizon sustainability — Priority A

Although sustainability is explicit in much of the corpus, environmental benefit is often modelled rather than measured, and many studies call for richer hydrology, soil, crop, nutrient, livestock, emissions, climate or long-term sustainability representation.

The author-gap coding identifies this theme in **23/53 publications and 22/44 families**.

**Research priority:** connect agent decisions to credible biophysical processes and long-horizon environmental outcomes, including uncertainty and rebound/trade-off effects.

**Boundary:** a better optimisation objective or lower simulated resource use is not automatically evidence of real environmental improvement.

### RG5 — Reproducibility and transparent research artefacts — Priority A

This gap is primarily synthesis-derived rather than an author-frequency claim.

Reported implementation code is available for only **8/53 publications**, and reported data availability for **14/53**. Reproducibility/data-availability limitations are also common in the extraction.

**Research priority:** publish or document implementation code, model parameters, input data, seeds, scenario definitions, evaluation procedures and dependency information wherever licensing and privacy permit.

**Boundary:** reported availability does not guarantee that an artefact is complete, executable or independently reproducible.

### RG6 — Comparative evaluation and baseline quality — Priority A

The review contains algorithmic comparisons, historical-practice comparisons, scenario counterfactuals, calibrations and ablations, but these support different strengths of inference.

The author-gap coding identifies explicit requests for additional comparator/mechanism evaluation in **9/53 publications and 7/44 families**, while the RQ4 adjudication shows a broader need to distinguish comparator strength consistently.

**Research priority:** select transparent comparators matched to the claim being made and clearly distinguish model-internal scenario comparisons from external or operational validation.

**Boundary:** a populated comparator field is not equivalent to a rigorous control.

### RG7 — Scalability, sensing, computation and real-time operation — Priority B

The author-gap coding identifies this theme in **14/53 publications and 13/44 families**.

The literature calls for faster training/optimisation, scalable coordination, state estimation, edge operation, collision/path planning, communication efficiency, real-time control and better sensing/data-quality handling.

**Research priority:** evaluate compute, communication, sensing, latency and failure costs as system size and heterogeneity increase.

**Boundary:** computational scalability in simulation does not establish deployability under real sensing, networking and actuation constraints.

### RG8 — Cross-domain and multi-resource integration — Priority B

The author-gap coding identifies this theme in **12/53 publications and 12/44 families**.

The corpus already contains many integrated-system studies, so the gap is not simply a lack of integration. Rather, coupling remains uneven across water, energy, nutrients, livestock, labour, machinery, markets and land-use processes.

**Research priority:** integrate interacting resource domains where cross-system feedback materially changes decisions or sustainability outcomes.

**Boundary:** integration should be problem-driven; unnecessary coupling can increase calibration burden and reduce interpretability.

### RG9 — Adaptive, distributed and institutionally realistic coordination — Priority B

The author-gap coding identifies this theme in **19/53 publications and 16/44 families**.

Step 6H shows that learning-based adaptive coordination and direct negotiation are smaller strands than hierarchical, environment-mediated and optimisation-based coordination. Several authors propose MARL, distributed optimisation, richer auctions, bargaining, coalition formation or collective-action mechanisms.

**Research priority:** evaluate adaptive/distributed mechanisms where ownership, uncertainty, decentralised information or shared-resource governance makes them meaningful, and compare them against simpler alternatives.

**Boundary:** low prevalence of MARL, negotiation or distributed architectures is not by itself evidence that those methods should be used more widely.

## 4. Coverage-derived evidence gaps by application domain

The Step 6H evidence map adds several domain-level signals:

- **Irrigation/water management** is the largest and most structurally diverse domain, but 23/24 publications are still simulation maturity. This strengthens RG1 rather than creating a new irrigation-specific gap.
- **Energy/WEF** contains five publications but only three study families, all simulation-based. This supports RG1 and RG8.
- **Soil/nutrient/environmental management** contains only four study families and is entirely simulation-based. This supports RG1 and RG4.
- **Livestock/integrated farming** contains more prototype/decision-support work than most domains, but the adjudicated outcome evidence is primarily mixed, descriptive or non-directional. This supports stronger outcome validation rather than a claim that the approaches are ineffective.
- **Workforce/robotics** is strongly centralised and optimisation-oriented and contains no direct-sustainability-coded publications in the current extraction. This is a legitimate coverage signal for human/environmental integration, but absent peer, negotiation or learning mechanisms should not automatically be labelled deficiencies.

## 5. Sparse areas that are not promoted to standalone research gaps

The following are deliberately **not** treated as final research gaps:

- only two distributed-architecture publications;
- only one LLM-based publication;
- sparse direct negotiation outside irrigation;
- sparse learning-based coordination in several domains;
- only two decision-support/monitoring publications;
- empty domain × mechanism cells in the Step 6H matrix.

These observations describe the corpus, but a missing mechanism may simply be inappropriate for the problem.

For example, the review does **not** support claims that agricultural MAS generally need more distributed architectures, more MARL, more LLM agents, or more negotiation.

## 6. Final hierarchy for the SLR

### Priority A — strongest, cross-validated gaps

1. Field, operational and longitudinal validation.
2. Robustness, uncertainty and transferability.
3. Behavioural, stakeholder and social validity.
4. Biophysical/environmental realism and long-horizon sustainability.
5. Reproducibility and transparent research artefacts.
6. Comparative evaluation and baseline quality.

### Priority B — important but more context-dependent gaps

7. Scalability, sensing, computation and real-time operation.
8. Cross-domain and multi-resource integration.
9. Adaptive, distributed and institutionally realistic coordination.

This hierarchy should be used in the final SLR report. It is more defensible than ranking gaps solely by publication frequency because it triangulates author statements, corpus coverage and evidence-strength limitations.

## 7. Step 6I conclusion

The principal limitation of the agricultural MAS evidence base is **not a lack of proposed architectures or algorithms**. The larger problem is the distance between increasingly sophisticated coordination models and strong evidence that they remain robust, reproducible, socially valid and environmentally beneficial under real agricultural conditions.

The formal taxonomy shows substantial methodological diversity. The research-gap synthesis therefore prioritises **evidence quality, transferability and operational validity** before simply calling for more complex MAS techniques.

With Step 6I complete, the analytical sequence in the planned workflow is complete:

```text
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
```

The next stage is **Step 7 — Final PRISMA 2020 Reporting**.
