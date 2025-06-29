# 💻 Online Transaction Processing System (OLTP)

## 🔍 What is OLTP?

- **OLTP (Online Transaction Processing)** is a type of data processing that manages real-time transaction data.
- Common in applications like **banking**, **e-commerce**, **inventory**, and **order processing**.
- Designed for **high-speed**, **high-volume**, and **low-latency** transactions.

---

## 🧠 Key Characteristics of OLTP Systems

- Handles a **large number of short, atomic transactions**
- **Highly normalized** schema to reduce redundancy
- **Real-time processing** with rapid query and update capability
- Focused on **data integrity** and **concurrency control**

---

## 📌 Differences Between OLTP and OLAP

| Feature                 | OLTP                              | OLAP                              |
|------------------------|-----------------------------------|-----------------------------------|
| Purpose                | Transactional processing          | Analytical processing             |
| Data Structure         | Highly normalized                 | Denormalized (star/snowflake)     |
| Operations             | INSERT, UPDATE, DELETE            | SELECT (complex queries)          |
| Speed                  | Fast for read/write               | Optimized for complex reads       |
| Data Volume            | Smaller transactions              | Large datasets                    |
| Examples               | ATM, e-commerce checkout          | Sales reporting, dashboarding     |

---

## 🧰 Common Azure Services for OLTP

| Service                      | Purpose                                      |
|-----------------------------|----------------------------------------------|
| **Azure SQL Database**      | Managed relational database for OLTP workloads |
| **Azure Cosmos DB**         | Globally distributed NoSQL database          |
| **Azure Database for MySQL/PostgreSQL** | OLTP for open-source RDBMS            |
| **Azure Database for MariaDB** | Another option for structured OLTP data   |

---

## 🧪 Example Use Case

> An e-commerce website processes customer orders:

- When a customer places an order:
  - The system inserts a new **Order** record into Azure SQL Database
  - Updates **Inventory** records
  - Triggers a **transaction log**
- This is done with **ACID** (Atomicity, Consistency, Isolation, Durability) compliance

---

## 🧠 Key Concepts to Remember

| Concept         | Description                                                  |
|----------------|--------------------------------------------------------------|
| **ACID**        | Properties ensuring safe transactions                        |
| **Atomicity**   | All steps in a transaction succeed or fail together         |
| **Normalization** | Organizing data to reduce duplication                     |
| **Concurrency Control** | Managing multiple users accessing the same data     |
| **Latency**     | Time taken to process a transaction                         |

---

## 📌 Exam Tips

- Understand use cases for **OLTP vs OLAP**
- Know Azure services that support **OLTP workloads**
- Be familiar with **ACID principles** and **normalization**
- Identify when to use **Cosmos DB** vs **SQL Database** for transactional needs
