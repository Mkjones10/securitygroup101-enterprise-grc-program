# SecurityGroup101 – Enterprise GRC, Risk & Resilience Program

SecurityGroup101 is a rapidly growing fintech company specializing in cloud-based financial platforms, digital payment processing, and financial data analytics. As the organization scaled, leadership identified fragmented risk processes, inconsistent controls, and increasing exposure to cyber threats and financial-sector regulatory requirements.

This repository simulates a full consulting engagement to design and implement a comprehensive Governance, Risk, and Compliance (GRC) program aligned to industry frameworks and fintech regulatory expectations — covering risk assessment, regulatory compliance, resilience planning, governance design, and third-party risk management.

**[Read the one-page Executive Summary →](./Executive_Summary.pdf)**

---

## Program Scope

- Quantitative Risk Assessment (NIST SP 800-30)
- Disaster Recovery and Business Continuity Planning (NIST SP 800-34)
- Regulatory and Compliance Alignment (GLBA, PCI DSS, FFIEC, SOX)
- Enterprise Governance Framework (NIST CSF, ISO 27001, COBIT 2019)
- Third-Party / Vendor Risk Management
- ISO/IEC 27001:2022 Statement of Applicability (93 controls)

This end-to-end GRC program reflects the type of work performed by a junior GRC analyst supporting fintech clients in a consulting environment.

---

## Document Index

Every workstream below has a detailed markdown source and a consolidated, client-ready PDF.

| Workstream | Markdown Source(s) | PDF Deliverable |
|---|---|---|
| Quantitative Risk Assessment | [risk-register.md](./risk-assessment/risk-register.md), [ale-calculations.md](./risk-assessment/ale-calculations.md), [risk-heatmap.md](./risk-assessment/risk-heatmap.md) | [Quantitative_Risk_Assessment.pdf](./pdf/Quantitative_Risk_Assessment.pdf) |
| Regulatory Compliance Gap Analysis | [glba-gap-analysis.md](./compliance/glba-gap-analysis.md), [pci-dss-crosswalk.md](./compliance/pci-dss-crosswalk.md), [ffiec-controls.md](./compliance/ffiec-controls.md) | [Regulatory_Compliance_Gap_Analysis.pdf](./pdf/Regulatory_Compliance_Gap_Analysis.pdf) |
| Disaster Recovery & Business Continuity | [disaster-recovery-plan.md](./drp/disaster-recovery-plan.md), [business-continuity-plan.md](./drp/business-continuity-plan.md), [dr-testing-schedule.md](./drp/dr-testing-schedule.md) | [DRP_BCP.pdf](./pdf/DRP_BCP.pdf) |
| Enterprise GRC Program | [governance-model.md](./grc-program/governance-model.md), [control-catalog.md](./grc-program/control-catalog.md), [grc-roadmap.md](./grc-program/grc-roadmap.md) | [Enterprise_GRC_Program_Charter.pdf](./pdf/Enterprise_GRC_Program_Charter.pdf) |
| Statement of Applicability | — (new) | [Statement_of_Applicability.pdf](./pdf/Statement_of_Applicability.pdf) |
| Third-Party / Vendor Risk | — (new) | [Third_Party_Vendor_Risk_Assessment.pdf](./pdf/Third_Party_Vendor_Risk_Assessment.pdf) |

All markdown source files remain in place under their original folders (`risk-assessment/`, `compliance/`, `drp/`, `grc-program/`); the PDFs in `/pdf` are polished, client-ready consolidations of that same underlying analysis, plus two new deliverables that close gaps the analysis itself identified.

---

## Repository Structure

```text
/SecurityGroup101-GRC-Program
│
├── README.md
├── Executive_Summary.pdf
│
├── risk-assessment/
│   ├── risk-register.md
│   ├── ale-calculations.md
│   └── risk-heatmap.md
│
├── compliance/
│   ├── glba-gap-analysis.md
│   ├── pci-dss-crosswalk.md
│   └── ffiec-controls.md
│
├── drp/
│   ├── disaster-recovery-plan.md
│   ├── business-continuity-plan.md
│   └── dr-testing-schedule.md
│
├── grc-program/
│   ├── governance-model.md
│   ├── control-catalog.md
│   └── grc-roadmap.md
│
├── vendor-risk/
│   └── third-party-vendor-risk-assessment.md
│
├── compliance/statement-of-applicability/
│   └── statement-of-applicability.md
│
└── pdf/
    ├── Quantitative_Risk_Assessment.pdf
    ├── Regulatory_Compliance_Gap_Analysis.pdf
    ├── DRP_BCP.pdf
    ├── Enterprise_GRC_Program_Charter.pdf
    ├── Statement_of_Applicability.pdf
    └── Third_Party_Vendor_Risk_Assessment.pdf
```

---

## Project Overview

This project consolidates four original workstreams, plus two additions that close gaps identified within the program itself, into a unified GRC program.

### 1. Quantitative Risk Assessment (NIST SP 800-30)

