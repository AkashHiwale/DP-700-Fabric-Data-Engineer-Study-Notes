# 🔄 Ingest Data Using Data Pipelines

## 🔍 What is a Data Pipeline?

- A **data pipeline** is a sequence of steps that automate the **movement**, **transformation**, and **loading** of data from one system to another.
- Commonly used for **ETL** (Extract, Transform, Load) or **ELT** (Extract, Load, Transform) processes.

---

## 🚀 Why Use Pipelines?

- Automate data ingestion from multiple sources
- Schedule data movement and processing
- Apply transformations and cleaning before storing
- Orchestrate complex workflows using control flows

---

## 🧰 Azure Tools for Pipelines

| Tool                        | Purpose                                      |
|-----------------------------|----------------------------------------------|
| **Azure Data Factory (ADF)**| Cloud-based ETL/ELT tool for data pipelines  |
| **Azure Synapse Pipelines** | Built-in orchestration engine in Synapse     |
| **Microsoft Fabric Pipelines** | Modern unified data engineering pipelines |

---

## 🧱 Components of a Pipeline

| Component      | Description                                                        |
|----------------|--------------------------------------------------------------------|
| **Pipeline**   | The container that holds all steps (activities)                    |
| **Activity**   | A single task (e.g., copy data, run a stored proc, execute script) |
| **Dataset**    | Metadata for input/output data (e.g., a folder or table)           |
| **Linked Service** | Connection info for source/destination systems              |
| **Trigger**    | Starts the pipeline (e.g., schedule, event, manual)                |
| **Integration Runtime** | Infrastructure used to perform data movement            |

---

## 🔄 Example Workflow

> Ingest CSV data from Azure Blob Storage to Azure SQL Database using a pipeline:

1. Create **Linked Services** for Blob and SQL DB
2. Define a **Dataset** for the CSV file and SQL table
3. Add a **Copy Data Activity** in the pipeline
4. Configure **mapping**, file path, and schema
5. Add a **Trigger** to schedule or run on demand

---

## 🧪 Example Use Case in Synapse

- Ingest IoT sensor data from Data Lake to Synapse table daily
- Steps:
  - Extract raw Parquet files from Data Lake
  - Load into staging table using Copy Activity
  - Run transformation using SQL script or Data Flow
  - Store final data in curated warehouse

---

## 📌 Supported Sources and Destinations

- **Sources**: Blob Storage, Data Lake, SQL Server, REST APIs, etc.
- **Destinations**: Azure SQL DB, Synapse, Cosmos DB, Dataverse, etc.

---

## ⚙️ Monitoring and Logging

- Use **Pipeline Monitoring Pane** for execution status
- View **output logs**, **errors**, and **data metrics**
- Set up **alerts** for failures or performance issues

---

## 🧠 Key Concepts to Remember

| Term               | Description                                        |
|--------------------|----------------------------------------------------|
| **ETL**            | Extract → Transform → Load                         |
| **ELT**            | Extract → Load → Transform                         |
| **Copy Activity**  | Moves data from source to sink                     |
| **Data Flow**      | Visual, code-free transformation layer             |
| **Trigger**        | Event or schedule that starts pipeline             |

---

## 📌 Exam Tips

- Know the difference between **pipeline**, **dataset**, and **linked service**
- Be able to identify when to use **Copy Activity** vs **Data Flow**
- Understand ETL vs ELT patterns and when each is used
- Expect questions about setting up and monitoring pipeline activities
