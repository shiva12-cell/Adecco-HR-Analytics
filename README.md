# Adecco HR Analytics: Boosting Retention with Data Insights

- **Domain:** Human Resources Analytics, Workforce Optimization & People Analytics
- **Primary Tech Stack:** Python (`pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`), Excel / Power BI Business Intelligence
  
- **Core Scope:** End-to-end People Analytics study evaluating workforce attrition dynamics across 1,470 employee records and 35 organizational attributes at Adecco India to identify voluntary departure drivers, assess department-level flight risks, and build a strategic retention framework.

---

## Executive Summary
Adecco India faced an overall voluntary employee attrition rate of 16.12%, surpassing standard industry benchmarks (12%–15%) and generating substantial replacement costs (averaging 1.5× to 2.0× annual salary per employee) along with operational burnout across delivery units.

This project delivers an enterprise-grade People Analytics investigation integrating demographic profiles, compensation structures, workload indicators, and engagement surveys across 1,470 employees. The study isolates structural catalysts behind employee turnover—revealing that excessive unmitigated overtime is the single largest flight risk, junior sales representatives face disproportionate early-tenure turnover, compensation gaps between departing and retained staff widen turnover, and equity vesting programs provide an immediate 61.5% reduction in attrition.

---

## Key Metrics
- **Workforce Size & Attrition Rate:** 1,470 total employees analyzed; overall voluntary attrition is **16.12%** (237 departed employees).
- **Overtime Flight Risk:** Overtime workload is the #1 turnover catalyst ($r = +0.2461$), driving an attrition rate of **30.5%** among staff working regular overtime compared to non-overtime cohorts.
- **Department Disparities:** Sales experiences the highest turnover at **20.63%**, followed by HR (**19.05%**) and R&D (**13.84%**).
- **Role Vulnerability:** Junior Sales Representatives suffer severe early-career flight at **~39.8%** attrition.
- **Compensation Disparity:** Departing employees earn **$2,045.65 less per month (-29.9%)** on average compared to retained colleagues ($4,787 vs. $6,833; $r = -0.1598$).
- **Equity Vesting Multiplier:** Staff with zero stock options (Level 0) experience **24.41%** attrition; granting baseline equity (Level 1) drops attrition to **9.40%** (a **61.5% retention improvement**).
- **Commute Distance Friction:** Employees commuting $>20\text{ km}$ experience **22.81%** attrition, compared to **14.08%** for those living within $5\text{ km}$ ($>50\%$ risk increase).
- **Training Engagement Impact:** Zero annual training sessions yields **27.78%** turnover, whereas providing 5–6 training opportunities drops attrition to **9.23%**.

---

## Repository Structure
```text
Adecco-HR-Analytics/
│
├── Raw Data/                               # Unprocessed enterprise HRIS and survey datasets
├── Dataset/                                # Cleaned and transformed employee records
├── Dashboard_Image/                        # BI dashboard previews & visualizations
│   └── Dashboard.png
├── HR_Analytics_Case_Study_Document.md     # Business background, problem context & data dictionary
├── HR_Analytics_Solution_Guide.md          # Comprehensive statistical solutions & derivations
├── Adecco HR Analytics.pdf                 # Executive-ready case study & presentation report
└── README.md                               # Primary project documentation
```

---

## Strategic Recommendations
1. **Restructure Junior Sales Compensation & Base Pay:**
   - Elevate entry-level base compensation for Sales Representatives from ~$4,700 toward a $5,500 threshold to reduce over-reliance on volatile commissions and mitigate early-career turnover (39.8%).
2. **Institute Overtime Governance & Compensatory Offs:**
   - Enforce managerial approvals for overtime exceeding 15 hours/month and mandate compensatory time-off (comp-offs) to address the #1 turnover catalyst ($r = +0.2461$, 30.5% attrition).
3. **Broaden Micro-Vesting Equity (ESOP) Grants:**
   - Roll out baseline Level 1 stock option grants with 3-year cliff vesting to junior technical and commercial individual contributors to harness the proven 61.5% attrition reduction.
4. **Deploy a 2-Day Hybrid Commute Policy:**
   - Establish flexible work-from-home options for employees commuting $>15\text{–}20\text{ km}$ to lower transit burnout and curb the 22.81% long-distance turnover spike.
5. **Mandate Structured L&D Career Pathways:**
   - Require a minimum of 3–4 formalized technical/soft-skill training modules annually per employee, closing the flight vulnerability observed in zero-training cohorts (27.78% vs. 9.23%).
