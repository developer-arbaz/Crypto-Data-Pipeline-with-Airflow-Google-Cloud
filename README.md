# 🚀 Crypto Data Pipeline with Airflow & Google Cloud

An end-to-end data pipeline that extracts real-time cryptocurrency data from APIs, processes it, and loads it into Google BigQuery for analytics and visualization. The pipeline is fully automated using Apache Airflow (Google Cloud Composer).

---

## 📌 Project Overview

This project demonstrates a complete **data engineering workflow**, including:

- Data extraction from external APIs
- Data storage in Google Cloud Storage (GCS)
- Data transformation and cleaning
- Data warehousing using BigQuery
- Workflow orchestration using Airflow
- Data visualization using Looker

The pipeline runs on a **daily schedule**, ensuring up-to-date cryptocurrency insights.

---

## 🏗️ Architecture

```
API (CoinGecko)
      ↓
Google Cloud Storage (GCS)
      ↓
Data Transformation (Python)
      ↓
BigQuery (Data Warehouse)
      ↓
Stored Procedure (Analytics)
      ↓
Looker Dashboard (Visualization)
```

---

## ⚙️ Tech Stack

- **Programming Language:** Python  
- **Orchestration:** Apache Airflow (Google Cloud Composer)  
- **Cloud Platform:** Google Cloud Platform (GCP)  
- **Storage:** Google Cloud Storage (GCS)  
- **Data Warehouse:** BigQuery  
- **Visualization:** Looker  
- **API Source:** CoinGecko API  

---

## 🔄 Pipeline Workflow

### 1. Fetch Crypto Data
- Extracts real-time data for:
  - Bitcoin
  - Ethereum
  - Tether
  - Binance Coin
  - Solana  
- Data fetched via CoinGecko API  
- Stored in CSV format in GCS  

---

### 2. Data Transformation
- Cleans missing/null values  
- Standardizes column formats  
- Filters relevant fields  
- Prepares schema for BigQuery  

---

### 3. Load to BigQuery
- Data loaded into partitioned tables  
- Partitioning based on **date column**  
- Optimized for efficient querying  

---

### 4. Trigger Stored Procedure
- Runs post-load transformations  
- Performs aggregations and analytics  
- Generates final structured tables  

---

### 5. Visualization (Looker)
- Real-time dashboards showing:
  - Market trends  
  - Price comparisons  
  - Volume analysis  
  - Performance insights  

---

## 🧩 Airflow DAG Tasks

| Task Name | Description |
|----------|------------|
| `start` | Logs pipeline start time |
| `fetch_and_upload_data_gcs_task` | Fetches API data & uploads to GCS |
| `load_data_bq_task` | Loads data into BigQuery |
| `trigger_procedure_task` | Runs BigQuery stored procedure |
| `end` | Logs pipeline completion |

---

## 🗄️ Database Schema

### Tables:

- **crypto_data_temp** – Raw cryptocurrency data (USD, INR, EUR)  
- **final_data** – Cleaned and structured dataset  
- **market_metrics** – Total market capitalization  
- **volume_metrics** – 24-hour trading volume  

---

## 📊 Key Features

✅ Fully automated daily pipeline  
✅ Real-time crypto data ingestion  
✅ Scalable cloud-based architecture  
✅ Partitioned BigQuery tables  
✅ Interactive dashboards with Looker  
✅ Modular and reusable Airflow DAG  

---

## 🔐 Setup & Configuration

### Prerequisites:

- Google Cloud Account  
- Enabled services:
  - BigQuery  
  - Cloud Storage  
  - Cloud Composer  

### Required Setup:

1. Create a **GCS Bucket**  
2. Create a **BigQuery Dataset & Tables**  
3. Configure **IAM Roles**:
   - Storage Admin  
   - BigQuery Admin  
4. Deploy Airflow DAG in Composer  

---

## 📸 Screenshots

(Add screenshots here: Airflow DAG, BigQuery, Looker Dashboard)

---

## 📈 Future Enhancements

- Add more cryptocurrencies  
- Implement real-time streaming (Pub/Sub)  
- Add alerting system for price changes  
- Integrate ML models for prediction  

---

## 👨‍💻 Author

**Arbaz Khan**  
📧 arbazkhan21223@gmail.com  
🔗 https://www.linkedin.com/in/arbaz-data-analyst/  
💻 https://github.com/developer-arbaz  

---

## ⭐ If you like this project

Give it a ⭐ on GitHub!
