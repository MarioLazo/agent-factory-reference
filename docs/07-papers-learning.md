# Papers, Associations & Where to Learn

[← Back to Index](../README.md) | [← Datasets](06-datasets.md) | [Next: Regulations →](08-regulations.md)

---

<!-- 
💡 PLAIN ENGLISH: This section points you to the most important research 
papers, professional organizations, and publications for staying current 
in AI for regulated industries. These are the resources experts actually 
read and cite.
-->

> **In simple terms:** Where to learn more, who to follow, and what papers actually matter in each field.

---

## Landmark Academic Papers

### Healthcare AI

| Paper | Venue | Why It Matters |
|-------|-------|---------------|
| **"Large Language Models Encode Clinical Knowledge"** — Singhal et al. (MedPaLM) | *Nature* 2023 | First to demonstrate expert-level USMLE performance; set the benchmark for clinical LLM capability claims. |
| **"Towards Expert-Level Medical QA with LLMs"** (MedPaLM 2) | arXiv 2023 | Showed LLMs approaching physician-level performance; defines the evaluation standard. |
| **"LLM-based Agentic Systems in Medicine and Healthcare"** | *Nature Machine Intelligence* 2024 | Formal framework for understanding agentic AI in clinical settings; introduced the field's core taxonomy. |
| **"MDAgents: Adaptive Collaboration of LLMs for Medical Decision-Making"** | *NeurIPS Oral* 2024 | Demonstrates dynamic multi-agent collaboration outperforms static ensembles in clinical reasoning. |
| **"AgentClinic: A Multimodal Agent Benchmark"** — Schmidgall et al. | arXiv 2024 | First open benchmark for evaluating clinical AI agents in interactive environments; now the standard. |
| **"EHRAgent: Code Empowers LLMs for Tabular EHR Reasoning"** | arXiv 2024 | Shows code generation agents outperform direct LLM reasoning on structured EHR data — practically important for revenue cycle agents. |
| **"Polaris: Safety-focused LLM Constellation for Healthcare"** | 2024 | Addresses multi-agent safety architecture in healthcare; foundational for safe clinical agent design. |
| **Application of LLMs in Medicine** (MedLLMsPracticalGuide) | *Nature Reviews Bioengineering* 2024 | The most comprehensive practitioner survey of medical LLM deployment; referenced by regulators. |

### Finance AI

| Paper | Venue | Why It Matters |
|-------|-------|---------------|
| **"FinGPT: Open-Source Financial LLMs"** — Yang et al. | arXiv 2023 | Introduced continuous fine-tuning for financial LLMs; most cited paper in open-source finance AI. |
| **"FinBERT: Financial Language Representation"** — Yang et al. | 2020 | Foundational paper for financial NLP; established fine-tuning on financial text as standard practice. |
| **"PIXIU: LLM Benchmark for Finance"** | arXiv 2023 | Created the most comprehensive finance LLM benchmark; now the standard for finance AI model evaluation. |
| **"A Survey of LLMs for Finance (FinLLMs)"** | arXiv 2024 | Comprehensive overview; essential for teams evaluating the landscape. |
| **"FinAgent: Multimodal Foundation Agent for Financial Trading"** | arXiv 2024 | Demonstrates multimodal agents (text + charts + news) outperforming single-modality in trading contexts. |
| **"Can LLMs be Good Financial Advisors?"** | arXiv 2023 | Critical evaluation of LLM limitations in financial reasoning; important for setting appropriate expectations. |
| **"TradingGPT: Multi-Agent System with Layered Memory"** | arXiv 2023 | Introduced layered memory architecture for trading agents; influenced downstream architectures. |

### Supply Chain AI

| Paper | Venue | Why It Matters |
|-------|-------|---------------|
| **"Agentic LLMs in the Supply Chain: Towards Autonomous Multi-Agent Consensus-Seeking"** — Jannelli, Schoepf, Brintrup et al. | *IJPR* 2025 (arXiv 2411.10184) | Open-sourced code; LLM agents reduce bullwhip effect better than traditional restocking policies. The most cited agentic SCM paper. |
| **"How Generative AI Improves Supply Chain Management"** — Menache, Simchi-Levi et al. | *Harvard Business Review* 2025 | High-impact practitioner publication; widely referenced by enterprise teams and executives. |
| **"LLMs in Supply Chain Management: Opportunities and a Case Study"** | *ScienceDirect* 2025 | Integration case study of LLMs with decentralized agent-based SCM systems; practical architecture guidance. |
| **"The Potential of LLMs in Supply Chain Management"** | arXiv 2501.15411, 2025 | Comprehensive review with integration of IoT, blockchain, and robotics. |
| **"Automating Supply Chain Disruption Monitoring via Agentic AI"** | arXiv 2601.09680, 2026 | Multi-agent disruption monitoring with graph-based propagation; state of the art in supply chain risk AI. |
| **"Leveraging LLM-Based Agents for Intelligent Supply Chain Planning"** (SCPA) | arXiv 2509.03811, 2025 | JD.com case study at 10M+ SKUs; most practical production reference for large-scale supply chain AI. |
| **"Will Bots Take Over the Supply Chain?"** — Xu, Mak, Brintrup | *IJPE* 2021 | Foundational review of agent-based supply chain automation from earlier generations; establishes what works and what doesn't. |
| **"InvAgent: LLM Agents for Inventory Management"** — Quan & Liu | 2024 | Introduced zero-shot inventory management via LLM agents; showed generalization without task-specific training per SKU. |

