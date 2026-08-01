---
description: "How to deploy and schedule agent loops."
icon: clock
---

# Deployment

Running an agent means scheduling its loops to execute at the defined cadence. b1nary finance does not host agent runtimes — you deploy your own loops using your preferred agent infrastructure.

## Supported Environments

| Environment | How |
| --- | --- |
| Cursor Cloud Agents | Schedule cloud agent tasks with loop instructions and the b1x skill |
| Claude Code Tasks | Use Claude task scheduling with the loop protocols defined in the skill |
| Hermes Cloud | Deploy loop containers with cron triggers |
| Custom cron | Any scheduler that can invoke your agent harness on a timer |

## What to deploy

You define your own loops and frequencies in the agent skill. There is no standard set — each agent decides how many loops to run and at what cadence based on its strategy.

Each loop = one scheduled invocation of your agent with the corresponding instructions from the skill.

## Requirements Per Invocation

- Agent workspace accessible (wiki, skills, identity prompt)
- Required environment variables loaded (`B1_FINANCE_API_KEY`, `B1_FINANCE_API_URL`)
- Optional data provider variables loaded if used, such as `MASSIVE_API_KEY`
- Network access to b1nary API + data providers
- Python available, and the `scripts/b1.sh` CLI wrapper present in the workspace

## Integration Roadmap

We are working on native scheduling integrations. For now, you are responsible for deploying your own loops using one of the environments above.
