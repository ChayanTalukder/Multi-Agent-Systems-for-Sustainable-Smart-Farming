# Pilot Query V0.3c — IEEE Xplore

**Status:** Frozen  
**Database:** IEEE Xplore  
**Search interface:** Advanced Search → Command Search  
**Search date:** 29 September 2026  
**Protocol period:** 2010–2026  
**Eligible publication types:** Journals and Conferences  
**Final search:** V0.3c-A ∪ V0.3c-B  
**Final unique IEEE Xplore records:** 24  

---

## 1. Purpose

The IEEE Xplore search is a database-specific translation of the frozen Scopus V0.3c strategy.

The underlying conceptual logic was kept unchanged:

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

The IEEE query was adapted only where required by IEEE Xplore syntax and search constraints.

---

## 2. Why Two Separate IEEE Queries Were Used

The Scopus V0.3c query contains two outer `OR` branches.

A direct translation into one IEEE Command Search was not suitable because IEEE Xplore limits query complexity, including:

- a maximum of 25 search terms per clause;
- restrictions on wildcard usage.

The two logical branches were therefore executed separately:

```text
IEEE V0.3c-A = main explicit-MAS pathway
IEEE V0.3c-B = narrow recall-repair pathway
```

The final IEEE corpus is:

```text
IEEE V0.3c = V0.3c-A ∪ V0.3c-B
```

This preserves the original Boolean logic while allowing database-specific implementation.

No wildcard operators were used in the final IEEE queries.

---

# 3. Final Frozen Query — V0.3c-A

V0.3c-A requires:

```text
MAS in Document Title
AND
Agricultural context in Title/Abstract
AND
Focal application in Document Title
AND
Coordination / allocation / decision / control evidence
```

```text
(
    (
        "Document Title":"multi-agent"
        OR "Document Title":multiagent
    )

    AND

    (
        "Document Title":agriculture
        OR "Abstract":agriculture
        OR "Document Title":agricultural
        OR "Abstract":agricultural
        OR "Document Title":farming
        OR "Abstract":farming
        OR "Document Title":"smart farming"
        OR "Abstract":"smart farming"
        OR "Document Title":"precision agriculture"
        OR "Abstract":"precision agriculture"
        OR "Document Title":irrigation
        OR "Abstract":irrigation
        OR "Document Title":livestock
        OR "Abstract":livestock
        OR "Document Title":dairy
        OR "Abstract":dairy
        OR "Document Title":cattle
        OR "Abstract":cattle
        OR "Document Title":crop
        OR "Abstract":crop
        OR "Document Title":pasture
        OR "Abstract":pasture
        OR "Document Title":grain
        OR "Abstract":grain
    )

    AND

    (
        "Document Title":irrigation
        OR "Document Title":"water allocation"
        OR "Document Title":"water distribution"
        OR "Document Title":"water management"
        OR "Document Title":"water scarcity"
        OR "Document Title":"soil moisture"
        OR "Document Title":livestock
        OR "Document Title":dairy
        OR "Document Title":cattle
        OR "Document Title":pasture
        OR "Document Title":grazing
        OR "Document Title":manure
        OR "Document Title":"resource allocation"
        OR "Document Title":"resource sharing"
        OR "Document Title":"resource negotiation"
        OR "Document Title":"resource scheduling"
        OR "Document Title":"task allocation"
        OR "Document Title":"environmental sustainability"
        OR "Document Title":"climate adaptation"
        OR "Document Title":emission
        OR "Document Title":methane
        OR "Document Title":"renewable energy"
        OR "Document Title":"energy management"
        OR "Document Title":"nutrient management"
        OR "Document Title":microclimate
    )

    AND

    (
        "All Metadata":coordination
        OR "All Metadata":cooperation
        OR "All Metadata":negotiation
        OR "All Metadata":allocation
        OR "All Metadata":scheduling
        OR "All Metadata":"resource sharing"
        OR "All Metadata":"resource management"
        OR "All Metadata":"decision support"
        OR "All Metadata":"decision making"
        OR "All Metadata":"distributed control"
        OR "All Metadata":"adaptive control"
        OR "All Metadata":"peer-to-peer"
        OR "All Metadata":auction
        OR "All Metadata":consensus
        OR "All Metadata":control
    )
)
```

