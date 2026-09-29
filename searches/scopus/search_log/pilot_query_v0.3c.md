# Pilot Query V0.3c — Scopus

**Status:** Frozen  
**Database:** Scopus  
**Search stage:** Phase 2.2 — Pilot query refinement and validation  
**Final date coverage:** 2010–2026  
**Language filter:** English  
**Document types:** Article and Conference Paper  

---

## 1. Purpose of V0.3c

Pilot Query V0.3c was developed as a precision-oriented refinement of V0.3b.

V0.3b achieved a strong relevance profile and successfully retrieved the diagnostic seed studies and broader positive-control studies, but the final filtered result set remained too large for the intended single-reviewer workflow:

| Query | Final filtered records |
|---|---:|
| V0.3 | 1,026 |
| V0.3a | 688 |
| V0.3b | 689 |
| **V0.3c** | **60** |

The objective of V0.3c was therefore not to change the research questions or narrow the substantive project scope arbitrarily. Instead, the query was redesigned so that retrieved records had to show stronger evidence that:

1. an explicit Multi-Agent System is central to the study;
2. the study is situated in an agricultural context;
3. at least one of the four focal project areas is central to the study; and
4. the MAS performs meaningful coordination, allocation, scheduling, control, or decision-making.

The four focal areas remain:

- irrigation and agricultural water management;
- shared-resource allocation and management;
- livestock and dairy-farm management;
- environmental sustainability and environmental-resource management.

The final query therefore remains aligned with the accepted project scope while substantially reducing the title/abstract screening workload.

---

## 2. Transition from V0.3b to V0.3c

### 2.1 Problem identified in V0.3b

V0.3b produced:

| Stage | Records |
|---|---:|
| Unfiltered V0.3b search | 902 |
| After 2010–2026 year filter | 818 |
| After English-language filter | 769 |
| After Article + Conference Paper filter | 689 |

Its first-30 relevance assessment was strong:

- Clearly relevant (R): 24/30
- Potentially relevant (P): 4/30
- Clearly irrelevant (I): 2/30
- R + P: 28/30 = 93.3%

However, **689 records remained substantially above the intended workload for a single reviewer**.

The problem was therefore no longer primarily irrelevant noise. The broader issue was that the query still admitted a large number of studies in which agriculture, MAS terminology, resource management, sustainability, or coordination concepts were present but not necessarily central to the same agricultural decision problem.

### 2.2 Design decision

V0.3c therefore moved from a broad recall-oriented query to a **precision-first centrality strategy**.

The final design requires the explicit MAS concept to be central enough to appear in the **title**, while the focal agricultural application is also required to be central.

Several broad retrieval pathways used in earlier pilots were removed from the primary query.

The final V0.3c does **not** use:

- generic `agent*`;
- generic `autonomous agent*`;
- generic `intelligent agent*`;
- broad `sustainab*`;
- broad abstract-only MAS retrieval;
- general author-keyword rescue pathways;
- generic path-planning or agricultural robotics terminology;
- a general agent-based modelling branch;
- `AND NOT` exclusions.

This change was intended to reduce retrieval volume through positive conceptual precision rather than through negative exclusion terms.

---

## 3. Search Logic

The final V0.3c contains two branches.

### Branch 1 — Main explicit-MAS pathway

A record must satisfy:

```text
Explicit MAS in TITLE
AND
Agricultural context in TITLE or ABSTRACT
AND
At least one focal application area in TITLE
AND
Meaningful coordination / allocation / decision activity in TITLE or ABSTRACT
```

This is the primary retrieval pathway.

### Branch 2 — Narrow agricultural-MAS recall repair

A record may also enter when:

```text
Agriculture is explicit in TITLE
AND
MAS is explicit in TITLE
AND
A focal agricultural activity is present in ABSTRACT
AND
A coordination / decision / control mechanism is present in ABSTRACT
```

This branch was retained because a clearly relevant agricultural MAS study can identify the agricultural MAS centrally in its title while describing irrigation, fertilization, harvesting, resource allocation, or environmental management primarily in the abstract.

The branch was deliberately kept narrow so that it does not reopen the broad abstract-based retrieval pathways removed from the main query.

---

## 4. Final Frozen V0.3c Query

