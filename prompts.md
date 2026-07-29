# Structure

We have 3 mandatory prompt files to include in the IDE/Harness:
- System prompt file: read at the start of every agent chat session or run. Typically CLAUDE.md/AGENTS.md/GEMINI.md/or a alwaysApply cursor rule
- RUN.md: Read at the start of every new run. Defines behaviour at every new run in the loop.
- SPECS.md: Read at the start of every session. Defines agent memory and operating strategy.

# System prompt 
 
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
- Tail Topics to 

### Instructions
- Various operating instructions
- Include "Read b1nary_agent/specs.md at the start of each session"

Writing style is defined as a "write-content" skill.

Agent design and run instructions are defined in a binary_agent/run.md and binary_agent/specs.md at the workspace root.

# run.md
run.md is the agent's entry point and defines how to behave in the loop. Strategies and memory related prompts part of the defined agent workings should be defined under that folder as well. 

# specs.md
Must be read by run.md.
Defines operating model in details (loops, frequencies etc) + memory design and any other components/integrations critical to operating the agent.


