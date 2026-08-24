md


🏦 Banking Customer Churn & Value Analytics
📌 Project Overview
Banking Customer Churn & Value Analytics is an end-to-end Business
Intelligence project developed using Microsoft Power BI to analyze
customer churn, customer value, banking behavior, and risk.

The dashboard helps banking management understand which customers are
leaving, which customer groups are more likely to churn, and which
customers should be prioritized for retention strategies.

The project follows the complete Business Analytics workflow:

Raw Dataset → Data Transformation → Data Modeling → DAX → Power BI
Dashboard → Business Insights → Recommendations

🎯 Business Problem
Banks collect large amounts of customer information, but raw customer
data alone does not clearly show why customers leave or which customers
are most valuable.

The objective of this project is to build an interactive analytics
solution that helps the bank:

Monitor customer churn.

Identify customer groups with higher churn rates.

Analyze customer activity and banking behavior.

Understand the relationship between credit score, tenure, balance,
and churn.

Identify high-value customers.

Identify customers who may require retention efforts.

Support data-driven business decisions.

🎯 Project Objectives
Analyze customer churn using banking customer data.

Calculate important customer and churn KPIs.

Identify patterns in customer behavior.

Compare churn across different customer segments.

Analyze customer value using account balance and product usage.

Build an interactive Power BI dashboard.

Create DAX measures for business KPIs.

Provide actionable business recommendations.

📂 Dataset
The project uses a banking customer churn dataset containing 10,000
customer records.

Dataset columns
Column Description

CustomerId Unique customer identifier
CreditScore Customer credit score
Tenure Number of years with the bank
Balance Customer account balance
NumOfProducts Number of banking products used
HasCrCard Whether the customer has a credit card
IsActiveMember Whether the customer is an active member
Exited Customer churn indicator

Target Variable
Exited

0 → Customer retained

1 → Customer churned

Dataset statistics
Total records: 10,000

Main target: Customer churn (Exited)

Business domain: Banking / Finance

🛠️ Technologies Used
Microsoft Power BI Desktop

Power Query

DAX

Microsoft Excel

Power BI Data Modeling

Star Schema / Dimension Modeling

SQL/MySQL (optional extension)

🧹 Data Preparation
The raw dataset was prepared before dashboard development.

Data cleaning and transformation included:
Checking missing values.

Checking duplicate customer records.

Correcting data types.

Validating numeric fields.

Creating customer groups.

Creating age/tenure/value/risk categories where required.

Preparing fields for Power BI visualization.

Creating dimension tables for attributes such as gender, geography,
activity, credit card status, and exit status.

Power Query was used for transformation and preparation before loading
the data into the Power BI model.

🏗️ Data Model
The Power BI model contains the main customer churn fact/data table and
supporting dimension tables.

Main tables
Bank_Churn

CustomerInfo

Gender

Geography

CreditCard

ActiveCustomer

ExitCustomer

All Measures

Example model structure
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
The model uses relationships between customer attributes and the main
banking churn data to allow interactive filtering across the dashboard.

📐 Important DAX Measures
Some of the major measures used in the project include:

Total Customers
Total Customers =
DISTINCTCOUNT(Bank_Churn[CustomerId])
Active Customers
Active Customers =
CALCULATE(
    [Total Customers],
    Bank_Churn[IsActiveMember] = 1
)
Churn Rate
Churn Rate =
DIVIDE(
    CALCULATE(
        [Total Customers],
        Bank_Churn[Exited] = 1
    ),
    [Total Customers],
    0
)
Average Balance
Avg Balance =
AVERAGE(Bank_Churn[Balance])
Average Products
Avg Products =
AVERAGE(Bank_Churn[NumOfProducts])
Average Tenure
Avg Tenure =
AVERAGE(Bank_Churn[Tenure])
Additional measures were created for customer ranking, churn risk, early
churn, customer segmentation, and comparative analysis.

📊 Dashboard Pages
1. Executive Overview
The executive dashboard provides a high-level view of the bank's
customer base.

KPIs
Total Customers

Average Balance

Average Products

Average Tenure

Churn Rate

Visualizations
Total Customers by Number of Products

Total and Exited Customers by Region

Exited Customers by Salary Bracket

Churn Rate by Tenure

Churn Rate by Credit Score

Customer Segmentation

Customer joined by year

Churn rate by year

2. Churn Analysis
This page focuses on understanding customer churn patterns.

Analysis areas
Churn by tenure

Churn by credit score

Churn by gender

Churn by product usage

Churn by credit card ownership

Churn by customer category

Churn by year

Key purpose
To identify customer groups that show higher churn and require further
investigation.

3. Customer Value Analysis
This page analyzes the financial value and behavior of customers.

Analysis areas
Average balance by geography

Average balance by number of products

Customer value segmentation

Customer balance distribution

High-value customers

