# Risk Heatmap – SecurityGroup101

This heatmap translates quantitative risk metrics (ALE, SLE, ARO) into a qualitative view of likelihood and impact to support prioritization and executive decision-making.

---

## Methodology

- **Likelihood:** Derived from Annual Rate of Occurrence (ARO)  
- **Impact:** Derived from Single Loss Expectancy (SLE) and regulatory/business impact  
- **Risk Level:** Determined by combining likelihood and impact  

---

## Risk Classification Table

| Asset | Likelihood | Impact | Risk Level |
|------|-----------|--------|------------|
| **Customer Data** | High | High | Critical |
| **Employee Workstations** | High | Medium | High |
| **Financial Records** | Medium | High | High |
| **Backup Systems** | Medium | High | High |
| **Proprietary Software** | Medium | Medium | Medium |
| **Cloud Storage** | Low | High | Medium |
| **Development Environment** | Low | Medium | Medium |
| **Database Server** | Medium | Low | Moderate |
| **Email Server** | Medium | Low | Moderate |
| **Website** | Low | Medium | Moderate |

---

## Heatmap Interpretation

### Critical Risk (High Likelihood / High Impact)
- Customer Data  

Represents the highest priority due to financial, regulatory, and reputational impact.

---

### High Risk (Moderate–High Likelihood / High Impact)
- Employee Workstations  
- Financial Records  
- Backup Systems  

These systems are either likely entry points or high-impact assets that can escalate into enterprise-wide incidents.

---

### Medium Risk (Moderate Likelihood or Impact)
- Proprietary Software  
- Cloud Storage  
- Development Environment  

These systems introduce indirect risk through lateral movement, misconfiguration, or exposure of sensitive processes.

---

### Moderate Risk (Lower Impact or Likelihood)
- Database Server  
- Email Server  
- Website  

Lower priority individually but still relevant for monitoring, attack surface reduction, and defense-in-depth.

---

## Key Insights

- Customer Data remains the highest-risk asset and requires the strongest controls (encryption, access control, monitoring)  
- Employee Workstations represent the most likely attack vector due to high frequency of compromise  
- Backup Systems and Financial Records introduce significant secondary risk, particularly in ransomware scenarios  
- Lower-tier assets can still enable lateral movement and escalation if not properly secured  

---

## Business Impact

This heatmap supports:

- Risk-based prioritization of security controls  
- Alignment of Tier 1, Tier 2, and Tier 3 recovery strategies  
- Executive reporting using simplified risk visualization  
- Strategic decision-making for security investments and mitigation efforts  

---

## Summary

The risk heatmap provides a high-level visualization of enterprise risk posture, connecting:

- Quantitative risk analysis (ALE, SLE, ARO)  
- Operational security decisions  
- Executive-level communication  

It ensures that security efforts are focused on the most impactful and likely threats to the organization.
