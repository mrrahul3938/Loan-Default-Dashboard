# 🏦 Loan Default & Financial Profile Dashboard

### 📊 End-to-End Data Analytics Project using Power BI, SQL Server, and Figma

This project focuses on analyzing **loan default patterns** and **applicant financial profiles** to help financial institutions understand risk factors and borrower behavior.  
It is a **complete data analytics pipeline** project — from data import to visualization and automation.

---

## 🚀 Project Overview

The goal of this project is to analyze and visualize:
- Loan amount distribution across purposes, age groups, and employment types  
- Default rate trends across years and demographics  
- Applicant financial profiles by credit score, education, and marital status  
- Year-over-year (YOY) loan and default rate changes  

---

## 🛠️ Tools & Technologies Used

| Stage | Tools / Techniques |
|--------|--------------------|
| Data Source | SQL Server |
| Data Integration | Power BI Dataflows |
| Data Cleaning & Profiling | Power Query Editor |
| Data Modeling | DAX Measures |
| Dashboard Design | Figma |
| Visualization | Power BI Desktop |
| Deployment & Refresh | Power BI Service |

---

## 📂 Project Workflow

### 1️⃣ Data Sourcing
- Imported raw loan dataset into **SQL Server**
- Created tables, cleaned null/missing data, and added data types

### 2️⃣ Dataflow Creation
- Built a **Power BI Dataflow** from SQL Server tables
- Enabled scheduled refresh for automatic data updates

### 3️⃣ Data Transformation
- Used **Power Query Editor** for:
  - Data type correction  
  - Removing duplicates  
  - Profiling and column distribution checks  

### 4️⃣ Data Modeling & DAX
Created several calculated measures to analyze the data effectively.  
Here are some **DAX examples** used in the project:

```DAX
Loan amount by purpose = 
SUMX(
    FILTER('Loan_default', NOT(ISBLANK('Loan_default'[LoanAmount]))),
    'Loan_default'[LoanAmount]
)

Average Loan by Age Group = 
AVERAGEX(
    VALUES('Loan_default'[AgeGroups]),
    AVERAGE('Loan_default'[LoanAmount])
)
```

Other functions used across the project:
SUMX, CALCULATE, FILTER, NOT, ISBLANK, AVERAGEX, DIVIDE, VALUES, ALLEXCEPT, SWITCH, COUNTROWS, MEDIANX

5️⃣ Dashboard Design

Designed layout mockup in Figma

Implemented final visuals in Power BI Desktop

Added navigation buttons for page-to-page movement

6️⃣ Deployment

Published report to Power BI Service

Set up Scheduled Refresh for both Dataflow and Report

Shared report access with stakeholders

📈 Dashboard Pages & Insights
📄 Page 1 — Loan Default & Overview

Loan amount by purpose (Home, Business, Education, Auto, Other)

Default rate by employment type

Average income by employment type

Loan amount by age group

Default rate trends by year

🔍 Dashboard Preview:

📄 Page 2 — Applicant Demographics & Financial Profile

Median loan amount by credit score

Loan distribution by education type

Loan by marital status & age group

Loan comparison based on mortgage/dependents

🔍 Dashboard Preview:

📄 Page 3 — Financial Risk Metrics

YOY default and loan amount change

Loan amount by credit score & marital status

Income vs Employment Type distribution

YTD loan comparison

🔍 Dashboard Preview:

💡 Key Insights

🏠 Home Loans have the highest average loan amount (₹6545M)

📉 Default Rate highest among unemployed (3.39%)

👨‍💼 Average income increases with employment stability

📊 YOY analysis shows a spike in defaults during 2015–2016

🧮 Median loan amount decreases as credit score improves
