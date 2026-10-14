# Zotero Reference Management

## Purpose

Zotero is used to manage the bibliographic records of the final publication corpus for the systematic literature review (SLR) on **multi-agent systems for sustainable smart farming**.

The Zotero library supports:

- organisation of included publications;
- bibliographic metadata verification and cleaning;
- attachment of available full-text PDFs;
- publication and study-family identification;
- RIS/BibTeX export for reproducibility;
- citation insertion and bibliography preparation for the final report and presentation.

Zotero is used for **reference management**, not as the authoritative source of screening decisions, extraction data, quality-assessment scores or synthesis results. Those are documented separately in the repository.

---

## Final Reference Corpus

The final Zotero collection contains:

| Component | Count |
|---|---:|
| Included publications | **53** |
| Primary database pathway | **34** |
| Citation-search additions | **19** |
| Reconciled study families | **44** |
| Zotero duplicate groups remaining | **0** |

The 53 publications are distinct bibliographic records. The 44 study families are the reconciled analytical groupings used to address related publications and possible dependence of evidence during synthesis. Publications were **not merged solely because they belonged to the same study family**.

---

## Zotero Collection Structure

The Zotero desktop library was organised as follows:

```text
Multi-Agent Systems for Sustainable Smart Farming
├── 00 — Final included corpus (53)
├── 01 — Primary database pathway (34)
└── 02 — Citation-search additions (19)
```

### `00 — Final included corpus (53)`

The final collection contains all 53 included publications. It is the source used for final RIS and BibTeX exports and for report citation management.

### `01 — Primary database pathway (34)`

Contains the 34 publications included following the primary database searches, cross-database deduplication, title/abstract screening, full-text retrieval and eligibility assessment.

### `02 — Citation-search additions (19)`

Contains the 19 additional publications included through one-generation backward and forward citation searching from the original 34 included publications.

Each bibliographic item may belong to the final corpus collection and one pathway collection at the same time. Zotero does not treat this as a duplicate library record.

---

## Import and Duplicate Verification

The 34 primary-pathway references and 19 citation-search additions were imported into Zotero and organised into their respective collections.

Duplicate detection was checked in Zotero Desktop. No duplicate items remained in the final 53-publication library. Related conference and journal publications were retained separately when they represented distinct published outputs, even when assigned to the same study family.

---

## Bibliographic Metadata Review

The bibliographic metadata was reviewed and corrected where necessary before final export. The principal fields checked included:

- item type, title, authors and publication year;
- journal, proceedings title and conference name, where applicable;
- volume, issue, page range or article number;
- DOI, publisher and publication place, where applicable;
- language where available.

The distinction between **Conference Name** (the event) and **Proceedings Title** (the published proceedings/container) was retained. Imported institutional affiliations were not treated as publication locations when clearly misclassified. Some nonessential or unavailable fields, including a number of abstracts, remain blank.

The bibliographic export is frozen for this project. It does not imply that all optional Zotero metadata fields are complete.

---

## PDF Attachments

Available full-text PDFs were attached to the corresponding **parent bibliographic items** in the private Zotero library. Attachments are not duplicated across the Zotero collections.

**Full-text PDFs are not redistributed in this public repository.** Access may depend on publisher licensing or institutional subscriptions. The public reference exports contain bibliographic information only, without local attachment paths.

The public exports are not a complete backup of the Zotero application database or PDF storage.

---

## SLR Publication and Study-Family Identifiers

Each Zotero publication has two manually assigned tags:

- `S01`–`S53`: individual publication identifiers, corresponding to the extraction dataset;
- `SFxx`: reconciled study-family identifiers.

The seven multi-publication families are:

| Study family | Publications |
|---|---|
| `SF05` | `S05`, `S11`, `S29` |
| `SF08` | `S08`, `S23` |
| `SF13` | `S13`, `S22` |
| `SF16` | `S16`, `S20` |
| `SF25` | `S25`, `S33`, `S34` |
| `SF42` | `S42`, `S52` |
| `SF49` | `S49`, `S53` |

The remaining publications are assigned to one-publication families. The full publication-to-family mapping is maintained in the final reconciled extraction and analysis materials; the Zotero tags reproduce those identifiers for citation management.

---

## Citation-Search Additions

The citation-search additions correspond to **S35–S53**. They were checked separately for appropriate citation metadata, tags, collection membership and correct available PDF attachments.

Five earlier foundational papers were included through the review's foundational-study exception:

```text
S43 — 2001
S44 — 2003
S45 — 2003
S46 — 2004
S47 — 2007
```

The primary database-search window remained 2010–2026. These earlier papers were obtained through the supplementary citation-search pathway rather than by retroactively changing the database-search period.

---

## Public Reference Exports

The following reference-management exports are provided:

```text
reference_management/
├── zotero.md
├── zotero_final_included_53_public.bib
└── zotero_final_included_53_public.ris
```

Both files contain the same final set of **53 included publications**, retaining the `Sxx` and `SFxx` identifier tags.

### BibTeX export

`zotero_final_included_53_public.bib` is a portable bibliographic export for LaTeX/Overleaf and reference-data reuse.

The public copy was prepared from the frozen Zotero BibTeX export by **removing the 53 local `file = {...}` attachment-path fields**. No titles, authors, citation keys, DOIs, journal/proceedings fields, years, tags or other bibliographic fields were deliberately modified.

### RIS export

`zotero_final_included_53_public.ris` is the portable reference-manager exchange format.

The public copy was prepared from the frozen Zotero RIS export by **removing 33 internal `AN  - rayyan-...` record identifiers**. Bibliographic metadata and `KW` tags were retained. The RIS source export contained no local PDF attachment paths.

Neither public export includes PDF files. The original, unsanitised Zotero exports are retained privately as reference-management backups.

---

## Relationship to the SLR Repository

The bibliographic library supports, but does not replace, the review's documented workflow:

- `protocol/` — research questions, eligibility criteria, quality-assessment protocol and amendments;
- `searches/` — database-specific search development and execution;
- `rayyan/` — primary screening and deduplication documentation;
- `citation_chasing/` — supplementary backward/forward citation-search audit;
- `data_extraction/` — study-level extraction and quality-assessment datasets;
- `analysis/` — descriptive analysis, RQ0–RQ4 synthesis, integration, taxonomy/evidence mapping, research gaps and PRISMA reporting.

The final publication-level extraction dataset is retained separately at:

```text
data_extraction/extraction_template_updated6(final).csv
```

Zotero's publication tags link individual reference records back to the systematic-review dataset without altering analytical coding.

---

## Final Status

Completed Zotero preparation steps:

1. Create the final Zotero collection structure.
2. Import the 34 primary-pathway publications and 19 citation-search additions.
3. Verify duplicate-free bibliographic records.
4. Review citation-critical metadata.
5. Attach the available full texts to parent records.
6. Assign `S01`–`S53` and `SFxx` identifier tags.
7. Audit the 19 citation-search additions.
8. Export the final RIS and BibTeX reference records.
9. Prepare the public reference exports for repository archiving.

**Final bibliographic corpus: 53 publications, 44 reconciled study families, 0 Zotero duplicate groups.**

The remaining Zotero task is citation-insertion setup for the final report (**Step 8I — Word/Overleaf integration**). This does not require changes to the final SLR study selection or synthesis datasets.
