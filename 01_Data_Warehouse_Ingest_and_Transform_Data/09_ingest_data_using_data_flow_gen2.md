# 🌐 Ingest Data Using Dataflow Gen2

## 🔍 What is Dataflow Gen2?

- **Dataflow Gen2** is a visual data transformation tool available in **Microsoft Fabric** and **Power BI**.
- It allows you to ingest, clean, transform, and load data using **Power Query (M language)** in the cloud.
- Supports **no-code/low-code** ETL and **data prep** for both **BI** and **data science workloads**.

---

## 🧰 Where is it Used?

| Platform          | Purpose                                |
|-------------------|----------------------------------------|
| **Microsoft Fabric** | Unified data ingestion & transformation |
| **Power BI Service** | Reusable data prep for reports         |

---

## 🔁 When to Use

- To **ingest data from multiple sources** visually
- To **transform data** before loading into Lakehouse or Warehouse
- For **lightweight ETL** tasks where Power Query is sufficient
- When you need **reuse and sharing** of transformations

---

## 🧱 Dataflow Gen2 Key Features

| Feature                | Description                                       |
|------------------------|---------------------------------------------------|
| **No-code Interface**  | Drag-and-drop steps via Power Query editor        |
| **Multiple Sources**   | Connects to SQL, Excel, CSV, SharePoint, REST API |
| **Lakehouse Integration** | Output directly to Fabric Lakehouse or Warehouse |
| **Scheduled Refresh**  | Set auto-refresh for periodic data ingestion      |
| **Reusability**        | One Dataflow can feed multiple reports or models  |

---

## 🔄 Example Workflow: Load Data to Fabric Lakehouse

1. Go to **Microsoft Fabric → Dataflows (Gen2)**
2. Click **New Dataflow Gen2**
3. Choose a **data source** (e.g., Excel, SQL Server, Azure Blob)
4. Use **Power Query editor** to transform data:
   - Filter rows
   - Merge or join tables
   - Rename columns
   - Change data types
5. Choose **destination**: Lakehouse, Warehouse, or Power BI dataset
6. **Save & refresh** the dataflow manually or on a schedule

---

## 🧪 Example Use Case

> A business team wants to combine Excel and SharePoint data into a Lakehouse table:

- Source 1: Excel file from OneDrive
- Source 2: SharePoint list with product metadata
- Clean both datasets in **Dataflow Gen2**
- Merge and transform using Power Query
- Output the final result to a **Fabric Lakehouse table**

---

## 🧠 Key Concepts to Remember

| Term               | Description                                         |
|--------------------|-----------------------------------------------------|
| **Dataflow Gen2**   | Modern, cloud-first Power Query for Fabric & Power BI |
| **Power Query**     | Visual editor for filtering, shaping, and combining data |
| **Destination**     | Where data is saved (e.g., Lakehouse, Warehouse)   |
| **Refresh**         | Auto-update mechanism for loading new data         |
| **Dataflow**        | Reusable transformation pipeline                   |

---

## 📌 Exam Tips

- Know that **Dataflow Gen2 is for transformation & ingestion**
- Understand how to **connect sources** and **set outputs**
- Be familiar with **Power Query steps** like filter, join, split, etc.
- Expect conceptual questions on **schedule refresh**, **source types**, and **destinations**
