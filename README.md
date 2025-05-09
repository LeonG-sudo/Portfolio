# School Work Experience Portfolio

## Student Loans Analytics — Access Database Project

**Quill Financial Services** | Academic Project (Aug 2019)

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

**Quill Financial Services** | Academic Project (Apr 2023)

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
