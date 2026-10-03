# Case Study Document: HR Analytics – Boosting Retention with Data Insights at Adecco India

---

## 1. Background & Business Context

**Adecco India** is a medium-sized technology enterprise specializing in software development, cloud services, and IT consulting. The company employs a diverse workforce distributed across several core operational departments:
* **Engineering / Research & Development**
* **Sales & Account Management**
* **Human Resources**
* **Customer Support & Operations**
* **Marketing**

Recently, senior management has observed a noticeable rise in employee turnover across the company, with the sharpest spike occurring among **junior-level employees within the Sales department**.

---

## 2. Problem Statement & Business Scenario

### **What is the Problem?**
Adecco India is facing an elevated attrition rate that is disproportionately affecting early-career professionals in the Sales and Technical operations. This turnover creates team disruption, increases workload stress on remaining personnel, slows client onboarding, and hurts overall workplace morale.

### **Why is it Important to Solve?**
1. **Escalating Financial Costs:** Continuous recruiting, onboarding, and training of replacement personnel costs between $1.5\times$ to $2\times$ an employee’s annual compensation.
2. **Loss of Productivity & Pipeline Stagnation:** Unfilled sales quotas directly impair quarterly revenue targets and enterprise growth milestones.
3. **Workplace Morale & Capability Loss:** Frequent departures lead to burnout among retained team members, fostering a cycle of further attrition.
4. **Strategic Long-Term Goals:** Maintaining a stable, motivated talent bench is critical for Adecco India to maintain consistent delivery standards and client trust.

---

## 3. Stakeholder Analysis

| Stakeholder Group | Classification | Key Concerns & Objectives |
| :--- | :--- | :--- |
| **Senior Executive Leadership** | Internal | Enterprise workforce stability, bottom-line ROI, operating margin preservation, and long-term organizational health. |
| **Human Resources Department** | Internal | Reducing cost-per-hire, accelerating onboarding, designing competitive compensation tiers, and tracking employee pulse scores. |
| **Sales Department Leadership** | Internal | Quota achievement, pipeline velocity, team workload balance, and preventing burnout among junior sales reps. |
| **Engineering / R&D Leadership** | Internal | Preserving institutional technical knowledge, project delivery timelines, and mentor bandwidth. |
| **Customer Support & Ops** | Internal | Service Level Agreement (SLA) consistency, customer satisfaction, and frontline stability. |
| **Recruitment Agencies** | External | Sourcing qualified candidates, market compensation rate benchmarking, and talent availability. |
| **Training Providers & Vendors** | External | Delivering professional development, upskilling modules, and onboarding certifications. |

---

## 4. Data Requirements & Sourcing

To conduct comprehensive HR predictive and descriptive analytics, data is aggregated from four internal systems:
* **HRIS (Human Resource Information System):** Demographic records, employment duration, department, education, and compensation details.
* **Performance Management System (PMS):** Annual appraisal ratings, promotion intervals, training attendance, and work-life balance feedback.
* **Employee Engagement Surveys:** Standardized ratings (1–4 scale) covering job satisfaction, work environment, and job involvement.
* **Exit Interviews:** Categorical reasons for departure, feedback on managerial relationships, and compensation satisfaction.

---

## 5. Complete Data Dictionary (35 Attributes)

The dataset contains records for **$N = 1,470$ employees** across the following 35 columns:

| # | Attribute Name | Data Type | Value Domain / Scale | Description |
| :-: | :--- | :---: | :---: | :--- |
| **1** | `Age` | Numerical | 18 – 60 | Age of the employee in years. |
| **2** | `Attrition` | Categorical (Binary) | `Yes` / `No` | Whether the employee has exited the organization. |
| **3** | `BusinessTravel` | Categorical | `Non-Travel`, `Travel_Rarely`, `Travel_Frequently` | Frequency of business travel required for the role. |
| **4** | `DailyRate` | Numerical | $102 – $1,499 | Daily compensation rate in USD. |
| **5** | `Department` | Categorical | `Sales`, `Research & Development`, `Human Resources` | Department in which the employee works. |
| **6** | `DistanceFromHome` | Numerical | 1 – 29 | Commute distance from home to workplace (in km/miles). |
| **7** | `Education` | Scale (1–5) | 1 = Below College, 2 = College, 3 = Bachelor, 4 = Master, 5 = Doctor | Highest formal education level attained. |
| **8** | `EducationField` | Categorical | `Life Sciences`, `Medical`, `Marketing`, `Technical Degree`, `Human Resources`, `Other` | Academic specialization or field of study. |
| **9** | `EmployeeCount` | Numerical | 1 | Constant individual-level identifier (= 1). |
| **10** | `EmployeeNumber` | Numerical | Unique ID | Unique employee identification number. |
| **11** | `EnvironmentSatisfaction` | Scale (1–4) | 1 = Low, 2 = Medium, 3 = High, 4 = Very High | Employee's satisfaction with their physical work environment. |
| **12** | `Gender` | Categorical | `Male`, `Female` | Gender of the employee. |
| **13** | `HourlyRate` | Numerical | $30 – $100 | Hourly wage rate of the employee. |
| **14** | `JobInvolvement` | Scale (1–4) | 1 = Low, 2 = Medium, 3 = High, 4 = Very High | Degree of involvement and commitment to the current job. |
| **15** | `JobLevel` | Scale (1–5) | 1 = Entry/Junior to 5 = Executive/Director | Hierarchical position tier within Adecco India. |
| **16** | `JobRole` | Categorical | 9 distinct job titles | Role within the organization (e.g., Sales Rep, Lab Tech, Manager). |
| **17** | `JobSatisfaction` | Scale (1–4) | 1 = Low, 2 = Medium, 3 = High, 4 = Very High | Self-reported satisfaction score with job tasks and culture. |
| **18** | `MaritalStatus` | Categorical | `Single`, `Married`, `Divorced` | Marital status of the employee. |
| **19** | `MonthlyIncome` | Currency ($) | $1,009 – $19,999 | Gross monthly salary. |
| **20** | `MonthlyRate` | Numerical | $2,094 – $26,999 | Internal monthly billing/cost allocation rate. |
| **21** | `NumCompaniesWorked` | Numerical | 0 – 9 | Total number of external employers worked for prior to Adecco. |
| **22** | `Over18` | Categorical | `Y` | Verification that employee is over 18 years old (= Y). |
| **23** | `OverTime` | Categorical (Binary) | `Yes` / `No` | Whether the employee regularly performs overtime work. |
| **24** | `PercentSalaryHike` | Numerical | 11% – 25% | Percentage salary increase awarded at the last annual review. |
| **25** | `PerformanceRating` | Scale (1–4) | 3 = Excellent, 4 = Outstanding | Annual appraisal performance rating score. |
| **26** | `RelationshipSatisfaction`| Scale (1–4) | 1 = Low, 2 = Medium, 3 = High, 4 = Very High | Satisfaction with interpersonal relationships with colleagues/manager. |
| **27** | `StandardHours` | Numerical | 80 | Standard working hours per bi-weekly pay period (= 80). |
| **28** | `StockOptionLevel` | Scale (0–3) | 0 = None, 1 = Standard, 2 = Executive, 3 = Senior | Equity grant ownership level awarded to the employee. |
| **29** | `TotalWorkingYears` | Numerical | 0 – 40 | Total cumulative career experience across all companies. |
| **30** | `TrainingTimesLastYear` | Numerical | 0 – 6 | Number of formal training sessions attended in previous year. |
| **31** | `WorkLifeBalance` | Scale (1–4) | 1 = Bad, 2 = Good, 3 = Better, 4 = Best | Employee's subjective rating of work-life balance. |
| **32** | `YearsAtCompany` | Numerical | 0 – 40 | Total tenure duration with Adecco India in years. |
| **33** | `YearsInCurrentRole` | Numerical | 0 – 18 | Number of years in current job title/position. |
| **34** | `YearsSinceLastPromotion` | Numerical | 0 – 15 | Years elapsed since the last promotion or upward grade change. |
| **35** | `YearsWithCurrManager` | Numerical | 0 – 17 | Working duration in years under the current reporting manager. |

---

## 6. Case Study Questions

### **Basic-Level Questions (Excel-Oriented)**
1. **Overall Attrition Rate:** What is the overall attrition rate at Adecco India?
2. **Department Breakdown:** Which department has the highest attrition rate?
3. **Age Profile of Leavers:** What is the average age of employees who have left the company?
4. **Job Satisfaction Variation:** How does job satisfaction vary across different job roles?
5. **Gender Comparison:** Is there a significant difference in attrition rates between male and female employees?
6. **Compensation of Exited Staff:** What is the average monthly income of employees who have left the company?
7. **Commute Distance Impact:** How does distance from home impact employee attrition?
8. **Performance Distribution:** What is the distribution of performance ratings among employees?
9. **Overtime Prevalence:** How many employees work overtime regularly?
10. **Organizational Tenure:** What is the average number of years employees have worked at Adecco India?

### **Medium-Level Questions (Analytical & Correlation-Oriented)**
1. **Top Contributing Drivers:** What are the top three factors contributing to employee attrition at Adecco India?
2. **Job Involvement Impact:** How does the attrition rate vary with different levels of job involvement?
3. **Age vs. Satisfaction:** Is there a relationship between employee age and job satisfaction?
4. **Marital Status Dynamics:** How does marital status impact employee attrition?
5. **Training Effectiveness:** What is the impact of training on employee attrition?
6. **Work-Life Balance vs. Performance:** How does work-life balance affect employee performance ratings?
7. **Stock Option Retention Leverage:** What is the effect of stock options on employee attrition?
8. **Tenure vs. Satisfaction:** How does employee tenure relate to job satisfaction?
9. **Business Travel Stress:** What is the impact of business travel on job satisfaction?
10. **Promotion Stagnation:** How do years since last promotion affect employee performance?
