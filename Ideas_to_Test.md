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
