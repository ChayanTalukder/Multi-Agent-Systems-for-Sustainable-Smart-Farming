## Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.3 search | 1,507 |
| After 2010–2026 year filter | 1349 |
| After English-language filter | 1281 |
| After Article + Conference Paper filter | 1026 |

## Seed Validation

| ID | V0.1 | V0.2 | V0.3 |
|---|---|---|---|
| S1 | No | Yes | Yes |
| S2 | Yes | Yes | Yes |
| S3 | Yes | Yes | Yes |
| S4 | N/A | N/A | N/A |

## V0.3 Relevance and Noise Assessment

To evaluate the relevance and noise profile of Pilot Query V0.3, the first 30 records of the final filtered Scopus result set were inspected after sorting by relevance.

The assessment was conducted using titles, abstracts, author keywords, and indexed keywords.

This assessment was performed solely for search-query validation and does not constitute formal title/abstract screening.

### Classification Results

| Classification | Count | Percentage |
|---|---:|---:|
| Clearly relevant (R) | 19 | 63.3% |
| Possibly relevant (P) | 3 | 10.0% |
| Clearly irrelevant (I) | 8 | 26.7% |

Overall, **22 of the first 30 records (73.3%) were either clearly relevant or potentially relevant** to the review scope.

Compared with V0.1, where 17 of 30 records (56.7%) were classified as relevant or potentially relevant, V0.3 demonstrated an improved relevance profile among the highest-ranked Scopus results.

### Irrelevant-Record Diagnostic

The eight clearly irrelevant records were classified using the same diagnostic categories applied during V0.1.

| Code | Reason | Count |
|---|---|---:|
| I1 | Not an agricultural application | 8 |
| I2 | No meaningful Multi-Agent System | 0 |
| I3 | IoT / sensor monitoring only | 0 |
| I4 | Conventional ML / AI only | 0 |
| I5 | Agent-based modelling without relevant MAS interaction | 0 |
| I6 | Unrelated use of "agent" | 0 |
| I7 | Other | 0 |

The dominant source of clearly irrelevant retrieval therefore remained **non-agricultural application contexts**.

However, the proportion of clearly irrelevant records decreased from 43.3% in the V0.1 diagnostic sample to 26.7% in V0.3.

Notably, no clearly irrelevant record was classified as agent-based modelling without meaningful MAS interaction (I5). This suggests that the two-branch MAS structure introduced in V0.3 successfully constrained broader agent-based terminology within the inspected sample.

### Primary Noise Source

The remaining non-agricultural false positives generally occurred because agriculture or smart farming was mentioned in the title or abstract as one possible application domain, while the actual system was developed or evaluated for another domain.

Examples included studies whose primary applications concerned:

- smart street lighting;
- generic AI for social impact;
- circular supply chains;
- generic network-flow control;
- industrial resource management;
- aircraft-agent control; and
- generic IoT cybersecurity.

Thus, restricting the agricultural block to Title and Abstract reduced but did not eliminate incidental agricultural mentions.

### Observed Terminology

Relevant or potentially relevant records contained terminology including:

- multiagent / multiagents / multi-agents;
- distributed and fully distributed Multi-Agent Systems;
- cooperative and adaptive Multi-Agent Systems;
- autonomous agents;
- agent-based modelling;
- agent collaboration;
- leader-follower coordination and consensus;
- distributed architectures;
- resource allocation;
- peer-to-peer coordination and trading;
- integrated decision making;
- human-in-the-loop Multi-Agent Systems;
- self-organization and stigmergy;
- mission control and path planning.

These terms are retained in the terminology log for consideration during later query validation and cross-database adaptation. They are not automatically added to the search query.

### V0.3 Diagnostic Conclusion

Pilot Query V0.3 retained all three Scopus-indexed diagnostic seed studies while reducing the final filtered result set from 1,315 records in V0.2 to 1,026 records.

The first-30 relevance assessment also showed an improved relevance profile compared with V0.1. Twenty-two of 30 records (73.3%) were classified as clearly or potentially relevant, compared with 17 of 30 (56.7%) in V0.1.

The remaining clearly irrelevant records were exclusively associated with non-agricultural application contexts. No clearly irrelevant record in the sample resulted from generic agent-based modelling without meaningful MAS interaction.

These findings suggest that the two-branch MAS structure should be preserved. Further refinement should instead focus on reducing papers in which agriculture is mentioned only incidentally as a possible application domain.

Because the final result set of 1,026 records remains substantially larger than the intended screening workload, V0.3 will not be treated as the final Scopus query.

The next iteration will therefore be treated as a targeted refinement of V0.3, provisionally designated **V0.3a**, rather than a complete redesign of the search strategy.
