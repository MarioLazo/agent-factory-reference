# Regulatory Reference Guide

[← Back to Index](../README.md) | [← Papers & Learning](07-papers-learning.md) | [Next: Community →](09-community.md)

---

<!-- 
💡 PLAIN ENGLISH: These are the laws and rules you MUST follow when 
building AI for healthcare, finance, or supply chain. Breaking them 
can result in massive fines, lawsuits, or even criminal charges. 

This section isn't optional reading — it's the "don't go to jail" section.
-->

> **In simple terms:** The legal rules for AI in regulated industries. Read this before you build anything, or find someone who has.

> This section maps the specific regulations your Agent Factory must navigate in healthcare, finance, and supply chain. Each entry covers what it is, who it applies to, key requirements for AI systems, and concrete actions for your agent builds. The AI regulatory landscape is moving fast — check effective dates carefully.

---

## Healthcare Regulations

---

### HIPAA Security Rule (2025 Updates)
**Authority:** U.S. Department of Health & Human Services (HHS)
**Status:** Proposed rule published Jan 6, 2025; compliance timeline TBD
**Applies to:** Covered entities (hospitals, clinics, health plans) and Business Associates (AI vendors, third parties processing ePHI)

**What Changed**: The 2025 update **eliminates the distinction between "required" and "addressable" safeguards — all controls are now mandatory.**

| Requirement | Specific Mandate |
|---|---|
| **PHI Minimization** | AI tools access only minimum necessary PHI; document exactly which fields each model uses |
| **MFA** | Multi-factor authentication required at all ePHI access points, including AI APIs |
| **Encryption** | PHI must be unusable/unreadable in transit and at rest |
| **Vulnerability Scanning** | Every 6 months minimum; annual penetration testing |
| **Disaster Recovery** | Critical system restoration within 72 hours of incident |
| **Business Associate Agreements (BAAs)** | Ongoing vendor verification, not just onboarding; governs all AI vendors touching ePHI |
| **De-identification** | Safe Harbor or Expert Determination required when using PHI for AI/ML training |
| **Audit Logging** | Activity logs for all AI model access to ePHI; must be reviewable |

**Agent Factory Actions**:
- Embed PHI minimization checks into prompt engineering and data pipelines
- Require BAAs from all AI platform vendors (Azure, OpenAI, Anthropic, etc.)
- Use synthetic data generation for model training to avoid PHI exposure
- Log all agent access to health records with user/role attribution

---

### FDA AI/ML Medical Device Guidance — Total Product Life Cycle (TPLC)
**Authority:** U.S. Food and Drug Administration
**Status:** Draft guidance issued Jan 7, 2025; phased review ongoing
**Applies to:** AI-enabled Software as a Medical Device (SaMD), diagnostic AI, clinical NLP tools, predictive analytics for patient care

**Core Framework**: FDA requires AI governance across the **entire device lifespan** — design, training, deployment, and postmarket monitoring — not just at the point of approval.

| Phase | Requirement |
|---|---|
| **Pre-market Submission** | Data lineage, train/test splits, performance validation tied to clinical claims, demographic bias analysis |
| **Change Control** | Predetermined Change Control Plan (PCCP) for adaptive/continuously learning models |
| **Human Oversight** | Document level of clinician oversight required for each AI-assisted decision |
| **Post-market Monitoring** | Ongoing real-world performance tracking; incident reporting plan |
| **Bias Analysis** | Subgroup performance reporting across race, age, gender for clinical AI |

**Agent Factory Actions**:
- Build PCCP templates into your agent governance checklists for adaptive models
- Document AI decision boundaries for any clinical workflow agent
- Apply TPLC lifecycle tagging in your AI inventory (pre-market → deployed → monitored)

---

### U.S. State-Level AI Laws (Healthcare)
**Status:** 46 states introduced 250+ bills in 2025; 17 states enacted 27 laws
**Key States:** California (AB 3030, SB 1120), Pennsylvania, Colorado, Arizona, Texas

