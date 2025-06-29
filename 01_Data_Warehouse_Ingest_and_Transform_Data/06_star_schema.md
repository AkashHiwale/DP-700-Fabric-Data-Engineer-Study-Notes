# ⭐ Star Schema

## 🔍 What is a Star Schema?

- A **star schema** is a type of **data warehouse schema** that organizes data into:
  - A **central fact table** (quantitative data)
  - Multiple **dimension tables** (descriptive data)

- The layout **resembles a star**, with the fact table at the center and dimension tables surrounding it.

---

## 🧠 Key Characteristics

- **Denormalized** dimension tables (few joins, faster queries)
- Optimized for **OLAP (Online Analytical Processing)**
- Used for **reporting and analysis** in tools like Power BI
- Simple and intuitive for business users

---

## 📦 Structure

- **Fact Table**:
  - Contains measurable data (e.g., revenue, quantity)
  - Has **foreign keys** to dimension tables

- **Dimension Tables**:
  - Contain descriptive attributes (e.g., product name, region)
  - Join to the fact table through **primary keys**

---

## 🧾 Example Layout

### Fact Table: `SalesFact`

| sale_id | date_key | product_key | store_key | amount |
|---------|----------|-------------|-----------|--------|
| 1       | 20240101 | 1001        | 10        | 500.00 |

### Dimension Tables:

- `DateDim`: date_key, day, month, year
- `ProductDim`: product_key, product_name, category
- `StoreDim`: store_key, store_name, region

---

## 📈 Benefits

- Fast query performance (due to denormalized structure)
- Easy to understand and model
- Simplifies **aggregations and filtering**

---

## ⚠️ Limitations

- **Data redundancy** in dimension tables
- Updates to dimension data can be complex
- Not ideal when dimensions have complex hierarchies (use snowflake instead)

---

## 🧠 Key Concepts to Remember

| Term                | Description                                    |
|---------------------|------------------------------------------------|
| **Fact Table**       | Contains numeric metrics and foreign keys      |
| **Dimension Table**  | Contains descriptive data                      |
| **Denormalization**  | Repetition of data to optimize performance     |
| **Star Schema**      | Central fact table linked to dimension tables  |

---

## 📌 Exam Tips

- Know how to identify a **star schema layout**
- Understand differences between **star** and **snowflake**
- Be able to explain why star schema is good for **OLAP and BI**
- Expect questions about **performance, structure, and use cases**
