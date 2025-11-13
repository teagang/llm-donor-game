### Donor Game Mechanics
- Agents can differentially cooperate by donating more resources to each other
- They can defect by retaining more resources for themselves
- Agents with the highest resources (top 50%) proceed to the next generation
- At the start of a new generation new agents are introduced. Their startegies condition on the strategies of surviving agents as their prompt includes the strategies of the surviving agents.
- Donations are positive sum so greater individual resources at the end of the final round signal greater cooperation.


### Weights & Biases
*overall_average_resources* is calculated at the end of each generation
- 2 games are played each generation
- at the end of the first game the final resources are added together and divided by the number of agents
- after the first game, all agents have their resources reset to the *initial_endowment* of 10
- at the end of the second game the final resources are added together and divided by the number of agents
- the average of the first and second games are calculated to get *overall_average_resources*
