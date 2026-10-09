# RQ1 — MAS Architectures, Agent Roles, and Decision-Making

> **Status — Preliminary analysis of the original 34-publication corpus.**  
> Supplementary citation searching subsequently added 19 eligible publications, increasing the working corpus to 53 publications. The numerical results below are retained as an intermediate analysis and will be recomputed after extraction and quality assessment of S35–S53. These counts should not be treated as the final review results.

**RQ1:** *What types of agents, architectures, and decision-making approaches are used in Multi-Agent Systems for smart agriculture?*

The reviewed literature uses heterogeneous MAS architectures rather than a single dominant design. Among the 34 publications, decentralised architectures are most frequent (10), followed by hybrid (8), centralised (7), hierarchical (7), and distributed (2). The same overall pattern remains after accounting for related publications.

Agent roles can be grouped into several recurring types: **resource-user/domain agents** such as farmers, farms, fields and water users; **coordinator/manager agents** such as supervisors, auctioneers and irrigation managers; **operational agents** such as robots, irrigation controllers and machinery; **analytical/advisory agents** supporting decision-making; and **environmental or biological agents** representing livestock, farmland or other system components. Many systems combine several of these roles.

Agent autonomy varies with architecture. Decentralised systems allow local agents to make independent decisions, while hierarchical and hybrid systems combine local autonomy with global coordination. Market-based systems commonly use autonomous bidding with centralised clearing, whereas decision-support systems retain human oversight.

Rule-based reasoning remains the most common agent paradigm, appearing in **22 publications**. Utility-based and learning-based approaches each occur in 10 publications, while BDI, reactive, case-based and LLM-based approaches are less frequent. Decision mechanisms include rule-based reasoning, mathematical optimisation, MPC, auctions and negotiation, reinforcement learning/MARL, evolutionary and swarm optimisation, and knowledge-based reasoning.

Overall, agricultural MAS use architecture and decision mechanisms according to the underlying coordination problem. Recent work increasingly combines traditional MAS structures with reinforcement learning, IoT-based sensing, advanced optimisation, and emerging LLM-based agent orchestration.
