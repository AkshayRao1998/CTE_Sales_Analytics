# 📊 SQL Project: Customer & Sales Analysis Using CTEs

## 📌 Project Overview

This project demonstrates practical usage of **Common Table Expressions (CTEs)** to perform customer and sales analysis on the **AdventureWorksDW2025** database. The goal is to apply **Standalone, Multiple, and Nested CTEs** along with **window functions** to solve real-world business questions.

The project is designed to reflect **industry-level SQL practices** and is suitable for showcasing analytical SQL skills on GitHub or during technical interviews.

---

## 🛠️ Tools & Technologies

* **Database:** AdventureWorksDW2025
* **SQL Concepts Used:**

  * Standalone CTE
  * Multiple CTEs
  * Nested CTEs
  * Window Functions (ROW_NUMBER, RANK, LAG, NTILE)
  * Aggregations & CASE expressions

---

## 📂 Project Structure

```
CTE_Sales_Analysis/
│
├── 01_customer_summary.sql
├── 02_purchase_frequency.sql
├── 03_monthly_revenue_trend.sql
├── 04_top_customers.sql
├── 05_clv_segmentation.sql
└── README.md
```

---

## 🔍 Analysis Tasks & Explanations

### 1️⃣ Customer Order Summary (Standalone CTE)

**Objective:**
Summarize each customer’s purchase behavior.

**Key Metrics:**

* Total Orders
* Total Revenue
* First Order Date
* Last Order Date

**Approach:**
A single standalone CTE aggregates sales data at the `CustomerKey` level, ensuring **one row per customer**.

---

### 2️⃣ Customer Purchase Frequency Classification (Multiple CTEs)

**Objective:**
Classify customers based on how frequently they place orders.

**Segments:**

* One-Time Buyer
* Occasional Buyer
* Frequent Buyer

**Approach:**

* CTE 1 calculates total orders per customer
* CTE 2 applies business rules using `CASE WHEN` to segment customers

---

### 3️⃣ Monthly Revenue Trend Analysis (Nested CTEs)

**Objective:**
Analyze month-over-month revenue performance.

**Metrics:**

* Monthly Revenue
* Previous Month Revenue
* Revenue Difference
* Trend Indicator (Increase / Decrease)

**Approach:**

* Inner CTE aggregates monthly revenue
* Outer CTE uses `LAG()` window function to compare current and previous months

---

### 4️⃣ Top Customers by Revenue (CTE + Ranking)

**Objective:**
Identify top revenue-generating customers.

**Approach:**

* Aggregate total revenue per customer
* Apply `RANK()` window function
* Filter top 10 customers while handling ties correctly

---

### 5️⃣ Customer Lifetime Value (CLV) Segmentation (Advanced CTE)

**Objective:**
Segment customers based on lifetime revenue contribution.

**Segments:**

* High CLV
* Medium CLV
* Low CLV

**Approach:**

* Calculate total revenue per customer
* Use `NTILE(3)` to distribute customers into equal revenue-based segments
* Apply meaningful business labels using `CASE WHEN`

---

## 🎯 Key Learnings

* Clear separation of calculation and business logic using CTEs
* Correct usage of window functions on aggregated data
* Improved SQL readability and maintainability
* Business-oriented thinking in SQL analytics

---

## 🚀 How This Project Can Be Extended

* Convert queries to **PostgreSQL** syntax
* Visualize results using **Power BI / Tableau**
* Add customer demographic analysis
* Create stored views for reporting

---

## 👤 Author

**Akshay Rao**
SQL Developer | Data Analytics Enthusiast

---

✅ *This project reflects real-world SQL analytical workflows and demonstrates strong command over CTE-based query design.*
