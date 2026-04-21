# 🚗 EV Adoption in Washington State

Electric vehicle (EV) adoption is influenced by multiple factors including income levels, geographic distribution, and policy incentives. However, relevant datasets are often stored separately, limiting comprehensive analysis.

This project develops a **dimensional data warehouse** to integrate **EV registration data, county-level income data, and clean-fuel tax exemption classifications** for **Washington State** into a unified analytical system.

The goal is to enable **multi-dimensional analysis of EV adoption trends** across time, geography, vehicle characteristics, and socioeconomic factors.

---

### 🎯 Project Objective

This project addresses a key analytical challenge:

> How can we integrate fragmented EV, income, and policy datasets to analyze adoption trends across Washington State?

To solve this, a **data warehouse** was designed using a **STAR Schema** to support efficient querying, reporting and trend analysis over a **15 year period (2010–2024)**.

---

### 🏗️ Key Highlights

- Built a **STAR schema data warehouse** integrating EV population, income, and tax-exemption datasets  
- Designed and implemented **ETL pipelines using Oracle SQL Developer** for data cleaning and transformation  
- Modeled data using **fact and dimension tables** (Time, County, Vehicle, Vehicle Type, Income, Tax Exemption)  
- Performed **SQL-based exploratory data analysis and advanced analytics** using window functions (LAG, CORR, NTILE)  
- Enabled **multi-dimensional analysis** across time, geography, income levels, and vehicle attributes  

---

### 🧱 Data Warehouse Design

The warehouse is structured using a **dimensional model (STAR schema)** to support analytical workloads:

- **Fact Table:** `FACT_EV_REGISTRATION`  
  - Measures: EV Count, Electric Range, Base MSRP  

- **Dimension Tables:**  
  - `TIME_DIM` (Year)  
  - `COUNTY_DIM` (Geographic regions in Washington State)  
  - `VEHICLE_DIM` (Make, Model, Model Year)  
  - `VEHICLE_TYPE_DIM` (EV type and CAFV eligibility)  
  - `INCOME_DIM` (Median household income by county and year)  
  - `TAX_EXEMPTION_DIM` (Clean-fuel tax eligibility)  

This design enables:
- Efficient aggregation and reporting  
- Drill-down and roll-up analysis  
- Slicing and dicing across multiple analytical dimensions  

📄 Refer to the full report for schema diagrams and detailed design:  
👉 [Final Project](./Final%20Project.pdf)

---

### 🔍 Analytical Insights

Using SQL-based analysis and reporting on the integrated warehouse:

- EV registrations have **increased significantly over time**, with rapid growth after 2018  
- Strong **positive correlation (~0.68)** between median household income and EV adoption  
- EV adoption is **concentrated in urban counties** such as King County  
- **Battery Electric Vehicles (BEVs)** dominate (>95% of registrations)  
- **Tesla accounts for ~57%** of total EV registrations, indicating high market concentration  

These findings highlight the **economic, geographic, and policy-driven factors** influencing EV adoption in Washington State.

---

### 🛠️ Tech Stack

- **Oracle SQL Developer** – ETL, data modeling, and analytical querying  
- **SQL** – Data transformation, joins, aggregations, and advanced analytics  
- **Dimensional Modeling** – STAR schema design (fact & dimension tables)  
- **Data Warehousing Concepts** – Surrogate keys, OLAP modeling  
- **Excel / Data Processing** – Data preparation and structuring  

---

### 📄 Full Project Documentation

For a complete breakdown of:
- Data collection and cleaning  
- OLTP vs OLAP schema design  
- ETL workflow  
- STAR schema implementation  
- SQL queries and advanced analytics  
- Reporting and storytelling  

👉 Refer to: [Final Project](./Final%20Project.pdf)

---

### 💡 Key Takeaway

This project demonstrates how **data warehousing and SQL analytics** can transform fragmented datasets into a **scalable analytical system**, enabling deeper insights into EV adoption patterns and supporting data-driven decision-making in transportation and policy planning.