| Category | Requirement |
|---|---|
| **Transparency** | Disclose when AI is interacting with or making decisions about patients (90+ bills include this) |
| **Anti-discrimination** | Validate AI does not produce biased outcomes by demographic group |
| **Use-case Restrictions** | Prohibit AI-only coverage denials (5 states); require human verification |
| **Clinical Context Oversight** | AI recommendations must be reviewed by licensed clinicians before execution |

**Agent Factory Actions**:
- Build disclosure headers into all patient-facing agent responses
- Implement bias monitoring for any AI touching insurance, clinical, or administrative workflows
- Enforce human-in-the-loop gates for high-stakes decisions (coverage, diagnosis, triage)

---

## Finance Regulations

---

### EU AI Act — Financial Services
**Authority:** European Union
**Status:** In force Aug 2024; high-risk obligations effective **Aug 2, 2026**
**Applies to:** Any AI system used for credit scoring, underwriting, pricing, fraud detection, or automated financial decisions — including non-EU companies if EU consumers are impacted

| AI Use Case | Risk Tier | Oversight Level |
|---|---|---|
| Credit adjudication / underwriting | **High Risk** | Full compliance required |
| Pricing algorithms | **High Risk** | Full compliance required |
| Fraud detection (automated denial) | **High Risk** | Full compliance required |
| Customer chatbots | **Limited Risk** | Transparency notice required |
| Marketing/segmentation tools | **Minimal Risk** | Baseline controls |

| Requirement | What It Means |
|---|---|
| **Risk Management System** | Continuous identification, evaluation, mitigation across the model lifecycle |
| **Training Data Governance** | Demographic fairness audits; document data lineage and representativeness |
| **Explainability** | SHAP/LIME documentation required; decisions interpretable to regulators and consumers |
| **Human Oversight** | Mandatory human-in-the-loop for credit, pricing, and denial decisions |
| **Technical Documentation** | Lifecycle records from design through decommission |
| **Accuracy & Robustness** | Validated performance metrics; resilience against adversarial inputs |
| **Conformity Assessment** | Self-assessment for most financial AI; third-party audit for highest-risk categories |

**Agent Factory Actions**:
- Risk-tier all finance agents before POC approval (use EU Act categories as your template)
- Attach SHAP/LIME explainability outputs to every credit/fraud agent decision log
- Implement human review gates for any agent making binding financial decisions

---

### OSFI Guideline E-23 — Model Risk Management (Canada)
**Authority:** Office of the Superintendent of Financial Institutions (Canada)
**Status:** Final guideline released Sept 2025; **effective May 1, 2027**
**Applies to:** All federally regulated financial institutions (FRFIs) in Canada, including scaled fintechs

| Pillar | Key Obligations |
|---|---|
| **Model Inventory** | Evergreen registry with risk ratings, lifecycle status, decommission records; covers all AI/ML models |
| **Risk-Tiered Governance** | Oversight intensity proportional to model risk; allocate resources accordingly |
| **Independent Validation** | Required for high-risk models; multi-disciplinary teams (legal, ethics, data science) |

| Requirement | Detail |
|---|---|
| **Pre-deployment Assessment** | Cybersecurity risk, infrastructure vulnerability, explainability review before go-live |
| **Drift Monitoring** | Processes for detecting model drift, performance degradation, autonomous re-parametrization |
| **Autonomous Decision Risk** | Specific controls for AI making decisions without human review |
| **Documentation** | Full lifecycle model records; survivable through staff turnover |
| **Remediation Tracking** | Incident history and stabilization steps tracked in inventory |

**Agent Factory Actions**:
- Map E-23 inventory requirements into your AI inventory template (owners, risk tier, cadence, incidents)
- Build pre-deployment checklists aligned to E-23 pillars for all financial agents
- Assign independent validation workflows for high-risk financial agents before production

---

