# 📊 Marketing Campaign Performance Analytics

## 📌 Project Overview

**Marketing Campaign Performance Analytics** is a Power BI data analytics project designed to evaluate the performance of marketing campaigns using key business and marketing metrics.

The project analyzes campaign data to understand **ROI, conversion rate, acquisition cost, customer engagement, clicks, impressions, campaign channels, target audiences, locations, and customer segments**.

The goal is to transform raw marketing data into an **interactive Power BI dashboard** that helps businesses identify successful campaigns, understand customer behavior, compare marketing channels, and make data-driven marketing decisions.

---

## 🎯 Project Objectives

The main objectives of this project are:

* Analyze overall marketing campaign performance.
* Measure **Return on Investment (ROI)**.
* Analyze **Conversion Rate** across different campaigns.
* Compare marketing campaign types.
* Evaluate the performance of different marketing channels.
* Analyze customer engagement.
* Understand the relationship between clicks and impressions.
* Compare acquisition costs across campaigns.
* Identify high-performing target audiences.
* Analyze campaign performance across different locations.
* Compare customer segments.
* Provide interactive visual insights using Power BI.

---

## 📂 Dataset Information

The project uses a marketing campaign dataset containing:

* **200,000 records**
* **16 attributes**
* Campaign data covering **365 days**
* Multiple companies, campaign types, channels, locations, languages, and customer segments.

### Dataset Columns

| Column             | Description                                    |
| ------------------ | ---------------------------------------------- |
| `Campaign_ID`      | Unique identification number for each campaign |
| `Company`          | Company running the campaign                   |
| `Campaign_Type`    | Type of marketing campaign                     |
| `Target_Audience`  | Audience targeted by the campaign              |
| `Duration`         | Campaign duration                              |
| `Channel_Used`     | Marketing channel used                         |
| `Conversion_Rate`  | Percentage/rate of users converted             |
| `Acquisition_Cost` | Cost required to acquire customers             |
| `ROI`              | Return on Investment                           |
| `Location`         | Campaign location                              |
| `Language`         | Language used for the campaign                 |
| `Clicks`           | Number of clicks received                      |
| `Impressions`      | Number of times the campaign was displayed     |
| `Engagement_Score` | Engagement level of the campaign               |
| `Customer_Segment` | Target customer segment                        |
| `Date`             | Campaign date                                  |

---

## 📈 Key Performance Indicators

The dashboard focuses on important marketing KPIs such as:

### Total Campaigns

**200,000**

### Average Conversion Rate

Approximately **8.01%**

### Average ROI

Approximately **5.00**

### Total Clicks

Approximately **109.95 Million**

### Total Impressions

Approximately **1.10 Billion**

### Average Engagement Score

Approximately **5.49 / 10**

### Total Acquisition Cost

Approximately **$2.50 Billion**

### Average Acquisition Cost

Approximately **$12,504**

### Overall Click-Through Rate

Approximately **9.98%**

> These values are calculated from the provided dataset and may vary slightly depending on Power BI measures, filters, and rounding.

---

## 📊 Power BI Dashboard

The Power BI dashboard provides an interactive view of marketing campaign performance.

### Dashboard Features

The dashboard can be used to analyze:

* Overall campaign performance
* Campaign ROI
* Conversion performance
* Marketing channel performance
* Campaign type performance
* Customer segment performance
* Target audience performance
* Geographic performance
* Acquisition cost
* Engagement
* Clicks and impressions
* Performance trends over time

---

## 📌 Key Analysis Areas

### 1. Campaign Type Analysis

The dataset contains five major campaign types:

* Email
* Influencer
* Display
* Search
* Social Media

This allows businesses to compare which campaign types generate better ROI, engagement, and conversions.

---

### 2. Marketing Channel Analysis

The project analyzes six marketing channels:

* Google Ads
* YouTube
* Instagram
* Website
* Facebook
* Email

Channel-level analysis helps identify which platforms provide better customer engagement and campaign performance.

---

### 3. Customer Segment Analysis

The project contains five customer segments:

* Health & Wellness
* Fashionistas
* Outdoor Adventurers
* Foodies
* Tech Enthusiasts

This analysis helps identify which customer groups respond better to marketing campaigns.

---

### 4. Target Audience Analysis

The campaigns target different audience groups including:

* Men 18–24
* Men 25–34
* Women 25–34
* Women 35–44
* All Ages

Comparing these groups helps marketers understand audience-specific campaign performance.

---

### 5. Geographic Analysis

Campaign performance can be analyzed across:

* Chicago
* New York
* Los Angeles
* Miami
* Houston

This provides insight into geographical differences in marketing performance.

---

### 6. ROI Analysis

**Return on Investment (ROI)** is one of the major performance indicators in this project.

ROI analysis helps determine which campaigns provide better returns relative to their marketing investment.

Higher ROI can indicate a more effective use of marketing resources.

---

### 7. Conversion Rate Analysis

Conversion Rate measures how effectively campaigns turn users into desired customers or actions.

The dashboard allows conversion rates to be compared across:

* Campaign types
* Channels
* Locations
* Customer segments
* Target audiences

---

### 8. Engagement Analysis

The `Engagement_Score` provides an indication of how users interact with campaigns.

The dashboard can be used to identify campaigns with:

* High engagement
* Medium engagement
* Low engagement

This can help marketers understand which campaigns attract stronger customer interaction.

