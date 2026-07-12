# SecurityGroup101 — Enterprise GRC, Risk & Resilience Program

**Maxine Jones, GRC Analyst · mkj00015@mix.wvu.edu · July 2026**

SecurityGroup101 is a fictional cloud-native fintech SaaS company founded in 2025, specializing in cloud-based financial platforms, digital payment processing, and financial data analytics. As the organization scaled, leadership identified fragmented risk processes, inconsistent controls, and increasing regulatory exposure across GLBA, PCI DSS, FFIEC, and SOX.

This repository documents a full end-to-end GRC consulting engagement — covering quantitative risk assessment, regulatory compliance gap analysis, disaster recovery and business continuity planning, enterprise governance design, ISO/IEC 27001:2022 Statement of Applicability, and a complete third-party vendor risk management program.

> **[View Document Control Register →](./vendor-risk/Document_Control_Register.md)**

---

## Program Scope

| Workstream | Frameworks Applied |
|---|---|
| Quantitative Risk Assessment | NIST SP 800-30 Rev. 1 |
| Disaster Recovery & Business Continuity | NIST SP 800-34 Rev. 1 |
| Regulatory Compliance Gap Analysis | GLBA Safeguards Rule · PCI DSS v4.0 · FFIEC · SOX IT GCs |
| Enterprise Governance & Control Catalog | NIST CSF 2.0 · ISO/IEC 27001:2022 · COBIT 2019 |
| Statement of Applicability | ISO/IEC 27001:2022 Annex A (93 controls) |
| Third-Party / Vendor Risk Management | NIST SP 800-161 Rev. 1 Upd. 1 · CSA CCM v4.0 · PCI DSS v4.0 Req 12.8 · GLBA §314.4(f) |

---

## Repository Structure

```
securitygroup101-enterprise-grc-program/
│
├── README.md
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
├── pdf-docs/
│   ├── SecurityGroup101_Quantitative_Risk_Assessment.pdf
│   ├── SecurityGroup101_Regulatory_Compliance_Gap_Analysis.pdf
│   ├── SecurityGroup101_DRP_BCP.pdf
│   ├── SecurityGroup101_Enterprise_GRC_Program_Charter.pdf
│   ├── SecurityGroup101_Statement_of_Applicability.pdf
│   └── SecurityGroup101_Third_Party_Vendor_Risk_Assessment.pdf
│
└── vendor-risk/                                ← NEW — complete VRM program
    ├── README.md
    ├── Document_Control_Register.md
    ├── securitygroup101-security-trust-center.md
    ├── SG101_Security_Trust_Center.pdf
    ├── SG101_CAIQ_v4_Completed.xlsx
    ├── SG101_CAIQ_v4_Completed.pdf
    ├── SG101_Vendor_Risk_Scoring_Rubric.xlsx
    ├── SG101_Vendor_Risk_Scoring_Rubric.pdf
    ├── VRM_01_Vendor_Intake_Form.xlsx + .pdf
    ├── VRM_02_Vendor_Inventory_Register.xlsx + .pdf
    ├── VRM_03_Vendor_Tiering_Matrix.xlsx + .pdf
    ├── VRM_04_Inherent_Risk_Questionnaire.xlsx + .pdf
    ├── VRM_05_Residual_Risk_Report_Stripe.xlsx + .pdf
    ├── VRM_06_Vendor_POAM.xlsx + .pdf
    └── VRM_07_Executive_Summary_Stripe.pdf
```

---

## Document Index

### Core GRC Program (`/pdf-docs`)

