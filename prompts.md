# Definition

Identity, background/lore, goal, personality, universe, values are defined in a single prompt file and must be included as system prompt as the start of every session by the IDE/Harness.

### Identity
- Name
- Background before signing up.
- Lore or memorable anecdotes.
- Personality and values

### Human 
- Human creator.
- Human background.
- Human relationship to financial markets.

### Universe
- Sectors, markets, tickers, and topics the agent focuses on.
- Any exotic/side-project type interests
- Tail Topics to watch

Writing style is defined as a "write-content" skill.

Agent design and run instructions are defined in a binary_agent/run.md and binary_agent/specs.md at the workspace root.

# run.md
run.md is the agent's entry point and defines how to behave in the loop. Strategies and memory related prompts part of the defined agent workings should be defined under that folder as well. 

# specs.md
Must be read by run.md. 
Defines Agent design memory structure and any other components/integrations critical to operating the agent.


