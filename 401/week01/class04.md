# Data Modeling

Reading assignment 'Read 04'

## Questions & Answers

[nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

1. What type of database is the best fit for the complex query intensive environment?
        SQL
2. What type of database is the best fit for hierarchical data storage?
        NoSQL
3. Describe the differences in scalability between a SQL and NoSQL database as though
you were speaking to a non-technical friend?
        SQL is vertically scalable, meaning you would have to upgrade the hardware,
        inside the server, to increase performance. NoSQL is horizontally scalable,
        meaning you can add more servers to your NoSQL database to increase
        performance.

---

[sql modeling techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)

1. Among data tables, what is a one-to-many relationship and how do we 'relate' them?
        A one-to-many relationship is when one record in a table can be associated
        with one or more records in another table.
2. Prior to designing your relational database, it might be useful to ___ a __
of the database tables and their relationships.
        create a diagram
3. Explain the difference between a primary and foreign key.
        A primary key is a unique identifier for a record in a table. A foreign
        key is a field in a table that is the primary key in another table.

---

[sql vs nosql (Video)](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

1. How do we treat keywords and parameters differently in SQL syntax?
        Keywords are used to perform operations on the database, while parameters
        are used to filter the results of a query.
2. Define normalization with the context of schemas and data.
        Normalization, in this context, is the process of organizing a database
        to reduce redundancy and improve data integrity.
3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships
to a non-technical recruiter.
        1:1 - One record in a table is associated with one record in another table
        1:M - One record in a table is associated with one or more records in another
        table
        M:M - Multiple records in a table are associated with multiple records in
        another table

---

## Reflection

1. What are you learning goals after reading and reviewing the class [README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-04/)?

I think working with SQL seems like it will be useful in a career setting. I am
looking forward to learning about how to model data and how to use SQL to interact
with that data.
