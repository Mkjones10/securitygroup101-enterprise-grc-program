
---

## `/risk-assessment/risk-register.md`

```markdown
# Risk Register – SecurityGroup101

This risk register is based on a quantitative risk assessment (QRA) following NIST SP 800-30. It uses Single Loss Expectancy (SLE), Annual Rate of Occurrence (ARO), and Annualized Loss Expectancy (ALE) to prioritize risks across SecurityGroup101’s fintech environment.

## Methodology

- **SLE:** Estimated financial impact of a single incident per asset
- **ARO:** Estimated frequency of occurrence per year based on historical or assumed data
- **ALE:** SLE × ARO
- **Risk Rating:** Based on ALE, regulatory impact, and operational criticality

## Asset Risk Register

| Asset                | Description                                                                 | SLE ($)     | ARO  | ALE ($)   | Risk Tier | Primary Threats                                      | Key Dependencies                          |
|----------------------|-----------------------------------------------------------------------------|-------------|------|-----------|-----------|------------------------------------------------------|-------------------------------------------|
| Customer Data        | Personal, financial, and transactional customer data                        | 1,000,000   | 0.50 | 500,000   | Tier 1    | Ransomware, data breach, unauthorized access         | Cloud storage, DB servers, backup systems |
| Employee Workstations| End-user devices used to access internal and cloud systems                  | 200,000     | 2.00 | 400,000   | Tier 1    | Malware, phishing, credential theft                  | AD/IdP, email, VPN                        |
| Financial Records    | Accounting data, revenue, financial statements                              | 1,500,000   | 0.10 | 150,000   | Tier 2    | Fraud, tampering, unauthorized changes               | ERP/finance apps, DB servers              |
| Backup Systems       | On-prem and cloud backup infrastructure                                     | 600,000     | 0.25 | 150,000   | Tier 2    | Ransomware, corruption, failed restores              | Storage, DR site, backup software         |
| Proprietary Software | Internal financial analytics and payment-related applications               | 750,000     | 0.15 | 112,500   | Tier 2    | Exploitation, IP theft, code tampering               | Dev environment, CI/CD, cloud runtime     |
| Cloud Storage        | Cloud-based storage for operational and analytical data                     | 500,000     | 0.05 | 25,000    | Tier 3    | Misconfiguration, unauthorized access, data loss     | CSP IAM, network controls                 |
| Development Environment | Non-production systems for testing and development                      | 100,000     | 0.20 | 20,000    | Tier 3    | Code theft, insider threat, pivot to production      | Source control, CI/CD, access control     |
| Database Server      | Databases supporting internal and customer-facing applications              | 50,000      | 0.33 | 16,665    | Tier 3    | SQL injection, outages, corruption                   | App servers, storage, backups             |
| Email Server         | Corporate email and messaging                                               | 30,000      | 0.50 | 15,000    | Tier 3    | Phishing, BEC, malware delivery                      | Identity, endpoints, spam filtering       |
| Website              | Customer-facing web portal for transactions and account access              | 75,000      | 0.20 | 15,000    | Tier 3    | DDoS, defacement, web app exploitation               | WAF, CDN, app servers                     |

## Risk Prioritization

- **Tier 1 – Critical:** Customer Data, Employee Workstations  
- **Tier 2 – High:** Financial Records, Backup Systems, Proprietary Software  
- **Tier 3 – Moderate:** Cloud Storage, Development Environment, Database Server, Email Server, Website  

These tiers drive recovery prioritization, control implementation, and monitoring focus across the GRC program.