```text
(
    TITLE(
        "multi-agent system*" OR
        "multi agent system*" OR
        "multiagent system*" OR
        "multi-agent" OR
        multiagent*
    )

    AND

    TITLE-ABS(
        agricultur* OR
        farming OR
        "smart farm*" OR
        "smart farming" OR
        "precision agriculture" OR
        "precision farming" OR
        irrigat* OR
        livestock OR
        "precision livestock" OR
        dairy OR
        cattle OR
        crop* OR
        pasture OR
        grazing OR
        farmer* OR
        grain*
    )

    AND

    TITLE(
        irrigat* OR
        "irrigation water" OR
        "water allocation" OR
        "water distribution" OR
        "water sharing" OR
        "water management" OR
        "water demand" OR
        "water scarcity" OR
        "soil moisture" OR

        livestock OR
        "precision livestock" OR
        dairy OR
        cattle OR
        herd* OR
        pasture OR
        grazing OR
        manure OR
        "animal welfare" OR

        "resource allocation" OR
        "resource sharing" OR
        "resource negotiation" OR
        "resource scheduling" OR
        "task allocation" OR

        "environmental sustainability" OR
        "climate adaptation" OR
        "climate mitigation" OR
        emission* OR
        methane OR
        "greenhouse gas*" OR
        "renewable energy" OR
        "energy management" OR
        "energy trading" OR
        "nutrient management" OR
        runoff OR
        "soil health" OR
        "soil degradation" OR
        "agricultural waste" OR
        "farm waste" OR
        microclimate
    )

    AND

    TITLE-ABS(
        coordinat* OR
        cooperat* OR
        negotiat* OR
        allocat* OR
        schedul* OR
        "resource sharing" OR
        "resource management" OR
        "decision support" OR
        "decision-making" OR
        "decision making" OR
        "integrated decision*" OR
        "distributed decision*" OR
        "collective decision*" OR
        "distributed control" OR
        "adaptive control" OR
        "peer-to-peer" OR
        auction* OR
        consensus
    )
)

OR

(
    TITLE(
        agricultur* OR
        farming OR
        "smart farm*" OR
        "smart farming" OR
        "precision agriculture"
    )

    AND

    TITLE(
        "multi-agent system*" OR
        "multi agent system*" OR
        "multiagent system*" OR
        "multi-agent" OR
        multiagent*
    )

    AND

    ABS(
        irrigat* OR
        fertiliz* OR
        harvest* OR
        livestock OR
        dairy OR
        pasture OR
        manure OR
        "resource allocation" OR
        "resource sharing" OR
        "resource scheduling" OR
        "energy management" OR
        "energy trading" OR
        "renewable energy" OR
        "climate adaptation" OR
        "climate mitigation" OR
        emission*
    )

    AND

    ABS(
        coordinat* OR
        cooperat* OR
        negotiat* OR
        allocat* OR
        schedul* OR
        "decision support" OR
        "decision-making" OR
        "decision making" OR
        "distributed control" OR
        "adaptive control" OR
        "tracking control"
    )
)
```

---

## 5. Alignment with the Research Questions

### RQ0 — Primary Research Question

**How have Multi-Agent Systems been designed, implemented, and evaluated for coordinated decision-making in smart agriculture, particularly for irrigation, shared-resource allocation, livestock management, and environmental sustainability?**

V0.3c operationalizes the core population and phenomenon of RQ0 through four mandatory concepts:

```text
Explicit Multi-Agent System
+
Agricultural context
+
Focal application area
+
Coordination / decision-making mechanism
```

The four focal application areas named in RQ0 are represented directly in the query.

### RQ1 — MAS architectures, agent roles, and decision-making

Architecture-specific terminology is **not made mandatory in the search query**.

Terms such as `architecture`, `BDI`, `belief`, `goal`, `utility`, or specific agent-role names were deliberately not required because relevant MAS studies may describe their architecture using different terminology.

RQ1 will instead be answered during data extraction using fields such as:

- MAS architecture;
- agent types and roles;
- degree of autonomy;
- agent responsibilities;
- decision mechanism;
- environmental or sensor inputs;
- state/belief representation where applicable.

### RQ2 — Coordination, negotiation, and shared-resource management

RQ2 is represented directly in the retrieval logic through terms including:

- `coordinat*`;
- `cooperat*`;
- `negotiat*`;
- `allocat*`;
- `schedul*`;
- resource sharing;
- resource management;
- decision support;
- distributed and collective decision-making;
- distributed and adaptive control;
- peer-to-peer mechanisms;
- auctions;
- consensus.

This helps distinguish meaningful MAS coordination from papers that only mention agents or agricultural technology without substantive interaction.

### RQ3 — Agricultural, livestock, resource, and environmental outcomes

The query directly represents the application areas needed for RQ3, including:

- irrigation and water allocation;
- livestock, dairy, pasture, grazing, and manure management;
- shared-resource allocation, negotiation, and scheduling;
- climate adaptation and mitigation;
- emissions and methane;
- renewable energy and energy management;
- nutrient management and runoff;
- soil health and degradation;
- agricultural waste;
- microclimate management.

Specific outcome measures such as water savings, yield changes, energy savings, emissions reductions, resource-utilisation efficiency, or livestock outcomes are **not mandatory retrieval terms**.

These are outcomes to be extracted from included studies rather than conditions for retrieval.

### RQ4 — Evaluation, limitations, and research gaps

Evaluation and limitation terminology is also **not made mandatory in the Boolean query**.

Requiring terms such as `evaluation`, `validation`, `limitation`, or `research gap` could exclude otherwise relevant studies whose abstracts do not use those exact expressions.

RQ4 will instead be answered during full-text extraction and quality assessment through:

- evaluation design;
- simulation or real-world deployment;
- evaluation metrics;
- datasets or environmental data;
- reproducibility;
- scalability;
- uncertainty;
- interoperability;
- explainability;
- computational requirements;
- deployment limitations;
- environmental-modelling limitations;
- reported research gaps.

---

## 6. Alignment with the Original Project Goal and Scope

The query preserves the original project progression:

```text
Agent architecture
→
Communication and coordination
→
Resource management
→
Agricultural outcomes
→
Environmental outcomes
```

The final search is intentionally concentrated around the central part of this chain:

```text
MAS
→
Coordination / decision-making
→
Agricultural resource or management problem
```

The remaining dimensions are investigated during data extraction.

The original conceptual farm-agent scope also remains compatible with the final query:

- Farm Management Agent;
- Weather Agent;
- Water / Resource Agent;
- Livestock Agent;
- Crop / Field Agent.

These literal role names are not required in the search because terminology differs substantially between studies.

The environmental scope also remains represented through concrete concepts rather than a broad generic sustainability wildcard.

Relevant environmental dimensions include:

- freshwater and water scarcity;
- greenhouse-gas emissions;
- methane;
- renewable energy;
- energy management and trading;
- fertilizer and nutrient management;
- runoff and pollution-related management;
- soil health and degradation;
- agricultural and farm waste;
- microclimate management;
- climate adaptation and mitigation.

---

## 7. Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.3c search | 72 |
| After 2010–2026 year filter | 64 |
| After English-language filter | 62 |
| After Article + Conference Paper filter | **60** |

### Preliminary Observation

V0.3c reduced the final Scopus candidate set from **689 records in V0.3b to 60 records**.

This represents a reduction of approximately **91.3%** in the final filtered Scopus workload.

The unfiltered result set decreased from **902 records in V0.3b to 72 records in V0.3c**, a reduction of approximately **92.0%**.

The date window was **not shortened** to achieve this reduction.

The original **2010–2026** period was retained so that the workload reduction came from stronger conceptual precision rather than an arbitrary temporal restriction.

This also preserves older relevant studies, including the 2013 irrigation/climate-services seed study.

---

## 8. Diagnostic Seed Validation

Three diagnostic seed studies had previously been used to test retrieval behaviour.

### S1

**Smart water management approach for resource allocation in High-Scale irrigation systems**  
DOI: `10.1016/j.agwat.2021.107088`

**V0.3c status:** Not retrieved by the primary query.

Within the final V0.3c result set:

- DOI-based search did not retrieve S1;
- title-based searching returned a different irrigation/multi-agent study rather than S1 itself.

This was an expected consequence of the precision-oriented redesign.

S1 primarily represents an **agent-based modelling / irrigation ABM pattern** rather than an explicitly titled Multi-Agent System study.

