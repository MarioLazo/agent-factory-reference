# Healthcare — Tools & MCP Servers

[← Back to Index](../README.md) | [← Finance](02-finance.md) | [Next: Supply Chain →](04-supply-chain.md)

---

<!-- 
💡 PLAIN ENGLISH: These are AI tools designed for medical and clinical 
settings — reading patient records, understanding medical terminology, 
helping with diagnoses, and automating paperwork. They're built to 
understand healthcare-specific language and workflows.

⚠️ IMPORTANT: Healthcare AI has strict regulations (HIPAA, FDA) and
can directly impact patient safety. These tools require careful 
evaluation and proper clinical oversight before any use.
-->

> **In simple terms:** AI tools that understand medical language and healthcare workflows — like having a medical librarian and administrator who never sleeps.

---

## Core Repositories

---

**[Awesome AI Agents for Healthcare](https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare)**
> _The definitive curated list of agentic AI in clinical settings — updated weekly_

The healthcare equivalent of AI4Finance Foundation — continuously updated catalog covering clinical decision support agents, EHR-interacting systems, multi-agent diagnostic frameworks, surgical AI, mental health agents, and practical tooling (MCP servers, FHIR tools, prior auth agents, clinical trial automation). Start here when scoping any healthcare AI project.

---

**[Awesome AI Agents in Medicine (AIM-Research-Lab)](https://github.com/AIM-Research-Lab/Awesome-AI-Agents-Medicine)**
> _Systematic taxonomy and survey of medical LLM agent systems_

Backed by a formal peer-reviewed survey (TechRxiv, 2025), provides a structured **taxonomy of medical agent architectures**: single-agent, multi-agent, tool-augmented, RAG-augmented, multimodal. More academically rigorous — valuable for justifying architectural choices to clinical or regulatory stakeholders.

---

**[MedLLMsPracticalGuide](https://github.com/AI-in-Health/MedLLMsPracticalGuide)**
> _Nature Reviews Bioengineering — complete guide to medical LLM applications_

Accompanies a comprehensive review published in Nature Reviews Bioengineering. Covers model architectures (BioBERT, ClinicalBERT, BioGPT, MedPaLM), training approaches, evaluation benchmarks, and deployment considerations. Essential for **selecting a foundation model** for healthcare.

---

**[Awesome Healthcare Foundation Models](https://github.com/Jianing-Qiu/Awesome-Healthcare-Foundation-Models)**
> _Curated large AI models across every clinical modality_

Organized by modality: language models for clinical text, vision models for medical imaging, audio models for clinical conversations, multimodal models combining them. When your agent needs to process something other than text — an X-ray, ECG signal, pathology slide — this is where to find the relevant pre-trained model.

---

**[OpenMEDLab](https://github.com/openmedlab)**
> _Open platform for medical foundation models_

Multi-modal model hub covering imaging, NLP, bioinformatics, with evaluation benchmarks alongside models. For organizations working with Chinese-language patient populations, OpenMEDLab's multilingual support is particularly strong.

---

**[HealthFlow](https://github.com/yhzhu99/HealthFlow)**
> _Self-evolving AI agent with meta-planning for healthcare research_

An agent that learns from its own task history and evolves planning strategies over time. Particularly relevant for **healthcare research automation** — literature review, hypothesis generation, data analysis orchestration. Important: self-modification requires audit trails in clinical settings.

---

**[AgentClinic](https://agentclinic.github.io)**
> _Multimodal benchmark for AI agents in simulated clinical environments_

The most rigorous **evaluation framework** for clinical AI agents in open source. Grounded in USMLE Step 2/3 cases and NEJM case challenges. Also measures how cognitive biases affect diagnostic accuracy — directly relevant to FDA AI/ML bias evaluation guidance.

---

**[Awesome Specialized Medical LLMs](https://github.com/FreedomIntelligence/Awesome-Specialized-Medical-LLMs)**
> _Disease-specific LLMs organized by ICD-10 chapters_

When your agent needs expertise in a specific clinical area, this is your first stop. Organized by ICD-10 categories, maps specialty-specific models (Zodiac for cardiology, EpilepsyLLM for neurology) so you can find and evaluate them efficiently.

---

**[Medical Model Library](https://github.com/ExpertOpsAI/MedicalModelLibrary)**
> _Pre-trained healthcare AI models inventory_

Practical inventory of ready-to-use models across clinical NLP (BioBERT, ClinicalBERT, SciBERT, BioGPT) and medical imaging (U-Net, nnU-Net). A **model shopping list** organized by task.

---

**[LLM Agents in Scientific Discovery](https://github.com/zjlrock777/Awesome-LLM-Agents-Scientific-Discovery)**
> _AI agents for biomedical research, drug discovery, and genomics_

Bridges clinical AI and research AI. Covers agents for literature synthesis, hypothesis generation, experimental design, multi-omics analysis, and drug repurposing. Particularly relevant for **pharmaceutical and biotech teams**.

---

**[Agentic Clinical Dialogue](https://github.com/xqz614/Awesome-Agentic-Clinical-Dialogue)**
> _Medical agents for clinical conversation and patient interaction_

Focused on the conversational interface layer: how agents structure doctor-patient dialogue, gather symptoms, handle clinical uncertainty. Covers clinician-facing tools (SOAP note completion) and patient-facing tools (symptom checkers, medication adherence). Includes safety evaluation frameworks for clinical dialogue agents.

---

**[AI Agents for Medical Diagnostics](https://github.com/ahmadvh/AI-Agents-for-Medical-Diagnostics)**
> _Multi-specialist LLM agent system for complex case analysis_

Multi-specialist clinical agents running in parallel (cardiologist, pulmonologist, general medicine), each analyzing independently, then synthesizing findings. Mirrors how clinical consultation works at major medical centers. Valuable reference architecture for **clinical decision support tools**.

---

## MCP Servers — Healthcare

<!-- 
💡 PLAIN ENGLISH: These connections let AI agents read and write to 
electronic health record (EHR) systems like Epic or Cerner. They use 
FHIR — a standard way for health systems to share data — so the AI 
can actually look up real patient information (with proper authorization).

⚠️ CRITICAL: Healthcare data is protected by law. Any connection to 
patient data requires proper security, access controls, and compliance review.
-->

> **In simple terms:** Cables that connect AI to hospital record systems — allowing the AI to look up real patient data (when authorized) instead of making things up.

---

**[FHIR MCP Server (WSO2)](https://github.com/wso2/fhir-mcp-server)**
> _Production-grade MCP bridge between AI agents and any FHIR server_

Most enterprise-ready FHIR MCP server available. Supports OAuth 2.0 for Epic, Cerner, and other major EHR vendors. Full CRUD across all major FHIR resource types. Compatible with Claude Desktop, VS Code MCP, and any MCP client. For teams integrating with **Epic or Cerner EHR systems**, this handles OAuth complexity that trips most teams up.

---

**[FHIR MCP Server (The Momentum)](https://github.com/the-momentum/fhir-mcp-server)**
> _Developer-first FHIR MCP with automatic LOINC validation and semantic search_

Key differentiator: **automatic LOINC code validation** — prevents AI from hallucinating lab codes, a genuine patient safety concern. RAG-ready with vector embeddings. Works with Medplum, HAPI FHIR, Azure Health Data Services, and Epic.

---

**[AWS HealthLake MCP Server](https://awslabs.github.io/mcp/servers/healthlake-mcp-server)**
> _AI access to AWS HealthLake FHIR — with read-only safety mode_

Official AWS Labs server. 11 FHIR tools, advanced search, and critical **read-only mode** for compliance — lock agents to read-only until explicit human approval for write operations. 235 tests, 96% coverage. Best for organizations already on AWS.

---

**[Google Cloud Healthcare API MCP](https://github.com/Kartha-AI/google-cloud-healthcare-api-mcp)**
> _FHIR via GCP with PubMed, ClinicalTrials.gov, and FDA integration_

Connects to GCP Healthcare API with Firebase auth, plus PubMed, ClinicalTrials.gov, and FDA drug information. The **complete clinical intelligence stack** that decision support agents need. Best for GCP-first organizations.

---

**[Medplum MCP](https://github.com/rkirkendall/medplum-mcp)**
> _33 FHIR utility tools via Medplum's open-source EHR_

Ideal for teams **building EHR-adjacent applications** (clinical trial management, specialty clinic workflows, digital health apps). Medplum's sandbox is freely accessible — excellent for development and testing.

---

**[Enhanced FHIR MCP with Data Quality Assessment](https://github.com/jcafazzo/fhir-mcp)**
> _FHIR tools with built-in data quality validation_

Adds **data quality assessment** before agent action — validates completeness, consistency, and conformance. Essential for organizations migrating between EHR systems or working with multiple institutional data sources.

---

## Deployment Checklist

Before deploying a healthcare agent to production:

- [ ] PHI de-identification strategy documented
- [ ] HIPAA minimum necessary standard review completed
- [ ] Human-in-the-loop mechanism defined for clinical recommendations
- [ ] FHIR OAuth2 scope limited to minimum required resources
- [ ] Model evaluated on AgentClinic or equivalent clinical benchmark
- [ ] FDA SaMD classification determined
- [ ] Audit trail enabled for all agent decisions
- [ ] BAA signed with all cloud vendors

---

[← Finance](02-finance.md) | [Next: Supply Chain →](04-supply-chain.md)