### NIST AI Risk Management Framework (AI RMF)
**Authority:** U.S. National Institute of Standards and Technology
**Status:** Voluntary; widely referenced baseline globally
**Applies to:** All sectors — particularly useful as a foundational governance scaffold for fintech and any enterprise AI program

| Function | Purpose |
|---|---|
| **Govern** | Establish policies, roles, accountability structures, and culture of AI risk awareness |
| **Map** | Identify AI risks in context — business, technical, and societal impacts |
| **Measure** | Quantify and test risks: bias, accuracy, drift, explainability |
| **Manage** | Prioritize and treat risks; document decisions and residual risk |

**Agent Factory Actions**:
- Use Govern → Map → Measure → Manage as the backbone of your CoE governance cycle
- Apply as the cross-cutting baseline across healthcare, finance, and supply chain programs

---

### U.S. Treasury AI Guidance
**Authority:** U.S. Department of the Treasury
**Status:** Released **Feb 18, 2026**
**Applies to:** Financial services organizations deploying AI in consumer-facing and operational contexts

Focuses on responsible AI deployment, consumer protection, and systemic risk awareness. Two new resources released to guide financial institutions on AI governance alignment. Signals that federal financial regulators are moving toward more prescriptive AI guidance — watch for follow-on publications.

---

## Supply Chain Regulations

---

### EU AI Act — Supply Chain Applications
**Authority:** European Union
**Status:** GPAI obligations active Aug 2025; high-risk obligations effective **Aug 2, 2026**
**Applies to:** Supply chain AI for procurement, logistics, quality control, supplier selection, demand forecasting — especially tools from third-party AI vendors

| AI Use Case | Risk Level | Requirement |
|---|---|---|
| Automated vendor disqualification | **High** | Human verification required before execution |
| AI-driven contract rejection | **High** | Bias validation, human review gate |
| Quality inspection AI (robotics) | **High** | Transparency + monitoring from vendor |
| Demand forecasting / planning | **Minimal–Limited** | Baseline logging, performance tracking |
| Carrier/route optimization | **Minimal** | Light governance, audit trail |

| Requirement | Detail |
|---|---|
| **Vendor Transparency** | AI suppliers must provide risk and performance documentation; include in supplier reviews |
| **Bias Monitoring** | Validate procurement AI doesn't systematically disadvantage supplier categories |
| **Human Oversight** | High-impact decisions (vendor termination, contract awards) require human review |
| **Incident Escalation** | Define how AI behavior issues are reported and remediated across vendor chain |
| **Documentation** | Evidence of testing, updates, and contractual security responsibilities |

**Agent Factory Actions**:
- Identify all AI-based vendor tools in your supply chain; tag risk tier per EU Act
- Include AI governance obligations in supplier contracts
- Build escalation workflows in your orchestration layer for high-risk automated supply decisions

---

### 2026 NDAA — AI Supply Chain & Security (U.S. Defense)
**Authority:** U.S. Congress (National Defense Authorization Act)
**Status:** Effective 2026; primarily targets defense/government supply chains
**Applies to:** Companies supplying AI to U.S. defense and intelligence agencies

- Strict supply chain restrictions prohibiting "covered" technologies from adversary nations
- Cybersecurity standards expanding on CMMC (Cybersecurity Maturity Model Certification)
- DOD directed to develop AI-specific security standards
- Non-compliance = exclusion from the Defense Industrial Base

**Agent Factory Actions**:
- If serving government clients, map AI components against prohibited vendor lists
- Build CMMC-aligned cybersecurity controls into agent deployment pipelines

---

### CCPA / CPRA — Supply Chain Data
**Authority:** California Privacy Protection Agency (CPPA)
**Status:** Audit and risk assessment obligations rolling out 2025–2028
**Applies to:** Organizations processing California consumer data through supply chain services, vendors, or contractors

