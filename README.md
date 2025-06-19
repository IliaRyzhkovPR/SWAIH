# VECTORS Workshop Structure (80 mins)

## **Opening: The Tale of Two Cities (10 mins)**

**Context Setting (5 mins) - Neil**
- NHS data challenges: Trust mergers, system integration needs
- "Like the first kingdom building on sand - impressive towers that keep collapsing"

**Framework Introduction (5 mins) - Ilya** 
- The Seven Hills of VECTORS City story introduction
- "Today we'll journey through each foundation that makes digital infrastructure actually work"

**VECTORS stands for seven foundational principles:**
- **V**ersion Control
- **E**verything as Code  
- **C**I/CD Pipelines
- **T**esting
- **O**pen Source First
- **R**eference Architecture
- **S**ecurity by Design"
- 
---

## **The Seven Foundations Journey (45 mins)**

### **Hill 1: Version Control (6 mins) - Neil**
*"At the Chronicle Tower, where every change is recorded"*
- Change tracking, collaboration, audit trails
- **NHS Reality Check**: "When your EPR update breaks reporting at 3am, you need to know exactly what changed"
- **Transition**: "From the Chronicle Tower, we descend to the Scriptorium..."

### **Hill 2: Everything as Code (6 mins) - Ilya**
*"In the Scriptorium, where all infrastructure lives as code"*
- Reproducible infrastructure, disaster recovery
- **NHS Reality Check**: "Build test environment identical to production in minutes, not months"
- **Transition**: "Code flows from the Scriptorium through the Water-Pipe Station..."

### **Hill 3: CI/CD Pipelines (6 mins) - Ilya**
*"The Water-Pipe Station's automated flows"*
- Automated deployment, reduced manual errors
- **NHS Reality Check**: "Deploy safely during lunch break, not weekend maintenance windows"
- **Transition**: "But before anything flows to citizens, it must pass through the Proofing Grounds..."

### **Hill 4: Testing (6 mins) - Neil**
*"The Proofing Grounds where everything is validated"*
- Data quality assurance, regression protection
- **NHS Reality Check**: "Catch data pipeline errors before clinical dashboards go blank"
- **Transition**: "With proven foundations, we can safely trade in the Open Market..."

### **Hill 5: Open Source First (6 mins) - Ilya**
*"The bustling Open Market of battle-tested tools"*
- Cost efficiency, flexibility, no vendor lock-in
- **NHS Reality Check**: "When vendors demand £50k for simple integrations, you have alternatives"
- **Transition**: "All these diverse tools speak the same language, defined in the Blueprint Library..."

### **Hill 6: Reference Architecture (8 mins) - Neil**
*"The Blueprint Library's Common Data Model"*
- Single source of truth, system integration
- **NHS Reality Check**: "One patient, one record - whether EPR calls them 'John Smith' or lab calls them 'Smith, J.'"
- **Transition**: "This unified data is protected by the Shield Wall..."

### **Hill 7: Security by Design (7 mins) - Ilya**
*"The Shield Wall's intelligent protection"*
- PII protection, compliance, accessibility
- **NHS Reality Check**: "Protect patient data while enabling, not hindering, clinical workflow"

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



