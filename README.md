University Library Management System
Database (MySQL/Oracle/SQL Server) Course - Final Assignment

📋 Assignment Overview
This project represents the final assignment for the Database course, focusing on the development and implementation of a fully functional University Library Management System. Oracle Database has been used as the primary RDBMS platform to meet all specified requirements. The project reflects the culmination of concepts taught throughout the course and applies real-world database practices in a university setting.

Assignment Objectives
The primary aim of this assignment is to demonstrate proficiency in designing and implementing a robust database system for managing university library operations. It showcases my understanding of normalization principles, relational database theory, and practical implementation using complex SQL queries and PL/SQL programming. Additionally, it highlights my knowledge of database security mechanisms and performance optimization strategies.

Learning Outcomes Achieved
Throughout the completion of this assignment, I have effectively applied ER modeling and normalization techniques to design the system. I have demonstrated SQL proficiency across DML, DDL, DCL, and TCL operations. Moreover, I implemented PL/SQL code—including procedures, functions, and triggers—to support business logic. I also undertook essential database administration tasks such as user management and query optimization.

🎓 Assignment Parts Completed
Part 1: Database Design & Setup (15 Marks)
In this phase, I created all essential tables—BOOKS, MEMBERS, and TRANSACTIONS—ensuring appropriate constraints were applied. Sample data, including 20 books, 15 members, and 25 transactions, were inserted for testing and demonstration purposes.

Part 2: Basic SQL Operations (20 Marks)
I developed various SQL queries for data retrieval such as identifying available books, overdue members, and frequently borrowed books. Data manipulation queries were also written to update fines, add members, and archive old transactions.

Part 3: Advanced SQL Queries (25 Marks)
This section includes join operations (INNER, LEFT, SELF, and CROSS JOINs), subqueries, and advanced query constructs using aggregate and window functions. These queries offer insights like identifying top users and borrowing trends.

Part 4: PL/SQL Programming (25 Marks)
Three core PL/SQL components were developed: the ISSUE_BOOK procedure, CALCULATE_FINE function, and a trigger that updates the book inventory upon return. These automate critical library processes and enforce data integrity.

Part 5: Database Administration (15 Marks)
This part involved the creation of user roles such as librarian and student_user with defined privileges. I also implemented performance improvements using indexing and analyzed execution plans for optimization.

🛠️ Technologies Used
Component	Technology
Database	Oracle Database
Query Language	SQL (DML, DDL, DCL, TCL)
Procedural Language	PL/SQL
Administration	Oracle DB Tools

⭐ Key Features
1. Comprehensive Data Management
Books Management includes tracking title, author, publisher, ISBN, category classification, and inventory status. It ensures real-time monitoring of available copies.

Member Management supports multiple user types—students, faculty, and staff—and stores detailed contact information. Membership types and statuses are also maintained.

Transaction Management allows full tracking of borrow and return operations, including dates and fine status. It provides a clear audit trail for all activity.

2. Advanced Querying Capabilities
Data Retrieval includes book availability, overdue items, top-borrowed analytics, and activity summaries.

Data Manipulation features automated updates for fines, new member onboarding, and historical archiving.

Join Operations support detailed reports through INNER, LEFT, SELF, and CROSS JOINs across tables.

Subqueries help in identifying patterns such as most active users or those incurring high fines.

Analytics & Reporting employs aggregate functions and window operations for meaningful insights into library usage.

3. PL/SQL Automation & Business Logic
ISSUE_BOOK Procedure automates the issuance process by validating availability, inserting transactions, updating inventory, and handling errors.

CALCULATE_FINE Function accepts a transaction ID and dynamically calculates overdue fines using a daily rate model.

UPDATE_AVAILABLE_COPIES Trigger ensures real-time adjustment of the inventory when books are returned.

4. Database Administration
Security and User Management involves role-based access control where librarians have full privileges and student_users have limited read access.

Performance Optimization is achieved through strategic indexing, query tuning, and use of execution plans to improve response time and scalability.

📁 Assignment Submission Structure
pgsql
Copy
Edit
oracle-library-system-[student-id]/
│
├── README.md                 → This documentation file
│
└── sql/
    ├── setup.sql            → Part 1: DDL, table creation, sample data
    ├── queries.sql          → Part 2 & 3: All required queries with comments
    ├── plsql.sql            → Part 4: Procedures, functions, triggers
    └── admin.sql            → Part 5: User management & performance tuning
File Descriptions
setup.sql includes schema creation, constraints, and sample data insertions with defined primary/foreign keys.

queries.sql features all task-related SQL queries, each well-documented with purpose and output expectations.

plsql.sql holds PL/SQL code for stored procedures, functions, and triggers—complete with parameter and logic documentation.

admin.sql contains scripts for user role creation, privilege management, indexing, and general administration commands.

🚀 How to Run
Connect to Oracle Database
Use the following format to connect:
sqlplus username/password@database

Execute files in order:

less
Copy
Edit
@sql/setup.sql    -- Creates tables and inserts sample data  
@sql/queries.sql  -- Executes all SQL queries  
@sql/plsql.sql    -- Creates procedures, functions, triggers  
@sql/admin.sql    -- Performs user and performance configuration  
📊 Database Schema
Tables Created
BOOKS – Includes book_id, title, author, publisher, publication_year, ISBN, category, total_copies, available_copies, and price.

MEMBERS – Stores member_id, full name, email, phone, address, membership info, and type.

TRANSACTIONS – Tracks each borrowing activity with transaction_id, member_id, book_id, issue and return dates, fines, and status.

📝 Assignment Requirements
Sample Data
The system contains:

20 books from various categories

15 members representing different user types

25 transactions including returned, overdue, and pending entries

Key Queries Implemented
Some notable queries include:

Identifying books with available copies fewer than total

Finding members with overdue books

Listing top 5 most borrowed titles

Detecting members who frequently return books late

Calculating overdue fines at ₹5 per day

PL/SQL Components
ISSUE_BOOK: A stored procedure handling book issuance with validations

CALCULATE_FINE: A function returning calculated fines for delayed returns

A trigger that updates available book count upon book return

User Management
librarian role: Full privileges on all data and operations

student_user role: Read-only access to the BOOKS table
