# 🏦 Banking Customer Churn & Value Analytics

## 📌 Project Overview

**Banking Customer Churn & Value Analytics** is an end-to-end Business Intelligence project developed using **Microsoft Power BI** to analyze customer churn, customer value, banking behavior, and churn risk.

The dashboard helps banking management understand **which customers are leaving, which customer groups have higher churn, and which customers should be prioritized for retention strategies**.

The project follows the complete Business Analytics workflow:

**Raw Dataset → Data Cleaning → Data Transformation → Data Modeling → DAX → Power BI Dashboard → Business Insights → Recommendations**

---

## 🎯 Business Problem

Banks collect large amounts of customer data, but raw data does not clearly show why customers leave or which customers are most valuable.

The objective of this project is to develop an interactive analytics solution that helps the bank:

* Monitor customer churn.
* Identify customer groups with high churn rates.
* Analyze customer activity and banking behavior.
* Understand the relationship between credit score, tenure, balance, and churn.
* Identify high-value customers.
* Identify customers requiring retention efforts.
* Support data-driven business decisions.

---

## 🎯 Project Objectives

1. Analyze customer churn using banking customer data.
2. Calculate important customer and churn KPIs.
3. Identify patterns in customer behavior.
4. Compare churn across different customer segments.
5. Analyze customer value using account balance and product usage.
6. Build an interactive Power BI dashboard.
7. Create meaningful DAX measures.
8. Provide actionable business recommendations.

---

## 📂 Dataset

The project uses a **Bank Customer Churn dataset containing 10,000 customer records**.
### Target Variable

`Exited`

* `0` → Customer retained
* `1` → Customer churned

### Dataset Information

* **Total Records:** 10,000
* **Business Domain:** Banking / Finance
* **Main Analysis:** Customer Churn and Customer Value

---

## 🛠️ Technologies Used

* **Microsoft Power BI Desktop**
* **Power Query**
* **DAX**
* **Microsoft Excel**
* **Power BI Data Modeling**
* **SQL/MySQL** *(optional extension)*

---

## 🧹 Data Cleaning & Transformation

The dataset was prepared before developing the Power BI dashboard.

The data preparation process included:

* Checking missing values.
* Checking duplicate records.
* Correcting data types.
* Validating numerical columns.
* Creating customer categories.
* Creating age groups.
* Creating tenure groups.
* Creating credit score segments.
* Creating customer value segments.
* Creating churn risk categories.
* Preparing data for Power BI visualization.

**Power Query** was used for data cleaning and transformation.

---

## 🏗️ Data Model

The Power BI model contains the main banking churn table and supporting dimension tables.

### Main Tables

* `Bank_Churn`
* `CustomerInfo`
* `Gender`
* `Geography`
* `CreditCard`
* `ActiveCustomer`
* `ExitCustomer`
* `All Measures`

### Model Structure

```text
                     Gender
                       |
                       |
CustomerInfo ---- Bank_Churn ---- Geography
                       |
             -----------------------
             |          |          |
        CreditCard  ActiveCustomer ExitCustomer
                       |
                  All Measures
```

Relationships between these tables allow interactive filtering and analysis across the dashboard.

---

# 📐 DAX Measures

### Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(Bank_Churn[CustomerId])
```

### Active Customers

```DAX
Active Customers =
CALCULATE(
    [Total Customers],
    Bank_Churn[IsActiveMember] = 1
)
```

### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    CALCULATE(
        [Total Customers],
        Bank_Churn[Exited] = 1
    ),
    [Total Customers],
    0
)
```

### Average Balance

```DAX
Avg Balance =
AVERAGE(Bank_Churn[Balance])
```

### Average Products

```DAX
Avg Products =
AVERAGE(Bank_Churn[NumOfProducts])
```

### Average Tenure

```DAX
Avg Tenure =
AVERAGE(Bank_Churn[Tenure])
```

Additional DAX measures were created for customer ranking, churn risk, customer segmentation, and comparative analysis.

---

# 📊 Dashboard Pages

## 1. Executive Overview

This page provides management with a quick overview of the customer base.

### KPIs

* Total Customers
* Average Balance
* Average Products
* Average Tenure
* Churn Rate

### Visualizations

* Total Customers by Number of Products
* Total and Exited Customers by Region
* Exited Customers by Salary Bracket
* Churn Rate by Tenure
* Churn Rate by Credit Score
* Customer Segmentation
* Customer Joined by Year
* Churn Rate by Year

---

## 2. Churn Analysis

This page focuses on understanding why customers may leave the bank.

### Analysis

* Churn Rate by Tenure
* Churn Rate by Credit Score
* Churn Rate by Gender
* Churn Rate by Number of Products
* Churn Rate by Credit Card Ownership
* Churn Rate by Customer Category
* Churn Rate by Year

