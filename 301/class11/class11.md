# Mongo DB and Mongoose
[Module 301](./301)

Reading assignment for Class 11.

## Questions & Answers

[SQL vs NoSQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/)

1. Fill in the chart below with five differences between SQL and NoSQL databases:

| SQL | NoSQL |
| ---- | ---- |
| Relational Database | Non-Relational Database |
| Table based with `n` number of rows | Document based with `key-value` pairs, graph, or wide column stores |
| Predefined schema | Dynamic schema for unstructured data |
| Vertically scalable | Horizontally scalable |

1. What kind of data is a good fit for an SQL database? Heavy duty transactional type applications
2. Give a real world example. Like an online shopping website.
3. What kind of data a good fit a NoSQL database? Where data isn't perfectly structured like a social media platform where users can post various types of content/data.
4. Which type of database is best for hierarchical data storage? NoSQL
5. Which type of database is best for scalability? depends on vertical or horizontal scalability

--- 

[SQL vs NoSQL (Video)](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y&themeRefresh=1)

1. What does SQL stand for? structured query language 
2. What is a relational database? Type of database that organizes data into tables with rows and columns. Relationships between tables are done through keys.
3. What type of structure does a relational database work with? with a structured data model like SQL
4. What is a 'schema'? structure or blueprint of the data.
5. What is a NOSQL database? Document based with varying ways to structure data.
6. How does it work? data can be based with key-value pairs, graphs, or wide column stores
7. What is inside of a MongoDB? It is a popular NoSQL database, stores data in a format known as BSON (Binary JSON)
8. Which is more flexible - SQL or MongoDB? and why. MongoDB is more flexible as it doesn't need exact defined structured data. You can create schemas to be relative to the type of data the user will be inputing.
9. What is the disadvantage of a NoSQL database? Any disadvantage is only a disadvantage based on context. For a social media application having eventual consistency can allow a user to update information even if their connection has been disconnected. For a bank or healthcare software, data needs to be sync'd up quickly.

## SQL vs NoSQL

### Differences

* SQL databases aka - Relational Databases (RDBMS)
* NoSQL database aka - Non-Relational or Distributed database

---
* SQL databases are *table based* with `n` number of rows
* NoSQL *document based*  with `key-value` pairs, graph, or wide-column stores (no standard schema definitions which needs to be adhered to)

---
* SQL have predefined schema
* NoSQL have dynamic schema for unstructured data

---
* SQL is vertically scalable - hardware buff (CPU, RAM, SSD) on a single server
* NoSQL is horizontally scalable - increase servers

---
* SQL - Structured Query Language - defining and manipulation the data
* NoSQL - focused on collection of documents 
	* Sometimes called UnQL - Unstructured Query Language - syntax does vary

---
* SQL Examples - MySql, Oracle, Sqlite, Postgres and MS-SQL
* NoSQL Examples - MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j, CouchDb

--- 
* SQL is a goof fit for the complex query intensive environment
* NoSQL not a good fit for complex queries

--- 
* SQL is **not** the best fit for hierarchical data storage
* NoSQL fits better for the hierarchical data storage

___
* SQL is best fit for heavy duty transactional type applications as it is more stable and promises the atomicity
	* Atomicity - an operation appears to occur at a single instant between its invocation and its response. It is indivisible and uninterrupted.
* NoSQL *can* be used for transactions purpose, but not comparable or stable enough in high load and for complex transactional applications.

--- 
* SQL has 'excellent' support from vendors or independent consultations who can help with large scale deployments
* NoSQL will have to rely on community support and limited outside experts are available for you to setup and deploy large scale deployments.

---
* SQL emphasizes on ACID properties (Atomicity, Consistency, Isolation, and Durability)
* NoSQL follows Brewers CAP theorem ( Consistency, Availability and Partition tolerance)

___
* SQL is classified as either open-source or close-sourced
* NoSQL is classified on the way data is stored. Graph, key-value, document, column, and XML
