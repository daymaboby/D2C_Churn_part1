# Customer Churn Analysis Using Behavioral Data

## Project Overview
This project analyzes customer behavior to understand the key drivers of customer churn. The goal is to identify patterns in purchasing behavior, engagement, support interactions, refunds, and campaign exposure that indicate churn risk.

The analysis is based on real customer-level datasets and focuses on behavioral signals rather than assumptions.

---

## Objective
To explore customer data and identify:
- Behavioral patterns linked to churn
- High-risk customer segments
- Engagement and dissatisfaction signals
- Revenue concentration risks

---

## Datasets Used

- **Customers**: Demographics and profile information
- **Orders**: Purchase history, frequency, and spending behavior
- **Support Tickets**: Customer service interactions
- **Web/App Events**: User engagement activity
- **Campaigns**: Marketing exposure history
- **Churn Labels**: Target variable (churn_next_60d)

---

## Analysis Workflow

1. Data loading and merging of multiple datasets
2. Data quality checks (missing values, duplicates, skewness)
3. Exploratory Data Analysis (EDA):
   - Customer demographics analysis
   - Order frequency and spending behavior
   - Refund behavior analysis
   - Support ticket patterns
   - Web/app engagement analysis
   - Campaign exposure distribution
   - Churn distribution analysis
4. Identification of churn-risk patterns
5. Business interpretation of findings

---

## Key Insights

- Most customers place a low number of orders, indicating weak engagement.
- Revenue is highly concentrated among a small group of high-value customers.
- Low engagement in web/app activity is strongly associated with potential churn.
- Customers with high support ticket counts show signs of dissatisfaction.
- Refund-heavy customers are more likely to be at churn risk.
- Campaign exposure is uneven and does not guarantee engagement.
- Churn is a minority class, requiring careful modeling approaches.

---

## Files in This Repository

- `eda_audit.ipynb` → Full exploratory data analysis with charts and insights
- `data_quality_report.md` → Data quality issues and their impact on modeling
- `business_memo.md` → Business-focused churn insights and recommendations
- `requirements.txt` → Python dependencies for reproducibility

---

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Conclusion
This project shows that churn is primarily driven by behavioral signals such as low engagement, low purchase frequency, support issues, and refund behavior. The findings can be used to design targeted retention strategies instead of generic marketing campaigns.initial commit
