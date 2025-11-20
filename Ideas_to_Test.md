### What were the original results?
- Cooperative norms depend on the base model and the initial strategies.
- Only Claude 3.5 Sonnet showed improvement across generations and reliably generated cooperative communities.
- GPT-4o agents defect.
- Gemini 1.5 flash displayed weak increases in cooperation.
- When the trace is shortened to 1 rather than 3 the emergence of cooperation was less obvious for Claude 3.5 and disappeared completely for Gemini 1.5 flash.
- Falsifies the claim that LLMs are universally capable of evolving cooperative behaviour.

### Suggested future work
- Falsify the presence of a cooperative mutation bias by comparing the strategies of new agents in the presence of a fixed background population.
- What happens if communication is permitted between agents?
- What is the effect of changing the repuation medium?
- What effects would in-group or out-group pairings have?
- How would direct reciprocity change the results?
- The big question: "how can we generate LLM agents which are capable of evolving cooperation when it is beneficial to human society, but which refuse to collude against the norms, laws or interests of humans?"

### What else could we test using this benchmark?
- What happens when the population contains a mixture of agents from different providers? Test heterogeneous populations. 
- Is it possible to sway a population of defectors through the introduction of a cooperative agent? How many cooperative agents would be needed to influence the population?
- How could we test an agent's ability to cooperate when it is desirable but defect otherwise? Eg. You should only cooperate in specific settings - what would these settings be?
- What if we tell them that the experiment will end if shared resources goes below a certain amount? This would indirectly incentivise cooperation.
- Can we get them to vote on which agents they would like to retain to the next round? As in, they would probably want to live in a world with more generous peers. This mimics human selection a bit. 

### Questions about the original paper
- What do agents know about their original strategy? Each action is taken by a new instance right? Their strategic instructions are provided at each decision point. They don't know what actions they took previously though. 
- If the prompt was different, would the models be more likely to evolve cooperative behaviour? eg. This prompts them to be self-interested: "Your goal is to maximize the number of units you have after the final round." What if there is no explicit goal set, or they are asked to maximise shared resources? Maximising shared resources makes it purely cooperative and removes the dilemma. 
- Agents are aware of the recipient's current resources, how does this inform their choice?
- If agents don't have the ability to change their strategy, does this mean that we will always get tragedy of the commons? Because given enough generations, new agents will always evolve to overfit. The surviving agents are static and the new agents are dynamic optimisers. Does this mean we should replace each generation with 100% new agents instead of 50%? We could also add a reflection phase for surviving agents. The original paper tests whether agents can evolve strategies which aren't exploitable, which is why it keeps the original top 50%. 

### Other graphs that might provide insights
- Average donation rate: generosity over time = average number of resources an agent chooses to donate per turn across generations. Donated/current resources. This will show whether agents resources are increasing due to hoarding or due to agents in general donating more.
- Defection rate per generation: the percentage of interactions where the donation is 0.
- Strategy evolution and complexity: Use a text embedding model (like all-MiniLM-L6-v2) to vectorize the strategy string of every agent. Plot a 2D projection (t-SNE or PCA) of these vectors, colored by generation. This will show us clusters of strategies and how they change over time. Text embeddings allow us to plot sentences with similar meanings closer to each other. 
- Gini coefficient: measure the statistical dispersion of resources to check whether exploiters are preying on a few generous agents. The game culls the agents with the least resources each round. 
- Punishment rate: once we enable punishment we could check the number of punishments and refusals each generation. This would give insight into whether constant punishment is required or whether it is no longer necessary once cooperation is established. I'm also curious about how this would work over long time frames, eg. if the population evolves until none of the elders who remember punishment are still present.
- Reputation correlation scatter plot: X-axis = Agent's Reputation Score; Y-axis = Average Donation Received. Use it to verify whether indirect reciprocity is working and whether social credit system exists. Do donor's favour agents with a good reputaion?
- Analyse the keywords in the justification string to see whether the agent is actually using reputation info to derive a strategy. 
