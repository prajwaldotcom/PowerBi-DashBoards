
# HR Analytics Dashboard

## Weekly Assignment 6 – Creating HR Analytics Dashboards

### 📌 Project Overview

The **HR Analytics Dashboard** is an interactive Power BI dashboard developed to analyze employee demographics, workforce distribution, employee attrition, compensation, job satisfaction, and other HR-related factors.

The dashboard helps HR teams understand workforce patterns and identify factors associated with employee attrition. It provides interactive filters and visualizations to support better workforce planning and employee management decisions.

---

## 🎯 Problem Statement

The HR department of a multinational organization wants insights into:

* Employee demographics
* Workforce distribution
* Employee attrition
* Job roles and departments
* Compensation and experience
* Employee satisfaction
* Overtime and business travel

The objective is to develop an interactive HR Analytics Dashboard that provides meaningful insights and supports HR decision-making.

---

## 📊 Dataset

**Dataset:** IBM HR Analytics Employee Attrition & Performance

**Source:** Kaggle

The dataset contains employee-level HR information such as:

* Age
* Gender
* Department
* Job Role
* Education
* Education Field
* Monthly Income
* Daily Rate
* Hourly Rate
* Job Level
* Job Satisfaction
* Work-Life Balance
* Overtime
* Business Travel
* Attrition
* Years at Company
* Total Working Years
* Years Since Last Promotion
* Distance From Home
* Performance Rating

---

## 🛠️ Tools & Technologies

* **Power BI** – Dashboard development and visualization
* **Power Query** – Data cleaning and transformation
* **DAX** – Calculated measures and KPIs
* **GitHub** – Version control and project submission

---

## 🧹 Data Cleaning & Transformation

The following preprocessing steps were performed:

1. Imported the IBM HR Analytics dataset into Power BI.
2. Checked the dataset for missing values and duplicate records.
3. Reviewed and corrected data types where required.
4. Removed unnecessary columns such as `EmployeeCount`, `EmployeeNumber`, `Over18`, and `StandardHours` where they were not required for analysis.
5. Created calculated measures for employee count, employees who left, and attrition rate.
6. Used appropriate aggregations such as Count and Average for HR metrics.

---

## 📈 Dashboard KPIs

The dashboard contains the following key performance indicators:

* **Total Employees**
* **Employees Left**
* **Attrition Rate**
* **Average Age**
* **Average Monthly Income**
* **Average Years at Company**

These KPIs provide a quick overview of the organization's workforce and employee retention situation.

---

## 📊 Dashboard Visualizations

The dashboard includes multiple interactive visualizations:

### Pie Charts

* Employee Attrition Distribution
* Gender Distribution
* Overtime Distribution
* Business Travel Distribution

### Funnel Chart

* Employees by Education Level

### Scatter Chart

* Job Role analysis using Average Monthly Income and Average Years at Company

### Line Chart

* Average Monthly Income by Job Level

### Line and Clustered Column Chart

* Employee Count and Attrition Rate by Department

### Waterfall Chart

* Attrition distribution across departments

### Gauge Chart

* Overall Employee Attrition Rate

---

## 🎛️ Interactive Slicers

The dashboard provides interactive slicers for detailed analysis.

### List Slicers

* Department
* Job Role
* Education Field
* Business Travel
* Marital Status
* Education
* Job Level

### Button Slicers

* Gender
* Attrition
* Overtime
* Business Travel

### Input / Range Slicers

* Age
* Monthly Income
* Daily Rate
* Years at Company
* Total Working Years
* Distance From Home

Users can select different values to dynamically filter the dashboard visuals.

---

## 📐 Key DAX Measures

### Total Employees

```DAX
Total Employees = COUNTROWS('HR Data')
```

### Employees Left

```DAX
Employees Left =
CALCULATE(
    COUNTROWS('HR Data'),
    'HR Data'[Attrition] = "Yes"
)
```

### Attrition Rate

```DAX
Attrition Rate =
DIVIDE(
    [Employees Left],
    [Total Employees],
    0
)
```

### Average Age

```DAX
Average Age = AVERAGE('HR Data'[Age])
```

### Average Monthly Income

```DAX
Average Monthly Income =
AVERAGE('HR Data'[MonthlyIncome])
```

### Average Years at Company

```DAX
Average Years at Company =
AVERAGE('HR Data'[YearsAtCompany])
```

---

## 🔍 Key Insights

The dashboard helps identify important HR patterns, including:

* The overall size of the employee workforce.
* The number and percentage of employees who have left the organization.
* Differences in attrition across departments and job roles.
* Workforce distribution across education levels and job roles.
* The relationship between employee income and experience.
* The distribution of employees working overtime.
* Employee distribution based on business travel and demographics.
* Differences in workforce characteristics across job levels.

---

## 📁 Repository Structure

```text
HR-Analytics-Dashboard/
│
├── Dataset/
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
│
├── Dashboard/
│   └── HR_Analytics_Dashboard.pbix
│
├── Screenshots/
│   └── HR_Analytics_Dashboard.png
│
├── Documentation/
│   └── HR_Analytics_Report.pdf
│
└── README.md
```

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open the `.pbix` file using Microsoft Power BI Desktop.
3. If required, update the dataset/file path.
4. Use the slicers to filter employee information.
5. Interact with the charts and KPI cards to explore HR insights.

---

## 📌 Conclusion

The **HR Analytics Dashboard** provides an interactive and comprehensive view of employee data. By combining KPIs, charts, and interactive slicers, the dashboard enables HR teams to analyze workforce distribution, employee attrition, demographics, compensation, and other important HR factors.

The dashboard can support data-driven workforce planning, employee retention strategies, and better HR management decisions.

---

## 👨‍💻 Project Information

**Assignment:** Weekly Assignment 6
**Title:** Creating HR Analytics Dashboards
**Tool:** Microsoft Power BI
**Dataset:** IBM HR Analytics Employee Attrition & Performance
**Repository:** GitHub
