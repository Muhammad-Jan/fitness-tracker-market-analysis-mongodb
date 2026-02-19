# Fitness Tracker Market Analysis (MongoDB)

## Project Overview
This project demonstrates a **complete NoSQL database design and analytical implementation** using MongoDB for fitness tracker and smartwatch market analysis.

The objective is to develop a **scalable, flexible, and performance-optimized document-oriented database solution** capable of handling semi-structured product data while enabling efficient aggregation and business insight generation.

The project highlights:

- NoSQL database design (Document Model)
- JSON data import and transformation
- Business-driven MongoDB queries
- Aggregation framework usage
- Query performance optimization with indexing
- Professional documentation and reporting

---

## Business Problem

A wearable technology analytics client required a system to analyze product-level data for fitness trackers and smartwatches.

### Key Challenges:

- Difficulty identifying top-performing brands  
- No clear device-type distribution insights  
- Manual filtering of battery-life-based promotions  
- Lack of scalable database system for growing product catalog  
- Performance issues in large dataset querying  

**Solution:**  
Implement a MongoDB document database to centralize product data, enable flexible schema management, and perform optimized analytical queries.

---

## Dataset Description

- **Dataset:** [`D597 Task 1 Dataset 1_Fitness_trackers.csv`](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/blob/main/D597%20Task%201%20Dataset%201_Fitness_trackers.csv)  
- **Total Records:** 566  
- **Database:** `D597_Task_2`  
- **Collection:** `fitness_trackers`

### Key Attributes:

| Field | Description |
|-------|------------|
| `Brand Name` | Product manufacturer |
| `Device Type` | Smartwatch / Fitness Band |
| `Model Name` | Product model |
| `Selling Price` | Discounted price |
| `Original Price` | Original market price |
| `Display` | Screen specification |
| `Rating (Out of 5)` | Customer rating |
| `Strap Material` | Material type |
| `Average Battery Life (days)` | Battery duration |
| `Reviews` | Customer reviews count |

---

## Implementation Details

### 1️⃣ Database Creation

- **Database:** `D597_Task_2`  
- **Collection:** `fitness_trackers`  
- **Document-based storage model (BSON)**

``` create a collection
use D597_Task_2
db.createCollection("fitness_trackers")


## 2️⃣ Data Import & 3️⃣ MongoDB Analytical Queries

### Data Import

- CSV converted to JSON format  
- Imported via MongoDB Compass  
- Verified document integrity and structure  

### MongoDB Analytical Queries

Business-driven queries implemented:

- 📊 **Average rating by brand** (`$group` & `$avg`)  
- 📈 **Device type distribution analysis**  
- 🔋 **Filtering devices with battery life ≥ 14 days**  
- ⭐ **Top-rated product identification**  
- 💰 **Price comparison insights**  

📜 **All Queries:** [`mongo_queries.txt`](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/blob/main/mongo_queries.txt)  
📷 **Query Execution Screenshots:** [`Mongosh_Quries_pics`](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/tree/main/Mongosh_Quries_pics)  

---

### ⚡ Query Optimization

**Performance Analysis Using:** `.explain("executionStats")`  

**Before Indexing:**

- Collection Scan (COLLSCAN)  
- Higher execution time  
- Large number of documents examined  

**Indexes Applied:**

``` Index Quries
db.fitness_trackers.createIndex({ "Brand Name": 1 })
db.fitness_trackers.createIndex({ "Rating (Out of 5)": -1 })

## After Indexing

- **Index Scan (IXSCAN)**  
- Reduced execution time  
- Improved scalability  
- Optimized query execution plan  

---

### 🔒 Privacy & Security Considerations

Although this dataset contains product data only, enterprise deployment should include:

- Role-Based Access Control (RBAC)  
- Authentication & Authorization  
- TLS/SSL encrypted connections  
- Backup and disaster recovery strategy  
- Field-level encryption (if sensitive fields added)  

---

### 🛠 Scalability Strategy

MongoDB supports horizontal scaling via sharding.  
Project design supports:

- Flexible schema updates  
- Growing product catalog  
- Distributed architecture  
- Aggregation framework efficiency  
- Index-based query acceleration  

---

### 💻 Technical Environment

- **Database:** MongoDB (NoSQL)  
- **Query Language:** MongoDB Query Language (MQL)  
- **Tools Used:** MongoDB Compass & Mongosh  
- **Data Format:** CSV → JSON  
- **Documentation:** Word & PPTX  

---

### 🧠 Key Learning Outcomes

- Document-oriented data modeling  
- Aggregation framework implementation  
- Query performance analysis using execution stats  
- Indexing strategies in NoSQL systems  
- Scalable semi-structured data management  
- Business insight generation from product datasets  

---

### 📂 Project Files

- 📄 [MongoDB Project Documentation.docx](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/blob/main/MongoDB%20Project%20Documentation.docx)  
- 📊 [Problem Statement Presentation](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/blob/main/Problem%20Statement.pptx)  
- 📊 [PRESENTATION OF Fitness Trackers.pptx](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/blob/main/PRESENTATION%20OF%20Fitness%20Trackers.pptx)  
- 📜 [MongoDB Queries File](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/blob/main/mongo_queries.txt)  
- 📷 [Query Execution Screenshots Folder](https://github.com/Muhammad-Jan/fitness-tracker-market-analysis-mongodb/tree/main/Mongosh_Quries_pics)  

---

### 👨‍💻 Author

**Muhammad**  
*Data Analyst | SQL | MongoDB | NoSQL | Database Design | Data Analytics*
