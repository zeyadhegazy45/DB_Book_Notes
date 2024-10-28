# some notes 
- in the relational model the term relation is used to refer to a table
- while the term tuple is used to refer to a row. 
- the term attribute refers to a column of a table.
- The null value is aspecial value that signifies that the value is unknown or does not exist.

# the difference between database schema and database instance
1. **database schema:**
-  is the logical design of the database
2. **database instance:**
- is a snapshot of the data in the database at a given instant in time.
# Keys in a Database
1. **Superkey**
- A superkey is a set of one or more attributes that, when combined,can uniquely identify a tuple (row) in a relation (table).
- Any superset of a superkey is also a superkey.
2. **Candidate Key**
- A candidate key is a minimal superkey—a superkey with no redundant attributes.
3. **Primary Key**
- A primary key is one of the candidate keys chosen by the database designer as the main identifier for tuples in the table.
4. **Foreign Key and Referential Integrity**
- A foreign key is an attribute (or a set of attributes) in one table that references the primary key in another table.
- Referencing Relation: The table that contains the foreign key 
- Referenced Relation: The table that contains the primary key being referenced (e.g., department).
  
- **Referential Integrity:**

- Ensures that the value of a foreign key in the referencing relation must exist as a primary key value in the referenced relation.
- Foreign-key constraints are a specific type of referential integrity constraint where the referenced attribute is the primary key.
## Note:
- Most modern database systems support foreign-key constraints, but they do not enforce referential integrity where the referenced attribute is not a primary key.
  
# Relational Algebra
- Relational algebra is a set of operations used to manipulate and query data from relational databases. These operations take one or two relations (tables) as input and produce a new relation as output.

1. **Unary Operations**
- These operations act on a single relation.

1. Select (σ):
- Retrieves rows (tuples) that satisfy a given condition.
- Example: σ(department = 'CS')(instructor) selects all instructors in the 'CS' department.
2. Project (π):
- Retrieves specific columns (attributes) from a relation.
- Example: π(name, salary)(instructor) extracts only the name and salary attributes.
3. Rename (ρ):
- Renames a relation or attributes for easier reference.
- Example: ρ(new_instructor, instructor) renames the instructor relation to new_instructor.
2. **Binary Operations**
- These operations act on two relations.
1. Union (∪):
- Combines two relations and returns all unique rows.
- Example: R ∪ S combines relation R and S.
2. Cartesian Product (×):
- Returns all possible combinations of rows from two relations.
- Example: R × S pairs every row in R with every row in S.
3. Set Difference (-):
- Returns rows that appear in one relation but not in the other.
- Example: R - S returns rows present in R but not in S.
