# Pilot Query V0.3c — ScienceDirect

**Status:** Frozen  
**Database:** ScienceDirect  
**Search date:** 1 October 2026  
**Date coverage:** 2010–2026  
**Final unique records:** 20  

---

## Search Strategy

ScienceDirect could not support the complete V0.3c expression as a single query because the active interface imposed a maximum of eight Boolean connectors per field and did not support wildcard syntax in the Title field.

The frozen conceptual V0.3c strategy was therefore translated into six smaller branches:

```text
A1  — irrigation / water / livestock
A2r — resources / energy / climate
A3  — emissions / nutrients / soil / waste
A4  — pasture / grazing / manure / welfare / microclimate
B1  — agricultural-MAS recall: irrigation / livestock
B2  — agricultural-MAS recall: resources / environment
```

The final ScienceDirect corpus is:

```text
A1 ∪ A2r ∪ A3 ∪ A4 ∪ B1 ∪ B2
```

Two ScienceDirect fields were used:

```text
Title
Title, abstract or author-specified keywords
```

No `AND NOT` exclusions were used.

---

## Final Queries

### A1 — Irrigation / Water / Livestock

**Title**

```text
(
    "multi-agent"
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

**Title, abstract or author-specified keywords**

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

### A2r — Resources / Energy / Climate

**Title**

```text
(
    "multi-agent"
    OR multiagent
)
AND
(
    resource
    OR energy
    OR climate
)
```

**Title, abstract or author-specified keywords**

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
    OR trading
)
```

### A3 — Emissions / Nutrients / Soil / Waste

**Title**

```text
(
    "multi-agent"
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

**Title, abstract or author-specified keywords**

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

**Title, abstract or author-specified keywords**

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
    OR welfare
)
```

### B1 — Agricultural-MAS Recall: Irrigation / Livestock

**Title**

```text
(
    "multi-agent"
    OR multiagent
)
AND
(
    agriculture
    OR farming
)
```

**Title, abstract or author-specified keywords**

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
    OR multiagent
)
AND
(
    agriculture
    OR farming
)
```

**Title, abstract or author-specified keywords**

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

| Branch | Unfiltered | 2010–2026 |
|---|---:|---:|
| A1 | 12 | 11 |
| A2r | 9 | 8 |
| A3 | 1 | 1 |
| A4 | 0 | 0 |
| B1 | 2 | 2 |
| B2 | 6 | 5 |
| **Raw branch total** | **30** | **27** |

Branch overlap was consolidated using DOI and title matching.

```text
Year-filtered branch retrievals = 27
Unique ScienceDirect records    = 20
```

All 20 unique records contained DOI metadata.

No separate English-language filter was applied because the exported ScienceDirect RIS records did not provide a dedicated language field.

No additional document-type restriction was applied at this stage; publication-type eligibility will be handled during formal screening.

---

## Recall Validation and A2 Repair

Known relevant studies available through ScienceDirect were used to validate recall.

The following were successfully retrieved:

- *Multi-Agent Agro-Economic Simulation of Irrigation Water Demand with Climate Services for Climate Change Adaptation*;
- *Peer-to-peer energy trading in dairy farms using multi-agent systems*.

The irrigation study:

*Smart water management approach for resource allocation in High-Scale irrigation systems*

remained an intentionally supplementary/snowballing seed rather than a mandatory primary-query control.

During validation, the relevant ScienceDirect study:

*Peer-to-peer energy trading in dairy farms using multi-agent reinforcement learning*

was identified as a false negative of the original A2 branch.

The term:

```text
trading
```

was therefore added to the A2 functional block.

This produced:

| Version | Unfiltered | 2010–2026 |
|---|---:|---:|
| A2 | 8 | 7 |
| **A2r** | **9** | **8** |

A2r retained all original A2 records and recovered exactly one additional relevant record.

**Decision:** A2r replaced A2 in the final ScienceDirect strategy.

---

## Relevance and Noise Assessment

Because the final corpus contained only 20 unique records, all 20 were assessed rather than using a 30-record sample.

This assessment was used only to evaluate query behaviour and does not replace formal title/abstract screening.

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 16 | 80.0% |
| Possibly relevant (P) | 3 | 15.0% |
| Clearly irrelevant (I) | 1 | 5.0% |
| **R + P** | **19/20** | **95.0%** |

The three potentially relevant records concerned:

- cross-sector water allocation in which agriculture was one water-use sector;
- agricultural electric-tractor control where meaningful interaction among distinct agents was unclear from the abstract;
- an evolutionary stakeholder game involving government, farmers, and consumers.

The single clearly irrelevant record concerned multi-agent network/task offloading for agricultural robots, where the primary problem was communication and computational-resource management rather than agricultural or environmental decision-making.

### Irrelevant-Record Diagnostic

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 0 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other / peripheral technical application | 1 |

---

## Final Decision

The final ScienceDirect strategy achieved:

```text
27 year-filtered branch retrievals
20 unique records
16 clearly relevant
3 potentially relevant
1 clearly irrelevant
R + P = 95.0%
```

The targeted A2r repair recovered a demonstrated false negative while adding only one record.

Residual noise is minimal, and further Boolean restriction could unnecessarily reduce recall.

**Decision: ScienceDirect V0.3c is frozen.**

No further query refinement will be performed unless a later validation step identifies a substantive recall or scope failure.

Raw RIS exports will remain private and will not be committed to the public repository. Final cross-database deduplication and screening will be performed in Rayyan.