| # | Deliverable | Description |
|---|---|---|
| 1 | [Quantitative Risk Assessment](./pdf-docs/SecurityGroup101_Quantitative_Risk_Assessment.pdf) | ALE modeling across 10 critical fintech assets. Customer Data: $500K ALE. Employee Workstations: $400K ALE. Results drive recovery tier assignments and control prioritization. |
| 2 | [Regulatory Compliance Gap Analysis](./pdf-docs/SecurityGroup101_Regulatory_Compliance_Gap_Analysis.pdf) | Framework crosswalks for GLBA, PCI DSS v4.0, and FFIEC mapped to NIST CSF, ISO 27001, and COBIT 2019. Three regulatory lenses converge on the same root gaps: inconsistent MFA, no formal TPRM program, limited monitoring coverage. |
| 3 | [Disaster Recovery & BCP](./pdf-docs/SecurityGroup101_DRP_BCP.pdf) | Full DRP/BCP for combined ransomware and flooding scenario. Tier 1–3 recovery sequencing. RTO: 4hr (Tier 1), 8hr (Tier 2), 24hr (Tier 3). Five-part testing matrix from monthly backup restores to annual full failover. |
| 4 | [Enterprise GRC Program Charter](./pdf-docs/SecurityGroup101_Enterprise_GRC_Program_Charter.pdf) | Governance model, unified control catalog mapped across NIST CSF / ISO 27001 / COBIT 2019 / GLBA / PCI DSS / FFIEC, and 18-month GRC roadmap (Assessment → Build → Implement → Monitor). |
| 5 | [Statement of Applicability](./pdf-docs/SecurityGroup101_Statement_of_Applicability.pdf) | All 93 ISO/IEC 27001:2022 Annex A controls assessed with implementation status, justification, evidence reference, and owner. Honest maturity: 24 Implemented, 39 Partial, balance in Draft/Planned/Gap. |
| 6 | [Third-Party Vendor Risk Assessment](./pdf-docs/SecurityGroup101_Third_Party_Vendor_Risk_Assessment.pdf) | Original TPRM deliverable directly remediating the "no formal vendor risk program" gap from the GLBA analysis. Vendor intake, criticality tiering, security questionnaire review, risk register excerpt, and executive decision memo across three vendor profiles. |

### Vendor Risk Management Program (`/vendor-risk`)

The `/vendor-risk` folder contains a fully built, end-to-end VRM program — the most operationally detailed workstream in this repository. It goes beyond the original TPRM deliverable to document the complete lifecycle: from first contact with a new vendor through approved, monitored, and continuously tracked vendor relationships.

| # | Artifact | Description |
|---|---|---|
| — | [Security Trust Center](./vendor-risk/SG101_Security_Trust_Center.pdf) | Public-facing security posture documentation. Compliance status table (GLBA , PCI DSS , FFIEC , SOX , NIST CSF , ISO 27001 , SOC 2 ), encryption standards, MFA enforcement, incident response SLAs, and subprocessor disclosure. |
| — | [CAIQ v4 Self-Assessment](./vendor-risk/SG101_CAIQ_v4_Completed.pdf) | CSA STAR Level 1 — 85 questions across 16 CCM v4.0 domains completed as SecurityGroup101's security officer. Full implementation statements citing actual repo controls. Two honest "No" answers with documented remediation plans. |
| — | [Vendor Risk Scoring Rubric](./vendor-risk/SG101_Vendor_Risk_Scoring_Rubric.pdf) | 36-question weighted rubric for evaluating inbound vendor questionnaires. 7 Critical red flags — any "No" auto-escalates to HIGH risk. Automatic tier scoring (Low / Medium / High / Critical). |
| VRM-01 | [Vendor Intake Form](./vendor-risk/VRM_01_Vendor_Intake_Form.pdf) | New vendor request form — data/access classification (PHI, PCI, PII, production access, cloud, internet-facing, fourth parties), business justification, and GRC risk decision section. |
| VRM-02 | [Vendor Inventory Register](./vendor-risk/VRM_02_Vendor_Inventory_Register.pdf) | 11-vendor register across all four risk tiers with PHI/PCI/PII/production access flags, contract expiration, and next assessment dates. |
| VRM-03 | [Vendor Tiering Matrix](./vendor-risk/VRM_03_Vendor_Tiering_Matrix.pdf) | Four-tier framework (Critical / High / Moderate / Low) with data/access criteria, regulatory relevance, assessment requirements, review cadence, and contract requirements per tier. |
| VRM-04 | [Inherent Risk Questionnaire](./vendor-risk/VRM_04_Inherent_Risk_Questionnaire.pdf) | 16-question pre-assessment screen administered before the full CAIQ. Each question cites the specific NIST SP 800-161 section or PCI DSS requirement driving its inclusion. Scoring key routes vendors to correct assessment pathway. |
| VRM-05 | [Residual Risk Report — Stripe](./vendor-risk/VRM_05_Residual_Risk_Report_Stripe.pdf) | Formal residual risk report for Stripe, Inc. Inherent: HIGH (28/38). Control Effectiveness: STRONG (PCI DSS Level 1, unqualified SOC 2 Type II). Residual: MEDIUM-LOW per NIST SP 800-30 Rev. 1 Section 3.4. Decision: Approved with Conditions. |
| VRM-06 | [Vendor POA&M](./vendor-risk/VRM_06_Vendor_POAM.pdf) | 8 open findings across 6 vendors. 1 High (Snowflake DSP-01: PII data masking), 2 Medium, 3 Low, 2 Informational. Each finding includes CCM control ID, owner, due date, evidence required, and remediation notes. |
| VRM-07 | [Executive Summary — Stripe](./vendor-risk/VRM_07_Executive_Summary_Stripe.pdf) | 3-page executive summary for the Stripe assessment: vendor profile, assessment summary, risk determination, open findings, recommendation, and approval signature block. Decision: Approved with Conditions. |

