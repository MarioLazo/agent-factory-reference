# Ontologies & Knowledge Graphs

[← Back to Index](../README.md) | [← Supply Chain](04-supply-chain.md) | [Next: Datasets →](06-datasets.md)

---

<!-- 
💡 PLAIN ENGLISH: An "ontology" is basically a shared vocabulary with 
clear definitions. It tells the AI "when we say 'bond' in finance, we 
mean THIS specific thing." Without this, AI might confuse a bail bond 
with a savings bond with James Bond.

A "knowledge graph" is like a giant connected map of facts — "Company A 
bought Company B, which makes Product C, which competes with Product D."
-->

> **In simple terms:** These are the dictionaries and relationship maps that help AI understand domain-specific language — so it knows what words actually mean in your industry.

Ontologies are the **semantic foundation** of domain-aware agents. Without them, agents hallucinate terminology, misclassify entities, and make unreliable connections. This is the layer most teams skip — and then wonder why their agents make embarrassing domain errors.

---

## Finance Ontologies

**[FIBO — Financial Industry Business Ontology](https://github.com/edmcouncil/fibo)**
> _Standard ontology for financial contracts, instruments, and entities_

Developed post-2008 crisis when it became clear firms were using the same terms with incompatible meanings. Standardized by OMG; covers business entities, contracts, securities, derivatives, market data, regulatory reporting. Published in OWL/RDF for direct use in knowledge graphs. Mandatory for agents supporting **regulatory reporting** (Basel III, MiFID II, Dodd-Frank).

- Published: [spec.edmcouncil.org/fibo](https://spec.edmcouncil.org/fibo/)
- Hugging Face: [FIBO 2023 Q3](https://huggingface.co/datasets/wikipunk/fibo2023Q3)

**[ACTUS](https://www.actusfrf.org/)**
> _Machine-readable financial contract standards_

Defines algorithmic representations of financial contracts so cash flows and risk exposures can be computed deterministically. Essential for **risk calculation agents** simulating portfolio behavior under different market scenarios.

**Additional Finance Standards**: XBRL Taxonomy (FASB/IFRS), LEI (Legal Entity Identifier), CFI Codes (ISO 10962)

---

## Healthcare Ontologies & Terminology

**[UMLS — Unified Medical Language System](https://www.nlm.nih.gov/research/umls/)**
The backbone of clinical NLP. Maps concepts across 200+ medical vocabularies — 3M+ unique concepts, 15M+ concept names. Free with registration.
- GitHub tool: [UMLS to Graph](https://github.com/blpercha/umls-to-graph) — converts UMLS to Neo4j

**[SNOMED CT](https://www.snomed.org/)**
350,000+ clinical concepts in a rich hierarchical ontology. Designed for clinical documentation and decision support. Any agent reasoning about clinical concepts needs SNOMED CT grounding.
- SNOMED KG embeddings: [github.com/dchang56/snomed_kge](https://github.com/dchang56/snomed_kge)

**[ICD-10/ICD-11 (WHO)](https://www.who.int/standards/classifications/classification-of-diseases)**
Every hospital claim and public health report uses ICD codes. Essential for revenue cycle, claims processing, prior authorization, and population health agents.

**[RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/)**
Standard drug naming system. Prevents dangerous errors like treating "metoprolol succinate" and "metoprolol tartrate" as identical drugs (they have different clinical profiles).

**[LOINC](https://loinc.org/)**
Universal codes for lab tests and clinical measurements. Essential for any agent processing lab results or clinical observations.

**[BioPortal](https://bioportal.bioontology.org/)**
Repository of 1,000+ biomedical ontologies — Gene Ontology, ChEBI, HPO, NCI Thesaurus, MeSH. Essential for research-oriented AI in genomics, drug discovery, or precision medicine.

**[Awesome Healthcare Knowledge Bases](https://github.com/lujiaying/Awesome-HealthCare-KnowledgeBase)**
Comprehensive catalog including Hetionet, DrugBank, SPOKE, and Monarch Initiative. Start here for drug repurposing reasoning or gene-disease association lookups.

---

## Supply Chain Ontologies

- **GS1 Standards** (gs1.org) — Global supply chain language: barcodes, RFID, EDI, product data. If your agents identify products, locations, or shipments across trading partners, GS1 is the standard.
- **SCOR Model** — APICS/ASCM framework for supply chain process standardization; defines Plan, Source, Make, Deliver, Return, Enable processes and their KPIs.
- **UN/CEFACT** — UN trade and logistics standards; EDI message formats for cross-border trade.
- **Open Supply Hub** (opensupplyhub.org) — Open database of supply chain facility data with standardized identifiers.

---

[← Supply Chain](04-supply-chain.md) | [Next: Datasets →](06-datasets.md)
