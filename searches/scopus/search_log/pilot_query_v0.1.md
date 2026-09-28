## Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.1 search | 1,558 |
| After 2010–2026 year filter | 1,389 |
| After English-language filter | 1,316 |
| After Article + Conference Paper filter | 1,119 |


## Seed Validation

| ID | Seed study | Indexed in Scopus | Retrieved by V0.1 |
|---|---|---|---|
| S1 | Smart water management approach for resource allocation in High-Scale irrigation systems | Yes | No |
| S2 | Water distribution in community irrigation using a multi-agent system | Yes | Yes |
| S3 | Multi-Agent Agro-Economic Simulation of Irrigation Water Demand with Climate Services for Climate Change Adaptation | Yes | Yes |
| S4 | Digital twin management platform integrating multi-agent system for resource utilisation of crop-livestock waste and its applications | No | N/A |

### Seed Validation Observation

V0.1 retrieved two of the three diagnostic seed studies indexed in Scopus.

S1 was indexed in Scopus but was not retrieved by the pilot query. Inspection of the study terminology indicates that it describes its approach primarily as an "Agent-Based Model" / "Irrigation Agent-Based Model" rather than using the current query term "agent-based decision*".

The term `"agent-based model*"` is therefore retained as a candidate addition for the next query revision. No modification will be made until the relevance/noise profile of V0.1 has also been assessed.

## V0.1 Relevance and Noise Assessment

To evaluate the relevance and noise profile of Pilot Query V0.1, the first 30 records were inspected after sorting the Scopus result set by relevance.

This assessment was performed only for search-query validation and does not constitute formal title/abstract screening.

### Classification Results

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 11 | 36.7% |
| Possibly relevant (P) | 6 | 20.0% |
| Clearly irrelevant (I) | 13 | 43.3% |

Overall, **17 of the first 30 records (56.7%) were either clearly relevant or potentially relevant** to the review scope.

### Irrelevant-Record Diagnostic

The 13 clearly irrelevant records were classified according to the following diagnostic categories:

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 13 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other | 0 |

The dominant source of noise was therefore **non-agricultural retrieval**, rather than failure of the Multi-Agent Systems concept block.

### Observed Terminology

Terminology appearing in relevant or potentially relevant records, but not explicitly represented in V0.1, included:

- multiagent / multiagent systems
- multi-agents
- autonomous agents
- distributed multi-agent systems
- agent-based modelling
- agentic AI
- agent collaboration
- collaborative mechanisms
- task allocation
- resource allocation
- resource optimisation
- multi-agent-based automation
- human-in-the-loop multi-agent systems
- hypermedia multi-agent systems

These terms are recorded as candidate terminology for query refinement but are not automatically added to the search strategy.

### Primary Noise Sources

Two main sources of irrelevant retrieval were observed.

1. The broad agricultural term `farm*` retrieved non-agricultural meanings including:
   - wind farm;
   - wave farm;
   - offshore wind farm.

2. Some generic Multi-Agent Systems, robotics, or control papers were retrieved because Scopus assigned agriculture-related indexed keywords, even when the actual study was not conducted in an agricultural domain.

### V0.1 Diagnostic Conclusion

Pilot Query V0.1 demonstrated reasonable relevance among the highest-ranked results but produced an excessively large filtered result set of **1,119 records**.

The query also failed to retrieve one of the three Scopus-indexed diagnostic seed studies (S1), indicating a recall limitation associated with the current Multi-Agent Systems terminology.

Therefore, V0.1 will not be treated as the final Scopus query.

The next query revision will aim to:

1. improve recall for relevant agent-based agricultural decision systems;
2. reduce non-agricultural noise;
3. retain the relevant seed studies already retrieved;
4. reduce the overall screening workload without changing the conceptual scope of the review.