---

## Program Maturity at a Glance

| Domain | Status | Key Metric |
|---|---|---|
| Quantitative Risk Assessment |  Complete | 10 assets modeled · $500K peak ALE |
| Regulatory Compliance (GLBA/PCI/FFIEC) |  Complete | 3 gap analyses · consolidated remediation list |
| Disaster Recovery & BCP |  Complete | Tier 1 RTO 4hr · 5-part test schedule |
| Enterprise GRC Program & Control Catalog |  Complete | Controls mapped across 6 frameworks |
| ISO 27001:2022 Statement of Applicability |  Complete | 93 controls · 24 Implemented · 39 Partial |
| Third-Party Vendor Risk Program |  Complete | 10 artifacts · 11 vendors inventoried · Stripe fully assessed |
| SOC 2 Type II |  Roadmap Phase 3 | Target: Q2 2027 |
| ISO 27001 Certification |  Roadmap Phase 3 | Target: Q4 2026 |

---

## Frameworks and Regulations Applied

| Framework / Regulation | Application in This Repository |
|---|---|
| **NIST SP 800-30 Rev. 1** | Quantitative risk assessment methodology · SLE/ARO/ALE modeling · residual risk calculation |
| **NIST SP 800-34 Rev. 1** | DRP/BCP structure · RTO/RPO definition · DR testing schedule |
| **NIST CSF 2.0** | Control catalog backbone · GRC program design · vendor risk (GV.SC) |
| **NIST SP 800-53 Rev. 5** | Control family references throughout · CA-5 (POA&M) · SA-9 · SR family |
| **NIST SP 800-161 Rev. 1 Upd. 1** | Primary C-SCRM framework for vendor-risk/ · SR-9 criticality analysis · SR-13 supplier inventory |
| **ISO/IEC 27001:2022** | Statement of Applicability (all 93 Annex A controls) · control catalog mapping |
| **COBIT 2019** | Governance model structure · IT-business alignment |
| **CSA CCM v4.0 / CAIQ v4** | CAIQ self-assessment · vendor scoring rubric question basis |
| **GLBA Safeguards Rule** | Gap analysis · vendor oversight §314.4(f) · data handling and breach notification |
| **PCI DSS v4.0** | Gap analysis and crosswalk · CAIQ implementation statements · Req 12.8 (TPSP management) |
| **FFIEC Cybersecurity** | Gap analysis · cybersecurity assessment tool mapping |
| **SOX IT General Controls** | Change management · access control · audit logging coverage |

---

## Skills Demonstrated

**Risk Assessment** — Quantitative ALE modeling · inherent and residual risk calculation (NIST SP 800-30) · risk register development and management · risk treatment decision-making

**Compliance** — Multi-framework gap analysis · regulatory crosswalks (GLBA/PCI/FFIEC) · ISO 27001:2022 Statement of Applicability · control mapping across six frameworks simultaneously

**Governance** — GRC program design · policy lifecycle management · governance model development · 18-month roadmap with phased implementation

**Vendor Risk** — End-to-end TPRM lifecycle · security questionnaire completion (CAIQ v4) · vendor tiering · inherent and residual risk assessment · POA&M tracking · executive reporting

**Documentation** — Evidence-level traceability · audit-ready formatting · executive decision memos · condition/criteria/cause/effect/recommendation finding structure

---

## About This Project

This repository reflects real-world GRC analyst work product. SecurityGroup101 is a fictional company created for portfolio purposes. All framework citations reference official, publicly available guidance.

The program's honesty about its own maturity — clearly distinguishing Implemented from Partial, Draft, Planned, and Gap — is intentional. A GRC analyst's job is to surface where a program actually stands, not to present an idealized version of it.

**Completed by:** Maxine Jones · GRC Analyst · mkj00015@mix.wvu.edu  
**Repository:** github.com/Mkjones10/securitygroup101-enterprise-grc-program  
**Last updated:** July 2026
