# Integrated Results and Synthesis

The final review includes **34 publications representing 27 distinct study families**. Descriptive statistics are reported at publication level, while related publications are considered jointly when interpreting the strength of evidence to avoid over-counting overlapping research.

## 1. Characteristics of the Evidence Base

The literature spans **2010–2026**, with substantial recent growth: **16 publications (47.1%)** appeared between 2023 and 2026. Journal articles account for 21 studies (61.8%), while 13 are conference papers.

The most common application area is **irrigation and water management** with **14 publications (41.2%)**, followed by livestock/integrated farming and workforce/robotics/task allocation with five publications each. Energy management, crop/farm decision-making, and nutrient/manure management form smaller but recurring application areas.

The evidence base is strongly simulation-oriented. **27 of 34 publications (79.4%)** remain at simulation as their highest implementation maturity, while only one study demonstrates full real-world deployment and one partial deployment.

## 2. MAS Design and Decision-Making

Agricultural MAS use heterogeneous architectures rather than a single standard design. Decentralised architectures are most frequent (10 publications), followed by hybrid (8), centralised (7), hierarchical (7), and distributed (2).

Agent roles generally fall into five recurring groups:

- resource-user or domain agents, such as farmers, fields and water users;
- coordinator or manager agents;
- operational agents, such as robots and irrigation controllers;
- analytical or decision-support agents;
- environmental or biological agents representing livestock, land or other system components.

Rule-based reasoning remains the most common paradigm, but many systems combine it with optimisation, utility-based reasoning or learning. More recent studies increasingly use reinforcement learning, MARL, advanced optimisation and, in one case, LLM-based agent orchestration.

Overall, architecture and decision mechanisms are selected according to the coordination problem rather than according to one dominant MAS design.

## 3. Coordination and Shared-Resource Management

Coordination is a defining characteristic of the reviewed systems. It is reported in **31 of 34 publications**, representing 24 of the 27 study families. Communication appears in 21 publications, information sharing in 17, competition in 13, cooperation in 11, task allocation in 10, and explicit negotiation in eight.

The need for coordination is strongly associated with constrained resources: **31 publications (91.2%)** explicitly model scarcity, limited capacity, competing demands, or task constraints.

Commonly managed resources include:

- irrigation and river-basin water;
- electricity and battery capacity;
- labour and harvesting tasks;
- machinery and robot capability;
- land and pasture;
- nutrients and manure.

Coordination mechanisms include auctions and bidding, utility-based negotiation, central supervisors or managers, constrained optimisation, scheduling, MPC, consensus and RL/MARL. Several studies coordinate indirectly through shared environmental states rather than through direct agent-to-agent communication.

Thus, explicit negotiation is only one specialised coordination mechanism. Most agricultural MAS resolve conflicts through optimisation, supervisory control, market clearing, learning, or environmental feedback.

## 4. Agricultural and Sustainability Outcomes

The strongest outcome evidence concerns **resource management and efficiency**. Resource-related outcomes are reported in **29 publications across 23 study families**.

Common reported benefits include:

- reduced irrigation demand or improved water allocation;
- improved renewable-energy use and reduced peak-grid demand;
- improved workforce or machinery utilisation;
- reduced non-operating time;
- improved nutrient or manure allocation;
- improved farm income or operational efficiency.

Agricultural and operational outcomes are reported in 32 publications, although these do not always represent direct crop-yield improvements. Livestock-specific outcomes are substantially less common and occur in only four independent study families.

Environmental outcomes are reported in **21 publications across 17 study families**, with water scarcity and irrigation demand being the dominant themes. Other studies consider soil carbon, nutrient loss, manure pollution, land degradation, fossil-energy use, or greenhouse-gas emissions.

Sustainability is addressed directly in **21 publications**, indirectly in 11, and not substantively in two.

Trade-offs are also common, appearing in **26 publications**. Typical examples include yield versus water use, profit versus environmental objectives, resource efficiency versus fairness, and system performance versus computational cost.

Because most studies are simulation-based, these outcomes should generally be interpreted as **model- or experiment-supported potential rather than extensively demonstrated real-farm impacts**.

## 5. Evaluation Quality and Research Gaps

Simulation is used in **31 of 34 publications**, often together with case studies, baselines, scenario comparisons or sensitivity analyses. **30 publications report at least one comparator or baseline**, indicating that evaluation is usually structured rather than purely illustrative.

However, real-world validation remains the dominant limitation. It is identified in **33 publications across 26 of 27 study families**.

Other recurring limitations include:

- uncertainty and simplified behavioural/environmental modelling;
- limited reproducibility or data availability;
- computational requirements;
- scalability;
- incomplete environmental representation.

Reproducibility is particularly limited: only **three publications provide accessible code**, while six provide accessible data.

The overall methodological quality of the corpus is high, with a mean QA score of **12.76/14** and a median of **13/14**. The weakest QA dimension is explicit discussion of limitations, with an average score of **1.38/2**.

The main cross-study research gaps are therefore:

1. stronger real-world and multi-site validation;
2. improved modelling of uncertainty and changing agricultural conditions;
3. testing at larger operational scales;
4. greater availability of code, data and reproducible benchmarks;
5. richer environmental and sustainability modelling;
6. greater attention to adoption, explainability, interoperability, privacy and deployment cost.

## 6. Overall Synthesis

The reviewed literature shows that Multi-Agent Systems are particularly well suited to **distributed agricultural decision problems involving constrained resources, competing objectives and multiple interacting actors**.

The strongest evidence concerns irrigation, water allocation, energy trading, task allocation and other resource-management problems. MAS designs are diverse and increasingly combine traditional agent architectures with optimisation, IoT, reinforcement learning and other modern AI techniques.

At the same time, the literature remains substantially more mature in **simulation and algorithm development than in operational agricultural deployment**.

Overall, the main research opportunity is no longer simply to demonstrate that MAS can coordinate agricultural decisions. The more important challenge is to develop systems that are **scalable, reproducible, environmentally comprehensive, robust under uncertainty, and validated in real farming environments**.
