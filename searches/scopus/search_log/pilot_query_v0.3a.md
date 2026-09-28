## Result Counts

| Stage | Records |
|---|---:|
| Unfiltered V0.3a search | 901 |
| After 2010–2026 year filter | 817 |
| After English-language filter | 768 |
| After Article + Conference Paper filter | 688 |

### Seed Validation Observation

V0.3a retained all three diagnostic seed studies indexed in Scopus.

| ID | V0.1 | V0.2 | V0.3 | V0.3a |
|---|---|---|---|---|
| S1 | No | Yes | Yes | Yes |
| S2 | Yes | Yes | Yes | Yes |
| S3 | Yes | Yes | Yes | Yes |
| S4 | N/A | N/A | N/A | N/A |

The result indicates that the revised agricultural-domain logic reduced the candidate corpus without sacrificing recall for the existing diagnostic seed set.

The final filtered result count decreased from 1,026 records in V0.3 to 688 records in V0.3a, representing a reduction of approximately 32.9%.

Because V0.3a introduced a substantially stricter agricultural-domain condition, additional positive-control validation will be performed using known relevant studies identified during the V0.3 relevance assessment. This is intended to ensure that the refinement preserves coverage across multiple areas of the review scope rather than merely retaining the original seed studies.

## Positive-Control Validation

Because V0.3a introduced a stricter agricultural-domain criterion, six known relevant studies from the V0.3 diagnostic sample were used as additional positive controls.

| Positive control | Retrieved by V0.3a |
|---|---|
| Grain-storage microclimate MAS | Yes |
| Dairy-farm integrated decision MAS | Pending exact-record confirmation |
| Human-in-the-loop agricultural MAS | Yes |
| Distributed resource-allocation agricultural DSS | No |
| Dairy-farm P2P energy-trading MAS | Yes |
| UAV–robot path-optimization MAS | Yes |

### Positive-Control Observation

V0.3a retained four confirmed positive controls, while one remained to be confirmed and one clearly relevant study was not retrieved.

The missing study was the distributed resource-allocation agricultural decision-support paper. Its abstract explicitly describes an agricultural Decision Support System based on Multi-Agent Systems and Constraint Programming, but its title and author keywords do not contain agricultural terminology and its abstract does not contain one of the concrete agricultural entity terms required by V0.3a.

This indicates that the agricultural-domain criterion introduced in V0.3a is overly restrictive for relevant studies framed at the level of agricultural decision support or resource allocation.

Therefore, V0.3a will not be treated as the final query.

A targeted V0.3b refinement will preserve the V0.3a structure while adding a narrow abstract-level pathway for explicit agricultural decision-support terminology.
