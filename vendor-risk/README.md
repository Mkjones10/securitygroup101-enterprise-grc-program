# Vendor Risk Management Program

**SecurityGroup101 GRC Program  ·  Third-Party Risk Management**

This folder contains a complete, end-to-end vendor risk management (VRM) program built for SecurityGroup101, a fictional cloud-native fintech SaaS company. The program covers the full third-party risk lifecycle — from vendor intake through security questionnaire completion, risk tiering, inherent risk screening, CAIQ assessment, residual risk determination, remediation tracking, and executive reporting.

All artifacts are grounded in official framework guidance and reflect the day-to-day work of a GRC analyst supporting vendor risk assessment and security questionnaire operations.

**Frameworks:** NIST SP 800-161 Rev. 1 Upd. 1 (Nov. 2024) · NIST SP 800-30 Rev. 1 · NIST SP 800-53 Rev. 5 · NIST CSF 2.0 GV.SC · CSA CCM v4.0 / CAIQ v4 · PCI DSS v4.0 Req 12.8 · GLBA Safeguards Rule 16 CFR §314.4(f)

**Completed by:** Maxine Jones, GRC Analyst · mkj00015@mix.wvu.edu · July 2026

---

## Program Overview

The VRM program follows a nine-stage lifecycle aligned to NIST SP 800-161 Rev. 1 Upd. 1 supply chain risk management guidance:

```
Intake → Inventory → Tiering → Inherent Risk Screen → CAIQ Assessment
    → Scoring Rubric → Residual Risk Report → POA&M → Executive Summary
```

Each stage has a corresponding artifact in this folder. The Stripe, Inc. assessment is used as a worked example throughout — running from inherent risk scoring through the executive summary and approval signatures.

---

## Artifact Index

### Security Posture Documentation

| File | Description |
|---|---|
| `securitygroup101-security-trust-center.md` | Public-facing Security Trust Center documenting SecurityGroup101's compliance posture, encryption standards, MFA enforcement, incident response SLAs, subprocessor disclosure, and data handling commitments. |
| `SG101_Security_Trust_Center.pdf` | PDF version of the Security Trust Center. |

### Core Assessment Tools

| File | Description | Framework Basis |
|---|---|---|
| `SG101_CAIQ_v4_Completed.pdf` | CSA STAR Level 1 CAIQ v4 self-assessment completed as SecurityGroup101's security officer. 85 questions across 16 CCM v4.0 control domains with full implementation statements. 2 honest "No" answers with documented remediation plans. | CSA CCM v4.0 · NIST CSF 2.0 · ISO 27001:2022 · PCI DSS v4.0 · GLBA |
| `SG101_Vendor_Risk_Scoring_Rubric.pdf` | 36-question weighted vendor risk scoring rubric for reviewing inbound vendor questionnaires. 7 Critical red flags — any "No" triggers HIGH risk escalation regardless of overall score. Automatic risk tiering (Low / Medium / High / Critical). | CSA CCM v4.0 · NIST SP 800-161 Rev. 1 |

### VRM Program Artifacts

| File | Description | Framework Basis |
|---|---|---|
| `VRM_01_Vendor_Intake_Form.pdf` | New vendor request form capturing requestor info, vendor details, data and access classification (PHI / PCI / PII / production access / cloud / internet-facing / fourth parties), business justification, and GRC-use-only section for tier assignment and risk decision. | NIST SP 800-161 Rev. 1 GV.SC-02, SR-2 |
| `VRM_02_Vendor_Inventory_Register.pdf` | Third-party vendor inventory register with 11 vendors across all four risk tiers. Tracks business owner, tier, status, PHI/PCI/PII/production access flags, contract expiration, and next assessment date. | NIST SP 800-161 Rev. 1 SR-13 · NIST SP 800-53 Rev. 5 SR-2 · PCI DSS v4.0 Req 12.8.1 |
| `VRM_03_Vendor_Tiering_Matrix.pdf` | Four-tier risk tiering framework defining data/access criteria, regulatory relevance, assessment requirements, review frequency, and contract requirements for each tier. Tier 1 (Critical) through Tier 4 (Low). | NIST SP 800-161 Rev. 1 SR-9 · NIST CSF 2.0 GV.SC-06 · PCI DSS v4.0 Req 12.8.1 · GLBA §314.4(f) |
| `VRM_04_Inherent_Risk_Questionnaire.pdf` | 16-question inherent risk questionnaire administered before the full CAIQ to determine scope of due diligence required. Each question cites the specific NIST or PCI DSS provision that drives its inclusion. Scoring key with assessment pathway routing. | NIST SP 800-161 Rev. 1 SR-2, SR-9 · NIST SP 800-53 Rev. 5 RA-3 · NIST CSF 2.0 ID.RA-09 |
| `VRM_05_Residual_Risk_Report_Stripe.pdf` | Formal residual risk report for Stripe, Inc. (Tier 1 — Critical). Covers vendor identification, inherent risk assessment (HIGH, 28/38), control effectiveness assessment (STRONG — PCI DSS Level 1, unqualified SOC 2 Type II), residual risk determination (MEDIUM-LOW), and risk decision (Approved with Conditions). | NIST SP 800-30 Rev. 1 Section 3.4 · NIST SP 800-161 Rev. 1 · PCI DSS v4.0 Req 12.8 |
| `VRM_06_Vendor_POAM.pdf` | Vendor risk POA&M (Plan of Action and Milestones) tracking 8 open findings across 6 vendors (Stripe, AWS, Datadog, Zendesk, GitHub, Okta, Snowflake). 1 High finding (Snowflake DSP-01: PII data masking), 2 Medium, 3 Low, 2 Informational. Each finding includes owner, due date, evidence required, and analyst notes. | NIST SP 800-53 Rev. 5 CA-5 · NIST SP 800-161 Rev. 1 GV.SC-09 · NIST CSF 2.0 RS.MI |
| `VRM_07_Executive_Summary_Stripe.pdf` | Three-page executive summary for the Stripe assessment covering vendor profile, assessment summary (CAIQ 92.2%, SOC 2 Type II unqualified, PCI DSS AoC current), risk determination (Inherent HIGH → Controls STRONG → Residual MEDIUM-LOW), open findings, recommendation (Approved with Conditions), and approval signature block. | NIST SP 800-161 Rev. 1 · NIST SP 800-30 Rev. 1 · PCI DSS v4.0 Req 12.8 |

