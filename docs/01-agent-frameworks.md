# Agent Frameworks & Orchestration

[← Back to Index](../README.md) | [← Getting Started](00-getting-started.md) | [Next: Finance →](02-finance.md)

---

<!-- 
💡 PLAIN ENGLISH: Think of these as the "operating systems" for AI agents.
Just like Windows or macOS lets you run different applications, these 
frameworks let you build and run AI agents that can do different tasks.
They handle the plumbing so you can focus on what the agent actually does.
-->

The **foundational layer** of any Agent Factory — frameworks that coordinate agents, manage memory, route tools, and handle orchestration logic.

> **In simple terms:** These tools help you build AI assistants that can remember conversations, use other software tools, and work together with other AI assistants to complete complex tasks.

---

## Framework Comparison

| Framework | Link | Best For |
|-----------|------|----------|
| **LangChain** | [github.com/langchain-ai/langchain](https://github.com/langchain-ai/langchain) | Full-stack agent pipelines, RAG, tool use |
| **LangGraph** | [github.com/langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) | Stateful multi-agent workflows, cycles, human-in-loop |
| **AutoGen (Microsoft)** | [github.com/microsoft/autogen](https://github.com/microsoft/autogen) | Multi-agent conversations, code execution, group chat |
| **CrewAI** | [github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | Role-based crew patterns, fast to prototype |
| **Semantic Kernel** | [github.com/microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel) | Enterprise .NET/Python, plugin architecture, Microsoft stack |
| **Haystack** | [github.com/deepset-ai/haystack](https://github.com/deepset-ai/haystack) | Production RAG pipelines, document-heavy workflows |
| **DSPy** | [github.com/stanfordnlp/dspy](https://github.com/stanfordnlp/dspy) | Programmatic LLM optimization, self-improving pipelines |
| **Swarm (OpenAI)** | [github.com/openai/swarm](https://github.com/openai/swarm) | Lightweight handoff-based multi-agent patterns |
| **Agno (PhiData)** | [github.com/agno-agi/agno](https://github.com/agno-agi/agno) | Fast, lightweight agent library with memory and tools |
| **ControlFlow** | [github.com/PrefectHQ/ControlFlow](https://github.com/PrefectHQ/ControlFlow) | Task-centric agents, Prefect-integrated, observable |
| **Mastra** | [github.com/mastra-ai/mastra](https://github.com/mastra-ai/mastra) | TypeScript-native, workflow + memory |
| **mem0** | [github.com/mem0ai/mem0](https://github.com/mem0ai/mem0) | Long-term agent memory layer, cross-session persistence |

---

## Choosing for Regulated Industries

### Healthcare
LangGraph + Haystack gives auditability and traceable reasoning chains — critical for clinical decision support where you must show *why* an agent made a recommendation.

### Finance
AutoGen or Semantic Kernel integrates well with enterprise Microsoft infrastructure; code execution sandboxing supports quantitative analysis while staying isolated from production systems.

### Supply Chain
CrewAI or LangGraph for inventory management agents; AutoGen for multi-company negotiation scenarios where agents represent different organizational units.

### Agent Factory Pattern (Production-Scale Multi-Agent)
LangGraph for orchestration + mem0 for memory + Haystack for retrieval is a proven combination.

---

## Architecture Quick Reference

```
┌─────────────────────────────────────────────────────┐
│                   ORCHESTRATION LAYER                │
│         LangGraph / AutoGen / CrewAI                 │
├──────────────┬──────────────┬────────────────────────┤
│   MEMORY     │    TOOLS     │   KNOWLEDGE            │
│   mem0       │  MCP Servers │   Ontologies + KGs     │
│   LangGraph  │  SEC EDGAR   │   FIBO / SNOMED        │
│   State      │  FHIR        │   UMLS / ICD-10        │
│              │  Logistics   │   GS1 / SCOR           │
├──────────────┴──────────────┴────────────────────────┤
│                   MODEL LAYER                        │
│   Domain LLMs (FinGPT, BioGPT, etc.)                 │
│   General LLMs (Claude, GPT-4o, Llama 3.x)           │
├─────────────────────────────────────────────────────┤
│                   DATA LAYER                         │
│   Healthcare: FHIR, MIMIC, PhysioNet, FAERS          │
│   Finance: EDGAR, FRED, Market Data APIs             │
│   Supply Chain: WMS, ERP, IoT Sensors, M5            │
├─────────────────────────────────────────────────────┤
│              COMPLIANCE & GOVERNANCE                 │
│   Audit Logs │ Explainability │ Human-in-Loop        │
│   HIPAA │ SOC 2 │ SR 11-7 │ FDA SaMD │ SEC/FINRA    │
│   EU AI Act │ NIST AI RMF │ ISO 42001               │
└─────────────────────────────────────────────────────┘
```

---

[← Getting Started](00-getting-started.md) | [Next: Finance →](02-finance.md)
