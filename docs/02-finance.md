# Finance — Tools & MCP Servers

[← Back to Index](../README.md) | [← Agent Frameworks](01-agent-frameworks.md) | [Next: Healthcare →](03-healthcare.md)

---

<!-- 
💡 PLAIN ENGLISH: These are specialized AI tools built specifically for 
financial work — analyzing market data, reading SEC filings, understanding 
financial news, and helping with investment research. They understand 
financial language and concepts better than general-purpose AI.
-->

> **In simple terms:** Tools that help AI understand money, markets, and financial documents — like having an analyst who can read millions of pages instantly.

---

## Core Repositories

---

**[FinGPT](https://github.com/AI4Finance-Foundation/FinGPT)**
> _Open-source financial LLMs with continuous fine-tuning pipelines_

The standout feature isn't the models themselves — it's the **continuous update mechanism**. Financial markets are relentlessly current; a model trained six months ago on earnings calls is already stale. FinGPT solves this with automated pipelines that ingest market news, SEC filings, and social sentiment to fine-tune lightweight models (LLaMA, Falcon) on an ongoing basis. Most relevant for **sentiment analysis agents** and **market intelligence tools**.

---

**[FinNLP](https://github.com/AI4Finance-Foundation/FinNLP)**
> _NLP data pipelines and benchmarks for financial text_

The data layer that feeds FinGPT and similar models. Standardized connectors for financial news APIs, SEC EDGAR, Reddit/social sentiment, and earnings call transcripts — all formatted for LLM consumption. Includes NLP benchmarks for financial tasks: NER for companies and people, sentiment classification, and QA over financial documents. Saves weeks of ETL work when building **document intelligence agents**.

---

**[TradingAgents](https://github.com/virattt/ai-hedge-fund)**
> _Multi-agent trading system with specialized analyst roles_

A fully realized multi-agent architecture where distinct agents take on analyst personas: fundamentals analyst, technical analyst, sentiment analyst, risk manager, and portfolio manager who synthesizes their recommendations. Best open-source demonstration of the **role-based agent factory pattern** in finance. Excellent reference architecture for decision-support systems where multiple specialist AI perspectives are reconciled before a human makes a final call.

---

**[AI Hedge Fund](https://github.com/virattt/ai-hedge-fund)**
> _Complete AI-powered investment research and portfolio simulation_

End-to-end simulation of an AI-driven hedge fund: data ingestion, LLM-based analysis, trade signal generation, portfolio tracking. Not production-ready for live trading, but the most complete **reference implementation** for understanding how all the pieces fit together.

---

**[FinRL](https://github.com/AI4Finance-Foundation/FinRL)**
> _Deep reinforcement learning for quantitative finance_

The go-to library for RL-based trading strategy development. Provides a standardized gym environment for financial markets, multiple RL algorithm implementations (PPO, SAC, TD3), and integration with real market data sources. Most relevant for **algorithmic trading teams** and **quantitative researchers**. Requires extensive backtesting before any production consideration.

---

**[FinRobot](https://github.com/AI4Finance-Foundation/FinRobot)**
> _AI agent platform connecting finance data to LLMs_

Middleware between raw financial data and conversational AI. Agent SDK with built-in connectors to market data APIs, pre-built financial analysis tools (DCF modeling, ratio analysis, peer comparison), and agent templates for common finance workflows. If your team is building a **financial analyst copilot** or **client-facing research assistant**, FinRobot provides domain-specific tooling that generic agent frameworks lack.

---

**[Qlib (Microsoft)](https://github.com/microsoft/qlib)**
> _Enterprise quantitative investment AI platform from Microsoft Research_

Microsoft Research's production-grade quant platform — the most enterprise-ready option on this list. Covers the entire quant workflow: data handling, feature engineering, model training, backtesting, portfolio optimization, and live trading integration. Modular architecture allows replacing individual components. Best for **quantitative research teams** at institutional investors.

---

**[FinRL-DeepSeek](https://github.com/AI4Finance-Foundation/FinRL-DeepSeek)**
> _FinRL enhanced with DeepSeek reasoning models_

Integrates FinRL's RL infrastructure with DeepSeek's chain-of-thought reasoning. More interpretable trading rationales — a significant advantage in regulated environments where you need to **explain why an AI system recommended a trade**. Directly addresses core compliance challenges in AI-assisted trading.

---

**[AI4Finance Foundation](https://github.com/AI4Finance-Foundation)**
> _Umbrella organization for all open-source finance AI research_

Parent org for FinGPT, FinRL, FinNLP, FinRobot, and related projects. Follow as an organization to track what's coming next in finance AI.

---

**[FinLLM-Leaderboard / PIXIU](https://github.com/chancefocus/PIXIU)**
> _Benchmarking LLMs on financial tasks_

Before deploying any LLM in finance, know how it performs on domain-specific tasks: financial QA, NER, sentiment. PIXIU provides standardized benchmarks and a leaderboard for objective model comparison. Critical for **model selection decisions** and for justifying those choices to compliance and risk teams.

---

**[Open-Finance-Lab](https://github.com/Open-Finance-Lab)**
> _Collaborative research lab for open financial AI_

Focused on open, reproducible research in financial AI. Valuable for teams wanting to access peer-reviewed paper implementations or contribute to the community.

---

**[FinanceBench](https://github.com/patronus-ai/financebench)**
> _QA benchmark for financial reasoning over real documents_

Tests LLM performance on questions from actual 10-K and 10-Q filings — numerical reasoning, document understanding, financial logic. Use it to **validate models before finance deployments**.

---

**[OpenBB Terminal](https://github.com/OpenBB-finance/OpenBBTerminal)**
> _Open-source Bloomberg Terminal alternative_

Aggregates 100+ financial data sources. Useful as both a **reference data layer** for agent builds and a standalone analyst tool. Increasingly integrating with AI agents through its API layer.

---

**[500 AI Agents Projects — Finance Section](https://github.com/ashishpatel26/500-AI-Agents-Projects)**
> _Curated use cases with working implementations_

Concrete, runnable examples for: fraud detection, risk assessment, customer support, compliance monitoring, and more. Best as an **idea catalog** when scoping new agent capabilities.

---

## MCP Servers — Finance

<!-- 
💡 PLAIN ENGLISH: MCP servers are like "power adapters" that let AI agents 
plug into real data sources and services. Instead of the AI just making 
things up, it can actually look up real SEC filings, pull live stock 
prices, or read actual bank statements through these connections.
-->

> **In simple terms:** These are the cables that connect AI agents to real financial data — so they're working with facts, not guesses.

MCP (Model Context Protocol) servers are the **tool layer** of your agent stack — exposing structured, auditable APIs that agents use to query data, execute actions, and interact with external systems.

---

**[SEC EDGAR MCP](https://github.com/stefanoamorelli/sec-edgar-mcp)**
> _Direct AI access to SEC filings with exact numeric precision_

Real-time access to the full SEC EDGAR database: 10-K/10-Q filings, 8-K events, insider trading (Form 3/4/5), XBRL-parsed financial statements. Responses include source URLs for verification — critical for compliance audits. Exact numeric precision design prevents rounding errors in quantitative workflows.

```json
{
  "mcpServers": {
    "sec-edgar": {
      "command": "docker",
      "args": ["run", "-i", "--rm", "stefanoamorelli/sec-edgar-mcp:latest"]
    }
  }
}
```

---

**[EdgarTools + MCP Server](https://github.com/dgunning/edgartools)**
> _AI-native SEC EDGAR library with built-in MCP server_

10-30x faster than alternatives for EDGAR data extraction. Production MCP server included. Parses XBRL statements, tracks insider trading via Form 4, extracts institutional holdings from 13-F filings. Text formatted for LLM context, not raw HTML.

```json
{
  "mcpServers": {
    "edgartools": {
      "command": "python",
      "args": ["-m", "edgar.ai"],
      "env": {"EDGAR_IDENTITY": "Your Name your@email.com"}
    }
  }
}
```

---

**[Financial MCP Suite — 8 Specialized Servers](https://github.com/luisrincon23/sec-mcp)**
> _Institutional-grade financial research platform — 8 MCP servers in one_

Eight servers replicating institutional research capabilities: SEC scraping, news sentiment, analyst ratings, institutional holdings, alternative data, industry assumptions, economic data, and research administration. Best for **comprehensive equity research agents** needing all data types integrated.

---

**[Financial Modeling Prep MCP Server](https://github.com/imbenrabi/Financial-Modeling-Prep-MCP-Server)**
> _Complete financial data platform with 20+ toolsets_

Covers quotes, financials, earnings calendar, analyst estimates, insider trades, congressional trading, ESG scores, technical indicators, crypto, forex, and commodities. Dynamically enables/disables toolsets to reduce token overhead. Useful for **wealth management and advisory agents**.

---

**[Bloomberg MCP (blpapi-mcp)](https://github.com/djsamseng/blpapi-mcp)**
> _AI agent access to Bloomberg Terminal data_

For organizations with Bloomberg Terminal access, bridges Bloomberg's professional data to AI agents. Bloomberg has built enterprise middleware on top of MCP for SSO, audit trails, rate limiting, and compliance — a preview of where institutional finance AI infrastructure is heading.

---

**[Financial Datasets MCP](https://github.com/financial-datasets/mcp-server)**
> _Stock market API integration for AI agents_

Clean, simple MCP interface for stock market data — prices, fundamentals, financials. Good starting point for teams building **internal analytics agents**.

---

## Deployment Checklist

Before deploying a finance agent to production:

- [ ] Model risk management documentation complete (per SR 11-7)
- [ ] Independent model validation completed
- [ ] Explainability mechanism in place for agent recommendations
- [ ] Fair lending / disparate impact analysis completed (if credit-related)
- [ ] Supervisory controls defined for trading or execution
- [ ] Legal review of client-facing AI communications
- [ ] Data licensing verified for all market data sources
- [ ] Out-of-sample backtesting with documented methodology

---

[← Agent Frameworks](01-agent-frameworks.md) | [Next: Healthcare →](03-healthcare.md)
