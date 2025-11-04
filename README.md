# 🏥 Big Data Healthcare Analytics using PySpark

A Spark-based analytics pipeline for hospital admissions and billing datasets.  
Performs large-scale processing, visualization, and insight generation for healthcare optimization.

---

## 📖 Overview

This project demonstrates how **Apache Spark (PySpark)** can be used to analyze large-scale **healthcare data** efficiently.  
Using a dataset of **55,500 hospital admission records**, the system processes, cleans, and visualizes data to uncover insights about patient demographics, billing patterns, and admission types.

The project showcases how **distributed computing frameworks** can improve **healthcare decision-making**, optimize hospital workflows, and enable **data-driven cost management**.

---

## ⚙️ Features

- ✅ End-to-end **ETL pipeline** using PySpark (Extract, Transform, Analyze)
- 📊 Descriptive and correlation analysis of healthcare attributes  
- 🔍 Aggregation of average billing by medical condition and age  
- 📈 Visualization of admission types, test results, and billing trends  
- 🧠 Scalable execution on **Google Colab** using Spark DataFrame API  
- 💾 Data preprocessing, cleaning, and feature engineering  
- 📉 Weak correlation findings between age, billing, and stay duration  
- 🧮 Benchmarking Spark’s performance on 55K+ healthcare records  

---

## 🧰 Tools & Frameworks

| Category | Tool/Library | Purpose |
|-----------|---------------|----------|
| Big Data Framework | **Apache Spark (PySpark)** | Distributed data processing and computation |
| Programming Environment | **Google Colab** | Notebook-based Spark execution |
| Visualization | **Matplotlib**, **Seaborn** | Charts and dashboards for insights |
| Data Handling | **Spark SQL**, **DataFrame API**, **Pandas** | Data cleaning, grouping, and export |
| File Format | **CSV** | Input dataset for Spark processing |

---

## 🧪 Methodology

The project follows a **4-step ETA pipeline** (Extract–Transform–Analyze):

1. **Extraction**  
   Load hospital admission records using `spark.read.csv()` with schema inference.  

2. **Transformation**  
   - Clean and filter null or invalid entries  
   - Convert admission and discharge dates  
   - Derive new column: `Stay_Days` using `datediff()`  
   - Standardize and aggregate features  

3. **Analysis**  
   - Compute average billing and age per medical condition  
   - Calculate correlation between `Age ↔ Billing` and `Stay ↔ Billing`  
   - Summarize key statistics with `groupBy()` and `agg()`  

4. **Visualization**  
   - Convert to Pandas DataFrames for Seaborn/Matplotlib plotting  
   - Generate bar charts, scatter plots, heatmaps, and correlation matrices  

---

## 📊 Key Insights

- **Highest average billing** observed for *Diabetes* and *Obesity* (~$25,800 USD).  
- **Average patient age:** ~51 years across all conditions.  
- **Admission distribution:** Elective ≈ Urgent ≈ Emergency (~18K each).  
- **Correlation:** Age ↔ Billing (r = -0.004), Stay ↔ Billing (r = -0.006).  
- **Interpretation:** Cost primarily driven by condition type, not age or stay duration.  

---

## 📁 Project Structure

