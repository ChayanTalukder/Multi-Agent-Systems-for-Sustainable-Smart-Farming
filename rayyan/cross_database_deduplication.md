# Rayyan Screening Workflow

**Software:** Rayyan  
**Last updated:** 3 October 2026

---

## Cross-Database Deduplication

Five final database-level corpora were imported:

| Database | Records |
|---|---:|
| Scopus | 60 |
| IEEE Xplore | 24 |
| Web of Science Core Collection | 51 |
| ScienceDirect | 20 |
| SpringerLink | 31 |
| **Total imported** | **186** |

Rayyan duplicate detection identified 141 possible duplicate records.

All duplicate candidates were manually resolved before screening.

- Unresolved: 0
- Retained from duplicate sets: 57
- Marked as not duplicate: 0
- Duplicate records deleted: 84

Therefore:

```text
186 imported records
- 84 duplicate records removed
= 102 unique records
```

**102 unique records were retained for formal title/abstract screening.**

---

## Title and Abstract Screening

All 102 deduplicated records were screened using the predefined inclusion and exclusion criteria.

| Decision | Records |
|---|---:|
| Included for full-text assessment | 51 |
| Excluded | 51 |
| Maybe | 0 |
| **Total screened** | **102** |

```text
102 records screened
- 51 excluded
= 51 records advanced to full-text screening
```

Title/abstract screening was completed with no unresolved records.

---

## Full-Text Screening

Full-text assessment was conducted for the 51 records retained after title/abstract screening.

Full texts were successfully obtained for 35 records. The remaining 16 reports could not be retrieved after available access routes were checked and were retained in Rayyan as `Maybe` with the note:

```text
Full text unavailable — retrieval pending
```

Current full-text outcome:

| Decision | Records |
|---|---:|
| Included | 34 |
| Excluded after full-text assessment | 1 |
| Full text not retrieved (`Maybe`) | 16 |
| **Total** | **51** |

For PRISMA reporting:

```text
Reports sought for retrieval        = 51
Reports not retrieved               = 16
Reports assessed for eligibility    = 35
Reports excluded after full text    = 1
Studies currently included          = 34
```

Records for which the full text could not be obtained were **not excluded on substantive eligibility grounds**. They are documented separately as reports not retrieved.

---

## Screening Outcome

The Rayyan workflow currently gives:

```text
186 database records imported
↓
84 duplicate records removed
↓
102 unique records screened
↓
51 excluded at title/abstract stage
↓
51 reports sought for full text
↓
16 reports not retrieved
↓
35 full texts assessed
↓
1 full-text exclusion
↓
34 studies included
```

The **34 included studies** form the current corpus for data extraction and quality assessment.

The 16 unavailable reports remain documented separately and may be reassessed if their full texts become available.