A full asset-based risk assessment using SLE, ARO, and ALE to quantify financial exposure across 10 critical fintech assets. Customer Data carries the highest annualized loss exposure at $500,000; Employee Workstations follow at $400,000 driven by high incident frequency. Results are used to prioritize risks, define recovery tiers, and guide control implementation.

### 2. Regulatory and Compliance Alignment (GLBA, PCI DSS, FFIEC, SOX)

Gap analyses and framework crosswalks mapping regulatory requirements to NIST CSF, ISO 27001, and COBIT 2019. All three regulatory lenses converge on the same underlying weaknesses: inconsistent MFA enforcement, no formal vendor risk program, and limited security monitoring coverage.

### 3. Disaster Recovery and Business Continuity (NIST SP 800-34)

A complete DRP and BCP designed around a combined ransomware and flooding scenario. Includes RTO/RPO definitions, tiered recovery sequencing, failover strategy, and a structured testing program (monthly backup restores through annual full failover tests).

### 4. Enterprise GRC Program Design (NIST CSF, ISO 27001, COBIT 2019)

A governance model, unified control catalog, and an 18-month GRC roadmap covering assessment, design, implementation, and continuous improvement. The program is currently positioned within Phase 1–2 of that roadmap.

### 5. Statement of Applicability (ISO/IEC 27001:2022 Annex A)

All 93 Annex A controls assessed for applicability, with implementation status, justification, evidence reference, and owner for each. Status is drawn directly from the gap analyses and control catalog above rather than presented as a fully mature program — of 93 controls, 24 are Implemented, 39 Partial, and the remainder Draft, Planned, In Progress, Gap, or Not Applicable.

### 6. Third-Party / Vendor Risk Assessment Program

Directly remediates the "no formal TPRM program" gap identified in the GLBA Gap Analysis. Includes a vendor intake questionnaire, a four-factor criticality tiering model, a security questionnaire review with a documented finding (condition/criteria/cause/effect/recommendation format), a risk register excerpt, and an executive decision memo.

---

## Key Deliverables

### Quantitative Risk Register
- ALE modeling for 10 critical assets
- Tiered risk prioritization and color-coded heatmap
- Threat modeling aligned to fintech operations

### GLBA, PCI DSS, FFIEC Gap Analyses
- Identification of control deficiencies across all three frameworks
- Framework crosswalks to NIST CSF, ISO 27001, and COBIT 2019
- Consolidated, prioritized remediation list

### Disaster Recovery & Business Continuity Plan
- Tier 1–3 recovery sequencing with defined RTO/RPO targets
- Cloud failover strategy and backup validation processes
- Five-part testing matrix from monthly to annual cadence

### Unified Control Catalog
Mapped across NIST CSF, ISO 27001, COBIT 2019, GLBA, PCI DSS, and FFIEC, with explicit Implemented/Partial/Draft/Gap status tracking.

### 18-Month GRC Roadmap
Assessment → Build → Implementation → Monitor and Improve, with governance structure, policy lifecycle, and KPI/KRI reporting.

### Statement of Applicability
93-control ISO/IEC 27001:2022 Annex A assessment with justification, status, evidence, and ownership for every control.

### Third-Party Vendor Risk Assessment
Vendor intake, criticality tiering, security questionnaire review with a real finding, risk register, and executive decision memo across three vendor profiles (cloud IaaS, payment gateway, HR/payroll).

---

## Frameworks and Regulations

- NIST SP 800-30 (Risk Assessment)
- NIST SP 800-34 (Contingency Planning)
- NIST Cybersecurity Framework (CSF)
- ISO/IEC 27001:2022 (including full Annex A Statement of Applicability)
- COBIT 2019
- GLBA Safeguards Rule
- PCI DSS v4.0
- FFIEC Cybersecurity Expectations
- SOX IT General Controls

---

## Skills Demonstrated

- Quantitative risk assessment and ALE modeling
- Control mapping and framework harmonization
- Policy development and governance design
- Regulatory compliance analysis across three regulatory regimes
- Disaster recovery and business continuity planning
- Third-party / vendor risk management, including criticality tiering and security questionnaire review
- ISO/IEC 27001:2022 Statement of Applicability development
- SIEM and logging expectations
- Access control and identity governance
- Executive-level documentation and decision memos
- Multi-phase GRC program implementation

---

## Why This Project Matters

This repository reflects real-world GRC consulting work and aligns directly with entry-level GRC analyst responsibilities, including:

- Assessing and improving security controls
- Developing policies, risk assessments, and a full Statement of Applicability
- Crosswalking multiple regulatory frameworks
- Building risk registers, vendor risk programs, and remediation plans
- Translating technical requirements into business-aligned recommendations for executive audiences

The program's honesty about its own maturity — clearly distinguishing Implemented from Partial, Draft, Planned, and Gap controls — is intentional. A GRC analyst's job is to surface where a program actually stands, not to present an idealized version of it.
