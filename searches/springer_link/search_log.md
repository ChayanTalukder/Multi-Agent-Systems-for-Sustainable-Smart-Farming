# Pilot Query V0.3c — SpringerLink

**Status:** Frozen  
**Database:** Springer Nature Link (SpringerLink)  
**Search date:** 1 October 2026  
**Date coverage:** 2010–2026  
**Language:** English  
**Final Article/Conference Paper corpus:** 31 unique records  

---

## Search Strategy

The frozen V0.3c conceptual strategy was adapted to SpringerLink using the Advanced Search fields:

```text
Title
Keywords
```

SpringerLink's `Keywords` field searches more broadly than conventional author-keyword indexing and may match terms occurring elsewhere in the document. The strategy therefore retained explicit MAS and focal concepts in the `Title` field to preserve centrality.

Six branches were used:

```text
A1 — irrigation / water / livestock
A2 — resources / energy / climate
A3 — emissions / nutrients / soil / waste
A4 — pasture / grazing / manure / welfare / microclimate
B1 — agricultural-MAS recall: irrigation / livestock
B2 — agricultural-MAS recall: resources / environment
```

The final search is:

```text
A1 ∪ A2 ∪ A3 ∪ A4 ∪ B1 ∪ B2
```

No `AND NOT` exclusions were used.

---

## Final Queries

### A1 — Irrigation / Water / Livestock

**Title**

```text
(
    "multi-agent"
    OR "multi agent"
    OR multiagent
)
AND
(
    irrigation
    OR water
    OR livestock
    OR dairy
    OR "soil moisture"
)
```

**Keywords**

```text
(
    agriculture
    OR farming
    OR crop
)
AND
(
    coordination
    OR allocation
    OR scheduling
    OR control
    OR decision
)
```

### A2 — Resources / Energy / Climate

**Title**

```text
(
    "multi-agent"
    OR "multi agent"
    OR multiagent
)
AND
(
    resource
    OR energy
    OR climate
)
```

**Keywords**

```text
(
    agriculture
    OR farming
    OR livestock
    OR dairy
)
AND
(
    coordination
    OR allocation
    OR scheduling
    OR control
    OR decision
)
```

### A3 — Emissions / Nutrients / Soil / Waste

**Title**

```text
(
    "multi-agent"
    OR "multi agent"
    OR multiagent
)
AND
(
    emission
    OR methane
    OR nutrient
    OR runoff
    OR soil
    OR waste
)
```

**Keywords**

```text
(
    agriculture
    OR farming
    OR crop
)
AND
(
    coordination
    OR allocation
    OR control
    OR decision
)
```

### A4 — Pasture / Grazing / Manure / Welfare / Microclimate

**Title**

```text
(
    "multi-agent"
    OR "multi agent"
    OR multiagent
)
AND
(
    pasture
    OR grazing
    OR manure
    OR welfare
    OR microclimate
)
```

**Keywords**

```text
(
    agriculture
    OR farming
    OR livestock
    OR dairy
)
AND
(
    coordination
    OR allocation
    OR control
    OR decision
)
```

### B1 — Agricultural-MAS Recall: Irrigation / Livestock

**Title**

```text
(
    "multi-agent"
    OR "multi agent"
    OR multiagent
)
AND
(
    agriculture
    OR farming
)
```

**Keywords**

```text
(
    irrigation
    OR fertilizer
    OR harvest
    OR livestock
    OR dairy
)
AND
(
    coordination
    OR control
    OR decision
)
```

### B2 — Agricultural-MAS Recall: Resources / Environment

**Title**

```text
(
    "multi-agent"
    OR "multi agent"
    OR multiagent
)
AND
(
    agriculture
    OR farming
)
```

**Keywords**

```text
(
    resource
    OR energy
    OR climate
    OR emission
)
AND
(
    coordination
    OR allocation
    OR scheduling
    OR control
    OR decision
)
```

---

## Result Counts

