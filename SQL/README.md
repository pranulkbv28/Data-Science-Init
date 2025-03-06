# Intro to SQL

## Database

- What is a database?
  - It is essentially a place where we can store `data`.

- Why do we need DB?
  - Data Organisation
  - Data Integrity
  - Efficient Data Retrieval
  - Scalability
  - Data Security

### Types of Databases

- Hierarchial Databases
- Relational Databases
- NoSQL Databases
- Network Databses
- Object Oriented Databases
- Cloud Databases
- Centralised Databases
- Operational Databases

## Our Objective

We will be working mainly on `Relational Databases`.

### What is a Relational Database?

- It is a database which will be storing our data in a `tabular structure`.
- The info will be stored in `rows` and `columns`.

### RDBMS vs DBMS

- Data Structure
- Data Relationships
- Data Integrity & Normalisation
- `ACID` Compliance
- Query Language

### What is SQL

- It is called as `Structred Query Language`.
- It is a platform to access our database and communicate with as well.

#### Types of Codes in SQL

- **DML** -> Data Manipulation Language
- **DDL** -> Data Definition Language
- **DCL** -> Data Control Language
- **TCL** -> Transaction Control Language
- **DQL** -> Data Query Language

#### Types of Relationships

- One to One -> `One` PK of Table1 will have `exactly` one row present in Table 2.
- One to Many -> `One` PK of Table1 will have `multiple` rows present in Table 2.
- Many to One -> `One` PK of Table2 will have `multiple` rows present in Table 1.
- Many to Many -> `Multiple` PK of Table1 and Table2 will have `multiple` rows present in both the tables.

#### Normalisation

- Unique Rows (Avoid Redundancy)
- PK is of utmost importance
- FK is to be used for relations

#### Types of Keys in Database

- **Primary Key (PK)** -> Column in which every row can be `uniquely` identified
- **Composite Key** -> Combination of 2 or more columns that act as PK
- **Candidate Key** -> The individual columns of a `Composite Key` are called `Candidate Keys`
- **Foreign Key (FK)** -> It is the `linkage` between two or more tables

#### Basic Querying Techniques in SQL

1. SELECT -> followed by the columns that you want to display -- **Mandatory** --
2. FROM -> followr=ed by the table name -- **Mandatory** --
3. WHERE -> followed by the conditions -- **Optional** --
4. GROUP BY -> followed by how you want to group or aggregate the items -- **Optional** --
5. HAVING -> if there are any further filters that we want to apply on `GROUP BY`, we can use this -- **Optional** --
6. ORDER BY -> follwed by the column name or number -- **Optional** --
7. LIMIT -> followed by the number of rows you want to see -- **Optional** --

- Examples

```SQL
SELECT EmpName, Age, Salary FROM Employee WHERE Salary > 10000 ORDER BY Salary /* This sorts the output based on the Salary column */
```

```SQL
CREATE TABLE Products (
    Product_Id INT PRIMARY KEY,
    URI VARCHAR(255),
    Brand_Name VARCHAR(100),
    Category VARCHAR(50),
    Individual_Category varchar(50),
    Category_by_Gender varchar(20),
    Description TEXT,
    DiscountPrice Decimal (10, 2), /* This lets us insert a value where in, there are 2 places after the decimal and 10 places before */
    OriginalPrice decimal (10, 2),
    DiscountOffer varchar (10),
    SizeOption varchar (50),
    Ratings DECIMAL (3, 2),
    Reviews int
); -- this is used to create a table named Products with these columns

-- Adding columns after creation
ALTER TABLE Products ADD Stock INT;

-- Delete a Table
drop table Products;

-- Insert records into the table
INSERT INTO Products (Product_Id, URI, Brand_Name, Category, Individual_Category, Category_by_Gender, Description, DiscountPrice, OriginalPrice, DiscountOffer, SizeOption, Ratings, Reviews, Stock)
VALUES
(1, 'http://expample.com/product1', 'BrandX', 'Electronics', 'Latops', 'Unisex', 'High Performance Laptop')
```