Earlier query versions showed that introducing general `agent-based model*` pathways substantially enlarged the candidate corpus.

For V0.3c, S1 is therefore retained as a **supplementary-search / snowballing seed**, not as a mandatory primary-query recall control.

S1 remains eligible for the review if full-text assessment confirms that its agents satisfy the substantive MAS inclusion criteria.

The study may be recovered through:

- backward citation searching;
- forward citation searching;
- seed-based related-paper searching;
- supplementary searching.

This distinction prevents broad agricultural ABM literature from dominating the primary database search while preserving the possibility of including MAS-like ABM studies that meet the review criteria.

### S2

**Water distribution in community irrigation using a multi-agent system**  
DOI: `10.1080/03036758.2022.2117830`

**V0.3c status:** Retrieved.

Validation:

- exact-title search: retrieved;
- DOI search: retrieved.

S2 provides a direct test of the irrigation, water-sharing, and explicit MAS components of the query.

### S3

**Multi-Agent Agro-Economic Simulation of Irrigation Water Demand with Climate Services for Climate Change Adaptation**  
DOI: `10.4081/ija.2013.e23`

**V0.3c status:** Retrieved.

Validation:

- exact-title search: retrieved;
- DOI search: retrieved.

S3 confirms that the precision-oriented redesign still retains older MAS work involving irrigation demand, farmer decision-making, and climate adaptation.

---

## 9. Positive-Control Validation

The positive-control set was revised for V0.3c so that mandatory controls correspond more directly to the final focal scope.

The generic UAV/robot path-optimization paper used during earlier broad-query diagnostics is no longer treated as a mandatory control because path optimization by itself is not one of the four focal application areas of the final review.

The following controls were retained because they directly test irrigation, shared resources, livestock management, agricultural decision-making, distributed control, or environmental management.

| Positive control | Representative review area | Retrieved by V0.3c |
|---|---|---|
| Modelling a multi agent system for dairy farms for integrated decision making | Livestock management and integrated farm decision-making | Yes |
| Distributed resource allocation: Generic model and solution based on constraint programming and multi-agent system for machine to machine services | Agricultural Decision Support System and distributed resource allocation | Yes |
| A Multi-agent Systems Approach for Peer-to-Peer Energy Trading in Dairy Farming | Dairy farming, shared energy resources, renewable energy, and sustainability | Yes |
| Human-in-the-Loop Tracking Control for Nonlinear Agricultural Multi-Agent Systems: A Fully Distributed Fuzzy Adaptive Method | Agricultural coordination and distributed/adaptive control | Yes |
| Multi-Agent System for Forecasting and Controlling the Microclimate in Grain Storage Facilities with Diverse Crops | Crop/storage management and environmental control | Yes |

Together with S2 and S3, these controls demonstrate retrieval across:

- irrigation and water management;
- distributed resource allocation;
- livestock and dairy-farm management;
- integrated agricultural decision-making;
- distributed and adaptive control;
- renewable-energy management;
- peer-to-peer resource coordination;
- grain-storage environmental control.

---

## 10. Human-in-the-Loop Recall Repair

During validation of the initial precision-oriented V0.3c structure, the following known relevant study was not retrieved:

**Human-in-the-Loop Tracking Control for Nonlinear Agricultural Multi-Agent Systems: A Fully Distributed Fuzzy Adaptive Method**  
DOI: `10.23919/CCC64809.2025.11179386`

The paper was considered important because its title explicitly identifies an **agricultural Multi-Agent System**, while the abstract describes focal agricultural activities and distributed/adaptive control.

The initial narrow recall branch required focal-topic and coordination terms to occur within a `W/5` proximity condition.

This was judged unnecessarily restrictive because the title already supplied strong evidence for both the agricultural context and the MAS methodology.

The second branch was therefore repaired from:

```text
ABS(
    focal-topic
    W/5
    coordination-function
)
```

to:

```text
ABS(focal-topic)
AND
ABS(coordination-function)
```

The relaxation applies only when both agriculture and the explicit MAS concept already appear in the title.

After this targeted repair:

- exact-title search retrieved the Human-in-the-Loop study;
- DOI search retrieved the Human-in-the-Loop study;
- the final filtered corpus increased only to **60 records**.

