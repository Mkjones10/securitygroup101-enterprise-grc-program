# Control Catalog – SecurityGroup101

This control catalog harmonizes requirements across **NIST CSF, ISO 27001, COBIT 2019, GLBA, PCI DSS, and FFIEC** into a unified set of security controls for SecurityGroup101.

It provides a centralized view of control implementation, alignment, and gaps across the enterprise.

---

## Objectives

- Standardize security controls across multiple frameworks  
- Enable consistent control implementation and tracking  
- Support compliance and audit readiness  
- Provide visibility into control effectiveness and gaps  

---

## Control Catalog

| Control ID | Framework(s) | Control Name | Description | Status |
|-----------|--------------|--------------|-------------|--------|
| **AC-01** | NIST CSF, ISO 27001 A.9 | Access Control Policy | Defined access control policy outlining roles, responsibilities, and access rules | Draft |
| **AC-02** | NIST CSF, GLBA, PCI DSS 8 | Strong Authentication | Multi-factor authentication enforced for administrative and remote access | Partial |
| **AC-03** | NIST CSF, FFIEC | Least Privilege | Access granted based on least privilege and business need-to-know | Partial |
| **DS-01** | NIST PR.DS-1, ISO 27001 A.10, GLBA | Data-at-Rest Protection | Encryption of customer and financial data at rest | Partial |
| **DS-02** | NIST PR.DS-2, PCI DSS 3.4 | Data-in-Transit Protection | Encryption of sensitive data in transit | Implemented |
| **DS-03** | GLBA, PCI DSS, FFIEC | Data Loss Prevention | DLP controls for email, endpoints, and cloud storage | Gap |
| **IP-01** | NIST PR.IP-12, PCI DSS 6.2 | Patch Management | Formal patching process with risk-based SLAs | Partial |
| **IP-02** | COBIT DSS05 | Vulnerability Management | Continuous vulnerability scanning, prioritization, and remediation | Partial |
| **DE-01** | NIST DE.CM-1, FFIEC | Security Monitoring | Centralized logging and SIEM monitoring for critical systems | Partial |
| **RS-01** | NIST RS, GLBA | Incident Response Plan | Documented incident response plan with defined roles and procedures | Draft |
| **RC-01** | NIST RC.IM-1 | Lessons Learned | Post-incident reviews and continuous improvement processes | Gap |
| **RE-01** | NIST SP 800-34, FFIEC | Disaster Recovery | DRP aligned with business priorities and regularly tested | Implemented |
| **RE-02** | NIST SP 800-34, FFIEC | Business Continuity | BCP supporting operational continuity and workforce resilience | Partial |

---

## Control Status Definitions

- **Implemented:** Fully deployed and operational  
- **Partial:** Implemented but incomplete or inconsistent  
- **Draft:** Defined but not yet implemented  
- **Gap:** Control not implemented  

---

## Key Insights

- Core identity and access controls (MFA, least privilege) are not fully enforced  
- Data protection controls are partially implemented, increasing exposure risk  
- Monitoring and detection capabilities require expansion for full coverage  
- Incident response and continuous improvement processes are not fully mature  

---

## Business Impact

This control catalog supports:

- Unified alignment across multiple regulatory frameworks  
- Improved audit readiness and compliance reporting  
- Risk-based prioritization of control implementation  
- Integration with the enterprise risk register and GRC roadmap  

---

## Summary

The control catalog provides a centralized framework for managing security controls across SecurityGroup101.

It enables consistent tracking of implementation status, identification of gaps, and alignment with industry standards, supporting the broader **GRC program, risk management strategy, and compliance initiatives**.
