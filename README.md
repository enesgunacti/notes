# T-SQL README

## Contents
1. [Creating Tables](#creating-tables)
2. [Inserting Data](#inserting-data)
3. [SELECT Statement](#select-statement)
4. [INSERT Statement](#insert-statement)
5. [UPDATE Statement](#update-statement)
6. [DELETE Statement](#delete-statement)
7. [WHERE Clause](#where-clause)
8. [ORDER BY Clause](#order-by-clause)
9. [GROUP BY Clause](#group-by-clause)
10. [HAVING Clause](#having-clause)

## Creating Tables
First, we will create two tables: `Departments` and `Employees`.

```sql
CREATE TABLE Departments (
    DepartmentID INT PRIMARY KEY,
    DepartmentName NVARCHAR(50)
);

CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName NVARCHAR(50),
    LastName NVARCHAR(50),
    DepartmentID INT,
    Salary DECIMAL(10, 2),
    FOREIGN KEY (DepartmentID) REFERENCES Departments(DepartmentID)
);
```

## Inserting Data

Next, we will insert data into these tables.

```sql
INSERT INTO Departments (DepartmentID, DepartmentName)
VALUES (1, 'Sales'), (2, 'Marketing'), (3, 'HR'), (4, 'IT');

INSERT INTO Employees (EmployeeID, FirstName, LastName, DepartmentID, Salary)
VALUES
(101, 'John', 'Doe', 1, 50000),
(102, 'Jane', 'Smith', 2, 60000),
(103, 'Michael', 'Johnson', 3, 55000),
(104, 'Patricia', 'Brown', 4, 70000),
(105, 'Linda', 'Davis', 1, 65000),
(106, 'Robert', 'Miller', 2, 72000),
(107, 'William', 'Wilson', 3, 48000),
(108, 'Elizabeth', 'Moore', 4, 62000);
```

## SELECT Statement

Used to query data from the database.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

Example : 
```sql
SELECT FirstName, LastName
FROM Employees
WHERE DepartmentID = 1;
```

## INSERT Statement

Used to insert new records into a table.

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

Example : 
```sql
INSERT INTO Employees (EmployeeID, FirstName, LastName, DepartmentID, Salary)
VALUES (109, 'George', 'Clark', 1, 55000);
```

## UPDATE Statement

Used to modify existing records in a table.

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

Example : 

```sql
UPDATE Employees
SET Salary = 68000
WHERE EmployeeID = 105;
```

## DELETE Statement

Used to delete records from a table.

```sql
DELETE FROM table_name
WHERE condition;
```

Example : 

```sql
DELETE FROM Employees
WHERE EmployeeID = 107;
```

## WHERE Clause

Used to filter records based on specified conditions.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

Example : 

```sql
SELECT FirstName, LastName
FROM Employees
WHERE DepartmentID = 2;
```

## ORDER BY Clause

Used to sort the result set in ascending or descending order.

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC], column2 [ASC|DESC], ...;
```

Example : 

```sql
SELECT FirstName, LastName, Salary
FROM Employees
ORDER BY Salary DESC, FirstName ASC;
```

## GROUP BY Clause

Used to group rows that have the same values into summary rows, often used with aggregate functions.

```sql
SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1;
```

Example : 

```sql
SELECT DepartmentID, COUNT(*)
FROM Employees
GROUP BY DepartmentID;
```

## HAVING Clause

Used to filter records after a GROUP BY is applied.

```sql
SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1
HAVING condition;
```

Example : 

```sql
SELECT DepartmentID, COUNT(*)
FROM Employees
GROUP BY DepartmentID
HAVING COUNT(*) > 1;
```


This README provides a basic overview of essential T-SQL commands and clauses. For more detailed information, please refer to the official T-SQL documentation. 

[Microsoft T-SQL Documentation](https://learn.microsoft.com/en-us/sql/t-sql/language-reference?view=sql-server-ver16)


[W3Schools SQL Tutorial](https://www.w3schools.com/sql/sql_intro.asp)
