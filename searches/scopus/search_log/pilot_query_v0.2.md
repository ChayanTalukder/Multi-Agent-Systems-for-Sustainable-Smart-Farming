Pilot Query V0.2 was developed in response to the recall and precision issues identified during the evaluation of V0.1.

The main problems identified were:

1. V0.1 failed to retrieve diagnostic seed study S1;
2. the result set remained too large for a single-reviewer SLR;
3. the main source of irrelevant retrieval in the first-30 diagnostic sample was non-agricultural literature;
4. the generic term `farm*` retrieved non-agricultural concepts such as wind farms, wave farms, and offshore wind farms;
5. some generic MAS, robotics, and control studies were retrieved because Scopus assigned agriculture-related indexed keywords even when the study itself was not agricultural.

The primary objective of V0.2 is therefore to **improve recall without changing the conceptual scope of the review**, while also attempting to reduce non-agricultural noise.

---

## Changes Introduced from V0.1

The following changes were made.

### Multi-Agent Systems terminology

The following terms were added:

- `"agent-based model*"`
- `multiagent*`
- `"autonomous agent*"`

The term `"agent-based model*"` was particularly important because S1 described its approach primarily as an **Agent-Based Model / Irrigation Agent-Based Model**, terminology not sufficiently represented in V0.1.

### Agricultural terminology

The broad term:

```text
farm*
```

was removed because the V0.1 diagnostic showed that it retrieved non-agricultural concepts such as:

- wind farm;
- wave farm;
- offshore wind farm.

More targeted agricultural terms were retained or added, including:

- `"smart farm*"`
- `"precision agriculture"`
- irrigation
- livestock
- `"precision livestock"`
- `crop*`
- pasture
- `"dairy farm*"`

### Agricultural field restriction

The agricultural concept block was changed from:

```text
TITLE-ABS-KEY(...)
```

to:

```text
TITLE-ABS(...)
```

This change was intended to reduce retrieval of generic MAS/control papers that were matched only because Scopus had assigned agriculture-related indexed keywords.

### Coordination and resource terminology

Standalone:

```text
water
```

was removed from the third concept block because it was considered overly broad.

Additional terms were introduced to better represent coordination and resource-management concepts observed during the V0.1 pilot:

- `"resource optimisation"`
- `"resource optimization"`
- `"resource management"`
- `"task allocation"`
- `"decision support"`
- `"decision-making"`
- `"decision making"`

---

## V0.2 Query

```text
TITLE-ABS-KEY(
    "multi-agent system*" OR
    "multi agent system*" OR
    "multi-agent" OR
    multiagent* OR
    "intelligent agent*" OR
    "autonomous agent*" OR
    "agent-based decision*" OR
    "agent-based model*"
)
AND
TITLE-ABS(
    agricultur* OR
    "smart farm*" OR
    "precision agriculture" OR
    irrigation OR
    livestock OR
    "precision livestock" OR
    crop* OR
    pasture OR
    "dairy farm*"
)
AND
TITLE-ABS-KEY(
    coordination OR
    cooperation OR
    negotiation OR
    "resource allocation" OR
    "resource optimisation" OR
    "resource optimization" OR
    "resource management" OR
    "task allocation" OR
    "decision support" OR
    "decision-making" OR
    "decision making" OR
    decision* OR
    sustainab* OR
    environment*
)
```

---

## Search Filters

The same filters used for V0.1 were retained to ensure comparability between pilot queries.

- Publication years: **2010–2026**
- Language: **English**
- Document types:
  - Article
  - Conference Paper

No subject-area, country, affiliation, open-access, source-title, or funding restrictions were applied.

---

## Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.2 search | 1,803 |
| After 2010–2026 year filter | 1,642 |
| After English-language filter | 1,570 |
| After Article + Conference Paper filter | 1,315 |

The final filtered V0.2 result set therefore contained **1,315 records**.

For comparison:

| Query | Final filtered records |
|---|---:|
| V0.1 | 1,119 |
| V0.2 | 1,315 |

V0.2 retrieved **196 more records** than V0.1, representing an increase of approximately **17.5%**.

---

## Seed Validation

The same diagnostic seed studies used for V0.1 were retained.

| ID | Seed study | Indexed in Scopus | Retrieved by V0.1 | Retrieved by V0.2 |
|---|---|---|---|---|
| S1 | Smart water management approach for resource allocation in High-Scale irrigation systems | Yes | No | Yes |
| S2 | Water distribution in community irrigation using a multi-agent system | Yes | Yes | Yes |
| S3 | Multi-Agent Agro-Economic Simulation of Irrigation Water Demand with Climate Services for Climate Change Adaptation | Yes | Yes | Yes |
| S4 | Digital twin management platform integrating multi-agent system for resource utilisation of crop-livestock waste and its applications | No | N/A | N/A |

S1 and S3 retrieval were additionally confirmed using DOI-based searches within the V0.2 result set.

---

## Seed Validation Observation

V0.2 successfully retrieved **all three diagnostic seed studies indexed in Scopus**.

This represents an improvement in recall compared with V0.1, which failed to retrieve S1.

The retrieval of S1 supports the decision to introduce broader agent-based terminology, particularly:

```text
"agent-based model*"
```

However, this improvement in seed recall was accompanied by a substantial increase in total retrieved records.

