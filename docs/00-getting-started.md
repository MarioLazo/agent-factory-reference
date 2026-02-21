# Getting Started

[← Back to Index](../README.md)

---

## 📣 What This Is

<!-- 
💡 PLAIN ENGLISH: This is a starting point, not a complete manual.
Think of it like a well-organized toolbox — we've gathered the tools that 
actually work, but you still need to know how to use them for your specific job.
-->

This reference started as a simple list. It grew into what I wish had existed when I was in front of hospital CIOs and bank risk committees trying to explain why most AI pilots fail — not because the technology is bad, but because nobody had a map.

If it saves one team from rebuilding what already exists, or helps one practitioner find the right ontology before spending six months on the wrong one, it was worth the effort.

**— Mario Lazo**

---

## 🧭 Before You Begin: Setting Expectations

### This Is a Starting Point, Not a Complete Manual

<!-- 
💡 PLAIN ENGLISH: An "Agent Factory" is a system for building and running 
AI assistants that can take actions on your behalf — like automating 
paperwork, analyzing data, or answering questions from your systems.
-->

**What is an "Agent Factory"?**
An Agent Factory is a structured approach to building AI systems that can take actions — reading documents, querying databases, making recommendations, or automating workflows. Unlike simple chatbots that just answer questions, these agents interact with your real systems.

**Why does this require expertise?**
Building agents for regulated industries (healthcare, finance, supply chain) isn't like building a demo. In these environments:

- **A wrong answer can cause real harm** — misdiagnosed patients, bad investment advice, supply chain failures
- **Regulations have teeth** — HIPAA violations can cost millions, SEC infractions can end careers
- **Trust is everything** — one bad AI decision can destroy years of institutional credibility

**What you'll need beyond this reference:**

| What | Why |
|------|-----|
| **Domain expertise** | Someone who deeply understands healthcare workflows, financial regulations, or supply chain operations |
| **Compliance knowledge** | A person (or team) who knows your specific regulatory obligations — not generic AI ethics, but actual legal requirements |
| **Technical implementation skills** | Engineers who can build, test, deploy, and monitor production systems |
| **Organizational buy-in** | Stakeholders who understand that AI adoption is a process, not a one-time installation |

> **Bottom line**: This reference shows you *what tools exist*. You still need people who understand *how to use them responsibly* in your specific context.

### What This Guide Is and Isn't

| ✅ This Guide IS | ❌ This Guide IS NOT |
|------------------|---------------------|
| A curated starting point | A complete implementation manual |
| A map of available tools | A guarantee that tools will work for you |
| A compliance checklist starting point | Legal or regulatory advice |
| A living document that evolves | A one-time read-and-forget resource |
| A community effort | The opinion of one person |

### Who Should Use This

- **Technical leads** evaluating agent frameworks for regulated environments
- **Consultants** advising healthcare, finance, or supply chain organizations on AI adoption
- **Product managers** scoping AI capabilities with compliance in mind
- **Compliance officers** understanding what questions to ask about AI systems
- **Researchers** seeking domain-specific datasets and benchmarks

---

## ⚠️ Disclaimer

**Read this before using anything in this guide.**

### Not Legal or Compliance Advice

This is a reference document — a collection of links and descriptions. It is not a product recommendation, legal opinion, or compliance certification. Nothing here substitutes for:

- Your organization's legal counsel
- Your compliance team's evaluation
- Your security team's assessment
- The vendor's own documentation and terms

### Things Change Fast

This list is reviewed and updated **at minimum every two months**. But the AI space moves faster than any document can keep up with:

- Repositories get abandoned
- Standards get superseded
- Regulations change
- Better tools appear weekly
- Companies get acquired or shut down

**If something is outdated, wrong, or missing — open a PR or file an issue.** That's the whole point.

### Data Use Agreements Matter

Several datasets listed here (particularly MIMIC) have strict data use agreements that **prohibit transmission to third-party cloud APIs**. Always read the DUA before touching sensitive data. Violating a DUA can end careers and trigger legal action.

### No Endorsements

Listing a tool here means it was found useful or seen used in production. It does not mean:

- There is a financial relationship with the creators
- It will work for your use case
- It meets your compliance requirements
- It's the best option available

HIPAA, SOC 2, FDA SaMD, SEC/FINRA, EU AI Act, and other frameworks impose obligations that no curated GitHub list can satisfy. You still have to do the work.

---

## 📚 Recommended Companion References

This guide focuses on AI agents for regulated industries. These complementary resources cover areas we don't:

### General AI/ML Engineering

