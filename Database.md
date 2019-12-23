# Databases

***

## Relational vs Non-Relational Databases

There are two main types of databases, relational and non-relational. The major difference between them is how they handle data.

Relational databases are structured. You have tables and these tables may have dependencies on each other, or relationships. The most popular ones are Microsoft SQL Server, Oracle, MySQL, MariaDB, PostgreSQL, and Microsoft Azure SQL.

You'll want to use relational databases when you want to enforce atomicity, consistency, isolation and durability. This reduces anomalies and enforces integrity. It is the preferred method for commerce and financial applications. Also, use relational databases if your data structure is not changing. (Or at least, not changing very often.)

Non-relational databases are document-oriented. This allows multiple categories of data to be stored in one construct or document. They are basically huge JSON files. This allows for far more flexibility and adaptability. However, this results in a need for additional processing effort and more storage as the document sizes grow. The most popular ones are MongoDB, Oracle NoSQL, Apache CouchDB, and Redis.

You'll want to use non-relational databases when you are doing rapid application development. They support rapidly changing designs and is perfect for more Agile settings. You'll also want it if you're storing large amounts of data with little to no structure.

***

## Normalization

Normalization is a database design technique that organizes tables in a manner that reduces redundancy and dependency of data.

It divides larger tables to smaller tables and links them using relationships.

Most database systems are normalized up to the third normal forms.

***

## First Normal Form (1NF)

Each table cell should contain a single value.

Each record needs to be unique.

This elimnates repeating groups.

***

## Second Normal Form (2NF)

The tables have to be in first normal form.

The tables must have only one primary key column. 

***

## Third Normal Form (3NF)

The tables have to be in second normal form.

The tables must not have any transitive functional dependencies.

***

## Key

A key is a value used to identify a record in a table uniquely. It could be a single column or combination of multiple columns.

A primary key is a single column value used to identify a database record uniquely. It cannot be null, it must be unique, and it must be given when a new record is inserted.

A composite key is a primary key composed of multiple columns used to identify a record uniquely. For example, we can have a person with the same name but two different addresses, so we would use both the name and address columns to identify them. 

A foreign key references the primary key of another table. It helps connect your tables.

***

## Transitive Functional Dependencies

A transitive functional dependency is when changing a non-key column might cause of the other non-key columns to change.

***

## Entity-Relationship Model

An entity-relationship model is a theoretical and conceptual way of showing data relationships. It is a database modeling technique that generates an abstract diagram or visual representation of a system's data that can be helpful in designing a relational database.

***