| Branch | Unfiltered | 2010–2026 | English |
|---|---:|---:|---:|
| A1 | 13 | 10 | 10 |
| A2 | 14 | 14 | 14 |
| A3 | 0 | 0 | 0 |
| A4 | 0 | 0 | 0 |
| B1 | 9 | 7 | 7 |
| B2 | 15 | 13 | 13 |
| **Raw branch total** | **51** | **44** | **44** |

After DOI-based branch-overlap consolidation:

```text
Raw year/language-filtered branch retrievals = 44
Unique records                              = 33
```

SpringerLink classified the 33 unique records as:

| Content type | Records |
|---|---:|
| Article | 13 |
| Conference paper | 18 |
| Chapter | 2 |
| **Total** | **33** |

The two records classified only as `Chapter` were excluded because the protocol restricts the primary corpus to journal articles and conference papers.

```text
Final SpringerLink Article/Conference Paper corpus = 31
```

No platform content-type filter was applied during searching because Springer conference proceedings may be represented through chapter-based publication structures. Content type was therefore checked after export.

---

## Recall Validation

Known relevant Springer-hosted studies were checked against the final strategy.

The following focal control was successfully retrieved:

```text
A Multi-agent Systems Approach for Peer-to-Peer Energy Trading
in Dairy Farming
DOI: 10.1007/978-3-031-50485-3_27
```

It was retrieved through multiple branches and directly represents:

```text
dairy farming
+ Multi-Agent Systems
+ resource exchange
+ peer-to-peer energy coordination
```

The Springer-hosted MAELIA study was also successfully retrieved:

```text
The MAELIA Multi-Agent Platform for Integrated Analysis of
Interactions Between Agricultural Land-Use and Low-Water
Management Strategies
DOI: 10.1007/978-3-642-54783-6_6
```

This provided additional validation for agricultural decision-making, land use, water management, and multi-agent modelling.

Other previously used controls published outside SpringerLink were not treated as SpringerLink query failures.

No demonstrated SpringerLink false negative required a query repair.

---

## Relevance and Noise Assessment

Because only 31 unique Article/Conference Paper records remained, all 31 were assessed.

This assessment was performed only for search-query validation and does not replace formal title/abstract screening in Rayyan.

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 9 | 29.0% |
| Possibly relevant (P) | 4 | 12.9% |
| Clearly irrelevant (I) | 18 | 58.1% |
| **R + P** | **13/31** | **41.9%** |

The four potentially relevant records included:

- an agricultural water-conservancy stakeholder evolutionary-game study;
- a livestock/pasture-resource multi-agent simulation;
- an agricultural knowledge-graph multi-agent decision-support framework;
- a multi-agent organic-farming value-chain model.

These were retained as `P` because formal screening is required to determine whether their agent interaction satisfies the substantive MAS eligibility criterion.

### Irrelevant-Record Diagnostic

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 12 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Agricultural context but peripheral technical application | 6 |

The dominant noise arose from SpringerLink's broad `Keywords` search behaviour.

`I1` records included generic applications such as smart grids, energy systems, enterprise resource management, climate-economic modelling, and non-agricultural water management.

`I7` primarily contained agricultural UAV, networking, computing, trajectory/coverage, and embedded-processing studies in which the MAS addressed peripheral technical infrastructure rather than the review's focal agricultural resource, irrigation, livestock, or environmental decision problem.

---

## Final Decision

The frozen SpringerLink V0.3c search produced:

```text
51 unfiltered branch retrievals
44 after 2010–2026 + English filtering
33 unique records after branch consolidation
31 unique Article/Conference Paper records

R = 9
P = 4
I = 18
R + P = 13/31 = 41.9%
```

Although SpringerLink produced more noise than Scopus, Web of Science, or ScienceDirect, the absolute screening workload is small and relevant agricultural MAS studies were successfully retained.

Further Boolean restriction was therefore not justified because it could increase the risk of false negatives for limited workload reduction.

**Decision: SpringerLink V0.3c is frozen.**

No further SpringerLink query refinement will be performed unless a later validation step identifies a substantive recall failure.

Raw SpringerLink CSV exports will remain private and will not be committed to the public repository.

Final cross-database deduplication and formal title/abstract screening will be performed in Rayyan.
