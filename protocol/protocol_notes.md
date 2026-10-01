# Protocol Notes

## Version

**Version:** 1.1  
**Date:** 1 October 2026

## Purpose

This file records methodological decisions made during the Systematic Literature Review. The main protocol was defined before executing the final database searches. Any later changes are documented here to maintain transparency and reproducibility.

---

# Protocol Decisions

## Publication Window

Primary search period: **2010–2026**

Earlier foundational studies may be included through backward citation searching when directly relevant.

---

## Primary Information Sources

- Scopus
- Web of Science Core Collection
- IEEE Xplore
- ScienceDirect
- SpringerLink

Supplementary discovery may use:

- Google Scholar;
- backward and forward citation searching.

---

## ACM Digital Library Search Decision

ACM Digital Library was originally planned as a primary database.

During search execution, the available ACM Digital Library account provided access to the basic search interface but did not permit the advanced query editing required to reproduce the frozen V0.3c Boolean strategy using title- and abstract-specific field combinations.

A preliminary title-only syntax test was possible, but the restricted interface did not support the reproducible multi-field Boolean construction required for the review protocol.

ACM Digital Library was therefore removed from the primary database set rather than using a simplified search that would not be methodologically comparable with the Scopus, Web of Science, and IEEE Xplore implementations.

The final primary database set is:

- Scopus
- Web of Science Core Collection
- IEEE Xplore
- ScienceDirect
- SpringerLink

Relevant ACM-published studies may still be identified through overlapping indexing in Scopus or Web of Science and through supplementary backward/forward citation searching.

This change is recorded as a protocol deviation caused by database-access and search-interface limitations.

## Screening Threshold

The initial search will aim to maximise reasonable coverage while maintaining relevance. If the **deduplicated corpus exceeds approximately 100 records**, indicating that the search may be too broad for the scope and timeline of this single-reviewer SLR, the search will be refined to the closest available equivalents of:

- Title
- Abstract
- Keywords

while preserving the same conceptual search terms.

The threshold is intended as a **trigger for search refinement rather than a strict maximum number of studies**. If a refined search still returns more than approximately 100 highly relevant records, the search will not be artificially restricted solely to reach a numerical target.

Search-query refinement may also be performed during database-specific pilot testing when the retrieved candidate set is clearly too broad for the intended scope. Such refinement must be based on conceptual precision and recall validation rather than an arbitrary numerical cut-off.

---

## Database Syntax

The master search strategy represents the review concepts rather than one literal query.

Database-specific versions may modify:

- wildcard syntax;
- Boolean syntax;
- field names;
- quotation syntax;
- search-field restrictions.

Any adaptation must preserve the conceptual meaning of the original search strategy.

The current frozen conceptual strategy is **V0.3c**. Its core logic requires:

```text
Explicit Multi-Agent System
AND
Agricultural context
AND
Focal agricultural/resource/environmental application
AND
Coordination / allocation / scheduling / decision / control mechanism
```

A narrow secondary recall branch is retained for studies where agriculture and the Multi-Agent System are explicit in the title but the focal agricultural activity and coordination/control mechanism are described mainly in the abstract.

Database-specific repairs may be made only when recall validation identifies a substantive false negative. Such repairs must be documented and should not be transferred automatically to other databases unless independently required.

---

## Screening Software

**Rayyan** will be used as the authoritative environment for:

- deduplication;
- title/abstract screening;
- full-text screening;
- inclusion/exclusion decisions;
- exclusion reasons;
- PRISMA counts.

Formal cross-database deduplication will be performed **once after the planned primary database searches have been completed and their records imported into Rayyan**.

Database-level overlaps may be identified earlier for audit purposes, such as overlap between multiple query branches within one database, but these checks do not replace the authoritative Rayyan deduplication stage.

---

## Reference Management

**Zotero** will be used for:

- permanent literature organisation;
- PDFs;
- metadata;
- notes and annotations;
- citations;
- bibliography generation.

---

## Reviewer Structure

The review is conducted by one researcher. Measures used to improve consistency include:

- predefined eligibility criteria;
- piloting the criteria;
- recording exclusion reasons;
- retaining uncertain studies during initial screening;
- reconsidering ambiguous full texts;
- potentially re-screening a subset of studies.

---

## Database Export and Repository Handling

Database exports containing provider-supplied metadata, abstracts, references, or other licensed bibliographic information will be retained privately for audit, deduplication, and screening.

The public repository will contain reproducibility documentation including:

- database name;
- search date;
- exact or database-specific query;
- filters;
- result counts;
- recall/positive-control validation;
- relevance/noise diagnostics where performed;
- methodological decisions and query-repair rationale.

Raw Scopus, IEEE Xplore, Web of Science, and equivalent database exports will not be committed to the public repository unless redistribution is explicitly permitted.

---

# Protocol Amendments

Any meaningful change made after Version 1.0 will be recorded below.

| Date | Version | Change | Reason |
|---|---|---|---|
| 25 Sep 2026 | 1.0 | Initial protocol frozen | Start of SLR |
| 29 Sep 2026 | 1.1 | Scopus pilot strategy refined and **V0.3c frozen** as the final Scopus implementation. Final filtered Scopus corpus: **60 records**. | Earlier query versions retained excessive candidate volumes. V0.3c introduced stronger MAS and focal-application centrality while preserving the substantive RQ0–RQ4 scope and validated recall. |
| 29 Sep 2026 | 1.1 | S1 (*Smart water management approach for resource allocation in High-Scale irrigation systems*) retained as a **supplementary-search / citation-chaining seed** rather than a mandatory primary-query recall control. | Recovering S1 required reopening a broad agricultural agent-based-modelling pathway that substantially increased retrieval volume. S1 remains eligible if later recovered and if full-text assessment satisfies the substantive MAS criteria. |
| 29 Sep 2026 | 1.1 | IEEE Xplore V0.3c translated into two separately executed branches: **V0.3c-A** and **V0.3c-B**. | IEEE Xplore search constraints made a single direct translation of the complete Scopus expression impractical. The final IEEE corpus is defined as the unique union `A ∪ B`. |
| 29 Sep 2026 | 1.1 | IEEE V0.3c-A repaired by adding generic `control` to the functional block. Final IEEE result: **19 A records + 6 B records − 1 branch overlap = 24 unique records**. | Recall validation identified the grain-storage microclimate study as a genuine false negative. The targeted repair recovered it while introducing only a small increase in retrieval volume. All three IEEE-specific positive controls were then retrieved. |
| 30 Sep 2026 | 1.1 | Web of Science Core Collection V0.3c translated using `TI` and `AB` fields and frozen with **51 final filtered records**. | The WoS translation preserved the frozen V0.3c title/abstract logic. Recall validation retrieved the indexed explicit-MAS controls; no WoS-specific query repair was required. |
| 30 Sep 2026 | 1.1 | Web of Science validation confirmed that the Dairy integrated-decision study and Resource-allocation DSS control were not found in the full WoS Core Collection, while S1 was indexed but not retrieved by V0.3c. | Absence of non-indexed controls is not treated as a query failure. The S1 result is consistent with the previously documented supplementary-seed decision and therefore did not trigger query expansion. |
| 30 Sep 2026 | 1.1 | Raw database CSV/Excel/RIS exports designated as **private working/audit data**; the public repository will retain methodological and reproducibility documentation instead. | Database exports may contain provider-supplied or licensed metadata and abstracts that should not be redistributed unnecessarily through the public repository. |
| 1 Oct 2026 | 1.1 | ACM Digital Library removed from the primary database set. Final planned primary sources: **Scopus, Web of Science Core Collection, IEEE Xplore, ScienceDirect, and SpringerLink**. | The available ACM Basic Edition permitted a preliminary title-only search but did not provide the advanced query-editing functionality required to reproduce the frozen V0.3c title/abstract Boolean strategy. A simplified ACM search was rejected because it would not be methodologically comparable with the other primary database implementations. Relevant ACM publications may still be recovered through overlapping indexes and citation searching. |
