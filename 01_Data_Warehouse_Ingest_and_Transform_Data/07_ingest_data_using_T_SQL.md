# 📥 Ingest Data Using T-SQL `COPY INTO` Command

## 🔍 What is `COPY INTO`?

- The `COPY INTO` command is a **T-SQL-based** method used in **Azure Synapse Analytics** and **Fabric Data Warehouse** to **ingest data** from external sources (like CSV/Parquet files) into a **table**.
- It supports **bulk loading** with **schema auto-detection** and **column mapping**.

---

## ✅ When to Use

- Load data from:
  - **Azure Data Lake Storage Gen2**
  - **Azure Blob Storage**
  - **OneLake (Microsoft Fabric)**
- Works well for:
  - One-time large data loads
  - Incremental ingestion in pipelines

---

## 🧾 Basic Syntax

```sql
COPY INTO [schema].[table_name]
FROM 'https://<storage-account>.dfs.core.windows.net/<container>/<folder>/'
WITH (
    FILE_TYPE = 'CSV',  
    CREDENTIAL = (IDENTITY = 'Managed Identity'),
    FIELDTERMINATOR = ',',
    ROWTERMINATOR = '\n',
    FIRSTROW = 2
);
```

---

## 🔧 Common Parameters

| Option              | Description                                         |
|---------------------|-----------------------------------------------------|
| `FILE_TYPE`         | 'CSV', 'PARQUET', 'JSON'                            |
| `CREDENTIAL`        | Use 'Managed Identity' or SAS/Storage key          |
| `FIELDTERMINATOR`   | Defines column separator in CSV                    |
| `ROWTERMINATOR`     | End-of-line character (`\n`, `\r\n`, etc.)         |
| `FIRSTROW`          | Row number to start reading data (useful for headers) |
| `MAXERRORS`         | Max number of rows that can fail before failing    |
| `ERRORFILE`         | Path to store rows that failed to load             |

---

## 📁 Example: Load from CSV in Azure Storage

```sql
COPY INTO dbo.SalesOrders
FROM 'https://mydatalake.dfs.core.windows.net/files/sales/'
WITH (
    FILE_TYPE = 'CSV',
    CREDENTIAL = (IDENTITY = 'Managed Identity'),
    FIELDTERMINATOR = ',',
    ROWTERMINATOR = '\n',
    FIRSTROW = 2
);
```

---

## 📁 Example: Load from OneLake in Microsoft Fabric

```sql
COPY INTO dbo.Products
FROM 'https://onelake.dfs.fabric.microsoft.com/myworkspace.myLakehouse/Files/products/'
WITH (
    FILE_TYPE = 'CSV',
    CREDENTIAL = (IDENTITY = 'Managed Identity'),
    FIRSTROW = 2
);
```

---

## 🧠 Best Practices

- Make sure **target table exists** before running `COPY INTO`
- Always **verify data formats** (CSV vs Parquet)
- Use `MAXERRORS` and `ERRORFILE` for debugging
- Prefer **Managed Identity** for secure access

---

## 📌 Exam Tips

- Understand the **syntax** and **supported file types**
- Know how to reference files in **Azure Data Lake** and **OneLake**
- Be familiar with **CREDENTIAL** and **FIRSTROW** options
- Practice writing a `COPY INTO` command with different file types
