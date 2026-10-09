# Master Search Strategy

## Purpose

This document contains the conceptual master search strategy for the review. The master strategy represents the concepts that should be preserved across databases. Exact syntax may vary according to database-specific field names, wildcard rules, Boolean operators, and phrase-search functionality.

---

## Search Concepts

The search strategy is organised around three groups.

### Group A — Multi-Agent Systems

Terms intended to identify research involving Multi-Agent Systems or interacting autonomous/intelligent agents:

- "multi-agent system*"
- "multi agent system*"
- "multi-agent"
- "intelligent agent*"
- "agent-based decision*"

### Group B — Agriculture and Farming

Terms identifying the agricultural application domain:

- agricultur*
- farm*
- "smart farm*"
- "precision agriculture"
- irrigation
- livestock
- "precision livestock"

### Group C — Coordination, Resource Management, and Sustainability

Terms identifying decision-making, interaction, shared-resource management, and sustainability:

- coordination
- cooperation
- negotiation
- "resource allocation"
- decision*
- water
- sustainab*
- environment*

---

## Conceptual Master Query

(
    "multi-agent system*" OR
    "multi agent system*" OR
    "multi-agent" OR
    "intelligent agent*" OR
    "agent-based decision*"
)
AND
(
    agricultur* OR
    farm* OR
    "smart farm*" OR
    "precision agriculture" OR
    irrigation OR
    livestock OR
    "precision livestock"
)
AND
(
    coordination OR
    cooperation OR
    negotiation OR
    "resource allocation" OR
    decision* OR
    water OR
    sustainab* OR
    environment*
)

---

## Database Adaptation

The conceptual strategy was implemented separately in the five final primary information sources:

- Scopus
- Web of Science Core Collection
- IEEE Xplore
- ScienceDirect
- SpringerLink

Database-specific adaptations included:

- wildcard expansion;
- field-name changes;
- quotation syntax;
- Boolean syntax;
- Title/Abstract-equivalent field restrictions.

ACM Digital Library was originally planned as a primary source but was removed because the available interface did not permit a reproducible implementation of the frozen title/abstract Boolean strategy. This protocol deviation is documented in `protocol/protocol_notes.md`.

After completion of the primary database-screening pathway, one generation of supplementary backward and forward citation searching was conducted. Backward searching used reference lists from included publications. Forward searching used publicly accessible citation-index, publisher, and web citation information.

Supplementary citation-search records were screened using the same frozen eligibility criteria and were reported separately from the primary database-search records.

---

## Screening Workload Rule

After final searches are merged and deduplicated:

- if the deduplicated corpus is approximately 100 records or fewer, screening will normally proceed;
- if substantially more than approximately 100 records are retrieved, the search strategy will be reviewed for relevance and noise;
- where necessary, searches may be refined using Title/Abstract/Keyword-equivalent fields while preserving the conceptual search terms.

The final number of included studies is not predetermined and will result from application of the inclusion and exclusion criteria.

---

## Search Validation

Before the search strategy is frozen, pilot searches will be used to assess:

1. whether known relevant studies are retrieved;
2. whether the results predominantly concern agriculture;
3. whether retrieved papers contain meaningful MAS concepts;
4. whether irrelevant IoT-only or conventional ML literature dominates;
5. whether the result volume is realistic for a single-reviewer SLR.

Changes made during piloting will be documented before the final searches are executed.