---

## 🔄 Project Workflow

```text
Raw Marketing Dataset
        ↓
Data Loading
        ↓
Data Cleaning & Transformation
        ↓
Data Analysis
        ↓
Power BI Data Modeling
        ↓
KPI & Measure Creation
        ↓
Interactive Visualizations
        ↓
Marketing Performance Insights
        ↓
Data-Driven Decisions
```

---

## 🧹 Data Preparation

Before visualization, the dataset can be prepared for analysis by:

* Checking missing values
* Checking duplicate records
* Converting date fields into proper date format
* Converting acquisition cost from text/currency format into numeric values
* Checking data types
* Validating numerical fields
* Creating calculated measures
* Creating appropriate relationships and filters in Power BI

### Important Transformation

The `Acquisition_Cost` column is stored as a currency-formatted text field, for example:

```text
$16,174.00
```

For numerical analysis, it can be converted into:

```text
16174.00
```

This allows acquisition cost to be used in calculations and visualizations.

---

## 📊 Suggested Visualizations

The Power BI dashboard uses/Can include different visualizations such as:

### KPI Cards

Used to display:

* Total Campaigns
* Average ROI
* Average Conversion Rate
* Total Clicks
* Total Impressions
* Average Engagement

### Bar Charts

Useful for comparing:

* ROI by campaign type
* Conversion rate by channel
* Acquisition cost by company
* Engagement by customer segment

### Column Charts

Useful for:

* Campaign performance
* Target audience comparison
* Location comparison

### Line Charts

Useful for:

* Campaign performance over time
* ROI trends
* Conversion trends

### Donut/Pie Charts

Useful for showing:

* Campaign type distribution
* Channel distribution
* Customer segment distribution

### Slicers

Interactive filters can be provided for:

* Company
* Campaign Type
* Channel
* Location
* Target Audience
* Customer Segment
* Date

---

## 💡 Business Insights

The project helps answer important marketing questions such as:

1. Which campaign types generate the highest ROI?
2. Which marketing channels provide better engagement?
3. Which customer segments respond better to campaigns?
4. Which target audience has the highest conversion rate?
5. Which locations generate better campaign performance?
6. How much is being spent on customer acquisition?
7. How effective are campaigns at converting users?
8. Which campaigns receive the most clicks?
9. What is the relationship between impressions and clicks?
10. Which areas require improvement in marketing strategy?

---

## 🛠️ Tools & Technologies

### Power BI

Used for:

* Data transformation
* Data modeling
* DAX calculations
* KPI creation
* Interactive dashboards
* Data visualization
* Business intelligence analysis

### Dataset

The project uses a CSV-based marketing campaign dataset containing **200,000 records**.

---

## 📁 Project Structure

```text
Marketing-Campaign-Analytics/
│
├── README.md
│
├── marketing_campaign_dataset.csv
│
├── Marketing_Campaign.pbix
│
└── screenshots/
    └── marketing_campaign_dashboard.png
```

> If the CSV is too large for GitHub, consider using Git LFS or provide the dataset separately.

---

## 🚀 How to Use the Project

### Step 1: Download the Repository

Clone the repository:

```bash
git clone <your-repository-url>
```

### Step 2: Open the Power BI File

Open:

```text
Marketing_Campaign.pbix
```

using **Microsoft Power BI Desktop**.

### Step 3: Check the Dataset

Make sure the dataset path is correctly configured in Power BI.

### Step 4: Interact With the Dashboard

Use the available:

* Filters
* Slicers
* Charts
* KPI cards
* Tables

to explore campaign performance.

---

## 📌 Example Business Scenario

Imagine a company is running thousands of marketing campaigns across multiple platforms.

Simply looking at the amount of data is not enough.

The company needs to understand:

```text
Which campaign works?
        ↓
Which channel works?
        ↓
Which customers respond?
        ↓
How much does acquisition cost?
        ↓
What is the ROI?
        ↓
Where should the company invest more?
```

This Power BI project converts the raw campaign data into meaningful business insights that can support these decisions.

---

## 🎓 Learning Outcomes

Through this project, the following skills are demonstrated:

* Data analysis
* Data cleaning
* Business intelligence
* Power BI dashboard development
* Data visualization
* KPI development
* Marketing analytics
* Customer segmentation
* Performance analysis
* Business decision-making
* Interactive reporting

---

## 🔮 Future Enhancements

The project can be further improved by adding:

* Predictive campaign performance
* Customer conversion prediction
* Machine learning models
* Campaign recommendation system
* Customer lifetime value analysis
* Automated data refresh
* Advanced DAX measures
* Time-series forecasting
* Campaign profitability analysis
* Real-time marketing dashboards

---

## 👨‍💻 Project Author

**Prajwal L P**

### Project Type

**Business Intelligence / Data Analytics Project**

### Domain

**Marketing Analytics**

### Tool

**Microsoft Power BI**

---

## ⭐ Conclusion

The **Marketing Campaign Performance Analytics** project demonstrates how large-scale marketing data can be transformed into meaningful and actionable business insights.

By analyzing **ROI, conversion rate, acquisition cost, engagement, clicks, impressions, campaign types, channels, customer segments, audiences, and locations**, businesses can better understand their marketing performance and make more informed decisions.

The project showcases the practical application of **Power BI and data analytics in marketing**, turning raw data into an interactive decision-support dashboard.