| Requirement | Detail |
|---|---|
| **Data Inventory** | Comprehensive mapping of personal data collected, processed, shared across all vendors |
| **Vendor Contracts** | Written contracts with all sub-processors; must include audit rights and opt-out mechanisms |
| **AI Cybersecurity Audit** | Contractors must cooperate on cybersecurity audits (Article 9, effective Jan 1, 2026) |
| **Risk Assessments** | AI-related risk assessments required (Article 10); annual reports to CPPA beginning April 1, 2028 |
| **Opt-Out Rights** | Consumer right to opt out of automated decision-making that produces significant effects |

**Agent Factory Actions**:
- Build data flow maps for all supply chain agents handling California consumer data
- Include CCPA audit cooperation clauses in AI vendor agreements
- Implement opt-out mechanisms for consumer-facing supply chain automation

---

### CISA / NIST Cybersecurity Framework (CSF 2.0)
**Authority:** CISA and NIST
**Status:** CSF 2.0 released Feb 2024; continuously updated
**Applies to:** All critical infrastructure sectors including healthcare, finance, and supply chain

> Supply chain attacks doubled in 2025, averaging approximately 26 incidents per month — making this framework operationally critical, not just a compliance checkbox.

| Control | Purpose |
|---|---|
| **SBOM (Software Bill of Materials)** | Full inventory of software components in AI systems; validate no vulnerable or prohibited dependencies |
| **Third-Party Risk Scoring** | Continuous vendor risk monitoring; supply chain attacks doubled in 2025 |
| **Zero Trust Architecture** | Assume breach; verify every access request including agent-to-agent calls |
| **Incident Response Plan** | Defined playbooks for supply chain-specific attack vectors (ransomware, data exfiltration) |

**Agent Factory Actions**:
- Generate SBOMs for all agent frameworks and dependencies
- Implement zero trust principles in multi-agent orchestration (no implicit trust between agents)
- Run vendor risk scoring as an automated agent function for supply chain clients

---

## Cross-Sector Regulatory Quick Reference

| Regulation | Sector | Jurisdiction | Effective | Core AI Obligation |
|---|---|---|---|---|
| **HIPAA Security Rule 2025** | Healthcare | U.S. | 2025 (proposed) | MFA, encryption, PHI minimization, BAAs |
| **FDA TPLC AI Guidance** | Healthcare | U.S. | Jan 2025 (draft) | Data lineage, bias analysis, PCCP, post-market monitoring |
| **State AI Laws (CA, PA, TX…)** | Healthcare | U.S. States | 2025–2026 | Disclosure, anti-bias, human verification |
| **EU AI Act (High-Risk)** | Finance, Supply Chain | EU/Global | **Aug 2, 2026** | Risk tiers, explainability, human-in-loop, technical docs |
| **OSFI E-23** | Finance | Canada | **May 1, 2027** | Model inventory, drift monitoring, independent validation |
| **NIST AI RMF** | All sectors | U.S./Global | Voluntary | Govern, Map, Measure, Manage lifecycle |
| **U.S. Treasury AI Guidance** | Finance | U.S. | **Feb 18, 2026** | Responsible AI deployment, consumer protection |
| **2026 NDAA AI Supply Chain** | Supply Chain (Defense) | U.S. | 2026 | Vendor restrictions, CMMC-aligned cybersecurity |
| **CCPA / CPRA** | Supply Chain, Finance | California/U.S. | 2025–2028 | Data mapping, vendor contracts, risk assessments |
| **CISA / NIST CSF 2.0** | All sectors | U.S. | Active | SBOM, zero trust, third-party risk, incident response |

> **Compliance is not a one-time checklist.** Regulations listed here with "proposed" or "draft" status will finalize. Regulations with future effective dates are already shaping what enterprise buyers require of AI vendors today. Build your Agent Factory to these standards now — retrofitting compliance into production systems is significantly more expensive than designing for it from the start.

---

[← Papers & Learning](07-papers-learning.md) | [Next: Community →](09-community.md)