---

# 4. Final Frozen Query — V0.3c-B

V0.3c-B is a narrow recall-repair branch requiring:

```text
Agriculture in Document Title
AND
MAS in Document Title
AND
Focal agricultural activity in Abstract
AND
Coordination / decision / control mechanism in Abstract
```

```text
(
    (
        "Document Title":agriculture
        OR "Document Title":agricultural
        OR "Document Title":farming
        OR "Document Title":"smart farming"
        OR "Document Title":"precision agriculture"
    )

    AND

    (
        "Document Title":"multi-agent"
        OR "Document Title":multiagent
    )

    AND

    (
        "Abstract":irrigation
        OR "Abstract":fertilizer
        OR "Abstract":fertilization
        OR "Abstract":harvest
        OR "Abstract":livestock
        OR "Abstract":dairy
        OR "Abstract":pasture
        OR "Abstract":manure
        OR "Abstract":"resource allocation"
        OR "Abstract":"resource sharing"
        OR "Abstract":"resource scheduling"
        OR "Abstract":"energy management"
        OR "Abstract":"energy trading"
        OR "Abstract":"renewable energy"
        OR "Abstract":"climate adaptation"
        OR "Abstract":emission
    )

    AND

    (
        "Abstract":coordination
        OR "Abstract":cooperation
        OR "Abstract":negotiation
        OR "Abstract":allocation
        OR "Abstract":scheduling
        OR "Abstract":"decision support"
        OR "Abstract":"decision making"
        OR "Abstract":"distributed control"
        OR "Abstract":"adaptive control"
        OR "Abstract":"tracking control"
    )
)
```

---

## 5. Query Development and Recall Repair

The initial IEEE translation produced:

| Query | Unfiltered records |
|---|---:|
| V0.3c-A | 16 |
| V0.3c-B | 6 |

Recall was checked using three IEEE-indexed positive controls.

| Positive control | Initial A | B |
|---|:---:|:---:|
| *A multi-agent system framework for autonomous crop irrigation* | Yes | No |
| *Human-in-the-Loop Tracking Control for Nonlinear Agricultural Multi-Agent Systems* | No | Yes |
| *Multi-Agent System for Forecasting and Controlling the Microclimate in Grain Storage Facilities with Diverse Crops* | No | No |

The grain-storage study exposed a specific false negative.

It satisfied:

```text
MAS → title
Agricultural context → grain/crops
Focal area → microclimate
```

but the functional block contained only narrower control expressions such as:

```text
"distributed control"
"adaptive control"
```

The study instead used the more general concept of microclimate **control**.

V0.3c-A was therefore repaired by adding:

```text
OR "All Metadata":control
```

No broader terms such as `monitoring`, `sensor`, `automation`, or generic IoT terms were added.

After the repair:

```text
A unfiltered: 16 → 21
```

and the grain-storage study was retrieved by both exact-title and DOI validation.

This repair was accepted because it corrected a known false negative with only a small increase in retrieval volume.

V0.3c-B required no further modification.

---

## 6. Final Validation

Final positive-control coverage:

| Positive control | A | B | A ∪ B |
|---|:---:|:---:|:---:|
| Autonomous crop irrigation | Yes | No | **Yes** |
| Human-in-the-Loop agricultural MAS | No | Yes | **Yes** |
| Grain-storage microclimate MAS | Yes | No | **Yes** |

Therefore:

```text
Positive controls recovered = 3/3
```

The two branches serve complementary functions:

- **A** retrieves studies where the focal application is explicit in the title;
- **B** recovers agricultural MAS studies where the specific task/control mechanism is mainly described in the abstract.

---

## 7. Final Result Counts

### V0.3c-A

| Stage | Records |
|---|---:|
| Initial unfiltered query | 16 |
| Repaired unfiltered query | 21 |
| Final Journal + Conference export | **19** |

The earliest retained A record is from 2012.

The protocol period nevertheless remains **2010–2026**; no 2010–2011 records happened to be present in the retained IEEE set.

### V0.3c-B

| Stage | Records |
|---|---:|
| Unfiltered | 6 |
| Final Journal + Conference export | **6** |

