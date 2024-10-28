# Definition of DBMS
-->A database-management system ( DBMS ) is a collection of interrelated data and a set of programs to access those data.
--> the DB is a collection of data
-------------------------------------------------------------------------------------------------------------------------------
# there are two modes in which databases are used.
• The ﬁrst mode is to support online transaction processing, where a large number of users use the database, with each user retrieving relatively small amounts of
data, and performing small updates. This is the primary mode of use for the vast majority of users of database applications such as those that we outlined earlier.
• The second mode is to support data analytics, that is, the processing of data to draw conclusions, and infer rules or decision procedures, which are then used to drive business decisions.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
major disadvantages of ﬁle-processing system
1-Data redundancy and inconsistency.         
2-Diﬃculty in accessing data.
3-Data isolation : data are scattered in various ﬁles, and ﬁles may be in different formats so retrieve the appropriate data is diﬃcult.
4-Integrity problems:The data values stored in the database must satisfy certain types of consistency constraints
5-Atomicity problems 
6-Concurrent-access anomalies.: When multiple users or transactions try to access a database simultaneously, issues may arise
7-Security problems.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
data model
--> a collection of conceptual toolsfor describing data, data relationships, data semantics, and consistency constraints

The data models can be classiﬁed into four diﬀerent categories:
1-Relational Model. 
--> The relational model uses a collection of tables to represent both data and the relationships among those data. 
Each table has multiple columns, and each column has a unique name
2-Entity-Relationship Model. 
--> The entity-relationship ( E-R ) data model uses a collection of basic objects,called entities, and relationships among these objects.
3-Semi-structured Data Model.
--> The semi-structured data model permits the speciﬁcation of data where individual data items of the same type may have diﬀerent
sets of attributes.
--> JSON and Extensible Markup Language ( XML ) are widely used semi-structured data representations.
4-Object-Based Data Model. Object-oriented programming (especially in Java, C++,or C#) has become the dominant software-development methodology
