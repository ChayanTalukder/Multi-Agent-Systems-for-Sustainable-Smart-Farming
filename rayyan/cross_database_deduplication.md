# Rayyan Screening Workflow

**Software:** Rayyan  
**Last updated:** 9 October 2026

---

## Primary Database-Search Pathway

Five final database-level corpora were imported:

| Database | Records |
|---|---:|
| Scopus | 60 |
| IEEE Xplore | 24 |
| Web of Science Core Collection | 51 |
| ScienceDirect | 20 |
| SpringerLink | 31 |
| **Total imported** | **186** |

Rayyan duplicate detection identified possible duplicate records and all duplicate candidates were manually resolved before screening.

A total of **84 duplicate records were removed**.

```text
186 imported database records - 84 duplicate records = 102 unique primary-search records
```

### Title / Abstract Screening

| Decision | Records |
|---|---:|
| Advanced to full-text assessment | 51 |
| Excluded | 51 |
| **Total** | **102** |

### Full-Text Screening

| Outcome | Reports |
|---|---:|
| Reports sought for retrieval | 51 |
| Reports not retrieved | 16 |
| Reports assessed for eligibility | 35 |
| Full-text exclusions | 1 |
| **Included publications** | **34** |

The 16 reports that could not be retrieved were not treated as substantive eligibility exclusions.

---

# Supplementary Citation-Search Pathway

After completion of the initial database-screening pathway, one generation of backward and forward citation searching was conducted from the 34 initially included publications.

The supplementary search identified **24 new candidate records**.

These were compared with the complete 102-record post-deduplication database-search corpus. No citation-search candidate represented an existing primary-search record.

After import into Rayyan, duplicate detection identified three highly similar publication pairs. Manual inspection confirmed that all three pairs represented related but distinct publications, and both publications in each pair were retained.

### Title / Abstract Screening

| Decision | Records |
|---|---:|
| Advanced to full-text assessment | 21 |
| Excluded | 3 |
| **Total** | **24** |

### Full-Text Retrieval and Screening

| Outcome | Reports |
|---|---:|
| Reports sought for retrieval | 21 |
| Reports not retrieved | 1 |
| Reports assessed for eligibility | 20 |
| Full-text exclusions | 1 |
| **Included publications** | **19** |

The report not retrieved was:

**SHADOC: a multi-agent model to tackle viability of irrigated systems**

The citation-search full-text exclusion was:

**A new BDI agent architecture based on the belief theory. Application to the modelling of cropping plan decision-making**

Reason:

**Insufficient meaningful multi-agent interaction**

---

# Combined Review Status

The two identification pathways are retained separately for PRISMA reporting.

```text
PRIMARY DATABASE PATHWAY

186 records imported
↓
84 duplicates removed
↓
102 records screened
↓
51 title/abstract exclusions
↓
51 reports sought
↓
16 reports not retrieved
↓
35 full texts assessed
↓
1 full-text exclusion
↓
34 publications included
```

```text
SUPPLEMENTARY CITATION-SEARCH PATHWAY

24 new records identified
↓
24 records screened
↓
3 title/abstract exclusions
↓
21 reports sought
↓
1 report not retrieved
↓
20 full texts assessed
↓
1 full-text exclusion
↓
19 publications included
```

Therefore:

```text
34 primary-search inclusions
+19 citation-search inclusions
=53 included publications
```

Across both pathways:

| Outcome | Total |
|---|---:|
| Reports sought for retrieval | 72 |
| Reports not retrieved | 17 |
| Reports assessed at full text | 55 |
| Full-text exclusions | 2 |
| **Included publications** | **53** |

The 53 included publications form the current working corpus for final data extraction, quality assessment, study-family reconciliation, and evidence synthesis.
