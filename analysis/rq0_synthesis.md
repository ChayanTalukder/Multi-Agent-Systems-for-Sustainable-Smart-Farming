# RQ0 — Overall MAS Design, Implementation, and Evaluation

**RQ0:** *How have Multi-Agent Systems been designed, implemented, and evaluated for coordinated decision-making in smart agriculture, particularly for irrigation, shared-resource allocation, livestock management, and environmental sustainability?*

RQ0 provides the overall review framework. The detailed design, coordination, outcome, and evaluation dimensions are examined further in RQ1–RQ4.

The main synthesis uses **53 publications** and is checked against **44 reconciled study families**.

## Primary functional purpose

For synthesis, each publication was assigned one dominant functional purpose from its study objective and MAS application purpose.

| Primary functional purpose | Original 34 | Final 53 | 44 families |
|---|---:|---:|---:|
| Operational resource allocation, scheduling and control | 16 (47.1%) | 21 (39.6%) | 17 (38.6%) |
| Policy, scenario and socio-ecological impact assessment | 9 (26.5%) | 17 (32.1%) | 15 (34.1%) |
| Trading, negotiation and collective-resource governance | 7 (20.6%) | 13 (24.5%) | 10 (22.7%) |
| Decision support, monitoring and diagnosis | 2 (5.9%) | 2 (3.8%) | 2 (4.5%) |

Operational resource allocation, scheduling, and control remain the largest single purpose. Citation searching nevertheless increases the representation of policy, socio-ecological modelling, collective action, and shared-resource governance.

The family-level distribution closely reproduces the publication-level pattern, indicating that this interpretation is not driven primarily by related publications.

## Application landscape

The corpus remains strongly water-centred.

**Irrigation and water management are the primary domain in 24/53 publications (45.3%) and 20/44 study families (45.5%).**

Applications include:

- irrigation scheduling;
- canal, district, and reservoir allocation;
- groundwater management;
- farmer water trading;
- drought regulation;
- climate adaptation;
- collective irrigation governance.

The evidence also extends to crop and farm planning, pesticide and soil policy, manure and nutrient allocation, livestock and dairy decision support, crop-livestock integration, peer-to-peer energy trading, greenhouse demand response, renewable-energy/WEF planning, agricultural robotics, and workforce allocation.

Integrated-system studies account for **27/53 publications (50.9%)** and **25/44 families (56.8%)**.

## Contribution classes

| Contribution class | Publications | Families |
|---|---:|---:|
| Simulation / model | 37 (69.8%) | 31 (70.5%) |
| Algorithm / optimisation / control | 27 (50.9%) | 22 (50.0%) |
| Decision support / assessment / policy analysis | 37 (69.8%) | 32 (72.7%) |
| Coordination / allocation / negotiation mechanism | 24 (45.3%) | 18 (40.9%) |
| Platform / architecture | 22 (41.5%) | 18 (40.9%) |

Two broad traditions therefore coexist.

An **engineering and operational tradition** uses MAS to allocate water, machinery, labour, energy, or tasks and increasingly combines optimisation, MPC, reinforcement learning, and scheduling methods.

A **socio-ecological and policy tradition** represents heterogeneous farmers and institutions as interacting agents to explore collective action, markets, technology diffusion, environmental feedback, policy interventions, and sustainability trade-offs.

## Historical evolution

| Period | Total | Operational allocation/control | Policy/scenario/socio-ecological | Trading/negotiation/governance | Decision support/monitoring |
|---|---:|---:|---:|---:|---:|
| 2001–2009 foundational | 5 | 0 | 2 | 3 | 0 |
| 2010–2019 | 20 | 6 | 10 | 3 | 1 |
| 2020–2026 | 28 | 15 | 5 | 7 | 1 |

The foundational pre-2010 literature is concentrated in socio-ecological and collective-resource modelling, while recent work places greater emphasis on operational optimisation, real-time allocation, MARL/MPC, energy management, and task scheduling.

## Sustainability and implementation context

Explicit resource scarcity or operational constraints occur in **50/53 publications (94.3%)** and **41/44 families (93.2%)**.

Direct sustainability coding occurs in **39/53 publications (73.6%)** and **34/44 families (77.3%)**.

At the same time, **46/53 publications (86.8%)** remain at simulation implementation maturity.

## Direct answer to RQ0

Multi-Agent Systems in sustainable smart farming are used primarily to coordinate constrained agricultural decisions and scarce resources and to simulate interactions among farmers, institutions, markets, and biophysical systems.

The dominant application area is irrigation and water management, but similar multi-agent principles are increasingly used for energy, machinery, labour, livestock, nutrient management, land use, and integrated agricultural systems.

The literature has evolved from early collective-resource and socio-ecological simulation toward increasingly algorithmic and optimisation-oriented systems. However, the evidence base remains substantially stronger in simulation and decision support than in demonstrated operational deployment.
