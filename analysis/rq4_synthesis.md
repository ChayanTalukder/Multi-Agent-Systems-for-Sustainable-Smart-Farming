# RQ4 — Evaluation, Implementation Maturity, Limitations, and Research Gaps

**RQ4:** *How are agricultural Multi-Agent Systems evaluated, and what methodological, technical, and practical limitations or research gaps are reported in the literature?*

The final RQ4 synthesis uses **53 included publications (S01–S53)** as the primary unit of analysis and **44 reconciled study families** as an evidence-independence sensitivity check.

Family-level values indicate whether at least one publication in a study family contains the relevant characteristic. Because different publications from the same family may report different evaluation settings or maturity levels, family-level multi-label counts are not necessarily mutually exclusive.

---

## 1. Implementation Maturity

Implementation maturity was extracted as a publication-level categorical field.

| Implementation maturity | Original 34 | Final 53 | 44-family evidence |
|---|---:|---:|---:|
| Simulation | 27 (79.4%) | 46 (86.8%) | 39 (88.6%) |
| Prototype | 4 (11.8%) | 4 (7.5%) | 3 families |
| Field pilot | 2 (5.9%) | 2 (3.8%) | 2 families |
| Controlled experiment | 1 (2.9%) | 1 (1.9%) | 1 family |

The evidence base is therefore overwhelmingly **simulation-oriented**.

Citation searching strengthened rather than reduced this pattern because several newly retrieved foundational socio-ecological and resource-management publications were simulation studies.

Implementation maturity must also be distinguished from real-world deployment. A publication may use real agricultural data, a real geographical case study, or a cyber-physical component without demonstrating a fully operational MAS in routine farm use.

---

## 2. Real-World Deployment

The extracted `Real_World_Deployment` field records:

```text
No        51
Yes        1
Partial    1
```

The source-coded `Yes` publication is **S02**, while **S06** is coded `Partial`.

These values require conservative interpretation.

The accessible evidence for S02 supports the design of a smart-farming multi-agent platform and associated services, but the targeted source check did **not** establish sufficiently strong evidence of persistent operational on-farm deployment.

S06 contains partial physical/cyber-physical irrigation evidence, but this is not equivalent to prospective validation of long-term farm effectiveness.

Accordingly, the final review should state that **real-world deployment is rare and incompletely established**.

It should **not** state that two independent operational deployments were conclusively verified.

---

## 3. Evaluation Designs

The extraction records describe several overlapping evaluation approaches.

| Evaluation description | Final 53 | 44 families |
|---|---:|---:|
| Simulation mentioned | 50 (94.3%) | 42 (95.5%) |
| Case-study evaluation mentioned | 37 (69.8%) | 32 (72.7%) |
| Comparative evaluation / benchmarking mentioned | 25 (47.2%) | 21 (47.7%) |
| Sensitivity / robustness / uncertainty analysis mentioned | 13 (24.5%) | 12 (27.3%) |
| Validation or calibration explicitly mentioned | 15 (28.3%) | 15 (34.1%) |

These categories are overlapping and were derived from the evaluation descriptions recorded during extraction.

They describe **what type of evaluation activity is reported**, not a uniform grading of evidence quality.

For example, the presence of the word `validation` may refer to:

* calibration against historical observations;
* comparison with observed spatial or production patterns;
* internal model validation;
* retrospective case-study evaluation;
* or, much more rarely, prospective physical testing.

These forms of evidence should not be treated as equivalent.

---

## 4. Comparator and Baseline Strength

The original extraction field `Baselines_Comparators` is populated for most studies, but a populated comparator description does **not** imply the presence of a rigorous experimental control.

The Step 6G adjudication therefore distinguishes several kinds of comparison.

| Comparator description | Safe interpretation |
|---|---|
| Explicit algorithmic or heuristic comparator | Relative performance within the specified experimental setting |
| Historical or operational practice | Descriptive comparison with observed or existing practice; not automatically causal |
| Alternative policy or scenario | Model-internal counterfactual or scenario comparison |
| Calibration or observational fit | Evidence of model plausibility or correspondence with observations |
| Ablation or system-component comparison | Evidence concerning the contribution of a particular model or system component |
| None / NR / unspecified | Feasibility or descriptive evidence only |

Comparator types may overlap within a publication.

The earlier observation that **49/53 publications contain non-empty comparator text must not be reported as 49 rigorous baselines**.

Likewise, no definitive source-verified frequency distribution of strong versus weak comparator designs is claimed for all 53 publications.

The comparator analysis is therefore used primarily to constrain interpretation of individual results rather than to create an artificial evidence-quality ranking.

---

## 5. Reproducibility and Research Artefacts

Reported accessibility of implementation artefacts remains limited.

| Indicator | Original 34 | Final 53 | 44 families |
|---|---:|---:|---:|
| Code available | 3 (8.8%) | 8 (15.1%) | 8 (18.2%) |
| Data available | 6 (17.6%) | 14 (26.4%) | 13 (29.5%) |

Citation searching improves the apparent availability of code and data, but the majority of the corpus still lacks clearly accessible implementation artefacts.

These fields record **reported availability**. They do not establish that every repository, dataset, configuration, dependency, or experiment can be independently reproduced without additional information.

---

## 6. Reported and Reviewer-Coded Limitations

The structured extraction identified several recurring limitation categories.

