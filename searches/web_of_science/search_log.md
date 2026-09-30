# Pilot Query V0.3c — Web of Science

**Status:** Frozen  
**Database:** Web of Science Core Collection  
**Search interface:** Advanced Search → Query Builder  
**Search date:** 29–30 September 2026  
**Protocol period:** 2010–2026  
**Language:** English  
**Document types:** Article and Proceedings Paper  
**Final filtered records:** 51  

---

## 1. Purpose

The Web of Science search is a database-specific translation of the frozen Scopus V0.3c strategy.

The conceptual search logic was kept unchanged:

```text
Explicit Multi-Agent System
AND
Agricultural context
AND
Focal agricultural/resource/environmental application
AND
Coordination / allocation / decision / control mechanism
```

The focal review areas remain:

- irrigation and agricultural water management;
- shared-resource allocation and management;
- livestock and dairy-farm management;
- environmental sustainability and environmental-resource management.

Unlike IEEE Xplore, Web of Science supports sufficiently expressive title and abstract field queries, so the two V0.3c branches could be retained in a single Boolean search.

---

## 2. Database-Specific Translation

The Scopus fields were translated as follows:

```text
Scopus TITLE(...)     → WoS TI=(...)
Scopus ABS(...)       → WoS AB=(...)
Scopus TITLE-ABS(...) → WoS (TI=(...) OR AB=(...))
```

`TI` and `AB` were preferred over the broader Web of Science `TS` Topic field so that retrieval remained as close as possible to the frozen Scopus title/abstract strategy.

The Web of Science query retained wildcards because the platform supports truncation expressions such as:

```text
agricultur*
irrigat*
coordinat*
allocat*
```

No database-specific expansion was added unless required by recall validation.

---

## 3. Final Frozen V0.3c Query

```text
(
    TI=(
        "multi-agent system*" OR
        "multi agent system*" OR
        "multiagent system*" OR
        "multi-agent" OR
        multiagent*
    )

    AND

    (
        TI=(
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

        OR

        AB=(
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
    )

    AND

    TI=(
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

    (
        TI=(
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

        OR

        AB=(
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
)

OR

(
    TI=(
        agricultur* OR
        farming OR
        "smart farm*" OR
        "smart farming" OR
        "precision agriculture"
    )

    AND

    TI=(
        "multi-agent system*" OR
        "multi agent system*" OR
        "multiagent system*" OR
        "multi-agent" OR
        multiagent*
    )

    AND

    AB=(
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

    AB=(
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

## 4. Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.3c | 61 |
| After 2010–2026 filter | 52 |
| After English-language filter | 51 |
| After Article / Proceedings Paper filter | **51** |

The document-type restriction caused no further reduction after the language filter.

The final Web of Science candidate corpus is therefore:

```text
51 records
```

---

## 5. Recall Validation

Known studies were checked using exact-title and DOI searches.

For searches within the V0.3c result set:

```text
#N AND TI=("exact title")
#N AND DO=(DOI)
```

For full Web of Science Core Collection indexing checks:

```text
TI=("exact title")
DO=(DOI)
```

This allowed non-retrieval to be distinguished from non-indexing.

### Validation Results

| Control | Retrieved by V0.3c | WoS indexing / interpretation |
|---|:---:|---|
| S1 — Smart water management approach for resource allocation in High-Scale irrigation systems | No | Indexed; retained as supplementary/snowballing seed |
| S2 — Water distribution in community irrigation using a multi-agent system | **Yes** | Title and DOI retrieved |
| S3 — Multi-Agent Agro-Economic Simulation of Irrigation Water Demand with Climate Services for Climate Change Adaptation | **Yes** | Title and DOI retrieved |
| Dairy integrated decision-making | No | Not found in full WoS Core Collection |
| Resource-allocation DSS | No | Not found by title or DOI in full WoS Core Collection |
| Dairy peer-to-peer energy trading | **Yes** | Title and DOI retrieved |
| Human-in-the-Loop agricultural MAS | **Yes** | Retrieved by exact title |
| Grain-storage microclimate MAS | **Yes** | Retrieved by exact title |

The missing DOI matches for the Human-in-the-Loop and grain-storage records were not treated as retrieval failures because the corresponding records were directly present in the V0.3c result set by exact title.

---

## 6. S1 Decision

S1:

**Smart water management approach for resource allocation in High-Scale irrigation systems**  
DOI: `10.1016/j.agwat.2021.107088`

is indexed in Web of Science but is not retrieved by the primary V0.3c query.

This behaviour is consistent with the earlier Scopus V0.3c decision.

S1 represents the broader agricultural agent-based-modelling pathway rather than an explicitly titled MAS study. Earlier pilot searches showed that broad ABM retrieval substantially increased the candidate corpus.

Therefore:

```text
S1 remains eligible as a supplementary-search /
backward-forward citation-searching seed.