---

## The Assessment Lifecycle — Stripe, Inc.

The Stripe assessment demonstrates how all seven VRM artifacts connect in practice:

**1. Intake (VRM_01)** — New vendor request submitted by VP Finance. Data classification flags: PCI = Yes, PII = Yes, Production Access = Yes. Risk tier pre-assigned: Tier 1 — Critical.

**2. Inventory (VRM_02)** — Stripe added to vendor inventory register as Vendor #2. Status: Active. Contract expiration: March 2027. Next assessment: April 2027.

**3. Tiering (VRM_03)** — Tier 1 criteria met: PCI-scoped payment card data + direct production API integration. Full CAIQ v4 + SOC 2 Type II required. Annual review cadence.

**4. Inherent Risk Screen (VRM_04)** — 16-question IRQ administered. Score: 28/38 (73.7%). Rating: **HIGH**. Drivers: PCI scope (+4), PII (+3), production API access (+3), cloud SaaS (+2), subprocessors (+2), sole-source criticality (+2). Credit: PCI DSS Level 1 certification (−1).

**5. CAIQ Assessment** — Full 85-question CAIQ v4 completed. Score: 83/90 weighted points (92.2%). Two honest gaps documented with remediation plans: DSP-09 (data sharing register in progress) and STA-06 (supply chain risks not yet in risk register).

**6. Scoring Rubric** — 36-question rubric applied to Stripe's inbound questionnaire responses. All 7 Critical red flags passed. Overall: LOW risk rating.

**7. Residual Risk (VRM_05)** — Inherent: HIGH. Control Effectiveness: STRONG (PCI DSS Level 1 + unqualified SOC 2 Type II + FIDO2 MFA + AES-256/TLS 1.3). Residual Risk: **MEDIUM-LOW** per NIST SP 800-30 Rev. 1 Section 3.4.

**8. POA&M (VRM_06)** — 2 findings from Stripe tracked: VRM-2026-001 (DSP-09, Low, Q4 2026) and VRM-2026-002 (STA-06, Informational, Q4 2026).

**9. Executive Summary (VRM_07)** — Decision: **Approved with Conditions**. Conditions: annual CAIQ + SOC 2 reassessment, POA&M items closed by Q4 2026, 30-day subprocessor change notice, right-to-audit clause in MSA. Next review: July 2027.

---

## Vendor Inventory Summary

| # | Vendor | Tier | PCI | PHI | PII | Prod Access | Status |
|---|---|---|---|---|---|---|---|
| 1 | Amazon Web Services | Tier 1 — Critical | No | No | Yes | Yes | Active |
| 2 | Stripe | Tier 1 — Critical | Yes | No | Yes | No | Active |
| 3 | Okta | Tier 1 — Critical | No | No | Yes | Yes | Active |
| 4 | Datadog | Tier 2 — High | No | No | No | No | Active |
| 5 | GitHub (Microsoft) | Tier 2 — High | No | No | No | No | Active |
| 6 | Zendesk | Tier 2 — High | No | No | Yes | No | Active |
| 7 | DocuSign | Tier 3 — Moderate | No | No | Yes | No | Active |
| 8 | Snowflake | Tier 1 — Critical | Yes | No | Yes | Yes | Active |
| 9 | Twilio | Tier 3 — Moderate | No | No | Yes | No | Active |
| 10 | Acme Catering Co. | Tier 4 — Low | No | No | No | No | Active |
| 11 | Legacy CRM Vendor | Tier 2 — High | No | No | Yes | No | Offboarded |

