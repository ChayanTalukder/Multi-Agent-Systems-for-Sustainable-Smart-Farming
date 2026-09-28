## Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.3b search | 902 |
| After 2010–2026 year filter | 818 |
| After English-language filter | 769 |
| After Article + Conference Paper filter | 689 |

### Preliminary Observation

V0.3b produced a final filtered result set of **689 records**, compared with **688 records in V0.3a**.

The only modification from V0.3a was the addition of a narrow abstract-level pathway for explicit agricultural decision-support terminology.

This modification added exactly one record at every search stage.

Because the V0.3b modification was introduced as an additional OR condition, all records retrieved by V0.3a remain eligible under V0.3b. The additional record will be checked to determine whether it corresponds to the known relevant distributed resource-allocation agricultural decision-support study that was missed by V0.3a.

Compared with V0.3, the final V0.3b result set decreased from **1,026 to 689 records**, representing a reduction of approximately **32.8%**.

## Positive-Control Validation

Because V0.3b was introduced as a targeted recall repair of V0.3a, the same six known relevant studies previously selected from the V0.3 diagnostic sample were used as positive controls.

These studies represent different parts of the review scope, including crop and storage management, livestock management, agricultural coordination, distributed resource allocation, sustainable farm-energy management, and cooperative agricultural robotics.

| Positive control | Representative review area | Retrieved by V0.3b |
|---|---|---|
| Multi-Agent System for Forecasting and Controlling the Microclimate in Grain Storage Facilities with Diverse Crops | Crop/storage management and environmental control | Yes |
| Modelling a multi agent system for dairy farms for integrated decision making | Livestock management and integrated farm decision-making | Yes |
| Human-in-the-Loop Tracking Control for Nonlinear Agricultural Multi-Agent Systems: A Fully Distributed Fuzzy Adaptive Method | Agricultural coordination and distributed control | Yes |
| Distributed resource allocation: Generic model and solution based on constraint programming and multi-agent system for machine to machine services | Agricultural decision support and distributed resource allocation | Yes |
| A Multi-agent Systems Approach for Peer-to-Peer Energy Trading in Dairy Farming | Livestock farming, shared energy resources, and sustainability | Yes |
| Intelligent Multi-Agent Systems for UAV-Robot Path Optimization via Reflective Evolution | Precision agriculture and cooperative agricultural robotics | Yes |

The dairy-farm integrated decision-making study was confirmed by locating the exact 2017 record by Thangaraj et al. within the V0.3b result set.

The distributed resource-allocation agricultural Decision Support System, which was not retrieved by V0.3a, was successfully recovered by V0.3b using both its exact title and DOI.

---

## Positive-Control Observation

V0.3b successfully retrieved **all six positive-control studies**.

This is important because the positive-control set represents a broader range of agricultural Multi-Agent System applications than the original three diagnostic seed studies alone.

The controls demonstrate retained coverage across:

- crop and grain-storage management;
- livestock and dairy-farm decision-making;
- distributed agricultural coordination and control;
- shared-resource allocation;
- agricultural Decision Support Systems;
- renewable-energy and sustainability management; and
- cooperative UAV/robot applications in precision agriculture.

The most important improvement over V0.3a was the recovery of the distributed resource-allocation agricultural Decision Support System.

V0.3a produced **688 final filtered records** but failed to retrieve this known relevant study. V0.3b introduced a narrow abstract-level pathway for explicit agricultural decision-support terminology and produced **689 final filtered records**.

Thus, the V0.3b modification increased the candidate corpus by only **one record** while successfully recovering the relevant study that motivated the revision.

The result indicates that the targeted recall repair improved coverage without materially increasing the screening workload.

Together with the successful retrieval of all three Scopus-indexed diagnostic seed studies, the positive-control validation provides evidence that V0.3b preserves coverage across multiple major dimensions of the review while maintaining the substantial reduction in retrieval volume achieved by V0.3a.

A new relevance/noise assessment of the first 30 V0.3b records sorted by Scopus relevance will therefore be conducted before any further query refinement is considered.

