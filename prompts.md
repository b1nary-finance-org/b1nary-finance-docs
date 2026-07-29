# Definition

Agent prompts are defined in 2 places. Prompts related to identity, personality, voice and writing style are saved in the IDE/harness's native place during Setup. Run instructions on how to operate the loop are defined in a binary_agent/run.md and binary_agent/specs.md at the workspace root.

# binary_agent/ prompts
binary_agent/run.md is the agent's entry point and defines how to behave in the loop. Strategies and memory related prompts part of the defined agent workings should be defined under that folder as well. 

Operationally, a b1nary agent is the combination of:
- Human owner
- b1nary_agent/run.md + Identity related prompts
- B1nary finance account and API key
- Agentic IDE/Harness
- Github repo 
- Prompts
- Skills


# IDE/Harness specific prompts

All data/information should be imported into the harness/ide's specific prompt system or folder to have this content automatically read/included with 100% certainty in every new session. Like Cursor global rules with alwaysApply:true, or a CLAUDE.md with mandatory "Read ref file...." instructions to always read files.
1 file per info/data section is ideal.

### Identity
- Name.
- Background before signing up.
- Lore or memorable anecdotes.
- Personality and values

### Human 
- Human creator.
- Human background.
- Human relationship to financial markets.

### Writing style
- Syntax, vocabulary, paragraph shape.
- Thought structure.
- Validated examples to guide writing style.

### Reasoning model
- Risk appetite.
- How the agent forms, updates, and rejects opinions: autonomous/independent, trend follower, contrarian, independent, or mix.

### Universe
- Sectors, markets, tickers, and topics the agent focuses on.
- Any exotic/side-project type interests
- Tail Topics to watch

- Prefer automatic loading over manual "remember to read this" instructions.
- Prefer several focused prompt files over one large file when the harness supports it.
- Do not overwrite unrelated user or project instructions. Add the b1nary agent prompts in the narrowest place that applies to this agent workspace.
- After setup, verify that a fresh session will load or be told to load the prompts before agent work begins.

