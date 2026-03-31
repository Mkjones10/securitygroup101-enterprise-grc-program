# ALE Calculations – SecurityGroup101

This document details the quantitative risk calculations used to determine **Annualized Loss Expectancy (ALE)** across critical assets in the SecurityGroup101 environment.

These calculations support risk prioritization, control implementation, and disaster recovery planning.

---

## Formula

- **Annualized Loss Expectancy (ALE) = SLE × ARO**

Where:

- **SLE (Single Loss Expectancy):** Financial impact of a single incident  
- **ARO (Annual Rate of Occurrence):** Estimated frequency per year  

---

## ALE Calculations

| Asset | SLE ($) | ARO | Calculation | ALE ($) |
|------|--------|-----|------------|--------|
| **Customer Data** | 1,000,000 | 0.50 | 1,000,000 × 0.50 | **500,000** |
| **Employee Workstations** | 200,000 | 2.00 | 200,000 × 2.00 | **400,000** |
| **Financial Records** | 1,500,000 | 0.10 | 1,500,000 × 0.10 | 150,000 |
| **Backup Systems** | 600,000 | 0.25 | 600,000 × 0.25 | 150,000 |
| **Proprietary Software** | 750,000 | 0.15 | 750,000 × 0.15 | 112,500 |
| **Cloud Storage** | 500,000 | 0.05 | 500,000 × 0.05 | 25,000 |
| **Development Environment** | 100,000 | 0.20 | 100,000 × 0.20 | 20,000 |
| **Database Server** | 50,000 | 0.33 | 50,000 × 0.33 | 16,665 |
| **Email Server** | 30,000 | 0.50 | 30,000 × 0.50 | 15,000 |
| **Website** | 75,000 | 0.20 | 75,000 × 0.20 | 15,000 |

---

## Key Insights

- **Customer Data ($500K ALE)** represents the highest financial risk due to regulatory exposure and breach impact  
- **Employee Workstations ($400K ALE)** indicate high likelihood (ARO = 2.0), making endpoints a primary attack vector  
- Mid-tier systems (e.g., backups, financial systems) present **significant secondary risk** if compromised during an attack  
- Lower-tier assets still contribute to **attack paths and lateral movement risk**

---

## Business Impact

These calculations enable:

- **Risk-based prioritization** of cybersecurity investments  
- Alignment of **RTO/RPO tiers** in disaster recovery planning  
- Justification of **security controls using financial impact**  
- Executive-level reporting using **quantifiable risk metrics**  

---

## Summary

This ALE model translates technical cybersecurity risks into **financial terms**, allowing leadership to:

- Prioritize high-impact threats  
- Allocate resources effectively  
- Align security strategy with business risk tolerance  
