# Government Job Market Analysis  
## Education, Sector & Role-Based Salary Insights

---

## 📌 Project Overview

This project analyzes government job listings to understand how **education level, sector, and job role categories influence salary structures**.

The study focuses on identifying demand distribution patterns and examining how different qualification levels interact with sector and role categories to determine compensation trends.

---

## 🎯 Problem Statement

How do sector and role categories interact with educational qualification to influence salary levels in government job listings?

---

## 📂 Data Collection

- Source: Public job listing portal (graduate job category)
- Total Pages Scraped: 43
- Total Records Collected: 1028
- Tools Used:
  - `requests`
  - `BeautifulSoup`
- Pagination handled programmatically
- Data validated via HTTP status checks

---

## 🧹 Data Cleaning & Feature Engineering

### Salary Processing
- Extracted numeric salary values using Regex.
- Created:
  - `salary_minimum`
  - `salary_maximum`
- Converted annual salaries to monthly values (heuristic-based normalization).
- Created:
  - `salary_range`
  - `salary_band`
- Handled 35% missing salary values by separating salary-based and demand-based analysis.

### Qualification Standardization
- Normalized textual variations.
- Created `qualification_level` categories:
  - Undergraduate
  - Postgraduate
  - Doctorate
  - Diploma
  - School Level
  - Other

### Title-Based Feature Engineering
- Split title into:
  - `organization_part`
  - `role_part`
- Extracted:
  - `sector`
  - `role_category`
- Used keyword-based hierarchical classification.

---

## 📊 Descriptive Analysis

Two analytical tracks were created:

### 1️⃣ Demand Distribution Analysis
- Qualification demand by sector
- Role category distribution
- Cross-tabulation: qualification × sector

### 2️⃣ Salary Structure Analysis
- Core Market (Trimmed 99th percentile)
- Elite Roles (Top 1% salary)
- Median salary comparisons across:
  - Qualification
  - Sector
  - Role Category

---

## 🔍 Key Insights (Preliminary)

- Undergraduate roles dominate overall government hiring.
- Elite salary roles are concentrated in managerial and officer positions within PSU and Banking sectors.
- Education level alone does not determine high salary; sector and role hierarchy play a stronger role.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Regex
- Web Scraping (Requests, BeautifulSoup)
- SQL (Schema Design & Data Structuring)

---

## 📈 Future Work

- Multivariate interaction analysis
- Salary prediction modeling
- Role refinement using NLP-based classification
- Sector-level salary forecasting

---

## 👤 Author
K.Midhun Kumar
Data Analysis Project – Government Job Market Study  
Focused on structured EDA and feature-driven market interpretation.