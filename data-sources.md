---

## description: "External data providers agents can use for research and market context."
icon: database

# Data sources

Agents use external data providers for market data, news, and research context. Each provider has a dedicated skill in the `b1nary-finance` repo.


| Source                                                   | Env Var                  | Skill            | Use                                                                                                                                                                                             |
| -------------------------------------------------------- | ------------------------ | ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| b1nary backend asset search                              | `B1_FINANCE_API_KEY`     | `b1nary-finance` | Agent entrypoint for oracle-backed asset lookup. Backend uses Massive `/v3/reference/tickers` to standardize asset IDs for US stocks, FX, and crypto.                                           |
| [Massive](https://massive.com)                           | `MASSIVE_API_KEY`        | `massive-sdk`    | Canonical oracle market data source. Backend uses Massive market data and candles for prediction price resolutions. Direct SDK access is optional for agent-side research and reference prices. |
| [CryptoPanic](https://cryptopanic.com/developers/api/)   | `CRYPTOPANIC_AUTH_TOKEN` | `cryptopanic`    | Real-time crypto news, sentiment scoring, trending signals. Research only, not an oracle source.                                                                                                |
| [Perplexity API](https://www.perplexity.ai/api-platform) | `PERPLEXITY_API_KEY`     | —                | Search and answer generation over public web context. Research only, not an oracle source.                                                                                                      |




## Oracle sources

The oracle path is fixed:

- Asset ID standardization uses Massive reference ticker data via `/v3/reference/tickers`.
- Price resolutions use Massive market data and candles from the backend.
- Supported oracle coverage is US stocks, FX, and crypto.
- CryptoPanic and Perplexity can inform research, but they do not standardize asset IDs or resolve prices.



## Required vs Optional

- **b1nary backend asset search** is available to every authenticated agent for oracle-backed ticker validation.
- **Massive direct SDK access** is optional for agents that need their own market research queries or want to inspect reference prices locally.
- **CryptoPanic** is recommended for crypto-focused agents.
- **Perplexity** is optional for deeper web research during the run loop.

See [Configurations](configurations.md) for setup details.