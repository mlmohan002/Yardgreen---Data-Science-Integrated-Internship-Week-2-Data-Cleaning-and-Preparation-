project Link:https://app.powerbi.com/Redirect?action=OpenApp&appId=9b203364-b774-430f-a966-e90f7843004e&ctid=3e71a923-9a43-4d6c-b58f-49294d89e08f&experience=power-bi
# Yardgreen---Data-Science-Integrated-Internship-Week-2-Data-Cleaning-and-Preparation-
○ Identify and handle missing values using techniques like imputation or removal.  ○ Standardize date and time formats for easy filtering and analysis.  ○ Detecting and eliminating outliers that could distort traffic patterns.

# 🚦 Traffic Data Cleaning and Analysis with Power BI

This project focuses on cleaning, preprocessing, and visualizing traffic sensor data to uncover meaningful patterns and support data-driven decisions. The dataset includes vehicle counts across various junctions with timestamps.

---

## 📁 Dataset Overview

- **Rows:** ~48,000 traffic entries
- **Columns:**  
  - `ID`: Unique identifier  
  - `DateTime`: Timestamp of data collection  
  - `Junction`: ID of the junction  
  - `Vehicles`: Number of vehicles recorded  

---

## ✅ Deliverables

### 1. Missing Values Report

- **Missing Columns:** None  
- **% Missing per Column:** 0% across all columns  
- **Handling Technique:**  
  - Imputation not required  
  - No rows or columns removed  
- ✅ Final dataset has **no missing values**

---

### 2. Standardized Date & Time Format

- Converted `DateTime` to uniform format: `YYYY-MM-DD HH:MM:SS`
- **Derived Fields for Analysis:**
  - Hour (0–23)
  - Day of Week (e.g., Monday)
  - Month (e.g., January)
- 📊 Enabled better time-based analysis (hourly, daily, monthly traffic patterns)

---

### 3. Outlier Detection and Removal

- **Method Used:** Interquartile Range (IQR)
- **Upper Bound (Q3 + 1.5*IQR):** 59 vehicles
- **Outliers Found:** 3,617 entries
- **Action Taken:** Removed all rows with `Vehicles > 59`
- ✅ Resulting clean dataset: 44,503 records

---

### 4. Refined, Clean Dataset

- ✅ No missing values
- ✅ Clean, consistent date/time format
- ✅ Outliers removed
- ✅ Optimized for Power BI visual analytics

---

## 📊 Visualizations in Power BI

Here’s a list of key visual insights created in Power BI:

- **Line Chart** – Vehicle trends over time
- **Bar Chart** – Traffic by Hour & Day
- **Donut Chart** – Junction-wise traffic share
- **Heat Map** – Hour vs Day traffic intensity
- **Decomposition Tree** – Drill-down analysis
- **Anomaly Detection** – Spikes in traffic
- **Slicers** – Filters for Junction, Hour, Month

---

## 🚀 How to Use

1. Clone or download the repository.
2. Open `Power BI Desktop`.
3. Import the cleaned `.csv` dataset (provided in `/data` folder).
4. Load the `.pbix` file to view pre-built dashboards (optional).
5. Explore, filter, and interact with the report visuals.

---

## 📂 Repository Structure

```plaintext
├── data/
│   └── traffic_cleaned.csv         # Final cleaned dataset
├── reports/
│   └── traffic_analysis.pbix       # Power BI file (if provided)
├── README.md                       # This file

