# 🚀 Multi-Cloud Data Pipeline: Nested JSON → Snowflake (CDC + GenAI Ready)

<img width="258" height="41" alt="image" src="https://github.com/user-attachments/assets/d0dabf32-127b-4943-b713-1b4998b2e63a" />

![AWS](https://img.shields.io/badge/Cloud-AWS-orange)
![Azure](https://img.shields.io/badge/Cloud-Azure-blue)
![GCP](https://img.shields.io/badge/Cloud-GCP-green)
![Streaming](https://img.shields.io/badge/Streaming-Kafka-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Overview

This project demonstrates a **production-grade, multi-cloud data engineering pipeline** that processes:

* 📦 Large (20GB+) Nested JSON files
* 🔄 Change Data Capture (CDC)
* ☁️ Multi-cloud ingestion (AWS / GCP / Azure)
* 🧠 AI-ready data (RAG / GenAI integration)

---

## 🏗️ Architecture

```
          +----------------------+
          |   JSON (20GB Files)  |
          +----------+-----------+
                     |
      +--------------+--------------+
      |       Cloud Storage         |
      |  (S3 / GCS / ADLS)         |
      +--------------+--------------+
                     |
               Snowpipe
                     |
              Raw Table (VARIANT)
                     |
           Stream + Task (CDC)
                     |
              Silver Table
                     |
        +------------+------------+
        |                         |
     BI Tools                 GenAI Chatbot
```

---

## 📂 Project Structure

```
├── part1_local/      # Local testing (Laptop)
├── part2_aws/        # AWS (S3 → Snowflake)
├── part3_gcp/        # GCP (GCS → Snowflake)
├── part4_azure/      # Azure (ADLS → Snowflake)
├── common/           # Shared logic
├── ui/               # Streamlit dashboard
├── ai/               # RAG chatbot
├── cost/             # Cost optimization
```

---

## 🔥 Key Features

✔️ Handles **nested JSON at scale**
✔️ Implements **CDC using Streams + MERGE**
✔️ Supports **Batch + Streaming (Kafka)**
✔️ Integrates with **GenAI (RAG)**
✔️ Works across **multi-cloud environments**

---

## 🧪 Part-wise Execution

### ▶️ Part 1: Local

```bash
python generate_data.py
snowsql -f create_tables.sql
```

---

### ☁️ Part 2: AWS

* Upload to S3
* Configure Snowpipe
* Auto-ingest to Snowflake

---

### 🌐 Part 3: GCP

* Upload to GCS
* Configure Storage Integration
* Run Snowpipe

---

### 🔷 Part 4: Azure

* Upload to ADLS
* Configure SAS integration
* Run ingestion pipeline

---

## 🤖 GenAI Integration

* Snowflake → Embeddings → Vector DB
* RAG-based chatbot
* Query your data using natural language

---

## 💰 Cost Optimization

* Warehouse usage analysis
* Auto recommendations
* Multi-cloud cost comparison

---

## 📊 Demo Flow

1. Upload large JSON
2. Snowpipe ingestion
3. CDC merge
4. Query via UI
5. Ask chatbot

---

## 👨‍💻 Author

**Lakshman Rao M**
Senior Data Architect | Multi-Cloud | AI/ML

---

## ⭐ If you found this useful, give it a star!

