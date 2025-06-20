# VECTORS Workshop Structure (80 mins)

## **Opening: You Can't Build a House on Quicksand (10 mins)**

**Context Setting (5 mins) - Neil**
- NHS data challenges: Trust mergers, system integration needs
- "You can't build a cathedral on quicksand - or lasting digital infrastructure on shaky foundations"

**Framework Introduction (5 mins) - Ilya** 
- The Seven Pillars that support any digital house
- "Today we'll examine each foundation pillar that separates thriving organisations from struggling ones"

**VECTORS stands for seven foundational pillars:**
- **V**ersion Control
- **E**verything as Code  
- **C**I/CD Pipelines
- **T**esting
- **O**pen Source First
- **R**eference Architecture
- **S**ecurity by Design

---

## **Building the Digital House (45 mins)**

### **Pillar 1: The House Plans (Version Control) (6 mins) - Neil**
*"Every change to the blueprints tracked and approved"*

**Solid Foundation:**
Imagine building a house where every single change to the blueprints is recorded in a master logbook. When the architect decides to move a door, it's documented: who made the change, when, why, and exactly what was modified. If the builder discovers the new door placement won't work, they can instantly see the original design and revert back. Multiple architects can work on different sections simultaneously without overwriting each other's work. The foreman can see exactly what's changed between yesterday's plans and today's before starting work.

**Shaky Foundations:**
*"The electrician wired the kitchen based on last week's plans, but someone moved the sink location and forgot to tell anyone. Now there are power outlets under where the tap will be, and nobody remembers who decided to move the sink or why."*

**Technical Explainer:** Version control via Git tracks every change to code, configurations, and documentation. Collaborative working through remote Git repositories enables teams to work together safely - branching for features, merging with approval, and rolling back when needed.

**Transition**: "With approved plans in hand, we move to creating the digital design..."

### **Pillar 2: The Digital Design (Everything as Code) (6 mins) - Ilya**
*"House plans, permits, certifications - all stored electronically"*

**Solid Foundation:**
Rather than keeping blueprints as paper drawings that can be lost, damaged, or misinterpreted, everything is stored as precise digital specifications. The foundation depth, concrete mix ratios, pipe specifications, electrical standards - all defined in digital format that machines can read and execute exactly. If a storm destroys the building site, you can recreate the exact same house anywhere by running the digital specifications through construction equipment. No human interpretation errors, no "I think it was supposed to be like this."

**Shaky Foundations:**
*"The original architect left the company, taking his knowledge with him. The hand-drawn plans are water-damaged and illegible in crucial sections. The builders are guessing how deep the foundations should be based on 'what looks right.'"*

**Technical Explainer:** Infrastructure as Code using Terraform for cloud resources, SQL databases with SSDT (SQL Server Data Tools) for version-controlled database schemas, and dbt or SQLMesh for data transformations. Everything is defined in readable code files that can be reviewed, tested, and versioned. Avoid black-box tools like SSIS packages where you can't see what's happening inside - if you can't read it, you can't maintain it reliably.

**Transition**: "Digital designs flow through our automated plumbing system..."

### **Pillar 3: The Plumbing System (CI/CD Pipelines) (6 mins) - Ilya**
*"Automated pipes that deliver clean water and remove waste"*

**Solid Foundation:**
Your house has intelligent plumbing that automatically tests water quality before it reaches any taps. If contaminated water enters the system, automatic valves shut off flow until the problem is fixed. Clean water flows smoothly from the source through filtering, quality testing, and final delivery to every room. The system monitors itself - if pressure drops or impurities are detected anywhere, warning lights show exactly where the problem is. No contaminated water ever reaches the residents.

**Shaky Foundations:**
*"Water is carried manually in buckets from the well to each room. Sometimes the water is clean, sometimes it's contaminated, but you only find out after someone gets sick. Moving water is exhausting work that takes all day, leaving no time for anything else."*

**Technical Explainer:** Continuous Integration/Continuous Deployment pipelines using tools like Azure Pipelines, GitLab CI, or GitHub Actions. When code is committed, automated systems build it, test it, scan for security issues, and deploy it through staging to production. No manual steps, no forgotten configurations, no human errors in deployment.

**Transition**: "But before anything flows to residents, it must pass electrical inspection..."

### **Pillar 4: The Electrical Inspection (Testing) (6 mins) - Neil**
*"Every wire tested before the power goes live"*

