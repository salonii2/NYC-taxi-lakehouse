# NYC Taxi Data Lakehouse 🚕
### End-to-End Data Engineering Project using Azure Databricks, PySpark and Delta Lake

## 📌 Project Overview

This project focuses on building an end-to-end Data Engineering pipeline using the NYC Yellow Taxi trip dataset.

The goal is to develop a Lakehouse architecture following the **Medallion Architecture (Bronze, Silver and Gold)** to ingest, process, clean and transform raw taxi trip data into analytics-ready datasets.

The project is being developed using Databricks, PySpark, Delta Lake and SQL.

## 🏗️ Architecture

The project follows the Medallion Architecture:

- **Bronze Layer:** Ingest and store raw taxi trip data in Delta format.
- **Silver Layer:** Clean, validate and transform raw records.
- **Gold Layer:** Create aggregated datasets for business intelligence and analytics.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Databricks | Lakehouse development platform |
| Apache Spark | Distributed data processing engine |
| PySpark | Data processing using Python |
| Delta Lake | Reliable storage and table management |
| SQL | Data querying and analytics |
| Parquet | Source dataset format |
| GitHub | Version control and documentation |

## 📂 Dataset

**Source:** NYC Taxi & Limousine Commission (TLC)

Dataset: January 2025 Yellow Taxi Trip Records

Source: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

- File: `yellow_tripdata_2025-01.parquet`
- File size: Approximately 56.42 MB
- Records: 3,475,226
- Columns: 20

## 🥉 Bronze Layer — Completed

The Bronze layer is the initial ingestion stage of the pipeline.

### Implementation

1. Created a Databricks Unity Catalog schema.
2. Created a managed Unity Catalog Volume.
3. Uploaded the original January 2025 Parquet dataset.
4. Read the dataset using PySpark.
5. Inspected the schema, column names and record count.
6. Stored the original dataset as a managed Delta table.

### Databricks Storage Structure

```text
workspace
└── nyc_taxi_lakehouse
    └── Volumes
        └── nyc_taxi_raw
            └── yellow_tripdata_2025-01.parquet
```

### Bronze Delta Table

```text
workspace.nyc_taxi_lakehouse.bronze_yellow_taxi
```

The Bronze Delta table was successfully created using PySpark.

## 🥈 Silver Layer — Upcoming

Planned transformations:

- Identify and handle missing values.
- Detect duplicate records.
- Validate trip distances and fare amounts.
- Handle invalid timestamps.
- Apply data quality checks.
- Store cleaned records in a Silver Delta table.

## 🥇 Gold Layer — Upcoming

Planned analytical datasets:

- Daily taxi trip metrics.
- Daily revenue analysis.
- Average trip distance.
- Payment method analysis.
- Popular pickup and drop-off locations.
- Business intelligence reporting.

## 📁 Repository Structure

```text
nyc-taxi-lakehouse/
│
├── README.md
├── notebooks/
│   ├── 01_nyc_taxi_bronze.py
│   ├── 02_nyc_taxi_silver.py
│   └── 03_nyc_taxi_gold.py
├── sql/
│   └── analytics_queries.sql
├── docs/
│   ├── architecture.md
│   └── project_progress.md
└── .gitignore
```

## 🎯 Project Objective

Build a practical end-to-end Data Engineering solution while developing hands-on experience with:

- Data ingestion and processing.
- Distributed computing using Apache Spark.
- PySpark DataFrame operations.
- Delta Lake and Lakehouse architecture.
- Data quality and transformation.
- SQL-based analytics.
- Version control using Git and GitHub.

---

**Project Status:** In Progress 🚀

Currently completed: Bronze Layer.

Next milestone: Silver Layer implementation.
