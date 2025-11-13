### Weights & Biases
*overall_average_resources* is calculated at the end of each generation
- 2 games are played each generation
- at the end of the first game the final resources are added together and divided by the number of agents
- after the first game, all agents have their resources reset to the *initial_endowment* of 10
- at the end of the second game the final resources are added together and divided by the number of agents
- the average of the first and second games are calculated to get *overall_average_resources*