### Objective

To identify customer groups with higher churn and help management develop appropriate retention strategies.

---

## 3. Customer Value Analysis

This page analyzes the financial value and behavior of customers.

### Analysis

* Average Balance by Geography
* Average Balance by Number of Products
* Customer Value Segmentation
* Balance Distribution
* High-Value Customers
* Average Salary
* Product Usage

### Customer Segments

* **High Value**
* **Medium Value**
* **Low Value**

This helps the bank prioritize valuable customers.

---

## 4. Churn Risk Analysis

This page focuses on identifying customers and groups with higher churn risk.

### Analysis

* High-Risk Customers
* Medium-Risk Customers
* Low-Risk Customers
* Risk by Geography
* Risk by Tenure
* Risk by Credit Score
* Risk by Customer Activity
* Risk by Number of Products

The purpose is to help the bank focus retention efforts on customers who require the most attention.

---

## 5. What-If Analysis & Recommendations

A **What-If parameter** can be used to simulate different customer retention scenarios.

Example:

```text
Retention Campaign
5% → 10% → 15% → 20% → 25% → 30%
```

Management can select a retention percentage and estimate the potential number of customers retained.

This makes the dashboard useful for **business planning and decision-making**.

---

# ❓ Business Questions

The dashboard answers the following business questions:

1. What is the overall customer churn rate?
2. How many customers have exited the bank?
3. Which regions have the highest number of churned customers?
4. Which customer groups have the highest churn rate?
5. Does customer tenure affect churn?
6. Does credit score influence customer churn?
7. Does the number of banking products affect churn?
8. Are inactive customers more likely to churn?
9. Which customer segments have the highest value?
10. Which customer groups should the bank prioritize for retention?

---

# 💡 Business Insights

The dashboard helps management identify important patterns such as:

### Customer Churn

The bank can monitor the overall churn rate and identify whether customer retention is becoming a business concern.

### Geography

Different regions can have different churn levels. Regions with higher churn can be investigated further for customer service or engagement issues.

### Customer Activity

Inactive members can be analyzed to understand whether reduced engagement is associated with higher churn.

### Tenure

Customers at different stages of their relationship with the bank can show different churn behavior.

### Credit Score

Churn can be compared across credit score segments to identify customer groups requiring further investigation.

### Product Usage

The number of products used by a customer can be compared with churn to understand whether stronger product engagement is associated with better retention.

---

# 📈 Business Recommendations

Based on the dashboard analysis, the bank can consider the following strategies:

1. **Prioritize high-risk customers** for retention campaigns.
2. **Improve engagement with inactive customers** through personalized communication.
3. **Monitor new customers closely** during the early stage of their relationship.
4. **Promote suitable banking products** to increase customer engagement.
5. **Develop personalized retention offers** for high-value customers.
6. **Investigate regions with high churn** and identify possible service issues.
7. **Use customer segmentation** to create targeted strategies.
8. **Continuously monitor churn KPIs** through the Power BI dashboard.

---

# 🎛️ Dashboard Filters

The dashboard provides interactive filters such as:

* Gender
* Geography / Region
* Age Group
* Tenure Group
* Active Member
* Credit Card
* Number of Products
* Customer Value Segment
* Exit Category

These filters allow users to analyze specific customer groups.

---

# 🔄 End-to-End Project Workflow

```text
Raw Banking Dataset
        ↓
Data Cleaning
        ↓
Power Query
        ↓
Data Transformation
        ↓
Data Modeling
        ↓
Relationships
        ↓
DAX Measures
        ↓
Power BI Visualizations
        ↓
Interactive Dashboard
        ↓
Churn & Customer Value Analysis
        ↓
Business Questions
        ↓
Business Insights
        ↓
Recommendations
        ↓
Business Decision Making
```

---

# 🚀 Future Enhancements

The project can be further enhanced with:

* MySQL database connectivity.
* SQL queries and views.
* Power BI Service deployment.
* Scheduled data refresh.
* Row-Level Security (RLS).
* Machine Learning-based churn prediction.
* Automated data pipelines.
* API-based data integration.
* Customer Lifetime Value prediction.
* Advanced churn-risk scoring.
* Incremental refresh for larger datasets.

# 🏆 Project Outcome

The **Banking Customer Churn & Value Analytics** project transforms raw banking customer data into an interactive Business Intelligence solution.

The dashboard enables management to understand **customer churn, customer value, customer behavior, and churn risk**, allowing the bank to make more informed decisions regarding customer retention and engagement.

### Final Goal

> **Identify customer churn patterns, understand customer value, and help the bank make data-driven decisions to improve customer retention and maximize customer value.**

