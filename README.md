# Project 5 - AI Supply Chain Demand Forecasting Lakehouse

### *End-to-End ETL + Machine Learning + Analytics Dashboard*

---

## 🚀 Project Overview

This project simulates a **real-world supply chain optimization system**, where retail sales data flows through a **Bronze → Silver → Gold Lakehouse Architecture**, followed by **AI-based demand forecasting**, and a **Streamlit dashboard for real-time analytics & predictions**.

It demonstrates how retail companies can:

✔ Forecast future product demand
✔ Optimize inventory levels
✔ Analyze sales trends & product contribution
✔ Use machine learning to make data-driven decisions

---

## 🏗 Architecture Workflow

```
        Raw Data (CSV)
              │
              ▼
        🟫 Bronze Layer
        - Raw ingestion
        - Data stored as-is
              │
              ▼
        ▫ Silver Layer
        - Cleaning + Feature Engineering
        - Date Extracts (Year/Month/Week)
        - DuckDB Lakehouse table
              │
              ▼
        🟨 Gold Layer
        - AI Model Training (RandomForestRegressor)
        - Demand Forecast Model Saved (.pkl)
              │
              ▼
        📊 Streamlit Dashboard
        - Visual Insights & Demand Prediction UI
```

---

## 🛠 Tech Stack & Tools

| Component       | Tool                                 | Purpose                                |
| --------------- | ------------------------------------ | -------------------------------------- |
| Programming     | **Python**                           | Core development                       |
| Data Storage    | **DuckDB**                           | Local Lakehouse table for silver layer |
| Data Processing | **Pandas**                           | Cleaning, transformation               |
| ML Model        | **Scikit-Learn (RandomForestRegr.)** | Forecast future demand                 |
| Serialization   | **Joblib**                           | Save trained ML model                  |
| Dashboard       | **Streamlit**                        | Interactive UI & visualization         |
| Visualization   | **Plotly**                           | Trend charts & product distribution    |
| Environment     | **Virtualenv**                       | Isolated execution env                 |

---

## 📂 Project Structure

```
Project_5_Supply_Chain_Demand_Forecasting/
│── data/
│   ├── raw/retail_sales.csv
│   ├── silver/silver_data.csv
│   ├── gold/gold_feature_set.csv
│
│── lakehouse/retail.db           ← Silver stored in DuckDB
│── models/demand_forecast.pkl    ← Final ML model
│
│── src/
│   └── pipeline_demand_forecasting.py   ← ETL + Training Pipeline
│
│── app/
│   └── streamlit
```