Its absence does not trigger expansion of the
primary V0.3c Boolean query.
```

No broad `agent-based model*` branch was added.

---

## 7. Query-Repair Decision

No Web of Science-specific query repair was required.

In particular, the generic `control` repair added during IEEE Xplore validation was **not** copied automatically into Web of Science.

The reason is empirical:

```text
Grain-storage microclimate control → retrieved
Human-in-the-Loop control          → retrieved
```

Therefore, the existing WoS translation already provided adequate recall for the relevant control-oriented studies.

Database-specific repairs are applied only where an actual false negative demonstrates a need.

---

## 8. Relevance / Noise Diagnostic

The first 30 records of the final 51-record set were inspected after sorting by **Web of Science Relevance**.

The assessment used title and abstract information and serves only as a search-query diagnostic.

### Classification

```text
R = Clearly relevant
P = Potentially relevant / retain
I = Clearly irrelevant
```

### Results

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 20 | 66.7% |
| Potentially relevant (P) | 3 | 10.0% |
| Clearly irrelevant (I) | 7 | 23.3% |
| **R + P** | **23/30** | **76.7%** |

The three potentially relevant studies were retained because their agricultural/MAS relevance was clear but the degree of inter-agent interaction or direct focal-scope alignment could not be established confidently from title and abstract alone.

---

## 9. Noise Profile

The seven clearly irrelevant records were classified as:

| Code | Reason | Count |
|---|---|---:|
| I1 | Not a substantive agricultural application | 4 |
| I2 | No meaningful MAS | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | ABM without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other / peripheral technical agricultural application | 3 |

The main noise consisted of:

- urban water-management applications;
- wind-energy applications;
- livestock knowledge-graph construction;
- agricultural heterogeneous-network resource allocation;
- O-RAN / UAV / wireless-sensor-network scheduling.

The I7 records were agriculturally contextualized but primarily optimized communication, information-processing, or infrastructure resources rather than farm-management resources.

Residual noise was considered manageable and did not justify further query restriction.

---

## 10. Alignment with RQ0–RQ4

The query directly operationalizes RQ0 through:

```text
MAS
+
agricultural context
+
focal management/resource problem
+
coordination / decision mechanism
```

RQ2 is represented through terms such as:

- coordination;
- cooperation;
- negotiation;
- allocation;
- scheduling;
- resource sharing;
- decision support;
- distributed/adaptive control;
- peer-to-peer mechanisms;
- auctions;
- consensus.

RQ3 is represented through:

- irrigation and agricultural water;
- livestock and dairy;
- shared-resource allocation;
- climate adaptation/mitigation;
- emissions and methane;
- renewable energy;
- nutrient management;
- soil/environmental management;
- microclimate.

Architecture terminology for RQ1 and evaluation/limitation terminology for RQ4 were deliberately not made mandatory search conditions.

Those dimensions will be evaluated during data extraction and quality assessment.

---

## 11. Export and Data Handling

All 51 final records were exported in two formats:

```text
Excel → Full Record
RIS   → Full Record
```

The RIS export was verified to contain:

```text
51 record starts
51 record ends
```

and includes abstracts, keywords, DOI where available, publication metadata, and Web of Science accession identifiers.

The full exports are retained privately.

Raw Web of Science metadata and abstracts should not be committed to the public repository.

The repository should contain:

- the exact query;
- filters;
- result counts;
- recall-validation results;
- diagnostic relevance/noise assessment;
- methodological decisions;
- final freeze decision.

---

## 12. Deduplication Note

The 51 records represent the **Web of Science database-level corpus only**.

They must not be directly added to:

```text
Scopus = 60
IEEE Xplore = 24
```

because substantial overlap between databases is expected.

The authoritative workflow remains:

```text
Complete all database searches
↓
Combine all database exports
↓
Import into Rayyan
↓
Cross-database deduplication
↓
Formal title / abstract screening
```

Rayyan will remain the authoritative source for duplicate resolution, screening decisions, and PRISMA counts.

Zotero will be used as the permanent bibliographic/PDF library.

---

## 13. Final Decision

Web of Science V0.3c produced:

```text
Unfiltered                         = 61
2010–2026                          = 52
English                            = 51
Article / Proceedings Paper       = 51

Final WoS corpus                   = 51
First-30 R + P                     = 23/30 = 76.7%
```

Recall validation successfully retrieved the indexed explicit-MAS controls covering:

- irrigation and water distribution;
- climate adaptation;
- dairy energy management;
- distributed agricultural control;
- grain-storage microclimate management.

The two missing non-S1 controls were not found in the Web of Science Core Collection and therefore do not represent query failures.

S1 remains an intentionally supplementary ABM/snowballing seed.

No substantive recall failure requiring query modification was identified.

**Decision: Web of Science V0.3c is frozen as the final Web of Science search strategy for the current SLR protocol.**

No further Boolean refinement will be performed unless later validation identifies a substantive scope or recall failure.

---
