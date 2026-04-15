# 🚀 Project O.R.A – Oracle Retail Analytics  
### End-to-End ETL Pipeline using IICS

---

## 📌 Overview  
Project O.R.A is an end-to-end ETL pipeline built using Informatica Intelligent Cloud Services (IICS).  
It extracts retail data from CSV files, transforms it using business logic, and loads it into an Oracle Data Warehouse with automated taskflow orchestration.

---

## 🎯 Objectives  
- Build a scalable ETL pipeline  
- Perform data cleaning, transformation, and aggregation  
- Implement Taskflow orchestration with dependency handling  
- Ensure data consistency using Full Refresh strategy  

---

## 🏗️ Architecture  

**Mappings:**  
`m_Store_Load` | `m_Product_Load` | `m_Sales_Fact_Load`  

**Taskflow:**  
Start → Store → Product → Decision → Sales → Notification → End  

---

## ⚙️ Tech Stack  
- Informatica IICS  
- Oracle Database  
- SQL  
- CSV (Flat Files)  

---

## 🔄 ETL Pipeline  

### Extract  
- Store Data  
- Product Data  
- Sales Transactions  

### Transform  
- Add `LOAD_DATE`  
- Filter products (`BASE_PRICE > 500`)  
- Lookup for data enrichment  
- Standardization using UPPERCASE  
- Aggregation to calculate `TOTAL_REVENUE`  

### Load  
- DIM_STORE  
- DIM_PRODUCT  
- FACT_SALES  
- Full Refresh (TRUNCATE & LOAD)  

---

## ⚠️ Challenges & Solutions  

| Challenge | Solution |
|----------|---------|
| ORA-02266 (Foreign Key issue) | Maintained correct load order (FACT → DIM) |
| Date format errors | Applied data type conversions |
| Invalid/dirty data | Used filtering and validation |

---

## ✅ Results  
- Processed 100+ records  
- Cleaned and validated data  
- Fully automated ETL pipeline  
- Ensured data consistency  

---

## 💡 Key Learnings  
- ETL pipeline design in IICS  
- Lookup and Aggregator transformations  
- Taskflow orchestration  
- Handling real-world data issues  

---

## 📌 Conclusion  
This project demonstrates practical knowledge of:
- Data Engineering  
- ETL Pipeline Development  
- Data Warehousing  
- Workflow Automation  

---

## 👨‍💻 Author  
Alok Kumar Singh  
