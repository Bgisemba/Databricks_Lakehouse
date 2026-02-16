# 🏗️ End-to-End Data Engineering Pipeline on Databricks  
## Medallion Architecture (Bronze → Silver → Gold)

![Databricks](https://img.shields.io/badge/Platform-Databricks-red)
![Spark](https://img.shields.io/badge/Engine-Apache_Spark-orange)
![Delta Lake](https://img.shields.io/badge/Storage-Delta_Lake-blue)
![Architecture](https://img.shields.io/badge/Architecture-Medallion-green)
![Status](https://img.shields.io/badge/Status-Production_Ready-success)

---

## 📌 Project Summary

This project demonstrates the design and implementation of a scalable **Lakehouse data pipeline** using **Databricks** and **Delta Lake**, following the **Medallion Architecture** pattern.

The pipeline ingests raw sales data, applies structured transformations, enforces data quality rules, and produces analytics-ready datasets optimized for reporting and business intelligence tools.

The workflow is fully orchestrated using a **Databricks Job** to simulate a production-grade data engineering pipeline.

---

## 🏛️ Architecture Overview

The project implements a three-layer architecture:

Raw Data → Bronze → Silver → Gold → BI / Analytics


### 🥉 Bronze Layer – Raw Data Ingestion
**Purpose:** Preserve raw data for auditability and traceability.

- Ingested raw sales data into Delta tables
- Maintained original schema structure
- Enabled schema enforcement
- Stored data in append mode for incremental processing

📌 Output: Raw Delta tables (immutable source of truth)

---

### 🥈 Silver Layer – Data Cleansing & Transformation
**Purpose:** Improve data quality and enforce business logic.

Transformations performed:
- Removed duplicates
- Handled null and missing values
- Standardized date formats and categorical values
- Applied business transformation logic
- Ensured referential and schema consistency

📌 Output: Cleaned and validated Delta tables

---

### 🥇 Gold Layer – Business-Level Aggregation
**Purpose:** Deliver analytics-ready datasets.

- Created aggregated sales metrics
- Optimized tables for reporting queries
- Structured data for BI consumption
- Designed tables for dashboard integration

📌 Output: Curated business-ready datasets

---

## ⚙️ Pipeline Orchestration

A **Databricks Job** was created to automate:

- Bronze ingestion
- Silver transformation
- Gold aggregation
- Sequential task dependencies
- Scheduled execution

This ensures:
- Reproducibility  
- Automation  
- Scalability  
- Production simulation  

---

## 🛠️ Tech Stack

| Component        | Technology Used |
|-----------------|----------------|
| Processing Engine | Apache Spark (PySpark) |
| Storage Layer     | Delta Lake |
| Platform          | Databricks Lakehouse |
| Querying          | Spark SQL |
| Version Control   | Git & GitHub |

---