**Solid Foundation:**
Before any electricity flows through the house, every single wire, connection, and component is rigorously tested. Automated testing equipment checks voltage levels, identifies shorts, verifies safety switches work, and simulates various load conditions. The testing is so thorough that when you flip a light switch for the first time, you're absolutely confident it will work safely. If any component fails testing, the system identifies exactly which wire or connection needs fixing before power can be enabled.

**Shaky Foundations:**
*"Electricity is connected hopefully, with fingers crossed. Sometimes lights work, sometimes they don't. Occasionally outlets spark or circuit breakers trip randomly. The family has learned to check every switch carefully and keep torches handy for when things fail unexpectedly."*

**Technical Explainer:** Automated testing at multiple levels - unit tests for individual functions, regression tests to compare outputs, and data quality testing that validates schemas, checks for missing values, and ensures consistency. All tests run automatically before any deployment reaches production.

**Transition**: "With safety certified, we can source materials from reliable building supplies..."

### **Pillar 5: The Building Supplies (Open Source First) (6 mins) - Ilya**
*"Standard bricks, standard fittings - never locked to one supplier"*

**Solid Foundation:**
Your house is built using standard materials available from multiple suppliers. The bricks are standard size, so any brick manufacturer can provide replacements. The plumbing uses standard fittings, so any plumber can work on them with normal tools. If your usual supplier goes out of business or raises prices unreasonably, you can switch to another supplier immediately without rebuilding anything. The materials are proven designs used in thousands of other houses, with extensive community knowledge about best practices.

**Shaky Foundations:**
*"Your house is built with proprietary materials available from only one supplier. When the sink breaks, only that company can fix it - and they charge £500 for a repair that would cost £50 with standard parts. When they decide to discontinue your window type, you can't get replacements. You're trapped."*

**Technical Explainer:** Prioritising open source solutions whenever possible to avoid vendor lock-in and costly licence spikes. Not possible everywhere for various reasons, but an ingestion algorithm can be built in Python rather than expensive proprietary platforms. Open source provides access to source code, community support, and freedom to modify. Multiple vendors can support the same open source technology, preventing lock-in.

**Transition**: "All these different supplies connect through our consumer unit..."

### **Pillar 6: The Consumer Unit (Reference Architecture) (8 mins) - Neil**
*"Despite different voltage inputs - mains, solar, generator - all devices get standard 240V power"*

**Solid Foundation:**
Your house has a sophisticated consumer unit that takes electricity from multiple sources - mains power, solar panels, backup generator, even car batteries - and delivers consistent, reliable 240V to every device. Whether your power comes from the grid at 415V, solar panels at 12V, or emergency generator at varying voltages, every appliance in your house receives exactly what it needs. Plugs are standardised, voltage is regulated, and devices work identically regardless of the power source. The TV doesn't care whether it's running on solar or mains power.

**Shaky Foundations:**
*"Each room has different voltage depending on its power source. The kitchen runs on mains power at 240V, but the garage runs on solar at 12V, so different appliances work in different rooms. The backup generator puts out 230V, so some devices fail when switching to emergency power. Nothing is standardised - it's a constant guessing game."*

**Technical Explainer:** FHIR has been in place for communication for some time. OMOP is good but not for generic purposes. Build something based on open standards like the NHS data dictionary. If you have multiple Patient Administration Systems (PAS), they all feed one Common Data Model so all descriptions appear the same downstream. Whether data comes from different PAS systems with varying patient formats, they all map to consistent canonical records with standardised identifiers and terminology.

**Transition**: "This standardised power flows safely through our security system..."

### **Pillar 7: The Security System (Security by Design) (7 mins) - Ilya**
*"Smart locks that recognise residents but stop burglars"*

**Solid Foundation:**
Your house has intelligent security built into its very structure. The locks recognise family members automatically and grant appropriate access - parents can enter any room, children can't access the workshop, guests are limited to common areas. The system knows who should be where and when. Sensitive rooms like the home office containing financial documents have additional protection, but family members with legitimate access aren't inconvenienced. Security is invisible to authorised users but impenetrable to those who shouldn't be there.

**Shaky Foundations:**
*"Security is an afterthought - a simple deadbolt on the front door and bars on the windows. Everyone either has access to everything or access to nothing. The filing cabinet with important documents sits in the living room because there's nowhere secure to put it. When guests visit, you hide valuables and hope for the best."*

**Technical Explainer:** For data engineering, security means PII data is within different schemas with access only by those who need it. Sensitive patient information is segregated from general reporting data, with granular permissions controlling who can access what level of detail.

---

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



















