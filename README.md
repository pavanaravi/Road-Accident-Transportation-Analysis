🚦 Road Accident Transportation Analysis

An end-to-end data analytics project that cleans a real-world road transportation accident dataset and turns it into a suite of dashboards — from hotspot mapping and severity analysis to predictive threat scoring and executive reporting — for road safety decision-making.



 📌 Project Overview

This project analyzes a **12,316-row, 32-column** road transportation accident dataset covering driver demographics, vehicle details, road and weather conditions, collision details, and casualty information. After cleaning and feature engineering, the dataset powers a set of dashboards that surface accident patterns, operational performance, and predictive risk — giving stakeholders a clear, monitorable view of road safety.

 🎯 Objectives

- Clean and validate a real-world, messy accident dataset
- Engineer time-based, risk-based, and category features for deeper analysis
- Visualize accident hotspots, severity distribution, and risk surfaces
- Build executive dashboards for security risk assessment and predictive threat analytics
- Translate findings into a monitorable baseline for road safety interventions

 🧹 Data Preparation

Before any dashboard was built, the raw dataset went through cleaning and preprocessing:

- **Cleaning:** 0 duplicate records found; missing values handled per column using mode imputation, rule-based conditional filling, group-based imputation, and context-based imputation (e.g. `Road_surface_type` filled based on `Weather_conditions`, `Driving_experience` filled based on `Age_band_of_driver`)
- **Type optimization:** `Time` converted to `datetime64`; 29 text columns converted to `category` dtype, cutting memory from 3.0 MB to 646.7 KB (~78% reduction)
- **Outlier handling:** IQR-based detection and capping on `Number_of_vehicles_involved` and `Number_of_casualties` — no rows dropped
- **Feature engineering:** `Accident_Hour`, `Time_Period`, `High_Risk_Weather`, `Vehicles_Category`, `Casualties_Category`
- **Feature selection:** dropped redundant/low-value columns → final clean dataset: **12,316 rows × 33 columns**, 0 missing values

## 📊 Dataset

| Detail | Description |
|---|---|
| Rows | 12,316 |
| Columns (final) | 33 (2 numeric, 29 categorical, 1 datetime-derived, 1 object) |
| Duplicates | 0 |
| Missing values (final) | 0 |
| Column groups | Driver & Vehicle · Road & Environment · Collision Details · Casualty Info |

---

## 📊 Dashboard Analysis

### Hotspot Intelligence Maps
Geospatial mapping of accident concentration, identifying the specific locations and zones where incidents cluster most heavily.

### Risk-Surface Visualization
A continuous risk-surface view layered over accident data, highlighting gradients of risk intensity across the road network rather than isolated points.

### Incident Response Performance
Analysis of how quickly and effectively incidents are responded to, surfacing performance gaps in response time and coverage.

### Resource Deployment & Operational Coverage
Visualization of where response resources are deployed versus where accident risk is highest, exposing coverage gaps.

### Security Risk Assessment Dashboard
Consolidated risk scoring across locations and conditions to flag high-security-risk zones for intervention.

### Predictive Threat Analytics
Forward-looking analytics that model the likelihood and severity of future incidents based on historical patterns.

### Executive Command-Center Dashboard
A high-level, decision-maker-facing view consolidating risk, severity, and operational metrics into a single monitorable baseline.

### Forecasting, Alerting & Performance Optimization
Forecasting models and alert thresholds tuned against the dataset, producing:
- **15.4%** critical accident rate
- **11.38%** alert rate

---

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy)
- Power BI
- Microsoft Excel
- Data Visualization
- Data Analytics
- Power BI Forecasting
- Interactive Slicers & Filters

---

## 🔑 Key Insights

Across all dashboards, the project delivers an end-to-end view of road accident risk — from raw incident data to predictive threat scoring. Key risk drivers consistently point to **darkness without lighting, weekend timing, and lack of distancing** as the strongest predictors of severe outcomes. The Executive Command Center and Forecasting dashboards translate these findings into a clear, monitorable baseline, equipping stakeholders to prioritize interventions by location, time of day, and weather condition — improving both response speed and long-term road safety planning.
