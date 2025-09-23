##STUDENT AND COURSE INFORMATION

PL/SQL Window Functions Mastery Project.

Course: Database Development with PL/SQL (INSY 8311). 

Student: Uwitonze Pacific.

Instructor: Eric Maniraguha.

student id: 26893.

Date: September 2025.

> ### Project Report
> For a comprehensive review of this assignment, please see the full report document located in the `/report` directory. It contains all commented queries, high-resolution screenshots, and detailed interpretations.

##Business Problem
This project addresses a business problem for a Rwandan retail company to provide data-driven insights for strategic decisions.
  1.Business Context: A retail sales company with branches in Kigali, Huye, and Musanze, specializing in beverages, food, and household items. 
  
  2.Data Challenge: Management needs to analyze customer purchasing behavior and sales performance to identify top products, track growth patterns, and effectively segment             customers for targeted promotions. 
  
  3.Expected Outcome: To leverage PL/SQL window functions to deliver actionable insights on regional product performance, monthly revenue trends, and customer value                    segmentation. 

  
##Success Criteria
The analysis is guided by five specific, measurable goals: 

Identify the top  products per region/quarter using RANK().

Track running monthly sales totals using SUM() OVER().

Analyze month-over-month growth using LAG() / LEAD().

Segment customers into spending quartiles using NTILE(4).

Calculate 3-month moving averages to identify trends using AVG() OVER().


 ##Database Schema
The database is designed in Third Normal Form (3NF) to ensure data integrity and consists of three related tables.

customers: Stores unique customer information.

<img width="935" height="80" alt="image" src="https://github.com/user-attachments/assets/60f36b57-c39e-4b9e-a225-bddcbdb2c480" />


products: Contains the product catalog.

<img width="925" height="115" alt="image" src="https://github.com/user-attachments/assets/d8b07389-3ec8-41bb-a1de-1438b927f5a7" />

transactions: Records all sales and links customers and products via foreign keys.

<img width="975" height="196" alt="image" src="https://github.com/user-attachments/assets/89ab32bd-c6f6-48af-bc60-c2223eff2e1d" />

The following images shows how we inserted data in created tables which are  customers, products and transactions 

<img width="975" height="492" alt="image" src="https://github.com/user-attachments/assets/39003e4d-e30f-4dcf-9621-5548e17ed4cb" />

<img width="975" height="538" alt="image" src="https://github.com/user-attachments/assets/63b06736-dfbc-4da0-b127-791fa54aeb35" />

<img width="975" height="491" alt="image" src="https://github.com/user-attachments/assets/c7287b2c-090b-4949-a47d-a355f2725737" />

ER diagram
This ER diagram models the retail sales database, showing how the CUSTOMERS and PRODUCTS tables connect to a central TRANSACTIONS table through one-to-many relationships enforced by primary and foreign keys. 

<img width="975" height="512" alt="image" src="https://github.com/user-attachments/assets/92879267-8e8f-4a26-be51-990d2f76e2df" />

##Window Functions Implementation

I have implemented the 4 categories of window functions. Include query, screenshot, and interpretation

A. Ranking Functions

<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/25bc4ef1-6897-4025-b85b-9a4f93142fc0" />

Interpretation:
This query provides a comprehensive ranking of customers by their total spending. Reece James is clearly the top customer. The different functions (ROW_NUMBER, RANK, etc.) offer various ways to view this ranking, which is essential for identifying high-value customers for loyalty programs.

B. Aggregate Functions

<img width="975" height="570" alt="image" src="https://github.com/user-attachments/assets/fc204a03-0af8-4690-bc88-61bfd43146b0" />

Interpretation:
This query is excellent for trend analysis. The running total shows the cumulative revenue growth in each region. The two days moving avg helps to smooth out daily fluctuations, giving a clearer view of recent sales performance.

C. Navigation Functions

<img width="975" height="557" alt="image" src="https://github.com/user-attachments/assets/14605fde-1f59-43bc-b5af-e7b53a69fe89" />

<img width="975" height="545" alt="image" src="https://github.com/user-attachments/assets/ab3bdce7-9db8-49cb-902f-d23455a1b426" />

Interpretation:
This analysis is vital for performance reviews. It clearly shows that the Kigali region recovered from a -60% drop in July with a strong 150% growth in August. The LEAD function also helps with forecasting by showing the subsequent month's performance.

D. Distribution Functions

<img width="975" height="762" alt="image" src="https://github.com/user-attachments/assets/70771d87-98be-48b6-8497-fb2038930952" />


Interpretation:
The NTILE (4) function divides customers into four distinct segments. The top two customers fall into Quartile 1, representing the highest-spending group. The CUME_DIST shows that the top 43% of customers (tiers 1 and 2) generate the majority of the revenue, allowing marketing to focus its efforts effectively.

##Results Analysis
Descriptive (What happened?): The analysis revealed that customer value is highly concentrated, with the top customer, Reece James, contributing significantly more revenue (65,000 RWF). Sales performance varies dramatically by region; the Huye region showed strong month-over-month growth, while Kigali experienced more volatility.

Diagnostic (Why?): The revenue concentration is likely due to repeat, high-value purchases from loyal customers. The sales growth in Huye could be attributed to successful local marketing, while volatility in other regions may be due to seasonal factors or inconsistent promotions.

Prescriptive (What next?): The business should implement a loyalty program to retain top-quartile customers. Furthermore, they should analyze the successful strategies in Huye to replicate them in other regions and launch targeted promotions for lower-spending customer segments.

 ##References
Oracle Corporation. (2025). Database SQL Language Reference: Analytic Functions.

Maniraguha, E. (2025). Lecture 01 - Introduction to SQL Command Basics (Recap).

Ben-Gan, I. (2019). T-SQL Window Functions: For data analysis and beyond.

GeeksforGeeks. (2024). SQL | Window Functions.

Khandelwal, P. (2022). Practical SQL for Data Analysis.

SQLShack. (2021). Overview of SQL RANK functions.

DataCamp. (2024). SQL Window Functions Tutorial.

Essential SQL. (2023). SQL Window Functions Introduction.

W3Schools. (2025). SQL Window Functions.

TowardsDataScience. (2023). The Simple Yet Powerful SQL Window Function.