The seed-validation result therefore indicates that broader agent-based terminology is useful for identifying relevant agricultural decision systems, but that it requires additional constraints to avoid excessive retrieval of broader agent-based literature.

---

## V0.2 Relevance and Noise Assessment

A new 30-record relevance/noise assessment was **not performed for V0.2**.

This was a deliberate methodological decision.

The purpose of V0.2 was primarily to test whether broader agent-based terminology could recover the relevant seed study missed by V0.1 while reducing the overall candidate corpus.

V0.2 successfully improved seed recall, but the final filtered result set increased from:

```text
1,119 records in V0.1
```

to:

```text
1,315 records in V0.2
```

Because V0.2 had already failed the workload/precision objective by increasing the candidate set, repeating the same first-30 relevance/noise diagnostic was not considered necessary at this stage.

No relevance percentages or irrelevant-record counts are therefore reported for V0.2.

This avoids fabricating or inferring a relevance profile that was not actually measured.

---

## Irrelevant-Record Diagnostic

A separate irrelevant-record diagnostic was **not conducted for V0.2** because no new 30-record relevance sample was performed.

The V0.1 diagnostic had already established that the dominant observed source of clearly irrelevant retrieval was **non-agricultural literature**.

V0.2 attempted to address this by:

- removing generic `farm*`;
- restricting the agricultural concept block to Title and Abstract;
- using more targeted agricultural terminology.

However, the increase in overall retrieval volume indicates that the addition of broader agent-based terminology introduced a new precision/workload problem before the effectiveness of these agricultural-domain refinements could be meaningfully isolated.

No V0.2-specific irrelevant-reason counts are therefore reported.

---

## Terminology Assessment

No new systematic terminology assessment was performed for V0.2 because the first-30 relevance sample was not repeated.

V0.2 instead incorporated selected terminology identified during the V0.1 relevance assessment and seed-study analysis.

Terms introduced or expanded in V0.2 included:

- `multiagent*`
- `"autonomous agent*"`
- `"agent-based model*"`
- `crop*`
- pasture
- `"dairy farm*"`
- `"resource optimisation"`
- `"resource optimization"`
- `"resource management"`
- `"task allocation"`

These additions were treated as **pilot query refinements**, not as evidence that every term should necessarily remain in the final search strategy.

No additional terminology is claimed to have been discovered from V0.2 itself.

---

## Primary V0.2 Observation

V0.2 demonstrated a clear trade-off between **recall and precision/workload**.

### Recall

V0.2 improved diagnostic seed recall:

```text
V0.1: S1 = No, S2 = Yes, S3 = Yes
V0.2: S1 = Yes, S2 = Yes, S3 = Yes
```

### Retrieval Volume

At the same time, the final filtered result count increased:

```text
V0.1 = 1,119
V0.2 = 1,315
```

The likely primary contributor to this increase was the addition of:

```text
"agent-based model*"
```

This terminology is important for retrieving relevant agricultural decision systems such as S1, but it also represents a much broader class of agent-based modelling research.

Agricultural agent-based models may investigate:

- farmer behaviour;
- land-use decisions;
- agricultural economics;
- climate adaptation;
- policy behaviour;
- social systems;
- resource use;

without necessarily implementing meaningful Multi-Agent System communication, coordination, cooperation, or negotiation.

V0.2 therefore improved recall but reduced the practical precision of the search strategy.

---

## Methodological Interpretation

The V0.2 results suggest that **explicit Multi-Agent System terminology and broader agent-based modelling terminology should not necessarily be treated as equivalent search concepts**.

Terms such as:

```text
"multi-agent system*"
"multi-agent"
multiagent*
```

already provide relatively strong evidence that a study may concern a Multi-Agent System.

In contrast, broader terms such as:

```text
"agent-based model*"
"agent-based modelling"
```

can describe studies that do not contain the meaningful agent interaction required by this review.

A more selective search structure is therefore required in which broader agent-based terminology is combined with additional evidence of:

- coordination;
- cooperation;
- negotiation;
- resource allocation;
- task allocation;
- distributed or collective decision-making.

This distinction will guide the next pilot-query revision.

---

## V0.2 Diagnostic Conclusion

Pilot Query V0.2 successfully addressed the primary recall limitation identified in V0.1 by retrieving all three Scopus-indexed diagnostic seed studies.

However, it did not improve the practical precision or manageability of the search.

The final filtered result set increased from **1,119 records in V0.1 to 1,315 records in V0.2**, substantially exceeding the intended screening workload for a single-reviewer SLR.

V0.2 will therefore **not** be treated as the final Scopus query.

The main methodological lesson from V0.2 is that broader agent-based terminology is necessary to capture relevant studies that do not explicitly label themselves as Multi-Agent Systems, but this terminology must be constrained by meaningful interaction or coordination concepts.

The next query revision should therefore aim to:

1. retain S1, S2, and S3;
2. preserve the broader agent-based terminology required for recall;
3. distinguish explicit MAS terminology from generic agent-based modelling;
4. require stronger evidence of coordination or interaction when broader agent-based terminology is used;
5. maintain a clearly agricultural application domain;
6. substantially reduce the overall candidate corpus;
7. preserve the conceptual scope defined in the SLR protocol.

---

## V0.2 Status

**Rejected as final Scopus query.**

Reason:

> Improved diagnostic seed recall, but increased the filtered candidate corpus and therefore failed the precision/workload objective.

The findings from V0.2 will be used to design Pilot Query V0.3.
