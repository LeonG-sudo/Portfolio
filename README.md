# Work Experience Portfolio

## Student Loans Analytics — Access Database Project

**Quill Financial Services** | Academic Project (March 2025)

A Microsoft Access solution to import, model, query, and report on student-loan data for Quill Financial Services.

---

### 🚀 Project Overview

- **Goal:** Build a relational database to manage and analyze student-loan clients.
- **Data Sources:**  
  - `Clients.xlsx` (loan records)  
  - Pre-provided `Colleges` table
  - Not real numbers in this Portfilio (All Names and Numbers Are Made Up)

---

### 💼 My Responsibilities

1. **Data Import & Schema Design**  
   - Imported `Clients.xlsx` into an Access table; set `ClientID` as PK  
   - Adjusted field properties (data types, sizes, formats) for data integrity  

2. **Data Modeling**  
   - Established one-to-many relationship between `Clients` and `Colleges`  
   - Enforced referential integrity with cascade update/delete  

3. **Query Development**  
   - **2019 Graduates**: Filtered expected‐graduation = 2019; selected key client/contact fields  
   - **Loan Payments**: Used `Pmt()` to calculate 10-year, 5% monthly payments; formatted as currency; summarized averages  
   - **Loan Summary by College**: Count of loans and average loan amount per college  

4. **Form & Report Design**  
   - Built a **Split Form** for streamlined data entry; reordered fields; updated sample records  
   - Designed **Client Loans** report (landscape, grouped by graduation year, Integral theme) for executive print distribution  

5. **Presentation & Documentation**  
   - Provided screenshots and step-by-step instructions in project deliverables  
   - Documented all table modifications, query logic, and report formatting  

---

### 🛠 Technologies & Functions

- **Microsoft Access 2016+**  
- Data import features, Design view, Relationships window  
- VBA built-in functions: `Pmt(rate, nper, pv, fv, type)`  
- Layout & Presentation: Split Forms, Report Wizard, Themes  

---

### ▶️ How to Run

1. Clone this repo.  
2. Open `Advising Project` in Access.  
3. Review tables, queries, forms, and reports as per the instructions.  

---

### 📸 Screenshots


