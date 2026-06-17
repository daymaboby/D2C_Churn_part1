# Data Quality Report

## Overview
A data quality assessment was conducted across customers, orders, support tickets, web/app activity, campaigns, and churn datasets. The goal was to identify issues that may affect analysis reliability and churn modeling.

---

## 1. Missing Values
Some datasets contain missing or incomplete records across customer-level and transactional fields.

### Impact:
- Incomplete customer profiles may lead to biased segmentation.
- Missing behavioral data (orders, tickets, web activity) can underrepresent customer engagement.
- Models trained on incomplete data may misclassify churn risk.

---

## 2. Duplicate and Repeated Records
Customer behavior data such as orders, tickets, and events may contain repeated or duplicate-like entries due to event tracking systems.

### Impact:
- Inflation of order frequency, ticket counts, or engagement metrics.
- Overestimation of customer activity levels.
- Bias in churn-related feature creation.

---

## 3. Skewed and Extreme Distributions
Key variables such as gross_amount, order frequency, ticket counts, and web activity show strong right-skewed distributions.

### Observations:
- A small group of customers contributes disproportionately high revenue.
- Most customers show low activity across orders, tickets, and engagement.

### Impact:
- Mean-based metrics may be misleading.
- Models may become biased toward high-activity customers.

---

## 4. Join and Key Consistency Issues
All datasets rely on customer_id for merging.

### Impact:
- Missing customer_ids across datasets can result in incomplete customer profiles.
- Inconsistent joins may reduce accuracy of churn features.

---

## 5. Temporal Data Considerations
Order dates and activity timestamps require proper handling for recency-based analysis.

### Impact:
- Incorrect date handling may distort churn signals such as inactivity.
- Time-based leakage may occur if future data is used incorrectly.

---

## 6. Potential Data Leakage
Some features (especially future behavior or post-churn activity) may lead to leakage if not handled carefully.

### Risk:
- Inflated model performance during training.
- Poor real-world generalization.

---

## Conclusion
The dataset is suitable for churn analysis after preprocessing. However, skewed distributions, potential duplicates, missing values, and temporal inconsistencies must be handled carefully before modeling.