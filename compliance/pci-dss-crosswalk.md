# PCI DSS v4.0 Crosswalk – SecurityGroup101

SecurityGroup101 processes payment card data and must comply with **PCI DSS v4.0**.  

This document maps PCI DSS requirements to controls across **NIST CSF, ISO 27001, and COBIT 2019**, enabling a unified and scalable compliance framework.

---

## Scope

This crosswalk applies to:

- Cardholder Data Environment (CDE)  
- Payment processing applications  
- Supporting cloud infrastructure and network components  

---

## Control Mapping

| PCI DSS Requirement | Description | Mapped Framework Control | Current State | Gap Summary |
|--------------------|------------|--------------------------|--------------|------------|
| **1.2 Network Segmentation** | Restrict CDE from other networks | NIST CSF PR.AC-5, COBIT DSS01 | Partial | Segmentation not formally validated |
| **3.4 PAN Protection** | Render PAN unreadable where stored | ISO 27001 A.10, NIST PR.DS-1 | Partial | Encryption not standardized |
| **6.2 Vulnerability Management** | Ensure timely patching and remediation | NIST PR.IP-12, COBIT DSS05 | Partial | No defined remediation SLAs |
| **8.3 Strong Authentication** | MFA for remote and administrative access | NIST PR.AC-7, ISO 27001 A.9 | Partial | MFA not consistently enforced |
| **10.2 Logging and Monitoring** | Track access to CDE systems | NIST DE.CM-1, COBIT DSS05.04 | Partial | Incomplete log sources and retention |

---

## Key Gaps Identified

- Absence of documented quarterly ASV (Approved Scanning Vendor) scans  
- Lack of formal network segmentation validation and documentation  
- Log retention below PCI DSS requirement of 12 months  
- Inconsistent enforcement of MFA for administrative and remote access  

---

## Recommendations

- Implement automated vulnerability scanning and schedule quarterly ASV scans  
- Document, validate, and periodically test CDE network segmentation  
- Extend log retention to meet or exceed 12-month PCI DSS requirements  
- Enforce MFA across all administrative and remote access points  

---

## Key Insights

- Control implementation is **partially aligned but lacks consistency and formalization**  
- Identity and access management gaps increase exposure to unauthorized access  
- Logging and monitoring deficiencies reduce visibility into potential compromises  
- Network segmentation weaknesses increase risk of lateral movement into the CDE  

---

## Business Impact

This crosswalk supports:

- Alignment with **PCI DSS v4.0 compliance requirements**  
- Integration into a **unified control framework (NIST, ISO 27001, COBIT)**  
- Risk-based prioritization of remediation activities  
- Improved audit readiness and compliance reporting  

---

## Summary

This PCI DSS crosswalk provides a structured approach to:

- Align payment security controls with multiple frameworks  
- Identify and prioritize compliance gaps  
- Strengthen protection of cardholder data  
- Support continuous improvement within the enterprise GRC program  

These controls are integrated into the broader **control catalog, risk register, and GRC roadmap** to ensure consistent governance and compliance.
