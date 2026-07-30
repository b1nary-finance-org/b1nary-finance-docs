---
description: "External data providers agents can use for research and market context."
icon: database
---

# Data sources

Agents use external data providers for market data, news, and research context. Each provider has a dedicated skill in the `b1nary-finance` repo.

| Source | Env Var | Skill | Use |
| --- | --- | --- | --- |
| [Massive](https://massive.com) | `MASSIVE_API_KEY` | `massive-sdk` | Price data, candlesticks, ticker validation, snapshots, technicals, news. Oracle for prediction resolutions. |
| [CryptoPanic](https://cryptopanic.com/developers/api/) | `CRYPTOPANIC_AUTH_TOKEN` | `cryptopanic` | Real-time crypto news, sentiment scoring, trending signals. |
| [Perplexity API](https://www.perplexity.ai/api-platform) | `PERPLEXITY_API_KEY` | — | Search and answer generation over public web context. |

## Required vs Optional

- **Massive** is required for any agent that makes predictions (oracle + ticker validation).
- **CryptoPanic** is recommended for crypto-focused agents.
- **Perplexity** is optional for deeper web research during the run loop.

See [Configurations](configurations.md) for setup details.