| Resource | What It Covers | Link |
|----------|---------------|------|
| **Awesome Machine Learning** | Foundational ML libraries and tools | [github.com/josephmisiti/awesome-machine-learning](https://github.com/josephmisiti/awesome-machine-learning) |
| **ML Papers of the Week** | Current research worth reading | [github.com/dair-ai/ML-Papers-of-the-Week](https://github.com/dair-ai/ML-Papers-of-the-Week) |
| **Papers With Code** | Research papers with implementations | [paperswithcode.com](https://paperswithcode.com/) |
| **Hugging Face Hub** | Models, datasets, demos | [huggingface.co](https://huggingface.co/) |

### LLM-Specific Resources

| Resource | What It Covers | Link |
|----------|---------------|------|
| **LLM Course** | Comprehensive LLM learning path | [github.com/mlabonne/llm-course](https://github.com/mlabonne/llm-course) |
| **Awesome LLM** | Curated LLM tools and research | [github.com/Hannibal046/Awesome-LLM](https://github.com/Hannibal046/Awesome-LLM) |
| **Open LLM Leaderboard** | Model benchmarks and comparisons | [huggingface.co/spaces/open-llm-leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) |

### Prompt Engineering & RAG

| Resource | What It Covers | Link |
|----------|---------------|------|
| **Prompt Engineering Guide** | Prompting techniques that work | [github.com/dair-ai/Prompt-Engineering-Guide](https://github.com/dair-ai/Prompt-Engineering-Guide) |
| **Awesome RAG** | Retrieval-augmented generation patterns | [github.com/frutik/Awesome-RAG](https://github.com/frutik/Awesome-RAG) |
| **LangChain Templates** | Production-ready agent patterns | [github.com/langchain-ai/langchain/tree/master/templates](https://github.com/langchain-ai/langchain/tree/master/templates) |

### AI Safety & Governance

| Resource | What It Covers | Link |
|----------|---------------|------|
| **NIST AI RMF Playbook** | Risk management framework implementation | [airc.nist.gov/AI_RMF_Knowledge_Base](https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook) |
| **AI Incident Database** | Documented AI failures and harms | [incidentdatabase.ai](https://incidentdatabase.ai/) |
| **Responsible AI Toolbox** | Microsoft's fairness and explainability tools | [github.com/microsoft/responsible-ai-toolbox](https://github.com/microsoft/responsible-ai-toolbox) |

### Data Engineering

| Resource | What It Covers | Link |
|----------|---------------|------|
| **Awesome Data Engineering** | Data pipeline tools and patterns | [github.com/igorbarinov/awesome-data-engineering](https://github.com/igorbarinov/awesome-data-engineering) |
| **Great Expectations** | Data validation and documentation | [github.com/great-expectations/great_expectations](https://github.com/great-expectations/great_expectations) |
| **dbt** | Data transformation in warehouses | [github.com/dbt-labs/dbt-core](https://github.com/dbt-labs/dbt-core) |

### MLOps & Deployment

| Resource | What It Covers | Link |
|----------|---------------|------|
| **Awesome MLOps** | Production ML operations | [github.com/visenger/awesome-mlops](https://github.com/visenger/awesome-mlops) |
| **MLflow** | Experiment tracking and model registry | [github.com/mlflow/mlflow](https://github.com/mlflow/mlflow) |
| **Weights & Biases** | Experiment tracking and monitoring | [wandb.ai](https://wandb.ai/) |

> **Why these?** They fill gaps. This reference focuses on domain-specific tools for regulated industries. The resources above cover general ML/AI infrastructure that you'll also need.

---

## 📌 How to Use This Guide

### Document Structure

| Document | What You'll Find |
|----------|------------------|
| [01-agent-frameworks.md](01-agent-frameworks.md) | Orchestration tools: LangChain, AutoGen, CrewAI, etc. |
| [02-finance.md](02-finance.md) | Finance repos + MCP servers |
| [03-healthcare.md](03-healthcare.md) | Healthcare repos + MCP servers |
| [04-supply-chain.md](04-supply-chain.md) | Supply chain tools and datasets |
| [05-ontologies.md](05-ontologies.md) | FIBO, SNOMED, UMLS, GS1, domain vocabularies |
| [06-datasets.md](06-datasets.md) | MIMIC, FAERS, FRED, M5, training data |
| [07-papers-learning.md](07-papers-learning.md) | Research, associations, where to learn more |
| [08-regulations.md](08-regulations.md) | HIPAA, FDA, SEC, EU AI Act, compliance checklists |
| [09-community.md](09-community.md) | Contributing, adoption, quality standards |

### Search Tips

- Use `Ctrl+F` / `Cmd+F` to search for specific tools or terms
- Keywords are written in plain English — search for what you need, not acronyms
- Each entry includes a one-line description of what it does

### Reading Time

- **Skim the tables**: ~10 minutes
- **Read descriptions**: ~45 minutes
- **Deep dive with links**: Several hours

---

[Next: Agent Frameworks →](01-agent-frameworks.md)