---

## Open POA&M Findings Summary

| Finding ID | Vendor | CCM Control | Severity | Due Date | Status |
|---|---|---|---|---|---|
| VRM-2026-001 | Stripe | DSP-09 | Low | Q4 2026 | Open |
| VRM-2026-002 | Stripe | STA-06 | Informational | Q4 2026 | In Progress |
| VRM-2026-003 | AWS | CEK-05 | Low | Aug 2026 | Open |
| VRM-2026-004 | Datadog | LOG-04 | Informational | Aug 2026 | Open |
| VRM-2026-005 | Zendesk | STA-05 | **Medium** | Sep 2026 | Open |
| VRM-2026-006 | GitHub | TVM-01 | **Medium** | Sep 2026 | In Progress |
| VRM-2026-007 | Okta | IAM-06 | Low | Oct 2026 | Open |
| VRM-2026-008 | Snowflake | DSP-01 | **High** | Aug 2026 | In Progress |

---

## Framework Reference Index

| Framework | Version | How It's Applied in This Folder |
|---|---|---|
| NIST SP 800-161 | Rev. 1 Upd. 1 (Nov. 2024) | Primary C-SCRM framework. SR-2 (supply chain risk management plan), SR-9 (criticality analysis), SR-13 (supplier inventory), GV.SC-02 (roles and responsibilities), GV.SC-06 (tiering), GV.SC-09 (POA&M) |
| NIST SP 800-30 | Rev. 1 | Risk assessment methodology. Section 3.4 (residual risk calculation: inherent risk adjusted for control effectiveness) applied in VRM_05 |
| NIST SP 800-53 | Rev. 5 | Control family references throughout CAIQ. CA-5 (POA&M), SA-9 (external information system services), SR-2 (supply chain risk management), RA-3 (risk assessment), RA-5 (vulnerability monitoring), AC-2 (account management), AC-6 (least privilege) |
| NIST CSF 2.0 | 2024 | GV.SC (govern supply chain risk), ID.RA (risk assessment), ID.RA-09 (third-party risk), DE.CM (continuous monitoring), RS.MI (incident mitigation), RS.AN (incident analysis) |
| CSA CCM | v4.0 | CAIQ v4 question domains: AIS, BCR, CCC, CEK, DSP, GRC, HRS, IAM, IPY, IVS, LOG, SEF, STA, TVM, UEM. Scoring Rubric weighted by CCM control criticality |
| PCI DSS | v4.0 | Req 12.8 (TPSP management): written agreement, annual compliance confirmation, list of TPSPs, subprocessor disclosure. Req 12.8.1 (vendor inventory), Req 12.8.5 (subcontractor disclosure) |
| GLBA Safeguards Rule | 16 CFR Part 314 | §314.4(f): vendor oversight obligations — due diligence, contractual protections, ongoing monitoring. Breach notification requirements. Data handling and disposal in vendor contracts |
| ISO 27001 | 2022 | A.5.21 (information security in supplier relationships), A.5.22 (managing supplier service delivery), A.5.23 (cloud services). Referenced in CAIQ implementation statements |

---

## Skills Demonstrated

- **Security questionnaire completion** — 85-question CAIQ v4 self-assessment completed with full implementation statements citing actual framework controls and repo documentation
- **Vendor risk assessment** — End-to-end third-party risk assessment of Stripe, Inc. from inherent risk screening through executive approval
- **Risk tiering** — Four-tier vendor classification framework with documented criteria, regulatory relevance, and assessment requirements per tier
- **Vendor inventory management** — 11-vendor register with PHI/PCI/PII/production access tracking and assessment scheduling
- **Residual risk calculation** — NIST SP 800-30 Rev. 1 methodology: inherent risk adjusted for control effectiveness to produce residual risk rating
- **POA&M management** — 8 open findings across 6 vendors with assigned owners, due dates, evidence requirements, and remediation tracking
- **Executive reporting** — Three-page executive summary translating technical assessment results into a clear risk decision for CISO and business owner sign-off
- **Framework alignment** — NIST SP 800-161 Rev. 1 Upd. 1, NIST SP 800-30 Rev. 1, NIST SP 800-53 Rev. 5, NIST CSF 2.0, CSA CCM v4.0, PCI DSS v4.0, GLBA Safeguards Rule

---

*Part of the SecurityGroup101 Enterprise GRC Program · [View full repository](https://github.com/Mkjones10/securitygroup101-enterprise-grc-program) · Completed by Maxine Jones, GRC Analyst · mkj00015@mix.wvu.edu · July 2026*
