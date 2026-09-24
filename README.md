# Customer Churn Analysis 
An end-to-end **Data Analytics with AI** project developed as part of the **IBM SkillsBuild Data Analytics with AI Internship 2026**, offered in collaboration with **AICTE and BharatCares**.

The project analyzes customer churn, subscription behavior, customer support interactions, retention, revenue impact, and customer risk using **SQL and Python**.

---

## Program

**IBM SkillsBuild Data Analytics with AI Internship 2026**
**Offered in collaboration with:** AICTE & BharatCares
**Duration:** 17 August 2026 – 30 September 2026
**Mode:** Virtual

The internship includes training in data analytics, data cleaning, exploratory data analysis, predictive analytics, machine learning fundamentals, visualization, and AI-driven insights, along with a final project submission.

---

## Project Overview

Customer churn analysis focuses on understanding three key questions:

* **Who** is leaving?
* **Why** are customers leaving?
* **When** is churn happening?

This project integrates customer, subscription, and support data to identify churn patterns and quantify their potential business impact.

The overall workflow is:

```text
SQLite Database
      ↓
SQL Data Extraction
      ↓
Data Cleaning
      ↓
Data Integration
      ↓
Feature Engineering
      ↓
Exploratory Data Analysis
      ↓
Data Visualization
      ↓
Business Insights
      ↓
Recommendations
```

---

## Objectives

* Calculate overall churn and retention rates.
* Analyze churn across subscription plans.
* Compare monthly and annual contract churn.
* Identify geographic churn patterns.
* Identify periods with higher churn.
* Analyze customer tenure and ARPU.
* Quantify revenue loss and CLTV impact.
* Analyze customer complaints and support escalations.
* Examine customer churn-risk indicators.
* Convert analytical findings into actionable business insights.

---

## Tech Stack

* **Python**
* **SQL**
* **SQLite**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

---

## Dataset Structure

The project uses three relational datasets connected through `customerid`.

### Customer

Contains:

* Customer ID
* Name
* Country
* State
* Gender
* Date of Birth
* Interests
* Pincode

### Subscription

Contains:

* Customer ID
* Subscription Start Date
* Subscription Type
* Renewal Date
* Plan Type
* Contract Type
* Cancellation Date
* Cancellation Reason
* Monthly Charges
* CLTV
* Churn Score

### Support

Contains:

* Customer ID
* Complaint Date
* Escalations
* CSAT Score
* Comments

---

## Key Analysis

### Overall Churn & Retention

The analysis identified:

| Metric         |    Result |
| -------------- | --------: |
| Churn Rate     | **28.6%** |
| Retention Rate | **71.4%** |

Approximately 28.6% of customers in the analyzed dataset were identified as churned.

---

### Churn by Subscription Plan

The **Basic plan recorded the highest churn** among the analyzed subscription plans.

This makes the Basic segment an important area for further investigation into pricing, plan changes, customer experience, and service expectations.

---

### Monthly vs Annual Contracts

One of the strongest patterns identified in the analysis was the difference between monthly and annual contracts:

| Contract Type | Churn Rate |
| ------------- | ---------: |
| Monthly       |  **55.6%** |
| Annual        |   **8.3%** |

The monthly-contract churn rate was approximately **6.7× higher** than the annual-contract churn rate in the analyzed dataset.

This indicates a strong association between contract structure and observed churn.

---

### Geographic Churn

**Karnataka** was identified as the most affected state in the analyzed dataset.

Possible contributing factors should be investigated further rather than assumed. Areas for investigation include:

* Customer complaints
* Pricing changes
* Technical issues
* Service experience
* Competitive activity

---

### Churn Over Time

The highest churn was observed in **September 2024**.

This period should therefore be examined for changes in:

* Subscription pricing
* Product or service experience
* Customer support
* Plan structure
* Competitive conditions

---

## Revenue & Customer Value Insights

The analysis produced the following metrics:

| Metric                    |         Result |
| ------------------------- | -------------: |
| Average Customer Tenure   | **1,451 days** |
| ARPU                      |      **₹18.8** |
| Total Revenue             |        **395** |
| Revenue Loss Due to Churn |         **74** |
| CLTV Lost                 |      **2,047** |
| Percentage Revenue Loss   |        **18%** |

