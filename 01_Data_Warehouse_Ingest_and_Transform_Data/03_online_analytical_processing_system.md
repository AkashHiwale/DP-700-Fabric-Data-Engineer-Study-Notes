# 📊 Online Analytical Processing System (OLAP)

## 🔍 What is OLAP?

- **OLAP (Online Analytical Processing)** is used for **analyzing large volumes of data**.
- Enables users to perform **multi-dimensional analysis** of business data.
- Common in scenarios like **reporting**, **dashboarding**, and **data exploration**.

---

## 🧠 Key Characteristics of OLAP Systems

- Supports **complex queries**, aggregations, and summaries
- Data is **read-heavy** (low updates)
- Uses **denormalized schemas** (star or snowflake schema)
- Ideal for **decision support** and **historical trend analysis**

---

## 📌 OLTP vs OLAP Comparison

| Feature                 | OLTP                              | OLAP                              |
|------------------------|-----------------------------------|-----------------------------------|
| Purpose                | Day-to-day transactions           | Data analysis and reporting       |
| Query Type             | Simple (INSERT/UPDATE)            | Complex (JOIN, GROUP BY, etc.)    |
| Schema Design          | Normalized                        | Denormalized                     |
| Response Time          | Fast for write operations         | Fast for large reads              |
| Data Volume            | Operational data                  | Historical data (big volumes)     |
| Example                | Bank transaction                  | Sales summary over months         |

---

## 🧰 Common Azure Services for OLAP

| Service                        | Purpose                                           |
|-------------------------------|---------------------------------------------------|
| **Azure Synapse Analytics**   | Main OLAP platform – handles large-scale queries  |
| **Azure Data Lake Gen2**      | Stores raw/semi-structured analytical data        |
| **Power BI**                  | Creates reports/dashboards from OLAP data         |
| **Azure Analysis Services**   | Multi-dimensional models for OLAP analysis        |
| **Serverless SQL Pool (Synapse)** | Used for querying big data files ad-hoc       |

---

## 🧪 Example Use Case

> A retail company wants to analyze last year’s sales by region and product category:

- Raw data is ingested into **Azure Data Lake Gen2**
- Transformed and loaded into **Synapse Analytics**
- A **Power BI** dashboard is built to slice data by:
  - Region
  - Time period
  - Product line
- Business users interactively analyze sales patterns

---

## 🧠 Key Concepts to Remember

| Term                  | Description                                                |
|-----------------------|------------------------------------------------------------|
| **Star Schema**       | Fact table connected to dimension tables                   |
| **Snowflake Schema**  | Normalized form of star schema                             |
| **Aggregations**      | Pre-computed summaries for faster analysis                 |
| **Cube**              | Multi-dimensional data model (used in Analysis Services)   |
| **Drill-down**        | Navigating from summary to detailed data                   |
| **Slice and Dice**    | Viewing data from different angles (e.g., by time, region) |

---

## 📌 Exam Tips

- Know which Azure services support **OLAP workloads**
- Be clear on **star vs snowflake** schema differences
- Understand **data flow** from ingestion to dashboarding
- Know how **Power BI**, **Synapse**, and **Data Lake** work together
- Expect conceptual questions around **data modeling** and **aggregation**