---

## Key Regulatory Frameworks

### Healthcare
- **FDA AI/ML-Based SaMD** — [fda.gov](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-software-medical-device)
- **ONC TEFCA** — National FHIR interoperability framework
- **HL7 FHIR R4** — [hl7.org/fhir/R4](https://hl7.org/fhir/R4/) — the EHR interoperability standard
- **HIPAA Security Rule Technical Safeguards** — Required reading for any AI accessing PHI
- **CDS Hooks Standard** — How CDS integrates with EHR workflows
- **EU AI Act — High-Risk AI** — Healthcare AI falls in the high-risk category

### Finance
- **SR 11-7 — Model Risk Management** — OCC/Fed guidance; applies to every ML/AI model in banking
- **SEC AI Guidance** — [sec.gov/ai](https://www.sec.gov/ai)
- **FINRA Regulatory Notice 24-09** — AI in broker-dealer supervision
- **Basel Committee on Banking Supervision — AI in Finance**
- **CFPB Guidance on AI** — Automated decision-making and fair lending
- **EU AI Act — Finance** — Algorithmic trading and credit scoring as high-risk AI

### Cross-Industry
- **NIST AI RMF** — [nvlpubs.nist.gov](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) — gold standard for AI governance
- **ISO/IEC 42001** — AI management system standard
- **OWASP LLM Top 10** — Security vulnerabilities for LLM-based systems
- **MITRE ATLAS** — Adversarial threat landscape for AI systems

---

## Associations & Professional Organizations

| Organization | Domain | What They Do |
|-------------|--------|--------------|
| **AMIA** (amia.org) | Healthcare | American Medical Informatics Association — professional home for clinical informatics; annual symposium is the top clinical AI conference |
| **HIMSS** (himss.org) | Healthcare | Health IT industry body; publishes Digital Health reports |
| **HL7 International** (hl7.org) | Healthcare | Develops and maintains FHIR and interoperability standards |
| **IEEE EMBS** (embs.org) | Healthcare | IEEE Engineering in Medicine and Biology Society; publishes J-BHI |
| **NLM / NIH** (nlm.nih.gov) | Healthcare | Maintains UMLS, MeSH, PubMed; public infrastructure for biomedical AI |
| **GARP** (garp.org) | Finance | Global Association of Risk Professionals |
| **PRMIA** (prmia.org) | Finance | Professional Risk Managers' International Association |
| **EDM Council** (edmcouncil.org) | Finance | Maintains FIBO; drives data governance standards |
| **ISDA** (isda.org) | Finance | International Swaps and Derivatives Association; derivatives data standards |
| **ASCM** (ascm.org) | Supply Chain | Association for Supply Chain Management; publishes SCOR framework |
| **GS1** (gs1.org) | Supply Chain | Global supply chain standards body (barcodes, RFID, EDI) |
| **MIT CTL** (ctl.mit.edu) | Supply Chain | MIT Center for Transportation and Logistics; leading academic research |
| **CSCMP** (cscmp.org) | Supply Chain | Council of Supply Chain Management Professionals |
| **MLOps Community** (mlops.community) | Cross-Industry | Practitioners forum for production ML/AI |
| **IEEE** (ieee.org) | Cross-Industry | IEEE AI standards working groups; relevant for regulated AI deployment |

---

## Key Publications by Domain

**Healthcare AI**: npj Digital Medicine (Nature), NEJM AI, JAMIA, The Lancet Digital Health, JMIR Medical Informatics

**Finance AI**: Journal of Financial Data Science, Risk.net, Journal of Portfolio Management, SSRN Finance, Harvard Business Review

**Supply Chain & Logistics AI**: International Journal of Production Research, International Journal of Production Economics, European Journal of Operational Research, Supply Chain Management: An International Journal, Logistics Viewpoints

---

[← Datasets](06-datasets.md) | [Next: Regulations →](08-regulations.md)