These results demonstrate that churn has an impact beyond customer count, affecting revenue and customer lifetime value.

---

## Customer Support & Churn

Customer support information was integrated with subscription and churn data to examine whether support interactions were associated with churn.

The analysis considers:

* Complaints
* Escalations
* CSAT
* Churn status

Support escalation is treated as a **risk signal**, and any observed relationship should be interpreted as an association rather than proof that support issues directly caused churn.

---

## Churn Risk Analysis

Customer risk was examined using available subscription, tenure, support, and churn-score information.

Higher-risk customers can be investigated using:

* Churn score
* Customer lifetime value
* Contract type
* Subscription plan
* Complaint history
* Escalation history
* Customer tenure

This provides a way to move from simply describing churn to identifying customers who may require additional analysis.

---

## Key Findings

### Finding 1 — Overall Churn

**28.6% churn** was observed, with **71.4% retention**.

### Finding 2 — Contract Structure

Monthly contracts showed **55.6% churn**, compared with **8.3% for annual contracts**.

### Finding 3 — Subscription Plan

The **Basic plan** recorded the highest churn in the analyzed dataset.

### Finding 4 — Geography

**Karnataka** showed the highest observed churn among the analyzed states.

### Finding 5 — Time

**September 2024** recorded the highest observed churn.

### Finding 6 — Financial Impact

The analysis identified **74 in revenue loss due to churn** and **2,047 in CLTV lost**, with an overall reported revenue-loss percentage of **18%**.

---

## Recommended Areas for Further Investigation

Based on the observed patterns:

1. Investigate the reasons behind higher churn in Karnataka.
2. Review changes affecting Basic-plan customers.
3. Examine events and business changes around September 2024.
4. Investigate why monthly-contract customers show substantially higher churn.
5. Analyze higher-risk customers using churn score, LTV, complaints, and escalation history.
6. Examine cancellation reasons to understand the underlying drivers of churn.

These are investigation areas derived from the observed patterns; they are not presented as confirmed causal explanations.

---

## Project Structure

```text
Customer-Churn-Analysis/
│
├── README.md
├── requirements.txt
│
├── notebooks/
│   └── customer_churn_analysis.ipynb
│
├── data/
│   ├── customer_churn.db
│   └── churn_data.csv
│
├── outputs/
│   ├── churn_by_plan.png
│   ├── churn_by_contract.png
│   ├── churn_by_state.png
│   ├── churn_trend.png
│   └── ...
│
└── reports/
    └── Customer_Churn_Analysis_Report.pdf
```

---

## How to Run

### Clone the repository

```bash
git clone https://github.com/your-username/Customer-Churn-Analysis.git
cd Customer-Churn-Analysis
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/customer_churn_analysis.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

---

## Learning Outcomes

This project provided practical experience in:

* SQL database querying
* Relational data integration
* Python data analysis
* Data cleaning
* Feature engineering
* Exploratory Data Analysis
* Data visualization
* KPI calculation
* Customer churn analysis
* Revenue and CLTV analysis
* Risk analysis
* Business insight generation

These areas correspond closely with the internship's project structure, which includes data cleaning, EDA, predictive analytics, machine learning fundamentals, visualization, AI-driven insights, and final project development.

---

## Disclaimer

This project was developed as part of the **IBM SkillsBuild Data Analytics with AI Internship 2026**, offered in collaboration with **AICTE and BharatCares**, for educational and project-submission purposes.

The findings presented in this repository are based on the dataset analyzed in this project. Observed relationships and patterns should not automatically be interpreted as causal relationships or generalized to other customer populations.

## Acknowledgement

I would like to acknowledge **AICTE, BharatCares, and IBM SkillsBuild** for providing the internship learning environment, mentorship, masterclasses, and project-based learning opportunities.

## Contact

**Bobby**
AI/ML Engineer
Rajasthan, India

* **GitHub:** [github.com/Bobby-balyan](https://github.com/Bobby-balyan)
* **LinkedIn:** [linkedin.com/in/bobbybalyan](https://www.linkedin.com/in/bobbybalyan)
* **Portfolio:** [bobbybalyan.vercel.app](https://bobbybalyan.vercel.app)

For questions, feedback, or collaboration, feel free to connect with me through LinkedIn or GitHub.

---

**Thank you for reviewing this project.**
