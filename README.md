# 📊 HR Attrition & Workforce Analytics Dashboard

## 📌 Project Overview
Employee turnover is one of the highest unseen costs in corporate environments. This project focuses on human resources analytics, utilizing a dataset of 500 employee records to identify attrition drivers, calculate key performance indicators (KPIs), and present the findings in an interactive, executive-level dashboard.

## 🏗️ Architectural Design (The 3-Tier Model)
To ensure data integrity and prevent user-generated errors, this tool was engineered using a strict three-tier architecture, mimicking professional BI software:
1. **Inputs (Data Layer):** The raw employee dataset, enhanced with newly engineered categorical columns.
2. **Calculations (Logic Layer):** A hidden mathematical engine that powers the dashboard metrics.
3. **Dashboard (Presentation Layer):** A clean, gridless graphical user interface (GUI) designed for executive end-users.

## ⚙️ Core Methodologies & Skills Demonstrated

### 1. Data Transformation & Demographic Bucketing
Continuous variables were transformed into categorical buckets to allow for trend analysis.
* **Logic Used:** Advanced `=IFS()` statements.
* **Application:** Grouped individual ages into generational brackets (e.g., "25-34", "35-44") and converted exact years of service into Experience Levels (e.g., "Entry", "Veteran"). 

### 2. The KPI Calculation Engine
Instead of relying entirely on Pivot Tables, a hard-coded calculation matrix was built to calculate baseline HR metrics dynamically.
* **Logic Used:** `=COUNTA()`, `=COUNTIF()`, and mathematical division.
* **Application:** Calculated Total Historical Headcount, isolated Current Active Employees, and computed the overall **Baseline Attrition Rate**.

### 3. Interactive Visual Storytelling (UI/UX)
The presentation layer was designed to provide immediate insights with zero required Excel knowledge from the end-user.
* **Executive Summary Cards:** Built dynamic shape objects linked directly to the Calculation Engine to display high-level KPIs instantly.
* **Relational Filtering:** Deployed interactive **Slicers** connected across multiple PivotCharts via *Report Connections*. This allows leadership to filter the entire dashboard by `Department` or `JobTitle` with a single click, instantly recalculating all charts and demographic splits.

## 📂 Repository Contents
* `HR_Attrition_Dashboard.xlsx`: The complete, interactive Excel workbook.
* `Raw_HR_Data.csv`: The original unformatted dataset used for the project (sourced from Kaggle).