---
![image](https://github.com/user-attachments/assets/5a989989-0c80-4973-b9bc-1e742e5cc414)
![image](https://github.com/user-attachments/assets/78e98a42-6317-4fa9-bb20-6ec6cef56deb)
![image](https://github.com/user-attachments/assets/da3ad0cf-4dbe-4242-8dc1-be32bc25a486)


### ⚡️ Key Takeaways

- Solidified relational-database design and data-integrity best practices.  
- Automated financial calculations via Access queries.  
- Delivered polished, print-ready reports for stakeholders.


## Excel Project One

**Quill Financial Services** | Academic Project (Apr 2025)

An Excel workbook demonstrating advanced formula and function skills to automate inventory restocking logic, calculate costs, and parse text information for streamlined analysis.

---

## 🚀 Project Overview

- **Goal:** Build an Excel model to  
  1. Flag low-stock items for reorder  
  2. Compute per-line and total inventory costs  
  3. Extract and standardize product codes via text functions  
  4. Summarize key metrics with aggregate formulas  
- **Data Source:**  
  - `Functions.xlsx` (equipment inventory list)

---

## 💼 My Responsibilities

1. **Logic & Conditional Testing**  
   - In **F4**, used  
     ```excel
     =IF([@Stock]<15, "Order", "No Order")
     ```  
     to flag any item with stock below 15 for reorder; auto-filled through F62.

2. **Inventory Cost Calculations**  
   - In **G4**, set  
     ```excel
     =[@Quantity] * [@Cost_Each]
     ```  
     to calculate line-item cost; copied down to G62.  

3. **Text Extraction & Formatting**  
   - In **I4**, extracted the last 3 characters and capitalized them:  
     ```excel
     =PROPER(RIGHT([@ItemCode],3))
     ```  
   - In **J4**, took the first 2 characters as lowercase type codes:  
     ```excel
     =LOWER(LEFT([@ItemCode],2))
     ```  
   - In **K4**, grabbed the middle 4 characters as uppercase category codes:  
     ```excel
     =UPPER(MID([@ItemCode],3,4))
     ```  
   - Combined all parsed codes in **H4**:  
     ```excel
     =I4 & "-" & J4 & "-" & K4
     ```

4. **Aggregate & Conditional Summaries**  
   - **Total Cost:**  
     ```excel
     =SUM(G4:G62)
     ```  
   - **Max/Min/Average Costs:**  
     ```excel
     =MAX(G4:G62), =MIN(G4:G62), =AVERAGE(G4:G62)
     ```  
   - **Order-Only Totals & Averages:**  
     ```excel
     =SUMIF(F4:F62,"Order",G4:G62)
     =COUNTIF(F4:F62,"Order")
     =AVERAGEIF(F4:F62,"Order",G4:G62)
     ```

5. **Workbook Polish & Best Practices**  
   - Applied **Named Ranges** for inputs and outputs.  
   - Auto-fitted all columns for readability.  
   - Locked formula cells to prevent accidental edits.

---

## 🛠 Technologies & Functions

- **Microsoft Excel 2016+**  
- Key functions: `IF`, `SUM`, `MAX`, `MIN`, `AVERAGE`, `SUMIF`, `COUNTIF`, `AVERAGEIF`, `LEFT`, `RIGHT`, `MID`, `UPPER`, `LOWER`, `PROPER`

# SQL Project One 

## Movie Rental Database — SQL Fundamentals Project

A self-contained SQL project demonstrating core database design, data loading, CRUD operations, joins, aggregations, subqueries, and basic window functions.

---

## 🚀 Project Overview

- **Goal:** Build and explore a “Movie Rental” database for a video store that does not exist.
- **Key Skills:**  
  - Schema design (tables, PK/FK constraints)  
  - Data loading (INSERT or bulk load)  
  - CRUD operations (SELECT, INSERT, UPDATE, DELETE)  
  - Joins & filters  
  - Aggregations (`GROUP BY`, `COUNT`, `AVG`)  
  - Subqueries & basic window functions  

- **schema.sql**  
  - `CREATE TABLE` statements for `customers`, `movies`, `rentals`, and `staff`  
  - Primary keys, foreign keys, and appropriate data types  

- **data-load.sql**  
  - `INSERT` scripts (or `COPY`/`LOAD DATA`) to populate each table with 20–50 sample rows  

- **queries**  
  - **01-basic-selects.sql**: Examples of simple `SELECT` queries (example: customers joined last month)  
  - **02-crud-examples.sql**: Demonstrates `INSERT`, `UPDATE`, `DELETE` operations  
  - **03-joins-and-filters.sql**: Queries combining tables and applying filters (example: overdue rentals)  
  - **04-aggregates.sql**: `GROUP BY` analyses (example: top 3 most-rented movies, average rental duration)  
  - **05-subqueries-window.sql**:  
    - Subquery: customers who rented every “Action” movie  
    - (Optional) Window function: rank movies by rental count
  
---

## 💾 Tech Stack & Tools

- **Database:** SQL Server
- **Client:** SQLQuery
- **Version Control:** Git & GitHub  

---

# SQL Project Two
## E-Commerce Sales & Analytics — SQL Server Project

A relational database for a fictitious online retailer, showcasing schema design, ETL, stored procedures, views, and analytical queries, which were all built in SQL Server and documented for reproducibility.

---

## 🚀 Project Overview

- **Goal:** Implement an end-to-end SQL Server solution to manage orders, inventory, customers, products and promotions, then generate operational and strategic reports.
- **Core Skills:**  
  - Schema design (tables, PK/FK, data types, indexes)  
  - ETL via `BULK INSERT` and staging  
  - T-SQL programming: stored procedures, triggers, user-defined functions, views  
  - Query performance tuning (execution plans, index strategy)  
  - Analytical reporting with window functions and CTEs
 
## 📄 WorkFlow

- **schema.sql**  
  - Defines `Customers`, `Products`, `Orders`, `OrderItems`, `Inventory`, `Suppliers`, and `Promotions`  
  - Sets primary/foreign keys, data types (`DECIMAL`, `DATE`, `VARCHAR`), and clustered/non-clustered indexes  

- **data-load.sql**  
  - Creates staging tables  
  - Loads CSV exports using `BULK INSERT`  
  - Cleans data via CTEs (trimming, type conversions)  

- **tsql/**  
  - **Stored Procedures:**  
    - `usp_PlaceOrder` (inserts order, order items; adjusts inventory; applies promotions)  
    - `usp_AdjustInventory` (adds or deducts stock; logs adjustments)  
  - **User-Defined Function:**  
    - `fn_CustomerLifetimeValue(@CustomerID)` returns cumulative spend  
  - **View:**  
    - `vw_TopSellingProducts` lists top 10 products by units sold last month  
  - **Trigger:**  
    - `trg_PreventNegativeStock` rolls back any inventory update that would drop stock below zero  

- **queries/**  
  - **operational.sql:** everyday operations queries (e.g., unfulfilled orders, low-stock items)  
  - **analytics.sql:** business insights (monthly revenue, customer retention cohorts, promotion performance)  
  - **performance.sql:** scripts to review execution plans and rebuild fragmented indexes

---

## 💾 Tech Stack

- **Database:** Microsoft SQL Server 2017+  
- **Client:** SQL Server Management Studio (SSMS)  
- **Version Control:** Git & GitHub  


