# Database Management System (DBMS)

A Database Management System (DBMS) is a collection of interrelated data and a set of programs to access and manage that data.
A database (DB) is a structured collection of data.

# Modes of Database Usage

Databases are used in two primary modes:
- 1-Online Transaction Processing (OLTP):
- Supports a large number of users accessing small amounts of data.
- Users perform frequent, small updates and queries (e.g., e-commerce transactions, banking applications).
- This is the most common mode for most database applications.
- 2-Data Analytics (OLAP):
- Focuses on analyzing data to derive insights, patterns, and business rules.
- Used for making strategic decisions based on trends or predictions (e.g., business intelligence, market analysis).

# Major Disadvantages of File-Processing Systems

1. **Data Redundancy and Inconsistency:**
- Data duplication across files can lead to inconsistency.
2. **Difficulty in Accessing Data:**
- Retrieving data efficiently becomes complex without proper indexing or structure.
3. **Data Isolation:**
- Data scattered across multiple files and formats makes access and management difficult.
4. **Integrity Problems:**
- Data must meet certain consistency rules, but enforcing them is difficult in scattered systems.
5. **Atomicity Issues:**
- Ensuring complete success or failure (all-or-nothing) in data operations is challenging.
6. **Concurrent-Access Anomalies:**
- Multiple users accessing or modifying data simultaneously can lead to conflicts.
7. **Security Problems:**
- Managing permissions and securing data is harder in unstructured systems.

# Data Models
A data model is a collection of tools for describing:
Data structure ,
Data relationships,
Data semantics ,
Consistency constraints

# Types of Data Models
1. **Relational Model:**
- Represents data and their relationships using tables (relations).
- Each table consists of multiple columns with unique names.
- Example: SQL databases like MySQL, PostgreSQL.
2. **Entity-Relationship (E-R) Model:**
- Uses entities (objects) and relationships between them to represent data.
- Often used in database design for conceptual modeling.
3. **Semi-Structured Data Model:**
- Allows data items of the same type to have varying attributes.
- Common formats: JSON and XML.
4. **Object-Based Data Model:**
- Based on object-oriented programming concepts (e.g., Java, C++, C#).
- Integrates data with the methods that manipulate them, often used in object-oriented databases.

# we have several types of abstraction 
 1. **Physical level.**
-  The lowest level of abstraction describes how the data are actually stored.
-  The physical level describes complex low-level data structures in detail
2. **Logical level.**
-  The next-higher level of abstraction describes what data are stored in the database, and what relationships exist among those data.
3. **View level.**
- The highest level of abstraction, showing only specific parts of the database to different users.
- It helps ensure security by providing limited access to the relevant data (e.g., employees can view only their department data).

# Integrity Constraints in Database Systems
- Databases use integrity constraints to ensure data is valid and consistent.
- Only constraints with minimal overhead are typically implemented:

1. **Domain Constraints:**
- Every attribute (column) must follow a specific data type, such as integers, text, or dates.
- Example: A “Birth Year” column must only contain numbers.
2. **Referential Integrity:**
- Ensures that a value in one table must exist in another related table.
- Example: If a course references a department, that department must already exist in the university’s department table.
- If the relationship is broken (like deleting a department), the database blocks the action to avoid inconsistency.
3. **Authorization:**
- Controls what different users can do with the data (read, write, modify, or delete).
- Example: A student may view their grades but not modify them, while an admin has full access.

#  Storage Manager
-The storage manager is the component of a database system that provides the interface
 between the low-level data stored in the database and the application programs and
 queries submitted to the system.

 #Components of the Storage Manager

 1. **Authorization and Integrity Manager:**
- Verifies user permissions to access data.
- Ensures data follows integrity constraints.
2. **Transaction Manager:**
- Keeps the database in a consistent state, even in case of system failures.
- Manages concurrent transactions to avoid conflicts between users.
3. **File Manager:**
-Allocates space on the disk for data storage.
- Manages the structure of data on disk.
4. **Buffer Manager:**
-Fetches data from the disk into main memory.
- Decides what data to keep in memory for quick access, enabling the database to manage more data than the size of available memory.

#Data Structures in the Storage Manager
1. **Data Files:**
- Store the actual data of the database.
- This includes all the records and tables used by the system.
2. **Data Dictionary:**
- Stores metadata about the database, such as the schema (structure of tables, attributes, and relationships).
- Acts like a guidebook for how the data is organized and accessed.
3. **Indices:**
- Provide fast access to specific data items by acting as pointers to relevant records.

#Database Architecture
1. **Centralized Architecture:**
All data and processing are managed on a single server or computer system.
Users access the database through a network, but the entire database resides in one place.

2. **Parallel Architecture:**
- Uses multiple processors or servers working together to manage large databases efficiently.
- Data and queries are divided into smaller parts, processed simultaneously.

3. **Distributed Architecture:**
- The database is spread across multiple locations (servers or data centers).
- Each site can store and manage part of the data, but they work together to present a unified view to users.