### Irrelevant-Record Diagnostic

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 0 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other | 2 |

## V0.3b Relevance and Noise Assessment

To evaluate the relevance and noise profile of Pilot Query V0.3b, the first 30 records of the final filtered Scopus result set were inspected after sorting by relevance.

The assessment used the title, abstract, author keywords, and indexed keywords of each record.

This assessment was performed solely for search-query validation and does not constitute formal title/abstract screening.

### Classification Results

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 24 | 80.0% |
| Possibly relevant (P) | 4 | 13.3% |
| Clearly irrelevant (I) | 2 | 6.7% |

Overall, **28 of the first 30 records (93.3%) were either clearly relevant or potentially relevant** to the review scope.

This represents a substantial improvement over the previous pilot assessments:

| Query | R + P | Percentage |
|---|---:|---:|
| V0.1 | 17/30 | 56.7% |
| V0.3 | 22/30 | 73.3% |
| V0.3b | 28/30 | 93.3% |

### Irrelevant-Record Diagnostic

The two clearly irrelevant records were classified using the same diagnostic categories applied during previous pilot assessments.

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 0 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other | 2 |

No clearly irrelevant record was classified as a non-agricultural application.

This is an important improvement over V0.3, where all eight clearly irrelevant records in the diagnostic sample were classified as I1.

The two V0.3b records assigned to I7 involved genuinely agricultural material but applied Multi-Agent Systems primarily to tasks outside the central review focus:

1. automated semantic metadata extraction and interoperability between crop-model software platforms; and
2. cybersecurity and communication-network infrastructure for smart-farming IoT systems.

Neither represented the coordinated agricultural decision-making, farm-resource management, livestock management, irrigation management, or environmental-management applications that form the central scope of the review.

### Primary Noise Source

The dominant non-agricultural noise observed in V0.3 was not present among the clearly irrelevant V0.3b records.

The revised agricultural-domain logic therefore appears to have substantially reduced studies in which agriculture was mentioned only incidentally as a possible application domain.

The residual noise is instead associated with studies that are genuinely situated in an agricultural technological context but whose Multi-Agent Systems perform peripheral technical functions outside the central decision-making and resource-management scope of the review.

### Observed Terminology

Relevant and potentially relevant records contained terminology including:

- multi-agent systems / multiagent systems;
- agent-based modelling;
- autonomous agents;
- cooperative and collaborative agents;
- distributed optimization;
- distributed adaptive protocols;
- leader-follower consensus;
- virtual organizations;
- human-in-the-loop Multi-Agent Systems;
- constraint programming with Multi-Agent Systems;
- multi-agent decision-support systems;
- peer-to-peer coordination and energy trading;
- digital twins;
- emergent intelligence;
- self-organized resource management;
- resource scheduling;
- agricultural robotics;
- agent communication and coordination;
- agentic AI and LLM-based multi-agent architectures.

These terms are retained in the terminology log but are not automatically added to the search query.

### V0.3b Diagnostic Conclusion

Pilot Query V0.3b produced a final filtered result set of **689 records** and successfully retained all three Scopus-indexed diagnostic seed studies.

It also retrieved all six broader positive-control studies representing different areas of the review scope.

The first-30 relevance assessment showed that **24 records (80.0%) were clearly relevant**, four (13.3%) were potentially relevant, and only two (6.7%) were clearly irrelevant.

Thus, **28 of 30 records (93.3%) were relevant or potentially relevant**.

This represents a substantial improvement over both V0.1 and V0.3.

Most importantly, no clearly irrelevant V0.3b record was classified as a non-agricultural application (I1), suggesting that the agricultural-domain refinement successfully addressed the dominant source of noise identified during V0.3.

The remaining clearly irrelevant records arose from peripheral agricultural technology applications rather than incidental agricultural mentions.

V0.3b therefore demonstrates a strong relevance profile while preserving the known relevant seed and positive-control studies.

However, the final candidate corpus of **689 records** remains substantially larger than the intended screening workload. Further refinement should therefore be considered carefully, with priority given to preserving the strong recall and relevance profile achieved by V0.3b.