This repair was therefore accepted because it recovered a clearly relevant false negative without reopening a broad abstract-only retrieval pathway.

No additional paper-specific OR branches were added.

---

## 11. Relevance and Noise Assessment

To evaluate the precision of the frozen V0.3c, the first **30 records** of the final filtered Scopus result set were inspected after sorting by **Scopus relevance**.

The assessment used:

- title;
- abstract;
- author keywords;
- indexed keywords.

This assessment is a **search-query diagnostic only**.

It does not replace the formal title/abstract screening of all 60 retrieved records.

### Classification Scheme

- **R — Clearly relevant:** directly fits the agricultural MAS and focal review scope.
- **P — Potentially relevant:** plausibly relevant, but title/abstract information is insufficient for a confident inclusion decision.
- **I — Clearly irrelevant:** does not fit the central review scope.

### Classification Results

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 23 | 76.7% |
| Potentially relevant (P) | 2 | 6.7% |
| Clearly irrelevant (I) | 5 | 16.7% |

Overall:

**25 of the first 30 records (83.3%) were clearly relevant or potentially relevant.**

---

## 12. Comparison with Earlier Relevance Pilots

| Query | R + P | Percentage |
|---|---:|---:|
| V0.1 | 17/30 | 56.7% |
| V0.3 | 22/30 | 73.3% |
| V0.3b | 28/30 | 93.3% |
| **V0.3c** | **25/30** | **83.3%** |

V0.3c has a lower first-30 R+P percentage than V0.3b.

However, the difference must be interpreted together with retrieval workload:

| Query | Final filtered records |
|---|---:|
| V0.3b | 689 |
| **V0.3c** | **60** |

V0.3c therefore trades a modest decrease in the diagnostic relevance rate for an approximately **91.3% reduction in the Scopus candidate corpus**.

For the single-reviewer project, this was judged to provide a substantially better balance between precision, recall validation, scope coverage, and practical screening workload.

---

## 13. Irrelevant-Record Diagnostic

The same diagnostic categories used in the earlier pilot documentation were retained.

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 2 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other | 3 |

### I1 — Non-agricultural applications

Two records were classified as I1.

The observed cases included:

- a vehicular/edge-network bandwidth-allocation study without a substantive agricultural application;
- an urban water-energy-food-greenhouse-gas management study in which the main decision problem was urban water management and agriculture was peripheral.

### I7 — Agricultural but peripheral technical applications

Three clearly irrelevant records were assigned to I7 because they were genuinely connected to agriculture but the MAS was primarily used for technical functions outside the central review focus.

The observed patterns were:

1. multi-UAV / wireless-sensor-network task scheduling and energy/resource sharing where the primary problem was communication and network infrastructure;
2. livestock knowledge-graph construction where agents primarily performed information extraction, ontology normalization, relation extraction, and knowledge fusion;
3. agricultural heterogeneous-network resource allocation where the primary allocation problem concerned communication-network resources and quality of service.

These studies are close semantic neighbours of the review topic, but they do not primarily address coordinated farming decisions, agricultural resource management, livestock operational management, irrigation management, or environmental management.

---

## 14. Primary Noise Source

The dominant noise pattern in V0.1 was non-agricultural retrieval, especially records matched through broad terms such as `farm*`.

V0.3b largely solved that problem but retained a very large candidate set.

V0.3c changes the noise profile again.

The remaining noise is limited mainly to:

- non-agricultural multi-agent resource-allocation/control studies that happen to satisfy some contextual terms; and
- genuinely agricultural technology papers whose multi-agent component performs peripheral infrastructure or information-processing functions.

Importantly, the first-30 V0.3c sample did **not** show evidence that generic IoT-only studies, conventional ML-only studies, unrelated uses of the word "agent", or broad agricultural ABM studies were major remaining noise sources.

The residual noise is considered manageable during formal title/abstract screening.

---

## 15. Observed Terminology

Relevant and potentially relevant V0.3c records contained terminology including:

