# 🏢 Data Warehouse

## 🔍 What is a Data Warehouse?

- A **data warehouse** is a centralized repository that stores structured data from multiple sources.
- Used for **reporting**, **business intelligence (BI)**, and **data analysis**.
- Optimized for **read-heavy** operations (not for frequent updates like OLTP systems).

---

## 🧠 Key Characteristics

- **Historical data storage** (usually large volumes)
- **OLAP** (Online Analytical Processing) optimized
- Supports **complex queries** and aggregations
- Typically follows a **star or snowflake schema**

---

## 📌 Azure Services for Data Warehousing

| Service                        | Description                                                 |
|-------------------------------|-------------------------------------------------------------|
| **Azure Synapse Analytics**   | Microsoft’s enterprise data warehouse and analytics platform|
| **Dedicated SQL Pool**        | Scalable analytics DB inside Synapse (formerly SQL DW)      |
| **Serverless SQL Pool**       | Pay-per-query model for ad-hoc querying                     |
| **Azure Data Factory**        | ETL (Extract-Transform-Load) orchestration tool             |
| **Azure Data Lake Gen2**      | Stores raw/semi-structured/structured data                  |
| **Power BI**                  | Data visualization and dashboarding tool                   |

---

## 📦 Architecture Overview

1. **Data Ingestion**: Bring in data from various sources (Azure Data Factory, Event Hubs, etc.)
2. **Data Storage**:
   - Raw data in **Data Lake Storage**
   - Curated, structured data in **Synapse Dedicated SQL Pool**
3. **Data Processing**:
   - Use **SQL**, **Spark**, or **Synapse Pipelines**
4. **Visualization**:
   - Use **Power BI** or **Excel** to analyze and visualize the data

---

## 🧪 Example Use Case

> A retail company wants to analyze monthly sales trends from multiple regions:

- Ingest sales data from stores using **Azure Data Factory**
- Store raw data in **Data Lake Gen2**
- Clean and transform it using **Synapse Pipelines**
- Load curated data into **Dedicated SQL Pool**
- Visualize trends using **Power BI**

---

## 🧠 Key Concepts to Remember

| Term              | Meaning                                                   |
|-------------------|-----------------------------------------------------------|
| **ETL**           | Extract, Transform, Load – used in traditional warehouses |
| **ELT**           | Extract, Load, Transform – used in modern cloud patterns  |
| **Star Schema**   | Central fact table with surrounding dimension tables      |
| **Snowflake Schema** | Normalized version of star schema                      |
| **Partitioning**  | Improves query performance by splitting large tables      |
| **PolyBase**      | Query external files (CSV, Parquet, etc.) directly        |

---

## 📌 Exam Tips

- Know when to use **Dedicated SQL Pool** vs **Serverless SQL Pool**
- Understand the **ETL vs ELT** processes
- Be clear on **star** and **snowflake** schema designs
- Remember which services do **ingestion**, **processing**, and **visualization**