All B records fall within 2019–2026.

### Combined IEEE corpus

```text
A = 19
B = 6
```

One record occurred in both branches:

**A Multi-Agent Deep Reinforcement Learning Framework for Resource Allocation Optimization in Agricultural Heterogeneous Network**

DOI:

```text
10.1109/TCE.2026.3681349
```

Therefore:

```text
19 + 6 - 1 = 24 unique IEEE Xplore records
```

---

## 8. Relevance / Noise Diagnostic

All 24 unique IEEE records were inspected at title/abstract level as a **query-quality diagnostic**, not as formal screening.

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 9 | 37.5% |
| Potentially relevant (P) | 2 | 8.3% |
| Clearly irrelevant (I) | 13 | 54.2% |
| **R + P** | **11** | **45.8%** |

The main residual noise consisted of:

- generic multi-agent resource-allocation studies;
- cloud/edge computing;
- communication-network optimization;
- robotics;
- battery-energy systems;
- offshore wind systems;
- agricultural networking studies where the optimized resource was primarily communications infrastructure rather than a farming resource.

The two potentially relevant records were retained because the agricultural application was clear but the extent of autonomous inter-agent interaction was not fully established from the abstract.

Although precision is lower than the Scopus V0.3c pilot, the final IEEE corpus contains only **24 unique records**, so further query tightening was not considered justified.

The risk of losing relevant agricultural control/coordination studies was considered greater than the benefit of removing a small number of additional records.

---

## 9. Alignment with RQ0–RQ4

The search directly represents the core of RQ0:

```text
MAS
+
agricultural context
+
focal management problem
+
coordination / decision / control
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

RQ3 is represented through application terms covering:

- irrigation and water management;
- livestock/dairy;
- shared resources;
- energy;
- climate adaptation;
- emissions;
- methane;
- nutrient management;
- microclimate.

Architecture-specific terminology for RQ1 and evaluation/limitations terminology for RQ4 were deliberately **not required** in the query.

These dimensions will be handled during data extraction and quality assessment to avoid excluding relevant studies based on terminology differences.

---

## 10. Export and Data Handling

Each branch was exported separately as:

```text
CSV
RIS
```

RIS export settings:

```text
Format: RIS
Include: Citation and Abstract
```

Final working files:

```text
ieee_xplore_v0.3c-A_final.csv
ieee_xplore_v0.3c-A_final.ris
ieee_xplore_v0.3c-B_final.csv
ieee_xplore_v0.3c-B_final.ris
```

Consistency checks confirmed:

```text
A: 19 CSV records = 19 RIS records
B: 6 CSV records  = 6 RIS records
```

The final union contains:

```text
24 unique IEEE records
```

All 24 records contain abstracts and DOI identifiers.

Raw IEEE exports are retained privately. The public repository contains the reproducibility documentation rather than the database-provided metadata/abstract exports.

---

## 11. Deduplication Note

The 24-record count represents **IEEE Xplore only**.

It must not be added directly to the 60 Scopus records because cross-database duplication is expected.

The workflow remains:

```text
Complete all database searches
↓
Combine exports
↓
Import into Rayyan
↓
Deduplicate once
↓
Formal title/abstract screening
```

Rayyan will be the authoritative source for deduplication, screening decisions, and PRISMA counts.

Zotero will be used as the permanent literature/PDF and citation library.

---

## 12. Final Decision

The final IEEE implementation preserves the frozen V0.3c conceptual search while adapting it to IEEE Xplore's field syntax and query constraints.

The final strategy produced:

```text
V0.3c-A final export = 19
V0.3c-B final export = 6
A/B overlap          = 1
Unique IEEE records  = 24
Positive controls    = 3/3
```

The only substantive recall repair was the addition of:

```text
"All Metadata":control
```

to V0.3c-A, which successfully recovered the grain-storage microclimate study without materially increasing the workload.

Residual technical noise is considered manageable through formal screening.

**Decision: IEEE Xplore V0.3c-A and V0.3c-B are frozen as the final IEEE Xplore search strategy.**

No further Boolean refinement will be performed unless later validation identifies a substantive recall or scope failure.

---