- multi-agent systems / multiagent systems;
- multi-agent digital twins;
- game-theoretic multi-agent coordination;
- multi-agent reinforcement learning;
- autonomous irrigation;
- irrigation scheduling;
- water distribution;
- water scarcity;
- auction-based water allocation;
- resource sharing;
- distributed resource allocation;
- distributed optimization;
- task allocation;
- hierarchical and cooperative control;
- adaptive control;
- climate services;
- sustainable agriculture;
- dairy-farm decision-making;
- peer-to-peer energy trading;
- renewable-energy management;
- grain-storage microclimate control;
- farm decision-support systems.

These terms are retained in the terminology log for interpretation and data extraction.

They are **not automatically added to the Boolean query**, because repeatedly expanding the query from every observed synonym was one of the causes of excessive retrieval volume during earlier pilots.

---

## 16. Date-Range Decision

A shorter date window was considered because of the single-reviewer workload.

However, after the V0.3c redesign the final Scopus corpus decreased to only **60 records** while retaining the existing **2010–2026** window.

The date range was therefore not reduced.

Reasons:

- the workload is now manageable at the Scopus stage;
- the project is not restricted to only recent or post-2020 MAS research;
- retaining 2010–2026 preserves historical development within the review period;
- older known relevant work, including S3 from 2013, remains searchable;
- reducing the date range solely to meet a numerical target would be less defensible than reducing workload through conceptually justified query precision.

The 2010–2026 period is therefore retained for V0.3c.

---

## 17. Interpretation of the 60-Record Corpus

The **60 records are title/abstract screening candidates**, not 60 papers automatically requiring full-text review.

The formal workflow remains:

```text
60 Scopus records
↓
Import into Rayyan
↓
Deduplication
↓
Title / abstract screening
↓
Full-text eligibility assessment
↓
Quality assessment
↓
Data extraction
↓
Synthesis for RQ0–RQ4
```

The number proceeding to full-text assessment will depend on application of the predefined inclusion and exclusion criteria.

The 60-record figure also represents **Scopus only**.

Searches in the other planned databases may add records, although substantial duplication across databases is expected.

The single-reviewer workload threshold should ultimately be judged using the **deduplicated multi-database corpus**, not by summing raw database result counts.

---

## 18. V0.3c Diagnostic Conclusion

Pilot Query V0.3c produced:

- **72 unfiltered records**;
- **64 records after the 2010–2026 filter**;
- **62 records after the English-language filter**;
- **60 records after restricting document type to Article and Conference Paper**.

The first-30 relevance assessment found:

- **23 clearly relevant records (76.7%)**;
- **2 potentially relevant records (6.7%)**;
- **5 clearly irrelevant records (16.7%)**;
- **25/30 records (83.3%) relevant or potentially relevant**.

Compared with V0.3b, V0.3c reduced the final filtered Scopus candidate corpus from **689 to 60 records**, a reduction of approximately **91.3%**.

The query retained the explicit-MAS diagnostic seeds S2 and S3 and the focal positive controls covering:

- irrigation and water management;
- agricultural resource allocation;
- livestock and dairy management;
- integrated farm decision-making;
- distributed/adaptive agricultural control;
- renewable-energy and peer-to-peer coordination;
- environmental and microclimate management.

S1 was not retrieved by the primary query because the final design deliberately does not include a broad agricultural agent-based-modelling pathway. S1 is retained as a supplementary-search and snowballing seed and remains eligible if it satisfies the review's substantive MAS criteria.

A targeted repair to the second query branch successfully recovered the Human-in-the-Loop agricultural MAS control without materially increasing the workload.

V0.3c therefore provides a substantially improved balance between:

- alignment with RQ0–RQ4;
- coverage of the original project scope;
- retrieval precision;
- preservation of important explicit-MAS controls;
- historical coverage;
- and feasibility for a single reviewer.

**Decision: V0.3c is frozen as the final Scopus query for the current SLR protocol.**

No further Boolean refinement will be performed unless a later validation step identifies a substantive scope or recall failure.

---

## 19. Repository and Data-Handling Note

The public repository should contain:

- this query documentation;
- search date;
- database name;
- applied filters;
- result counts;
- seed and positive-control validation;
- relevance/noise assessment;
- methodological decisions and rationale.

Raw Scopus CSV/RIS exports containing licensed database metadata or abstracts should be retained privately rather than committed to the public repository.

Formal deduplication and screening decisions should be maintained in Rayyan, while Zotero can be used as the permanent literature/PDF and citation library.
