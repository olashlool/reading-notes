# Read: 11 - ERDs

## Data Models 

> Database Schema is like a blueprint of how the database is constructed.

Data annotation attributes can fix the display format. - in the .cs file you can add a using System.ComponentModel.DataAnnotations; statement at the top of the page.

- DataType attribute specifies the data type.

- StringLength sets maximum length.

- RegularExpression- sets restrictions to the input

- MaxLength - similar to StringLength but without client side validation

- using System.ComponentModel.DataAnnotations.Schema

  - this allows the user to use attributes that control how classes and properties are mapped to the database.

## DBMS

DBMS stands for Data Base Management System 

- The advantages of DBMS is using realistic real-world entities in its architecture design.
  - for example in a school database you can use students as an entity.
- It uses relation based tables - This allows a user to understand relationships just be looking at the table names. The school might have a table called students and another called classes.
- Isolation of data and application the systems is different from its data. DBMS also stores metadata which is data about data.
- Normalization - splits a relation when there are redundancy in attribute values.
- Consistency - every relation in the table is consistent
- Query Language - can be used to apply filters when retrieving data.
- multiuser and concurrent access multiple users can access the data at the same time
- multiple views - views can be different based on a user role. Sales will see a views specific to sales and buyer will see a view specific their role.
- Security - DBMS can be compartmentalized so access to sensitive data input and views can be limited by role and permissions.

### 1. Do some research on what a Database Schema is.

- What is a Schema?

> A document that describes the organization and structure of a database.

- Why do we use them?

> Primarily to handle organization/structure of the database as well as establish permissions.

- What do they look like?

> They contain objects like tables, columns, data types, views, stored procedures, relationships, primary keys, foreign keys, etc.

### 2. What are the different types of Database Keys?

- What is a Primary Key?

> A uniquely identified field that is used as a reference for relating tables in the database.

- What is a Foreign Key?

> Non-unique field connected to the primary key of a different table in the same database.

- What is a Composite Key?

> A combination of 2 or more attributes/columns to form a primary key for a table.

- How are they different? When do you use 1 over the others?

> Foreign keys are used to tie two tables together, a primary key is the standard for most tables, it's like an index in an enumerable, it should be used for standard tables that need a simple, unique identifier. Composite keys should be used when two pieces of information are needed to uniquely identify items in a database.

### 3. What are Relationships in a relational database?

- What is a 1:1 relationship?

> A relationship wherein one row of a table is linked to only one row in another table and vice versa, which means it's created using a Primary Key - Unique foreign key relationship.

- What is a Many:Many relationship?

> A relationship wherein a parent row in one table contains several child rows in a second table and vice - versa.

- How about a 1: Many or a Many:1?

> These are a relationship between two tables wherein a row from one table can have several matching rows in another table, it's created using a Primary Key - Foreign key relationship.