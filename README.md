# healthcare-financial-modeling
A PostgreSQL-based analytical framework for managing hospital operations and revenue cycles. This project models the relationship between patient care (appointments, diagnoses, medications) and financial outcomes (billing, insurance coverage, and provider revenue ranking).

To make your repository stand out to recruiters and back up the **"Financial Data Modeling"** claim on your CV, your README should focus on the business value of your SQL logic.

Copy and paste the following into a file named `README.md` in your repository.

---

# Healthcare Financial Modeling & Analytics (PostgreSQL)

## 📋 Project Overview
This repository contains a comprehensive relational database schema and a suite of advanced analytical queries designed for a **Healthcare Management System**. The project focuses on the intersection of clinical operations and financial performance, modeling how patient treatments, provider actions, and insurance payouts impact the revenue cycle.

**Key Focus Areas:**
* **Relational Data Modeling:** Designing structured tables for patients, providers, and clinical events.
* **Revenue Cycle Analytics:** Ranking provider performance and identifying insurance coverage gaps.
* **Operational Intelligence:** Analyzing peak clinic hours and patient no-show rates.

---

## 🏗️ Data Architecture
The database is built on a relational star-like schema to ensure data integrity and query efficiency. It consists of six core tables:

* **`patients`**: Demographic and insurance provider data.
* **`doctors`**: Provider specialties and clinic locations.
* **`appointments`**: The central fact table linking patients and doctors.
* **`billing`**: Financial records, including total amounts and insurance portions.
* **`diagnosis`**: Clinical assessments using ICD-10 style coding.
* **`medications`**: Prescriptions, dosages, and treatment timelines.

---

## 🚀 Technical Highlights
The analytical suite (`database_schema_and_analytics.sql`) utilizes advanced PostgreSQL features to drive insights:

* **Window Functions:** Used `RANK()` to identify top-performing doctors by revenue and `LEAD()` to project future patient visits.
* **Common Table Expressions (CTEs):** Employed for complex, multi-step calculations such as identifying doctors with above-average appointment rates.
* **Data Normalization & Type Casting:** Cleaned and transformed raw string data (e.g., extracting numeric values from "50mg" strings) for mathematical analysis.
* **Conditional Logic:** Used `CASE` statements for age-group bucketization and peak-day identification.

---

## 📊 Key Business Insights Generated

### 1. Financial Performance
* **Provider Ranking:** Identified top revenue-generating doctors to assist in performance reviews.
* **Insurance Audit:** Flagged cases where insurance covered less than 70% of the bill, highlighting potential financial risk for patients.

### 2. Clinical Operations
* **Capacity Planning:** Determined peak days of the week for appointments to optimize staffing.
* **No-Show Analysis:** Identified providers with high no-show rates to improve scheduling efficiency.
* **Chronic Disease Tracking:** Isolated patient populations for specific conditions (Hypertension, Diabetes) based on ICD codes and medication history.

---

## 🛠️ How to Use
1.  **Environment:** Ensure you have a PostgreSQL instance running.
2.  **Setup:** Run the first section of `database_schema_and_analytics.sql` to create the tables.
3.  **Analysis:** Execute the queries in the second section to generate the operational and financial reports.

---

## 📈 Future Enhancements
* Implementation of **Indexes** on `patient_id` and `appointment_date` to optimize query speed for larger datasets.
* Integration of a **View** layer for real-time financial dashboarding.
* Addition of a `procedure_logs` table to track specific medical actions vs. billing codes.

---

### Author
**[Your Name]**
*Financial Data Modeler | SQL Developer*
