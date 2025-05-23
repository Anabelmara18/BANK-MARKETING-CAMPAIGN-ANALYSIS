# BANK-MARKETING-CAMPAIGN-ANALYSIS
To analyze the effectiveness of direct marketing campaigns, understand key factors influencing customer responses, and offer actionable insights to optimize future campaigns for improved targeting, efficiency, and ROI.

## Project Overview
This project analyzes data from a bank's direct marketing campaign to uncover patterns in customer behavior that influence the likelihood of subscribing to a term deposit. By transforming raw data into visual insights through a comprehensive dashboard, this analysis identifies key demographic and behavioral factors impacting subscription rates. The aim is to support strategic decisions for improving marketing efforts.

---

## Column Descriptions
| Column Name     | Description                                                         |
|-----------------|---------------------------------------------------------------------|
| **Age**         | Age of the client in years.                                         |
| **Job**         | Type of job held by the client (e.g., "admin", "blue-collar", "technician"). |
| **Marital**     | Marital status ("single", "married", "divorced").                   |
| **Education**   | Education level ("primary", "secondary", "tertiary").              |
| **Default**     | Whether the client has credit in default ("yes", "no").             |
| **Balance**     | Client’s account balance in euros (€).                              |
| **Housing**     | Whether the client has a housing loan ("yes", "no").                |
| **Loan**        | Whether the client has a personal loan ("yes", "no").               |
| **Contact**     | Communication method used (e.g., "cellular", "telephone").          |
| **Day**         | Day of the month when the last contact was made (1-31).             |
| **Month**       | Month of the last contact ("jan", "feb", etc.).                     |
| **Duration**    | Duration of the last contact in seconds.                            |
| **Campaign**    | Number of contacts made during this campaign.                       |
| **Pdays**       | Days since the client was last contacted (999 means no prior contact). |
| **Previous**    | Number of contacts made before this campaign.                       |
| **Poutcome**    | Outcome of the previous campaign ("failure", "success", "other").  |
| **Y**           | Whether the client subscribed to a term deposit ("yes", "no").     |
| **Balance Group** | Grouped balance categories using a formula (e.g., "Below 1K", "1K-5K", etc.). |
| **Call Duration** | Call duration in minutes, categorized into time intervals (e.g., "Less Than 3mins", "3-6mins", etc.). |
| **Period of Month** | Categorizes contact date into beginning, middle, or end of the month. |

---

## Steps Taken