| Limitation category | Final 53 | 44 families |
|---|---:|---:|
| Need for real-world validation | 52 (98.1%) | 43 (97.7%) |
| Uncertainty | 35 (66.0%) | 29 (65.9%) |
| Reproducibility / data availability | 18 (34.0%) | 17 (38.6%) |
| Environmental modelling | 18 (34.0%) | 17 (38.6%) |
| Computational requirements | 17 (32.1%) | 12 (27.3%) |
| Scalability | 11 (20.8%) | 9 (20.5%) |
| Explainability | 1 (1.9%) | 1 (2.3%) |
| Interoperability | 1 (1.9%) | 1 (2.3%) |
| Deployment cost | 1 (1.9%) | 1 (2.3%) |

These are **reviewer extraction codes** derived from study limitations and evidence context.

The frequency `52/53` for real-world validation must therefore not be described as 52 authors independently making the exact same recommendation.

Similarly, the low explicit coding frequencies for explainability, interoperability, or deployment cost do not demonstrate that these problems are solved or unimportant. They indicate that they are comparatively underrepresented in the extracted limitation reporting.

---

## 7. Evaluation Strength and Evidence Boundaries

Several safeguards are required when interpreting the RQ4 evidence.

### Simulation is not deployment

Real weather, farm, sensor, market, or spatial data can make a simulation more realistic, but do not by themselves constitute operational deployment.

### Calibration is not effectiveness validation

A model reproducing historical observations or known spatial patterns provides evidence of plausibility, but it does not demonstrate that the proposed MAS intervention will improve real agricultural outcomes prospectively.

### Scenario comparison is not a causal control

Alternative policies, behavioural assumptions, drought scenarios, or parameter settings are useful for model analysis, but they are not equivalent to randomised or controlled operational comparisons.

### Algorithmic superiority is context-specific

A MAS algorithm outperforming another optimiser or heuristic under a particular dataset, parameterisation, or simulation environment supports a relative computational result. It does not automatically establish superiority under real farming conditions.

### Study-family overlap matters

Multiple publications from one study family may describe related experiments, datasets, platforms, or extensions. Their results should not be counted automatically as independent replications.

---

## 8. Research Needs Emerging from RQ4

The RQ4 evidence consistently points toward several broad research needs:

1. **Prospective field validation**  
   Evaluate MAS under monitored farm conditions across multiple seasons, farms, and environmental settings.

2. **Robustness and transferability**  
   Test changing weather, soil, crop, livestock, market, behavioural, and resource conditions beyond the original calibration setting.

3. **Stronger comparative evaluation**  
   Use clearly defined operational practices, non-MAS controls, algorithmic benchmarks, or other defensible comparators appropriate to the research question.

4. **Reproducibility**  
   Provide code, datasets, configuration information, parameter values, seeds, scenario definitions, and evaluation procedures where possible.

5. **Scalability and operational cost**  
   Evaluate computational requirements, communication overhead, sensing requirements, physical constraints, and deployment costs at realistic scales.

6. **Environmental and social validity**  
   Evaluate long-term environmental outcomes, distributional effects, fairness, rebound effects, farmer behaviour, and institutional constraints rather than assuming that optimisation objectives directly represent sustainability.

7. **Human oversight, explainability, and interoperability**  
   Examine how agricultural users interpret MAS recommendations and how multi-agent tools can integrate with existing farm-management systems, IoT infrastructure, and institutional processes.

These themes are important inputs to **Step 6I — Consolidated Research Gaps**.

They should not yet be treated as a final prioritised gap taxonomy, because Step 6I will combine RQ4 with the Step 6H evidence map, RQ0–RQ3 findings, author-reported gaps, and synthesis-derived coverage gaps.

---

## 9. Study-Family Sensitivity

The principal RQ4 conclusions remain stable after accounting for related publications.

Simulation maturity appears in:

- **46/53 publications (86.8%)**;
- **39/44 study families (88.6%)**.

Reported code availability appears in:

- **8/53 publications**;
- **8/44 study families**.

Reported data availability appears in:

- **14/53 publications**;
- **13/44 study families**.

The need for stronger real-world validation also remains pervasive after study-family aggregation.

Therefore, the main RQ4 conclusions are not explained simply by repeated publications from the same research lines.

However, family-level prevalence does **not** constitute independent experimental replication and should not be interpreted as a meta-analytic effect estimate.

---

## 10. Direct Answer to RQ4

Agricultural Multi-Agent Systems are evaluated predominantly through **simulation, case studies, scenario comparisons, algorithmic experiments, calibration, and retrospective validation**.

A substantial portion of the literature includes structured comparative evaluation, sensitivity analysis, or observational calibration, but these forms of evidence vary markedly in strength and should not be conflated with prospective operational validation.

The evidence base remains strongly simulation-dominated, while confirmed real-world deployment is exceptional and incompletely documented.

Code and data availability improve in the expanded corpus but remain limited, constraining reproducibility and cross-study comparison.

The most important methodological challenges concern:

- real-world validation;
- robustness under uncertainty;
- appropriate comparator design;
- reproducibility;
- scalability;
- realistic environmental and social modelling;
- practical integration with agricultural users and infrastructure.

Overall, RQ4 shows that agricultural MAS have substantial **modelling and algorithmic maturity**, but the central unresolved challenge is translating promising computational results into **robust, reproducible, and empirically validated agricultural systems**.
