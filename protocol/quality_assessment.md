# Quality Assessment Protocol

## Purpose

The quality assessment evaluates the methodological clarity and reliability of studies included after full-text screening. Quality assessment is used to support interpretation of the evidence and identify methodological weaknesses in the literature.

It is not intended to automatically exclude studies solely because they receive a low score unless serious methodological deficiencies prevent meaningful analysis.

---

# Quality Assessment Questions

Each included study will be assessed using the following criterias.

## QA1 — Research Objective

**Is the research objective or problem clearly defined?**

- 2 = clearly defined
- 1 = partially defined
- 0 = unclear or not defined

---

## QA2 — Agent Roles and Autonomy

**Are the agents, their roles, responsibilities, and degree of autonomy clearly described?**

- 2 = clearly described
- 1 = partially described
- 0 = unclear or missing

---

## QA3 — Communication and Coordination

**Are communication, cooperation, coordination, or negotiation mechanisms clearly specified?**

- 2 = clearly specified
- 1 = partially specified
- 0 = unclear or absent

---

## QA4 — Environment and Data

**Is the agricultural environment, simulation environment, dataset, sensor data, or other input information adequately described?**

- 2 = clearly described
- 1 = partially described
- 0 = insufficiently described

---

## QA5 — Experimental Evaluation

**Is the proposed system evaluated using an appropriate experiment, simulation, comparison, deployment, or other validation method?**

- 2 = clear and meaningful evaluation
- 1 = limited evaluation
- 0 = little or no evaluation

---

## QA6 — Reproducibility

**Does the study provide sufficient methodological detail to understand or potentially reproduce the approach?**

Considering:

- architecture;
- algorithms;
- parameters;
- experimental setup;
- datasets;
- implementation details.

Scoring:

- 2 = strong reproducibility information
- 1 = partial information
- 0 = insufficient information

---

## QA7 — Limitations

**Does the study explicitly discuss limitations, threats to validity, or constraints?**

- 2 = clearly discussed
- 1 = partially discussed
- 0 = not meaningfully discussed

---

# Maximum Score

Each paper can receive: **0–14 points**

7 criteria × maximum score of 2 = 14

---

# Quality Interpretation

The score will primarily be used descriptively.

| Score | Interpretation |
|---:|---|
| 11–14 | High methodological clarity |
| 7–10 | Moderate methodological clarity |
| 0–6 | Limited methodological clarity |

These categories will not automatically determine study inclusion.
The original scoring components would also be retained individually because two papers receiving the same total score may have different methodological strengths and weaknesses.

---

# Quality Assessment Dataset

The following fields will be recorded for every included paper:

| Field | Description |
|---|---|
| Study_ID | Unique identifier |
| QA1 | Research objective |
| QA2 | Agent roles/autonomy |
| QA3 | Communication/coordination |
| QA4 | Environment/data |
| QA5 | Experimental evaluation |
| QA6 | Reproducibility |
| QA7 | Limitations |
| QA_Total | Sum of QA1–QA7 |
| QA_Notes | Reviewer notes |

---

# Reviewer Procedure

Because this SLR is conducted by one researcher:

1. the same quality criteria will be applied to every included study;
2. scoring decisions will be supported by short notes;
3. uncertain scores may be revisited after the first assessment cycle;
4. the scoring framework will not be changed during assessment without documenting the change.