Average salary

Product usage

Customer segments
Customers can be grouped into:

High Value

Medium Value

Low Value

This helps management prioritize valuable customers for retention
activities.

4. Churn Risk Analysis
This page focuses on identifying customers and segments with higher
churn risk.

Risk analysis
High-risk customers

Medium-risk customers

Low-risk customers

Risk by geography

Risk by tenure

Risk by credit score

Risk by customer activity

Risk by number of products

The purpose is to help the bank focus retention resources on customers
who need the most attention.

5. What-If Analysis & Recommendations
The project can include a retention scenario using a What-If
parameter.

For example:

Retention Campaign
5% → 10% → 15% → 20% → 25% → 30%
Management can change the retention percentage and estimate the
potential number of customers retained.

This demonstrates how Power BI can be used not only to analyze
historical data but also to support business planning.

❓ Business Questions
The dashboard is designed to answer the following business questions:

What is the overall customer churn rate?

How many customers have exited the bank?

Which regions have the highest number of churned customers?

Which customer groups have the highest churn rate?

Does customer tenure affect churn?

Does credit score influence customer churn?

Does the number of banking products affect churn?

Are inactive customers more likely to churn?

Which customer segments have the highest value?

Which customers or segments should the bank prioritize for
retention?

💡 Key Business Insights
The dashboard can help management identify insights such as:

Customer Churn
A significant portion of the customer base may be at risk of leaving,
making customer retention an important business priority.

Geography
Churn differs across geographic regions, allowing the bank to
investigate regional customer experience and service factors.

Customer Activity
Inactive customers generally require closer monitoring because reduced
engagement can be associated with higher churn.

Tenure
Customers at different stages of their relationship with the bank can
show different churn patterns. Early-tenure customers can be monitored
more closely.

Credit Score
Customers with different credit-score segments can display different
churn behavior, helping the bank identify customer groups that need
additional analysis.

Product Usage
The number of products used by a customer can be compared with churn to
identify opportunities for stronger customer engagement.

📈 Business Recommendations
Based on the dashboard analysis, the bank can consider the following
strategies:

Prioritize high-risk customers for retention campaigns.

Improve engagement with inactive customers through personalized
communication.

Monitor new customers closely during the early stage of their
relationship.

Promote suitable banking products to increase customer
engagement.

Develop personalized retention offers for high-value customers.

Investigate regions with higher churn and identify local service
issues.

Use customer segmentation to avoid applying the same retention
strategy to every customer.

Continuously monitor churn KPIs through Power BI.

📌 Dashboard Filters
The dashboard provides interactive filters/slicers such as:

Gender

Region / Geography

Age Group

Tenure Group

Active Member

Credit Card

Number of Products

Customer Value Segment

Churn / Exit Category

These filters allow users to drill down into specific customer groups.

🔄 End-to-End Workflow
                 RAW BANKING DATA
                        ↓
                 Excel / CSV Dataset
                        ↓
                  Data Cleaning
                        ↓
                  Power Query
                        ↓
                 Data Transformation
                        ↓
                   Data Model
                        ↓
                 Relationships
                        ↓
                    DAX KPIs
                        ↓
              Interactive Power BI
                   Dashboard
                        ↓
             Churn & Value Analysis
                        ↓
              Business Questions
                        ↓
                 Insights
                        ↓
              Recommendations
                        ↓
             Business Decisions
🚀 Future Enhancements
The project can be extended with:

MySQL database connectivity.

SQL views for data preparation.

Power BI Service deployment.

Scheduled data refresh.

Row-Level Security (RLS).

Advanced customer churn prediction using Machine Learning.

Automated data pipeline.

API-based data integration.

Customer lifetime value prediction.

Advanced churn-risk scoring.

Incremental refresh for larger datasets.

📁 Suggested Project Repository Structure
Banking-Customer-Churn-Analytics/
│
├── Dataset/
│   └── Bank_Churn.xlsx
│
├── PowerBI/
│   └── Banking_Customer_Churn.pbix
│
├── SQL/
│   ├── database.sql
│   ├── tables.sql
│   └── analysis_queries.sql
│
├── Screenshots/
│   ├── Executive_Overview.png
│   ├── Churn_Analysis.png
│   ├── Customer_Value.png
│   └── Churn_Risk.png
│
├── Documentation/
│   └── Project_Report.pdf
│
└── README.md
👨‍💻 Project Summary
Banking Customer Churn & Value Analytics demonstrates how Business
Intelligence can transform raw banking customer data into actionable
information.

The project combines data preparation, data modeling, DAX, interactive
visualization, customer segmentation, churn analysis, and business
recommendations to help banking management understand customer
behavior and make informed retention decisions.

Project Goal
Identify customer churn patterns, understand customer value, and
help the bank make data-driven decisions to improve customer retention
and maximize customer value.


