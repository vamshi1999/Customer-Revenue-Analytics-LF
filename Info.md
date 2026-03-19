# Customer Revenue Analytics Pipeline (Lakehouse + Lakeflow)

## Overview

This project implements a **data engineering pipeline** using **Databricks Lakehouse architecture**. It processes raw data from files, transforms it through multiple layers, and generates business-ready analytics tables.

The pipeline follows the **Medallion Architecture (Bronze → Silver → Gold)** and is orchestrated using **Databricks Workflows (Lakeflow DAG)**.

---

## Architecture

```
Raw Files (Volume)
        │
        ▼
Bronze Layer (Delta Tables)
        │
        ▼
Silver Layer (Enriched Data)
        │
        ▼
Gold Layer (Business Metrics)
```

---

## Key Features

### Medallion Architecture

* Clear separation of ingestion, transformation, and serving layers

### Delta Lake

* ACID transactions
* Partitioning for performance

### Incremental Processing

* Uses `processing_date` parameter
* Processes only new data

### Parameterized Pipeline

* Uses Databricks widgets
* Supports backfills and reprocessing

### Broadcast Joins

* Optimized joins for small dimension tables

### Window Functions

* Top-N product ranking

### Customer Segmentation

* High / Medium / Low value users

---