### Data Cleaning:
- Checked for missing data using:
  ```excel
  =IF(COUNTA(A2:Q4522)=ROWS(A2:Q4522)*COLUMNS(A2:Q4522),"No Missing Data","Missing Data Found")
- Formatted monetary values according to accounting standards for better readability.
- Flagged negative balances with **dark orange fill** to indicate potential financial distress.
- Highlighted zero balances in **red** to suggest clients requiring re-engagement.
- Excluded rows with **undefined education levels** to maintain data consistency.

### Data Transformation
- Converted call duration from **seconds to minutes** and rounded to **1 decimal place**.
- Grouped call duration and account balances using the `IFS()` formula for better segmentation.
- Categorized the day of the month into:
  - **Beginning** (1–10)
  - **Middle** (11–20)
  - **End** (21–31)  
  This supported strategic timing analysis for outreach.


## Tools Used
- **Microsoft Excel**: Data cleaning, transformation, pivot tables, and dashboard creation.
- **Power Query**: Efficient data preprocessing.
- **Pivot Charts**: Interactive visualizations and insights.
- **Custom Icons & Design Elements**: Enhanced readability and visual appeal.

---

## Objectives
- Understand the demographic and behavioral factors contributing to term deposit subscriptions.
- Identify the most effective communication channels, timing, and customer profiles for higher subscription rates.
- Evaluate the role of call duration, frequency, and campaign history in influencing conversions.
- Recognize resistance factors such as loan burdens and housing status that may impact campaign success.
- Provide actionable recommendations to optimize future marketing strategies for better targeting and ROI.

---

## Data Source
> The dataset was provided by **Internpulse** as part of a data analytics internship project.  
> It contains records of marketing interactions conducted by a bank to promote **term deposit subscriptions**.

---
## DashBoard SnapShots
![Screenshot 2025-05-23 201206](https://github.com/user-attachments/assets/36c14dff-e21f-456d-84df-e01f8a44d8a1)
![Screenshot 2025-05-23 201531](https://github.com/user-attachments/assets/1f7042d5-295a-4832-91f4-38cb48ed8536)



## Executive Summary
This analysis explores the factors influencing customer subscriptions to a bank’s term deposit offerings.

- **Total Records**: 4,521 marketing contacts  
- **Conversions**: 521 successful subscriptions  
- **Conversion Rate**: **11.52%**

The goal is to optimize marketing strategies to increase conversions and improve campaign ROI by focusing on key demographics, effective channels, and optimal contact timing.

---


## 📊 Section 1: Key Insights

### 1. Demographic and Behavioral Drivers
- **Age**:  
  - Clients aged **27–42** represent **55%** of total subscriptions.  
  - Highest responsiveness in **27–34** and **35–42** groups.  
  - **19–26** and **67+** groups show low conversion rates.

- **Profession**:  
  - **White-collar workers** have the highest conversion rates.  
    - Management: **131** subscriptions  
    - Technicians: **83**  
    - Blue-collar: **69**

- **Education** (Conversion Rates):  
  - Tertiary: **14%**  
  - Secondary: **11%**  
  - Primary: **9%**

- **Marital Status**:  
  - **Married clients** more likely to subscribe (**53%** conversion), possibly due to financial stability.

---

### 2. Contact Channel and Timing Performance
- **Channel**:  
  - **Mobile phone calls** (cellular) are most effective — **80%** of total conversions.  
  - Landline: only **8%**.

- **Timing**:  
  - **Peak Months**: April, July, March, June, August  
  - **Low Months**: December, January  
  - **Best Quarter**: Q2 (April–June)  
  - **Weaker Quarters**: Q3 and Q4–Q1

- **Call Duration**:  
  - Most effective: **3–9 minutes**  
  - Under 3 minutes: often rejected  
  - Over 15 minutes: diminishing returns

---

### 3. Call Frequency and Campaign History
- **Contact Frequency**:  
  - **1–10 contacts** → highest conversions (**516**)  
  - **>11 contacts** → diminishing returns

- **Previous Campaigns**:  
  - **Previous Failures**: Little predictive value  
  - **Previous Successes**: Low re-subscription likelihood  
  - **Unknown History**: 82% — high untapped potential

---

### 4. Resistance Factors
- **Loan Status**: Clients with **existing loans** are more likely to convert.

- **Housing Loans**:  
  - Lower conversion rates — likely due to financial constraints.

- **Default History**:  
  - Mixed results; re-engagement strategies may help.

- **Balance Insights**:
  - **€1K–€5K**: Highest conversion rate at **15.9%** — ideal target group.
  - **< €1K**: Lowest rate (**9.9%**) but largest subscriber base.
  - **> €10K**: Only **5.4%** — may not favor fixed deposits, prefer other investments.

---

## Section 2: Strategic Recommendations

### A. Precision Targeting
- **Primary Focus**:
  - Individuals aged **27–42**
  - Tertiary education
  - Strong job roles
  - **€5K+ balances**
  - Married with loan relationships

- **Secondary Segments**:
  - Divorced individuals  
  - Ages **43–50** with high balances

---

### B. Contact Strategy Optimization
- **Channel**:  
  - Prioritize **mobile outreach** (cellular)  
  - Support with **SMS** and **mobile app** messaging

- **Timing**:  
  - Focus **March–July** (60% of budget)  
  - Use **August–February** for nurturing

- **Frequency**:  
  - Max **3 contact attempts** per client/month  
  - Optimal **call duration**: 6–12 minutes

---

### C. Overcoming Resistance
- **Clients with Housing Loans**:  
  - Promote **flexible deposit options**  
  - Highlight **liquidity and access**

- **Previous Campaign Failures**:  
  - Apply a **cool-off period**  
  - Use **new messaging angles**

---

### D. Balance-Specific Strategies
- **€1K–€5K Clients**:  
  - Highest conversion rate  
  - Target with **personalized**, **low-risk** deposit options

- **< €1K Clients**:  
  - Largest base  
  - Offer **micro-deposit plans** + **financial education**

- **> €10K Clients**:  
  - Low engagement  
  - Introduce **premium offerings** or **custom financial services**

- **€5K–€10K Clients**:  
  - Moderate results  
  - Use **bonuses** and **upgraded deposit plans**
hnicians (83), Blue-collar (69)
- **Education**:  
  - Tertiary: 14%  
  - Secondary: 11%  
  - Primary: 9%
- **Marital Status**:  
  - Married individuals convert more (53%) due to financial stability.

  - Cellular = 80% of conversions  
  - Landline = 8% of conversions
- **Timing**:  
  - **Peak Months**: April, July, March, June, August  
  - **Low Activity**: December, January  
  - **Best Quarter**: Q2 (April–June)
- **Call Duration**:  
  - 3–9 minutes = Optimal  
  - <3 mins = Likely rejection  
  - >15 mins = Diminishing returns

---


### D. ROI Enhancement Initiatives
| Phase        | Actions                                                                 | Expected Outcome                          |
|--------------|-------------------------------------------------------------------------|--------------------------------------------|
| Short-Term   | Demographic filters, contact caps, budget reallocation                  | +35-50% conversions, -25% CPA              |
| Mid-Term     | Predictive lead scoring, mobile-first onboarding                        | +60-80% lead accuracy                      |
| Long-Term    | Tiered segmentation, quarterly budget planning                          | Sustained growth, +120% ROI improvement    |

---

## Implementation Timeline

| Month Range | Milestone                                                                 |
|-------------|---------------------------------------------------------------------------|
| 1–2         | Launch demographic targeting and contact controls                         |
| 3–4         | Restructure campaign calendar, adopt mobile-first strategies              |
| 5–6         | Develop and test lead-scoring models                                      |
| 7–12        | Execute full-scale optimizations, review performance regularly            |

---

## Expected Business Impact

| Metric                      | Conservative Estimate | Optimized Potential      |
|----------------------------|-----------------------|--------------------------|
| Conversion Rate Increase   | 35–45%                | 60–80%                   |
| CPA Reduction              | 25–35%                | 30–50%                   |
| ROI Improvement            | 50–70%                | 80–120%                  |
| Lead Qualification Accuracy| +60%                  | Up to 2× improvement     |

---

## Conclusion
This project delivers actionable insights into customer behavior and marketing performance. By implementing the outlined data-driven strategies, the bank can:

- Significantly improve targeting
- Boost conversion rates
- Lower acquisition costs
- Maximize ROI

This marks a strategic shift toward a more personalized, efficient, and profitable marketing engine.

---

## Author

**Amankwe Amarachi Francisca**  
_Data Analyst | Internpulse Project_

