# Risk Register – SecurityGroup101

This risk register is based on a quantitative risk assessment (QRA) aligned with **NIST SP 800-30**. It uses financial risk modeling (SLE, ARO, ALE) to prioritize cybersecurity risks across a fintech environment.

---

## Methodology

- **Single Loss Expectancy (SLE):** Estimated financial impact of a single incident  
- **Annual Rate of Occurrence (ARO):** Estimated frequency of occurrence per year  
- **Annual Loss Expectancy (ALE):** `SLE × ARO`  
- **Risk Rating:** Determined based on ALE, regulatory exposure, and operational criticality  

---

## Asset Risk Register

| Asset | Description | SLE ($) | ARO | ALE ($) | Risk Tier | Primary Threats | Key Dependencies |
|------|------------|--------|-----|--------|-----------|-----------------|-----------------|
| **Customer Data** | Personal, financial, and transactional customer data | 1,000,000 | 0.50 | 500,000 | **Tier 1** | Ransomware, data breach, unauthorized access | Cloud storage, DB servers, backups |
| **Employee Workstations** | End-user devices accessing internal/cloud systems | 200,000 | 2.00 | 400,000 | **Tier 1** | Malware, phishing, credential theft | AD/IdP, email, VPN |
| **Financial Records** | Accounting data, revenue, financial statements | 1,500,000 | 0.10 | 150,000 | Tier 2 | Fraud, tampering, unauthorized changes | ERP systems, DB servers |
| **Backup Systems** | On-prem and cloud backup infrastructure | 600,000 | 0.25 | 150,000 | Tier 2 | Ransomware, corruption, failed restores | Storage, DR site, backup software |
| **Proprietary Software** | Internal financial analytics and payment applications | 750,000 | 0.15 | 112,500 | Tier 2 | Exploitation, IP theft, code tampering | Dev environment, CI/CD, cloud runtime |
| **Cloud Storage** | Cloud-based operational and analytical storage | 500,000 | 0.05 | 25,000 | Tier 3 | Misconfiguration, unauthorized access, data loss | CSP IAM, network controls |
| **Development Environment** | Non-production systems for testing and development | 100,000 | 0.20 | 20,000 | Tier 3 | Code theft, insider threats, lateral movement | Source control, CI/CD, access control |
| **Database Server** | Databases supporting applications and services | 50,000 | 0.33 | 16,665 | Tier 3 | SQL injection, outages, corruption | App servers, storage, backups |
| **Email Server** | Corporate email and messaging systems | 30,000 | 0.50 | 15,000 | Tier 3 | Phishing, BEC, malware delivery | Identity systems, endpoints, filtering |
| **Website** | Customer-facing web portal | 75,000 | 0.20 | 15,000 | Tier 3 | DDoS, defacement, web exploitation | WAF, CDN, app servers |

---

## Risk Prioritization

### 🔴 Tier 1 – Critical
- Customer Data  
- Employee Workstations  

### 🟠 Tier 2 – High
- Financial Records  
- Backup Systems  
- Proprietary Software  

### 🟡 Tier 3 – Moderate
- Cloud Storage  
- Development Environment  
- Database Server  
- Email Server  
- Website  

---

## Key Insights

- **Customer Data ($500K ALE)** and **Employee Workstations ($400K ALE)** represent the highest financial and operational risk  
- Endpoint compromise and data breaches are the most likely entry points for enterprise-wide incidents  
- Moderate-tier assets still present cascading risk due to dependencies on critical systems  

---

## Business Impact

This risk register supports:

- Risk-based prioritization of security controls  
- Disaster recovery tiering (RTO/RPO alignment)  
- Compliance mapping (NIST, ISO 27001, PCI DSS, GLBA, FFIEC)  
- Executive-level risk reporting using financial metrics  

---

## Summary

This quantitative risk model enables leadership to:

- Translate cybersecurity risk into financial impact  
- Prioritize mitigation strategies based on measurable loss exposure  
- Align security investments with business risk tolerance  
