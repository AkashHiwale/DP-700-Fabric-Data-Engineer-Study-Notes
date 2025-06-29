# 🔑 Alternate Key and Surrogate Key

## 🧩 What is a Key?

- A **key** uniquely identifies a record in a database table.
- In data warehousing, keys play a critical role in connecting **fact** and **dimension** tables.

---

## 🔁 Surrogate Key

### ✅ Definition:
- A **system-generated unique identifier** used as the **primary key** in a table.
- Usually has **no business meaning**.

### 🔑 Characteristics:
- Often implemented as an **auto-incremented integer**
- Acts as a **substitute** for a natural (business) key
- Improves performance and avoids complications from changes in natural keys

### 🧾 Example:
| product_sur_key | product_id | product_name |
|------------------|------------|---------------|
| 101              | P001       | T-shirt        |
| 102              | P002       | Shoes          |

> `product_sur_key` is the **surrogate key**

### 📌 Use Cases:
- In **dimension tables** for better join performance
- When **natural keys can change** (e.g., customer email)
- To ensure **uniqueness** when combining multiple systems

---

## 🔁 Alternate Key

### ✅ Definition:
- A **candidate key** that can uniquely identify a record, but is **not used as the primary key**.
- Provides a **second way** to identify a record.

### 🔑 Characteristics:
- Has **business meaning**
- Can be used for **lookup or validation**
- Declared as **unique** in the database

### 🧾 Example:
| customer_key | email_id           | phone_number   |
|--------------|--------------------|----------------|
| 2001         | john@example.com   | 9999988888     |

> `email_id` and `phone_number` can be **alternate keys**

---

## 🔍 Comparison Table

| Feature              | Surrogate Key                 | Alternate Key                        |
|----------------------|-------------------------------|--------------------------------------|
| Meaning              | System-generated, no meaning  | Business-defined, meaningful         |
| Used as Primary Key  | Yes                           | No (but could have been)             |
| Stability            | Never changes                 | May change (e.g., email, phone)      |
| Type                 | Integer/UUID                  | Email, Code, Phone, etc.             |
| Use Case             | Joins, performance            | Uniqueness, validation               |

---

## 🧠 Key Concepts to Remember

| Term              | Description                                 |
|-------------------|---------------------------------------------|
| **Surrogate Key**  | Unique ID with no business meaning          |
| **Alternate Key**  | A candidate key not used as primary         |
| **Natural Key**    | A key derived from business data (e.g., SSN)|
| **Primary Key**    | Main unique identifier for a table          |

---

## 📌 Exam Tips

- Surrogate keys are best for **dimension tables** to handle SCD (Slowly Changing Dimensions)
- Alternate keys are helpful for **ensuring uniqueness** and **validating business rules**
- Understand when to choose surrogate vs natural/alternate keys in **data modeling**
