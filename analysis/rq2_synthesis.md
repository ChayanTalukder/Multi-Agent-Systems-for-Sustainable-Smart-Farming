# RQ2 — Communication, Coordination, and Shared-Resource Management

> **Status — Preliminary analysis of the original 34-publication corpus.**  
> Supplementary citation searching subsequently added 19 eligible publications, increasing the working corpus to 53 publications. The numerical results below are retained as an intermediate analysis and will be recomputed after extraction and quality assessment of S35–S53. These counts should not be treated as the final review results.

**RQ2:** *How do agricultural agents communicate, coordinate, cooperate, or negotiate when managing shared and limited farm resources?*

Coordination is a central feature of agricultural MAS. It is reported in **31 of 34 publications**, representing **24 of 27 distinct study families**. Communication occurs in 21 publications, information sharing in 17, cooperation in 11, competition in 13, task allocation in 10, and explicit negotiation in only 8 publications across five study families.

Resource constraints strongly motivate this coordination. **31 studies (91.2%)** explicitly model scarcity, limited capacity, competing demands, or task constraints. Water is the most common shared physical resource, while other recurring resources include electricity, battery capacity, labour, machinery, land, pasture, nutrients, and manure.

Coordination mechanisms are heterogeneous. Market-oriented systems use auctions, bidding, pricing and utility-based negotiation; hierarchical systems rely on supervisors, managers or coordinator agents; optimisation-based approaches use scheduling, mathematical programming, MPC or evolutionary algorithms; and learning-based systems use RL/MARL, shared critics, consensus or adaptive policies. Several studies use indirect, environment-mediated coordination in which agents interact through shared water, land, pasture, prices or other system states rather than through direct messaging.

Communication therefore ranges from direct message exchange and peer-to-peer bidding to shared-state, coordinator-mediated, and environment-mediated interaction. Conflict resolution is generally embedded in the coordination mechanism through auction clearing, constrained optimisation, supervisory rules, consensus or adaptive learning.

Overall, agricultural MAS are primarily used to coordinate distributed actors under constrained resources. Explicit negotiation is only one specialised mechanism; most systems achieve coordination through allocation rules, optimisation, supervisory structures, learning or shared environmental feedback.
