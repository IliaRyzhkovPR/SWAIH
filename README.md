## Workshop Structure (80 mins)

**Opening (10 mins)**
- Context setting: NHS data challenges, Trust mergers, system integration needs `Neil`
- Framework overview: Why these 7 pillars matter for healthcare data `Ilya`

**Core Framework (45 mins, ~5 mins per pillar)**
1. **IaC/Everything in Code** - Reproducible infrastructure, disaster recovery `Ilya`
2. **Version Control** - Change tracking, collaboration, audit trails `Neil`
3. **CI/CD** - Automated deployment, reduced manual errors `Ilya`
4. **Data Model/CDM** - Single source of truth, system integration `Neil`
5. **Open-source First** - Cost efficiency, flexibility, no vendor lock-in `Ilya`
6. **Security & Schema Isolation** - PII protection, compliance, accessibility `Ilya`
7. **Testing** - Data quality assurance, regression protection `Neil`

**Live Demo (10 mins)** `Ilya`
- Azure VM setup with Airflow
- SQLMesh integration for data modelling
- Simple pipeline demonstration

**SFT Case Study (15 mins)** `Neil`
- Trust merger challenges (multiple patient admin systems)
- Siloed data sources; duplicated code and different logic for similar workflows. Inconsistent metrics.
- New EHR integration strategy
- Data migration backend feeding

## Technical Prep 
- Pre-configured Azure VM template
- Airflow + SQLMesh installation scripts
- Sample NHS-like dataset (anonymised)
- Demo pipeline code

**Key Message**: Framework enables NHS Trusts to build resilient and future-proof data platforms that can adapt to organisational changes and new system procurements.
