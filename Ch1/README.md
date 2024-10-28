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
 3-**Data Isolation:**
- Data scattered across multiple files and formats makes access and management difficult.
4-**Integrity Problems:**
- Data must meet certain consistency rules, but enforcing them is difficult in scattered systems.
5-**Atomicity Issues:**
- Ensuring complete success or failure (all-or-nothing) in data operations is challenging.
6-**Concurrent-Access Anomalies:**
- Multiple users accessing or modifying data simultaneously can lead to conflicts.
7-**Security Problems:**
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
2- **Entity-Relationship (E-R) Model:**
- Uses entities (objects) and relationships between them to represent data.
- Often used in database design for conceptual modeling.
3-**Semi-Structured Data Model:**
- Allows data items of the same type to have varying attributes.
- Common formats: JSON and XML.
4-**Object-Based Data Model:**
- Based on object-oriented programming concepts (e.g., Java, C++, C#).
- Integrates data with the methods that manipulate them, often used in object-oriented databases.

