# Exp 9 Implementation of ROLLUP in SQL.
## AIM:
To write a sql query to perform ROLLUP in SQL.
## PROCEDURE:
### STEP 1:
create database ROLLUP_OPERATION  .
### STEP 2:
create table Employees.
### STEP 3:
Insert Value to the table.
### STEP 4:
Perform ROLLUP on Employees table.
## PROGRAM:
```sql
CREATE DATABASE ROLLUP_OPERATION;
USE ROLLUP_OPERATION;

CREATE TABLE Employees (
  ID INT PRIMARY KEY,
  FirstName VARCHAR(50),
  LastName VARCHAR(50),
  Salary DECIMAL(10, 2),
  Department VARCHAR(50)
);

INSERT INTO Employees (ID, FirstName, LastName, Salary, Department) VALUES
(1, 'John', 'Doe', 50000.00, 'HR'),
(2, 'Jane', 'Smith', 60000.00, 'Finance'),
(3, 'Michael', 'Johnson', 75000.00, 'IT'),
(4, 'Emily', 'Davis', 55000.00, 'Marketing'),
(5, 'David', 'Brown', 70000.00, 'Finance');

SELECT Department, FirstName, LastName, SUM(Salary) AS TotalSalary
FROM Employees
GROUP BY Department, FirstName, LastName WITH ROLLUP;
```
## OUTPUT:
![image](https://github.com/Karthikeyan21001828/DBMS_EX09/assets/93427303/c165f7b1-db82-478a-8d8b-2f8ad397a130)

## RESULT:
A sql query to perform ROLLUP in sql has been executed.
