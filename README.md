# Customer and DVDs SQL Project

## Table of Contents
- [Project Overview](#project-overview)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [Features](#features)
- [Model Implementation](#model-implementation)
- [Controller Implementation](#controller-implementation)
- [View Implementation](#view-implementation)
- [Styling and Design](#styling-and-design)
- [Running the Application](#running-the-application)
- [Disclaimer](#disclaimer)

## Project Overview
This project demonstrates the creation and management of two SQL Server 2012 databases for a **DATA6212** assessment.  
The databases simulate real-world use cases involving accommodation bookings and DVD store inventory management.  
Each question file showcases advanced SQL concepts such as **joins**, **views**, **stored procedures**, **constraints**, and **aggregate functions**.

**Question 1 (ExamQ1.sql):**  
Implements a booking system for accommodation venues, allowing queries on customers, bookings, and venue statistics.

**Question 2 (ExamQ2.sql):**  
Implements a DVD rental and stock-tracking system, showcasing database normalization, stock aggregation, and availability tracking.

## Technology Stack
- **Database Engine:** Microsoft SQL Server 2012  
- **Language:** Transact-SQL (T-SQL)  
- **Environment:** SQL Server Management Studio (SSMS)  
- **File Format:** `.sql` scripts  
- **Compatibility:** SQL Server 2012 and later  

## Project Structure
```plaintext
customer-and-dvds-sql/
│
├── ExamQ1.sql   # Accommodation Booking Database (Venues and Customers)
├── ExamQ2.sql   # DVD Rental and Availability Database
└── README.md    # Project Documentation
````

## Installation and Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/HChristopherNaoyuki/customer-and-dvds-sql.git
   ```
2. **Open SQL Server Management Studio (SSMS).**
3. **Execute the SQL Scripts:**

   * Run `ExamQ1.sql` to create and populate the accommodation booking database.
   * Run `ExamQ2.sql` to create and populate the DVD store database.
4. **Verify Tables and Data:**

   * Use `SELECT * FROM <table_name>` to confirm table creation and data insertion.

## Features

### ExamQ1.sql — Accommodation Booking System

* Database creation with three related tables: **CUSTOMERS**, **VENUES**, and **ACCOMMODATION_BOOKINGS**.
* Uses **foreign keys** and **composite primary keys** to maintain referential integrity.
* **View (`ExtendedBookings`)** filters long-stay bookings within 2020.
* **Stored Procedure (`FindVenueBookings`)** retrieves all bookings for a specified venue.
* Aggregation queries calculate **total nights booked per venue**.
* **CASE** expressions display booking status for all venues.

### ExamQ2.sql — DVD Store Database

* Database creation with **DVDS**, **STORES**, and **AVAILABILITY** tables.
* Includes composite keys, foreign keys, and relational mappings.
* **ALTER TABLE** and **UPDATE** statements demonstrate schema evolution and data modification.
* Aggregation queries compute **total available stock per DVD**.
* Identifies **DVDs not available in any store** and **top store stock levels**.

## Model Implementation

The **model layer** is represented by SQL table structures:

* **CUSTOMERS**, **VENUES**, and **ACCOMMODATION_BOOKINGS** (for ExamQ1)
* **DVDS**, **STORES**, and **AVAILABILITY** (for ExamQ2)

Each model defines:

* **Primary keys** for unique identification.
* **Foreign keys** for relational integrity.
* **Constraints** to ensure consistent and valid data.

## Controller Implementation

The **controller logic** is embedded in SQL statements that manage data interaction:

* **Stored Procedures** such as `FindVenueBookings` perform parameterized data retrieval.
* **ALTER** and **UPDATE** statements control schema and record updates.
* **Aggregate queries** function as business logic controllers, summarizing booking or inventory data.

## View Implementation

The **views** provide filtered, reusable data perspectives:

* `ExtendedBookings` (ExamQ1) displays customers with extended stays in 2020.
* Query outputs serve as the interface between stored data and user queries.

These views improve readability, abstraction, and reusability.

## Styling and Design

While SQL scripts are not visually styled, the code structure follows professional formatting conventions:

* Consistent use of uppercase for SQL keywords.
* Indentation aligned with logical SQL blocks.
* Inline comments for readability.
* Query sections separated by headings for clarity.

## Running the Application

1. Launch **SQL Server Management Studio (SSMS)**.
2. Connect to a SQL Server instance.
3. Open the `.sql` file (either `ExamQ1.sql` or `ExamQ2.sql`).
4. Execute the script using **Execute (F5)**.
5. Verify the database creation under the **Object Explorer**.
6. Run the final **SELECT** statements to view query outputs.

## Disclaimer

This project was developed for **academic purposes** under the **DATA6212** module.
All code aligns with the SQL Server 2012 programming standards taught in the course.
Unauthorized reproduction or distribution without proper attribution is prohibited.
For educational review and portfolio demonstration only.

---
