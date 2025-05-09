# School Work Experience Portfolio

# Student Loans Analytics — Access Database Project

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
2. Open `MOS19_AC_PROJ2_Student_Loans.accdb` in Access.  
3. Review tables, queries, forms, and reports as per the instructions.  

---

### 📸 Screenshots

<p float="left">
  <img src="[screenshots/payment_query_result.png](https://github.com/user-attachments/assets/8b2b872b-a931-4b7f-9b89-d6c96e8a06c3)" width="200" /> 
  <img src="[screenshots/loan_summary_report.png" width="200](https://github.com/user-attachments/assets/82e6c469-5ae5-4e87-bc32-9ae0f4ceed0a)" />
</p>

---

### ⚡️ Key Takeaways

- Solidified relational-database design and data-integrity best practices.  
- Automated financial calculations via Access queries.  
- Delivered polished, print-ready reports for stakeholders.


## Excel Project One
