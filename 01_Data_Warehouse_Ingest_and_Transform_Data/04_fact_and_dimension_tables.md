# 📂 Fact and Dimension Tables

## 🔍 What are Fact and Dimension Tables?

- These are core components of **data warehouse schemas** like **star** and **snowflake**.
- Used to organize data for **analytical processing (OLAP)**.

---

## 📊 Fact Table

### ✅ Definition:
- Contains **quantitative data** (measurable facts) related to business processes.
- Stores **metrics**, **measurements**, or **aggregates**.

### 🔑 Characteristics:
- Large table with **foreign keys** to dimension tables
- Data is **numeric and additive** (e.g., revenue, quantity)
- Can contain **aggregated values** by time, location, etc.

### 🧾 Examples:
- `SalesFact`: sales amount, units sold
- `OrderFact`: order total, shipping cost

| sale_id | date_key | product_key | store_key | amount  |
|---------|----------|-------------|-----------|---------|
| 1       | 20240601 | 101         | 12        | 500.00  |

---

## 📁 Dimension Table

### ✅ Definition:
- Contains **descriptive attributes** (textual/contextual data) about business entities.

### 🔑 Characteristics:
- Smaller than fact tables
- Each dimension has a **primary key** referenced by fact tables
- Used for **filtering**, **grouping**, **slicing/dicing** data

### 🧾 Examples:
- `ProductDim`: product name, category
- `DateDim`: calendar, fiscal details
- `StoreDim`: store name, region

| product_key | product_name | category  |
|-------------|--------------|-----------|
| 101         | T-shirt      | Apparel   |

---

## 🧱 Star Schema vs Snowflake Schema

| Feature            | Star Schema                     | Snowflake Schema                   |
|--------------------|----------------------------------|-------------------------------------|
| Structure          | Flat, denormalized              | Normalized (dimensions split)       |
| Query Performance  | Faster                          | Slightly slower due to joins        |
| Maintenance        | Simpler                         | More complex                        |

---

## 🧪 Use Case

> You want to analyze sales by product category and region:
- **Fact Table** stores: amount, quantity, product_key, store_key
- **Dimension Tables** store: product details and store regions
- Use SQL JOINs to link facts to dimensions for reports in **Power BI**

---

## 🧠 Key Concepts to Remember

| Concept           | Description                                    |
|-------------------|------------------------------------------------|
| **Fact Table**     | Contains numeric metrics, foreign keys         |
| **Dimension Table**| Descriptive info, joined to facts              |
| **Granularity**    | Level of detail in a fact table                |
| **Surrogate Key**  | Unique ID used instead of natural keys         |
| **Slowly Changing Dimension (SCD)** | Tracks historical changes in dimension data |

---

## 📌 Exam Tips

- Know the purpose and examples of fact vs dimension tables
- Be able to identify them in schema diagrams
- Understand how they relate in **star** and **snowflake schemas**
- Be familiar with **surrogate keys** and **SCD types**
