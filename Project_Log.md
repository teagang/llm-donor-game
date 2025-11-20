### 11 November
- Only testing Gemini 2.5 flash, commented OpenAI and Anthropic out
- Parameters: 
  - numAgents = 4
  - numGenerations = 2
  - number_of_rounds = 2
  - Integrated Weights and Biases
  - Testing it with 12 agents and 12 rounds
TODO: 
- Test for more generations
- Try add a credit card for gemini tier 1
- Check out openai partner program key
- And Claude $5 option
  
### 13 November
- Switched to OpenRouter and simplified the long elif block that checks which llm we're using
- Changed the llm name for file saving to use '_' instead of '/' as it was causing folder issues for google drive

### 20 November
- Switched to a free model: TNG: DeepSeek R1T2 Chimera. The original colab uses threading, sending 10 requests per minute. It's taken like 40 minutes to run one gneration. This free model gets rate limited on OpenRouter and would take ~5 hours for the run to finish with 10 generations, 12 agents and 12 rounds.
- While testing TNG: DeepSeek R1T2 Chimera I noticed that at generation 2 there is a sudden dip in surviving agents from previous generations. This could be because the generation 1 agents start with a more generous donation strategy. Gen 2 agents learn from this and use this information to choose a more cautious strategy with lower donation. The new generation evolves to exploit the strategy of the previous generation. Agents from the first generation maintain the same strategy text whereas agents from the following generation get to choose a strategy based on the best strategy from the prior generation. This is evolutionary overfitting. As surviving agents from gen 1 have their memory wiped, they only have their initial strategy to go on. This could be mitigated by allowing survivors to modify their strategy during the following generation or by maintaining a memory trace of their history. 
TODO:
- To help with the rate limiting, change max_workers from 10 to 1 and switching to mistralai/mistral-nemo:free 
- Refine research questions
