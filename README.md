# PL/SQL Window Functions – Assignment I

**Course:** Database Development with PL/SQL (INSY 8311)  
**Instructor:** Eric Maniraguha  
**Student:** Uwitonze Pacific  
**Date:** September 2025  

---

## 📌 Business Problem
A retail company operating across multiple regions wants to analyze customer behavior and product performance. They face challenges in identifying top products, tracking sales trends, and segmenting customers for targeted marketing.  

**Expected Outcome:**  
Provide insights on top products per region, sales growth trends, and customer segmentation using PL/SQL window functions.  

---

## 🎯 Success Criteria
1. Top 5 products per region/quarter → `RANK()`
2. Running monthly sales totals → `SUM() OVER()`
3. Month-over-month growth → `LAG()` / `LEAD()`
4. Customer quartiles → `NTILE(4)`
5. 3-month moving averages → `AVG() OVER()`

---

## 🗄️ Database Schema
### Tables
- **Customers**: customer_id (PK), name, region  
- **Products**: product_id (PK), name, category  
- **Transactions**: transaction_id (PK), customer_id (FK), product_id (FK), sale_date, amount  

![ER Diagram](screenshots/er_diagram.png)

---

## 🧑‍💻 Window Functions Implementation
Queries are in `queries/window_functions.sql`.  

Each query includes:
- SQL code  
- Screenshot of output (in `screenshots/`)  
- Interpretation  

---

## 📊 Results Analysis
**Descriptive:**  
- Customers in Kigali region show higher frequency of purchases in beverages.  
- Top 5 products are consistent across quarters with minor seasonal variations.  

**Diagnostic:**  
- Beverages dominate because of recurring consumption.  
- Growth slows in Q2 due to fewer promotions.  

**Prescriptive:**  
- Increase Q2 promotions.  
- Focus marketing on loyal beverage customers.  
- Segment high-value customers for retention campaigns.  

---

## 📚 References
1. Oracle Documentation – Window Functions  
2. Oracle SQL Tutorial – Analytics and Ranking  
3. GeeksforGeeks – SQL Window Functions  
4. W3Schools – SQL Analytics  
5. TutorialsPoint – PL/SQL Guide  
6. DatabaseJournal – SQL Window Functions Explained  
7. StackOverflow – Practical PL/SQL Questions  
8. TowardsDataScience – SQL Analytics  
9. Academic Paper: SQL Analytics in Business  
10. Oracle Live SQL Examples  

---

## ✅ Integrity Statement
All sources were properly cited. Implementations and analysis represent original work.  
No AI-generated content was copied without attribution or adaptation.  

---
